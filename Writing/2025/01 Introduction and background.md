



Goal and objectives

Abstract ...................................................................................................................................... I

Table of Contents.....................................................................................................................IV 
List of Figures ..........................................................................................................................VI 
List of Tables ......................................................................................................................... VII 
Keys and abbreviation ............................................................................................................VIII


CHAPTER 1. Introduction and Problem Statement ..................................................................
1 1.1 Introduction .................................................................................................................
1 1.2 Problem Statement ......................................................................................................3 
1.3 Thesis Aim and Objectives .........................................................................................4 

2.8 Novelty of Thesis ......................................................................................................2
1.4 Thesis Layout ..............................................................................................................5





# Introduction 

1.0 Overview | project summary
2.0 Goals and Objectives



3.0 Research Background.
	3.1 design and Multi-objective optimization background
	3.2 Techno-economic background.
	3.3 RE system background



**1.0 Introduction**  
1.1 Background and Motivation  
1.2 Scope and Objectives  
1.3 Thesis Structure

# Background

Adapting from the comprehensive report.


Objective and novelty of this study.









Objectives:
To optimize the design parameters in pem electrolyser to reduce cost and increase efficiency
To determine optimum capacity ratio for renewable energy sources green hydrogen production.
To access the feasibility of algorithmic optimization for green hydrogen production.



Sensitivity analysis
Hydrogen production analysis dashboard.
PV-Wind | location optimization|



## 1.0 CHAPTER 1. Introduction and Problem Statement
### 1.1 Overview

The transition to a low‐carbon energy economy has placed green hydrogen at the forefront of global decarbonization strategies. A hydrogen production system, when powered by renewable electricity, yields minimal lifecycle greenhouse gas emissions, unlike hydrogen produced from natural gas or coal.  Yet, despite its environmental promise, green hydrogen remains significantly more expensive than fossil‐derived alternatives, with levelized costs frequently exceeding $6 /kg, compared to $1–2 /kg for grey hydrogen produced from natural gas.  @mcqueenDepartmentEnergyHydrogen2020; @marzoukLevelizedCostGreen2023
Governments and industry leaders have responded with a variety of policies and incentives. The EU and its member states, through the REPowerEU plan and the Clean Industrial Deal, aim for 40 GW of electrolyser capacity by 2030. Section 45v of the Inflation Reduction Act (IRA)  introduced a production tax credit (PTC) of up to $3 per kilogram to narrow this cost gap. @gomezDeterminingLifeCycle; @45VHydrogenTax Yet in practice, these incentives alone do not guarantee long‐term competitiveness. Political shifts, changes in subsidy schemes, and volatility in renewable electricity markets can render incentive‐driven projects economically vulnerable. In this context, a more enduring solution lies in driving down the intrinsic production costs of proton‐exchange‐membrane (PEM) electrolyzers through advances in electrolyzer design, scale economies, and system-level optimization.

Current projections indicate that demand for green hydrogen in the US could rise from less than 11.16 million metric tons in 2021 to over 27 million tons by 2040 driven by heavy industries, long‐haul transportation, and steel making @nyangonAdvancementsHydrogenEnergy2024 . Among the various electrolysis technologies, PEM electrolyzers stand out for their high efficiency and compact footprint. Their operational flexibility makes them particularly well‐suited to dynamic renewable power inputs. Nevertheless, the capital cost of PEM stacks, their balance‐of‐plant (BoP) requirements, and the high price of electricity feedstock continue to dominate the levelized cost of hydrogen (LCOH). At the same time, these cost drivers are tightly interwoven with design choices such as current density, membrane thickness, catalyst loading, and operating temperature and with the temporal variability of upstream renewable generation. As a result, optimizing PEM hydrogen production requires a comprehensive analysis that spans electrochemical physics, economics, and energy systems modeling. Although individual studies have looked at alternatives to membranes or substitutions for catalysts, very few have systematically connected changes in material properties to their economic and technical outcomes. This gap makes it harder to pinpoint which material investments actually lead to cost-effective performance improvements when scaled up to commercial module sizes.

