

To dos


**TEA**
- [>] Cost model connect @due(2025-04-23) @started(2025-04-22)
	- [ ] energy sys Model Cost component + analysis table
- [ ] summarize TEA capital cost in 100% @due(2025-04-22)

- [ ] Performance capacity factor @due(2025-04-22)
- [ ] distributed vrs central sys @due(2025-04-21)
- [ ] Uncertainty in energy price
- [ ] Energy system uncertainty factor
- [ ] Cost model to MJ: python @due(2025-04-21)


**Algo Optimization**
- [ ] Grok model test
- [ ] Design fixed
- [ ] PEM model to streamlit
- [ ] Optimization of MEA -
- [ ] Model documentations
- [ ] Model visualization

**Defense**
- [ ] Send email to comittee
- [ ] Outlook visualization
- [ ] Diagrams for demos
- [ ] Appyfy research



1. Cost model
	PEM curve fitting model

2. Sensitivity analysis
	for NPV
	for LCOE

	2.1 sensitivity focus on
		PEM design module
		economic parameter
		energy system

	energy system on LCOE
		wind
		PV

3. Montecarlo uncertainty analysis
capital cost
Electricity pricing
LCOE
	PV | wind  Energy parameters;
		


4. Algo optimization
	- Pem design
		- MEA design
	- Energy system
		- location
		- load mix


Scenarios 
energy mix
	Full grid
		pilot location
	PV/Wind pair
	

---

**Task 1.1 {completed}:**  
Develop a detailed electrochemical and mathematical model of the PEM electrolyzer stack, including membrane hydration, overpotential losses, Faradaic efficiency, and gas crossover effects.

PEM design and Electrochemical

Cell Design Parameters: Inputs and Outputs

| Parameter                             | Value                                  |
| ------------------------------------- | -------------------------------------- |
| Faraday constant, F (C/mol)           | 96485                                  |
| Gas constant, R (J/mol K)             | 8.314                                  |
| The cell operating temperature, T (K) | 333.15                                 |
| The cell operating pressure, P (bar)  | 1 (anode), 30 (cathode)                |
| The maximum current density, (A/cm²)  | 2                                      |
| Exchange current density, (A/cm²)     | 2.618 x 10⁻⁶ (anode), 1.0e-1 (cathode) |
| Limiting current density (A/cm²)      | 6                                      |
| The electrode thickness, (microns)    | 200                                    |
| The electrode porosity                | 0.3                                    |
| The membrane thickness, (microns)     | 178                                    |
| Titanium resistivity, (ohm cm)        | 5.0 x 10⁻³                             |
| Carbon paper resistivity, (ohm cm)    | 8.00x10⁻²                              |
| Transfer coefficient                  | 2.0 (anode), 0.5 (cathode)             |
| Water dynamic viscosity (N s/cm²)     | 3.55x10⁻⁸                              |
| Water density, (g/cm³)                | 1                                      |
| Active area, (cm²)                    | 877                                    |
| No electrons                          | 2                                      |
| Number of cells                       | 877                                    |
| Cell voltage, V                       | 1.79                                   |
| Voltage efficiency                    | 0.69                                   |
| Cell Power rating, kW/cell            | 3.14                                   |
| Total power rating, kW                | 19,034                                 |
| Specific Energy consumption           | 49                                     |
| Membrane type                         | PFSA, Nafion 117                       |
| Anode catalyst loading, mg/cm²        | 1.54                                   |
| Cathode catalyst loading mg/cm²       | 0.4                                    |

(Bessarabov & Miller, 2018)

Results
- [ ] sensitity of parameters to system output metric( efficiency)
- [ ] validate result by comparing with experimental results


![[image-33.png|388x211]]


![[image-34.png|391x267]]

The plot above shows:

- **Reversible voltage (V_rev)** as a baseline (horizontal line).
- **V_rev + η_act** (activation overpotential) rising rapidly at low current.
- **V_rev + η_act + η_ohm** (adding ohmic losses) with a linear trend.
- **Full polarization curve (no bubbles)** in solid magenta.
- **Full polarization curve (with bubbles)** in dashed blue, illustrating the extra voltage penalty at higher currents due to bubble coverage.
    
This clearly highlights how bubble formation exacerbates both ohmic and concentration losses, steepening the polarization curve. 




This means that the model being evaluated has the following characteristics relative to the Debe method:

- **RMSE (Root Mean Squared Error) of 32 mV:** This is the square root of the average of the squared differences between the predicted values and the actual values from the Debe method, in this case measured in millivolts.
    - **Interpretation:** On average, the model's predictions differ from the Debe method's measurements by approximately 32 mV.
    - **Lower RMSE implies better accuracy**, so 32 mV represents the average error magnitude of the predictions.
- **MAE (Mean Absolute Error) of 28 mV:** This is the average of the absolute differences between the predicted values and the actual values from the Debe method, also in millivolts.
    - **Interpretation:** The average absolute difference between the predicted and actual values is 28 mV.
    - **MAE is less sensitive to outliers than RMSE** because it doesn't square the errors. This means that the impact of large errors is not as exaggerated as it would be with RMSE.
- **R² (Coefficient of Determination) of 0.897:** This is a statistical measure that indicates how well the independent variable(s) in the model explain the variation in the dependent variable compared to the Debe method.
    - **Interpretation:** An R² of 0.897 means that **89.7% of the variability in the dependent variable (measured by the Debe method) can be explained by the model**.
    - **A higher R² value indicates a better fit of the model to the data**. In this context, 0.897 suggests a reasonably strong relationship between the model's predictions and the Debe method's measurements. 

**In summary:**

