
5.1 Summary of Key Findings  
5.2 Intellectual merit and Broader Impact
5.3 Limitations
5.3 Future Work  
5.4 Policy and Industry Implications



### 6.1 Summary of Key Findings

In this thesis, we have developed and applied a tightly integrated physics‐economic framework for assessing green hydrogen production via PEM electrolysis. By validating a physics-based PEM model against literature  and experimental data, we confirmed that our PEM stack achieve 65–70 % HHV efficiency at ~49 kWh kg⁻¹ SEC. A fitted CAPEX curve shows that uninstalled cost falls steeply up to about 10 MW, after which economies of scale flatten. Together these metrics underpin a baseline LCOH of ≈ 7 USD kg⁻¹ for a 10 000 kg d⁻¹ plant supplied with 0.07 USD kWh⁻¹ electricity.
Univariate tornado analyses revealed electricity price as the first-order cost driver: a ±0.04 USD kWh⁻¹ swing shifts LCOH by ±2 USD kg⁻¹ and NPV by ±50 – 100 M USD. Installed CAPEX ranks second, while efficiency, fixed O&M and water costs are tertiary. Multivariate contour maps confirmed that sub-5 USD kg⁻¹ hydrogen resides in a basin defined by ≤ 0.05 USD kWh⁻¹ power and/or SEC ≤ 45 kWh kg⁻¹, provided plant scale exceeds ~8 000 kg d⁻¹.

Financially, the mid-scale (10 000 kg d⁻¹) configuration delivers the best balance of risk and return—an IRR of 32 % and an NPV of 84 M USD—while mega-scale projects (> 50 000 kg d⁻¹) magnify absolute value but add market-sizing risk. Distributed units clear the WACC yet generate limited NPV, indicating a niche for captive-use or resilience-driven deployments.

Among off-grid options, pure PV yields the lowest CAPEX but a middling LCOH because of low capacity factor; wind offers higher utilisation but expensive electricity; PV-wind hybrids strike a compromise. Adding battery storage enhances dispatchability but increases LCOH unless electricity-market revenues offset the storage premium.

I developed and validated a coupled physics-economic framework that links detailed PEM electrolyzer performance models with a standard discounted-cash-flow engine to forecast the levelized cost of hydrogen (LCOH) and economic metrics. Our baseline scenario, a 10 000 kg H₂ day⁻¹ plant operating at 333 K, 30 bar, and drawing grid power at $0.07 kWh⁻¹—yields an LCOH near $7 kg⁻¹, an IRR of 32 %, and an NPV of $84 million.


Conclusion
This thesis delivers a definitive framework for forecasting the true cost and value of grid-connected and renewable-driven PEM hydrogen production. By rigorously validating our physics-based electrolyzer model against published polarization data and then embedding it within a DOE-aligned discounted-cash-flow engine, we establish unequivocal benchmarks: a 10 000 kg d⁻¹ plant at 333 K and 30 bar, fueled at $0.07 kWh⁻¹, produces hydrogen at $7 kg⁻¹ with a 32 % IRR and an $84 M NPV.
Through systematic scenarios-based sensitivity analysis, we demonstrated that electricity price is the dominant lever: capable of swinging LCOH by up to $2 kg⁻¹ for every $0.04 kWh⁻¹ shift in the tariff and altering NPV by tens of millions of dollars. Installed capital expense emerges as the next critical driver: driving stack and BoP costs down to $250 kW⁻¹ is not a marginal improvement but a transformational step that can lower hydrogen cost by more than $1.50 kg⁻¹. Efficiency improvements (45–55 kWh kg⁻¹ SEC) and optimized O&M regimes offer incremental benefits, typically under $0.50 kg⁻¹ in savings, while water and oxygen streams exert negligible economic impact under current market parameters.
Contour mappings across plant scale and power price reveal a clear "sweet spot" for sub-$5 kg⁻¹ hydrogen: midsize plants (> 8 000 kg d⁻¹) paired with electricity tariffs ≤ $0.05 kWh⁻¹. Financially, plants in this region achieve IRRs above 35 % and NPVs in the low hundreds of millions, whereas smaller or higher‐cost configurations struggle to clear the financing hurdle. Mid-scale deployments (8 000–20 000 kg day⁻¹) emerge as the most balanced path forward: large enough to capture scale economies yet sufficiently agile to avoid the market‐sizing risks of mega‐scale projects.
Among off-grid options, pure PV yields the lowest CAPEX but a middling LCOH because of the low capacity factor; wind offers higher utilization but expensive electricity; PV-wind hybrids strike a compromise. Adding battery storage enhances dispatchability but increases LCOH unless electricity-market revenues offset the storage premium.


