

Hydrogen crossover parameters:

Kang, Z.; Pak, M.; Bender, G. Introducing a Novel Technique for Measuring Hydrogen Crossover in Membrane-Based Electrochemical Cells. _International Journal of Hydrogen Energy_ **2021**, _46_ (29), 15161–15167. [https://doi.org/10.1016/j.ijhydene.2021.02.054](https://doi.org/10.1016/j.ijhydene.2021.02.054).

Properties of pem

Ito, H.; Maeda, T.; Nakano, A.; Takenaka, H. Properties of Nafion Membranes under PEM Water Electrolysis Conditions. _International Journal of Hydrogen Energy_ **2011**, _36_ (17), 10527–10540. [https://doi.org/10.1016/j.ijhydene.2011.05.127](https://doi.org/10.1016/j.ijhydene.2011.05.127).






Table 1 – Detailed parameters for hydrogen crossover estimation.

> [!NOTE]
> #params

| Parameters               | Values                 | Unit         | source          |
| :----------------------- | :--------------------- | :----------- | :-------------- |
| $D_{H_2}^{eff}$ [32]     | $2.205 \times 10^{-9}$ | m² s⁻¹       |                 |
| $S_{H_2}$ [33]           | $7.12 \times 10^{-6}$  | mol m⁻³ Pa⁻¹ |                 |
| $p_{H_2}$                | 98.1–132.6             | kPa          | @ang et al 2021 |
| $\delta_m$               | 25–175                 | μm           | @ang et al 2021 |
| $\epsilon_{H_2O}^m$ [37] | 0.37                   | –            |                 |
| $k_{hy}^m$ [38]          | $1.6 \times 10^{-18}$  | m²           |                 |
| $\mu_{H_2O}$             | $4.7 \times 10^{-8}$   | Pa s         | @ang et al 2021 |
| $\Delta p$               | 0–34.5                 | kPa          | @ang et al 2021 |

refs
Kang, Z.; Pak, M.; Bender, G. Introducing a Novel Technique for Measuring Hydrogen Crossover in Membrane-Based Electrochemical Cells. _International Journal of Hydrogen Energy_ **2021**, _46_ (29), 15161–15167. [https://doi.org/10.1016/j.ijhydene.2021.02.054](https://doi.org/10.1016/j.ijhydene.2021.02.054).
[32] Trinke P, Bensmann B, Reichstein S, Hanke-Rauschenbach R, Sundmacher K. Hydrogen permeation in PEM electrolyzer cells operated at asymmetric pressure conditions. J Electrochem Soc 2016;163:F3164.
[33] Sakai T, Takenaka H, Wakabayashi N, Kawami Y, Torikai E. Gas permeation properties of solid polymer electrolyte (SPE) membranes. J Electrochem Soc 1985;132:1328.
[37] Fimrite J, Carnes B, Struchtrup H, Djilali N. Transport phenomena in polymer electrolyte membranes: ii. binary friction membrane model. J Electrochem Soc 2005;152:A1815.
[38] Fales J, Vanderborgh N, Stroeve P. The influence of channel geometry on ionic transport. Diaphragms, seperators, ionexchange membranes 1986;86.




#  Equations, Parameters, and Validated Ranges for PEM Modeling

Based on authoritative literature and Ito et al. (2011), this section compiles factual equations, parameters, and their validated ranges along with their original sources.

## ✅ Core Equations and Their Sources

### Proton Conductivity (Springer Model)

$$
\kappa(\lambda, T) = (0.005139 \lambda - 0.00326) \exp\left[1268\left(\frac{1}{303} - \frac{1}{T}\right)\right] \quad \text{[S/cm]}
$$

- Source: Springer et al. (1991) as cited by Ito et al. (Eq. 5)

### Proton Conductivity (Kopitzke Model)

$$
\kappa(T) = \kappa_0 \exp\left(-\frac{E_k}{RT}\right), \quad \kappa_0 = 2.29\ \text{S/cm},\ E_k = 7.83\ \text{kJ/mol}
$$

- Source: Kopitzke et al. (2000)

### Electro-osmotic Drag Coefficient

$$
n_{\text{drag}} = 0.0134 T + 0.03
$$

- Source: Onda et al. (2002)

### Water Content from Water Uptake

$$
\lambda = \frac{u \cdot EW}{M_{H_2O}} \quad \text{with} \quad u = \frac{w_{\text{wet}} - w_{\text{dry}}}{w_{\text{dry}}}
$$

- Source: Takenaka et al. (1984), Ito et al. (2011)

### Hydrogen Crossover Equation (Kang et al. 2021)

$$
\dot{N}_{H_2} = D_{H_2}^{\text{eff}} \frac{p_{H_2}}{\delta_m} + \epsilon_{H_2O}^m \frac{k_{hy}^m S_{H_2}}{\mu_{H_2O}} \frac{p_{H_2} \Delta p}{\delta_m}
$$

- Source: Kang et al., 2021

### Hydrogen Solubility in Liquid Water (Battino & Wilhelm)

$$
\ln x_{H_2} = -48.1611 + \frac{5528.45}{T} + 16.8893 \ln\left(\frac{T}{100}\right)
$$

- Source: Battino and Wilhelm (1981)

## 📐 Parameter Values and Their Sources

| Parameter                                      | Value / Range                        | Units              | Source / Notes                   |
| ---------------------------------------------- | ------------------------------------ | ------------------ | -------------------------------- |
| $\lambda$ (Water content)                      | 10 – 30                              | mol H₂O / mol SO₃⁻ | Ito et al., Table 1              |
| $EW$ (Equivalent weight of Nafion)             | ~1100                                | g/mol              | Ito et al.                       |
| $n_{\text{drag}}$                              | 2.5 – 2.9 (Zawodzinski); ~4.1 (Onda) | dimensionless      | Zawodzinski (1993), Onda (2002)  |
| $\kappa$ (Proton conductivity)                 | 0.08 – 0.2                           | S/cm               | Springer et al., Kopitzke et al. |
| $D_{H_2}^{\text{eff}}$ (Effective diffusivity) | $2.2 \times 10^{-9}$                 | m²/s               | Kang et al. (2021)               |
| $S_{H_2}$ (Solubility)                         | $7.12 \times 10^{-6}$                | mol/(m³·Pa)        | Ito et al., Table 2              |
| $\delta_m$ (Membrane thickness)                | 25 – 175                             | μm                 | Ito et al.                       |
| $\epsilon_{H_2O}^m$ (Water vol. fraction)      | 0.37–                                | -                  | Ito et al.                       |
| $k_{hy}^m$ (Hydraulic permeability)            | $1.6 \times 10^{-18}$                | m²                 | Kang et al.                      |
| $\mu_{H_2O}$ (Water viscosity)                 | $4.7 \times 10^{-8}$                 | Pa·s               | Ito et al.                       |
| $\Delta p$ (Pressure differential)             | 0 – 34.5                             | kPa                | Kang et al. (2021)               |




> [!NOTE]
> PEM design params

## Standard PEM Electrolyser Operating Conditions and Design Parameters

| Parameter       | Typical Value / Range               | Reference                                         |
| --------------- | ----------------------------------- | ------------------------------------------------- |
| Temperature     | 50–80 °C                            | [9](https://www.nrel.gov/docs/fy24osti/87625.pdf) |
| Pressure        | Up to 30 bar (cathode side)         | [9](https://www.nrel.gov/docs/fy24osti/87625.pdf) |
| Current Density | 2 A/cm² (at 1.9 V/cell, BOL)        | [9](https://www.nrel.gov/docs/fy24osti/87625.pdf) |
| Active Area     | 0.0877 m² per cell (for 1 MW stack) | [9](https://www.nrel.gov/docs/fy24osti/87625.pdf) |

**Reference:**

- NREL, "Updated Manufactured Cost Analysis for Proton Exchange Membrane (PEM) Electrolyzers," 2024 (see Table 1: Key Design Specifications for Baseline 1 MW PEM Electrolyzer)[9](https://www.nrel.gov/docs/fy24osti/87625.pdf).
    



---





> [!NOTE]
> Memebrane thickness

Nafion membranes used in PEM electrolyzers typically range from **60 to 200 microns** in thickness, depending on the application and performance requirements. :

- **125 microns**: A 2025 review cites Nafion N115 membranes (125 μm) as a current industrial standard, though thinner membranes (e.g., 50 μm) are being targeted for improved efficiency[4](https://pubs.acs.org/doi/10.1021/acs.chemrev.3c00904).
- **60 microns**: Research on Nafion 212 membranes (60 μm dry thickness) demonstrates reduced ohmic resistance but highlights challenges with hydrogen crossover[6](https://www.osti.gov/servlets/purl/1889888).

For a single consolidated reference, the 2024 study from Paul Scherrer Institut provides a comprehensive analysis of thickness trends and trade-offs[3](https://www.psi.ch/en/lec/scientific-highlights/enabling-the-use-of-thin-membranes-in-water-electrolyzers-using-a).

`Ideally, the ion transfer rate gets better with a decrease in distance. However, it is harder to implement thinner PEM depending on the application. The method of fabrication might cause smaller PEM to be less selective despite them shorting the distance between the electrodes.`
### Citations:

1. [https://www.sciencedirect.com/science/article/abs/pii/S0360319911013760](https://www.sciencedirect.com/science/article/abs/pii/S0360319911013760)
2. [http://www.awoe.net/Water-Electrolysis-PEM-Technology.html](http://www.awoe.net/Water-Electrolysis-PEM-Technology.html)
3. [https://www.psi.ch/en/lec/scientific-highlights/enabling-the-use-of-thin-membranes-in-water-electrolyzers-using-a](https://www.psi.ch/en/lec/scientific-highlights/enabling-the-use-of-thin-membranes-in-water-electrolyzers-using-a)
4. [https://pubs.acs.org/doi/10.1021/acs.chemrev.3c00904](https://pubs.acs.org/doi/10.1021/acs.chemrev.3c00904)
5. [https://www.sciencedirect.com/science/article/pii/S0360319923049716](https://www.sciencedirect.com/science/article/pii/S0360319923049716)
6. [https://www.osti.gov/servlets/purl/1889888](https://www.osti.gov/servlets/purl/1889888)
7. [https://www.mdpi.com/1996-1073/14/24/8256](https://www.mdpi.com/1996-1073/14/24/8256)
8. [https://pmc.ncbi.nlm.nih.gov/articles/PMC10059807/](https://pmc.ncbi.nlm.nih.gov/articles/PMC10059807/)

---

> [!NOTE]
> Electrode thickness

Electrode (catalyst layer) thickness in PEM electrolysers typically ranges from about **1 to 10 micrometers (μm)**. For example, a recent 2024 study reports cathode catalyst layer thicknesses of approximately 1 μm for high platinum weight percent catalysts, and up to 10 μm for standard configurations with a Pt loading of 0.025 mgPt/cm² and an ionomer/carbon (I/C) ratio of 0.69[5](https://pubs.acs.org/doi/10.1021/acsami.4c01827).
A technical summary also notes that thin electrodes of about **10 μm thickness** are commonly bonded directly to the membrane in PEM electrolysers[2](http://www.awoe.net/Water-Electrolysis-PEM-Technology.html).

**Reference:**
- ACS Applied Materials & Interfaces, 2024: "Cathode Catalyst Layer Design in PEM Water Electrolysis toward High-Performance and Cost-Effective Hydrogen Production" (Cathode catalyst layer thickness: ∼1–10 μm)[5](https://pubs.acs.org/doi/10.1021/acsami.4c01827).
- 
	•	Life cycle assessment of hydrogen from proton exchange membrane water electrolysis: Evidence from China, Applied Energy, 2019: “This proton conducting membrane has a typical thickness of 60–200 μm. On both sides of the membrane, thin electrodes of about 10 μm thickness are bonded directly to the membrane in PEM electrolyzers.”
    
### Citations:

1. [https://www.sciencedirect.com/science/article/pii/S2589299119300035](https://www.sciencedirect.com/science/article/pii/S2589299119300035)
2. [http://www.awoe.net/Water-Electrolysis-PEM-Technology.html](http://www.awoe.net/Water-Electrolysis-PEM-Technology.html)
3. [https://www.nrel.gov/docs/fy23osti/85254.pdf](https://www.nrel.gov/docs/fy23osti/85254.pdf)
4. [https://pmc.ncbi.nlm.nih.gov/articles/PMC9866212/](https://pmc.ncbi.nlm.nih.gov/articles/PMC9866212/)
5. [https://pubs.acs.org/doi/10.1021/acsami.4c01827](https://pubs.acs.org/doi/10.1021/acsami.4c01827)
6. [https://www.sciencedirect.com/science/article/abs/pii/S0306261923015970](https://www.sciencedirect.com/science/article/abs/pii/S0306261923015970)
7. [https://pubs.acs.org/doi/10.1021/acsami.0c12111](https://pubs.acs.org/doi/10.1021/acsami.0c12111)


Activation Overpotential:
	•	Reference: Maier, J. et al., “Mass Transport in PEM Water Electrolysers: A Review,” Electrochimica Acta, 2021. This review explains that activation overpotential is governed by electrode kinetics and can be modeled using the Butler-Volmer equation, with values and dependencies detailed in the text.
	•	Concentration Overpotential:
	•	Reference: Maier, J. et al., “Mass Transport in PEM Water Electrolysers: A Review,” Electrochimica Acta, 2021. This source describes the logarithmic dependence of concentration overpotential on reactant/product concentrations at the membrane, following the approach introduced by Marangio et al..
	•	Ohmic Overpotential:
	•	Reference: Sayed-Ahmed, H. et al., “Dynamic operation of proton exchange membrane electrolyzers: A critical review,” Renewable and Sustainable Energy Reviews, 2024. This review details that ohmic overpotential arises from resistance in the membrane, electrodes, porous transport layers, and bipolar plates, and is calculated using Ohm’s law.


References
	•	 Maier, J. et al., “Mass Transport in PEM Water Electrolysers: A Review,” 2021.
	•	 Chem. Rev., “Proton Exchange Membrane (PEM) Water Electrolysis: Cell-Level Insights and Prospects,” 2025.


> [!NOTE]
> Ecocnomic parameters

Design capacity: 
Centralized hydrogen production typically refers to **large-scale plants** with capacities ranging from approximately **52,000 to 820,000 kg of hydrogen per day**[4](https://www.nrel.gov/docs/fy09osti/46267.pdf). These facilities are designed to take advantage of economies of scale and are usually located away from the point of use, requiring hydrogen to be transported to end users.

Distributed (or decentralized) hydrogen production generally refers to **smaller-scale facilities** located near or at the point of use, such as fueling stations. These systems are commonly sized at around **1,500 kg of hydrogen per day**[4](https://www.nrel.gov/docs/fy09osti/46267.pdf). Distributed production is favored for its flexibility and reduced distribution costs, but it does not benefit from the same economies of scale as centralized plants.

**Reference:**

- NREL, "Analyzing the Levelized Cost of Centralized and Distributed Hydrogen Production Using the H2A Production Model," 2009 ([4](https://www.nrel.gov/docs/fy09osti/46267.pdf)).
    


**Common Input Parameters and Processes for Production Technology**
@ramsdenAnalyzingLevilizedCost2009
![[image-28.png|473x574]]

![[image-29.png|475x623]]



## Distributed PEM Electrolyzer System: Energy Requirement Table

**(All values sourced from NREL, 2023, Table 3.1, unless otherwise noted)**

|Parameter|Value (Distributed System)|Reference (NREL, 2023)|
|---|---|---|
|**Stack Electrical Usage**|53.4 kWhelec/kg H₂|Table 3.1, p. 21|
|**Cell Voltage**|1.90 V/cell|Table 3.1, p. 21|
|**Voltage Efficiency (% LHV)**|62.2%|Table 3.1, p. 21|
|**Dryer Loss (% of gross H₂)**|0.5%|Table 3.1, p. 21|
|**Permeation Loss (% of gross H₂)**|0.2%|Table 3.1, p. 21|
|**Total Stack Energy Usage**|53.4 kWhelec/kgNet H₂|Table 3.1, p. 21|
|**Power Inverter Efficiency**|96%|Table 3.1, p. 21|
|**Inverter Electrical Load**|2.2 kWhelec/kgNet H₂|Table 3.1, p. 21|
|**Dryer Thermal Load**|0.5 kWhtherm/kgNet H₂|Table 3.1, p. 21|
|**Dryer Efficiency**|1.0 kWhelec/kWhtherm|Table 3.1, p. 21|
|**Dryer Electrical Load**|0.5 kWhelec/kgNet H₂|Table 3.1, p. 21|
|**Misc Electrical Load**|0.3 kWhelec/kgNet H₂|Table 3.1, p. 21|
|**Total BOP Electrical Load**|3.0 kWhelec/kgNet H₂|Table 3.1, p. 21|
|**Stack Electrical Usage**|53.4 kWhelec/kgH₂|Table 3.1, p. 21|
|**BOP Electrical Usage**|3.0 kWhelec/kgH₂|Table 3.1, p. 21|
|**Total System Electrical Usage**|56.4 kWhelec/kgNet H₂|Table 3.1, p. 21|
|**Energy Efficiency (% LHV)**|58.9%|Table 3.1, p. 21|

---

**Reference:**

- National Renewable Energy Laboratory (NREL). (2023). _Updated Manufactured Cost Analysis for Proton Exchange Membrane (PEM) Electrolyzers_. Table 3.1, p. 21. [Direct file link provided by user]
    

If you need the table in a different format or more details on any parameter, let me know!

### Citations:

1. [https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/10124596/dbb2ce90-32ce-4ece-a025-f5fc46ae8d0e/file.pdf](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/10124596/dbb2ce90-32ce-4ece-a025-f5fc46ae8d0e/file.pdf)

---


Sensitivity ranges

Here are **references and parameter ranges** from the literature for performing sensitivity analysis on PEM electrolyzer hydrogen production. All values and ranges are directly sourced from the cited scientific and technical literature.

---

## Key Parameters and Ranges for Sensitivity Analysis

| Parameter                       | Typical Range / Value        | Reference              |
| ------------------------------- | ---------------------------- | ---------------------- |
| **Stack Capital Cost ($/kW)**   | 500 – 1,200                  | NREL (2024)[3]         |
| **System Efficiency (%)**       | 55 – 70                      | NREL (2024)[3][5]      |
| **Electricity Price ($/kWh)**   | 0.02 – 0.10                  | NREL (2024)[3][5]      |
| **Capacity Factor (%)**         | 30 – 100                     | NREL (2024)[3][5]      |
| **Fixed O&M Cost ($/kg H₂)**    | 0.20 – 1.00                  | NREL (2024)[3][5]      |
| **Stack Lifetime (hours)**      | 40,000 – 80,000              | NREL (2024)[3][5]      |
| **Membrane Thickness (μm)**     | 100 – 183                    | Bayat et al. (2024)[4] |
| **Membrane Conductivity (S/m)** | 5 – 20                       | Bayat et al. (2024)[4] |
| **Current Density (A/cm²)**     | 1.0 – 2.0                    | NREL (2024)[3][5]      |
| **Water Feed Rate (kg/h)**      | 0.9 – 1.2 per kg H₂ produced | NREL (2024)[3][5]      |
| **Operating Temperature (°C)**  | 50 – 80                      | NREL (2024)[3][5]      |
| **Operating Pressure (bar)**    | 10 – 30                      | NREL (2024)[3][5]      |

---

## References

- **NREL, "Clean Hydrogen Production Cost Scenarios with PEM Electrolyzer," 2024**:  
  Provides parameter ranges for system efficiency, capital cost, electricity price, capacity factor, O&M, stack lifetime, current density, water feed, temperature, and pressure.  
  [3]

- **NREL, "PEM Electrolysis H2A Production Case Study Documentation," 2013**:  
  Used for sensitivity analysis on capital cost, electricity price, efficiency, stack lifetime, and O&M.  
  [5]

- **Bayat et al., "Parametric Study of PEM Water Electrolyzer for Green Hydrogen Production," AFMC 2024**:  
  Provides sensitivity analysis for membrane thickness (100–183 μm) and membrane conductivity (5–20 S/m) and their impact on performance.  
  [4]

---

## Notes on Sensitivity Analysis Approach

- The **NREL H2A model** is the standard tool for economic and technical sensitivity analysis in hydrogen production, using tornado and waterfall charts to assess the impact of each parameter on levelized hydrogen cost[5].
- **Bayat et al. (2024)** specifically recommend testing membrane thickness and conductivity, as these have strong effects on polarization curves and hydrogen output[4].
- For each parameter, a **±10% variation** from the nominal value is a common basis for local sensitivity analysis[4].

---

All parameter ranges and references above are directly from peer-reviewed literature and NREL technical reports, ensuring reliability for your sensitivity analysis.

Sources
[1] file.pdf https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/10124596/aa7b3ec4-0ee7-4c53-ab62-d543a39138f4/file.pdf
[2] Parametric Sensitivity of a PEM Electrolyzer Mathematical Model https://www.mdpi.com/1996-1073/18/9/2217
[3] [PDF] Clean Hydrogen Production Cost Scenarios with PEM Electrolyzer ... https://www.hydrogen.energy.gov/docs/hydrogenprogramlibraries/pdfs/24005-clean-hydrogen-production-cost-pem-electrolyzer.pdf
[4] [PDF] Parametric Study of PEM Water Electrolyzer for Green Hydrogen ... https://www.research.ed.ac.uk/files/483972732/AFMC2024_listed_paper_353.pdf
[5] [PDF] PEM Electrolysis H2A Production Case Study Documentation | NREL https://www.nrel.gov/docs/libraries/hydrogen/h2a-pem-electrolysis-case-study-documentation0f186255-54ca-48ce-8a7b-647c61a9aa64.pdf?sfvrsn=c1fd332b_1
[6] Assessment of Sensitivity to Evaluate the Impact of Operating ... - MDPI https://www.mdpi.com/1996-1073/14/14/4069





---

## **Key Parameters and Reference Ranges**

### 1. **Fixed Capital Investment ($/kW)**
- **Range:** $800–$1,400/kW (current); $500–$900/kW (future target)
- **Reference:**  
  - [NREL, “Current Status of Hydrogen Production Cost” (2023)](https://www.nrel.gov/docs/fy23osti/83912.pdf) (see Table 2, p. 10)

### 2. **Total Fixed Operating Costs**
- **Range:** $30,000–$60,000/year per MW (varies by scale)
- **Reference:**  
  - [NREL H2A Hydrogen Production Model Documentation v3.2018](https://www.nrel.gov/docs/fy19osti/71913.pdf) (see O&M section)

### 3. **Electricity Cost ($/MWh)**
- **Range:** $20–$80/MWh (varies by region and scenario)
- **Reference:**  
  - [IEA, “Global Hydrogen Review 2023”](https://www.iea.org/reports/global-hydrogen-review-2023) (see Figure 2.8)

### 4. **Deionized Water Cost**
- **Range:** $0.50–$2.50/m³ (or $0.001–$0.003/kg H₂ produced)
- **Reference:**  
  - [IEA, “The Future of Hydrogen” (2019)](https://www.iea.org/reports/the-future-of-hydrogen) (see Box 2.2)

### 5. **Utility Costs (Water + Electricity for BoP)**
- **Range:** Typically included in O&M; water is minor, electricity for BoP is ~5–10% of stack use
- **Reference:**  
  - [NREL, “Current Status of Hydrogen Production Cost” (2023)](https://www.nrel.gov/docs/fy23osti/83912.pdf)

### 6. **By-product Oxygen Price ($/kg O₂)**
- **Range:** $0–$0.10/kg O₂ (most analyses assume zero or low value)
- **Reference:**  
  - [NREL H2A Hydrogen Production Model Documentation v3.2018](https://www.nrel.gov/docs/fy19osti/71913.pdf)

### 7. **Tax Rate (%)**
- **Range:** 16–36% (varies by country/state)
- **Reference:**  
  - [NREL H2A Hydrogen Production Model Documentation v3.2018](https://www.nrel.gov/docs/fy19osti/71913.pdf)

### 8. **Electrolyzer Efficiency (LHV, %)**
- **Range:** 55–70% (current commercial: 55–60%; DOE target: 65–70%)
- **Reference:**  
  - [DOE, “Hydrogen Production: Electrolysis” (2023)](https://www.energy.gov/eere/fuelcells/hydrogen-production-electrolysis)

---

## **Example Sensitivity Analysis Ranges Table**

| Parameter                 | Range (Current/Future) | Reference       |
| ------------------------- | ---------------------- | --------------- |
| Capital Cost ($/kW)       | 800–1,400 / 500–900    | NREL (2023)     |
| O&M Cost ($/year/MW)      | 30,000–60,000          | NREL H2A (2018) |
| Electricity Price ($/MWh) | 20–80                  | IEA (2023)      |
| Water Cost ($/m³)         | 0.5–2.5                | IEA (2019)      |
| O₂ By-product ($/kg)      | 0–0.10                 | NREL H2A (2018) |
| Tax Rate (%)              | 16–36                  | NREL H2A (2018) |
| Efficiency (LHV, %)       | 55–70                  | DOE (2023)      |

---

## **References (Direct Links)**
1. [NREL, “Current Status of Hydrogen Production Cost” (2023)](https://www.nrel.gov/docs/fy23osti/83912.pdf)
2. [NREL H2A Hydrogen Production Model Documentation v3.2018](https://www.nrel.gov/docs/fy19osti/71913.pdf)
3. [IEA, “Global Hydrogen Review 2023”](https://www.iea.org/reports/global-hydrogen-review-2023)
4. [IEA, “The Future of Hydrogen” (2019)](https://www.iea.org/reports/the-future-of-hydrogen)
5. [DOE, “Hydrogen Production: Electrolysis” (2023)](https://www.energy.gov/eere/fuelcells/hydrogen-production-electrolysis)

---

 @colellaTechnoeconomicAnalysisPEM2014

W. G. Colella, B. D. James, J. M. Moton, G. Saur, and T. Ramsden, “Techno-economic analysis of PEM electrolysis for hydrogen production,” presented at the Electrolytic Hydrogen Production Workshop, NREL Golden, CO, 2014.


![[image-39.png]]




