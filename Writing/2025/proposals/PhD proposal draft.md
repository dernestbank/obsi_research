
 Agentic Machine-Learning Framework for Autonomous Process Systems Analysis Integrating Techno-Economic Analysis and Life Cycle Assessment


key words: low TRL,

## 1. Introduction and Problem Statement
Process systems analysis (PSA) plays a critical role in evaluating the viability and sustainability of chemical processes through **techno-economic analysis (TEA)** and **life cycle assessment (LCA)**. TEA assesses the economic performance (e.g. costs, profitability) of a process or product, while LCA quantifies environmental impacts across the process life cycle. TEA and LCA provide complementary insights for decision-makers but require extensive data collection and computation, which is _often a limiting factor_ especially for emerging technologies.
Most studies frequently rely on ad-hoc spreadsheet models, specialized tools and human expertise, making it difficult to rapidly iterate designs or integrate new data. 
Current PSA methods face limitations in terms of integration, efficiency, and scope. Recent advances in machine learning (ML) and artificial intelligence (AI) – notably **large language models (LLMs)** – present an opportunity to **automate and accelerate PSA** beyond the conventional paradigm.
This proposal outlines a research plan to develop a novel LLM-driven agentic framework that orchestrates process simulation tools, TEA/LCA models, and predictive ML in a unified system. The goal is to **streamline and enhance TEA-LCA workflows** using AI agents, enabling faster, more comprehensive process evaluations. 

Despite their importance, current PSA practices face significant challenges. Performing a rigorous LCA demands “a great deal of time and data”, which often limits its application during early process development. @kockAutomationLifeCycle2023 TEA and LCA are typically carried out by different domain experts using separate tools (e.g. process simulators for TEA, LCA software for environmental analysis), leading to expertise bottlenecks and integration complexity. 

TEA studies frequently rely on ad-hoc spreadsheet models and human expertise, making it difficult to rapidly iterate designs or integrate new data. As a result, **current PSA methods face limitations** in terms of integration, efficiency, and scope.

Recent reviews highlight a pressing need for automation and integration in PSA. Köck _et al._ (2023) found that automating data flow between process simulations and LCA can “make integration of environmental impacts into decisions easier, less time-consuming, and improve data quality”.  However, existing efforts at PSA automation remain limited. Automation has been implemented mostly via custom interfaces linking simulators to LCA databases, or via machine learning (e.g. neural networks for predicting molecular properties). Fewer than one-third of published methods share open code, and only 10 of 30 surveyed papers included uncertainty analysis @kockAutomationLifeCycle2023 – indicating that current solutions are often proprietary, not reproducible, and may neglect uncertainty quantification.

Research Gap

No existing framework unifies TEA, LCA, large language models (LLMs), and predictive machine learning in an _autonomous, agentic system_ for process analysis. Tools like **BioSTEAM** (an open-source process simulation and TEA platform) and its LCA extension have demonstrated the value of tighter integration – e.g. BioSTEAM-LCA automates early-stage TEA-LCA for biorefineries, enabling simultaneous economic and environmental evaluation under uncertainty.
 BioSTEAM integrates uncertainty into simulations to _“streamline and automate early-stage technology evaluations”_, providing rigorous sensitivity analyses. It _“enables the integration of design, simulation, TEA and LCA to improve consistency and transparency”_ of sustainability metrics
@cortes-penaBioSTEAMBiorefinerySimulation2020; @cortes-penaBioSTEAMFastFlexible2020 . Yet, even these advanced tools do not incorporate the **agentic intelligence** now possible with AI. Large Language Models have recently shown remarkable ability to plan and execute complex tasks autonomously in scientific workflows