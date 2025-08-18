


Checklist for consistency
- [ ] Basis to write up
- [ ] catalyst loading.


# Appendix A: Design Parameters

### Cell design parameters

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
| The membrane thickness, (microns)     | 178 \| 114                             |
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


Table S3: Values of 

Reference for Current Density and Activation Energy for Anode and cathode half-cells at 318 k()
insp: @chungDesignSpacePEM2024

| Variable                             | Value                 | Units    | Reference                                                                                                |
| ------------------------------------ | --------------------- | -------- | -------------------------------------------------------------------------------------------------------- |
| $i_{0, \text{cathode}}^{\text{ref}}$ | $0.75 \times 10^{-3}$ | A/cm$^2$ | @garcia-valverdeSimplePEMWater2012 , @carmoComprehensiveReviewPEM2013 ,  @coutanceauChapter3Hydrogen2018 |
| $E_{\text{act, cathode}}$            | 30,000                | J/mol    | @heHydrogenEvolutionPt1112017                                                                            |
| $i_{0, \text{anode}}^{\text{ref}}$   | $1.0 \times 10^{-7}$  | A/cm$^2$ | @garcia-valverdeSimplePEMWater2012  , @carmoComprehensiveReviewPEM2013 , @coutanceauChapter3Hydrogen2018 |
| $E_{\text{act, anode}}$              | 90,000                | J/mol    | @garcia-valverdeSimplePEMWater2012   18 @suermannComparingKineticActivation2018                          |
Tables
References for current density and activation energy for OER and ERR


| $i_{0,a}$ (A/cm$^2$)  | $i_{0,c}$ (A/cm$^2$) | Anode and cathode catalyst | References                                 |
| --------------------- | -------------------- | -------------------------- | ------------------------------------------ |
| $1.0 \times 10^{-12}$ | $1.0 \times 10^{-3}$ | Pt–Ir anode<br>Pt cathode  | @choiSimpleModelSolid2004                  |
| $1.65 \times 10^{-8}$ | $9.0 \times 10^{-2}$ | Pt–Ir anode<br>Pt cathode  | @harrisonSemiempiricalModelDetermining2005 |
| $1.0 \times 10^{-7}$  | $1.0 \times 10^{-3}$ | Pt–Ir anode<br>Pt cathode  | @marangioDirectHighPressure2009            |



Validation data

@debeInitialPerformanceDurability2012

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


### Exchange Current Densities (Table 1)

| Catalyst                | $j_{0,a}$ (A cm⁻²) | $j_{0,c}$ (A cm⁻²) | Source               |
| ----------------------- | ------------------ | ------------------ | -------------------- |
| Pt–Ir anode, Pt cathode | 1.0 × 10⁻¹²        | 1.0 × 10⁻³         | Choi et al. [17]     |
| Pt–Ir anode, Pt cathode | 1.65 × 10⁻⁸        | 9.0 × 10⁻²         | Harrison et al. [30] |
| Pt–Ir anode, Pt cathode | 1.0 × 10⁻⁷         | 1.0 × 10⁻³         | Marangio et al. [22] |


Model Parameterization 


