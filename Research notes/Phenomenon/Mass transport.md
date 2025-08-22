
Basis from grand design.
[[equations]]

**4. Mass Transport & Flow-Field**
    * Effective Diffusivity ($D_{eff} = \frac{\varepsilon}{\tau} \cdot D$)
    * Bubble-Corrected Diffusivity ($D_{bub} = D_{eff} \cdot (1-\theta_{bubble})^{1.5}$)
    * Sherwood Correlation ($Sh = a \cdot Re^b \cdot Sc^c$)
    * Limiting Current Density ($i_{L,eff} = n \cdot F \cdot k_{m,eff} \cdot c_{bulk}$)
    * Concentration Overpotential ($\eta_{conc} = -\frac{RT}{zF} \ln\!\Bigl(1 - \frac{i}{i_{L,eff}}\Bigr)$)

**5. Bubble Dynamics**
    * Bubble Flux ($J_{gas} = \frac{i}{zF}$)
    * Coverage Diameter (order 100–500 µm)
    * Effects:
        * Blocks active sites (ECSA)
        * Raises local resistance (Bruggeman)
        * Slows mass transport

**6. Water Management & Capillarity**
    * Electro-osmotic Drag ($N_{osm} = \frac{n_d \cdot i}{F}$)
    * Back-Diffusion ($N_{diff} = -D_{\lambda} \frac{\rho_{dry}}{EW} \cdot \frac{d\lambda}{dx}$)
    * Hydraulic Crossover ($N_{hyd} = -\frac{K_{mem}}{\mu_w} \cdot \Delta p$)
    * Capillary Flux ($P_c = -\frac{2\gamma \cos\theta}{r_p}$, $N_{cap} = -\frac{k_{cap}}{\mu_w} \cdot \nabla P_c$)


![[membranes-10-00310-ag.webp|431x219]]


water movement across the membrane is important for
	proton conduction 
	Prevent dehydration of the anode side and flooding of the cathode side.


### **Diagram Components**

#### 🔁 **Crossover (Center of Membrane)**

- **H₂ (Hydrogen) and O₂ (Oxygen) crossover:** Ideally, the membrane should prevent crossover, but some molecules diffuse through, especially under high pressure or thin membranes. This leads to **efficiency loss and safety risks** (possible gas mixing)
#### 📉**Mechanical Stress**
- Arises from **hydration/dehydration cycles** and pressure gradients.
- Affects membrane durability and transport properties.
    
#### 💧 **Water Transport**
- **Water movement** across the membrane is crucial for:

#### 🧮 **Flux Equation (Purple Box)**

This is the **water flux equation (Nw,m)** combining:

- **Diffusion (∇μw)**: Movement from high to low water chemical potential (like humidity difference).
- **Drag (i/F)**: Protons dragging water molecules (electro-osmotic drag) from anode to cathode.

**1. Water Flux Driven by Chemical Potential Gradient:**
$$N_{w,m} = -\alpha_{w,m} \nabla \mu_w + \frac{i}{F}$$
Where:
* $N_{w,m}$: Molar flux of water (mol m⁻² s⁻¹).
-  $\alpha_{w,m}$: Electro-osmotic drag coefficient (mol H₂O mol⁻¹ H⁺). This term represents the number of water molecules dragged along with each proton moving through the membrane due to the electric field.
* $\nabla \mu_w$: Gradient of the chemical potential of water (J mol⁻¹ m⁻¹). This term accounts for water transport driven by differences in water concentration or activity across the membrane (diffusion due to concentration gradients).
* $i$: Current density (A m⁻²). This term represents the flux of protons (or other charge carriers). 
* $F$: Faraday constant (approximately 96485 C mol⁻¹).
* $\frac{i}{F}$: Represents the molar flux of protons (assuming all current is carried by protons). This equation indicates that water flux is driven by both the gradient of the chemical potential of water (diffusion) and the electro-osmotic drag associated with ion movement.
* 
**2. Water Flux Driven by Concentration Gradient:**
$N_w = -D_w \nabla C_w + \xi \frac{i}{F}$
Where: 
* $N_w$: Molar flux of water (mol m⁻² s⁻¹). 
* $D_w$: Diffusion coefficient of water in the membrane (m² s⁻¹). 
* $\nabla C_w$: Gradient of the concentration of water (mol m⁻³ m⁻¹). This term directly represents the driving force for water diffusion due to concentration differences. * $\xi$: Electro-osmotic drag coefficient (mol H₂O mol⁻¹ H⁺), which may or may not be equal to $\alpha_{w,m}$ depending on the model and assumptions. * $\frac{i}{F}$: Again, represents the molar flux of protons.



The total flux ($N_w$) also combines:

$$N_w = -D_w \nabla C_w + \xi \frac{i}{F}$$
- Where:
    - $D_w$​: Water diffusion coefficient.
    - $C_w$​: Water concentration.
    - $\xi$: Electro-osmotic drag coefficient.
    - i: Current density.
    - F: Faraday’s constant.
        
#### ⚡ **Ohm’s Law in Membrane (Green Box)**

This shows protonic current conduction
The current density ($i$) is given by:

$$i = -\kappa \nabla \phi - \frac{\kappa \xi}{F} \nabla \mu_w$$
- First term: **Ionic conductivity** (voltage gradient drives current).
- Second term: **Streaming current** (some authors include this to capture water-migration-driven current).



### ⚛️ **Summary in PEM Electrolyzer Operation**

> [!important] 
> This model is just based on the depiction in the diagram

- **Protons (H⁺)** are generated at the **anode** and move through the membrane to the **cathode**.
- **Water management** is critical: imbalance leads to degradation or poor performance.
- **Drag and diffusion** govern water transport.
- **Ohm's law** is extended to include chemical potential gradients.
- **Crossover** and **mechanical stress** are inefficiencies that must be minimized through membrane design and operating condition control.

----




# From literature

@kangIntroducingNovelTechnique2021  The hydrogen crossover happens under the impact of both diffusive and convective transport

The molar flow rate of hydrogen ($\dot{N}_{H_2}$) is given by:

$$\dot{N}_{H_2} = \dot{N}_{Diff} + \dot{N}_{Conv} = D_{H_2}^{eff} \frac{p_{H_2}}{\delta_m} + \epsilon_{H_2O}^m \frac{k_{hy}^m S_{H_2}}{\mu_{H_2O}} \frac{p_{H_2} \Delta p}{\delta_m} \quad (2)$$
Where 
$D_{H_2}^{eff}$ is the effective diffusion coefficient for hydrogen in the dissolved water of the membrane,
$S_{H_2}$ is the solubility of hydrogen in liquid water, 
$p_{H_2}$ is the partial pressure of hydrogen, 
$\delta_m$ is the membrane thickness, 
$\epsilon_{H_2O}^m$ is the water volume fraction in the membrane,
$k_{hy}^m$ is the hydraulic  permeability of liquid water through the membrane, 
$\mu_{H_2O}$ is the water dynamic viscosity, 
$\Delta p$ is the differential pressure that induces the hydraulic water transport from high pressure to low pressure side.

