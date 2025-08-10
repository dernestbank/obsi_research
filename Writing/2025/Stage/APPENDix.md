


## Appendix A. Model Parameters and Assumptions

This appendix details the parameters, constants, and key assumptions used in the mathematical models for the PEM electrolyzer and the renewable energy systems.
### Table A.1 Cell Design Parameters

**Table A.1** Cell geometry, materials, and operating conditions

| Parameter                                   | Value                                   | Reference / Justification                   |
| ------------------------------------------- | --------------------------------------- | ------------------------------------------- |
| Faraday constant, F (C mol⁻¹)               | 96 485                                  | Standard value                              |
| Gas constant, R (J mol⁻¹ K⁻¹)               | 8.314                                   | Standard value                              |
| Cell temperature, T (K)                     | 333.15                                  |                                             |
| Cell pressure, Pₐ/P𝒸 (bar)                 | 1 (anode) / 30 (cathode)                |                                             |
| Maximum current density, jₘₐₓ (A cm⁻²)      | 2.0                                     | (Marangio et al., 2009)                     |
| Limiting current density, jₗᵢₘ (A cm⁻²)     | 6.0                                     | (Carmo et al., 2013)                        |
| Exchange current density, j₀ₐ/j₀𝒸 (A cm⁻²) | 2.618×10⁻⁶ (anode) / 1.0×10⁻¹ (cathode) |                                             |
| Electrode thickness, dₑ (µm)                | 200                                     |                                             |
| Electrode porosity, ε                       | 0.30                                    |                                             |
| Membrane thickness, dₘ (µm)                 | 178 (Nafion 117)                        |                                             |
| Titanium resistivity, ρₜᵢ (Ω cm)            | 5.0×10⁻³                                |                                             |
| Carbon‐paper resistivity, ρ_{CP} (Ω cm)     | 8.0×10⁻²                                |                                             |
| Charge‐transfer coeffs. αₐ/α𝒸              | 2.0 / 0.5                               | (Carmo et al., 2013)(Marangio et al., 2009) |
| Water viscosity, μ_{H₂O} (N s cm⁻²)         | 3.55×10⁻⁸                               |                                             |
| Water density, ρ_{H₂O} (g cm⁻³)             | 1.0                                     |                                             |
| Active area, A (cm²)                        | 877                                     |                                             |
| Cell voltage, V                             | 1.79                                    |                                             |
| Voltage efficiency                          | 0.69                                    |                                             |
| Power per cell, kW                          | 3.14                                    |                                             |
| Total stack power, kW                       | 19 034                                  |                                             |
| Specific energy consumption, kWh kg⁻¹ H₂    | 49                                      |                                             |
| Anode catalyst loading, mg cm⁻²             | 1.54                                    |                                             |
| Cathode catalyst loading, mg cm⁻²           | 0.40                                    |                                             |

---

### A.2 Electrochemical Kinetic Parameters

**Table A.2** Reference exchange currents and activation energies

|Variable|Value|Units|Reference(s)|
|---|---|---|---|
|i₀, cathode (ref)|0.75×10⁻³|A cm⁻²|García‐Valverde et al. (2012), Carmo et al. (2013), Coutanceau & Barrière (2018)|
|Eₐ𝒸ₜ, cathode|30 000|J mol⁻¹|He et al. (2017)|
|i₀, anode (ref)|1.0×10⁻⁷|A cm⁻²|García‐Valverde et al. (2012), Carmo et al. (2013), Coutanceau & Barrière (2018)|
|Eₐ𝒸ₜ, anode|90 000|J mol⁻¹|García‐Valverde et al. (2012), Suermann et al. (2018)|

---

### A.3 Polarization Curve Validation

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

### A.4 System‐Level Design (H2A Case)

**Table A.4** On‐site vs central plant assumptions

|Parameter|On-site|Central|Basis|
|---|---|---|---|
|H₂ outlet pressure (bar)|30|30|—|
|Cell voltage (V)|1.79|1.79|From cell model|
|Stack energy use (kWh kg⁻¹ H₂)|49.23|49.23|—|
|BOP electrical load (kWh kg⁻¹ H₂)|5.40|5.04|Inverter, dryer, misc. (industry data)|
|Total system energy use (kWh kg⁻¹ H₂)|54.6|54.3|Sum of stack + BOP|

---

### A.5 Renewable Energy Integration Parameters

#### A.5.1 Effective Capacity Factors

**Table A.5** Renewables and storage

|Category|Capacity (MW)|Capacity factor|
|---|--:|--:|
|PV|—|25 %|
|Wind|10|34 %|
|Grid|—|95 %|
|Battery|0|17 %|
|**Hybrid system**|10|34 %|

#### A.5.2 Levelized Cost of Energy (LCOE)

**Table A.6** Wind‐only case

|Parameter|Value|Unit|Notes|
|---|--:|---|---|
|Capacity (MW)|10|MW|—|
|CF_RE|0.3400|—|Capacity factor|
|CapEx|$17 758 000|$|—|
|OpEx (renewables)|$442 000 yr⁻¹|$ yr⁻¹|—|
|Annual output, Eₐₙₙₑₐₗ (MWh)|29 784|MWh yr⁻¹|—|
|Discount rate, r|0.12|—|—|
|Lifetime, n|25|yr|—|
|CRF|0.2914|—|Capital recovery factor|
|Levelized fixed cost, LFC|$173.76 MWh⁻¹|$ MWh⁻¹|—|
|Marginal cost|$14.84 MWh⁻¹|$ MWh⁻¹|—|
|**LCOE**|**$188.60 MWh⁻¹**|**$ MWh⁻¹**|**$0.19 kWh⁻¹**|

#### A.5.3 Wind Turbine Parameters

**Table A.7** Design & Weibull model inputs

|Parameter|Symbol|Value|Unit|
|---|---|--:|--:|
|Air density|ρ|1.225|kg m⁻³|
|Swept area per MW|A|3 000|m² MW⁻¹|
|Rated power|P_{rated}|1|MW|
|Cp (power coefficient)|Cₚ|0.40|—|
|Weibull scale (λ)|λ_base|7|m s⁻¹|
|Weibull shape (k)|k_shape|2|—|
|Cut‐in / rated / cut‐out speeds|V_c/V_r/V_f|3/13/25|m s⁻¹|
|Tip‐speed ratio|λ|10|—|
|Pitch angle|β|2|°|
|Polynomial coefficients c₀–c₁₁|—|as in Castillo et al. (2023)|—|

#### A.5.4 PV System Parameters

**Table A.8** Irradiance, performance, and temperature model

|Parameter|Symbol|Value|Unit|Notes|
|---|---|--:|--:|---|
|PV rated power|P_{PV,rated}|1.0|MW|—|
|Clear‐sky GHI|G_max|1 000|W m⁻²|—|
|Tilt factor|GTI/GHI|1.0457|—|GTI on module plane|
|Derating factor (soiling, etc.)|f_derPV,y|0.90|—|Annual combined losses|
|Cell temperature coefficient|K_p|–0.0035|% °C⁻¹|—|
|NOCT|NOCT|45|°C|Nominal operating cell temp|
|Ambient temperature (annual mean / amp.)|T_mean / T_amp|15 / 10|°C|—|
|Module cell temp.|T_{pv-cell}|49.32|°C|At NOCT conditions|
|Declination, elevation, latitude|δ/σ/φ|21.75/71.75/40|°|—|

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