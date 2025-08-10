


5. 1 PEM design validation and parameter sensitivity
 5.2. Univariate sensitivity and scenario analysis
 - PEM design level sensitivity to process metrics
- Centralized vrs distribution model under RE comparison.
	- System-level sensitivity
		Tornado chart showing a univariate sensitivity of LCOH  to key parameters
		Tornado chart showing a univariate sensitivity of NPV to key parameters
	Capital cost of breakdown of energy system configuration
	LCOE and the corresponding LCOH impact for hydrogen production for energy configuration scenarios
5.3 Multivariate sensitivity and uncertainty analysis
Contour of LCOH (\$/kg H₂) versus design capacity (kg H₂ /day) and electricity cost ($/kWh). The white marker denotes the 10 000 kg /day baseline case at $0.07 kWh
fig 5.3.2
The IRR and NPV for distributed  and centralized systems
Contour of LCOH (\$/kg H₂) versus specific energy consumption (kWh /kg H₂) and electricity cost ($/kWh).
5.4 Limitations of the Study
5.5 Future Research Directions

## 5. 1 PEM design validation and parameter sensitivity

Electrolyzer model, efficiency











## 5.2. Univariate sensitivity and scenario analysis


- PEM design level sensitivity to process metrics
Design params and NPV



- Centralized vrs distribution model under RE comparison.
Results fig 5.2.1
LCOH at different plant capacities of 1500kg/day(on-site generation), 10,000kg/day and 50,000kg/day(centralized)
![[fig 5.2.1 LCOH at different plant capacities of 1500kg_day_on-site generation_, 10,000kg_day and 50,000kg_day_centralized_.png]]

Figure 5.2.1 compares the levelized cost of hydrogen (LCOH) and its component breakdown for three plant capacities—1 500 kg day⁻¹ (distributed), 10 000 kg day⁻¹ (baseline), and 50 000 kg day⁻¹ (centralized)—all assuming grid electricity at 0.07 USD kWh⁻¹. We found that economies of scale drive a sharp decline in LCOH between the smallest and mid-scale cases, but yield only marginal benefit beyond 10 000 kg day⁻¹.

At the distributed scale (1 500 kg day⁻¹), the LCOH reaches approximately **8.65 USD kg⁻¹**. Here, electricity feedstock dominates, accounting for roughly 43 % of total cost, followed by fixed OPEX (maintenance, labor, overhead) at 26 %, capital recovery (FCI) at 19 %, utilities and minor variable costs at 5 %, and working-capital charges at 2 %. When we scale to the baseline mid-scale (10 000 kg day⁻¹), LCOH falls by 22 % to **6.75 USD kg⁻¹**, driven by a 30 % reduction in fixed-OPEX per kilogram and a 15 % drop in capital-recovery costs per unit. Electricity remains the single largest component (~53 %), reflecting the continued importance of SEC and tariff structure at larger scale.

Further expansion to a centralized plant (50 000 kg day⁻¹) delivers only a modest additional decline, bringing LCOH to **6.85 USD kg⁻¹**. This slight rebound owes to incremental BoP complexity and pumping loads that grow non-linearly with size, which partially offset the incremental capital-cost savings. Notably, fixed OPEX rebounds to 28 % of the total, and capital recovery climbs to 22 %, while feedstock electricity share dips to 50 %. This plateau in LCOH above 10 000 kg day⁻¹ suggests that the sweet spot for on-site to near-site hydrogen production—balancing plant footprint, BoP complexity, and economies of scale—lies around the mid-scale range.

---
Take 2
#### 5.2.1 Capacity‐Scale Scenario

Figure 5.2.1 compares the levelized cost of hydrogen (LCOH) and its cost‐component breakdown across three plant capacities: a small‐scale “distributed” unit (1 500 kg day⁻¹), our mid‐scale “baseline” reference (10 000 kg day⁻¹), and a large “centralized” plant (50 000 kg day⁻¹). The baseline configuration achieves the lowest LCOH at roughly 6.7 USD kg⁻¹, benefiting from a balanced compromise between capital‐cost dilution and manageable BoP complexity. In contrast, the distributed plant’s high per‐unit capital intensity drives its LCOH above 8.5 USD kg⁻¹, despite only modest feedstock and operating‐cost savings at this small scale. Scaling further to the centralized plant yields diminishing returns: although fixed capital and working‐capital shares decline, the incremental drop in LCOH is marginal (to ~6.9 USD kg⁻¹), reflecting the curvature of the cost‐capacity relationship in (4.7).