This report addresses this challenge by presenting an integrated framework that unites three previously siloed domains. First, we develop a detailed, physics‐based model of a PEM electrolyzer stack, capturing activation, ohmic and concentration overpotentials, Faradaic efficiency, and gas crossover effects. Next, we couple these cell‐level performance metrics with a modular techno‐economic assessment (TEA) to quantify how material choices, operating conditions, and scale‐dependent capital costs drive LCOH and net present value (NPV). Finally, we embed an hourly‐resolved energy‐supply layer to simulate photovoltaic, wind, hybrid, and grid‐interactive configurations. We examine how renewable intermittency and geographic resource variability affect production economics and carbon intensity. By merging these three components, thus, electrochemical, economic, and energy system models, into a single cohesive framework, our research uncovers interactions and trade‐offs that remain opaque under conventional, one‐dimensional analyses.

Our findings reveal several significant insights. First, energy feedstock cost and uninstalled capital cost emerge as the two most influential drivers of LCOH and NPV. The cost of electricity feedstock overshadows the economies of scaling plant capacity beyond 10kg of H2 day of hydrogen. In our sensitivity analysis, a $0.09 /kWh difference in electricity price affects over 80% of the NPV. Similarly,  a difference in the target uninstalled CAPEX from $250 to $1 500 /kW affects more than half of the NPV. The choice of renewable energy configuration (PV, wind, hybrid, or grid‐interactive) and the local resource profile can shift LCOH by 20 – 30 percent, emphasizing the need for site‐tailored system architectures.

Looking forward, our framework paves the way for several avenues of future research. In subsequent tasks, we will expand the TEA by exploring cost-reduction levers through material substitution by incorporating hydrocarbon-based membranes and non-precious-metal catalysts and quantifying their impact via global sensitivity analysis. We will introduce a surrogate-accelerated particle swarm optimizer to identify optimal renewable-electrolyzer-storage configurations across hundreds of candidate sites, producing geospatial LCOH maps that highlight "sweet-spot" regions for green hydrogen investment.




### **1.2 Goals and Objectives**

The overarching goal of this research is to develop and validate an integrated modeling framework that couples detailed, physics‐based PEM electrolyzer design with system‐level techno-economic analysis and dynamic renewable energy system modeling, in order to identify key cost drivers and optimize green hydrogen production. By unifying electrochemical, economic, and energy-resource perspectives, the framework will enable data-driven decision-making for next-generation PEM electrolyzers and their deployment under diverse operating conditions.

### Research question

To achieve this goal, we will address the following research questions:

1. What are the principal techno-economic cost drivers in PEM electrolyzer hydrogen production, and how do these drivers vary with plant scale, material selection, and operating conditions?

2. In what ways do electrolyzer design variables such as membrane thickness, catalyst layer loading, and cell operating temperature affect energy efficiency, Faradaic performance, and stack durability, and how do these trade-offs translate into changes in levelized cost of hydrogen (LCOH) and net present value (NPV)?

3. What is the impact of different renewable energy supply configurations (photovoltaic, wind, hybrid, or grid-interactive) on hydrogen production cost and capacity factor, when modeled at an hourly resolution for location-specific scenarios?

To answer these questions, the project is organized around three specific Aims and objectives:

Aim 1: Develop a Physics-Based Electrochemical Model and Multi-Objective Design Optimization. 

In this Aim, we will refine and extend our lumped-parameter PEM electrolyzer model by incorporating activation, ohmic, and concentration overpotentials; membrane hydration; Faradaic efficiency; and gas crossover effects and and prepare it for a multi-objective optimization framework.  

Aim 2: Construct a Modular Techno-Economic Assessment (TEA) Integrating Electrolyzer Performance. 

Building on the cell-level outputs from Aim 1, Aim 2 will establish a comprehensive system boundary encompassing the electrolyzer stack and balance-of-plant components. We will develop a modular TEA that computes LCOH and NPV over a 20-year horizon by combining stack power requirements, capital cost scaling laws, acceleration-based depreciation schedules, and operating expense drivers (electricity, maintenance, membranes, catalysts, and water treatment). We will also study a scenario based sensitivity and scaling effects to quantify how variations in uninstalled CAPEX, electricity price, efficiency, fixed O&M, and other inputs affect financial metrics, thereby pinpointing the highest-impact cost levers.

Aim 3: Integrate Dynamic, Hourly-Resolved Renewable Energy Modeling and Location-Specific Optimization. 

Aim 3 will couple the system TEA from Aim 2 with an energy supply layer that simulates hourly output from photovoltaic, wind, hybrid, and grid-interactive configurations at selected U.S. locations. By computing time-series data on renewable availability, curtailment, and LCOE, we will drive the electrolyzer dispatch to calculate annual capacity factors, hydrogen yields, and temporal cost profiles.
Together, these Aims will fulfill our objectives of identifying cost drivers, optimizing electrolyzer design parameters, and determining the most promising energy-system architectures for scalable, cost-effective green hydrogen production.





