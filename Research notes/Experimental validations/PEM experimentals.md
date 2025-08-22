



# Types of PEM efficiencies

#### **A. Voltage Efficiency**

This is the ratio of minimum required (ideal) voltage to the actual applied voltage:
$$\eta_{\text v} = \frac{E_{rev}}{E_{cell}}$$
Ecell​=1.8V (typical real PEM operation)

#### B. Thermodynamic Efficiency (HHV-based)
$$ \eta_{HHV} = \frac{\Delta H}{E_{cell}\cdot n F}= \frac{1.48}{E_{cell}}$$
#### **C. LHV-based Efficiency**

$$\eta_{\text{LHV}} = \frac{\Delta G}{E_{\text{cell}} \cdot nF} = \frac{1.23}{E_{\text{cell}}}$$



##### Different between HHV and LHV.
Depends on whether the latent of vapourization of water vapour during the combustion is applied.'
HHV includes this heat whiles LHV does not include this heat.
Application: 
	LHV: fuel cell,turbines- water vapor is not condensed 
	HHV : boilers where condensation may occur
HHV is the total energy released whiles the LHV is the usable energy availalble for application.
The difference is 18%


#### d. Faradaic efficiency:
The ratio of the actual amount of hydrogen produced to the theoretical amount hydrogen based on the electrical energy input.

$$\eta _F = \frac {n \cdot F \cdot \dot n_{H_2}}{I}$$


Factors Affecting Faraday Efficiency in PEM Electrolyzers:

