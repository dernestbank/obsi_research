


![[Rafael Nogueira Nakashima - Multi-objective optimization of hydrogen and electricity cogeneration using s SOFCs and biogas [j2LEng9MhmM - 983x553 - 0m14s] 1.png]]

https://www.youtube.com/watch?v=j2LEng9MhmM&list=PLmxfuTb_nF4sxFjOM353YA8IkKtrojSpl&index=3


![[Rafael Nogueira Nakashima 0m14s 1.png]]

![[Rafael Nogueira  0m34s.png]]

![[Rafael Nogueira  1m30s.png]]
Obj: To optimize the production of hydrogen from pem electrolyser using RE

![[Rafael Nogueira 1m57s.png]]

The base secnario
![[Rafael Nogueira  2m31s.png]]

Overview:
Variables
Variables chosen by Parametric analysis from previous studies
![[Rafael Nogueira.png]]

The **NSGA-II multi-objective optimization algorithm** was used to maximize **net present value (NPV) and exergy efficiency**.

![[Rafael Nogueira .png]]

The model was design using python.
QUASI-2d MODEL

![[Rafael Nogueira  (2).png]]
**Key Findings – Hydrogen vs. Power-Only Generation (05:17 - 06:16)**

- **Cogeneration of hydrogen and power improves net present value by at least 2.4 times compared to power-only systems.**
- **Exergy efficiency in cogeneration is 5-17% higher than power-only generation.**
- Hydrogen production benefits from its higher efficiency at low fuel use ratios, reducing energy losses.
![[Rafael Nogueira 6m11s.png]]

Understanding the influence of decisign variables of the system.
Current density: effect on NPV EFF. 
increase in current density decrease in stack size, and consequently it's cost.
but it also reduces the efficiency of power conversion.
 Thus a low current density would favor higher efficiencies, while a high current density may benefitt revenues.
 **Impact of Design Variables (06:16 - 07:38)**

- Higher **current density** reduces fuel cell size and cost but lowers power conversion efficiency.
 - **Fuel use ratio** is higher in power-only generation but lower in hydrogen production to allow for hydrogen recovery.
- **Temperature and air ratio** affect methane reforming, which influences hydrogen availability.


![[Rafael Nogueira 7m50s].png]]

**Capital Investment & Cost Trade-offs (08:11 - 09:03)**

- Hydrogen cogeneration **reduces fuel cell size and cost by 45%**, balancing out additional equipment costs.
- **Heat exchanger network costs are higher** for hydrogen production due to lower available high-temperature heat.
![[Rafael Nogueira 8m56s.png]]

**Overall Conclusion & Implications (09:03 - 10:21)**

- **Hydrogen and electricity cogeneration improves NPV by 140-170% and exergy efficiency by 5-17%, with only a 5% increase in investment costs.**
- **Fuel cells suffer efficiency losses at high fuel use ratios**, making hydrogen enrichment and separation viable for efficiency gains (62-65%).
- The investment cost remains similar to power-only systems due to fuel cell size reduction.
![[Rafael Nogueira 9m38s.png]]


----

![[image-7.png]]


![[image-8.png]]

![[image-9.png]]



-----

Farhads,

4.1.2- Task 1.2: Estimating the capital investments and operational costs, and performing TEA
analysis {completed}
![[image-14.png]]

![[image-13.png|377x343]]


![[image-15.png|522x362]]


4.2.1- Task 2.1: Integrating reaction kinetic models in process simulations {completed}

![[image-16.png|339x301]]

![[Presentaions/attachments/image-12.png|662x274]]



![[image-11.png|488x300]]


![[image-17.png|366x332]]



4.3- Aim 3: Investigating the impact of plant location, feedstock/product logistics, recycling
technology, and process configurations on sustainability of advanced plastic waste
management methods

![[image-18.png]]





# Image Diagram instructions standard.

###  **Font**

- **Font Family**:
    - Use **sans-serif** fonts like:
        - **Arial** 
        
- **Font Size**:
    - **Axis Labels**: 12 pt
    - **Tick Labels**: 10 pt
    - **Legend/Annotations**: 10 pt
    - **Title/Subtitles** (if allowed): 14 pt
    - Font size must be **legible when the figure is scaled to 1-column (≈3.5”) or 2-column (≈7”) width**.


- **Image Dimensions**:
    - Common widths:
        - **Single column**: ~85 mm (3.35 in)
        - **Double column**: ~170 mm (6.7 in)
            
    - Height should not exceed ~230 mm (9 in)
    - Maintain a consistent aspect ratio.


### **🎨** **Colors and Line Styles**

- **Color Scheme**:
    - Use **colorblind-friendly palettes** (e.g., **Color Universal Design**, **Okabe-Ito**, or **viridis** in Python/Matplotlib)
    - Avoid red-green combinations unless clearly distinguishable
        
    
- my favourite colors:
	Light purple #9286e0
	Light Green  #91cfa3
	Light Yellow-Gold #f8d87f
	Light Orange : #f7965d
	Bright Red-Orange #f85c32


- **Line Styles**:
    - Use solid, dashed, dotted, or dash-dot lines consistently
    - Lines must be at least **0.5 pt thick**


### **📊** **Graph Elements**

- **Axes**:
    - Clearly labeled with units (e.g., “Time (s)” or “Concentration (mg/L)”)
    - Use scientific notation where necessary
        
- **Legends**:
    - Should not obscure data
    - Avoid unnecessary borders
    - Keep it simple and concise
        
- **Gridlines**:
    - no gridlines  