Purpose of the Study

| Aim       | Chapter(s)    | Brief Description                                                                                                                                                                                          |
| --------- | ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Aim 1** | **3.1**       | Develop a physics-based PEM stack model capturing activation, ohmic and concentration losses, membrane hydration, Faradaic efficiency and gas crossover, and prepare it for multi-objective optimisation . |
| **Aim 2** | **3.2–3.5**   | Build a modular TEA that links stack outputs to 20-year discounted-cash-flow metrics, includes capital-cost scaling and scenario-based sensitivity analyses .                                              |
| **Aim 3** | **3.1.2 & 4** | Integrate an hourly PV-, wind-, hybrid- and grid-interactive energy-supply layer; compute dispatch, capacity factor and emissions for location-specific cases .                                            |



**Structure of the Thesis**  
This thesis is organized into five chapters (plus appendices), aligned with three specific research aims:

- **Chapter 1: Introduction and Problem Statement**  
    Defines the challenge of high LCOH for green hydrogen, outlines the gap in linking PEM-design innovations to system-level economics, and presents research questions.
    
* **Chapter 2: Literature Review**
  Reviews global hydrogen policies and electrolyzer “color” taxonomy; examines PEM cell components (membranes, catalysts, bipolar plates, flow fields) and key degradation mechanisms; surveys TEA frameworks and identifies dominant cost drivers and renewable integration strategies.
    
- **Chapter 3: Materials and Methods**  
    Describes the development of the physics-based PEM electrolyzer model (overpotentials, conductivity, Faradaic efficiency), the modular TEA methodology (capital-cost scaling, cash-flow analysis, sensitivity and uncertainty techniques), and the hourly renewable-energy supply submodel.
    
- **Chapter 4: Results and Discussion**  
    Presents model validation, parametric and univariate sensitivity analyses, scenario comparisons for distributed versus centralized systems, multivariate and Monte Carlo simulations, and the impact of energy-system configurations on LCOH and NPV.
    
- **Chapter 5: Conclusion**  
    Summarizes key findings, highlights intellectual merit and broader impacts, discusses limitations, and outlines future research directions (material-substitution sensitivity, surrogate-based optimization, geospatial LCOH mapping).
    
- **Appendices**  
    Provide detailed electrolyzer-design parameters (Appendix A), economic and system parameter tables (Appendix B), uncertainty and sensitivity inputs (Appendix C), and code/documentation (Appendix D).




The thesis is organized as follows:

- **Chapter 1** sets the stage by outlining hydrogen’s promise in a low-carbon economy and summarizing today’s electrolyzer landscape.
    
- **Chapter 2** surveys existing electrolyzer technologies, dissects the key PEM components and operating modes, and reviews prior techno-economic analyses of hydrogen production.
    
- **Chapter 3** translates the core electrochemical and transport phenomena of water splitting into a detailed PEM stack model.
    
- **Chapter 4** builds on that model to develop a steady-state cost framework, using it to calculate the levelized cost of hydrogen under constant operation.
    
- **Chapter 5** introduces a dynamic optimization scheme, applying it to assess how variable operation affects hydrogen cost.
    
- **Chapter 6** uses the techno-economic tool to explore future cost drivers—electrolyzer learning curves, performance improvements and electricity-price scenarios—and their impact on LCOH.
    
- **Chapter 7** draws together the main findings, highlights the study’s contributions and outlines directions for further research.














This Aim will deliver a suite of validated cell-level design maps that quantify the inherent trade-offs between efficiency, material cost, and mechanical integrity.
The objective will be to identify Pareto-optimal combinations of membrane thickness, catalyst layer loading, electrode thickness, current density, and operating temperature that simultaneously minimize specific energy consumption and overall MEA thickness, subject to durability constraints.


. A dynamic optimization algorithm that leverages a particle swarm method with Gaussian process surrogates will then identify optimal combinations of renewable capacities, electrolyzer sizing, and battery storage that minimize LCOH under site-specific resource and policy constraints. This Aim will produce spatial maps of “sweet spot” regions where green hydrogen can be produced most economically, as well as guidelines for matching system configurations to local grid conditions.



