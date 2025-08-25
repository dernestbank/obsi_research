
A review of automation potentials in PSA
@kockAutomationLifeCycle2023


![[Figure 3. Methods of LCI data generation with automation potential identified in the literature..png]]




@vyasAutonomousControlLeveraging2025

LLMs can unify high-level symbolic planning and low-level continuous control, paving the way toward resilient, language-driven automation in chemical engineering.



My old references
----
@chenAdvancingLifeCycle2024

By starting small by consolidating papers focused on the LCA of proton exchange membrane water electrolysis, which produces green hydrogen, and ML applications in LCA. These papers are uploaded to OpenAI to create the LlamaIndex, enabling future queries. Using the LangChain framework, researchers query the customised model (GPT-3.5-turbo), receiving tailored responses.

code development


@cornagoHowCanTransformers2023
how the field of LCA and its practitioners can benefit from powerful neural network architectures like Transformers (Vaswani et al., 2017).
ChatGPT is currently limited to discussing LCA impacts for simple and well-documented products.
To support decision-making, fine-tuning could be aimed at analyzing past LCI and LCA impacts data for hotspot identification and prioritization to reduce LCA impacts

![[swot analysis for LLMs.png]]

The main internal strengths lie in the supportfor the automationand integration of LCA applications. Integrated tools for decision-making support could be more beneficial than data pipeline automation,
Data quality is at the center of internal weaknesses. Referencing functions

The four phases of LCA and its application


@goridkovWhatsThisLCA2024
What’s in this LCA Report? A Case Study on Harnessing Large Language Models to Support Designers in Understanding Life Cycle Reports Nicole Goridkova, Ye Wangb, Kosa Goucher-Lambert

However, LCA reports are typically dense and technically complex,

during the early stages of the design process: TRL

we investigate how four LCA- and sustainabilitycentric prompting frameworks can extract relevant design knowledge from LCA reports, demonstrated through a case study where an LLM (ChatGPT) is prompted on a provided electric toothbrush LCA report.
Proposed for automatic knowledge extraction from life cycle documents,

![[llm prompting frameworks.png]]


trengths and weaknesses of LLMs in analyzing LCA reports and proposes how future work

facilitating knowledge transfer of sustainability information from these sources and thereby lowering the barrier to sustainability information access
**Methods:**
Thus, we explore alternative prompting frameworks, namely (1) no report queries (akin to zero-shot prompting), whose purpose are to explore the baseline capabilities of the model with no LCA report as input, (2) report summary queries whose purpose are to learn more about the LCA report, and (3) life-cycle stage queries whose purpose are to learn more about each life cycle stage analyzed in the report.

parsing through an LCA document

![[image-3.png|513x451]]


3.1. Proposed prompt templates

A prompt’s core elements include any or all of: [24]: 1. Instruction: a specific task or instruction you want the model to perform 2. Context: external information or additional context that can steer the model to better responses 3. Input: the input or question of interest for a response. 4. Output indicator: the type or format of the output.

![[examle prompt.png|455x274]]

the model is prompted (without any raw LCA reports being used, or no context) with the following example queries: What are the important components of the product of interest to consider? OR What are the important life cycle phases of the product of interest to consider?

3.1.2. Report Summary Queries LLMs are well-known for their summarization abilities, as discussed in Section 2.2,

3.1.2. Report Summary Queries
> Going step-by-step, summarize this document.

3.1.3. Life Cycle Stage Queries Life cycle stages (raw material extraction, manufacturing, distribution, use, and disposal)
this framework is used as a sustainability baseline, with an example query shown below:
> Identify information about the life cycle stage phase of this LCA. OR Identify the life cycle stage with the highest environmental impact.

3.1.4. LCA Expert Queries Previous work by the authors [6] built a framework around how LCA experts seek information when handling LCA reports, and how these techniques can be leveraged to support non-experts in interacting with LCA reports.

> Identify the category. The definition of category is description.

![[different prompting frameworkds.png|496x318]]

LLMs summarization capabilities should be leveraged for priming readers to the main points a report contains • Use established terminology (like life cycle stage definitions) to identify key information from these reports in a focused manner [11] • LLMs generative capabilities can be used for proposing novel sustainable design suggestions during ideatio


@preussLargeLanguageModels2024 
Large language models for life cycle assessments: Opportunities, challenges, and risks 
Nathan Preuss

prompt engineering techniques. most literature

the risk that models cannot take responsibility for generated content can be ameliorated by having the LCA practitioner carefully review the LLM output and take responsibility for decisions made based on the generated content.
@me Agent Human in Loop solutions

MM-LLM Multi-modal large language model
RLHF Reinforcement learning with human feedback
VDB Vector databases


![[Preeuss et al.png]]
Fig. 1. Overview of the topics discussed in this study. An overview of LLMs, including training methods and model variants is given in Section 2. The strengths of LLMs and their application to a comprehensive selection of LCA tasks is given in Section 3. The challenges with using LLMs for LCA tasks are identified in Section 3, but methods to address these challenges are discussed in Section 4, culminating in the perspective of LLM-augmented LCA frameworks to increase LCA quality while spending significantly reduced time on the LCA. Section 5 discusses the risks of using LLMs for LCA tasks and potential mitigation methods.


LLM-augmented LCA frameworks to increase LCA quality while spending significantly reduced time on the LCA
2.1. Architecture
consists of two blocks, an encoder and decoder,
The encodertakes an input, or prompt, and maps it onto a target vector, which the decoder then translates into an output (Sutskever et al., 2014). LLMs are grouped into autoencoding models, autoregressive models, and sequence-to-sequence models, depending on which parts of the transformer architecture are used.
LLMs that only use a decoder are also called autoencoding models, which typically take in a user prompt and generate a response as an output. Common autoencoding models including GPT-4 from OpenAI (OpenAI, 2023), and Gemini from Google among others

When autoencoding models are trained, they attempt to predict the next token in a sequence given the previous tokens, in essence solving a very large conditional probability problem (Min et al., 2024 ).

20 multi-modal benchmarks (Gemini Team et al., 2023), (Pichai), and Sora,
This type of LLM can be useful for LCA tasks that could involve image generations,

![[llm training, architecture and use.png|559x356]]

2.2. Training

the dataset has been processed, it is often tokenized to decrease the computational cost of training.
 inner alignment, LLMs are trained to achieve the goals of the designer (Shen et al., 2023). This goal is typically achieved through minimizing the loss function by tuning the model parameters.

Outer alignment of an LLM occurs when the training objective matches the goal of the human designer (Shen et al., 2023). Outer alignment is generally considered to be achieved if an AI model is considered to be helpful, honest, and harmless (Askell et al., 2021),
and these properties are primarily developed through reinforcement learning with human feedback (RLHF) (Christiano et al., 2017), (Wolf et al., 2023).


LLMs with a larger number of pa rameters in the model outperform smaller models when trained on the same training data by having a response with greater complexity and verisimilitude (Srivastava et al., 2023), (Rosoł et al., 2023), (Brown et al., 2020).

LLMs that have been fine-tuned on a domain-specific task outperform a general LLM (Gururangan et al., 2020). Taking advantage of these findings. some organizations have pre-trained and fine-tuned LLMs on sustainability (Kaiwu), climate (Webersinke et al., 2022), or Intergovernmental Panel on Climate Change (Vaghefi et al., 2023) literature to improve model performance, but no one has yet built an LLM for LCA tasks.

advantages of LLMs, such as improving the accessibility of LCAs, increasing time efficiency, providing expert-level advice, and improving data management.

![[image-4.png]]
