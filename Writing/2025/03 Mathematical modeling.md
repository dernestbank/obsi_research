---
keywords: overpotentials in anode and cathode. Nerst equation , butlervolmer equation, mass transport of hydrogen, water, oxygen, overcrossing, faradays's efficiency. geometrical parameters( cell area, electrode and electrolyte thickness, number of channels , flow field plate thickness,...) electrode parameters(thickness, porosity , tortuosity, pore radius , resistivity, ESCA etc...) electrode parameters( Membrane Parameter, Thickness, Porosity, Tortuosity, Wetness factor, Oxygen diffusivity, Hydrogen diffusivity, Weight percent of water, Darcy's constant for water crossover, Bruggeman's exponent, electroosmotic drag coefficient, diffusion, fouling resistant, voltage loss, shunt loss function)
---


**To dos**
- [x] Electrochemical model
	- [x] efficiency, overpotentials, mass transport faradays efficiency
- [x] Mass transport model
- [x] Cost model
	- [x] Cost of Electrolyzer model
		- [ ] @ badget et al plot 
		- [x] @ astriani 
	- [ ] Cost of BoP
	- [x] Cost of Energy system
- [x] Energy system model
- [x] performance effect
- [x] montecarlo and uncertainty analysis
- [x] reformat equation tags \tag{2}
- [ ] Key for all variables and symbols
----

The design and assembly of the PEM Electrolyser cell is described and the method of implementing the RE is described in detail

## 3.1 Electrolyzer and Electrochemical Module


The core of PEM electrolysis involves splitting water molecules into oxygen and hydrogen.

$$ H_{2}O \rightarrow H_{2}+ 1/2 O_{2} \tag{1}$$

The reaction occurs in two half cells. First, the catalyst at the anode initiates the Oxygen Evolution Reaction (OER) to produce protons ($H^+$).

$$H_{2}O_{(l)} \rightarrow 1/2 O_{2}{(g)} + 2H^{+} + 2e^{-} \tag{2}$$ The protons then migrate to the cathode half-cell to be reduced through a Hydrogen Evolution Reaction to produce hydrogen molecules.

$$2H^{+} + 2e^{-} \rightarrow H_{2}{(g)} \tag{3} $$

It is an endothermic reaction because the energy difference between products and reactants is positive. The enthalpy of the reaction includes both electrical and thermal energy, with electrical energy prevailing in low-temperature electrolytic systems (< $100 ^oC$). Conversely, in high-temperature electrolytic systems operating between 700 °C and 1000 °C, such as in SOEC, the reaction is driven by supplied heat, which reduces electricity consumption.

$$\Delta H = \Delta G + T \cdot \Delta S \tag{4}$$

To overcome the resistance to flow of protons in the cell, additional potential must be generated. The total cell voltage needed for the electrochemical reaction is the sum of the ideal voltage and the overpotentials caused by the cell's design. Overpotential arises from the electrode and electrolyte materials. @bessarabovPEMElectrolysisHydrogen2016

Theoretically, the minimum voltage required to initiate the reaction under ideal conditions, without any energy losses, is: z, the number of moles of electrons transferred (z=2) $$ V_{rev}= \frac{\Delta G}{zF} = 1.23 \tag{5} $$

The voltage needed to sustain the electrochemical reaction at a constant temperature—where the heat produced by the reaction exactly equals the heat consumed—is the thermoneutral voltage, given as: $$ V_{th}= \frac{\Delta H}{zF} = 1.48\text{ V} \tag{6} $$


----
### The Open circuit / reversible voltage
The Nernst equation relates the system temperature and pressure thus the reversible open-circuit voltage.  At standard conditions (1 atm, 298 K) with liquid water product, $V \approx 1.229$ V @carmoComprehensiveReviewPEM2013 . 
$$
V_{\text{rev}} = V^0_{rev} + \frac{RT}{zF} \ln\left(\frac{\alpha_{\text{H}_2} \sqrt{\alpha_{\text{O}_2}}}{\alpha{\text{H}_2O}}\right) \tag{7}
$$

where $V^0$ is the standard potential ($\approx 1.23$ V for the PEM reaction), $R$ is the gas constant, $F$ is Faraday’s constant, and $a_i$ are the activities of $\text{H}_2$, $\text{O}_2$, and $\text{H}_2\text{O}$. 
For gases, $\alpha_{\text{gas}} \approx \frac{p_{\text{gas}}}{p^0}$ (ratio of partial to standard pressure) and for liquid water $\alpha_{\text{H}_2O} \approx 1$. 
$${V_{rev} = V_{rev}^{0} + \frac{RT}{zF}\ln\left(\frac{p_{H_{2}} \cdot \sqrt{ p_{O_{2}}}}{\alpha_{H_{2}O}}\right)} \tag{8}$$
 The partial pressures of the products, hydrogen $𝑝_{𝐻_{2}}$ and oxygen $𝑝_{𝑂_{2}}$ , are 0.53 and 0.47 bar respectfully.   The reversible voltage at STP is related as @carmoComprehensiveReviewPEM2013 :
