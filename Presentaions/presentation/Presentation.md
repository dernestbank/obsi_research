
Objectives:
----
- [ ] To plan out my speech 
	- [ ] framework for explaining results
	- [ ] actual transcript for methods and results
	- [ ] transcript for background
	- [ ] filler words
- [ ] practicing Q&A
- [ ] Random question slides


# Prelude
Thanks for attendance.
Acknowledgement
ASD , neurodivergent declaration.

# Introduction

#survey
Earlier this year I had the privilege to interview industrial personal of the challenges the faces the adoptions of the hydrogen market. through the NSF icorps program.

#fill in some except of the interview. Toyota guy

And the results was quiet similar to what a survey results the DOE had publish. Most people assume tthe  biggest barrier to the adoption of the hydrogen market is the cost.

#proection
Meanwhile , IES has projected the global hydrogen demand to surge art ##### in the next five.
Ofcourse this will be influenced by the growth in demand the ....industrys.


# Background
#reported_cost of hydrogen


#total_cost_composition







#tax_credit and #incentives.








# Aims and Objectives

### Description of Framework


#Lead_into:
And so we will break this down into 3 aims and specific objection.


### Aims and task


#research_Question
should be based on conflicts and gaps in literature.
as the point comes out
 - what are the cost drivers: arrises from the confusiion of what the the main cost drivers are in electrolyser. This answer will be addressed with the contour plot. (In the study of ... and that they were not wrong but because thery were all looking at different scales.)
- how does the PEM design affect the cost( it parameters such as the current density)
- How does energy CONFfiguration




### Metrics and 



**Format for Explaining results**
How to read and interpret: 
Observations from visuals. 
Reasons for observation
Insights and Implication
What does it clarifies from literature
keywords



## Model validation
#Electrochemical_validation
the second task under the fir aim was to validate our electrochemical module
And so we validated our model using data from literature (debe et al...) @debeInitialPerformanceDurability2012 
within the acceptable level of error.
The basis of our model. 
The VIR the polarization curve, IR curve:
thte activaton overpoential dominate cus of voltage loss. The anod

posible questions
what is the an acceptable level of error in that particula

### **Suggested Talking Points (What to Say):**

"To build confidence in our framework, the first step was to validate our electrochemical model. We couldn't make reliable economic forecasts without a trustworthy physics foundation."

**(Point to the left chart - the polarization curve):**

"Here on the left, you can see our model's output, shown by the solid line, plotted against experimental data points from the literature. As you can see, the model tracks the real-world performance of a PEM cell with very high fidelity across a wide range of operating current densities. Quantitatively, we achieved a Root Mean Square Error of just 32 millivolts, which confirms the model is robust and accurate."

**(Point to the right chart - the voltage breakdown):**

"With a validated model, we could then use it to understand _why_ the cell performs the way it does. This chart breaks down the total cell voltage into its core components. The blue area at the bottom is the ideal, reversible voltage required for water splitting."

"What's crucial to see is the large orange section, which represents the **activation overpotential**. This is the extra energy needed to get the chemical reactions started at the anode and cathode. Our model clearly shows that this activation loss is the single largest contributor to inefficiency in the system."

"This physical insight is important because it validates the global research focus on developing better catalysts. By improving the catalyst, we can lower this activation barrier, reduce the overall cell voltage, and directly decrease the amount of electricity needed to produce each kilogram of hydrogen."

---
# PEM design sensitivity
Effec of membrane thickness

Application:
In fuel cell range of thickness
 5 to 100 micrometers (µm), with thinner membranes generally preferred for increased conductivity and efficiency
`The specific thickness chosen depends on the type of fuel cell, operating conditions, and desired performance characteristics. For example, fuel cell vehicles often utilize thinner membranes (e.g., 5-20 µm) to maximize range and power density. In contrast, direct methanol fuel cells may use thicker membranes to mitigate methanol crossover.`

