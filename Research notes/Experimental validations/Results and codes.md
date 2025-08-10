

## Annotations
To do
---

add lines and and directions

### For electricity vrs production capacity
Baseline effective
- market prices line for different colours of hydrogen.

### SEC efficiency vrs electricity 
Limitations and effects on SEC
- DOE targets params, 
- boundaries of practicalities for efficiency
practical PEM electrolyzer systems achieve efficiencies in the range of 70-80%. While advancements in materials and design are continuously improving these efficiencies, the theoretical efficiency limit, which is calculated based on the thermodynamic minimum energy required for water splitting, cannot be fully reached due to these inherent losses.

- **State-of-the-art PEM stacks** (2 A/cm², 80 °C, 20 bar) achieve ~65–75 % LHV efficiency.
- **System-level efficiencies** (including balance-of-plant) typically fall in the 50–65 % range.

- Overpotentials: (Activation, ohmic , concentration overpotential )
	Ecell​=E0​+ηa​+ηi​+ηm​

**Hydrogen compression or purification** (up to 10–15 % of energy)
### 3. Operating Conditions
- **Current density**: Pushing to 2–3 A/cm² can raise cell voltage to 1.8–2.0 V, cutting LHV efficiency to 60–70 %.
- **Temperature**: Raising T to ≈80 °C lowers activation and ohmic losses, but membrane stability caps PEM at ≲90 °C.
- **Pressure**: Producing H₂ at high pressure (20–30 bar) adds 0.05–0.15 V extra, reducing cell efficiency by a few percent.



Energy configr.nd capacity factor

Unify colors for plots
Correct tornado basis for tax
subscirpts for H2 andn O2


## Install packages in sandbox
```python
import micropip 
await micropip.install(['numpy','matplotlib'])
import numpy as np 
import matplotlib.pyplot as plt

```


## Contour plots





```python
import matplotlib.pyplot as plt
import numpy as np
import matplotlib.colors as mcolors

# Set the font family to Arial
plt.rcParams['font.family'] = 'Arial'

feature_x = [9.65, 19.3, 38.6, 57.9, 77.2]
feature_y = [1.21, 1.38, 1.75, 2.04, 2.15, 2.54, 2.89]

# Creating 2-D grid of features
[X, Y] = np.meshgrid(feature_x, feature_y)

fig, ax = plt.subplots(1, 1)

z = [3.22, 2.84, 2.59, 2.51, 2.45,
     3.69, 3.30, 3.06, 2.98, 2.91,
     4.70, 4.31, 4.06, 3.98, 3.92,
     5.49, 5.10, 4.85, 4.77, 4.71,
     5.79, 5.40, 5.15, 5.07, 5.01,
     6.85, 6.46, 6.22, 6.14, 6.07,
     7.80, 7.42, 7.17, 7.09, 7.02]

Z = np.array(z).reshape(len(feature_y), len(feature_x))

# Define custom colors
lower_color = (0, 128/255, 128/255)
upper_color = (144/255, 238/255, 144/255)

# Create a colormap that smoothly transitions between the colors
cmap = mcolors.LinearSegmentedColormap.from_list('custom_colormap', [lower_color, upper_color])

# Customize colors using the custom colormap
contour_plot = ax.contourf(X, Y, Z, cmap='magma')

ax.set_title('')
ax.set_xlabel('SAF Production Capacity (MM Gal/year)', fontsize="12", fontname="Arial")
ax.set_ylabel('Ethanol Price ($/gal)', fontsize="12", fontname="Arial")

# Add contour with market price (MSFP)
cp2 = plt.contour(X, Y, Z, levels=[6.69], colors='black', linestyles='dashed')
fmt = {}
strs = ['      Market Price:  $6.69/Gal      ']
for l, s in zip(cp2.levels, strs):
    fmt[l] = s
ax.clabel(cp2, inline=True, fmt=fmt)

# Add a colorbar
cbar = fig.colorbar(contour_plot)
cbar.set_label('Minimum SAF Selling Price ($/gal)', fontsize="12", fontname="Arial")

# Save the plot as an image file (e.g., PNG)
plt.savefig('Figure Qual.jpeg', dpi=700, bbox_inches='tight')

plt.show()

# Define the directory and filename
directory = 'This PC/Downloads'  # Replace with the path you want to use
filename = 'my_plot.png'

import os

# Ensure the directory exists
if not os.path.exists(directory):
    os.makedirs(directory)
```

Anotations