- Developed a physic based module
- established a Baseline that maximizes economiies of scale, reflects a scale diminishing effects
- identified the main cost drivers
-  A dynamic energy systenGeographic variability and depencies of the sustainabilty and cost of green hydrogen
## 6.2 Intellectual Merit

This study advances the techno-economic analysis of green hydrogen production by introducing a rigorously coupled, multi-scale modeling framework that integrates detailed electrochemical physics, system-level cost assessment, and dynamic renewable energy integration. Unlike prior work that treats PEM electrolyzer design and energy supply in isolation, our approach unifies these domains through three novel contributions:

1. Physics-Driven Optimization: We develop a first-principles, 0D/1D PEM electrolyzer model, parametrized for activation, ohmic and concentration overpotentials, membrane hydration, and gas crossover. , 

2. Dynamic, Location-Specific Energy Coupling: We incorporate hourly-resolved PV, wind, and hybrid generation profiles, sourced from high-resolution irradiance and wind reanalysis data, directly into the electrolyzer simulation. By coupling LCOE-based pricing signals with electrolyzer dispatch, the framework quantifies the cost and emissions impacts of intermittency, which will enable dynamic optimization of renewable-electrolyzer-storage configurations through surrogate-accelerated particle swarm methods.



## **6.0 Broader Impact**

The outcomes of this integrated analysis extend well beyond academic insight. It offers tangible benefits for energy policy, industry strategy, and societal decarbonization goals. First, by providing site‐specific LCOH and NPV maps that account for regional renewable resources, this work equips policymakers and planners with the quantitative evidence needed to tailor incentives, such as production tax credits, renewable energy mandates, or locational subsidies, to locations where green hydrogen can be produced most cost‐effectively.

We have demonstrated that distributed, smaller‐scale electrolyzers can achieve competitive LCOH in grid‐constrained or remote regions, underscores a pathway for industrial decarbonization in hard‐to‐reach communities and emerging markets. Localized hydrogen production reduces dependence on long-distance gas pipelines, enhances energy resilience, and creates new green job opportunities in manufacturing, operations, and maintenance.

Moreover, the framework's dynamic modeling of intermittency informs grid operators and utilities about the value of flexible loads and hydrogen storage in balancing high penetrations of variable renewable energy sources. By demonstrating how electrolyzers can provide demand response and ancillary services, our work aligns with broader efforts to modernize electric grids, reduce curtailment of solar and wind output, and integrate large‐scale clean energy systems.



## 5.4 Limitations of the Study


 Our techno-economic framework offers a comprehensive view of PEM hydrogen economics, but several limitations exist. We focused only on production, excluding downstream costs like compression, storage, and transportation. In situations where hydrogen needs to be transported long distances or stored at high pressures, total supply-chain costs can increase by 20–30%, which could reduce the attractive LCOH and financial returns reported here.

Second, our renewable‐integration scenarios employ a simplified dispatch logic that allocates power instantaneously to the electrolyzer and, where applicable, to battery storage. Real‐world operations are complicated by grid‐connection agreements, ramp‐rate limits, and ancillary service obligations that can impose additional curtailment or balancing costs. Likewise, we assumed perfect foresight of hourly resource availability, whereas actual operation will face forecasting errors that lead to suboptimal utilization and slight efficiency penalties.

Third, our financial model uses fixed WACC, tax rate, and offtake price assumptions over the 20-year horizon. Market conditions, policy incentives, and capital market risk premiums may change, particularly under carbon pricing regimes or fluctuating interest rate environments, resulting in tail risks or upside opportunities that are not captured in the static DCF. Renewable hydrogen models depend on multi-year power purchase agreements, and the termination or renegotiation of these agreements can significantly affect project economics.

Fourth, technical inputs such as stack lifetime, efficiency, and replacement schedules are informed by current literature and vendor data. However, they may not fully account for emerging degradation modes when managing variable renewable resource operations. We also abstract away detailed water‐chemistry dynamics and membrane‐electrode‐assembly fouling, aspects that can influence maintenance cycles and unplanned downtime.

Finally, our site-specific renewable resource profiles are based on a representative U.S. inland location and may not apply to coastal, arid, or high-latitude regions without recalibration. We maintain consistent policies, tax rates, depreciation schedules, and incentives. However, project sites often encounter changing regulations that significantly impact economics.




## 5.5 Future Research Directions

Based on the insights from our techno-economic and sensitivity analyses, we've identified several areas for future research. We will focus on improving the accuracy of PEM hydrogen modeling and refining the paths to green hydrogen costs towards DOEs target of $2-1 /kg of H2.

### 5.5.1 Multi-Objective Stack Optimization

