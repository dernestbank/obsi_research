
4/05/2025 
Documentation here [[PEM model docs]]

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.integrate import solve_ivp
from scipy.optimize import curve_fit

# ====================================================
# 1. PEM Electrolyser Model (Electrochemical Module)
# ====================================================
class PEMElectrolyzer:
    def __init__(self, area=1.0, T=298, 
                 E0=1.23,         # Standard reversible voltage (V)
                 t_mem=50e-6,     # Membrane thickness (m)
                 k_mem=0.1,       # Membrane ionic conductivity (S/m)
                 i0_anode=1e4,    # Anode exchange current density (A/m²)
                 i0_cath=1,       # Cathode exchange current density (A/m²)
                 alpha=0.5,       # Charge transfer coefficient
                 i_lim=800        # Limiting current density (A/m²)
                ):
        self.area = area
        self.T = T
        self.E0 = E0
        self.t_mem = t_mem
        self.k_mem = k_mem
        self.i0_anode = i0_anode
        self.i0_cath = i0_cath
        self.alpha = alpha
        self.i_lim = i_lim

    def nernst_voltage(self, p_H2=1.0, p_O2=1.0, a_H2O=1.0):
        # Nernst equation (Eq. (1))
        return self.E0 + (8.314 * self.T) / (2 * 96485) * np.log((p_H2 * np.sqrt(p_O2)) / a_H2O)

    def activation_overpotential(self, i, i0, electrode='cathode'):
        # For the anode, assume a minimal kinetic loss; for the cathode use a Tafel approximation.
        if electrode.lower() == 'anode':
            return 0.005  # small fixed drop (V)
        return (8.314 * self.T) / (self.alpha * 96485) * np.log(i / i0)

    def ohmic_loss(self, i):
        # Ohmic loss: η_ohm = i * t_mem / k_mem
        return i * self.t_mem / self.k_mem

    def conc_overpotential(self, i):
        # Concentration overpotential: η_conc = - (RT/(2F)) * ln(1 - i/i_lim)
        if i >= self.i_lim:
            i = 0.9999 * self.i_lim  # Avoid singularity near i_lim
        return - (8.314 * self.T) / (2 * 96485) * np.log(1 - i / self.i_lim)

    def cell_voltage(self, i, p_H2=1.0, p_O2=1.0, a_H2O=1.0):
        """
        Overall cell voltage:
            V_cell = E_rev - (η_act,anode + η_act,cathode + η_ohm + η_conc)
        """
        E_rev = self.nernst_voltage(p_H2, p_O2, a_H2O)
        eta_act_anode = self.activation_overpotential(i, self.i0_anode, electrode='anode')
        eta_act_cath = self.activation_overpotential(i, self.i0_cath, electrode='cathode')
        eta_ohm = self.ohmic_loss(i)
        eta_conc = self.conc_overpotential(i)
        return E_rev - (eta_act_anode + eta_act_cath + eta_ohm + eta_conc)

    def simulate_polarization_curve(self, i_range, p_H2=1.0, p_O2=1.0, a_H2O=1.0):
        # Returns an array of cell voltages for the given current density range.
        return np.array([self.cell_voltage(i, p_H2, p_O2, a_H2O) for i in i_range])

# ====================================================
# 2. Thermal Dynamics and Water Management Module
# ====================================================
def cell_voltage_for_thermo(i, T, E0, p_H2, p_O2, a_H2O, i0_anode, i0_cath, alpha, t_mem, k_mem, i_lim):
    """
    Standalone version of the cell voltage calculation for the thermal ODE.
    """
    E_rev = E0 + (8.314 * T) / (2 * 96485) * np.log((p_H2 * np.sqrt(p_O2)) / a_H2O)
    eta_act_anode = 0.005  # Assumed fixed small drop for the fast anode reaction
    eta_act_cath = (8.314 * T) / (alpha * 96485) * np.log(i / i0_cath)
    eta_ohm = i * (t_mem / k_mem)
    if i >= i_lim:
        i_eff = 0.9999 * i_lim
    else:
        i_eff = i
    eta_conc = - (8.314 * T) / (2 * 96485) * np.log(1 - i_eff / i_lim)
    return E_rev - (eta_act_anode + eta_act_cath + eta_ohm + eta_conc)

