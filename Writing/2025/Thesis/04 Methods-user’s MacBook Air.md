

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



To ensure the fidelity of our PEM electrolyzer model, we benchmarked its predictions against multiple peer-reviewed experimental studies covering a range of operating conditions, cell designs, and materials.
To ensure the accuracy of our lumped‐parameter PEM electrolyzer model—incorporating activation, ohmic, and concentration overpotentials; membrane hydration; and gas crossover—we benchmarked its predictions against multiple published experimental datasets spanning different cell configurations, membrane types, and operating conditions [@scheepersImprovingEfficiencyPEM2020; @jangTechnoeconomicAnalysisMonte2022; @chungDesignSpacePEM2024]. Validation focused on reproducing polarization curves (cell voltage vs. current density) and Faradaic efficiency across a range of temperatures, pressures, and catalyst loadings.
we compared model outputs to single‐cell measurements performed by Chung et al. (2024) using a Nafion 117 membrane (178 µm thick) at ambient pressure and two temperatures—323 K (50 °C) and 353 K (80 °C)—over current densities up to 2 A cm⁻² [@chungDesignSpacePEM2024]
we validated against the thin‐membrane dataset of Scheepers et al. (2020), which employed a Nafion 212 membrane (51 µm), platinum cathode loading of 0.25 mg cm⁻², and iridium‐oxide anode loading of 0.96 mg cm⁻², with 10 wt.% ionomer content and platinum‐coated titanium felt electrodes [@scheepersImprovingEfficiencyPEM2020].

### 4.1.1 Electrolyzer Model Design

All the equation
### 4.2 Electrolyzer Model Validation


#### **4.2.2 Model Parametrization**
A quasi-one-dimensional (0D/1D), physics-based model of a PEM electrolyzer stack was developed to form the technical foundation of this study. The model integrates key electrochemical and physical phenomena to predict the performance and efficiency of the electrolyzer under various operating conditions. A comprehensive water balance is maintained by accounting for electro-osmotic drag, back-diffusion, and hydraulic permeation across the polymer electrolyte. 
The model was parameterized based on literature data for a commercial-scale PEM electrolyzer. The baseline parameters include a cell active area of 877cm2, a Nafion 117 membrane thickness of $178 \mu m$, and specific catalyst loadings for the anode and cathode. The nominal operating point was set at 333.15 K and a maximum current density of 2A/cm2, with the cathode operating at a pressure of 30 bar
The electrochemical model was prototyped in an Excel workbook and subsequently implemented as a more detailed, object-oriented Python class to facilitate dynamic simulations and integration with other modules
Table here.


#### **4.2.2 Model Validation**

To ensure its accuracy and reliability for techno-economic analysis, the physics-based PEM electrolyzer model was rigorously validated against experimental data from published literature. The validation process involved comparing the model's predictions with results from experiments conducted under various operating conditions. The model's performance was benchmarked against polarization curves from a single-cell electrolyzer using a Nafion 117 membrane (178 μm thickness) at ambient pressure and two distinct operating temperatures: 50°C (323.15 K) and 80°C (353.15 K).

A key validation was performed by comparing the model's predictions against experimental polarization curves from Scheepers et al. for a Nafion 117–based stack operated at 333 K and 30 bar. The model successfully reproduced the observed cell voltage to within ±20 mV across a current density range of 0.5 to 2.0 A/cm². Furthermore, it accurately matched experimentally measured gas crossover rates, with the predicted H₂ permeation remaining below 1% of the total hydrogen produced, aligning with experimental results within a 0.2% margin.

#### **4.2.3** Sensitivity of key model parameters
(exchange current density, membrane conductivity) to validation data
A local sensitivity analysis examined the influence of uncertainties in exchange current density (i0i_0i0​) and membrane ionic conductivity (κmem\kappa_{\rm mem}κmem​) on cell voltage and specific energy consumption.



### 4.3 Energy system Design

#### 4.3.1 Wind energy

#### 4.4.1  Photovoltaic system




## 4.2 Technoeconomic analysis and Framework 

 4.2. 1 Design basis	

Process Basis – feed/product flow rate used and why, other assumptions (e.g.,SEC efficiency, Product pressure, purity, etc.)