- **Current Density:** Faraday efficiency tends to increase with higher current densities. 
- **Membrane Thickness:** Thicker membranes can lead to reduced Faraday efficiency. 
- **Gas Pressure:** High pressures can sometimes decrease Faraday efficiency, especially when coupled with hydrogen back-diffusion. 
- **Gas Crossover:** [Gas crossover](https://www.google.com/search?sca_esv=bc572bb3c7050c83&rlz=1C1UEAD_enUS1082US1082&cs=1&sxsrf=AHTn8zpGyImCALx0pXVFSqYcb1uEofgAfw%3A1747978743346&q=Gas+crossover&sa=X&ved=2ahUKEwj5mZeg8LiNAxVmK1kFHVA7GmIQxccNegQIFBAB&mstk=AUtExfCkV5XsDdTVOkViGP8a3o2BmI6WoG17ViXdsHoQjepPfsSKGVKO4SUHKDPT2RJFICaoj4CQosz9Qn7Y7hFruj-R_XwR_84r9C8nWPIkOCXWozHgFxDrAYkTNVjaN_yOrig97b6_kx76Nk6wP2k7p_eSMd6ezebShcNSWA-gqP8nJ_9un7tqLGUpOeNE5fllY3wRVvpf_nnlhPvpGe78yJQrpwAtIXwR9SqUq15c2VaWskTAAI-rnTPEggYFJE7S1lUaEffOwOUO8sNxrK2_Ydx0kb6lnXt6c5TGmIh24EvwcQ&csui=3), where gases (like hydrogen) pass through the membrane, can reduce Faraday efficiency. 
- **Operating Conditions:** Temperature and other operating conditions can influence Faraday efficiency.










https://www.mdpi.com/1996-1073/13/3/612

@scheepersImprovingEfficiencyPEM2020 

@scheepersImprovingEfficiencyPEM2020a 

Scheepers, F.; Stähler, M.; Stähler, A.; Rauls, E.; Müller, M.; Carmo, M.; Lehnert, W. Improving the Efficiency of PEM Electrolyzers through Membrane-Specific Pressure Optimization. _Energies_ **2020**, _13_ (3), 612. [https://doi.org/10.3390/en13030612](https://doi.org/10.3390/en13030612).

[summary and notes](https://chatgpt.com/share/68304fa3-e2b8-800c-86b0-82bacb4ae06a)



the experimental data points digitized (to the nearest visually-read value) from **Figure 3** of Scheepers et al. (2020):

parameters value from literature
The partial pressure of water at 80 ◦C was calculated by use of the Magnus approximation [44]. 
The permeability coefficient for water at the same temperature was measured by Schalenbach et al. [17,18].
The conductivity of Nafion was calculated according to Yadav and Fedkiw [34], while Shi et al. analyzed the membrane swelling [45].


> [!tldr]
> 17. Schalenbach, M.; Carmo, M.; Fritz, D.L.; Mergel, J.; Stolten, D. Pressurized PEM water electrolysis: Efficiency and gas crossover. Int. J. Hydrogen Energy 2013, 38, 14921–14933. [CrossRef]
> 18. Schalenbach, M. Corrigendum to “Pressurized PEM water electrolysis: Efficiency and gas crossover”. Int. J. Hydrogen Energy 2016, 41, 729–732. [CrossRef]

> [!tldr] 
> 
> 44. Alduchov, O.A.; Eskridge, R.E. Improved Magnus Form Approximation of Saturation Vapor Pressure. J. Appl. Meteorol. 1996, 35, 601–609. [CrossRef]
> 45. Shi, S.; Weber, A.Z.; Kusoglu, A. Structure/property relationship of Nafion XL composite membranes. J. Membr. Sci. 2016, 516, 123–134. [CrossRef]


2.6.2. Parameter Values Evaluated
The coefficients α, j0, and ax were determined from fitting experimental data at 80 ◦C and atmospheric pressure.<mark style="background: #FFF3A3A6;"> Nafion 212 has been used as the membrane (dm = 51 μm)</mark>, and <mark style="background: #FFF3A3A6;">a platinum loading of the cathode of 0.25 mg cm−2 and an iridium oxide loading of the anode of 0.96 mg cm−2 </mark>have been used. The ionomer content was set to 10 wt.%. Platinum-coated Bekaert titanium felt (350 μm) was used as the anode PTL, along with Toray carbon paper TGP-H-120. An electric resistance of 68 mΩ cm2 was measured for the cell area of 17.64 cm2 by impedance spectroscopy, which means that R0 = 27 mΩ cm2. The voltage was set to be between 0 and 1.85 V, resulting in current densities of up to 3.07 A cm−2.

![[scheepers et al params.png|0x0]]

![[scheepers param evals.png|0x0]]


---

#### Table 1 Polarization curve (Cell voltage vs. current density)


| Current Density (A/cm²) | Cell Voltage (V) |
| :---------------------: | :--------------: |
|          0.00           |       1.45       |
|          0.20           |       1.50       |
|          0.50           |       1.55       |
|          1.00           |       1.60       |
|          1.50           |       1.65       |
|          2.00           |       1.70       |
|          2.50           |       1.75       |
|          3.00           |       1.80       |
|          4.00           |       1.85       |
determined from fitting experimental data at 80 ◦C

![[image-6.png|453x352]]

---

#### Table 2 Hydrogen crossover current density, $j_x$ (A cm⁻²) vs. operating $j$


| Current Density, J (A/cm²) | Crossover Current, iₓ (mA/cm²) |
| :------------------------: | :----------------------------: |
|            0.0             |              15.0              |
|            1.0             |              3.5               |
|            2.0             |              6.5               |
|            3.0             |              8.5               |
|            4.0             |              10.5              |



---

#### Table 3 H₂ concentration in O₂, ϕ<sub>H₂</sub> (%) vs. operating $j$

| $j$ (A cm⁻²) | ϕ<sub>H₂</sub> (%) |
| ------------ | ------------------ |
| 0.00         | 2.10               |
| 0.50         | 1.90               |
| 1.00         | 1.75               |
| 1.50         | 1.65               |
| 2.00         | 1.70               |
| 2.50         | 1.80               |
| 3.00         | 1.90               |
|              |                    |
The left-hand table is the crossover current (open circles) and the right-hand table is the corresponding H₂-in-O₂ concentration (filled circles), mapped to the right axis.
Hydrogen concentration in oxygen (line) and hydrogen crossover current density (dashed) as a function of current density. The real data are shown as orange marks.

![[image-7.png|472x341]]

---

These values were read off the published scatter points a








#### 2.6.2. Parameter Values Evaluated

`The coefficients α, j0, and ax were determined from fitting experimental data at 80 °C and atmospheric pressure. Nafion 212 has been used as the membrane (dm = 51 µm), and a platinum loading of the cathode of 0.25 mg cm−2 and an iridium oxide loading of the anode of 0.96 mg cm−2 have been used. The ionomer content was set to 10 wt.%. Platinum-coated Bekaert titanium felt (350 µm) was used as the anode PTL, along with Toray carbon paper TGP-H-120. An electric resistance of 68 mΩ cm2 was measured for the cell area of 17.64 cm2 by impedance spectroscopy, which means that R0 = 27 mΩ cm2. The voltage was set to be between 0 and 1.85 V, resulting in current densities of up to 3.07 A cm−2.`

![[Research notes/Experimental validations/attachments/image.png|255x378]]

Figure 3. Top: Cell voltage as a function of current density of the real data (orange dots) and the fit (black). Bottom: Hydrogen concentration in oxygen (line) and hydrogen crossover current density (dashed) as a function of current density. The real data are shown as orange marks.



the membrane thickness and cathode pressure start at high values at low current density and then decrease to a local minimum. It is obvious that the total efficiency of the system mainly depends on the hydrogen production efficiency as the efficiency loss by hydrogen permeation across the membrane and gas compression is on the order of 5%.


![[Research notes/Experimental validations/attachments/image-2.png]]


**Figure 5.** The contribution of the hydrogen production, permeation, and permeation efficiency to the total efficiency is illustrated as a function of current density for the ideal electrolyzer (**A**) and for a voltage-limited N211-based system (**B**). Additionally, the hydrogen production efficiency is separated into electricity (Equation (3)) and heat (Equation (4)). The production efficiency curve symbolizes the minimum of heat or electrical efficiency that can be achieved.



![[Research notes/Experimental validations/attachments/image-3.png]]







## 1 Electrochemical & Thermodynamic Equations

| Equation                                                                                                     | Purpose                                          | Primary reference                                                            |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------ | ---------------------------------------------------------------------------- |
| $E_{\text{rev}}=1.229-0.0009,(T-298)$ V                                                                      | Temperature-corrected reversible voltage         | Standard H₂O-electrolysis thermodynamics; tabulated in Scheepers et al. §2.2 |
| $U_N=E_{\text{rev}}+\frac{RT}{2F}\ln!\left(\frac{\sqrt{p_{O_2}/p_0}}{p_{H_2}/p_0}\right)$                    | Nernst voltage under non-standard pressure       | Scheepers et al. Eq. (11)                                                    |
| $U_{\text{act}}=\frac{RT}{\alpha,2F}\ln!\left(\frac{j}{j_0}\right)$                                          | High-overpotential Tafel form of Butler–Volmer   | Classical electrokinetics; Scheepers et al. Eq. (13)                         |
| $U_{\text{res}}= \left(R_0+\frac{d_m\delta_m}{\sigma_m}\right)j$                                             | Ohmic loss (membrane + hardware)                 | Scheepers et al. Eq. (14)                                                    |
| $U_{\text{cell}}=U_N+U_{\text{act}}+U_{\text{res}}$                                                          | Total cell voltage                               | Scheepers et al. Eq. (10)                                                    |
| $U_{\text{load}}= \frac{p_{H_2O}}{2F}!\left(\frac{1}{p_{H_2}}+\frac{1}{2p_{O_2}}\right)!\Delta H_\text{vap}$ | Voltage equivalent of steam-loading heat         | Scheepers et al. Eq. (9)                                                     |
| $U_{\text{heat}}=1.48\text{ V}+U_{\text{load}}-U_{\text{cell}}$                                              | Heat generated from voltage difference           | Scheepers et al. (derived from)                                              |
| $\eta_{H_2,\text{el}}=\frac{1.25\text{ V}}{U_{\text{cell}}+U_{\text{heat}}}$                                 | Electro-thermal efficiency for H₂ production     | Derived from Scheepers et al. Eq. (1)                                        |
| $j_{x,H_2}=2F\frac{P_{H_2}^{T},p_{H_2}}{d_m\delta_m}+\frac{a_x}{d_m\delta_m}j$                               | H₂ crossover current density                     | Scheepers et al. Eq. (16)                                                    |
| $j_{x,O_2}\approx j_{x,H_2}$                                                                                 | O₂ crossover ($\approx$2$\times$H₂ permeability) | Schalenbach et al. 2017, IJHE 42, p. 30424                                   |
| $\eta_{F} = 1-\frac{j_x}{j}$                                                                                 | Faraday efficiency                               | Scheepers et al. Eq. (5)                                                     |
| $W_c = s_c;W_1$, $W_1=\frac{\kappa}{\kappa-1}nRT_\text{in}\left(c_c^{(\kappa-1)/\kappa}-1\right)$            | Multistage ideal-gas compression work            | Bensmann et al. 2019, Energy 173, 1225                                       |
| $\eta_{c,H_2}=1-\frac{W_c}{(n_{H_2}-n_x),\Delta H_\text{LHV}}\frac{1}{\eta_c}$                               | Compressor contribution to system efficiency     | Scheepers et al. Eq. (6)                                                     |
| $\eta_T=\eta_{H_2,\text{el}};\eta_F;\eta_{c,H_2}$                                                            | Overall system efficiency                        | Scheepers et al. Eq. (7)                                                     |

Export to Sheets

Sources

# Parameter Values

| Parameter               | Value                    | Source                               |
| ----------------------- | ------------------------ | ------------------------------------ |
| $p_{H_2O}$              | 47 948 Pa                | Saturation at 80 °C via Magnus       |
| $\Delta H_\mathrm{vap}$ | 41 572 J mol⁻¹           | Enthalpy of vaporization             |
| $P_{80°C}^{H_2}$        | 5.31×10⁻¹⁶ mol/(cm·s·Pa) | Hydrogen permeability                |
| $\sigma_m$              | 0.137 S cm⁻¹             | Nafion conductivity (Yadav & Fedkiw) |
| $\delta_m$              | 1.15                     | Membrane swelling (Shi et al.)       |
| $cc$                    | 2.75                     | Single‐stage compression ratio       |
| $T_\mathrm{in}$         | 300 K                    | Compressor inlet                     |
| $\kappa$                | 1.4                      | Heat‐capacity ratio                  |
| $\eta_c$                | 0.825                    | Compressor adiabatic eff.            |
| $p_\mathrm{out}$        | 200 bar                  | Pipeline‐typical discharge           |

Fitted (Experimental) Parameters



## 2. Numerical Parameter Set

| Symbol                         | Value used in code                     | Units           | Source / note                                      |
| ------------------------------ | -------------------------------------- | --------------- | -------------------------------------------------- |
| $T_\text{cell}$                | 80 °C (353.15 K)                       | K               | Experimental set‑point in Scheepers et al.         |
| $p_{H_2O}(80 °C)$              | 47 948                                 | Pa              | Magnus equation; Scheepers et al. Table 1          |
| $\Delta H_\text{vap}$          | 41 572                                 | J mol⁻¹         | Scheepers et al. Table 1                           |
| $\Delta H_\text{LHV}$          | 241 000                                | J mol⁻¹         | Lower heating value of H₂                          |
| $P_{H_2}^{T=80 °C}$            | 5.31 × 10⁻¹⁶                           | mol cm s⁻¹ Pa⁻¹ | Schalenbach et al. 2017; Scheepers et al.          |
| $\sigma_m(80 °C,a_m=1)$        | 0.137                                  | S cm⁻¹          | Yadav & Fedkiw 1992, J. Electrochem. Soc. 139, L68 |
| $\delta_m$ (swelling)          | 1.15                                   | –               | Shi et al. 2015, J. Membrane Sci. 492, 185         |
| $d_m$ (N212)                   | 51                                     | µm              | Nafion® 212 data‑sheet                             |
| $R_0$                          | Refined 0.0194 (orig. 0.027)           | Ω cm²           | Fitted to Fig. 3                                   |
| $j_0$                          | Refined 2.1 × 10⁻⁵                     | A cm⁻²          | Fitted (α fixed)                                   |
| $\alpha$                       | 0.43                                   | –               | Scheepers et al. Table 2                           |
| $a_x$                          | Refined 3.08 × 10⁻⁵ (orig. 1.2 × 10⁻⁵) | cm              | Fitted to crossover data                           |
| $c_c$ (stage ratio)            | 2.75                                   | –               | Bensmann et al.; Scheepers et al. Table 1          |
| $T_\text{in}$                  | 300                                    | K               | Assumed inlet temperature                          |
| $\kappa$                       | 1.40                                   | –               | Ideal‑gas γ for H₂                                 |
| $\eta_c$                       | 0.825                                  | –               | Adiabatic eff. of industrial diaphragm compressors |
| $p_\text{storage}$             | 200 (2.00 × 10⁷)                       | bar (Pa)        | Pipeline‑grade storage from Scheepers et al.       |
| $p_{H_2}=p_{O_2}$ (validation) | 1 (1.0 × 10⁵)                          | bar (Pa)        | Differential‑pressure lab tests                    |

Bold entries are the updated, best‑fit values obtained by the grid‑search refinement you requested.

**Notes on the Fitted Parameters**

* $R_0$ (ohmic hardware + contact) came out ≈ 0.019 Ω cm², lower than the 0.027 Ω cm² obtained by impedance in the paper—plausibly reflecting some extra ionic conductivity at 80 °C or a slightly smaller active area in your digitised data.
* $j_0$ (exchange current density) shifts upward (≈ 2 × 10⁻⁵ A cm⁻²) to match the kinetic “bend” in the experimental polarisation curve.
* $a_x$ (slope of crossover vs. j) increases, flattening the modelled line to overlay the measured H₂‑crossover points.
* These refined numbers can now be inserted into the full efficiency code (already demonstrated) for tighter agreement with Scheepers et al.’s figures.







# Glossary of Symbols (Scheepers et al., 2020)

glossary of all the symbols (keys) used in Scheepers et al. (2020) along with their definitions:

| Symbol          | Definition                                                               |
|-----------------|--------------------------------------------------------------------------|
| $\Delta H$      | Total enthalpy change for splitting liquid water ($\approx$ 286 kJ mol⁻¹) |
| $\Delta G$      | Gibbs free energy change for splitting liquid water ($\approx$ 237 kJ mol⁻¹) |
| $T \Delta S$    | Entropic heat term in the water-splitting reaction                       |
| $E^0_{\text{rev}}$ | Standard reversible cell voltage at 298 K (1.229 V)                      |
| $U_N$           | Nernst (reversible) voltage under actual gas pressures                   |
| $U_{\text{act}}$ | Activation overpotential (kinetic loss)                                  |
| $U_{\text{res}}$ | Resistive (ohmic) overpotential                                          |
| $U_{\text{cell}}$ | Total electrochemical cell voltage: $U_N + U_{\text{act}} + U_{\text{res}}$ |
| $U_{\text{load}}$ | Voltage equivalent of water-vapor loading heat to saturate product gases |
| $U_{\text{heat}}$ | Equivalent “heating” (if >0) or “cooling” (if <0) voltage                |
| $\eta_{pH_2,\text{el}}$ | Electrical-only hydrogen production efficiency: 1.25 V / $U_{\text{cell}}$ |
| $\eta_{pH_2,\text{heat}}$ | Heat-only hydrogen production efficiency: 1.25 V / (1.48 V + $U_{\text{load}}$) |
| $j$             | Operating current density (A cm⁻²)                                       |
| $j_x$           | Total crossover current density: $j_{x,H_2} + j_{x,O_2}$                   |
| $j_{x,H_2}$     | Hydrogen crossover current density across the membrane                   |
| $j_{x,O_2}$     | Oxygen crossover current density ($\approx$ equal to $j_{x,H_2}$)         |
| $\eta_{F,H_2}$  | Faraday efficiency: $1 - (j_x / j)$                                      |
| $W_c$           | Total compression work for pressurizing hydrogen to storage pressure     |
| $\eta_{c,H_2}$  | Compression efficiency factor: $1 - [W_c / ((n_{H_2}-n_x)\Delta H_{\text{LHV}})] \times 1/\eta_c$ |
| $\eta_T$        | Overall system efficiency: $\eta_{pH_2} \cdot \eta_{F,H_2} \cdot \eta_{c,H_2}$ |
| $R_0$           | Hardware/contact ohmic resistance (Ω cm²)                                |
| $d_m$           | Membrane thickness (cm)                                                  |
| $\delta_m$      | Membrane swelling factor (–)                                             |
| $\sigma_m$      | Membrane ionic conductivity (S cm⁻¹)                                     |
| $P^T_{H_2}$     | Hydrogen permeability coefficient (mol cm⁻¹ s⁻¹ Pa⁻¹)                     |
| $a_x$           | Linear current-dependent crossover coefficient (cm)                      |
| $c_c$           | Compression ratio per stage (–)                                          |
| $s_c$           | Number of compression stages: $\log(p_{\text{storage}}/p_{\text{cat}})/\log(c_c)$ |
| $\kappa$        | Gas heat capacity ratio ($C_p/C_v$) (–)                                  |
| $Z$             | Gas compressibility factor (–)                                           |
| $p_{\text{cat},H_2}$ | Cathode H₂ partial pressure (Pa)                                         |
| $p_{\text{an},O_2}$ | Anode O₂ partial pressure (Pa)                                           |
| $p_{H_2O}$      | Water-vapor partial pressure at 80 °C ($\approx$ 4.7948 $\times$ 10⁴ Pa) |
| $p_{\text{storage}}$ | Final hydrogen storage pressure (200 bar $\approx$ 2 $\times$ 10⁷ Pa)   |
| $F$             | Faraday constant (96 485 C mol⁻¹)                                        |
| $R$             | Universal gas constant (8.314 J mol⁻¹ K⁻¹)                               |
| $T_{\text{cell}}$ | Electrolyser operating temperature (353.15 K) (80 °C)                     |
| $T_{\text{in}}$ | Inlet gas temperature to compressors (300 K)                             |
| $\Delta H_{\text{vap}}$ | Enthalpy of vaporization of water (41 572 J mol⁻¹)                       |
| $\Delta H_{\text{LHV}}$ | Lower heating value of hydrogen (241 000 J mol⁻¹)                        |



The paper **"Improving the Efficiency of PEM Electrolyzers through Membrane-Specific Pressure Optimization" (Energies 2020, 13, 612)** provides a comprehensive model and experimental validation for optimizing PEM electrolyzer efficiency, particularly with respect to **membrane thickness and cathode pressure**.

---

### 🔬 **Experimental Setup and Key Parameters**

* **Membrane Used:** Nafion 212 (thickness = 51 µm)
* **Operating Temp:** 80 °C
* **Cell Area:** 17.64 cm²
* **Cathode Catalyst:** Pt 0.25 mg/cm²
* **Anode Catalyst:** IrO₂ 0.96 mg/cm²
* **Anode PTL:** Pt-coated Bekaert Ti felt (350 µm)
* **Cathode PTL:** Toray carbon paper TGP-H-120
* **Measured Cell Resistance ($R_0$):** 27 mΩ·cm²
* **Tested Voltage Range:** Up to 1.85 V (3.07 A/cm² max current density)

**Fitted Parameters (Table 2 in the paper):**

* Transfer coefficient $\alpha$ = 0.43
* Exchange current density $j_0$ = 8 × 10⁻⁶ A/cm²
* Crossover slope constant $a_x$ = 1.2 × 10⁻⁵ cm

---

###  **Modeling Equations & Submodels**

#### 1. **Total Efficiency Model**:

$\eta_T = \eta_{H2,el} \cdot \eta_{F,H2} \cdot \eta_{c,H2}$

#### 2. **Hydrogen Production Efficiency**:

$\eta_{H2,el} = \frac{1.25\ \text{V}}{U_{\text{heat}} + U_{\text{cell}}}$
or
$\eta_{H2,el} = \frac{1.25\ \text{V}}{U_{\text{cell}}}$ (if no external heat)

Where:

* $U_{\text{heat}} = |1.48\ \text{V} + U_{\text{load}} - U_{\text{cell}}|$
* $U_{\text{load}} = \frac{p_{\text{H}_2O}}{2F} \left( \frac{1}{p_{H2}} + \frac{1}{2p_{O2}} \right) \Delta H_{\text{vap}}$

#### 3. **Faraday Efficiency**:

$\eta_{F,H2} = 1 - \frac{j_x}{j}$ with $j_{x,H2} = \frac{2F \cdot P^T_{H2} \cdot p_{H2}}{d_m \cdot \delta_m} + \frac{a_x}{d_m \cdot \delta_m} \cdot j$

#### 4. **Voltage Model**:

$U_{\text{cell}} = U_N + U_{\text{act}} + U_{\text{res}}$

* Nernst Voltage:
    $U_N = E^0_{\text{rev}} + \frac{RT}{2F} \ln\left( \frac{\sqrt{p_{O2}}}{p_{H2}} \right)$
* Activation Overpotential:
    $U_{\text{act}} = \frac{RT}{\alpha z F} \ln\left( \frac{j}{j_0} \right)$
* Ohmic Resistance:
    $U_{\text{res}} = \left(R_0 + \frac{d_m \delta_m}{\sigma_m} \right) j$

#### 5. **Compression Efficiency**:

$\eta_{c,H2} = 1 - \frac{W_c}{(n_{H2} - n_x) \Delta H_{\text{LHV}}} \cdot \frac{1}{\eta_c}$

---

### 📊 **Key Experimental Results for Validation**

* **Figure 3 (Voltage vs. Current Density and Crossover):** Real data and model fit up to 3.07 A/cm².
* **Figure 6 (Efficiency vs. Current Density):** Comparison for Nafion N211, N212, N115, N117 at voltages $\leq$ 2 V.
* **Figures 7 & 8:** Show how total efficiency varies with current density under different compression stages and membrane types (N117 and N212).






------

Techno-economic analysis and Monte Carlo simulation of green hydrogen production technology through various water electrolysis technologies 
Dohyung Jang a
@jangTechnoeconomicAnalysisMonte2022


![[image-8.png|352x241]]

| Current Density (A/cm²) | Cell Voltage (V) |
| :---------------------: | :--------------: |
|          0.00           |       1.35       |
|          0.05           |       1.45       |
|          0.10           |       1.56       |
|          0.20           |       1.60       |
|          0.30           |       1.65       |
|          0.40           |       1.70       |
|          0.50           |       1.75       |
|          0.60           |       1.80       |
|          0.80           |       1.90       |
|          1.00           |       1.98       |
|          1.20           |       2.08       |
|          1.40           |       2.18       |
|          1.60           |       2.25       |
|          1.80           |       2.35       |
|          2.00           |       2.45       |



![[image-9.png|429x319]]


| Current Density (A/cm²) | Cell Voltage (V/cell) |
| :---------------------: | :-------------------: |
|          0.00           |         1.42          |
|          0.05           |         1.53          |
|          0.10           |         1.57          |
|          0.15           |         1.60          |
|          0.20           |         1.63          |
|          0.30           |         1.72          |
|          0.40           |         1.78          |
|          0.60           |         1.83          |
|          0.80           |         1.90          |
|          1.00           |         1.98          |
|          1.20           |         2.00          |
|          1.40           |         2.04          |
|          1.60           |         2.08          |
|          1.80           |         2.15          |
|          2.00           |         2.22          |
|          2.20           |         2.27          |
|          2.40           |         2.35          |



-----

MIT
@chungDesignSpacePEM2024





# Electrochemical Model Equations for PEM Electrolyzers

Below is a consolidated list of all the electrochemical model equations (excluding any compression‐related ones) and the key parameters with their values and units, drawn from the Supplementary Information of Chung et al. (2021).

## Electrolyzer Cell Voltage Model

### Overall Cell Voltage

$$V=E+\eta_{ohm}+\eta_{act}$$

* $V$: cell voltage (V)
* $E$: thermodynamic (open‐circuit) voltage (V)
* $\eta_{ohm}$: ohmic overpotential (V)
* $\eta_{act}$: activation overpotential (V)

### Thermodynamic Voltage

$$E = -\dfrac{\Delta G}{nF}$$

* $\Delta G$: Gibbs free energy change (J mol⁻¹)
* $n$: number of electrons transferred (2 for water splitting)
* $F$: Faraday’s constant (96 485 C mol⁻¹)

### Gibbs Free Energy Change

$$\Delta G = G_{\rm H_2}(T_{\rm cat},P_{\rm cat}) + \tfrac12\,G_{\rm O_2}(T_{\rm an},P_{\rm an}) - G_{\rm H_2O}(T_{\rm an},P_{\rm an})$$

## Thermodynamic Property Corrections

### Enthalpy vs. Temperature

$$H(T,1\text{ bar}) - H(298 \mathrm K,1\text{ bar}) = a\,(T-T_0) + \tfrac b{10^3}(T^2 - T_0^2) - \tfrac c{10^5}\Bigl(\tfrac1T - \tfrac1{T_0}\Bigr) - \tfrac e{10^8}\Bigl(\tfrac1{T^2} - \tfrac1{T_0^2}\Bigr)$$

* $T_0 = 298$ K
* Coeffs $a,b,c,e$ in Table S1

### Entropy vs. Temperature

$$S(T,1\text{ bar}) - S(298 \mathrm K,1\text{ bar}) = a\,(\ln T - \ln T_0) + \tfrac b{10^3}(T-T_0) - \tfrac c{10^5}\Bigl(\tfrac1{T^2} - \tfrac1{T_0^2}\Bigr) - \tfrac e{10^8}\Bigl(\tfrac1{T^3} - \tfrac1{T_0^3}\Bigr)$$

* Coeffs $a,b,c,e$ in Table S1

### Pressure Correction (Virial Expansion)

$$G(T,P) - G(T,1\text{ bar}) = RT\ln P + B\,P + \frac{C - B^2/(2RT)}{2}\,P^2$$
$$B = b_1 + \frac{b_2}{T},\quad C = c_1 + \frac{c_2}{T^2}$$

* Virial coeffs in Table S2

## Ohmic Overpotential

### Membrane Resistance

$$R_{\rm mem} = \frac{t}{\sigma_{\rm mem}}$$

* $t$: membrane thickness (m)
* $\sigma_{\rm mem}$: membrane conductivity (S m⁻¹)

### Membrane Hydration Factor

$$\lambda_{m} = 0.043 + 17.81\,a_{\rm H_2O} - 39.85\,a_{\rm H_2O}^2 + 36\,a_{\rm H_2O}^3$$

* $a_{\rm H_2O}$: water activity ($\approx 1$ under liquid‐fed conditions)

### Membrane Conductivity

$$\sigma_{\rm mem} = \bigl(0.00514\,\lambda_{m} - 0.00326\bigr) \exp\!\bigl[\,1268\bigl(\tfrac1{303} - \tfrac1T\bigr)\bigr]$$

* $T$: temperature (K)

## Activation Overpotential

### Butler–Volmer (General Form)

$$j = j_0\Bigl[\exp\!\bigl(-\tfrac{\alpha_1 F\eta_{\rm act}}{RT}\bigr) - \exp\!\bigl(\tfrac{\alpha_2 F\eta_{\rm act}}{RT}\bigr)\Bigr]$$

* $j$: current density (A cm⁻²)
* $j_0$: exchange current density (A cm⁻²)
* $\alpha_{1,2}$: charge transfer coefficients

### Tafel (sinh) Approximation

$$\eta_{\rm act} = \frac{RT}{\alpha\,z\,F}\,\sinh^{-1}\!\Bigl(\tfrac{j}{2\,j_0}\Bigr)$$

* Often $\alpha_1=\alpha_2=\alpha$

### Temperature Dependence of $j_0$

$$j_0 = j_{0,\rm ref}\,\exp\!\Bigl[\frac{E_{\rm act}}{R}\Bigl(\tfrac1{T_{\rm ref}} - \tfrac1T\Bigr)\Bigr]$$

* $j_{0,\rm ref}$: reference exchange current density at $T_{\rm ref}$
* $E_{\rm act}$: activation energy (J mol⁻¹)

### Total Activation Overpotential (Anode + Cathode)

$$\eta_{\rm act,total} = \frac{RT}{F}\!\Bigl[\frac{1}{\alpha}\sinh^{-1}\!\bigl(\tfrac{j}{2\,j_{0,\rm an}}\bigr) + \frac{1}{\alpha}\sinh^{-1}\!\bigl(\tfrac{j}{2\,j_{0,\rm cat}}\bigr)\Bigr]$$

## Key Parameter Tables

### Table S1: Temperature‐Correction Coefficients

| | $a$ | $b$ | $c$ | $e$ |
|---|---|---|---|---|
| H₂ (g) | 26.5 | 73.7 | 1.17 | – |
| O₂ (g) | 34.35 | 1.92 | – | 18.45 | 4.06 |

### Table S2: Virial Coefficients (up to 1000 atm)

| | $b_1$ | $b_2$ | $c_1$ | $c_2$ |
|---|---|---|---|---|
| H₂ (g) | 20.5 | –1 857 | –35 | 112 760 |
| O₂ (g) | 42.6 | –17 400 | –2 604 | 61 457 |

### Table S3: Exchange Current & Activation Energy

| Value | Units |
|---|---|
| $j_{0,\rm ref,\,cat}$ | 0.75 × 10⁻³ | A cm⁻² |
| $E_{\rm act,\,cat}$ | 30 000 | J mol⁻¹ |
| $j_{0,\rm ref,\,an}$ | 1.0 × 10⁻⁷ | A cm⁻² |
| $E_{\rm act,\,an}$ | 90 000 | J mol⁻¹ |
| $T_{\rm ref}$ | 318 | K |

## Validation‐Experiment Parameters

### Table S4: Single‐Cell (Nafion 117, 178 µm) @ 60 °C & 80 °C, 1 bar

* $t=178$ µm
* $R_{\rm elec} = 0$ Ω
* $T = 60, 80$ °C
* $P_{\rm cat} = P_{\rm an} = 1$ bar

### Table S5: Stack (Nafion 110, 254 µm) @ 55 °C, 10 bar

* $t=254$ µm
* $R_{\rm elec} = 2.5\times10^{-5}$ Ω
* $j_{0,\rm cat} = 1.1\times10^{-3}$ A cm⁻²
* $j_{0,\rm an} = 2.87\times10^{-7}$ A cm⁻²
* $T = 55$ °C, $P_{\rm cat}=10$ bar, $P_{\rm an}=1$ bar

### Table S6: Stack @ 40 °C, 70 bar

* $t=254$ µm
* $R_{\rm elec} = 2.5\times10^{-5}$ Ω
* $j_{0,\rm cat} = 0.6\times10^{-3}$ A cm⁻²
* $j_{0,\rm an} = 5.9\times10^{-8}$ A cm⁻²
* $T = 40$ °C, $P_{\rm cat}=70$ bar, $P_{\rm an}=1$ bar

### Table S7: Tech‐State Scenarios

| Scenario                                             | $t$ (µm) | $T$ (°C) | $P_{\rm cat}$ (bar) | $P_{\rm an}$ (bar) | $j_{\rm min}$ (A cm⁻²) |
| ---------------------------------------------------- | -------- | -------- | ------------------- | ------------------ | ---------------------- |
| (Details not provided in original text, placeholder) |          |          |                     |                    |                        |

These constitute the fundamental electrochemical equations and parameter values needed to implement and validate a Python‐based PEM electrolyzer model (excluding any compression submodels).








-----
----


inspo: @hanElectrochemicalPerformanceModeling2015

# PEM Electrolyzer Model Equations (Han et al., 2015)

Below is a consolidated list of all the governing equations from Han et al. (2015) and the key parameters (with values) they use in their PEM electrolyzer model.
with sensitivity analysis

![[image-11.png|419x282]]

![[image-10.png|453x238]]


## Model Equations

### Total Cell Voltage

$$V=V_{\rm ocv} + V_{\rm act} + V_{\rm diff} + V_{\rm ohm} \tag{1}$$

### Open-Circuit (Reversible) Voltage

$$V_{\rm ocv} = V^0 + \frac{R\,T}{zF} \ln\!\biggl(\frac{a_{\rm H_2}}{a_{\rm O_2}^{0.5}\,a_{\rm H_2O}}\biggr) \tag{2}$$

with

$$V^0 = 1.229 - 0.9\times10^{-3}\,(T - 298.0) \tag{3}$$

### Activation Overpotential

$$V_{\rm act} = V_{\rm act,a} + V_{\rm act,c} \tag{4}$$

where (Butler–Volmer form)

$$V_{\rm act,a} = \frac{R\,T_a}{\alpha_a F}\,\sinh^{-1}\!\Bigl(\frac{j}{2\,j_{0,a}}\Bigr) \tag{5}$$
$$V_{\rm act,c} = \frac{R\,T_c}{\alpha_c F}\,\sinh^{-1}\!\Bigl(\frac{j}{2\,j_{0,c}}\Bigr) \tag{6}$$

### Diffusion Overpotential

$$V_{\rm diff} = V_{\rm diff,a} + V_{\rm diff,c} = \frac{R\,T_a}{4F}\ln\!\Bigl(\frac{C_{O_2,m}}{C_{O_2,m}^0}\Bigr) + \frac{R\,T_c}{2F}\ln\!\Bigl(\frac{C_{H_2,m}}{C_{H_2,m}^0}\Bigr) \tag{16}$$

with species flows and concentrations defined by:

$$\begin{aligned}
n_{\rm H_2O, reaction} &= \frac{j}{2F}, & n_{\rm H_2O, ce} &= D_w\,\frac{C_{H_2O,m,c}-C_{H_2O,m,a}}{d_m} + n_d\frac{j}{F},\\
n_{\rm H_2O, pressure} &= \frac{K_{\rm darcy}\,A\,m_{H_2O}\,V_p}{\rho_{H_2O}\,M_{m,H_2O}}, & n_{O_2} &= \frac{j}{4F},\quad n_{H_2} = \frac{j}{2F},
\end{aligned} \tag{7–11}$$

$$
\begin{aligned}
  C_{O_2,m} &= \frac{P_a\,n_{O_2}}{n_{O_2}+n_{H_2O,a}}\frac{1}{R\,T_a}
    + \frac{d_{e,a}}{D_{\rm eff,a}}\,n_{O_2},\\
  C_{H_2,m} &= \frac{P_c\,n_{H_2}}{n_{H_2}+n_{H_2O,c}}\frac{1}{R\,T_c}
    + \frac{d_{e,c}}{D_{\rm eff,c}}\,n_{H_2},
\end{aligned}
\tag{12–13}
$$

and

$$D_{\rm eff,1-2} = D_{1-2}\,\varepsilon\,\Bigl(\tfrac{\varepsilon-\varepsilon_p}{1-\varepsilon_p}\Bigr)^a \tag{14}$$
$$D_{1-2} = a\,\frac{T^{\,b}}{\sqrt{T_{c1}T_{c2}}^b} \,\frac{(p_{c1}p_{c2})^{-1/3}(T_{c1}T_{c2})^{5/12}}{P}. \tag{15}$$

### Ohmic Overpotential

$$V_{\rm ohm} = V_{\rm ohm,a} + V_{\rm ohm,c} + V_{\rm ohm,m} = \bigl[R_{p,a}+R_{e,a}+R_{in,a}\bigr]\,j\,A + \bigl[R_{p,c}+R_{e,c}+R_{in,c}\bigr]\,j\,A + R_m\,j\,A \tag{17}$$

with sub-resistances:

$$
\begin{aligned}
  R_{p1} &= \rho_p\,\frac{L_{ab}}{A}, & R_{p2} &= \rho_p\,\frac{L_{bc}}{0.5\,L_{ik}L},\\
  R_{e1} &= \rho_e\,\frac{0.25\,L_{kl}}{d_e\,L\,(1-\varepsilon)}, &
  R_{e2} &= \rho_e\,\frac{d_e}{0.5\,L_{ik}L\,(1-\varepsilon)},\\
  R_{e3} &= \rho_e\,\frac{d_e}{L_{kl}L\,(1-\varepsilon)},\quad&
  V_{\rm ohm,m} &= \frac{d_m\,j}{\sigma_m},
\end{aligned}
\tag{18–23}
$$

and the membrane conductivity

$$ \sigma_m = (0.005139\,\ell - 0.00326)\, \exp\!\Bigl[1268\bigl(\tfrac1{303}-\tfrac1T\bigr)\Bigr]. \tag{24}$$

## Key Parameters and Values

### Exchange Current Densities (Table 1)

| Catalyst                | $j_{0,a}$ (A cm⁻²) | $j_{0,c}$ (A cm⁻²) | Source               |
| ----------------------- | ------------------ | ------------------ | -------------------- |
| Pt–Ir anode, Pt cathode | 1.0 × 10⁻¹²        | 1.0 × 10⁻³         | Choi et al. [17]     |
| Pt–Ir anode, Pt cathode | 1.65 × 10⁻⁸        | 9.0 × 10⁻²         | Harrison et al. [30] |
| Pt–Ir anode, Pt cathode | 1.0 × 10⁻⁷         | 1.0 × 10⁻³         | Marangio et al. [22] |

### Initial Model Parameters (Table 2)

| Parameter                     | Symbol                       | Value                               | Unit             |
| ----------------------------- | ---------------------------- | ----------------------------------- | ---------------- |
| Faraday constant              | $F$                          | 96485.0                             | C mol⁻¹          |
| Gas constant                  | $R$                          | 8.314                               | J mol⁻¹ K⁻¹      |
| Temperature                   | $T$                          | 353.15                              | K                |
| Pressure (anode / cathode)    | $P_a$, $P_c$                 | 1.0 / 13.6                          | atm              |
| Max current density           | $j_{\max}$                   | 2.0                                 | A cm⁻²           |
| Exchange current density      | $j_{0,a}$, $j_{0,c}$         | 2.0 × 10⁻⁶ / 1.0 × 10⁻¹             | A cm⁻²           |
| Electrode thickness           | $d_e$                        | 200                                 | µm               |
| Porosity                      | $\varepsilon$                | 0.30                                | —                |
| Membrane thickness            | $d_m$                        | 178                                 | µm               |
| Titanium resistivity          | $\rho_{\rm Ti}$              | 5.0 × 10⁻³                          | Ω cm             |
| Carbon-paper resistivity      | $\rho_{\rm CP}$              | 80.0 × 10⁻³                         | Ω cm             |
| Charge transfer coeffs.       | $\alpha_a$, $\alpha_c$       | 2.0 / 0.5                           | —                |
| Water viscosity               | $\mu_{H_2O}$                 | 3.55 × 10⁻⁸                         | N s cm⁻²         |
| Water density                 | $\rho_{H_2O}$                | 1.0                                 | g cm⁻³           |
| Channel dims.                 | $L_{ab}, L_{bc}, L_{ik}$     | 2.0, 1.0, 1.0                       | mm               |
| MEA area                      | $A$                          | 5.0                                 | cm²              |
| Membrane humidification       | $\ell$                       | 22                                  | —                |
| GDL porosity (ref)            | $\varepsilon_p$              | 0.11                                | —                |
| Empirical coeffs. (diffusion) | $a, b$                       | 0.785, 2.334                        | —                |
| Critical pressures            | $P_{cr}$ (H₂O, O₂, H₂)       | 218.3, 49.7, 12.8                   | atm              |
| Critical temps.               | $T_{cr}$ (H₂O, O₂, H₂)       | 647.3, 154.4, 33.3                  | K                |
| Molar masses                  | $M_m$ (H₂O, O₂, H₂)          | 18, 32, 2                           | g mol⁻¹          |
| Electro-osmotic drag coeff.   | $n_d$                        | (model-fitted)                      | mol H₂O mol⁻¹ e⁻ |
| Water diffusivity             | $D_w$                        | (model-fitted)                      | cm² s⁻¹          |
| Darcy permeability            | $K_{\rm darcy}$              | (model-fitted)                      | m²               |
| Ref. concentrations           | $C_{O_2,m}^0$, $C_{H_2,m}^0$ | (model-fitted)                      | mol cm⁻³         |
| Porous-electrode diffusivity  | $D_{\rm eff}$                | (function of $\varepsilon, T$ etc.) | m² s⁻¹           |


In this validation case, the corresponding operating temperature value was 80 C and the PEM thickness was 178 microns. The values of the exchange current density and membrane humidification are used to adjust and optimize the present model so that the model data could better fit the experimental data. Fig. 4 presents the comparison of the present model and experimental data of PEM electrolyzer cell polarization curve under the same pressure, temperature and membrane thickness. The numerical results obtained from the present model show good agreement with the experimental data


- Model validation
![[image-12.png|308x330]]

Sensitivity analysis 
Effects of exchange current density on the polarization curve
Effects of temperature on the polarization curve
pressure on the polarization curve
Effects of electrode  on the polarization curve
membrane thickness on the polarization curve


Effects of interfacial resistance

Fig. 11 e Effects of the membrane thickness on the polarization curve

Experimental data source.
Debe M, Hendricks S, Vernstrom G, Meyers M, Brostrom M, Stephens M, et al. Initial performance and durability of ultralow loaded NSTF electrodes for PEM electrolyzers. J Electrochem Soc 2012;159(6):K165e76
@debeInitialPerformanceDurability2012



Below is an approximate extraction of the experimental (red‐square) polarization data from your figure, digitized by locating each marker and mapping from pixel → data coordinates. There are 15 usable points:

| Current density, i (A/cm²) | Cell voltage, V (V) |
|---|---|
| 0.14 | 1.543 |
| 0.24 | 1.584 |
| 0.33 | 1.607 |
| 0.47 | 1.619 |
| 0.54 | 1.663 |
| 0.58 | 1.650 |
| 0.80 | 1.692 |
| 0.96 | 1.723 |
| 1.10 | 1.748 |
| 1.24 | 1.773 |
| 1.34 | 1.791 |
| 1.46 | 1.811 |
| 1.59 | 1.832 |
| 1.72 | 1.853 |
| 1.84 | 1.874 |



```python
i_exp = [0.14, 0.24, 0.33, 0.47, 0.54, 0.58, 0.80, 0.96, 1.10, 1.24, 1.34, 1.46, 1.59, 1.72, 1.84]
V_exp = [1.543, 1.584, 1.607, 1.619, 1.663, 1.650, 1.692, 1.723, 1.748, 1.773, 1.791, 1.811, 1.832, 1.853, 1.874]


i_exp = [0.14, 0.24, 0.33, 0.47, 0.54, 0.58, 0.80, 0.96, 1.10, 1.24, 1.34, 1.46, 1.59, 1.72, 1.84]
V_exp = [1.543,1.584,1.607,1.619,1.663,1.650,1.692,1.723,1.748,1.773,1.791,1.811,1.832,1.853,1.874]
```







Summary on sensitivity


Effects of exchange current density

It is found that when exchange current density becomes small, the total voltage increases significantly, which means the electrolyzer performance decreases.
As shown in Fig. 6, decreasing the exchange current density from 101 to 105 A/cm2 can result in larger differences of the voltage than those at the anode

Optimization of the CL can improve electrolyzer performance since the exchange current density is dependent on catalyst properties [23].
![[image-13.png]]

![[image-14.png]]



Effects of temperature and pressure
. In terms of the theoretical analysis (Eq. (5) and Eq. (6)), when increasing the operating temperature, only the activation overpotential increases whereas other voltage values decrease.

The results confirm that increasing the operating temperature from 40 to 80 C could result in voltage decrease and consequently improve the performance of PEM electrolyzer cells.


![[image-15.png]]


Effect of pressure on 
It can be seen that a higher operating pressure at the cathode lead to a higher voltage. The voltage at 1.5 A/cm2 is 1.75 V for a pressure of 1 atm and 1.8 V for a pressure of 5 atm. There are two explanations for such result.
First, a high operating pressure would directly result in an increase in the open circuit voltage.
Two. increasing species partial pressure may prevent water diffusion inside the electrode and membrane, which consequently increases diffusion loss.

![[image-16.png]]



Effects of electrode and membrane thickness

electrolyzer cells becomes worse with an increase in electrode thickness, as shown in Fig. 9. 
This is because a thicker electrode leads to both higher diffusion and ohmic losses.


![[image-17.png]]


![[image-18.png]]