![[H2 crossover params @kang et al 2021.png|374x211]]
## Table 1 – Detailed parameters for hydrogen crossover estimation.

> [!NOTE]
> #params

| Parameters               | Values                 | Unit         | source          |
| :----------------------- | :--------------------- | :----------- | :-------------- |
| $D_{H_2}^{eff}$ [32]     | $2.205 \times 10^{-9}$ | m² s⁻¹       |                 |
| $S_{H_2}$ [33]           | $7.12 \times 10^{-6}$  | mol m⁻³ Pa⁻¹ |                 |
| $p_{H_2}$                | 98.1–132.6             | kPa          | @ang et al 2021 |
| $\delta_m$               | 25–175                 | μm           | @ang et al 2021 |
| $\epsilon_{H_2O}^m$ [37] | 0.37                   | –            |                 |
| $k_{hy}^m$ [38]          | $1.6 \times 10^{-18}$  | m²           |                 |
| $\mu_{H_2O}$             | $4.7 \times 10^{-8}$   | Pa s         | @ang et al 2021 |
| $\Delta p$               | 0–34.5                 | kPa          | @ang et al 2021 |

> [!important] 
> refs

Kang, Z.; Pak, M.; Bender, G. Introducing a Novel Technique for Measuring Hydrogen Crossover in Membrane-Based Electrochemical Cells. _International Journal of Hydrogen Energy_ **2021**, _46_ (29), 15161–15167. [https://doi.org/10.1016/j.ijhydene.2021.02.054](https://doi.org/10.1016/j.ijhydene.2021.02.054).
[32] Trinke P, Bensmann B, Reichstein S, Hanke-Rauschenbach R, Sundmacher K. Hydrogen permeation in PEM electrolyzer cells operated at asymmetric pressure conditions. J Electrochem Soc 2016;163:F3164.
[33] Sakai T, Takenaka H, Wakabayashi N, Kawami Y, Torikai E. Gas permeation properties of solid polymer electrolyte (SPE) membranes. J Electrochem Soc 1985;132:1328.
[37] Fimrite J, Carnes B, Struchtrup H, Djilali N. Transport phenomena in polymer electrolyte membranes: ii. binary friction membrane model. J Electrochem Soc 2005;152:A1815.
[38] Fales J, Vanderborgh N, Stroeve P. The influence of channel geometry on ionic transport. Diaphragms, seperators, ionexchange membranes 1986;86.

(C) shows the calculated hydrogen crossover rate through different Nafion membranes









----


## Transport Model Framework for a PEM Electrolyzer Membrane

**Tags:** #PEM #electrolyzer #transportmodel #membrane #waterflux #protonflux #gas crossover #NernstPlanck #FicksLaw #multiphysics #modeling

> [!important] 
> Where I integrate the transport session of my bigger PEM model

This framework describes the transport phenomena within a Polymer Electrolyte Membrane (PEM) electrolyzer, considering the fluxes of hydrogen (H₂), oxygen (O₂), protons (H⁺), and water (H₂O) through the membrane. It accounts for four principal water-flux mechanisms.



**1. Geometry & Coordinate System**

* **1D Through-Plane Coordinate:** $x \in [0, L_m]$
    * $x = 0$: Anode/membrane interface
    * $x = L_m$: Cathode/membrane interface
* **Membrane Properties:**
    * $L_m$: Membrane thickness
    * $\rho_{dry}$: Dry density
    * $EW$: Equivalent weight

**2. Species & Flux Definitions**

For each species $k \in \{\text{H}_2, \text{O}_2, \text{H}^+, \text{H}_2\text{O}\}$, the molar flux $N_k(x)$ (mol m⁻² s⁻¹) is positive in the anode → cathode direction.

**2.1 Proton Flux (Nernst–Planck)**

$N_{H^+} = -\kappa(\lambda) \frac{d\phi}{dx} - \frac{\kappa(\lambda) RT}{F} \frac{1}{c_{H^+}} \frac{dc_{H^+}}{dx}$

Where:
* $\kappa(\lambda)$: Proton conductivity (function of membrane water content $\lambda$).
* $\phi(x)$: Electric potential.
* $R$: Ideal gas constant.
* $T$: Temperature.
* $F$: Faraday constant.
* $c_{H^+} \approx \frac{\rho_{dry}}{EW} \lambda$: Proton concentration (approximation).

**2.2 Gas Crossover (Fick’s Law)**

For H₂ and O₂ dissolved in the membrane ($k \in \{\text{H}_2, \text{O}_2\}$):

$N_{k} = -D_{k}(\lambda) \frac{dc_{k}}{dx}$

Where:
* $D_{k}(\lambda)$: Diffusivity of gas $k$ (increasing with hydration $\lambda$).
* $c_k(x)$: Concentration of dissolved gas $k$.

**2.3 Water Flux Components**

Total water flux $N_w(x)$ is the sum of four mechanisms:

$N_w(x) = N_{\mathrm{osm}} + N_{\mathrm{diff}} + N_{\mathrm{hyd}} + N_{\mathrm{cap}}$

* **Electro-osmotic Drag:**
    $N_{\mathrm{osm}} = \frac{n_d(\lambda) i(x)}{F}$
    Where $n_d(\lambda)$ is the drag coefficient (H₂O per H⁺) and $i(x) = F N_{H^+}(x)$.

* **Back-Diffusion:**
    $N_{\mathrm{diff}} = -D_{\lambda} \frac{\rho_{dry}}{EW} \frac{d\lambda}{dx}$
    Where $D_{\lambda}$ is the diffusion coefficient of water in the polymer.

* **Hydraulic Crossover (Pressure-Driven):**
    $N_{\mathrm{hyd}} = -\frac{K_{mem}}{\mu_w} \frac{dp}{dx}$
    Where $K_{mem}$ is membrane permeability, $\mu_w$ is water viscosity, and $p(x)$ is hydraulic pressure.

* **Capillary Flux:**
    $N_{\mathrm{cap}} = -k_{cap} \frac{dS}{dx}$
    Where $S(x)$ is the local saturation (liquid fraction), and $k_{cap}$ is the capillary-pressure permeability.

**3. Conservation Equations**

For each species, mass conservation in steady state gives:

$\frac{dN_k}{dx} = R_k(x)$

Where $R_k$ is the volumetric source/sink:

* **H⁺:** $R_{H^+} = 0$ inside the membrane.
* **H₂ and O₂:** $R_k = 0$ (no reaction in bulk).
* **H₂O:** Include water produced/consumed by electrochemical reaction only at interfaces (Dirichlet boundary conditions on flux).

**4. Boundary Conditions**

| Interface           | Variable   | Condition                                                                           |
| :------------------ | :--------- | :---------------------------------------------------------------------------------- |
| $x = 0$ (anode)     | $\phi$     | Set by cell voltage                                                                 |
|                     | $c_{H^+}$  | From local catalyst layer hydration $\lambda_a$                                     |
|                     | $c_{H_2O}$ | $\lambda_a \rightarrow$ water concentration                                         |
|                     | $p$        | $p_a$ (e.g., cell backpressure)                                                     |
| $x = L_m$ (cathode) | $\phi$     | Ground (0 V)                                                                        |
|                     | $c_{H^+}$  | $\lambda_c$                                                                         |
|                     | $c_{H_2O}$ | $\lambda_c \rightarrow$ water concentration                                         |
|                     | $p$        | $p_c$                                                                               |
| Boundaries          | Gas conc.  | Set by Henry’s law with partial pressures $p_{H2}, p_{O2}$ in the porous electrode. |

**5. Coupling & Solution Strategy**

1. Initialize $\lambda(x)$, $\phi(x)$, $p(x)$.
2. Compute local transport properties $\kappa(\lambda)$, $D_k(\lambda)$, $n_d(\lambda)$.
3. Discretize flux equations and mass balances.
4. Apply boundary conditions.
5. Solve the coupled nonlinear system (e.g., Newton-Raphson).

**6. Key Outputs & Diagnostics**

* Proton current $i(x) = F N_{H^+}(x) \rightarrow$ should be constant.
* Water balance: check $N_w(0)$ vs. $N_w(L_m)$ to avoid net drying.
* Gas crossover rates $N_{H_2}(L_m)$, $N_{O_2}(0)$.
* Local hydration $\lambda(x)$.
* Pressure profile $p(x)$ to evaluate hydraulic stress.

**Next Steps**

* Parameterize each coefficient ($D_{\lambda}$, $K_{mem}$, $k_{cap}$, etc.) from experiments or literature.
* Implement in your preferred numerical framework (MATLAB, Python+FiPy, COMSOL).
* Validate against water-balance measurements and gas-crossover data.

This model provides a robust framework for simulating transport phenomena within a PEM electrolyzer membrane, accounting for the intricate interplay of various species and flux mechanisms. It can be extended for more complex scenarios by incorporating temperature dependence or two-dimensional gradients.


---



## Folding Experimental Crossover Expression into Membrane Transport Framework

**Tags:** #PEM #electrolyzer #transportmodel #H2crossover #Kang2021 #diffusion #convection #massbalance #boundarycondition

> [!important] 
> Where I leveraged on literature data and modified my model with experimental parameters values

This note demonstrates how to integrate an experimentally derived hydrogen crossover expression from Kang et al. (2021) into a general PEM membrane transport framework. We will map the experimental terms to diffusive and hydraulic fluxes, express total H₂ crossover as a function of operating conditions and membrane properties, and embed it into a 1D mass balance.

**1. Kang et al. Crossover Expression**

Kang et al. (2021) provide the total hydrogen molar flow ($\dot N_{H_2}$) across the membrane as:

$\dot N_{H_2} = \underbrace{D_{H_2}^{\rm eff}\,\frac{p_{H_2}}{\delta_m}}_{\dot N_{\rm Diff}} \;+\; \underbrace{\epsilon_{H_2O}^m \,\frac{k_{hy}^m \, S_{H_2}}{\mu_{H_2O}}\; \frac{p_{H_2}\,\Delta p}{\delta_m}}_{\dot N_{\rm Conv}} \quad (2)$

Where:

* $D_{H_2}^{\rm eff}$: Effective H₂ diffusivity in hydrated membrane (m² s⁻¹)
* $p_{H_2}$: Hydrogen partial pressure (Pa)
* $\delta_m$: Membrane thickness (m)
* $\epsilon_{H_2O}^m$: Membrane water volume fraction (–)
* $k_{hy}^m$: Hydraulic permeability (m²)
* $S_{H_2}$: H₂ solubility in water (mol m⁻³ Pa⁻¹)
* $\mu_{H_2O}$: Water viscosity (Pa s)
* $\Delta p$: Across-membrane pressure difference (Pa)

**2. Correspondence to General Transport Model**

In our 1D model for dissolved-gas crossover:

$N_{H_2}(x) = -D_{H_2}(\lambda)\,\frac{dc_{H_2}}{dx} \;+\; \underbrace{\Bigl(-\tfrac{K_{mem}}{\mu_w}\,\tfrac{dp}{dx}\Bigr)}_{\text{hydraulic term}} \;{\times}\; c_{H_2}(x)$

Where $c_{H_2} = S_{H_2}\,p_{H_2}$. Integrating across $x \in [0, \delta_m]$ yields:

* **Diffusive term:**
    $\dot N_{\rm Diff} = D_{H_2}^{\rm eff}\,\frac{c_{H_2}(0)-c_{H_2}(\delta_m)}{\delta_m} \approx D_{H_2}^{\rm eff}\,\frac{S_{H_2}\,p_{H_2}}{\delta_m}$ (assuming low cathode-side H₂ concentration).

* **Convective (hydraulic) term:**
    $\dot N_{\rm Conv} = \int_0^{\delta_m} \Bigl(\tfrac{k_{hy}^m}{\mu_{H_2O}}\Bigr)\,\frac{dp}{dx}\; S_{H_2}\,p_{H_2}\;dx \;\approx\; \epsilon_{H_2O}^m\,\frac{k_{hy}^m\,S_{H_2}}{\mu_{H_2O}}\, \frac{p_{H_2}\,\Delta p}{\delta_m}$ (pulling out $\epsilon_{H_2O}^m$ for liquid volume fraction).

Thus, Kang's formula represents the integrated form of our local-flux laws over the membrane thickness, with the terms directly corresponding to diffusive and convective (hydraulic) transport of hydrogen.

**3. Embedding into the 1D Mass Balance**

In steady state, the mass balance for H₂ within the membrane simplifies to:

$\frac{dN_{H_2}}{dx} = 0 \quad \Longrightarrow \quad N_{H_2}(x) \equiv \dot N_{H_2}$

Therefore, instead of solving a PDE for $N_{H_2}(x)$, we can impose the constant crossover flux:

$$\boxed{
\dot N_{H_2}
=
D_{H_2}^{\rm eff}\,\frac{p_{H_2}}{\delta_m}
\;+\;
\epsilon_{H_2O}^m\,\frac{k_{hy}^m\,S_{H_2}}{\mu_{H_2O}}\,
\frac{p_{H_2}\,\Delta p}{\delta_m}
}$$

as a known sink at the cathode-side boundary in our finite-difference stencil:

* **Anode boundary ($x = 0$):** No H₂ present $\rightarrow c_{H_2}(0) = 0$.
* **Cathode boundary ($x = \delta_m$):** Impose a flux $N_{H_2}(\delta_m) = \dot N_{H_2}$.

**4. Implementation Tips**

Parameter ranges (from provided table):

* $D_{H_2}^{\rm eff} = 2.205 \times 10^{-9} \, \text{m}^2/\text{s}$
* $S_{H_2} = 7.12 \times 10^{-6} \, \text{mol} \, \text{m}^{-3} \, \text{Pa}^{-1}$
* $\epsilon_{H_2O}^m = 0.37$
* $k_{hy}^m = 1.6 \times 10^{-18} \, \text{m}^2$
* $\mu_{H_2O} = 4.7 \times 10^{-8} \, \text{Pa} \, \text{s}$

**Units:** Ensure consistent units. Convert $\delta_m$ from μm to m and pressures from kPa to Pa in your implementation.

**Code stub (Python-style):**

```python
D_eff = 2.205e-9       # m2/s
S_h2  = 7.12e-6        # mol/(m3·Pa)
eps_w = 0.37
k_mem = 1.6e-18        # m2
mu_w  = 4.7e-8         # Pa·s

def h2_crossover(p_h2, delta_p, delta_m):
    """
    p_h2, delta_p in Pa; delta_m in m
    returns N_dot_H2 in mol/(m2·s)
    """
    diff  = D_eff * p_h2 / delta_m
    conv  = eps_w * k_mem * S_h2 / mu_w * (p_h2 * delta_p) / delta_m
    return diff + conv



```



## Orientation Check & Boundary-Condition Update for a PEM Electrolyzer

**Tags:** #PEM #electrolyzer #orientation #boundaryconditions #H2crossover #anode #cathode #transportmodel

This note clarifies the orientation and boundary conditions for a PEM electrolyzer transport model, ensuring consistency with the physical processes where hydrogen (H₂) is generated at the cathode and oxygen (O₂) at the anode.

**1. Coordinate & Side Labels (Through-Plane)**

| x          | Interface          | Gas phase present | Main reaction                                         |
| :--------- | :----------------- | :---------------- | :---------------------------------------------------- |
| $x = 0$    | Anode / membrane   | O₂ + liquid H₂O  | 2 H₂O → O₂ + 4 H⁺ + 4 e⁻                            |
| $x = L_m$  | Cathode / membrane | H₂              | 4 H⁺ + 4 e⁻ → 2 H₂                                    |

In an electrolyzer:

* **Protons (H⁺):** Source at $x = 0$ (anode), sink (consumption) at $x = L_m$ (cathode).
* **Water Drag (Electro-osmotic drag):** Carries water from anode → cathode with the proton flow.
* **Gas Crossover:**
    * **H₂:** Diffuses/convects from cathode → anode (undesired).
    * **O₂:** Diffuses from anode → cathode (undesired).

**2. Hydrogen Crossover Expression in the Right Direction**

From Kang et al. (2021), the total hydrogen molar flow ($\dot N_{H_2}$) across the membrane is given as:

$\dot N_{H_2} = \underbrace{D_{H_2}^{\rm eff}\,\frac{p_{H_2}^{\text{cat}}}{\delta_m}}_{\text{diffusion}} + \underbrace{\epsilon_{H_2O}^m \frac{k_{hy}^m S_{H_2}}{\mu_{H_2O}} \frac{p_{H_2}^{\text{cat}}\;\Delta p}{\delta_m}}_{\text{hydraulic/convective}}$

Where:
* $p_{H_2}^{\text{cat}}$: Hydrogen partial pressure on the cathode side (Pa).
* $\Delta p = p_{\text{cat}} - p_{\text{an}}$: Across-membrane pressure difference (Pa) (positive when cathode pressure is higher).

This expression yields a positive $\dot N_{H_2}$ value, indicating the molar flow from the cathode (high H₂ partial pressure) to the anode (low/zero H₂ partial pressure).

**3. Boundary Conditions for Electrolyzer Model**

| Variable          | $x = 0$ (anode)                 | $x = L_m$ (cathode)               |
| :---------------- | :------------------------------ | :-------------------------------- |
| Electric potential ($\phi$) | $V_{\text{cell}}$ (anode more positive) | $0 \, \text{V}$                  |
| Proton flux ($N_{H^+}$) | Outward injection $= i/F$      | Inward removal $= i/F$           |
| H₂ concentration ($c_{H_2}$) | $\approx 0$ (no H₂ in anode channel) | $S_{H_2}\,p_{H_2}^{\text{cat}}$ |
| H₂ flux ($N_{H_2}$) | Impose sink $= +\dot N_{H_2}$   | Impose source $= -\dot N_{H_2}$ |
| O₂ analogue       | Reversed directions             | Reversed directions             |
| Water content ($\lambda$) | Set by anode RH               | Unknown, determined by balance   |
| Pressure ($p$)    | $p_{\text{an}}$                 | $p_{\text{cat}}$                 |

**Sign Convention:** Positive flux is defined as anode → cathode. Therefore, the hydrogen crossover flux, which occurs from cathode → anode, is negative within the membrane domain. However, when considering the flux *emerging* at the anode interface, it's positive. Conversely, it's negative when *leaving* the cathode interface.

**4. Quick Code Snippet Reflecting Electrolyzer Orientation**

```python
D_eff = 2.205e-9       # m2/s
S_h2  = 7.12e-6        # mol/(m3·Pa)
eps_w = 0.37
k_perm = 1.6e-18        # m2
mu_w  = 4.7e-8         # Pa·s

def h2_crossover_electrolyzer(p_h2_cat, delta_p, delta_m):
    """
    Hydrogen crossover rate (mol m-2 s-1) from cathode -> anode.
    p_h2_cat : cathode H2 partial pressure (Pa)
    delta_p  : p_cat - p_an (Pa)   # positive for typical differential-pressure stacks
    delta_m  : membrane thickness (m)
    """
    diff  = D_eff * p_h2_cat / delta_m                 # diffusion term
    conv  = eps_w * k_perm * S_h2 / mu_w * p_h2_cat * delta_p / delta_m
    return diff + conv            # ALWAYS positive; direction is cathode -> anode




```

----


## Nafion Membrane Properties and Correlations for PEM Electrolysis (Ito et al., 2011)

**Tags:** #PEM #electrolysis #Nafion #membrane #properties #correlations #wateruptake #conductivity #electroosmoticdrag #gassolubility #gasdiffusivity #gaspermeability

> [!important] 
> Where I add more literature empirical corelations to my transport model from a review paper by ito et al (2011). This is my note take aways from the equations from the review paper


This note compiles key material properties, empirical correlations, and transport equations for Nafion membranes under PEM electrolysis conditions, based on Ito et al. (2011). These can be directly incorporated into a 1D through-plane model.
@itoPropertiesNafionMembranes2011
**1. Water Uptake & Swelling**

* **Water Content ($\lambda$) from Liquid-Water Equilibration:**
    $\lambda = \frac{u \cdot EW}{M_{H_2O}} \quad \text{with} \quad u = \frac{w_{\rm wet}-w_{\rm dry}}{w_{\rm dry}}$
    Where:
    * $EW = 1100 \, \text{g/mol}$ (Equivalent Weight of Nafion)
    * $M_{H_2O} = 18 \, \text{g/mol}$ (Molar mass of water)
    * $u$: Water uptake ratio
    * $w_{\rm wet}$: Wet membrane weight
    * $w_{\rm dry}$: Dry membrane weight
    * Fully hydrated $\lambda \approx 20-30$ (depending on pretreatment).

* **Swelling Ratios (Wet vs. Dry):**
    * In-plane ($d_{id}/d_{id}$): Up to 40% increase.
    * Through-plane ($d_{td}/d_{td}$): Up to 45% increase.
    - [ ] To Use specific values from Table 1 of Ito et al.).

