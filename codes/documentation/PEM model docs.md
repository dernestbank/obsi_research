
---

04/05/25
code here: [[PEM model]]

# Documentation for the PEM Electrolyser Model

## Overview

This model simulates a PEM electrolyser (or fuel cell) by combining several physical phenomena into one framework. The model is divided into four main modules:

1. **Electrochemical Module:**  
    Computes the cell voltage as a function of current density by accounting for:
    
    - **Reversible voltage** using the Nernst equation.
        
    - **Activation losses** using Butler–Volmer kinetics (via a Tafel approximation).
        
    - **Ohmic losses** through the membrane.
        
    - **Concentration overpotential** due to mass transport limitations.
        
2. **Thermal Dynamics and Water Management Module:**  
    Models the transient evolution of the cell’s temperature and the membrane’s water content by solving coupled ordinary differential equations (ODEs) based on:
    
    - An energy balance (heat generation from reaction enthalpy and ohmic losses minus cooling losses).
        
    - A water balance that includes electro-osmotic drag (transport of water along with proton current) and back-diffusion toward an equilibrium water content.
        
3. **Mass Transport Module:**  
    Solves a transient, spatially resolved one-dimensional mass transport equation (using a finite-difference method) for oxygen concentration through a porous electrode. The domain is split into:
    
    - **Gas Diffusion Layer (GDL):** No reaction occurs, with properties determined by porosity and tortuosity.
        
    - **Catalyst Layer (CL):** Oxygen is consumed by the electrochemical reaction, which is modeled with first-order kinetics.
        
    
    Local effective diffusivities are calculated based on electrode geometry and material properties. The local current density in the catalyst layer is then estimated from the oxygen consumption rate.
    
4. **Calibration and Validation Component:**  
    Compares the simulated polarization curve (cell voltage vs. current density) with experimental (or synthetic) data. The calibration is performed using a nonlinear least-squares optimizer to adjust key parameters (e.g., cathode exchange current density and membrane conductivity) to best fit the measured data.

---
## 1. Electrochemical Module

### Class: `PEMElectrolyzer`

This class encapsulates the core electrochemical model. It is responsible for calculating the cell voltage based on a set of input parameters.

#### **Key Attributes:**

- **area:** Electrode active area (in m²).
- **T:** Operating temperature (K).
- **E0:** Standard reversible voltage (V), typically ≈1.23 V.
- **t_mem:** Membrane thickness (m).
- **k_mem:** Membrane ionic conductivity (S/m).
- **i0_anode:** Anode exchange current density (A/m²); assumed to be large due to fast kinetics.
- **i0_cath:** Cathode exchange current density (A/m²); usually smaller and controls the activation loss.
- **alpha:** Charge transfer coefficient (dimensionless, typically around 0.5).
- **i_lim:** Limiting current density (A/m²) representing mass transport limitations.
    

#### **Key Methods:**

- **`nernst_voltage(p_H2, p_O2, a_H2O)`**  
    Implements the Nernst equation (Eq. (1)). Returns the reversible cell potential given partial pressures of hydrogen (H₂) and oxygen (O₂) and water activity $a_{\text{H}_2O}$.
    
- **`activation_overpotential(i, i0, electrode)`**  
    Calculates the activation overpotential. For the anode, a fixed small overpotential is assumed; for the cathode, a Tafel-like expression is used:
	$$ $$
- **`conc_overpotential(i)`**  
	Calculates the concentration (mass transport) overpotential (using Eq. (4)):

	A safeguard is included to prevent singular behavior as i→ilimi \to i_{\text{lim}}i→ilim​.