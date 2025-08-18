## 2. User Manual
2.1.Outline
The current iteration of the HySupply Cost Analysis tool comprises of ten worksheets. The first 
three sheets are the Project Title, Project Description, and the Index. The Inputs sheet is the 
primary sheet that is used to define the variables to be used for analysis. This sheet also contains 
the ‘Calculate’ button which must be used each time the inputs are changed to run the analysis. 
The Results sheet presents the outcomes of the model. The next four sheets contain the 
Levelised Cost Analysis, Cash Flow Analysis, Raw Data and Working Data. These sheets 
are for calculations and data only, and do not contain any inputs apart from the option to add user￾defined generation traces. The Electrolyser Parameters sheet allows the user to adjust the 
electrolyser operating profile. The tool worksheet data flow is represented below in Figure 2

![[Figure 2 Hysupply cost Analysis tool worksheet data flow.jpg]]

Figure 2. HySupply Cost Analysis Tool Worksheet Data Flow

2.2. Quick start guide
The tool opens by automatically loading the Index sheet. The Index sheet summarises the 
functionality of each of the sheets and hyperlinks are provided to each sheet (activated by clicking 
on the sheet number). The tool inputs are stored in the 'S1. Inputs’ sheet. Each input relevant to 
key aspects of the tool have been summarised under a pertinent heading to assist the user in 
navigating the tool (e.g. all electrolyser-based parameters are grouped under the “Electrolyser 
Parameter” heading), as shown in Figure 3. The user can choose a location from the drop-down 
list or enter their own hourly electricity generation data in the ‘Raw Data’ sheet (further explained in Section 3). The project scale should be entered as the electrolyser nominal capacity in MW. A 
table has been included in the far right of the Inputs sheet to show the suggested MW capacity 
for a certain annual hydrogen production. Next, select from the options for the Power Plant 
Configuration. This cell contains a dropdown with the configurations that can be modelled. This 
includes a solar only, wind only or hybrid (solar and wind) generator as well as options for a 
battery, retailing of excess generation or a PPA. Depending on the selection, different cells may 
become grey to indicate they will not be used in the model. Change the orange ‘inputs’ cells and 
then click the red ‘Calculate’ button. This will start the calculation of the annual hydrogen 
production and cash flows which can take a few minutes to process. The user will then be 
automatically taken to the ‘S2. Results’ sheet which provides a summary of the results in both 
tabular and graphical formats.

![[Figure 3 The S1 inputs.jpg]]
Figure 3. The S1. Inputs sheet

The outputs are given in a table on the ‘S2. Results’ sheet, as in Figure 2 below. Additional 
figures detailing capacity factors, duration curves and cost breakdowns are included in the results.
These figures are explained in Section 3.

![[Figure 4 The outputs section of the results sheet.jpg]]

Figure 4. The outputs section of the Results sheet.


-----


## 3. Worksheets

P1. Project Title
Introduces the project including the project name, developers, acknowledgements, affiliations and 
copyright information.

P2. Project Description
Provides a summary of the tool including the project statement, project scope, tool competencies 
and methodology.

Index
Contains the table of contents and a key for the colour coding used throughout the workbook
(Figure 6).

![[Figure 6 The contents of the tool as defined in sheet  _Index_.jpg]]
Figure 6. The contents of the tool as defined in sheet 'Index'.


S1. Inputs
This sheet is where the majority of the model inputs are stored. The inputs are separated into 
separate categories for the system sizing, electrolyser, power plant, battery, and financing. Each
input has a name, value, unit, notes and default value. The defaults are suggested values and 
some of these may depend on a formula such as the battery costs which vary with the duration 
of storage. Note: Once all of the parameters are defined, please click the “Calculate” button to 
activate the calculation. The calculations may take a few minutes, and once the calculation is 
complete the user will be automatically taken to the Results sheet. If changes are made to the 

![[Figure 7 The scope and system sizing sections of  sheet _S1 inputs_.jpg]]
Figure 7. The Scope and System Sizing sections of sheet 'S1. Inputs'

S2. Results
The Results sheet provides a concise summary of the model’s key inputs and results (Figure 4), 
represented as a table with the following parameters.
The summary of the key inputs include:
 Location: The location selected from the dropdown list in the inputs sheet.
 Configuration: which represents the configuration of the power plant and electrolyser 
operation (also based on the selection from the drop-down list in the inputs sheet).
 Electrolyser Capacity: the capacity of the electrolyser is translated over from the inputs
sheet, based on the nominal capacity defined by the user.
 Power Plant Capacity: the capacity of the power plant is copied from the inputs sheet, based 
on the nominal capacity defined by the user.
 Battery Capacity: if the battery is included in the model, then the capacity of the battery is 
translated over from the inputs sheet based on the nominal capacity defined by the user.

The summary of the key results include:
 Power Plant Capacity Factor (%): The power plant capacity factor is evaluated as the ratio 
of the total energy that the power plant generates over the year to the energy the power plant 
would generate if it operated at full capacity. This capacity factor is evaluated based on the 
solar and wind traces. Note: If a battery is included in the model, the effect is included in the 
results for the electrolyser rather than the power plant.
 Time Electrolyser is at its Maximum Capacity (% of 8760 hrs/yr): represents the number 
of hours in a year that the electrolyser operates at its maximum capacity (which is defined by 
the user in the Inputs sheet), as a percentage of the total hours in a year.
 Total Time Electrolyser is Operating (% of 8760 hrs/yr): represents the number of hours 
in a year the electrolyser operates (over its complete load range, which is defined by the user 
in the Inputs sheet) as a percentage of the total hours in a year.
 Electrolyser Capacity Factor (%): represents the ratio of the total energy input to the 
electrolyser over the total energy that would be required to run the electrolyser at its maximum 
capacity for the whole year.
 Energy Consumed by Electrolyser (MWh/yr): represents the average energy consumed 
by the electrolyser in each year over the project life.
 Excess Energy Not Utilised by Electrolyser (MWh/yr): represents the average additional 
annual energy output from the power plant which is not consumed by the electrolyser over 
the project life.
 Hydrogen Output (t/yr): represents the average amount of hydrogen generated per year of 
the plant life.
 $LC_{H_2}$ ($/kg): represents the levelised cost of hydrogen
 Retail Cost of Hydrogen ($/kg): represents the cost at which the hydrogen is retailed. It is
based on the levelised cost of hydrogen evaluated by the tool and a sales margin cost (an 
additional $/kg on top of the levelised costs the hydrogen is retailed by the electrolyser, the 
sales margin is provided by the user).
 Net Profit ($): represents the total profit generated over the project life.
 Return on Investment (%): represents the ratio of the net profit to the total capital investment 
required to develop the project. 
 Payback Period (years): represents the time period in years needed to recover the total 
investment required to develop the project.
These parameters are elaborated in the following sections in greater detail (Section 4 and 5)


There are also a number of plots showing the power plant and electrolyser annual duration curves
(Figure 8), hourly capacity factors (Figure 9), breakdown of costs in the levelized cost (Figure 
10), components of CAPEX and OPEX (Figure 11) the cash flows over the lifetime of the project
(Figure 12-Figure 14). At the far right is the result for each year of operation, which only vary if 
degradation of the power plant and/or electrolyser is included in the model. 

