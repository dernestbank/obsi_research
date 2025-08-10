

![[flow field design configs.png]]
ref DOI:[10.1002/tcr.202000138](http://dx.doi.org/10.1002/tcr.202000138)

![[Research notes/PEM electrolyser/attachments/image-1.png]]
@maierMassTransportPEM2022

---

### **3.3 Flow Field Design and Its Effect on Electrolyzer Performance**

In a Proton Exchange Membrane (PEM) electrolyzer, the flow field configuration—etched or machined channels on the bipolar plates—plays a critical role in distributing reactants (water and gases), removing products (oxygen and hydrogen), and managing pressure drop and thermal gradients. While often considered a mechanical feature, flow field architecture strongly influences **mass transport**, **bubble removal**, **water saturation**, **gas crossover**, and **pressure balancing** across the membrane electrode assembly (MEA). Hence, a well-designed flow field can enhance overall electrochemical performance, operational stability, and efficiency.

#### **3.3.1 Flow Field Architectures: Overview**

The most common geometries in PEM electrolyzers include:

- **Serpentine Flow Field**: A single continuous path with sharp turns.
- **Parallel Flow Field**: Multiple straight, parallel channels connected to common inlet and outlet manifolds.
- **Interdigitated Flow Field**: Non-connected channels that force flow through the porous electrode layer (forced convection).
- **Pin-type or Mesh Flow Fields**: Complex designs involving turbulence promoters or porous medium inserts.
    

For PEM **electrolyzers** (as opposed to fuel cells), **serpentine** and **parallel** configurations are the most widely used due to manufacturing simplicity and low reactant pressure demands. However, the selection affects multiple aspects of operation. @sauermoserFlowFieldPatterns2020 

---

#### **3.3.2 Mass Transport and Reactant Utilization**

Flow fields influence the distribution of **liquid water** (inlet reactant) at the anode and removal of **oxygen bubbles** generated during the Oxygen Evolution Reaction (OER). Poor reactant distribution or bubble accumulation leads to localized dry-out, poor catalyst utilization, and concentration overpotentials.

##### (a) **Serpentine Flow Fields**
Serpentine designs offer **uniform flow distribution** due to their single-path nature. The high pressure gradient forces water into all parts of the active area, avoiding stagnant zones. However, at higher current densities, oxygen bubble accumulation can occur at channel bends, increasing local resistance and possibly leading to uneven current distribution.

The **convective transport** improves mass transfer in the catalyst layer, but the longer channel length results in **higher pressure drop** ($\Delta P$), which requires additional pumping energy.

$$P_{\text{serp}} \approx \frac{12 \mu L Q}{w h^3} \left(1 + \frac{2 h}{w} \right) \tag{18}$$

where:

- $\mu$ is the dynamic viscosity of water [Pa·s],
- $L$ is the channel length [m],
- $Q$ is the volumetric flow rate [m³/s],
- $w$, $h$ are channel width and height [m].
    

##### (b) **Parallel Flow Fields**

Parallel channels reduce the flow resistance and pressure drop significantly, enhancing **energy efficiency** of the BoP system. However, the uniformity of flow distribution is sensitive to channel blockage (e.g., by gas bubbles). Inconsistent water supply across channels can create localized dry regions, reducing Faradaic efficiency and accelerating degradation.

To address this, **pressure compensation strategies** or **modified inlet manifolds** are often implemented to balance flow.

---

#### **3.3.3 Bubble Dynamics and Gas Removal**

Oxygen bubbles generated at the anode during electrolysis can obstruct reactant transport to the catalyst surface (two-phase flow effects). Bubble behavior is influenced by:
- **Channel geometry** (serpentine promotes bubble detachment),
- **Flow rate** (higher flow assists removal),
- **Contact angle** and **channel surface treatment** (hydrophilicity affects nucleation).

Excessive gas holdup increases concentration overpotential and can physically disrupt membrane-electrode bonding. A dimensionless **Capillary number** $Ca$ can be used to evaluate bubble removal effectiveness:
$$Ca = \frac{\mu u}{\gamma} \tag{19}$$

where:

- $\mu$ is viscosity [Pa·s],
- $u$ is velocity [m/s],
- $\gamma$ is surface tension of water [N/m].

Higher $Ca$ implies more efficient bubble transport. Serpentine channels generally operate in regimes of higher $Ca$, leading to better gas purging.

---

#### **3.3.4 Impact on Thermal and Pressure Distribution**

Flow fields also affect **thermal gradients** and **mechanical stress** across the MEA:
- **Serpentine fields** promote better thermal uniformity but generate asymmetric mechanical loads due to high $\Delta P$.
- **Parallel fields** can result in localized hot spots or cold zones due to poor flow distribution unless carefully designed.
    

A non-uniform temperature field influences water content in the membrane, impacting:
- Membrane conductivity $\sigma_{\text{mem}}(T,\lambda)$,
- Water crossover behavior
- Risk of membrane drying or swelling.
    

---

#### **3.3.5 Electrochemical Impedance and Flow Field Geometry**

Empirical and computational studies (e.g., @espinosa-lopezModellingExperimentalValidation2018) show that flow field geometry alters the **electrochemical impedance spectra (EIS)**:
- Higher mass transport resistance is observed in parallel fields at high current density due to bubble clogging.
- Ohmic and kinetic resistances remain similar between geometries under low-load conditions.
    

Thus, flow field geometry indirectly influences **overpotentials** and should be modeled in conjunction with:
- Local current density mapping $i(x,y)$,
- Channel humidity and pressure profiles,
- Two-phase flow models (e.g., Volume of Fluid (VOF) CFD models).
    

---

### Summary of Flow Field Effects

| Flow Field     | Mass Transport                     | Pressure Drop | Gas Removal                | Thermal Profile | Notes                   |
| -------------- | ---------------------------------- | ------------- | -------------------------- | --------------- | ----------------------- |
| Serpentine     | High (uniform)                     | High          | Efficient (bubble sweep)   | Uniform         | Good for dynamic loads  |
| Parallel       | Moderate (risk of channel dry-out) | Low           | Poor (bubble accumulation) | Non-uniform     | Requires flow balancing |
| Interdigitated | Very High (forced convection)      | High          | Very Efficient             | Moderate        | Risk of flooding        |

---

### Practical Implications for Electrolyzer Modeling

To build a **full PEM electrolyzer model**, the choice of flow field design must be explicitly included in:

- **Pressure drop estimation** (affecting pump sizing and BoP energy),
- **Two-phase flow simulations** (for bubble formation and removal),
- **Electrochemical area effectiveness** (adjusting $A_{\text{cell}}$ due to inactive zones),
- **Thermal model coupling** (affecting $Q_{\text{gen}}$ and $Q_{\text{cool}}$).
    

In simulation environments like COMSOL Multiphysics or custom Python-CFD solvers, incorporating channel-level flow and gas transport models provides better resolution of local phenomena critical to system optimization.

---
Next
Would you like the next section to be on 
**degradation mechanisms** (e.g., catalyst sintering, membrane thinning)
the **techno-economic optimization** domain next?


---




### **3.5 Integrated PEM Electrolyzer Model with Flow Field Effects**

To capture the coupled impacts of electrochemistry, hydrodynamics, mass transport, and parasitic balance‑of‑plant (BoP) power, we now assemble a unified set of governing equations that explicitly include **flow field geometry**. This integrated model is suitable for stack‑level simulation and techno‑economic optimization.

---

#### **3.5.1 Electrochemical Voltage with Flow‑Dependent Mass Transport**

The cell voltage under steady current density ii now incorporates a concentration overpotential that depends on the limiting current density iLi_L, which itself is a function of channel flow velocity uu and geometry:

$$V_{\text{cell}}(u,i) = V_{\text{rev}} + V_{\text{act}}(i) + i\,R_{\text{int}} - \frac{RT}{zF}\,\ln\!\Bigl(1 - \tfrac{i}{i_L(u)}\Bigr) \tag{30}$$

Here:

- $- i_L(u) = n F\,k_m(u)\,c_{\text{bulk}}$
    
- The **mass‑transfer coefficient** $k_m$ relates to the Sherwood number $Sh$, which depends on the Reynolds ($Re$) and Schmidt ($Sc$) numbers for a given channel shape:
    $$k_m(u) = \frac{\mathrm{Sh}(u)\,D}{L_{\text{cl}}}, \quad \mathrm{Sh} = a\,\mathrm{Re}^b\,\mathrm{Sc}^c \quad \mathrm{Re} = \frac{\rho\,u\,h}{\mu} \tag{31}$$
    where $D$ is the diffusion coefficient,  $L_{\text{cl}}$ is the characteristic diffusion length (e.g., catalyst‑layer thickness), and h is channel height.
    

By selecting **serpentine** versus **parallel** flow fields, one modifies the friction factor and thus the velocity $u$ at a given pump power, altering $i_L$ and correspondingly the concentration overpotential.

---

#### **3.5.2 Balance‑of‑Plant Parasitic Power**

The BoP pump energy required to maintain liquid water flow through NchN_{\text{ch}} channels of width ww, height hh, and length LL is:

$$W_{\text{pump}} = \sum_{\text{ch}=1}^{N_{\text{ch}}} \Delta P_{\text{ch}}\;Q_{\text{ch}} \;=\;N_{\text{ch}} \left(\frac{12\,\mu\,L\,Q_{\text{ch}}}{w\,h^3}\Bigl(1+2\frac{h}{w}\Bigr)\right) \;Q_{\text{ch}} \tag{32}$$

with the single‑channel volumetric flow rate    $Q_{\text{ch}} = u\,w\,h\;$. For serpentine channels, $\Delta P$ is higher (due to turns), whereas parallel channels yield lower  $\Delta P$ but risk uneven u.

The **total BoP power** also includes cooling and power electronics:

$$W_{\text{BoP}} = W_{\text{pump}} + W_{\text{cool}} + W_{\text{elec}} \tag{33}$$

---

#### **3.5.3 Stack Voltage and Power**

For a stack of $N_{\text{cell}}$ cells operating at current density i and active area  $A_{\text{cell}}$:

$$V_{\text{stack}}(u,i) = N_{\text{cell}}\;V_{\text{cell}}(u,i), \quad P_{\text{stack}} = V_{\text{stack}} \, (i\,A_{\text{cell}}) \tag{34}$$

The **total electrical power** drawn by the electrolyzer system is

$P_{\text{EL}} = P_{\text{stack}} + W_{\text{BoP}} \tag{35}$

---

#### **3.5.4 Efficiency Metrics with Flow Field Integration**

Using the integrated power expression, the **HHV efficiency** becomes:


$$\eta_{\text{HHV}}(u,i) = \frac{m_{H_2}\,HHV_{H_2}}{P_{\text{stack}} + W_{\text{BoP}}} = \frac{\displaystyle \tfrac{i\,A_{\text{cell}}}{2F}\,HHV_{H_2}} {\displaystyle V_{\text{stack}}\,i\,A_{\text{cell}} \;+\; W_{\text{BoP}}} \tag{36}$$

Similarly, the **specific energy consumption** is updated to:

$$SE_{H_2}(u,i) = \frac{P_{\text{stack}} + W_{\text{BoP}}}{m_{H_2}} \tag{37}$$

Because $W_{\text{pump}}$ scales with channel geometry and required velocity u, **flow field choice** directly influences both $\eta_{\text{HHV}}$ and $SE_{H_2}$. For example, a serpentine design improves  $i_L$ (lower $V_{\text{conc}})$ at the cost of higher  $W_{\text{pump}}$, whereas parallel channels reduce $W_{\text{pump}}$ but may incur larger mass transport penalties under high load.

---

#### **3.5.5 Model Implementation and Parameterization**

1. **Select geometry**: define  $N_{\text{ch}},\,w,\,h,\,L$for serpentine or parallel.
    
2. **Compute**  $\mathrm{Re}(u)$ to obtain $\mathrm{Sh}$ (Eq. 31) and $i_L(u)$.
    
3. **Evaluate** $V_{\text{cell}}$ (Eq. 30) and stack power (Eq. 35).
    
4. **Calculate** BoP pump energy (Eq. 32) and overall efficiencies (Eqs. 36–37).
    
5. **Optimize** current density i and flow rate u to maximize ηHHV $\eta_{\text{HHV}}$ or minimize  $SE_{H_2}$ subject to degradation constraints (Sec. 3.4).
    

---

This integrated framework allows simultaneous evaluation of **electrochemical losses**, **hydraulic penalties**, and **efficiency trade‑offs** inherent to different flow‑field architectures—forming the basis for advanced multi‑objective optimization in PEM electrolyzer design.







links
https://chatgpt.com/share/6800eddb-6fd4-800c-b54f-c252abebe995

https://www.perplexity.ai/search/hey-i-want-you-to-be-my-refere-iJxKdYQhSY.GJ.s1UOoaVg?2=r


https://chatgpt.com/share/6800eddb-6fd4-800c-b54f-c252abebe995