| Parameter, Unit                                | Symbol                       | Value                               |
| ---------------------------------------------- | ---------------------------- | ----------------------------------- |
| Faraday constant, C mol⁻¹                      | $F$                          | 96485.0                             |
| Gas constant, J mol⁻¹ K⁻¹                      | $R$                          | 8.314                               |
| Temperature, K                                 | $T$                          | 353.15                              |
| Pressure (anode / cathode), atm                | $P_a$, $P_c$                 | 1.0 / 13.6                          |
| Max current density, A cm⁻²                    | $j_{\max}$                   | 2.0                                 |
| Exchange current density, A cm⁻²               | $j_{0,a}$, $j_{0,c}$         | 2.0 × 10⁻⁶ / 1.0 × 10⁻¹             |
| Electrode thickness, µm                        | $d_e$                        | 200                                 |
| Porosity                                       | $\varepsilon$                | 0.30                                |
| Membrane thickness, µm                         | $d_m$                        | 178                                 |
| Titanium resistivity, Ω cm                     | $\rho_{\rm Ti}$              | 5.0 × 10⁻³                          |
| Carbon-paper resistivity, Ω cm                 | $\rho_{\rm CP}$              | 80.0 × 10⁻³                         |
| Charge transfer coeffs.                        | $\alpha_a$, $\alpha_c$       | 2.0 / 0.5                           |
| Water viscosity, N s cm⁻²                      | $\mu_{H_2O}$                 | 3.55 × 10⁻⁸                         |
| Water density, g cm⁻³                          | $\rho_{H_2O}$                | 1.0                                 |
| Channel dims., mm                              | $L_{ab}, L_{bc}, L_{ik}$     | 2.0, 1.0, 1.0                       |
| MEA area, cm²                                  | $A$                          | 5.0                                 |
| Membrane humidification                        | $\ell$                       | 22                                  |
| GDL porosity (ref)                             | $\varepsilon_p$              | 0.11                                |
| Empirical coeffs. (diffusion)                  | $a, b$                       | 0.785, 2.334                        |
| Critical pressures, atm                        | $P_{cr}$ (H₂O, O₂, H₂)       | 218.3, 49.7, 12.8                   |
| Critical temps., K                             | $T_{cr}$ (H₂O, O₂, H₂)       | 647.3, 154.4, 33.3                  |
| Molar masses, g mol⁻¹                          | $M_m$ (H₂O, O₂, H₂)          | 18, 32, 2                           |
| Electro-osmotic drag coeff. , mol H₂O mol⁻¹ e⁻ | $n_d$                        | (model-fitted)                      |
| Water diffusivity, cm² s⁻¹                     | $D_w$                        | (model-fitted)                      |
| Darcy permeability, m²                         | $K_{\rm darcy}$              | (model-fitted)                      |
| Ref. concentrations, mol cm⁻³                  | $C_{O_2,m}^0$, $C_{H_2,m}^0$ | (model-fitted)                      |
| Porous-electrode diffusivity, m² s⁻¹           | $D_{\rm eff}$                | (function of $\varepsilon, T$ etc.) |








## System Design Parameters

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




# EFFECTIVE CAPACITY FACTOR OF SYSTEM

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

# LCOE FOR ENERGY SYSTEMS

| Parameter                        | Value          | Unit      | Notes                        |
| -------------------------------- | -------------- | --------- | ---------------------------- |
| Energy mix                       | Wind           |           |                              |
| Total Capacity                   | 10             | MW        |                              |
| Total CF_RE                      | 0.3400         |           | use the pink colored instead |
| Total CapEx                      | $17,758,000.00 | $         |                              |
| Total RE OpEx                    | $442,000.00    | $/yr      |                              |
| hours                            | $8,760.00      | hr        |                              |
| Annual Production rate, E_annual | $29,784.00     | MWh       |                              |
| discount rate, r                 | 0.12           |           |                              |
| life of system, n                | 25             | year      |                              |
| CRF                              | 0.2914         |           |                              |
| Levelised Fixed Cost, LFC        | $173.76        | $/MWh     |                              |
| Marginal Cost                    | $14.84         | $/MWh     |                              |
| **LCOE**                         | **$188.60**    | **$/MWh** |                              |
|                                  | **$0.19**      | **$/kWh** |                              |









## Design Parameters and assumptions for Wind Energy system

Design parames

# Wind power modeling.

| Parameter                                                       | Symbol          | Value       | Unit             |
| --------------------------------------------------------------- | --------------- | ----------- | ---------------- |
| Power output capacity                                           | P_wt            | 0.000756712 | MW               |
| air density (1.23 kg/m3)                                        | $\rho$          | 1.225       | kg/m3            |
| Specific Wind turbine's blades swept area (m2)/MW               | A               | 3,000.00    | m2/MW            |
| P_rated                                                         | P_rated         | 1           | MW               |
| $\eta$WT is wind turbine's mechanical (drive train and gearbox) | $\eta$WT        | 1           |                  |
| wind scale parameter(m/s), \| base weibull scale                | $\lambda\_base$ | 7           | m/s              |
| wind shape parameter \| k_shape                                 | k_shape         | 2           |                  |
| Wind velocity                                                   |                 | 1.009751488 | m/s              |
| Cp is the power coefficient of the wind turbine, <0.59          | Cp              | 0.4         |                  |
| dynamic Cp($\lambda,\beta$)                                     |                 | 0.436011916 |                  |
| the tip speed ratio ($\lambda$) (0-15),                         | $\lambda$       | 10          |                  |
| degree of pitch angle ($\beta$) (0-45 degrees angle)            | $\beta$ k       | 2           |                  |
| effective tip speed                                             | $\lambda$i      | 10.15611111 |                  |
| Wind power curve constants                                      | c1              | 0.5176      |                  |
|                                                                 | c2              | 116         |                  |
|                                                                 | c3              | 0.4         |                  |
|                                                                 | c4              | 5           |                  |
|                                                                 | c5              | 21          |                  |
|                                                                 | c6              | 0.0068      |                  |
| hour of day(0-23)                                               |                 | 12          | hour             |
| day of the year                                                 |                 | 150         | day number       |
| A_season , seasonal amplitude                                   | As              | 0.2         |                  |
| $\phi\_season$ \| day of the year                               | $\phi\_season$  | 355         | day of year      |
| A_diurnal                                                       |                 | 0.15        |                  |
| P_rated                                                         |                 |             |                  |
| $\phi\_diurnal$ \| hour of the day                              | $\phi\_diurnal$ | 6           | hours of the day |
| S_season                                                        | S_season        | 1.075541593 |                  |
| S-diurnal                                                       | S-diurnal       | 1.15        |                  |
| $\lambda\_eff$                                                  | $\lambda\_eff$  | 8.658109824 |                  |
| **rating and key wind speeds**                                  |                 |             |                  |
| V_cut-in                                                        | V_c             | 3           |                  |
| V_r                                                             | V_r             | 13          |                  |
| V_cut-out                                                       | V_f             | 25          |                  |
| Wind speed (hub height) effect                                  | h               |             |                  |
|                                                                 | ho              |             |                  |
|                                                                 | v_o             |             |                  |