$$V_{rev}^{0} = 1.229-0.09 \times 10^{-3}(T-298.0) \tag{9}$$ 
Pressure has a lesser effect on the $V_{r}$ than temperature due to the logarithmic term. Therefore, increasing hydrogen or oxygen pressure raises the open-circuit voltage, while accumulating product water (e.g., vapor) lowers it. Temperature dependence enters through $V^0(T)$, with a more detailed form including entropy change $\Delta S$:


### Activation Overpotentials 
There is a voltage drop when current flows between the two half-cells due to kinetic inefficiencies. The drop is described by the Butler-Volmer equation as the activation overpotential. The activation overpotential ($V_{act}$) results from the energy required to drive a slow reaction step. The reaction at the anode half-cell limits the kinetics and is the main contributor to the total activation overpotential, while the Pt/C catalyst influences the faster kinetics at the cathode. @awasthiDynamicModelingSimulation2011

When the reaction reaches a steady state, the current at the anode and cathode is equal; this current density is called the exchange current density ($i_{0}$) and depends mainly on the materials used in the design.

The exchange current density ($i_{o}$), as referenced, is given by $i_{o,an} =K_{io,an}.exp⁡(\frac {E_{act,an}}{R.T})$ is referenced to the pre-exponential factor ($K_{i_o}$) measured in $21600000$ A/cm² and the activation energy ($E_{act,anode}$) at 76,000 J/mol. [@crespiExperimentalTheoreticalEvaluation2023] 



$$
i = i_0 \left[ \exp\left(\frac{\alpha_a zF V_{\text{act}}}{RT}\right) - \exp\left(\frac{-\alpha_c zF V_{\text{act}}}{RT}\right) \right] \tag{10}
$$
$\alpha_a$, $\alpha_c$ are anodic and cathodic charge transfer coefficients ( $\alpha_a= 2.0$, $\alpha_c= 0.5$), applicable to both the anode (hydrogen oxidation) and cathode (oxygen reduction) reactions @marangioDirectHighPressure2009; @carmoComprehensiveReviewPEM2013.

The oxygen anode, $i_{0,\text{anode}}$, is several orders of magnitude lower than $i_{0,\text{cathode}}$, making the anode activation loss dominant [@espinosa-lopezModellingExperimentalValidation2018]; [@garcia-valverdeSimplePEMWater2012]. Enhancing the anode exchange current density ($i_0$) to effectively accelerate the oxygen evolution reaction (OER) can reduce the overpotential ($V_{act,anode}$). Exchange current density and activation energy values for both the cathode and anode reactions are reported in <mark style="background: #FFB86CA6;">Appendix</mark>.

In practice, separate Butler–Volmer expressions are written for each electrode, including reactant concentrations.
$$V_{act} = V_{act,a} + V_{act,c} \tag{11}$$
$$
V_{act,a} = \frac{RT_a}{\alpha_a F}\text{sinh}^{-1}\left(\frac{i}{2i_{0,a}}\right) = \frac{RT_a}{\alpha_a F}\ln\left(\frac{i}{2i_{0,a}} + \sqrt{1 + \left(\frac{i}{2i_{0,a}}\right)^2}\right) \quad (12)
$$

$$
V_{act,c} = \frac{RT_c}{\alpha_c F}\text{sinh}^{-1}\left(\frac{i}{2i_{0,c}}\right) = \frac{RT_c}{\alpha_c F}\ln\left(\frac{i}{2i_{0,c}} + \sqrt{1 + \left(\frac{i}{2i_{0,c}}\right)^2}\right) \quad (13)
$$
$V_{act,a}$, $V_{act,c}$, $T_a$, and $T_c$ are the anode and cathode voltages, and the anode and cathode operating temperatures, respectively.

At high anodic overpotential, the equation can be simplified to the Tafel equation:

$$
V_{\text{act,anode}} \approx \frac{RT}{\alpha_a F} \ln\left(\frac{i}{i_0}\right) \tag(14)
$$

For further simplification, the Butler-Volmer can also be expressed as,

