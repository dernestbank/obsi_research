
---

**Meeting Summary: Green Hydrogen Modeling Discussion**

  
**Date:** Thursday

**Time:** 09:05

**Participants:** Ernest 1 (Presenter), Speaker 2 (Advisor)

---

**Key Discussion Points**

1. **Project Update & Objectives**

• The presenter introduced updates to their green hydrogen cost model.

• Originally, the model was based on electricity prices only; it now incorporates **renewable energy** components, transitioning towards **green hydrogen** modeling.

• Key additions include modeling the **energy system**, **plant costing**, and **electrolyzer costs**.

2. **Model Development**

• The model integrates a **cost function** with variables (C1, C2, C3, C4) derived from literature.

• C1–C4 are intended to represent:

• **C1**: Base cost at minimum capacity.

• **C2**: Linear scaling for smaller capacities.

• **C3**: Economies of scale at larger capacities.

• **C4**: Diminishing cost effects at very high capacities (can become negative).

3. **Data Sources & Validation**

• Equations were referenced from **Paper 1**, while data were primarily sourced from **Paper 2**, which provided estimates of electrolyzer costs.

• A significant issue identified was incorrect data usage due to misaligned adjustment years (2020 adjusted vs. raw data).

• After correction, the model’s fit improved, revealing non-linear trends consistent with economies of scale.

4. **Presentation Feedback**

• The advisor stressed the importance of:

• Clear **definitions for all variables** and constants.

• Distinct slide formatting separating **literature-derived** and **custom model** outputs.

• Consistency in **units** (e.g., megawatts vs. kilowatts).

• Explicitly noting data sources and years of estimation.

5. **Accuracy and R² Concerns**

• The presenter reported an **R² of 0.53**.

• The advisor indicated this might be borderline acceptable depending on the **application domain**, but emphasized comparing this value with standard references (e.g., Aspen models or heuristic accuracy benchmarks).

• Importance of aligning with **order-of-magnitude methods** and established **accuracy levels** (20–35% uncertainty ranges depending on approach).
Seider heuristics as benchmarck
What 

6. **Future Steps**

• Improve slide clarity, especially for defining equations and showcasing data transformations.

• Consider increasing data points or adjusting the model to further improve R².

• Benchmark against literature models and clarify the methodology used for cost estimation.

• Review and integrate formal citation styles and data reference notations.

---

**Action Items**

• **[Presenter]** Refine definitions for model variables (C1–C4, PL, etc.) and integrate them clearly into slides.

• **[Presenter]** Reformat slides to distinguish between literature and custom model results.

• **[Presenter]** Add units and textual annotations directly on plots.

• **[Presenter]** Compare the model’s accuracy to benchmarks (Aspen, literature models).

• **[Presenter]** Clarify and correctly reference data sources and equations.

• **[Presenter]** Consider retaking the writing course or arranging accommodations to improve academic presentation skills.

---

Let me know if you’d like this in a different format or turned into a meeting minutes template.




---- notes after meeting
“Product and Process Design Principles” by Warren D. Seider et al., cost estimation is categorized into three levels, each with varying degrees of uncertainty:

1. **Order-of-Magnitude Estimate (Class 5):** Also known as a “factored estimate,” this preliminary assessment is based on limited data, often derived from similar previous projects or capacity scaling. The expected accuracy range is typically within ±50%.

2. **Study Estimate (Class 4):** Referred to as a “budget estimate,” this level utilizes more detailed information, including preliminary process flow diagrams and equipment specifications. The accuracy range for study estimates is generally within ±30%.

3. **Preliminary Estimate (Class 3):** Known as a “definitive estimate,” this assessment is based on comprehensive engineering data, such as detailed process designs and equipment quotes. The accuracy range for preliminary estimates is typically within ±20%.

  

These classifications align with industry-standard practices for capital cost estimation, where the accuracy of an estimate improves as more detailed information becomes available

@seiderProductProcessDesign 
“Product and Process Design Principles” by Warren D. Seider et al., cost estimation levels are discussed in Chapter 16, titled “Capital Cost Estimating,” specifically in Section 16.2, “Types of Capital Cost Estimates.” The three levels of cost estimates—Order-of-Magnitude, Study, and Preliminary—are detailed in this section.
page numb: 445. 
481

Method 1. Order-of-Magnitude Estimate (based
on the method of Hill, 1956)
The method is particularly useful for low-pressure petrochemical plants, where it has an accuracy of approximately ±50%. For moderate-to-highpressurepro-
cesses, the actual cost may be as much as twice the estimate. To
produce the estimate, only two things are needed


Method 2. Study Estimate (based on the overall factor method of Lang, 1947a, b, and 1948)
making a study estimate than for the preceding order-of-magnitude
estimate. But the accuracy is improved to ±35%. 


Method 3. Preliminary Estimate (Based on the Individual Factors Method of Guthrie, 1969, 1974)

but the accuracy is improved to perhaps ±20%. To apply the method, the
f.o.b. purchase cost of each piece of major equipment must be
estimated, as was the case with the Lang method.