polynomial cp curves  Power coefficient curves in wind turbines @castilloComparisonPowerCoefficients2023

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



## Design Parameters and assumptions for PV Energy system




PV Energy system 

# PV Model

| Parameter                                                                                           | Symbol                    | Value       | Unit                | Notes |
| --------------------------------------------------------------------------------------------------- | ------------------------- | ----------- | ------------------- | ----- |
| PV Power produced                                                                                   | P_PV,h y                  | 0.87999265  | MW                  |       |
| PV plant-rated power (kW)                                                                           | P_PV,rated                | 1           | MW                  |       |
| the derating factor of the PV module which increases annually, (eg soiling)                         | f_pv \| f_derPV,y         | 0.9         |                     |       |
| G_max Clear sky peak irradiance (W/m2) \| global horizontal irradiance                              | G_max \| GHI              | 1000        | W/m2                |       |
| hour of day (0-23)                                                                                  | d                         | 12          | hour                |       |
| index day of the year                                                                               | d                         | 150         | day number          |       |
| latitude of the considered location                                                                 | $\phi$                    | 40          | sites latitude +pos |       |
| the declination angle                                                                               | $\delta$                  | 21.75085248 |                     |       |
| the elevation angle                                                                                 | alpha \| sigma            | 71.75085248 |                     |       |
| the tilt angle of the PV module                                                                     | theta                     | 25          |                     |       |
| GHI correction factor for GTI \| Tilted plane factor                                                |                           | 1.045659418 |                     |       |
| GHI time day effect                                                                                 |                           | 1022.060886 |                     |       |
| (global tilted irradiance) is the solar irradiation intensity (kW/m2) falls to the tilted PV module | G_o (irradiance) \| GTI_h | 1068.727592 |                     |       |
| STC irradiance. \| solar irradiance under standard test condition (STC), i.e., 1 kW/m2,             | G_tsc                     | 1000        | W/m2                |       |
| the coefficient of temperature affecting PV output power (%/oC)                                     | K_p                       | -0.0035     |                     |       |
| the constant of module temperature in STC (25oC)                                                    | T_stc                     | 25          | oC                  |       |
| losses that occurred in the PV plant as the sum of losses due to PV inverter,                       | PP_losses                 |             |                     |       |
| Nominal Operating cell Temp oC                                                                      | NOCT                      | 45          | oC                  |       |
| Annual Mean Temperature                                                                             | T_mean                    | 15          | oC                  |       |
| Seasonal amp. Of ambient temp (o C), Amplified                                                      | T_amp                     | 10          | oC                  |       |
| Real PV cell module temperature (C),                                                                | T_pv-cell \| T_pv^h       | 49.31676207 | oC                  |       |
| Ambient temperature                                                                                 | T_amb                     | 15.91902483 | oC                  |       |




# Appendix B:  Economic and system Parameters 


## Economic Parameters and Assumptions



Baseline Design Parameters: Technical Operating Parameters and Specifications and Financial Input Values

