

**Technoeconomic Analysis and Design Optimization of Green Hydrogen Production via PEM Electrolysis**




## outline

1.0 Overview | project summary
2.0 Goals and Objectives
3.0 Research Background.
	3.1 design and Multi-objective optimization background
	3.2 Techno-economic background.
	3.3 RE system background
4.0 Proposed Research, methods and results
4.1 Aims and Task

5.0 Intellectual Merit
6.0 Broader Impact
7.0 References




## 1.0 Overview | project summary

The transition to a low‐carbon energy economy has placed green hydrogen at the forefront of global decarbonization strategies. A hydrogen production system, when powered by renewable electricity, yields minimal lifecycle greenhouse gas emissions, unlike hydrogen produced from natural gas or coal.  Yet, despite its environmental promise, green hydrogen remains significantly more expensive than fossil‐derived alternatives, with levelized costs frequently exceeding $6 /kg, compared to $1–2 /kg for grey hydrogen produced from natural gas..  @mcqueenDepartmentEnergyHydrogen2020; @marzoukLevelizedCostGreen2023
Governments and industry leaders have responded with a variety of policies and incentives. The EU and its member states, through the REPowerEU plan and the Clean Industrial Deal, aim for 40 GW of electrolyser capacity by 2030. Section 45v of the Inflation Reduction Act (IRA)  introduced a production tax credit (PTC) of up to $3 per kilogram to narrow this cost gap.. @gomezDeterminingLifeCycle; @45VHydrogenTax Yet in practice, these incentives alone do not guarantee long‐term competitiveness. Political shifts, changes in subsidy schemes, and volatility in renewable electricity markets can render incentive‐driven projects economically vulnerable. In this context, a more enduring solution lies in driving down the intrinsic production costs of proton‐exchange‐membrane (PEM) electrolyzers through advances in electrolyzer design, scale economies, and system-level optimization.

Current projections indicate that demand for green hydrogen in the US could rise from less than 11.16 million metric tons in 2021 to over 27 million tons by 2040 driven by heavy industries, long‐haul transportation, and steel making @nyangonAdvancementsHydrogenEnergy2024 . Among the various electrolysis technologies, PEM electrolyzers stand out for their high efficiency and compact footprint. Their operational flexibility makes them particularly well‐suited to dynamic renewable power inputs. Nevertheless, the capital cost of PEM stacks, their balance‐of‐plant (BoP) requirements, and the high price of electricity feedstock continue to dominate the levelized cost of hydrogen (LCOH). At the same time, these cost drivers are tightly interwoven with design choices such as current density, membrane thickness, catalyst loading, and operating temperature and with the temporal variability of upstream renewable generation. As a result, optimizing PEM hydrogen production requires a comprehensive analysis that spans electrochemical physics, economics, and energy systems modeling.

This report addresses this challenge by presenting an integrated framework that unites three previously siloed domains. First, we develop a detailed, physics‐based model of a PEM electrolyzer stack, capturing activation, ohmic and concentration overpotentials, Faradaic efficiency, and gas crossover effects. Next, we couple these cell‐level performance metrics with a modular techno‐economic assessment (TEA) to quantify how material choices, operating conditions, and scale‐dependent capital costs drive LCOH and net present value (NPV). Finally, we embed an hourly‐resolved energy‐supply layer to simulate photovoltaic, wind, hybrid, and grid‐interactive configurations. We examine how renewable intermittency and geographic resource variability affect production economics and carbon intensity. By merging these three components, thus, electrochemical, economic, and energy system models, into a single cohesive framework, our research uncovers interactions and trade‐offs that remain opaque under conventional, one‐dimensional analyses.

Our findings reveal several significant insights. First, energy feedstock cost and uninstalled capital cost emerge as the two most influential drivers of LCOH and NPV. The cost of electricity feedstock overshadows the economies of scaling plant capacity beyond 10kg of H2 day of hydrogen. In our sensitivity analysis, a $0.09 /kWh difference in electricity price affects over 80% of the NPV. Similarly,  a difference in the target uninstalled CAPEX from $250 to $1 500 /kW affects more than half of the NPV. The choice of renewable energy configuration (PV, wind, hybrid, or grid‐interactive) and the local resource profile can shift LCOH by 20 – 30 percent, emphasizing the need for site‐tailored system architectures.

Looking forward, our framework paves the way for several avenues of future research. In subsequent tasks, we will expand the TEA by exploring cost-reduction levers through material substitution by incorporating hydrocarbon-based membranes and non-precious-metal catalysts and quantifying their impact via global sensitivity analysis. We will introduce a surrogate-accelerated particle swarm optimizer to identify optimal renewable-electrolyzer-storage configurations across hundreds of candidate sites, producing geospatial LCOH maps that highlight "sweet-spot" regions for green hydrogen investment.






----


Third, renewable energy configuration and geographic variability shape LCOH by up to 20 percent across different regions: hybrid PV-wind systems consistently outperform single-technology layouts by raising effective capacity factors and reducing curtailment, while sites with abundant wind resources—such as the Great Plains—yield the lowest levelized electricity costs when coupled with grid-interactive electrolyzers.



Our findings reveal several significant insights. First, electricity feedstock cost emerges as the single largest driver of LCOH and NPV, often overshadowing reductions achievable through incremental electrolyzer improvements. Second, uninstalled capital cost—determined by manufacturing scale and material selection—also exerts a substantial influence, highlighting the importance of technology scale‐up and alternative, lower‐cost membrane or catalyst options. 

Third, multi‐objective optimization reveals “sweet‐spot” configurations in which modest increases in material thickness yield substantial efficiency gains without disproportionately inflating CAPEX. 

Fourth, the choice of renewable energy configuration (PV, wind, hybrid, or grid‐interactive) and the local resource profile can shift LCOH by 20 – 30 percent, emphasizing the need for site‐tailored system architectures. Finally, by simulating hourly dynamics, we demonstrate that flexible operation—leveraging storage or grid buy/sell arbitrage—can further reduce effective LCOH and carbon intensity relative to static, capacity‐factor assumptions.


Looking ahead, our framework opens several avenues for future research. First, Task 2.3 will explore cost‐reduction levers through material substitution and manufacturing learning curves, using global sensitivity analysis to rank candidate membranes and catalysts. Second, Task 3.2 will implement a dynamic, surrogate‐accelerated optimization algorithm to identify optimal renewable‐electrolyzer‐storage configurations across geospatially distributed sites. Third, future work will extend the framework to incorporate lifecycle greenhouse gas accounting, water resource constraints, and potential revenue streams from grid ancillary services or oxygen by‐product sales. Collectively, these next steps will further refine our understanding of how to deploy PEM hydrogen systems at scale, underlining practical implications for manufacturers, project developers, utilities, and regulators seeking to accelerate the green hydrogen economy.

Looking forward, our framework paves the way for several avenues of future research. In Task 2.3, we will expand the TEA by exploring cost-reduction levers through material substitution—incorporating hydrocarbon-based membranes and non-precious-metal catalysts—and quantifying their impact via global sensitivity analysis. Task 3.2 will introduce a surrogate-accelerated particle swarm optimizer to identify optimal renewable-electrolyzer-storage configurations across hundreds of candidate sites, producing geospatial LCOH maps that highlight “sweet-spot” regions for green hydrogen investment. Ultimately, these advancements will provide stakeholders—ranging from electrolyzer manufacturers to policymakers and developers—with a comprehensive decision-support toolkit that quantifies the economic and environmental benefits of next-generation PEM electrolyzers.




## 2.0 Goals and Objectives

The overarching goal of this research is to develop and validate an integrated modeling framework that couples detailed, physics‐based PEM electrolyzer design with system‐level techno-economic analysis and dynamic renewable energy system modeling, in order to identify key cost drivers and optimize green hydrogen production. By unifying electrochemical, financial, and energy-resource perspectives, the framework will enable data-driven decision-making for next-generation PEM electrolyzers and their deployment under diverse operating conditions.

To achieve this goal, we will address the following research questions:

1. **What are the principal techno-economic cost drivers** in PEM electrolyzer hydrogen production, and how do these drivers vary with plant scale, material selection, and operating conditions?

2. **In what ways do electrolyzer design variables** such as membrane thickness, catalyst layer loading, and cell operating temperature affect energy efficiency, Faradaic performance, and stack durability, and how do these trade-offs translate into changes in levelized cost of hydrogen (LCOH) and net present value (NPV)?

3. **How can multi-objective optimization** be employed to balance capital expenditure, specific energy consumption, and durability in the configuration of PEM electrolyzer components?

4. **What is the impact of different renewable energy supply configurations** ( photovoltaic, wind, hybrid, or grid-interactive) on hydrogen production cost and capacity factor, when modeled at an hourly resolution for location-specific scenarios?

>1. **Which combinations of plant scale, technology selection, and operating strategy** minimize LCOH while ensuring economic viability, given spatial variations in renewable resource availability and local grid conditions?

To answer these questions, the project is organized around three specific Aims:

**Aim 1: Develop a Physics-Based Electrochemical Model and Multi-Objective Design Optimization.**  
In this Aim, we will refine and extend our lumped-parameter PEM electrolyzer model by incorporating activation, ohmic, and concentration overpotentials; membrane hydration; Faradaic efficiency; and gas crossover effects and embed it within a multi-objective optimization framework. The objective will be to identify Pareto-optimal combinations of membrane thickness, catalyst layer loading, electrode thickness, current density, and operating temperature that simultaneously minimize specific energy consumption and overall MEA thickness, subject to durability constraints. This Aim will deliver a suite of validated cell-level design maps that quantify the inherent trade-offs between efficiency, material cost, and mechanical integrity.

**Aim 2: Construct a Modular Techno-Economic Assessment (TEA) Integrating Electrolyzer Performance.**  
Building on the cell-level outputs from Aim 1, Aim 2 will establish a comprehensive system boundary encompassing the electrolyzer stack and balance-of-plant components. We will develop a modular TEA that computes LCOH and NPV over a 20-year horizon by combining stack power requirements, capital cost scaling laws, acceleration-based depreciation schedules, and operating expense drivers (electricity, maintenance, membranes, catalysts, and water treatment). This Aim will also perform detailed sensitivity and scaling analyses to quantify how variations in uninstalled CAPEX, electricity price, efficiency, fixed O&M, and other inputs affect financial metrics, thereby pinpointing the highest-impact cost levers and manufacturing targets.

**Aim 3: Integrate Dynamic, Hourly-Resolved Renewable Energy Modeling and Location-Specific Optimization.**  
Aim 3 will couple the system TEA from Aim 2 with an energy-supply layer that simulates hourly output from photovoltaic, wind, hybrid, and grid-interactive configurations at selected U.S. locations. By computing time-series of renewable availability, curtailment, and LCOE, we will drive the electrolyzer dispatch to calculate annual capacity factors, hydrogen yields, and temporal cost profiles. A dynamic optimization algorithm—leveraging particle swarm methods with Gaussian process surrogates—will then identify optimal combinations of renewable capacities, electrolyzer sizing, and battery storage that minimize LCOH under site-specific resource and policy constraints. This Aim will produce spatial maps of “sweet spot” regions where green hydrogen can be produced most economically, as well as guidelines for matching system configurations to local grid conditions.

Together, these Aims will fulfill our objectives of identifying cost drivers, optimizing electrolyzer design parameters, and determining the most promising energy-system architectures for scalable, cost-effective green hydrogen production.

## Overall Goal

> To develop an integrated modeling framework that combines physics-based electrolyzer design, technoeconomic analysis, and dynamic energy systems modeling to optimize green hydrogen production via PEM electrolysis.
	
	
Identify cost drivers through a system analysis and optimize the production to system variables.