$$
V_{act} = \frac{RT}{z\alpha_aF} \cdot \ln(i) - \frac{RT}{z\alpha_aF} \cdot \ln(i_0) = a \cdot \ln(i) - b \tag{15}
$$
The Tafel constant (b) helps measure the exchange current density ($i_o$ ), while the Tafel slope (a) indicates the slowest step in the electrode reaction pathway @zhangStatusPerspectivesKey2022 


### Ohmic Losses
Ohmic overpotential $V_{\text{ohm}}$ generates from resistive losses in the ionic and electronic conducting parts of the cell.  Ohmic loss is  modeled by Ohm’s law:
$$
V_{\text{ohm}} = I \cdot R_{\text{total}}= V_{ohm,a} + V_{ohm,c} + V_{ ohm,m} \tag{16}
$$

where $I$ is the cell current (A) for $I = i \cdot A_{cell}$, and $R_{total}$ is the total internal resistance (Ω) that opposes the flow of electrons. The total resistance depends on the membrane electrolyte $R_{m}$, the porous-electrode (GDL + CL) layers $R_{elec}$, the interfacial contact resistance $R_{in}$, and the resistance from the bipolar plates $R_{bpp}$.

$$R_{total} = R_{a}+ R_{c} + R_{m} = (R_{bpp,a} + R_{elec,a} + R_{in,a}) + (R_{bpp,c} + R_{elec,c}+ R_{in,c}) +R_m \tag{17}$$     
The resistance of the membrane is:
$$
R_{m} = \dfrac{t_{m}}{\sigma_{m}\cdot A_{cell}}
\tag{18}$$

where $t_m$ is membrane thickness thickness in micrometers (µm)  $\sigma_m$ is the proton conductivity of the  material used in Siemens per centimeter (S/cm). 
The membrane conductivity is modeled as a function of the temperature and water content. @leeThreeDimensionalTransportModeling2008   A membrane's hydration ($λ$ )informs the ionic conductivity $\sigma_{\text{mem}}$ as  @springerPolymerElectrolyteFuel1991
$$
\sigma_{\text{mem}} = \left(0.0051392\lambda - 0.0005326\right) \cdot \exp\left(1.268 \left(\frac{1}{303} - \frac{1}{T}\right)\right)
\tag{19}
$$
and is valid for 5≤λ≤22 and 30 °C ≤ _T_ ≤ 120 °C . 
A well-hydrated membrane has high $\sigma$ (e.g. 0.1 S/cm); if $λ$ drops (dry membrane), $\sigma$ falls and ohmic losses rise steeply @springerPolymerElectrolyteFuel1991 .

The resistivity in the electrode catalyst layer as a function of the the material resistivity ($ρ_{el}$) is  of the electrode(ohm.cm), ($t_{el}$) is the electrode thickness(cm) ($t_{el}$), is the catalyst layer resistance
$$
R_{\text{elec}} = \frac{t_{\text{el}}}{A_{\text{cell}} }\cdot \rho_{\text{el}}
\tag{20}
$$
$$
V_{\text{ohm,cat}} = V_{\text{ohm,an}} = \rho_{\text{el}} \cdot t_{\text{el}} \cdot i
\tag{21}
$$


A well distributed resistance along the flow-filed length and channels are given as (Fig 111) , the internal resistance of a PEM electrolyzer @hanElectrochemicalPerformanceModeling2015 .
![[image-68.png]]


Each component resistance is determined as follows:

The total Plate resistance along flow-field length $L_{ab}$  is given as @hanElectrochemicalPerformanceModeling2015 ,
$$ R_{bpp1} = \rho_{p}\,\dfrac{L_{ab}}{A} \tag{22}
$$
$$R_{bpp2} = \rho_{p}\,\dfrac{L_{bc}}{0.5\,L_{ik}\,L}\tag{23}$$

The resistance from to electrodes and gas channel, in-plane r and through-plane is given as, @hanElectrochemicalPerformanceModeling2015
$$R_{e1ec1} = \rho_{e}\,\dfrac{0.25\,L_{kl}}{t_{el}\,L\,(1 - \varepsilon)} \tag{24}$$
$$R_{elec2} = \rho_{e}\,\dfrac{t_{el}}{0.5\,L_{km}\,L\,(1 - \varepsilon)} \tag{25}$$
$$R_{elec3} = \rho_{e}\,\dfrac{t_{el}}{L_{kl}\,L\,(1 - \varepsilon)}\tag{26}$$

Where as the Interfacial resistance is empirically taken as twice the through-plane electrode resistance, $R_{\rm in}=2\,R_{e2}$, to fit polarization data. @marangioDirectHighPressure2009


