

To do.
---
- [x] Add more results to abstract
- [x] Add more results o summary.
- [x] Polish methodology
- [x] Correct errors
- [x] Import feedbacks


From Bright
References inconsistent, title names and cases variations, different fonts (times and calibri), spaces on fractions, (a/b not a / b), and worse images. You need the actual data connected data plots so that we can edit, not pictures but graphs

I actually sent an older version
![[Thesis June Draft 06  +lit edit -Bright.docx]]

Font size 11 approved for times new roman? Or 12?

---


Abstract



The global transition to a low-carbon economy hinges on making green hydrogen cost-competitive with fossil fuel-derived alternatives. Proton Exchange Membrane (PEM) electrolysis has evolved as an optimistic solution; however, its adoption is hindered by the high cost of production. While various government incentives can help bridge this gap, long-term viability requires fundamental cost optimization in production technology. This study addresses the critical need for a systematic framework that connects advances in PEM electrolyzer design and electricity source configuration to estimate the levelized cost of hydrogen (LCOH) and net present value (NPV).

The electrochemical module determines the Specific Energy Consumption from the activation, ohmic, and concentration overpotentials based on the PEM design. The Techno-Economic Analysis (TEA) model applies capital-cost scaling with a 20-year discounted cash flow. An hourly resolved energy sub-model simulates photovoltaic, wind, hybrid, and grid-interactive configurations at representative inland locations in the U.S. Great Plains.  

The electrochemical model achieved an RMSE of 32 mV for an LCOH of $7.05/kg, a 32 % IRR and an $77 M NPV at the baseline plant capacity of 10,000 kg H₂/day at 333 K and 30 bar. Sensitivity analyses revealed that the electricity feedstock cost and the equipment cost are the dominant cost drivers. Economies of scale show diminishing returns beyond the baseline capacity, as electricity costs begin to dominate cost levers.  A capacity factor of 40-50 % is found to be optimal for PEM-Renewable Energy (RE) integration. Variability in local RE potential can alter the LCOH by 20–30%. 

This framework recommends that achieving sub-$5/kg of H2 requires technical targets of specific energy consumption ≤ 45 kWh/kg, installed cost ≤ $500/kW, and electricity tariffs ≤ $0.05/kWh, thus guiding R&D and investment toward DOE’s $1–2/kg goals. The modularity of the framework enables future expansion, such as material-substitution sensitivity, surrogate-accelerated optimization, and geospatial LCOH mapping to inform policy and commercial deployment strategies.

----



His recommendation is 35% of text is likely AI


**Model Validation:** Achieved an RMSE of 32 mV against experimental polarization curves

Results summary
1. **Model Validation:** Achieved an RMSE of 32 mV against experimental polarization curves, indicating activation overpotentials dominate
2. **PEM design optimization**: Optimized PEM electrolyser design parameters with current density (1.5-2)A/cm2, thin (< 125 µm) membranes and temperature (60–80 °C) for maximum efficiency  to reach sub-$7 kg⁻¹ LCOH
3. **Techno-economic Baseline Design:** Determined an optimal electrolyzer capacity of 10,000 kg H₂/day at 333 K and 30 bar, assuming an industrial electricity rate of $0.073 /kWh for LCOH of $7 kg⁻¹ LCOH
4. **Cost Drivers:** Identified electricity expenses as the primary cost driver, followed by uninstalled capital costs; secondary drivers include the system’s specific energy consumption (SEC), tax rates, and fixed O&M costs.
5. **Renewables Integration:** Found an optimal capacity factor of 40-50 % for renewable energy supply, balancing intermittency with plant utilization.


----
## 3.0 Description of Framework

To deliver a holistic techno-economic evaluation, we developed an integrated modeling framework that couples a validated physics-based PEM electrolyzer model with a system-level discounted-cash-flow (DCF) cost module. As illustrated in Figure, the primary dependent variables are the specific energy consumption (SEC),  hydrogen output, capacity factor and LCOE. These dynamic variables are influenced by the design parameters from the PEM design module and the RE system module. Capital and operating costs through the economic parameters are annualized and discounted to present value.