```python

# Add contour with market price (MSFP)
cp2 = plt.contour(X, Y, Z, levels=[6.69], colors='black', linestyles='dashed')
fmt = {}
strs = ['      Market Price:  $6.69/Gal      ']
for l, s in zip(cp2.levels, strs):
    fmt[l] = s
ax.clabel(cp2, inline=True, fmt=fmt)

```

![[farhards annotation.png]]

```python

# Add a baseline annotation with a dot
plt.scatter(10000, 0.0733, color='white', zorder=5)  # Dot at the specified location
plt.text(10500, 0.079, 'Baseline', fontsize=12, color='white', ha='right')


```


### Electricity cost vrs Scalling



# Design Capacity vrs Electricity tariff

```python
import micropip
await micropip.install(['numpy','matplotlib'])
import numpy as np
import matplotlib.pyplot as plt

# Set the font family to Arial
plt.rcParams['font.family'] = 'Arial'

# Design capacities and electricity prices
design_capacities = np.array([1500, 3000, 4500, 6000, 7500, 9000, 10500, 12000, 13500, 15000]) # kg H₂/day
electricity_prices = np.array([0.01, 0.03, 0.05, 0.07, 0.09, 0.11, 0.13, 0.15, 0.17, 0.19, 0.21]) # $/kWh

# Data values from the table
cost_data = np.array(
    [
        [8.429, 5.690, 4.677, 4.157, 3.922, 3.771, 3.711, 3.660, 3.631, 3.631],
        [9.485, 6.746, 5.734, 5.214, 4.978, 4.828, 4.767, 4.717, 4.687, 4.688],
        [10.542, 7.803, 6.790, 6.270, 6.035, 5.884, 5.824, 5.773, 5.744, 5.744],
        [11.598, 8.859, 7.846, 7.327, 7.091, 6.941, 6.880, 6.830, 6.800, 6.801],
        [12.655, 9.916, 8.903, 8.383, 8.148, 7.997, 7.937, 7.886, 7.857, 7.857],
        [13.711, 10.972, 9.959, 9.440, 9.204, 9.054, 8.993, 8.942, 8.913, 8.914],
        [14.767, 12.029, 11.016, 10.496, 10.261, 10.110, 10.050, 9.999, 9.970, 9.970],
        [15.824, 13.085, 12.072, 11.553, 11.317, 11.167, 11.106, 11.055, 11.026, 11.027],
        [16.880, 14.141, 13.129, 12.609, 12.374, 12.223, 12.163, 12.112, 12.083, 12.083],
        [17.937, 15.198, 14.185, 13.666, 13.430, 13.279, 13.219, 13.168, 13.139, 13.139],
        [18.993, 16.254, 15.242, 14.722, 14.487, 14.336, 14.276, 14.225, 14.196, 14.196]
    ]
)

# Create the contour plot
X, Y = np.meshgrid(design_capacities, electricity_prices)
plt.figure(figsize=(10, 6))
contour = plt.contourf(X, Y, cost_data, cmap='viridis')
plt.colorbar(contour).set_label('LCOH, $/kg H2')  # Adding label to the colorbar


# Add contour with market price (MSFP)
cp2 = plt.contour(X, Y, Z, levels=[7.05], colors='black', linestyles='dashed')
fmt = {}
strs = ['      Baseline Price:  $7.05/Gal      ']
for l, s in zip(cp2.levels, strs):
    fmt[l] = s
ax.clabel(cp2, inline=True, fmt=fmt)


# Add a baseline annotation with a dot
plt.scatter(10000, 0.0733, color='white', zorder=5)  # Dot at the specified location
plt.text(10500, 0.079, 'Baseline', fontsize=12, color='white', ha='right')

plt.xlabel('Design Capacity,(kg H₂/day)', fontsize="12")
plt.ylabel('Cost of Energy ($/kWh)', fontsize="12")
plt.title('LCOH based on design capacity and Cost of Energy', fontsize="12", pad=20)
plt.show()
```