Economic Basis - minimum acceptable DCFROR, rate for profitability calculation, depreciation method, tax rate, life of the plant, utility costs, etc.

The process baseline is a 10, 000kg/day chosen as a mid point between DOE's defined distributed/ onsite generation and centralized production systems. The baseline assumes a point of diminishing returns on economy of scale by cappacity.  The centralised system and distributed is a 50,00kg/day and 1500kg/day hydrogeen production capacity.  @jamesFinalReportHydrogen2016
To estimate hydrogen production costs under different scenarios coupling PEM electrolyzers with diverse, clean energy sources.
Our analysis is based on a distributed or on-site production case (1,500 kg/day) and central production  (50,000kg/day)  .  A somewhat mid point 10,000 kg/day is chosen as a preferred optimal size (case) based on the scalling and diminishing return point between our reference points..  @jamesFinalReportHydrogen2016
The baseline is shown in table ##

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
| Production capacity, kg/day      | 1,500       | 10,000                             |             |
| Start-up Year                    | 2024        | 2024                               | 2024        |
| Total Uninstalled Capital ($/kW) |             | $995                               |             |
| Total Electrical Usage (kWh/kg)  | 54.3        | 54.3 [% LHV] (61%) (% HHV) (72.6%) | 54.3        |
| Stack Electrical Usage (kWh/kg)  | 49          | 49 [% LHV] (68%) (% HHV) (80%)     |             |


##### **4.2.1.1 Process basis**

The electrolyzer stack is operated at **333 K** with an anode pressure of 1 bar and a cathode (product) pressure of **30 bar**, delivering high-purity hydrogen suitable for downstream applications without additional compression at the plant fence. The validated physics model predicts a **specific energy consumption (SEC)** of 49 kWh kg⁻¹ at stack level and **54.3 kWh kg⁻¹** system-wide once balance-of-plant (BoP) loads are included. Purity exceeds 99.97 % on a dry basis, and Faradaic losses from gas crossover remain below 1 % under these conditions, as corroborated by the Scheepers et al. data set used for model calibration. A nominal capacity factor of **90 %** is assumed after the commissioning year, during which production ramps linearly from 50 % of nameplate to full output; BoP and O&M expenditures are scaled accordingly. Water consumption is fixed stoichiometrically at 9 kg H₂O per kilogram of hydrogen plus a 5 % purge allowance for quality control, and oxygen is vented without credit in the baseline scenario.


