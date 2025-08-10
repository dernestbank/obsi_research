


Fitting Curves 
target NREL

Target Astraini @ Hysupply
@astrianiOptimalPlanningRenewable2024

PEM cost module:

`IEA stated that cost for PEM electrolyzer in 2020 is around $1400-1700/kW and will be decreased to around $440–500 in 2030 projects and around $300 under net zero energy (NZE) scenario in 2050. The electrolyzer cost in this study is based on the cost curve presented in Ref. [19], which used a 10 MW electrolyzer cost as the baseline for the projection. the price of electrolyzer is adjusted refer to the report in Ref. [52], i.e., $1752 per kW electrolyzer.`
The fitting model
![[Pasted image 20250324194911.png]]
‘fitnlm’ Matlab command, the values of constant and coefficients c1, c2, c3, and c4 are retrieved and their values are 1046.931, -3.479, 2061.567, and -0.261, respectively.
@GreenHydrogenCost2020
![[Pasted image 20250325193020.png|500]]



![[Pasted image 20250325195616.png]]

@rekstenProjectingFutureCost2022
$$
C = \left(k_0 + \frac{k}{Q} Q^{\alpha} \right) \left( \frac{V}{V_0} \right)^{\beta}
$$
where C is the electrolyser plant cost pr kW, k0 and k are fitting constants, Q is the electrolyser plant capacity and V and V0 are plant installation year and reference year, respectively. a and b are fitting constants and usually referred to as a scaling factor and learning factor,



<mark style="background: #FF5582A6;">I will fit this to my own data</mark>
and compare my data to other models

Fitted parameters (with 95% confidence intervals):
c1 = 1200.253 ± 1660.658
c2 = -0.006 ± 0.035
c3 = 16990.394 ± 5529.687
c4 = -0.010 ± 0.011
R^2 = 0.5378
RMSE = 4148.15

Assuming 10% uncertainty in cost measurements


## Comparing fitting Models

1. **Linear**:
   $$
   \text{Cost}(P) = a + bP
   $$

   This is the simplest approach. If your data covers a narrow range or if you suspect nearly linear scaling, it might suffice.

2. **Power-Law**:
   $$
   \text{Cost}(P) = \alpha P^{\beta}
   $$
   Captures economies of scale if $\beta < 1$. Watch out for zero or negative capacities.

3. **Exponential**:
   $$
   \text{Cost}(P) = c_1 + c_2 P + c_3 e^{c_4 P}
   $$
   Useful if you see cost behavior that cannot be captured well by polynomial or power-law forms.




# the investment cost of RE plants





## 1. Power Law Scaling (Economies of Scale)

**Equation:**

$$
\text{CapEx}_{\text{PV}} = a \cdot C^b
$$

- **CapEx**: Capital cost (\$)
- **C**: System capacity (kW or MW)
- **a**: Baseline cost coefficient (\$/kW or \$/MW)
- **b**: Scaling exponent (typically \( b < 1 \), reflecting economies of scale)

**Example:**

For utility-scale PV (\( C > 1\,\text{MW} \)):

$$
\text{CapEx} = 800 \cdot C^{0.92} \;\$/\text{kW} \quad \text{[NREL, 2023]}
$$

This implies an **8% cost reduction** for every doubling of capacity.



## 2. Learning Curve Model (Cost vs. Cumulative Capacity)

**Equation:**

$$
\text{CapEx}(t) = \text{CapEx}_0 \cdot \left( \frac{Q(t)}{Q_0} \right)^{-b}
$$

- **CapEx(t)**: Cost at time \( t \)  
- **\( Q(t) \)**: Cumulative installed capacity at time \( t \)  
- **$( \text{CapEx}_0, Q_0 )$**: Initial cost and capacity  
- **\( b \)**: Learning rate (historically ~20% for PV)

**Source:** Wright’s Law, applied in studies like *Barbose et al. (2021)* and *IRENA (2024)*.



## 3. Levelized Cost of Energy (LCOE)

**Equation:**

$$
\text{LCOE} = \frac{\text{CapEx} \cdot \text{CRF} + \text{OpEx}}{\text{Annual Generation}}
$$

- **CRF**: Capital recovery factor  
  $$
  \text{CRF} = \frac{r(1+r)^n}{(1+r)^n - 1}
  $$
  where \( r \) = discount rate, \( n \) = system lifetime

- **Annual Generation**:  
  $$
  C \cdot \text{CF} \cdot 8760
  $$
  where CF = capacity factor

**Source**: Standardized in *NREL’s Annual Technology Baseline* reports.


## Cost Analysis of Renewable Energy Systems: Wind and Solar PV

## **Capital Costs**