The model produces predictions that, on average, are around 28-32 mV away from the values obtained by the Debe method. [Arize AI says](https://arize.com/blog-course/r-squared-understanding-the-coefficient-of-determination/)R-squared of 0.897 indicates that the model explains a significant portion of the variability seen in the Debe method's results. The specific "goodness" of these values (32 mV, 28 mV, 0.897) depends on the context of the electrical measurements and what is considered an acceptable level of error in that particular field or application.


### Sensitivity of design parameters



![[image-86.png]]








![[image-81.png]]

**Results and Discussion**

Figure X presents the levelized cost of hydrogen (LCOH) as a function of two key PEM electrolyzer operating parameters: cell temperature (40–100 °C) and current density (0.5–5 A /m²). The contour lines span an LCOH range of roughly $6.0–$8.4 per kg H₂, illustrating how thermal management and electrochemical design together shape hydrogen economics.

---

### 1. Quantitative Findings

1. **LCOH Range:**
    - Across the design space (current density from 0.1 to 5 kA m⁻², temperature from 40 °C to 100 °C), LCOH varies from roughly **$6.0/kg** (low density & high temperature) up to **$8.4/kg** (high density & low temperature).
        
2. **Temperature Effect:**
    - **At fixed current density (e.g. 2 kA m⁻²)**, raising temperature from 40 °C → 100 °C reduces LCOH by ≈$0.6 /kg.
    - **Mechanism:** Higher temperature lowers both activation overpotentials (faster reaction kinetics) and membrane resistance, cutting the specific energy consumption (SEC) by several kWh/kg.
        
3. **Current Density Effect:**
    - **At fixed temperature (e.g. 60 °C)**, increasing current density from 1 kA m⁻² → 3 kA m⁻² raises LCOH by ≈$0.8 /kg.
    - **Mechanism:** Higher current density drives larger kinetic and Ohmic overpotentials, increasing SEC even as the required cell‑stack area (and thus capex) shrinks.
        
4. **Interaction:**
    
    - The steepest contours appear in the upper‐left (high density, low temperature), indicating a compounding penalty when both parameters move in the “inefficient” direction.
        
    - Contour lines flatten toward the lower‐right (low density, high temperature), where additional efficiency gains yield diminishing LCOH improvements.
### 1. Temperature Dependence

- **Monotonic decline in LCOH with temperature**  
    Raising cell temperature from 40 °C to 100 °C reduces LCOH by ~$0.6/kg at fixed current density. This reduction arises because elevated temperatures lower the thermodynamic voltage and accelerate reaction kinetics—both of which decrease the electrical energy required per kilogram of H₂.
    
- **Diminishing marginal gains**  
    The steepest decline occurs between 40 °C and 60 °C (~$0.3/kg per 20 °C), whereas further heating to 100 °C yields smaller savings (~$0.3/kg over 40 °C). Practically, this suggests tempered returns on stack materials and system complexity required to operate above ~80 °C.
    

---

### 2. Current Density Effects

- **LCOH rises with current density**  
    Increasing current density from 0.5 kA m⁻² to 5 kA m⁻² raises LCOH by ~$1.0–$1.4/kg, depending on temperature. At higher loadings, additional overpotentials (activation, ohmic, and concentration losses) drive up the cell voltage—and thus the energy consumption—to produce each kilogram of hydrogen.
    
- **Greater sensitivity at low temperature**  
    The incremental cost penalty for boosting current density is steeper at 40 °C (~~$0.28/kg per kA m⁻²) than at 100 °C (~~$0.19/kg per kA m⁻²). Warmer operation therefore also mitigates the efficiency loss incurred by high‐rate electrolysis.
    

---

### 3. Design Trade-Off: Throughput vs. Efficiency

- **High‐throughput operation (≥3 kA m⁻²)** reduces required stack area—and thus CAPEX—for a given hydrogen production rate, but imposes an energy penalty of up to $1.4/kg.
    
- **Low‐density operation (≤1 kA m⁻²)** maximizes energy efficiency (LCOH ≈$6.3/kg at 80 °C), but increases stack size—and CAPEX—by a factor of 3–5.
    
- **Optimal region** lies in the “sweet spot” around **1.5–2.5 kA m⁻² at 70–80 °C**, where LCOH is minimized (~$6.5–$7.0/kg) without excessively inflating either CAPEX (via oversized stacks) or OPEX (via high overpotentials).
    

---

### 4. Implications for PEM Electrolyzer Design

1. **Thermal management:** Operating at 60–80 °C delivers most of the efficiency advantage with moderate system complexity—avoiding the steep material and sealing challenges of >100 °C stacks.
    
2. **Current‐density targeting:** Designing electrodes and flow fields to sustain 1.5–2.5 kA m⁻² strikes the best compromise between capital investment and energy consumption. Exceeding 3 kA m⁻² generally requires advanced catalysts and thicker bipolar plates that may offset any CAPEX savings with higher cell costs.
    
3. **System integration:** Coupling a PEM electrolyzer with waste heat recovery or low‐grade process heat can further push effective operating temperature into the optimal range without additional heating energy.
    

4. **Optimal Operating Window:**
    
    - **Temperature:** Operate as close to **80–90 °C** as the membrane and catalyst materials allow. This range captures most of the kinetic benefit without incurring excessive materials degradation or cooling losses.
        
    - **Current Density:** Target a **moderate density** of **1–2 kA m⁻²**. Below 1 kA m⁻², capex per kg H₂ becomes onerous; above 2 kA m⁻², rising energy losses dominate.
        
5. **Capex vs. Opex Trade‑off:**
    
    - Lowering current density reduces OPEX (due to improved energy efficiency) but increases CAPEX (larger cell area). Conversely, pushing density higher saves on stack hardware but inflates the electricity bill per kilogram of H₂.
        
    - The contour plateau at low density/high temperature identifies the **“sweet spot”** where marginal capex increases are balanced by substantial OPEX savings.
        
6. **Material and Durability Considerations:**
    
    - Operating at ≥90 °C demands high‑temperature membranes (e.g. reinforced PFSA or PBI‐based) and corrosion‑resistant components, which can elevate initial stack cost and risk accelerated degradation.
        
    - Similarly, current densities >2 kA m⁻² stress catalysts and gas diffusion layers, potentially shortening stack lifetime and raising replacement costs that must be amortized in the LCOH.

---

### 5. Conclusion

> **“To minimize LCOH, PEM electrolyzer systems should be designed for moderate current densities (≈1.5–2.5 kA m⁻²) and elevated temperatures (60–80 °C).** Beyond these bounds, the marginal energy savings or CAPEX reductions are outweighed by engineering complexity, material costs, and diminishing returns on both thermal and electrochemical performance.”

Such a targeted design envelope ensures that both capital and operating expenditures are jointly optimized, delivering hydrogen at the lowest achievable cost.

“For a balanced cost‐efficient PEM electrolyzer, specify cells capable of stable operation at 80–85 °C and design the system for an average current density of ~1.5 kA m⁻². This choice minimizes energy losses (keeping LCOH near $6.4–6.6 /kg) while avoiding the steep capital and durability penalties associated with ultra‑low densities or ultra‑high temperatures.”


for pressentation
1. **Target Moderate Temperatures (60–80 °C) for Maximum Efficiency Gains**  
    Operating the PEM stack in the 60–80 °C range captures over 80 % of the potential energy‑efficiency benefit (−$0.5–$0.6/kg LCOH) while avoiding the steep material and sealing challenges—and diminishing returns—associated with > 80 °C operation.
2. **Optimize Current Density at 1.5–2.5 kA/m² to Balance CAPEX and OPEX**  
    Designing electrodes and flow fields for 1.5–2.5 kA/m² minimizes combined capital and energy costs—delivering an LCOH near $6.5–$7.0/kg—whereas pushing above 3 kA/m² incurs an extra $1+/kg penalty in overpotentials that outweighs any stack‑size savings.
3. **Deprioritize Extreme Operating Conditions in Favor of System Integration**  
    Improvements beyond 100 °C or > 3 kA/m² yield < $0.3/kg additional savings, making it more effective to focus R&D on balance‑of‑plant heat recovery, thermal management, and securing low‑cost electricity than on incremental gains at the electrochemical extremes.


![[image-82.png]]

**Results and Discussion**

Figure X depicts the influence of membrane thickness (50–550 µm) and operating current density (0.5–5 A/ cm⁻²) on the levelized cost of hydrogen (LCOH) for a proton-exchange-membrane (PEM) electrolyzer.

**Results and Discussion**

Figure X depicts the influence of membrane thickness (50–550 µm) and operating current density (0.5–5 kA m⁻²) on the levelised cost of hydrogen (LCOH) for a proton-exchange-membrane (PEM) electrolyser. Two intertwined physical mechanisms explain the observed gradients: (i) _ohmic resistance_—which scales linearly with membrane thickness and current density—and (ii) _stack-area dilution_—where lower current densities increase the required active area and thus capital cost.

---

### 1. Membrane Thickness: Ohmic Loss Penalty Dominates

- **Monotonic LCOH increase with thickness.** At a fixed current density of 2 kA m⁻², thickening the membrane from 50 µm to 500 µm raises LCOH from ≈ $7.0 kg⁻¹ to > $10 kg⁻¹. The main driver is the ohmic voltage loss (ηohm=i⋅Rmη_\mathrm{ohm}= i·R_m), where Rm∝R_m\propto thickness.
    
- **Accelerating penalty at high thickness.** Contours steepen beyond ~300 µm, indicating that each additional 50 µm costs progressively more in $ kg⁻¹ H₂ because the ohmic term approaches parity with the thermodynamic voltage.
    

### 2. Current Density: Throughput–Efficiency Trade-Off

- **Rising LCOH with current density.** For a 100 µm membrane, moving from 0.5→5 kA m⁻² increases LCOH from ~$6.4 to ~$8.8 kg⁻¹. The rise reflects higher kinetic, ohmic and mass-transport overpotentials, which outweigh the CAPEX benefit of reduced stack area.
    
- **Steeper slope for thick membranes.** At 500 µm, the same current-density sweep drives LCOH from ~$7.2 to > $11 kg⁻¹, underscoring that ohmic resistance amplifies the energy penalty of aggressive loading.
    

### 3. Optimal Operating Envelope

- **Economic sweet spot.** The lowest LCOH region (~$6.2–6.8 kg⁻¹) lies at membrane thicknesses ≤ 125 µm and current densities of 1–2 kA m⁻². Here, ohmic losses remain modest while capital dilution is tolerable.
    
- **Diminishing returns.** Thinning the membrane below ~75 µm yields < $0.2 kg⁻¹ savings yet introduces durability and gas-crossover risks. Likewise, current densities below 1 kA m⁻² reduce OPEX only marginally but inflate stack-area CAPEX.
- -
- **Optimal design region**  
The lowest cost envelope ($6.0–$7.0 /kg) lies at **thin membranes (≤100 µm)** combined with **moderate current density (1–2 kA m⁻²)**. In this regime, ionic resistance is kept low and overpotentials remain modest, yielding minimal energy waste without requiring excessively large membrane area.

---

### Implications for PEM Electrolyser Design

1. **Adopt Thin, Reinforced Membranes (≤ 125 µm).**  
    Commercially available composite PFSA or PFSA-PFPE membranes in the 50–100 µm range minimise ohmic voltage while maintaining mechanical integrity, enabling LCOH reductions of up to $3 kg⁻¹ relative to legacy 200 µm stacks.
    
2. **Limit Nominal Current Density to ~2 kA m⁻².**  
    Operating above ~2.5 kA m⁻² on any membrane thickness sharply inflates LCOH (> $8 kg⁻¹) unless ultra-low electricity prices are available; vendors should therefore optimise catalyst layers and cooling to perform efficiently at moderate loadings.
    
3. **Prioritise Ohmic-Loss Mitigation Over Extreme Upscaling.**  
    Engineering resources spent on larger cell footprints or exotic high-load hardware provide less cost leverage than systematic resistance reduction (e.g., thinner membranes, highly conductive porous transport layers, and shortened current paths).
    

---

**Conclusion**

> **“The contour analysis confirms that ohmic resistance—set jointly by membrane thickness and current density—is a decisive driver of hydrogen cost. To reach sub-$7 kg⁻¹ LCOH, PEM systems should pair thin (< 125 µm) membranes with moderate current densities (~2 kA m⁻²); thicker membranes or ultra-high loadings impose energy penalties that dwarf any capital-area savings.”**

These insights guide material selection, stack architecture, and operating protocols in the next generation of cost-competitive PEM electrolysers.

Assertiveness
--
### 1. Membrane Thickness Drives Ohmic Losses

- **Thicker membranes incur higher LCOH across all current densities**  
    At a moderate current density of 2.5 kA m⁻², increasing membrane thickness from 20 µm to 500 µm raises LCOH from ~$7.2 to ~$9.2 /kg—a $2.0 /kg penalty.
    
- **Nonlinear escalation at high thickness**  
    The incremental cost per 100 µm jump grows with thickness: moving from 20→120 µm adds ~$0.4/kg, whereas 400→500 µm adds over $0.6/kg. This reflects the quadratic relationship of ohmic overpotential to membrane thickness.
    

---

### 2. Current Density Amplifies Thickness Effects

- **Steeper LCOH rise at high current density**  
    At 5 kA m⁻², LCOH increases from ~$8.0 to $11.8 /kg as thickness goes 20→500 µm (Δ$3.8/kg), whereas at 0.5 kA m⁻² the same thickness change only raises LCOH from ~$6.1 to $7.0 /kg (Δ$0.9/kg).
    
- **Coupled sensitivity**  
    The conjoint effect means that high‐throughput operation (to reduce CAPEX) must be paired with ultrathin membranes (<100 µm) to avoid prohibitive energy penalties.
    

---

### 3. Optimal Design Envelope

- **Sweet spot region:**
    - **Current density:** 1.5–3.0 kA m⁻²
    - **Membrane thickness:** 20–80 µm  
        In this envelope, LCOH remains below $7.5/kg, balancing moderate stack area (CAPEX) against manageable ohmic losses (OPEX).


![[image-73.png]]






---


**Task 1.2 {ongoing}:**  
Formulate and solve a multi-objective optimization problem minimizing both CAPEX and specific energy consumption, while maximizing efficiency and membrane durability, under realistic operating constraints.

- [ ] diagram of optimization
- [ ] solution from optimization




**Objective**: To pinpoint high-impact parameters in green hydrogen production cost and assess design configurations under varied operational scales.

**Task 2.1 {Completed}:**  
Design a modular technoeconomic assessment (TEA) model integrating the physical PEM model into a system-level hydrogen production cost framework using  LCOH, and NPV as primary metrics

Basis:
Electricity: Industrial rate.


LCOH at differenct capacitiyes and cosposition.



|                                   | Distributed, 1500 kg/day | Baseline, 10,000 kg/day | Centralised, 50,000 kg/day |
| --------------------------------- | ------------------------ | ----------------------- | -------------------------- |
| Fixed Opex                        | 2.328                    | 1.536                   | 2.061                      |
| Feedstock (Electricity and Water) | 3.684                    | 3.684                   | 3.684                      |
| Utility cost                      | 0.387                    | 0.387                   | 0.387                      |
| Other variable cost               | 0.008                    | 0.008                   | 0.008                      |
| FCI                               | 1.887                    | 0.930                   | 0.661                      |
| Working capital                   | 0.341                    | 0.168                   | 0.120                      |
|                                   | 8.635                    | 4.714                   | 6.921 $/kW                 |


![[image-35.png|395x259]]


![[image-36.png|426x239]]

|     | Distributed    | Baseline        | Centralised      |
| --- | -------------- | --------------- | ---------------- |
| IRR | 0.136          | 0.320           | 0.380            |
| NPV | $ 6,120,530.58 | $ 84,330,199.17 | $ 409,929,882.43 |

![[image-71.png]]




today 2025-07-09T00:00:00-04:00


|                  | distributed   | baseline       | central         |
| :--------------- | :------------ | :------------- | :-------------- |
| **Fixed Opex**   | 2.2066        | 1.452          | 1.9515          |
| **Feedstock**    | 3.8184        | 3.814          | 3.8184          |
| **Utility cost** | 0.736         | 0.735          | 0.736           |
| **Other variab** | 0.0078        | 0.008          | 0.0078          |
| **FCI**          | 1.786         | 0.878          | 0.626           |
| **Working cca**  | $ 0.32        | 0.159          | 0.1132          |
| **LCOH**         | **8.877**     | **7.046**      | **7.253**       |
|                  |               |                |                 |
| **IRR**          | 13%           | 32%            | 37%             |
| **NPV**          | $5,506,385.00 | $77,859,024.39 | $377,340,292.00 |


> [!NOTE]
> Now one can argue that , power can be purchased at a cheaper rate for larger capacity systems and lead to a better projection for centralized systems. 

limitation:

Colors of hydrogen and prices


# Economies of scale and baseline capacity vrs


![[image-74.png|657x389]]


![[image-76.png|527x310]]





|                | distributed    | baseline        | central          |
| -------------- | -------------- | --------------- | ---------------- |
| Fixed Opex     | 2.2066         | 1.452           | 1.9515           |
| Feedstock      | 3.8184         | 3.814           | 3.8184           |
| Utility cost   | 0.736          | 0.735           | 0.736            |
| Other variable | 0.0078         | 0.008           | 0.0078           |
| FCI            | 1.786          | 0.878           | 0.626            |
| Working ccap   | $ 0.32         | 0.159           | 0.1132           |
| **LCOH**       | **8.877**      | **7.046**       | **7.253**        |
|                |                |                 |                  |
| IRR            | 13%            | 32%             | 37%              |
| NPV            | $ 5,506,385.00 | $ 77,859,024.39 | $ 377,340,292.00 |


|             | distributed | baseline | central |
| ----------- | ----------- | -------- | ------- |
| percentages |             |          |         |
|             | 25%         | 21%      | 27%     |
|             | 43%         | 54%      | 53%     |
|             | 8%          | 10%      | 10%     |
|             | 0%          | 0%       | 0%      |
|             | 20%         | 12%      | 9%      |
|             | 4%          | 2%       | 2%      |
|             | 1           | 1        | 1       |



# Sensitivity analysis

![[Pasted image 20250329010705.png|489x293]]



results fig 5.2.2
Tornado chart showing a univariate sensitivity of LCOH  to key parameters
![[image-77.png]]

![[image-78.png]]

|                                                 | low  | base | high |
| ----------------------------------------------- | ---- | ---- | ---- |
| Total Energy Feedstock Cost (0.03, 0.12) $/kWh  | 4.73 | 7.05 | 9.51 |
| Uninstalled capital cost (250, 1500)$/kW        | 5.31 | 7.05 | 8.22 |
| Total Fixed Operating Costs, (.4M, 5.9M) $/yr   | 6.84 | 7.05 | 7.44 |
| SEC, PEMel efficiency, (45, 55 kWh/kg H2)       | 6.67 | 7.05 | 7.89 |
| Total Utility Costs (0.9M, 3M) $/year           | 6.93 | 7.05 | 7.25 |
| Total Non Energy Feedstock (0.95M, 1.7M) $/year | 6.92 | 7.05 | 7.13 |
| By product O2 price, $/kg O2                    | -    | -    | -    |

Tornado chart showing a univariate sensitivity of NPV to key parameters



![[Tornardo chat showing sensitivity to NPV.png]]

![[image-79.png]]

|                                                  | low             | base           | high           |
| ------------------------------------------------ | --------------- | -------------- | -------------- |
| Total Energy Feedstock Cost (0.03, 0.12) $/kWh   | $124,954,376.67 | $77,641,604.35 | $27,296,837.89 |
| Uninstalled capital cost (250, 1500)$/kW         | $115,525,342.67 | $77,641,604.35 | $51,873,651.11 |
| PEC, PEMel efficiency, kWh/kg H2 (45-55 kW/kg)   | $85,529,536.60  | $77,641,604.35 | $34,265,341.82 |
| Tax rate, (16-36%)                               | $84,998,394.30  | $77,641,604.35 | $70,284,814.41 |
| Total Fixed Operating Costs, (.4M, 5.9M) $/yr    | $81,716,831.94  | $77,641,604.35 | $69,984,331.85 |
| Total Utility Costs (0.9M, 3M) $/year            | $79,922,300.23  | $77,641,604.35 | $73,450,908.56 |
| Total Non Energy Feedstock (0.95M, 1.7M) $/year  | $80,281,677.16  | $77,641,604.35 | $75,869,364.66 |
| By product O2 price, $/kg O2 (0 - 0.028 $/kg O2) | $77,641,604.35  | $77,641,604.35 | $82,025,083.52 |










Contour plots of interest
 electricity | design capacity | LCOE
 - [ ] centralized vrs distributed systems
![[image-37.png|448x312]]

**“This contour shows that while scale reduces your LCOH, power cost is the master variable.** Secure sub-$0.07/kWh electricity first—ideally through PPAs or on-site renewables—then size your plant to around 8–10 t/day to hit the $6–$8/kg ‘sweet spot.’ Beyond 12 t/day, focus on further lowering power cost or improving utilization (e.g., with storage) rather than mere scale.”

the questions it raises, and the high-level takeaways for a hydrogen project:
- **How sensitive is LCOH to energy price vs. plant size?**
- **What combinations of capacity & power cost achieve “target” LCOH thresholds (e.g. $4, $6, $8 per kg)?**
    
- **Where are the diminishing returns on adding capacity?**


**Scale drives down costs**: As you move right (↑ capacity, from 2 000 → 15 000 kg/day), LCOH falls—from upwards of $12–$15/kg at small scale to $4–$6/kg at the largest sizes—because fixed CAPEX is spread over more output.

- **“baseline”**: Your white dot at ~10 000 kg/day & $0.07/kWh sits at ≈$7.2/kg. This shows a commercially plausible mid-point: large enough to grab scale benefits, but still sensitive to power costs.

## 3. Answering Those Questions

| Question                   | Evidence from Plot                                                                                                                                                                                   | Assertion                                                                                                                                 |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Sensitivity**         | • At 10 000 kg/day, a ±$0.05/kWh swing in power cost (say $0.07→$0.12) changes LCOH by ~$2.5–3/kg.  <br>• At $0.07/kWh, doubling capacity from 5 000→10 000 kg/day only cuts LCOH by ~$1/kg.         | **Electricity price is the more powerful single lever**: LCOH moves more when power costs fluctuate than when capacity doubles.           |
| **2. Target thresholds**   | • **$8/kg** is reachable at 4 000 kg/day if power <$0.06/kWh, or at 10 000 kg/day if power <$0.10/kWh.  <br>• **$6/kg** requires either >12 000 kg/day & <$0.05/kWh, or >15 000 kg/day & ~$0.07/kWh. | Achieving “cheap” green hydrogen (<$6/kg) demands **both** very low power costs and very large scale.                                     |
| **3. Diminishing returns** | Contour lines flatten noticeably beyond ~12 000 kg/day: each extra 3 000 kg/day adds <$0.5/kg savings.                                                                                               | **Scale benefits plateau** around 12–15 t/day; past that, it’s cheaper to invest in lower‐cost power or higher CF.                        |
| **4. Lever priority**      | The vertical spacing between contours (energy axis) is tighter than horizontal spacing at mid-ranges.                                                                                                | **Locking in low‐cost energy** should be your first priority; expand capacity only once you’ve secured a cheap PPA or on-site renewables. |



## 1. The Big Picture: Scale vs. Energy Cost Trade-Off

- **Rightward (→) movement** = bigger plant.
    - Spreads your fixed capital across more kilograms of H₂, pulling your LCOH down.
    - But beyond ~10 000 kg/day the color bands flatten: each extra 1 000 kg/day only trims the LCOH by a few cents.
        
- **Upward (↑) movement** = more expensive electricity.
    - This steeply drives your LCOH higher—in this chart, going from $0.02→$0.12/kWh at a fixed 10 000 kg/day jumps LCOH from ~$4→$10/kg.

 “Baseline” sits at 10 000 kg/day & $0.07/kWh—and the contour shading there (~dark teal) corresponds to an LCOH of roughly **$7/kg**.

---

## 2. Core Questions Raised

1. **How sensitive is my LCOH to electricity price vs. plant size?**
2. **What combinations of capacity & power cost can hit competitive targets (e.g. $4/kg, $6/kg)?**
3. **Where do I hit diminishing returns on scale?**
4. **Is my “Baseline” healthy, or do I need to push harder on scale or on energy price?**
## 3. Answering Those Questions

| Question                                 | Evidence from Plot                                                                                                                                                                                        | Assertion                                                                                                                              |
| :--------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------- |
| **Electricity vs. capacity sensitivity** | • At **10 000 kg/day**, raising cost from $0.05→$0.10/kWh increases LCOH by ~$3/kg. • At **$0.07/kWh**, boosting capacity from 5 000→15 000 kg/day only cuts LCOH by ~$1.5/kg.                            | **Electricity price is your single most powerful lever**—even big jumps in plant size can’t compensate for paying an extra $0.05/kWh.  |
| **Hitting LCOH targets**                 | • **$6/kg** requires either: – ≥12 000 kg/day & ≤$0.06/kWh, or – ≥8 000 kg/day & ≤$0.04/kWh. • **$4/kg** is only reachable with very large scale (>15 000 kg/day) **and** ultra-cheap power (<$0.03/kWh). | **Competitive green H₂ (<$4–6/kg)** demands either rock-bottom electricity costs or massive scale—ideally both.                        |
| **Diminishing returns on scale**         | • Contours beyond ~12 000 kg/day crowd closely: +1 000 kg/day yields <$0.10/kg savings then.                                                                                                              | **Once you’re above ~10 000 kg/day, focus on energy cost**—you’ll get more bang for your buck there than on incremental scale.         |
| **Baseline health check**                | • At (10 000 kg/day, $0.07/kWh) → **$7/kg** LCOH. • Dropping power cost to $0.05 → **$5.5/kg** (–$1.5/kg). • Scaling to 15 000 at $0.07 → **$6.5/kg** (–$0.5/kg).                                         | **Baseline should prioritize securing cheaper electricity** (e.g. PPAs, co-located renewables) before chasing bigger plant footprints. |

## 4. Alternative Perspectives

- **Site-specific renewables:** If you can build behind-the-meter solar/wind at $0.03/kWh, even a 5 000 kg/day plant can hit <$5/kg.
- **Risk & financing:** A huge centralized plant carries financing risk if power prices spike. A slightly smaller plant with guaranteed low-cost power can be less risky.
- **Technology readiness:** As electrolyzer stack costs fall, the sweet spot shifts—scale becomes easier, but energy cost remains king.
    

---

## 5. Implications for NPV & Project Design

- **Every $0.50/kg LCOH drop** at 10 000 kg/day is ~$1.8 million extra annual margin.
- **NPV maximization** hinges on locking in low-cost power first, then dialing in scale up to the ~10 000–12 000 kg/day range.
- **Transport & logistics**: Don’t forget that centralized scale often means trucking or piping hydrogen—adds $0.5–$2/kg.
    

---

## 6. Bottom-Line Guidance

> **“Map your project on this contour: if you’re near the Baseline, pursue cheaper electricity contracts (e.g. PPAs, dedicated renewables). Only after you secure sub-$0.06/kWh power should you invest in growing beyond 10 000 kg/day—because that’s where you really squeeze the last drops of CAPEX savings.”**

The alignment of **scale** and **energy cost** will drive both your **LCOH targets** and the **financial returns** you can deliver to investors.


Figure # illustrates the sensitivity of the levelized cost of hydrogen (LCOH) to two principal techno‐economic drivers: the cost of electrical energy and the electrolyzer's design capacity. Across the parameter space examined design capacities ranging from 2 000 to 15 000 kg H₂/day and electricity prices spanning $0.01 to $0.21 per kWh, the contour lines reveal two fundamental insights. First, electrical energy cost emerges as the most powerful lever for driving down LCOH. Holding capacity constant at 10,000 kg/day (the baseline), a reduction in electricity price from $0.12 to $0.02 per kWh decreases LCOH from approximately $10/kg to below $4/kg. Conversely, increasing capacity from 5,000 to 15,000 kg/day at a fixed electricity price of $0.07 per kWh lowers LCOH by only about $1.5/kg. This asymmetric sensitivity underscores that, for green hydrogen systems, securing low‐cost power through power purchase agreements, grid‐side renewables, or behind‐the‐meter generation is a more effective strategy than indefinite plant upscaling.

Second, while economies of scale do reduce unit costs, they exhibit pronounced diminishing returns beyond roughly 10,000 kg/day. In the lower‐left quadrant of Figure 1, small‐scale units (≤ 4 000 kg/day) experience steep LCOH declines of $2–3/kg for each additional 2 000 kg/day of capacity. However, beyond 10 000 kg/day, the contours flatten, indicating that a further 2 000 kg/day expansion delivers only marginal (< $0.2/kg) cost savings. This plateau effect arises because fixed capital expenditures, although spread over greater throughput, become a progressively smaller fraction of total cost as operational expenditures (dominated by electricity) prevail.

These results carry clear implications for project developers and policymakers. Achieving LCOH targets in the $4–6/kg range requires either electricity costs below $0.05/kWh, capacity factors in excess of 90 percent on firm power, or a combination of moderate scale (8 000–12 000 kg/day) with sub‐$0.06/kWh energy. Attempting to drive down LCOH solely via plant size would necessitate impractically large electrolyzer installations both technically and financially without concomitant access to low‐cost, low‐carbon power. In contrast, integrating cost‐effective renewable electricity options (e.g., utility‐scale wind, solar plus storage) or securing long‐term low‐price PPAs will yield far greater reductions in hydrogen unit cost.

In summary, while both design capacity and energy price fundamentally shape LCOH, the contour analysis definitively indicates that initiatives to lower electricity cost should take precedence. Once a favorable power contract is in place, developers can then optimize plant size up to the point of diminishing returns to achieve the most economically and operationally efficient hydrogen production system.

o4-mini-high



---


### SEC( efficiency) to the cost of energy.
Improving design or lowing cost of energy

![[image-38.png|468x281]]

## 1. The Story in the Plot

- **Both axes “multiply” into your cost**
    - **SEC (x-axis)** appears in _both_ your CAPEX term (because a more-efficient stack needs less installed kW per kg/h) and your OPEX term (directly via kWh/kg).
    - **Cost of Energy (y-axis)** only enters the OPEX term—but does so in proportion to SEC (kWh/kg × $/kWh).
        
- **Hyperbolic contours**
    - At **low SEC** (40 kWh/kg) and **low power cost** (≈$0.02/kWh), you can hit LCOH ≈$3/kg.
    - At **high SEC** (70 kWh/kg) and **high power cost** (≈$0.20/kWh), you’re up near $20/kg.
        
- **Baseline check**
    - Your white dot at **SEC = 50, cost = $0.08** lands in the ~$9/kg band—matching what we’ve been using as our reference.


## 2. Key Questions Raised

1. **Per-unit sensitivity:** Which is the stronger lever—shaving 1 kWh/kg off SEC or knocking $0.01/kWh off power cost?
2. **Target envelopes:** What SEC–power-cost combos let me hit LCOH = $6/kg or $8/kg?
3. **Diminishing returns:** At what point does further efficiency improvement or cheaper power give me only tiny LCOH drops?

## 3. Assertion-Backed Answers

| Question                   | Evidence & Numbers                                                                                                                                                                                                                                                                                                                                  | Assertion                                                                                                                                                                 |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. 1 kWh vs. $0.01**     | • **CAPEX term per SEC:** ≈$0.011 / kWh (from $1 000/kW, CRF=0.1).  <br>• **Energy term per SEC:** = cost-of-energy ($/kWh).  <br>➡ At $0.08/kWh, each 1 kWh cut saves ≈$0.091/kg.  <br>• Each $0.01/kWh drop (at SEC=50) saves 50×0.01 = $0.50/kg.                                                                                                 | **Power-price improvements beat efficiency improvements per “unit” in our baseline**—you get ~$0.5/kg per cent of power, vs. ~$0.09/kg per kWh of SEC.                    |
| **2. Hitting $8/kg**       | Solve LCOH = (0.011+cost)×SEC:  <br>• If SEC=40 → need cost≈(8/40–0.011)=0.19/kWh.  <br>• If cost=0.05 → need SEC≈8/(0.061)=131 kWh/kg (impossible).  <br>• In practice, **$8/kg** only feasible if cost≤0.10/kWh _and_ SEC≤50.                                                                                                                     | **To get to $8/kg, you must have both decent efficiency (<50 kWh/kg) and power cost ≤$0.10/kWh.**                                                                         |
| **3. Diminishing returns** | • At cost=0.08, moving SEC 50→40 chops LCOH by ~0.9 $/kg.  <br>• Going 40→30 (if you could) chops another ~0.9 $/kg—same step size.  <br>• But **power-cost**: at SEC=50, $0.10→0.05 saves 50×0.05 = $2.50/kg, whereas 0.05→0.00 only saves $2.50 again. **Both are linear**, but your realistic “room to move” is much larger on cost than on SEC. | **Efficiency gains never plateau mathematically, but your practical headroom (40→50 kWh/kg) is limited—whereas power contracts can sometimes move in bigger increments.** |


## 4. Alternative Interpretations

- **High-power-cost regimes:** If you’re stuck paying >$0.12/kWh, efficiency improvements (even expensive stack R&D) become more attractive—because each 1 kWh you shave now saves >$0.13/kg.
- **Low-power-cost regimes:** Once you lock in ~$0.02–$0.04/kWh, further cuts yield only ~$0.02–$0.04/kg, so pushing SEC below 45 kWh/kg is less impactful than scaling up or adding storage.
- **Stack-cost trade-off:** Achieving 40 kWh/kg performance may raise your electrolyzer CAPEX by 20–30%. You must compare that extra CAPEX term (stack materials, manufacturing) against the OPEX savings of ~$0.9/kg


## 5. Implications for LCOH & NPV

- **Combined leverage:** Every 1 kWh/kg of SEC improvement saves you both CAPEX _and_ energy OPEX. At high power cost, that dual saving can be $0.16/kg per kWh—making R&D pay back in <$1 M of extra annual margin for a 10 t/day plant.
    
- **Project focus:**
    - If your site offers only expensive grid power, **prioritize efficiency** (stack improvements, heat integration).
    - If you can secure sub-$0.05/kWh renewables, **deprioritize further efficiency** and instead scale plant size or add storage to capture more clean hours.

## 4. Implications & Trade-Offs

- **Electricity cost remains king.** A $0.01/kWh reduction is worth ~$0.50/kg of H₂ saved when SEC is ~50. Lock in PPAs, behind-the-meter renewables, or demand-response contracts first.
    
- **Efficiency matters—but up to a point.** If your stack is at 60→70 kWh/kg, investing in membrane or catalyst upgrades (shaving 10 kWh/kg) can slash your cost by $4–$5/kg. However, pushing from 45→40 kWh/kg only nets $1–$2/kg.
    
- **Project design:**
    - If you can only secure “mid-range” power (0.07–0.10 $/kWh), prioritize efficiency improvements (target SEC ≤60).
    - If your electrolyzer is already high-performance (SEC ≤50), double down on cheaper power rather than incremental efficiency R&D.
## 6. Bottom-Line Narrative

> **“Efficiency and energy cost are a one-two punch on LCOH.** If you’re paying >$0.10/kWh, even a 5 kWh/kg efficiency gain slashes roughly $0.75/kg. But once you secure ultra-cheap power (<$0.04/kWh), your ‘next dollar’ is better spent on scale or resilience rather than squeezing the last few kWh out of your stack.”


Figure 1 presents the levelized cost of hydrogen (LCOH) as a function of specific energy consumption (SEC) and electricity price for a PEM electrolyzer system. SEC, defined here in kWh of electricity per kilogram of H₂ produced, simultaneously influences both the capital‐recovery component (by determining the required installed power capacity) and the energy‐consumption component of LCOH. Electricity price enters directly into the latter term.

**1. Sensitivity of LCOH to SEC and Electricity Price**  
A local linearization around the baseline point (SEC = 50 kWh/kg; electricity price = $0.08/kWh) indicates that a 1 kWh/kg reduction in SEC yields an approximate LCOH decrease of 0.09 $/kg, whereas a 0.01 $/kWh reduction in electricity price produces a 0.50 $/kg decrease in LCOH. Thus, under baseline conditions, negotiating a one‐cent reduction in the power contract delivers over five times the cost savings of achieving a one‐kWh improvement in stack efficiency.

**2. Target Cost Envelopes**  
Solving the LCOH expression for common competitive thresholds demonstrates that achieving $8/kg requires both an SEC below ~50 kWh/kg and an electricity price at or below $0.10/kWh. Lowering LCOH to $6/kg is only feasible when SEC remains under 45 kWh/kg in conjunction with sub–$0.06/kWh power. In practical terms, simultaneous improvements in efficiency and power procurement must be pursued to attain LCOH values in the $4–6/kg range.

**3. Diminishing Returns and Strategic Priorities**  
Although efficiency improvements produce continuous, linear reductions in LCOH, the realistic headroom for SEC improvements (e.g., from 50 to 40 kWh/kg) is limited by current membrane and catalyst technologies. In contrast, power‐purchase agreements can often deliver larger incremental cost reductions. Consequently, once electricity pricing falls below approximately $0.04/kWh, further investment in SEC gains yields smaller marginal benefits relative to opportunities in plant scale, storage integration, or resilience measures.

**4. Implications for Technology and Project Design**  
– In high–electricity‐cost regimes (> $0.10/kWh), prioritizing R&D efforts to reduce SEC offers the greatest return on investment, as each kWh of efficiency improvement significantly lowers OPEX and CAPEX burdens.  
– Where ultra‐low–cost renewables (< $0.04/kWh) can be secured, project developers should shift focus toward scaling plant capacity or incorporating energy‐storage solutions to maximize capacity factor and fully exploit low‐cost power.

**5. Conclusion**  
The contour analysis reveals that, while both SEC and electricity price are critical levers on LCOH, their relative importance depends on the achievable range of each parameter. For projects constrained by grid tariffs, efficiency enhancements represent the most effective cost‐reduction pathway. Conversely, in contexts where renewable energy can be procured at very low cost, strategic investments in scale and operational resilience will deliver superior economic performance.

### 1. Local Sensitivities at the Baseline

Baseline conditions:
- SEC₀ = 50 kWh/kg
- Price₀ = $0.08/kWh
- LCOH₀ ≈ $9.0/kg
    

**a. Efficiency Improvement**
- A reduction of 1 kWh/kg (∆SEC = –2% relative) lowers LCOH by ≈$0.09/kg.
- **Relative savings:** 0.09 / 9.0 ≈ 1.0% LCOH reduction.
- **Normalized sensitivity:** (1 % SEC improvement) ⇒ (0.5 % LCOH reduction).
    

**b. Electricity‐Price Improvement**
- A reduction of $0.01/kWh (∆Price = –12.5% relative) lowers LCOH by ≈$0.50/kg.
- **Relative savings:** 0.50 / 9.0 ≈ 5.6% LCOH reduction.
- **Normalized sensitivity:** (1 % price reduction) ⇒ (0.45 % LCOH reduction).
    

> **Key insight:** Per “unit” of relative improvement, SEC gains and price gains are of the same order (0.5 % vs. 0.45 % LCOH per 1 % change), but the _realistic headroom_ for electricity‐price negotiations (often >20 %) typically exceeds that for stack‐efficiency improvements (<20 %), making power‐contract negotiations the higher‐leverage lever in most projects.

---

### 2. Scenario‐Level Improvements

Let us compare two plausible improvement pathways:

|Improvement Pathway|Parameter Change|Relative Change|LCOH Change|% LCOH Change|
|---|---|---|---|---|
|**Moderate efficiency R&D**|SEC: 50 → 45 kWh/kg|–10 %|–$0.9/kg|–10 %|
|**Aggressive PPA negotiation**|Price: $0.08 → $0.06/kWh|–25 %|–$1.1/kg|–12 %|
|**Combined (R&D + PPA)**|SEC → 45 kWh/kg & Price → $0.06/kWh|–10 %, –25 %|–$2.0/kg|–22 %|

- A **10 % SEC improvement** alone reduces LCOH by ~10 % (≈$0.9/kg).
- A **25 % electricity‐price reduction** alone reduces LCOH by ~12 % (≈$1.1/kg).
- Pursuing **both** simultaneously yields a **22 %** LCOH reduction (≈$2.0/kg).

---

### 3. “Stretch” Improvements

For long‐term, transformational targets:

| Stretch Pathway                                | Parameter Change                    | Relative Change | LCOH Change | % LCOH Change |
| ---------------------------------------------- | ----------------------------------- | --------------- | ----------- | ------------- |
| **High‐efficiency membranes**                  | SEC: 50 → 40 kWh/kg                 | –20 %           | –$2.7/kg    | –30 %         |
| **Zero‐subsidy renewables (behind‐the‐meter)** | Price: $0.08 → $0.04/kWh            | –50 %           | –$3.6/kg    | –40 %         |
| **Combined deep improvements**                 | SEC → 40 kWh/kg & Price → $0.04/kWh | –20 %, –50 %    | –$6.3/kg    | –70 %         |

- A **20 % improvement in SEC** can cut LCOH by ≈30 % (≈$2.7/kg).
- A **50 % drop in power cost** can cut LCOH by ≈40 % (≈$3.6/kg).
- **Together**, these deep improvements drive a **70 %** reduction in LCOH (from $9.0 to $2.7/kg).

---

### 4. Implications for Project Strategy

1. **Short‐term wins**:
    - Focus on electricity‐price reductions, which often yield larger absolute LCOH savings given typical negotiation headroom (>20 %).
    - A 25 % PPA improvement alone can deliver >10 % LCOH reduction—equivalent to considerable R&D effort.
        
2. **Medium‐term balance**:
    - Concurrently pursue modest R&D (SEC → 45 kWh/kg) and PPA efforts (Price → $0.06), cumulatively cutting LCOH by ~22 %.
        
3. **Long‐term ambition**:
    - Combine high‐performance membranes (SEC ≈ 40 kWh/kg) with behind‐the‐meter renewables ($0.04/kWh) to approach LCOH levels below $3/kg (≈70 % reduction).
        

---

### 5. Conclusion

By expressing both stack‐efficiency and power‐cost improvements in relative—and therefore directly comparable terms, one sees that **electricity‐price interventions typically unlock larger, more immediately attainable LCOH savings**, whereas **SEC improvements** offer sustained, linear benefits but require major technology development to deliver equivalent impact. A **balanced pathway**, integrating modest R&D and aggressive PPA strategies, can achieve robust (20–30 %) LCOH reductions within typical project lifecycles.



----
Figure 5.3.3 reinforces the multivariate insight that efficiency enhancements and energy efficiency both serve as important supporting levers, but the economic fate of a PEM electrolyzer plant is overwhelmingly dictated by the price of its power. Strategic efforts that couple modest SEC gains (to ~45 kWh kg⁻¹) with contracting or on‐site generation at ≤ 0.05 USD kWh⁻¹ create the most robust pathway toward sub-5 USD kg⁻¹ green hydrogen.
Synergies and diminishing returns.
reading downward at fixed SEC underscores once more that electricity price is the dominant lever: even a highly efficient 45 kWh kg⁻¹ electrolyzer costs ~5.5 USD kg⁻¹ at 0.05 USD kWh⁻¹ but balloons to > 9 USD kg⁻¹ at 0.15 USD kWh⁻¹. In the high-electricity price scenarios, efficiency gains flatten the contour slightly, but the bands remain widely spaced vertically, each one‐cent change in tariff translates to ~0.5 USD kg⁻¹ shift in LCOH regardless of SEC.
**“Safe-harbor” efficiency targets.**  
A practical takeaway is the identification of an “efficiency plateau” beyond which further SEC reductions deliver only marginal cost benefit under typical power prices. For tariffs near 0.07 USD kWh⁻¹, R&D should prioritize pushing SEC below ~48 kWh kg⁻¹ to break under 6 USD kg⁻¹ hydrogen; achieving 45 kWh kg⁻¹ extends that cost line only modestly to ~5.8 USD kg⁻¹. Below ~0.05 USD kWh⁻¹, the contour bends more sharply, suggesting that highly efficient stacks (< 45 kWh kg⁻¹) paired with ultra-low‐cost power could reach the 4 USD kg⁻¹ milestone crucial for industrial parity.




**Design-choice implications.**

- **Efficiency investments** (e.g., thin-film catalysts, advanced bipolar plates) pay back fastest in regions with volatile or high grid tariffs, because every avoided kilowatt-hour offsets a premium price.


At high electricity prices (≥ $0.12/kWh), a 5 kWh/kg efficiency gain delivers $1–$1.5/kg LCOH savings making stack efficiency improvement through R&D more valuable. Whereas at low electricity prices (≤ $0.05/kWh), that same efficiency gain only saves ≤ $0.3/kg. Our baseline sits below the green-hydrogen threshold. This indicates that even current electrolyzer efficiencies (50 kWh/kg) can produce cost-competitive hydrogen if power can be sourced at 0.075/kWh. Further improvements in SEC will deepen that cost advantage. Approaching blue hydrogen price point will require SEC lesser than 45 kWh/kg and power < $0.03/kWh thus demanding both catalytic breakthroughs and cheaper electricity source.

~~Reading downward at fixed SEC highlights once again that electricity price is the primary lever: even a highly efficient 45 kWh/kg electrolyzer costs ~5.5 $/kg at $0.05/kWh, but rises to over $9/kg at $0.15/kWh. In scenarios with high electricity prices, efficiency gains slightly flatten the contour, but the bands remain widely spaced vertically; each one-cent change in tariff translates to about $0.5/kg shift in LCOH, regardless of SEC. For tariffs near $0.07/kWh, R&D should focus on reducing SEC below  48 kWh/kg to lower the cost to under $6/kg of hydrogen; achieving 45 kWh/kg only modestly improves that cost to about $5.8/kg. Below approximately $0.05/kWh, the contour steepens more noticeably, indicating that highly efficient stacks (under 45 kWh/kg) paired with ultra-low-cost power could achieve the $4/kg milestone, which is crucial for industrial parity.


![[image-84.png]]



The $11.5/kg “green‐hydrogen” threshold (dashed line) shows that at  CapEx levels ($800–$1 000/kW), the plant must run at Capacity factor (CF) greater than 0.7 to be with the baseline price.  Plant downtime can be improve through predictive maintenance ( fault detection) and reliable RE system configuration. The efficiency of the PEM Electrolyzer is a function of the availability and ratio of energy supplied to the rated power of the electrolyzer system @astrianiOptimalPlanningRenewable2024 .










capacity factor | LCOE cost of energy sys |  LCOE
logic is choice of energy source or mix to the cost the energy system.

grid energy mix?
RE only effect?



capacity factor | capital cost of energy | LCOE



visual description of energy composition
bar chart
	LCOE and composition of different energy system





---
	now 2025-07-18T08:44:45-04:00
Energy system results

Goal: variation in LCOE for different configurations with different component contributions
LCOH

Basis: 20MW rated system

configurations:
	Wind
	PV
	Hybrid
	Hybrid with storage

component.
Capital cost
opex ( fixeed + variable)
Indirect cost( installation + land cost)
Battery cost


---
## Cost Breakdown by Configuration

20MW each
10MW x10MW hydrid confiig
20MW hydbrid with 5 MW storage


ConfigurationEquipment cost ($)Land and installation ($)Fixed & variable O&M ($)Battery cost ($)Battery O&M ($)Total cost ($)PV15,341,000920,000235,000096,00016,592,000Wind30,683,0002,455,000345,000096,00033,579,000Hybrid24,664,0001,808,000145,000096,00026,713,000Hybrid with storage24,664,0001,808,000145,0005,620,00096,00032,333,000

![[Writing/2025/attachments/image-23.png]]

![[Writing/2025/attachments/image-24.png]]


## Performance Metrics by Configuration
![[Writing/2025/attachments/image-21.png]]

#capacity factor

![[image-27.png]]


LCOE breakdown
![[image-26.png]]

## LCOH Comparison Across Configurations


![[Writing/2025/attachments/image-25.png]]


------


# Key PEM Electrolyzer Cost and Performance Parameters for Sensitivity Analysis
nges

**Capital cost:** Future DOE targets envision highly scaled manufacturing driving down stack and BoP costs to ≈ $800 /kW, whereas today’s smaller‐volume deployments often see up to $3 500 /kW installed capital costs.

**Fixed O&M:** Lower values reflect optimized maintenance regimes and service contracts; H2A defaults sit at 5 % of capex, while legacy systems can run closer to 8 % annually.

**Electricity cost:** At times of excess renewables, electrolyzers can procure power at $0.03 /kWh; average U.S. industrial rates hover around $0.07 /kWh, and peaking or retail rates can spike past $0.15 /kWh.

**Water cost:** Deionized water is a minor contributor, H2A assumes $0.005 /gal—but costs can vary with local treatment infrastructure.

**O₂ credit:** Many projects don’t monetize oxygen (low end), but large‐scale gas producers can sell at $0.09–0.17 /kg.

**Tax rate:** Reflects the 21 % federal corporate rate plus state levies (0–12 %), yielding combined rates from 21 % up to ≈ 33 %.

**Efficiency:** Modern PEM stacks achieve ≈ 55 kWh/kg H₂ (≈ 65 % LHV efficiency), with R&D targets pushing down toward 45 kWh/kg; less optimal designs may consume 60–65 kWh/kg.


driving “tornado” or Monte Carlo simulations 
to see which factors most influence the levelized cost of hydrogen in your case studies




![[image-32.png]]



![[image-31.png]]


##### 5.2.4 Energy‐Supply Configuration Comparison

To round out our scenario analysis, we examined four distinct electricity‐supply options: PV‐only, wind‐only, a PV–wind hybrid, and a hybrid coupled with battery storage, and quantified both their capital‐cost structure and their impact on LCOH. Figure 5.2.4 (a) breaks down the installed and O&M expenditures for each configuration, while Figure 5.2.4 (b) overlays the resulting LCOH.

Quantitatively, a standalone PV plant entails the lowest upfront investment, ≈ 16 million USD, because of the relatively low per-kW capital cost of solar panels and minimal site-prep requirements. However, its capacity factor (20–25 %) limits annual hydrogen output and drives its LCOH down only to ≈ 9 USD kg⁻¹ (Figure 5.2.4b), the lowest among the four but still electricity‐limited. Conversely, the wind‐only configuration carries the highest installed CAPEX ≈ , 34 million USD, due to costlier turbine hardware and civil works, and its LCOH peaks at ≈ 12 USD kg⁻¹, mirroring the high levelized cost of wind‐derived electricity, despite a higher capacity factor (35–40 %).

Introducing both PV and wind in a hybrid layout smooths power delivery and raises the capacity factor to ≈ 30–35 %, enabling a CAPEX reduction of ≈ 28 million USD compared with wind alone. As a result, its LCOH moderates to ≈ 11 USD kg⁻¹ lower than wind but above PV, demonstrating how mixed‐technology portfolios can balance capital demands and output variability. Finally, adding a two-hour battery buffer to the hybrid brings total CAPEX back up to ≈ 32 million USD, evenly split between renewable and storage hardware, and nudges LCOH upward to ≈ 11.5 USD kg⁻¹. Although storage increases firm capacity factors to > 85 %, an important feature for guaranteed dispatch, its high capital and O&M overheads only marginally improve hydrogen pricing when grid‐parity power remains elusive.

Taken together, these results show that equipment cost is the primary driver of CAPEX in all off‐grid scenarios and that capacity factor gains from hybridization can offset some of the renewable‐system premium but cannot fully substitute for access to low‐cost grid or wholesale power. From a project planning perspective, a pure‐PV system offers the lowest barrier to entry, while hybrid configurations trade modest cost increases for greater dispatch reliability. Adding storage further insulates hydrogen production from renewable intermittency but at a capital premium that must be justified by downstream value such as time‐sensitive refueling or grid‐services revenue. Ultimately, the choice of energy configuration should align with local resource profiles, off-taker requirements, and financing constraints, bearing in mind that CAPEX savings here flow directly into lower LCOH only insofar as they preserve a high utilization rate of the electrolyzer.





We find that **PV‐only supply** is the most attractive for green‐hydrogen plants when capacity factors exceed ~25 %, thanks to its low capital intensity. **Wind‐only** is less economic unless turbine prices fall below 1 000 USD kW⁻¹ or O&M can be dramatically reduced. A **hybrid** design can capture some of wind’s low marginal‐cost benefit without fully inheriting its high capex, resulting in a middling but more stable LCOH. Finally, **battery storage**—while valuable for grid‐islanded or time‐shifting applications—must achieve a capital cost below ~ 400 USD kWh⁻¹ to avoid pushing hydrogen costs above that of the hybrid without storage.





----
now 2025-07-17T07:33:11-04:00

![[image-80.png]]

The operating power is the ratio of the power supplied to the electrolyzer and the electrolyzer rated power.

**Results and Discussion**

Figure X presents the levelized cost of hydrogen (LCOH) as a function of two operational parameters: the electricity price (from $0.01 to $0.15 per kWh) and the electrolyzer operating power expressed as a percentage of its rated power (5 %–100 %). Operating power here captures the fraction of time and load at which the stack is actually energized, and it directly governs annual hydrogen throughput relative to installed capacity.

Here, “operating power” is defined as the ratio of actual electrical input to the electrolyzer versus its nameplate power rating—effectively a proxy for utilization or capacity factor under dynamic dispatch.

---
### 1. Extreme Cost Inflation at Low Operating Power

At very low operating power (≤ 10 %), LCOH rises precipitously—exceeding $40 /kg even at the lowest electricity prices. This behavior reflects the dominance of capital‐recovery costs when the same electrolyzer stack is scarcely utilized: with only 876–1 752 hours of full‐power equivalent operation per year, each kilogram of hydrogen bears a disproportionately high share of the fixed‐charge burden.

---
### 2. Diminishing Returns Above Mid‐Load Operation

Between 20 % and 50 % operating power, LCOH falls sharply as utilization improves. For example, at $0.08/kWh, increasing operating power from 20 % to 50 % reduces LCOH from roughly $18 /kg to $8 /kg (Δ$10/kg). However, above ≈ 50 % load the contour lines flatten: pushing from 50 % to 100 % only yields another $3–4/kg reduction. This inflection marks the point where further increases in utilization deliver progressively smaller amortization benefits, and where operating‐cost (electricity) begins to dominate.

---
### 3. Electricity Price as the Overarching Lever

Across all operating‐power levels, reducing electricity price remains the most potent lever. At 100 % operating power, cutting price from $0.15→$0.05/kWh lowers LCOH by ~$12/kg, whereas raising operating power from 50 %→100 % at a fixed $0.10/kWh only saves ~$4/kg. In practical terms, securing long‐term low‐cost power contracts or integrating on‐site renewables has a larger impact on hydrogen economics than squeezing marginal increases in load factor once past moderate utilization.

---
### 4. Implications for System Design

- **Intermittent renewables alone** (e.g. standalone PV or wind with CF ≈ 30 %) imply operating power ≲ 30 % and thus LCOH > $12/kg unless subsidized—or unless coupled with storage or demand‐management to boost effective load.
    
- **Hybrid or firm power integration** that ensures ≥ 50 % operating power is essential to bring LCOH into the competitive $6–8/kg band, especially when paired with electricity prices below $0.08/kWh.
    
- **Oversizing strategies** (installing more electrolyzer capacity than renewable peak) can elevate operating power but raise capital outlay; the contour flattening beyond 50 % suggests a balanced sizing that targets 50–70 % utilization maximizes economic returns.
    
### Implications for Renewable Integration and Market Participation

- **Intermittent Renewables:** Systems tied solely to solar or wind (with typical capacity factors of 20–40 %) will face LCOH in excess of $8–12 /kg unless paired with storage or backup dispatch.
    
- **Demand-Response & Flexibility:** Operating only during low‐price “duck curve” hours (e.g. 30 % of the time) risks hydrogen costs >$15/kg. Developers should therefore target at least 50–60 % utilization to achieve LCOH in the $6–8/kg range.
    
- **PPA Strategy:** Securing low, firm energy contracts (< $0.05 /kWh) is essential to harness the cost benefits of high utilization. Without such contracts, even 100 % operating power can only drive LCOH down to ~$6/kg, provided power remains below $0.06/kWh.
---

### 5. Conclusion

The contour analysis underscores that **both** high utilization and low electricity cost are necessary to achieve economically viable green hydrogen. However, **electricity price** is the dominant cost driver across all operating‐power regimes. Developers should therefore prioritize securing cost‐effective, high‐availability power—through PPAs, co‐located renewables with storage, or grid‐firm contracts—before seeking incremental gains in stack utilization.


### 5. Bottom‐Line Narrative

> **“Electrolyzer utilization and electricity price act together to shape LCOH: below ~40 % operating power, capital costs dominate and yield prohibitively high hydrogen prices; above ~60–70 %, electricity cost takes over as the key lever.**  
> – **For intermittent renewables**, aim for hybrid configurations or storage that boost utilization above 50 %.  
> – **For grid-tied projects**, secure PPAs under $0.06 /kWh and operate above 80 % to reach competitive LCOH levels ($5–7/kg).



---


Stack column chart for cost commposition.


 EFFECTIVE CAPACITY FACTOR OF SYSTEM

Basis

| Category                    | installed capacity, MW | CF                                |
| --------------------------- | ---------------------- | --------------------------------- |
| Capacity factors of RE sys  |                        |                                   |
| PV                          | 20MW                   | 25%                               |
| Wind                        | 20MW                   | 34%                               |
| Hybrid                      | 10-10MW                |                                   |
| Industrial grid electricity |                        | 95%                               |
| Nominal Battery capacity    | 20MWh                  |                                   |
| battery cycles per day      | 1                      |                                   |
| Annual battery discharged   | 7300                   | MWh                               |
| Battery round trip eff      | 0.88                   | round-trip efficiency (typically) |
| CF hybrid total             | 0.34                   |                                   |



![[newplot.png]]


For PEM hydrogen production, the choice of renewable feedstock is often framed around capacity factor and marginal electricity price.
**PV as a Cost‐Effective Baseline:** Despite its lower capacity factor, PV’s low capital cost makes it the cheapest option for driving the electrolyser in this costing framework.
**Hybridization and Firming Trade-Offs:** Hybridizing PV and wind smooths generation profiles but comes at a 30–40 % capital premium. 
**storage should be reserved for applications requiring 24/7 output rather than pure cost-reduction** 

Developers targeting minimal LCOH should therefore consider PV-centric sites or PPAs first, then layer in wind or storage only if high utilization or firm dispatch is critical to their business case.

> [!question] 
> Quuestion : Why does hybrid not have higer
> Because it is average half of the capacities of both RE systems.

Total operational cost including battery maintaince and system maintenance



![[image-80.png]]
Figure X presents the levelized cost of hydrogen (LCOH) as a function of two operational parameters: the electricity price (from $0.01 to $0.15 per kWh) and the electrolyzer operating power expressed as a percentage of its rated power (5 %–100 %)  
Here, “operating power” is defined as the ratio of actual electrical input to the electrolyzer versus its nameplate power rating. Thus, a proxy for utilization or capacity factor under dynamic dispatch.   
At very low operating power (≤ 10 %), LCOH rises precipitously, exceeding $40 /kg even at the lowest electricity prices. This behavior reflects the dominance of capital‐recovery costs when the same electrolyzer stack is scarcely utilized: with only 876–1,752 hours of full‐power equivalent operation per year. Between 20 % and 50 % operating power, LCOH falls sharply as utilization improves from roughly $18 /kg to $8 /kg (Δ$10/kg). However, above ≈ 50 % load, the contour lines flatten: pushing from 50 % to 100 % only yields another $3–4/kg reduction. This inflection marks the point where further increases in utilization deliver progressively smaller amortization benefits, and where operating‐cost (electricity) begins to dominate.  
The results imply that Intermittent renewables alone operating power ≲ 30 % will risk hydrogen costs > $12/kg unless subsidized or unless coupled with storage or demand‐management to boost effective load. A Hybrid power integration that ensures ≥ 50 % operating power is essential to bring LCOH into the competitive $6–8/kg band, especially when paired with electricity prices below $0.08/kWh. Therefore, priority should be given to securing cost‐effective, high‐availability power through PPAs, co‐located renewables with storage, or grid‐firm contracts



LCOE
Figure X. LCOE and the corresponding LCOH impact for hydrogen production for energy configuration scenarios. 
To round off our scenario analysis, we examined four distinct electricity supply options: PV-only, wind-only, a PV–wind hybrid, and a hybrid coupled with battery storage. For PEM hydrogen production, the choice of renewable feedstock is often framed around capacity factor and marginal electricity price. The basis represents a uniform 20 MW installed capacity for PV and wind services (10 + 10 MW for the hybrid), with capacity factors of 25 % (PV), 34 % (wind), and a hybrid configuration and storage cycles at one 20 MWh discharge per day.
The PV‑only scenario exhibits the lowest energy production cost per kWh ($0.11/ kWh) in fixed charges and negligible marginal cost, yielding an LCOE of ($0.12/ kWh) and an LCOH of ($9 /kg). Its modest 25 % utilization is more than offset by the relatively lower per‑kW price of solar panels and minimal BoP complexity. Wind-only delivers more consistent output (CF ≈ 34 %) but incurs higher levelized fixed charges ($0.16 /kWh) and a larger marginal cost ($0.03/ kWh) reflecting turbine O&M. The turbine CAPEX outweighs its better capacity factor to produce the highest LCOH at $12.2/ kg. 
These altogether show that equipment costs are the primary drivers of LCOE in all off-grid scenarios. Greater RE availability does not automatically translate into cheaper hydrogen. Gains in capacity factor from hybridization can offset some of the premium associated with renewable systems, but cannot completely replace access to a low-cost grid or a good PPA tariff.  
A standalone PV system offers the lowest barrier to entry, while hybrid configurations trade modest cost increases for improved reliability. Incorporating storage further protects hydrogen production from renewable intermittency, but incurs a capital premium that must be justified by downstream value, such as time-sensitive refueling or grid services revenue. Ultimately, the choice of energy configuration should align with local resource profiles, off-taker requirements, and financing constraints. RE system cost savings will translate to lower LCOH only if they maintain a high utilization rate of the electrolyzer.