The independent variables from the PEM design module, such as the MEA thickness, temperature, and current density, determine the Specific Energy required to produce a unit kilogram of product hydrogen. The sub-system is modeled as an electrochemical reaction, whereas the economic module follows the U.S. Department of Energy's H2A v3.2018 methodology, adopting its structured input–output architecture and default financial parameters. Uninstalled stack and balance-of-plant capital costs are modified to the system size using a curve-fitting function adopted from  Astraini et al. It is assumed that both small, distributed units (1,500 kg/day) and large, centralized plants (50,000 kg/day) share a consistent installation cost basis[74]. We then apply installation lang factors, contingency allowances, and non-depreciable land and permitting charges exactly as defined in H2A framework.

On the operating side, the framework ingests an hourly electricity cost time-series from renewable energy (RE) configurations, solar PV, wind, and hybrid PV–Wind along with grid tariffs. The seasonal and diurnal modulating factors on the irradiance, temperature and wind speed affect the capacity factor of the energy configuration. Hourly RE generation profiles, obtained from National Renewable Energy Laboratory (NREL) data, are passed through a levelized cost of electricity (LCOE) subroutine to produce weighted average power prices under seasonal and diurnal variability. These dynamic power costs, together with fixed O&M, water treatment, and periodic stack replacement charges, drive the annual cash-flow streams.

We determine the levelized cost of hydrogen (LCOH) from the DCF model. Net present value (NPV) and internal rate of return (IRR) are determined from the same cash-flow series. By linking our physics-based SEC and capacity-factor outputs to a configurable RE supply model and a DCF model, this framework allows us to explore how design choices, cell area, catalyst loading, power electronics efficiency, and energy-supply scenarios jointly influence LCOH, NPV, and IRR.

The following sections outline the design basis and assumptions used in this framework to analyze the economies of scale (Section 4.5) and renewable integration strategies (Section 5.2).









---
# Conclusion

## 5.1 Summary of Key Findings

This study delivers a definitive framework for forecasting the true cost and value of grid-connected and renewable-driven PEM hydrogen production. We designed and achieved an RMSE of 32 mV against experimental polarization curves. The activation overpotential dominates total voltage loss, suggesting improvement in catalyst layer design. By embedding our validated physics-based electrolyzer model within an economic discounted-cash-flow methodology, we establish benchmarks: a 10,000 kg/day plant at 333 K and 30 bar, fueled at $0.07/kWh, produces hydrogen at $7/kg with a 32 % IRR and an $77 M NPV.

Through systematic scenario-based sensitivity analysis, we showed that the cost of electricity is the dominant lever, capable of affecting LCOH by up to $2/kg for every $0.04/kWh change in the tariff. Uninstalled capital cost is the next key driver: achieving DoE’s target of $250/kW stack and BoP can lower hydrogen cost by more than $1.50/kg. Efficiency improvements (45–55 kWh/kg SEC) and optimized O&M strategies provide incremental gains, under $0.50/kg in savings, while water and oxygen streams have little economic impact under current market conditions.

Multivariate sensitivity analysis across plant scale and power price shows a clear "sweet spot" for sub-$5 /kg hydrogen: midsize plants (> 8,000 kg/day) paired with electricity tariffs ≤ $0.05/kWh. Financially, plants in this area achieve IRRs above 35% and NPVs in the low hundreds of millions, while smaller or more expensive setups struggle to meet financing requirements. Mid-scale onsite generation (10,000 kg/day) stands out as the most balanced approach: large enough to benefit from scale economies yet sufficiently agile to avoid the market‐sizing risks of mega-scale projects.

Among off-grid options, PV-only systems have the lowest capital expenditure (CAPEX) but a moderate levelized cost of hydrogen (LCOH) because of the low capacity factor; wind offers a higher capacity factor but results in more expensive electricity; PV-wind hybrids provide a compromise. Adding battery storage improves dispatchability but raises LCOH unless electricity-market revenues offset the storage costs. An optimal capacity factor of 40-50 % for renewable energy supply offers a balance of intermittency with plant utilization




---- 

Finals
![[MSc Thesis eqb5538 Ernest Boakye Danquah.pdf]]


![[Thesis July Draft- 3 .docx]]