**2. Proton Conductivity ($k$)**

* **Springer et al. (Fuel-Cell Fit, $\lambda > 2$, 25-90 °C):**
    $k(\lambda,T) \, [\text{S/cm}] = (0.005139 \, \lambda - 0.00326) \, \exp\left[\frac{1268}{303} - \frac{1268}{T}\right] \quad (5)$
    * Activation energy $E_a = 10.5 \, \text{kJ/mol}$.
    * $T$ in Kelvin, $\lambda$ from fully hydrated membrane ($\approx 22$).

* **Kopitzke et al. (Liquid-Water-Equilibrated Fit, $\lambda \approx 22$, 25-90 °C):**
    $k(T) = k_0 \, \exp\left[-\frac{E_k}{R\,T}\right] \quad \text{with} \quad k_0 = 2.29 \, \text{S/cm}, \, E_k = 7.83 \, \text{kJ/mol} \quad (6)$
    * $R$: Ideal gas constant ($8.314 \, \text{J mol}^{-1} \text{K}^{-1}$).

**3. Electro-osmotic Drag ($n_d$)**

* **Zawodzinski et al. ($\lambda = 22$, 30 °C):**
    $n_d \approx 2.5 - 2.9$.

* **Onda et al. (Temperature Fit under Liquid-Water Electrolysis):**
    $n_d(T) = 0.0134 \, T + 0.03 \quad (T \text{ in } ^\circ\text{C}) \quad (7)$
    * Yields $n_d \approx 4.1$ at 30 °C.