def odes(t, y, params):
    """
    ODE system for temperature T (K) and membrane water content λ (dimensionless).
    
    Energy balance (Eq. (14)-(15)):
       m C_p dT/dt = Q_gen - Q_loss
       where Q_gen = I*(ΔH/(2F) - V_cell) + I² * R_eq, and Q_loss = h*(T - T_amb)
    
    Water balance:
       dλ/dt = n_d*i/(F*t_mem) - (D_w/(t_mem²))*(λ - λ_eq)
    """
    T = y[0]
    lam = y[1]
    
    # Unpack parameters:
    A = params['A']             # Active area (m²)
    t_mem = params['t_mem']     # Membrane thickness (m)
    k_mem = params['k_mem']     # Membrane conductivity (S/m)
    E0 = params['E0']           # Standard voltage (V)
    p_H2 = params['p_H2']       # H2 partial pressure (atm)
    p_O2 = params['p_O2']       # O2 partial pressure (atm)
    a_H2O = params['a_H2O']     # Water activity (≈1)
    i0_anode = params['i0_anode']   # Anode exchange current density (A/m²)
    i0_cath = params['i0_cath']     # Cathode exchange current density (A/m²)
    alpha = params['alpha']         # Charge transfer coefficient
    i = params['i']                 # Current density (A/m²)
    i_lim = params['i_lim']         # Limiting current density (A/m²)
    
    m_cell = params['m_cell']       # Effective cell mass (kg)
    C_p = params['C_p']             # Specific heat capacity (J/(kg*K))
    h = params['h']                 # Cooling coefficient (W/K)
    T_amb = params['T_amb']         # Ambient temperature (K)
    deltaH = params['deltaH']       # Reaction enthalpy (J/mol)
    R_eq = t_mem / k_mem            # Effective ohmic resistance (Ω·m²)
    
    n_d = params['n_d']             # Electro-osmotic drag coefficient (water molecules/proton)
    D_w = params['D_w']             # Water diffusivity in the membrane (m²/s)
    lam_eq = params['lam_eq']       # Equilibrium water content
    
    I_total = i * A  # Total current (A)
    V_cell = cell_voltage_for_thermo(i, T, E0, p_H2, p_O2, a_H2O, i0_anode, i0_cath, alpha, t_mem, k_mem, i_lim)
    
    # Heat generation (W)
    Q_gen = I_total * (deltaH/(2*96485) - V_cell) + (I_total**2) * R_eq
    # Heat loss (W)
    Q_loss = h * (T - T_amb)
    
    dT_dt = (Q_gen - Q_loss) / (m_cell * C_p)
    dlam_dt = n_d * i / (96485 * t_mem) - (D_w / (t_mem**2)) * (lam - lam_eq)
    
    return [dT_dt, dlam_dt]

# ====================================================
# 3. Mass Transport Module (Finite-Difference Approach)
# ====================================================
# Define the 1D domain (through thickness of electrode)
L_GDL = 100e-6    # Thickness of Gas Diffusion Layer (m)
L_CL  = 20e-6     # Thickness of Catalyst Layer (m)
L_total = L_GDL + L_CL

N = 50                          # Number of spatial nodes
x_space = np.linspace(0, L_total, N)
dx = x_space[1] - x_space[0]

# GDL properties:
epsilon_GDL = 0.7               # Porosity
tau_GDL = 2.0                   # Tortuosity
D_O2_air = 2e-5                 # Bulk oxygen diffusivity in air (m²/s)
D_eff_GDL = epsilon_GDL * D_O2_air / tau_GDL  # Effective diffusivity in GDL

# Catalyst Layer (CL) properties:
epsilon_CL = 0.4                # Porosity
tau_CL = 2.5                    # Tortuosity
D_O2_CL = 1e-5                  # Bulk oxygen diffusivity in CL (m²/s)
D_eff_CL = epsilon_CL * D_O2_CL / tau_CL       # Effective diffusivity in CL

# Set spatially varying properties:
epsilon_arr = np.zeros_like(x_space)
D_eff_arr = np.zeros_like(x_space)
for i, xi in enumerate(x_space):
    if xi < L_GDL:
        epsilon_arr[i] = epsilon_GDL
        D_eff_arr[i]   = D_eff_GDL
    else:
        epsilon_arr[i] = epsilon_CL
        D_eff_arr[i]   = D_eff_CL

