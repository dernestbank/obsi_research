


$SEC(KWh/kg) = a \times Load^2 + b \times Load +c$

`Load` = % of rated power (e.g., 100%, 80%)

`SEC` = kWh of electricity needed to produce 1 kg of hydrogen

Coefficients:

- `a = -0.499`
    
- `b = 48.756`
    
- `c = 6.096`

![[Pasted image 20250405125236.png|400]]



How specific energy consumption changes with load


comparing with
Vrs [@astrianiOptimalPlanningRenewable2024]
Models **efficiency as a function of operating power** using an **exponential + linear** model.
Shows a **peak efficiency** curve — high at optimal load (typically 60–80%), then drops.

![[Pasted image 20250405125255.png|400]]


## **Key Differences & Use Cases**

| Feature            | Excel SEC Model                        | Research η Model                             |
| ------------------ | -------------------------------------- | -------------------------------------------- |
| **Output**         | SEC (kWh/kg H₂)                        | η (Efficiency %)                             |
| **Input**          | % Rated Load                           | % Rated Power                                |
| **Focus**          | Energy needed per kg H₂                | Electrical-to-hydrogen conversion efficiency |
| **Application**    | TEA, basic modeling, Excel calculators | Simulation, advanced optimization, MATLAB    |
| **Interpretation** | Lower SEC = better                     | Higher η = better                            |


## **How They Relate**

They're **inversely related**

$$η ≈ \frac{LHV_2}{SEC}$$
Where:

- `LHV_H₂` = Lower heating value of hydrogen (e.g., 33.3 kWh/kg)
    
- So if SEC = 51.27 kWh/kg → η ≈ 33.3 / 51.27 ≈ 65%







-----------

Power model of WInd Turbine

Wind turbine power generation can be predicted using the fundamental equation:

**Power (W) = 0.5 × ρ × πr² × Cp × v³**  
where:

- **ρ** = Air density (typically 1.225 kg/m³ at sea level)[1](https://www.omnicalculator.com/ecology/wind-turbine)[7](https://energyeducation.ca/encyclopedia/Wind_power)
    
- **r** = Rotor radius (meters)[1](https://www.omnicalculator.com/ecology/wind-turbine)[7](https://energyeducation.ca/encyclopedia/Wind_power)
    
- **Cp** = Power coefficient (turbine efficiency, ≤ 59.3% per Betz's law)[1](https://www.omnicalculator.com/ecology/wind-turbine)[3](https://reads.alibaba.com/7-factors-that-impact-wind-turbine-efficiency/)
    
- **v** = Wind speed (m/s)[1](https://www.omnicalculator.com/ecology/wind-turbine)[7](https://energyeducation.ca/encyclopedia/Wind_power)
    

## Key Dependencies Explained

## 1. **Wind Speed (v)**

- Power output increases **cubically** with wind speed (doubling wind speed increases power 8x)[7](https://energyeducation.ca/encyclopedia/Wind_power)[8](https://energy-elege.com/wind-turbine-power-generation-efficiency/).
    
- Turbines operate between **cut-in** (3–4 m/s) and **cut-out** (25–30 m/s) speeds[5](https://www.landgate.com/news/how-weather-affects-wind-turbines-in-the-united-states)[7](https://energyeducation.ca/encyclopedia/Wind_power).
    

## 2. **Air Density (ρ)**

- Depends on altitude, temperature, and pressure. Colder, denser air increases output[3](https://reads.alibaba.com/7-factors-that-impact-wind-turbine-efficiency/)[5](https://www.landgate.com/news/how-weather-affects-wind-turbines-in-the-united-states)[7](https://energyeducation.ca/encyclopedia/Wind_power).
    

## 3. **Rotor Radius (r)**

- Larger blades capture more kinetic energy: **swept area (A = πr²)** is proportional to power[3](https://reads.alibaba.com/7-factors-that-impact-wind-turbine-efficiency/)[7](https://energyeducation.ca/encyclopedia/Wind_power)[8](https://energy-elege.com/wind-turbine-power-generation-efficiency/).
    

## 4. **Turbine Efficiency (Cp)**

- Combines aerodynamic, mechanical, and electrical losses. Typical real-world efficiency: **30–40%**[1](https://www.omnicalculator.com/ecology/wind-turbine)[3](https://reads.alibaba.com/7-factors-that-impact-wind-turbine-efficiency/)[8](https://energy-elege.com/wind-turbine-power-generation-efficiency/).
    
- Includes wake effects, gearbox losses, and downtime[1](https://www.omnicalculator.com/ecology/wind-turbine)[4](https://pmc.ncbi.nlm.nih.gov/articles/PMC6686152/).
    

## Secondary Factors

- **Altitude/Hub Height**: Higher elevations reduce air density but increase wind speed due to reduced ground friction[3](https://reads.alibaba.com/7-factors-that-impact-wind-turbine-efficiency/)[5](https://www.landgate.com/news/how-weather-affects-wind-turbines-in-the-united-states).
    
- **Temperature**: Affects air density and component thermal expansion[3](https://reads.alibaba.com/7-factors-that-impact-wind-turbine-efficiency/)[5](https://www.landgate.com/news/how-weather-affects-wind-turbines-in-the-united-states).
    
- **Control Systems**: Pitch/yaw adjustments optimize blade angle for varying wind conditions[3](https://reads.alibaba.com/7-factors-that-impact-wind-turbine-efficiency/)[8](https://energy-elege.com/wind-turbine-power-generation-efficiency/).
    
- **Turbine Spacing**: Closely spaced turbines reduce efficiency due to wake effects[4](https://pmc.ncbi.nlm.nih.gov/articles/PMC6686152/)[7](https://energyeducation.ca/encyclopedia/Wind_power).
    

## Example Calculation

For a turbine with:

- Rotor radius = 50 m
    
- Wind speed = 12 m/s
    
- Cp = 35%
    
- ρ = 1.225 kg/m³
    

Power = 0.5 × 1.225 × π × 50² × 0.35 × 12³ ≈ **2.3 MW**[1](https://www.omnicalculator.com/ecology/wind-turbine)[6](https://x-engineer.org/wind-turbine-energy/)[7](https://energyeducation.ca/encyclopedia/Wind_power).

This equation and dependencies enable accurate modeling of wind energy potential for site selection and turbine design[1](https://www.omnicalculator.com/ecology/wind-turbine)[3](https://reads.alibaba.com/7-factors-that-impact-wind-turbine-efficiency/)[7](https://energyeducation.ca/encyclopedia/Wind_power).

Share

Export

Rewrite








-----
now

## **3. Degradation Factors:**

- `(1 - solarDeg)^($B$7 - 1)`
    
- `(1 - windDeg)^($B$7 - 1)`
    

**Purpose:** Models the reduction in system performance due to **degradation** over time:

- `solarDeg` = solar degradation rate per year (e.g., 0.005 for 0.5%).
    
- `windDeg` = wind degradation rate per year.
    
- `$B$7` = the number of years.
    
- `($B$7 - 1)` ensures that **degradation is applied starting from year 2 onward**.


## **4. Hybrid Case Calculation:**

For `genType="Hybrid"`:
- Combines **both Solar and Wind** contributions.
    
- `solarCap` and `windCap`: The installed capacity (probably MW) for Solar and Wind.
    
- `totalRECap`: The total renewable energy capacity (solarCap + windCap).
    
- Formula **adds the weighted solar and wind outputs**, adjusted for degradation, and **normalizes** by total capacity.
## **Summary of Logic:**

|genType|Calculation Logic|
|---|---|
|Solar|Lookup solar data → adjust for degradation.|
|Wind|Lookup wind data → adjust for degradation.|
|Hybrid|Weighted sum of solar and wind (with their respective degradation), divided by total capacity.|