* **Marangio et al.:** Effective drag per H₂ varies 1.4–1.9 with pressure and current.

**4. Gas Solubility & Diffusivity in Liquid Water**

* **Hydrogen Solubility ($x_{H_2}$, mole-fraction at 1 atm, 273 ≤ T ≤ 353 K):**
    $\ln x_{H_2} = -48.1611 + \frac{5528.45}{T} + 16.8893 \, \ln\left(\frac{T}{100}\right) \quad (8)$

* **Oxygen Solubility ($x_{O_2}$, mole-fraction at 1 atm, 273 ≤ T ≤ 348 K):**
    $\ln x_{O_2} = -66.73538 + \frac{8747.547}{T} + 24.45264 \, \ln\left(\frac{T}{100}\right) \quad (11)$

* **Gas Diffusivity in Water ($D(T)$, Wise & Houghton):**
    $$D(T) = D_0 \, \exp\left[-\frac{E_D}{R\,T}\right], \quad
    \begin{cases}
        D_{0,H_2} = 4.9 \, \text{cm}^2/\text{s}, \, E_{D,H_2} = 16.51 \, \text{kJ/mol} \\
        D_{0,O_2} = 4.2 \, \text{cm}^2/\text{s}, \, E_{D,O_2} = 18.38 \, \text{kJ/mol}
    \end{cases} \quad (14)$$