# Reaction parameters in the catalyst layer:
k_react = 1e-4  # Reaction rate constant (1/s) in the CL

def reaction_coeff(x_val):
    """
    Returns the local reaction coefficient (1/s) at position x.
    Reaction occurs only in the catalyst layer.
    """
    return -k_react if x_val >= L_GDL else 0.0

def odes_mass_transport(t, c):
    """
    Discretized transient mass transport equation for oxygen concentration c(x,t):
       ε * ∂c/∂t = ∂/∂x (ε D_eff ∂c/∂x) + S * c
    Approximated using finite differences.
    """
    dc_dt = np.zeros_like(c)
    for i in range(1, N-1):
        flux_plus  = 0.5 * (epsilon_arr[i+1]*D_eff_arr[i+1] + epsilon_arr[i]*D_eff_arr[i]) * (c[i+1] - c[i]) / dx
        flux_minus = 0.5 * (epsilon_arr[i]*D_eff_arr[i] + epsilon_arr[i-1]*D_eff_arr[i-1]) * (c[i] - c[i-1]) / dx
        diffusion_term = (flux_plus - flux_minus) / dx
        S_local = reaction_coeff(x_space[i])
        dc_dt[i] = (diffusion_term + S_local * c[i]) / epsilon_arr[i]
    
    # Boundary conditions:
    # At x = 0: Dirichlet (fixed oxygen concentration)
    c_in = 9.24  # mol/m³ (approximate concentration for 21% O2)
    dc_dt[0] = 0  # Enforced externally by resetting c[0] later
    # At x = L_total: Neumann (zero flux)
    i_edge = N - 1
    S_edge = reaction_coeff(x_space[i_edge])
    dc_dt[i_edge] = (S_edge * c[i_edge]) / epsilon_arr[i_edge]
    
    return dc_dt

# ====================================================
# 4. Calibration and Validation Component
# ====================================================
def simulate_voltage_curve(i_range, i0_cath, k_mem):
    """
    Simulation function for the polarization curve.
    Adjusts the cathode exchange current density and membrane conductivity.
    """
    model = PEMElectrolyzer(
        area=0.01,   # 100 cm² electrode area
        T=298,
        E0=1.23,
        t_mem=50e-6,
        k_mem=k_mem,
        i0_anode=1e4,
        i0_cath=i0_cath,
        alpha=0.5,
        i_lim=800
    )
    return model.simulate_polarization_curve(i_range)