Recomendation: polymer ionomer engineering to improve conductivity..
minimize gass cro type of polymers, reinforcement polymers, 
Minimizing ohmic losses
Thinning the membrane: A thinner membrane reduces the distance protons need to travel, thereby lowering the electrical resistance and resulting in decreased ohmic losses.
Increasing mechanical stability
Reinforcing the membrane: Using materials like expanded polytetrafluoroethylene (ePTFE) or other reinforcing polymers or oxides can enhance the membrane's mechanical strength
Reducing gas crossover
Increasing membrane thickness: A thicker membrane can act as a better barrier against the permeation of hydrogen 
Implementing recombination catalysts: Incorporating catalysts, such as platinum particles, within the membrane or catalyst layers can facilitate the recombination of hydrogen and oxygen that crosses over, reducing the overall concentration of hydrogen in the oxygen stream.

Effect of temperation
reducs activation overpotential by hencing the rate of reaction.

- application
- Low-Temperature electrolysis (LTE)
temperatures between 50-80°C, where the benefits of temperature increase are balanced with the need to avoid excessive degradation. 
- High-Temperature Electrolysis (HTE)

#### Design on LCOH

high temperature (≥ 90 °C) and moderate current density (0.5–1.5 A/cm²) yields LCOH ≈ 6.2–6.5 $/kg.
higher saves on stack hardware but inflates the electricity bill per kilogram of H₂.

 The contour plateau at low density/high temperature identifies the **“sweet spot”** where marginal capex increases are balanced by substantial OPEX savings.

![[image-81.png]]

membrane
thicker membrane high capital cost, lower efficiency(SEC), 

![[image-82.png]]

- [ ] Annotate different membranes thickness for different applications

introducting the multiobjective obtimization problm

![[Presentaions/presentation/attachments/image-2.png]]

----





## Aim 2: Economoic analysis

Basis
Scop -> Basis -> Process descrioption
P.D : liquid gas separation unit
electrolyser specification
Energy configuration
Gas purification.
The scope of our analysis volves the PEM electrolyser and the Balance of plant, and the the electricity ource. We excluded the storage and transportation to enable us eeffect ......

We established a baseline plant of production capacity 10 ton, over 20 years. we assume a construction period of 3 years. The plant operating with an average capacity factor of 0.965We used a depreciating method of MACRS and WACC.

> [!question] 
> What is the MACRS:
> why that: 
> what other type could you have used

#scale_comparison
- keywords:
CO-location or onsite generation, pre-optimal basis, 
- how to interpret
The distributed refers to onsite colocation green hydrogen production for other process that require intermittent supply of green hydrogen at a high pressure of 30bar.
centralized refers to large production plants meant to supply a region. But will have additional cost of storage, (we mentioned that the cost of storage and transport is outside the scope of this research)
- observations 
we observe a significant decline in levelized cost, from approximately $8.6/kg to $6.6/kg. Two cost drivers account for most of this 23% reduction. 
Reasons for observation
1. economies of scale considerably reduce the cost per kilogram contribution of fixed OPEX and FCI: the larger plant spreads labor, administration, and capital recovery over a production volume nearly seven times greater, compressing those bars in the stacked profile
 2. "sub-linear cost scaling": As the facility gets bigger, the cost of these components doesn't increase at the same rate as the facility's size.   Because of this, when a facility produces more hydrogen, the cost to build and maintain these components per unit of hydrogen produced actually decreases. This makes larger facilities more economically efficient in terms of capital recovery,

- insights
First, right-sizing a plant for a specific offtake avoids both the high unit costs of undersized assets and the electricity-driven economics of mega-scale installations operating at today's power prices
Second, feedstock electricity price volatility becomes more significant than any other single parameter once capacities exceed approximately 10,000 kg/day
Finally, the modest cost penalty of the distributed case highlights its potential niche wherever

- clarification
a comparison between centralized and distributed systems. It suggests that while distributed systems may have a slightly higher cost, they offer advantages in certain situations:  
1. Transport compression: reduced need for long-distance transportation of resources.  
  
2. Permitting: Potentially easier to obtain necessary permits for smaller, distributed facilities.  
  
3. Resiliency: Distributed systems may be more resilient to disruptions or failures.  
These benefits could make distributed systems preferable in some cases, even if they are not the cheapest option. The text implies that in scenarios where these factors are more important than minimizing costs, distributed systems could be the better choice.