Across all three scales, electricity (feedstock) remains the dominant cost driver—accounting for roughly 50 % of LCOH—while fixed capital recovery (FCI) and fixed OPEX together contribute between 25 % (baseline) and 35 % (distributed) of the total. Utility‐related costs (water treatment, stack replacement power draw) and other variable expenses (maintenance consumables, purge handling) each represent only single‐digit percentages of LCOH.

---
Take 3
### ### 5.2 Univariate Sensitivity and Scenario Analysis

The first lens through which we examine scale effects is a direct comparison of the levelized cost of hydrogen for three discrete plant capacities: a 1 500 kg H₂ day⁻¹ distributed unit, our 10 000 kg day⁻¹ baseline, and a 50 000 kg day⁻¹ centralized facility. Figure 5.2 disaggregates each LCOH into its principal cost categories—fixed operating expenditure, electricity feedstock, utilities, other variable costs, fixed-capital investment (FCI) recovery, and working capital.

Moving from the distributed to the mid-scale plant, we observe a pronounced decline in levelized cost, from roughly 8.6 USD kg⁻¹ to 6.6 USD kg⁻¹. Two drivers account for most of this 23 % reduction. First, the economies of scale significantly reduce the cost per kilogram contribution of fixed OPEX and FCI: the larger plant spreads labor, administration, and capital recovery over a production volume nearly seven times greater, compressing those bars in the stacked profile. Second, the power-conditioning and water-treatment components that dominate balance-of-plant costs exhibit sub-linear cost scaling (Section 4.4.1), further lowering capital recovery per unit of hydrogen.

When capacity is expanded an additional five-fold to 50 000 kg day⁻¹, the LCOH drops only marginally and, in our model, bottoms out at 6.4–6.9 USD kg⁻¹. While fixed costs continue to fall on a per-kilogram basis, the feedstock electricity bar, already the single largest contributor, grows in absolute height because total power demand increases linearly with output. At the assumed tariff of 0.07 USD kWh⁻¹, electricity represents roughly 55 % of the centralized LCOH, swallowing most of the savings realized elsewhere. The slight uptick between the baseline and centralized configurations (6.6 → 6.8 USD kg⁻¹), therefore, reflects a tipping point at which diminishing scale advantages in CAPEX and labor are counter-balanced by the electrical energy consumption.

Several insights for project developers can be inferred from this scenario analysis. First, right-sizing a plant for a given offtake avoids both the high unit costs of undersized assets and the electricity-dominated economics of mega-scale installations operating at today's power prices. Second, feedstock electricity price volatility matters more than any other single parameter once capacities exceed roughly 10,000 kg day⁻¹; subsequent tornado-diagram results (Section 5.2.2) will confirm this dominance quantitatively. Finally, the modest cost penalty of the distributed case underscores its potential niche wherever transport compression, permitting, or resiliency considerations outweigh pure cost minimization.

---

- System-level sensitivity
results fig 5.2.2
Tornado chart showing a univariate sensitivity of LCOH  to key parameters
![[fig 5.2.2 Tornado chart showing a univariate sensitivity of LCOH  to key parameters.png]]


The tornado analysis makes clear that our LCOH projections are highly contingent on both current market realities and forward‐looking technical targets. 
In the “high‐cost” scenario: where electricity is priced at 0.15 USD kWh⁻¹, installed CAPEX hovers near 1 500 USD kW⁻¹, SEC at 55 kWh kg⁻¹, and O&M peaks (≈ 8 % of CAPEX), the LCOH soars toward 9.5 USD kg⁻¹. Under these conditions, green hydrogen risk remains elevated and concessional financing or premium offtake contracts would likely be required to achieve acceptable returns. Conversely, the “low‐cost” scenario, where power can be procured at 0.03 USD kWh⁻¹ during renewable surpluses, CAPEX falls to DOE‐target levels (≈ 250USD kW⁻¹), SEC achieves the 45 kWh kg⁻¹ R&D goal, and O&M is optimized to 5 % of CAPEX, drives LCOH down below 5 USD kg⁻¹. 

Between these extremes, our base assumptions (0.07 USD kWh⁻¹, 1 114 USD kW⁻¹ installed CAPEX, 54.3 kWh kg⁻¹ SEC, 6 % O&M) yield an LCOH of 7.05 USD kg⁻¹. The 4.8 USD kg⁻¹ span resulting from electricity‐price variation shorts the 1.7 USD kg⁻¹ swing from CAPEX uncertainty and the sub‐0.5 USD kg⁻¹ shifts attributable to efficiency or O&M improvements. In practical terms, this means that while manufacturing scale‐up and incremental stack efficiency gains are both worthwhile R&D avenues, securing low‐cost, firm renewable power—or unlocking time‐of‐use arbitrage opportunities—offers the single greatest lever for cost reduction.

