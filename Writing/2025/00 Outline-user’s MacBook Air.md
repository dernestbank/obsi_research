


Contents

[Abstract. ](Abstract)

[Acknowledgements. 2](Abstract#Acknowledgement)

[[01 Introduction and background| Chapter 1: Introduction]]
	[1.1 Background and Motivation. 4](#_Toc192135799)
	[1.2 Global Policies for green hydrogen production. 5](#_Toc192135800)
	[1.2.1 USA Energy Landscape and Key Goals. 5](#_Toc192135801)
	[1.3 Objectives of the Study. 8](#_Toc192135802)
	[1.4 Significance of the Study. 10](#_Toc192135803)
	[1.5 Structure of the Thesis. 10](#_Toc192135804)

[[02 literature review |Chapter 2: Literature Review.. 11]]
	[2.1. Hydrogen Production Technologies. 11](#_Toc192135806)
		[2.1.1 Colors of hydrogen and types of hydrogen production. 11](#_Toc192135807)
		[2.1.1 Electrolytic Hydrogen Production. 11](#_Toc192135808)
	[2.2 PEM electrolyser Design and configuration. 11](#_Toc192135809)
	[2.2.1 Membrane electrode Assembly and PEM Cell design. 11](#_Toc192135810)
	[2.2.2 Electrocatalyst. 12](#_Toc192135811)
	[2.2.3 Electrode design: Cation exchange Membrane. 12](#_Toc192135812)
	[2.2.4 Porous Transport Layer /Gas Diffusion Layer. 15](#_Toc192135813)
	[2.2.5 Bipolar plate design. 15](#_Toc192135814)
	[2.4 Cost drives in electrolytic hydrogen Production. 16](#_Toc192135815)
	[2.4.1  Previous Cost Modeling Approaches. 16](#_Toc192135816)

[[03 Mathematical modeling | Chapter 3: Mathematical modeling. ]]
	[3.1 Electrolyzer and Electrochemical Module. 17](#_Toc192135818)
	[3.2 Cost model 17](#_Toc192135819)
	[3.2.1 Capital cost: Manufacturing cost. 17](#_Toc192135820)
	[3.2.2 Levelized cost of hydrogen(LCOH) 17](#_Toc192135821)
	[3.3 Energy system model 17](#_Toc192135822)
	[3.3.1 PV power model 17](#_Toc192135823)
	[3.3.2 Wind PV plant model 17](#_Toc192135824)

[[04 Methods| Chapter 4: Materials and Methods ]]
	[4.1. Overview of the modelling process. 18](#_Toc192135826)
	[4.2. Scope and indicators. 18](#_Toc192135827)
	[4.3. modeling unit and data sources. 18](#_Toc192135828)
	[4.4. System analysis. 18](#_Toc192135829)
	[4.4.1. Process economics. 18](#_Toc192135830)
	[4.4.2. Sensitivity analysis and optimization. 18](#_Toc192135831)

[[05 Results and Discussion| Chapter 5: Results and Discussion. 19]]
	[5. 1 Cost drivers and compositions Manufacturing cost and material composition. 19](#_Toc192135833)
	[5.2. Economic comparison. 19](#_Toc192135834)
	[5.3 Comparing different optimization methods. 19](#_Toc192135835)
	[5.2 Sensitivity Analysis and Potential Cost Reductions. 19](#_Toc192135836)
	[5.6 Limitations of the Study. 19](#_Toc192135837)
	[5.4 Future Research Directions. 20](#_Toc192135838)

[Chapter 6: Conclusion. 22](#_Toc192135839)

[References. 23](#_Toc192135840)





Chapter 3: Mathematical modeling. ]]
	3.1 Electrolyzer and Electrochemical Module.
		Reversible voltage
		Activation overpotential
		Ohmic overpotential
		Diffusion overpotential
	3.2 Cost model 
	3.3 Energy system model
	3.3.1 PV power model 
	3.3.2 Wind PV plant model 

3Levelized cost of hydrogen(LCOH) 17]

Techno-Economic Analysis (TEA)




**1.0 Introduction**  
1.1 Background and Motivation  
1.2 Scope and Objectives  
1.3 Thesis Structure

**2.0 Literature Review**  
2.1 Green Hydrogen Production Technologies  
2.1.1 Alkaline Electrolysis  
2.1.2 Proton Exchange Membrane (PEM) Electrolysis  
2.2 Technoeconomic Assessments in H₂ Production  
2.3 Gaps and Research Opportunities

**3.0 Methodology**  
3.1 PEM Electrolyzer Model Development  
 3.1.1 Electrochemical Design Equations  
 3.1.2 Mass and Energy Balances  
3.2 Technoeconomic Analysis (TEA) Framework  
 3.2.1 Capital Expenditure (CapEx) Assumptions  
 3.2.2 Operating Expenditure (OpEx) Assumptions  
3.3 Integration with Renewable Energy Supply Scenarios  
3.4 Assumptions and Uncertainty Treatment

**4.0 Results and Discussion**  
4.1 Base-Case Performance and Costs  
4.2 Sensitivity Analysis (e.g., electricity price, stack lifetime)  
4.3 Scenario Analysis: Grid vs. Renewables Integration  
4.4 Environmental and Industrial Relevance

**5.0 Conclusions and Outlook**  
5.1 Key Findings  
5.2 Limitations and Future Work  
5.3 Policy and Industry Implications






# Committee

This Thesis has been reviewed and approved by the following:

Dr. Rui Shi

Assistant Professor of Chemical Engineering Thesis advisor

Dr. Phillip Savage

Walter L. Robb Family Chair, Professor of Chemical Engineering.

Dr. Andrew Zydney

Bayard D. Kunkle Chair, Professor of Chemical Engineering.


Dr. Bruce Logan

Evan Pugh University Professor and Kappe Professor of Environmental Engineering, Civil and Environmental Engineering





# Acknowledgements
I would like  tank Dr Shi for his continual support.

I will like to acknowledge the work of H2A team

Thank Dr. Philip Savage , Dr. Andrew Zydney and Dr. Bruce Logan for being on my committee.





pandoc Thesis_Draft.docx \
  --from=docx \
  --to=docx \
  --lua-filter=zotero.lua \
  --metadata=zotero.client=zotero \
  --bibliography=library.json \
  --metadata=zotero.csl-style=ieee \
  -o output2.docx



pandoc \
  Thesis_Draft.docx \
  --from=docx \
  --to=docx \
  --lua-filter=./zotero.lua \
  --metadata=zotero.client=zotero \
  --metadata=zotero.csl-style=ieee \
  -o Thesis_Draft_Converted.docx



pandoc \
  Thesis_Draft.docx \
  --from=docx \
  --to=docx \
  --bibliography=library.json \
  --citeproc \
  --csl=ieee.csl \
  -o Thesis_Draft_Formatted.docx



Abstract
Understand the Purpose:
**Key Elements to Include:**

- **Introduction/Background:** Briefly introduce the topic and provide essential context.
- **Problem/Objective:** Clearly state the research problem or objective you addressed.
- **Methodology:** Explain how you conducted your research and addressed the research question.
- **Key Findings/Results:** Summarize your main findings and results.
- **Conclusions/Implications:** Explain the meaning, impact, or broader implications of your research.
**Tips for Effective Writing:**

- **Conciseness and Clarity:** Use clear, concise, and specific language. Avoid jargon or define necessary discipline-specific terminology.
- **Summarize, Don't Evaluate:** The abstract should describe your work, not offer evaluations or defenses.
- **Keywords:** Include relevant keywords to help readers find your research. Choose them carefully for maximum visibility.
- **Word Limit and Formatting:** Adhere to the specified word count (typically 150-300 words) and any formatting requirements.
- **New Text:** Write the abstract as entirely new text, rather than cutting and pasting from your paper.
- **Stand-Alone:** The abstract should be understandable on its own, without requiring the reader to consult the main paper.
- **Focus on Findings:** Highlight the key results and their implications. Avoid unnecessary details or methodological intricacies.
- **Read Other Abstracts:** Examine abstracts from similar papers to get a sense of structure and style.
- **Proofread Carefully:** Thoroughly check for spelling and grammar errors. 

**4. Structure and Flow:**

- While the specific structure can vary, a logical flow often involves moving from background/problem to methods, results, and conclusions.
- Consider a "thesis-first" approach, stating your main findings or conclusions upfront. 

**5. What to Avoid:**

- **Mini-Literature Reviews:** Avoid extensive citations in the abstract unless it's a critical reference.
- **Exaggeration:** Do not exaggerate or include information that is not present in the main text.
- **Undefined Abbreviations:** Avoid using abbreviations that are only explained in the main paper.
- **Sensationalizing or Speculating:** Focus on presenting the actual research, not making unsubstantiated claims or predictions.


The global transition to a low-carbon economy hinges on making green hydrogen cost-competitive with fossil-derived alternatives. PEM electrolysers have evolved as optimistic solution While various government incentives can help bridge this gap, long-term viability requires fundamental cost optimization in production technology. This thesis addresses the critical need for a systematic framework that connects advances in proton-exchange-membrane (PEM) electrolyzer design and electricity source configuration with their system-level techno-economic outcomes.


This framework equips stakeholders with decision-support tools to guide the cost-effective, resilient design and deployment of next-generation PEM hydrogen systems.
# Abstract

**Abstract**

The global transition to a low-carbon economy hinges on making green hydrogen cost-competitive with fossil-derived alternatives. While government incentives help bridge this gap, long-term viability requires fundamental cost reductions in production technology. This thesis addresses the critical need for a systematic framework that connects advances in proton-exchange-membrane (PEM) electrolyzer design with their system-level techno-economic outcomes, a link that has been largely underexplored. The primary objective was to develop and validate an integrated model that unifies electrochemical physics, modular techno-economic assessment (TEA), and dynamic renewable energy modeling to identify key cost drivers and optimize green hydrogen production.

The methodology involved developing a detailed, physics-based PEM electrolyzer model, which was validated against experimental data. This electrochemical model was then coupled with a comprehensive TEA framework, following DOE H2A guidelines, to compute the levelized cost of hydrogen (LCOH), net present value (NPV), and internal rate of return (IRR). Finally, an hourly-resolved energy-supply layer was integrated to simulate photovoltaic, wind, hybrid, and grid-interactive power configurations, allowing for a nuanced analysis of how renewable intermittency impacts production economics.

The analysis reveals that electricity feedstock cost and uninstalled capital cost are the two most influential drivers of LCOH and NPV, with electricity price volatility posing the primary risk to project profitability. For a 10,000 kg/day baseline facility, a $0.09/kWh difference in electricity price impacts over 80% of the NPV. Furthermore, the choice of renewable energy configuration and the local resource profile can alter the LCOH by 20–30%. Economies of scale show diminishing returns beyond a capacity of approximately 10,000 kg/day, as electricity costs begin to dominate savings from capital investment.

This research concludes that achieving cost-competitive green hydrogen (sub-$5/kg) requires a strategic combination of mid-scale plant designs (>8,000 kg/day) and access to low-cost electricity (≤$0.05/kWh). The integrated framework presented herein provides a robust tool for data-driven decision-making, enabling the optimization of next-generation PEM electrolyzer deployments. Future work will focus on multi-objective design optimization, evaluating novel material cost-reduction levers, and developing geospatial LCOH maps to identify optimal investment regions.

_**Word Count Check:**_ _[Approx. 300 Words]_

_**Keywords:**_ _Green Hydrogen, PEM Electrolysis, Technoeconomic Analysis (TEA), Levelized Cost of Hydrogen (LCOH), Renewable Energy Integration, System Modeling, Cost Optimization_



alt 2
System Design and Technoeconomic Analysis of Green Hydrogen Production via PEM Electrolysis investigates strategies to reduce the cost of hydrogen generated by proton-exchange-membrane (PEM) electrolysis powered by variable renewable electricity. Green hydrogen offers near-zero lifecycle CO₂ emissions, yet its levelized cost of hydrogen (LCOH) often exceeds $6/kg versus $1–2/kg for fossil-derived alternatives. This thesis develops an integrated framework coupling (1) a physics-based, lumped-parameter model of a PEM electrolyzer—capturing activation, ohmic, and concentration overpotentials, Faradaic efficiency, and gas crossover—with (2) a modular technoeconomic assessment (TEA) that applies capital-cost scaling laws, balance-of-plant expenditures, and 20-year discounted-cash-flow analysis to compute LCOH and net present value (NPV), and (3) an hourly-resolved energy-supply layer simulating photovoltaic, wind, hybrid, and grid-interactive configurations at representative U.S. sites. Sensitivity and uncertainty analyses reveal that electricity feedstock cost and uninstalled electrolyzer CAPEX dominate economic performance: a $0.09/kWh variation shifts NPV by over 80%, while CAPEX changes from $250 to $1 500/kW alter NPV by more than 50%. Renewable configuration and local resource profiles further influence LCOH by 20–30%. These results underscore the importance of site-tailored system design and targeted material innovations to drive down intrinsic production costs. The framework lays the groundwork for future work on advanced membrane and catalyst materials, multi-objective optimization of energy system architectures, and geospatial mapping of LCOH “sweet spots.”

**Keywords:** PEM electrolyzer, green hydrogen, technoeconomic analysis, levelized cost of hydrogen (LCOH), net present value (NPV), renewable integration, sensitivity analysis.
# Acknowledgements

I would like to thank Dr. Rui Shi for guidance and advice throughout this process. The NSF icorps northeast region facilators for their support and 
Dr. Toyota for his advice and contribution. 
My mom and dad for thier encouragement and emotional support.
RCCG living spring, HVCC their social and spiritual support
I would also like to acknowledge the work of James Alamia and Dr. Hariteja Nandimandalam for their work and advice on this project, as well as their contributions to the separate manuscript submitted in tandem with this thesis. 
Finally, I would like to thank Dr. Phillip Savage, Dr. Andrew Zydney, and Dr. Bruce Logan for being on my committee




!.2 State of the Problem 
Purpose of the study
Impotance of the Study
Limitation, Delimitations, Assuumptions
Organization of Thesis
Definitions