```python

import numpy as np
import matplotlib.pyplot as plt

# Use Arial throughout
plt.rcParams['font.family'] = 'Arial'

# Design capacities and electricity prices
design_capacities = np.array([1500, 3000, 4500, 6000, 7500, 9000, 10500, 12000, 13500, 15000])  # kg H₂/day
electricity_prices = np.array([0.01, 0.03, 0.05, 0.07, 0.09, 0.11, 0.13, 0.15, 0.17, 0.19, 0.21])  # $/kWh

# LCOH data (rows = electricity prices, cols = capacities)
cost_data = np.array([
    [8.429, 5.690, 4.677, 4.157, 3.922, 3.771, 3.711, 3.660, 3.631, 3.631],
    [9.485, 6.746, 5.734, 5.214, 4.978, 4.828, 4.767, 4.717, 4.687, 4.688],
    [10.542,7.803, 6.790, 6.270, 6.035, 5.884, 5.824, 5.773, 5.744, 5.744],
    [11.598,8.859, 7.846, 7.327, 7.091, 6.941, 6.880, 6.830, 6.800, 6.801],
    [12.655,9.916, 8.903, 8.383, 8.148, 7.997, 7.937, 7.886, 7.857, 7.857],
    [13.711,10.972,9.959, 9.440, 9.204, 9.054, 8.993, 8.942, 8.913, 8.914],
    [14.767,12.029,11.016,10.496,10.261,10.110,10.050, 9.999, 9.970, 9.970],
    [15.824,13.085,12.072,11.553,11.317,11.167,11.106,11.055,11.026,11.027],
    [16.880,14.141,13.129,12.609,12.374,12.223,12.163,12.112,12.083,12.083],
    [17.937,15.198,14.185,13.666,13.430,13.279,13.219,13.168,13.139,13.139],
    [18.993,16.254,15.242,14.722,14.487,14.336,14.276,14.225,14.196,14.196]
])

# Meshgrid for plotting
X, Y = np.meshgrid(design_capacities, electricity_prices)

# Switch to OO API so we can keep hold of the Axes
fig, ax = plt.subplots(figsize=(10, 6))

# Filled contour of LCOH surface
contour = ax.contourf(X, Y, cost_data, cmap='viridis')
cbar = fig.colorbar(contour, ax=ax)
cbar.set_label('LCOH, $/kg H₂')

# Dash‑style contour at your market/baseline price of 7.05
cs = ax.contour(X, Y, cost_data, levels=[7.05], colors='black', linestyles='dashed')
ax.clabel(cs, fmt={7.05: 'Baseline Price: $7.05/kg'}, inline=True)

# Baseline dot + annotation
# (Adjust these coords if your “baseline” design capacity and electricity cost differ)
ax.scatter(10000, 0.0733, color='white', zorder=5)
ax.text(10500, 0.079, 'Baseline', color='white', ha='right', va='bottom')

# Labels & title
ax.set_xlabel('Design Capacity (kg H₂/day)')
ax.set_ylabel('Cost of Energy ($/kWh)')
ax.set_title('LCOH based on Design Capacity and Cost of Energy')

plt.show()

```


Diminishing effect


## SEC vrs electricity tarrif


```python

import numpy as np
import matplotlib.pyplot as plt

# Set the font family to Calibri
plt.rcParams['font.family'] = 'Arial'

# Electrical usage and electricity prices
electrical_usage = np.array([40, 45, 50, 55, 60, 65, 70])  # kWh/kg H2
electricity_prices = np.array([0.01, 0.02, 0.04, 0.06, 0.08, 0.10, 0.12, 0.14, 0.16, 0.18, 0.20])

# LCOH data from the table
lcoh_data = np.array([
    [3.280, 3.571, 3.862, 4.153, 4.444, 4.736, 5.027],
    [3.730, 4.071, 4.412, 4.754, 5.095, 5.436, 5.777],
    [4.631, 5.072, 5.513, 5.954, 6.396, 6.837, 7.278],
    [5.532, 6.073, 6.614, 7.155, 7.696, 8.238, 8.779],
    [6.432, 7.074, 7.715, 8.356, 8.997, 9.638, 10.280],
    [7.333, 8.074, 8.816, 9.557, 10.298, 11.039, 11.780],
    [8.234, 9.075, 9.917, 10.758, 11.599, 12.440, 13.281],
    [9.135, 10.076, 11.017, 11.959, 12.900, 13.841, 14.782],
    [10.036, 11.077, 12.118, 13.159, 14.201, 15.242, 16.283],
    [10.937, 12.078, 13.219, 14.360, 15.501, 16.643, 17.784],
    [11.837, 13.079, 14.320, 15.561, 16.802, 18.043, 19.285]
])

# Create the contour plot
X, Y = np.meshgrid(electrical_usage, electricity_prices)
plt.figure(figsize=(10, 6))
contour = plt.contourf(X, Y, lcoh_data, cmap='viridis')

# Add grid lines
plt.grid(False)

# Add tick labels and rotate them for better readability
plt.xticks(rotation=45)
plt.yticks(rotation=45)

# Add a color bar
cbar = plt.colorbar(contour)
cbar.set_label('LCOH, $/kg H2', fontsize="12")

# Add title and axis labels
plt.title('LCOH based on Specific Energy Consumptionn and Cost of energy', fontsize="12", pad=20)
plt.xlabel('SEC, efficiency (kWh/kg H2)', fontsize="12")
plt.ylabel('Cost of energy ($/kWh)', fontsize="12")

# Add a baseline annotation with a dot
baseline_x = 49.86
baseline_y = 0.0733
plt.scatter(baseline_x, baseline_y, color='white', zorder=5)  # Dot at the specified location
plt.text(51.5, 0.09, 'Baseline', fontsize=12, color='white', ha='right')

# Dash‑style contour at your market/baseline price of 7.05
plt.contour(X, Y, cost_data, levels=[4.5], colors='black', linestyles='dashed')
plt.clabel(cs, fmt={7.05: 'Blue hydrogen: $4.5/kg'}, inline=True)

# Show the plot
plt.show()

```