# ====================================================
# Main Execution: Running and Plotting All Components
# ====================================================
if __name__ == "__main__":
    # ----- Part A: Calibration of the Polarization Curve -----
    i_data = np.linspace(10, 750, 50)  # Current densities (A/m²)
    # Generate synthetic "experimental" data using true parameters (i0_cath=1, k_mem=0.1) with added noise
    true_voltage = simulate_voltage_curve(i_data, i0_cath=1, k_mem=0.1)
    np.random.seed(42)
    noise = np.random.normal(0, 0.005, size=true_voltage.shape)
    voltage_exp = true_voltage + noise
    
    # Calibrate the model parameters (i0_cath and k_mem) using nonlinear least squares
    p0 = [0.8, 0.09]  # Initial guesses
    popt, pcov = curve_fit(simulate_voltage_curve, i_data, voltage_exp, p0=p0)
    calibrated_i0_cath, calibrated_k_mem = popt
    print(f"Calibrated i0_cath: {calibrated_i0_cath:.4f} A/m²")
    print(f"Calibrated k_mem: {calibrated_k_mem:.4f} S/m")
    
    # Plot experimental data vs. calibrated model
    i_fit = np.linspace(10, 750, 100)
    voltage_fit = simulate_voltage_curve(i_fit, calibrated_i0_cath, calibrated_k_mem)
    
    plt.figure(figsize=(8,5))
    plt.scatter(i_data, voltage_exp, color='red', label='Experimental Data')
    plt.plot(i_fit, voltage_fit, 'b-', lw=2, label='Calibrated Model')
    plt.xlabel("Current Density (A/m²)")
    plt.ylabel("Cell Voltage (V)")
    plt.title("Calibration: Polarization Curve")
    plt.legend()
    plt.grid(True)
    plt.show()
    
    # ----- Part B: Transient Thermal Dynamics and Water Management -----
    # Define simulation parameters for the thermal-water ODE system
    params = {
        'A': 0.01,             # Active area (m²)
        't_mem': 50e-6,        # Membrane thickness (m)
        'k_mem': 0.1,          # Membrane conductivity (S/m)
        'E0': 1.23,            # Standard reversible voltage (V)
        'p_H2': 1.0,           # H2 partial pressure (atm)
        'p_O2': 1.0,           # O2 partial pressure (atm)
        'a_H2O': 1.0,          # Water activity
        'i0_anode': 1e4,       # Anode exchange current density (A/m²)
        'i0_cath': 1,          # Cathode exchange current density (A/m²)
        'alpha': 0.5,          # Charge transfer coefficient
        'i': 500,              # Current density (A/m²)
        'i_lim': 800,          # Limiting current density (A/m²)
        'm_cell': 0.05,        # Effective cell mass (kg)
        'C_p': 4000,           # Specific heat capacity (J/(kg*K))
        'h': 10,               # Cooling coefficient (W/K)
        'T_amb': 298,          # Ambient temperature (K)
        'deltaH': 286e3,       # Reaction enthalpy (J/mol)
        'n_d': 2.5,            # Electro-osmotic drag coefficient
        'D_w': 1e-6,           # Water diffusivity in membrane (m²/s)
        'lam_eq': 14           # Equilibrium water content
    }
    
    y0 = [params['T_amb'], params['lam_eq']]  # Initial conditions: ambient T and equilibrium water content
    t_span = (0, 100)  # Simulate for 100 seconds
    t_eval = np.linspace(t_span[0], t_span[1], 200)
    
    sol_thermal = solve_ivp(fun=lambda t, y: odes(t, y, params),
                            t_span=t_span, y0=y0, t_eval=t_eval, method='RK45')
    
    plt.figure(figsize=(10,4))
    plt.subplot(1,2,1)
    plt.plot(sol_thermal.t, sol_thermal.y[0], 'r-', lw=2)
    plt.xlabel("Time (s)")
    plt.ylabel("Temperature (K)")
    plt.title("Transient Temperature Evolution")
    plt.grid(True)
    
    plt.subplot(1,2,2)
    plt.plot(sol_thermal.t, sol_thermal.y[1], 'b-', lw=2)
    plt.xlabel("Time (s)")
    plt.ylabel("Membrane Water Content λ")
    plt.title("Transient Water Content Evolution")
    plt.grid(True)
    plt.tight_layout()
    plt.show()
    
    # ----- Part C: Transient Mass Transport in Electrode -----
    # Initial oxygen concentration is set to the inlet value everywhere.
    c0 = np.ones(N) * 9.24  # mol/m³
    t_span_mt = (0, 5)      # Simulate mass transport for 5 seconds
    t_eval_mt = np.linspace(t_span_mt[0], t_span_mt[1], 100)
    
    sol_mt = solve_ivp(odes_mass_transport, t_span_mt, c0, t_eval=t_eval_mt, method='RK45')
    # Enforce Dirichlet BC at x = 0 (inlet concentration)
    sol_mt.y[0, :] = 9.24
    
    plt.figure(figsize=(10,4))
    for idx in [0, 20, 40, 60, 80, 99]:
        plt.plot(x_space*1e6, sol_mt.y[:, idx], label=f"t = {sol_mt.t[idx]:.2f} s")
    plt.xlabel("Position (µm)")
    plt.ylabel("Oxygen Concentration (mol/m³)")
    plt.title("Transient O₂ Concentration Profiles in Electrode")
    plt.legend()
    plt.grid(True)
    plt.show()
    
    # Compute local current distribution in the Catalyst Layer (CL) at final time.
    # Stoichiometry: 1 mole O₂ consumed produces 4F coulombs.
    i_local = np.zeros(N)
    for i_node in range(N):
        if x_space[i_node] >= L_GDL:  # Only in the catalyst layer
            i_local[i_node] = 4 * 96485 * k_react * sol_mt.y[i_node, -1]
        else:
            i_local[i_node] = 0.0
    
    plt.figure(figsize=(6,4))
    plt.plot(x_space*1e6, i_local, 'ro-')
    plt.xlabel("Position (µm)")
    plt.ylabel("Local Current Density (A/m³)")
    plt.title("Local Current Distribution in Catalyst Layer\n(t = {:.2f} s)".format(sol_mt.t[-1]))
    plt.grid(True)
    plt.show()

```
