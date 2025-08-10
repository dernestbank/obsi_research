




Scope of Analysis and Inputs
4.1.System Boundary

![[HS-. System boundary for Version 1 of the cost tool..png]]



― Process for Extracting Additional Solar and Wind Traces from Renewable Ninja:
Additional Solar and Wind traces can be extracted using Renewables Ninja
(https://www.renewables.ninja/). Requests for data can be made anonymously or by registering 
for a free account within the website. Anonymous users are limited to 5 retrieval requests per day
for data from the year 2014, whereas registered users are limited to 50 retrieval requests per hour
for data between 2000-2019.

, as 
well as a choice between MERRA-2 (global data) and CM-SAF SARAH (European data) data 

Sites can be selected either by entering the location name, by latitude and longitude, or by dropping a pin on the map.

![[Figure 24 Renewable Ninja User input Fields.png|395x403]]


For solar PV, user inputs can be made for:
• Capacity (kW) – the default input is 1 kW. The data retrieved from Renewables Ninja in 
the HCAT tool uses a capacity of 1000 kW.
• System Loss (fraction) – the default input is 0.1. The data retrieved from Renewables Ninja 
in the HCAT tool uses a system loss of 0.
• Tracking – tracking setups will be dependent on the specific project parameters of the 
solar farm. The data retrieved from Renewables Ninja in the HCAT tool uses single axis 
tracking.
o Fixed tilt (None)
o 1-axis (azimuth)
o 2-axis (tilt and azimuth)
• Tilt (°) – This field defines how far a panel is inclined from the horizontal plane. If using a 
fixed tilt system (no tracking), the tilt of the system should be equal to the latitude of the 
site in order to maximise the solar farm’s yield. For single and dual axis tracking, setting a
tilt angle in this field will not affect the yield.
• Azimuth (°) – This field defines the compass direction in which the solar farm is facing. To 
maximise yields in the southern hemisphere, solar farms should be facing north, defined 
by 180° in Renewables Ninja. To maximise yields in the northern hemisphere, solar farms 
should be facing south, defined by 0° in Renewables Ninja. 

For Wind, user inputs can be made for:
• Capacity (kW) – the default input is 1 kW. The data retrieved from Renewables Ninja in 
the HCAT tool uses a capacity of 1000 kW.
• Hub height (m) – this field defines the height of the turbine’s tower and will be dependent 
on the specific turbine model that will be used on the wind farm
• Turbine Model – this field allows for the selection of the make and model of the wind 
turbines. Model names typically will include the manufacturer, the blade diameter in 
meters, and the rated capacity in kW or MW.


Once all fields have been defined, clicking on run will begin the retrieval process and clicking 
on “Save hourly output as CSV” will allow for the downloading of the data.

4.2.3. Power Plant Configuration
The HySupply Cost Analysis Tool allows the user to model the electrolyser operation based on 
certain the power plant configuration scenario. These scenarios allow for the choice between a 
Solar PV, Wind or Hybrid power plant which can be standalone (within the system boundary) or 
outsourced (via a power purchase agreement).
These configurations for the electrolyser-power 
plant are summarised below.
 C1. Standalone Solar PV Generator with Electrolyser
 C2. Standalone Solar PV Generator with Electrolyser and Battery
 C3. Grid Connected Solar PV Generator with Electrolyser 
 C4. Grid Connected Solar PV Generator with Electrolyser with Surplus Retailed to Grid
 C5. Grid Connected Solar PV Generator with Electrolyser and Battery
 C6. Grid Connected Solar PV Generator with Electrolyser and Battery with Surplus Retailed 
to Grid
 C7. Solar PPA with Electrolyser 
 C8. Solar PPA with Electrolyser and Battery 
 C9. Standalone Wind Generator with Electrolyser
 C10. Standalone Wind Generator with Electrolyser and Battery
 C11. Grid Connected Wind Generator with Electrolyser 
 C12. Grid Connected Wind Generator with Electrolyser with Surplus Retailed to Grid
 C13. Grid Connected Wind Generator with Electrolyser and Battery 
 C14. Grid Connected Wind Generator with Electrolyser and Battery with Surplus Retail to 
Gird
 C15. Wind PPA with Electrolyser 
 C16. Wind PPA with Electrolyser and Battery 
 C17. Standalone Hybrid Generator with Electrolyser
 C18. Standalone Hybrid Generator with Electrolyser and Battery
 C19. Grid Connected Hybrid Generator with Electrolyser 
 C20. Grid Connected Hybrid Generator with Electrolyser with Surplus Retailed to Grid
 C21. Grid Connected Hybrid Generator with Electrolyser and Battery 
 C22. Grid Connected Hybrid Generator with Electrolyser and Battery with Surplus Retailed 
to Grid
 C23. Hybrid PPA with Electrolyser 
 C24. Hybrid PPA with Electrolyser and Battery


The above scenarios can be categorised into the following configurations.
― Standalone Configuration: 
For the standalone system, the renewable power plant is assumed to be built within the 
boundary of the electrolyser facility. The key features of this scenario are:
 The electricity output from the power plant is used directly by the electrolyser to generate 
hydrogen and any surplus is either stored in the battery or curtailed.


― Grid Configuration: 
As an alternate to the standalone system, the renewable power plant can also be connected 
to the electrolyser through the grid. In this case it is assumed that the power plant is built at 
a different site, while the electricity to drive the electrolyser is supplied using the grid. The key 
features of this scenario are:
 The electricity output from the power plant is used directly by the electrolyser to generate 
hydrogen and any surplus is either stored in the battery or retailed to the grid.
 Additional cost of grid connection and grid service charges (e.g., Transmission use of 
system charges) are added as additional upfront capital and ongoing operating costs.
 If the option to retail the surplus is chosen from the configuration drop down list, the user 
can provide a spot price to evaluate the surplus electricity sales. The option is available 
in the ‘S1. Inputs’ Sheet as shown in Figure
 For this scenario the capital and operating costs of the power plant and the electrolyser 
are directly passed on to the project proponent (appearing in the cash flow statement).
The configuration options: C3-C6, C11-C14 and C19-C22 fall in the grid connected categories.

― PPA Configuration:
The third option is to purchase the electricity from a 3rd Party a through a Power Purchase 
Agreement (PPA). The key features of this scenario are:
 The generator type, capacity and the generation profile of the power plant are defined by 
the user. Elaborated in Section 4.3. (below)
 The PPA could ether include only the electricity to drive the electrolyser or include 
additional electricity to charge the battery (depending on the choice from the 
configuration drop down list)
 The electricity sourced is then costed as a fixed unit cost of electricity (A$/MWh), that is 
defined by the user. 
The configuration options: C7-C8, C15-C16 and C23-C24 fall in the PPA category.


4.5. Power Plant Parameters
4.5.1.Power Plant Capacity and Operating Parameters
 Degradation Rates of Solar PV and Wind Farm (%): Similarly, to the electrolyser, the user 
can also define the degradation rate of the solar and wind farms. This input is provided as a 
percentage reduction in output and is multiplied by the capacity factor figures to get the power 
plant output per unit capacity for each hour of each year. Note: For the hybrid scenario, the 
degradation rate should be provided for both the solar and wind farm. This function will be 
further improved after engagement with stakeholders. 


- Power Plant Indirect Cost: The power plant indirect costs include the cost of land and 
EPC. In the tool, the user is provided the option to define these values as a percentage of 
the individual solar/wind power plant CAPEX. 
 Hybrid Power Plant Costs: In case the hybrid power plant is chosen, the aggregate of the 
capital of the individual solar and wind farm proportional to their share in the total capacity 
of the hybrid power plant is taken to represent the capital costs of hybrid systems (Eq. 3).


 Here, 𝐶𝐶𝑆𝑆 is the cost component of solar farm, 𝐶𝐶𝑊𝑊 is the cost component of the wind farm, 
while 𝑃𝑃𝑠𝑠 is the capacity of the solar PV in the hybrid system, and 𝑃𝑃𝑤𝑤 is the capacity of the 
wind farm. The cost components can either be represented by the total capital cost 


