

Daily solar flux as a function of latitude and time


https://kb.solargis.com/docs/pv-energy-yield-simulation
### Evaluate application simulations

Solargis Evaluate web application, specifically the PV energy system simulator, employs our latest and most advanced simulation methods. It supports two types of energy systems, each using a distinct simulation approach:

- **GTI simulator** for theoretical calculation within GTI energy systems
- **PV simulator** for photovoltaic (PV) energy systems.


#### GTI simulator

The GTI simulator is designed as a fast and simple tool for calculating Global Tilt Irradiance (GTI) **without involving electrical simulations**. It focuses exclusively on horizontal and inclined planes of PV module, lacking support for terrain variations, and is limited to simple layouts without bi-facial PV module capabilities.


GTI energy system simulation inputs

Key input data types to the GTI simulator:

- **Solar and Meteorological Time Series**: Essential are GHI and DNI solar radiation inputs.
- **Site Conditions**: This includes location latitude and longitude.
- **PV system configuration**:
    - **Mounting details**: Select from several PV module mountings.
    - **Azimuth**: Orientation of the GTI system to the cardinal points.
    - **Spacing**: Distance between PV modules.


>> GTI energy system simulation processing
The processing consists of an optical simulation only, which includes calculations of the light interaction with surface of a PV module:
> - [Isotropic Sky Model](https://kb.solargis.com/docs/incident-irradiance#solargis-isotropic-sky-model): GTI model assumes uniform distribution of solar radiation in the sky dome.
> - [View Factor](https://kb.solargis.com/docs/incident-irradiance#view-factor): Calculates the proportion of the sky visible from a given point on the panel, which enables quick shading assessment.


GTI energy system simulation outputs

The GTI simulator generates several outputs, including:

- **GTI Theoretical**: Provides GTI inoput to the front side of a PV modul ignoring possible shading.


>> PV energy system simulation inputs
The PV energy system simulator processes the following inputs:
>- **Solar and Meteorological Time Series and TMY data**: Essential for assessing solar radiation and climate conditions.
    
>- **Site Geographical Conditions**: Includes location coordinates, terrain, ground albedo, soiling and snow losses, and horizon.
>- **PV System Configuration**:
    - **PV Configuration from energy system designer**: Details about the photovoltaic system setup, e.g., module or table layout.    
    - **Components**: Specifications of PV modules, inverters, and transformers.    
    - **Electrical Components Layout**: Electrical connections of the components, including losses.    
- **Other Factors**: Considerations such as self-consumption, degradation rates, and system unavailability.




PV energy system simulation outputs

The PV energy system simulator provides the following outputs:

- **GTI Outputs**: We provide Global Tilt Irradiance (GTI) values per time slot, detailing various stages of losses—from theoretical estimates to spectrally corrected values.
    
- **PV Output**: The simulation delivers photovoltaic output data, including total yield and specific yield per time slot, reflecting various stages of losses, including electrical losses due to snow and soiling, up to the grid connection.
    
- **Uncertainty Analysis**: We include an assessment of uncertainty associated with the solar radiation and meteorological parameters, including the one in individual PV simulation steps, helping users understand the reliability of the results.
    
- **Analytical Outputs**: The Evaluate application offers a range of analytical outputs, including graphs and charts that visualize key performance metrics and trends.
    
- **Data Deliverables**: Comprehensive reports and data sets are provided, enabling further analysis and integration into other systems or reports.


![[image.png]]