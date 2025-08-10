other files
	[[equations]]
	[[catalyst design and parameters]]

- [ ] the objectives of your model? 
- [ ] the level of detail of model? [^1])
- [ ]  physical phenomena of model accounted for  (e.g., electrochemistry, mass transport, heat transport, fluid dynamics, membrane phenomena, electrical resistance?)
- [ ] document the key equations or principles model is based on? (e.g., Butler-Volmer equation, Fick's law, conservation equations?)
- [ ]  components of the electrolyzer included in the model: (e.g., membrane, catalyst layers (anode and cathode), gas diffusion layers (GDLs), bipolar plates, flow channels?)
- [ ] write on all assumptions made in developing the model?
- [ ] write are the inputs  of model (e.g., operating voltage, current density, temperature, pressure, flow rates, material properties?)
- [ ] **What outputs does the model provide (e.g., hydrogen production rate, efficiency, temperature distribution, species concentrations, voltage losses?)

 - **What are the objectives of your model?** (e.g., <span style="color:rgb(146, 208, 80)">predict performance</span>, <span style="color:rgb(146, 208, 80)">optimize design</span>, study specific phenomena, <span style="color:rgb(146, 208, 80)">system-level simulation</span>?)
- **What level of detail does your model include?** [^1](e.g., 0D ( lumped parameter), 1D, <span style="color:rgb(146, 208, 80)"><span style="color:rgb(146, 208, 80)">2</span>D</span>, 3D?)
-  **What physical phenomena does your model account for?** (e.g., <span style="color:rgb(146, 208, 80)">electrochemistry</span>, <span style="color:rgb(146, 208, 80)">mass transport</span>, heat transport, fluid dynamics, membrane phenomena, electrical resistance?)
- **What are the key equations or principles your model is based on?** (e.g., <span style="color:rgb(146, 208, 80)">Butler-Volmer equation</span>, <span style="color:rgb(146, 208, 80)">Fick's law</span>, conservation equations?)
- **What components of the electrolyzer does the model include?** (e.g., membrane, catalyst layers (anode and cathode), gas diffusion layers (GDLs), bipolar plates, flow channels?)
- **What assumptions have you made in developing the model?**
- **What inputs does your model require?** (e.g., operating voltage, <span style="color:rgb(146, 208, 80)">current density</span>, <span style="color:rgb(146, 208, 80)">temperature</span>, <span style="color:rgb(146, 208, 80)">pressure</span>, <span style="color:rgb(146, 208, 80)">flow rates</span>,<span style="color:rgb(146, 208, 80)"> material properties</span>?)
- **What outputs does your model provide?** (e.g., <span style="color:rgb(146, 208, 80)">hydrogen production rate</span>, <span style="color:rgb(146, 208, 80)">efficiency</span>, temperature distribution, <span style="color:rgb(146, 208, 80)">species concentrations</span>, <span style="color:rgb(146, 208, 80)">voltage losses</span>?)



From literature pre-2016 @abdolrahimOverviewPolymerElectrolyte2016 

![[Lit review of PEM modules 2016.png]]

[54] K.W. Harrison, E. Hernandez-Pacheco, M. Mann, H. Salehfar, Semiempirical model for determining PEM electrolyzer stack characteristics, J. Fuel Cell Sci. Technol. 3 (2006) 220.
[55] N.V. Dale, M.D. Mann, H. Salehfar, Semiempirical model based on thermo￾dynamic principles for determining 6kW proton exchange membrane elec￾trolyzer stack characteristics, J. Power Sources 185 (2008) 1348e1353.
[56] M. Santarelli, P. Medina, M. Calì, Fitting regression model and experimental validation for a high-pressure PEM electrolyzer, Int. J. Hydrogen Energy 34 (2009) 2519e2530.
[57] K. Onda, T. Murakami, T. Hikosaka, M. Kobayashi, R. Notu, K. Ito, Performance analysis of polymer-electrolyte water electrolysis cell at a small-unit test cell and performance prediction of large stacked cell, J. Electrochem. Soc. 149 (2002) A1069.
[58] H. Gorgun, Dynamic modelling of a proton exchange membrane (PEM) electrolyzer, Int. J. Hydrogen Energy 31 (2006) 29e38.
[59] F. Marangio, M. Santarelli, M. Cali, Theoretical model and experimental analysis of a high pressure PEM water electrolyser for hydrogen production, Int. J. Hydrogen Energy 34 (2009) 1143e1158.
[60] S.A. Grigoriev, A.A. Kalinnikov, P. Millet, V.I. Porembsky, V.N. Fateev, Math￾ematical modeling of high-pressure PEM water electrolysis, J. Appl. Elec￾trochem. 40 (2009) 921e932.
[61] A. Awasthi, K. Scott, S. Basu, Dynamic modeling and simulation of a proton exchange membrane electrolyzer for hydrogen production, Int. J. Hydrogen Energy 36 (2011) 14779e14786.
[62] B. Lee, K. Park, H.M. Kim, Dynamic simulation of PEM water electrolysis and comparison with experiments, Int. J. Electrochem. Sci. 8 (Jan 2013) 235e248.
[63] M. Chandesris, V. Medeau, N. Guillet, S. Chelghoum, D. Thoby, F. Fouda- Onana, Membrane degradation in PEM water electrolyzer: numerical modeling and experimental evidence of the influence of temperature and current density, Int. J. Hydrogen Energy 40 (2015) 1353e1366.
[64] H. Kim, M. Park, K.S. Lee, One-dimensional dynamic modeling of a high￾pressure water electrolysis system for hydrogen production, Int. J. Hydrogen Energy 38 (2013) 2596e2609.








# Electrochemical Module

$$
V_{cell}=E_{0} +η_{act}+η_{Ω}+η_{conc}
$$
where ηact, and ηconc are activation, ohmic, and concentration overpotentials,
Where:

- Vcell​ is the cell voltage
- Erev​ is the reversible cell voltage
- ηactηact​ is the activation overpotential
- ηohmηohm​ is the ohmic overpotential [4](https://www.mdpi.com/1996-1073/13/24/6556)


## Open circuit Voltage
A simplified Nerst equation

$$V_{oc}=\frac{∆G_R^O }{z.F}+\frac{R.T}{z.F} ln(\frac{p_{H_2}  {p_{O_{2}}^0.5}}{α_{H_2 O} })$$
- E0 is the standard cell potential
- R is the gas constant
- T is temperature
- z is the number of electrons transferred (2 for water electrolysis)
- F is Faraday's constant
- pH2​​ and pO2​​ are partial pressures of hydrogen and oxygen
- aH<sub>2​</sub>O​ is the activity of water[ 6 ](https://www.mdpi.com/2311-5629/6/2/29)

is the standard Gibs free energy of the electrolysis reaction z is the number of electrons involved in the reaction(2 for hydrogen), F is Faraday’s constant, R is the gas constant, 𝛼 is the activity coefficient.


## The activation (Faradaic losses) voltages
The ηact has contributions from both anode and cathode i.e.$$ ηact=η_{act}^{anode}+η_{act}^{anode} $$
Using _the Butler–Volmer equation_ , η±act (– for anode and + for cathode)
$$
η_{act}^±=  \frac{RT}{(2α_± )} ln⁡(\frac{j}{j_{o,±}} )
$$
where R is the ideal gas constant, T is the operating temperature, α± is the charge transfer coefficient (assumed to be 0.5 ), j is the cell current density (i.e. the cell current normalized with respect to the electrode cross–sectional area), and j0,± is the exchange current density
[ref][https://www.mdpi.com/2311-5629/6/2/29]

the cathode is significantly faster than the kinetics of the oxygen evolution reaction at the anode (Espinosa-López et al., 2018; García-Valverde et al., 2012)
for exchange current density:

  $$i_{o,an} =K_{io, an}.exp⁡(\frac {E_{act,an}}{R.T})$$

Kio is the pre-exponential factor and Eact is the activation energy of the reaction at the anode.=2160000A/cm2 or 

the activation energy for the anode (Eact,anode) is equal to 76,000 J/mol (Crespi et al., 2023)

1 - \beta=  \alpha_a


Pressure and Temperature dependence

$$
i_0​=i_{0,ref}​ \left( \frac{P{O_2}}{P_{O_2​​​,ref}} \right) ^γ exp\left(\frac{-ΔG}{RT_c​​}(1−\frac{T_c​​}{T_{ref}​})\right)
$$
![[Pasted image 20250115154149.png]]
Where:

- P_{O_2} is the oxygen partial pressure
- γ is a pressure coefficient
- ΔG is the Gibbs free energy change[ 5](https://digital.csic.es/bitstream/10261/304811/1/Intl%20J%20of%20Energy%20Research%20-%202022%20-%20Aguilar%20-%20Control%E2%80%90oriented%20estimation%20of%20the%20exchange%20current%20density%20in%20PEM%20fuel%20cells.pdf) 
4. Catalyst Layer Properties:  
    The exchange current density is influenced by catalyst layer properties:

$$ i_{0}=i_{0,ref}⋅RF $$
Where RF is the roughness factor of the catalyst layer, representing the ratio of actual surface area to geometric surface area

```
Influence of Porosity and Thickness
In porous electrodes, the effective exchange current density can be modified by considering the porosity and thickness of the catalyst layer. The exchange current density per geometric area can be expressed as:
$$
i_{o,eff}= i_o.\frac{\epsilon}{\delta}
$$

- i0,eff​ = effective exchange current density per geometric area
- ϵϵ = porosity of the catalyst layer (fractional volume)
- δδ = thickness of the catalyst layer (cm)

**catalyst loading on Limiting Current Density**:
Increasing catalyst loading can enhance the limiting current density (ilimilim​) up to a certain point. This is because more catalyst increases the number of active sites available for reactions, thus allowing higher current densities

 -  For instance, in one study, it was noted that at lower ionomer-to-carbon (I/C) ratios, the thickness of the catalyst layer (δδ) was linearly dependent on carbon loading (LCLC​), which in turn is related to platinum loading (LPtLPt​) [1](https://pmc.ncbi.nlm.nih.gov/articles/PMC11082850/).

δCL∝LC

```

$$
i_{o,eff}= i_o.\frac{\epsilon}{\delta}
$$


## **The concentration overpotential (ΔV conc),**

considering only the anode side, where the dominant contribution is present ( @colbertaldoZerodimensionalDynamicModeling2017   Colbertaldo et al., 2017; García-Valverde et al., 2012 @garcia-valverdeSimplePEMWater2012 )
https://youtu.be/9FsHJFowgAo


$$
V_{con}=\frac{R.T}{z.α_{an}.F} (ln( \frac{j_L}{(j_L-i)}))
$$
α_an is the charge transfer coefficient of the reaction occurring at the anode and iL the limiting current density.
The limiting current density is assumed equal to 6 A/cm2 (@bessarabovPEMWaterElectrolysis2018 Bessarabov & Millet, 2018)

$$
V_{con}=\frac{R.T}{z.α_{an}.F} (ln( \frac{C_b}{C_s}))
$$
Where:

- R is the gas constant
- T is the temperature
- n is the number of electrons transferred
- F is Faraday's constant
- C_b is the bulk concentration of the reactant
- C_s is the surface concentration of the reactant

the **limiting current density**
j_lim: Limiting current density. This represents the maximum current density that can be achieved when the reaction rate is limited by mass transport. the limiting current density can be derived from Fick's laws of diffusion and is given by:

$$ i_{lim} = \frac{nFDc}{L} $$
Where:

- n = number of electrons transferred per reaction (typically 2 for water electrolysis)
- F = Faraday's constant (approximately 96485 C/mol)
- D = diffusion coefficient of the reactant (e.g., water)
- c = concentration of the reactant (e.g., water concentration)
- L = thickness of the porous transport layer (PTL)
[ref][[Experimental assessment and analysis of mass transport limiting current density in water vapor-fed polymer electrolyte membrane electrolyzers | Scientific Reports](https://www.nature.com/articles/s41598-024-79935-6)]

The binary diffusion coefficient of any two substances can be extrapolated from reference values for a given temperature and pressure,

$$D= D^{ref} (\frac{T}{_{ref}} )^{2.33} (\frac{P_(ref)}{P})$$ Where _D__ref_ is a reference diffusivity, _T_ is the cell temperature, _T__ref_ is the reference temperature, _p__ref_ is reference pressure, and _p_ is absolute pressure.


Porosity and tortuosity relate effective transport properties, K eff, with bulk transport properties, K through the following relation
![[Pasted image 20250113040600.png]]


[Insights into Interfacial and Bulk Transport Phenomena Affecting Proton Exchange Membrane Water Electrolyzer Performance at Ultra‐Low Iridium Loadings - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC8564452/)






## **The ohmic overpotential (ΔVohm)**

The ohmic overpotential is related with the materials resistance to the protons flux. The magnitude of ohmic losses depends on the materials properties.

$$V_{ohm,an}=V_{ohm,an}   +V_{ohm,ca}   +V_{ohm,mem}$$$
$$∆V_{ohm}=(R_{el,an}+R_{el,cat}+R_{mem} )i.A_{cell}$$

$$ V_{ohm,an}=V_{ohm,cat}=ρ_{el}.t_{el}.I$$

$$V_{ohm,mem}=\frac{t_{mem}}{σ_{mem}} . i$$
$$R_{el,X}=\frac{t_{el,X}}{A_{cell}}  ρ_{el,X}$$

$$R_{mem}=\frac{t_{mem}}{σ_{mem}.A_cell }$$
ρ_el is the material resistivity of the electrode, σ_memis the membrane resistivity, t_el is the electrode thickness, and t_mem is the membrane thickness.
The thickness of the membrane (tmem), which a sensitivity analysis shows as the main term influencing the ohmic loss and therefore the cell polarization curve

σ_{mem}=(0.005139λ-0.00326).exp⁡(1268(1/303-1/T))

λ Represents the number of water molecules per sulfonic acid site in the membrane (SO3H)


![[Pasted image 20250115154402.png]]


**Calculation of the local volumetric current density in the cathode catalyst layer**

local volumetric current density(i<sub>v</sub>), A/cm3 
$$i_{v} = \frac{\eta_{HER}}{\delta .R_{K, HER}}$$
where δ is the cathode catalyst layer thickness, ηHER is the kinetic overpotential and RK, HER is the charge transfer resistance for the HER. [re][https://doi.org/10.1149/2.0641805jes.]

RK, HER =hcarge transfer resistance 
$$
R_{K,HER} = \frac{R.T}{(\alpha_{a}+\alpha_{c}.F.L_{Pt}.A_{Pt}.i_{o,HER})}$$
where R is the gas constant, T is the temperature, (αa + αc) is the sum of the anodic and cathodic transfer coefficients, F is the Faraday constant, LPt is the Pt loading, APt is the specific Pt surface area, and i0, HER is the exchange current density of the HER.

\eta
The kinetic overpotential ηHER
the derivations made by Thompson et al. for the hydrogen oxidation reaction: [ref][https://doi.org/10.1149/1.2943203.]
$$
\eta_{HER}|x = \frac{i}{s.k_{eff}}. \frac{cosh(s(\delta-x))}{sinh(s.\delta)}$$
i is the geometric current density, κeff is the effective proton conductivity of the cathode catalyst layer, and s is a kinetic parameter:

$$S= [\frac{1}{K_{eff}.\delta}.\frac{1}{R_{K,HER}}]^{0.5}$$
The effective proton conductivity κeff

$$K_eff =\frac{1}{\rho{H+,cath}}$$
where ρH+, cath is the effective proton resistivity of the cathode catalyst layer, and is estimated to be ~ 25 Ohm·cm for an I/C ratio of 0.69 and ~ 60 Ohm·cm for an I/C ratio of 0.35
[ref][https://doi.org/10.1149/1.3435323.]
![[Pasted image 20250120111654.png]]

Zhang, Z.; Baudy, A.; Testino, A.; Gubler, L. Cathode Catalyst Layer Design in PEM Water Electrolysis toward Reduced Pt Loading and Hydrogen Crossover. _ACS Appl Mater Interfaces_ **2024**, _16_ (18), 23265–23277. [https://doi.org/10.1021/acsami.4c01827](https://doi.org/10.1021/acsami.4c01827).



Bruggeman core

 the tortuosity factor model applies the tortuosity factor with includes the relation on porosity in this case  
 transport efficiency"  B  
 B=ϵ/τ
 =ϵ/ϵ−1/2=ϵ3/2 .


---
4/12/25


# 4. Geometrical Parameters

- **Cell Active Area (A):** This is the electrode area available for reaction (in cm² or m²). The total cell current is $I = j \cdot A$, where _j_ (A/m²) is the current density. A larger area allows higher total currents for a given current density. 
	- Geometric area also influences ohmic resistance (a larger cross-sectional area for current reduces resistance: $R_{\text{mem}} = \rho_{\text{mem}} t_{\text{mem}}/A$) 
	- the rate of heat removal (large area can dissipate more heat to flowing gases or coolant) ([](https://webthesis.biblio.polito.it/30809/1/tesi.pdf#:~:text=Practically%2C%20is%20evaluated%20the%20water,anode%20and%20cathode%20catalyst%20layer)) ([](https://webthesis.biblio.polito.it/30809/1/tesi.pdf#:~:text=than%20is%20made%20the%20mean,final%20integration%20in%20made%2037)).
- **Number of Flow Channels:** The flow field design (e.g. number of channels, channel width, and length) influences pressure drop and reactant distribution. More channels (or wider channels) in parallel result in lower pressure drop but also lower flow velocity, which might reduce convective removal of water. Fewer channels (or longer serpentine paths) ensure reactants travel across the whole area but at the cost of higher pressure drop and possibly uneven distribution if channels are very long. 
	- using an effective 1D approximation with a certain stoichiometric flow rate and pressure drop correlation.
	- a **serpentine** flow field with one long channel ensures uniform flow but is often modeled in segments; a **parallel** multi-channel design may need a 2D model to capture flow maldistribution if any. 
	- Geometrical parameters like channel hydraulic diameter and length are used in computing Reynolds number and friction factor for flow (to get pressure drop, which affects the inlet pressure to the Nernst equation via $p_{H2}, p_{O2}$). .
- **Bipolar Plate and Separator Thickness:** : These affect the volume and weight of the stack and also the thermal conduction path. A thicker graphite or metal bipolar plate (which includes channels) can carry heat away more uniformly but adds resistance if it’s not highly conductive. 
	 A thicker plate also increases the distance between cells if cooling channels are integrated. Typically, flow field plates are a few millimeters thick; their thickness doesn’t directly enter electrochemical equations, but if one is modeling the _stack compression_, it could impact contact resistance (thicker, stiffer plates distribute pressure differently).
-  **Electrode and Membrane Thickness:** Thicker electrodes (GDL or catalyst layer) provide longer pathways for mass transport and charge conduction.  Fick’s law flux $\sim D_{\text{eff}}(C_{\text{chan}}-C_{\text{int}})/L$).
	 - Catalyst layer thickness must balance having enough catalyst/electrolyte interface versus mass transport limits; typical CL thickness is only ~5–20 μm. 
	- The **membrane thickness** strongly affects ohmic loss and water crossover. A thicker membrane increases ionic path length (linearly raising $\eta_{\text{ohm}}$) but also reduces gas crossover and improves durability.  increasing Nafion membrane thickness from 25 μm to 125 μm can cut crossover by ~80%, improving Faraday efficiency ([Introducing a Novel Technique for Measuring Hydrogen Crossover in Membrane-Based Electrochemical Cells](https://www.osti.gov/servlets/purl/1774854#:~:text=diffuses%20to%20the%20anode,the%20most%20commonly%20used%20hydrogen)).  However, a very thick membrane may require higher compression and can increase the cell’s internal resistance, so an optimal thickness is chosen. the membrane thickness _tmem_ also affects the water diffusion time constant (roughly $t_{\text{mem}}^2/D_w$).
- 
## Electrode parameters

The porous electrodes (anode and cathode) are characterized by properties that affect reaction kinetics and mass transport. 
Key parameters include thickness (already discussed), porosity, tortuosity, pore size, electrical/ionic conductivity, and electrochemically active surface area:
- **Porosity (ε):** This is the fraction of void volume in the gas diffusion layer (GDL) or catalyst layer (CL). A higher porosity means more open space for gas to flow and diffuse. (Eq. 7) ( [Three-Dimensional Transport Modeling for Proton Exchange Membrane(PEM) Fuel Cell with Micro Parallel Flow Field - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC3663005/#:~:text=) ) ( [Three-Dimensional Transport Modeling for Proton Exchange Membrane(PEM) Fuel Cell with Micro Parallel Flow Field - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC3663005/#:~:text=where%20%CE%B5%20is%20the%20porosity,of%20water%20in%20the%20cathode) ). It directly influences the effective diffusivity ($D_{\text{eff}} = \varepsilon D/\tau$) and permeability $K$ in Darcy’s law. Typical GDL porosity ~0.6–0.8, CL porosity ~0.3–0.6 (CL has pores within catalyst + ionomer). <span style="color:rgb(146, 208, 80)">A design trade-off</span>: too high porosity reduces mechanical support and may flood easily; too low porosity hinders gas transport.
-
- **Tortuosity (τ):** This dimensionless factor (>1) accounts for the convoluted path gas must take through the pores. **Bruggeman correlation**, relating tortuosity to porosity by $τ ≈ ε^{-b}$ with $b≈0.5$ for straight pores or $~1.5$ for more complex structures. Effective diffusivity can be written $D_{\text{eff}} = D \frac{ε}{τ}$ ([Analytical-based simulation approach for an anion exchange membrane fuel cell](https://www.nrel.gov/docs/fy23osti/84813.pdf#:~:text=%F0%9D%91%83%F0%9D%91%9F%F0%9D%91%92%F0%9D%91%93%20%290,effective%20exchange%20current%20densities%20for)) ([Analytical-based simulation approach for an anion exchange membrane fuel cell](https://www.nrel.gov/docs/fy23osti/84813.pdf#:~:text=%E2%88%92%20%F0%9D%91%92%F0%9D%91%A5%F0%9D%91%9D%20,effective%20exchange%20current%20densities%20for)); Tortuosity also affects effective ionic conductivity in the catalyst layer (protons moving through ionomer phase) and electron conduction in porous media with binder. Many models include τ implicitly by fitting $D_{\text{eff}}$ or using empirical diffusivity measurements ([Analytical-based simulation approach for an anion exchange membrane fuel cell](https://www.nrel.gov/docs/fy23osti/84813.pdf#:~:text=%F0%9D%91%83%F0%9D%91%9F%F0%9D%91%92%F0%9D%91%93%20%290,effective%20exchange%20current%20densities%20for)).
-
- **Pore Radius and Capillarity:** The average pore radius (and pore size distribution) influences how liquid water forms and moves. According to the Washburn equation, the capillary pressure $p_c$ in a pore is $p_c = \frac{-2γ \cosθ}{r_{\text{pore}}}$, where $γ$ is surface tension and $θ$ the contact angle. Smaller pores have higher capillary pressure, meaning they hold water more tightly (harder to drain, leading to flooding if produced water accumulates). Electrode designs often use hydrophobic treatments (e.g. PTFE coating) to increase contact angle and help expel water. pore size and wettability come into play in two-phase water models: e.g. one may set a capillary pressure vs saturation relation $p_c(s)$ to simulate how pores fill with water as $s$ rises ([Analytical-based simulation approach for an anion exchange membrane fuel cell](https://www.nrel.gov/docs/fy23osti/84813.pdf#:~:text=%283%29%20%F0%9D%91%96%20%3D%20%F0%9D%91%960%2C%F0%9D%91%90%20,)) ([Analytical-based simulation approach for an anion exchange membrane fuel cell](https://www.nrel.gov/docs/fy23osti/84813.pdf#:~:text=%F0%9D%91%83%F0%9D%91%9F%F0%9D%91%92%F0%9D%91%93%20%290,effective%20exchange%20current%20densities%20for)).  

- **Electrical Resistivity:** The electrodes must conduct electrons (in the GDL and through the carbon catalyst support) and protons (in the ionomer within the catalyst layer). The GDL is usually a carbon paper or cloth; its through-plane resistivity contributes to $R_{\text{eq}}$. Similarly, the catalyst layer contains carbon and ionomer; its **ionic resistivity** (proton pathway through ionomer) can cause additional voltage loss, sometimes called _charge transport resistance_ in the CL ([Analytical-based simulation approach for an anion exchange membrane fuel cell](https://www.nrel.gov/docs/fy23osti/84813.pdf#:~:text=electrodes%20are%20not%20strictly%20ohmic,of%20the%20effective%20ionic%20resistance)) ([Analytical-based simulation approach for an anion exchange membrane fuel cell](https://www.nrel.gov/docs/fy23osti/84813.pdf#:~:text=entire%20current%20density%2C%20while%20the,inherent%20water%20imbalance%20in%20an)). 
	Models often include an **electronic resistance** for the GDL ($R_{\text{GDL}}$) and an **ionic resistance** for the catalyst layer ($R_{\text{CL}}$). $R_{\text{CL}}$ can be modeled by considering the CL thickness, ionomer volume fraction, and conductivity of the ionomer (which depends on hydration). If the catalyst layer is thin and well hydrated, this may be small, but if the CL dries, ionic resistivity increases and can severely limit performance at high current ([Analytical-based simulation approach for an anion exchange membrane fuel cell](https://www.nrel.gov/docs/fy23osti/84813.pdf#:~:text=electrodes%20are%20not%20strictly%20ohmic,of%20the%20effective%20ionic%20resistance)) ([Analytical-based simulation approach for an anion exchange membrane fuel cell](https://www.nrel.gov/docs/fy23osti/84813.pdf#:~:text=entire%20current%20density%2C%20while%20the,inherent%20water%20imbalance%20in%20an)). 
	The ohmic overpotential is $\eta_{\text{ohm}} = i (t_{\text{mem}}/\kappa_{\text{mem}} + t_{\text{CL}}/\kappa_{\text{ion,CL}} + R_{\text{GDL,elec}})$, where $\kappa_{\text{ion,CL}}$ is the proton conductivity in the CL ionomer (S/m). 
separate potentials for proton and electron conduction in the catalyst layer using Ohm’s law ($\nabla \cdot (σ_e \nabla \Phi_e) = -S_{\text{charge}}$, $\nabla \cdot (σ_i \nabla \Phi_i) = +S_{\text{charge}}$) to capture local overpotentials.

 **Electrochemically Active Surface Area (ECSA):** This is the real surface area of catalyst accessible for reaction, per unit geometric area (m²_real/m²_geo). A higher ECSA (via finely dispersed Pt nanoparticles, etc.) increases the exchange current density $i_0$ because more reaction sites are available ([Analytical-based simulation approach for an anion exchange membrane fuel cell](https://www.nrel.gov/docs/fy23osti/84813.pdf#:~:text=each%20species%20,%E2%88%92)). Often, kinetic parameters are reported per real area (i₀real in A/m²_real);
 in the model, We multiply by ECSA to get the effective $i_0$ per geometric area.
`if a cathode has ECSA = 100 m²_pt per m²_geo and the fundamental exchange current is 0.1 A/m²_pt, the effective $i_{0,\text{cath}}$ in Eq. (2) would be 10 A/m²_geo. `
ECSA can degrade over time (catalyst sintering or carbon corrosion), effectively lowering $i_0$ and thus increasing activation losses for the same current. Some models include a decay function for ECSA with time or with charge throughput.

Porosity and tortuosity modify diffusion and permeability in the mass transport equations. Pore structure and wettability determine how water saturates the electrode, affecting available area for gas flow. Resistivity and connectivity of the solid and ionomer phases influence ohmic losses in the electrodes. And ECSA scales the kinetic current response in the Butler–Volmer equations. 
We  compute a Knudsen diffusivity correction for $D_{\text{eff}}$. Electrode thickness combined with diffusivity yields the mass transport resistance that informs $i_L$.
## Membrane parameters

PEM (ion-exchange membrane)
parameters include thickness, ionic conductivity (which depends on water content), permeability to gases and water, and durability factors:
- **Thickness (tmem):**  A thinner membrane reduces ionic resistance (good for performance) but increases gas crossover and may have lower mechanical strength. Nafion membranes come in various thicknesses (e.g. Nafion 212 is 50 μm, Nafion 115 is 127 μm). In the model,
	- _tmem_ appears in ohm’s law for membrane voltage drop ($V_{\text{ohm}} = i \cdot t_{\text{mem}}/\kappa_{\text{mem}}$) and in the diffusion length for water crossover. 
	-  Thinner membranes may also have lower water intake capacity(less volume to hold water), which can lead to a more rapid drying if water balance isn't mantained at downtimes.
	- thinner membranes might increase shunt currents (in electrolyzers) due to higher ionic conductivity of leakage paths
	
- **Equivalent Weight and Water Uptake:** Membranes like Nafion are characterized by equivalent weight (EW, grams of dry polymer per mole of sulfonic acid, typically ~1100 g/mol). The **weight percent of water** or water uptake is often given as a percentage increase in mass from dry to hydrated state, or as the water content $λ$ (mentioned earlier). 
	Nafion 117 (thicker membrane) can absorb ~30% of its weight in water at 100% RH, corresponding to $λ \approx 14$ (14 H₂O/SO₃H) ( [Three-Dimensional Transport Modeling for Proton Exchange Membrane(PEM) Fuel Cell with Micro Parallel Flow Field - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC3663005/#:~:text=where%20%CE%BB%20represents%20water%20contend,of%20the%20membrane%20described%20as) ) ( [Three-Dimensional Transport Modeling for Proton Exchange Membrane(PEM) Fuel Cell with Micro Parallel Flow Field - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC3663005/#:~:text=where%20a_,expressed%20as) ).
	In the model, water uptake influences **wetting factor** – effectively how saturated the membrane is. A “wetness factor” could refer to a normalized water content $λ/λ_{\text{max}}$. If the membrane is partially dry, conductivity and $n_d$ drop. 
	Empirical conductivity relations is used  (e.g. $\kappa_{\text{mem}}(λ,T)$ , such relation for Nafion is $\kappa_{\text{mem}} = (0.005139,λ - 0.00326)\exp!\Big[\frac{1268}{303}\big(1 - \frac{303}{T}\big)\Big]$ (S/cm) ( [Three-Dimensional Transport Modeling for Proton Exchange Membrane(PEM) Fuel Cell with Micro Parallel Flow Field - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC3663005/#:~:text=) ), which shows strong dependence on $λ$ and $T$.
	Thus, membrane ionic resistance $R_{\text{mem}} = \frac{t_{\text{mem}}}{\kappa_{\text{mem}}(λ,T) A}$ couples to hydration and thermal conditions.
	
- **Gas Diffusivity (H₂ and O₂ crossover):** An ideally operating PEM should be impermeable to gases, but in reality some hydrogen and oxygen can diffuse through the membrane (especially at high pressure or thin membranes). This gas crossover is often quantified by a diffusion coefficient or **permeability** $P = D_{\text{gas}} \cdot k_H$ (product of diffusivity and Henry’s law solubility). For hydrogen in Nafion, $D_{H2}$ might be on the order of 10⁻¹¹ to 10⁻¹⁰ m²/s with a solubility that increases with pressure. 
	- In modeling Faraday efficiency
	- using a simple first-order permeation: $J_{H2,\text{xover}} = \frac{D_{H2,\text{mem}}}{t_{\text{mem}}}(C_{H2,\text{anode}} - C_{H2,\text{cath}})$ for diffusion-driven crossover ([Cathode Catalyst Layer Design in PEM Water Electrolysis toward Reduced Pt Loading and Hydrogen Crossover | ACS Applied Materials & Interfaces](https://pubs.acs.org/doi/10.1021/acsami.4c01827#:~:text=lowers%20the%20faradaic%20efficiency%20and,law%20by%20assuming%20an%20equilibrium)). Since cathode H₂ is usually near zero for (fuel cells) or anode O₂ zero (electrolyzer), it simplifies to $J_{\text{xover}} \approx \frac{D,C_{\text{feed}}}{t_{\text{mem}}}$. This s converted to a current loss ($i_{\text{xover}} = 2FJ_{H2,\text{xover}}$).
	- For oxygen crossover (less discussed because hydrogen crossover is limiting safety factor), a similar term exists.
	- Gas crossover rates increase with temperature and also if the membrane dries out (somewhat counterintuitively, dry membrane can allow more gas diffusion as polymer pores enlarge; however, very dry membrane also might crack or develop leaks).([Introducing a Novel Technique for Measuring Hydrogen Crossover in Membrane-Based Electrochemical Cells](https://www.osti.gov/servlets/purl/1774854#:~:text=diffuses%20to%20the%20anode,the%20most%20commonly%20used%20hydrogen)) (OCV drops when gases mix).

 - **Water Permeability (Darcy’s Constant):** The membrane can transport water not only by diffusion and drag, but also by pressure-driven flow if liquid water is present.
	 - a **hydraulic permeability** is defined (having units m², like Darcy’s law coefficient $K_{\text{mem}}$).  
	 **Darcy’s constant** for the membrane. If an electrolyzer anode is at higher pressure (liquid water feed) than the cathode, some water permeates and appears as vapor in the hydrogen stream. Experimental data can provide $K_{\text{mem}}$; for Nafion, values on the order of 10⁻¹⁸ to 10⁻¹⁷ m² have been reported ([[PDF] Impact of Water Properties on the Performance of PEM Electrolyzer](https://www.preprints.org/manuscript/202305.1511/v1/download#:~:text=Electrolyzer%20www,electrolyzer%20and%20further%20increase)) ([[PDF] Impact of Water Properties on the Performance of PEM Electrolyzer](https://www.preprints.org/manuscript/202305.1511/v1/download#:~:text=Additionally%2C%20TDS%20can%20cause%20fouling,electrolyzer%20and%20further%20increase)).
	this as an additional term in the water flux equation (Eq. 13). If $\Delta p$ is significant (e.g. 1–2 bar across the membrane in a pressurized system), ignoring this term could under-predict hydrogen crossover and water content on the dry side.
	
- **Electro-Osmotic Drag Coefficient:** it is a membrane property often provided by the manufacturer or measured. For Nafion at 30 °C, $n_d≈2.5$ at full hydration, dropping to ~1 at low humidity ([](https://webthesis.biblio.polito.it/30809/1/tesi.pdf#:~:text=%E2%80%A2%20Electro,7%5D%3A%20Nosmotic%20%3D%20nd)). Some advanced membranes have different $n_d$ characteristics (e.g. Aquivion, composite membranes). 
	 either a constant $n_d$ or a function $n_d(λ)$ (as in Eq. 16) ([](https://webthesis.biblio.polito.it/30809/1/tesi.pdf#:~:text=%E2%80%A2%20Electro,7%5D%3A%20Nosmotic%20%3D%20nd)). This coefficient directly influences water distribution: higher $n_d$ means the membrane pulls more water to the cathode side  which can cause anode dry-out if back-diffusion isn’t sufficient.
- **Fouling and Degradation:** Over time, membranes can experience **fouling** (if contaminants from feed gases or water enter and get trapped) and chemical degradation (attack by radicals). Fouling might introduce a resistance to water or proton transport
	- cations (Na⁺, Ca²⁺) from impure water can occupy sulfonate sites, reducing proton conductivity and water content. Fouling is set to gradually decrease $λ_{\text{max}}$ or $\kappa_{\text{mem}}$ over time or with a added R_foul.
	- if calcium contamination leads to 10% of sulfonate sites being blocked, one might multiply conductivity by 0.9 to simulate it. Fouling also refers to possible precipitation of scales in porous components in liquid-fed systems ([[PDF] Impact of Water Properties on the Performance of PEM Electrolyzer](https://www.preprints.org/manuscript/202305.1511/v1/download#:~:text=Electrolyzer%20www,electrolyzer%20and%20further%20increase)) ([[PDF] Impact of Water Properties on the Performance of PEM Electrolyzer](https://www.preprints.org/manuscript/202305.1511/v1/download#:~:text=Additionally%2C%20TDS%20can%20cause%20fouling,electrolyzer%20and%20further%20increase)). 
	- In a PEM electrolyzer, minerals in water can deposit on the membrane or electrodes, effectively adding a diffusion barrier. In modeling, one could increase $R_{\text{ohm}}$ or decrease $K_{\text{mem}}$ to reflect that. While detailed fouling chemistry is beyond scope, its impact can be captured by adjusting model parameters and is often validated against long-term performance decline.
	
- **Voltage Loss and Shunt Currents:** In multi-cell stacks, **shunt currents** are unwanted leakage currents that bypass some cells and cause additional voltage losses. They typically occur when a conductive path exists outside the intended circuit – for example, in a PEM **electrolyzer stack** with a common water feed manifold, the water can conduct current from a high-voltage cell to a lower-voltage cell, effectively bypassing some of the load ([Shunt Currents in an Alkaline Electrolyzer Stack - COMSOL](https://www.comsol.com/model/shunt-currents-in-an-alkaline-electrolyzer-stack-113041#:~:text=Shunt%20Currents%20in%20an%20Alkaline,shunt%20currents%20flow%20between)) ([Shunt Currents in an Alkaline Electrolyzer Stack - COMSOL](https://www.comsol.com/model/shunt-currents-in-an-alkaline-electrolyzer-stack-113041#:~:text=In%20an%20alkaline%20electrolyzer%20stack%2C,shunt%20currents%20flow%20between)). Shunt currents do not pass through the membrane of each cell and thus do not generate hydrogen, hurting Faraday efficiency.  
- The **shunt loss** is the voltage drop due to this current in the external circuit. If $I_{\text{shunt}}$ flows through a resistance outside the cell, that is a loss of current to the stack’s output. 
- shunt effects by reducing the net current that actually goes through the cells: $I_{\text{net}} = I_{\text{draw}} - I_{\text{shunt}}$. Alternatively, an efficiency term can be included similar to Faraday efficiency.
- Empirical functions exist; shunt current often increases with the number of cells (higher total stack voltage) and the conductivity of the fluid path. A simple model might assume $I_{\text{shunt}} = \frac{V_{\text{stack}}}{R_{\text{leak}}}$, where $R_{\text{leak}}$ depends on water conductivity and geometry of the manifold. The **shunt voltage loss** then is $I_{\text{shunt}}\times R_{\text{ext}}$, but since $R_{\text{ext}}$ is just the circuit, more directly it just means less current is delivered. 
- In terms of efficiency, one could write an effective $\eta_{\text{shunt}} = 1 - I_{\text{shunt}}/I_{\text{total}}$. 
- In a well-designed PEMFC stack (with separate gas lines per cell), shunt currents are negligible, but in electrolyzers they can be a few percent of the current ([Faraday’s Efficiency Modeling of a Proton Exchange Membrane Electrolyzer Based on Experimental Data](https://www.mdpi.com/1996-1073/13/18/4792#:~:text=been%20carried%20out%20on%20the,current%20and%20hydrogen%20pressure%20on)) ([Faraday’s Efficiency Modeling of a Proton Exchange Membrane Electrolyzer Based on Experimental Data](https://www.mdpi.com/1996-1073/13/18/4792#:~:text=expression%20valid%20for%20the%20PEM,efficiency%20according%20to%20the%20operating)). Mitigation involves segmenting the manifold or adding resistive shims to increase the path resistance. In modeling a single cell, shunt currents are usually not included. 

Trade


**Sources:**

1. Springer, T. E. _et al._ “Polymer Electrolyte Fuel Cell Model.” _J. Electrochem. Soc._ **138**, 2334 (1991).
2. Bernardi, D. M. & Verbrugge, M. W. “Mathematical Model of a Gas Diffusion Electrode Bonded to a Polymer Electrolyte.” _J. Electrochem. Soc._ **139**, 2477 (1992).
3. Wang, Y. _et al._ “Modeling two-phase flow and liquid water transport in PEM fuel cells.” _J. Power Sources_ **147**, 148–161 (2005).
4. Hinaje, M. _et al._ “Faraday’s Efficiency Modeling of a PEM Electrolyzer Based on Experimental Data.” _Energies_ **13**, 4792 (2020). ([Introducing a Novel Technique for Measuring Hydrogen Crossover in Membrane-Based Electrochemical Cells](https://www.osti.gov/servlets/purl/1774854#:~:text=diffuses%20to%20the%20anode,the%20most%20commonly%20used%20hydrogen)) ([Cathode Catalyst Layer Design in PEM Water Electrolysis toward Reduced Pt Loading and Hydrogen Crossover | ACS Applied Materials & Interfaces](https://pubs.acs.org/doi/10.1021/acsami.4c01827#:~:text=lowers%20the%20faradaic%20efficiency%20and,law%20by%20assuming%20an%20equilibrium))
5. Mora, J. M. _et al._ “Analytical Model for Anion Exchange Membrane Fuel Cells: Coupled Electrochemical, Thermal, and Water Management.” _Energy Conv. Manag._ **273**, 116382 (2022). ([Analytical-based simulation approach for an anion exchange membrane fuel cell](https://www.nrel.gov/docs/fy23osti/84813.pdf#:~:text=The%20Nernst%20equation%20is%20used,%E2%88%92%20%F0%9D%91%85%F0%9D%91%87)) ([Analytical-based simulation approach for an anion exchange membrane fuel cell](https://www.nrel.gov/docs/fy23osti/84813.pdf#:~:text=each%20species%20,%E2%88%92))
6. Polito, M. _et al._ “High-Fidelity PEM Fuel Cell System Modeling for Maritime Applications.” Politecnico di Torino Thesis (2021). ([](https://webthesis.biblio.polito.it/30809/1/tesi.pdf#:~:text=As%20soon%20as%20the%20a,current%20are%20the%20Activation%20Losses)) ([](https://webthesis.biblio.polito.it/30809/1/tesi.pdf#:~:text=Practically%2C%20is%20evaluated%20the%20water,anode%20and%20cathode%20catalyst%20layer))
7. Zhu, X. G. _et al._ “Three-Dimensional Transport Modeling in PEM Fuel Cells with Parallel Channels.” _Int. J. Energy Res._ **35**, 940–955 (2011). ( [Three-Dimensional Transport Modeling for Proton Exchange Membrane(PEM) Fuel Cell with Micro Parallel Flow Field - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC3663005/#:~:text=2) ) ( [Three-Dimensional Transport Modeling for Proton Exchange Membrane(PEM) Fuel Cell with Micro Parallel Flow Field - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC3663005/#:~:text=%23%201%29.%20Electro) )
8. Kusoglu, A. & Weber, A. Z. “New Insights into Perfluorinated Sulfonic-Acid Ionomers.” _Chem. Rev._ **117**, 987–1104 (2017). (Membrane properties and water transport).
9. Yi, J. S. & Nguyen, T. V. “An along-the-channel model for PEMFC.” _J. Electrochem. Soc._ **145**, 1149 (1998). (Mass transport and two-phase effects).
10. Komsiyska, L. _et al._ “Hydrogen crossover in PEM electrolysis: dependence on membrane properties and differential pressure.” _Electrochim. Acta_ **178**, 592–600 (2015).
































# Footnotes

[^1]: - **0D (Lumped Parameter):**
	    
	    Treats the entire system as a single, uniform entity, using ordinary differential equations to model changes over time. This approach is computationally fast but neglects spatial variations and may not accurately capture local phenomena. 
	    
	- **1D:**
	    
	    Accounts for changes in one spatial dimension (e.g., along the flow direction) while assuming uniformity in the other two. This allows for more detailed modeling of transport phenomena like mass transfer and heat transfer within a single cell. 
	    
	- **2D:**
	    
	    Models changes in two spatial dimensions (e.g., across the membrane plane) and assumes uniformity in the third. This approach is useful for studying phenomena like electrode potential variations and flow distribution within a single cell or across a stack. 
	    
	- **3D:**
	    
	    Provides the most detailed spatial resolution, modeling changes in all three dimensions. This allows for a comprehensive understanding of the system, including phenomena like pressure drop, temperature distribution, and gas mixing across the entire electrolyzer stack.
