




### **Appendix A: PEM Electrolyzer Model Parameters**

This section details the electrochemical, physical, and material parameters used for the PEM electrolyzer model.

#### **Table A.1: PEM Electrochemical and Physical Parameters**

| Parameter                         | Symbol | Value              | Basis & Reference |
| :-------------------------------- | :----- | :----------------- | :---------------- |
| **Constants**                     |        |                    |                   |
| Faraday Constant                  | F      | 96,485.3           | C/mol             |
| Universal Gas Constant            | R      | 8.314              | J/(mol·K)         |
| Number of Electrons Transferred   | z      | 2                  | -                 |
| **Operating Conditions**          |        |                    |                   |
| Cell Operating Temperature        | T      | 333.15             | K (60 °C)         |
| Anode Operating Pressure          | Pa​    | 1                  | bar               |
| Cathode Operating Pressure        | Pc​    | 30                 | bar               |
| **Electrode & Membrane Geometry** |        |                    |                   |
| Membrane Type                     | -      | Nafion™ 117 / PFSA | -                 |
| Membrane Thickness                | tm​    | 178                | µm                |
| Electrode Thickness               | tel​   | 200                | µm                |
| Cell Active Area                  | Acell​ | 877                | cm²               |
| **Material Properties**           |        |                    |                   |
| Anode Catalyst Loading (IrO₂)     | -      | 1.54               | mg/cm²            |
| Cathode Catalyst Loading (Pt)     | -      | 0.4                | mg/cm²            |
| Porosity (GDL/Catalyst Layer)     | ε      | 0.3                | -                 |
| Resistivity of Titanium (BPP)     | ρTi​   | 5.0 x 10⁻⁵         | Ω·m               |
| Resistivity of Carbon Paper (GDL) | ρCP​   | 8.0 x 10⁻⁴         | Ω·m               |


#### **Table A2: Catalyst Performance Parameters**

_This table summarizes literature values for catalyst loading and the resulting kinetic parameters, which are highly dependent on the specific materials used._

| Catalyst System            | Anode Loading   | Cathode Loading | Anode Exchange Current Density (i0,a​) | Cathode Exchange Current Density (i0,c​) | Reference              |
| :------------------------- | :-------------- | :-------------- | :------------------------------------- | :--------------------------------------- | :--------------------- |
| **Model Input Assumption** | **1.54 mg/cm²** | **0.4 mg/cm²**  | **2.62 x 10⁻⁶ A/cm²**                  | **1.0 x 10⁻³ A/cm²**                     | **This Study**         |
| Pt–Ir / Pt                 | -               | -               | 1.0 x 10⁻¹² A/cm²                      | 1.0 x 10⁻³ A/cm²                         | Choi et al. (2004)     |
| Pt–Ir / Pt                 | -               | -               | 1.65 x 10⁻⁸ A/cm²                      | 9.0 x 10⁻² A/cm²                         | Harrison et al. (2005) |
| Pt–Ir / Pt                 | 2.0 mg/cm²      | 0.6 mg/cm²      | 1.0 x 10⁻⁷ A/cm²                       | 1.0 x 10⁻³ A/cm²                         | Marangio et al. (2009) |


#### **Table A.2: Electrochemical Kinetic & Transport Parameters**

| Parameter                            | Symbol | Value       | Basis & Reference |
| :----------------------------------- | :----- | :---------- | :---------------- |
| **Kinetics**                         |        |             |                   |
| Anodic Charge Transfer Coefficient   | αa​    | 2.0         | -                 |
| Cathodic Charge Transfer Coefficient | αc​    | 0.5         | -                 |
| Anode Exchange Current Density       | i0,a​  | 2.62 x 10⁻⁶ | A/cm²             |
| Cathode Exchange Current Density     | i0,c​  | 1.0 x 10⁻³  | A/cm²             |
| **Mass Transport**                   |        |             |                   |
| Limiting Current Density             | iL​    | 6.0         | A/cm²             |
| Water Dynamic Viscosity (at 60°C)    | μH2​O​ | 4.67 x 10⁻⁴ | Pa·s              |
| Water Density                        | ρH2​O​ | 983.2       | kg/m³             |