With annotations

```python
# Hydrogen color price ranges (USD/kg)
hydrogen_ranges = {
    'Brown':     (1.00, 2.20),
    'Grey':      (1.00, 2.50),
    'Blue':      (1.50, 4.50),
    'Turquoise': (2.30, 3.20),
    'Green':     (2.50, 7.00),
    'Pink':      (2.75, 7.37)
}
colors_map = {
    'Brown': 'saddlebrown',
    'Grey': 'grey',
    'Blue': 'blue',
    'Turquoise': 'turquoise',
    'Green': 'green',
    'Pink': 'magenta'
}


# Dash‑style contour at your market/baseline price of 7.05
cs = ax.contour(X, Y, cost_data, levels=[4.5], colors='black', linestyles='dashed')
ax.clabel(cs, fmt={7.05: 'Blue hydrogen: $4.5/kg'}, inline=True)

```


Anotation:
Different price of hydrogen

```python

import numpy as np
import matplotlib.pyplot as plt

# Use Arial
plt.rcParams['font.family'] = 'Arial'

# Electrical usage and electricity prices
electrical_usage = np.array([40, 45, 50, 55, 60, 65, 70])  # kWh/kg H2
electricity_prices = np.array([0.01, 0.02, 0.04, 0.06, 0.08, 0.10, 0.12, 0.14, 0.16, 0.18, 0.20])  # $/kWh

# LCOH data from the table (shape: 11 rows × 7 columns)
lcoh_data = np.array([
    [3.280, 3.571, 3.862, 4.153, 4.444, 4.736, 5.027],
    [3.730, 4.071, 4.412, 4.754, 5.095, 5.436, 5.777],
    [4.631, 5.072, 5.513, 5.954, 6.396, 6.837, 7.278],
    [5.532, 6.073, 6.614, 7.155, 7.696, 8.238, 8.779],
    [6.432, 7.074, 7.715, 8.356, 8.997, 9.638, 10.280],
    [7.333, 8.074, 8.816, 9.557, 10.298, 11.039, 11.780],
    [8.234, 9.075, 9.917, 10.758, 11.599, 12.440, 13.281],
    [9.135, 10.076, 11.017, 11.959, 12.900, 13.841, 14.782],
    [10.036, 11.077, 12.118, 13.159, 14.201, 15.242, 16.283],
    [10.937, 12.078, 13.219, 14.360, 15.501, 16.643, 17.784],
    [11.837, 13.079, 14.320, 15.561, 16.802, 18.043, 19.285]
])

# Create meshgrid for contour
X, Y = np.meshgrid(electrical_usage, electricity_prices)

# Plot contour
plt.figure(figsize=(10, 6))
contour = plt.contourf(X, Y, lcoh_data, cmap='viridis')

# Contour of different hydrogen colours
# Contour line for $4.5/kg
cs = plt.contour(X, Y, lcoh_data, levels=[4.5], colors='black', linestyles='dashed')
plt.clabel(cs, fmt={4.5: 'Blue Hydrogen: $4.5/kg'}, inline=True)

cs = plt.contour(X, Y, lcoh_data, levels=[11.5], colors='black', linestyles='dashed')
plt.clabel(cs, fmt={11.5: 'Green Hydrogen: $11.5/kg'}, inline=True)

cs = plt.contour(X, Y, lcoh_data, levels=[2.50], colors='black', linestyles='dashed')
plt.clabel(cs, fmt={2.50: 'Gray Hydrogen: $2.50/kg'}, inline=True)

# Color bar
cbar = plt.colorbar(contour)
cbar.set_label('LCOH, $/kg H₂', fontsize=12)

# Add a baseline annotation with a dot
baseline_x = 49.86
baseline_y = 0.0733
plt.scatter(baseline_x, baseline_y, color='white', zorder=5)
plt.text(51.5, 0.09, 'Baseline', fontsize=12, color='white', ha='right')

# Axis labels and title
plt.xlabel('SEC (kWh/kg H₂)', fontsize=12)
plt.ylabel('Electricity Price ($/kWh)', fontsize=12)
plt.title('LCOH Based on SEC and Electricity Cost', fontsize=12, pad=20)

# Ticks and layout
plt.xticks(rotation=45)
plt.yticks(rotation=45)
plt.grid(False)
plt.tight_layout()
plt.show()


```