![[Fig 8. Annual duration curves for the power plant and electrolyser from sheet S2. Results.png]]

Figure 8. Annual duration curves for the power plant and electrolyser from sheet 'S2. Results'. Note: the values in the figures are representative and subjective to change based on user input.

![[Figure 9. Interactive plot showing the hourly capacity factors of the power plant and electrolyser from sheet 'S2.jpg]]
Figure 9. Interactive plot showing the hourly capacity factors of the power plant and electrolyser from sheet 'S2. 
Results'. Note: the values in the figure are representative and subjective to change based on user input

![[Figure 10. Waterfall plot showing the relative components of the LCH2 from sheet 'S2. Results.jpg]]
Figure 10. Waterfall plot showing the relative components of the LCH2 from sheet 'S2. Results'. Note: the values in 
the figure are representative and subjective to change based on user input.

![[Figure 11 Breakdown of the componneets of the capital and indirct cost from sheet S2.Reults.png]]
Figure 11. Breakdown of the components of the capital and indirect costs from sheet 'S2. Results'. Note: the values in the figures are representative and subjective to change based on user input.

![[Figure 12. Annual sales plot from sheet 'S2. Results'.jpg]]
Figure 12. Annual sales plot from sheet 'S2. Results'. Note: the values in the figure are representative and subjective to change based on user input.


![[Figure 13. Annual operating cost plot from sheet 'S2. Results'.jpg]]
Figure 13. Annual operating cost plot from sheet 'S2. Results'. Note: the values in the figure are representative and 
subjective to change based on user input. The spikes indicate years in which the stack replacement occurs.

![[Figure 14. Cumulative cash flow from sheet 'S2. Results’.jpg]]
Figure 14. Cumulative cash flow from sheet 'S2. Results’. Note: the values in the figure are representative and subjective to change based on user inp


S3. Levelised Cost Analysis
This sheet calculates the capital and operating costs for each component of the model. It presents
the annual operational profile for each year up to the lifetime as well as the discounted and non￾discounted cash flows. Note: All these cells are automatically generated once the “Calculate” 
button is activated. The values are based on the user inputs and background calculations from 
the ‘S6. Working data’ sheets.  

![[Figure 15. Sheet 'S3. Levelised Cost Analysis' which includes a summary of the capital and operating costs and the annual cash flows.jpg]]
Figure 15. Sheet 'S3. Levelised Cost Analysis' which includes a summary of the capital and operating costs and the annual cash flows. Note: the values in the figure are representative and subjective to change based on user input.

S4. Cash Flow Analysis
Sheet S4 contains the detailed cash flows required for calculation of the net profit, return on 
investment and payback period.

![[Figure 16. Sheet 'S4. Cash Flow Analysis' presents a NPV calculation to find the net profit, return on investment and payback period.jpg]]
Figure 16. Sheet 'S4. Cash Flow Analysis' presents a NPV calculation to find the net profit, return on investment and payback period. Note: the values in the figure are representative and subjective to change based on user input.

S5. Raw Data
To calculate the annual hydrogen production, the tool relies on hourly electricity generation 
profiles in the form of capacity factor traces. 
 The Raw Data sheet currently contains hourly solar and wind traces 
The user may also input their own project-specific trace to run the tool for a location other than 
those already included. These traces could include potential solar and wind traces or the historical 
generation profile of an actual solar or wind farm in that location. 
Custom location will then use the api to pull all necessary data
To do this the user will select the ‘Custom’ option from the locations drop down on the ‘S1. Inputs’ sheet.

![[Figure 17 Sheet 'S5 Raw Data' contains solar and wind traces for 41 locations across Australia.jpg]]
Figure 17. Sheet 'S5. Raw Data' contains solar and wind traces for 41 locations across Australia with the additional option to include solar and/or wind traces for a custom location.

S6. Working Data
The Working Data sheet (Figure 18) is where the hourly electrolyser operation and outputs are 
calculated. Note: These cells are automatically generated once the “Calculate” button is 
activated. The values are based on the user inputs and background calculations from the ‘S5. 
Raw Data’ sheets

![[Figure 18. Sheet 'S6. Working Data' where the hourly operation is calculated.jpg]]
Figure 18. Sheet 'S6. Working Data' where the hourly operation is calculated. Note: the values in the figure are representative and subjective to change based on user input.

A1. Electrolyser Parameters
The Specific Energy Consumption (SEC) for both the AE and PEM electrolyser, which is 
elaborated in Section 4, are known to vary based on the operational load of the electrolyser at 
any given time.1 This functionality has been included in the tool as an advanced feature, which 
can be activated by selecting the ‘variable’ option from the drop down list (SEC vs Load Profile) 
present in cell B28 of the ‘S1. Inputs’ Sheet. 

Once the option has been selected, further inputs are required on the ‘A1. Electrolyser 
Parameters’ sheet. In this sheet, the user must define the SEC (as a percentage of the SEC at 
nominal load), across the load range of the electrolyser (in cell B6 onwards as shown in Figure 
19). The SEC vs Load profile is then plotted automatically, and a second order polynomial 
equation is defined as a best fit that passes through up to 7 manually selected points. The 
coefficients used for the calculation are displayed in cells G8 to G10. This polynomial function is 
used to determine the SEC at any given load of the electrolyser, which is passed into the 
‘S6. Working Data’ sheet to determine the amount of hydrogen generated based on the available 
energy from the power plant in each hour. Note: The SEC profile vs load (orange shaded cells) 
are the only inputs required from the user. All other calculations on this sheet are automatic. 

![[Figure 19. Sheet ‘A1. Electrolyser Parameters’ defines the electrolyser specific energy consumption vs load profile.jpg]]
Figure 19. Sheet ‘A1. Electrolyser Parameters’ defines the electrolyser specific energy consumption vs load profile.
Note: the values in the figure are representative and subjective to change based on user input.

Moreover, actual SEC profiles of AE and PEM electrolysers established in literature are also 
provided as a reference to guide the user in defining their own profiles (Figure 20-Figure 21).

![[Figure 20. Preloaded SEC vs Load Profile of AE electrolyser adopted from literature.jpg]]
Figure 20. Preloaded SEC vs Load Profile of AE electrolyser adopted from literature

![[Preloaded SEC vs Load Profile of PEM electrolyser adopted from literature.jpg]]
Figure 21. Preloaded SEC vs Load Profile of PEM electrolyser adopted from literature3.


----

# 4. Scope of Analysis and Inputs

## 4.1. System Boundary

The system boundary (Figure 22) of Version 1 of the  Hydrogen Cost Analysis Tool is restricted to the hydrogen output from the electrolyser. The key components within the boundary are the electrolyser systems (including its balance of plant - BoP), and the solar and/or wind power plant. Depending on the configuration (elaborated below), additional components like battery storage and electricity transmission network are added to the power plant. The water supply source to drive the electrolyser is assumed outside the scope of the analysis, however, to represent the associated costs of the water used, the user has been provided an option to input the wholesale water price. Additional functionality is provided for the user to retail any surplus electricity and the by-product oxygen.

Figure 22. System boundary for Version 1 of the cost tool.

Note: that the system boundary is being expanded iteratively with more stakeholder input in the next stage of  Hydrogen Project.


## 4.2. Scope of Analysis

To define the analysis scope the user has to set the following parameters:

### 4.2.1. Site Location

The Hydrogen Cost Analysis Tool is designed for a spatial analysis of hydrogen generation costs, based on the solar and wind resources across United state. In its present iteration, the tool includes a number of pre-determined sites within USA, of which contain solar and wind traces that are representative of a year of renewable resources for each renewable generation technology type. In particular, sites within the National Electricity Market (NEM), have utilised the Australian Energy Market Operator’s (AEMO) historical solar and wind data from the 2020 Integrated System Plan (ISP). Non-NEM sites have been represented by modelled solar and wind data obtained via the “Renewables Ninja” open-source tool. The sites that have been included in the tool can be categorised as such:

- **NEM sites**
    - New South Wales (NSW)
    - Queensland (QLD)
    - Victoria (VIC)
    - South Australia (SA)
    - Tasmania (TAS)
        
- **Non-NEM sites**
    - Northern Territory (NT)
    - Western Australia (WA)
        

The NEM sites have been chosen with reference to the Renewable Energy Zones (REZ) as documented by the AEMO’s 2020 Integrated System Plan (ISP).4 AEMO defines REZs as follows:

> “REZs are areas in the NEM where clusters of large-scale renewable energy can be developed to promote economies of scale in high-resource areas and capture geographic and technological diversity in renewable resources.”

While AEMO’s 2020 ISP did not include hydrogen in the scope of the investigation, the  Hydrogen Cost Analysis Tool leverages the abundance of these high-resource areas to model green hydrogen potential. For non-NEM locations, the selected sites have taken into consideration the renewable energy resources that are available as well as the site’s proximity to infrastructure such as roads, railways, gas pipelines, and ports. Reports such as the Western Australian Renewable Hydrogen Strategy have also informed the site selection, aligning the Hydrogen Cost Analysis Tool with sites that are of interest to the relevant state government and the private sector for their renewable energy/green hydrogen potential.

The location can be set through the drop-down list . Custom locations can be defined. The full list of preloaded locations is provided

_Figure 23. Site Selection Drop Down List._ Hydrogen

### 4.2.2. Solar and Wind Traces

To calculate the electricity generation, the  Hydrogen Cost Analysis Tool relies on time-sequential, hourly observations of the solar and wind data at each specific location. The trace data that has been obtained through sites is for the reference year of 2024 and has been modelled by the market operator to reflect observed historical patterns. The non-NEM sites of NT and WA use traces were produced using the open-source tool “Renewables Ninja”.6 The data obtained from this tool uses inputs from **NASA’s Modern-Era (MERRA) Retrospective Analysis (Reanalysis**), and CM-SAF’s The Surface Solar Radiation Data Set - Heliosat (SARAH) dataset pertaining to 2024.

In addition, the user has the option to include their own solar and wind traces for a custom analysis, these traces could either be based on potential solar and wind resources at a particular region not included in the analysis or actual outputs from existing solar and wind farms. 

- **Process for Extracting Additional Solar and Wind Traces from Renewable Ninja:** Additional Solar and Wind traces can be extracted using Renewables Ninja (
    
    [https://www.renewables.ninja/](https://www.renewables.ninja/)). Requests for data can be made anonymously or by registering for a free account within the website. Anonymous users are limited to 5 retrieval requests per day for data from the year 2014, whereas registered users are limited to 50 retrieval requests per hour for data between 2000-2019. The Renewables Ninja website interface allows for specific solar PV and wind system setups, as well as a choice between MERRA-2 (global data) and CM-SAF SARAH (European data) data sets as seen in Figure 24. Sites can be selected either by entering the location name, by latitude and longitude, or by dropping a pin on the map.
    
![[Figure 24 Renewable Ninja User input Fields.png]]
_Figure 24 Renewable Ninja User Input Fields_

For **solar PV**, user inputs can be made for:

- **Capacity (kW)** – the default input is 1 kW. The data retrieved from Renewables Ninja in the HCAT tool uses a capacity of 1000 kW.
    
- **System Loss (fraction)** – the default input is 0.1. The data retrieved from Renewables Ninja in the HCAT tool uses a system loss of 0.
    
- **Tracking** – tracking setups will be dependent on the specific project parameters of the solar farm. The data retrieved from Renewables Ninja in the HCAT tool uses single axis tracking.
    
    - Fixed tilt (None)
    - 1-axis (azimuth)
    - 2-axis (tilt and azimuth)
        
- **Tilt (°)** – This field defines how far a panel is inclined from the horizontal plane. If using a fixed tilt system (no tracking), the tilt of the system should be equal to the latitude of the site in order to maximise the solar farm’s yield. For single and dual axis tracking, setting a tilt angle in this field will not affect the yield.
    
- **Azimuth (°)** – This field defines the compass direction in which the solar farm is facing. To maximise yields in the southern hemisphere, solar farms should be facing north, defined by 180° in Renewables Ninja. To maximise yields in the northern hemisphere, solar farms should be facing south, defined by 0° in Renewables Ninja.
    

For **Wind**, user inputs can be made for:

- **Capacity (kW)** – the default input is 1 kW. The data retrieved from Renewables Ninja in the HCAT tool uses a capacity of 1000 kW.
    
- **Hub height (m)** – this field defines the height of the turbine’s tower and will be dependent on the specific turbine model that will be used on the wind farm
    
- **Turbine Model** – this field allows for the selection of the make and model of the wind turbines. Model names typically will include the manufacturer, the blade diameter in meters, and the rated capacity in kW or MW.

Once all fields have been defined, clicking on run will begin the retrieval process and clicking on “Save hourly output as CSV” will allow for the downloading of the data.

### 4.2.3. Power Plant Configuration

The  Hydrogen Cost Analysis Tool allows the user to model the electrolyser operation based on certain the power plant configuration scenario. These scenarios allow for the choice between a Solar PV, Wind or Hybrid power plant which can be standalone (within the system boundary) or outsourced (via a power purchase agreement). For the standalone system, the user can also choose to manage surplus electricity generation by integrating a battery as an auxiliary intermediate or retailing the surplus to the grid. These configurations for the electrolyser-power plant are summarised below.

- C1. Standalone Solar PV Generator with Electrolyser
    
- C2. Standalone Solar PV Generator with Electrolyser and Battery
    
- C3. Grid Connected Solar PV Generator with Electrolyser
    
- C4. Grid Connected Solar PV Generator with Electrolyser with Surplus Retailed to Grid
    
- C5. Grid Connected Solar PV Generator with Electrolyser and Battery
    
- C6. Grid Connected Solar PV Generator with Electrolyser and Battery with Surplus Retailed to Grid
    
- C7. Solar PPA with Electrolyser
    
- C8. Solar PPA with Electrolyser and Battery
    
- C9. Standalone Wind Generator with Electrolyser
    
- C10. Standalone Wind Generator with Electrolyser and Battery
    
- C11. Grid Connected Wind Generator with Electrolyser
    
- C12. Grid Connected Wind Generator with Electrolyser with Surplus Retailed to Grid
    
- C13. Grid Connected Wind Generator with Electrolyser and Battery
    
- C14. Grid Connected Wind Generator with Electrolyser and Battery with Surplus Retail to Gird
    
- C15. Wind PPA with Electrolyser
    
- C16. Wind PPA with Electrolyser and Battery
    
- C17. Standalone Hybrid Generator with Electrolyser
    
- C18. Standalone Hybrid Generator with Electrolyser and Battery
    
- C19. Grid Connected Hybrid Generator with Electrolyser
    
- C20. Grid Connected Hybrid Generator with Electrolyser with Surplus Retailed to Grid
    
- C21. Grid Connected Hybrid Generator with Electrolyser and Battery
    
- C22. Grid Connected Hybrid Generator with Electrolyser and Battery with Surplus Retailed to Grid
    
- C23. Hybrid PPA with Electrolyser
    
- C24. Hybrid PPA with Electrolyser and Battery
    

These options can be selected using the drop-down list in Cell B5 of the Inputs sheet as shown in Figure 25. Note: The drop-down list has an additional feature, the choices provided are then used to determine which input cells (orange colour) are marked as inactive (grey colour)

_Figure 25. Drop down list of Power Plant Configurations._

The above scenarios can be categorised into the following configurations.

- **Standalone Configuration:** For the standalone system, the renewable power plant is assumed to be built within the boundary of the electrolyser facility. The key features of this scenario are:
    
    - The electricity output from the power plant is used directly by the electrolyser to generate hydrogen and any surplus is either stored in the battery or curtailed.
        
    - For this scenario the capital and operating costs of the power plant and the electrolyser are directly passed on to the project proponent (appearing in the cash flow statement).
        
        Of the above, C1-C2, C9-C10, C17-C18 fall into this configuration.
        
- **Grid Configuration:** As an alternate to the standalone system, the renewable power plant can also be connected to the electrolyser through the grid. In this case it is assumed that the power plant is built at a different site, while the electricity to drive the electrolyser is supplied using the grid. The key features of this scenario are:
    
    - The electricity output from the power plant is used directly by the electrolyser to generate hydrogen and any surplus is either stored in the battery or retailed to the grid.
        
    - Additional cost of grid connection and grid service charges (e.g., Transmission use of system charges) are added as additional upfront capital and ongoing operating costs.
        
    - If the option to retail the surplus is chosen from the configuration drop down list, the user can provide a spot price to evaluate the surplus electricity sales. 
        

Figure 26. Surplus Electricity Sales. Note: the values in the figure are representative and subjective to change based on user input.

```
-   For this scenario the capital and operating costs of the power plant and the electrolyser are directly passed on to the project proponent (appearing in the cash flow statement). [cite: 360]
The configuration options: C3-C6, C11-C14 and C19-C22 fall in the grid connected categories. [cite: 361]
```

- **PPA Configuration:** The third option is to purchase the electricity from a 3rd Party a through a Power Purchase Agreement (PPA). The key features of this scenario are:
    
    - The generator type, capacity and the generation profile of the power plant are defined by the user. Elaborated in Section 4.3. (below)
        
    - The PPA could ether include only the electricity to drive the electrolyser or include additional electricity to charge the battery (depending on the choice from the configuration drop down list)
        
    - The electricity sourced is then costed as a fixed unit cost of electricity ($/MWh), that is defined by the user.
        
        The configuration options: C7-C8, C15-C16 and C23-C24 fall in the PPA category.
        

## 4.3. System Sizing

This section requires the size (capacity) of the electrolyser, individual solar and wind farms and the battery. The user has to provide the following options:

- **Nominal Electrolyser Capacity (MW):** The scale of the electrolyser is based on the user’s requirement and is then used as the nominal capacity of the electrolyser system for the consequent analysis. A guide is provided in the tool to assist the user in selecting the appropriate scale for a certain annual production level (Figure 27).
    

Figure 27. Reference guide for setting electrolyser capacity.

- **Nominal Power Plant Capacity (MW):** The user must define the nominal capacity of the power plant to be used for the analysis. Depending on the chosen scenario (Section 4.3.2), the user is provided the generator type to assist in appropriately defining the individual capacities (Cell B13). If the solar-based configuration is selected then the user need only provide the nominal solar farm capacity, similarly if the wind-based configuration is selected then the user need only provide the nominal wind farm capacity. If the hybrid-based configuration is selected, then the user must provide the nominal capacity of both the solar and wind farms. These capacities are added to represent the total nominal capacity of the hybrid power plant.
    
    - **Oversizing of Power Plant** As an additional strategy to optimise the capacity factor, the user can choose to oversize the capacity of the power plant (i.e., make it larger compared to the capacity of the electrolyser). This strategy creates an advantage as having a larger power plant ensures that larger amounts of renewable energy is available to drive the electrolyser at any given time than otherwise would with a smaller capacity powerplant. E.g., a 10 MW powerplant would have to operate at 100% capacity factor to ensure that a 10 MW electrolyser runs at 100% capacity factor, but instead if there is a 12 MW capacity powerplant that could power the same electrolyser at 100% capacity as long as it operates at or higher than 80% capacity factor. Our prior analysis, has explored this scenario in greater detail, revealing that an appropriate size combination can lead to lower levelised cost despite additional capital and operating costs associated with a larger powerplant.7 Oversizing scenarios with a 1.2 – 1.5 times oversized solar and wind farms were found to be the most optimum combination, but this is subject to the solar and wind traces. The downside of oversizing is the need to curtail the powerplant in an absence of a grid connection.
        
    - **Surplus Energy** Any energy generated by the power plant outside the load range of the electrolyser is considered to be surplus and can be handled in different ways depending on the chosen system configuration (Section 4.3.2). The tool currently deals with surplus renewable energy in one of three ways:
        
        - Curtailing the solar and/or wind power plant to avoid surplus,
            
        - If the solar/wind farms are connected to the grid, the surplus can be retailed onto the grid.
            
        - If a battery is included, then storing the surplus in the battery and reusing it to power the electrolyser when the solar and wind generation starts to fall.
            
            The surplus renewable energy can also be used to power operations downstream of the electrolyser such hydrogen compressors, or the staff camp/buildings etc., though these options are not included in the base version of the tool they can be added based on user requirement.
            
- **Nominal Battery Capacity (MW):** The user has the option to define the battery capacity when the relevant configuration is selected. (Note: The capacity can be defined only if a battery-based configuration is selected from the power plant configuration drop down list, else it will be set to zero). The battery capacity in turn is based on the battery’s rated power (the maximum energy the battery can store or discharge at any given time in MW), and the duration of storage (number of hours that the battery takes to charge/ discharge at its max power level). Both of these parameters must be defined by the user, with the duration of storage selected from a drop-down list (Cell B18). The tool currently caters for 1, 2, 4 and 8 hours of storage (Note: This is subject to change after consultation with stakeholders).
    

Figure 28. Input parameters for system sizing. Note: the values in the figure are representative and subjective to change based on user input.

## 4.4. Electrolyser Parameters

### 4.4.1. Electrolyser Capacity and Operating Parameters

The tool currently is tailored for the Alkaline Electrolyte (AE) Electrolyser and Polymer Electrolyte Membrane (PEM) Electrolyser. Note: that in subsequent iterations, solid oxide electrolysers will also be considered. The user is provided with the option to define the following electrolyser parameters:

- **Electrolyser Choice:** The user may select either AE or PEM from a drop-down list (Cell B22), the choice then reflects in the project summary (in the results sheet).
    
- **Electrolyser specific energy consumption (SEC):** The SEC is defined as a combination of the following subcomponents:
    
    - **The SEC at nominal load (kWh/kg):** which represents the kWh of electricity required per kg of H2 output by the electrolyser at the nominal load. This value must be provided by the user.
        
    - **SEC vs Load profile:** the function allows for the user to select the profile of how the SEC varies with load. The fixed profile assumes that the SEC is independent of the load. In comparison, the variable profile assumes that the SEC varies for load to mimic the more realistic nature of electrolyser operations. The tool can account for both fixed and variable specific energy consumption with electrolyser load. For the variable case, the relationship between the specific energy consumption of the electrolyser and the electrolyser load is based on a curve fit to a set of input points provided by the user (SEC as a function of the % of the electrolyser load). This is available to view and edit in sheet ‘A1. Electrolyser Parameters’ as highlighted earlier.
        
    - **SEC correction factor (%):** In our model, we assume that the SEC represents the energy consumption of just the stack. An additional factor (SEC correction) to accommodate for the energy requirement of the BoP of the electrolyser is also provided. This factor is the ratio of the energy provided to the electrolyser and the total energy consumed by the stack to generate the hydrogen. For example, if the factor is assumed to be 80%, then only 80% of the electricity provided to the electrolyser is used to generate hydrogen and the rest of the energy is consumed internally by the BoP and internal system losses. Note: the factor is optional, and by default we set it at 100% assuming that the user provides the SEC for the total system (stack and BoP) in the SEC at Nominal Load.
        
- **Electrolyser Load Range (%):** The user also needs to define the electrolyser load range as a maximum and minimum percentage of the electrolyser’s nominal capacity that the electrolyser can operate at within at any given time. Note: In practice, the minimum value operating valye of electrolyser is dictated by the electrolyser’s operational safety limit, which varies depending on electrolyser type. Literature suggests the low-end load range of AE as 10 – 40% of nominal capacity and of 0 – 10% for PEM electrolyser.8
    
- **Electrolyser Load Overloading:** Modern electrolyser especially, PEM electrolyser technology, have been shown to be able to overload to 120% to 150% of its nominal capacity.9 Future KPI targets for electrolyser target the overload range of 300% for both AE and PEM.10 Our model allows for the electrolyser to be overloaded to a set value by the user with a cool down period before the electrolyser can be overloaded again. When overloading, the electrolyser will operate at a load up to the maximum set value (minimum to maximum overloading capacity) provided there is enough electricity supply from the power plant.
    
    _Note: This functionality will be further improved after stakeholder engagement._
    
- **Electrolyser Degradation (%/year):** Both the AE and PEM electrolyser are susceptible to degradation which leads to loss of efficiency, performance, and durability of the system. The degradation rate is conventionally represented as a loss in voltage per hour of operation (usually represented in micro volt lost per hour - µV/hr). Degradation of any level leads to increase of electrical consumption to achieve the same hydrogen output. Our model caters for this scenario by providing the user the option to define the degradation rate as a set percentage loss of hydrogen per year. E.g., by setting a degradation of 1% per year would mean that the electrolyser generating 1000 ton/yr in year 1 would generate 990 ton/yr in year 2.
    
- **Stack Replacement:** A key parameter of electrolyser operation is the need for stack replacement. Our model allows the user to handle this option in either of the following ways:
    
    - **Cumulative hours (hours):** In this option, the user provides stack lifetime, which is then compared with the cumulative operational hours of the electrolyser, and once these hours exceed the stack lifetime the stack has to be replaced.
        
    - **Maximum degradation level (%):** In this option, the user can provide a maximum degradation level. The stack is expected to be replaced when the cumulative degradation per year adds up to the maximum degradation level. Note: for this scenario, the user must provide the yearly degradation rate. Further guides to set the degradation levels and improvements to this function will be included after stakeholder engagements.
        
- **Water Requirement (L/kg):** The water requirement represents the water consumed for driving the electrolyser in terms of litres of water consumed per kg of hydrogen output.
    

_Figure 29. Electrolyser Operating and Performance Parameters. Note: the values in the figure are representative and subjective to change based on user input._

### 4.4.2. Electrolyser Capital and Operating Costs

For the costs analysis, the tool considers the following parameters:

- **Electrolyser Capital Cost:** The electrolyser capital cost is based off the direct cost associated with the purchase of the equipment (electrolyser CAPEX) and the indirect costs which include the land and engineering and procurement costs (EPC). This capital cost is evaluated as:
    
    - **Electrolyser CAPEX:** The electrolyser CAPEX is evaluated based on a literature based economies of scale model11,12, where a reference cost (A\$/kW) is provided at a reference scale (kW) which is then used to establish the scaled purchase cost of the electrolyser ($/kW) at the user defined capacity of the electrolyser by the user. The following logarithmic function is used to scale up or down the CAPEX (Eq.1):
        
        $C_B(A/kW) = C_A \times (1 - C_r)^{\log_{\text{Ref}}(S_B/S_A)}$ Here the CB is evaluated cost at the nominal electrolyser scale SB, CA is the cost at the reference scale SA (both of which are provided by the user), Cr is the percentage scale reduction in CAPEX per a set fold increase in capacity (Ref). This set number of fold increase in capacity dictates when the economies of scale are triggered. E.g., if the reference electrolyser CAPEX is set to be A
        
        1,000/kWat 1,000kW scale witha 10810/kW.
        
        _Note: this function will be further improved after engagement with stakeholders._
        
    - **Electrolyser Indirect Cost:** As mentioned earlier, the electrolyser indirect costs include the cost of land and EPC. In the tool, the user is provided the option to define these values as a percentage of the electrolyser CAPEX.
        
        _Note: this function will be further improved after engagement with stakeholders._

		> We also add a custom unistalled capital cost curve function 2024
		> $Cost_{el} = c_1 +c_2P-{El,rated}+ c_3*e^{c_4, P{El,rated}}$ , uni in ($/kW)
		> $P_{El,rated}$ at MW
		> the default constants are c_1= 1046.93 , c_2=-3.479, c_3=61.567, c_4=-0.261 referenced to astrani et al 
		> user will have the option to customize this cost curve function
		
		
		user will have the option to chose the economies of scale profile type for the equipment cost setting. weaher self Defind, Scale index, Curve Fitted or custom

- **Electrolyser Operating Cost:** The electrolyser operating costs (OPEX) includes the fixed operating and maintenance costs (O&M), cost of stack replacement and the water consumption costs. These can be defined as:
    
    - **Electrolyser O&M:** The tool allows for the O&M to be defined as a percentage of the electrolyser CAPEX per year.
        
    - **Stack Replacement Cost (%):** Similarly, the cost associated with the electrolyser replacement can be represented as % of the electrolyser CAPEX per replacement.
        
    - **Water Consumption Cost ($/kL):** The water cost is evaluated based on the user provided wholesale price which is then correlated with the water requirement (L/kg H2) required to establish the yearly cost.
        

Figure 30. Electrolyser Capital and Operating Cost Parameters.

Note: the values in the figure are representative and subjective to change based on user input.

## 4.5. Power Plant Parameters

### 4.5.1. Power Plant Capacity and Operating Parameters

- **Degradation Rates of Solar PV and Wind Farm (%):** Similarly, to the electrolyser, the user can also define the degradation rate of the solar and wind farms. This input is provided as a percentage reduction in output and is multiplied by the capacity factor figures to get the power plant output per unit capacity for each hour of each year. Note: For the hybrid scenario, the degradation rate should be provided for both the solar and wind farm. This function will be further improved after engagement with stakeholders.
    

Figure 31: Power Plant Performance Parameters.

### 4.5.2. Power Plant Capital and Operating Costs

The power plant capital and operating costs depend on whether the plant is owned and built by the project proponent or sourced through the electricity grid.

- **Standalone Configuration:** For the standalone configuration, depending on the operational scenario (Scenario 4.3.2), the capital and operating cost of the individual solar and wind farm must be defined by the user. This is done in a similar way to the electrolyser, where the power plant CAPEX is based on the CAPEX of the solar/wind farm CAPEX and any indirect costs. The tool evaluates these in the following manner:
    
    - **Power Plant CAPEX:** The power plant CAPEX is evaluated based on the similar economies of scale model used for the electrolyser, in which a reference cost (A\$/kW) that is provided at a reference scale (kW) is scaled up or down to determine the CAPEX at the nominal capacity of the power plant through Eq.2.: $C_B(A/kW) = C_A \times (1 - C_r)^{\log_{\text{Ref}}(S_B/S_A)}$
        
    - **Power Plant Indirect Cost:** The power plant indirect costs include the cost of land and EPC. In the tool, the user is provided the option to define these values as a percentage of the individual solar/wind power plant CAPEX.
        
    - **Hybrid Power Plant Costs:** In case the hybrid power plant is chosen, the aggregate of the capital of the individual solar and wind farm proportional to their share in the total capacity of the hybrid power plant is taken to represent the capital costs of hybrid systems (Eq. 3).
        
        Hybrid Power Plant $Cost=(Ps​+Pw​)(Ps​×CS​+Pw​×CW​)​$
        
        Here,
        
        C_S is the cost component of solar farm, C_W is the cost component of the wind farm, while P_s is the capacity of the solar PV in the hybrid system, and P_w is the capacity of the wind farm. The cost components can either be represented by the total capital cost (including indirect costs associated with EPC and land) or the operating costs of the individual solar and wind farms.
        
    - **Fixed and Variable O&M Costs (A\$/MW/yr):** The tool provides the option to include the fixed and variable operation and maintenance cost of the power plant as an aggregate $/MW/yr value based on the nominal capacity of the power plant. These can be individually defined for both the solar and wind farm.
        
    - **Hybrid Power Plant OPEX:** For the Hybrid system the individual operating cost of solar and wind farm are aggregated in the same manner as the capital costs using Eq. 3.
        

Figure 32. Standalone Power Plant Capital and Operating Cost Parameters.

Note: the values in the figure are representative and subjective to change based on user input.

- **Grid Connected Configurations:** For the Grid Connected Configurations, in addition to the CAPEX (including indirect costs) and OPEX of the power plant, the user also can provide the gird connection and additional transmission charges. In the tool the user can add the grid connection costs as a total upfront cost ($) and the grid service charges as a unit cost ($ MWh-1) as shown in Figure 33 below:
    

Figure 33. Additional Grid Connection Costs.

Note: the values in the figure are representative and subjective to change based on user input.

- **PPA Configurations:** For the PPA Configurations, the capital and operating costs of the power plant are expected to be integrated within the PPA cost as follows:
    
    - **Principal PPA Cost ($/MWh):** Selecting the PPA option allows for the operation of the electrolyser based on electricity sourced from the grid. The PPA price represents the cost per unit of electricity consumed by the electrolyser. It is assumed in this case that the electrolyser still follows the hourly operational profile of the generator, but capital and operating costs are simplified into a single per unit cost.
        
    - **Transmission Connection Costs ($):** An additional upfront cost that can be included to account for connection costs.
        
    - **Total PPA Cost ($/MWh):** The principal PPA cost, and the additional transmission charges are summed to represent the total PPA cost as shown in Figure 34.
        
        _Note: For the PPA configurations, the grid connection cost must also be provided._
        

Figure 34. Power Purchase Agreement (PPA) Costing. Note: the values in the figure are representative and subjective to change based on user input.

## 4.6. Battery Parameters

### 4.6.1. Battery Capacity and Operating Parameters

The battery is defined by both its size and a set of operational parameters. The operating parameters can be changed to suit different battery types.

- **Round Trip Efficiency (%):** Proportion of energy retained after a charge and discharge cycle of the energy storage system.
    
- **Minimum State of Charge (%):** Minimum level of battery charge for safe operation, given as a proportion of the battery rated power capacity.
    
- **Maximum State of Charge (%):** Maximum level of battery charge for safe operation, given as a proportion of the battery rated power capacity.
    

_Figure 35. Battery Performance Parameters._

### 4.6.2. Battery Capital and Operating Costs:

- **Battery Capital Costs:** The battery capital costs are based on the following user defined values:
    
    - **Battery CAPEX ($/kWh):** The capital cost of the battery system per unit of battery energy capacity.
        
    - **Battery Indirect Costs:** As for the other components of the system, the battery indirect costs include the cost of land and EPC, both of which are defined as a percentage of the CAPEX.
        
- **Battery Operating Costs:** The operating costs of batteries considered in the tool include:
    
    - **Battery Replacement Cost (%):** Defines the percentage of the CAPEX to be spent each time the battery is replaced. This may be less than the original CAPEX since the infrastructure is already in place and the battery cells need replacing more often than the rest of the system. Note: The model assumes that this cost is incurred as an additional operating expense in the annual cash flow whenever the battery life expires. This function will be improved after stakeholder engagement.
        
    - **Battey OPEX ($/MW/yr):** The OPEX is the fixed and variable operation and maintenance cost of the battery as an aggregate $/MW/yr value, based on the power capacity.
        

Figure 36. Battery Capital and Operating Cost Parameters.

Note: the values in the figure are representative and subjective to change based on user input.

## 4.7. Additional Costs

- **Additional Upfront Costs:** The user can include any unaccounted upfront cost if required as a lump sum amount in Cell B98 of the ‘S1. Inputs’ sheet.
    
- **Additional Annual Costs:** The user can include any unaccounted annual costs if required as in Cell B99 of the ‘S1. Inputs’ sheet.
    

_Figure 37. Option to include Additional Costs._

## 4.8. Additional Revenue Streams

- **Surplus Electricity Retail:** If the PPA configuration is selected (Section 4.3.2) and any surplus energy from the powerplant can be potentially retailed. The tool provides the user the option to include this by setting the above conditions as the inputs and by providing the average electricity spit price in Cell B102.
    
- **By-product Oxygen Retail:** Oxygen is produced as a byproduct of the electrolyser operation (8 kg of O2 produced per kg of Hydrogen), this by product can also be retailed as an additional revenue stream. The tool provides the user the option to include this by setting the oxygen retail price in Cell B103.
    

Note: These additional revenue streams are included as a potential scenario, and they may or may not apply, depending on the user’s scope of analysis.

_Figure 38: Option to include Additional Revenue Streams._

## 4.9. Financing Parameters

The key inputs for the financial analysis include:

- **Plant Life:** The user has been provided the option to define the plant life. Currently the plant life of the electrolyser (including multiple stack replacements) and the power plant are assumed to be the same. The user can set the plant life to up to 50 years if required. A macro has been designed that iterates the production profile of hydrogen per year until the plant life is achieved. This is to account for the degradation of the electrolyser and power plant. If degradation is not included in the analysis, then the hydrogen production and other operational outputs in each year will be identical. The cash flows also automatically adjust to match the plant life. Project decommissioning is assumed to occur in the subsequent year after plant.
    
- **Discount Rate:** The user is required to provide the discount rate for the Net Present Value analysis.
    
    Note: This must be provided to calculate the levelised cost of hydrogen.
    
- **Investment Breakdown:** The tool allows the user to finance the total investment required using a combination of:
    
    - **Financing via Equity:** The equity can then be financed through a combination of direct equity which is directly borne (paid by the project proponent – a negative cash injection) and indirect equity which are not directly borne by the project proponent but are leveraged through external support like grants etc. (a positive cash flow injection – but on a non-loan basis). The user can define the share of equity as an input as a percentage of total investment, with a further split between direct and indirect equity as a percentage of total equity.
        
    - **Financing Via Loan:** The rest of the total investment is then financed using loans, the user is provided the option to define the loan term (Period over which the loan is returned - the tool currently considers yearly repayment of loans) and the interest rate on loan (% p.a.)
        
- **Investment Breakdown:** Post project cash flows currently include:
    
    - **Salvage Costs:** The capital that can be potentially recovered by reselling the equipment at the end of the project. The user can define the salvage costs as a percent of the total investments.
        
    - **Decommissioning Costs:** The cost incurred by to dismantle the equipment and reverse modifications that were made in setting up in the landscape. The user can define the salvage costs as a percent of the total investments.
        
        Note: This functionality will be improved after consulting with stakeholders.
        
- **Additional Labilities:** Additional labilities considered currently include:
    
    - **Inflation Rate:** The user can define their own inflation rate as a % increase in costs per annum. The inflation rate is then applied to the sales and operating costs.
        
    - **Tax Rate:** The user can define their own tax rate as % of total income per annum.
        
        _Note: This functionality will be improved after consulting with stakeholders._
        
- **Depreciation:** The cash flow analysis also considers depreciation of the investment. Of the total investment the depreciable investment includes the cost of the equipment (CAPEXs of electrolyser, power plant, battery, grid connection and any additional upfront capital costs), the land cost is assumed to be non-depreciable. The depreciation is automatically evaluated by the tool, based on the depreciation profile selected by the user. The user can select the depreciation profile from the drop-down list in Cell B120 of the input sheets. These profiles include the straight-line depreciation (with the total depreciable investment divided equally over project life) or through the Modified Accelerated Cost Recovery System schedule for 3,5,7,10,15, or 20 years. The profiles are laid out in the ‘A3. Conversion Factor Sheet’.
    

Figure 39. Financing Parameters.

Note: the values in the figure are representative and subjective to change based on user input.

# 5. Methods and Evaluation

## 5.1. Hourly Energy Flows

### 5.1.1. Power Plant Capacity Factors

The generation data is sourced as a ratio of the potential energy (MWh) generated by the power plant to the installed capacity of the power plant. These ratios vary hourly, daily, and seasonally based on the solar and wind traces, between a minimum (0%) and maximum level (100%), with 0% representing no energy output from the power plant and 100% representing the maximum energy output. The average of this yearly distribution of the ratios represents the power plant capacity factor. Currently, for simplification it is assumed that the performance of the generator is independent of its size, and so the same traces are used for all nominal capacities of solar and wind farm.


### 5.1.2. Hybrid Power Plant – Combination of Solar and Wind

For the hybrid power plant, the capacity factors from a solar farm and a wind farm in the same location are added in a weighted sum based on the solar and wind capacities. This is described in the equation below (Eq 4.).

$CF_h(t)=(P_s \times CF_s(t)+P_w \times CF_w(t))/(P_s+P_w)$

Here,

CF_h(t) is the capacity factor of the hybrid system at any given time t, in hours, CF_s(t) and CF_w(t) are the capacity factor of the individual solar PV and wind farm respectively, while P_s is the capacity of the solar PV in the hybrid system, and P_w is the capacity of the wind farm.

### 5.1.3. Battery Storage Model

The tool includes the option to incorporate energy storage in the form of a battery energy storage system (BESS), though future iterations may include the option for pumped hydro storage. To model the battery storage an algorithm was designed such that any excess electricity not utilised by the electrolyser is stored and then discharges when the electricity supply falls below the electrolyser maximum capacity. This is described in the following flow diagram (Figure 40).

![[Figure 40 BESS Tool Logic.png]]
_Figure 40. BESS Tool Logic_

The inclusion of the battery depends on the scenario which is selected by the user. If the battery is included then the capacity of the battery is set based on the storage capacity (MW) and storage duration (a choice between 1, 2, 4 and 8 hours of storage) provided by the user. The model also includes additional operational factors like the minimum state of charge (SOC) i.e., the minimum capacity of the battery that must be maintained at all times (% of maximum battery capacity), maximum allowable SOC, and the round-trip efficiency (% of the stored energy loss per charge and discharge cycle).



### 5.1.4. Electrolyser Capacity Factor and Output

Given that the electrolyser is the primary load of the power plant, the electrolyser capacity factors will directly be influenced by that of the power plant. Moreover, the electrolyser capacity factor is constrained by the inherent maximum and minimum operating loads of the electrolyser. Modern electrolyser systems are being designed to be highly adaptive and flexible to enable their operation with variable renewable energy supply. However, due to safe operating limits intrinsic to each class of electrolyser, a lower load range (higher than 0% of nominal load) must always be maintained while operational. The model uses the hourly electrolyser capacity factor to determine the energy rating of the electrolyser (Eq 5.).

$\text{Electrolyser∗Energy Rating}(\text{Elec∗ER})=CF_e(t)\times \text Elec_{Cap}(MW)\times 1\text hr$

Here the CF_e(t) is the hourly capacity factor of the electrolyser and the ElecCap represents the nominal capacity of the electrolyser. The electrolyser energy rating is then subsequently co related with the electrolyser’s specific energy consumption (SEC), that is the energy consumed by the electrolyser to generate a unit of hydrogen (usually represented as a kWh/kg of H2) to determine the amount of hydrogen generated during that hour (Eq 6.)

$H_2 \text Gen(\text kg/hr)=Elec_{ER}(MWh)\times \frac{1}{SEC(\text kWh/kg)}$

Note: If the variable profile for the SEC is selected, the tool adjusts the SEC to match the operating load of the electrolyser in each hour using the polynomial function (Defined)

## 5.2. Economic Analysis

### 5.2.1. Levelised Cost Analysis – LCH2

The levelised cost of hydrogen was used as the key metric for our analysis. To evaluate the levelised costs, the annual hydrogen output per year (inclusive of effects of degradation and overloading) is fed into a cost model to determine the levelised cost of hydrogen (LCH2) for the input configuration in $/kg. Here,

Y is the total number of years of operation, r is the discount rate, and P_n is the production of hydrogen in year n. Lastly,

C_n is the system costs in year n, which is inclusive of year 0 capital costs for the renewable energy generation, electrolysers and BESS, operation and maintenance costs for the renewable energy generation, electrolysers and BESS, stack replacement costs and water costs. Any additional sales (Sn) from by-products like surplus electricity retail to the grid or sale of by-product hydrogen are then subtracted from the costs as additional revenue streams as shown in Eq. 7.

$$LCH_2 = \frac{\sum_{n=0}^{Y} \frac{C_n - S_n}{(1 + r)^n}}{\sum_{n=0}^{Y} \frac{P_n}{(1 + r)^n}}$$

### 5.2.2. Business Case Analysis

For a comprehensive analysis, a detailed cash flow modelling is included the tool to evaluate additional metrics of net profit (at end of project life), return on investment (ROI) and payback period. The cash flow statements are built around the following factors:

- **Total Investment Required:** The total investment required encapsulates the capital cost of the electrolyser, battery, powerplant including cost of grid connection and any additional upfront costs plus indirect costs associated to EPC activities and land acquisition.
    
- **Project Financing:** The user is provided the option to finance the total investment required through a split of equity and loan, based on the input scenarios (Section 4.9)
    
- **Depreciation:** The tool automatically accounts for the depreciation based on the depreciation profile selected by the user. the depreciation profiles available in the tool include the straight line depreciation (with the total depreciable investment divided equally over project life) or through the Modified Accelerated Cost Recovery System schedule for 3,5,7,10,15, or 20 years.
    
- **Post Project Cash Flows:** The post-project cash flows include the salvage and decommissioning cost. The salvage cost is assumed as a positive cash flow and the decommission costs is assumed as a negative cash flow. The user can define both these costs as a percentage of total investment required.
    
- **Revenue:** The revenue is composed of the following inflows:
    
    - **Hydrogen Farm-Gate Sales Price:** The hydrogen sales rely on the retail cost of hydrogen; this retail cost is based on the levelised cost of hydrogen (evaluated by the tool) and a retail margin which is provided by the user as a $/kg of H2. This sale margin is set by the user in cell F80 of the ‘S2. Results sheet’ (as shown in Figure 41).
        
        Figure 41. Breakdown of retail cost of Hydrogen The cash flow statement section in the results sheet allows the user to define the retail cost of hydrogen based on the evaluated levelised cost and the additional sales margin provided by the user.
        
        Note: the values in the figure are representative and subjective to change based on user input.
        
    - **Surplus Electricity Sales:** The user can define the retail price of surplus energy to the grid as an average electricity spot price in the inputs sheet.
        
    - **Oxygen Sales:** The user can opt to retail the by-product oxygen as well, by defining the oxygen retail price in the inputs sheet. The amount of oxygen generated is evaluated by using the stochiometric ratio that 8 kg of O2 are generated per kg of H2 while splitting a mole of water.
        
- **Operating Costs:** The operating costs are in turn composed of the following outflows:
    
    - **Fixed OPEX:** The fixed OPEXs include the electrolyser OPEXs (O&M plus stack replacement), Power Plant OPEXs (O&Ms), Battery OPEXs (O&M and battery replacement) plus any additional annual operating costs included by the user.
        
    - **Variable OPEX:** The variable OPEXs include the cost of water consumed to drive the electrolyser and the cost of electricity purchased via PPA if applicable.
        
- **Additional Liabilities:** The additional labilities considered are:
    
    - **Inflation:** The user is provided the option to include the inflation rate in the inputs sheet. The inflation is then subsequently applied to all the sales and the operating costs.
        
    - **Variable OPEX:** The variable OPEXs include the cost of water consumed to drive the electrolyser and the cost of electricity purchased via PPA if applicable.
        

These cash flows are then used to establish the net cash flow statement. Our tool then subsequently uses the net cash flow statement to evaluate the following:

- **Net Profit:** The cumulative net cash flow at the end of the project then provides the profit at the end of the project (Eq.8).
    
    $$\text{Net Profit} = \sum_{i=0}^{i=n} \text{CNCF}_i$$
    
    Here i is the operating year, with i = 0 representing the plant installation and startup year, where all the required capital is invested upfront. n is the project life defined by the user (which can be upto 50 years), the tool automatically adjusts the cash flows to iterate upto the project life. CNCF represents the cumulative net cash flow for the year i.
    
- **The Return on Investment (ROI):** The ROI is then evaluated as the ratio of the net profit to the initial total investment
    
- **Payback:** To evaluate the payback period, the excel sheet calculates the number of years required for the positive cash flows to payback the initial capital investment, as shown in Eq. 9:
    
    $$
\text{Pay Back Period} = Y_n + \frac{|\text{CNCF}(Y_n)|}{\text{NCF}(Y_{n+1})}
$$
    
    Here, Yn represents the last year in which the cumulative net cash flow (CNCF) is negative, Yn+1 is the year it becomes positive for the first time and NCF is the net cash flow (income after tax and depreciation) in the year Yn+1.
    
    Note: The tool automatically evaluates these parameters based on the user inputs. These scenarios will be further improved after stakeholder engagement and the road mapping stage of the  Hydrogen Feasibility study.
    

# 6. Tool Limitations and Next Steps

The tool currently has the following limitations:

- The scope of the tool is currently limited to farm-gate hydrogen generation.
    
- The preloaded solar and wind traces are based time-sequential, hourly observations of the solar and wind data at each specific location (through historical data). These do not include solar and wind outputs from existing power plants in the area, however data from the existing solar and wind farms can be added as a custom analysis (Section 4.2.1). The traces for existing power plants connected to the NEM can be accessed from our other open-source tool NEMOSIS (available here)
    
- The tool also currently relies on purely renewable powered electricity supply both in standalone and on grid connected configuration, additional functionality of having a fossil fuel electricity mix is planned to be included in the next iteration (version) of the tool.
    
- The storage model is currently simplistic, further room for optimising the battery operation remains.
    

The next steps of the tool development are expected to involve:

- A website-based version of this tool.
    
- A python-based optimisation code to evaluate the high-capacity factor and least cost operation parameters is being developed.
    
- This tool is part of larger project which aims to develop a feasibility framework for complete hydrogen value chain that includes generation, storage, transportation, conversion, and export of hydrogen/hydrogen carriers, which are in development.
    