### Mass Transport (Concentration) Losses
 At high current levels, reactant consumption can create concentration gradients and cause depletion near the electrodes, leading to additional overpotential. When the reactant supply rate cannot meet the demand, the local partial pressure (or concentration) at the catalyst decreases, effectively lowering the cell voltage. We assume a limiting current density $i_L$ of 6 $A/cm^2$, and the loss can be written as  @bessarabovPEMWaterElectrolysis2018 :
 
$$
V_{\text{conc}} = -\frac{RT}{zF} \ln\left(1 - \frac{i}{i_L}\right)
\tag{27}
$$
The voltage loss increases as the current density approaches the limiting current density.

### Overall Cell Voltage and Efficiencies 
Combining these contributions, the instantaneous total voltage under under steady-state conditions for a number of cell $N_{\text{cell}}$ is:
$$V_{\text{cell}} = V_{\text{rev}} + V_{\text{act, anode}} + V_{\text{act, cathode}} + V_{\text{ohm}} + V_{\text{conc}}
\tag{28}
$$
$$V_{\text{stack}} = N_{\text{cell}} V_{\text{cell}}
\tag{29}$$

Faradaic Efficiency
We define a faraday efficiency  $\eta_F$ to account for current losses like hydrogen crossover or internal shunt current . Thus the fraction of the applied current that prouces the target reaction products. 

$$\eta_F = \frac{\text{actual reaction current}}{\text{total current}} = 1 - \frac{i_{\text{loss}}}{i} \tag{30}$$

where $i_{\text{loss}}$ is the parasitic current density corresponding to side reactions or crossover.
A high-quality membrane (thicker or less permeable) and lower differential pressure improve $\eta_F$ by reducing crossover.
In practice, Faraday efficiency in modern PEM electrolyzers can exceed 98–99% at high current density, but drops at low loads or high pressure due to increased crossover @kangIntroducingNovelTechnique2021
 Faradaic losses manifest as a lower observed hydrogen production (or lower fuel cell current for a given fuel feed) and is modeled here as an efficiency loss rather than a direct voltage term.






 **Table 2  parameters for a PEM electrolyzer cell.**

| Description, unit                     | Value                                      |
| ------------------------------------- | ------------------------------------------ |
| Faraday constant, F (C/mol)           | 96485.0                                    |
| Gas constant, R (J/mol K)             | 8.314                                      |
| The cell operating temperature, T (K) | 353.15                                     |
| The cell operating pressure, P (atm)  | 1 (anode), 30 (cathode)                    |
| The maximum current density, (A/cm²)  | 2.0                                        |
| Exchange current density, (A/cm²)     | 2.0e$^{-6}$ (anode), 1.0e$^{-1}$ (cathode) |
| The electrode thickness, (microns)    | 200                                        |
| The electrode porosity                | 0.3                                        |
| The membrane thickness, (microns)     | 178                                        |
| Titanium resistivity, (ohm cm)        | 5.0e$^{-3}$ [20]                           |
| Carbon paper resistivity, (ohm cm)    | 80.0e$^{-3}$ [31]                          |
| Transfer coefficient                  | 2.0 (anode), 0.5 (cathode)                 |
| Water dynamic viscosity (N s/cm²)     | 3.55e$^{-8}$                               |
| Water density, (g/cm³)                | 1.0                                        |
| L$_{ab}$, (mm)                        | 2.0                                        |
| L$_{bc}$, (mm)                        | 1.0                                        |
| L$_{kl}$, (mm)                        | 1.0                                        |
| L, (cm)                               | $\sqrt{5}$                                 |
| MEA area, (cm²)                       |                                            |




## The mass and Energy  balance

The mass balance based on Faraday's law of electrolysis.
<mark style="background: #FF5582A6;">insp</mark>: @abdolrahimOverviewPolymerElectrolyte2016


![[image-67.png]]

The reactant water $\dot n^{a}_{H_2O,\text{in}}$ is fed to the anode half-cell and is consumed to form oxygen and protons. The oxygen and water are recirculated from the anode half cell to through the gas separator.
$$
\dot n^{a}_{O_2,\text{out}} = \dot n^{a}_{O_2,\text{in}} + \frac{i A_{\text{cell}}}{4F}
\tag{31}
$$
$$
\dot n^{a}_{H_2O,\text{out}} = \dot n^{a}_{H_2O,\text{in}} - \frac{i A_{\text{cell}}}{2F} - \dot n^{\text{trans}}_{H_2O}
\tag{32}
$$
Water  crossover through the membrane via multiple mechanisms: electro-osmotic drag $\dot n_{\text{osm}}$ , back-diffusion $\dot n_{\text{diff}}$, and hydraulic permeation $\dot n_{\text{hyd}}$, though electro-osmotic drag is the dominant mechanism.
$$\dot n^{\text{trans}}_{H_2O}=\dot n_{\text{osm}}+\dot n_{\text{diff}}+\dot n_{\text{hyd}}
\tag{33}$$