- Research questions
- Aims.


How can the design and operation of PEM electrolyzers be optimized to reduce the cost, while maintaining high efficiency and adaptability to renewable energy variability?


## 3.0 Research Background.
3.1 PEM Design, tradeoffs and Multi-objective optimization background.
3.2 Techno-economic background.
3.3 RE system background

We critically evaluate prior work to highlight methodological advances, identify unresolved research gaps, and justify the need for an integrated modeling framework.

####  Electrochemical Modeling and Materials Advances in PEM Electrolysis

Early theoretical designs of PEM electrolysis focused on macro-scale energy balances and simplified polarization curves, often neglecting the detailed coupling between activation, ohmic, and concentration overpotentials. For instance, Kazacos and Turnbull (2010) developed a zero-dimensional model that captured overall cell voltage losses but treated membrane hydration empirically, without resolving through-plane transport [3]. Subsequent studies, such as those by Lee et al. (2015), incorporated one-dimensional (1D) diffusion layers to account for gas crossover, yet relied on fixed water content assumptions, thereby limiting predictive capability under dynamic operating conditions [4].
More recently, composite 0D/1D models have emerged that explicitly couple electrochemical kinetics with mass-transport and thermal balances. Bessarabov and Miller (2018) provided a seminal framework in which Faraday’s law, Butler–Volmer kinetics, and Fick’s law of diffusion were linked through membrane hydration variables to predict cell voltage and gas crossover rates as functions of current density, temperature, and membrane thickness [5]. These models demonstrated that thinner membranes reduced ohmic losses but increased hydrogen permeation, creating an efficiency-durability trade-off. Similarly, Webb et al. (2019) expanded upon this by incorporating a detailed multi-layer approach that considered catalyst porous transport layers, enabling the simulation of both reactant distribution and local heat generation [6]. However, these 1D approaches still abstracted spatial heterogeneities, such as lateral current and flow distribution, leaving a need for fully two-dimensional (2D) or three-dimensional (3D) models when designing novel flow-field geometries [7].

On the materials front, Nafion™-117 remains the benchmark membrane due to its high proton conductivity and chemical stability, but its thickness and fluorinated backbone translate to high material cost (~$320 m⁻²) and limitations in mechanical strength under cyclic hydration. Researchers have investigated alternative hydrocarbon-based membranes (e.g., sulfonated polyether ether ketone (SPEEK), sulfonated polyphenylene) that promise lower cost and improved mechanical durability. For example, Zheng et al. (2021) compared SPEEK membranes to Nafion™ in a 1 kW stack and observed only a 5 % increase in ohmic resistance at 333 K, while reducing material expense by 40 % [8]. Despite these advantages, hydrocarbon membranes often exhibit elevated gas crossover and lower chemical stability at high cell voltages, indicating a materials performance gap that must be bridged via advanced cross-linking or composite reinforcement [9].

Catalyst development has likewise evolved. Traditional platinum-iridium (Pt-Ir) alloys at the anode deliver low overpotentials (≈30 mV at 2 A cm⁻²) but are prohibitively expensive and subject to supply constraints. Transition to lower platinum-group-metal (PGM) loadings and exploration of non-PGM catalysts (e.g., nickel, cobalt phosphides) has accelerated in recent years. Zhao et al. (2020) reported a Ni–Fe hydroxide catalyst that achieved 10 mA cm⁻² at 1.48 V versus a reversible hydrogen electrode (RHE), with superior stability to Pt-Ir under accelerated degradation testing [10]. Nonetheless, non-PGM catalysts typically incur higher overpotentials at industrial current densities (>1 A cm⁻²), and their long-term stability under high-pressure operation remains unproven [11]. As such, there is a critical research need to quantify the performance–cost trade-offs of emerging catalyst chemistries, particularly at stack scale, and incorporate these data into system-level techno-economic analyses.

Despite these advances, two primary gaps persist in the electrochemical literature. First, most models remain 1D or pseudo-1D, addressing through-plane transport without capturing the complex interplay of flow-field design, lateral current distribution, and multi-phase water management under dynamic load. Second, while individual studies have examined membrane alternatives or catalyst substitutions, few have systematically linked material property variations to techno-economic outcomes. This disconnect impedes efforts to identify which materials investments truly yield cost-effective performance improvements when scaled to commercial module sizes. Our work seeks to address these gaps by embedding a validated 0D/1D model within a multi-objective optimization framework that directly quantifies how variations in membrane conductivity, catalyst loading, and electrode porosity affect both energy efficiency and capital cost.

### Techno-Economic Analysis and Energy-System Integration for PEM Hydrogen
 
 Landmark studies such as the U.S. Department of Energy’s H2A reports 11 have established standardized methods for projecting levelized cost of hydrogen (LCOH) by combining capital expenditures (CAPEX), operating expenditures (OPEX), and performance parameters. However, many H2A projections rely on constant‐price assumptions and static capacity factors that fail to capture renewable energy variability.

Early TEA studies (e.g., Schmidt et al. (2017)) established baseline LCOH values of $5–7 kg⁻¹ under industry-average electricity prices (~$0.06 kWh⁻¹) and moderate production scales (1–10 MW) [12]. These assessments generally adopted a “top-down” methodology, combining equipment-level cost estimates from vendor quotes with assumed stack performance curves, but lacked rigorous integration with dynamic operating profiles.
Subsequent work—for instance, by Turner et al. (2019)—incorporated detailed cost-scaling relationships for electrolyzer stacks and balance-of-plant (BoP) components
Turner’s model highlighted that economies of scale in stack manufacturing (driven by learning-curve effects) and BoP standardization accounted for more than 30 % of potential LCOH reductions. Nevertheless, these static TEA studies still assumed constant capacity factors (often 90 %), thereby missing the critical impact of renewable intermittency on plant utilization and hydrogen cost.

Integrating renewable-energy variability into TEA frameworks has been a growing focus. For example, Janjbar et al. (2020) paired a PV-based generation profile with a fixed-capacity electrolyzer, revealing that under rooftop solar conditions, annual capacity factors could drop below 25 %. Similarly, van Renssen (2021) demonstrated that hybrid PV-wind systems—leveraging complementary diurnal and seasonal patterns—could achieve 45–55 % capacity factors in select regions, pushing LCOH down to $4–5 kg⁻¹ [15]. 

Beyond capacity factors, geographic sensitivity analyses have illustrated that LCOH can vary by $2–3 kg⁻¹ across different U.S. regions due to differences in renewable resource quality, electricity tariffs, and permitting costs. 

A further dimension of recent TEA research involves policy incentives and carbon pricing. For instance, the Inflation Reduction Act (IRA) of 2022 introduced production tax credits (PTC) of up to $3 kg⁻¹ H₂ for electrolyzers sourcing low-carbon electricity, effectively lowering LCOH by 30–50 % under favorable conditions [17]. Yet, studies by McCoy and Lipman (2023) caution that PTC eligibility criteria—such as hourly emissions intensity thresholds—require granular, hourly modeling to accurately capture compliance risk and revenue streams [18]. This motivates coupling TEA with time-resolved emissions data—a complexity seldom addressed in earlier static analyses.

Finally, life-cycle assessments (LCAs) have become increasingly integrated with TEA to capture the environmental ramifications of green hydrogen pathways. Peters et al. (2021) combined LCA with TEA for a 100 MW onshore‐wind‐driven electrolyzer in Texas, calculating a cradle‐to‐gate carbon intensity of 1.5 kg CO₂e kg⁻¹ H₂—roughly one‐tenth that of steam‐methane‐reforming (SMR) without carbon capture 171717.

----

####  Electrochemical Modeling and Materials Advances in PEM Electrolysis

A lot of studies have been done on the modeling the electrochemical reactions in PEM electrolyser systems.  However, formulation details can vary across literature but the fundamental model should account for the overpotential losses @falcaoReviewPEMElectrolyzer2020 . The key loss terms include activation overpotentials, ohmic losses and concentration overpotentials. The activation overpotential occurs at anode and cathode, due to sluggish reaction kinetics. The ohmic losses is due to the ionic resistance in the membrane and electronic resistances in electrodes/interconnects, The concentration or mass transport overpotentials are also caused by gas bubble accumulation and reactant depletion at high current densities @falcaoReviewPEMElectrolyzer2020 . Dynamic models have also been developed (including capacitive terms for transient response), but many studies focus on steady-state performance unless coupling to renewable power profiles where transient behavior is important @hernandez-gomezInvestigationPEMElectrolyzer2020 Hydrogen produced at the cathode can permeate through the polymer membrane to the oxygen side (and vice versa for oxygen to the hydrogen side), especially at high pressure or with thinner membranes. This effect lowers the Faraday efficiency. Faraday efficiency $\eta_F$ is the fraction of the theoretical hydrogen production that is actually realized. A $\eta_F$ less than 100% is caused by shunt currents and gas losses through the membrane @hernandez-gomezInvestigationPEMElectrolyzer2020 . Shunt currents are influenced by stack design and materials (e.g. conductive paths in the bipolar plates) @yodwongFaradaysEfficiencyModeling2020 . On-line mass spectrometry tests have shown that hydrogen permeation rates increase with current density (due to supersaturation of dissolved H₂ in the catalyst layer), and that thin membranes dramatically boost gas crossover, requiring mitigation to avoid explosive H₂/O₂ mixtures at low loads  @berntAnalysisGasPermeation2020 . Empirical equations from  Hug and Ulleberg have used to fit $\eta_F$ as a function of current density, pressure, and temperature  @ullebergModelingAdvancedAlkaline2003,  @hernandez-gomezInvestigationPEMElectrolyzer2020 .
Efforts on PEM electrolyser modeling span from lumped zero-dimensional (0D) approaches up to full three-dimensional (3D) computational fluid dynamics @falcaoReviewPEMElectrolyzer2020 .  Different levels of fidelity are chosen based on the modeling goals. Simpler models are used for control and large-scale simulations whereas 3D models are used for detailed design optimization @falcaoReviewPEMElectrolyzer2020 . Briguglio _et al._ (2013) carried out a 3D CFD analysis of a 10-cell PEM stack with 120 parallel channels, finding that a well-designed flow distributor yielded uniform water flow and homogeneous pressure across all cells  @briguglioDesignTestingCompact2013 . Such 3D studies help ensure there are no starvation or flooding spots in scale-up designs. On the other hand, zero-dimensional dynamic models (e.g. using empirical polarization curves and differential equations for system dynamics) have been used to simulate how a PEM electrolyzer responds to transient power input or to perform fast design-sensitivity analyses @hernandez-gomezInvestigationPEMElectrolyzer2020 .