---

### **Appendix B: Energy System & Plant-Level Assumptions**

This section details the parameters for the renewable energy system components and the overall plant performance specifications.

#### **Table B.1: PV System Model Parameters**

| Parameter                     | Symbol   | Value   | Basis & Reference |
| :---------------------------- | :------- | :------ | :---------------- |
| STC Irradiance                | GSTC​    | 1000    | W/m²              |
| STC Cell Temperature          | TSTC​    | 25      | °C                |
| System Derating Factor        | fderate​ | 0.90    | -                 |
| Annual Degradation Rate       | -        | 0.5%    | per year          |
| Power Temperature Coefficient | αp​      | -0.0035 | /°C               |
| Nominal Operating Cell Temp.  | NOCT     | 45      | °C                |
| Site Latitude                 | ϕ        | 40      | degrees           |
| Panel Tilt Angle              | θPV​     | 25      | degrees           |

#### **Table B.2: Wind System Model Parameters**

| Parameter                         | Symbol    | Value     | Basis & Reference |
| :-------------------------------- | :-------- | :-------- | :---------------- |
| Drivetrain & Generator Efficiency | ηWT​      | 0.94      | -                 |
| Air Density (sea level)           | ρ         | 1.225     | kg/m³             |
| Power Coefficient Parameters      | c0​..c11​ | See Table | -                 |
| Weibull Shape Parameter           | k         | 2.0       | -                 |
| Weibull Scale Parameter           | λ         | 7.0       | m/s               |
| Cut-in Wind Speed                 | vcin​     | 3.0       | m/s               |
| Rated Wind Speed                  | vr​       | 13.0      | m/s               |
| Cut-out Wind Speed                | vcout​    | 25.0      | m/s               |

#### **Table B.3: Overall Plant Operating Assumptions**

| Parameter                           | Value  | Unit      | Basis & Reference                                     |
| :---------------------------------- | :----- | :-------- | :---------------------------------------------------- |
| Hydrogen Production Capacity        | 10,000 | kg/day    | Design Target                                         |
| Electrolyzer System Capacity Factor | 90%    | -         | Based on H2A model; high availability assumed         |
| Total System Energy Consumption     | 54.3   | kWh/kg H₂ | Design basis from H2A Centralized PEM model           |
| Stack-only Energy Consumption       | 49.0   | kWh/kg H₂ | Design basis from H2A Centralized PEM model           |
| Balance of Plant (BOP) Consumption  | 5.3    | kWh/kg H₂ | Calculated difference, includes drying, cooling, etc. |
| Renewable Energy (Wind) Capacity    | 10     | MW        | System design assumption                              |
| Wind Capacity Factor                | 34%    | -         | Site-specific assumption                              |
| PV Capacity                         | 0      | MW        | Scenario assumption (wind-only)                       |

---

### **Appendix C: Economic and Financial Assumptions**

This section details the cost data and financial parameters used for the techno-economic analysis, primarily based on the NREL H2A (Hydrogen Analysis) framework.

#### **Table C.1: Capital Costs (CapEx) - 2023 USD**

| Item                                     | Value                   | Basis & Reference                                             |
| :--------------------------------------- | :---------------------- | :------------------------------------------------------------ |
| **Direct Capital Cost**                  |                         |                                                               |
| Uninstalled Electrolyzer System          | $995 / kW               | Based on NREL H2A PEM cost projections (Badgett et al., 2024) |
| Installation Factor                      | 12% of uninstalled cost | H2A model default                                             |
| **Indirect Capital Costs**               |                         | (% of Total Direct Cost unless specified)                     |
| Site Preparation & Construction          | Variable                | H2A defaults based on AACE standards                          |
| Engineering & Design                     | Variable                | H2A defaults                                                  |
| Project Contingency                      | 15%                     | H2A model default                                             |
| **Total Fixed Capital Investment (FCI)** | **$27,455,339**         | Sum of direct and indirect costs                              |
| Working Capital                          | 15% of FCI              | H2A model default                                             |

