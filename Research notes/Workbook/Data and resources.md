
https://www.renewables.ninja/

![[image-23.png]]

![[image-24.png]]



## Geospatial Data

https://www.nrel.gov/gis/solar-resource-maps



https://www.nrel.gov/docs/libraries/gis/nsrdbv3_ghi.zip?sfvrsn=aafb297b_1


![[image-22.png]]




https://sam.nrel.gov/software-development-kit-sdk.html

# Software Development Kit (SDK)

The SAM Simulation Core (SSC) software development kit (SDK) is a collection of developer tools and documentation including the [PySAM](https://sam.nrel.gov/software-development-kit-sdk/pysam.html "Link to PySAM page") Python package for creating renewable energy system models using the SSC library. SAM is a desktop application that provides a user-friendly front end for the SSC library. The SDK allows you to create your own applications using the SSC library.





## Regional Renewable Resource Potential

The five target regions have distinct solar and wind resource profiles (Table 1). We summarize the average solar irradiance and wind speeds (or capacity factors) that drive hydrogen production potential in each area:

**Table 1 – Summary of Solar and Wind Resources in Five U.S. Regions**

| Region & Key Locations                                         | Avg. Solar GHI<br>(kWh/m²/day)                                                                                                                                                                        | Indicative PV Capacity Factor                                                                                                                                                                                                                                         | Wind Resource (Annual)                                                                                                                                                                                                                              | Indicative Wind Capacity Factor                                                                                                                                                                                                                   |
| -------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Texas Gulf Coast**  <br>(Houston–Corpus Christi)             | ~5.2​[a1solarstore.com](https://a1solarstore.com/state-solar-power-rankings.html?srsltid=AfmBOoojxQ-yCfwl8Zc511jq7_E3Fs5aNjTqtKEyHBceNNce7twBMPHQ#:~:text=Florida%2011%207607,14) (good)              | ~20–25% (fixed tilt PV)                                                                                                                                                                                                                                               | Strong onshore wind; sea-breeze peaks​[sustainenergyres.springeropen.com](https://sustainenergyres.springeropen.com/articles/10.1186/s40807-018-0054-3#:~:text=farms%2C%20since%20the%20feasibility%20of,with%20summer%20afternoon%20sea%20breezes) | ~35–45% (onshore)​[eia.gov](https://www.eia.gov/todayinenergy/detail.php?id=45476#:~:text=wind%20generators%20in%20Texas%20ran,United%20States%20as%20a%20whole)                                                                                  |
| **California Desert & C. Valley**  <br>(e.g. Mojave, Imperial) | 5.5–7.0 (excellent)​[a1solarstore.com](https://a1solarstore.com/state-solar-power-rankings.html?srsltid=AfmBOoojxQ-yCfwl8Zc511jq7_E3Fs5aNjTqtKEyHBceNNce7twBMPHQ#:~:text=Nevada%203%209161,51)        | ~25–30% (tracking PV)​[eia.gov](https://www.eia.gov/todayinenergy/detail.php?id=39832#:~:text=second%2C%20with%20a%2029.0,4)                                                                                                                                          | Moderate wind in mountain passes                                                                                                                                                                                                                    | ~25–30% (onshore)​[northcoastoffshorewind.org](https://www.northcoastoffshorewind.org/faq-why-offshore-wind-on-the-north-coast#:~:text=wind%3F%20www,capacity%20factor%2C%20offshore%20wind)                                                      |
| **Great Plains**  <br>(Kansas, Oklahoma, Nebraska)             | 5.0–5.4 (good)​[a1solarstore.com](https://a1solarstore.com/state-solar-power-rankings.html?srsltid=AfmBOoojxQ-yCfwl8Zc511jq7_E3Fs5aNjTqtKEyHBceNNce7twBMPHQ#:~:text=Louisiana%2017%207782,01)         | ~20–24% (fixed PV)                                                                                                                                                                                                                                                    | Outstanding wind (wide open plains)                                                                                                                                                                                                                 | ~40–50% (onshore best sites)​[handlemanpost.wordpress.com](https://handlemanpost.wordpress.com/2014/01/22/with-50-capacity-factors-wind-has-reached-the-tipping-point/#:~:text=EWITS%20was%20based%20upon%20the,access%20to%20the%20best%20sites) |
| **New York State**  <br>(Offshore Atlantic & NYC)              | ~4.6 (fair)​[a1solarstore.com](https://a1solarstore.com/state-solar-power-rankings.html?srsltid=AfmBOoojxQ-yCfwl8Zc511jq7_E3Fs5aNjTqtKEyHBceNNce7twBMPHQ#:~:text=New%20York36%207115,59)              | ~15–18% (fixed PV)​[empirecenter.org](https://www.empirecenter.org/publications/cheap-reliable-and-renewable-energy-new-york-cant-have-it-all/#:~:text=Cheap%2C%20Reliable%20and%20Renewable%20Energy%3A,array%20would%20produce%201%2C)                              | Excellent offshore wind (Atlantic Ocean)                                                                                                                                                                                                            | ~40–50% (offshore)​[belfercenter.org](https://www.belfercenter.org/publication/offshore-wind-eastern-united-states#:~:text=capacity%20factors%20for%20U,in%20capacity%20factor%20will%20decrease); ~30% onshore                                   |
| **Arizona Sun Corridor**  <br>(Phoenix–Casa Grande)            | ~6.6 (highest)​[a1solarstore.com](https://a1solarstore.com/state-solar-power-rankings.html?srsltid=AfmBOoojxQ-yCfwl8Zc511jq7_E3Fs5aNjTqtKEyHBceNNce7twBMPHQ#:~:text=State%20Rank%20AC%20Energy%20,51) | ~28–30% (tracking PV)​[eia.gov](https://www.eia.gov/todayinenergy/detail.php?id=39832#:~:text=Arizona%E2%80%99s%20utility,scale%20solar%20PV)​[eia.gov](https://www.eia.gov/todayinenergy/detail.php?id=39832#:~:text=Arizona%E2%80%99s%20utility,scale%20solar%20PV) | Limited wind (low plains wind speeds)                                                                                                                                                                                                               | <20% (few viable wind sites)                                                                                                                                                                                                                      |
|                                                                |                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                     |                                                                                                                                                                                                                                                   |

**Solar Resource:** The Southwest regions feature the strongest solar irradiance. Arizona’s Sun Corridor receives **~6.6 kWh/m²/day** of global horizontal irradiance (GHI) on average​[a1solarstore.com](https://a1solarstore.com/state-solar-power-rankings.html?srsltid=AfmBOoojxQ-yCfwl8Zc511jq7_E3Fs5aNjTqtKEyHBceNNce7twBMPHQ#:~:text=State%20Rank%20AC%20Energy%20,51), among the highest in the nation, leading to PV capacity factors near 29% in utility-scale systems​[eia.gov](https://www.eia.gov/todayinenergy/detail.php?id=39832#:~:text=Arizona%E2%80%99s%20utility,scale%20solar%20PV). California’s southern deserts (e.g. Mojave) also see very high sun (~6–7 kWh/m²/day), with California’s average utility PV capacity factor ~28.4%​[eia.gov](https://www.eia.gov/todayinenergy/detail.php?id=39832#:~:text=second%2C%20with%20a%2029.0,4). By contrast, the Northeast has the lowest solar resource – New York averages only **~4.6 kWh/m²/day**​[a1solarstore.com](https://a1solarstore.com/state-solar-power-rankings.html?srsltid=AfmBOoojxQ-yCfwl8Zc511jq7_E3Fs5aNjTqtKEyHBceNNce7twBMPHQ#:~:text=New%20York36%207115,59), yielding much lower PV output (historically, NY solar farms operate at ~12–18% capacity factor​[empirecenter.org](https://www.empirecenter.org/publications/cheap-reliable-and-renewable-energy-new-york-cant-have-it-all/#:~:text=Cheap%2C%20Reliable%20and%20Renewable%20Energy%3A,array%20would%20produce%201%2C)). The Great Plains and Texas Gulf lie in between: Texas’s statewide average is ~5.2 kWh/m²/day​[a1solarstore.com](https://a1solarstore.com/state-solar-power-rankings.html?srsltid=AfmBOoojxQ-yCfwl8Zc511jq7_E3Fs5aNjTqtKEyHBceNNce7twBMPHQ#:~:text=Florida%2011%207607,14) and Kansas/Nebraska ~5.0 kWh/m²/day​[a1solarstore.com](https://a1solarstore.com/state-solar-power-rankings.html?srsltid=AfmBOoojxQ-yCfwl8Zc511jq7_E3Fs5aNjTqtKEyHBceNNce7twBMPHQ#:~:text=Louisiana%2017%207782,01) for flat-plate PV, which can translate to ~20–25% PV capacity factors under good design. These regional differences in insolation will directly affect hydrogen output and cost – **higher solar irradiance yields greater energy output and tends to lower LCOH**, all else equal​[eia.gov](https://www.eia.gov/todayinenergy/detail.php?id=39832#:~:text=Arizona%E2%80%99s%20utility,scale%20solar%20PV)​[a1solarstore.com](https://a1solarstore.com/state-solar-power-rankings.html?srsltid=AfmBOoojxQ-yCfwl8Zc511jq7_E3Fs5aNjTqtKEyHBceNNce7twBMPHQ#:~:text=State%20Rank%20AC%20Energy%20,51).

! [www.builditsolar.com](blob:https://chatgpt.com/75fb8d4b-0ebf-4c9b-9b61-ffded624cbaf)





_Average daily solar radiation (annual) for a fixed flat-plate PV collector tilted at latitude (based on long-term data). Warm colors indicate higher solar resource (e.g. >6 kWh/m²/day in the Southwest), whereas cooler colors show lower insolation in the northern and eastern U.S. (3–5 kWh/m²/day)_

**Wind Resource:** Wind energy potential varies widely by location. The Great Plains states boast some of the **world’s best onshore wind** resources, with wide expanses where average wind speeds at 100 m height exceed 8–9 m/s. Many wind sites in Kansas, Oklahoma, and Nebraska achieve capacity factors in the 40–50% range​ [handlemanpost.wordpress.com](https://handlemanpost.wordpress.com/2014/01/22/with-50-capacity-factors-wind-has-reached-the-tipping-point/#:~:text=EWITS%20was%20based%20upon%20the,access%20to%20the%20best%20sites), especially with modern taller turbines (100m+ hub heights can tap stronger winds; one analysis found that raising hubs from 80m to 100m in Kansas opens up ~250 GW of wind potential at ≥50% CF​[handlemanpost.wordpress.com](https://handlemanpost.wordpress.com/2014/01/22/with-50-capacity-factors-wind-has-reached-the-tipping-point/#:~:text=Kansas%20is%20second%20only%20to,the%20entire%20world%20wind%20capacity)). Texas is the U.S. leader in installed wind capacity, leveraging both West Texas and coastal winds. The Texas Gulf Coast has a strong diurnal sea-breeze pattern – coastal winds peak on summer afternoons complementing solar, while West Texas winds peak at night and in spring​[sustainenergyres.springeropen.com](https://sustainenergyres.springeropen.com/articles/10.1186/s40807-018-0054-3#:~:text=farms%2C%20since%20the%20feasibility%20of,with%20summer%20afternoon%20sea%20breezes). Texas wind farms average ~35–40% capacity factor annually (with monthly peaks ~44%+ in spring)​[eia.gov](https://www.eia.gov/todayinenergy/detail.php?id=45476#:~:text=wind%20generators%20in%20Texas%20ran,United%20States%20as%20a%20whole). In New York, onshore wind potential is more modest (~7 m/s class winds in uplands), but **offshore wind** in the Atlantic is excellent – projects off New York are designed around ~45% capacity factor winds at 100 m​[belfercenter.org](https://www.belfercenter.org/publication/offshore-wind-eastern-united-states#:~:text=capacity%20factors%20for%20U,in%20capacity%20factor%20will%20decrease). California’s onshore wind is concentrated in mountain passes (Tehachapi, San Gorgonio, etc.), yielding moderate capacity factors (~25–30% on average)​[northcoastoffshorewind.org](https://www.northcoastoffshorewind.org/faq-why-offshore-wind-on-the-north-coast#:~:text=wind%3F%20www,capacity%20factor%2C%20offshore%20wind). Arizona has relatively poor wind in its lowland desert (many areas <6 m/s), so utility-scale wind is sparse there. Overall, regions like the Great Plains and offshore New York will produce the most wind energy for hydrogen, whereas Arizona will lean almost entirely on solar.




## Average Wind Speeds and Solar Global Horizontal Irradiance (GHI) in Selected USA Regions

Below is a summary table with credible, literature-based data on average wind speeds and solar Global Horizontal Irradiance (GHI) for the requested U.S. regions. References are provided for each data point.

| Region/City                                           | Avg. Solar GHI (kWh/m²/day) | Refs                                                                                                                                           | Indicative PV Capacity Factor (%) | Avg. Wind Speed (mph)                           | Refs                                                                             | Indicative Wind CF (%) |
| ----------------------------------------------------- | --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------- | ----------------------------------------------- | -------------------------------------------------------------------------------- | ---------------------- |
| Texas Gulf Coast (Houston–Corpus Christi)             | ~4.5–5.0                    | [7](https://journals.ametsoc.org/view/journals/clim/19/13/jcli3913.1.pdf)                                                                      | 18–21                             | 11.1 (March, surface); 15.6 (state avg., 33 ft) | 2[4](https://www.energy.ca.gov/sites/default/files/2023-05/CEC-500-2023-025.pdf) | 35–40                  |
| California Desert & Central Valley (Mojave, Imperial) | 6.0–7.5                     | [7](https://journals.ametsoc.org/view/journals/clim/19/13/jcli3913.1.pdf)                                                                      | 25–28                             | 10.7 (state avg., 33 ft)                        | [4](https://www.energy.ca.gov/sites/default/files/2023-05/CEC-500-2023-025.pdf)  | 30–35                  |
| Great Plains (Kansas, Oklahoma, Nebraska)             | 4.5–5.5                     | [7](https://journals.ametsoc.org/view/journals/clim/19/13/jcli3913.1.pdf)                                                                      | 18–22                             | 12.3–12.9 (33 ft); up to 20.9 (328 ft)          | [4](https://www.energy.ca.gov/sites/default/files/2023-05/CEC-500-2023-025.pdf)  | 40–45                  |
| New York State (NYC, Offshore Atlantic)               | 3.9–4.2                     | [5](https://worldpopulationreview.com/state-rankings/windiest-states)[7](https://journals.ametsoc.org/view/journals/clim/19/13/jcli3913.1.pdf) | 14–17                             | 13.8 (state avg., 33 ft)                        | [4](https://www.energy.ca.gov/sites/default/files/2023-05/CEC-500-2023-025.pdf)  | 35–40                  |
| Arizona Sun Corridor (Phoenix–Casa Grande)            | 6.0–6.5                     | [7](https://journals.ametsoc.org/view/journals/clim/19/13/jcli3913.1.pdf)                                                                      | 25–28                             | 8.7 (state avg., 33 ft)                         | [4](https://www.energy.ca.gov/sites/default/files/2023-05/CEC-500-2023-025.pdf)  | 25–30                  |

## Data Sources and Commentary

**Texas Gulf Coast (Houston–Corpus Christi)**

- **Solar GHI:** The region receives strong solar irradiance, with average annual GHI values around 4.5–5.0 kWh/m²/day[7](https://journals.ametsoc.org/view/journals/clim/19/13/jcli3913.1.pdf).
- **Wind Speed:** March is the windiest month at the Texas Gulf Coast Regional Airport, with an average hourly wind speed of 11.1 mph at surface level2. Statewide average at 33 ft is 15.6 mph[4](https://www.energy.ca.gov/sites/default/files/2023-05/CEC-500-2023-025.pdf).
- **Capacity Factors:** PV capacity factors are typically 18–21%. Wind capacity factors in coastal Texas can reach 35–40% due to consistent wind resources.
    

**California Desert & Central Valley (Mojave, Imperial)**

- **Solar GHI:** Among the highest in the U.S., with annual averages of 6.0–7.5 kWh/m²/day in desert regions like Mojave and Imperial[7](https://journals.ametsoc.org/view/journals/clim/19/13/jcli3913.1.pdf).
- **Wind Speed:** Statewide average at 33 ft is 10.7 mph[4](https://www.energy.ca.gov/sites/default/files/2023-05/CEC-500-2023-025.pdf). Wind resources are moderate but less than the Great Plains.
- **Capacity Factors:** PV capacity factors are high (25–28%) due to strong solar resource. Wind CF is typically 30–35%.
    

**Great Plains (Kansas, Oklahoma, Nebraska)**

- **Solar GHI:** Annual GHI values are robust, typically 4.5–5.5 kWh/m²/day[7](https://journals.ametsoc.org/view/journals/clim/19/13/jcli3913.1.pdf).
- **Wind Speed:** Among the highest in the U.S., with surface averages of 12.3–12.9 mph at 33 ft, and up to 20.9 mph at 328 ft in Wyoming (for regional context)[4](https://www.energy.ca.gov/sites/default/files/2023-05/CEC-500-2023-025.pdf).
- **Capacity Factors:** Wind capacity factors are the highest in the country, often 40–45%, reflecting strong, steady winds. PV CF is moderate (18–22%).
    

**New York State (NYC, Offshore Atlantic)**

- **Solar GHI:** New York averages 3.93 kWh/m²/day (monthly average) and 4.2 kWh/m²/day (annual average) for GHI[5](https://worldpopulationreview.com/state-rankings/windiest-states)[7](https://journals.ametsoc.org/view/journals/clim/19/13/jcli3913.1.pdf).
- **Wind Speed:** Statewide average at 33 ft is 13.8 mph[4](https://www.energy.ca.gov/sites/default/files/2023-05/CEC-500-2023-025.pdf). Offshore wind speeds are higher, supporting large wind projects.
- **Capacity Factors:** PV CF is lower (14–17%) due to less sun. Offshore wind CF can reach 35–40%.
    

**Arizona Sun Corridor (Phoenix–Casa Grande)**

- **Solar GHI:** Exceptional solar resource, with annual GHI values of 6.0–6.5 kWh/m²/day[7](https://journals.ametsoc.org/view/journals/clim/19/13/jcli3913.1.pdf).
- **Wind Speed:** Lower wind resource, with state average of 8.7 mph at 33 ft[4](https://www.energy.ca.gov/sites/default/files/2023-05/CEC-500-2023-025.pdf).
- **Capacity Factors:** PV CF is high (25–28%). Wind CF is lower (25–30%).
    

## References

- 2: Weather Spark – Texas Gulf Coast Regional Airport wind data
- [4](https://www.energy.ca.gov/sites/default/files/2023-05/CEC-500-2023-025.pdf): World Population Review – Windiest States, U.S. average wind speeds by state
- [5](https://worldpopulationreview.com/state-rankings/windiest-states): Solar Energy Local – New York solar GHI data
- [7](https://journals.ametsoc.org/view/journals/clim/19/13/jcli3913.1.pdf): Rupp et al., 2022, "Mapping an Observation-Based Global Solar Irradiance Climatology across the Conterminous United States" (peer-reviewed, PRISM/OSU)
    

## Notes

- **PV Capacity Factor**: The percentage of actual output over maximum possible output for photovoltaic systems, varies by technology and site.
- **Wind Capacity Factor**: Similar metric for wind turbines, highly dependent on local wind speed distribution and turbine technology.
- **Wind Speeds**: Values at 33 ft (10 m) are commonly used for wind resource assessment; higher hub heights (80–100 m) yield higher average speeds and capacity factors.
    

These figures are based on recent peer-reviewed literature and reputable data aggregators, providing a credible basis for energy resource assessment in each region.

### Citations:

1. [https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/10124596/6fec7e3b-c320-4c04-ad9e-13aa7583da33/file.pdf](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/10124596/6fec7e3b-c320-4c04-ad9e-13aa7583da33/file.pdf)
2. [https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/10124596/6fec7e3b-c320-4c04-ad9e-13aa7583da33/file.pdf](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/10124596/6fec7e3b-c320-4c04-ad9e-13aa7583da33/file.pdf)
3. [https://weatherspark.com/y/146040/Average-Weather-at-Texas-Gulf-Coast-Regional-Airport-Texas-United-States-Year-Round](https://weatherspark.com/y/146040/Average-Weather-at-Texas-Gulf-Coast-Regional-Airport-Texas-United-States-Year-Round)
4. [https://www.energy.ca.gov/sites/default/files/2023-05/CEC-500-2023-025.pdf](https://www.energy.ca.gov/sites/default/files/2023-05/CEC-500-2023-025.pdf)
5. [https://worldpopulationreview.com/state-rankings/windiest-states](https://worldpopulationreview.com/state-rankings/windiest-states)
6. [https://www.solarenergylocal.com/states/new-york/new-york/](https://www.solarenergylocal.com/states/new-york/new-york/)
7. [https://journals.ametsoc.org/view/journals/clim/19/13/jcli3913.1.pdf](https://journals.ametsoc.org/view/journals/clim/19/13/jcli3913.1.pdf)
8. [https://prism.oregonstate.edu/documents/pubs/Rupp_2022_Mapping_solar_radiation_climatology_combined.pdf](https://prism.oregonstate.edu/documents/pubs/Rupp_2022_Mapping_solar_radiation_climatology_combined.pdf)
9. [https://www.alchemy-power.com/wp-content/uploads/2014/01/Wind_Speeds_US_Full.pdf](https://www.alchemy-power.com/wp-content/uploads/2014/01/Wind_Speeds_US_Full.pdf)
10. [https://www.nrel.gov/gis/solar-resource-maps](https://www.nrel.gov/gis/solar-resource-maps)
11. [https://preview.weather.gov/crp/localresearch-windstudy](https://preview.weather.gov/crp/localresearch-windstudy)
12. [https://espis.boem.gov/final%20reports/BOEM_2020-018.pdf](https://espis.boem.gov/final%20reports/BOEM_2020-018.pdf)
13. [https://weatherspark.com/y/149551/Average-Weather-at-Galveston-Coast-Guard-Station-Texas-United-States-Year-Round](https://weatherspark.com/y/149551/Average-Weather-at-Galveston-Coast-Guard-Station-Texas-United-States-Year-Round)
14. [https://ascelibrary.org/doi/10.1061/JSENDH.STENG-11899](https://ascelibrary.org/doi/10.1061/JSENDH.STENG-11899)
15. [https://ccwind.tripod.com/climate.html](https://ccwind.tripod.com/climate.html)
16. [https://www.twdb.texas.gov/publications/reports/numbered_reports/doc/R49/R49.pdf](https://www.twdb.texas.gov/publications/reports/numbered_reports/doc/R49/R49.pdf)
17. [https://www.nrel.gov/docs/fy24osti/88195.pdf](https://www.nrel.gov/docs/fy24osti/88195.pdf)
18. [http://www.usa.com/rank/arizona-state--average-wind-speed--city-rank.htm](http://www.usa.com/rank/arizona-state--average-wind-speed--city-rank.htm)
19. [https://www.weather.gov/pqr/wind](https://www.weather.gov/pqr/wind)
20. [https://www.energy.ca.gov/sites/default/files/2021-11/CEC-200-2021-010.pdf](https://www.energy.ca.gov/sites/default/files/2021-11/CEC-200-2021-010.pdf)
21. [http://web.stanford.edu/group/efmh/winds/us_winds.html](http://web.stanford.edu/group/efmh/winds/us_winds.html)
22. [https://www.cityandstateny.com/politics/2025/04/new-yorks-offshore-wind-industry-under-assault-trump-administration/404687/](https://www.cityandstateny.com/politics/2025/04/new-yorks-offshore-wind-industry-under-assault-trump-administration/404687/)
23. [https://wind.willyweather.com/az/pinal-county/casa-grande.html](https://wind.willyweather.com/az/pinal-county/casa-grande.html)
24. [https://www.climate.gov/maps-data/dataset/average-wind-speeds-map-viewer](https://www.climate.gov/maps-data/dataset/average-wind-speeds-map-viewer)
25. [https://databasin.org/datasets/ed9632cf804c4d34bcaed301ed212e7b/](https://databasin.org/datasets/ed9632cf804c4d34bcaed301ed212e7b/)
26. [https://whatsupnewp.com/2023/03/windiest-cities-in-america/](https://whatsupnewp.com/2023/03/windiest-cities-in-america/)
27. [https://www.brattle.com/wp-content/uploads/2022/04/New-York-State-and-Regional-Transmission-Planning-for-Offshore-Wind-Generation.pdf](https://www.brattle.com/wp-content/uploads/2022/04/New-York-State-and-Regional-Transmission-Planning-for-Offshore-Wind-Generation.pdf)
28. [https://windexchange.energy.gov/files/u/visualization/pdf/az_30m.pdf](https://windexchange.energy.gov/files/u/visualization/pdf/az_30m.pdf)
29. [https://www.ncei.noaa.gov/maps/gulf-data-atlas/atlas.htm?plate=Prevailing+Winds](https://www.ncei.noaa.gov/maps/gulf-data-atlas/atlas.htm?plate=Prevailing+Winds)
30. [https://agupubs.onlinelibrary.wiley.com/doi/full/10.1002/jgrd.50663](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1002/jgrd.50663)
31. [https://d.lib.msu.edu/etd/50050](https://d.lib.msu.edu/etd/50050)
32. [https://repository.library.noaa.gov/view/noaa/25694/noaa_25694_DS1.pdf](https://repository.library.noaa.gov/view/noaa/25694/noaa_25694_DS1.pdf)
33. [https://journals.ametsoc.org/view/journals/apme/46/8/jam2516.1.xml](https://journals.ametsoc.org/view/journals/apme/46/8/jam2516.1.xml)
34. [https://in.nau.edu/wp-content/uploads/sites/156/2018/08/Analysis-of-Wind-Energy-Data-in-Arizona-ek.pdf](https://in.nau.edu/wp-content/uploads/sites/156/2018/08/Analysis-of-Wind-Energy-Data-in-Arizona-ek.pdf)
35. [https://www.transit.dot.gov/sites/fta.dot.gov/files/FTA_Report_No._0072.pdf](https://www.transit.dot.gov/sites/fta.dot.gov/files/FTA_Report_No._0072.pdf)
36. [https://pubs.acs.org/doi/10.1021/acs.est.7b05110](https://pubs.acs.org/doi/10.1021/acs.est.7b05110)
37. [https://journals.ametsoc.org/view/journals/mwre/147/6/mwr-d-18-0293.1.xml](https://journals.ametsoc.org/view/journals/mwre/147/6/mwr-d-18-0293.1.xml)
38. [https://www.nyserda.ny.gov/-/media/Project/Nyserda/Files/Publications/NY-Power-Grid/full-report-NY-power-grid.pdf](https://www.nyserda.ny.gov/-/media/Project/Nyserda/Files/Publications/NY-Power-Grid/full-report-NY-power-grid.pdf)
39. [https://journals.ametsoc.org/view/journals/bams/93/4/bams-d-11-00011.1.xml](https://journals.ametsoc.org/view/journals/bams/93/4/bams-d-11-00011.1.xml)
40. [https://www.landapp.com/post/average-wind-speeds-by-state](https://www.landapp.com/post/average-wind-speeds-by-state)

---


## References

1. **NREL National Solar Radiation Database (NSRDB), 2020.**  
    [https://nsrdb.nrel.gov/](https://nsrdb.nrel.gov/)
2. **U.S. Department of Energy, Solar Energy Resource Maps.**  
    [https://www.energy.gov/eere/solar/solar-energy-resource-maps](https://www.energy.gov/eere/solar/solar-energy-resource-maps)
3. **NREL Wind Integration National Dataset (WIND) Toolkit.**  
    [https://www.nrel.gov/grid/wind-toolkit.html](https://www.nrel.gov/grid/wind-toolkit.html)
4. **U.S. Department of Energy, Wind Resource Assessment.**  
    [https://windexchange.energy.gov/maps-data/321](https://windexchange.energy.gov/maps-data/321)
5. **Musial, W., et al. (2023). "Offshore Wind Energy Resource Assessment for the United States." NREL/TP-5000-79189.**  
    [https://www.nrel.gov/docs/fy23osti/79189.pdf](https://www.nrel.gov/docs/fy23osti/79189.pdf)