To be compete with blue hydrogen, PPA should focus on tariff below 25cent/kwhe at same sec.


# System capacity factor vrs  Capital cost


```python
import numpy as np
import matplotlib.pyplot as plt

# Set the font family to Arial
plt.rcParams['font.family'] = 'Arial'

# Capacity factors and cost data
capacity_factors = np.array([0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0])
capital_costs = np.array([1, 200, 400, 600, 800, 1000, 1200])

# LCOH data from the table
lcoh_data = np.array([
    [8.147578038, 7.310499297, 6.808252052, 6.473420556, 6.234255201, 6.054881185, 5.915368061, 5.803757563],
    [9.487269545, 8.315267927, 7.612066956, 7.143266309, 6.808408704, 6.5572655, 6.361931897, 6.205665015],
    [10.83369317, 9.325085646, 8.419921131, 7.816478122, 7.3854474, 7.062174359, 6.810739772, 6.609592102],
    [12.1801168, 10.33490336, 9.227775307, 8.489689934, 7.962486097, 7.567083219, 7.259547647, 7.01351919],
    [13.52654042, 11.34472108, 10.03562948, 9.162901747, 8.539524793, 8.071992078, 7.708355522, 7.417446277],
    [14.87296405, 12.3545388, 10.84348366, 9.836113559, 9.11656349, 8.576900938, 8.157163397, 7.821373365],
    [16.21938767, 13.36435652, 11.65133783, 10.50932537, 9.693602186, 9.081809797, 8.605971272, 8.225300452]
])

# Create the contour plot
X, Y = np.meshgrid(capacity_factors, capital_costs)
plt.figure(figsize=(10, 6))
contour = plt.contourf(X, Y, lcoh_data, cmap='plasma')
cbar = plt.colorbar(contour)
cbar.set_label('LCOH, $/kg H2')

# Add a baseline annotation with a dot
plt.scatter(0.9, 800, color='white', zorder=5)  # Dot at the specified location
plt.text(0.93, 830, 'Baseline', fontsize=12, color='white', ha='right')

# Contour of different hydrogen colours
# Contour line for $4.5/kg
cs = plt.contour(X, Y, lcoh_data, levels=[4.5], colors='black', linestyles='dashed')
plt.clabel(cs, fmt={4.5: 'Blue Hydrogen: $4.5/kg'}, inline=True)

cs = plt.contour(X, Y, lcoh_data, levels=[11.5], colors='black', linestyles='dashed')
plt.clabel(cs, fmt={11.5: 'Green Hydrogen: $11.5/kg'}, inline=True)

cs = plt.contour(X, Y, lcoh_data, levels=[2.50], colors='black', linestyles='dashed')
plt.clabel(cs, fmt={2.50: 'Gray Hydrogen: $2.50/kg'}, inline=True)


plt.xlabel('Capacity factor', fontsize="12",)
plt.ylabel('Capital cost ($/kW)', fontsize="12",)
plt.title('LCOH based on capacity factor and capital cost', pad=20 )
plt.show()
```