**5. Gas Permeability in Nafion Membrane ($P_m = D \cdot S$)**

* Parameterized by Arrhenius fit from wet-membrane experiments:
    $P_m(T) = P_{m,0} \, \exp\left[-\frac{E_p}{R\,T}\right]$

* Typical literature values (wet Nafion 117 near 80 °C):
    * $P_{m,H_2} \approx 10^{-15} - 10^{-16} \, \text{mol} \, \text{m}^{-1} \text{s}^{-1} \text{Pa}^{-1}$
    * $P_{m,O_2} \approx (0.5 - 0.8) \times 10^{-16} \, \text{mol} \, \text{m}^{-1} \text{s}^{-1} \text{Pa}^{-1}$
    - [ ] See Figs. 6-7 in Ito et al. for exact fits).


![[Research notes/Phenomenon/attachments/image.png|353x555]]

![[Research notes/Phenomenon/attachments/image-1.png|266x449]]


**6. High-Pressure Crossover & Current Efficiency**

* **Kang et al. (2021) Crossover Law:**
    $\dot N_{H_2} = D_{H_2}^{\rm eff}\,\frac{p_{H_2}}{\delta_m} +\epsilon_{w}\,\frac{k_{hy}\,S_{H_2}}{\mu_w}\, \frac{p_{H_2}\,\Delta p}{\delta_m}$

* **Takenaka et al. (1985) Mass-Balance Model for Current Efficiency ($h_F$) and Impurity ($a$):**
    $x_{H^+} + 2\,x_O = \frac{i}{2F}\, \left(\frac{1-h_F}{1-3a}\right)!, \quad a = \frac{x_{\rm imp}}{V_{\rm prod}+x_{\rm imp}}$
    Where $x_i = P_{m,i}\,\Delta p/\delta_m$.

**▶ How to Plug into Your Model:**

* **Hydration Profile:** Set $\lambda = 20-25$ (liquid-water equilibrated).
* **Proton Conductivity:** Compute $k(\lambda,T)$ with Eq. (5) or (6) for the Ohm's law term.
* **Drag Coefficient:** Use $n_d(T)$ from Eq. (7).
* **Back-Diffusion:** Use $D_{\lambda}$ from literature or neglect (fully saturated).
* **Hydraulic & Capillary:** Use $K_{mem}$, $\mu_w$, and $k_{cap}$ as previously defined.
* **Gas Crossover Boundary Fluxes:** Impose Kang's $\dot N_{H_2}$ and its O₂ analogue (using the corresponding permeability and partial pressure difference).

By incorporating these refined, experimentally validated parameters and correlations, your PEM electrolyzer membrane model will achieve a more accurate representation of water management, ohmic losses, and crossover phenomena under liquid-water, high-pressure operating conditions.


references:

[45] Springer TE, Zawodzinski TA, Gottesfeld S. Polymer electrolyte fuel cell model. J Electrochem Soc 1991;138: 2334e42.
@springerPolymerElectrolyteFuel1991
[46] Kopitzke R, Linkous CA, Anderson HR, Nelson GL. Conductivity and water uptake of aromatic-based proton exchange membrane electrolytes. J Electrochem Soc 2000; 147:1677e81.
@kopitzkeConductivityWaterUptake2000
[36] Zawodzinski TZ, Derouin C, Radzinski S, Sherman RJ, Smith VT, Springer TE, et al. Water uptake by and transport through Nafion 117 membranes. J Electrochem Soc 1993;140: 1041e7
@zawodzinskiWaterUptakeTransport1993
[50] Onda K, Murakami T, Hikosaka T, Kobayashi M, Notu R, Ito K. Performance analysis of polymer-electrolyte water electrolysis cell at a small-unit test cell and performance prediction of large stacked cell. J Electrochem Soc 2002;149: A1069e78.
@ondaPerformanceAnalysisPolymerElectrolyte2002
[64] Wise DL, Houghton G. The diffusion coefficient of ten slightly soluble gases in water at 10-60 C. Chem Eng Sci 1966;21: 999e1010.
@wiseDiffusionCoefficientsTen1966
[55] Marangio F, Santarelli M, Pagani M, Calı  M. Direct high pressure hydrogen production: a laboratory scale PEM electrolyser prototype. ECS Trans 2009;17(1): 555e67.
@marangioDirectHighPressure2009



-----

write up

# Mass Transport and Properties of Nafion Membranes under PEM Water Electrolysis Conditions (Review)

## 1.0 Introduction

The global hydrogen market surpassed 97 million tons (Mt) in 2023, and demand is estimated to reach 150 Mt under the IEA’s net-zero emissions target by 2030. About 30% of the total demand was driven by existing industries switching from fossil-derived hydrogen. Among various hydrogen production technologies, proton exchange membrane (PEM) water electrolysis has garnered significant attention. It promises an on-demand, low-emission hydrogen production due to their high current density, rapid dynamic response, and compatibility with intermittent renewable power sources [1], [2].

Nafion remains the industry standard for ionic exchange membrane for PEM electrolyser and fuel cell applications. The core of the PEM electrolyzer is a perfluorosulfonic acid (PFSA) membrane, which serves as both a proton conductor from the anode (oxygen evolution reaction) to the cathode (hydrogen evolution reaction) and a separator for the product gases [3]. The performance and longevity of PEM electrolyzers are linked to the complex mass transport phenomena occurring within the membrane. Efficient proton transport minimizes ohmic losses, while effective water management ensures adequate hydration for high conductivity without causing flooding. Furthermore, the undesired crossover of product gases through the membrane not only reduces Faradaic efficiency but also poses safety risks [4, 5]. Consequently, a thorough understanding and accurate modelling of these transport processes are essential for the rational design, optimization, and scale-up of PEM electrolyzer technology.

This review aims to provide an overview of the current knowledge regarding mass transport in PFSA membranes, with a particular focus on Nafion, the most widely employed material. The literature is based on experimental data and empirical correlations on the properties of Nafion membranes, such as water uptake, swelling, proton conductivity, drag coefficients, gas solubility, and diffusivity, from Ito et al. [6] and other relevant studies. We then integrate these properties into a unified 1D through-plane transport model that accounts for the proton conduction, water transport, and gas crossover in the membranes.

## 2. PEM Structure & Material Properties

### 2.1 Chemical Composition and Microstructure

Nafion is a PFSA polymer consisting of a hydrophobic polytetrafluoroethylene (PTFE) backbone with perfluorovinyl ether side chains terminated by sulfonic acid groups (–SO₃H) [6]. Upon hydration, phase separation occurs, forming hydrophilic ionic clusters (4–5 nm) connected by water-filled channels (1–3 nm). These channels provide pathways for the transport of protons and water [9].

### 2.2 Water Uptake, Swelling, and Hydration

Ito et al. [6] measured Nafion® 117 to determine water uptake and swelling under liquid-water equilibration conditions. Their findings revealed a direct correlation between the water content ($\lambda$), defined as the number of water molecules per sulfonic acid group, and the relative humidity or water activity of the surrounding environment.

**Water content ($\lambda$, H₂O/SO₃⁻):**
$\lambda=\frac{u\thinspace E W}{M_{H_2O}},\emsp u=\frac{w_{\mathrm{wet}}-w_{\mathrm{dry}}}{w_{\mathrm{dry}}}$

where EW is the equivalent weight of the membrane (typically 1100 g mol⁻¹ for Nafion 117) and $M_{H_2O}$ is the molar mass of water (18 g mol⁻¹). Under fully hydrated conditions, $\lambda$ can reach values between 20 and 30. Swelling alters the dimensions and tortuosity of the transport pathways, thereby influencing the effective diffusivity and permeability of different species within the membrane.

The degree of membrane hydration ($\lambda$) strongly influences key transport coefficients, including proton conductivity ($\kappa(\lambda)$), water diffusion ($D_{\lambda}$), and the effective diffusivity of gases $D_k(\lambda)$.

### 2.3 Proton Conductivity and Temperature Dependence

Several empirical correlations have been developed to describe this relationship under liquid water conditions. The widely used correlation proposed by Springer et al. [10], originally developed for fuel cells but often applied to electrolyzers, is valid for $\lambda>2$ and temperatures between 25 and 90 °C:

**Springer et al. [10]: Valid for $\lambda > 2$ and temperatures between 25–90 °C.**
$\kappa\left(\lambda,T\right)=\left[0.005139\thinspace\lambda-0.00326\right]\exp{\left[1268\thinspace\left(\frac{1}{303}-\frac{1}{T}\right)\right]}\;\left(\mathrm{S/cm}\right)\emsp\left(5\right)$

**Kopitzke et al. (Liquid-water fit) [6]:**
$\kappa\left(T\right)=k_0\thinspace\exp{\left(-\frac{E_k}{RT}\right)},\emsp k_0=2.29\thinspace\mathrm{S/cm},\;E_k=7.83\thinspace\mathrm{kJ/mol}\emsp\left(6\right)$

High proton conductivity is desirable to minimize ohmic losses within the electrolyzer.

## 3. Transport Mechanisms in PEMs

Several driving forces and mechanisms govern the transport of various species within the hydrated Nafion membrane.

### 3.1 Proton Conduction (Nernst-Planck Equation)

Proton transport through the interconnected hydrophilic channels occurs primarily via a combination of vehicular transport (movement of hydrated protons, H₃O⁺) and Grotthuss mechanism (hopping of protons between adjacent water molecules and sulfonic acid groups). The local proton flux ($N_{H^+}$) is described by the Nernst-Planck equation [4], which accounts for both the electric field gradient and the concentration gradient:

$N_{H^+}=-\kappa\left(\lambda,T\right)\thinspace\frac{d\phi}{dx}-\frac{\kappa\left(\lambda,T\right)\thinspace R T}{F\thinspace c_{H^+}}\thinspace\frac{dc_{H^+}}{dx},\emsp\left(3.1\right)$

where $\kappa(\lambda,T)$ is the proton conductivity obtained from Eq. (5) or (6), and the proton concentration $c_{H^+}(x)$ is approximated as:

$c_{H^+}\left(x\right)=\frac{\rho_{dry}}{EW}\thinspace\lambda\left(x\right)$

Here, R is the ideal gas constant, T is the temperature, and F is the Faraday constant. Under steady current conditions ($i=F\thinspace N_{H^+}=\mathrm{constant}$), the second term (related to concentration gradients) is often small compared to the first term (driven by the electric field) in well-hydrated membranes [10].

### 3.2 Water Transport Components

Water transport across the PEM influences membrane hydration, reactant supply and product gas purity. The total water flux $N_w(x)$ within the membrane is a combination of four primary mechanisms [7]: electro-osmotic drag ($N_{osm}$), back-diffusion ($N_{diff}$), hydraulic crossover ($N_{hyd}$), and capillary flux ($N_{cap}$):

$N_w=N_{\mathrm{osm}}+N_{\mathrm{diff}}+N_{\mathrm{hyd}}+N_{\mathrm{cap}}.\emsp\left(3.2\right)$

**Electro-osmotic Drag:** Water molecules are dragged along with the moving protons due to electrostatic interactions. The electro-osmotic flux is proportional to the proton flux and is quantified by the electro-osmotic drag coefficient ($n_d$):
$N_{\mathrm{osm}}=\frac{n_d\left(\lambda,T\right)\thinspace i}{F},\emsp n_d\left(T\right)=0.0134\thinspace T+0.03\emsp\left(3.3\right)$

The electro-osmotic drag coefficient $n_d(T)$ is temperature-dependent, as described by Onda et al. [6].

**Back-Diffusion:** Water diffuses within the membrane due to gradients in its electrochemical potential, often approximated by the concentration gradient of water (or hydration level $\lambda$). The back-diffusion flux $N_{diff}$ is:
$N_{\mathrm{diff}}=-D_\lambda\left(T\right)\thinspace\frac{\rho_{dry}}{EW}\thinspace\frac{d\lambda}{dx},\emsp\left(3.4\right)$

The diffusion coefficient of water in the polymer, $D_\lambda(T)$, is typically in the range of $10^{-10}$ to $10^{-9}\thinspace\mathrm{m}^2/\mathrm{s}$ [6].

**Hydraulic Crossover:** A pressure difference across the membrane can drive water flow. The hydraulic flux $N_{hyd}$ is described by:
$N_{\mathrm{hyd}}=-\frac{K_{mem}\left(T\right)}{\mu_w\left(T\right)}\thinspace\frac{dp}{dx}\emsp\left(3.5\right)$

where $K_{mem}(T)$ is the membrane hydraulic permeability (typically $\approx1.6\times10^{-18}\thinspace\mathrm{m}^2$ [8]), and $\mu_w(T)$ is the dynamic viscosity of water.

**Capillary Flux:** In partially saturated regions, capillary forces arising from the liquid-vapor interface curvature within the porous structure can induce water flow. The capillary flux $N_{\mathrm{cap}}$ is:
$N_{\mathrm{cap}}=-k_{\mathrm{cap}}\thinspace\frac{dS}{dx},\emsp\left(3.6\right)$

where $S\in[0,1]$ is the local water saturation, and $k_{\mathrm{cap}}$ is the capillary permeability (typically $\sim10^{-12}\thinspace\mathrm{m/s}$ [7]).

### 3.3 Gas Crossover

The permeation of product gases (hydrogen and oxygen) across the PEM is an undesirable phenomenon that reduces the electrolyzer's Faradaic efficiency and can pose safety hazards due to the potential formation of explosive gas mixtures. Gas crossover occurs primarily through two mechanisms: Fickian diffusion and hydraulic convection.

#### 3.3.1 Fickian Diffusion

Dissolved gas molecules permeate through the membrane down their concentration gradient. The diffusive flux $N_k^{\mathrm{diff}}$ of a dissolved gas $k\in\{\mathrm{H}_2,\mathrm{O}_2\}$ as governed by Fick's law:

$N_k^{\mathrm{diff}}=-D_k\left(\lambda,T\right)\thinspace\frac{dc_k}{dx},\emsp c_k\left(x\right)=S_k\left(T\right)\thinspace p_k\left(x\right),\emsp\left(3.7\right)$