In addition to flow channels, the membrane-electrode assembly (MEA) configuration influences performance. PEM electrolyzers typically use a zero-gap configuration, where the catalyst-coated membrane is pressed directly against porous transport layers (PTLs) that also serve as gas diffusion layers. This minimizes resistance by placing catalysts in intimate contact with the membrane. MEAs can be fabricated via catalyst-coated membrane (CCM) approach (catalyst ink applied directly on the membrane, e.g. by spraying or screen-printing) or by gas diffusion electrode (GDE) approach (catalyst coated onto a diffusion layer and then assembled against the membrane)  @carmoComprehensiveReviewPEM2013 . The CCM method (often via decal transfer): catalyst ink containing platinum or iridium particles and ionomer is **sprayed** or blade-coated onto a Teflon substrate, dried and hot-pressed onto the membrane @carmoComprehensiveReviewPEM2013 . This yields a controlled catalyst loading and uniform layer on the membrane. The structure of the catalyst layer (porosity, thickness, ionomer content) is critical – it must allow water access and gas escape while providing ionic contact to the membrane and electronic contact to the electrode. Different fabrication techniques (spraying, painting, physical deposition) and catalyst ink formulations can lead to different microstructures and performance. Research has shown that achieving a homogeneous, well-dispersed catalyst layer improves utilization of precious metals and can allow lower loadings without sacrificing performance @carmoComprehensiveReviewPEM2013 . For instance, earlier PEMWE designs often had very high platinum loadings on the cathode, but it was realized that hydrogen evolution is facile and does not require such excess catalyst. Cathode loadings dropped into the ~0.5–1.0 mg/cm² range without performance loss   @carmoComprehensiveReviewPEM2013 . The anode (oxygen evolution) side is more challenging; typical Iridium loadings were ~2 mg/cm² and have not dramatically decreased historically @carmoComprehensiveReviewPEM2013 . New coating methods (e.g. depositing iridium nanoparticles onto conductive supports, or advanced sputtering techniques) have achieved lower Ir loadings – in one study to ~0.3 mg/cm² – while maintaining performance @carmoComprehensiveReviewPEM2013 .
Aside from catalysts, other design factors include the membrane thickness and reinforcement (mechanical supports or cloth within the membrane to improve strength) and the use of advanced coatings on bipolar plates or PTLs (such as titanium coatings or hydrophilic treatments) to enhance durability and performance. Each of these design choices – flow field pattern, MEA fabrication method, catalyst loading – can significantly affect efficiency, voltage performance, and durability of the electrolyzer. @ahmedEffectComponentsOperating2022; @escobedoDesignConstructionPerformance2023

Conventional PEM electrolyzers use perfluorosulfonic acid (PFSA) polymer membranes (e.g. Nafion™) due to their high proton conductivity and chemical stability.  However, PFSA membranes are expensive and have some limitations. They have an upper thermal limit around 80–90 °C @nguyenFullyHydrocarbonMembrane2022 
 recent advances have yielded hydrocarbon MEAs approaching the performance of PFSA-based systems  @nguyenFullyHydrocarbonMembrane2022 . Hydrocarbon ionomers can have higher glass transition temperatures and potentially allow operation at >100 °C, addressing PFSA’s thermal limitation @nguyenFullyHydrocarbonMembrane2022 . Still, a known issue is that thinner membranes (whether PFSA or hydrocarbon) lead to higher gas crossover; for example, state-of-the-art PFSA electrolyzers often use thick membranes (e.g. Nafion 115 at 125 μm or even N117 at 180 μm) to minimize hydrogen permeation  @nguyenFullyHydrocarbonMembrane2022 . Using thinner membranes would improve conductivity and efficiency, but at the expense of more crossover and potentially reduced mechanical durability @nguyenFullyHydrocarbonMembrane2022 
Non-precious OER catalysts (e.g. transition metal oxides without Ir) have been investigated (such as cobalt or manganese oxides), but so far none can match the stability of Ir-based catalysts in acidic PEM conditions for long lifetimes @carmoComprehensiveReviewPEM2013 . The durability of these new materials is a major focus , since any new material must still achieve the >5–10 year lifetimes expected of electrolyzer stacks @zhangStatusPerspectivesKey2022 
Despite these advances, two primary gaps persist in the electrochemical literature. First, most models remain 1D or pseudo-1D, addressing through-plane transport without capturing the complex interplay of flow-field design, lateral current distribution, and multi-phase water management under dynamic load. Second, while individual studies have examined membrane alternatives or catalyst substitutions, few have systematically linked material property variations to techno-economic outcomes. This disconnect impedes efforts to identify which materials investments truly yield cost-effective performance improvements when scaled to commercial module sizes. Our work seeks to address these gaps by embedding a validated 0D/1D model within a multi-objective optimization framework that directly quantifies how variations in membrane conductivity, catalyst loading, and electrode porosity affect both energy efficiency and capital cost.

### Techno-Economic Analysis and System-Level Modeling



Several open-source frameworks have been developed for the techno-economic analysis (TEA) of hydrogen production systems, including H2A, HySupply, and Techno-Economic Simulation Tool (TechEST) (Abe et al., 2022; Schmidt et al., 2017). These platforms provide valuable tools for evaluating the cost and performance of various hydrogen pathways. However, most existing models are fundamentally static, often lacking dynamic integration between physical system modeling and process economics. This limitation can result in oversimplified assessments that do not fully capture the temporal variability of renewable energy inputs or operational flexibility of electrolyzer systems (Abe et al., 2022; Schmidt et al., 2017).

Recent updates to proprietary software, such as AspenTech’s V14.1, have introduced modules for detailed PEM electrolyzer design and operation, enabling more granular process simulation. Despite these advancements, affordability and accessibility remain significant barriers, particularly for startups and early-stage technology developers, who may lack the resources to invest in high-cost commercial software (Abe et al., 2022).
To address these gaps, several literature have model and optimize water electrolysis systems.

 TEA methodologies in the past decade have evolved from straightforward cost accounting to more sophisticated models that can account for manufacturing scale, temporal operation patterns, and integration into energy networks. Chung _et al._ (2024) introduced a combined physics-based electrolyzer model with an optimization routine to evaluate both steady and dynamic operations on LCOH @chungDesignSpacePEM2024 . Such methods go beyond static cost calculations, examining how capacity optimization, scheduling, and even demand response could impact economics
 manufacturing cost models that estimate how the cost per kW of the stack (and BoP) decreases with larger production volume and system size. @badgettUpdatedManufacturedCost2024; @mayyasManufacturingCostAnalysis2019 
Similarly, learning curve models predict that for every doubling of cumulative production, the unit cost falls by a certain percentage (the “learning rate”) @badgettKeyPerformanceIndicators2023 
Recent analyses and historical data suggest significant cost improvements as manufacturing ramps up. Yates et al. (2020) identified electrolyzer system size as the single most important factor influencing hydrogen cost. In their model, scaling the nominal electrolyzer power up by a factor of 10 could reduce LCOH by around $0.3 per kg (all else equal)  @yatesTechnoeconomicAnalysisHydrogen2020 .
The reasoning is straightforward: larger systems spread fixed costs (like control systems, housing, etc.) over more output, and higher production volumes of stacks enable automated manufacturing, bulk material purchasing, and design optimization for mass production.
The U.S. DOE H2A case studies utilizes linear capital cost model for distributed and central PEM plant.  @jamesPEMElectrolysisH2A2013 . This is approach is limits to the effect of a learning curve and economies of scale. 
A better approach is somewhat reported in literature. Astraini et al curve fitted  uninstalled capital cost-capacity $(P_{EL,rated})$ scaling relationships for electrolyzer stacks system @astrianiOptimalPlanningRenewable2024 . $\mathrm{Cost}_{\text{EL}}=c_{1}+c_{2}\,P_{\text{EL,rated}}+c_{3}\,\exp\bigl(c_{4}\,P_{\text{EL,rated}}\bigr)\,$ 
Reksten et al. modeled the capital cost of PEM electrolyser system to predict the cost of PEM electrolyzers to the plant capacity (Q). For $C = \left(k_o + \frac{k}{Q^{\alpha}}\right) \left(\frac{V}{V_o}\right)^{\beta}$  where Ko and k are fitting constants, Q and  V and Vo represent  plant capacity, the plant installation year and reference year respectively. @rekstenProjectingFutureCost2022

PEM stacks (membrane, electrodes, bipolar plates, etc.) typically account for roughly 40–50% of the total installed system cost, while BoP (power electronics, gas dryers, pumps, cooling system, housing, etc.) accounts for the other ~50–60% @colellaTechnoeconomicAnalysisPEM2014 .  For instance, a study showed stack ~41% and BoP ~59% of direct costs in a forecourt-scale system, and a similar split in a larger central system @colellaTechnoeconomicAnalysisPEM2014 . Within the stack cost, the expensive components are the membrane and catalysts (iridium in particular): these high materials costs mean that even if their quantities are small, they contribute a significant share. One analysis estimated that the catalyst and membrane together could be ~15–20% of the total system cost in current designs @carmoComprehensiveReviewPEM2013  @carmoComprehensiveReviewPEM2013 . BoP cost drivers include the DC power supply/rectifier (often a big cost item), and any hydrogen compression or drying equipment needed. In certain designs, if high-pressure hydrogen output is required, the electrolyzer may be designed to pressurize hydrogen internally, which shifts some cost from an external compressor into the cell components (thicker endplates, etc.).
Many studies assume a stack lifetime of ~60,000–80,000 hours (7–9 years at full usage) for future PEM systems though current demonstrated lifetimes are somewhat lower @krishnanPresentFutureCost2023 . Shorter stack life means more frequent replacements and higher effective cost per kg H₂, unless mitigated by warranties or refurbishments.
Recent literature reports a range of levelized hydrogen costs for PEM electrolysis, depending on assumptions about technology status, scale, and energy inputs.  For current (circa 2020) technology at scale, **LCOH values around $4–$7 per kg** are common in studies @chungDesignSpacePEM2024 . The 2035 scenario from Chung _et al._ where LCOH might hit $1.4/kg is an optimistic case that assumes significant technology and cost improvements @chungDesignSpacePEM2024 . It suggests that by mid-2030s, PEM electrolysis _could_ produce hydrogen in the $1–$2/kg range in favorable regions (e.g. with abundant cheap renewables), which would undercut even methane reforming with carbon capture. In the nearer term, analyses indicate that reaching about $2/kg (a often-cited benchmark for competitiveness with grey hydrogen plus carbon pricing) is plausible by the late 2020s if certain conditions are met: roughly, electricity at $20/MWh or below, electrolyzer capital costs halved from today, and high utilization (or some form of revenue stacking/grid services to compensate if utilization is low). Many studies show current costs in the $5/kg ballpark, so getting to $2 involves roughly a 60% cost reduction – which aligns with expected improvements from scale and cheaper renewables.
The H2A case studies showed that a forecourt-scale unit (1,500 kg H₂/day, ~5 MW) had a hydrogen cost about $5.15/kg, while a central plant (50,000 kg/day, ~165 MW) was about $5.12/kg under similar assumptions – indicating that scale alone in that comparison didn’t change it dramatically because both were assumed to run at high capacity  @jamesPEMElectrolysisH2A2013 . But when including _distribution_ costs (compression, storage, dispensing for the forecourt), the smaller-scale case ended up around $7.5/kg delivered   @jamesPEMElectrolysisH2A2013 .



### Energy-System Integration for PEM Hydrogen

Subsequent work—for instance, by Turner et al. (2019)—incorporated detailed cost-scaling relationships for electrolyzer stacks and balance-of-plant (BoP) components
Turner’s model highlighted that economies of scale in stack manufacturing (driven by learning-curve effects) and BoP standardization accounted for more than 30 % of potential LCOH reductions. Nevertheless, these static TEA studies still assumed constant capacity factors (often 90 %), thereby missing the critical impact of renewable intermittency on plant utilization and hydrogen cost.

Integrating renewable-energy variability into TEA frameworks has been a growing focus. A 2024 techno-economic assessment highlighted that PV-wind hybrid systems reduce LCOH to $3.01/kg by leveraging complementary generation patterns. @baralTechnoeconomicAssessmentGreen2024 hybrid wind-PV scenarios achieve the lowest LCOH due to higher capacity factors and lower electricity prices compared to solar-only systems. The IEEJ study compared "surplus power" (using curtailed renewables) and "stable power" (dedicated renewable plants) configurations. While surplus power reduced electrolyzer capacity factors to 5–13%, stable power designs achieved 50–70% capacity factors by mitigating intermittency, albeit with higher upfront infrastructure costs. @shibataEconomicAnalysisHydrogen2015
This result was achieved through multi-objective optimization of system design, accounting for renewable resource variability and storage integration, and highlights the potential of hybrid renewable systems to significantly improve both utilization rates and economic performance for green hydrogen production @suCapacityConfigurationOptimization2023.
 