```python
import numpy as np
import matplotlib.pyplot as plt

# Set a clean, available font
plt.rcParams['font.family'] = 'DejaVu Sans'

# ── First dataset: SEC vs Electricity Price ────────────────────────────────────
electrical_usage = np.array([40, 45, 50, 55, 60, 65, 70])            # kWh/kg H₂
electricity_prices = np.array([0.01, 0.02, 0.04, 0.06, 0.08,
                               0.10, 0.12, 0.14, 0.16, 0.18, 0.20])  # $/kWh
lcoh_sec_price = np.array([
    [3.280, 3.571, 3.862, 4.153, 4.444, 4.736, 5.027],
    [3.730, 4.071, 4.412, 4.754, 5.095, 5.436, 5.777],
    [4.631, 5.072, 5.513, 5.954, 6.396, 6.837, 7.278],
    [5.532, 6.073, 6.614, 7.155, 7.696, 8.238, 8.779],
    [6.432, 7.074, 7.715, 8.356, 8.997, 9.638, 10.280],
    [7.333, 8.074, 8.816, 9.557, 10.298, 11.039, 11.780],
    [8.234, 9.075, 9.917, 10.758, 11.599, 12.440, 13.281],
    [9.135, 10.076, 11.017, 11.959, 12.900, 13.841, 14.782],
    [10.036, 11.077, 12.118, 13.159, 14.201, 15.242, 16.283],
    [10.937, 12.078, 13.219, 14.360, 15.501, 16.643, 17.784],
    [11.837, 13.079, 14.320, 15.561, 16.802, 18.043, 19.285]
])
X1, Y1 = np.meshgrid(electrical_usage, electricity_prices)

# ── Second dataset: Capacity Factor vs Capital Cost ────────────────────────────
capacity_factors = np.array([0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0])
capital_costs   = np.array([1, 200, 400, 600, 800, 1000, 1200])            # $/kW
lcoh_cf_cc = np.array([
    [8.1476, 7.3105, 6.8083, 6.4734, 6.2343, 6.0549, 5.9154, 5.8038],
    [9.4873, 8.3153, 7.6121, 7.1433, 6.8084, 6.5573, 6.3619, 6.2057],
    [10.8337,9.3251, 8.4199, 7.8165, 7.3854, 7.0622, 6.8107, 6.6096],
    [12.1801,10.3349,9.2278, 8.4897, 7.9625, 7.5671, 7.2595, 7.0135],
    [13.5265,11.3447,10.0356,9.1629, 8.5395, 8.0720, 7.7084, 7.4174],
    [14.8730,12.3545,10.8435,9.8361, 9.1166, 8.5769, 8.1572, 7.8214],
    [16.2194,13.3644,11.6513,10.5093,9.6936, 9.0818, 8.6060, 8.2253]
])
X2, Y2 = np.meshgrid(capacity_factors, capital_costs)

# ── Create figure with two subplots ───────────────────────────────────────────
fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(14, 6))

# a) First contour plot
cs1 = ax1.contourf(X1, Y1, lcoh_sec_price)
for level, label in [(4.5, 'Blue H₂: $4.5/kg'),
                     (11.5,'Green H₂: $11.5/kg'),
                     (7.05, 'Baseline: $7.05/kg')]:
    c = ax1.contour(X1, Y1, lcoh_sec_price,
                    levels=[level],
                    colors='black',
                    linestyles='dashed')
    ax1.clabel(c, fmt={level: label}, inline=True)
ax1.set_xlabel('SEC (kWh/kg H₂)')
ax1.set_ylabel('Electricity Price ($/kWh)')
ax1.set_title('LCOH vs SEC & Electricity Cost')
fig.colorbar(cs1, ax=ax1, label='LCOH ($/kg H₂)')
# Add subplot label
ax1.text(-0.1, 1.05, '(a)', transform=ax1.transAxes,
         fontsize=14, fontweight='bold')

# b) Second contour plot
cs2 = ax2.contourf(X2, Y2, lcoh_cf_cc, cmap='plasma')
for level, label in [(4.5, 'Blue H₂: $4.5/kg'),
                     (11.5,'Green H₂: $11.5/kg'),
                     (7.05, 'Baseline: $7.05/kg')]:
    c = ax2.contour(X2, Y2, lcoh_cf_cc,
                    levels=[level],
                    colors='black',
                    linestyles='dashed')
    ax2.clabel(c, fmt={level: label}, inline=True)
ax2.set_xlabel('Capacity Factor')
ax2.set_ylabel('Capital Cost ($/kW)')
ax2.set_title('LCOH vs Capacity Factor & CapEx')
fig.colorbar(cs2, ax=ax2, label='LCOH ($/kg H₂)')
# Add subplot label
ax2.text(-0.1, 1.05, '(b)', transform=ax2.transAxes,
         fontsize=14, fontweight='bold')

plt.tight_layout()
plt.show()


```





anotation
 price line

----

# Design param contours

Results

#### Current densities (rows) and Temperatures (columns)