#IRR_NPV

![[image.png]]

context and basis
basis effect

NOw one can argue that , power can be purchased at a cheaper rate for larger capacity systems and lead to a better projection for centralized systems. But to reduces the assessment is don't on an equal prices of energy for all three scenarios.



**Centralized Systems (50,000 kg/day):** Deliver the highest NPV (over $370 Million) but offer only marginal IRR improvements (37%), suggesting that further upscaling introduces complexities (permitting, supply chain) without proportional financial gains.

#### Project Value Maximized by Larger Scales, with Plateauing IRR
- **Substantial NPV Growth:** Net Present Value (NPV) dramatically increases with scale, from limited value for distributed systems to $77M for baseline and over $370M for centralized plants.
    - This indicates significant cumulative value creation for larger projects over their lifetime.
        
- **IRR Gains Plateau:** While Internal Rate of Return (IRR) improves from 13% (distributed) to 32% (baseline), it only marginally increases to 37% for centralized systems.
    - This suggests that while larger projects generate more absolute profit, their capital efficiency gains diminish beyond a certain point.

---

Contour plot
--
clarification on the disagreement on what the main cost driver of hydrogen i s explained.

studies that assume lower production volume found .
studies hat assume larger volumes founds electricity cost to be the main cost driver.



---


#Sensitivty_analysis
keep the same slides and move pointer with changing basis and point references

- how to interpret
these outline a band of economic possibilities anchored at our 10,000 kg/day baseline and widening to $4.7–9.5/kg across the envelope of scenarios. The blue color band indicates optimistic scenarios, whereas the orange color band shows high-end scenarios.

- Observations
The tornado analysis shows that our cost estimates for hydrogen heavily depend on current market conditions and future technical goals. In the high-end scenarios, where electricity could be priced at $0.15/kWh in certain states, or installed CAPEX at $1,500/kW, SEC at 55 kWh/kg, and O&M around 8% of CAPEX, the LCOH could potentially rise to $9.5/kg. Here, the risk for green hydrogen is high, and special financing or contracts might be necessary to achieve acceptable returns. Conversely, in the “low-cost” scenarios, where power can be obtained at $0.03/kWh during renewable surpluses or if DOE targets for PEM are met (CAPEX ≈ $250/kW and SEC at 45 kWh/kg), or if O&M is optimized to 5% of CAPEX, LCOH could drop below $5/kg.

Reasons for observation
keep the same slides and move pointer with changing basis and point references

Item, context, effect, take away, refs
- context and basis's
#### Electricity cost
item:IEA trend and distribution: 
Low: $4.7/kg. in regions with high solar penetration (e.g., California’s midday surplus) or in markets where electrolyzers are co-located behind the meter with dedicated PV and wind. 
within reach of blue hydrogen under mid-range carbon-capture costs

High:$9.50/kg. in a peaking-price region, relying on 24/7 renewable energy certificates. 
way far from >>gray hydrogen produced from SMR
Application: Average price for Middle Atlantic regions of Pennsylvania, new jersey 
source EIA
base of 7.03 /kg East South Central of Alabama, Kentucky , Tennessee.
Effect and Take away: electricity cost volatility poses the primary threat to project economics
levelized cost of electricity (LCOE) translate
 emphasize ultra-low-cost, high-capacity-factor power procurement over marginal efficiency gains

#### Uninstall capital cost
item:The cost curve
Low Doe target: lower LCOH by ~$1.8/kg. optimistic 2030 DOE target. that assumes serial production of large-format stacks, thin-film catalyst deposition, and integrated MEA

High end: $1,500/kW, today’s small-lot quotes of

Take away: manufacturing scale-up offers the second most influential lever after affordable power
While capital cost has a lesser effect than electricity cost, it is greater than any other operational cost. Future breakthroughs in cost optimization for stack manufacturing will more decisively reduce hydrogen prices than incremental gains in water, labor, or utility efficiency.


#### Fixed operation
such as like insurance, property taxes, and maintenance contracts -
items: states with no property tax
**Stack Replacements:**
 Electrolyzer stack replacements, while technically a fixed cost over the system's lifetime, are often handled separately due to their significant impact on overall costs.