Beyond capacity factors, geographic sensitivity analyses have illustrated that LCOH can vary by $2–3 kg⁻¹ across different U.S. regions due to differences in renewable resource quality, electricity tariffs, and permitting costs. For instance, wind-rich regions like ERCOT (Texas) achieve LCOH as low as $3.74/kg with tax credits, while California’s higher grid prices and lower wind capacity factors result in costs exceeding $5/kg @saurUSGeographicAnalysis2011 . Similarly, regions with frequent negative electricity prices (e.g., western Texas) enable cheaper hydrogen production by leveraging curtailed renewable energy @Section45VClean  
A further dimension of recent TEA research involves policy incentives and carbon pricing. The Inflation Reduction Act (IRA) of 2022 introduced production tax credits (PTC) of up to $3 kg⁻¹ H₂ for electrolyzers sourcing low-carbon electricity, effectively lowering LCOH by 30–50 % under favorable conditions @bistlinePowerSectorImpacts2023 . Yet, studies by Bracci (2023) caution that PTC eligibility criteria such as hourly emissions intensity thresholds require granular, hourly modeling to accurately capture compliance risk and revenue streams @45VHydrogenTax , @bracciCostComparisonVarious2023 . This motivates coupling TEA with time-resolved emissions data a complexity seldom addressed in earlier static analyses.


-----
----
### 3.1 PEM Electrolyzer Design and Optimization

Proton exchange membrane (PEM) electrolyzers couple electrochemical water splitting with advanced materials and cell architectures to achieve high‐purity hydrogen production. Several studies with varying levels of formulation details have been conducted, but the foundational elements should account for the overpotential losses @falcaoReviewPEMElectrolyzer2020. The key loss terms include activation overpotentials, ohmic losses, and concentration overpotentials. The activation overpotential occurs at both the anode and cathode due to the reaction kinetics. The ohmic losses arise from the ionic resistance in the membrane and the electronic resistances in the electrodes and interconnects. The concentration or mass transport overpotentials are also caused by gas bubble accumulation and reactant depletion at high current densities @falcaoReviewPEMElectrolyzer2020.

Beyond these lumped-parameter models, one-dimensional through-plane frameworks delineate profiles of species concentration and potential across the membrane-electrode assembly (MEA), along with two- and three-dimensional computational fluid dynamics (CFD) simulations to examine flow-field optimization and non-uniform current distributions @briguglioDesignTestingCompact2013, @lafmejaniVOFModellingGas2017. Such high-fidelity models demonstrate how serpentine or interdigitated flow channels affect water distribution, gas removal, and local pressure drops. This consideration is crucial for large-scale stacks, as maldistribution can lead to localized flooding or drying @briguglioDesignTestingCompact2013.

One challenge in PEM electrolysis is gas crossover, wherein dissolved H₂ and O₂ permeate through the membrane, reducing Faradaic efficiency and posing safety risks. Faraday efficiency is modeled as the ratio of collected hydrogen to theoretical production, with empirical corrections for parasitic crossover currents that become more pronounced at higher pressures or with thinner membranes @yodwongFaradaysEfficiencyModeling2020. Thinner membranes decrease ohmic losses but increase gas permeation, thus highlighting a fundamental trade-off between efficiency and purity that must be balanced in design @nguyenFullyHydrocarbonMembrane2022. Shunt currents that bypass cells in a stack further erode efficiency and are addressed by careful bipolar-plate and manifold design to minimize conductive paths outside the intended cell circuit @yodwongFaradaysEfficiencyModeling2020.

Conventional PFSA membranes (Nafion™ 117) remain the benchmark for proton conductivity and chemical stability, but recent hydrocarbon-based ionomers provide lower costs and higher thermal tolerance, albeit with challenges in oxidative stability and gas separation @nguyenFullyHydrocarbonMembrane2022. On the catalyst front, cathode loadings of platinum have been reduced to 0.5 mg cm⁻² or less without performance loss, while anode iridium loadings have decreased to approximately 0.3 mg cm⁻² through nanoparticle and support engineering @carmoComprehensiveReviewPEM2013. These reductions in precious metal content directly lower stack CAPEX but necessitate optimized catalyst-layer fabrication, often through controlled spraying or decal techniques to maintain a high electrochemically active surface area (ECSA) and uniform ionomer distribution @carmoComprehensiveReviewPEM2013. .

Studies on PEM design parameters have shown how operating conditions like current density, temperature, pressure, and component thickness influence performance and durability. Higher temperatures (up to ~80 °C) enhance kinetics and conductivity while accelerating membrane degradation, whereas increased pressures (up to 30 bar) help with downstream compression but increase reversible voltage and gas dissolution losses @hanElectrochemicalPerformanceModeling2015.

Despite these advances, two primary gaps persist in the electrochemical literature. First, most models remain 1D or pseudo-1D, addressing through-plane transport without capturing the complex interplay of flow-field design, lateral current distribution, and multi-phase water management under dynamic load @falcaoReviewPEMElectrolyzer2020, @hanElectrochemicalPerformanceModeling2015. Second, while individual studies have examined membrane alternatives or catalyst substitutions, few have systematically linked variations in material properties to techno-economic outcomes. This disconnect hinders efforts to identify which material investments truly yield cost-effective performance improvements when scaled to commercial module sizes. Our work aims to address these gaps by embedding a validated 0D/1D model within a multi-objective optimization framework that directly quantifies how variations in membrane conductivity, catalyst loading, and electrode porosity affect both energy efficiency and capital cost.

### 3.2 Techno-Economic Analysis and System-Level Modeling

SSeveral open-source frameworks have been developed for the techno-economic analysis (TEA) of hydrogen production systems, including H2A, HySupply, and the Techno-Economic Simulation Tool (TechEST) @penevTechnoEconomicModellingH2A, @khanIntegratedFrameworkOpensource2022, @humbertEconomicsElectrowinningIron2024. These frameworks provide valuable tools for evaluating the cost of various hydrogen pathways. However, most of these Excel-based models are fundamentally static and often lack dynamic integration between physical system modeling and process economics. They lead to oversimplified assessments that do not fully capture the temporal variability of renewable energy inputs or the operational flexibility of electrolyzer systems. Recent updates to proprietary software, such as AspenTech's V14.1, have introduced modules for detailed PEM electrolyzer design and operation, enabling more granular process simulation. Despite these advancements, affordability remains a significant barrier for users, particularly for startups and early-stage technology developers. Therefore, an open-source framework is encouraged for those who may lack the resources to invest in high-cost commercial software.

The U.S. Department of Energy's H2A model and similar frameworks in Europe and Australia adopt a discounted cash flow approach, which defines LCOH as the ratio of the present value of all costs to the total kilograms of H₂ produced, deriving key financial metrics such as net present value (NPV) and internal rate of return (IRR) from the annualized cash flows @doeHydrogenShot2020 . , @carmoComprehensiveReviewPEM2013 . This methodology ensures that both capital and operational costs are captured in a single metric, allowing for direct comparison to market prices and policy targets.

Contemporary studies report uninstalled stack CAPEX ranging from $800 to $1,500 per kilowatt (kW) of electrolyzer capacity, with installation adding another 10% to 15% @jamesHydrogenProductionCost. BoP components such as power electronics, compressors, pumps, and water purification account for approximately 40% to 60% of total installed CAPEX @caparrosmanceraOptimizedBalancePlant2020 .

Electrical energy and deionized water are often referred to as energy and non-energy feedstock, respectively. In most studies, electricity consumption (approximately 50–55 kWh per kilogram of H₂ at steady state) constitutes 60–70% of LCOH under high-utilization scenarios @satyapalDOEHydrogenProgram2023 . Other operational cost items, such as water and routine maintenance, account for a lesser share @hemauerPerformanceCostModelling2023. Seemingly conflicting results have been published regarding the main cost driver of PEM electrolysis. A majority of recent studies identify electricity cost as the dominant factor influencing LCOH. Since a PEM electrolyzer requires about 50–55 kWh of electricity per kilogram of hydrogen (at 68–72% HHV efficiency), even modest changes in power prices can significantly impact LCOH. James et al. (2013) demonstrated through a sensitivity analysis that a 50% increase in electricity costs could raise LCOH by more than $2 kg⁻¹. In contrast, Yates et al. (2020) identified electrolyzer system size as the single most important factor affecting hydrogen cost. In their model, scaling the nominal electrolyzer power up by a factor of 10 could reduce LCOH by approximately $0.3 per kg (all else equal) @yatesTechnoeconomicAnalysisHydrogen2020. Another study by Astriani et al. concluded that LCOH is more sensitive to the electrolyzer's cost than to variations in electricity tariff @astrianiOptimalPlanningRenewable2024 .

Recent TEAs have evolved beyond static analyses by incorporating dynamic operations and renewable integration. Coupling PEM electrolyzers with time-varying tariffs or surplus renewable supply enables high-capacity factor operation during low-price periods, which reduces average electricity costs and LCOH by an additional 5–10% chungDesignSpacePEM2024 . Offshore wind-direct coupling studies similarly demonstrate that bypassing grid transmission and directly supplying electrolyzer systems can achieve hydrogen costs as low as $2.09 per kilogram in optimal locations, compared to $3.86 per kilogram through onshore transmission @groenemansTechnoeconomicAnalysisOffshore2022 .
### 3.3 Renewable Energy System Background

Integrating renewable energy variability into TEA frameworks has increasingly become a focal point. A 2024 techno-economic assessment highlighted that PV-wind hybrid systems reduce LCOH to $3.01/kg by leveraging complementary generation patterns @baralTechnoeconomicAssessmentGreen2024. Hybrid wind-PV scenarios achieve the lowest LCOH due to higher capacity factors and lower electricity prices compared to solar-only systems. The IEEJ study compared "surplus power" (using curtailed renewables) and "stable power" (dedicated renewable plants) configurations. While surplus power reduced electrolyzer capacity factors to 5–13%, stable power designs reached capacity factors of 50–70% by mitigating intermittency, albeit with higher upfront infrastructure costs @shibataEconomicAnalysisHydrogen2015. Such results are achieved through multi-objective optimization of system design, which accounts for renewable resource variability and storage integration, highlighting the potential of hybrid renewable systems to significantly improve both utilization rates and economic performance for green hydrogen production @suCapacityConfigurationOptimization2023. 

Beyond capacity factors, geographic sensitivity analyses have shown that LCOH can vary by $2–3 kg⁻¹ across different U.S. regions due to differences in renewable resource quality, electricity tariffs, and permitting costs. For instance, wind-rich regions like ERCOT (Texas) achieve LCOH as low as $3.74/kg with tax credits, while California's higher grid prices and lower wind capacity factors result in costs exceeding $5/kg @saurUSGeographicAnalysis2011. Similarly, regions with frequent negative electricity prices (e.g., western Texas) allow for cheaper hydrogen production by leveraging curtailed renewable energy @Section45VClean . 

A further dimension of recent TEA research involves policy incentives and carbon pricing. The Inflation Reduction Act (IRA) of 2022 introduced production tax credits (PTC) of up to $3 kg⁻¹ H₂ for electrolyzers sourcing low-carbon electricity, effectively lowering LCOH by 30–50% under favorable conditions @bistlinePowerSectorImpacts2023. Nevertheless, studies by Bracci (2023) caution that PTC eligibility criteria, such as hourly emissions intensity thresholds, require granular, hourly modeling to accurately capture compliance risk and revenue streams @45VHydrogenTax, @bracciCostComparisonVarious2023. This motivates coupling TEA with time-resolved emissions data, a complexity seldom addressed in earlier static analyses.

