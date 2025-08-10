

### **3.4 Degradation Mechanisms in PEM Electrolyzers**

Over the lifetime of a PEM electrolyzer, performance decline arises from multiple degradation pathways that impair catalyst activity, ionomer/membrane integrity, and overall cell assembly. In this section, we examine the principal mechanisms—**catalyst sintering**, **membrane thinning and chemical attack**, and **bipolar plate corrosion**—and present models for their kinetics and impact on cell performance.

---

#### **3.4.1 Catalyst Layer Degradation**

**a. Sintering and Surface Area Loss**  
Platinum‐based catalysts in both the oxygen evolution reaction (OER) and hydrogen evolution reaction (HER) layers are prone to sintering under high potentials and elevated temperature. Sintering leads to particle growth, reducing the electrochemically active surface area (ECSA). The rate of ECSA loss is often modeled by an Arrhenius‐type relationship:

$$\frac{dA_{\text{ECSA}}}{dt} = -k_{\text{sin}}(T)\,A_{\text{ECSA}}, \quad k_{\text{sin}}(T)=k_0\exp\!\Big(-\tfrac{E_a}{RT}\Big) \tag{20}$$

where:
- $A_{\text{ECSA}}$ is the active surface area [m²],
- $k_{\text{sin}}$ is the sintering rate constant [s⁻¹],
- $k_0$ is a pre‐exponential factor,
- $E_a$ is the activation energy for Pt atom migration [J/mol],
- $T$ is temperature [K].
    

As $A_{\text{ECSA}}$ decays, the exchange current density $i_0$ diminishes proportionally, increasing the **activation overpotential**:

$$V_{\text{act}}(t) \approx \frac{RT}{\alpha_a F}\ln\!\bigg(\frac{i}{i_0(t)}\bigg) \quad\text{with}\quad i_0(t)\propto A_{\text{ECSA}}(t) \tag{21}$$

**b. Carbon Support Corrosion**  
At the anode, carbon supports can oxidize under high potential (>1.5 V vs. RHE):

$$\ce{C + 2H2O -> CO2 + 4H+ + 4e-}, \quad E^\circ\approx0.207\text{ V vs. SHE}$$

This reaction leads to catalyst detachment and further loss of ECSA. The corrosion current density $i_{\text{corr}}$ can be related to local potential $V$ and water activity $a_{\ce{H2O}}$.

---

#### **3.4.2 Membrane Thinning and Chemical Degradation**

**a. Radical Attack and Thickness Loss**  
Peroxide radicals (HO•, HOO•) generated from oxygen crossover can cleave the polymer backbone of Nafion, thinning the membrane. A first‐order thinning model is:

$$\frac{dt_{\text{mem}}}{dt} = -k_{\text{chem}}\,a_{\ce{O2}}\,t_{\text{mem}}, \quad k_{\text{chem}} = k_r\,[\text{radical}] \tag{22}$$

where:

- $t_{\text{mem}}$ is membrane thickness [m],
- $k_{\text{chem}}$ is the chemical thinning rate [s⁻¹],
- $a_{\ce{O2}}$ is local oxygen activity,
- $[\text{radical}]$ is radical concentration, proportional to crossover flux.
    

As thickness decreases, **ohmic resistance** rises:

$$R_{\text{mem}}(t) = \frac{t_{\text{mem}}(t)}{\sigma_{\text{mem}}(T,\lambda)\,A_{\text{cell}}} \quad\Longrightarrow\quad V_{\text{ohm}}(t) = i\,R_{\text{mem}}(t) \tag{23}$$

**b. Mechanical Swelling and Dry–Wet Cycling**  
Repeated hydration/dehydration cycles cause mechanical stress, leading to micro‐cracking. Crack density $\rho_{\text{crack}}$ can be modeled as a function of cycle number $N$:
$$\rho_{\text{crack}}(N) = k_{\text{mech}}\,N^\beta, \quad 0<\beta<1 \tag{24}$$

Increased cracking facilitates gas crossover, reducing Faradaic efficiency:

$$\eta_F(t) = 1 - \frac{i_{\text{xover}}(t)}{i}, \quad i_{\text{xover}}(t)\propto \rho_{\text{crack}}(t) \tag{25}$$

---

#### **3.4.3 Bipolar Plate and Flow Field Corrosion**

**a. Metallic Bipolar Plate Oxidation**  
Titanium or stainless‐steel bipolar plates develop oxide layers under anodic conditions. This corrosion increases interfacial contact resistance (ICR). The ICR growth over time follows:

$$\text{ICR}(t) = \text{ICR}_0 + k_{\text{corr}}\,t^{n}, \quad 0<n<1 \tag{26}$$

Higher ICR contributes to additional ohmic losses:

$$V_{\text{ohm,BPP}}(t) = i\,\bigl(R_{BPP,0} + \Delta R_{\text{corr}}(t)\bigr) \tag{27}$$

**b. Channel Erosion and Delamination**  
Flow field channels can erode under cavitation or particulate abrasion, altering local mass transport. Channel depth $h(t)$ decays linearly with cumulative volumetric throughput $Q_{\text{tot}}$:

$$h(t) = h_0 - k_{\text{ero}}\,Q_{\text{tot}}(t) \tag{28}$$

Shallower channels increase local velocity and pressure drop, impacting BoP energy consumption and water distribution uniformity.

---

### **3.4.4 Impact on Long‐Term Performance**

Combining all degradation pathways, the **stack voltage** under constant current $i$ drifts upward:

$$V_{\text{cell}}(t) = V_{\text{rev}} + V_{\text{act}}(t) + V_{\text{ohm}}(t) + V_{\text{conc}}(t) \tag{29}$$

An accelerated test protocol often measures voltage degradation rate (VDR) in mV · h⁻¹. A well‐maintained PEM electrolyzer exhibits VDR ≲10 µV · h⁻¹, while systems without optimized materials or flow fields can exceed 50 µV · h⁻¹, halving stack life expectancy.

---

**References for Degradation Models**

1. **Sintering kinetics**: @zhangStatusPerspectivesKey2022;
2. **Carbon corrosion**: @espinosa-lopezModellingExperimentalValidation2018;
3. **Radical‐induced thinning**: @leeThreeDimensionalTransportModeling2008;
4. **Mechanical cracking**: @garcia‑valverdeSimplePEMWater2012;
5. **Bipolar plate ICR growth**: @kimTechnoeconomicAnalysisAnion2024.
    

---

This completes the core degradation mechanisms section of your PEM electrolyzer model. Next, you may wish to integrate these degradation rate equations into your transient stack simulations or explore mitigation strategies—such as catalyst alloying, membrane reinforcement, or flow field coatings—to enhance long‐term durability.