$$\dot n_{\text{osm}} = \frac{n_d\, i}{F} \cdot A_{\text{cell}}\ , \tag{34}
$$
The electroosmotic drag coefficient $n_d$   quantifies the amount of water molecules transported through a membrane per proton.  Water molecules are carried along with protons across the membrane from anode to cathode by electro-osmotic drag ( $\dot n_{\text{osm}}$ (mol/·s)). 
$$n_d(T) = 0.0134 \, T + 0.03 \quad (T \text{ in } ^\circ\text{C}) \quad \tag{35}$$ @ondaPerformanceAnalysisPolymerElectrolyte2002 

When the cathode side get very moist with concentration difference, water tends to diffuse across the membrane .  $\dot n_{\text{diff}}$ represents the molar flow due to the concentration gradient between the half cells. 
$$\dot n_{\text{diff}} = -D_w\,\frac{dC_w}{dx} \cdot A_{\text{cell}} \tag{36}$$
(where $C_w$ is water concentration in the membrane). it’s written in terms of water content $λ$ (number of water molecules per sulfonic acid group) @leeThreeDimensionalTransportModeling2008 .
$$\dot n_{\text{diff}} = -\,\frac{D_\lambda \,\rho_{\text{dry}}}{EW}\,\frac{dλ}{dx} \cdot A_{\text{cell}}, \tag{37}$$
with $\rho_{\text{dry}}$ the dry membrane density and $EW$ the equivalent weight (kg/mol of sulfonic acid) ( 
This form converts $∇λ$ to a concentration gradient ($\rho_{\text{dry}}/EW$ is mol sulfonic sites per volume). $D_w$ (or $D_λ$) strongly depends on hydration; empirical fits are used @leeThreeDimensionalTransportModeling2008.

Hydraulic crossover occurs due to the pressure difference across the membrane. This is modeled by Darcy’s law for flow through a porous medium: @itoPropertiesNafionMembranes2011
$$\dot n_{\text{hyd}} = -\frac{K_{\text{mem}}}{\mu_w}\,\Delta p \cdot A_{\text{cell}} \tag{38}$$
Where $K_{\text{mem}}$ is the effective permeability of the membrane to water, and $\mu_w$ water viscosity. Darcy-driven water flux is generally small in PEM fuel cells, but in water electrolyzers with thin membranes at high differential pressure, it can contribute to additional hydrogen crossover.

Hydrogen and oxygen leaves the cathode half cell and are future processed and recirculated in the $H_2$ gas separator.
$$
\dot n^{c}_{H_2,\text{out}} =\dot n^{c}_{H_2,\text{in}} + \frac{i A_{\text{cell}}}{2F} \tag{39}
$$
$$
\dot n^{c}_{H_2O,\text{out}} =\dot n^{c}_{H_2O,\text{in}}  + n^{\text{trans}}_{H_2O} \tag{40}
$$

##### The energy balance of cell
A PEM cell generates heat from multiple sources: (i) the reaction enthalpy that is not converted to electrical work, and (ii) Joule heating from ohmic losses, and (iii) any heat of mixing or phase change (e.g. water evaporation/condensation).  The 49 kJ/mol difference in ΔH and ΔG is released as heat even at open circuit (eqn 1-6) .
Additional overpotential losses further converts electrical energy to heat. Therefore, to represents the rate of heat generation in a single cell $Q_{\text{gen}}$ due to the cell operating voltage beyond the thermoneutral voltage: 
$$Q_{\text{gen}} = I \cdot (V_{cell} - V_{th})\tag{41}$$

The total temperature of the cell is determined by an energy balance that includes heat generation, heat removal, and energy flow from the reactant and product streams. We assume the cell has a uniform temperature. For a lumped cell mass $m$ with heat capacity $C_p$
$$m C_p \frac{dT}{dt} = Q_{\text{gen}} - Q_{\text{cool}} - Q_{\text{env}}, \tag{42}$$
where $Q_{\text{cool}}$ is heat removed by coolant and $Q_{\text{env}}$ is losses to ambient (convection, radiation). We assume steady-state is reached when generation equals removal. The bipolar plates are used to dissipate heat and maintain uniform temperature. Non-uniform temperature can cause dry spots or flooding in different areas, so thermal management aims to keep the cell at an optimal temperature (often ~60–80 °C) @molinaHeatManagementSystem2024 .










The input parameters for cell design are: 
Cell Design Parameters: Inputs and Outputs

| Parameter                             | Value                                  |
| ------------------------------------- | -------------------------------------- |
| Faraday constant, F (C/mol)           | 96485                                  |
| Gas constant, R (J/mol K)             | 8.314                                  |
| The cell operating temperature, T (K) | 333.15                                 |
| The cell operating pressure, P (bar)  | 1 (anode), 30 (cathode)                |
| The maximum current density, (A/cm²)  | 2                                      |
| Exchange current density, (A/cm²)     | 2.618 x 10⁻⁶ (anode), 1.0e-1 (cathode) |
| Limiting current density (A/cm²)      | 6                                      |
| The electrode thickness, (microns)    | 200                                    |
| The electrode porosity                | 0.3                                    |
| The membrane thickness, (microns)     | 178                                    |
| Titanium resistivity, (ohm cm)        | 5.0 x 10⁻³                             |
| Carbon paper resistivity, (ohm cm)    | 8.00x10⁻²                              |
| Transfer coefficient                  | 2.0 (anode), 0.5 (cathode)             |
| Water dynamic viscosity (N s/cm²)     | 3.55x10⁻⁸                              |
| Water density, (g/cm³)                | 1                                      |
| Active area, (cm²)                    | 877                                    |
| No electrons                          | 2                                      |
| Number of cells                       | 877                                    |
| Cell voltage, V                       | 1.79                                   |
| Voltage efficiency                    | 0.69                                   |
| Cell Power rating, kW/cell            | 3.14                                   |
| Total power rating, kW                | 19,034                                 |
| Specific Energy consumption           | 49                                     |
| Membrane type                         | PFSA, Nafion 117                       |
| Anode catalyst loading, mg/cm²        | 1.54                                   |
| Cathode catalyst loading mg/cm²       | 0.4                                    |



## 3.3 Energy system model


<mark style="background: #BBFABBA6;">insp</mark>. @astrianiOptimalPlanningRenewable2024
### 3.3 Energy System Modeling

#### 3.3.1 Photovoltaic (PV) Power Model

In modeling the photovoltaic (PV) system, the goal is to accurately estimate electricity generation from solar energy to incorporate into the hydrogen analyses. The output power of the PV depends on the solar irradiance incident on the PV array and the module’s temperature. The hourly and yearly PV power output can be represented as @khattakTechnoeconomicEnvironmentalAnalysis2024

$$
P_{PV,hY} = P_{STC,rated}\cdot f_{derPV,y} \frac{GTI_h}{G_{STC}} \left( 1 + \alpha_p \left( T_{PV,cell}^{h} - T_{STC} \right) \right)f_{derate} \tag{43}
$$
$P_{STC,rated}$ indicates the rated peak capacity of the PV system under standard test conditions (STC) at 1 MW. To account for the reduction in module efficiency over time, the annual derating factor $f_{derPV,y}$ is applied. The global tilted irradiance (${GTI_h}$), measured in kW/m², describes the solar radiation incident on the tilted photovoltaic module surfaces during hour $h$. Solar irradiance data, which is often available online, is usually given as global horizontal irradiance (GHI). Therefore, to obtain the global tilted irradiance (GTI), this data is adjusted based on the tilt and orientation of the solar panels. This conversion involves correcting for the module's tilt angle and solar geometry, using the following equation: @uchennaWindsolarHybridPower2012

$$
GTI = GHI \frac{\sin(\sigma + \theta_{PV})}{\sin \sigma} \tag{44}
$$
Here, $θ_{PV}$  is the angle at which the photovoltaic panels are tilted relative to the horizontal.  σ represents the angle of solar elevation, defined as: @elmghouchiModelsObtainingDaily2016


$$
\sigma = 90 - \phi + \delta \tag{45}
$$

$\phi$ indicates the latitude of the installation site, while $\delta$ represents the solar declination angle, which varies throughout the year and is defined as @elmghouchiModelsObtainingDaily2016

$$
\delta = 23.4 \cos \left( \frac{360}{365} (d + 284) \right) \tag{46}
$$

with corresponding to the day number of the year from1 through 365.
The cell temperature ($T_{\rm PV, cell}^{h}$) influences efficiency and energy output, adjusted against the standard temperature conditions ($T_{\rm STC}=25 °C$ ) through the temperature coefficient $\alpha_p\approx -0.0035/°\text{C}$. @duboisStepbystepEvaluationPhotovoltaic2017
$$T_{\rm PV, cell}^{h} = T_{\rm amb}^{h} + \frac{\mathrm{NOCT} - 20}{800} \;G[h] \tag{47}$$
with $T_{\rm amb}[h]$ modeled as a seasonal sine wave to reflect seasonal variations and Nominal Operating Cell Temperature (NOCT) in Celsius. G[h] represents the global tilted irradiance $GTI_h$ from Equation (44), measured in W/m². Systematic losses such as inverter efficiency, cable losses, and thermal effects are included as $f_{\rm derate}\approx0.90$. Incorporating these losses improves the accuracy and usability of the PV model, ensuring comprehensive evaluation and reliable results when used in broader energy system simulations and analyses.




### 3.3.2 Wind Power Plant Modeling

The surrogate modeling of wind energy generation involves calculating the wind turbine's power output as a function of wind speed, considering several performance-related factors. The relationship used to determine the wind turbine power output ($P_{WT}$) at any given moment is governed by the Betz-Lanchester equation as: @duffieSolarEngineeringThermal2020

$$
P_{WT} = 0.5 \eta_{WT}\cdot \rho A C_p(\omega, \beta) v^3 \tag{48}
$$
The mechanical efficiency,($\eta_{WT}$ ), accounts for energy losses in critical mechanical components such as gearboxes and drivetrains, directly influencing the effective power available from wind energy conversion. The air density ($\rho$) ( approximated at 1.23 kg/m³), is essential as denser air carries more kinetic energy, significantly affecting power output. @gunturuCharacterizationWindPower2012 The swept area ($A$),m² is defined by the circular area created by rotating turbine blades, determines the quantity of wind intercepted, thus proportionally affecting turbine output.
The power coefficient, ($C_p(\omega, \beta$)), captures the aerodynamic efficiency of the turbine and varies according to the tip speed ratio ($\omega$) and blade pitch angle $\beta$. ( $\omega$ ) is the ratio of blade tip speed to wind speed, while ($\beta$), which adjusts the blades’ orientation relative to wind flow to optimize efficiency. The polynomial power coefficient curves from literature are summarized in<mark style="background: #FF5582A6;"> Appendix</mark>  @castilloComparisonPowerCoefficients2023
The mechanical efficiency ($\eta_{WT}$) accounts for energy losses in critical mechanical components like gearboxes and drivetrains, directly affecting the effective power available from wind energy conversion. The air density ($\rho$), approximated at 1.23 kg/m³, is crucial since denser air carries more kinetic energy, significantly impacting power output. @gunturuCharacterizationWindPower2012 The swept area ($A$), measured in m², is defined by the circular area created by the rotating turbine blades and determines how much wind is intercepted, thereby proportionally influencing turbine output. The power coefficient ($C_p(\omega, \beta$)), captures the aerodynamic efficiency of the turbine and varies based on the tip speed ratio ($\omega$) and blade pitch angle ($\beta$). ( $\omega$ ) is the ratio of the blade tip speed to the wind speed, while ($\beta$) adjusts the blades’ orientation relative to the wind flow to optimize efficiency. The polynomial power coefficient curves from literature are summarized in


$$
C_p(\omega, \beta) = c_0 \left(\frac{c_1}{\omega_i} - c_2\beta - c_3\beta \omega_i - c_4{\omega}_i^{c_5} - c_6 \right) e^{-\frac{c_7}{\omega_i}} + c_8\omega \tag{49}
$$

where:

$$
\frac{1}{\omega_i} = \frac{1}{\omega + c_9\beta + c_{10}} - \frac{c_{11}}{1 + \beta^3} \tag{50}
$$
Lastly, wind speed ($v$)), (m/s), critically influences power output as the cubic term indicates that even slight variations in wind speed significantly affect available power. 
The frequency of wind speeds $v$ is well-fitted by a Weibull probability density,  @zhangJointProbabilityDistribution2015 :