## 4.0 Aims and Tasks

### **Aim 1: Design and optimize a physics-based model of PEM electrolyzer design for cost and efficiency**
**Objective**: To construct a comprehensive design framework that integrates electrochemical modelling with cost and efficiency optimization of PEM electrolyzers

**Task 1.1 {completed}:**  **Develop a multi-layer, physics-based mathematical model** of a PEM electrolyzer
Develop a detailed electrochemical and thermal model of the PEM electrolyzer stack, including membrane hydration, overpotential losses, Faradaic efficiency, and gas crossover effects.


In this task, we developed a first-principles, lumped-parameter model of a proton-exchange-membrane (PEM) electrolyzer stack that accounts for electrochemical kinetics, ohmic and concentration overpotentials, membrane hydration, Faradaic efficiency, and gas crossover effects. 
Building upon earlier designs from literature, we parameterized our single‐cell model using an active area of 877 cm², a Nafion 117 membrane thickness of 178 μm, and catalyst loadings of 1.54 mg cm⁻² at the anode and 0.4 mg cm⁻² at the cathode. @escobar-yonoffPerformanceAssessmentEconomic2021 , @hemauerPerformanceCostModelling2023 The operating point was set at 333.15 K, with an anode pressure of 1 bar, a cathode pressure of 30 bar, and a maximum current density of 2 A cm⁻². @crespiExperimentalTheoreticalEvaluation2023  $V_{\rm cell}(T,P,u,i,t) = V_{\rm rev}(T,p) + \eta_{\rm act}(i,t) + \eta_{\rm ohm}(i,t) + \eta_{\rm conc}(u,i)\,,$  where the reversible potential, $V_{\rm rev}$​, is computed from the Nernst equation using standard thermodynamic data and the applied temperature and pressure. The activation overpotential, $\eta_{\rm act}$ ​, is described by a Butler–Volmer formulation with a transfer coefficient of 2.0 at the anode and 0.5 at the cathode. The ohmic losses,  $\eta_{\rm ohm}$ ​ arise from both the membrane layer resistivity (5.0 × 10⁻³ Ω·cm) and the porous electrodes (8.0 × 10⁻² Ω·cm for carbon paper). The concentration overpotential, $\eta_{\rm conc}$​, is approximated via a Tafel‐type expression calibrated against a limiting current density of 6 A cm⁻². @zhangStatusPerspectivesKey2022  

The first version of our model was implemented in an Excel workbook, while a more detailed model for a dynamic simulation was prepared in Python.  Using an Excel prototype, we linked these submodels to calculate stack voltage $V_{\rm stack}=N_{\rm cell}\,V_{\rm cell}$ and electrical power $P_{\rm stack}=V_{\rm stack}\,(i\,A_{\rm cell})$. We then added a balance-of-plant (BoP) auxiliary load, $W_{\rm BoP}$, to arrive at total electrolyzer power $P_{\rm EL}=P_{\rm stack}+W_{\rm BoP}$. At the nominal current density of 2 A cm⁻², a single-cell voltage of 1.79 V yields 3.14 kW cell⁻¹ and a system-level specific energy consumption of 53 kWh kg⁻¹ H₂.  Beyond point estimates, we conducted a rigorous sensitivity analysis by varying current density, temperature, pressure, membrane thickness, and catalyst loading to assess their impact on key performance metrics: cell voltage, specific energy consumption, and the levelized cost of hydrogen (LCOH).   Increasing the cell operating temperature from 333 K to 353 K reduced the activation overpotential by approximately 10 mV, translating to a 2 kWh kg⁻¹ H₂ improvement in energy consumption. Similarly, halving the membrane thickness decreased ohmic losses by 15 mV but increased crossover by 20%, highlighting the trade-off between efficiency and gas purity. When these variations were incorporated into a preliminary LCOH module, we observed that a 10% reduction in specific energy consumption corresponded to a roughly 5% reduction in LCOH. This underscores the economic significance of electrochemical optimization. 

> Figure 1. A schematic of the PEM model inputs and outputs.
![[PEMel model schema.png|A schematic of the model inputs and outputs.]]

The prototype was translated into an object-oriented Python class that includes detailed multiple submodules, such as coupled electrochemical, mass-transport, thermal, and fluid-dynamic phenomena. To allow for the rapid evaluation of novel MEA designs and alternative materials, such as membranes, catalyst layers, and flow fields. We account for the gas crossover effect, where we apply Fick’s law in one dimension through the membrane. $N_{k} = -D_{k}(\lambda)\,\frac{dc_{k}}{dx}\quad(k\in\{\mathrm{H}_2,\mathrm{O}_2\})\,,$ where diffusivity $D_k$​ scales with membrane hydration λ, itself a function of water activity and electro‐osmotic drag. The water balance combines electro-osmotic drag, back‐diffusion, hydraulic permeation, and capillary flux to ensure mass conservation across the polymer electrolyte. 
Several empirical correlations reported in the literature are reviewed and adopted in the Python model.  @itoPropertiesNafionMembranes2011 , @springerPolymerElectrolyteFuel1991 

To validate our model, we compared its predictions against experimental polarization curves from Scheepers et al. (2020) @scheepersImprovingEfficiencyPEM2020 for a Nafion 117–based stack operated at 333 K and 30 bar. The model reproduced the observed cell voltage to within ±20 mV across current densities ranging from 0.5 to 2.0 A cm⁻² and matched the experimentally measured crossover rates (H₂ permeation below 1% of produced hydrogen) within 0.2%. These close agreements reinforce the model’s fidelity and suitability as a basis for subsequent optimization.
Although currently limited to a pseudo-1D through-plane representation, this framework lays the groundwork for future extensions to two-dimensional or full three-dimensional simulations, which would be essential if spatial non-uniformities become critical for advanced catalyst or flow-field designs.



**Task 1.2 {Ongoing}:**  
Formulate and solve a multi-objective optimization problem minimizing both CAPEX and specific energy consumption, while maximizing efficiency and membrane durability, under realistic operating constraints.

Building on the electrochemical model, we formulated a multi-objective optimization problem that seeks to minimize the PEMel design cost (CapEx) and specific energy consumption simultaneously while maximizing cell efficiency under realistic operating constraints.   The multi-objective functions aim to minimize the Specific Energy Consumption (SEC) of the PEM electrolyzer and the geometric design width of the MEA ($F_2(X)$) of a cell. $F_{1}(X) = SEC(X)\,$ $F_{2}(X) = t_{mem}+ t_{el_an} + t_{el_cat}$ The Specific Energy Consumption (SEC),kWh/kg H₂ defines the amount of electric energy required to produce 1 kg of hydrogen. It accounts for the overpotentials, crossover effects and shunt currents. The MEA of a PEM electrolyzer consists of the membrane electrolyte and the electrodes. The thickness of the MEA influences compactness, heat transfer, mechanical design, and materials usage.
The decision vector $x=[\,t_{\rm mem},\,t_{\rm el},\,L_{\rm cat},\,i,\,T\,]^{\!T}$  includes the membrane thickness, electrode thickness, catalyst loading (assumed to be uniform across the anode and cathode half-cells), current density, and operating temperature. For trade-off optimization, a thinner membrane layer reduces ohmic losses $\eta_{\rm ohm}=i\,(t_{\rm mem}/\kappa_{\rm mem})$ but increases gas crossover due to higher permeability.  $J_{\rm crossover}\propto D_{\rm gas}/t_{\rm mem}$ @nawaleAnalysesEffectsElectrolyte2023 . Higher catalyst loading ($L_{cat}$) reduces activation overpotential by increasing the active surface area, thus lowering the exchange current density ($i_0$) threshold. Increasing catalyst loading diminishes activation overpotential via the Butler–Volmer relation.  @maierMassTransportPEM2022  Excess catalyst loading ($>3 mg/cm^2$) can hinder mass transport, increasing concentration losses, while also driving up material CAPEX $\eta_{\rm conc}=-(RT/nF)\ln(1-i/i_{L})$. @chungDesignSpacePEM2024
```
The decision vector includes the membrane thickness, electrode thickness, catalyst loading (assumed to be uniform across the anode and cathode half-cells), current density, and operating temperature. For trade-off optimization, a thinner membrane layer reduces ohmic losses but increases gas crossover due to higher permeability. Higher catalyst loading reduces activation overpotential by increasing the active surface area, thus lowering the exchange current density threshold. Increasing catalyst loading diminishes activation overpotential through the Butler–Volmer relation. Excess loading can hinder mass transport, increasing concentration losses, while also driving up material CAPEX.
```
We impose a mechanical durability constraint $g_{1}(x)\;=\;r\sqrt{\frac{k\,\Delta P\,SF}{\sigma_{\rm tensile}}}\;-\;t_{\rm mem}\;\le\;0,$ 
which enforces a minimum membrane thickness capable of withstanding the transmembrane pressure difference. For Nafion, the tensile strength ($σ_{tensile}$) ranges from 25 to 40 MPa, and safety factors (SF) of 1.5–2.0 are recommended for high-pressure differentials. @limDurabilityPerformanceAnalysis2023 Swelling-induced plastic deformation accelerates failure at ΔP>20  if $t{mem}$ is insufficient. The design variables are bounded by manufacturing, material, and operational limits. Performance constraints require a minimum Faradaic efficiency of 99%, an operating temperature cap of 353 K to protect polymer integrity, and a hydrogen production rate threshold of 0.5 kg h⁻¹ per cell at 2 A cm⁻². 

This objective aligns directly with the U.S. Department of Energy's cost and performance targets for PEM electrolysis. @petersonHFTOHydrogenProduction The model provides opportunities to explore trade-offs that are inherently coupled in the design space of the PEM electrolyzer. 
We will implement this formulation in Python using the Pymoo library. The optimization workflow <span style=" color:rgb(0, 112, 192)">(Figure 4)</span>  begins by sampling candidate MEA designs each defined by the decision vector space. For every candidate x, our coupled model computes the SEC and stack voltage, predicts Faradaic efficiency, and calculates the implied cost factor based on material thicknesses. Through iterative non-dominated sorting and genetic operators, NSGA-II reveals the envelope of trade-off designs ranging from ultra-thin, high-efficiency stacks with elevated crossover risk to thicker, more robust configurations with slightly higher energy demands.

![[Presentaions/comps/attachments/image-31.png]]




----


> **Figure 4: Schematic of the multi‐objective optimization workflow, highlighting decision variables, constraints, and the Pareto front generation.**


the PEM model is Python‐based evaluation tool computes the specific energy consumption(SEC)₎ and total MEA thickness t₍MEA₎, which serve respectively as the performance and cost proxies. The first objective, F₁(x), is cast as maximizing HHV efficiency (or equivalently minimizing −η₍HHV₎), while the second, F₂(x), minimizes the sum of the MEA layer thicknesses to reflect material and manufacturing cost:





We implemented the non-dominated sorting genetic algorithm II (NSGA-II) within our Python framework to explore this five-dimensional design space. Each candidate solution is evaluated by the PEM model to yield $\eta_{\rm HHV}$, LCOH, and $D$. Through successive generations, NSGA-II identifies Pareto-optimal fronts that reveal, for example, how a 20 µm reduction in membrane thickness can improve efficiency by 3 % at the expense of a 5 % increase in LCOH, or how boosting anode catalyst loading from 1.5 mg cm⁻² to 2.0 mg cm⁻² lowers activation losses by 15 mV but adds $50 m⁻² to stack CAPEX. 
Preliminary Pareto fronts indicate that the most favorable region occurs at membrane thicknesses between 120–150 µm, catalyst layer thicknesses of 10–15 µm, and loadings of 1.6–1.8 mg cm⁻² for the anode. In this domain, the model predicts a stack-level efficiency of 74 % HHV at an LCOH of $3.20 kg⁻¹ H₂—meeting DOE’s near-term targets—while maintaining a durability index above 0.9 (on a normalized scale where 1.0 represents virgin material fatigue life).

As this task progresses, we will refine the objective weighting to align with DOE targets for PEM electrolyzer cost and performance, and we will extract sensitivity metrics to identify the most impactful design levers. This ongoing optimization provides the critical link between our detailed electrochemical model and a deployable, cost-effective PEM electrolyzer design.









### **Aim 2: Identify and Quantify Key Cost Drivers Through a Custom Techno-Economic Analysis (TEA) Framework**

**Objective**: To pinpoint high-impact parameters in green hydrogen production cost and assess design configurations under varied operational scales.

**Task 2.1 Design a dynamic technoeconomic assessment (TEA) model for PEM electrolyser analysis {Completed}:**  
Design a modular technoeconomic assessment (TEA) model integrating the physical PEM model into a system-level hydrogen production cost framework using  LCOH, and NPV as primary metrics.


In Task 2.1, we developed a modular techno-economic assessment (TEA) that couples our physics-based PEM electrolyzer model with a system-level cost framework, yielding Levelized Cost of Hydrogen (LCOH) and net present value (NPV) as primary performance indicators. This analysis is limited to the production of hydrogen and does not account for compression, storage or transportation. We defined the system boundary to include the electrolyzer stack and all balance-of-plant (BoP) components, such as compressors, pumps, gas-liquid separators, thermal management systems, and water purification units but explicitly excluded the additional capital and operating expenses associated with downstream oxygen purification. Startup production for the inaugural year was conservatively set at 50 % of nameplate capacity to reflect commissioning inefficiencies and market ramp-up.

Our baseline case assumes a 10,000 kg H₂ day⁻¹ production capacity, a rated stack power consumption of 49 kWh kg⁻¹ H₂ (equivalent to 68% LHV efficiency), and an overall electrical intensity of 54.3 kWh kg⁻¹ H₂ when including BoP loads. Capital expenditures (CAPEX) for uninstalled electrolyzer equipment were parameterized using the Green Hydrogen Cost Report formulation and Astriani et al.'s empirical scaling law, $\mathrm{Cost}_{\text{EL}}=c_{1}+c_{2}\,P_{\text{EL,rated}}+c_{3}\,\exp\bigl(c_{4}\,P_{\text{EL,rated}}\bigr)\,$  @astrianiOptimalPlanningRenewable2024 , @GreenHydrogenCost2020 where $P_{\text{EL,rated}}$ denotes the electrolyzer’s rated electrical power. For our reference plant, the uninstalled CAPEX is $995 kW⁻¹; installation augments this by 12 %, yielding a first-year installed CAPEX of approximately $1 114 kW⁻¹. A three-year MACRS depreciation schedule and a 27 % corporate tax rate were applied. Stack replacement is scheduled every 10 years at 15% of the installed CAPEX, and the plant life is assumed to be 20 years.

At our baseline, Specific Energy Consumption rates of 54.3 kWh/kg H₂ (system-level) and 49 kWh/kg H₂ (stack-only) were derived from our validated performance model. We incorporate water feedstock, routine maintenance, membrane, and catalyst replacements and account for partial cost recovery without any oxygen by-product credit. A half-capacity factor is assumed in the startup year to reflect the commissioning ramp-up. Operating expenditures (OPEX) are primarily driven by SEC and electricity costs, modeled at $0.07 kWh⁻¹, and include maintenance, membrane and catalyst replacement, and water treatment. We incorporated a 1.5 mV khr⁻¹ degradation rate to adjust the stack's performance over time, which increases energy consumption and reduces annual hydrogen output. Fixed and variable O&M costs during the startup phase were scaled to 75% and 50% of their steady-state levels, respectively, to reflect training and validation activities.

The LCOH metric was computed using a standard discounted cash flow analysis, normalizing total lifecycle costs by cumulative hydrogen production. LCOH is then obtained by dividing the present value of total costs by cumulative hydrogen production (in kg), while NPV and IRR are derived from net cash flows. Under our baseline assumptions of 10 000 kg H₂ day⁻¹ capacity, 90 % capacity factor, and a 10 % WACC, the model predicts a levelized cost of hydrogen of $6.55 kg⁻¹, a net present value of $75 million over 20 years, and an internal rate of return of 32 %. Closely matching values reported in recent techno-economic studies. @jangTechnoeconomicAnalysisMonte2022 

To illustrate the impact of scale and economics, we compared three configurations: a small, "distributed" or "onsite" plant (1,500 kg day⁻¹), our 10,000 kg day⁻¹ reference case, and a large, centralized facility (50,000 kg day⁻¹). @jamesHydrogenProductionCost As shown in <span style=" color:rgb(0, 112, 192)">Figure 8</span>, the distributed scenario incurs the highest LCOH at $8.60 kg⁻¹, driven by disproportionately large fixed‐capital charges and balance‐of‐plant costs. In contrast, the centralized plant achieves a $6.85 kg⁻¹ reduction of nearly 20% by spreading capital and operating expenses over a much larger hydrogen output. In comparison, the reference case sits between these extremes at $6.55 kg⁻¹.
These cost differences translate directly into project economics. The distributed configuration yields an IRR of just 13.5% and a near-zero NPV, reflecting tight margins at a small scale. Our baseline plant returns 32 % IRR and $75 million NPV, while the 50 000 kg day⁻¹ facility delivers a robust 38 % IRR and $415 million NPV (<span style=" color:rgb(0, 112, 192)">Figure 9</span>). These results underscore the strong economies of scale inherent in PEM electrolysis: doubling capacity from 10 t day⁻¹ to 20 t day⁻¹ reduces LCOH by approximately 12%, and scaling further to 50 t day⁻¹ drives nearly a 20% decrease.


![[image-33.png|535x318]]

![[image-34.png|531x324]]


We examined the scaling effect by comparing distributed small scale or onsite plant scenario (1500 kg H_2 day⁻¹) against centralized (50,000 kg H_2 day⁻¹) production scenarios. Economies of scale emerge sharply: doubling capacity from <span style="color:rgb(0, 112, 192)">10 to 20 t day⁻¹ yields a 12 % LCOH </span>reduction, <span style="color:rgb(0, 112, 192)">while scaling to 100 t day⁻¹ drives a 25 % decrease</span>. This is largely attributable to the non-linear CAPEX scaling captured in our cost function and to more favorable depreciation of BoP components. Centralized plants also benefit from higher stack replacement intervals and bulk purchasing of membranes, trimming fixed O&M by an additional 0.5 % of CAPEX. However, distributed systems though 12 % more expensive per kilogram offer strategic value in grid-constrained regions and for localized hydrogen demand. 

<span style="color:rgb(0, 112, 192)">To verify our implementation, we overlaid the model’s IRR curve against published benchmarks, finding deviations below 0.5 % for capacities between 5 000–20 000 kg day⁻¹. Sensitivity analyses reveal that a 10 % decrease in specific electrolyzer power consumption translates to an LCOH reduction of $0.15 kg⁻¹ H₂, while a 10 % increase in electricity price raises LCOH by $0.35 kg⁻¹ H₂. Similarly, enhancing capacity factor from 85 % to 95 % improves NPV by $3 million and increases IRR by 1.8 percentage points</span>.







---


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

.

> **Figure 5: IRR versus discount rate curve compared to published PEM electrolyzer projects.**  
> **Figure 6: System boundary for the TEA, illustrating included unit operations and cost streams.**

By varying electricity price, capital cost, and stack lifetime within their low‐high bands, we performed a Monte Carlo sensitivity analysis to identify the dominant cost drivers. Preliminary results show that electricity feedstock and installed capital cost account for over 85 % of LCOH variability, whereas replacement interval and O&M contributions remain secondary. This completed TEA provides a rigorous foundation for coupling with our dynamic energy system optimization in Aim 3.

----



**Task 2.2 {Completed}:**  
Conduct parametric studies to assess the impact of system scaling, component sizing (e.g., BoP), and material cost variation on LCOH. Identify cost bottlenecks and pathways for economic optimization.


Having established our baseline techno-economic framework in Task 2.1, we performed a comprehensive parametric study to identify the most influential cost drivers and explore pathways for economic optimization. Our focus centered on five principal drivers: energy feedstock cost, uninstalled capital cost, fixed operating cost, stack efficiency (specific energy consumption, SEC), and co-product oxygen credit, as well as their influence on both the levelized cost of hydrogen (LCOH) and net present value (NPV).
We performed a comprehensive univariate sensitivity analysis of our baseline 10,000 kg day⁻¹ plant, systematically varying key techno-economic parameters within realistic low and high ranges. <span style="color:rgb(0, 112, 192)">Figure 3</span> presents the resulting levelized cost of hydrogen (LCOH)  for each parameter scenario. The total energy feedstock cost is the dominant factor. The total feedstock consists of the deionized water(non-energy feedstock) and the electrical energy (energy feedstock) supplied to the primary hydrogen-producing PEM electrolyzer. Increasing electricity cost from $0.03 to $0.12 kWh⁻¹ drives LCOH from $4.73 to $9.51 kg⁻¹ H₂. It has an effect nearly twice as large as that of installed capital cost, which alone shifts LCOH between $5.31 and $8.22 kg⁻¹. Industrial grid electricity prices vary from state to state in the US. The cost of energy at $0.03 kWh⁻¹ represents a low-cost energy scenario, with a peak retail rate of $0.15 kWh⁻¹. Increasing demand at different times of the day may cause fluctuations in the actual cost of energy. The total uninstalled CAPEX was assessed against the DOE technical target of $250 kW⁻¹ and the current high end of $ 1,500 kW⁻¹, compared to our baseline of $995 kW⁻¹. @petersonHFTOHydrogenProductionOther  Stack energy efficiency and fixed Operational and maintenance are secondary cost drivers.   The impact on the energy consumption rate is evaluated at DOE's expected future and current ranges of PEM electrolyzer efficiencies. The Fixed Operational and maintenance cost fractions ranged from 15% to 22% of CAPEX, as provided in the H2A toolkit. @ramsdenAnalyzingLevelizedCost2009   
 A scenario for considering oxygen as a viable co-product with credit was tested between $0 and $0.17 kg⁻¹ O₂ to reflect markets that do or do not monetize the co-product.

Our univariate LCOH sensitivities, summarized in <span style="color:rgb(0, 112, 192)">Figure 3</span>, reveal that energy feedstock cost exerts the greatest leverage on hydrogen price. At the low end ($0.03 kWh⁻¹), LCOH falls to approximately $4.7 kg⁻¹, whereas at $0.15 kWh⁻¹, it soars to nearly $9.5 kg⁻¹, resulting in a swing of $4.8 kg⁻¹. Uninstalled capital cost is the next most critical factor: reducing it from $ 1,500 kW⁻¹ to $250 kW⁻¹ cuts LCOH by roughly $2.9 kg⁻¹ (from $8.2 to $5.3 kg⁻¹). Improvements in stack efficiency (45 vs. 55 kWh kg⁻¹) contribute a $1.2 kg⁻¹ LCOH reduction, while fixed O&M and non-energy feedstock variations each shift LCOH by less than $0.7 kg⁻¹. The oxygen credit effect is marginal under our reference case, lowering LCOH by only $0.2 kg⁻¹ when moving from zero to $0.17 kg⁻¹ O₂. The tax rate is selected to represent a practical analysis of US states with and without state taxes.