An ongoing task is the formulation and solution of  a multi-objective optimization problem that seeks to minimize the PEMel design cost (CapEx) and specific energy consumption simultaneously while maximizing cell efficiency under realistic operating constraints.  The multi-objective functions aim to minimize the Specific Energy Consumption (SEC) of the PEM electrolyzer and the geometric design width of the MEA ($F_2(X)$) of a cell. $F_{1}(X) = SEC(X)\,$ $F_{2}(X) = t_{mem}+ t_{el_an} + t_{el_cat}$ . Decision variables would include membrane thickness, catalyst loading, ionomer content, and operating temperature/current setpoints. 

We impose a mechanical durability constraint $g_{1}(x)\;=\;r\sqrt{\frac{k\,\Delta P\,SF}{\sigma_{\rm tensile}}}\;-\;t_{\rm mem}\;\le\;0,$ 
which enforces a minimum membrane thickness capable of withstanding the transmembrane pressure difference. For Nafion, the tensile strength ($σ_{tensile}$) ranges from 25 to 40 MPa, and safety factors (SF) of 1.5–2.0 are recommended for high-pressure differentials. @limDurabilityPerformanceAnalysis2023 Swelling-induced plastic deformation accelerates failure at ΔP>20  if $t{mem}$ is insufficient. The design variables are bounded by manufacturing, material, and operational limits. Performance constraints require a minimum Faradaic efficiency of 99%, an operating temperature cap of 353 K to protect polymer integrity, and a hydrogen production rate threshold of 0.5 kg h⁻¹ per cell at 2 A cm⁻². 
This objective aligns directly with the U.S. Department of Energy's cost and performance targets for PEM electrolysis. @petersonHFTOHydrogenProduction The model provides opportunities to explore trade-offs that are inherently coupled in the design space of the PEM electrolyzer. 
We will implement this formulation in Python using the Pymoo library. The optimization workflow <span style=" color:rgb(0, 112, 192)">(Figure 4)</span>  begins by sampling candidate MEA designs each defined by the decision vector space. For every candidate x, our coupled model computes the SEC and stack voltage, predicts Faradaic efficiency, and calculates the implied cost factor based on material thicknesses. Through iterative non-dominated sorting and genetic operators, NSGA-II reveals the envelope of trade-off designs ranging from ultra-thin, high-efficiency stacks with elevated crossover risk to thicker, more robust configurations with slightly higher energy demands.
Applying evolutionary algorithms or Pareto-front techniques can reveal trade-off frontiers between cost and performance, guiding R&D priorities and highlighting “sweet-spot” designs that deliver near-optimal economics without sacrificing longevity (Figure 4)

> **Figure 6. : Schematic of the multi‐objective optimization workflow, highlighting decision variables, constraints, and the Pareto front generation.**
![[image-54.png]]




### 5.5.2 Evaluation of Cost-Reduction Levers

Building on our completed sensitivity analyses, the next phase is to develop a systematic framework for assessing how alternative materials and manufacturing pathways can reduce both the capital and operating costs of PEM electrolyzers. In particular, we will focus on three critical components: the membrane, the anode catalyst layer, and the cathode catalyst layer electrodes. By integrating material property libraries derived from experimental studies into our Python model, we can rapidly simulate the techno-economic impact of substituting lower-cost or higher-performance materials and quantify the trade-offs in terms of efficiency, durability, and manufacturability.
The proposed workflow will begin with a comprehensive literature survey of advanced membrane chemistries (hydrocarbon-based polymers, reinforced PFSA composites) and low-loading or non-precious-metal catalysts (Ni–Fe, transition-metal carbides) reported in peer-reviewed journals. @CriticalStrategicRaw2024.  We will catalog these alternative PEM electrolyzer materials and extract their key design parameters and cost metrics. This “material library” will feed directly into our existing lumped Python electrolyzer model, replacing baseline Nafion 117 and iridium‐platinum catalysts. We will adopt cost functions from both the Green Hydrogen Cost Report and recent NREL reports on manufacturing analyses, which describe how uninstalled stack and BoP costs decline with cumulative production volume. @badgettUpdatedManufacturedCost2024 ,  @mayyasManufacturingCostAnalysis2019  For each material scenario, we will compute learning-curve coefficients that reflect both material cost reductions (e.g., bulk polymer synthesis) and process innovations (roll-to-roll membrane casting, inkjet catalyst deposition). 

By integrating material property libraries derived from experimental studies into our Python model, we can rapidly simulate the techno-economic impact of substituting lower-cost or higher-performance materials and quantify the trade-offs in terms of efficiency, durability, and manufacturability. Once the material and scale-up cost functions are in place, we will perform a rigorous global sensitivity and uncertainty analysis using BioSTEAM's built-in Monte Carlo and Sobol sampling routines. By coupling our Python electrolyzer class to the BioSTEAM flowsheet framework, we can simulate hundreds of thousands of design variants, systematically perturbing material properties (e.g., membrane thickness and conductivity), catalyst attributes (e.g., loading and ECSA), and cost-learning parameters.