Looking ahead, even modest targets could materially reshape economics. Achieving a mid‐range CAPEX of 1 000 USD kW⁻¹ and an SEC of 50 kWh kg⁻¹ while maintaining grid‐average power rates would lower LCOH to the mid‐5 USD kg⁻¹ range, a level many analysts consider the tipping point for broad industrial uptake. Similarly, monetizing oxygen at just 0.10 USD kg⁻¹ becomes meaningful only when coupled with low power costs and tight CAPEX control, illustrating that by‐product valorization is a nice-to-have rather than a core enabler.


---
that our most optimistic and pessimistic scenarios for key inputs drive dramatically different hydrogen‐cost outcomes—ranging from a low of roughly 4.7 USD kg⁻¹ under the most favorable conditions to nearly 9.5 USD kg⁻¹

During midday solar surpluses or via long-term low-cost PPAs, can halve the LCOH relative to relying on peak-time grid rates near 0.15 USD kWh⁻¹. This underscores the strategic value of co-locating electrolyzers with cheap renewable generation or pursuing sub-hourly market participation.

Similarly, stack and balance-of-plant capital costs between 250 and 1 500 USD kW⁻¹ create a swing of about 1.7 USD kg⁻¹: achieving the DOE’s 250 USD kW⁻¹ manufacturing target would, all else equal, reduce LCOH by roughly 0.5 USD kg⁻¹ versus today’s high-volume bids. Meanwhile, improvements in specific energy consumption (driving SEC down from 55 to 45 kWh kg⁻¹ in future low-overpotential membrane and catalyst designs) can potentially lower LCOH by nearly 0.4 USD kg⁻¹.  This infers that catalyst and membrane R&D remains an important lever for incremental cost savings.

By contrast, variations in water-treatment costs, routine O&M, and even potential oxygen sales have comparatively minor effects. They influence LCOH by only a few cents per kilogram, suggesting these parameters are unlikely to be major cost drivers.

---
The span of each bar in Figure 5.2.2 can be read as a thought-experiment: what would the Levelized cost of hydrogen if a single parameter were to reflect a plausible “optimistic” future and a conservative “present-day” or “legacy” value while everything else remained unchanged? Taken together, these one-at-a-time excursions trace out a band of economic possibilities that is anchored at 7.05 USD kg⁻¹ for our 10 000 kg day⁻¹ baseline and broadens to 4.7–9.5 USD kg⁻¹ across the envelope of scenarios.

Low-power-price scenario (0.03 USD kWh⁻¹) reflects curtailed-renewable or “overbuild-and-spill” regimes now emerging in regions with high solar penetration (e.g., California’s midday surplus) or in markets where electrolyzers are co-located behind the meter with dedicated PV and wind. [ref] In such settings, the plant can procure electricity below the long-run marginal cost of the grid, compressing LCOH to ≈ 4.7 USD kg⁻¹ in our model. Crucially, this lower bound is already within reach of blue hydrogen under mid-range carbon-capture costs; hence projects pursuing a pure-renewables arbitrage strategy can be competitive today without further technology breakthroughs [ref]. Conversely, a merchant-grid electrolyzer in a peaking-price region, from a 24/7 renewable energy certificates could face tariffs at or above 0.12 USD kWh⁻¹, driving LCOH to almost 9.5 USD kg⁻¹. That price sits far from gray hydrogen from SMR, indicating that electricity cost volatility is the primary threat to project economics whenever low-cost PPAs or behind-the-meter designs are unavailable. Even modest reductions in the average electricity tariff by a point or two of levelized cost of electricity (LCOE) translate almost one-for-one into hydrogen cost savings. This will validate business models that prioritizes ultra-low-cost, high-capacity-factor power procurement over incremental efficiency gains.


Capital-cost trajectory (250 USD kW⁻¹) scenarios approximate an optimistic 2030 DOE target that assumes serial production of large-format stacks, thin-film catalyst deposition, and integrated MEA [ref]. Achieving this goal could lower LCOH by ~1.8 USD kg⁻¹ relative to today’s small-lot quotes of 1 500 USD kW⁻¹ about the same magnitude as a 15 % swing in electricity cost. Hence manufacturing scale-up offers the second most influential lever after cheap power. Capital cost holds lesser effect than electricity cost but larger than any operational cost. Future cost optimization breakthroughs in stack manufacture will cut into hydrogen prices more decisively than incremental gains in water, labour, or utility efficiency.