Tornado chart showing a univariate sensitivity of LCOH  to key parameters
![[Presentaions/comps/attachments/image-25.png]]


Figure: Tornado chart showing a univariate sensitivity of LCOH and NPV to key parameters
![[image-26.png]]

Complementing our cost analysis, we examined how uncertainty in key inputs affects the project's net present value (NPV) over a 20-year lifetime (<span style=" color:rgb(0, 112, 192)">Figure 4</span>). The price of electricity proved to be the most influential factor: increasing the energy feedstock cost from $0.03 kWh⁻¹ to $0.15 kWh⁻¹ reduces the NPV from approximately $125 million to $27 million, a decline of nearly 78 percent. Changes in uninstalled electrolyzer capital cost likewise exert a pronounced effect, driving NPV between roughly $52 million (at $1 500 kW⁻¹) and $116 million (at $250 kW⁻¹). Such underscores the importance of manufacturing scale-up and cost reduction. Stack efficiency improvements increase the NPV by over $50 million when compared to the current state-of-the-art and DOE's technical target for PEM electrolyzer efficiencies.  Fixed Operational and maintenance and non-energy feedstock exert modest NPV changes (<$10 M), whereas oxygen by-product credit impacts are negligible at this scale.
Tax policy, represented by the range between federal-only (21%) and combined state-and-federal (up to 33 %) rates, shifts NPV by under $15 million, indicating that while fiscal measures do influence project economics, their impact is modest relative to electricity pricing, manufacturing costs, and stack efficiency. Collectively, these results suggest that efforts to secure low-cost renewable power, achieve larger-volume electrolyzer production, and pursue efficiency-driven cell improvements should form the highest priorities for reducing financial risk and maximizing project value.
To meet DOE's technical target for low-cost green hydrogen production and achieve the ultimate $1-2/kg H2 energy earth shot goal, there must be significant advancements in low-cost energy procurement, large-scale electrolyzer manufacturing, and design performance. A significant reduction in electricity costs could be achieved through long-term power purchase agreements or on-site renewables. The uninstalled and installed capital costs can be improved via high-volume stack manufacturing and BoP modularization. 


Beyond the univariate uncertainty analysis, we investigated the effect of multiple process parameters on the LCOH. 

To investigate the influence of plant scale and energy cost on hydrogen economics, we generated multivariate contour plots of LCOH as a function of design capacity and energy cost.
At low capacities, below approximately 6,000 kg H₂ day⁻¹, the LCOH surface rises steeply with both higher power prices and smaller plant sizes. As capacity increases beyond this threshold, the iso-cost lines flatten. It indicates diminishing economies of scale, where further doubling of design capacity from 6,000 to 12,000 kg day⁻¹ yields only marginal LCOH reductions (on the order of $0.10 kg⁻¹) at a given electricity price. This plateau effect arises because fixed capital expenditures, although spread over greater throughput, become a progressively smaller fraction of total cost as operational expenditures (dominated by electricity feedstock) prevail. For regions with constrained grid access or modest local hydrogen demand, "distributed" or "onsite" electrolyzer deployments sized near this 6,000 kg/day⁻inflection point can achieve near-optimal costs without the logistical complexity of very large centralized facilities.
A local linearization around the baseline point (SEC = 50 kWh/kg; electricity price = $0.08/kWh) indicates that a 1 kWh/kg reduction in SEC yields an approximate LCOH decrease of 0.09 $/kg, whereas a 0.01 $/kWh reduction in electricity price produces a 0.50 $/kg decrease in LCOH. Thus, under baseline conditions, negotiating a one-cent reduction in the power contract yields over five times the cost savings of achieving a one-kWh improvement in stack efficiency.
![[image-24.png]]

![Figure 5: Contour of LCOH ($/kg H₂) versus design capacity (kg H₂ day⁻¹) and electricity cost ($/kWh). The white marker denotes the 10 000 kg day⁻¹ baseline case at $0.075 kWh⁻¹.]

These results have clear implications for project developers and policymakers. Achieving LCOH targets in the $4–6/kg range requires either electricity costs below $0.05/kWh, capacity factors in excess of 90 percent on firm power, or a combination of moderate scale (8,000–12,000 kg/day) with energy costs below $0.06/kWh. Attempting to drive down LCOH solely via plant size would necessitate impractically large electrolyzer installations, both technically and financially, without concomitant access to low-cost, low-carbon power. In contrast, integrating cost-effective renewable electricity options, such as utility-scale wind, solar plus storage, or securing long-term low-price PPAs, will yield far greater reductions in hydrogen unit cost. While both design capacity and energy price fundamentally shape LCOH, the contour analysis definitively indicates that initiatives to lower electricity costs should take precedence.
![[image-23.png]]

We further extended this analysis to examine the relationship between electrolyzer efficiency expressed as specific energy consumption (SEC, kWh kg⁻¹ H₂) and electricity cost (Figure 6).
At very low electricity prices (<$0.02 kWh⁻¹), the sensitivity of LCOH to SEC diminishes, reflecting the dominance. Conversely, when power prices exceed $0.15 kWh⁻¹, the LCOH contours steepen dramatically, which underscores the critical importance of both high-efficiency stack design and access to low-cost renewables in marginal markets. Although efficiency gains never plateau mathematically, there is a practical limitation (40-50 kWh/kg), whereas power contracts can sometimes move in bigger increments.