#**H2A Methodology:** 5% of the capital cost
- **Fixed vs. Variable Costs:**
    Fixed operating costs are independent of the amount of hydrogen produced, while variable costs fluctuate based on production volume.


Electrolyzer stack replacements, while occurring periodically (e.g., every 10 years), are treated as a significant fixed cost component over the system's lifetime, typically estimated at 15% of the initial installed CAPEX according to H2A methodology




----
To NPV

There are **no states in the United States that have zero property tax**.
some states have **very low property tax rates**,
- Hawaii: Known for the nation's lowest effective property tax rate (around 0.27%-0.32%).
- Alabama: Has one of the lowest rates, often below 0.40%.
- Colorado: Offers relatively low rates, often around 0.49%-0.55%.

states with  exemptions or low rates for industrial property
**1. States that generally exempt or don't tax business personal property (including potential industrial equipment):** 

- North Dakota
- South Dakota
- Ohio
- Pennsylvania
- New Jersey
- New York
- New Hampshire
- Hawaii
- Delaware
- Illinois
- Minnesota
- Iowa
https://lyallcpa.com/tips/which-states-have-business-personal-property-tax#:~:text=WHICH%20STATES%20DO%20NOT%20TAX,Iowa
@hicksPropertyTaxNew1983

take away: 

These numbers set clear technical targets: achieve ≤45 kWh/kg SEC, ≤$500/kW installed cost, and a power tariff of ≤$0.05/kWh, and green hydrogen becomes competitive in large swaths of the North American market even without extraordinary policy support.

#### for utility and non-energy feedstocks

three-fold increase in water and ancillary utility cost only affects the LCOH by less than ± 0.15 $/kg.

water consumption is economically immaterial (≈ 2% of total variable cost).

- Electricity 
take aways
a one-cent increase per kilowatt-hour corresponds to roughly $12 million in project value over twenty years

### NPV sensitivity
how individual parameters affect the levelized cost of hydrogen, project developers and investors ultimately prioritize value creation measured by NPV.

### Electricity and Electrical efficiency

Low and High: 
for the same assumptions as before

Take aways: 


improve writting by making it practical with us states that and discuss the results and implications of the analysis in the contest of the thesis

### Tax

federal cooperate tax rate of 21% was 35% until 1993
HIgh: Minnesota 9.8 -, illinois, Alaska 9.4% and new Jersey 9% 
whereas below 5%

To provide a practical analysis using US states with similar tax rates, we can examine the impact of tax policy on green hydrogen projects in specific locations. Let's consider three states with comparable combined effective tax rates: California (28.4%), New Jersey (28.0%), and Minnesota (28.5%) (Tax Foundation, 2023). In these states, the combined federal and state corporate tax rates are approximately 7-8 percentage points higher than the federal-only rate of 21%. This increase in tax burden would reduce the Net Present Value (NPV) of a green hydrogen project by roughly 5-6 million USD, assuming all other factors remain constant. While this impact is less severe than the 15 million USD reduction mentioned in the original text, it still represents a significant financial consideration for project developers. The tax policy effects in these states can be contextualized by comparing them to technical improvements in electrolyzer efficiency. For instance, a 2-3% increase in stack efficiency might yield comparable financial benefits to operating in a state with more favorable tax rates. This comparison underscores the importance of considering both technical and policy factors when evaluating project feasibility. However, it's crucial to note that while tax incentives can improve project economics, they cannot fully compensate for unfavorable electricity costs or power availability. In states like California, where electricity prices are relatively high, the benefits of a competitive tax rate may be outweighed by increased operational expenses. Conversely, Minnesota's lower electricity costs could potentially offset its slightly higher tax rate compared to New Jersey. This analysis demonstrates that while tax policy is an important consideration in green hydrogen project planning, it should be evaluated in conjunction with other critical factors such as electricity costs, renewable energy availability, and local incentives for clean energy projects. Project developers must weigh these various elements to optimize the financial viability of their investments across different states.