```python
import numpy as np
import matplotlib.pyplot as plt

# Current densities (rows) and Temperatures (columns)
current_densities = np.array([0.1, 1, 2, 3, 4, 5])
temperatures = np.array([40, 60, 80, 100])

# Measured values (rows: current density, columns: temperature)
lcoh = np.array([
    [6.441, 6.357, 6.275, 6.194],
    [6.885, 6.761, 6.654, 6.558],
    [7.231, 7.053, 6.909, 6.788],
    [7.560, 7.326, 7.145, 6.997],
    [7.889, 7.600, 7.380, 7.206],
    [8.236, 7.893, 7.637, 7.437]
])

# ── Meshgrid for contouring ───────────────────────────────────────────────
X, Y = np.meshgrid(temperatures, current_densities)

# ── Plot ───────────────────────────────────────────────────────────────────
fig, ax = plt.subplots(figsize=(6.7, 4.0))       # ≈ double-column width

cf = ax.contourf(
    X, Y, lcoh,
    levels=10,
    cmap='viridis'
)

cs = ax.contour(
    X, Y, lcoh,
    levels=10,
    colors='black',
    linewidths=0.5
)
ax.clabel(cs, fmt='%1.1f', fontsize=9)

# Colorbar
cbar = fig.colorbar(cf, ax=ax)
cbar.set_label('LCOH ($ per kg H₂)', fontsize=12)

# Labels / title
ax.set_xlabel('Temperatures (C)')
ax.set_ylabel('Current density (kWh kg⁻¹ H₂)')   # adjust wording/units as desired
ax.set_title('Levelized Cost of Hydrogen\n. Current density and Temperature')

plt.tight_layout()
plt.show()
```

Temperature dominate over current density. 
membrane and catalyst degradation risk beyond 90 celcis

### Current density and Membrane Thickness
```python
import numpy as np
import matplotlib.pyplot as plt

# Membrane thicknesses (columns)
membrane_thickness = np.array([1, 75, 150, 225, 300, 375, 450, 525])  # in microns

# Current densities (rows)
current_density = np.array([0.1, 1, 2, 3, 4, 5])  # in A/cm²

# LCOH data (in USD/kg)
lcoh = np.array([
    [6.336, 6.350, 6.364, 6.378, 6.392, 6.406, 6.420, 6.434],  # 0.1 A/cm²
    [6.550, 6.688, 6.828, 6.968, 7.109, 7.249, 7.390, 7.530],  # 1 A/cm²
    [6.630, 6.907, 7.188, 7.469, 7.750, 8.032, 8.312, 8.593],  # 2 A/cm²
    [6.692, 7.107, 7.529, 7.951, 8.372, 8.793, 9.213, 9.632],  # 3 A/cm²
    [6.753, 7.307, 7.870, 8.432, 8.993, 9.551, 10.108, 10.661],  # 4 A/cm²
    [6.834, 7.527, 8.230, 8.932, 9.630, 10.324, 11.014, 11.699]  # 5 A/cm²
])

# ── Meshgrid for contouring ───────────────────────────────────────────────
X, Y = np.meshgrid(membrane_thickness, current_density)

# ── Plot ───────────────────────────────────────────────────────────────────
fig, ax = plt.subplots(figsize=(6.7, 4.0))       # ≈ double-column width

cf = ax.contourf(
    X, Y, lcoh,
    levels=15,
    cmap='viridis'
)

cs = ax.contour(
    X, Y, lcoh,
    levels=15,
    colors='black',
    linewidths=0.5
)
ax.clabel(cs, fmt='%1.1f', fontsize=9)

# Colorbar
cbar = fig.colorbar(cf, ax=ax)
cbar.set_label('LCOH ($ per kg H₂)', fontsize=12)

# Labels / title
ax.set_xlabel('Membrane thickness (Microns)')
ax.set_ylabel('Current density (kWh kg⁻¹ H₂)')   # adjust wording/units as desired
ax.set_title('Levelized Cost of Hydrogen\n. Current density and Membrane thickness')

plt.tight_layout()
plt.show()
```

For low thickness application such as in fuel cells, current density should prioitsed over membrane thickness. Since it yields more cost savings


Into Subplots Subplots