#### **Table C.2: Operating Costs (OpEx) - 2023 USD**

|Item|Value|Basis & Reference|
|:--|:--|:--|
|**Fixed OpEx**|||
|Maintenance & Repairs|5% of direct capital/year|H2A model default|
|Labor, G&A, Taxes, Insurance|Variable|Calculated based on H2A defaults for labor rates and tax law|
|**Total Fixed OpEx**|**$4,771,667 / year**|Sum of fixed cost items|
|**Variable OpEx**|||
|Electricity Price (Grid)|$0.07 / kWh|U.S. industrial average (EIA, 2024)|
|Deionized Water Cost|$0.007 / gallon|H2A model default|
|Oxygen Byproduct Credit|($0.03) / kg|Assumed credit for sold oxygen|
|**Total Variable OpEx (at 90% CF)**|**~$18,575,000 / year**|Sum of variable costs, dominated by electricity|

#### **Table C.3: Financial Assumptions**

|Parameter|Value|Basis & Reference|
|:--|:--|:--|
|Plant Life|25 years|Typical for industrial plants and PPA agreements|
|Stack Replacement Interval|10 years|Assumed lifetime based on degradation|
|Discount Rate / WACC|10% (real)|Investor hurdle rate for mature projects|
|Corporate Tax Rate (Combined)|27%|Assumed federal + state average|
|Depreciation Schedule|MACRS|U.S. standard for accelerated depreciation|

---

### **References**


















Hydrogen economy and policies

1. Hydrogen economy and Policy Landscape