Fixed-O&M optimization (5 – 8 % CAPEX yr⁻¹) 
Implementing predictive maintenance, service contracts, and remote diagnostics  could potentially trim annual outlays by almost 2 M USD for a 20-MW plant. The LCOH benefit (± 0.2 USD kg⁻¹) is modest compared with power or CAPEX swings but remains strategically valuable because these savings accrue annually and compound under a discounted-cash-flow lens. Tightening preventive-maintenance schedules and negotiating leaner service contracts reduce the fixed-O&M burden to 6.84 USD kg⁻¹ on the low side. Higher maintenance and operational cost toward 8 % of CAPEX nudges can inflate cost up to **7.44 USD kg⁻¹**. These levers matter for competitiveness among projects drawing from similar power pools, yet they remain second-order compared with the electricity tariff or plant CAPEX.

**Stack efficiency (45 – 55 kWh kg⁻¹).** The 45 kWh kg⁻¹ target represents advanced membrane-electrode assemblies with sub-500 mV cell voltages and improved ohmic conductance. The benefit scales only with the electricity share of cost. Achieving this performance saves roughly 0.4 USD kg⁻¹ off LCOH. Thus, half the gain from hitting DOE's CAPEX target for PEM electrolysers while simultaneously reducing cooling load and BoP sizing. Because efficiency gains reduce both variable electricity cost and some capital line items, they remain a worthwhile R&D focus even in low-power-price regions.

On the scenario for utility and non-energy feedstocks, tripling water and ancillary utility charges affect the LCOH by less than ± 0.15 USD kg⁻¹, It confirms the conventional wisdom that deionized-water consumption is economically immaterial (≈ 2 % of total variable cost). Nevertheless, in arid regions or microgrid deployments where water may be trucked in, these costs could escalate and warrant site-specific analysis.


**By-product oxygen credit.** Even at the upper end of industrial gas price ranges (0.17 USD kg⁻¹ O₂), the revenue offsets less than 0.05 USD kg⁻¹ of hydrogen cost at 10 000 kg H₂ day⁻¹. Only very large facilities (> 200 t day⁻¹) integrated with steel or chemical plants that consume oxygen in situ are likely to capture meaningful credits; otherwise, venting remains the simplest strategy.
Even a generous monetisation of vent oxygen 0.17 USD kg⁻¹ in industrial gas markets would save only a few cents per kilogram of hydrogen at today’s scales. These findings justify our modelling choice to exclude oxygen credit from the baseline and to treat water price as a fixed, low-risk cost. 

**Tax-rate variability (21 – 33 %).** Because depreciation shields the early years of a project, the effective tax sensitivity is muted (± 0.1 USD kg⁻¹) once cash flows are discounted. Nonetheless, siting in low-tax jurisdictions—particularly those offering investment or production tax credits—still enhances NPV and IRR even when LCOH moves only slightly.

Conversely, if capital dives to DOE’s 250 USD kW⁻¹ target while mid-continent electricity stabilises near 0.05 USD kWh⁻¹, LCOH would converge near 5.3 USD kg⁻¹—below the 5.5–6 USD kg⁻¹ range many analysts cite as the parity threshold with blue hydrogen under a moderate carbon price. Those numbers set clear technical targets: achieve ≤45 kWh kg⁻¹ SEC, ≤500 USD kW⁻¹ installed cost, and a power tariff of ≤0.05 USD kWh⁻¹, and green hydrogen becomes competitive in large swaths of the North American market even without extraordinary policy support.

---

results fig 5.2.3
Tornado chart showing a univariate sensitivity of NPV to key parameters
![[fig 5.2.3 Tornado chart showing a univariate sensitivity of NPV to key parameters.png]]

**5.2.3 Profitability Levers: Net-Present-Value Sensitivity**

While the preceding analysis isolates how individual parameters influence the levelized cost of hydrogen, project developers and investors ultimately care about value creation. Figure 5.2.3, therefore, reorders the same seven levers according to their impact on the baseline net present value of 77.6 million USD. Once again, electricity price emerges as the most crucial factor: at a tariff of 0.03 USD kWh⁻¹, the project's cumulative, discounted cash surplus increases to 125 million USD, whereas a punitive 0.12 USD kWh⁻¹ power cost all but erases profitability, shrinking NPV to 27 million USD. In other words, one cent per kilowatt-hour translates to roughly 12 million USD of project value over twenty years.

