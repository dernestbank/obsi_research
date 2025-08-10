
- [x] Aims and objective slides + Animations
- [ ] Finish all methods and results writeup
	- [ ] Aim 1
	- [ ] Aim 2
	- [ ] Aim 3
- [ ] literature review content
- [ ] reference add ( IEE)
- [ ] background animation



Challenges and limitations from literature




Slide content:
---
Affirmative header: message i want to communicate

Figure of results, illustrate
	
Summary of information and results communicated.
	Challenge being addressed
	why it's important (notes_clue)
	messages to communicate
Table of basis and assumptions.
Reference


Figures
---
Arial font
Width boarders
Annotations if necessary

How to interprete()
	Follow annoation
	
#Citations 
---
I provide details such as the full citation, DOI, title and authors, etc.),
generate them for you in the same shortened format as your example:

**[Number]. [First Author Initial]. [Last Name] et al., [Journal Abbreviation]. [Year], [Volume], [Page Range/Article Number].**

(in APA style):
U.S. Energy Information Administration. (2023, May). _Monthly Energy Review_. Retrieved July 10, 2024, from [https://www.eia.gov/totalenergy/data/monthly/index.php](https://www.eia.gov/totalenergy/data/monthly/index.php)

Assuming this is the next reference in your list, here is option 6:

**6. U.S. EIA, _Monthly Energy Review_, May 2023.**






# Aims and objectives

#structure 
	Aims and task
	Method
	Results 
	Recommendation






## Introduction


cost drivers( technoeconomic background)
- conflicts from literature on cost drivers
- supply chain : production cost vrs stoarge ctransportation.(add bbasis to the transportation)
`manufactuing parameters targeting the capital cost, econoic paramters targets the operational cost, the perfomance paramters targeting the efficiency of the sytsem `

research gap:


Energy config
- opportunities for policy implementation and valuation
- geographic variability in the cost of hydrogen
- 


# Background

#### slide 1

Challenges and limitations from literature

**What Has Been Done**

- State-of-the-art materials have been established: PFSA membranes (like Nafion), Platinum-group metals for catalysts (Iridium Oxide for the anode, Platinum on Carbon for the cathode)


**Research Gaps**
- There is a disconnect between lab-scale material discoveries and their real-world economic impact when scaled up.
- A need exists for stable, earth-abundant alternative materials such as catalysts to replace iridium.

**Key Literature References**
- Carmo et al., _Int. J. Hydrogen Energy_, 2013 (Comprehensive PEM Review)
- Klose et al., _Adv. Energy Mater._, 2020 (Hydrocarbon Membranes)

@curcioTechnoeconomicAnalysisHydrogen2025
@badgettMethodsIdentifyingCost2021
##### Slide 2
Existing Economic Models Provide a Foundation but Often Oversimplify Reality with Static Assumptions


research
Tool accessibility & scaling: Proprietary simulation platforms limit reproducibility; little open-source work unifying electrochemical detail with economic scaling
Downstream oversimplifications: Storage, transport, co-product valorization (e.g., O₂), and stack replacement scheduling are frequently omitted or treated separately

Implication: These conflicts and simplifications propagate into wide LCOH uncertainty and weaken strategic decision guidance.

**Reproducibility/accessibility:** Need for an open-source, validated framework that can be used by academia and startups without reliance on black-box tools.

**Challenges & Limitations**

- **Static Nature:** Most models are fundamentally static, using fixed, year-long averages. They cannot capture the hour-by-hour operational dynamics required when using variable renewable energy.
    
- **Unrealistic Assumptions:** Many studies assume constant, low electricity prices and unrealistically high capacity factors (e.g., 90%), which are not achievable with solar or wind power alone.
    
- **Simplified Degradation:** Stack degradation is typically modeled as a simple replacement every 7-10 years, ignoring the gradual loss of efficiency that increases electricity consumption over the stack's life.


##### Slide 3
Integrating Renewables is Essential for "Green" Hydrogen, but Intermittency Poses the Core Economic Challenge

**What Has Been Done**
- Various renewable energy (RE) configurations have been explored, including solar-only, wind-only, and hybrid systems

Challenges & Limitations

Research Gaps

Techno-economic analyses (H2A framework) quantifying LCOH under fixed assumptions of capacity factor and static electricity prices.

Static TEA assumptions: Common models assume constant capacity factor and flat electricity prices, failing to capture hourly renewable variability and electrolyzer flexibility.

@bracciCostComparisonVarious2023
@satyapalDOEHydrogenProgram2023



------


Aim 1
---
To design and optimize a physics-based electrochemical model for PEM electrolyzer hydrogen production simulation and optimization.

Tasks
Task 1.1 Review and design a standard PEM electrolyzer model.
Develop and refine a lumped‑parameter PEM electrolyzer model incorporating activation, ohmic, and concentration overpotentials, membrane hydration, Faradaic
Task 1.2
validate the electrochemical model against experimental polarization and efficiency data to ensure predictive accuracy.
Future
Task 1.3
Perform a multi‑objective design optimization simultaneously balancing efficiency, cost, and durability metrics to identify optimal operating and material configurations.

### Results: Validation
- Title: Validated Model Accurately Predicts PEM Cell Performance

 The electrochemical model reproduces real‑world polarization behavior across low to high current densities (0–3 A/cm²) under industrial operating conditions.
- Validation:
Model vs. Debe et al. data yields RMSE ≈ 15 mV, confirming accuracy of activation, ohmic, and mass‑transport submodels.
Source of error: faradic efficiency simplification, we assume a steady state, uniform current density, 
##### Possible Sources of Error
- **Parameter Uncertainty:** Variations in catalyst loading or membrane hydration not captured exactly.
- **Simplified Hydration Dynamics:** Lumped hydration model may under‐represent transient water transport effects.
- **Data Digitization:** Experimental points extracted from published plots introduce small reading errors.
- **Uniform Flow-Field Assumption:** Real cells may exhibit channel‐to‐channel pressure or temperature gradients.
- table
PEM Configuration: anode and cathode catalyst type of membrane

|**Component**|**Specification**|
|---|---|
|**Membrane**|Nafion™ 117, 183 µm thickness|
|**Catalyst Layer**|Pt–Ir oxide, 0.5 mg/cm² loading|
|**Flow Field Plates**|Serpentine, graphite composite|
|**Active Area**|877 cm²|
|**Operating Pressure**|1 bar (anode) / 30 bar (cathode)|
|**Cell Temperature**|333 K|
|**Stack Power**|19 034 kW|

**Overpotential Breakdown:**
- Activation losses dominate at low currents (< 1 A/cm²)
- Ohmic losses significant across the range, rising linearly
- Diffusion overpotentials become non‑negligible beyond 1.5 A/cm²
Activation overpotential is dominant,
we see and increasing ohmic overpotential with increasing current density.

Refs
@debeInitialPerformanceDurability2012

-> B. Han et al., Int. J. Hydrogen Energy 2015, 40, 7006–7016.
[1] B. Han, S. M. Steen, J. Mo, and F.-Y. Zhang, “Electrochemical performance modeling of a proton exchange membrane electrolyzer cell for hydrogen energy,” International Journal of Hydrogen Energy, vol. 40, no. 22, pp. 7006–7016, Jun. 2015, doi: 10.1016/j.ijhydene.2015.03.164.



M. K. Debe _et al._, “Initial Performance and Durability of Ultra-Low Loaded NSTF Electrodes for PEM Electrolyzers,” _J. Electrochem. Soc._, vol. 159, no. 6, pp. K165–K176, 2012, doi: [10.1149/2.065206jes](https://doi.org/10.1149/2.065206jes).

[1]
 -> F. Scheepers et al., Energies 2020, 13, 30612.
F. Scheepers _et al._, “Improving the Efficiency of PEM Electrolyzers through Membrane-Specific Pressure Optimization,” _Energies_, vol. 13, no. 3, Art. no. 3, Jan. 2020, doi: [10.3390/en13030612](https://doi.org/10.3390/en13030612).

### Results: Sensitivity
1.2 Membrane thickness:
Thickness level application in fuel cell vrs electrolyzer.
ohmic overpotential
- Thicker membranes (25 µm → 50 µm) increase ohmic losses, raising cell voltage by ~100–200 mV at 2 A/cm². 
- Thinner membranes reduce ohmic drop but may compromise mechanical stability and gas crossover.

Temperature:
Basics for SOEC, high temperatures.
Higher temperatures minnimizes activation overpotential by increasing the ration

- Higher temperatures (323 K → 383 K) lower activation and ohmic losses, decreasing cell voltage by ~50–100 mV across the range.
- Elevated temperature enhances ionic conductivity but may accelerate membrane degradation


Results: contours


Aim two
--
To Construct a Modular Techno-Economic Assessment (TEA) Integrating Physic-Based Electrolyzer model. 


Task 2.1: Model and establish a baseline scenario for PEM electrolyzer hydrogen production.
Task 2.1. Conduct a comprehensive techno-economic analysis (TEA) of the base-case process and identify key drivers of the production process economics

Task 2.1

The Challenge Being Addressed:

Determining the optimal plant size by balancing capital cost reductions against rising operational costs.

**Results Summary:**

- Scaling from a distributed (1,500 kg/day) to a baseline (10,000 kg/day) plant reduces LCOH by 21% (from $8.88/kg to $7.05/kg). This is driven by the reduction in the relative contribution of Fixed Capital Investment (FCI).
    
- Further scaling to a centralized (50,000 kg/day) plant provides minimal cost reduction because electricity feedstock becomes the overwhelming cost driver.
    
- The IRR and NPV improve significantly with scale, confirming financial viability, but the LCOH benefit flattens.
    
- This establishes a "sweet spot" for plant sizing around the **10,000 kg/day** mark to balance cost and complexity.

**Economies of Scale in CAPEX**  
This scale effectively dilutes fixed costs over a larger production volume.
Uninstalled capital cost declines from $2 000/kW (1.5 t/ d) to $995/kW (10 t/ d) and $708/kW (50 t /d), reflecting strong scale‐up benefits.
While fixed costs continue to decrease on a per-kilogram basis, electricity feedstock costs, which scale linearly with output, become the dominant factor, offsetting further capital saving


Centralized (50 t/ d) sees slight rebound (~$7.3/kg) due to diminishing operational efficiencies at very large scale.
Fixed OPEX and fixed capital investment shares decrease from ~30 % to ~20 % with scale

- **Benchmark Implications**  
    The 10 t d⁻¹ configuration represents an optimal balance of low LCOH and robust financial returns, suggesting a mid‐scale plant may be most viable under current cost assumptions.
    
- **Policy & R&D Focus**  
    Targeted reductions in electricity price and SEC are critical across all scales; capital‐expenditure innovations yield the greatest marginal benefit at small to mid‐scale projects.


---
Econies of scale



Sensitivity of LCOH
basline:
take away
practi

electricity cost as the most influential factor for green hydrogen economics

Electricity cost
distribution of eectricity.
refs
@2025StateCorporate2025
@penevTechnoEconomicModellingH2A
Krishnan
S. Krishnan et al., Int. J. Hydrogen Energy 2023, 48, 32313–32330
@krishnanPresentFutureCost2023
@fuelcellstoreMembranes
@chemoursNafionMembranesDispersions
J. J. Caparrós Mancera et al., Electronics 2020, 9, 0871.
@bessarabovPEMElectrolysisHydrogen2016; @bessarabovPEMWaterElectrolysis2018
temperture
. R. Escobar-Yonoff et al., Heliyon 2021, 7, 3.
D. Bessarabov et al., PEM Elec. Hyd. Prod: CRC Press, 2016
@TotalEnergyM

target
@satyapalDOEHydrogenProgram2023
@doeHydrogenShot2020
@jamesHydrogenProductionCost; @badgettUpdatedManufacturedCost2024
likely questions

- [ ] Depreciation method: 20-year MACRS explain
- [ ] weighted average cost of capital




Aim three
--

Aim 3: To Integrate Dynamic, Hourly-Resolved Renewable Energy Modeling and Location-Specific Optimization. 
- **Task 3.1:** Model a dynamic renewable‑energy system (PV, wind, and hybrid configurations) to produce hourly generation and price profiles.
    
- **Task 3.2:** Integrate the dynamic RE system with the validated PEM electrolyzer TEA framework to simulate coupled operation under real‑time dispatch and electrolyzer flexibility.
    
- **Task 3.3:** Generate spatial LCOH maps across selected U.S. regions. highlighting geographic cost variation as a function of local renewable resource profiles and electricity tariffs.

Task 3.1 is to model a dynamic renewable-energy systemfor PV, wind an hybrid configurations. to produce dynamic renewable‑energy system (PV, wind, and hybrid configurations) to produce hourly generation and price profiles.Task 3.2  will combine the outputs from Aim 1 and Aim 2 with an energy sub-module to simulate a typical U.S region.



Method

refs: O. C. Castillo, V. R. Andrade, J. J. R. Rivas, and R. O. González, “Comparison of Power Coefficients in Wind Turbines Considering the Tip Speed Ratio and Blade Pitch Angle,” Energies, vol. 16, no. 6, Art. no. 6, Jan. 2023, doi: 10.3390/en16062774. 
>>O. C. Castillo et al., Energies 2023, 16, 62774.

A. Delgado, C. Gertig, E. Blesa, A. Loza, C. Hidalgo, and R. Ron, “Evaluation of the variability of wind speed at different heights and its impact on the receiver efficiency of central receiver systems,” AIP Conference Proceedings, vol. 1734, no. 1, p. 030011, May 2016, doi: 10.1063/1.4949063.
>> A. Delgado et al., AIP Conf. Proc. 2016, 1734, 030011.


PV

**Key Inputs:**
- **Hourly Irradiance Data:** Utilizes high-resolution Global Horizontal Irradiance (GHI) and Direct Normal Irradiance (DNI) from reanalysis datasets (e.g., NSRDB, MERRA-2) for the specific geographic location.
- **System Parameters:** Includes PV panel efficiency, array tilt and azimuth angles, derating factors (e.g., for temperature, soiling, shading), and inverter efficiency.
- **Temperature Effects:** Accounts for temperature-dependent performance degradation of PV panels

derating factor vrs degradation rate

derating factor accounts for real-world applications like shading , temperature fluctuations, dust
Systematic losses 
an annual degradation rate towards the end of life 25 yrs is.

 Solar irradiation intensity falls

Table of assumptions:

Image of hourly solar distribution
Image of annual simulation

![[image-4.png]]

https://www.tandfonline.com/doi/full/10.1080/15435075.2018.1529593#d1e285
@jahidHybridPowerSupply2019
## Summary

We modeled and developed a physics-base PEM electrolyzer with a 32mV RMSE against experimental polarization curves. , 

Identified optimum range of design parameter at of with current density (1.5-2)A/cm2, thin (< 125 µm) membranes and temperature (60–80 °C) for maximum efficiency  to reach sub-$7 /kg LCOH

Established a pre-optimum echno-economic design baseline capacity of f 10,000 kg H₂/day at 333 K and 30 bar, assuming an industrial electricity rate of $0.073 /kWh for LCOH of $7 /kg LCOH

Identified the primary cost drivers as electricity cost, capital cost and energy efficiency.
secondary cost drivers: secondary drivers include the system’s specific energy consumption (SEC), tax rates, and fixed O&M costs.

The solar energy is the most cost effective RE configuration
Found an optimal capacity factor of 40-50 % for renewable energy supply, balancing intermittency with plant utilization.



1. Model Validation: Achieved an RMSE of 32 mV against experimental polarization curves, indicating activation overpotentials dominatethe toal voltage loss.
2. PEM design optimization: Optimized PEM electrolyser design parameters with current density (1.5-2)A/cm2, thin (< 125 µm) membranes and temperature (60–80 °C) for maximum efficiency  to reach sub-$7 /kg LCOH
3. Techno-economic Baseline Design: Determined an optimal electrolyzer capacity of 10,000 kg H₂/day at 333 K and 30 bar, assuming an industrial electricity rate of $0.073 /kWh for LCOH of $7 /kg LCOH
4. Cost Drivers: Identified electricity expenses as the primary cost driver, followed by uninstalled capital costs; secondary drivers include the system’s specific energy consumption (SEC), tax rates, and fixed O&M costs.
5. Renewables Integration: Found an optimal capacity factor of 40-50 % for renewable energy supply, balancing intermittency with plant utilization.


# Extra

S. Krishnan et al., Int. J. Hydrogen Energy 2023, 48, 32313–32330
@krishnanPresentFutureCost2023
![[PEM material selection choice.png]]


![[material.png]]