| Parameters                                                             | Input                              |
| ---------------------------------------------------------------------- | ---------------------------------- |
| Production capacity, kg/day                                            | 10,000                             |
| Start-up Year                                                          | 2024                               |
| Total Uninstalled Capital ($/kW)                                       | $995                               |
| Total Electrical Usage (kWh/kg)                                        | 54.3 [% LHV] (61%) (% HHV) (72.6%) |
| Stack Electrical Usage (kWh/kg)                                        | 49 [% LHV] (68%) (% HHV) (80%)     |
| BoP Electrical Usage (kWh/kg)                                          | 5.04                               |
| Stack Current Density (A/cm²)                                          | 2                                  |
| Cell Voltage (V)                                                       | 1.8                                |
| Specific Electrolyzer Power Consumption at Peak Production (kWh/kg H₂) | 49                                 |
| Outlet Pressure from Electrolyzer (bar)                                | 30                                 |
| Installation Cost (% of uninstalled capital cost)                      | 12%                                |
| Stack Replacement Interval (years)                                     | 10                                 |
| Stack Replacement Cost Percentage (% of installed capital cost)        | 15%                                |
| Plant Life (years)                                                     | 20                                 |
| Stack Degradation Rate (mV/khrs)                                       | 1.5                                |
| Cell Active Area (cm²)                                                 | 877                                |
| Capacity Factor (%)                                                    | 90%                                |
| Tax rate                                                               | 27%                                |
| Plant Life (years)                                                     | 20                                 |
| Depreciation Type                                                      | MACRS                              |
| Depreciation Schedule Length (years)                                   | 3                                  |
| % of Capital Spent in 1ˢᵗ, 2ⁿᵈ, 3ʳᵈ year of construction               | 10%, 60%, 30%                      |
| % of Fixed and Variable Operating Cost During Start-up                 | 75%, 50%                           |
Modified Accelerated Cost Recovery System (MACRS).