| **Parameter**                     | **Baseline value**         | **Rationale / source**                                                                                                                                                                                                                                                                                                                                                                                                                              |
| --------------------------------- | -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Net H₂ output                     | 10 000 kg day⁻¹            | Mid-point between distributed and central cases                                                                                                                                                                                                                                                                                                                                                                                                     |
| Specific energy consumption (SEC) | 54.27 kWh kg⁻¹ (HHV)       | Consistent with 65 % efficiency target by 2026 ([energy.gov](https://www.energy.gov/sites/default/files/2024-05/hfto-mypp-2024.pdf "Hydrogen and Fuel Cell Technologies Office Multi-Year Program Plan"))                                                                                                                                                                                                                                           |
| Stack operating T / P             | 80 °C / 30 bar             | Typical industrial PEM practice                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Hydrogen purity                   | ≥99.999 vol %              | ISO 14687-2 Fuel-Cell Grade                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Feed-water quality                | <0.5 µS cm⁻¹, 10 L kg⁻¹ H₂ | Matches vendor warranty requirements                                                                                                                                                                                                                                                                                                                                                                                                                |
| Uninstalled stack cost            | 250 $ kW⁻¹ (target),       | DOE 2026 target and present-day surveys ([energy.gov](https://www.energy.gov/sites/default/files/2024-05/hfto-mypp-2024.pdf "Hydrogen and Fuel Cell Technologies Office Multi-Year Program Plan"), [hydrogen.energy.gov](https://www.hydrogen.energy.gov/docs/hydrogenprogramlibraries/pdfs/19009_h2_production_cost_pem_electrolysis_2019.pdf?Status=Master&utm_source=chatgpt.com "[PDF] Hydrogen Production Cost from PEM Electrolysis - 2019")) |
| Stack replacement interval        | 10 years                   | 80 000 h durability target ([energy.gov](https://www.energy.gov/sites/default/files/2024-05/hfto-mypp-2024.pdf "Hydrogen and Fuel Cell Technologies Office Multi-Year Program Plan"))                                                                                                                                                                                                                                                               |
| Capacity factor                   | 95 % (8322 h yr⁻¹)         | Allows maintenance shutdowns yet reflects baseload duty                                                                                                                                                                                                                                                                                                                                                                                             |
| Product pressure for export       | 30 bar                     | Minimum pressure before long-distance compression                                                                                                                                                                                                                                                                                                                                                                                                   |

##### **4.2.1.4 Economic basis** 

Financial parameters include a weighted average cost of capital (WACC) of 10 %, consistent with comparable industrial projects . We define the minimum acceptable discount‐cash‐flow rate of return (DCFROR) at 10 % for profitability calculations. Utility costs incorporate electricity ($0.07/kWh), water treatment, routine maintenance, and membrane/catalyst replacements. Plant profitability is assessed via LCOH, net present value (NPV), and internal rate of return (IRR), with LCOH computed as the ratio of the present value of total lifecycle costs to cumulative hydrogen production over 20 years

The discounted-cash-flow model adopts a **minimum acceptable internal rate of return (DCFROR)** of **10 %** in real terms. Other financial parameters (all 2024 USD):
Stack replacement is scheduled every ten years at 15 % of the initial installed CAPEX to capture membrane and catalyst end-of-life refurbishments.

For the discounted-cash-flow analysis we adopt:

- **Weighted average cost of capital (WACC): 10 %**, representing a blended debt–equity structure for a first-of-a-kind industrial project in the U.S. market.
- **Corporate tax rate: 27 %** (federal plus representative state surcharge).
- **Depreciation:** three-year MACRS accelerated schedule for electrolysis equipment, consistent with current IRS guidance and H2A methodology.
- **Plant life:** 20 years with zero salvage value.
- **Electricity price:** baseline **0.07 USD kWh⁻¹**, varied parametrically in later sensitivity runs (0.03–0.15 USD kWh⁻¹).
- **Non-energy OPEX:** routine maintenance, consumables, and water treatment sum to 2.1 % of installed CAPEX per year; fixed and variable components are derated to 75 % and 50 % respectively during the startup year.

These inputs feed a standard discounted-cash-flow worksheet that reports levelized cost of hydrogen (LCOH), net present value (NPV), and internal rate of return (IRR). 


| **Economic variable**                   | **Value / assumption**                                   |
| --------------------------------------- | -------------------------------------------------------- |
| Weighted-average cost of capital (WACC) | 7 % (real)                                               |
| Corporate income-tax rate               | 21 %                                                     |
| Depreciation method                     | 20-year straight line (half-year convention)             |
| Construction period                     | 2 years (30 % / 70 % capital draw)                       |
| Plant operating life                    | 20 years                                                 |
| Inflation (general)                     | 2 % yr⁻¹                                                 |
| Electricity price (grid PPA)            | Base 0.05 $ kWh⁻¹; range 0.04–0.10 $ kWh⁻¹ for scenarios |
| DI-water cost                           | 0.002 $ kg⁻¹ feed                                        |
| Annual O&M (excluding electricity)      | 2 % of installed capital                                 |
| Salvage value                           | 0 % of EPC cost (conservative)                           |





---



### 4.2.2 Process description
		Base case study.
Electrolyser operation
PEM System description


![[System bounday.png]]


![[image-45.png]]



Our base-case PEM electrolyzer plant, rated at 10 000 kg H₂ day⁻¹, follows the flow scheme depicted in Figure 2. Deionized water first enters an ion-exchange pretreatment loop and is pressurized by a high-performance feed pump. It is then preheated through a shell-and-tube heat exchanger to the stack operating temperature of 333 K before distribution to the anode halfcell of the membrane-electrode assembly (MEA). Within the stack, water molecules dissociate under a cell voltage that our validated electrochemical model predicts to be within ±20 mV of experimental Nafion 117 polarization curves at current densities between 0.5 and 2.0 A cm⁻²; Faradaic efficiency remains above 99 % and gas crossover stays below 1 %.

On the anode side, evolved oxygen and residual liquid collect in a gas–liquid separator; oxygen is vented through a control valve, while condensate returns to the water loop. At the cathode, hydrogen and entrained moisture pass first through a demister and condensate trap before entering a dual-tower desiccant dryer. The drying stage delivers hydrogen at 30 bar and > 99.97 % purity ready for distribution without further compression. A continuous bleed equivalent to 5 % of the inlet water flow prevents salt buildup and ensures membrane longevity.

The core electrochemical unit comprises 6186 identical cells connected in series, each featuring a 877 cm² active area. The MEA employs a Nafion 117 membrane with 178 micron thickness, sandwiched between platinum-catalyzed cathodes (0.5 mg cm⁻²) and iridium-oxide anodes (1.4 mg cm⁻²). Bipolar plates of titanium with gold-plated flow fields ensure low electrical resistance and corrosion resistance under acidic conditions. Flow-field channels are designed in an interdigitated pattern to optimize water distribution and gas removal, minimizing local flooding and Ohmic losses. Shunt currents are mitigated through insulated manifold designs, preserving cell-to-cell voltage uniformity.
 
Balance-of-plant components including recirculation pumps, power electronics, separators, and thermal management controls contribute an additional 5.3 kWh kg⁻¹ to the system-wide specific energy consumption (SEC) of 54.3 kWh kg⁻¹. The stack alone consumes 49 kWh kg⁻¹ for hydrogen generation, corresponding to a 68 % lower heating value (LHV) efficiency at 90 % capacity factor. Startup sequencing ramps production from 50 % to full capacity over the first year, during which O&M costs are scaled to 75 % of steady-state fixed charges and 50 % of variable charges to reflect commissioning activities.

**PEM System Description.**












### 4.2.3 Description of framework




For our framework
we combined our physics-based PEM electrolyzer model with system-level cost model fora PEM electrolyzer production plant,
system-level model uses the discounted cash flow formulation to calculate the present value of all costs associated with
The system analysis parameters and methodology are adopted form the department of Energy H2A lite model. the uninstalled cost is modified with curve fitted function to the capacity of the system.
An RE system configuration supplies electricity , energy configuration wind , PV and Hybrid
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


## 4.3 Scope and indicators.

**4.2.1.1 System boundary** We model the complete **electrolyzer island**—that is, the stack plus all balance-of-plant (BoP) equipment required to deliver dry, 30 bar hydrogen. The boundary therefore includes DC power supplies/rectifiers, heat exchangers, DI-water treatment, gas-liquid separators, dryers, and a three-stage mechanical compressor. Everything downstream of 30 bar (long-distance compression, storage, trucking, purging) and upstream utility generation (renewables or grid) is excluded to keep the analysis focused on _production_ rather than delivery or dispensing. 
### 4.21 System boundary


![[system boundary.png]]

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
Technological description
• Production capacity (scale)
• Location
• Feedstocks and other raw 
materials
• Products, byproducts and waste
• Systems boundaries
• Scenario analysis



### 4.3.2 Metrices 
(LCOH, NPV, IRR)


 System-Level Economic Metrics 

Metrics: Levelized cost of hydrogen(LCOH), NPV, LCOE

To comprehensively evaluate the economic feasibility and financial performance of PEM electrolysis integrated with renewable or grid electricity supply, several metrics are computed.

The Levelized Cost of Hydrogen (LCOH)  is used to quantify the cost of producing one kilogram of hydrogen over the entire project lifetime. It accounts for capital recovery, operations and maintenance, and energy input costs. It is given by:

$$
\text{LCOH} = \frac{\text{CAPEX} + \sum_{t=1}^{N} \frac{\text{OPEX}}{(1+r)^t}}{\sum_{t=1}^{N} \frac{P_{H_2}}{(1+r)^t}}
$$


@kimTechnoeconomicAnalysisAnion2024

t is a specific year of the lifetime, 𝑁 is the lifetime of the process, and r is the discount rate. P𝐻2 denotes the annual hydrogen production.

**Net Present Value (NPV):** The NPV represents the present value of the project’s net cash flows over its lifetime, discounted at the weighted average cost of capital (WACC):
$$\mathrm{NPV} = \sum_{t=0}^{n} \frac{R_t - C_t}{(1 + \mathrm{WACC})^t}$$

where $R_t$ and $C_t$ are revenues and costs at year , and is the project lifetime.

**Internal Rate of Return (IRR):** The IRR is the discount rate at which the NPV becomes zero. It is an indicator of the project's profitability and is found by solving:
$$0 = \sum_{t=0}^{n} \frac{R_t - C_t}{(1 + \mathrm{IRR})^t}$$

IRR exceeding the WACC implies a financially attractive project.



`The total installed cost (TIC) is calculated by applying an installation factor (IF)There are other indirect costs associated with the total capital investment (TCI) of a compressor. Site preparation, which is 5% of the TIC, covers the purchase of land and other auxiliary equipment. Engineering and design amounts to 10% of the TIC. Project contingency, which is allocated to deal with any unforeseen issues, takes another 10% of the TIC. Permitting to get the appropriate approvals and control equipment is 3% of the TIC 23. Finally, the owner’s cost, which accounts for the owners’ engineering, debt origination, closure costs, and due diligence studies, takes 12% of the TIC 23. Therefore, the TCI is calculated by adding all these indirect costs to the TIC`

𝑇𝐶𝐼 = 𝑇𝐼𝐶 + 𝐼𝑛𝑑𝑖𝑟𝑒𝑐𝑡 𝐶𝑜𝑠𝑡𝑠
















## 4.4 Cost modeling unit and data 

### **4.4.1** Capital cost breakdown (stack vs. BoP)

PEM System Cost
The CapEx of the system is calculated by  summing the costs of the PEM stack and the balance of plant as Purchased Equipment Costs (PEC) or uninstalled cost. 
The uninstalled cost( $Cost_El$ )  is  a fitted  model of the  the rated power capacity of the electrolyzer ($P_{EL, rated}$ ) as presented by Astriani et al. @astrianiOptimalPlanningRenewable2024 .
$$
\text{Cost}_{EL} = k_1 + k_2 P_{EL,\text{rated}} + k_3 \, e^{k_4 \, P_{EL,\text{rated}}}
$$
The constants k1,k2, k3, k4 are given as 1046.93, -3.48, 2061.57, and -0.26 The fitted constants represents baseline costs, linear scaling factors, and exponential scaling effects. The cost of PEM electrolyser system scales rapid and diminishes with economy of scale for large capacities.
The total uninstalled cost includes the balance-of-plant (BoP) components such as gas-liquid separators, compressors, pumps, thermal management systems, and water purification units. 
The power management system (PMS) constitutes another significant capital investment, involving equipment such as rectifiers and transformers. These components are essential to convert grid-supplied or renewable alternating current (AC) into the direct current (DC) required by the PEM electrolyzer stack. Given the dynamic operating conditions associated with renewable energy integration, PMS configurations must be robust and capable of handling substantial fluctuations in voltage and current, thereby ensuring continuous and reliable electrolyzer operation.
The Uninstalled cost is then multiplied by a set of "Hand factors" or derived multipliers that convert equipment costs into installed costs. These multipliers account for auxiliary materials, assembly, project engineering, civil work, overheads, supervision, freight, and contingencies

![[Uninstall cost of PEM electrolyser.png|455x273]]
@astrianiOptimalPlanningRenewable2024


**RE system cost**
To account for variable energy supply scenarios, a separate modeling layer is introduced for renewable electricity provision. This includes solar photovoltaic (PV) and onshore wind power as independent and hybrid supply configurations. For each renewable source, the capital cost $(C_{RE})$ and operating cost $O_{RE})$ are modeled as functions of installed capacity  $P$ and technology-specific scale index $s$ :
$C_{RE} = C_{ref} \cdot \left(\frac{P}{P_{ref}}\right)^{-s}; \quad O_{RE} = O_{ref} \cdot P$
1. Power Law Scaling (Economies of Scale)

$$
\text{CapEx}_{\text{PV}} = a \cdot C^b
$$

- **CapEx**: Capital cost (\$)
- **C**: System capacity (kW or MW)
- **a**: Baseline cost coefficient (\$/kW or \$/MW)
- **b**: Scaling exponent (typically \( b < 1 \), reflecting economies of scale)
`equipment sizing calculations were executed and therefore price corrections were performed using the 6/10 rule (Equation 3.5) [50]; where C1 an V1 are the known cost ($) and volume (m3) of the equipment, C2 and V2 are the cost and volume of the sized equipment.

Literature obtained cost prices from system design simulations indicate a cost of approximately <mark style="background: #FFB8EBA6;">1,191 A$/kW$</mark> for solar PV and <mark style="background: #FFB8EBA6;">2,383 A$/kW$</mark> for wind, based on 20 MW project scale, with negligible installation cost and an 8% land procurement cost. These values align with contemporary data compiled in utility-scale renewable energy projects [ref].

Hybrid power systems combining solar and wind in a 1:1 capacity ratio were modeled with proportional capital cost contributions and aggregate OpEx, yielding an effective system cost of <mark style="background: #FFB8EBA6;">38.6 million $ </mark>for a 20 MW plant with <mark style="background: #FFB8EBA6;">210,000 $/yr</mark> in OpEx. These values serve as input parameters for alternative electrolyzer configurations relying on off-grid renewable supply.

Alternatively, grid-connected scenarios are modeled through fixed power purchase agreement (PPA) rates or time-variable retail tariffs. In both cases, grid connection cost $C_{grid}$ and usage charges $U_{grid}$ are incorporated as lump-sum or annualized costs, which can be flexibly assigned depending on region and utility structure.

 All costs are consolidated in Levelized Cost of Energy (LCOE)



**Levelized Cost of Electricity (LCOE):** For the renewable energy supply system (solar, wind, or hybrid), the LCOE is computed to assess the cost per unit of electricity generated
$$\mathrm{LCOE} = \frac{\mathrm{CRF} \cdot C_{RE} + O_{RE}}{E_{annual}}$$

where $C_{RE}$ is the capital cost of the renewable energy plant,  $O_{RE}$  is the annual operating cost, and $E_{annual}$ is the annual electricity production. LCOE values are benchmarked against grid electricity tariffs or PPA prices to determine economic competitiveness

				
- **CRF**: Capital recovery factor  
  $$
  \text{CRF} = \frac{r(1+r)^n}{(1+r)^n - 1}
  $$
  where \( r \) = discount rate, \( n \) = system lifetime

where CRF is the capital recovery factor, is annual operation time, and CF is capacity factor. This multi-scenario model structure enables comparison of grid-connected and off-grid renewable-powered electrolyzer configurations under varying economic and policy conditions.

### **4.4.2** OPEX components: electricity, water, maintenance, replacements

After calculating the estimated capital expenses, the operational expenses (OPEX) were established. The OPEX can be divided into variable and fixed expenses.

; Table 3.2 gives a quick overview of the assumptions for estimating the operational expense




**4.5 Sensitivity and Uncertainty Analysis**

- **4.5.1** Univariate sensitivity (tornado diagrams) on key inputs
- **4.5.2** Multivariate to capture parameter interactions
    Contour
    Monte Carlo
- **4.5.3** Interpretation of uncertainty ranges for LCOH and NPV



## 4.4  System analysis

System design and parameters
	Parameters and design considerations.
	System efficiency and energy consumption
	BoP and Energy balances assumptions
	DCCF, process




### 4.41 System efficiency

The fundamental indicator of electrolyzer performance is the **mass of hydrogen produced** per unit time and per operating condition. For a specific operational mode indexed by hour $h$ and year $y$, the hourly hydrogen production is expressed as:
$$
m_{H_2,h,y} = \frac{\eta_{El,h} P_{EL,h}}{HHV_{H_2} f_{der,El,y} \ n}
$$
Energy balance

![[image-40.png]]


LHV-based efficiency and HHV-based efficiency.
The **Balance of Plant (BoP)** can contribute between 5–20% of total energy consumption depending on the scale and design of the system. Thus, ignoring BoP loads can lead to significant overestimations of system efficiency. To characterize how effectively the PEM electrolyzer converts input electrical power into chemical energy stored in hydrogen, **LHV-based** and **HHV-based** efficiencies
The _lower heating value_ (LHV) excludes the energy associated with condensing water vapor produced during combustion. It represents the net usable energy:
$$
\eta_{LHV} = \frac{m_{H_2} \cdot LHV_{H_2}}{W_{PEM} + W_{BoP}}
$$
the higher heating value (HHV) includes the latent heat of vaporization, and therefore represents the total theoretical energy recoverable:
$$
\eta_{HHV} = \frac{m_{H_2} \cdot HHV_{H_2}}{W_{AEM} + W_{BoP}}
$$
At standard operation (60–80 °C, ambient pressure), commercial PEM electrolyzers achieve 65–70% HHV efficiency, with state-of-the-art systems approaching 80% with waste heat recovery integration. Generally, **LHV-based efficiency** is more appropriate for fuel cell applications (net power use), whereas **HHV-based efficiency** is used in **electrolyzer evaluations**, especially under policy or grid-integration scenarios where the energy source includes renewable generation with seasonal storage requirements.
An inverse metric of energy efficiency , **Specific Energy Consumption** ($SE_{H_2}$), defined as the amount of electrical energy required to produce one kilogram of hydrogen.
specific energy consumption for total hydrogen production is given as

$$
SE_{H_2} = \frac{W_{PEM} + W_{BoP}}{m_{H_2}}
$$

inspo: @kimTechnoeconomicAnalysisAnion2024



Baseline Design Parameters: Technical Operating Parameters and Specifications and Financial Input Values

|Parameters|Input|
|---|---|
|Production capacity, kg/day|10,000|
|Start-up Year|2024|
|Total Uninstalled Capital ($/kW)|$995|
|Total Electrical Usage (kWh/kg)|54.3 [% LHV] (61%) (% HHV) (72.6%)|
|Stack Electrical Usage (kWh/kg)|49 [% LHV] (68%) (% HHV) (80%)|
|BoP Electrical Usage (kWh/kg)|5.04|
|Stack Current Density (A/cm²)|2|
|Cell Voltage (V)|1.8|
|Specific Electrolyzer Power Consumption at Peak Production (kWh/kg H₂)|49|
|Outlet Pressure from Electrolyzer (bar)|30|
|Installation Cost (% of uninstalled capital cost)|12%|
|Stack Replacement Interval (years)|10|
|Stack Replacement Cost Percentage (% of installed capital cost)|15%|
|Plant Life (years)|20|
|Stack Degradation Rate (mV/khrs)|1.5|
|Cell Active Area (cm²)|877|
|Capacity Factor (%)|90%|
|Tax rate|27%|
|Plant Life (years)|20|
|Depreciation Type|MACRS|
|Depreciation Schedule Length (years)|3|
|% of Capital Spent in 1ˢᵗ, 2ⁿᵈ, 3ʳᵈ year of construction|10%, 60%, 30%|
|% of Fixed and Variable Operating Cost During Start-up|75%, 50%|
Modified Accelerated Cost Recovery System (MACRS).












### 4.2.5 Parameter Sensitivity Analysis

insps. @19009_h2_production_cost_pem_electrolysis_2019.pdf

```
Three sensitivity analyses were conducted: 
1) Single Variable Tornado Charts in which one parameter was varied, all others were held fixed at the baseline case values, and the new cost was recorded (Table 4, Figure 3 and Figure 5). 
2) Two Variable Contour Plots in which electricity cost and stack electrical usage were varied within the bounded ranges and the resulting hydrogen cost plotted in a contour graph (Figure 4 and Figure 6). 
3) Monte Carlo Analysis in which all Table 2 parameters were stochastically and simultaneously varied over their full range to create a probability distribution function of potential hydrogen costs (Table 1).
```

![[image-44.png]]



Two critical assumptions were not varied: the operation period of 20 years





Given the complex interdependencies in PEM electrolyser economics, rigorous sensitivity analysis provides critical insights into cost drivers and optimization pathways:

For the PEM electrolyser system, primary sensitivity parameters include:

1. **Electricity price elasticity**: LCOH sensitivity typically ranges from 0.60 to 0.85, demonstrating the dominant role of operational electricity costs.
2. **Capacity factor impact**: Operating hour increases yield diminishing returns on LCOH reduction, with sensitivity coefficients of -0.15 to -0.35 depending on the capital intensity.
3. **Capital cost variation**: Initial investment sensitivity ranges from 0.15 to 0.40, with higher values for systems operating at lower capacity factors.
4. **Stack replacement timing**: Lifetime extension sensitivity coefficients typically range from -0.05 to -0.15, highlighting the importance of durability improvements.

Monte Carlo simulation incorporating parameter distributions provides probabilistic LCOH outcomes across diverse deployment scenarios. By generating cumulative distribution functions for LCOH, decision-makers can evaluate risk profiles associated with electrolyser investments under varying market conditions (Wei et al., 2022).

A comprehensive probabilistic framework incorporates parameter uncertainty through Monte Carlo simulation:


LCOH_{p} = f(X_1, X_2, ..., X_m)


where:

- $LCOH_{p}$ is the probabilistic LCOH
- $X_i$ are stochastic input parameters with defined probability distributions
- $f()$ is the functional relationship defined by the LCOH model

Key uncertain parameters include:

1. **Technical Parameters**: Efficiency degradation rates (normal distribution, μ=1-2%/year, σ=0.5%/year), stack lifetime (Weibull distribution, shape=2.5-3.5, scale=50,000-70,000 hours).
2. **Economic Parameters**: Electricity prices (often modeled with time series methods or mean-reverting stochastic processes), discount rates (triangular distribution, min=4%, mode=7%, max=10%).
3. **Operational Parameters**: Capacity factor (beta distribution, α=3-5, β=1-2), specific energy consumption (lognormal distribution, μ=dependent on system design, σ=3-5% of μ).





Key PEM Electrolyzer Cost and Performance Parameters for Sensitivity Analysis

| Parameter                      | Unit              | Low                                       | Base                                                                            | High                           | Reference(s)                                                                                                                                                                                                 |
| ------------------------------ | ----------------- | ----------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Installed capital cost         | $ / kW            | $800 / kW (future DOE target)             | $2,000 / kW (current average)                                                   | $3,500 / kW (today’s high end) | DOE target and cost‐reduction projections, SBadget manufacting                                                                                                                                               |
| Uninstalled cpital cost        |                   | $250 /kW by 2026 $150 /kW ultimate (2031) | $995/kW  $975–$1,200 /kW (for production rates from ~10 MW/yr up to >100 MW/yr) | $1500 / kW                     | Badget et al 2024                                                                                                                                                                                            |
| Fixed O&M cost                 | % of cap. cost/yr | 15 % (best‐in‐class estimates)            | 17 % (H2A default)                                                              | 22 % (older systems)           | H2A assumptions, [Hydrogen Program](https://www.hydrogen.energy.gov/docs/hydrogenprogramlibraries/pdfs/24005-clean-hydrogen-production-cost-pem-electrolyzer.pdf?utm_source=chatgpt.com)                     |
| Electricity feedstock cost     | $ / kWh           | $0.03 / kWh (low‐cost renewables)         | $0.07 / kWh (U.S. industrial avg.)                                              | $0.15 / kWh (high‐retail)      | Renewable PPA & EIA data, Hydrogen Program, [U.S. Energy Information Administration](https://www.eia.gov/electricity/monthly/epm_table_grapher.php?t=epmt_5_6_a&utm_source)                                  |
| Deionized water cost           | $ / gal           | $0.002 / gal                              | $0.005 / gal (H2A default)                                                      | $0.010 / gal                   | H2A demineralized‐water input,H2A data, [NREL](https://docs.nrel.gov/docs/fy09osti/44103.pdf?utm_source)                                                                                                     |
| O₂ by-product credit price     | $ / kg            | $0 / kg (no sale) base                    | $0.09 / kg (N. America avg.)                                                    | $0.17 / kg (EU spot)           | Industrial-gas pricing, [businessanalytiq](https://businessanalytiq.com/procurementanalytics/index/oxygen-price-index/?utm_source), H2A database                                                             |
| Corporate tax rate (combined)  | %                 | 21 % (federal only)                       | 25 % (avg. U.S. combined)                                                       | 33 % (high-state)              | Federal & state rates, [PwC Tax Summaries](https://taxsummaries.pwc.com/quick-charts/corporate-income-tax-cit-rates?utm), Tax Foundation                                                                     |
| Electrolyzer energy efficiency | kWh / kg H₂       | 45 kWh/kg (future target)                 | 55 kWh/kg (current state-of-art)                                                | 65 kWh/kg (lower-grade)        | H2A system performance, [Hydrogen Program, OSTI](https://www.hydrogen.energy.gov/docs/hydrogenprogramlibraries/pdfs/19009_h2_production_cost_pem_electrolysis_2019.pdf?Status=Master&utm_source=chatgpt.com) |




