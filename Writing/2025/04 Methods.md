

Chapter 4: Materials and Methods 
	[4.1. Overview of the modelling process. ](#_Toc192135826)
	TEA, H2A mention
	[4.2. Scope and indicators. 18]
	system boundary
	metrices (LCOH, NPV, IRR)
	[4.3. Cost model unit and data sources. ]
	cost model curve, H2A
	H2A and data tables, Price and costs,estimates
	RE cost model
	Operational cost
	LCOE 
	Primary and secondary data sources.
	[4.4. System analysis. 18](#_Toc192135829)
	System design and parameters
	Parameters and design considerations.
	System efficiency and energy consumption
	BoP and Energy balances assumptions
	DCCF, process
	[4.4.1. Process economics. 18](#_Toc192135830)
	Tables of	OPEX structure, Capex structure
	Assumptions

4.4.2. Sensitivity and uncertainty analysis 

for RE
Economies of scale, indirect cost + operating cost
cost for battery

for rid
cost for grid connection
Fixed price of  bought from grd





Insp @kimTechnoeconomicAnalysisAnion2024

4. Methodology

 4.1 Electrolyzer Model Validation
	4.1.2 Model Parametrization
	4.1.2 Model Validation
	4.1.3 Sensitivity of key model parameters
 4.2. Technoeconomic analysis and Frameworks
	4.2.1 Design basis
		Reference plant specifications (capacity, SEC, uninstall cost, etc
		Financial assumptions (WACC, tax rate, depreciation schedule  etc
	4.2.2 Process description
	Base case study.
		- Flow diagram of hydrogen production process
	    - Base Case Study: 10 000 kg H₂/day PEM plant
	    - Data sources for CAPEX, OPEX, performance inputs
	4.2.3 Description of framework
	Structure of the TEA module (input–output mapping)
	Integration of electrolyzer model outputs (SEC, efficiency)
	integration of energy system
 4.3. Scope and indicators
4.3.1 System boundary
	Surrounding: no compression, transportation
	Define clear, transparent goals
	• Time horizon
	• Target audience
	• Potential limitations in usability
	• Product application
	• Functional unit/reference flow, kg of Hydrogen
	 Location
	• Feedstocks and other raw 	materials( energy and non energy feedstock)
	• Products, byproducts and waste
	• Systems boundaries
	• Scenario analysis
4.3.2 Key metrics: LCOH , NPV ($), IRR (%)

 4.4. Cost modeling
**4.4.1** Capital cost breakdown (stack vs. BoP)
**4.4.2** OPEX components: electricity, water, maintenance, replacements

 4.5. Sensitivity and uncertainty analsysi analysis

 4.5.1 System efficiency
 4.5.2 Parameters sensitivity and uncertainty analysis
 **4.5.1** Univariate sensitivity (tornado diagrams) on key inputs
 **4.5.2** Multivariate to capture parameter interactions
    Contour
    Monte Carlo


 4.4.1. Process parameters and economics
Capital investment, Operating and feedstock cost

4.4.2 Parametric sensitivity analysis

 4.4.2. Sensitivity analysis and optimization

Sensitivity on PEM electrolyzer model
Design parameters, variables


## 4.1 Mathematical model 



@inps: @chungDesignSpacePEM2024 . supplementary

Model is validiated against experimental works. experiments that were conducted in different operating conditions. 

In the first benchmarking experiment 12 a single-cell electrolyzer with Nafion 117 (membrane thickness of 178 μm) was tested at two different temperatures (50°C and 80°C) at ambient pressure. was used.


Experimented data from sheepers et al. (2020), Jang et al 2022, Chung et al 2024
Scheepers et al. (2020):
 Nafion 212 has been used as the membrane (dm = 51 μm), and a platinum loading of the cathode of 0.25 mg cm−2 and an iridium oxide loading of the anode of 0.96 mg cm−2 have been used. The ionomer content was set to 10 wt.%. Platinum-coated Bekaert titanium felt (350 μm) was used as the anod
Chung
 Nafion 117 (membrane thickness of 178 μm)
@scheepersImprovingEfficiencyPEM2020; @jangTechnoeconomicAnalysisMonte2022; @chungDesignSpacePEM2024
Electrolyzer params


Table S4 summarizes the parameters that were used in the model.
![[image-42.png]]

![[image-43.png]]



To ensure the fidelity of our PEM electrolyzer model, we benchmarked its predictions against multiple peer-reviewed experimental studies covering a range of operating conditions, cell designs, and materials. We primarily compared model outputs to single‐cell measurements from Debe et et al. (2024) using a Nafion 117 membrane (178 µm thick) at ambient pressure and  temperatures, 23 K (50 °C) and 353 K (80 °C), over current densities up to 2 A cm⁻² @debeInitialPerformanceDurability2012 
Other secondary source of experimental data were considered [@scheepersImprovingEfficiencyPEM2020; @jangTechnoeconomicAnalysisMonte2022; @chungDesignSpacePEM2024]. 
The validation focused on reproducing polarization curves (cell voltage vs. current density) and Faradaic efficiency across a range of temperatures, pressures, and catalyst loadings.





We compared model outputs to single‐cell measurements from Debe et et al. (2024) using a Nafion 117 membrane (178 µm thick) at ambient pressure and two temperatures, 23 K (50 °C) and 353 K (80 °C), over current densities up to 2 A cm⁻² @debeInitialPerformanceDurability2012   .



Whereas the data from Scheepers et al. (2020) employed a Nafion 212 membrane (51 µm), platinum cathode loading of 0.25 mg cm⁻², and iridium‐oxide anode loading of 0.96 mg cm⁻², with 10 wt.% ionomer content and platinum‐coated titanium felt electrodes [@scheepersImprovingEfficiencyPEM2020].


- {'RMSE': 0.03236, 'MAE': 0.0279, 'R2': 0.8969}



### 4.1.1 Electrolyzer Model Design

All the equation


### 4.2 Electrolyzer Model Validation and parameterization

To ensure the fidelity of our PEM electrolyzer model, we benchmarked its predictions against multiple peer-reviewed experimental studies covering a range of operating conditions, cell designs, and materials. We primarily compared model outputs to single‐cell measurements from Debe et et al. (2024) using a Nafion 117 membrane (178 µm thick) at ambient pressure and  temperatures, 23 K (50 °C) and 353 K (80 °C), over current densities up to 2 A cm⁻² @debeInitialPerformanceDurability2012 
Other secondary source of experimental data were considered [@scheepersImprovingEfficiencyPEM2020; @jangTechnoeconomicAnalysisMonte2022; @chungDesignSpacePEM2024]. 
The validation focused on reproducing polarization curves (cell voltage vs. current density) and Faradaic efficiency across a range of temperatures, pressures, and catalyst loadings. The sensitivity of the design parameters to the cell voltage at different current densities are tested.






#### **4.2.2 Model Parametrization**
A quasi-one-dimensional (0D/1D), physics-based model of a PEM electrolyzer stack was developed to form the technical foundation of this study. The model integrates key electrochemical and physical phenomena to predict the performance and efficiency of the electrolyzer under various operating conditions. A comprehensive water balance is maintained by accounting for electro-osmotic drag, back-diffusion, and hydraulic permeation across the polymer electrolyte. 


The model was parameterized based on literature data for a commercial-scale PEM electrolyzer. The baseline parameters include a cell active area of 877cm2, a Nafion 117 membrane thickness of $178 \mu m$, and specific catalyst loadings for the anode and cathode. The nominal operating point was set at 333.15 K and a maximum current density of 2A/cm2, with the cathode operating at a pressure of 30 bar. A summary of the design parameters is given in <mark style="background: #FF5582A6;">table### </mark>The electrochemical model was prototyped in an Excel workbook and subsequently implemented as a more detailed, object-oriented Python class to facilitate dynamic simulations and integration with other modules. The codes for the mode is given in the <mark style="background: #FF5582A6;">APPENDIX</mark>

Table here.


A schematic of the PEM model inputs and outputs.
![[A schematic of the PEM model inputs and outputs..png]]
#### **4.2.2 Model Validation and sensitivity**

To ensure its accuracy and reliability for techno-economic analysis, the physics-based PEM electrolyzer model was rigorously validated against experimental data from literature. The validation process involved comparing the model's predictions with results from experiments conducted under various operating conditions. @debeInitialPerformanceDurability2012 The model's performance was benchmarked against polarization curves from MEA made of Nafion 117 membrane (178 μm thickness) at ambient anode pressure and operating temperature: 60°C (323.15 K). And Curre

A key validation was performed by comparing the model's predictions against experimental polarization curves from Scheepers et al. for a Nafion 117–based stack operated at 333 K and 30 bar. The model successfully reproduced the observed cell voltage to R2 and RMSE of 0.032 respectively across a current density range of 0.5 to 2.0 A/cm². Furthermore, it accurately matched experimentally measured gas crossover rates, with the predicted H₂ permeation remaining below 1% of the total hydrogen produced.

corresponding operating temperature value was 80 C and the PEM thickness was 178 microns
presents the comparison of the present model and experimental data of PEM electrolyzer cell polarization curve under the same pressure, temperature and





We primarily compared model  the model's predictions against experimental polarization curves from Debe et et al. (2024) of  a Nafion 117 membrane (178 µm thick) at ambient pressure and  temperatures, 23 K (50 °C) and 353 K (80 °C), over current densities up to 2 A cm⁻² @debeInitialPerformanceDurability2012 
Other secondary source of experimental data were considered [@scheepersImprovingEfficiencyPEM2020; @jangTechnoeconomicAnalysisMonte2022; @chungDesignSpacePEM2024]. 
The validation focused on reproducing polarization curves (cell voltage vs. current density) and Faradaic efficiency across a range of temperatures, pressures, and catalyst loadings. 
A local sensitivity analysis examined the influence of uncertainties in exchange current density ($i_0$​) and membrane thickness, and Temperature on cell voltage .


#### **4.2.3** Sensitivity of key model parameters



<mark style="background: #FFB86CA6;">insps</mark> : @hanElectrochemicalPerformanceModeling2015





### 4.3 Energy system Design

#### 4.3.1 Wind energy

#### 4.4.1  Photovoltaic system




## 4.2 Technoeconomic analysis and Framework 

 4.2. 1 Design basis	

Process Basis – feed/product flow rate used and why, other assumptions (e.g.,SEC efficiency, Product pressure, purity, etc.)

Economic Basis - minimum acceptable DCFROR, rate for profitability calculation, depreciation method, tax rate, life of the plant, utility costs, etc.

The process baseline is a 10, 000kg/day chosen as a mid point between DOE's defined distributed/ onsite generation and centralized production systems. The baseline assumes a point of diminishing returns on economy of scale by capacity.  The centralized system and distributed is a 50,00kg/day and 1500kg/day hydrogen production capacity.  @jamesFinalReportHydrogen2016
To estimate hydrogen production costs under different scenarios coupling PEM electrolyzers with diverse, clean energy sources.
Our analysis is based on a distributed or on-site production case (1,500 kg/day) and central production  (50,000kg/day)  .  A somewhat mid point 10,000 kg/day is chosen as a preferred optimal size (case) based on the scaling and diminishing return point between our reference points..  @jamesFinalReportHydrogen2016
The baseline is shown in table ## and future at Appendix A





Table 4.2.1:  Parameters for Distributed , baseline and centralized hydrogen production systems

| Parameters                       | Distributed | Baseline                           | Centralized |
| -------------------------------- | ----------- | ---------------------------------- | ----------- |
| Production capacity, kg/day      | 1,500       | 10,000                             |             |
| Start-up Year                    | 2024        | 2024                               | 2024        |
| Total Uninstalled Capital ($/kW) |             | $995                               |             |
| Total Electrical Usage (kWh/kg)  | 54.3        | 54.3 [% LHV] (61%) (% HHV) (72.6%) | 54.3        |
| Stack Electrical Usage (kWh/kg)  | 49          | 49 [% LHV] (68%) (% HHV) (80%)     |             |


Key assumptions for the Baseline.
A 20-year plant lifetime with stack replacement every 10 years.
A 10% weighted average cost of capital (WACC) and a 27% corporate tax rate.


A plant capacity factor of 90%, with startup year production conservatively set to 50% of nameplate capacity to account for commissioning and ramp-up.

A baseline electricity cost of $0.07/kWh.


---

### **4.2.1 Design Basis**

We modeled a  plant capable of producing 10,000 kg H₂/day, chosen as the pre-optimal midpoint between small-scale (1,500 kg/day) and large-scale (50,000 kg/day) facilities to balance economies of scale against . @jamesFinalReportHydrogen2016 The boundary mirrors DOE H2A PEM case studes for distributed and central hydrogen production system. The baseline capacity reflects the inflection point at which diminishing returns begin to outweigh cost savings from further scaling.    The basis allow co-location with wind or solar farms or embedded at industrial brown-fields sites.



Distributed , Baseline and centralized

| Parameters                       | Distributed | Baseline                           | Centralized |
| -------------------------------- | ----------- | ---------------------------------- | ----------- |
| Production capacity, kg/day      | 1,500       | 10,000                             | 50,000      |
| Start-up Year                    | 2024        | 2024                               | 2024        |
| Total Uninstalled Capital ($/kW) | 2000        | $995                               | 708         |
| Total Electrical Usage (kWh/kg)  | 54.3        | 54.3 [% LHV] (61%) (% HHV) (72.6%) | 54.6        |
| Stack Electrical Usage (kWh/kg)  | 49          | 49 [% LHV] (68%) (% HHV) (80%)     | 49          |


##### **4.2.1.1 Process basis**

The electrolyzer stack is operated at **333 K** with an anode pressure of 1 bar and a cathode (product) pressure of **30 bar**, delivering high-purity hydrogen suitable for downstream applications without additional compression at the plant fence. The validated physics model predicts a **specific energy consumption (SEC)** of 49 kWh kg⁻¹ at stack level and **54.3 kWh kg⁻¹** system-wide once balance-of-plant (BoP) loads are included. Purity exceeds 99.97 % on a dry basis, and Faradaic losses from gas crossover remain below 1 % under these conditions, as corroborated by the Scheepers et al. data set used for model calibration. A nominal capacity factor of **90 %** is assumed after the commissioning year, during which production ramps linearly from 50 % of nameplate to full output; BoP and O&M expenditures are scaled accordingly. Water consumption is fixed stoichiometrically at 9 kg H₂O per kilogram of hydrogen plus a 5 % purge allowance for quality control, and oxygen is vented without credit in the baseline scenario.


| Parameter                             | Value                                      |
| ------------------------------------- | ------------------------------------------ |
| Plant Capacity (kg/day)               | 10 000                                     |
| The cell operating temperature, T (K) | 333.15                                     |
| The cell operating pressure, P (bar)  | 1 (anode), 30 (cathode)                    |
| The maximum current density, (A/cm²)  | 2                                          |
| Exchange current density, (A/cm²)     | 2.618 x 10⁻⁶ (anode), 1.0e-1 (cathode)     |
| Limiting current density (A/cm²)      | 6                                          |
| The electrode thickness, (microns)    | 200                                        |
| The electrode porosity                | 0.3                                        |
| The membrane thickness, (microns)     | 114                                        |
| Active area, (cm²)                    | 877                                        |
| Cell voltage, V                       | 1.79                                       |
| Voltage efficiency, V                 | 0.69                                       |
| Cell Power rating, kW/cell            | 3.14                                       |
| Total power rating, kW                | 19,034                                     |
| Specific Energy consumption, kWh/kg   | 49                                         |
| Membrane type                         | PFSA, Nafion 117                           |
| Hydrogen purity                       | ≥99.999 vol %, ISO 14687-2 Fuel-Cell Grade |
| Capacity factor                       | 95 % (8322 h yr⁻¹)                         |



| **Parameter**                                 | **Baseline value**         | **Rationale / source**                                                                                                                                                                |
| --------------------------------------------- | -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Plant Capacity (kg/day)                       | 10 000                     | Mid-point between distributed and central cases                                                                                                                                       |
| Specific energy consumption (SEC), ( kWh /kg) | 54.27 kWh kg⁻¹ (HHV)       |                                                                                                                                                                                       |
| Stack operating Temperature                   | 60 °C                      |                                                                                                                                                                                       |
| Stack output presure, (bar)                   | 30 bar                     | Minimum pressure before long-distance compression                                                                                                                                     |
| Hydrogen purity                               | ≥99.999 vol %              | ISO 14687-2 Fuel-Cell Grade                                                                                                                                                           |
| Feed-water quality,                           | <0.5 µS cm⁻¹, 10 L kg⁻¹ H₂ |                                                                                                                                                                                       |
| Current density                               | 2 A/cm2                    |                                                                                                                                                                                       |
| Stack replacement interval                    | 10 years                   | 80 000 h durability target ([energy.gov](https://www.energy.gov/sites/default/files/2024-05/hfto-mypp-2024.pdf "Hydrogen and Fuel Cell Technologies Office Multi-Year Program Plan")) |
| Capacity factor                               | 95 % (8322 h yr⁻¹)         | Allows maintenance shutdowns yet reflects baseload duty                                                                                                                               |
| Product pressure for export                   | 30 bar                     |                                                                                                                                                                                       |

##### **4.2.1.4 Economic basis** 

Financial parameters include a weighted average cost of capital (WACC) of 10 %, consistent with comparable industrial projects . We define the minimum acceptable discount‐cash‐flow rate of return (DCFROR) at 10 % for profitability calculations. Utility costs incorporate electricity ($0.07/kWh), water treatment, routine maintenance, and membrane/catalyst replacements. Plant profitability is assessed via LCOH, net present value (NPV), and internal rate of return (IRR), with LCOH computed as the ratio of the present value of total lifecycle costs to cumulative hydrogen production over 20 years

The discounted-cash-flow model adopts a **minimum acceptable internal rate of return (DCFROR)** of **10 %** in real terms. Other financial parameters (all 2023 USD):
Stack replacement is scheduled every ten years at 15 % of the initial installed CAPEX to capture membrane and catalyst end-of-life refurbishments.

For the discounted-cash-flow analysis we adopt:

Weighted average cost of capital (WACC) 10 %**, representing a blended debt–equity structure for a first-of-a-kind industrial project in the U.S. market.
- **Corporate tax rate: 27 %** (federal plus representative state surcharge).
- **Depreciation:** three-year MACRS accelerated schedule for electrolysis equipment, consistent with current IRS guidance and H2A methodology.
- **Plant life:** 20 years with zero salvage value.
- **Electricity price:** baseline **0.07 USD kWh⁻¹**, varied parametrically in later sensitivity runs (0.03–0.15 USD kWh⁻¹).
- **Non-energy OPEX:** routine maintenance, consumables, and water treatment sum to 2.1 % of installed CAPEX per year; fixed and variable components are derated to 75 % and 50 % respectively during the startup year.

These inputs feed a standard discounted-cash-flow worksheet that reports levelized cost of hydrogen (LCOH), net present value (NPV), and internal rate of return (IRR). 


| **Economic variable**                   | **Value / assumption**                                     |
| --------------------------------------- | ---------------------------------------------------------- |
| Plant operating life, years             | 20                                                         |
| Weighted-average cost of capital (WACC) | 10 %                                                       |
| Corporate income-tax rate               | 27 %                                                       |
| Depreciation method                     | 20-year Modified Accelerated Cost Recovery System (MACRS). |
| Construction period                     | 3 years                                                    |
|                                         |                                                            |
| Electricity price (grid PPA) , $/ kWh   | 0.07                                                       |
| DI-water cost, $/kg                     | 0.002                                                      |
| Annual O&M (excluding electricity)      | 2 % of installed capital                                   |
| Salvage value                           | 0 % of EPC cost (conservative)                             |
| Uninstalled captal cost, $995/kW        | 995                                                        |
1. **Weighted Average Cost of Capital (WACC)**: 10%, reflecting a blended debt–equity structure typical of first-of-a-kind industrial projects in the U.S. market.

2. **Corporate Tax Rate**: Set at 27%, inclusive of both federal taxes and relevant state surcharges.

3. **Depreciation**: Adopting a three-year Modified Accelerated Cost Recovery System (MACRS) accelerated schedule for electrolysis equipment, in accordance with current IRS guidelines and H2A methodology.

4. **Plant Life**: Estimated at 20 years, with an assumption of zero salvage value at the end of the operational life.

5. **Electricity Pricing**: Establishing a baseline electricity cost of $0.07 per kWh, to be adjusted parametrically in subsequent sensitivity analyses, spanning a range from $0.03 to $0.15 per kWh.

6. **Non-Energy Operating Expenditures (OPEX)**: Anticipated to constitute approximately 2.1% of installed CAPEX annually, with an adjustment during the startup year where the fixed and variable components are reduced to 75% and 50%, respectively.





---



### 4.2.2 Process description
		Base case study.
Electrolyser operation
PEM System description


![[System bounday.png]]


![[image-45.png]]


**PEM System Description.**

Our base-case PEM electrolyzer plant, rated at 10 000 kg H₂ day⁻¹, follows the flow scheme depicted in Figure 2. Deionized water first enters an ion-exchange pretreatment loop and is pressurized by a high-performance feed pump. It is then preheated through a shell-and-tube heat exchanger to the stack operating temperature of 333 K before distribution to the anode halfcell of the membrane-electrode assembly (MEA). Within the stack, water molecules dissociate under a cell voltage that our validated electrochemical model predicts to be within ±20 mV of experimental Nafion 117 polarization curves at current densities between 0.5 and 2.0 A cm⁻²; Faradaic efficiency remains above 99 % and gas crossover stays below 1 %.

On the anode side, evolved oxygen and residual liquid collect in a gas–liquid separator; oxygen is vented through a control valve, while condensate returns to the water loop. At the cathode, hydrogen and entrained moisture pass first through a demister and condensate trap before entering a dual-tower desiccant dryer. The drying stage delivers hydrogen at 30 bar and > 99.97 % purity ready for distribution without further compression. A continuous bleed equivalent to 5 % of the inlet water flow prevents salt buildup and ensures membrane longevity.

The core electrochemical unit comprises 6186 identical cells connected in series, each featuring a 877 cm² active area. The MEA employs a Nafion 117 membrane with 178 micron thickness, sandwiched between platinum-catalyzed cathodes (0.4 mg cm⁻²) and iridium-oxide anodes (1.54 mg cm⁻²). Bipolar plates of titanium with gold-plated flow fields ensure low electrical resistance and corrosion resistance under acidic conditions. Flow-field channels are designed in an interdigitated pattern to optimize water distribution and gas removal, minimizing local flooding and Ohmic losses. Shunt currents are mitigated through insulated manifold designs, preserving cell-to-cell voltage uniformity.
 
Balance-of-plant components including recirculation pumps, power electronics, separators, and thermal management controls contribute an additional 5.3 kWh kg⁻¹ to the system-wide specific energy consumption (SEC) of 54.3 kWh kg⁻¹. The stack alone consumes 49 kWh kg⁻¹ for hydrogen generation, corresponding to a 68 % lower heating value (LHV) efficiency at 90 % capacity factor. Startup sequencing ramps production from 50 % to full capacity over the first year, during which O&M costs are scaled to 75 % of steady-state fixed charges and 50 % of variable charges to reflect commissioning activities.







### 4.2.3 Description of framework




For our framework
we combined our physics-based PEM electrolyzer model with system-level cost model fora PEM electrolyzer production plant,
system-level model uses the discounted cash flow formulation to calculate the present value of all costs associated with
The system analysis parameters and methodology are adopted form the department of Energy H2A lite model.  were performed using the H2A v3.2018 model.
the uninstalled cost is modified with curve fitted function to the capacity of the system. 
We design and confgure An RE system configuration supplies electricity , energy configuration wind , PV and Hybrid
energy configuration wind , PV and Hybrid
s


TEA
assumes construction in year 0, project start in year 1, a project lifetime of 20 years, a discount rate of 10%, and an annual inflation rate of 1.9%.
, which is a one-time investment incurred before the plant start-up
tack replacements  planned replacement cost is 15% of the direct capital incurred at a stack replacement interval, which is assumed to be 10 years
The annual fixed operating cost, ,
Direct fixed cost and 
indirect fixed cost
Tax and insuranc
FCI

were performed using the H2A v3.2018 model.

insp @chungDesignSpacePEM2024
different capacities, distributed and centralized


![[LCOH Framework.png]]


#### 4.2.3 Description of Framework

To deliver a holistic techno-economic evaluation, we developed an integrated modeling framework that couples our validated physics-based PEM electrolyzer model with a system-level discounted-cash-flow (DCF) cost module. As illustrated in <mark style="background: #FFB8EBA6;">Figure 3</mark>, key outputs from the electrolyzer design such specific energy consumption (SEC), stack efficiency, and hydrogen output and feed directly into the economic core, where capital and operating costs are annualized and discounted to present value.

Our cost module follows the U.S. Department of Energy’s H2A v3.2018 methodology, adopting its structured input–output architecture and default financial parameters. Uninstalled stack and balance-of-plant capital costs are modified to the system size using a curve-fitting function adopted from  Astraini et al. It assumes that both small, distributed units (1 500 kg day⁻¹) and large, centralized plants (50 000 kg day⁻¹) share a consistent installation cost basis. We then apply installation lang factors, contingency allowances, and non-depreciable land and permitting charges exactly as prescribed by H2A, but replace the default learning-curve parameters with our own empirically derived exponents to reflect recent manufacturing advances in PEM stacks.

On the operating side, the framework ingests an hourly electricity cost time-series from renewable energy (RE) configurations solar PV, wind, and hybrid PV–wind along with grid tariffs. Hourly RE generation profiles, obtained from National Renewable Energy Laboratory (NREL) data, are passed through a levelized cost of electricity (LCOE) subroutine to produce weighted average power prices under seasonal and diurnal variability. These dynamic power costs, together with fixed O&M, water treatment, and periodic stack replacement charges, drive the annual cash-flow streams.

We determine the levelized cost of hydrogen (LCOH) from the DCF model. Net present value (NPV) and internal rate of return (IRR) emerge naturally from the same cash-flow series.

By linking our physics-based SEC and capacity-factor outputs to a configurable RE supply model and a DCF model, this framework allows us to explore how design choices, cell area, catalyst loading, power electronics efficiency, and energy-supply scenarios jointly influence LCOH, NPV, and IRR. 
In the following sections, we employ this platform to interrogate scale effects (Section 4.5) and renewable integration strategies (Section 5.2), always retaining identical notation and boundary definitions so that comparisons remain apples-to-apples.


where is the weighted average cost of capital, the project life (20 years), and the annual hydrogen yield. 

## 4.3 Scope and indicators.

**4.2.1.1 System boundary** We model the complete **electrolyzer island**,that is, the stack plus all balance-of-plant (BoP) equipment required to deliver dry, 30 bar hydrogen. The boundary therefore includes DC power supplies/rectifiers, heat exchangers, DI-water treatment, gas-liquid separators, dryers, and a three-stage mechanical compressor. Everything downstream of 30 bar (long-distance compression, storage, trucking, purging) and upstream utility generation (renewables or grid) is excluded to keep the analysis focused on _production_ rather than delivery or dispensing. 

 4.3. 1 System boundary

goal ,scope , boundaries.
Surrounding: no compression, transportation
Define clear, transparent goals
• Time horizon
• Target audience
• Potential limitations in usability
• Product application
• Functional unit/reference flow, kg of Hydrogen
• Block flow diagram
• Benchmark product, blue and gray hydrogen
• Production capacity (scale)
• Location
• Feedstocks and other raw 
materials
• Products, byproducts and waste
• Systems boundaries
• Scenario analysis: eefect of scalling by production capacity, RE energy scenario


### 4.3.1 System Boundary


Figure 4.4’s block flow diagram illustrates the plant boundary:
To ensure clarity and reproducibility, the scope of our analysis is explicitly delimited by a well-defined system boundary that encompasses water treatment, electrolyzer operation, and gas-handling up to the point of dry, high-purity hydrogen at the plant fence. As illustrated in Figure 4.5, our boundary includes the renewable-or grid-supplied power management system, the PEM stack assembly, the associated water pretreatment train, and the hydrogen and oxygen gas management modules; it excludes downstream compression, transportation, and end-use facilities. By holding the scope fixed, we can transparently compare the techno-economic performance of “green” hydrogen against benchmark cases.(blue hydrogen produced via steam-methane reforming with carbon capture, and gray hydrogen without capture) on a common basis.
![[system boundary.png]]
The time horizon for all cash-flow and environmental indicators spans the 20-year design life of the plant, consistent with IRS MACRS depreciation schedules and H2A Lite conventions. Our analysis is tailored to project developers, policymakers, and industrial offtakers evaluating on-site or near-site hydrogen production options, and thus it focuses on capital and operating parameters most relevant to early-stage deployments. We acknowledge that excluding compression and transportation may understate total system costs for remote or bulk distribution scenarios; this limitation is addressed in our discussion of future work
The functional unit for comparison is one kilogram of hydrogen delivered at 30 bar and > 99.97 % purity. All mass and energy flows including feedstock water, electrical input, and by-product oxygen are normalized to this unit to facilitate benchmarking across scales and technologies. Production capacities of 1 500 kg day⁻¹ (distributed), 10 000 kg day⁻¹ (mid-scale), and 50 000 kg day⁻¹ (central) define three case studies used in our scenario analysis, which probes the impact of economies of scale and renewable-energy penetration on key metrics.

Geographically, we assume a temperate U.S. inland site with access to medium-voltage grid infrastructure and typical solar irradiance and wind-speed profiles. Feedstock electricity is modeled under three configurations: grid only, solar-PV only, and a 50:50 PV–wind hybrid, using hourly resource data to capture seasonal and diurnal variability. Water is assumed to meet ultrapure standards after on-site treatment of municipal supply, and purge streams are neutralized within the plant. Waste streams (oxygen vent gas and spent ion-exchange regenerant) are managed per local environmental regulations but are not credited economically.

### 4.3.2 Metrices 

#### 4.3.2.1 System efficiency

`The fundamental indicator of electrolyzer performance is the **mass of hydrogen produced** per unit time and per operating condition. For a specific operational mode indexed by hour $h$ and year $y$, the hourly hydrogen production is expressed as: @astrianiOptimalPlanningRenewable2024
`$$m_{H_2,h,y} = \frac{\eta_{El,h} P_{EL,h}}{HHV_{H_2} \ } \quad(56)$$
`

LHV-based efficiency and HHV-based efficiency.
To characterize how effectively the PEM electrolyzer converts input electrical power into chemical energy stored in hydrogen, we define the system efficiency bases on the Lower Heating Value (LHV) and Higher Heating Value (HHV) basis as @kimTechnoeconomicAnalysisAnion2024$$
\eta_{LHV} = \frac{m_{H_2} \cdot LHV_{H_2}}{E_{PEM el } + E_{BoP}} \quad(56)
$$

$$
\eta_{HHV} = \frac{m_{H_2} \cdot HHV_{H_2}}{E_{PEM el} + E_{BoP}} \quad(57)
$$
where $E_{\text{el},h,y}$ ​  is the net electrical power inputs to the stack $E_{PEMel}$ and BoP units $E_{BoP}$ .  $LHV_{H_2}$ is the lower heating value of hydrogen, which excludes the latent heat of vaporization of product water, while $HHV_{H_2}$   includes the total energy released during combustion @kimTechnoeconomicAnalysisAnion2024 . The $LHV_{H_2}$ and $HHV_{H_2}$  are 33.32 kWh/kg   39.44 kWh/kg respectively @bessarabovPEMElectrolysisHydrogen2016 .   They represent the net usable energy at the application. 

At standard operation (60–80 °C, ambient pressure), commercial PEM electrolyzers achieve 65–70% HHV efficiency, with state-of-the-art systems approaching 80% with waste heat recovery integration @carmoComprehensiveReviewPEM2013 . Generally, **LHV-based efficiency** is more appropriate for fuel cell applications (net power use), whereas **HHV-based efficiency** is used in **electrolyzer evaluations**, especially under policy or grid-integration scenarios where the energy source includes renewable generation with seasonal storage requirements @staffellRoleHydrogenFuel2019 .
An inverse metric of energy efficiency , **Specific Energy Consumption** ($SEC_{H_2}$), defined as the amount of electrical energy required to produce one kilogram of hydrogen.
specific energy consumption for total hydrogen production is given as

$$
SEC_{Total} = \frac{E_{PEMel} + E_{BoP}}{m_{H_2}} \quad(58)
$$

<mark style="background: #FFB86CA6;">inspo</mark>: @kimTechnoeconomicAnalysisAnion2024
More details on the W_bop are given in the appendix section.
Throughout this study, we report system-wide SEC including balance-of-plant loads to facilitate  comparisons across scales and energy-supply scenarios. 



`
`4.3.2.2 System-Level Economic Metrics 

`Metrics: Levelized cost of hydrogen(LCOH), NPV, IRR, LCOE

`To comprehensively evaluate the economic feasibility and financial performance of PEM electrolysis integrated with renewable or grid electricity supply, several metrics are computed.

`The Levelized Cost of Hydrogen (LCOH)  is used to quantify the cost of producing one kilogram of hydrogen over the entire project lifetime. It accounts for capital recovery, operations and maintenance, and energy input costs. It is given by:

$$
\text{LCOH} = \frac{\text{CAPEX} + \sum_{t=1}^{N} \frac{\text{OPEX}}{(1+r)^t}}{\sum_{t=1}^{N} \frac{P_{H_2}}{(1+r)^t}} \quad(60)
$$


@kimTechnoeconomicAnalysisAnion2024

`t is a specific year of the lifetime, 𝑁 is the lifetime of the process, and r is the discount rate. P𝐻2 denotes the annual hydrogen production.

`**Net Present Value (NPV):** The NPV represents the present value of the project’s net cash flows over its lifetime, discounted at the weighted average cost of capital (WACC):
$$\mathrm{NPV} = \sum_{t=0}^{n} \frac{R_t - C_t}{(1 + r)^t} \tag{61}$$

where $R_t$ and $C_t$ are revenues and costs at year ,t and is the project lifetime.

`**Internal Rate of Return (IRR):** The IRR is the discount rate at which the NPV becomes zero. It is an indicator of the project's profitability and is found by solving:
$$0 = \sum_{t=0}^{n} \frac{R_t - C_t}{(1 + \mathrm{IRR})^t} \tag{62}$$

`IRR exceeding the WACC implies a financially attractive project.




---


#### 4.3.2.2 System-Level Economic Metrics

To assess the financial viability of PEM electrolysis under varying energy-supply scenarios, we compute four principal economic indicators, levelized cost of hydrogen (LCOH), net present value (NPV), internal rate of return (IRR), and levelized cost of electricity (LCOE). Each captures a distinct facet of project performance over the plant’s 20-year lifetime.

**Levelized Cost of Hydrogen (LCOH).** 
The LCOH represents the average cost per kilogram of hydrogen produced, taking into account capital recovery, operation and maintenance, and energy expenses, all discounted to present value. Formally @kimTechnoeconomicAnalysisAnion2024

$$
\text{LCOH} = \frac{\sum_{t=0}^{N} \frac{C_{\text{cap},t} + C_{\text{om},t}  }{(1 + r)^t}}{\sum_{t=0}^{N} \frac{M_{\text{H}_2,t}}{(1 + r)^t}} \tag{60}
$$

where $C_{\text{cap},t}$, and $C_{\text{om},t}$, are the capital-related, O&M, and electricity costs incurred in year $t$, respectively. $M_{\text{H}_2,t}$ is the mass of hydrogen produced in year $t$; $r$ is the weighted average cost of capital; and $N$ is the plant life (20 years).


**Net Present Value (NPV).** 
The NPV measures the present‐value surplus (or deficit) of cash flows over the project’s lifetime, providing a direct indicator of value creation. It is given by
$$\mathrm{NPV} = \sum_{t=0}^{n} \frac{R_t - C_t}{(1 + r)^t} \tag{61}$$
where $R_t$ and $C_t$ are revenues and costs at year ,t and is the project lifetime.
**Internal Rate of Return (IRR).** The IRR is defined as the discount rate ρ\rhoρ that brings the NPV to zero. A higher IRR indicates greater project profitability relative to the WACC benchmark.

$$0 = \sum_{t=0}^{n} \frac{R_t - C_t}{(1 + \mathrm{IRR})^t} \tag{62}$$
**Levelized Cost of Electricity (LCOE).** 
For the renewable energy supply system (solar, wind, or hybrid), the LCOE is computed to assess the cost per unit of electricity generated
$$\mathrm{LCOE} = \frac{\mathrm{CRF} \cdot C_{RE} + O_{RE}}{E_{annual}} \tag{63}$$

where $C_{RE}$ is the capital cost of the renewable energy plant,  $O_{RE}$  is the annual operating cost, and $E_{annual}$ is the annual electricity production. LCOE values are benchmarked against grid electricity tariffs or PPA prices to determine economic competitiveness
Where  Capital recovery factor (CRF) is  
  $$
  \text{CRF} = \frac{r(1+r)^n}{(1+r)^n - 1} \tag{64}
  $$
  at discount rate (r), of 0.12,  system lifetime (n) of 25 years.



## 4.4 Cost modeling unit and data 

 ### **4.4.1** Capital cost breakdown 
 
#### **4.4.1.1 PEM System Cost**
The total uninstalled capital cost (CapEx) of the PEM hydrogen production system is consist of the electrolyzer stack and the balance-of-plant (BoP). Following Astriani et al.'s parametric fitting of global cost data, the uninstalled stack cost, $Cost_{EL}$, is expressed as an exponential-linear function of the rated electrical capacity of the electrolyzer, $P_{EL,rated}$ (in kW):
 @astrianiOptimalPlanningRenewable2024 .
$$
\text{Cost}_{EL} = k_1 + k_2 P_{EL,\text{rated}} + k_3 \, e^{k_4 \, P_{EL,\text{rated}}} \tag{65}
$$
The constants k1, k2, k3, and k4 are given as 1046.93, -3.48, 2061.57, and -0.26. The fitted constants represent baseline costs, linear scaling factors, and exponential scaling effects. The cost of the PEM electrolyzer system scales rapidly and diminishes with economies of scale for large capacities.  
The total uninstalled cost includes the balance-of-plant (BoP) components such as gas-liquid separators, compressors, pumps, thermal management systems, and water purification units.  
The power management system (PMS) constitutes another significant capital investment, involving equipment such as rectifiers and transformers. These components are essential for converting grid-supplied or renewable alternating current (AC) into the direct current (DC) required by the PEM electrolyzer stack. Given the dynamic operating conditions associated with renewable energy integration, PMS configurations must be robust and capable of handling substantial fluctuations in voltage and current, thereby ensuring continuous and reliable electrolyzer operation.  
The Uninstalled cost is then multiplied by a set of "Hand factors" or derived multipliers that convert equipment costs into installed costs. These multipliers account for auxiliary materials, assembly, project engineering, civil work, overheads, supervision, freight, and contingencies.

![[Uninstall cost of PEM electrolyser.png|455x273]]
@astrianiOptimalPlanningRenewable2024



#### **4.4.1.2 RE system cost**
To account for variable energy supply scenarios, a separate modeling layer is introduced for renewable electricity provision. The RE system includes solar photovoltaic (PV) and onshore wind power as independent and hybrid supply configurations. For each renewable source, the capital cost $(C_{RE})$ and operating cost $O_{RE})$ are modeled as functions of installed capacity  $P$ and scale index $s$ for price corrections were adopts the 6/10 rule :
$$C_{RE} = C_{ref} \cdot \left(\frac{P}{P_{ref}}\right)^{-s}; \quad O_{RE} = O_{ref} \cdot P \tag{66}$$

The cost of solar PV and wind systems is based on a 1 MW reference scaled to a 20 MW project scale and includes an 8% land procurement cost @khanDesigningOptimalIntegrated  .We assume the purchase cost includes the cost of installation. Hybrid power systems that combine solar and wind in a 1:1 capacity ratio were modeled with proportional capital cost contributions and aggregate operational costs. These values serve as input parameters for alternative electrolyzer configurations that rely on an off-grid renewable supply.

All RE investment costs are consolidated into the Levelized Cost of Energy (LCOE) for the hydrogen production system. LCOE for solar, wind, or hybrid configuration is computed to assess the cost per unit of electricity generated
$$\mathrm{LCOE} = \frac{\mathrm{CRF} \cdot C_{RE} + O_{RE}}{E_{annual}}$$

where $C_{RE}$ is the capital cost of the renewable energy plant,  $O_{RE}$  is the annual operating cost, and $E_{annual}$ is the annual electricity production. LCOE values are benchmarked against grid electricity tariffs or PPA prices to determine economic competitiveness
Capital recovery factor (**CRF**) :  
  $$
  \text{CRF} = \frac{r(1+r)^n}{(1+r)^n - 1}
  $$
  where \( r \) = discount rate, \( n \) = system lifetime


 All RE investment costs are consolidated into Levelized Cost of Energy (LCOE) for the hydrogen production system. LCOE for solar, wind, or hybrid configuration is computed to assess the cost per unit of electricity generated





### 4.4.2 Operational Expenditure Components

The total OPEX is categorized into fixed and variable components, each representing distinct drivers of annual expenditures. Table 3.2 offers a concise summary of the assumptions used to estimate these costs. The fixed costs comprise direct fixed labor and indirect fixed overheads. For labor, we assume a wage rate of $31.29 per person-hour and staff the plant to ensure that total maintenance labor averages 1,500 man-hours per year. Maintenance should be distributed across routine inspections and corrective repairs. Indirect fixed costs include an annual budget of $50,000 for licensing and permitting, property taxes, and insurance assessed at 1.5% of total installed CAPEX (approximately $1.7 million per year), along with facility rent of $75,000 per year. Together, these direct and indirect fixed charges account for nearly 4% of installed capital each year, providing a stable base load of overhead against which variable costs are measured. These assumptions are all consistent with NREL's 2019 H2A and H2AFAST tools for distributed systems @penevTechnoEconomicModellingH2A

Variable OPEX is driven by feedstocks, utilities, and consumables that scale directly with hydrogen production. Electricity represents the single largest line item; for grid-connected cases, it is simply the product of SEC and the contracted price. For off-grid cases, we substitute the time-series LCOE developed in Section 4.3.2.2. Water costs encompass three distinct streams: demineralized process water at $0.002 per liter, cooling-loop water at $0.0005 per liter, and a small purge stream treated and discharged at $0.10 per kilogram of spent regenerant. Oxygen vented to the atmosphere carries no economic credit in our baseline but incurs compression power in the event of on-site utilization, which we capture as a variable BoP load. Finally, periodic stack replacements are scheduled every ten years at 15% of initial CAPEX, entered into the cash-flow model as a lump-sum variable cost in years ten and twenty.





## **4.5 Parametric Sensitivity and Uncertainty Analysis**
Building on the detailed techno‐economic framework, we subject key model inputs to both deterministic and probabilistic interrogation to ascertain which parameters most strongly influence project economics and to quantify the inherent uncertainty in our LCOH, NPV, and IRR estimates.
The basis and ranges for the sensitivity analysis are given in <mark style="background: #FFB86CA6;">Tablex</mark>

- **4.5.1** Univariate sensitivity (tornado diagrams) on key input parameters

In the univariate sensitivity analysis, each input parameter is varied independently between a low and high bounds while all other assumptions remain fixed at the base value. Each bound represent a scenario reflecting plausible near‐term or DOE's technical target for under the Hydrogen earth-shot values  at their base case. @HydrogenShot  <mark style="background: #FFB86CA6;">Figure 4.7</mark> presents tornado diagrams  based on parameter variation and effect on LCOH and NPV. The plot illustrates Total Energy Feedstock Cost \$/kWh ,Uninstalled capital cost \$/kW , Specific energy efficiency, kWh/kg H2 kW/kg , Tax rate %, , Total Fixed Operating Costs,  \$/yr , Total Utility Costs \$/year) , Total Non Energy Feedstock $/year, co-product O2 selling price, $/kg O2.   (Table #, Figure # and Figure #)
A scenario comparison between a centralized and a distributed system is compared to the base line on NPV and IRR.

- **4.5.2** Multivariate to capture parameter interactions
    Contour
We complemented the univariate study with multivariate and Monte Carlo simulations to capture parameter interactions and probabilistic risk. In a two-dimensional contour analysis, we jointly vary electricity costs and capital expenditures across their respective ranges to generate LCOH contour plots. The contour plots demonstrate the trends and the dominating parameters related to the metrics being assessed (Figure 4).

For the Monte Carlo simulation, we incorporated parameter distributions to provide probabilistic LCOH outcomes across diverse deployment scenarios. This simulation specifically integrated the variability of the energy system design parameters, considering its impact on the effective capacity factor and the resulting hydrogen production. Nine inputs parameters (Tax rate, Discount rate, Fixed Capital Investment, Fixed Operational cost, Design capacity, Non energy feedstock cost, Working Capital and, Utility) were stochastically and simultaneously varied between their low and high ranges. A cumulative distribution functions for LCOH and NPV, enables an effective evaluation on risk profiles associated with electrolyser investments under varying market conditions and energy supply characteristics.




    Monte Carlo
Monte Carlo simulation incorporating parameter distributions provides probabilistic LCOH outcomes across diverse deployment scenarios. By generating cumulative distribution functions for LCOH, and NPV decision-makers can evaluate risk profiles associated with electrolyser investments under varying market conditions
Beyond pairwise interactions, we implement a 5 000‐iteration Monte Carlo simulation in which all nine critical inputs (Tax rate, Discount rate, Fixed Capital Investment, Fixed Operational cost, Design capacity, Non energy feedstock cost, Working Capital and, Utility) were stochastically and simultaneously varied between their low and high ranges. Each vairable follow either normal, uniform, triangular or probability distributions defined by values as indicated in <mark style="background: #FFB86CA6;">Appendix</mark>
(Table #, Figure # and Figure #)



Energy cost
Tax rate, Discount rate, Fixed Capital Investment, Fixed Operational cost, Design capacity, Non energy feedstock cost, Working Capital and, Utility


Total Energy Feedstock Cost \$/kWh ,Uninstalled capital cost \$/kW , Specfic energy efficiency, kWh/kg H2 kW/kg , Tax rate %, , Total Fixed Operating Costs,  \$/yr , Total Utility Costs \$/year) , Total Non Energy Feedstock $/year, co-product O2 selling price, $/kg O2. 



To add
**Economic Parameters**

**Technical Parameters**:
Two critical assumptions were not varied: the operation period of 20 years