```python

import numpy as np
import matplotlib.pyplot as plt

# -----------------------------
# Subplot 1: Temperature vs Current Density
# -----------------------------
# Current densities (rows) and Temperatures (columns)
current_densities = np.array([0.1, 1, 2, 3, 4, 5])
temperatures = np.array([40, 60, 80, 100])

# LCOH data (rows: current density, columns: temperature)
lcoh_temp = np.array([
    [6.441, 6.357, 6.275, 6.194],
    [6.885, 6.761, 6.654, 6.558],
    [7.231, 7.053, 6.909, 6.788],
    [7.560, 7.326, 7.145, 6.997],
    [7.889, 7.600, 7.380, 7.206],
    [8.236, 7.893, 7.637, 7.437]
])
X1, Y1 = np.meshgrid(temperatures, current_densities)

# -----------------------------
# Subplot 2: Membrane Thickness vs Current Density
# -----------------------------
membrane_thickness = np.array([1, 75, 150, 225, 300, 375, 450, 525])  # in microns
current_density = np.array([0.1, 1, 2, 3, 4, 5])  # in A/cm²

lcoh_mem = np.array([
    [6.336, 6.350, 6.364, 6.378, 6.392, 6.406, 6.420, 6.434],
    [6.550, 6.688, 6.828, 6.968, 7.109, 7.249, 7.390, 7.530],
    [6.630, 6.907, 7.188, 7.469, 7.750, 8.032, 8.312, 8.593],
    [6.692, 7.107, 7.529, 7.951, 8.372, 8.793, 9.213, 9.632],
    [6.753, 7.307, 7.870, 8.432, 8.993, 9.551, 10.108, 10.661],
    [6.834, 7.527, 8.230, 8.932, 9.630, 10.324, 11.014, 11.699]
])
X2, Y2 = np.meshgrid(membrane_thickness, current_density)

# -----------------------------
# Create Combined Plot
# -----------------------------
fig, axs = plt.subplots(1, 2, figsize=(13, 5), constrained_layout=True)

# Plot 1: Temperature
cf1 = axs[0].contourf(X1, Y1, lcoh_temp, levels=10, cmap='viridis')
cs1 = axs[0].contour(X1, Y1, lcoh_temp, levels=10, colors='black', linewidths=0.5)
axs[0].clabel(cs1, fmt='%1.1f', fontsize=9)
axs[0].set_xlabel('Temperature (°C)', fontsize=11)
axs[0].set_ylabel('Current Density (A/cm²)', fontsize=11)
axs[0].set_title('LCOH vs Temperature and Current Density', fontsize=12)
cbar1 = fig.colorbar(cf1, ax=axs[0])
cbar1.set_label('LCOH ($/kg H₂)', fontsize=11)

# Plot 2: Membrane Thickness
cf2 = axs[1].contourf(X2, Y2, lcoh_mem, levels=15, cmap='viridis')
cs2 = axs[1].contour(X2, Y2, lcoh_mem, levels=15, colors='black', linewidths=0.5)
axs[1].clabel(cs2, fmt='%1.1f', fontsize=9)
axs[1].set_xlabel('Membrane Thickness (µm)', fontsize=11)
axs[1].set_ylabel('Current Density (A/cm²)', fontsize=11)
axs[1].set_title('LCOH vs Membrane Thickness and Current Density', fontsize=12)
cbar2 = fig.colorbar(cf2, ax=axs[1])
cbar2.set_label('LCOH ($/kg H₂)', fontsize=11)

plt.suptitle('Levelized Cost of Hydrogen – Sensitivity to Design Parameters', fontsize=14, fontweight='bold')
plt.show()

```


# For energy system


Electricty price and Operating power %

```python
import numpy as np
import matplotlib.pyplot as plt

# Electricity prices (rows)
electricity_price = np.array([0.001, 0.03, 0.06, 0.09, 0.12, 0.15])  # in USD/kWh

# Operating power percentages (columns)
operating_power = np.array([5, 10, 15, 30, 60, 90, 100])  # in %

# LCOH values (USD/kg)
lcoh = np.array([
    [12.652, 6.546, 5.08, 4.574, 4.335, 4.324, 3.794],   # $0.001/kWh
    [18.342, 9.490, 7.36, 5.819, 5.515, 5.501, 5.501],   # $0.03/kWh
    [24.228, 12.536, 9.72, 7.686, 7.284, 7.266, 7.266],  # $0.06/kWh
    [30.113, 15.581, 12.08, 9.553, 9.054, 9.032, 9.031],  # $0.09/kWh
    [35.999, 18.627, 14.44, 11.420, 10.824, 10.797, 10.796],  # $0.12/kWh
    [41.885, 21.672, 16.80, 13.287, 12.593, 12.562, 12.561]   # $0.15/kWh
])

# ── Meshgrid for contouring ───────────────────────────────────────────────
X, Y = np.meshgrid(operating_power, electricity_price)

# ── Plot ───────────────────────────────────────────────────────────────────
fig, ax = plt.subplots(figsize=(6.7, 4.0))       # ≈ double-column width

cf = ax.contourf(
    X, Y, lcoh,
    levels=20,
    cmap='viridis'
)

cs = ax.contour(
    X, Y, lcoh,
    levels=20,
    colors='black',
    linewidths=0.5
)
#ax.clabel(cs, fmt='%2.1f', fontsize=9)

# Colorbar
cbar = fig.colorbar(cf, ax=ax)
cbar.set_label('LCOH ($ / kg H₂)', fontsize=12)

# Labels / title
ax.set_xlabel('operating_power,%')
ax.set_ylabel('electricity_price ($/kWh)')   # adjust wording/units as desired
ax.set_title('Levelized Cost of Hydrogen\n. electricity_price  and operating_power,%')

plt.tight_layout()
plt.show()
```


