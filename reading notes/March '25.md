Papers read and refs
@astrianiOptimalPlanningRenewable2024
@kimTechnoeconomicAnalysisAnion2024




3/32025
Optimal planning of renewable energy park for green hydrogen production using detailed cost and efficiency curves of PEM electrolyzer. @astrianiOptimalPlanningRenewable2024

obj:       optimizing three scenarios photo-voltaic PV, wind-only and PV-wind for green hydrogen in different locations with different RE potentials.
selecting suitable location
optimum size ratio ratio

#MyQuestion
```where in the us is a potential Renewable energy parks
searching for highest average wind speed and lowest irradiance level.
```

Lit review and conclusions
the utilization of a proton exchange membrane (PEM) electrolyzer becomes cost-effective when it operates with at least 3000–6000 full load hours annually [4].
offshore wind have higher wind speed  ~ costeffective[11]
wind power xould have large output during nighttime, and PV as buffer in the daytime[4].
hybrid PV-wind is costeffectie compared to PV-only or Wind-only
the cost for a small scale electrolyzer is around $13,333-33,333/kW, while for a largescale electrolyzer, the cost is around $1500-3800/kW [18].
IRENA also stated that, in addition to the projection cost, when the capacity of the electrolyzer increases from 1 MW to 20 MW, the cost of the electrolyzer decreases by over a third [19].
the electrolyzer’s efficiency increases with a higher operating temperature and more effective heat exchangers but decreases as the electrolyte membrane thickness and the inlet H2O flow rate increase.
electrolyzer’s efficiency curves have been presented with its current density in Ref. [21] and its loading percentage
RE based power plants will have a flutating output power. the distribution of solar irradiation will reach it's peak intensity 4 h, ie 11 to 2 pm everyday. also solar irradiation differs every month.


A nonliner regression method to determine the electrolyzer costs and efficiency models.
this study investigated the complementarity between PV and wind power as the supply for PEM electrolyzer to produce hydrogen

a. a PV-only system producing hydrogen is simulated and analyzed to get its optimal sizing of the PV plant and electrolyzer.

b. same is applied to wind power at same location


Contributions
model of electrolyzer system efficiency vrs operating power
investment cost against capacity
LCOH vrs wind, PV pant capacity characterisitc cureve
Hydrogen production of fixed efficinecy vrs dynamic efficiency.
location and cost variation impact to LCOH.

to have an accurate ratio between PV and wind power sizes, a larger search space vector is employed; thus, the second optimization employs one of the stochastic methods known as particle swarm optimization (PSO).

sensitivity of LCOH with electricity tariffs, electrolyzer cost