where $D_k(\lambda,T)$ is the effective diffusivity of gas k in the hydrated membrane, and $c_k(x)$ is the concentration of the dissolved gas, related to its partial pressure $p_k(x)$ by the solubility $S_k(T)$ (Henry's Law). Solubility $S_k(T)$ and diffusivity $D_k(T)$ can be obtained from Eqs. (8), (11), and (14) [6].

#### 3.3.2 Hydraulic-Convective Transport

As formulated by Kang et al. [8], a pressure difference across the membrane contributes to convective gas transport:

$\dot{N_{\mathrm{conv}}}=\epsilon_w\thinspace\frac{k_{hy}S_k}{\mu_w}\thinspace\frac{p_k\thinspace\Delta p}{\delta_m}.\emsp\left(3.8\right)$

Here, $\epsilon_w$ is the membrane water volume fraction, $k_{hy}$ is the hydraulic permeability, $S_k$ is the gas solubility, $\mu_w$ is the water viscosity, $p_k$ is the gas partial pressure, and $\Delta p$ is the pressure difference across the membrane ($\delta_m$ is the membrane thickness). The total gas crossover at steady state is the sum of the integrated diffusive flux (3.7) and the convective flux (3.8).

## 4.0 Conclusions

This review has provided a comprehensive overview of the mass transport phenomena in PEM electrolyzers utilizing Nafion membranes for hydrogen production. The mathematical framework outlined above relies heavily on the integration of empirical correlations derived from experimental studies. The works of Ito et al. [6], Springer et al. [10], Kopitzke et al. [6], Onda et al. [6], Wise & Houghton (as cited in [6]), and Kang et al. [8] provide crucial relationships for parameterizing the model. The fundamental material properties of Nafion, the key transport mechanisms governing protons, water, and gases, and a one-dimensional mathematical modeling framework integrating these aspects have been discussed in detail.

## References

[1] J. Larminie and A. Dicks, *Fuel Cell Systems Explained*. Wiley, 2003.
[2] M. Carmo et al., “A comprehensive review on PEM water electrolysis,” *Int. J. Hydrogen Energy*, vol. 38, pp. 4901–4934, 2013.
[3] R. Borup et al., “Scientific aspects of polymer electrolyte fuel cell durability and degradation,” *Chem. Rev.*, vol. 107, pp. 3904–3951, 2007.
[4] J. Newman and K. E. Thomas-Alyea, *Electrochemical Systems*, 3rd ed. Wiley, 2004.
[5] A. Mench, *Fuel Cell Engines*, 2nd ed. Wiley, 2008.
[6] M. Ito et al., “Properties of perfluorosulfonic acid membranes for water electrolysis,” *J. Membr. Sci.*, vol. 369, pp. 405–415, 2011.
[7] X. Xie et al., “Comprehensive water transport model in PEM fuel cells,” *Electrochim. Acta*, vol. 55, pp. 4634–4646, 2010.
[8] S.-J. Kang et al., “Introducing novel technique for hydrogen crossover estimation,” *Int. J. Hydrogen Energy*, 2021.
[9] O. Borup et al., “PFSA ionomers: Structure and transport,” *J. Electrochem. Soc.*, vol. 162, pp. F500–F516, 2015.
[10] T. E. Springer et al., “Polymer electrolyte fuel cell model,” *J. Electrochem. Soc.*, vol. 138, no. 8, pp. 2334–2342, 1991.





----




https://www.mdpi.com/1420-3049/29/19/4676
`[Figure 9](https://www.mdpi.com/1420-3049/29/19/4676#fig_body_display_molecules-29-04676-f009) shows the various gas transport mechanisms through the membrane, e.g., the Poiseuille flow, Knudsen diffusion, capillary condensation, molecular sieving, surface diffusion, and facilitated transport. In the Poiseuille flow mechanism, gas separation occurs depending on their differential flow rates through the membrane. The flow of gases is governed by the molecular size of the gases, pore radius, pore length, pressure difference, and the viscosity and diffusivity of the gas material [[138](https://www.mdpi.com/1420-3049/29/19/4676#B138-molecules-29-04676)].
`Knudsen diffusion takes place when the membrane pore size is smaller compared to the mean free path. Hence, the gas molecules repeatedly collide with the pore wall and pass the membrane. This involves greater molecule–wall collisions than intermolecular collisions. The gases are separated based on their molecular velocity difference. Molecules with a low molecular weight (H2) travel faster than heavier gases such as CH4 and CO2. For Knudsen diffusion, the membrane should be finely porous with a controlled pore size [[139](https://www.mdpi.com/1420-3049/29/19/4676#B139-molecules-29-04676)].`



![[Research notes/Phenomenon/attachments/image-2.png]]


`The capillary condensation mechanism takes place when one of the gas components from the mixture is condensable. At a lower pressure, the gas condenses into the small pores of the membrane. The gas separation occurs based on the difference in condensation properties. The condensed gas occupies the pores, particularly mesopores and small macropores, at a lower pressure than the bulk pressure. Because of the condensation menisci formed at both ends of the pore, transport occurs via a hydrodynamic flow driven by a capillary-pressure difference between the ends. The condensable gas will form a liquid layer, which restricts the flow of non-condensable gases. Gases with an equal molecular size but different condensation properties can be easily distinguished. Hence, capillary condensation provides very high selectivity compared to other mechanisms. As it operates at a lower pressure, it consumes less energy. Here, by varying the polymer membrane material and adjusting the pore structure, tailor-made separation properties can be achieved for particular gases [[140](https://www.mdpi.com/1420-3049/29/19/4676#B140-molecules-29-04676)].

`Molecular sieving occurs if the membrane pore dimension is identical to the required gas component. Smaller-sized gas components can pass through the pore channels, while larger gas molecules will be rejected. Molecular sieving works on the principle of size exclusion. The size or dimensions of the gas molecules can be defined by their kinetic diameter. Thus, the kinetic diameter will be a decisive parameter for separation across a membrane [[139](https://www.mdpi.com/1420-3049/29/19/4676#B139-molecules-29-04676)]. When a gas molecule is adsorbed on the porous wall of the membrane and migrates along the surface from one end to another, this process is called surface diffusion. For surface diffusion, one of the gas components needs to be preferentially adsorbed onto the membrane surface. The amount of the gas transported through surface diffusion largely depends on the adsorption and movement of the selective component. The driving force may be a difference in the temperature, pressure, or concentration. The migration over the surface can be influenced by the physical and chemical properties of the membrane surface and the interaction between the gas–membrane surface. A high surface area and a high concentration of the selective component make this diffusion dominant over other transport mechanisms [[45](https://www.mdpi.com/1420-3049/29/19/4676#B45-molecules-29-04676)].`

`The solution diffusion mechanism is driven by the solubility and diffusion of individual gas components in the polymer matrix [[141](https://www.mdpi.com/1420-3049/29/19/4676#B141-molecules-29-04676)]. The facilitated transport mechanism occurs through a chemical interaction between the selective component of the membrane and the gas of interest. Here, the selective component of the membrane works as a carrier for the selective gas, transporting the gas of interest through the membrane and inhibiting the travel of other components from the mixture [[142](https://www.mdpi.com/1420-3049/29/19/4676#B142-molecules-29-04676)].`

`Organic polymers are the primary materials for the preparation of gas-separation membranes due to their high selectivity and ease of processing. Polymeric membranes are generally prepared by the phase inversion process ([Figure 10](https://www.mdpi.com/1420-3049/29/19/4676#fig_body_display_molecules-29-04676-f010)). This process facilitates the fabrication of a large-scale membrane. The prepared membrane has an asymmetric structure, with a thin selective-membrane layer on top of a porous structure [[143](https://www.mdpi.com/1420-3049/29/19/4676#B143-molecules-29-04676)]. The characteristics of the selective layer and beneath the porous structure depend on the type of polymer used, the solution concentration, the used non-solvent, the temperature, the humidity, the rate of phase inversion, etc. Polymeric membranes are fabricated in various configurations, such as flat sheets, hollow fibers, disk shapes, etc., and their modules are prepared in the form of hollow-fiber tubular modules or spiral-wound membranes [[143](https://www.mdpi.com/1420-3049/29/19/4676#B143-molecules-29-04676)]. Gas separation occurs through the solution diffusion mechanism. Depending on the affinity toward the polymer material, the membrane can be either a hydrogen-selective or a hydrogen-rejective membrane. These terms will be elaborated on later on in this review. Over time, various polymers, such as polybenzimidazole (PBI), polyimide (PI), polysulfone (PSF), polyetherimide (PEI), and polyethersulfone (PES), were studied for hydrogen purification ([Figure 11](https://www.mdpi.com/1420-3049/29/19/4676#fig_body_display_molecules-29-04676-f011)). Among these, PI, PBI, and their derivatives (Kapton, LARC-TPI, IP-2080, and Matrimid) are the most widely studied due to their high selectivity and thermal stability [[45](https://www.mdpi.com/1420-3049/29/19/4676#B45-molecules-29-04676)].`