$$f(v) \;=\; \frac{k}{\lambda} \Bigl(\frac{v}{\lambda}\Bigr)^{\,k - 1} \exp\!\Bigl[-\bigl(v/\lambda\bigr)^k\Bigr], \quad v \ge 0, \tag{51}$$
where $\lambda$ is the scale parameter ( the average wind speed), and $k$ is the shape parameter ( peaked the distribution is). @zhangJointProbabilityDistribution2015 Seasonal and diurnal modulating factors are applied to the local velocity of wind. @jafarianEffectsEnviromentalParameters2008 The velocity is further adjusted to the height of the Turbine from ground level. @delgadoEvaluationVariabilityWind2016 
We clamped the design to cut-in/cut-out constrains for a 1 MW-based turbine to  protecting the turbine from structural stress such that.


$$
P_{WT} =
\begin{cases} 
    0, & v < v_{in}, \ v > v_{out} \\
    P_{WT}(v), & v_{in} \leq v \leq v_r \\
    P_{WT,rated}, & v_r \leq v \leq v_{out}
\end{cases}
\tag{52}
$$
 
No output is generated when wind speeds are below the cut-in speed ($v_{in}$) or above the cut-out speed ($v_{out}$). Between the rated speed ($v_r$) and the cut-out speed ($v_{out}$), the turbine operates at its constant rated power ($P_{WT,rated}$). For wind speeds between cut-in ($v_{in}$) and rated speed ($v_r$), the output power follows the curve $P_{WT}(v)$, assuming that $A$, $\rho$, and $C_{p}$ remain effectively constant. $P_{WT}(v)$ refers to the power from Equation (48). This helps with forecasting and facilitates the effective integration of wind power within the broader energy system analysis.