| Parameter                                        | Baseline value                                    | Rationale / source                                                                                                                                                                                                                                                                                              |
| ------------------------------------------------ | ------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Discounted cash-flow rate of return (DCFROR)** | 10 % real (≈ 12 % nominal)                        | Matches hurdle rates reported by independent-power producers and hydrogen developers in 2024 investor filings.                                                                                                                                                                                                  |
| **Weighted-average cost of capital (WACC)**      | 7 % nominal                                       | DOE H2FAST/H2A-Lite default for mature projects ([docs.nrel.gov](https://docs.nrel.gov/docs/fy24osti/90103.pdf?utm_source=chatgpt.com "[PDF] Capital Structure for Techno-Economic Analysis of Hydrogen Projects")).                                                                                            |
| **Depreciation**                                 | 20-year straight line (MACRS sensitivity in §4.5) | Simplicity for cross-scenario comparison.                                                                                                                                                                                                                                                                       |
| **Corporate tax rate**                           | 21 % U.S. federal                                 | Current statutory rate.                                                                                                                                                                                                                                                                                         |
| **Plant life**                                   | 20 years                                          | Aligns with membrane warranty and power-purchase-agreement tenors.                                                                                                                                                                                                                                              |
| **Electricity price**                            | $0.04–0.10 kWh⁻¹ (scenario range)                 | Covers bulk-renewable PPAs through to commercial-tariff retail rates.                                                                                                                                                                                                                                           |
| **Deionized-water cost**                         | $0.20 m³⁻¹                                        | Municipal‐supply average for Northeastern U.S. sites.                                                                                                                                                                                                                                                           |
| **Stack replacement**                            | Every 7 years at $450 kW⁻¹ (installed)            | Based on 2019 DOE PEM cost record, escalated to 2025 dollars ([hydrogen.energy.gov](https://www.hydrogen.energy.gov/docs/hydrogenprogramlibraries/pdfs/19009_h2_production_cost_pem_electrolysis_2019.pdf?Status=Master&utm_source=chatgpt.com "[PDF] Hydrogen Production Cost from PEM Electrolysis - 2019")). |


## Capex Cost

Fixed direct Capital cost   :  $ 20,440,000.00

#### Indirect Depreciable Capital Costs

| Description                                                              | Reference Year (2023) Dollars | Notes                                                                                                                                                              |
| ------------------------------------------------------------------------ | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Site preparation ($) and construction costs)                             | $3,852,940.00                 | H2A Default for 1500kg/day. Site Prep Using AACE* cost categories for a ">150psi >400F Gas Process". Foundation: (1% of process cost); Materials: 5% Labor: 6.65%. |
| Engineering & design ($)                                                 | $60,249.30                    | Miscellaneous (% of process cost); Materials: 4% Labor: 3.2%                                                                                                       |
| Process contingency ($)                                                  | $0.00                         |                                                                                                                                                                    |
| Project contingency ($)                                                  | $3,066,000.00                 | 15% direct capital                                                                                                                                                 |
| Other (Depreciable) capital) ($)                                         | $0.00                         |                                                                                                                                                                    |
| One-time Licensing Fees ($)                                              | $0.00                         | most licensing fees are not one time, but renewable                                                                                                                |
| Up-Front Permitting Costs ($) (legal and contractors fees included here) | $36,149.50                    | H2A Default for 1500kg/day FC Prod.: $30,000. Includes multiple visits to multiple agencies and a public review/ comment process.                                  |
| **Total Indirect Capital (TIC)**                                         | **$7,015,338.80**             |                                                                                                                                                                    |
| **Total Depreciable Capital Costs/ Fixed Capital Invest. (FCI)**         | **$27,455,338.80**            |                                                                                                                                                                    |

#### Non-Depreciable Capital Costs

| Description                             | Reference Year (2023) Dollars | Notes                                                                                                                                                                                          |
| --------------------------------------- | ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Cost of land ($/m2)                     | $1,071.94                     | average for factory, Turner and Townsend n.d. http://www.turnerandtownsend.com/ICC_Survey_Brochure_final_6MGIa.pdf file)                                                                       |
| Land required (m2)                      | $1,310.64                     | upmetrics (https://upmetrics.co/) suggests a range of 4,300 to 10,000 square feet for a small station, and 15,000 to 35,000 square feet for one with a convenience store. 1ft to meters 0.3048 |
| Land Cost ($)                           |                               |                                                                                                                                                                                                |
| Other non depreciable capital costs     | -$1,404,925.76                |                                                                                                                                                                                                |
| **Total Non-Depreciable Capital Costs** | **$0.00**                     |                                                                                                                                                                                                |

#### Working Capital

| Description     | Reference Year (2023) Dollars | Notes      |
| --------------- | ----------------------------- | ---------- |
| Working Capital | $4,962,494.72                 | 15% of TCI |

#### Total Capital Costs

| Description | Value |
|---|---|
| Total Capital Costs | $27,455,338.88 |



## Operating Cost

### Fixed Operational cost

| Category                                                                 | Reference Year (2023) Dollars | Notes                                                                                                                                                            |
| ------------------------------------------------------------------------ | ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Fixed Operating Costs**                                                |                               |                                                                                                                                                                  |
| **Direct fixed**                                                         |                               |                                                                                                                                                                  |
| Total plant staff (number of FTEs employed by plant)                     | 10                            | 8-hour base shift, 3 shifts per day                                                                                                                              |
| Burdened labor cost, including overhead ($/man-hr)                       | $31.78                        | $31.29 hourly wage per worker, NREL 2019 (Note: Calculation is slightly off in original image for $31.78, should be $31.78 based on 24 * 1.324).                 |
| Labor cost, $/year                                                       | $650,895.44                   |                                                                                                                                                                  |
| G&A rate (% of labor cost)                                               |                               | Using H2A default                                                                                                                                                |
| G&A ($/year)                                                             | $130,179.09                   | Using H2A default                                                                                                                                                |
|                                                                          | $781,074.52                   |                                                                                                                                                                  |
| **Indirect fixed**                                                       |                               |                                                                                                                                                                  |
| Licensing, Permits and Fees ($/year)                                     | $3,392.62                     | Using H2A default                                                                                                                                                |
| Property tax and insurance rate (% of total capital investment per year) |                               | Using H2A default                                                                                                                                                |
| Property taxes and insurance ($/year)                                    | $549,106.78                   |                                                                                                                                                                  |
| Rent ($/year)                                                            | $11,557.69                    | Based on $3.23/m2/month and 936 ft2 dedicated for SMR H2 production. (Square footage and rent for H2 dispensing operations are calculated on the Refueling tab.) |
| Material costs for maintenance and repairs ($/year)                      | $0.00                         |                                                                                                                                                                  |
| Production Maintenance and Repairs ($/year)                              | $2,877,428.84                 | 5% of direct captial, Maintenance labor                                                                                                                          |
| Other Fees ($/year)                                                      | $0.00                         | Administrative & support labor                                                                                                                                   |
| Other Fixed O&M Costs ($/year)                                           | $0.00                         |                                                                                                                                                                  |
|                                                                          | $3,441,485.93                 |                                                                                                                                                                  |
| **Total Fixed Operating Costs**                                          | **$4,771,667.29**             | fixed per annum                                                                                                                                                  |

### Variable operational cost

#### Other Materials and Byproducts

| Category     | Demineralized Water | Cooling Water     | Process Water     | Oxygen             |
| ------------ | ------------------- | ----------------- | ----------------- | ------------------ |
| Usage Rate   | 3.534791667 m³/hr   | 3.534791667 l/kg  | 3.534791667 L/kg  | kg H2/hr           |
| Cost (2023)  | $0.00712485 $/gal   | $0.00011335 $/gal | $0.00237495 $/gal | $0.02852109 $/kg   |
| Other Value  | 0.00893             | 0.00893           | 0.00893           |                    |
| Income/Cost  | $1,398,756.67       | $22,252.95        | $466,252.22       | $745,650.31 $/year |
| Oxygen Usage |                     |                   |                   | 3141.58 kg O2/hr   |

#### Energy Feedstocks, Utilities, and Byproducts

| Category                         | Feedstock              | Utility                | Byproduct              |
| -------------------------------- | ---------------------- | ---------------------- | ---------------------- |
| **Feed or Product Type**         | Industrial Electricity | Commercial Electricity | Commercial Electricity |
| **Unit**                         | kWh                    | kWh                    | kWh                    |
| Price Conversion Factor (GJ/kWh) | 0.00360                | 0.0036 (GJ/kWh)        | 0.0036 (GJ/kWh)        |
| Price in Startup Year ($2023)    | $0.07                  | 0.073653701            | 0.073653701            |
| Production (kWh/kg H2)           | 54.27386875 kWh/kg     | 5.04 kWh/kg            | 0 kWh/kg               |
| Price in Startup Year            | $13,861,231.74 $/yr    | $1,287,670.18          | $ -                    |
#### Summary Costs

| Category                                             |     |               |
| ---------------------------------------------------- | --- | ------------- |
| Total Energy Feedstock Cost ($/year)                 | $   | 13,861,231.74 |
| Total Energy Utility Cost ($/year)                   | $   | 1,287,670.18  |
| Total Energy Byproduct Credit ($/year)               | $   | -             |
| Total Non Energy Feedstock ($/year)                  | $   | 1,700,000.00  |
| Total Non Energy Utility and Material Costs ($/year) | $   | 488,505.17    |
| Total Non Energy Byproduct Credits ($/year)          | $   | 745,650       |
| Total Feedstock Costs ($/year)                       | $   | 15,561,231.74 |
| Total Utility Costs ($/year)                         | $   | 2,987,670.18  |
| Total Byproduct Credits ($/year)                     | $   | 0.00          |

*Note: Some values, such as the income in startup year for cooling water and non-energy byproduct credits, are not directly connected in the image as summations but are listed as individual line items.*


#### Other variable operating cost
This covers waste disposal costs, non-feedstock fuels, environmental surcharges, etc. and is estimated at $800/month with 50% being attributed to refueling operations (the other 50% goes to convenience store operations) and is further pro-rata for the fraction of hydrogen dispensers out of total dispensers (3 out of 8 for large stations). Thus for a large station, annual “Other Variable Costs” are $800/month * 12 months/year * 50% fueling fraction * (3 H2 dispensers/8 total dispensers) = $1,800/year.
@penevTechnoEconomicModellingH2A

| Category                                    | Value              | Notes                                 |
| ------------------------------------------- | ------------------ | ------------------------------------- |
| Upstream Carbon Tax ($/year)                | $0                 |                                       |
| Total other Variables (OPEX)                | $25,560            |                                       |
| **Total Variable Operating Costs ($/year)** | **$18,574,500.00** | feedstock + utility + other variables |



---





# Appendix C. Uncertainty and Sensitivity parameters




## Sensitivity Analysis
These are the basis for the univariate sensitivity analysis

| Parameter                      | Unit              | Low                                       | Base                                                                            | High                           | Reference(s)                                                                                                                                                                                                 |
| ------------------------------ | ----------------- | ----------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Installed capital cost         | $ / kW            | $800 / kW (future DOE target)             | $2,000 / kW (current average)                                                   | $3,500 / kW (today’s high end) | DOE target and cost‐reduction projections,                                                                                                                                                                   |
| Uninstalled capital cost       |                   | $250 /kW by 2026 $150 /kW ultimate (2031) | $995/kW  $975–$1,200 /kW (for production rates from ~10 MW/yr up to >100 MW/yr) | $1500 / kW                     | DOE target and cost‐reduction projections,  Badget et al 2024                                                                                                                                                |
| Fixed O&M cost                 | % of cap. cost/yr | 15 % (best‐in‐class estimates)            | 17 % (H2A default)                                                              | 22 % (older systems)           | H2A assumptions,                                                                                                                                                                                             |
| Electricity feedstock cost     | $ / kWh           | $0.03 / kWh (low‐cost renewables)         | $0.07 / kWh (U.S. industrial avg.)                                              | $0.15 / kWh (high‐retail)      | Renewable PPA & EIA data, Hydrogen Program, [U.S. Energy Information Administration](https://www.eia.gov/electricity/monthly/epm_table_grapher.php?t=epmt_5_6_a&utm_source)                                  |
| Deionized water cost           | $ / gal           | $0.002 / gal                              | $0.005 / gal (H2A default)                                                      | $0.010 / gal                   | H2A demineralized‐water input,H2A data, [NREL](https://docs.nrel.gov/docs/fy09osti/44103.pdf?utm_source)                                                                                                     |
| O₂ by-product credit price     | $ / kg            | $0 / kg (no sale) base                    | $0.09 / kg (N. America avg.)                                                    | $0.17 / kg (EU spot)           | Industrial-gas pricing, [businessanalytiq](https://businessanalytiq.com/procurementanalytics/index/oxygen-price-index/?utm_source), H2A database                                                             |
| Corporate tax rate (combined)  | %                 | 21 % (federal only)                       | 25 % (avg. U.S. combined)                                                       | 33 % (high-state)              | Federal & state rates, [PwC Tax Summaries](https://taxsummaries.pwc.com/quick-charts/corporate-income-tax-cit-rates?utm), Tax Foundation                                                                     |
| Electrolyzer energy efficiency | kWh / kg H₂       | 45 kWh/kg (future target)                 | 55 kWh/kg (current state-of-art)                                                | 65 kWh/kg (lower-grade)        | H2A system performance, [Hydrogen Program, OSTI](https://www.hydrogen.energy.gov/docs/hydrogenprogramlibraries/pdfs/19009_h2_production_cost_pem_electrolysis_2019.pdf?Status=Master&utm_source=chatgpt.com) |


### Basis and scenarios for ranges

**Capital cost:** Future DOE targets envision highly scaled manufacturing driving down stack and BoP costs to ≈ $800 /kW, whereas today’s smaller‐volume deployments often see up to $1 500 /kW installed capital costs.

**Fixed O&M:** Lower values reflect optimized maintenance regimes and service contracts; H2A defaults sit at 5 % of capex, while legacy systems can run closer to 8 % annually.

**Electricity cost:** At times of excess renewables, electrolyzers can procure power at $0.03 /kWh; average U.S. industrial rates hover around $0.07 /kWh, and peaking or retail rates can spike past $0.15 /kWh. Also grid electricity tarif may varry largely by region of plant location and ppa. Renewable energy source may also inform cost of electricity.

**Water cost:** Deionized water is a minor contributor, H2A assumes $0.005 /gal—but costs can vary with local treatment infrastructure. 

**O₂ credit:** Many projects don’t monetize oxygen (low end), but large‐scale gas producers can sell at $0.09–0.17 /kg. scenario on the profitabilty and effect of o2 as a viable product.

**Tax rate:** Reflects the 21 % federal corporate rate plus state levies (0–12 %), yielding combined rates from 21 % up to ≈ 33 %. scenario for states with or without state tax.

** SEC, Efficiency:** Modern PEM stacks achieve ≈ 55 kWh/kg H₂ (≈ 65 % LHV efficiency), with R&D targets pushing down toward 45 kWh/kg; less optimal designs may consume 55–65 kWh/kg.

Total non-energy feedstock includes the deionized water.
The uncertainity in non energy feedstock is lower given the deionized water can be processed onsite

HHV of H2 is 39.39 kW/kg for 1 kg of h2
LHV- 33.33kWh

limitation:
scenario for o2 as a viable product. doesn't account for variable bob cost for the oxygen management and processing system.
Tax reate distribuution is unlimited

![[image-47.png]]



| Parameter                       | Unit          | Base (Mid) | Low   | High  |
| ------------------------------- | ------------- | ---------- | ----- | ----- |
| Installed capital cost          | $/kW          | 2 000      | 800   | 3 500 |
| Uninstalled capital cost        | $/kW          | 995        | 250   | 1 500 |
| Fixed O&M                       | % of capex/yr | 17 %       | 15 %  | 22 %  |
| Electricity cost                | $/kWh         | 0.07       | 0.03  | 0.15  |
| Water cost                      | $/gal         | 0.005      | 0.002 | 0.010 |
| Oxygen by-product credit        | $/kg          | 0.09       | 0     | 0.17  |
| Corporate tax rate              | %             | 25 %       | 21 %  | 33 %  |
| Electrolyzer energy consumption | kWh/kg H₂     | 55         | 45    | 65    |

_Table 2: Key cost and performance parameters for sensitivity analysis._




## Montecarlo Analysis

| Parameter       | Min Value    | Max Value      | Mean | Standard dev | Base Value   | Unit          | PDF        | Note                                                    |
| --------------- | ------------ | -------------- | ---- | ------------ | ------------ | ------------- | ---------- | ------------------------------------------------------- |
| Energy cost     | 0.03         | 0.12           | 8.12 | 0.563        | 0.07         | $/kW          | normal     | from eia data in energy feed& utility price tab         |
| Tax rate        | 21           | 30.4           |      |              | 27.00        | %             | Uniform    | Own judgment, Uniform integer                           |
| Discount rate   | 0.08         | 0.15           |      |              | 10.00        | %             | Uniform    |                                                         |
| FCI             | 5,933,166.00 | $41,598,990.00 |      |              | 27,455,338.8 | 27,455,338.88 | Triangular | using the uninstalledcapital cost$/kW for min max       |
| Fixed Opex cost | 4,000,000    | 5,900,000      |      |              | 4,771,667.28 | $/yr          | Triangular | include human workers etc                               |
| Design capacity | 866,875.00   | 3,650,000.00   |      |              | 3,467,500.00 | kg/year       | Triangular | times capacity factors, .25-.35 for PV and wind average |
| Non energy feed | 1,530,000.00 | 1,870,000.00   |      |              | 1,700,000.00 |               | Triangular | 10% uncertainty                                         |
| WC              | 3,969,995.77 | 5,554,993.66   |      |              | 4,962,494.72 |               | Triangular | 20% uncertainty                                         |
| Utility         | 2,590,136.14 | $3,585,204.21  |      |              | 2,987,670.2  | 2,987,670.18  | Triangular | 20% uncertainty                                         |










# Appendix D. Python code and documentation.

﻿




Will get gack to this

| Voltage Efficiency | % LHV         | 70.3% | 70.3% | Equation: 1.23/cell voltage                                                                                                                                                                      |
| ------------------ | ------------- | ----- | ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Dryer Loss         | % of gross H₂ | 3.0%  | 3.0%  | The 3% Dryer loss comes from industry ("3-4%"). The reductions (1.5%) are estimates based on a lower flow of water required for full saturation at higher outlet pressures in future cases.      |
| Permeation Loss    | % of gross H₂ | 0.7%  | 0.7%  | Based on back diffusion model (1.85x10⁻⁷cm²/s back diffusion coefficient): Industry input is 0.7% at 450psi, model says 0.3% at 450psi/3μm thick membrane, 2.02% at 1,000psi/2μm thick membrane. |






---








| Parameter                     | Typical Range / Value | Reference         |
| ----------------------------- | --------------------- | ----------------- |
| **Stack Capital Cost ($/kW)** | 500 – 1,200           | NREL (2024)[3]    |
| **System Efficiency (%)**     | 55 – 70               | NREL (2024)[3][5] |
| **Electricity Price ($/kWh)** | 0.02 – 0.10           | NREL (2024)[3][5] |

| **Operating Temperature (°C)**  | 50 – 80   | NREL (2024)[3][5]      |
| ------------------------------- | --------- | ---------------------- |
| **Operating Pressure (bar)**    | 10 – 30   | NREL (2024)[3][5]      |
| **Membrane Thickness (μm)**     | 100 – 183 | Bayat et al. (2024)[4] |
| **Membrane Conductivity (S/m)** | 5 – 20    | Bayat et al. (2024)[4] |
| **Current Density (A/cm²)**     | 1.0 – 2.0 | NREL (2024)[3][5]      |











## Design Parameters and assumptions for Wind Energy system






## Design Parameters and assumptions for PV Energy system