Efficiency gains matter significantly, as they can temper electricity consumption and improve the project's profitability. Improving specific energy consumption from 55 to 45 kWh kg⁻¹ raises NPV by roughly eight million dollars, a respectable figure that underscores the potential for improvement. However, it's important to note that this is still half the size of the power-price lever. Fixed O&M, utility water, and non-energy consumables shift NPV by no more than ±7 million USD across the realistic bounds we examined, confirming their tertiary status in project economics.

Tax policy is a significant factor that sits between the technical and operational levers. Moving from jurisdictions that impose only the 21 % federal rate to states with an effective 36 % combined rate trims NPV by roughly 15 million USD, a penalty similar in scale to modest improvements in stack efficiency. In other words, a favorable tax abatement can compensate financially for operating a slightly less efficient electrolyzer and vice-versa. Moreover, it implies that policy instruments such as investment tax credits or accelerated depreciation enhance project economics but cannot compensate for unfavorable power and electricity costs.

Even at the high end of industrial gas pricing (0.028 USD kg⁻¹ O₂), the additional revenue nudges NPV upward by less than five million dollars. Only at very large scales where oxygen volumes rival those of a dedicated air-separation unit would by-product valorization materially shift the investment case. That finding cautions against over-reliance on oxygen credits in pro-forma statements unless a firm offtake agreement is in place.

Collectively, the LCOH and NPV tornado analyses converge on a consistent hierarchy of sensitivities: electricity cost first, followed by capital cost, with efficiency, O&M, taxation, and ancillary streams trailing well behind. From an informed standpoint, the results suggest that early-stage project screening should focus on long-term power price commitments and credible CAPEX estimates; only once those anchors are favorable do incremental gains in efficiency or fiscal optimization meaningfully move the financial sustainability.


- Wind-PV-Grid comparison
results fig 5.2.4
Capital cost of breakdown of energy system configuration
![[fig 5.2.4 Capital cost of breakdown of energy system configuration.png]]


 LCOE and the corresponding LCOH impact for hydrogen production for energy configuration scenarios
![[results fig 5.2.5  LCOE and the corresponding LCOH impact for hydrogen production for energy configuration scenarios.png]]



Location comparison

## 5.3 Multivariate sensitivity and uncertainty analysis

Contour 
results fig 5.3.1 
 Contour of LCOH (\$/kg H₂) versus design capacity (kg H₂ /day) and electricity cost ($/kWh). The white marker denotes the 10 000 kg /day baseline case at $0.07 kWh
![[fig 5.3.1 Contour of LCOH __$_kg H₂_ versus design capacity _kg H₂ _day_ and electricity cost _$_kWh_. The white marker denotes the 10 000 kg _day baseline case at $0.07 kWh.png]]

![[results fig 5.3.1.png]]
       
![[fig 5.3.1 LCOE and Plant size to  LCOH.png]]

fig 5.3.2
The IRR and NPV for distributed  and centralized systems

![[fig 5.3.2 IRR and NPV on design capacity.png]]

|     | Distributed    | Baseline        | Centralised      |
| --- | -------------- | --------------- | ---------------- |
| IRR | 0.136          | 0.320           | 0.380            |
| NPV | $ 6,120,530.58 | $ 84,330,199.17 | $ 409,929,882.43 |

Uncertainty analysis
Contour of LCOH (\$/kg H₂) versus specific energy consumption (kWh /kg H₂) and electricity cost ($/kWh).
fig 5.3.3



![[fig 5.3.3 LCOH , SEC, LCOH.png]]


LCOE vrs CF to electrolyser perf


Montecarlo simulation

NPV and LCOH resuls

Normal distribuition
NPV freq
## 5.4 Limitations of the Study

Constraints and limitations encountered.

## 5.5 Future Research Directions


Formulate and solve a multi-objective optimization problem minimizing both CAPEX and specific energy consumption, while maximizing efficiency and membrane durability, under realistic operating constraints.

> **Figure 4: Schematic of the multi‐objective optimization workflow, highlighting decision variables, constraints, and the Pareto front generation.**

![[image-54.png]]


**Task 2.3 {future work}:**  
**To Evaluate the impact of cost-reduction levers**, including material substitutions and manufacturing scale-up.


4.3.2 Task 3.2 {future work} – Dynamic Optimization of Renewable-Electrolyzer Configurations
The renewable energy(RE) potential vary across geographical regions for different energy systems.@maclaurinRenewableEnergyPotential2021  

4.3.3 Task 3.3 {future work} – Geospatial, Hourly-Resolved LCOH Mapping with Policy and Emissions Layers









![[_ LCOH at different plant capacities.png|477x285]]

: LCOH at different plant capacities of 1500kg/day(distributed), 10,000kg/day and 50,000kg/day(centralized).