## Wind Energy

- **Onshore Wind Turbines**: The capital cost is approximately $1.3 million per megawatt (MW). For a typical 2-3 MW turbine, this amounts to $2.6–$4 million per turbine. Offshore turbines can cost significantly more due to their larger size and installation complexity, ranging up to $18 million for 16-18 MW turbines[1](https://weatherguardwind.com/how-much-does-wind-turbine-cost-worth-it/)[5](https://williamkamkwamba.com/how-much-wind-turbine-costs/).
    
- **Additional Costs**: Site preparation ($200,000–$400,000), grid connection ($150,000–$500,000), logistics ($60,000–$120,000), installation and commissioning ($300,000–$500,000), and other expenses like permitting and insurance[5](https://williamkamkwamba.com/how-much-wind-turbine-costs/).
    

## Solar PV Systems

- **Utility-Scale Systems**: The capital cost for large-scale solar PV systems is approximately $51/MWh, while smaller systems cost around $149/MWh[4](https://pmc.ncbi.nlm.nih.gov/articles/PMC10201302/).
    
- **Cost Breakdown**: Includes modules, inverters, energy storage systems (if applicable), structural and electrical balance of system components, fieldwork, office work, and other costs[8](https://www.energy.gov/eere/solar/solar-photovoltaic-system-cost-benchmarks).
    

## **Operational Costs**

## Wind Energy

- Annual operational costs range from $42,000 to $48,000 per turbine or about 1-2 cents per kilowatt-hour (kWh) produced. Offshore wind farms typically incur higher maintenance costs due to accessibility challenges[1](https://weatherguardwind.com/how-much-does-wind-turbine-cost-worth-it/)[6](https://weatherguardwind.com/wind-turbine-cost-and-roi-considerations-in-2023/)[9](https://www.osti.gov/servlets/purl/1544993).
    

## Solar PV Systems

- Operational costs are relatively lower than wind energy. Maintenance strategies include inverter replacements and cleaning panels periodically. Variability costs for solar PV are estimated at $8–11/MWh due to fluctuations in solar radiation[10](https://www.cmu.edu/ceic/assets/docs/publications/working-papers/ceic-11-04.pdf).

## **Market Price of Power**

## Wind Energy

The market value of wind power varies between 50% and 80% of the average power price depending on penetration rates. High penetration reduces prices due to oversupply during windy periods[3](https://d-nb.info/1166861082/34)[7](https://neon.energy/Hirth-2013-Market-Value-Renewables-Solar-Wind-Power-Variability-Price.pdf).

## Solar PV Systems

Solar PV electricity costs range from $51/MWh for large-scale systems to $149/MWh for smaller installations. Prices are location-dependent due to solar irradiance variability[4](https://pmc.ncbi.nlm.nih.gov/articles/PMC10201302/)[10](https://www.cmu.edu/ceic/assets/docs/publications/working-papers/ceic-11-04.pdf).

## **Variability Across Locations**

Both wind and solar energy exhibit significant variability:

- **Wind Energy**: Prices fluctuate based on wind speeds; higher variability leads to lower market prices during peak production periods[3](https://d-nb.info/1166861082/34)[7](https://neon.energy/Hirth-2013-Market-Value-Renewables-Solar-Wind-Power-Variability-Price.pdf).
    
- **Solar PV**: Solar radiation variability impacts generation costs more in regions with less consistent sunlight. Variability adds approximately $8–11/MWh to solar PV costs[10](https://www.cmu.edu/ceic/assets/docs/publications/working-papers/ceic-11-04.pdf).
    

These findings highlight the importance of location-specific assessments for renewable energy projects to optimize costs and performance.

## **Notable Papers & Reports**

1. **NREL (2023)**: _"U.S. Solar Photovoltaic System and Energy Storage Cost Benchmarks"_
    
    - Provides power-law scaling factors for residential, commercial, and utility-scale PV.
        
    - [Link](https://www.nrel.gov/docs/fy23osti/85332.pdf)
        
2. **IRENA (2024)**: _"Renewable Power Generation Costs in 2023"_
    
    - Global dataset linking capacity to costs, with learning curves for PV.
        
    - [Link](https://www.irena.org/publications)
        
3. **Lazard (2024)**: _"Levelized Cost of Energy Analysis"_
    
    - Compares LCOE ranges for PV across capacities (e.g., utility-scale: $24–$96/MWh vs. residential: $117–$282/MWh).
        
4. **Jäger-Waldau et al. (2022)**: _"PV Learning Curves: Historical Analysis of Market and Technology Drivers"_ (Energy Policy)
    
    - Quantifies cost reductions from R&D and economies of scale.


C