### 3.3.3 Integration of Renewable Energy Plant Outputs

The total power output of the renewable energy (RE) plant, comprising both photovoltaic and wind energy systems, must be quantified to assess the overall energy balance at each hour (*h*) of the year (*y*). The total RE power output ( $P_{RE,h,y}$) is thus calculated as: @astrianiOptimalPlanningRenewable2024

$$P_{RE,h,y} = P_{PV,h,y} + P_{WT,h,y}\tag{53}$$

To ensure continuous operation of the electrolyzer, which requires stable power input within the operational constraints of 5% to 100% of its rated capacity ( $P_{EL,rated}$ ), supplementary power from the upstream electrical grid may be required @astrianiOptimalPlanningRenewable2024 . Hence, the imported power ( $P_{import,h,y}$ ) from the grid is computed based on the minimal operational limit of the electrolyzer as follows:

$$
P_{\text{import},h,y} = \begin{cases} (0.05 \cdot P_{\text{EL,rated}}) - P_{\text{RE},h,y}, & \text{if } P_{\text{RE},h,y} < (0.05 \cdot P_{\text{EL,rated}}) \\ 0, & \text{otherwise} \end{cases}
\tag{54}
$$

This equation demonstrates that when the renewable energy production falls below the electrolyzer's minimum operational threshold, the deficit is compensated by importing power from the grid.