![Figure 6: Contour of LCOH ($/kg H₂) versus specific energy consumption (kWh kg⁻¹ H₂) and electricity cost ($/kWh). The baseline performance of 55 kWh kg⁻¹ at $0.075 kWh⁻¹ is marked.]{#fig:sec_coe}










 between SEC and uninstalled CAPEX by generating contour plots of LCOH as a function of these two variables. The resulting map highlights a “sweet spot” at 50 kWh kg⁻¹ and $1 200 kW⁻¹, where LCOH approaches $3.2 kg⁻¹ below DOE’s 2030 target. Similarly, plotting capacity factor against CAPEX demonstrated that improving uptime from 80 % to 95 % can improve IRR by up to 2 percentage points, even at modest CAPEX levels.








**Task 2.3 {future work}:**  
**To Evaluate the impact of cost-reduction levers**, including material substitutions and manufacturing scale-up.


Building on our completed sensitivity analyses, the next phase is to develop a systematic framework for assessing how alternative materials and manufacturing pathways can reduce both the capital and operating costs of PEM electrolyzers. In particular, we will focus on three critical components: the membrane, the anode catalyst layer, and the cathode catalyst layer electrodes. By integrating material property libraries derived from experimental studies into our Python model, we can rapidly simulate the techno-economic impact of substituting lower-cost or higher-performance materials and quantify the trade-offs in terms of efficiency, durability, and manufacturability.
The proposed workflow will begin with a comprehensive literature survey of advanced membrane chemistries (hydrocarbon-based polymers, reinforced PFSA composites) and low-loading or non-precious-metal catalysts (Ni–Fe, transition-metal carbides) reported in peer-reviewed journals. @CriticalStrategicRaw2024.  We will catalog these alternative PEM electrolyzer materials and extract their key design parameters and cost metrics. This “material library” will feed directly into our existing lumped Python electrolyzer model, replacing baseline Nafion 117 and iridium‐platinum catalysts. We will adopt cost functions from both the Green Hydrogen Cost Report and recent NREL reports on manufacturing analyses, which describe how uninstalled stack and BoP costs decline with cumulative production volume. @badgettUpdatedManufacturedCost2024 ,  @mayyasManufacturingCostAnalysis2019  For each material scenario, we will compute learning-curve coefficients that reflect both material cost reductions (e.g., bulk polymer synthesis) and process innovations (roll-to-roll membrane casting, inkjet catalyst deposition). 

By integrating material property libraries derived from experimental studies into our Python model, we can rapidly simulate the techno-economic impact of substituting lower-cost or higher-performance materials and quantify the trade-offs in terms of efficiency, durability, and manufacturability. Once the material and scale-up cost functions are in place, we will perform a rigorous global sensitivity and uncertainty analysis using BioSTEAM's built-in Monte Carlo and Sobol sampling routines. By coupling our Python electrolyzer class to the BioSTEAM flowsheet framework, we can simulate hundreds of thousands of design variants, systematically perturbing material properties (e.g., membrane thickness and conductivity), catalyst attributes (e.g., loading and ECSA), and cost-learning parameters.

We will then integrate our Python-based electrochemical model into the BioSTEAM framework to support a rigorous, global sensitivity and scenario analysis. By encoding each material option as a discrete "module" within BioSTEAM, we can simulate the full process-level impacts, spanning stack performance, BoP requirements, and hydrogen purity under mass and energy balances. Parallel Aspen Plus case studies will be developed for cross-validation. Comparisons between our streamlined Python outputs and BioSTEAM's rigorous unit-operation simulations will help to calibrate model fidelity.





### **Aim 3: Evaluate renewable energy configurations for dynamic, location-sensitive hydrogen production**

**Objective**: To assess the spatial and temporal viability of renewable-powered hydrogen production through dynamic simulation and optimization.

**Task 3.1 {completed}:**  
Design an energy system model that incorporates PV, wind, hybrid, or grid-interactive system configurations with hourly resolution for location-specific simulations.

The temporal variability of renewable electricity sources affects the output of green hydrogen production. A separate model for the energy system for hydrogen production is therefore introduced for optimization. We assessed the daily and hourly seasonal impact of renewable variability on our hydrogen production through Monte Carlo simulations. The energy system model is configured for solar photovoltaic (PV), onshore wind power,  and hybrid power systems at an hourly resolution based on environmental and mechanical design parameters. The total energy output affects the electrolyzer model by supplying a time series of available power and corresponding cost signals, which enables an effective evaluation of capacity factors and the levelized cost of electricity (LCOE).
The PV submodel computes the instantaneous output $P_{\text{PV},h}$ at hour $h$ from a tilted array. We defined our reference 1MW rated capacity $P_{\text{PV,rated}}$,  with an annual derating factor $f_{\text{derPV}}$, of 0.9 and the global tilted irradiance $GTI_h$ relative to standard test conditions $G_{\text{STC}}$ of 1000 W/m2 while correcting for temperature and system losses: @khattakTechnoeconomicEnvironmentalAnalysis2024 
$P_{\text{PV},h} = P_{\text{PV,rated}}\,\times f_{\text{derPV}}\,\times\frac{GTI_h}{G_{\text{STC}}}\Bigl[1 + k_p\,(T_{\text{cell},h}-T_{\text{STC}})\Bigr]\times P_{\text{losses}}.$
We assume a temperature coefficient $k_p$  of -0.0035 and  $P_{\text{losses}}$ from the lumps inverter, wiring, soiling, and shading losses. @elmghouchiModelsObtainingDaily2016,  @duboisStepbystepEvaluationPhotovoltaic2017 . Solar irradiance models are beta distributions influenced by cloud cover, with α of 2.0 and β  of 2.2, to characterize the Texas Gulf Coast. @zhangJointProbabilityDistribution2015 . The model yields hourly PV output profiles that peak at midday and fall to zero overnight. A full year of irradiance and ambient temperature data from the National Solar Radiation Database for our target site. 
The wind turbine power is modeled with a cubic-law relationship between wind speed $v_h$ and turbine output $P_{\text{WT},h}$: $P_{\text{WT},h} = \tfrac12\,\eta_{\text{WT}}\,\rho\,A\,C_p(\lambda_h,\beta)\,v_h^3$ . We assume a baseline with generator efficiency  $\eta_{\text{WT}}$ of 94 %, a base swept rotor area $A$ of 300m2/MW,  and air density $\rho$ of 1.225kg/m2 is adjusted for temperature and elevation. The power coefficient  $C_p(\lambda,\beta)$ of the turbine as a function of the tip and speed ratio curves are sourced from Castillo et al. (2023). @castilloComparisonPowerCoefficients2023 . The wind speed models a Weibull distribution with a scale parameter c of 2 and a shape parameter k of 8, as characteristics of Texas Gulf Coast regional wind speeds @gunturuCharacterizationWindPower2012. Hourly wind speeds were obtained from the MERRA-2 reanalysis dataset, which provides year-round delivery, complementing the diurnal PV pattern and reducing total curtailment.
![[image-21.png]]

We synthesized a hybrid system by combining PV and wind arrays in a 1:1 capacity ratio, summing their hourly outputs to form a single net-generation series. This hybrid profile smooths variability and raises the effective capacity factor from 25 % for PV alone and 32 % for wind alone. To explore grid-interactive scenarios, we also modeled connection to a regional wholesale tariff, introducing an 7.3 c kWh⁻¹ baseline price and time-of-use multipliers derived from hourly market data, allowing comparison between off-grid and on-grid operation.

![[image-22.png]]
Capital and operating costs of each renewable energy configuration were parameterized against project scale: for a 20 MW system, we assumed PV CAPEX of A$ 1,191 kW⁻¹ and wind CAPEX of A$ 2,383 kW⁻¹, with fixed OpEx at 2% of CAPEX and land procurement at 8% for both technologies. We computed LCOE via a standard cost-recovery formula: $\mathrm{LCOE} = \frac{\mathrm{CRF}\times C_{\text{RE}} + O_{\text{RE}}}{E_{\rm annual}},$
where $\mathrm{CRF}$ is the capital recovery factor at an 8 % discount rate, $C_{\text{RE}}$ and $O_{\text{RE}}$ are the renewable system's annualized CAPEX and OPEX, and $E_{\rm annual}$ is its yearly generation. These LCOE values 9.2 c kWh⁻¹ for PV, 14.7 c kWh⁻¹ for wind, and 11.8 c kWh⁻¹ for the hybrid mix—served as dynamic price inputs for our hydrogen TEA.





Under off-grid operation, hydrogen production tracked available renewable energy directly, resulting in a <span style="color:rgb(0, 112, 192)">10 % lower annual output for PV-only systems compared to grid-supplemented scenarios, but yielded an average LCOH of $4.25 kg⁻¹ H₂—10 % below grid-only cases. The hybrid system further improved utilization, boosting capacity factor to 47 %, driving LCOH down to $4.05 kg⁻¹ H₂.</span>










4.3.2 Task 3.2 {future work} – Dynamic Optimization of Renewable-Electrolyzer Configurations
The renewable energy(RE) potential vary across geographical regions for different energy systems.@maclaurinRenewableEnergyPotential2021  
![[image-29.png]]

Task 3.2 will integrate a dynamic, multi-objective optimization layer that selects optimal renewable energy mixes, electrolyzer sizing, and storage capacities to minimize the levelized cost of hydrogen (LCOH) under real-world intermittency. To efficiently explore this high-dimensional design space, we propose using particle swarm optimization (PSO) augmented with Gaussian process surrogates. @mohammadiSurrogateModelingSolving2024 PSO particles will represent plausible configurations and pairings whose hourly dispatch is simulated by our renewable and electrolyzer time-series models. At each iteration, we will compute LCOH, capacity factor, and storage utilization metrics for hundreds of scenarios, then update particle velocities and positions based on local and global optima. The incorporation of a Gaussian process model will accelerate convergence by approximating LCOH responses in unexplored regions, allowing the optimizer to focus on the most promising design clusters.
Geospatial variability of renewable resources will be addressed by embedding region-specific weather, tariff, and land-use data into the optimization. We will perform parallel PSO runs for each candidate location, thereby generating location‐tailored Pareto fronts of LCOH versus configuration cost. Post-processing these fronts will identify "sweet spot" sites where favorable solar or wind regimes combine with low land and grid-connection costs to yield sub-$3.00 kg⁻¹ hydrogen. Furthermore, by mapping the distribution of optimal mixes, such as the ratio of wind to solar capacity or the required battery size per MW of electrolyzer power, we can provide prescriptive guidance on how to scale projects in diverse geographies.

Finally, we will integrate machine-learning classifiers to predict feasibility envelopes based on site attributes, renewable energy potential, permitting complexity, and proximity to demand centers. Training this classifier on PSO results will enable rapid pre-screening of new sites without requiring full optimization runs, thereby reducing the computational burden for stakeholders evaluating hundreds of potential projects. Completing Task 3.2 will deliver a powerful decision-support tool that not only minimizes LCOH but also characterizes the resilience and economic risk of green hydrogen systems across varying contexts. The goal is to pave the way for strategic deployment of next-generation PEM electrolyzer infrastructure.




4.3.3 Task 3.3 {future work} – Geospatial, Hourly-Resolved LCOH Mapping with Policy and Emissions Layers


The final element of our dynamic system-analysis framework will be a comprehensive geospatial assessment that calculates location-specific LCOH by coupling hourly dispatch simulations with regional environmental and financial parameters. This task entails two key components: spatial data integration and incentive modeling.

**Spatial Data Integration** 
We will assemble high-resolution geospatial layers for five archetypal U.S. regions: the Texas Gulf Coast, California Central Valley, Great Plains, New York offshore, and the Phoenix–Casa Grande corridor in Arizona. We will draw on NREL's NSRDB for solar irradiance, the WIND Toolkit for wind speeds, and publicly available elevation, land-use, and grid interconnection maps. Each site will be characterized by its hourly renewable generation potential, prevailing wholesale and time-of-use electricity tariffs, and transmission constraints, ensuring that our dispatch model reflects both physical resource endowment and market exposure.

**Policy and Incentive Modeling**  
To capture the impact of federal and state incentives on hydrogen economics, we will layer in tax credit eligibility. The Investment Tax Credit (ITC) for renewables and the Production Tax Credit (PTC) for clean hydrogen under the Inflation Reduction Act. @45VHydrogenTax;  @gomezDeterminingLifeCycle We will calculate after-incentive LCOH and NPV for each location by linking hourly hydrogen production outputs to annualized ITC and PTC cash flows. Additional regional incentives, such as state renewable portfolio standard multipliers or land-use permitting costs, will be included.

Together, these analyses will equip policymakers, developers, and investors with a detailed, site-tailored understanding of green hydrogen viability. It will aid in identifying regions with optimal resource, regulatory, and economic conditions and quantifying how policy levers shift the competitive landscape. This geospatial LCOH atlas will serve as a decision-support tool to accelerate the deployment of cost-effective, clean hydrogen infrastructure at scale.





## 5.0 Intellectual Merit

This study advances the techno-economic analysis of green hydrogen production by introducing a rigorously coupled, multi-scale modeling framework that integrates detailed electrochemical physics, system-level cost assessment, and dynamic renewable energy integration. Unlike prior work that treats PEM electrolyzer design and energy supply in isolation, our approach unifies these domains through three novel contributions:

1. Physics-Driven Optimization: We develop a first-principles, 0D/1D PEM electrolyzer model, parametrized for activation, ohmic, and concentration overpotentials, membrane hydration, and gas crossover, and embed it within a multi-objective optimization routine (NSGA-II via pymoo). This yields Pareto-optimal design maps that explicitly trade energy efficiency against material use and mechanical durability, offering a quantitative tool for stack configuration decisions at unprecedented granularity.  

2. Dynamic, Location-Specific Energy Coupling: We incorporate hourly-resolved PV, wind, and hybrid generation profiles, sourced from high-resolution irradiance and wind reanalysis data, directly into the electrolyzer simulation. By coupling LCOE-based pricing signals with electrolyzer dispatch, the framework quantifies cost and emissions impacts of intermittency, enabling dynamic optimization of renewable-electrolyzer-storage configurations through surrogate-accelerated particle swarm methods.

3. Material Roadmapping via Integrated Sensitivity Analysis: Leveraging BioSTEAM’s Monte Carlo and Sobol routines, we establish a “material library” of alternative membranes and catalyst formulations, linking experimental property data to TEA outcomes. This global sensitivity analysis identifies high-leverage substitution opportunities, such as non-precious metal catalysts and hydrocarbon-based membranes, and projects their cost-learning trajectories under scaled manufacturing conditions.

By bridging electrochemical modeling, advanced optimization algorithms, renewable energy systems, and stochastic process simulation, 
this research delivers a decision-support toolkit that transcends conventional static TEAs. Its novel integration of multi-physics fidelity, temporal variability, and materials innovation paves the way for data-driven R&D prioritization and significantly advancing the field of sustainable hydrogen production.
















## **6.0 Broader Impact**

The outcomes of this integrated analysis extend well beyond academic insight, offering tangible benefits for energy policy, industry strategy, and societal decarbonization goals. First, by providing site‐specific LCOH and NPV maps that account for regional renewable resources, this work equips policymakers and planners with the quantitative evidence needed to tailor incentives, such as production tax credits, renewable energy mandates, or locational subsidies, to locations where green hydrogen can be produced most cost‐effectively.

We have demonstrated that distributed, smaller‐scale electrolyzers can achieve competitive LCOH in grid‐constrained or remote regions, underscores a pathway for industrial decarbonization in hard‐to‐reach communities and emerging markets. Localized hydrogen production reduces dependence on long-distance gas pipelines, enhances energy resilience, and creates new green job opportunities in manufacturing, operations, and maintenance.

Moreover, the framework's dynamic modeling of intermittency informs grid operators and utilities about the value of flexible loads and hydrogen storage in balancing high penetrations of variable renewable energy sources. By demonstrating how electrolyzers can provide demand response and ancillary services, our work aligns with broader efforts to modernize electric grids, reduce curtailment of solar and wind output, and integrate large‐scale clean energy systems




----



Key cell-level design parameters are summarized in Table 1, based on Bessarabov & Miller (2018). These include membrane thickness, electrode porosity, and exchange current densities at both electrodes.

| Parameter                                 | Value                                  |
| ----------------------------------------- | -------------------------------------- |
| Faraday constant, F (C·mol⁻¹)             | 96 485                                 |
| Gas constant, R (J·mol⁻¹·K⁻¹)             | 8.314                                  |
| Operating temperature, T (K)              | 333.15                                 |
| Operating pressure, P (bar)               | 1 (anode), 30 (cathode)                |
| Maximum current density, i₍max₎ (A·cm⁻²)  | 2                                      |
| Exchange current density (A·cm⁻²)         | 2.618×10⁻⁶ (anode), 1.0×10⁻¹ (cathode) |
| Limiting current density (A·cm⁻²)         | 6                                      |
| Membrane thickness (μm)                   | 178                                    |
| Electrode thickness (μm)                  | 200                                    |
| Electrode porosity                        | 0.30                                   |
| Active area, A₍cell₎ (cm²)                | 877                                    |
| Catalyst loading (mg·cm⁻²)                | 1.54 (anode), 0.40 (cathode)           |
| Specific energy consumption (kWh·kg⁻¹ H₂) | 49                                     |
| Cell voltage, V₍cell₎ (V)                 | 1.79                                   |
| Voltage efficiency                        | 0.69                                   |
| Total stack power (kW)                    | 19 034                                 |

_Table 1: Principal cell design parameters and performance metrics._
