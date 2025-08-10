

- [ ] Cost model for @due(2025-04-22)
- [ ] performance model @due(2025-04-21)
- [ ] Distribution function for PV system parameters
	- [ ] distribution function for PV, for Wind
- [ ] Writing on the energy system

[[Solar energy model]]
[[Wind energy]]
[[dpR Energy system research]]


More Data sources
Taylor, M., 2023. _Renewable Power Generation Cost Trends in 2022_, International Renewable Energy Agency. United Arab Emirates. Retrieved from [https://coilink.org/20.500.12592/mpg4mbb](https://coilink.org/20.500.12592/mpg4mbb) on 22 Apr 2025. [COI: 20.500.12592/mpg4mbb](https://coilink.org/20.500.12592/mpg4mbb).


**2.4.1 Temporal Variability in Renewable Energy Supply**

Renewable energy sources such as solar and wind exhibit inherent variability on both diurnal and seasonal timescales. Solar photovoltaic (PV) generation peaks during midday hours and varies with seasonal daylight availability, while wind energy can be more pronounced during nighttime and winter months. These fluctuations result in variable electricity availability, directly impacting the operational capacity of grid-connected PEM electrolyzers.​

PEM electrolyzers are well-suited to accommodate such variability due to their rapid response times and flexible operating ranges. However, operating electrolyzers under fluctuating power inputs can lead to suboptimal efficiency and increased degradation rates, thereby affecting the levelized cost of hydrogen (LCOH). Studies have shown that dynamic operation, while beneficial for grid integration, necessitates careful management to balance efficiency losses and equipment longevity .​[Aalto University's research portal](https://research.aalto.fi/files/126441611/1-s2.0-S1364032123007414-main.pdf?utm)[Aalto University's research portal+3Wikipedia+3arXiv+3](https://en.wikipedia.org/wiki/Hydrogen_economy?utm)

**2.4.2 Electricity Pricing and Economic Implications**

Electricity costs constitute a significant portion of the LCOH for hydrogen production via electrolysis. Time-of-use electricity pricing, which reflects the variability in electricity demand and supply, can influence the operational strategy of PEM electrolyzers. Operating electrolyzers during periods of low electricity prices—often coinciding with high renewable generation—can reduce production costs. Conversely, high electricity prices during peak demand periods can render hydrogen production economically unviable.​[arXiv+](https://arxiv.org/abs/2404.06748?utm)

Integrating PEM electrolyzers with energy management systems that respond to real-time electricity pricing can optimize operational schedules, enhancing profitability. Moreover, coupling electrolyzers with energy storage solutions can buffer against electricity price volatility, allowing for more consistent hydrogen production .​[EPRI Rest Service](https://restservice.epri.com/publicdownload/000000003002025738/0/Product?utm)

**2.4.3 System-Level Optimization Strategies**

To mitigate the challenges posed by energy system variability, several optimization strategies can be employed:​
- **Hybrid Energy Integration**: Combining multiple renewable energy sources, such as solar and wind, can smooth out supply variability, providing a more stable power input for electrolyzers .​
- **Advanced Control Algorithms**: Implementing predictive control algorithms that forecast renewable generation and electricity prices can optimize electrolyzer operation schedules, balancing production efficiency and cost .​
- **Modular Electrolyzer Design**: Utilizing modular electrolyzer systems allows for flexible scaling of hydrogen production in response to available electricity, enhancing adaptability to fluctuating energy inputs .​[arXiv](https://arxiv.org/abs/2402.05148?utm_source=chatgpt.com)

**2.4.4 Implications for Hydrogen Production Cost and Profitability**

The interplay between energy system variability and PEM electrolyzer operation significantly influences the LCOH. Dynamic operation aligned with periods of low electricity prices can reduce production costs, but may also accelerate equipment degradation, necessitating a trade-off analysis. System-level optimization that considers energy supply patterns, electricity pricing, and electrolyzer performance is essential to enhance the economic viability of green hydrogen production.​[Hydrogen Program+](https://www.hydrogen.energy.gov/docs/hydrogenprogramlibraries/pdfs/24005-clean-hydrogen-production-cost-pem-electrolyzer.pdf?utm_source=chatgpt.com)

Future research should focus on developing integrated models that simulate the complex interactions between energy systems and electrolyzer operations, incorporating factors such as renewable generation forecasts, electricity market dynamics, and equipment degradation mechanisms. Such models can inform the design of robust operational strategies that maximize profitability while ensuring sustainable hydrogen production.​

_References:_

- Sayed-Ahmed, H., et al. (2023). Dynamic operation of proton exchange membrane electrolyzers: A critical review. _Renewable and Sustainable Energy Reviews_, 189, 113883.​[Aalto University's research portal](https://research.aalto.fi/files/126441611/1-s2.0-S1364032123007414-main.pdf?utm_source=chatgpt.com)
    
- Schofield, L., et al. (2024). Dynamic Optimization of Proton Exchange Membrane Water Electrolyzers Considering Usage-Based Degradation. _arXiv preprint arXiv:2405.06766_.​[arXiv](https://arxiv.org/abs/2405.06766?utm_source=chatgpt.com)
    
- Henkel, V., et al. (2024). Combination of Site-Wide and Real-Time Optimization for the Control of Systems of Electrolyzers. _arXiv preprint arXiv:2404.06748_.​[arXiv](https://arxiv.org/abs/2404.06748?utm_source=chatgpt.com)
    
- Henkel, V., et al. (2024). Cost Optimized Scheduling in Modular Electrolysis Plants. _arXiv preprint arXiv:2402.05148_.​[arXiv](https://arxiv.org/abs/2402.05148?utm_source=chatgpt.com)
    
- IRENA. (2020). Green hydrogen cost reduction: Scaling up electrolysers to meet the 1.5°C climate goal. _International Renewable Energy Agency_.​[Wikipedia+2Wikipedia+2IRENA+2](https://en.wikipedia.org/wiki/Hydrogen_economy?utm_source=chatgpt.com)




 ==The grid's capacity factor is less dependent on time of day, but can be influenced by peak demand periods==.


solar
Solar PV (Photovoltaic)
- **Daylight Hours:**
        Solar PV systems produce electricity primarily during daylight hours. The capacity factor is highest when the sun is at its zenith (around midday) and decreases as the sun moves towards the horizon in the morning and evening.
- **Peak Demand:**
        Solar PV generation often aligns with peak electricity demand, typically in the late afternoon/early evening.
 - **Cloud Cover:**
        Cloud cover can significantly impact solar PV generation, leading to reduced capacity factors during cloudy periods.


Wind Power
- **Variable Wind Speeds:**
        Wind power generation is heavily reliant on wind speed and direction. Wind speeds can fluctuate throughout the day, leading to variable capacity factors.
  - **Time of Day:**
        While wind patterns can vary seasonally, wind speeds are generally not strongly tied to the time of day.
 - **Turbine Availability:**
        Maintenance, repair, and downtime can also affect the capacity factor of wind turbines, regardless of the time of day.


https://www.google.com/url?sa=i&url=http%3A%2F%2Feuanmearns.com%2Fsolar-pv-capacity-factors-in-the-us-the-eia-data%2F&psig=AOvVaw2unPu4P6_MAaBtwNLCrfYW&ust=1744630088504000&source=images&cd=vfe&opi=89978449&ved=0CBcQjhxqFwoTCLDMqO_01IwDFQAAAAAdAAAAABAE

![[Research notes/Workbook/attachments/image.png]]


### 📊 Seasonal Variability of Capacity Factors

**Solar PV**: Solar capacity factors peak during summer months due to longer daylight hours and higher solar irradiance. In Europe, for instance, solar capacity factors are highest in June and July.​

**Wind Power**: Wind capacity factors generally peak in winter months, attributed to stronger and more consistent wind patterns. This seasonal complementarity between solar and wind can help balance energy supply throughout the year.​[ResearchGate](https://www.researchgate.net/figure/Seasonal-cycle-of-the-capacity-factors-for-wind-and-PV-for-Europe-otherwise-same-as-Fig_fig4_334171681?utm_source=chatgpt.com)[Royal Meteorological Society (RMetS)](https://rmets.onlinelibrary.wiley.com/doi/10.1002/met.2093?utm_source=chatgpt.com)

A study analyzing the seasonal cycles of wind and PV capacity factors across Europe illustrates this complementarity, showing how combined wind and solar resources can lead to a more stable energy supply.​[ResearchGate](https://www.researchgate.net/figure/Seasonal-cycle-of-the-capacity-factors-for-wind-and-PV-for-Europe-otherwise-same-as-Fig_fig4_334171681?utm_source=chatgpt.com)

### Diurnal (Hourly) Variability

**Solar PV**: Solar generation follows a predictable daily pattern, ramping up in the morning, peaking around midday, and declining in the evening. This pattern aligns with daylight availability.​

**Wind Power**: Wind generation is more variable on an hourly basis and can differ by location. In some regions, wind speeds—and thus generation—are higher at night, while in others, they may peak during the day.​

_Visualization_: An analysis of hourly capacity factors for wind and solar in South Africa demonstrates these patterns, highlighting the variability and potential for complementarity between the two sources.​[ResearchGate](https://www.researchgate.net/figure/High-season-wind-hourly-average-capacity-factors-and-the-national-demand-curve-including_fig4_321192910?utm_source=chatgpt.com)
### Combined Wind and Solar Profiles

Integrating wind and solar energy sources can mitigate the variability inherent in each. For example, when solar generation decreases in the evening, wind generation may increase, depending on regional wind patterns.​

_Visualization_: A study on the variability of wind power generation across different U.S. regions shows how combining wind and solar resources can lead to a more balanced and reliable energy supply.

![[Research notes/Workbook/attachments/image-1.png]]

![[Research notes/Workbook/attachments/image-2.png]]


![[Research notes/Workbook/attachments/image-3.png]]

### Data Sources for Further Exploration

To delve deeper into capacity factors and their variability, consider exploring the following resources:

- **Renewables.ninja**: Provides simulated hourly data for wind and solar generation globally.​
- **Open Power System Data**: Offers datasets on European power systems, including generation and load profiles.​[Wikipedia+1arXiv+1](https://en.wikipedia.org/wiki/Open_energy_system_databases?utm_source=chatgpt.com)
- **Global Solar Atlas**: An interactive tool for assessing solar resource potential worldwide.​[ResearchGate+6Wikipedia+6arXiv+6](https://en.wikipedia.org/wiki/Global_Solar_Atlas?utm_source=chatgpt.com)
- **Global Wind Atlas**: Provides high-resolution data on wind resources globally.​[ScienceDirect+4Wikipedia+4Wikipedia+4](https://en.wikipedia.org/wiki/Global_Solar_Atlas?utm_source=chatgpt.com)




# Electricity demand and variability in the us

![[Research notes/Workbook/attachments/image-4.png]]


![[Research notes/Workbook/attachments/image-5.png]]


![[image-6.png]]


### Electricity Demand Patterns

**Daily Variations:**

- **Summer:** Electricity demand typically peaks in the late afternoon due to increased use of air conditioning.​
    
- **Winter:** Demand often has two peaks—one in the morning and another in the evening—as people heat their homes during colder periods.​
    
- **Spring and Fall:** These seasons generally see lower and more stable electricity demand.​
    

**Seasonal Variations:**

- Overall, electricity consumption is highest during the summer months, primarily due to cooling needs. ​[EIA](https://www.eia.gov/todayinenergy/detail.php?id=42915&utm_source=chatgpt.com)
    

---

### 💵 Electricity Pricing Patterns

**Time-of-Use (TOU) Pricing:**

- Electricity prices are often higher during peak demand hours (afternoon and early evening) and lower during off-peak hours (late night and early morning).​
    
- TOU programs allow consumers to reduce their bills by shifting usage to off-peak times. ​[Callmepower+6PAPowerSwitch+6The US Sun+6](https://www.papowerswitch.com/understanding-energy/about-rates-terms/time-of-use/?utm_source=chatgpt.com)
    

**Seasonal Pricing:**

- Electricity rates tend to be higher in summer and winter due to increased demand for cooling and heating, respectively.​[Constellation](https://www.constellation.com/energy-101/when-are-electricity-rates-lowest.html?utm_source=chatgpt.com)
    
- Rates are generally lower in spring and fall when demand is reduced.
    
    [Constellation](https://www.constellation.com/energy-101/when-are-electricity-rates-lowest.html?utm_source=chatgpt.com)
    
    ​
    

---

### 📈 Visualizing the Patterns

To better understand these variations, consider the following visualizations:

1. **Hourly Electricity Consumption by Season:**
    _Source: U.S. Energy Information Administration_
    
2. **Seasonal Average Electricity Consumption:**
    ![Seasonal average electricity consumption (kWh) by the hours of the weekdays and weekends](https://www.researchgate.net/profile/Gianluca-Trotta/publication/344192633/figure/fig1/AS:936401204551680@1600603063137/Seasonal-average-electricity-consumption-kWh-by-the-hours-of-the-weekdays-and-weekends.png)
    
    _Source: ResearchGate_
    
3. **Impact of Solar on Hourly Demand in New England:**
    
    _Source: U.S. Energy Information Administration_



#question_based_learning

# Capacity factor

## what is the capacity factor for mixed energy RE sys
#weighted_average


When mixing renewable energy (RE) systems with different capacity factors (CF), the **total system capacity factor** is calculated as a **weighted average** based on each source's installed capacity. Here's how to compute it:

## Formula for Total Capacity Factor

$$\text{Total CF}=\frac{∑(Capacity_i×CFi)}{∑Capacity_i}$$

Where:
- **Capacityᵢ** = Installed capacity of each RE source (e.g., MW)
- **CFᵢ** = Capacity factor of each RE source (decimal, e.g., 0.35 for 35%).
    

## Example Calculation

## Applications

- For a **solar-wind hybrid plant** with 80 MW solar (25% CF) and 120 MW wind (40% CF):
    
    Total CF = $\frac{(80 \times 0.25) + (120 \times 0.40)}{200} = \frac{20 + 48}{200} = 34\%$.
- For **solar + storage** (100 MW solar, 25% CF; 30 MW battery with 90% efficiency):  
    Effective CF ≈ 25% × 1.3 = **32.5%** (assuming storage offsets 30% losses).

## Industry Benchmarks

|System Mix|Typical Total CF Range|
|---|---|
|Solar + Wind|25–45%|
|Wind + Hydro|35–60%|
|Solar + Wind + Storage|30–50%|
- Matches methodologies used by NREL, EIA, and grid operators for hybrid systems[1](https://www.solisrenewables.com/blog/what-is-capacity-factor)[7](https://www.pnas.org/doi/10.1073/pnas.2205429119)[9](https://www.e-education.psu.edu/emsc297/node/649).
    

For multi-source systems, always prioritize granular CF data for each component



## **Key Sources and Findings**

- **NREL (2023):** Adding batteries to PV-wind systems can raise plant-level capacity factors to 60–80% or more, depending on battery size and system configuration[2](https://www.nrel.gov/docs/fy23osti/81902.pdf).
    
- **NREL ATB (2021):** Standalone battery CF is limited by storage duration (e.g., 16.7% for 4-hour batteries)[1](https://atb.nrel.gov/electricity/2021/utility-scale_battery_storage).
    
- **EIA:** Capacity factor is always the actual energy delivered divided by the maximum possible energy if the system ran at full power all year[8](https://www.eia.gov/todayinenergy/detail.php?id=42995).

## **Summary Table**

|System Type|Typical Capacity Factor (CF)|Source|
|---|---|---|
|Standalone Solar|15–25%|[2](https://www.nrel.gov/docs/fy23osti/81902.pdf)[7](https://aziz.seas.harvard.edu/files/newaziz/files/mja212_0.pdf)|
|Standalone Wind|30–45%|[2](https://www.nrel.gov/docs/fy23osti/81902.pdf)[7](https://aziz.seas.harvard.edu/files/newaziz/files/mja212_0.pdf)|
|Standalone Battery|8–17% (2–4 hr duration)|[1](https://atb.nrel.gov/electricity/2021/utility-scale_battery_storage)|
|PV-Wind-Battery|60–80%+ (with sufficient storage)|[2](https://www.nrel.gov/docs/fy23osti/81902.pdf)|

## What of RE with storage capacity

 **Formula for Hybrid System Capacity Factor with Storage**  
The effective (or “plant-level”) capacity factor for a hybrid system including storage can be approximated as:

$$\text{Total } \mathrm{CF}_{\text{hybrid}} = \frac{\text{Total annual energy delivered (incl. storage discharge)}}{\text{Installed hybrid system capacity} \times 8760}$$

- The numerator includes all energy delivered to the grid, whether directly from renewables or discharged from the battery.
    
- The denominator is the total installed capacity of the hybrid system (often the sum of the generator and battery inverter capacities, depending on configuration).

**Battery Storage’s Own Capacity Factor**

- Standalone battery storage has a theoretical maximum CF determined by its duration:
      - For a 4-hour battery: 4/24=16.7%[1](https://atb.nrel.gov/electricity/2021/utility-scale_battery_storage)
    - For a 2-hour battery: 2/24=8.3%[1](https://atb.nrel.gov/electricity/2021/utility-scale_battery_storage)
        
- In hybrid systems, batteries are often charged from renewables and discharged to maximize grid value, so the effective CF of the plant can be much higher.




To calculate the **capacity factor (CF) of a hybrid system** with PV, wind, and battery storage,each with different capacities and capacity factors,

you need to account for:

- The annual energy produced by each generator (PV, wind)
- The energy shifted and delivered by the battery (which depends on battery round-trip efficiency and operational strategy)
- The total installed (nameplate) capacity of the hybrid system
    


## **1. Basic Capacity Factor Formula**

For any power system:

$$\mathrm{CF} = \frac{\text{Annual Energy Output (kWh)}}{\text{Nameplate Capacity (kW)} \times 8760}$$

[4](https://samrepo.nrelcloud.org/help/mtp_capacity_factor.html)

## **2. Annual Energy Output for Each Component**

- **PV Annual Energy:**
	$E_{PV} = C_{PV} \times \mathrm{CF}_{PV} \times 8760$

- **Wind Annual Energy:**
	$E_{Wind} = C_{Wind} \times \mathrm{CF}_{Wind} \times 8760$

- **Battery Net Discharge Energy:**
	If the battery is charged only from on-site renewables, the net energy delivered to the grid is:
	$E_{Batt, net} = \text{Total annual battery discharge to grid} \times \eta_{batt}$

where $η_{batt}$ is the round-trip efficiency (typically 0.85–0.90)[5](https://aziz.seas.harvard.edu/files/newaziz/files/mja212_0.pdf)[2](https://atb.nrel.gov/electricity/2021/utility-scale_battery_storage).
    

## **3. Total Hybrid System Annual Output**


$E_{\text{Hybrid, annual}} = E_{\text{PV, direct}} + E_{\text{Wind, direct}} + E_{\text{Batt, net}}$

- $E_{\text{PV, direct}}$ and $E_{\text{Wind, direct}}$ are the portions of PV and wind generation sent directly to the grid (not stored).

- $E_{\text{Batt, net}}$ is the net battery output to the grid (after accounting for storage losses).


## **4. Hybrid System Nameplate Capacity**

The system nameplate capacity ($C_{Hybrid}$) is typically the sum of the inverter-limited outputs of PV, wind, and battery, or the maximum allowed grid export at any time (sometimes set by the point of interconnection)[1](https://www.nrel.gov/docs/fy23osti/81902.pdf)[6](https://orbit.dtu.dk/files/276242430/Component_Sizing_of_utility_scale_hybrid_power_plant.pdf).

$C_{\text{Hybrid}} = \text{Grid export limit (MW)}$
or
$C_{\text{Hybrid}} = C_{PV} + C_{Wind} + C_{\text{Batt, inverter}}$

(Use the appropriate value for your system design.)

## **5. Hybrid System Capacity Factor Formula**

$$\mathrm{CF}_{\text{Hybrid}} = \frac{E_{\text{Hybrid, annual}}}{C_{\text{Hybrid}} \times 8760}$$

Where:

- $E_{Hybrid, annual}$, annual includes all energy delivered to the grid (direct from PV/wind and from battery discharge)[4](https://samrepo.nrelcloud.org/help/mtp_capacity_factor.html)[5](https://aziz.seas.harvard.edu/files/newaziz/files/mja212_0.pdf)[6](https://orbit.dtu.dk/files/276242430/Component_Sizing_of_utility_scale_hybrid_power_plant.pdf).
    

## **6. Example Calculation**

**6. Example Calculation**

Suppose:
$C_{PV} = 50 \, \text{MW}$, $\mathrm{CF}_{PV} = 0.25$
$C_{Wind} = 30 \, \text{MW}$, $\mathrm{CF}_{Wind} = 0.40$
Battery: 20 MW (power), 80 MWh (energy), round-trip efficiency $\eta_{batt} = 0.88$
Annual battery discharge to grid: 50,000 MWh

Calculate each:
$E_{PV} = 50 \times 0.25 \times 8760 = 109,500 \, \text{MWh}$
$E_{Wind} = 30 \times 0.40 \times 8760 = 105,120 \, \text{MWh}$
$E_{Batt, net} = 50,000 \times 0.88 = 44,000 \, \text{MWh}$

Assume maximum grid export (nameplate) = 100 MW.

$E_{\text{Hybrid, annual}} = 109,500 + 105,120 + 44,000 = 258,620 \, \text{MWh}$
$\mathrm{CF}_{\text{Hybrid}} = \frac{258,620}{100 \times 8760} = 0.295 \, \text{or} \, 29.5\%$



## Summary Table of Key Formulas

| Component          | Formula                                                                                         |
| ------------------ | ----------------------------------------------------------------------------------------------- |
| PV Annual Energy   | $E_{PV} = C_{PV} \times \mathrm{CF}_{PV} \times 8760$                                           |
| Wind Annual Energy | $E_{Wind} = C_{Wind} \times \mathrm{CF}_{Wind} \times 8760$                                     |
| Battery Net Output | $E_{Batt, net} = \text{Annual battery discharge} \times \eta_{batt}$                            |
| Hybrid CF          | $\mathrm{CF}_{\text{Hybrid}} = \frac{E_{\text{Hybrid, annual}}}{C_{\text{Hybrid}} \times 8760}$ |



**References:**

- NREL SAM Help[4](https://samrepo.nrelcloud.org/help/mtp_capacity_factor.html)
    
- Aziz Group, storage efficiency and hybrid mapping[5](https://aziz.seas.harvard.edu/files/newaziz/files/mja212_0.pdf)
- - NREL hybrid system modeling and sizing [1](https://www.nrel.gov/docs/fy23osti/81902.pdf) [6](https://orbit.dtu.dk/files/276242430/Component_Sizing_of_utility_scale_hybrid_power_plant.pdf)


example 2
## **1. System Sizing & Inputs**

**1. System Sizing & Inputs**
From your description and the image, we know:
$C_{\text{Batt, power}} = 2 \, \text{MW}$ (Battery rated power)
$D_{\text{Storage}} = 4 \, \text{hours}$ (Duration of storage)
$E_{\text{Batt, capacity}} = 8 \, \text{MWh}$ (Nominal battery capacity)
Let's also assume example capacities and CFs for PV and wind:
$C_{PV} = 10 \, \text{MW}$, $\mathrm{CF}_{PV} = 0.25$
$C_{Wind} = 8 \, \text{MW}$, $\mathrm{CF}_{Wind} = 0.40$
Battery round-trip efficiency: $\eta_{batt} = 0.88$

**2. Annual Energy Output Calculations**
**PV Annual Energy:**
$E_{PV} = C_{PV} \times \mathrm{CF}_{PV} \times 8760 = 10 \, \text{MW} \times 0.25 \times 8760 = 21,900 \, \text{MWh}$

**Wind Annual Energy:**
$E_{Wind} = C_{Wind} \times \mathrm{CF}_{Wind} \times 8760 = 8 \, \text{MW} \times 0.40 \times 8760 = 28,032 \, \text{MWh}$


## **3. Battery Energy Considerations**

We need to estimate the **Annual Battery Discharge to Grid**. This is highly dependent on the operational strategy and energy management system. Let's assume the battery cycles once per day (fully charges and discharges), utilizing its full 8 MWh capacity:

**Annual Battery Discharge:**

$E_{\text{Batt, discharge}} = \text{Cycles per day} \times \text{Battery Capacity} \times 365 = 1 \times 8 \, \text{MWh} \times 365 = 2,920 \, \text{MWh}$

Then, the **Net Battery Energy Delivered** to the grid, considering efficiency:

$E_{\text{Batt, net}} = E_{\text{Batt, discharge}} \times \eta_{batt} = 2,920 \, \text{MWh} \times 0.88 = 2,570 \, \text{MWh}$

**4. Total Hybrid System Annual Output**

$E_{\text{Hybrid, annual}} = E_{PV} + E_{Wind} + E_{\text{Batt, net}}$
$E_{\text{Hybrid, annual}} = 21,900 \, \text{MWh} + 28,032 \, \text{MWh} + 2,570 \, \text{MWh} = 52,502 \, \text{MWh}$

## **5. Hybrid System Nameplate Capacity**

We have a power rating for the battery (2 MW) and the PV/wind, but the grid interconnection might be limited, use the **Grid Export Limit** if you know it. Otherwise, the reasonable default is the sum of the generators

$C_{\text{Hybrid}} = C_{PV} + C_{Wind} + C_{\text{Batt, power}} = 10 \, \text{MW} + 8 \, \text{MW} + 2 \, \text{MW} = 20 \, \text{MW}$

Note: You use the Power Rating of the battery (2 MW), not the energy capacity (8 MWh).

**6. Calculate Hybrid System Capacity Factor**

$\mathrm{CF}_{\text{Hybrid}} = \frac{E_{\text{Hybrid, annual}}}{C_{\text{Hybrid}} \times 8760} = \frac{52,502 \, \text{MWh}}{20 \, \text{MW} \times 8760 \, \text{hours}} = 0.299 \, \text{or} \, 29.9\%$

## **Summary**

- **PV Output:** 21,900 MWh
- **Wind Output:** 28,032 MWh
- **Battery Output:** 2,570 MWh (net)
- **Total Output:** 52,502 MWh
- **Hybrid Capacity:** 20 MW
- **Hybrid Capacity Factor:** 29.9%


- **Battery Dispatch:** The key assumption is how the battery is used (how many cycles per day). Real-world capacity factors can vary widely (from 5% to 50%) depending on optimization and market incentives.















## Is capacity factor added in calculating LCOE

yes, higher capacity factors implies more energy is produced from the potential rated power source

$$\mathrm{LCOE}_{\text{mix}} = \frac{\sum_i \text{Total Cost}_i}{\sum_i \text{Total Generation}_i}$$

where

$$\text{Total Generation}_i = \text{Installed Capacity}_i \times 8760 \times \mathrm{CF}_i$$

**Example 1: Wind + Solar Mix**

Suppose:

* Wind: 100 MW, CF = 40%, LCOE = $45/MWh
* Solar: 100 MW, CF = 25%, LCOE = $35/MWh
* Wind annual generation: 100 × 8760 × 0.40 = 350,400 MWh
* Solar annual generation: 100 × 8760 × 0.25 = 219,000 MWh
* Total annual generation: 569,400 MWh
* Total annual cost: (350,400 × $45) + (219,000 × $35) = $15,768,000 + $7,665,000 = $23,433,000

$\mathrm{LCOE}_{\text{mix}} = \frac{23,433,000}{569,400} \approx \$41.15/\text{MWh}$

| Energy Mix         | Typical LCOE (2024, US$/MWh) | Source                                                                        |
| ------------------ | ---------------------------- | ----------------------------------------------------------------------------- |
| Wind + Solar       | 41–45                        | [8](https://www.lazard.com/media/xemfey0k/lazards-lcoeplus-june-2024-_vf.pdf) |
| Solar + Storage    | 54–92                        | [8](https://www.lazard.com/media/xemfey0k/lazards-lcoeplus-june-2024-_vf.pdf) |
| Wind + Storage     | 45–74                        | [8](https://www.lazard.com/media/xemfey0k/lazards-lcoeplus-june-2024-_vf.pdf) |
| Gas Combined Cycle | 39–101                       | [8](https://www.lazard.com/media/xemfey0k/lazards-lcoeplus-june-2024-_vf.pdf) |



> [!question] 
> ## And for hydrogen production how does the capacity factor appears in the hydrogen output 




## Hydrogen Production vs. Capacity Factor

**Tags:** #hydrogen #electrolysis #capacityfactor #efficiency #LCOH #energy

### 1. Key Formula (Faraday's Law)

The mass of hydrogen produced annually is directly influenced by the electrolyzer's capacity factor:

$$\text{Annual H}_2 \text{ (kg)} = 0.0408 \times I \times t \times CF \times \eta_{\text{Faraday}}$$

Where:
- $I$ = Current (amps)
- $t$ = Annual operating hours (typically 8,760)
- $\eta_{\text{Faraday}}$ = Faraday efficiency ($\sim$85–95%)
- $CF$ = Capacity factor (decimal, e.g., 0.6 for 60%)

**Example:**

A 1 MW electrolyzer ($I = 4167 \, \text{A}$) with $CF = 60\%$:

$\text{Annual H}_2 = 0.0408 \times 4167 \times 8760 \times 0.6 \times 0.9 \approx 67,500 \, \text{kg}$

At $CF = 90\%$, this rises to $\sim 101,250 \, \text{kg}$.

### 2. Efficiency Impact

Electrolyzer efficiency ($\eta_{HHV}$) depends on the operating voltage ($V$), which is influenced by the capacity factor:

$$\eta_{HHV} = \frac{\text{HHV of H}_2}{\text{Energy Input}} = \frac{39.4 \, \text{kWh/kg}}{V \times I / 1000}$$

- **Higher CF (steady operation)** $\rightarrow$ Lower voltage ( $\sim$1.8–2.2 V) $\rightarrow$ Higher efficiency ($\sim$60–75% HHV).
- **Lower CF (intermittent operation)** $\rightarrow$ Voltage spikes during startups $\rightarrow$ Efficiency drops by 5–15%<sup>[46]</sup>.

### 3. Levelized Cost of Hydrogen (LCOH)

$$\text{LCOH} = \frac{\text{Annualized Capital Cost} + \text{O\&M Cost}}{\text{Annual H}_2 \text{ Production}}$$

Lower CF increases LCOH because fixed costs are spread over a smaller amount of hydrogen produced.

**Example:**

A system with $CF = 60\%$ has $\sim$40% higher LCOH than one at $CF = 90\%$.


## **Practical Implications**

|CF|Annual H₂ (kg/MW)|Efficiency (HHV)|LCOH ($/kg)|
|---|---|---|---|
|40%|45,000|62–68%|4.8–6.2|
|60%|67,500|65–72%|3.5–4.5|
|90%|101,250|70–75%|2.6–3.2|

 NREL (2024), Lazard (2023)_[1](https://energy.mit.edu/wp-content/uploads/2023/04/MITEI-WP-2023-02.pdf)[4](https://www.nrel.gov/docs/fy24osti/88746.pdf).

## **Why CF Matters**

- **High CF** (e.g., 80–95%): Achieved with **grid-buffered systems** or **hybrid plants** (wind/solar + storage)[4](https://www.nrel.gov/docs/fy24osti/88746.pdf).
    
- **Low CF** (e.g., 30–50%): Common in **curtailed renewable energy** setups, leading to higher costs and wear.

---







> [!question] 
> is there a different capacity factor for h2 production system and a different production capacity factor for the energy system: How do they relate.


## **How the Capacity Factors Differ and Relate**

## **1. Energy System Capacity Factor (CFenergyenergy)**

- This is the ratio of actual electricity generated by the renewable energy plant (e.g., wind, solar) to its maximum possible generation over a period[6](https://en.wikipedia.org/wiki/Capacity_factor)[8](https://www.solisrenewables.com/blog/what-is-capacity-factor)[9](https://www.stout.com/en/insights/commentary/understanding-capacity-factors-renewable-sources-fossil-fuels).
    
- It reflects resource variability (e.g., sun, wind), outages, and curtailment.
    

## **2. Hydrogen Production System Capacity Factor (CFH2H2)**

- This is the ratio of actual hydrogen produced (or actual electrolyzer operation) to the maximum possible hydrogen production if the electrolyzer ran at full power all the time[5](https://www.nrel.gov/docs/fy09osti/46267.pdf)[6](https://en.wikipedia.org/wiki/Capacity_factor).
- It is determined by how much electricity is available to the electrolyzer and by its own outages and maintenance[5](https://www.nrel.gov/docs/fy09osti/46267.pdf).
    
- **CFH2H2 is often lower than or equal to CFenergyenergy**, especially if the electrolyzer only operates when surplus renewable power is available (i.e., not grid-connected or not using storage)[1](https://www.sciencedirect.com/science/article/abs/pii/S030626192300380X)[7](https://eneken.ieej.or.jp/data/6475.pdf).
    

## **Relationship Between the Two**

- **If the electrolyzer is directly coupled to variable renewables:**  
    The electrolyzer can only run when there is enough renewable electricity. Thus, its capacity factor (CFH2H2) is limited by the availability of surplus power, which is often less than the average capacity factor of the renewable plant[1](https://www.sciencedirect.com/science/article/abs/pii/S030626192300380X)[7](https://eneken.ieej.or.jp/data/6475.pdf).


----
# Why the Average Capacity Factor Can't Exceed the Maximum

- **Definition:** Capacity factor is the ratio of actual energy output to the maximum possible output if the system ran at full capacity all the time.
    
- **Combining Systems:** When you combine two or more systems (e.g., wind and solar), the total energy output is the sum of each system’s output, and the total installed capacity is the sum of their rated capacities.
    
- **Weighted Average:** The combined (or average) capacity factor is a weighted average, not a sum. Mathematically:
    
    $CF_{total}=∑(Capacity_{i}×CF_{i})∑\text{Capacity}_{i}$ 
- **Limitation:** The average of several numbers cannot be greater than the largest number in the set. Thus, the combined CF cannot exceed the highest individual CF.
    

## **Why Not Higher?**

- **Physical Constraints:** Even if you combine systems with complementary generation profiles (like wind and solar), the total output is still limited by the maximum possible output of the installed capacity. You can't generate more energy than if the highest-performing unit ran at full power all year.
    
- **Curtailment and Limits:** In practice, hybrid systems can face additional constraints—such as inverter or interconnection limits, curtailment, or storage losses—which can further reduce the combined capacity factor relative to the theoretical maximum[1](https://www.nrel.gov/docs/fy22osti/75864.pdf)[7](https://hybridpowersystems.org/crete2019/wp-content/uploads/sites/13/2020/03/7B_2_HYB19_040_paper_Das_Kaushik.pdf).
    
- **Storage Helps, But...** Storage can shift output and smooth variability, raising the effective capacity factor compared to standalone renewables, but still cannot push the average above the best-performing component unless you "overbuild" generation and undercount capacity, which is not standard practice[1](https://www.nrel.gov/docs/fy22osti/75864.pdf)[5](https://www.frontiersin.org/journals/energy-research/articles/10.3389/fenrg.2023.1036183/full)[6](https://www.nrel.gov/docs/fy23osti/81901.pdf).
    

## **Illustrative Example**

## Illustrative Example: Combined Capacity Factor (Wind & Solar)

**Tags:** #capacityfactor #renewableenergy #wind #solar #combinedCF

**Suppose:**

* Wind Capacity Factor ($CF_{wind}$) = 40%
* Solar Capacity Factor ($CF_{solar}$) = 25%
* You install 50 MW of each.

**Combined Capacity Factor ($CF_{total}$):**

$CF_{total} = \frac{(50 \, \text{MW} \times 0.40) + (50 \, \text{MW} \times 0.25)}{50 \, \text{MW} + 50 \, \text{MW}} = \frac{20 + 12.5}{100} = \frac{32.5}{100} = 0.325 \, \text{or} \, 32.5\%$

**Key Takeaway:**

The combined capacity factor (32.5%) is between the two individual capacity factors (25% and 40%) and, importantly, it is **never higher** than the highest individual capacity factor (40% in this case, which is the wind's CF). This illustrates that combining intermittent renewable sources results in a more stable but not necessarily higher overall capacity factor.

## **Key Takeaways**

- **Combining systems increases reliability, reduces variability, and can raise the minimum output, but the average capacity factor cannot exceed the highest individual capacity factor.**
- **You combine systems to make output steadier and possibly higher than the lowest CF, but not to exceed the maximum CF of any component.**
- **Storage and hybridization can optimize output timing and raise the effective CF, but only up to the physical and operational limits of the system[1](https://www.nrel.gov/docs/fy22osti/75864.pdf)[5](https://www.frontiersin.org/journals/energy-research/articles/10.3389/fenrg.2023.1036183/full)[6](https://www.nrel.gov/docs/fy23osti/81901.pdf).**
    

**References:**[1](https://www.nrel.gov/docs/fy22osti/75864.pdf) NREL, "Influence of Hybridization on the Capacity Value of PV and Battery"[5](https://www.frontiersin.org/journals/energy-research/articles/10.3389/fenrg.2023.1036183/full) Frontiers in Energy Research, "Hybrid renewable energy systems: the value of storage..."[6](https://www.nrel.gov/docs/fy23osti/81901.pdf) NREL, "Complementarity of Renewable Energy-Based Hybrid Systems"







-----

## Probability Distribution Functions for PV and Wind Renewable Energy Systems in Hydrogen Production Modeling

**Tags:** #probabilitydistribution #PDF #windenergy #PV #solarenergy #hydrogen #MonteCarlo #modeling #statistics #uncertainty

This note summarizes common probability distribution functions (PDFs) used for modeling wind and solar renewable energy systems, particularly in the context of Monte Carlo simulations for hydrogen production.

### Wind Energy Systems

* **Common PDF:** Weibull distribution
* **Why:** Flexibility and empirical accuracy in modeling wind speed.
* **Parameters:**
    * Scale parameter ($\alpha$ or $k$)
    * Shape parameter ($\beta$ or $b$)
* **Formula:**
    $f(t) = \frac{\alpha}{\beta} \left(\frac{t}{\beta}\right)^{\alpha-1} \exp\left[-\left(\frac{t}{\beta}\right)^{\alpha}\right], \quad t > 0$
    where $t$ is the wind speed<sup>[69]</sup>.
* **Other Distributions (less common):** Rayleigh, Gamma, Log-normal, and Exponential<sup>[9]</sup>. [^1]
![[probability distribution curves.png]]

![[image-12.png]]

### Photovoltaic (PV) Systems

* **Stochastic Variable:** Solar irradiance.
* **Common PDFs:**
    * **Beta distribution:** Preferred due to its bounded nature between 0 and 1<sup>[134]</sup>.
    * **Normal (Gaussian) distribution:** Used for daily or hourly irradiance under certain conditions.
    * **Log-normal distribution:** Suitable for skewed irradiance data.
    * **Mixture models:** Combine several distributions for a better fit to observed data<sup>[134]</sup>.
* **Key Parameters:** Mean, variance, and shape parameters. These depend on local climate and historical irradiance data<sup>[15]</sup>.

### Parameters for Monte Carlo Modeling of Hydrogen Production

When using Monte Carlo simulations to assess the impact of renewable variability on hydrogen production, the following parameters are crucial:

**Wind System Parameters:**

* Wind speed distribution parameters (Weibull scale and shape)
* Turbine power curve
* Wind farm availability

**PV System Parameters:**

* Solar irradiance distribution parameters (mean, variance, or beta distribution shape parameters)
* PV panel efficiency
* System losses

**Electrolyzer and Hydrogen Production Parameters:**

* Electrolyzer efficiency (electricity to hydrogen conversion rate)
* Minimum and maximum operating power of the electrolyzer
* Hydrogen storage capacity and losses

**System-wide Parameters:**

* Correlation between wind and solar resource<sup>[8]</sup> (for hybrid systems)
* Load demand profile (if hydrogen production is demand-driven)
* Time resolution (hourly, daily, etc.)

**Monte Carlo Simulation Inputs:**

* Random samples drawn from the PDFs of wind speed and solar irradiance.
* Stochastic modeling of system failures or maintenance.
* Economic parameters (if cost modeling is included)<sup>[78]</sup>.

**Example Approach:**

1.  **Generate Random Samples:** Create a large number of random samples for wind speed and solar irradiance based on their chosen PDFs and estimated parameters.
2.  **Calculate Power Output:** For each sample, determine the power generated by the wind and PV systems using their respective models (e.g., turbine power curve, PV efficiency).
3.  **Simulate Hydrogen Production:** Use the calculated power output as input to the electrolyzer model to simulate hydrogen production for each time step.
4.  **Aggregate Results:** Analyze the collected data to estimate the probability distribution of hydrogen production, the mean output, and the associated uncertainties<sup>[78]</sup>.

### Summary Table: Common PDFs and Parameters

| Resource             | Common PDF(s)                      | Key Parameters                               |
| :------------------- | :--------------------------------- | :------------------------------------------- |
| Wind Speed           | Weibull, Rayleigh                  | Scale ($\alpha$), Shape ($\beta$)             |
| Solar Irradiance     | Beta, Normal, Log-normal, Mixture | Mean, Variance, Shape parameters             |
| Hydrogen Production  | Derived from above (via Monte Carlo) | Electrolyzer efficiency, storage, correlation factors |

### References to Modeling Approaches

* Weibull and other distributions for wind speed<sup>[69]</sup>.
* Mixture and empirical distributions for solar irradiance<sup>[13]</sup>.
* Monte Carlo simulation using these distributions and system parameters to model hydrogen production and its uncertainty<sup>[78]</sup>.

By appropriately selecting and parameterizing these probability distribution functions, Monte Carlo simulations can effectively model the inherent variability and uncertainty in renewable energy generation and its subsequent impact on hydrogen production systems.




# perfomance


## **Framework for Monte Carlo-Based Hydrogen Production Modeling with PV and Wind**

### **1. Locations of Interest**

Regions analyzed for resource potential:

- **Texas Gulf Coast (Houston–Corpus Christi Corridor)**
- **California (Central Valley & Southern Desert Regions)**
- **Great Plains (Kansas, Oklahoma, Nebraska)**
- **New York State (Offshore Wind & Urban Demand Centers)**
- **Arizona (Phoenix–Casa Grande Corridor)**
    

Each region will be characterized by:
- Historical solar irradiance (GHI / DNI) and wind speed (hub height specific).
- Seasonal and diurnal variation profiles.
- Technology deployment options (onshore wind, offshore wind, fixed-tilt PV, single-axis tracking PV).
    

---

### **2. System Scales for Comparison**

- **Distributed Hydrogen Production:** Small electrolyzers (e.g., 1–5 MW), co-located with RE systems at or near point of use.
    
- **Centralized Hydrogen Production:** Large electrolyzers (e.g., 10–100+ MW), industrial-scale installations with possible grid interaction.
    

---

### **3. Probabilistic Modeling Approach**

**Monte Carlo Simulation Framework:**

- Input uncertainty captured via **Probability Distribution Functions (PDFs)** for key parameters:
    - **Solar irradiance:** Often modeled using **Beta, Weibull, or Lognormal distributions** for daily/hourly GHI depending on region.
    - **Wind speed:** Standard practice is to use a **Weibull distribution** (2-parameter or 3-parameter depending on the dataset) for wind speeds at hub height.
    - **Ambient temperature:** Normally distributed or based on historical seasonal profiles.
    - **Derating factors:** Represented as fixed values or uniform distributions within realistic ranges (e.g., inverter efficiency 95–98%, soiling loss 1–5%).

### **4. Modeling Structure**

- **Hourly Time-Series Sampling:** Randomly sample irradiance, wind speed, temperature for each hour of the year from the PDFs.
    
- **Power Output Calculation:**

* **PV Output:**

    $P_{PV} = P_{STC} \times \frac{G}{G_{STC}} \times [1 + \alpha_p (T_{cell} - T_{STC})] \times f_{PV}$

    * Temperature effects calculated using NOCT-based cell temperature models.

* **Wind Output:**

    $P_{Wind} = \frac{1}{2} \rho A C_p v^3$

    * [ ] Apply manufacturer power curves and derating factors.



### **5. Hydrogen Production Model**

- **Electrolyzer Efficiency:** Variable with power input and load factor. Efficiency modeled as a function of operating point (part-load curves).
    
- **Hydrogen Production Rate:**
$$\dot{m}_{H_2} = \frac{P_{\text{input}} \cdot \eta_{\text{elec}}}{\text{Specific Energy Consumption per kg H}_2}$$

- **Monte Carlo Integration:** Calculate annual hydrogen output by summing hourly hydrogen production across sampled scenarios.
    
- Include random fluctuations and seasonal effects across thousands of simulations to assess the distribution of hydrogen output.


### **6. Monte Carlo on LCOH (Levelized Cost of Hydrogen)**

- CAPEX and OPEX modeled as distributions (e.g., triangular or normal with mean and standard deviation).
    
- Grid electricity prices modeled as random variables for grid-interactive systems (using historical price distributions).
    
- Monte Carlo draws random samples for:
    - Renewable generation
    - Electrolyzer utilization
    - System costs
        
- Output: **Distribution of LCOH values (mean, median, percentiles, boxplots).**
    

---

### **7. Outputs and Visualization**

- Probability distributions of:
    - Hourly/seasonal power outputs.
    - Annual hydrogen production.
    - LCOH (mean, standard deviation, 5th–95th percentile ranges).
        
- Visualization:
    
    - **Histograms and PDFs** of outputs.
    - **Boxplots** comparing distributed vs. centralized.
    - **Correlation heatmaps** of inputs vs. hydrogen production variability.
    - **Tornado diagrams** showing sensitivity of LCOH to key parameters.



### ✅ **Next Steps:**

1. [ ] Begin gathering the historical irradiance, wind, and temperature data for these five regions?
2. [ ] Build the first version of the Monte Carlo model in Python (with parameter definitions and sampling structure)?
3. [ ] Write a structured technical report summarizing the methodology with the equations and planned simulation design?





----
# Designing the perfomance in excel

**Generating hourly data**

to generate custom hourly profiles for PV (solar) and wind output, ideally using random generation formulas. We could easily handle this using Python, as it’s better suited for creating synthetic data. However, within the Excel context, using RAND() and other Excel formulas, though it might be a bit cumbersome for random distributions in Excel. In any case, the main goal is mimicking a characteristic system with the right parameters.


**Generating hourly data with Excel**

 a set of custom hourly data for PV and wind, For the solar generation, we can use formulas like `=MAX(0, Gmax * SIN())` combined with `RAND()` to create a sinusoidal irradiance profile, plus some noise. For wind generation, I can suggest a Weibull-like formula using `RAND()`. The idea is to help them generate data for a year, but we’ll stick with a simpler 24-hour example for demonstration. 


---

## 1. Set up your sheet

| Column | Header              | Formula / Notes                                                                        |
| :----: | ------------------- | -------------------------------------------------------------------------------------- |
|   A    | **Hour**            | 1, 2, 3, …, 8760 (fill down)                                                           |
|   B    | **HourOfDay**       | =MOD(A2–1,24)                                                                          |
|   C    | **DayOfYear**       | =INT((A2–1)/24)+1                                                                      |
|   D    | **G₀ (Irradiance)** | =MAX(0, Gₘₐₓ * SIN( (B2–6)/12_PI() )) * (1+0.1_(RAND()–0.5))                           |
|   E    | **Tamb**            | =Tₘₑₐₙ + Tₐₘₚ * SIN( (C2–80)/365_2_PI() ) + 2*(RAND()–0.5) ⇐ seasonal + a little noise |
|   F    | **T₍cell₎**         | =E2 + (NOCT–20)/800 * D2                                                               |
|   G    | **Pₚᵥ (MW)**        | =Pₛₜc * (D2/Gₛₜc) * (1+αₚ*(F2–Tₛₜc)) * fₚᵥ                                             |
|   H    | **v₍wind₎ (m/s)**   | =λ * (–LN(RAND()))^(1/k) ⇐ Weibull random: λ=scale, k=shape                            |
|   I    | **P𝚠ᵢₙd (MW)**     | =0.5 * ρ * A * Cₚ * H2^3 / 10^6 ⇐ convert W→MW                                         |

**Before you begin**, define these named cells (or just constants in your formulas):
STC- Standard test condition

| Name  | Description                        | Example Value |
| :---: | ---------------------------------- | ------------- |
| Gₘₐₓ  | Clear-sky peak irradiance (W/m²)   | 1000          |
| Gₛₜc  | STC irradiance (1000 W/m²)         | 1000          |
| Pₛₜc  | PV rated power (MW)                | 1             |
|  αₚ   | Temp. coefficient (per °C)         | –0.0035       |
| Tₛₜc  | STC cell temp (25 °C)              | 25            |
|  fₚᵥ  | PV system derate (e.g. soiling)    | 0.90          |
| NOCT  | Nominal operating cell temp (°C)   | 45            |
| Tₘₑₐₙ | Annual mean ambient temp (°C)      | 15            |
| Tₐₘₚ  | Seasonal amp. of ambient temp (°C) | 10            |
|   λ   | Wind scale parameter (m/s)         | 8             |
|   k   | Wind shape parameter               | 2             |
|   ρ   | Air density (kg/m³)                | 1.225         |
|   A   | Turbine swept area (m²)            | 5 000         |
|  Cₚ   | Power coefficient (≤0.59)          | 0.4           |

---

## 2. Formula breakdown

1. **Solar irradiance (D2):**  
    A simple daily sine-shape peaking at noon (HourOfDay=12) plus ±5% random noise.
    
    ```excel
    =MAX(0, Gₘₐₓ * SIN((B2–6)/12*PI())) * (1 + 0.1*(RAND()–0.5))
    ```
    
2. **Ambient temperature (E2):**  
    Seasonal sine wave with mid-year peak around Day 172 (here phase-shifted by 80) plus small random noise.
    
    ```excel
    =Tₘₑₐₙ + Tₐₘₚ * SIN((C2–80)/365*2*PI()) + 2*(RAND()–0.5)
    ```
    
3. **Cell temperature (F2):**  
    NOCT model: ambient + (NOCT–20)/800 · G.
    
    ```excel
    =E2 + (NOCT–20)/800 * D2
    ```
    
4. **PV power (G2):**  
    STC derate × irradiance ratio × temperature correction × soiling factor.
    
    ```excel
    =Pₛₜc * (D2/Gₛₜc) * (1 + αₚ*(F2–Tₛₜc)) * fₚᵥ
    ```
    
5. **Wind speed (H2):**  
    Inverse-Weibull sampling:
    
    ```excel
    =λ * (-LN(RAND()))^(1/k)
    ```
    
6. **Wind power (I2):**  
    ½ ρACₚv³ converted to MW.
    
    ```excel
    =0.5 * ρ * A * Cₚ * H2^3 / 1E6
    ```
    

---

## 3. Fill down & compute capacity factors

1. **Select A2:I2**, drag (or double-click) the fill-handle down to row 8761.
    
2. **Annual PV capacity factor:**
    
    ```excel
    =AVERAGE(G2:G8761) / Pₛₜc
    ```
    
3. **Annual Wind capacity factor:**
    
    ```excel
    =AVERAGE(I2:I8761) / WindRatedPower
    ```
    
    (If you used a rated power of, say, 2 MW per turbine, divide by that.)
    

---

### Why this works

- **Sinusoidal shapes** approximate daily/seasonal cycles.
    
- **RAND()-based noise** adds realism.
    
- **Weibull sampling** is a standard way to get wind-speed distributions.
    
- **Physics formulas** to ensure outputs scale correctly with G or v³.
    

You can tweak any parameter—Gₘₐₓ, αₚ, NOCT, λ, k, etc.—to “tune” your synthetic plant to reflect different climates or technologies. Once you have your hourly series, you can hook them right into your existing “Generation (MWh/MW)” lookups and capacity-factor calculations.



---


> [!bug] 
> The power coefficient (Cp) of a wind turbine is a function of both the [tip speed ratio (λ)] and the [pitch angle (β)]. Generally, ==as the tip speed ratio increases, the power coefficient also increases up to a certain point, after which it decreases==. Similarly, increasing the pitch angle (β) will generally lead to a decrease in the power coefficient.

- 
    **Tip Speed Ratio (λ):**
    
    The tip speed ratio is the ratio of the speed of the turbine blade tip to the wind speed. It's a key factor in determining how efficiently a turbine extracts energy from the wind. There's an optimal tip speed ratio for each turbine design that maximizes the power coefficient. 
    
- 
    **Pitch Angle (β):**
    
    The pitch angle refers to the angle of the blades relative to the wind. By adjusting the pitch angle, you can control the aerodynamic characteristics of the blades and, consequently, the power coefficient. Increasing the pitch angle generally reduces the power coefficient, especially at higher wind speeds, as it reduces the angle of attack of the blades and reduces the aerodynamic force. 
    
- 
    **Power Coefficient (Cp):**
    The power coefficient represents the efficiency of a wind turbine, specifically how much mechanical power is generated from the available wind power. A higher power coefficient means the turbine is extracting more power from the wind. 
- 


![[image-8.png|301x268]]

![[image-10.png]]
# Simulator for Studying the Wind Turbines Work

- June 2015

DOI:[10.1109/EEEIC.2015.7165319](http://dx.doi.org/10.1109/EEEIC.2015.7165319)


![[image-9.png|380x280]]





# Mathematical Modeling and Methodology for Renewable Energy Generation

This section outlines the mathematical formulation and methodology used to model the power output from photovoltaic (PV) and wind energy systems on an hourly basis over a one-year period (8760 hours). The model incorporates temporal variations in solar irradiance and ambient temperature for PV systems, and stochastic wind speed variations for wind turbines.

## 1. Temporal Framework

The model operates on an hourly resolution for a full year, resulting in a total of 8760 time steps.

- **Hour (h):** The simulation progresses through each hour of the year, indexed by $h$, where $h \in \{1, 2, ..., 8760\}$.
- **Hour of Day (HOD$_h$):** The hour of the day for a given hour $h$ is calculated using the modulo operation:
  $$HOD_h = MOD(h - 1, 24)$$
  This yields a value between 0 and 23, representing the hour within a 24-hour cycle.
- **Day of Year (DOY$_h$):** The day of the year for a given hour $h$ is determined by integer division:
  $$DOY_h = INT(\frac{h - 1}{24}) + 1$$
  This results in a value between 1 and 365 (or 366 for a leap year, though this model assumes a standard 365-day year), representing the day within the year.

## 2. Photovoltaic (PV) Power Generation

The power output of the PV system is modeled as a function of solar irradiance and cell temperature, considering the system's rated power and performance characteristics.

- **Global Irradiance on PV Array (G$_h$):** The hourly global irradiance incident on the PV array is estimated using a sinusoidal function to represent the diurnal variation, with added stochasticity to account for cloud cover and other unpredictable factors:
  $$G_h = MAX(0, G_{max} \cdot SIN(\frac{HOD_h - 6}{12}\pi)) \cdot (1 + 0.1 \cdot (RAND() - 0.5))$$
  where:
    - $G_{max}$ is the clear-sky peak irradiance (W/m²).
    - $RAND()$ is a random number drawn from a uniform distribution between 0 and 1, introducing hourly variability. The term $(1 + 0.1 \cdot (RAND() - 0.5))$ introduces a $\pm 5\%$ random fluctuation around the clear-sky irradiance profile.

  **Assumption:** This simplified model assumes a fixed tilt angle and orientation for the PV array. It also approximates the daily irradiance profile with a sinusoidal function peaking at solar noon (approximately hour 12, hence the offset of 6 in the sine function).

- **Ambient Temperature (Tamb,$_h$):** The hourly ambient temperature is modeled as a sinusoidal function representing the seasonal variation, superimposed with random noise to account for daily fluctuations:
  $$Tamb,h = T_{mean} + T_{amp} \cdot SIN(\frac{DOY_h - 80}{365} \cdot 2\pi) + 2 \cdot (RAND() - 0.5)$$
  where:
    - $T_{mean}$ is the annual mean ambient temperature (°C).
    - $T_{amp}$ is the seasonal amplitude of the ambient temperature (°C).
    - The term $2 \cdot (RAND() - 0.5)$ introduces a $\pm 1$ °C random fluctuation around the seasonal temperature profile.
    - The phase shift of 80 days approximates the coldest period occurring around the 80th day of the year.

  **Assumption:** This model assumes a sinusoidal seasonal temperature variation, which is a reasonable approximation for many locations.

- **PV Cell Temperature (Tcell,$_h$):** The operating temperature of the PV cells is estimated based on the ambient temperature and the incident solar irradiance, using a simplified linear relationship derived from the Nominal Operating Cell Temperature (NOCT):
  $$Tcell,h = Tamb,h + \frac{NOCT - 20}{800} \cdot G_h$$
  where:
    - $NOCT$ is the nominal operating cell temperature (°C), defined as the cell temperature under specific conditions (800 W/m² irradiance, 20 °C ambient temperature, and 1 m/s wind speed).

  **Assumption:** This model assumes a linear relationship between solar irradiance and the difference between cell and ambient temperature. Wind speed effects on cell temperature are implicitly incorporated within the NOCT parameter.

- **PV Power Output (Ppv,$_h$):** The hourly power output of the PV system (in MW) is calculated by adjusting the rated power for the actual irradiance and cell temperature:
  $$Ppv,h = P_{stc} \cdot (\frac{G_h}{G_{stc}}) \cdot (1 + \alpha_p \cdot (Tcell,h - T_{stc})) \cdot f_{pv}$$
  where:
    - $P_{stc}$ is the PV rated power under Standard Test Conditions (STC) (MW).
    - $G_{stc}$ is the irradiance at STC (1000 W/m²).
    - $\alpha_p$ is the temperature coefficient of power (per °C), representing the percentage change in power output per degree Celsius deviation from the STC temperature.
    - $T_{stc}$ is the cell temperature at STC (25 °C).
    - $f_{pv}$ is the PV system derate factor, accounting for losses due to soiling, wiring, and other system inefficiencies.

  **Assumption:** The model assumes a linear temperature dependence of the PV power output.

## 3. Wind Power Generation

The power output of the wind turbine is modeled based on the hourly wind speed, utilizing a simplified power curve relationship.

- **Wind Speed (vwind,$_h$):** The hourly wind speed (in m/s) is generated using a Weibull distribution, which is commonly used to model wind speed frequency distributions:
  $$vwind,h = \lambda \cdot (-LN(RAND()))^{\frac{1}{k}}$$
  where:
    - $\lambda$ is the scale parameter of the Weibull distribution (m/s), related to the average wind speed.
    - $k$ is the shape parameter of the Weibull distribution, influencing the spread of the distribution.
    - $RAND()$ is a random number drawn from a uniform distribution between 0 and 1.

  **Assumption:** This model assumes that the hourly wind speed follows a Weibull distribution. It does not account for wind direction or variations in wind speed with height across the turbine rotor.

- **Wind Power Output (Pwind,$_h$):** The hourly power output of the wind turbine (in MW) is calculated using a simplified power equation based on the kinetic energy of the wind:
  $$Pwind,h = 0.5 \cdot \rho \cdot A \cdot C_p \cdot vwind,h^3 / 10^6$$
  where:
    - $\rho$ is the air density (kg/m³).
    - $A$ is the turbine swept area (m²).
    - $C_p$ is the power coefficient, representing the fraction of the wind's kinetic energy that the turbine can convert into electrical power (Betz limit is approximately 0.59). The actual $C_p$ is a function of the tip-speed ratio and blade pitch angle, but here it is assumed to be a constant value.
    - The division by $10^6$ converts the power from Watts (W) to Megawatts (MW).

  **Assumption:** This model assumes a constant power coefficient ($C_p$) and does not incorporate the detailed power curve of the wind turbine, including cut-in, rated, and cut-out speeds. It also assumes a constant air density.

## 4. Model Implementation

The described equations are implemented on an hourly basis for the entire year (8760 hours). The parameters used in the model are provided in the accompanying table. The stochastic nature of the solar irradiance and wind speed introduces variability in the power output profiles, reflecting the inherent intermittency of these renewable energy sources. This hourly time series data can then be used for further energy system analysis, such as grid integration studies, energy storage requirements, and economic evaluations.



-----



## Power Coefficient Equation as a Function of Tip-Speed Ratio and Pitch Angle

The **power coefficient** ($C_p$) of a wind turbine quantifies the fraction of wind power that the turbine can extract. It is a function of both the **tip-speed ratio**($\lambda$) and the **pitch angle**($\beta$) of the blades[1][2][5]. The relationship is typically represented as $C_p = f(\lambda, \beta)$.

### Common Analytical Expression

A widely used empirical equation for the power coefficient surface is:

$$
C_p(\lambda, \beta) = C_1 \left( \frac{C_2}{\lambda_i} - C_3 \beta - C_4 \right) e^{-C_5/\lambda_i} + C_6 \lambda
$$

where:

- $\lambda$ is the tip-speed ratio,
- $\beta$ is the pitch angle (in degrees),
- $$\lambda_i = \frac{1}{\frac{1}{\lambda + 0.08\beta} - \frac{0.035}{\beta^3 + 1}}$$,
- $C_1, C_2, C_3, C_4, C_5, C_6$ are empirical constants determined by turbine design.

A commonly cited set of constants (for generic turbines) is:
- $C_1 = 0.5176$
- $C_2 = 116$
- $C_3 = 0.4$
- $C_4 = 5$
- $C_5 = 21$
- $C_6 = 0.0068$

### Example Equation

Plugging in these constants, the equation becomes:

$$
C_p(\lambda, \beta) = 0.5176 \left( \frac{116}{\lambda_i} - 0.4\beta - 5 \right) e^{-21/\lambda_i} + 0.0068\lambda
$$
where
$$
\lambda_i = \frac{1}{\frac{1}{\lambda + 0.08\beta} - \frac{0.035}{\beta^3 + 1}}
$$

This model captures the typical $C_p$ vs. $\lambda$ curve for different pitch angles($\beta$), and is used in many engineering studies and simulation tools[2][5].

### Key Points

- $C_p$ reaches its maximum at an optimal tip-speed ratio($\lambda_{opt}$), typically when $\beta = 0^\circ$[5].
- Increasing the pitch angle($\beta$) reduces the maximum achievable $C_p$ and shifts the curve downward, allowing control of power output at high wind speeds[4][5].
- The **maximum $C_p$** for most modern turbines is around 0.42–0.45 at $\lambda \approx 6-8$ and $\beta = 0^\circ$[5].

### Visualization

The relationship is often visualized as a family of curves (or a surface) showing $C_p$ versus $\lambda$ for various values of $\beta$[1][2][5]:

- For each fixed $\beta$, $C_p$ rises to a peak at a certain $\lambda$, then falls.
- As $\beta$ increases, the peak $C_p$ decreases and shifts slightly.

### Summary Table

| Parameter       | Symbol    | Typical Range / Value                          |
| --------------- | --------- | ---------------------------------------------- |
| Tip-speed ratio | $\lambda$ | 0–15                                           |
| Pitch angle     | $\beta$   | 0°–45°                                         |
| Max $C_p$       |           | ~0.42 at $\lambda \sim 6-8$, $\beta = 0^\circ$ |

### References to Provided Sources

- The mathematical dependence of $C_p$ on both $\lambda$ and $\beta$ is standard in wind turbine modeling[2][5].
- The maximum value and the effect of pitch angle are discussed in detail, with example curves and values[4][5].

---

**In summary:**
The power coefficient of a wind turbine as a function of tip-speed ratio and pitch angle is commonly described by an empirical equation such as:

$$
C_p(\lambda, \beta) = 0.5176 \left( \frac{116}{\lambda_i} - 0.4\beta - 5 \right) e^{-21/\lambda_i} + 0.0068\lambda
$$

where $\lambda_i$ is defined above. This equation can be used to generate the $C_p$ vs. $\lambda$ curves for different pitch angles[2][5].

**Citations:**
[1] Tip-speed ratio - Wikipedia https://en.wikipedia.org/wiki/Tip-speed_ratio
[2] Comparison of Power Coefficients in Wind Turbines Considering the ... https://www.mdpi.com/1996-1073/16/6/2774
[3] [PDF] Wind Energy Technology https://www.hawaii.edu/offices/cc/green/Wind_Turbine_Technology.pdf
[4] [PDF] Pitch-Controlled Variable-Speed Wind Turbine Generation - NREL https://www.nrel.gov/docs/fy00osti/27143.pdf
[5] Power Coefficient of a Wind Turbine https://windpowerplus.com/power-coefficient-of-a-wind-turbine/
[6] [PDF] 1 Momentum Theory - University of Notre Dame https://www3.nd.edu/~tcorke/w.windturbinecourse/Aerodynamics_Presentation.pdf
[7] Wind Turbine (Mechanical) - MATLAB - MathWorks https://www.mathworks.com/help/sps/ref/windturbinemechanical.html
[8] How to create cp-λ characteristics curve, for different values of the ... https://www.mathworks.com/matlabcentral/answers/1933845-how-to-create-cp-characteristics-curve-for-different-values-of-the-pitch-angle-for-wind-turbine
[9] Theoretical calculations of blade pitch angle - Rotor Aerodynamics https://forums.nrel.gov/t/theoretical-calculations-of-blade-pitch-angle/2559
[10] Power Coefficient - an overview | ScienceDirect Topics https://www.sciencedirect.com/topics/engineering/power-coefficient
[11] Wind Turbines - Tip Speed Ratio - Electronics Stack Exchange https://electronics.stackexchange.com/questions/527456/wind-turbines-tip-speed-ratio
[12] How is the power of a wind turbine calculated? - Thunder Said Energy https://thundersaidenergy.com/downloads/wind-power-impacts-of-larger-turbines/
[13] [PDF] Calculating the Tip Speed Ratio of Your Wind Turbine https://mmpa.org/wp-content/uploads/2015/09/Tip-Speed-Ratio-Provided-by-Kid-Wind-PDF.pdf



[^1]: **1. Weibull Distribution:**
	
	- **Flexibility:** The Weibull distribution is highly versatile and can model a wide range of data shapes by adjusting its parameters, making it suitable for various phenomena.
	- **Reliability Analysis:** Commonly used in reliability and failure analysis to model the time-to-failure of components or systems.
	- **Parameters:** The shape parameter (β) determines the shape of the distribution and influences whether the failure rate increases, decreases, or remains constant. The scale parameter (α) determines the spread or scale of the distribution. 
	
	**2. Rayleigh Distribution:**
	
	- **Special Case of Weibull:** The Rayleigh distribution is a specific instance of the Weibull distribution where the shape parameter (β) is fixed at 2.
	- **Modeling Wind Speeds:** Frequently used to model wind speed data, especially in wind energy analysis.
	- **Signal Processing and Communication Theory:** Used in various applications, including signal processing and communication theory to model fading in wireless communication channels. 
	
	**3. Gamma Distribution:**
	
	- **Waiting Times:** Models the waiting time until a certain number of events occur in a Poisson process.
	- **Applications:** Applied in areas like insurance, finance, and queuing theory.
	- **Flexibility:** Characterized by a shape parameter (k) and a scale parameter (θ) and can take on different shapes depending on the parameter values. 
	
	**4. Log-Normal Distribution:**
	
	- **Positive and Skewed Data:** Used to model data that is positive and skewed, meaning it has a long tail on one side, often to the right.
	- **Stock Prices and Income:** Used to model stock prices, income distributions, and other phenomena where values cannot be negative and are often skewed.
	- **Derived from Normal:** If the logarithm of a variable follows a normal distribution, the variable itself is log-normally distributed. 
	
	**5. Exponential Distribution:**
	
	- **Time Between Events:** Models the time between events in a Poisson process, where events occur continuously and independently at a constant average rate.
	- **Memoryless Property:** A key characteristic of the exponential distribution is its memoryless property, meaning the probability of an event occurring in the future is independent of past events.
	- **Applications:** Commonly used in reliability analysis, queuing theory, and other fields where waiting times are important.



---
now 2025-05-28T02:01:15-04:00


Here are key references for wind and solar distribution parameters in the specified U.S. regions, presented in Obsidian Markdown format:

## Regional Renewable Energy System Parameters

### Citations:

1.  [https://www.govinfo.gov/content/pkg/GOVPUB-I29-PURL-gpo59969/pdf/GOVPUB-I29-PURL-gpo59969.pdf](https://www.govinfo.gov/content/pkg/GOVPUB-I29-PURL-gpo59969/pdf/GOVPUB-I29-PURL-gpo59969.pdf)
2.  [https://acp.copernicus.org/articles/12/9687/2012/acp-12-9687-2012.pdf](https://acp.copernicus.org/articles/12/9687/2012/acp-12-9687-2012.pdf)
3.  [https://schatzcenter.org/pubs/2020-OSW-R2.pdf](https://schatzcenter.org/pubs/2020-OSW-R2.pdf)
4.  [https://journals.ametsoc.org/view/journals/clim/19/4/jcli3640.1.xml](https://journals.ametsoc.org/view/journals/clim/19/4/jcli3640.1.xml)
5.  [https://www.utdallas.edu/~jxz156730/Journals/JIE_2014_JEE_correlation.pdf](https://www.utdallas.edu/~jxz156730/Journals/JIE_2014_JEE_correlation.pdf)
6.  [https://arxiv.org/html/2405.11046v1](https://arxiv.org/html/2405.11046v1)



Here are key references for wind and solar distribution parameters in the specified U.S. regions:

## Wind System Parameters

Weibull distribution (scale $c$, shape $k$) characterizes regional wind speeds:

**Regional Applications:**
* **Texas Gulf Coast:**
    Typical $k$ = 1.8–2.2, $c$ = 6.5–8.5 m/s due to moderate coastal winds with seasonal tropical storm influences [24].
* **New York Offshore:**
    Higher $k$ = 2.3–2.7 (lower skewness) and $c$ = 9–11 m/s, reflecting steadier marine winds [4].
* **Great Plains:**
    $k$ = 1.6–2.0, $c$ = 7–9 m/s, indicating higher low-speed frequency but strong gusts [2].
* **California Central Valley:**
    Lower $k$ = 1.5–1.8 (greater skewness) and $c$ = 5–7 m/s due to terrain-driven variability [3].

## PV System Parameters

Solar irradiance follows beta or log-normal distributions influenced by cloud cover:

**Regional Applications:**
* **Arizona (Phoenix–Casa Grande):**
    Beta distribution parameters $\alpha$ = 2.1–2.5, $\beta$ = 1.8–2.2 for clear-sky-dominated irradiance [5, 6].
* **California Central Valley:**
    Higher variance ($\sigma^2$ = 0.8–1.2 kW/m²) due to coastal fog, with bimodal distributions in summer [6].
* **Texas Gulf Coast:**
    Mean irradiance 5.2–5.8 kWh/m²/day, skewed by convective cloud cover (beta $\alpha$ = 1.9–2.3, $\beta$ = 2.0–2.4) [5].
* **New York:**
    Lower mean irradiance (4.1–4.6 kWh/m²/day) with frequent overcast skies (beta $\alpha$ = 1.6–1.9, $\beta$ = 2.1–2.5) [6].

**For dynamic modeling:**

* **Wind:** We use Weibull $k$ and $c$ from regionally validated datasets [2, 4].
* **Solar:** We apply beta distribution parameters or hourly variability indices ( 0.15–0.25 variability index in Arizona vs. 0.3–0.4 in New York) [5, 6].

### Citations:

[1] https://www.govinfo.gov/content/pkg/GOVPUB-I29-PURL-gpo59969/pdf/GOVPUB-I29-PURL-gpo59969.pdf
[2] https://acp.copernicus.org/articles/12/9687/2012/acp-12-9687-2012.pdf
[3] https://schatzcenter.org/pubs/2020-OSW-R2.pdf
[4] https://journals.ametsoc.org/view/journals/clim/19/4/jcli3640.1.xml
[5] https://www.utdallas.edu/~jxz156730/Journals/JIE_2014_JEE_correlation.pdf
[6] https://arxiv.org/html/2405.11046v1
[7] https://www.science.gov/topicpages/s/statistical+downscaling+tool.html
[8] https://capla.arizona.edu/sites/default/files/VAF%20Field%20Guide%20Final%20r.pdf
[9] https://nvlpubs.nist.gov/nistpubs/Legacy/IR/nbsir86-3317.pdf
[10] https://thejournalofbusiness.org/index.php/site/article/download/57/56/111
[11] https://www.hancockcollege.edu/ccecho/documents/California%20Geography%20Version%201.2.pdf






----

# Excel RE config workflow
Blurb
	For the wind side, using a Weibull distribution to model hourly wind speeds is standard practice. In fact, most onshore wind-resource assessments assume that the annual distribution of wind speeds follows a Weibull($\lambda$, $k$) law. You then feed those hourly $v$ draws into your power-curve formula ($\tfrac{1}{2}\rho AC_p v^3$) (with cut-in/rated/cut-out clamps) to get realistic hourly wind outputs.
	.
	However, for PV (solar) you do not use a Weibull. Instead, you model solar irradiance ($G$) as a deterministic—plus some noise—sine wave or Beta-type distribution that captures the sun’s daily/seasonal angles. In other words:
	.
	* **Wind speeds** $\;\to$ Use Weibull($\lambda$,$k$) to generate random $v$ each hour.
	* **Solar irradiance** $\;\to$ Build a simple “bell-curve” over 24 hours (sin-based) adjusted for day length and tilt (plus $\pm$5% cloud noise), not a Weibull.
	.
	Below is a quick summary of each:

---

> [!NOTE]
> My Excel model documentation

### 1. Wind → Weibull

**Weibull?**

Empirical studies have shown that, over an entire year at a given site, the frequency of wind speeds $v$ is well-fitted by a Weibull probability density:

$f(v) \;=\; \frac{k}{\lambda} \Bigl(\frac{v}{\lambda}\Bigr)^{\,k - 1} \exp\!\Bigl[-\bigl(v/\lambda\bigr)^k\Bigr], \quad v \ge 0,$

where
* $\lambda$ is the scale parameter (roughly the average wind speed),
* $k$ is the shape parameter (how peaked the distribution is).

**How to draw hourly $v$:**

We use inverse-transform sampling in Excel or Python:
`= λ_base * ( -LN( RAND() ) ) ^ ( 1 / k_shape )`
which yields a random wind speed in m/s each hour (with `RAND() ∈ (0,1)`).

**Power calculation:**

1.  **Compute raw “physics” power:**
    $P_{\rm phys}(v) \;=\; \tfrac12\,\rho\,A_{\rm swept}\,C_p\,v^3 \;.$
2.  **Normalize** at your chosen “rated wind speed” (e.g. $v_{\rm rated}=13$ m/s) so that $P_{\rm phys}(v_{\rm rated})$ exactly equals your turbine’s nameplate ($P_{\rm rated}$).
3.  **Clamp:**
    * If $v < v_{\rm cut\text{-}in}$, output = 0.
    * If $v_{\rm cut\text{-}in} \le v \le v_{\rm rated}$, output = $P_{\rm rated}\times\bigl(P_{\rm phys}(v)/P_{\rm phys}(v_{\rm rated})\bigr)$.
    * If $v_{\rm rated} \le v \le v_{\rm cut\text{-}out}$, output = $P_{\rm rated}$.
    * If $v > v_{\rm cut\text{-}out}$, output = 0.

Typical cut-in/cut-out values for a 1 MW-class turbine are:

* $v_{\rm cut\text{-}in} \approx 3$ m/s
* $v_{\rm rated} \approx 13$ m/s
* $v_{\rm cut\text{-}out} \approx 25$ m/s

And you scale $A_{\rm swept}\approx3000$ m² per MW of rating as a rule of thumb.

---

### 2. PV → “Sine + Noise” (not Weibull)

Solar irradiance does not follow a Weibull distribution. Instead, you typically generate a realistic hourly profile by:

**Daily/Seasonal Sine Curve**
$G_{\rm hor}[h] = \max\!\Bigl(0,\;G_{\max}\,\sin\!\bigl[\tfrac{\pi}{12}\,(h - 6)\bigr]\Bigr) \times \Bigl(1 \pm \epsilon\Bigr)$
where
* $G_{\max}\approx1000$ W/m² is clear-sky peak irradiance,
* $h\in\{0,1,…,23\}$ is the hour of day,
* The $\sin$-term goes from 0 at 6 AM $\to$ 1 at noon $\to$ 0 by 6 PM $\to$ negative at night (clamped to 0).
* $\epsilon \in[-0.05,+0.05]$ is random cloud noise ( $\pm$ 5%) via `(1 + 0.1*(RAND()-0.5))`.

**Tilt Adjustment (optional)**

If you want “$G_{\rm on\;tilt}$” instead of horizontal:

1.  Calculate daily declination $\delta = 23.45^\circ\,\sin\!\bigl[\tfrac{2\pi}{365}(284 + d)\bigr]$.
2.  Compute hourly elevation $\alpha_{\rm hour} = \arcsin\bigl[\sin\phi\sin\delta + \cos\phi\cos\delta\cos(15(h - 12))\bigr]$.
3.  Set a fixed module tilt $\beta$.
Then
$G_{\rm module}[h] = G_{\rm hor}[h] \times \frac{\sin(\alpha_{\rm hour} + \beta)}{\sin(\alpha_{\rm hour})}.$
(Clamp the ratio to $\ge 0$ so you don’t produce negative irradiance at night.)

**PV Power**

Once you have hourly “tilted” or horizontal irradiance $G$, you compute cell temperature $T_{\rm cell}$ via NOCT, then
$P_{\rm PV}[h] = P_{\rm STC} \times \frac{G[h]}{G_{\rm STC}} \times \bigl[\,1 + \alpha_p\,\bigl(T_{\rm cell}[h] - T_{\rm STC}\bigr)\bigr] \times f_{\rm derate},$
where $P_{\rm STC}$ is the 1 MW rating (for a 1 MW system), $G_{\rm STC}=1000$ W/m², $\alpha_p\approx -0.0035/°\text{C}$, $T_{\rm STC}=25 °C$, $f_{\rm derate}\approx0.90$, and
$T_{\rm cell}[h] = T_{\rm amb}[h] + \frac{\mathrm{NOCT} - 20}{800} \;G[h],$
with $T_{\rm amb}[h]$ from a seasonal sine (plus noise) as previously discussed.

---

### Putting it all together

* **Wind side** $\to$ Implement a Weibull random draw each hour $\to$ clamp to your turbine’s power-curve $\to$ average/accumulate $\to$ get a time series of wind MWh per MW.
* **PV side** $\to$ Use a deterministic sine + noise for irradiance, plus tilt/NOCT corrections $\to$ compute hourly PV output per MW.

You then have two parallel hourly profiles—$P_{\rm wind}[h]$ and $P_{\rm PV}[h]$—each already on a “per MW of nameplate” basis. Those can feed directly into your Monte Carlo run (wind using random Weibull parameters each day, PV using fixed-sine+noise). At the end you’ll get a distribution of annual MWh/MW outputs for each technology and each region.

---

### Example in Excel

**Wind Hourly** (cells on a “Wind+Weibull” sheet):

* **A row 2–8761:** `Hour = ROW()-2`
* **B row 2–8761:** `HourOfDay = MOD(A2, 24)`
* **C row 2–8761:** `DayOfYear = INT(A2/24)+1`
* **D row 2–8761 ($\lambda_{\text{eff}}$):**
    ```excel
    = $X$1                                  ' base λ (m/s)
      * (1 + $X$2 * SIN((C2 - $X$3)/365 * 2*PI()))    ' seasonal mod
      * (1 + $X$4 * SIN((B2 - $X$5)/24  * 2*PI()))    ' diurnal mod
    ```
* **E row 2–8761 (WindSpeed):**
    ```excel
    = D2 * (-LN(RAND()))^(1 / $X$6)     
      ' where $X$6 is k_shape 
    ```
* **F row 2–8761 (P_phys):**
    ```excel
    = 0.5 * 1.225 * (3000) * 0.4 * E2^3 / 1E6
    ```
* **G row 2–8761 (Clamped Output):**
    ```excel
    = IF(E2 < 3, 0, 
        IF(E2 <= 13, F2 / (0.5*1.225*3000*0.4*13^3/1E6), 
           IF(E2 <= 25, 1, 0)
        )
      )
    ```
* **H row 2–8761 (Hourly CF):**
    ```excel
    = G2   ' already “MW per 1 MW” 
    ```

**PV Hourly** (on a “PV+Sine” sheet):

* **A row 2–8761:** `Hour = ROW()-2`
* **B row 2–8761:** `HourOfDay = MOD(A2, 24)`
* **C row 2–8761:** `DayOfYear = INT(A2/24)+1`
* **D row 2–8761 (Declination):**
    ```excel
    = 23.45 * SIN((284 + C2)/365 * 2*PI())
    ```
* **E row 2–8761 (Solar Elevation):**
    ```excel
    = DEGREES(ASIN(
        SIN(RADIANS($X$7)) * SIN(RADIANS(D2))
      + COS(RADIANS($X$7)) * COS(RADIANS(D2)) * COS(RADIANS(15*(B2-12)))
    ))
    ```
    where `$X$7` is your latitude (e.g. 40°).
* **F row 2–8761 (Tilt Ratio):**
    ```excel
    = MAX(0, SIN(RADIANS(E2 + $X$8)) / SIN(RADIANS(E2)))
    ```
    where `$X$8` is your fixed tilt (e.g. 25°).
* **G row 2–8761 (Horizontal Irradiance G₀):**
    ```excel
    = MAX(0, $X$9 * SIN((B2 - 6)/12 * PI())) * (1 + 0.1 * (RAND()-0.5))
    ```
    where `$X$9 = Gmax` (e.g. 1000 W/m²).
* **H row 2–8761 (Tilted Irradiance):**
    ```excel
    = G2 * F2
    ```
* **I row 2–8761 (T_amb): (Seasonal+Noise)**
    ```excel
    = $X$10                             ' T_mean
      + $X$11 * SIN((C2 - 80)/365 * 2*PI())   ' T_amp
      + 2*(RAND()-0.5)
    ```
    where `$X$10=T_mean`, `$X$11=T_amp`.
* **J row 2–8761 (T_cell):**
    ```excel
    = I2 + ($X$12 - 20)/800 * H2
    ```
    where `$X$12 = NOCT` (e.g. 45 °C).
* **K row 2–8761 (PV Output):**
    ```excel
    = 1 * (H2/1000) * (1 + $X$13 * (J2 - 25)) * $X$14
    ```
    where:
    * “1” is your 1 MW rating ($P_{\rm STC}$),
    * `H2/1000` is $G/G_{\rm STC}$ (since $G_{\rm STC}=1000$),
    * `$X$13` = $\alpha_p$ (e.g. –0.0035/°C),
    * “25” is $T_{\rm STC}$,
    * `$X$14` = $f_{\rm derate}$ (0.90).
* **L row 2–8761 (Hourly PV CF):**
    ```excel
    = K2   ' “MW per 1 MW”
    ```

**Aggregate**

On each sheet you now have an hourly CF time series (“Wind CF” in H2:H8761, “PV CF” in L2:L8761). You can sum or average these 8,760 rows to get annual MWh / MW or annual capacity factor for that one simulation run:

* **Annual Wind CF:**
    `= SUM('Wind+Weibull'!H2:H8761)/8760`
* **Annual PV CF:**
    `= SUM('PV+Sine'!L2:L8761)/8760`

**Monte Carlo Loop**

If you want a distribution of 1,000 annual CFs, copy the entire “Wind+Weibull” and “PV+Sine” blocks to the right 999 times (so you have 1,000 separate hourly simulations).
At the bottom of each block, compute that block’s annual sum/average into a single cell.
Stack those 1,000 annual CFs in a vertical column on a new tab (call it “Results”).

**Summary Statistics** (on the “Results” tab)

Let’s say your 1,000 annual PV CFs are in `Results!$A$2:$A$1001`. Then:

* **Mean:** `=AVERAGE($A$2:$A$1001)`
* **Median:** `=MEDIAN($A$2:$A$1001)`
* **StdDev:** `=STDEV.P($A$2:$A$1001)`
* **5th Percentile:** `=PERCENTILE.EXC($A$2:$A$1001, 0.05)` (or `PERCENTILE.INC`)
* **25th Percentile:** `=PERCENTILE.EXC($A$2:$A$1001, 0.25)`
* **75th Percentile:** `=PERCENTILE.EXC($A$2:$A$1001, 0.75)`
* **95th Percentile:** `=PERCENTILE.EXC($A$2:$A$1001, 0.95)`

Similarly, if your 1,000 annual wind CFs are in `Results!$B$2:$B$1001`, compute those stats in another column.

**Charting**

* **Histogram (Density Plot):**
    * Select your 1,000 annual PV CFs (`Results!$A$2:$A$1001`) $\to$ Insert ▸ Histogram Chart $\to$ in Format Axis set your bin width (e.g. 0.01).
    * Repeat for the 1,000 wind CFs (or overlay them by copying one series onto the other chart and setting bar overlap).
* **Box & Whisker:**
    * If you put PV CFs in column A and Wind CFs in column B, select both sets (`$A$2:$A$1001,$B$2:$B$1001`) $\to$ Insert ▸ Box & Whisker Chart.
    * Likewise for each region—just select the vertical column of CFs for TX, CA, and GP to get three side-by-side boxes.
* **Violin Plot (Workaround):**
    As described previously, create a small “bin/density” table (Bins in Column D, Density in E, Mirrored in F) then Insert ▸ Scatter with Smooth Lines $\to$ format so the two curves fill to look like a violin.

---

### Final Notes

* **Weibull for Wind only:**
    Yes—“Custom Wind + PV” means you use Weibull draws for each hour’s wind speed. For PV, keep using your sine-plus-noise approach (and tilt adjustments if desired).
* **Monte Carlo Runs:**
    In Excel, each “run” is accomplished by copying the entire block of hourly formulas rightward (because `RAND()` recalculates on each copy). Then you scrape off the final annual CF from each block into a single vertical list to build your distribution.
* **Speed tip:**
    If you only need a few hundred simulations, you can paste the entire sheet as values to “lock in” random draws before dragging a new copy. That way you don’t have 10,000 `RAND()` functions all recalculating every time you change a cell.

Once all the pieces are in place—Weibull wind, sine-based PV, clamped power, annual CF, and 1,000+ runs—you’ll have a fully Excel-native Monte Carlo setup. You can then produce exactly the histograms, box-and-whiskers, and percentile tables you saw in the video, all without leaving Excel.

If any formula or chart step needs extra detail, let me know!