Conversely, when renewable energy production surpasses the electrolyzer’s maximum operational capacity (rated power  $P_{EL,rated}$) the excess electricity is directed back to the electrical grid. The exported power ( $P_{export,h,y}$ ) in such scenarios is calculated by:

$$
P_{\text{export},h,y} = \begin{cases} P_{\text{RE},h,y} - P_{\text{EL,rated}}, & \text{if } P_{\text{RE},h,y} > P_{\text{EL,rated}} \\ 0, & \text{otherwise} \end{cases}
\tag{55}
$$

This comprehensive methodology allows for detailed assessments of system performance, stability, and economic viability across different operational conditions and renewable energy availability.





If $v < v_{\rm cut\text{-}in},(v_{i})$, output = 0.
If $v_{\rm cut\text{-}in} \le v \le v_{\rm rated}$, output = $P_{\rm rated}\times\bigl(P_{\rm phys}(v)/P_{\rm phys}(v_{\rm rated})\bigr)$.
If $v_{\rm rated} \le v \le v_{\rm cut\text{-}out}$, output = $P_{\rm rated}$.
If $v > v_{\rm cut\text{-}out}$, output = 0.




$$
P_{\text{import},h,y} = \begin{cases} (0.05 \cdot P_{\text{EL,rated}}) - P_{\text{RE},h,y}, \\ 0, \end{cases}
\tag{54}
$$


$$
P_{\text{export},h,y} = \begin{cases} P_{\text{RE},h,y} - P_{\text{EL,rated}}, &  \\ 0, \end{cases} \tag{55}
$$


$$ P_{import,h,y} = (0.05 \times P_{EL,rated}) - P_{RE,h,y}\tag{54}$$


$$P_{export,h,y} = P_{RE,h,y} - P_{EL,rated}\tag{55}$$


----


[[03 Mathematical modeling | Chapter 3: Mathematical modeling. ]]
	3.1 Electrolyzer and Electrochemical Module. 17
	Rev, Activation, Ohmic, Concentration
	Faradays,
	Mass and energy transport
	3.2 Energy system model
	3.3.1 PV power model
	3.3.2 Wind PV plant model



Metrice
[3.2.2 Levelized cost of hydrogen(LCOH) 17](#_Toc192135821)