quotes`

`A RE park is an area that is dedicated to the deployment of RE utilization. It may only consist of one RE resource, such as a solar farm, or multi-RE resources, such as a solar wind farm.` @astrianiOptimalPlanningRenewable2024

electroolyzer accepts only DC current - therefore a power invertor is needed


Ref. [27] has reviewed the trend of direct seawater electrolysis technologies from the patent documents listed in the Derwent Innovations Index database from 1963 to 2022. It found that there was a significant increase in the listed patents between 2016 and 2021, with most of them focused on developing new electrolytic systems and corrosion-resistant electrocatalysts.
In terms of the operating pressure, although a PEM electrolyzer can be operated under differential pressure, it requires around 15 min in its initial operation to stabilize the pressure using the regulating valve [34].


equations
The total RE plants output power at the hour h, year y (PRE,h,y) is
$P_{RE, h,y}= P_{PV}+ P_{WT}$

upstream grid ($P_{import,h,y}$)
$P_{import} = P_{EL, rated} \times 0.05 - P_{RE}$
the electrolyzer is assumed to continue to be operated at 5–100% of its rated power.

, if PRE,h,y higher than the electrolyzer’s rated power (PEL,rated), the RE park will export its excess power (Pexport,h,y )
$P_{export}= P_{RE} - P_{EL}$ 

PV plant modeling
PV output power (P_PV)
$$
P_{PV,hY} = P_{PV,rated} f_{derPV,y} \frac{GTI_h}{G_{STC}} \left( 1 + k_p \left( T_{PV}^{h} - T_{STC} \right) \right) P_{losses}
$$

$P_{PV,rated}$ is the PV plant-rated power (kW),
$f_{der,PV}$ is the derating factor of the PV module which increases annually,,
GTI (global tilted irradiance) is the solar irradiation intensity (kW/m2) falls to the tilted PV module,
GSTC is the constant of solar irradiation under standard test condition (STC), i.e., 1 kW/m 2,
kP is the coefficient of temperature affecting PV output power (%/oC),
$T_{PV}$ is the PV module temperature (C),
T_STC is the constant of module temperature in STC (25oC),
P_losses,PV is the losses that occurred in the PV plant as the sum of losses due to PV inverter efficiency, power dissipation through the cables,
h, y represent the index of hour and year respectively.

The #online available data usually provide irradiance profiles in global horizontal irradiance (GHI) value. Therefore, it is needed to calculate the radiation incident on the tilted PV module surface [38] to obtain the GTI values from GHI data
$$
GTI = GHI \frac{\sin(\sigma + \theta)}{\sin \sigma}
$$

where $\sigma$ is the elevation angle, and $\theta$ is the tilt angle of the PV module. Meanwhile, $\sigma$, as described in Ref. [39], is defined in (6) and (7).

$$
\sigma = 90 - \varphi + \delta
$$

$$
\delta = 23.4 \cos \left( \frac{360}{365} (d + 284) \right)
$$
where φ is the latitude of the considered location, δ is the declination angle, and d is the index of the day (e.g., 1st of January equal to 1).

the PV module temperature
the online available data related to temperature is the ambient temperature (Tambient)

![[image.png]]

Wind power modeling.

$$
P_{WT} = 0.5 \eta_{WT} \rho A C_p(\lambda, \beta) v^3
$$
`where ρ is air density (1.23 kg/m3), A is the wind turbine’s blades swept area (m2), ηWT is wind turbine’s mechanical (drive train and gearbox) efficiency, and Cp is the power coefficient of the wind turbine. Cp is a function of the tip speed ratio (λ) and degree of pitch angle (β)
.` A wind turbine will not produce power when the wind speed at the current time step is smaller than the cut-in wind speed or bigger than the cut-out wind speed. If the wind speed lies from vr to vs, the wind output power will equal to Pr. When v lies from vc to vr, with the assumption that ρ, A, and Cp are constant values, then the output power of the wind turbine as a function of v is defined in (10) [42]
$$
P_{wt} =
\begin{cases} 
    0, & v < v_c, \ v > v_s \\
    P_{wt}(v), & v_c \leq v \leq v_r \\
    P_{WT,rated}, & v_r \leq v \leq v_s
\end{cases}
$$
A polynomial model for the wind power curve can be represented in (11).
$$
P_{wt}(v) = k_j v^j + k_{j-1} v^{j-1} + \dots + k_1 v + k_0
$$


Electrolyzer.

The efficiency of PEM = $\frac{HHV}{E_{EL}}$

Electrolyzer efficiency against operating power.
based on the electrolyzer efficiency curves presented in a report [22] and studies @buttlerCurrentStatusWater2018  @liponiTechnoeconomicAnalysisHydrogen2022 ,
![[Pasted image 20250324192458.png|400]]
$$
\eta_{EL,h} = b_1 + b_2 P_{EL,\text{rated}} + b_3 \, e^{\left(b_4 \frac{P_{EL,h}}{P_{EL,\text{rated}}} \times 100\right)}
$$


PEl is the power supplied to the electrolyzer (W), PEl,rated is the electrolyzer rated power (W), while b1, b2, b3, b4 are the constant and coefficients of an exponential model.
The values of b1, b2, b3 from the curve in Fig. 4 are 103.561, 0.329, 101.909, and 0.102, respectively.
![[Pasted image 20250324192841.png|400]]

The amount of produced hydrogen (mH2,h,y)
$$
m_{H_2,h,y} = \frac{\eta_{El,h} P_{EL,h}}{HHV_{H_2} f_{der,El,y} \ n}
$$


PEM cost module:

`IEA stated that cost for PEM electrolyzer in 2020 is around $1400-1700/kW and will be decreased to around $440–500 in 2030 projects and around $300 under net zero energy (NZE) scenario in 2050. The electrolyzer cost in this study is based on the cost curve presented in Ref. [19], which used a 10 MW electrolyzer cost as the baseline for the projection`
The fitting model
![[Pasted image 20250324194911.png]]
‘fitnlm’ Matlab command, the values of constant and coefficients c1, c2, c3, and c4 are retrieved and their values are 1046.931, 3.479, 2061.567, and 0.261, respectively.

`cost of RE:`
the investment cost of RE plants as well as their operational and maintenance costs in this research are based on the report in Ref. [52].
large-scale PV is $1011/kW, and for an onshore wind power plant, it is $1763/kW. Operation and maintenance costs for large-scale PV and onshore wind are $11.3/kW and $16.7/kW, respectively. Moreover, this study uses 2% of its capital costs annually for the electrolyzer operation and maintenance costs [53].
![[Pasted image 20250324195326.png|400]]

n is a constant value 11.126 that is needed to convert hydrogen notation from Nm3 to kg.

$$
LCOH = \frac{\sum\limits_{y=1}^{Y} \left( C_{invest}^y + C_{O\&M}^y + C_{water}^y + C_{ET}^y \right) / (1 + r)^y}
{\sum\limits_{y=1}^{Y} m_{H_2}^y / (1 + r)^y}
$$

$$
EL_{fullloadhour} = \frac{\sum\limits_{h=1}^{HY} P_{EL,h,y} / P_{EL,rated}}{HY}
$$

where $C_{invest}^y + C_{O\&M}^y + C_{water}^y + C_{ET}^y$  are investment, operating and maintenance, water, and energy transfer costs, respectively
Y is the project lifetime, i.e., 20 years; H is the number of hours in a year,i.e., 8760 h, and r is the discounted rate, i.e., 8%. 
In addition, for the Cywater, CyO&M, and CyET, a yearly inflation rate of 2% will be included in the LCOH calculation.




Sensitivity analysis

1. Electrolyzer efficiency models for hydrogen production
2. Sizing optimization in locations with different RE resources characteristic



refs
power (PPV) is defined as given in (4) as presented in Ref. [37]
calculate the radiation incident on the tilted PV module surface [38] to obtain the GTI values from GHI data
where σ is the elevation angle, and θ is the tilt angle of the PV module. Meanwhile, σ as described in Ref. [39] is defined in (6) and (7).
Based on the data of ambient temperature, GHI, and wind speed (v), the PV module temperature can be predicted as shown in (8) [40]:

[37] Khattak S, Yousif M, Hassan SU, Hassan M, Alghamdi TAH. Techno-economic and environmental analysis of renewable energy integration in irrigation systems: a comparative study of standalone and grid-connected PV/diesel generator systems in Khyber Pakhtunkhwa. -e31025 Heliyon 2024;10(10):e31025. https://doi.org/10.1016/j.heliyon.2024.e31025. 
[38] Cajethan N, Uchenna UC, Theophilus M. Wind-solar hybrid power system for rural applications in the south eastern states of Nigeria. Journal of Electrical Systems 2012;8(3):304–16.
[39] El Mghouchi Y, El Bouardi A, Choulli Z, Ajzoul T. Models for obtaining the daily direct, diffuse and global solar radiations. Renew Sustain Energy Rev 2016;56: 87–99. https://doi.org/10.1016/j.rser.2015.11.044.
[40] Migan-Dubois A, Badosa J, Obaldía FC, Atlan O, Bourdin V, et al. Step-by-step evaluation of photovoltaic module performance related to outdoor parameters: evaluation of the uncertainty. In: 44th IEEE photovoltaic specialists conference. Washington, United States: IEEE-PVSC); Jun 2017. p. 626–31. https://doi.org/10.1109/PVSC.2017.8366615.




## Take aways, ideas, inspiration
optimization of MEA components. thickness
cost component driven by DFMA
Scenario of PV power vrs wind vrs Grid electricity
distributed vrs Centralized system under RE
comparing different optimization method ( PSO, NSGAII,)

oxygen and without oxygen
alternate materials





---

@kimTechnoeconomicAnalysisAnion2024

![[Pasted image 20250307070817.png|300]]
water transportation across the membrane (𝑛𝑡𝑟𝑎𝑛𝑠 𝐻2𝑂 ) occurs due to (1) the diffusion of water, (2) the pressure gradient at the two interfaces between the membrane and the catalysts, and (3) the electro-osmotic drag within the membrane.