We  examined the impact of tax policy on green hydrogen projects under different tax rates.  The high end scenarios reflects  a combined federal and state corporate tax rates at 28% such representing states such as California (28.4%), New Jersey (28.0%), and Minnesota (28.5%). The low end scenario also represents regions with low or no corporate income tax.[ref]  The effect of the in tax burden reduce the Net Present Value (NPV) of a green hydrogen project by roughly 5-6 million USD, assuming all other factors remain constant. The tax penalty is comparable in size to modest improvements in stack efficiency. In other words, a favorable tax abatement can financially offset the operation of a slightly less efficient electrolyzer and vice versa.
 Moreover, this indicates that policy instruments such as investment tax credits or accelerated depreciation improve project economics but cannot compensate for unfavorable power and electricity costs. In states like California, where electricity prices are relatively high, the benefits of a competitive tax rate may be outweighed by increased operational cost. Whereas, Minnesota's lower electricity costs could potentially offset its slightly higher tax rate compared to New Jersey. 

We  examined the impact of tax policy on green hydrogen projects under different tax rates.  The high-end scenario for tax and government policies reflects a combined federal and state corporate tax rate for states such as California (28.4%), New Jersey (28.0%), and Minnesota (28.5%). The low-end scenario includes regions with low or no corporate income tax. The tax burden reduces the Net Present Value (NPV) of a green hydrogen project by roughly 5-6 million USD, assuming all other factors remain constant. The tax penalty is comparable in size to modest improvements in stack efficiency. In other words, a favorable tax abatement can financially offset the operation of a slightly less efficient electrolyzer, and vice versa. Moreover, this suggests that policy instruments such as investment tax credits or accelerated depreciation enhance project economics but cannot compensate for unfavorable electricity tariffs. The advantages of a competitive tax rate may be outweighed by increased operational costs in states with elevated electricity tariffs, such as California. Whereas states like Minnesota, with lower electricity costs, could potentially offset its slightly higher tax rate compared to New Jersey.

We studied how tax policies affect green hydrogen projects under different tax rates. The high-end scenario for taxes and government policies reflects a combined federal and state corporate tax rate for states like California (28.4%), New Jersey (28.0%), and Minnesota (28.5%). The low-end scenario includes regions with low or no corporate income tax. The tax burden cuts the Net Present Value (NPV) of a green hydrogen project by about 5-6 million USD, assuming all other factors stay the same. The tax penalty is similar in effect to small improvements in stack efficiency. In other words, a favorable tax break can offset the costs of running a slightly less efficient electrolyzer, and vice versa. Additionally, this indicates that policy tools like investment tax credits or accelerated depreciation improve project economics but cannot compensate for unfavorable electricity tariffs.

. Increased operational costs in states with high electricity tariffs, such as California, may outweigh the advantages of a competitive tax rate. Whereas states like Minnesota, with lower electricity costs, could potentially offset its slightly higher tax rate compared to New Jersey.

> [!NOTE]
>  explain: no corporate income tax, but it imposes a state gross receipts tax.


> [!danger] 
> no H2 O2 in any diagram. Use subscript
> Tax rate basis is wrong.

Take aways:
that policy instruments such as investment tax credits or accelerated depreciation improve project economics but cannot compensate for unfavorable power and electricity costs.


### Oxygen as a coproduct
oxygen as a coproduct



## Contour plot





Among off-grid options, PV-only systems have the lowest CAPEX but a middling LCOH due to the low capacity factor; wind offers higher utilization but costs more for electricity; PV-wind hybrids find a middle ground. Adding battery storage improves dispatchability but raises LCOH unless electricity-market revenues compensate for the storage cost.



## RE Design basis 
justification speed:

Cut-in speed; birl
prevent turbine blades from spinning at low wiind speeds(curtailment)To reduce bat fatalities









![[newplot.png]]


For PEM hydrogen production, the choice of renewable feedstock is often framed around capacity factor and marginal electricity price.
**PV as a Cost‐Effective Baseline:** Despite its lower capacity factor, PV’s low capital cost makes it the cheapest option for driving the electrolyser in this costing framework.
**Hybridization and Firming Trade-Offs:** Hybridizing PV and wind smooths generation profiles but comes at a 30–40 % capital premium. 
**storage should be reserved for applications requiring 24/7 output rather than pure cost-reduction** 