Hydrogen has become a pivotal energy carrier in global decarbonization strategies.  Before the end of 2019 only five countries had issued national hydrogen strategies, but a year later nearly 20 countries had released plans (with at least 10 more forthcoming), and industry had announced ~25 GW of electrolyzer capacity for green hydrogen by 2026[Box](https://app.box.com/file/1885558866037). In the European Union, hydrogen features prominently in climate initiatives (e.g. the “Fit for 55” package and REPowerEU plan) with targets for tens of gigawatts of electrolyzers by 2030, alongside regulations to define renewable hydrogen. The United States through the Department of Energy’s “Hydrogen Shot” aims for agenda “$1 for 1 kg in 1 decade,” i.e. $1/kg H₂ by 2031[Box](https://app.box.com/file/1885558634189)[Box](https://app.box.com/file/1885558634189) . The 2022 Inflation Reduction Act created a new **Section 45V** clean hydrogen production tax credit up to $3/kg for hydrogen produced with a life-cycle carbon intensity <0.45 kg CO₂e per kg H₂[Box](https://app.box.com/file/1900826134981). Additionally, projects can opt for a 30% investment tax credit in lieu of the production credit if they commence construction by 2033 and meet labor standards[Box](https://app.box.com/file/1900826134981). Such incentives, alongside $8 billion appropriated for at least four regional clean hydrogen hubs (now expanded to seven hubs)[Box](https://app.box.com/file/1900826134981), signal robust U.S. federal support to accelerate a low-cost, clean hydrogen economy.
A critical regulatory development around “green” hydrogen is the definition of criteria for **additionality, deliverability, and temporal matching** of renewable power. These principles are intended to ensure that electrolytic hydrogen credited as “clean” is truly powered by new, clean energy sources rather than diverting existing generation. The U.S. Treasury’s proposed rules for 45V (and the finalized guidance in 2024) included three pillars for grid-connected electrolyzers using renewable electricity: (i) Incrementality – the renewable power source must be new or incremental (generally in operation ≤36 months before the H₂ facility; (ii) **Temporal matching** – the hydrogen production must be matched in time with renewable generation (hourly matching to be required by 2030); and (iii) Geographical deliverability – the renewable source must be located in the same region or electrically deliverable to the electrolyzer. In other words, projects claiming the credit via grid power need to procure Energy Attribute Certificates (EACs) from new renewable plants, ensure those EACs correspond to the same hour of H₂ production (after a transitional period of annual matching up to 2030), and source power from the same or an adjacent grid region. These requirements are designed to guarantee that “clean” hydrogen production truly adds renewable energy to the system and minimizes associated CO₂. The EU has pursued a similar approach in its Delegated Act on Renewable Hydrogen, emphasizing **additionality** of renewables, **temporal** and **geographic correlation** for grid-supplied electricity.

Over 95% of global hydrogen (approximately 70–90 million tonnes annually) is produced via steam methane reforming of natural gas or coal gasification, processes that emit large volumes of CO₂[Box](https://app.box.com/file/1885559555715)[Box](https://app.box.com/file/1885558866037). This status quo yields cheap hydrogen (often $1–2/kg) but negates climate goals. Transitioning to green hydrogen (from electrolysis with renewable power) or even lower-carbon **“blue” hydrogen** (from fossil fuels with carbon capture) will require massive investment and policy support[Box](https://app.box.com/file/1885558866037)[Box](https://app.box.com/file/1885558866037). The cost of green hydrogen currently averages 2–3 times higher than blue hydrogen; for example, fossil-based H₂ can cost $1–3/kg, whereas electrolytic hydrogen using low-carbon electricity is about $3.5–7.5/kg under current costs[Box](https://app.box.com/file/1900826134981). This gap is primarily because electricity input dominates production cost – roughly 50–60% of the levelized cost of hydrogen (LCOH) – making green H₂ very sensitive to power prices[Box](https://app.box.com/file/1885558866037)[Box](https://app.box.com/file/1885558866037). High capital costs of electrolyzers are the second major factor[Box](https://app.box.com/file/1885558866037).
A hydrogen economy instability arises in that without significant cost reductions, clean hydrogen cannot easily compete with grey hydrogen[Box](https://app.box.com/file/1900826134981)[Box](https://app.box.com/file/1900826134981). PEM electrolyzers rely on scarce **iridium** (for catalysts) and **gallium/platinum-coated** components, and a rapid scale-up in PEM deployment could strain the supply or drive up prices of these critical materials[Box](https://app.box.com/file/1885559555715)[Box](https://app.box.com/file/1885559555715). For instance, iridium is one of the rarest elements in Earth’s crust (~0.001 ppm) and wider adoption of PEM electrolysis would significantly increase global Ir demand (currently also driven by electronics and catalysis), risking price escalation[Box](https://app.box.com/file/1885559555715)[Box](https://app.box.com/file/1885559555715). This supply risk underscores the importance of R&D into  substituting noble metals in electrolyzers. Projections for green hydrogen economy remain optimistic despite these challenges . [Box](https://app.box.com/file/1900826134981)[Box](https://app.box.com/file/1900826134981).  Recent data from the International Energy Agency’s Hydrogen Projects Database documented 1,219 hydrogen projects worldwide slated for commissioning between 2020 and 2030[Box](https://app.box.com/file/1900826134981).
Hydrogen is often classified by a color taxonomy denoting production method and carbon footprint. **Green hydrogen** refers to H₂ produced via water electrolysis powered by renewable energy (solar, wind, hydro, etc.), yielding zero direct CO₂ emissions[Box](https://app.box.com/file/1885558866037). **Grey hydrogen** is made from fossil fuels without emissions mitigation (e.g. natural gas reforming or coal gasification releasing CO₂ to the air)[Box](https://app.box.com/file/1885558866037). Blue hydrogen is similarly fossil-derived but with carbon capture and storage applied to reduce net CO₂ emissions. “Blue” is considered a lower-carbon interim solution, though its life-cycle emissions depend on capture efficiency and methane leakage. Brown/black hydrogen typically refer to hydrogen from coal (brown for lignite, black for bituminous) without CCS, which has the highest CO₂ emissions. Pink (or purple) hydrogen denotes hydrogen produced by electrolysis powered by nuclear energy (zero carbon electricity that is not renewable). There are also terms like “turquoise” hydrogen for hydrogen from methane pyrolysis (splitting natural gas into H₂ and solid carbon) and “white” hydrogen for the rare case of naturally occurring geologic hydrogen @incer-valverdeColorsHydrogenDefinitions2023 . While these colorful labels aid discussion, in practice hydrogen is further judged by purity and usage standards. The ISO 14687 standard specifies two grades of hydrogen fuel for PEM fuel cell road vehicles: _Type I Grade D_ (gaseous) and _Type II Grade D_ (liquid) hydrogen @beureyReviewSurveyMethods2021 . Type I Grade D gaseous hydrogen, used for compressed H₂ tanks in cars and buses, must have a minimum hydrogen content of 99.97% (fuel index) with total non-H₂ impurities ≤300 µmol/mol . This corresponds to SAE J2719 and ISO requirements that limit key contaminants (H₂O, O₂, N₂, CO, CO₂, CH₄, sulfur compounds, etc.) to parts-per-million or lower levels to avoid poisoning the fuel cell. Type II Grade D liquid hydrogen has a similarly stringent purity but for cryogenic liquid fuel systems @hookhamImpactHydrogenLiquefaction2022. Notably, such high purities are most readily achieved by electrolytic hydrogen (which is produced at high purity by default). The emphasis on standards like ISO 14687 ensures that as hydrogen use expands – especially in vehicles – **interoperability and safety** are maintained.




### PEM electrolyser design

Working principle.
•	trade offs and constraints





![[PEM design structure.png]]



MEA design









![[Alternate materials for PEM.png]]



Cell Structure and MEA Design



![[MEA configuration.png]]



Membrane


![[flow field design.png]]




## Technoeconomic Analysis



![[badjet cost reduction.png]]






Renewable Energy Systems




-----
### More results


Design effects

![[image-73.png]]

Figure X: a) Contour of LCOH to Temperature and current density, b) Contour of LCOH to Membrane thickness and current density. 

Figure X: a)
Figure X presents the levelized cost of hydrogen (LCOH) as a function of two key PEM electrolyzer operating parameters: cell temperature (40–100 °C) and current density (0.5–5 A /m²). The contour lines span an LCOH range of roughly $6.0–$8.4 per kg H₂, illustrating how thermal management and electrochemical design together shape hydrogen economics.
Across the design space (current density from 0.1 to 5 A/ cm², temperature from 40 °C to 100 °C), LCOH varies from roughly $6.0/kg (low density & high temperature) up to $8.4/kg (high density & low temperature). 
Higher temperature lowers both activation overpotentials and membrane resistance, cutting the specific energy consumption (SEC) by several kWh/kg.
At fixed temperature(e.g., 60 °C), increasing current density from 1 A /cm² to 3 A /cm² raises LCOH by ≈$0.8 /kg. Higher current density drives larger kinetic and Ohmic overpotentials, increasing SEC even as the required cell‑stack area (and thus capex) shrinks.
Optimal region lies around 1.5–2.5 A/ cm² at 60–80 °C, where LCOH is minimized (~$6.5–$7.0/kg) without excessively inflating either CAPEX (via oversized stacks) or OPEX (via high overpotentials).

Figure X: b)

Figure X depicts the influence of membrane thickness (50–550 µm) and operating current density (0.5–5 A/ cm²) on the levelized cost of hydrogen (LCOH) for a proton-exchange-membrane (PEM) electrolyzer.  The lowest cost envelope ($6.0–$7.0 /kg) lies at thin membranes (≤100 µm) combined with moderate current density (1–2 A /cm⁻²). 
For a 100 µm membrane, moving from 0.5 to 5 A /cm⁻² increases LCOH from ~$6.4 to ~$8.8 /kg. The rise reflects higher kinetic, ohmic and mass-transport overpotentials, which outweigh the CAPEX benefit of reduced stack area. The lowest LCOH region ($6.2–6.8 /kg) lies at membrane thicknesses ≤ 125 µm and current densities of 1–2 A /cm². Here, ohmic losses remain modest while capital dilution is tolerable. Thinner membranes below 75 µm yield < $0.2 /kg savings yet introduce durability and gas-crossover risks. Commercially available composite PFSA or PFSA-PFPE membranes in the 50–100 µm range minimise ohmic voltage while maintaining mechanical integrity, enabling LCOH reductions of up to $3 /kg relative to > 200 µm stacks

Energy system
![[image-80.png]]
CF

Figure X presents the levelized cost of hydrogen (LCOH) as a function of two operational parameters: the electricity price (from $0.01 to $0.15 per kWh) and the electrolyzer operating power expressed as a percentage of its rated power (5 %–100 %)  
Here, “operating power” is defined as the ratio of actual electrical input to the electrolyzer versus its nameplate power rating. Thus, a proxy for utilization or capacity factor under dynamic dispatch.   
At very low operating power (≤ 10 %), LCOH rises precipitously, exceeding $40 /kg even at the lowest electricity prices. This behavior reflects the dominance of capital‐recovery costs when the same electrolyzer stack is scarcely utilized: with only 876–1,752 hours of full‐power equivalent operation per year. Between 20 % and 50 % operating power, LCOH falls sharply as utilization improves from roughly $18 /kg to $8 /kg (Δ$10/kg). However, above ≈ 50 % load, the contour lines flatten: pushing from 50 % to 100 % only yields another $3–4/kg reduction. This inflection marks the point where further increases in utilization deliver progressively smaller amortization benefits, and where operating‐cost (electricity) begins to dominate.  
The results imply that Intermittent renewables alone operating power ≲ 30 % will risk hydrogen costs > $12/kg unless subsidized or unless coupled with storage or demand‐management to boost effective load. A Hybrid power integration that ensures ≥ 50 % operating power is essential to bring LCOH into the competitive $6–8/kg band, especially when paired with electricity prices below $0.08/kWh. Therefore, priority should be given to securing cost‐effective, high‐availability power through PPAs, co‐located renewables with storage, or grid‐firm contracts



LCOE
Figure X. LCOE and the corresponding LCOH impact for hydrogen production for energy configuration scenarios. 
To round off our scenario analysis, we examined four distinct electricity supply options: PV-only, wind-only, a PV–wind hybrid, and a hybrid coupled with battery storage. For PEM hydrogen production, the choice of renewable feedstock is often framed around capacity factor and marginal electricity price. The basis represents a uniform 20 MW installed capacity for PV and wind services (10 + 10 MW for the hybrid), with capacity factors of 25 % (PV), 34 % (wind), and a hybrid configuration and storage cycles at one 20 MWh discharge per day.
The PV‑only scenario exhibits the lowest energy production cost per kWh ($0.11/ kWh) in fixed charges and negligible marginal cost, yielding an LCOE of ($0.12/ kWh) and an LCOH of ($9 /kg). Its modest 25 % utilization is more than offset by the relatively lower per‑kW price of solar panels and minimal BoP complexity. Wind-only delivers more consistent output (CF ≈ 34 %) but incurs higher levelized fixed charges ($0.16 /kWh) and a larger marginal cost ($0.03/ kWh) reflecting turbine O&M. The turbine CAPEX outweighs its better capacity factor to produce the highest LCOH at $12.2 /kg. 
These altogether show that equipment costs are the primary drivers of LCOE in all off-grid scenarios. Greater RE availability does not automatically translate into cheaper hydrogen. Gains in capacity factor from hybridization can offset some of the premium associated with renewable systems, but cannot completely replace access to a low-cost grid or a good PPA tariff.  
A standalone PV system offers the lowest barrier to entry, while hybrid configurations trade modest cost increases for improved reliability. Incorporating storage further protects hydrogen production from renewable intermittency, but incurs a capital premium that must be justified by downstream value, such as time-sensitive refueling or grid services revenue. Ultimately, the choice of energy configuration should align with local resource profiles, off-taker requirements, and financing constraints. RE system cost savings will translate to lower LCOH only if they maintain a high utilization rate of the electrolyzer.




