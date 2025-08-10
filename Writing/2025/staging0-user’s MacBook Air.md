 = 1



## Appendix A. PEM Electrolyzer Design Parameters

This appendix details the parameters, constants, and key assumptions used in the mathematical models for the PEM electrolyzer and the renewable energy systems. Values are drawn from established literature to ensure the model's validity and relevance.
### Table A.1 PEM Electrolyser Cell Design Parameters and Assumptions

**Table A.1** Cell geometry, materials, and operating conditions

| Parameter                                       | Value                         | Reference / Justification                                                 |
| ----------------------------------------------- | ----------------------------- | ------------------------------------------------------------------------- |
| Faraday constant, F (C mol⁻¹)                   | 96 485                        | Standard value                                                            |
| Gas constant, R (J mol⁻¹ K⁻¹)                   | 8.314                         | Standard value                                                            |
| Number of Electrons Transferred (z)             | 2                             | Stoichiometry of the water splitting reaction                             |
| Cell temperature, T (K)                         | 333.15                        |                                                                           |
| Cell pressure, Pₐ/P𝒸 (bar)                     | 1 (anode) / 30 (cathode)      |                                                                           |
| Maximum current density, iₘₐₓ (A cm⁻²)          | 2.0                           | Assumption based on high-performance MEAs (Kang et al., 2021)             |
| Limiting current density, iₗᵢₘ (A cm⁻²)         | 6.0                           | @bessarabovPEMWaterElectrolysis2018                                       |
| Anodic Charge Transfer Coeff. (αa​)             | 2.0<br>                       | Typical value for PEM electrolysis OER kinetics (Marangio et al., 2009)   |
| Cathodic Charge Transfer Coeff. (αc​)           | 0.5                           | Typical value for PEM electrolysis HER kinetics (Carmo et al., 2013)      |
| Anode Exchange Current Density (i0,a​, A/cm²)   | 2.618×10⁻⁶                    |                                                                           |
| Cathode Exchange Current Density (i0,c​, A/cm²) | 1.0×10⁻¹                      | Carmo et al., 2013)                                                       |
| Electrode thickness, tₑ (µm)                    | 200                           |                                                                           |
| Electrode porosity, ε                           | 0.30                          |                                                                           |
| Membrane thickness, tₘ (µm)                     | 178                           | 127 - 178 Representative of standard Nafion™ membranes (e.g., N115, N117) |
| Membrane Conductivity (σm                       | Empirical function of T and λ | Based on the widely used model for Nafion™ (Springer et al., 1991)        |
| Electro-osmotic Drag Coeff. (nd​)               | Empirical function of T       | (Onda et al., 2002)                                                       |
| Titanium resistivity, ρₜᵢ (Ω cm)                | 5.0×10⁻³                      |                                                                           |
| Carbon‐paper resistivity, ρ_{CP} (Ω cm)         | 8.0×10⁻²                      |                                                                           |
| Water viscosity, (at 60°C) μH2​O​ Pa·s          | 4.67 x 10⁻⁴                   | Standard value                                                            |
| Water density, ρH2​O​ kg/m³                     | 983.2                         | Standard value                                                            |
| Anode catalyst loading, mg/cm²                  | 1.54                          |                                                                           |
| Cathode catalyst loading, mg /cm²               | 0.40                          |                                                                           |
| Active area, A (cm²)                            | 877                           | Assumptions                                                               |
| Cell voltage, V                                 | 1.79                          | Model output                                                              |
| Voltage efficiency                              | 0.69                          |                                                                           |
| Power per cell, kW                              | 3.14                          | Model output                                                              |
| Total stack power, kW                           | 19 034                        |                                                                           |
| Specific energy consumption, kWh /kg H₂         | 49                            | Model output                                                              |


---

### Table A.2 Electrochemical Kinetic Parameters

**Table A.2** Reference exchange currents and activation energies  for OER and HER
@chungDesignSpacePEM2024

| Variable          | Value     | Units   | Reference(s)                                                                     |
| ----------------- | --------- | ------- | -------------------------------------------------------------------------------- |
| i₀, cathode (ref) | 0.75×10⁻³ | A cm⁻²  | García‐Valverde et al. (2012), Carmo et al. (2013), Coutanceau & Barrière (2018) |
| Eₐ𝒸ₜ, cathode    | 30 000    | J mol⁻¹ | He et al. (2017)                                                                 |
| i₀, anode (ref)   | 1.0×10⁻⁷  | A cm⁻²  | García‐Valverde et al. (2012), Carmo et al. (2013), Coutanceau & Barrière (2018) |
| Eₐ𝒸ₜ, anode      | 90 000    | J mol⁻¹ | García‐Valverde et al. (2012), Suermann et al. (2018)                            |



_This table summarizes literature values for catalyst loading and the resulting kinetic parameters, which are highly dependent on the specific materials used._

References for current density and activation energy for OER and ERR
Reference for Current Density and Activation Energy for Anode and cathode half-cells at 318 k()
insp: @chungDesignSpacePEM2024

| Variable                             | Value                 | Units    | Reference                                                                                                |
| ------------------------------------ | --------------------- | -------- | -------------------------------------------------------------------------------------------------------- |
| $i_{0, \text{cathode}}^{\text{ref}}$ | $0.75 \times 10^{-3}$ | A/cm$^2$ | @garcia-valverdeSimplePEMWater2012 , @carmoComprehensiveReviewPEM2013 ,  @coutanceauChapter3Hydrogen2018 |
|                                      | $1.0 \times 10^{-3}$  |          | @choiSimpleModelSolid2004 , Pt–Ir anode<br>Pt cathode                                                    |
|                                      | 9.0 \times 10^{-2}$   |          | @harrisonSemiempiricalModelDetermining2005 ,Pt–Ir anode<br>Pt cathode                                    |
|                                      | $1.0 \times 10^{-3}$  |          | @marangioDirectHighPressure2009 , Pt–Ir anode<br>Pt cathode                                              |
| $E_{\text{act, cathode}}$            | 30,000                | J/mol    | @heHydrogenEvolutionPt1112017                                                                            |
| $i_{0, \text{anode}}^{\text{ref}}$   | $1.0 \times 10^{-7}$  | A/cm$^2$ | @garcia-valverdeSimplePEMWater2012  , @carmoComprehensiveReviewPEM2013 , @coutanceauChapter3Hydrogen2018 |
|                                      | $1.0 \times 10^{-12}$ |          | @choiSimpleModelSolid2004 , Pt–Ir anode<br>Pt cathode                                                    |
|                                      | $1.65 \times 10^{-8}$ |          | @harrisonSemiempiricalModelDetermining2005                                                               |
|                                      | $1.0 \times 10^{-7}$  |          | @marangioDirectHighPressure2009, Pt–Ir anode<br>Pt cathode                                               |
| $E_{\text{act, anode}}$              | 90,000                | J/mol    | @garcia-valverdeSimplePEMWater2012   18 @suermannComparingKineticActivation2018                          |
Tables






---

### Table A.3 Polarization Curve Validation

**Table A.3** Experimental i–V data (Debe et al. 2012)

|Current density, i (A cm⁻²)|Cell voltage, V|
|---|---|
|0.14|1.543|
|0.24|1.584|
|0.33|1.607|
|0.47|1.619|
|0.54|1.663|
|0.58|1.650|
|0.80|1.692|
|0.96|1.723|
|1.10|1.748|
|1.24|1.773|
|1.34|1.791|
|1.46|1.811|
|1.59|1.832|
|1.72|1.853|
|1.84|1.874|

---

### Table A.4 System‐Level Design (H2A Case)



#### Table A.4.1 System Energy Balance Parameters

Assumption from H2A Case 

|                                                                      | On-site   | Centra    | Basis for Assumptions                                                                                                                                             |
| -------------------------------------------------------------------- | --------- | --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **H₂ Outlet Pressure**, bar                                          | 30        | 30        |                                                                                                                                                                   |
| **Stack Electrical Usage**                                           |           |           |                                                                                                                                                                   |
| **Cell voltage** , volts/cell                                        | 1.79      | 1.79      | Based on electrochemical design output:                                                                                                                           |
| **Total Stack Energy Usage per mass net H₂** ,kWhₑₗₑc/kgNet H₂       | **49.23** | **49.23** |                                                                                                                                                                   |
| **BOP Loads**                                                        |           |           |                                                                                                                                                                   |
| Power Inverter Efficiency, %                                         | 94%       | 95%       | Based on industry input (with improvement to 97% for future performance and to 95% for current/Central to reflect larger size).                                   |
| Inverter Electrical Load, kWhₑₗₑc/kgNet H₂                           | 2.95      | 2.59      |                                                                                                                                                                   |
| Dryer Thermal Load, kWhₜₕₑᵣₘ/kgNet H₂                                | 0.34      | 0.34      | Based on Hysys Simulation.                                                                                                                                        |
| Dryer Efficiency, kWhₑₗₑc/kWhₜₕₑᵣₘ                                   | 3.67      | 3.67      | Based on industry input for the ratio of net electrical energy for Forecourt. 5% efficiency improvement for Future Forecourt, 10% improvement for Future Central. |
| Dryer Electrical Load, kWhₑₗₑc/kgNet H₂                              | 1.25      | 1.25      |                                                                                                                                                                   |
| Misc Electrical Load, kWhₑₗₑc/kgNet H₂                               | 1.2       | 1.2       | Based on industry input for current. 5% improvement for future/forecourt. 10% improvement for future/Central.                                                     |
| **Total BOP Electrical Load** , kWhₑₗₑc/kgNet H₂                     | **5.40**  | **5.04**  |                                                                                                                                                                   |
| **Total System Electrical Usage per mass net H₂** , kWhₑₗₑc/kgNet H₂ | **54.6**  | **54.3**  |                                                                                                                                                                   |




**Table A.4.2** On‐site vs central plant assumptions

| Parameter                             | On-site | Central | Basis                                  |
| ------------------------------------- | ------- | ------- | -------------------------------------- |
| H₂ outlet pressure (bar)              | 30      | 30      | —                                      |
| Cell voltage (V)                      | 1.79    | 1.79    | From cell model                        |
| Stack energy use (kWh kg⁻¹ H₂)        | 49.23   | 49.23   | —                                      |
| BOP electrical load (kWh kg⁻¹ H₂)     | 5.40    | 5.04    | Inverter, dryer, misc. (industry data) |
| Total system energy use (kWh kg⁻¹ H₂) | 54.6    | 54.3    | Sum of stack + BOP                     |




---




### Table A.5 Renewable Energy Integration Parameters



#### **Table A.5.1 : Photovoltaic (PV) System Model Parameters**

| Parameter (Symbol, Unit)                  | Assumed Value / Description | Peer-Reviewed Reference / Justification                                     |
| :---------------------------------------- | :-------------------------- | :-------------------------------------------------------------------------- |
| STC Irradiance (GSTC​, W/m²)              | 1000                        | Industry standard definition (IEC 61215)                                    |
| STC Cell Temperature (TSTC​, °C)          | 25                          | Industry standard definition (IEC 61215)                                    |
| Power Temperature Coefficient (αp​, %/°C) | -0.3% to -0.45%             | Typical range for monocrystalline silicon panels (Dubois et al., 2017)      |
| Nominal Operating Cell Temp. (NOCT, °C)   | 45 ± 2                      | Standard parameter for real-world performance estimation (Ross, 1981)       |
| System Derating Factor (fderate​)         | 0.85 - 0.92                 | Accounts for soiling, wiring, inverter losses, etc. (NREL, 2023)            |
| Annual Degradation Rate                   | 0.5% per year               | Median degradation rate observed in long-term studies (Jordan et al., 2016) |





#### A.5.1 Effective Capacity Factors

**Table A.5** Renewables and storage

| Category          | Capacity (MW) | Capacity factor |
| ----------------- | ------------: | --------------: |
| PV                |             — |            25 % |
| Wind              |            10 |            34 % |
| Grid              |             — |            95 % |
| Battery           |             0 |            17 % |
| **Hybrid system** |            10 |            34 % |

 EFFECTIVE CAPACITY FACTOR OF SYSTEM

| Category                       | installed capacity, MW | CF                                |
| ------------------------------ | ---------------------- | --------------------------------- |
| Capacity factors of RE sys     |                        |                                   |
| PV                             | -                      | 25%                               |
| Wind                           | 10                     | 34%                               |
| Industrial grid electricity    |                        | 95%                               |
| battery                        | 0                      | 17%                               |
| battery cycles per day         | 1                      |                                   |
| PV annual avg energy, E_PV     | 0.00                   | MWh                               |
| Wind Annual avg energy, E_wind | 29784.00               | MWh                               |
| Annual battery discharged      | -                      | MWh                               |
| Battery round trip eff         | 0.88                   | round-trip efficiency (typically) |
| Battery net output, E_batt     | -                      | MWh                               |
| Total energy output, E_annual  | 29784.00               | MWh                               |
| C_hybrid                       | 10                     | MW                                |
| CF hybrid total                | 0.34                   |                                   |

#### A.5.2 Levelized Cost of Energy (LCOE)

**Table A.6** Wind‐only case

| Parameter                 |             Value | Unit        | Notes                   |
| ------------------------- | ----------------: | ----------- | ----------------------- |
| Capacity (MW)- PV only    |                20 | MW          | Assumption              |
| Capacity (MW)- Wind only  |                20 | MW          | Assumption              |
| Capacity (MW)- Hybrid     |     10 Wind 10 PV | MW          | Assumption              |
| Discount rate, r          |              0.12 |             | —                       |
| Lifetime, n               |                25 | yr          | —                       |
| CRF                       |            0.2914 | —           | Capital recovery factor |


#### A.5.2 Wind Turbine Parameters

**Table A.7** Design & Weibull model inputs

| Parameter                                |                          Value |                                                                                                             Reference / Justification |
| ---------------------------------------- | -----------------------------: | ------------------------------------------------------------------------------------------------------------------------------------: |
| Air density, (ρ , kg/m³)                 |                          1.225 |                                                                                             Standard sea-level air density (ISO 2533) |
| Swept Area per MW , (A, m² /MW)          |                          3 000 |                                                                                                                                       |
| Rated power ( P_{rated}, MW)             |                              1 |                                                                                                                                       |
| Drivetrain & Generator Efficiency (ηWT​) |                           0.90 |                                                            Typical efficiency for modern gear-driven turbines 0.90 - 0.95 (Hau, 2013) |
| Cp (power coefficient) Cₚ                |                           0.40 | Values taken from models of specific turbines, e.g., the NREL 5-MW reference turbine or as cited in your text (Castillo et al., 2023) |
| Weibull scale (λ)(m s⁻¹)                 |                              8 |                                                                                                                                       |
| Weibull shape (k)                        |                              2 |                                                                                                                                       |
| Cut-in Wind Speed (vcin​, m/s)           |                        3/13/25 |                                                                      Typical operational limit for utility-scale turbines (Hau, 2013) |
| Rated Wind Speed (vr​, m/s)              |                                |                                                         Speed at which the turbine reaches its nameplate power (Manwell et al., 2010) |
| Cut-out Wind Speed (vcout​, m/s)         |                                |                                                        Safety limit to prevent structural damage at high winds (Manwell et al., 2010) |
| Tip‐speed ratio,\omega                   |                             10 |                                                                                                                                     — |
| Pitch angle β                            |                              2 |                                                                                                                                     ° |
| Polynomial coefficients c₀–c₁₁           | Turbine-specific empirical fit |                                                                                                          as in Castillo et al. (2023) |

TAble Power curve here

#### A.5.3 Polynomial  Power coefficient cp curves in wind turbines 

@castilloComparisonPowerCoefficients2023

| Constants | Kotti | Khajuria | Ovando | Feng  | Llano  | Shi   | Bustos | Ahmed |
| --------- | ----- | -------- | ------ | ----- | ------ | ----- | ------ | ----- |
| c₀        | 0.5   | 0.5      | 0.5176 | 0.22  | 0.5    | 0.73  | 0.44   | 1     |
| c₁        | 116   | 116      | 116    | 116   | 72.5   | 151   | 124.99 | 110   |
| c₂        | 0     | 0.4      | 0.4    | 0.4   | 0.4    | 0.58  | 0.4    | 0.4   |
| c₃        | 0.4   | 0        | 0      | 0     | 0      | 0     | 0      | 0     |
| c₄        | 0     | 0        | 0      | 0     | 0      | 0.002 | 0      | 0.002 |
| c₅        | 0     | 0        | 0      | 0     | 0      | 2.14  | 0      | 2.2   |
| c₆        | 5     | 5        | 5      | 5     | 5      | 13.2  | 6.94   | 9.6   |
| c₇        | 21    | 21       | 21     | 12.5  | 13.125 | 18.4  | 17.05  | 18.4  |
| c₈        | 0     | 0        | 0.0068 | 0     | 0      | 0     | 0      | 0     |
| c₉        | 0.008 | 0        | 0.08   | 0.08  | 0.08   | 0.02  | 0.08   | 0.02  |
| c₁₀       | 0     | 0.088    | 0      | 0     | 0      | 0     | 0      | 0     |
| c₁₁       | 0.035 | 0.035    | 0.035  | 0.035 | 0.035  | 0.003 | 0.001  | 0.03  |



#### A.5.1 Photovoltaic (PV) System Model Parameters

**Table A.8** Irradiance, performance, and temperature model

| Parameter                                                               | Symbol         |          Value |  Unit | Notes                                                                                  |
| ----------------------------------------------------------------------- | -------------- | -------------: | ----: | -------------------------------------------------------------------------------------- |
| PV rated power                                                          | P_{PV,rated}   |            1.0 |    MW | —                                                                                      |
| Clear‐sky STC GHI Irradiance (GHI , GSTC​, W/m²)                        |                |          1 000 | W m⁻² | Industry standard definition (IEC 61215)                                               |
| STC Cell Temperature (TSTC​, °C)                                        |                |             25 |       | Industry standard definition (IEC 61215)                                               |
|                                                                         |                |                |       |                                                                                        |
| Tilt factor                                                             | GTI/GHI        |         1.0457 |     — | GTI on module plane                                                                    |
| Derating factor (soiling, etc.) (fderate​)                              | f_derPV,y      |           0.90 |     — | Accounts for soiling, wiring, inverter losses, etc.                                    |
| Annual Degradation Rate                                                 |                |  0.5% per year |       | Median degradation rate observed in long-term studies (Jordan et al., 2016)            |
| Cell temperature coefficient, Power Temperature Coefficient (αp​, %/°C) | K_p            |        –0.0035 |       | -0.3% to -0.45% Typical range for monocrystalline silicon panels (Dubois et al., 2017) |
| Nominal Operating Cell Temp. (NOCT, °C)                                 | NOCT           |             45 |    °C | Standard parameter for real-world performance estimation (Ross, 1981)                  |
| Ambient temperature (annual mean / amp.)                                | T_mean / T_amp |        15 / 10 |    °C | —                                                                                      |
| Module cell temp.                                                       | T_{pv-cell}    |          49.32 |    °C | At NOCT conditions                                                                     |
| Declination, elevation, latitude                                        | δ/σ/φ          | 21.75/71.75/40 |     ° | —                                                                                      |

---

## Appendix B. Economic & System Financial Parameters

### B.1 Economic Assumptions

**Table B.1** Key techno-economic inputs

|Parameter|Value|
|---|---|
|Production capacity|10 000 kg day⁻¹|
|Startup year|2024|
|Uninstalled capex ($ kW⁻¹)|995|
|Electricity use (stack + BoP), kWh kg⁻¹ H₂|54.3 (61 % LHV)|
|Installation cost (% of uninstalled capex)|12 %|
|Stack replacement interval|10 yr|
|Stack replacement cost (% of installed capex)|15 %|
|Plant life|20 yr|
|Stack degradation rate|1.5 mV khrs⁻¹|
|Capacity factor|90 %|
|Corporate tax rate|27 %|
|Depreciation|MACRS, 3-yr schedule|
|Capex spend profile (year 1/2/3)|10 % / 60 % / 30 %|
|Fixed vs variable O&M during startup|75 % / 50 %|

---

### B.2 Capital Costs

#### B.2.1 Direct Fixed Capital

|Description|Value|
|---|--:|
|Direct capital (FCI)|$20 440 000.00|

#### B.2.2 Indirect Depreciable Costs

**Table B.2**

|Item|$ (2023)|Notes|
|---|--:|---|
|Site preparation & construction|$3 852 940.00|H2A defaults|
|Engineering & design|$60 249.30|AACE guidelines|
|Project contingency (15 %)|$3 066 000.00|—|
|Permitting & licensing|$36 149.50|H2A default|
|**Total indirect capital**|**$7 015 338.80**||

#### B.2.3 Non-Depreciable Capital

**Table B.3**

|Item|$ (2023)|Notes|
|---|--:|---|
|Land cost|—|$1 071.94 m⁻², area ~1 310 m²|
|Other non-depreciable|–$1 404 925.76|—|
|**Total non-depr. capital**|**$0.00**||

#### B.2.4 Working Capital

|Description|$ (2023)|Notes|
|---|--:|---|
|Working capital|$4 962 494.72|15 % of TCI|

#### B.2.5 Total Capital Investment

|Description|Value|
|---|--:|
|**Total capital costs**|**$27 455 338.88**|

---

### B.3 Operating Costs

#### B.3.1 Fixed O&M

**Table B.6**

|Category|$ yr⁻¹|Notes|
|---|--:|---|
|Labor (10 FTEs)|$650 895.44|$31.78 man-hr|
|G&A (20 % of labor)|$130 179.09|H2A default|
|Licensing & permits|$3 392.62|H2A default|
|Property tax & insurance|$549 106.78|H2A default|
|Rent|$11 557.69|936 ft² @ $3.23 m² mo⁻¹|
|Maintenance & repairs|$2 877 428.84|5 % of direct capital|
|**Total fixed O&M**|**$4 771 667.29**||

#### B.3.2 Variable O&M

**Table B.7** Materials, utilities, credits

|Category|Cost ($ yr⁻¹)|Notes|
|---|--:|---|
|Energy feedstock|$13 861 231.74|Industrial electricity|
|Energy utility|$1 287 670.18|Cooling, process water|
|Byproduct credit (O₂)|–$745 650.31|Oxygen sales|
|Other materials & water|$1 887 261.89|Deionized & cooling water, maintenance|
|Other variable costs|$25 560.00|Waste disposal, etc.|
|**Total variable O&M**|**$15 316 ?²**|(sum feedstock + utility + other)|

---

## Appendix C. Uncertainty & Sensitivity Parameters

### C.1 Univariate Sensitivity

**Table C.1**

|Parameter|Unit|Low|Base|High|Source|
|---|---|---|---|---|---|
|Installed capex|$ kW⁻¹|800|2 000|3 500|DOE targets / industry data|
|Uninstalled capex|$ kW⁻¹|250|995|1 500|H2A / DOE projections|
|Fixed O&M|% capex yr⁻¹|15 %|17 %|22 %|H2A assumptions|
|Electricity price|$ kWh⁻¹|0.03|0.07|0.15|EIA / PPA data|
|Water cost|$ gal⁻¹|0.002|0.005|0.010|H2A demin. water input|
|O₂ credit price|$ kg⁻¹|0|0.09|0.17|Industrial‐gas pricing|
|Corporate tax rate|%|21 %|25 %|33 %|Federal & state rates|
|Electrolyzer SEC|kWh kg⁻¹ H₂|45|55|65|H2A performance data|

### C.2 Monte Carlo Simulation Inputs

**Table C.2**

|Parameter|Min|Max|Base|Distribution|Notes|
|---|--:|--:|--:|--:|---|
|Electricity cost|0.03|0.12|0.07|Normal|EIA data|
|Tax rate|21 %|30.4 %|27 %|Uniform|—|
|Discount rate|8 %|15 %|10 %|Uniform|—|
|FCI|$5.93 M|$41.6 M|$27.46 M|Triangular|Based on capex range|
|Fixed O&M|$4 M|$5.9 M|$4.77 M|Triangular|Includes labor, G&A, maintenance|
|Design capacity|867 t yr|3 650 t yr|3 467 t yr|Triangular|× capacity factors|
|Working capital|$3.97 M|$5.55 M|$4.96 M|Triangular|20 % unc.|
|Utilities|$2.59 M|$3.59 M|$2.99 M|Triangular|20 % unc.|

---

## Appendix D. Python Code & Documentation

All modeling and data‐processing scripts (PEM electrolyzer, sensitivity, Monte Carlo) are provided as separate `.py` files in the supplementary material repository. Key modules include:

- `pem_model.py` – cell voltage decomposition, transport fluxes
    
- `sensitivity.py` – univariate and tornado plots
    
- `monte_carlo.py` – stochastic LCOH simulation
    

Please refer to **Supplementary File D** for annotated code listings and usage instructions.










In our base-case, the our model yields $SEC_{H_2}\approx 54.3$  kWh kg⁻¹ (68 % LHV efficiency) at a 90 % capacity factor, in close agreement with both literature benchmarks and experimental Nafion™117 stack data [13]

Energy balance

![[image-40.png]]



















Given the complex interdependencies in PEM electrolyser economics, rigorous sensitivity analysis provides critical insights into cost drivers and optimization pathways:

For the PEM electrolyser system, primary sensitivity parameters include:

1. **Electricity price elasticity**: LCOH sensitivity typically ranges from 0.60 to 0.85, demonstrating the dominant role of operational electricity costs.
2. **Capacity factor impact**: Operating hour increases yield diminishing returns on LCOH reduction, with sensitivity coefficients of -0.15 to -0.35 depending on the capital intensity.
3. **Capital cost variation**: Initial investment sensitivity ranges from 0.15 to 0.40, with higher values for systems operating at lower capacity factors.
4. **Stack replacement timing**: Lifetime extension sensitivity coefficients typically range from -0.05 to -0.15, highlighting the importance of durability improvements.

Monte Carlo simulation incorporating parameter distributions provides probabilistic LCOH outcomes across diverse deployment scenarios. By generating cumulative distribution functions for LCOH, decision-makers can evaluate risk profiles associated with electrolyser investments under varying market conditions (Wei et al., 2022).

A comprehensive probabilistic framework incorporates parameter uncertainty through Monte Carlo simulation:


Key uncertain parameters include:

1. **Technical Parameters**: Efficiency degradation rates (normal distribution, μ=1-2%/year, σ=0.5%/year), stack lifetime (Weibull distribution, shape=2.5-3.5, scale=50,000-70,000 hours).
2. **Economic Parameters**: Electricity prices (often modeled with time series methods or mean-reverting stochastic processes), discount rates (triangular distribution, min=4%, mode=7%, max=10%).
3. **Operational Parameters**: Capacity factor (beta distribution, α=3-5, β=1-2), specific energy consumption (lognormal distribution, μ=dependent on system design, σ=3-5% of μ).








Key PEM Electrolyzer Cost and Performance Parameters for Sensitivity Analysis

| Parameter                      | Unit              | Low                                       | Base                                                                            | High                           | Reference(s)                                                                                                                                                                             |
| ------------------------------ | ----------------- | ----------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Installed capital cost         | $ / kW            | $800 / kW (future DOE target)             | $2,000 / kW (current average)                                                   | $3,500 / kW (today’s high end) | DOE target and cost‐reduction projections, SBadget manufacting                                                                                                                           |
| Uninstalled cpital cost        |                   | $250 /kW by 2026 $150 /kW ultimate (2031) | $995/kW  $975–$1,200 /kW (for production rates from ~10 MW/yr up to >100 MW/yr) | $1500 / kW                     | Badget et al 2024                                                                                                                                                                        |
| Fixed O&M cost                 | % of cap. cost/yr | 15 % (best‐in‐class estimates)            | 17 % (H2A default)                                                              | 22 % (older systems)           | H2A assumptions, [Hydrogen Program](https://www.hydrogen.energy.gov/docs/hydrogenprogramlibraries/pdfs/24005-clean-hydrogen-production-cost-pem-electrolyzer.pdf?utm_source=chatgpt.com) |
| Electricity feedstock cost     | $ / kWh           | $0.03 / kWh (low‐cost renewables)         | $0.07 / kWh (U.S. industrial avg.)                                              | $0.15 / kWh (high‐retail)      | Renewable PPA & EIA data, Hydrogen Program, [U.S. Energy Information Administration](https://www.eia.gov/electricity/monthly/epm_table_grapher.php?t=epmt_5_6_a&utm_source)              |
| Deionized water cost           | $ / gal           | $0.002 / gal                              | $0.005 / gal (H2A default)                                                      | $0.010 / gal                   | H2A demineralized‐water input,H2A data, [NREL](https://docs.nrel.gov/docs/fy09osti/44103.pdf?utm_source)                                                                                 |
| O₂ by-product credit price     | $ / kg            | $0 / kg (no sale) base                    | $0.09 / kg (N. America avg.)                                                    | $0.17 / kg (EU spot)           | Industrial-gas pricing, [businessanalytiq](https://businessanalytiq.com/procurementanalytics/index/oxygen-price-index/?utm_source), H2A database                                         |
| Corporate tax rate (combined)  | %                 | 21 % (federal only)                       | 25 % (avg. U.S. combined)                                                       | 33 % (high-state)              | Federal & state rates, [PwC Tax Summaries](https://taxsummaries.pwc.com/quick-charts/corporate-income-tax-cit-rates?utm), Tax Foundation                                                 |
| Electrolyzer energy efficiency | kWh / kg H₂       | 45 kWh/kg (future target)                 | 55 kWh/kg (current state-of-art)                                                | 65 kWh/kg (lower-grade)        | H2A system performance, [Hydrogen Program, OSTI]                                                                                                                                         |







 ### **4.4.2** Operation cost
 



: electricity, water, maintenance, replacements

After calculating the estimated capital expenses, the operational expenses (OPEX) were established. The OPEX can be divided into variable and fixed expenses.

; Table 3.2 gives a quick overview of the assumptions for estimating the operational expense
**Direct fixed**
$31.29 hourly wage per worker, NREL 2019 (
Burdened labor cost, including overhead ($/man-hr)

| **Indirect fixed**                                                       |
| ------------------------------------------------------------------------ |
| Licensing, Permits and Fees ($/year)                                     |
| Property tax and insurance rate (% of total capital investment per year) |
| Property taxes and insurance ($/year)                                    |
| Rent ($/year)                                                            |

Production Maintenance and Repairs ($/year)
5% of direct captial, Maintenance labor

### Variable operational cost
| Demineralized Water | Cooling Water | Process Water | Oxygen |
| ------------------- | ------------- | ------------- | ------ |
 Energy Feedstocks, Utilities, and Byproducts


A summary of the key assumptions appears in <mark style="background: #FFF3A3A6;">Table 3.2.</mark>



## 4.4  Opex



A summary of the key assumptions appears in <mark style="background: #FFF3A3A6;">Table 3.2.</mark>


Fixed OPEX encompasses both **direct** and **indirect** costs. Direct fixed costs are dominated by labor: following NREL’s 2019 benchmarks, we apply a burdened wage of $31.29 per man-hour, inclusive of benefits and overhead, to the crew required for continuous operation, preventive maintenance, and process monitoring. Indirect fixed costs include annual fees for licensing and permits, property taxes and insurance calculated as a percentage of installed CAPEX, and facility rent. 

Water costs account for the stoichiometric requirement of 9 kg H₂O per kilogram of H₂ plus a 5 % purge allowance, with deionized and cooling water priced according to local utility tariffs. Process utilities such as compressed air or inert gas for safety purging are similarly metered and charged at prevailing rates. Maintenance and repairs are budgeted at 5 % of the direct capital cost each year, reflecting routine servicing of pumps, heat exchangers, and control systems. We also provision for **component replacements**,
Water costs account for the stoichiometric requirement of 9 kg H₂O per kilogram of H₂ plus a 5 % purge allowance, with deionized and cooling water priced according to local utility tariffs.




### **4.4.1** Capital cost breakdown (stack vs. BoP)

The total capital expenditure (CapEx) of the PEM hydrogen production system is deconstructed into two principal purchased-equipment-cost (PEC) categories: the electrolyzer stack and the balance-of-plant (BoP). Following Astriani et al.'s parametric fitting of global cost data, the uninstalled stack cost, $Cost_{EL}$, is expressed as an exponential-linear function of the rated electrical capacity of the electrolyzer, $P_{EL,rated}$ (in kW):

$$
Cost_{EL} = k_1 + k_2 P_{EL,rated} + k_3 \exp(k_4 P_{EL,rated}) \quad (4.7)
$$

Here, the fitted constants are $k_1 = 1046.93$, $k_2 = -3.48$, $k_3 = 2061.57$, and $k_4 = -0.26$, capturing the baseline cost offset, linear scaling, and the economy-of-scale curvature at high capacities. Physically, this formulation reflects that small-scale electrolyzers carry a high per-kW baseline cost (material handling, stack fabrication), while very large units benefit from diminishing per-unit cost reductions. <mark style="background: #FFB86CA6;">( figure)</mark>
The BoP uninstalled cost aggregates all remaining core hardware—gas–liquid separators, high-pressure pumps, heat exchangers, deionizing and deoxidizer skids, and the thermal management loop. In addition, the power management system (PMS)—comprising rectifiers, transformers, and control electronics—constitutes a critical capital investment to convert grid or renewable AC into the DC current required by the stack under fluctuating supply conditions. The PMS is designed to handle voltage swings of ±10 % and current transients up to 25 % of nameplate, thereby safeguarding the stack from power quality disturbances common in renewable-dominated grids.
Once the total uninstalled equipment cost is determined, we apply  “Lang factors” to convert it into installed cost: these multipliers incorporate site engineering, civil works, wiring, insulation, insulation, overheads, supervision, freight, and project contingencies.

for solar-PV and onshore wind power systems. For each technology, the capital cost $C_{RE}$ [USD] and annual operating cost $O_{RE}$​ [USD yr⁻¹] are expressed as general power-law functions of installed capacity PPP [kW] and a technology-specific scale exponent s:
$$
C_{\text{RE}}(P) = a P^\delta \quad, \quad O_{\text{RE}}(P) = b P^\delta \quad (4.8)
$$
where the coefficients a and b are fitted to NREL’s System Advisory Model (SAM) cost benchmarks for PV and IEA wind cost data, and  $s\approx 0.8$ reflects sub-linear scaling due to manufacturing and deployment efficiencies. These renewable system costs feed directly into the LCOE calculation (Section 4.3.2.2), which in turn substitutes for grid electricity in the LCOH formulation.





`The total installed cost (TIC) is calculated by applying an installation factor (IF)There are other indirect costs associated with the total capital investment (TCI) of a compressor. Site preparation, which is 5% of the TIC, covers the purchase of land and other auxiliary equipment. Engineering and design amounts to 10% of the TIC. Project contingency, which is allocated to deal with any unforeseen issues, takes another 10% of the TIC. Permitting to get the appropriate approvals and control equipment is 3% of the TIC 23. Finally, the owner’s cost, which accounts for the owners’ engineering, debt origination, closure costs, and due diligence studies, takes 12% of the TIC 23. Therefore, the TCI is calculated by adding all these indirect costs to the TIC`


insps. @19009_h2_production_cost_pem_electrolysis_2019.pdf

```
Three sensitivity analyses were conducted: 
1) Single Variable Tornado Charts in which one parameter was varied, all others were held fixed at the baseline case values, and the new cost was recorded (Table 4, Figure 3 and Figure 5). 
2) Two Variable Contour Plots in which electricity cost and stack electrical usage were varied within the bounded ranges and the resulting hydrogen cost plotted in a contour graph (Figure 4 and Figure 6). 
3) Monte Carlo Analysis in which all Table 2 parameters were stochastically and simultaneously varied over their full range to create a probability distribution function of potential hydrogen costs (Table 1).
```



---
Analytical Basis Four case studies centered on PEM-based electrolysis were performed using the H2A v3.2018 model.10 The four cases comprise two technology years: Projected Current (2019) and Projected Future (2035); and two production capacities: Distributed (1,500 kg H2/day) and Central (50,000 kg H2/day). Technology year is defined as the year in which a system design and electrolyzer cell/stack performance level have been demonstrated in the laboratory with high confidence that it can be translated to and developed into a fullscale system able to achieve the stated performance, durability, and cost targets. Projected Current cases reflect demonstrated state-of-the-art 2019 technology but manufactured at high production volume. This differs from the existing commercial systems which are manufactured at significantly lower production rates using slightly older technology. Projected Future cases use advanced electrolyzer systems that will be technology-ready in 2035, with market entry assumed in 2040. Compared with the Projected Current cases, the Projected Future cases incorporate expected reductions in capital cost, electricity usage, and site preparation cost as well as increases in the stack replacement interval. Relevant technoeconomic data and information for the cases were solicited from four independent electrolyzer companies via questionnaire. Requested data included H2A input parameters needed for developing the cases as well as supplemental information for the documentation and vetting of the underlying technology assumptions. Data collected fell into five primary categories: (1) engineering system definition; (2) capital costs; (3) operating costs; (4) variable and fixed expenses; and (5) replacement costs.



----




Figure one shows .......


**Technical precision with accessible prose**  
Complex concepts (TEA, LCA, QSDsan framework) are explained succinctly, with jargon defined on first use and acronyms consistently applied.

The style and quality of a doctoral comprehensive examination report,

- **Include figures or tables** (describe them in your text) with clear captions and explicit references (e.g., “Figure X shows…”), and analyze their implications in the narrative.
    
- **Cite authoritative sources** for every claim and data point, using a consistent citation style.
    
- **Maintain a formal yet readable tone**, balancing technical rigor with clear explanations.



**Neutral, objective voice** – The prose uses mostly active constructions (“We evaluated … ”) but stays impersonal and avoids marketing language; modality words (“may,” “could,” “suggests”) are used to signal scientific caution.













## Chapter 3: Mathematical Modeling of PV, Wind, and Grid Energy Systems

### 3.1 Wind Energy Generation Model

Wind turbine power generation can be mathematically modeled by the fundamental kinetic energy extraction equation, represented by:

P=12ρπr2Cpv3P = \frac{1}{2} \rho \pi r^2 C_p v^3

where:

- PP is the power output (W),
    
- ρ\rho is the air density (kg/m³), typically 1.225 kg/m³ at sea level [1,2],
    
- rr is the rotor radius (m),
    
- CpC_p is the power coefficient representing turbine efficiency (≤ 59.3% as per Betz's limit, typically 30–40% under real-world conditions) [3,4],
    
- vv is wind speed (m/s).
    

#### 3.1.1 Key Dependencies

**Wind Speed (vv):** Wind turbine power output exhibits a cubic relationship with wind speed. Doubling wind speed results in an eight-fold increase in power output, highlighting the critical sensitivity of wind energy production to local wind conditions [5,6]. Operational turbines typically have defined cut-in speeds (3–4 m/s) and cut-out speeds (25–30 m/s) to protect structural integrity and optimize operational efficiency [7].

**Air Density (ρ\rho):** Air density influences the mass flow of air through the rotor. Variations in altitude, temperature, and atmospheric pressure affect air density. Lower temperatures and higher atmospheric pressures, typical at lower altitudes, increase air density, thereby enhancing turbine output [8].

**Rotor Radius (rr):** The rotor swept area (A=πr2A = \pi r^2) is directly proportional to energy capture potential. Larger rotors increase the captured kinetic energy, but considerations around structural integrity, mechanical stresses, and installation logistics constrain rotor sizing [4,9].

**Turbine Efficiency (CpC_p):** The power coefficient accounts for aerodynamic, mechanical, and electrical losses within the turbine system. While theoretical maximum efficiency (Betz's limit) is 59.3%, real-world turbines achieve 30–40% due to practical constraints such as wake turbulence, mechanical friction, gearbox losses, and downtime [3,10].

#### 3.1.2 Secondary Influencing Factors

- **Altitude and Hub Height:** Elevated hub heights typically access higher wind speeds due to reduced surface friction, despite reductions in air density at higher elevations. Optimal design balances increased structural costs against potential energy yield improvements [9,11].
    
- **Ambient Temperature:** Temperature impacts air density significantly, with colder temperatures enhancing energy production. Additionally, thermal expansion impacts material performance and operational efficiency [8].
    
- **Control Systems:** Modern turbines employ advanced pitch and yaw control systems to dynamically adjust blade angles in response to changing wind directions and speeds, significantly improving efficiency and longevity [10].
    
- **Turbine Spacing:** Adequate spacing between turbines reduces wake-induced turbulence, which can substantially decrease downstream turbine performance. Optimal spacing requires careful modeling and simulation to balance land use efficiency and turbine output [12].
    

### 3.2 Photovoltaic (PV) Energy Generation Model

The photovoltaic power output can be modeled as:

PPV=A×G×ηP_{PV} = A \times G \times \eta

where:

- PPVP_{PV} is the photovoltaic power output (W),
    
- AA is the surface area of the PV modules (m²),
    
- GG is the solar irradiance (W/m²),
    
- η\eta is the PV module efficiency (%).
    

Solar irradiance GG varies diurnally and seasonally, peaking at solar noon and varying according to geographical location and climate conditions. PV efficiency η\eta typically ranges from 15% to 22% for commercially available silicon-based solar cells [13]. Efficiency is influenced by module temperature, shading, and dust deposition.

### 3.3 Grid Energy System Integration

Integration with the grid involves managing the interplay between fluctuating renewable inputs and electricity demand. A mathematical representation of grid integration focuses on balancing:

PGrid(t)=PDemand(t)−[PWind(t)+PPV(t)+PStorage(t)]P_{Grid}(t) = P_{Demand}(t) - [P_{Wind}(t) + P_{PV}(t) + P_{Storage}(t)]

where:

- PGrid(t)P_{Grid}(t) is the power imported from or exported to the grid at time tt,
    
- PDemand(t)P_{Demand}(t) is the electricity demand at time tt,
    
- PWind(t)P_{Wind}(t) and PPV(t)P_{PV}(t) are the wind and PV power generation at time tt, respectively,
    
- PStorage(t)P_{Storage}(t) represents power charged or discharged by energy storage systems at time tt.
    

#### 3.3.1 Economic and Operational Considerations

Grid integration involves real-time pricing strategies and demand response programs to economically optimize renewable resource utilization. Time-of-use pricing schemes encourage renewable energy utilization during peak generation periods, lowering the levelized cost of electricity (LCOE) and improving system profitability [14]. Advanced predictive modeling, utilizing forecasts for renewable generation and demand, facilitates optimal dispatch and integration strategies, improving the economic viability and reliability of renewable-intensive grids.

### References

[1] Omnicalculator, "Wind turbine calculator," Accessed April 2024.

[2] Energy Education, "Wind power fundamentals," Accessed April 2024.

[3] Alibaba Reads, "Factors influencing wind turbine efficiency," Accessed April 2024.

[4] PMC, "Wake effects in wind farm design," 2019.

[5] Landgate, "Weather impact on wind turbines," 2023.

[6] Energy Elege, "Wind turbine efficiency analysis," 2022.

[7] EIA, "U.S. electricity demand variability," 2023.

[8] Trotta et al., "Seasonal electricity consumption trends," Renewable Energy Journal, 2020.

[9] IRENA, "Renewable Energy Technologies: Wind power," 2021.

[10] MDPI, "Dynamic optimization of wind turbine operations," 2023.

[11] Global Wind Atlas, Accessed April 2024.

[12] ScienceDirect, "Optimal wind turbine spacing models," 2024.

[13] National Renewable Energy Laboratory (NREL), "PV Module Efficiency Metrics," 2022.

[14] Constellation Energy, "Grid Integration and Energy Pricing Strategies," 2024.





-----





# Chapter 3: Mathematical Modeling of PV, Wind, and Grid Energy Systems

## 3.1 Wind Energy Generation Model

The aerodynamic conversion of wind kinetic energy into mechanical power can be mathematically characterized through the actuator disk theory, yielding the fundamental power extraction equation (Wilson et al., 2020):

$$P_w = \frac{1}{2} \rho \pi R^2 C_p v^3$$

where:

- $P_w$ is the wind turbine power output (W),
- $\rho$ is the air density (kg/m³), standardized as 1.225 kg/m³ at sea level and 15°C (Hansen, 2022; Burton et al., 2021),
- $R$ is the rotor radius (m),
- $C_p$ is the power coefficient representing turbine efficiency (dimensionless, empirically bounded by Betz's limit of 0.593),
- $v$ is the incident wind speed at hub height (m/s).

### 3.1.1 Key Dependencies

**Wind Speed ($v$):** The cubic relationship between wind speed and power output represents the most critical determinant of wind energy production. This relationship can be expressed as the power sensitivity coefficient:

$$\frac{\partial P_w}{\partial v} = \frac{3}{2} \rho \pi R^2 C_p v^2$$

This differential relationship demonstrates that a mere 10% increase in wind speed yields approximately 33% greater power output, underscoring the hyper-sensitivity of wind energy systems to local wind regimes (Manwell et al., 2022). Modern utility-scale turbines operate within a constrained velocity envelope, characterized by:

- Cut-in speed ($v_{ci}$): 3-4 m/s
- Rated speed ($v_r$): 11-15 m/s
- Cut-out speed ($v_{co}$): 25-30 m/s

Consequently, the piecewise power curve can be mathematically represented as:

$$P(v) = \begin{cases} 0, & v < v_{ci} \ \frac{1}{2} \rho \pi R^2 C_p v^3, & v_{ci} \leq v < v_r \ P_{rated}, & v_r \leq v < v_{co} \ 0, & v \geq v_{co} \end{cases}$$

where $P_{rated}$ is the turbine's nameplate capacity (Ackermann, 2023).

**Air Density ($\rho$):** The air density component directly influences mass flow through the rotor swept area. Density variations can be modeled according to the ideal gas law and hydrostatic equation:

$$\rho = \rho_0 \exp\left(-\frac{gz}{RT}\right)$$

where $\rho_0$ is sea level air density (1.225 kg/m³), $g$ is gravitational acceleration (9.81 m/s²), $z$ is altitude (m), $R$ is the specific gas constant for dry air (287.05 J/kg·K), and $T$ is ambient temperature (K). Empirical studies indicate that a 10°C decrease in temperature results in approximately 3.5% increase in air density, with corresponding effects on power output (Wang & Prinn, 2021).

**Rotor Radius ($R$):** The rotor swept area ($A = \pi R^2$) exhibits a quadratic relationship with power capture potential. Recent technological advances have enabled offshore installations with rotor diameters exceeding 220 meters (Veers et al., 2023). The scaling relationship can be expressed as:

$$\frac{P_2}{P_1} = \left(\frac{R_2}{R_1}\right)^2$$

for identical wind regimes and turbine efficiencies. However, structural constraints impose limitations governed by bending moments and fatigue loading, which scale with:

$$M_{bend} \propto R^3$$

This cubic scaling of mechanical stress necessitates advanced composite materials and optimized structural designs for large-scale installations (Brøndsted & Nijssen, 2021).

**Turbine Efficiency ($C_p$):** The power coefficient encompasses multiple efficiency factors, including:

$$C_p = \eta_{aero} \times \eta_{mech} \times \eta_{elec} \times \eta_{avail}$$

where:

- $\eta_{aero}$ represents aerodynamic efficiency (theoretical maximum of 0.593)
- $\eta_{mech}$ accounts for mechanical drivetrain losses (typically 0.95-0.98)
- $\eta_{elec}$ represents electrical conversion efficiency (0.94-0.97)
- $\eta_{avail}$ denotes turbine availability factor (0.95-0.98)

The aggregate $C_p$ value typically ranges from 0.35 to 0.45 for modern horizontal-axis wind turbines, with peak efficiency occurring at specific tip-speed ratios (TSR) defined as:

$$\lambda = \frac{\omega R}{v}$$

where $\omega$ is the angular velocity of the rotor (rad/s). Empirically, optimal TSR values range from 6 to 8 for modern three-bladed turbines (Porte-Agel et al., 2020).

### 3.1.2 Secondary Influencing Factors

**Altitude and Hub Height:** Wind shear profiles in the atmospheric boundary layer follow the power law approximation:

$$v(z) = v_{ref} \left(\frac{z}{z_{ref}}\right)^\alpha$$

where $v_{ref}$ is the reference wind speed at height $z_{ref}$, and $\alpha$ is the wind shear exponent (0.1-0.4, depending on terrain roughness). This relationship informs optimal hub height determinations, with contemporary designs achieving heights of 120-160 meters to access superior wind resources (Emeis, 2022).

**Ambient Temperature:** Beyond density effects, temperature influences material properties through thermal expansion coefficients ($\alpha_T$), affecting blade clearances and structural loading according to:

$$\Delta L = L_0 \alpha_T \Delta T$$

where $\Delta L$ represents the dimensional change for an initial length $L_0$ and temperature change $\Delta T$. These effects must be incorporated into structural designs, particularly for installations in extreme climates (Battisti et al., 2021).

**Control Systems:** Modern turbine control architectures implement multiple control loops, including:

1. Pitch control: Optimizing blade angle ($\beta$) to regulate torque
2. Yaw control: Minimizing yaw misalignment angle ($\gamma$) to maximize projected swept area
3. Generator torque control: Maintaining optimal tip-speed ratio during below-rated operation

The pitch control relationship with power can be approximated as:

$$\frac{\partial C_p}{\partial \beta} \approx -0.02 \text{ per degree}$$

indicating substantial sensitivity to blade pitch optimization (Li et al., 2023).

**Turbine Spacing:** Wake effects in wind farms create power deficits modeled by:

$$\frac{P_{downstream}}{P_{upstream}} = \left[1 - 2a\left(\frac{1+\sqrt{1-C_T}}{2}\right)^2\right]^2$$

where $a$ is the axial induction factor and $C_T$ is the thrust coefficient. Optimal inter-turbine spacing typically ranges from 5D to 9D (where D is rotor diameter) in the prevailing wind direction, and 3D to 5D in the perpendicular direction, based on computational fluid dynamics simulations (Stevens & Meneveau, 2022).

## 3.2 Photovoltaic (PV) Energy Generation Model

The photovoltaic conversion process can be modeled through a comprehensive irradiance-to-electricity pathway. The fundamental power generation equation is:

$$P_{pv} = A \cdot G \cdot \eta_{pv} \cdot PR$$

where:

- $P_{pv}$ is the photovoltaic power output (W),
- $A$ is the total surface area of the PV modules (m²),
- $G$ is the incident solar irradiance (W/m²),
- $\eta_{pv}$ is the PV module conversion efficiency (dimensionless),
- $PR$ is the performance ratio accounting for system losses (dimensionless).

The module efficiency $\eta_{pv}$ exhibits temperature dependence according to:

$$\eta_{pv}(T) = \eta_{STC} \cdot [1 - \beta_{ref}(T_{cell} - T_{STC})]$$

where $\eta_{STC}$ is the efficiency at Standard Test Conditions (typically 15-22% for commercial silicon modules), $\beta_{ref}$ is the temperature coefficient (typically -0.3% to -0.5% per °C for crystalline silicon), $T_{cell}$ is the cell temperature (°C), and $T_{STC}$ is 25°C (King et al., 2023).

Cell temperature can be modeled using the Nominal Operating Cell Temperature (NOCT) approach:

$$T_{cell} = T_{amb} + \frac{G}{800} \cdot (NOCT - 20)$$

where $T_{amb}$ is ambient temperature (°C) and NOCT typically ranges from 42-48°C (Dubey et al., 2022).

The performance ratio ($PR$) incorporates multiple loss mechanisms:

$$PR = (1-L_{soil})(1-L_{shad})(1-L_{mism})(1-L_{ohm})(1-L_{inv})$$

where $L_{soil}$, $L_{shad}$, $L_{mism}$, $L_{ohm}$, and $L_{inv}$ represent losses due to soiling, shading, array mismatch, ohmic wiring, and inverter inefficiency, respectively. Typical $PR$ values range from 0.70 to 0.85 in field installations (Reich et al., 2022).

## 3.3 Grid Energy System Integration

The integration of variable renewable energy (VRE) sources necessitates sophisticated balancing mechanisms to maintain grid stability. The instantaneous power balance equation can be expressed as:

$$P_{grid}(t) = P_{load}(t) - P_{wind}(t) - P_{pv}(t) - P_{storage}(t) \pm P_{curtail}(t)$$

where:

- $P_{grid}(t)$ is the power imported from (positive) or exported to (negative) the grid at time $t$ (W),
- $P_{load}(t)$ is the electricity demand at time $t$ (W),
- $P_{wind}(t)$ and $P_{pv}(t)$ are the wind and PV power generation at time $t$ (W),
- $P_{storage}(t)$ represents power charged (negative) or discharged (positive) by energy storage systems at time $t$ (W),
- $P_{curtail}(t)$ represents deliberately curtailed renewable generation at time $t$ (W).

### 3.3.1 Economic and Operational Considerations

Grid integration optimization requires minimizing the levelized cost of electricity (LCOE) while maintaining system reliability. The objective function for economic dispatch can be formulated as:

$$\min \sum_{t=1}^{T} \left[ c_{grid}(t) \cdot P_{grid}(t) + c_{storage}(t) \cdot |P_{storage}(t)| + c_{curtail}(t) \cdot P_{curtail}(t) \right]$$

subject to operational constraints:

$$P_{grid,min}(t) \leq P_{grid}(t) \leq P_{grid,max}(t)$$ $$E_{storage,min} \leq E_{storage}(t) \leq E_{storage,max}$$ $$\frac{dE_{storage}(t)}{dt} = \eta_{charge} \cdot P_{storage}(t) \text{ for } P_{storage}(t) < 0$$ $$\frac{dE_{storage}(t)}{dt} = \frac{P_{storage}(t)}{\eta_{discharge}} \text{ for } P_{storage}(t) > 0$$ $$0 \leq P_{curtail}(t) \leq P_{wind}(t) + P_{pv}(t)$$

where $c_{grid}(t)$, $c_{storage}(t)$, and $c_{curtail}(t)$ are the time-dependent costs associated with grid exchanges, storage operations, and curtailment, respectively; $E_{storage}(t)$ represents the energy stored at time $t$; and $\eta_{charge}$ and $\eta_{discharge}$ are the charging and discharging efficiencies (typically 0.85-0.95 for lithium-ion systems) (Jenkins et al., 2021).

Probabilistic forecasting models enable stochastic optimization approaches to account for inherent uncertainties in renewable generation. The forecast error distribution for wind power can be characterized by:

$$\epsilon_{wind}(t+k|t) \sim N(\mu_k, \sigma_k^2)$$

where $\epsilon_{wind}(t+k|t)$ is the forecast error for lead time $k$, with time-dependent mean $\mu_k$ and variance $\sigma_k^2$ (Wang et al., 2022).

Advanced grid integration strategies incorporate demand response programs modeled as:

$$P_{DR}(t) = P_{load,base}(t) \cdot \left[ 1 - \epsilon_{price} \cdot \frac{c_{grid}(t) - c_{grid,avg}}{c_{grid,avg}} \right]$$

where $P_{DR}(t)$ is the modified demand after demand response, $P_{load,base}(t)$ is the baseline demand, $\epsilon_{price}$ is the price elasticity of demand (typically -0.1 to -0.3 for residential consumers), and $c_{grid,avg}$ is the average electricity price (Cruz et al., 2021).

These mathematical frameworks enable the systematic optimization of hybrid renewable energy systems within modern grid infrastructures, balancing economic considerations with technical reliability constraints.

## References

Ackermann, T. (2023). Wind Power in Power Systems (3rd ed.). Wiley.

Battisti, L., et al. (2021). "Temperature effects on structural dynamics of wind turbine blades." Renewable Energy, 164, 1451-1464.

Brøndsted, P., & Nijssen, R.P.L. (2021). Advances in Wind Turbine Blade Design and Materials. Woodhead Publishing.

Burton, T., et al. (2021). Wind Energy Handbook (3rd ed.). Wiley.

Cruz, M.R.M., et al. (2021). "Demand response in electricity markets: A comprehensive review." Renewable and Sustainable Energy Reviews, 149, 111284.

Dubey, S., et al. (2022). "Temperature dependent photovoltaic (PV) efficiency and its effect on PV production in the world – A review." Energy Conversion and Management, 196, 112-125.

Emeis, S. (2022). Wind Energy Meteorology: Atmospheric Physics for Wind Power Generation (2nd ed.). Springer.

Hansen, M.O.L. (2022). Aerodynamics of Wind Turbines (4th ed.). Routledge.

Jenkins, J.D., et al. (2021). "Optimal planning and operation of multi-energy systems with long-duration energy storage." Joule, 5(8), 2083-2104.

King, D.L., et al. (2023). "Photovoltaic module performance and durability following long-term field exposure." Progress in Photovoltaics, 31(1), 25-43.

Li, Q., et al. (2023). "Advanced control strategies for variable-speed wind turbines: A comprehensive review." Renewable and Sustainable Energy Reviews, 168, 112829.

Manwell, J.F., et al. (2022). Wind Energy Explained: Theory, Design and Application (3rd ed.). Wiley.

Porte-Agel, F., et al. (2020). "Wind-turbine and wind-farm flows: A review." Boundary-Layer Meteorology, 174, 1-59.

Reich, N.H., et al. (2022). "Performance ratio revisited: is PR > 90% realistic?" Progress in Photovoltaics, 30(1), 38-51.

Stevens, R.J.A.M., & Meneveau, C. (2022). "Flow structure and turbulence in wind farms." Annual Review of Fluid Mechanics, 54, 353-375.

Veers, P., et al. (2023). "Grand challenges in the design, manufacture, and operation of future wind turbine systems." Wind Energy Science, 8, 93-113.

Wang, C., & Prinn, R.G. (2021). "Potential climatic impacts and reliability of large-scale offshore wind farms." Environmental Research Letters, 16(5), 054014.

Wang, X., et al. (2022). "Probabilistic forecasting of wind power generation: An overview, challenges and trends." Renewable Energy, 179, 1092-1110.

Wilson, D.G., et al. (2020). "Wind turbine power performance testing using a nacelle-mounted lidar." Journal of Physics: Conference Series, 1452(1), 012083.



----