> [!question] 
> Marginal cost vrs Fixed cost
> fixed costs remain constant regardless of production levels, while marginal costs represent the cost of producing one additional unit of energy
> Fixed costs typically include upfront investments like power plant construction, while marginal costs reflect variable expenses such as fuel, operation, and maintenance.

Developers targeting minimal LCOH should therefore consider PV-centric sites or PPAs first, then layer in wind or storage only if high utilization or firm dispatch is critical to their business case.

> [!question] 
> Quuestion : Why does hybrid not have higer
> Because it is average half of the capacities of both RE systems.


Assumption: we assume no tax on solar system
total installation cost (around 12%).
Analysis does not include tax credits, rebates or any other incentives.

The 30% federal solar tax credit can significantly reduce the net cost of a system.
Many states offer additional tax credits, rebates, or other incentives, further lowering costs.

## Aim 3
---

#### Method

Wind turbine
  The mechanical power output of a wind turbine is governed by the Betz-Lanchester equation

The distribution of wind speeds v is well-modeled by a Weibull probability density

( ω ) is the ratio of the blade tip speed to the wind speed, while (β) adjusts the blades’ orientation relative to the wind flow to optimize efficiency


where \lambda is the scale parameter (the average wind speed), and k is the shape parameter



contour of operating owner and cost of electricity


- PV system
The PV model calculates hourly electricity generation based on location-specific solar irradiance data and array characteristics.





res
S. Khattak et al., Heliyon 2024, 10, e31025.

Y. El Mghouchi et al., Renew. Sustain. Energy Rev. 2016, 56, 87–99.


Results:
-  **Optimal Operating Power (20%-50%):** LCOH drops significantly as utilization increases.
        - The steepest decline in LCOH occurs in this range, highlighting the importance of consistent power supply.
            
    - **High Operating Power (e.g., >50%):** LCOH benefits diminish, with contours flattening.
        - Beyond this point, the cost of electricity becomes the primary driver, outweighing further gains from increased utilization.

## Intermittent Renewables Require Strategic Integration
- **Takeaway:** Relying solely on highly intermittent renewable energy sources (e.g., standalone solar without storage) that lead to low electrolyzer operating power will result in prohibitively high LCOH.
    
- **Implication:** Achieving cost-competitive green hydrogen from renewables necessitates either:
    1. **Hybridization:** Combining complementary renewable sources (e.g., PV and wind) to smooth power delivery.
    2. **Storage Integration:** Utilizing battery or hydrogen storage to increase dispatchability and electrolyzer run-time.
    3. **Grid-Interactive Operation:** Leveraging grid power during renewable lulls, or selling excess power during renewable peaks, to maintain high electrolyzer utilization.





LCOH is both dependent on Cost of electricity and the CF of the operating system.


Battery rated power 5 MW
Duration of Storage 4 hours - hours that the battery takes to charge and discharge at max power level.
Nominal Battery Capacity 20M MWh


PV yield lowest LCOH while Wind give highest cost of LCOH , due to the different in capital cost of the system. [ref] 
Hybridization improve the CF.
Battery does improves the CF but increases the  cost of energy.

[ref] for capital cost

PV lowest marginal cost against high wind powered system due to difference in cost of infrasture.
easy colocation with PVs, land cost for wind powered system

why why?
This is cost of electricity not cost of equiment.

Mckensey style
- Start with a story. for a narrative 
- #SCQA
	Situation, Complication, Question Answer


- Lead with a take away.
- Keep ideas organized
	MECE - Mutually Exclusive collectively Exhaustive

- One Idea per slide.
- Use charts to highlight insights. Title is a full sentence headline
If Graph - point to the take aways

Prompt1. The overall asthetic should resemble slides from top-tier consulting firms like McKinsey or BCG simple, clear and business=class , academic oriented. Avoid any cartoonish icons, drop shadows or color embellishments.

For my scenario analysis. keep main tornado,, use a box shape to give emphasis to each scenario you want to talk about. with icons and notes to summarize basis and effects.