We will then integrate our Python-based electrochemical model into the BioSTEAM framework to support a rigorous, global sensitivity and scenario analysis. By encoding each material option as a discrete "module" within BioSTEAM, we can simulate the full process-level impacts, spanning stack performance, BoP requirements, and hydrogen purity under mass and energy balances. Parallel Aspen Plus case studies will be developed for cross-validation. Comparisons between our streamlined Python outputs and BioSTEAM's rigorous unit-operation simulations will help to calibrate model fidelity.




### 5.5.3 Dynamic Optimization of Renewable-Electrolyzer Configurations

The renewable energy(RE) potential vary across geographical regions for different energy systems. @maclaurinRenewableEnergyPotential2021  

![[image-51.png]]

Our next task will integrate a dynamic, multi-objective optimization layer that selects optimal renewable energy mixes, electrolyzer sizing, and storage capacities to minimize the levelized cost of hydrogen (LCOH) under real-world intermittency. To efficiently explore this high-dimensional design space, we propose using particle swarm optimization (PSO) augmented with Gaussian process surrogates. @mohammadiSurrogateModelingSolving2024 PSO particles will represent plausible configurations and pairings whose hourly dispatch is simulated by our renewable and electrolyzer time-series models. At each iteration, we will compute LCOH, capacity factor, and storage utilization metrics for hundreds of scenarios, then update particle velocities and positions based on local and global optima. The incorporation of a Gaussian process model will accelerate convergence by approximating LCOH responses in unexplored regions, allowing the optimizer to focus on the most promising design clusters.
Geospatial variability of renewable resources will be addressed by embedding region-specific weather, tariff, and land-use data into the optimization. We will perform parallel PSO runs for each candidate location, thereby generating location‐tailored Pareto fronts of LCOH versus configuration cost. Post-processing these fronts will identify "sweet spot" sites where favorable solar or wind regimes combine with low land and grid-connection costs to yield sub-$3.00 kg⁻¹ hydrogen. Furthermore, by mapping the distribution of optimal mixes, such as the ratio of wind to solar capacity or the required battery size per MW of electrolyzer power, we can provide prescriptive guidance on how to scale projects in diverse geographies.

Finally, we will integrate machine-learning classifiers to predict feasibility envelopes based on site attributes, renewable energy potential, permitting complexity, and proximity to demand centers. Training this classifier on PSO results will enable rapid pre-screening of new sites without requiring full optimization runs, thereby reducing the computational burden for stakeholders evaluating hundreds of potential projects. Completing Task 3.2 will deliver a powerful decision-support tool that not only minimizes LCOH but also characterizes the resilience and economic risk of green hydrogen systems across varying contexts. The goal is to pave the way for strategic deployment of next-generation PEM electrolyzer infrastructure.





### 5.5.4 Geospatial, Hourly-Resolved LCOH Mapping with Policy and Emissions Layers

 Geospatial, Hourly-Resolved LCOH Mapping with Policy and Emissions Layers

The final element of our dynamic system-analysis framework will be a comprehensive geospatial assessment that calculates location-specific LCOH by coupling hourly dispatch simulations with regional environmental and financial parameters. This task entails two key components: spatial data integration and incentive modeling.

**Spatial Data Integration** 
We will assemble high-resolution geospatial layers for five archetypal U.S. regions: the Texas Gulf Coast, California Central Valley, Great Plains, New York offshore, and the Phoenix–Casa Grande corridor in Arizona. We will draw on NREL's NSRDB for solar irradiance, the WIND Toolkit for wind speeds, and publicly available elevation, land-use, and grid interconnection maps. Each site will be characterized by its hourly renewable generation potential, prevailing wholesale and time-of-use electricity tariffs, and transmission constraints, ensuring that our dispatch model reflects both physical resource endowment and market exposure.

**Policy and Incentive Modeling**  
To capture the impact of federal and state incentives on hydrogen economics, we will layer in tax credit eligibility. The Investment Tax Credit (ITC) for renewables and the Production Tax Credit (PTC) for clean hydrogen under the Inflation Reduction Act. @45VHydrogenTax;  @gomezDeterminingLifeCycle We will calculate after-incentive LCOH and NPV for each location by linking hourly hydrogen production outputs to annualized ITC and PTC cash flows. Additional regional incentives, such as state renewable portfolio standard multipliers or land-use permitting costs, will be included.

Together, these analyses will equip policymakers, developers, and investors with a detailed, site-tailored understanding of green hydrogen viability. It will aid in identifying regions with optimal resource, regulatory, and economic conditions and quantifying how policy levers shift the competitive landscape. This geospatial LCOH atlas will serve as a decision-support tool to accelerate the deployment of cost-effective, clean hydrogen infrastructure at scale.











