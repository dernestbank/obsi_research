

# LCA on membranes
1. Goal and scope
	- To quantify the environmental impacts of PEM electrolyser / membrane production
	- LCA standards: ISO 14040 and 14044
	- Functional unit: rating of electrolyser or amount of h2 produced/ kg H2
	- geographical scope
- 
2. System boundaries.
	- input, outputs, processes for each system
	- electricity, chemical, material flows
	- outputs: direct emissions
	- cradle-to gate: form material extraction to operation
- 
1. Life cycle Inventory
	- Inputs | Units |quantity | Baseline
	using the ecoinvent v3.8 and US Life Cycle Inventory databases

2. Impact assessment
		-method: eg ReCiPe midpoint(E) assessment method
	- impact categories: GWP, 

3. Uncertainty Analysis
	Monte carlo simulation
	``to determine uncertainty ranges in the impact category data based on changes in the LCI	Inventory values were varied by ±10% using uniform distributions for 1000 iterations in the simulation. The uncertainty range associated with each impact category is based on a 95% confidence interval, and the standard deviation of each distribution is reported with impact category data.``
		- feature importance - we assign an importance score to the model's input based on how much they can affect the model output.
		- global sensitivity analysis- how uncertainty in the model out can be apportioned to different sources of uncertainty in the model input
		- statistical methods
4. 
Result and interpretation


@ prospective LCA of alkalne and PEM electrolyser systems.

The FC-HyGuide [14,15] has interpreted and adapted the ISO standards specifically for hydrogen producing systems. They state that the recommended functional unit for electrolyser systems is one MWh of primary energy (/MWhP) used, one m2 of active surface area (/ma2ctive SA) or one kg of hydrogen produced (/kg H2) over the lifetime of the electrolyser system. We chose the functional unit of per/kg H2 produced as this also accounts for the efficiency of the electrolysers.

![[Pasted image 20250217053900.png]]


Stack specifications
Stack Size (MW) 
No of cells 
Active surface area (m2)
Power density (W/ cm2) 
Current density (A/ cm2) 
Pressure (bar) Ambient
Temperature at Nominal load (0C) 
Voltage (V) 
Lifetime (years) 
Specific energy (kWh/ kgH2)
Operating hours at full load (offshore wind) (h/y) 
Operating hours at full load (grid electricity) (h/y) 
Yearly H2 production (tons/year) 









Green scope
Ruiz-Mercado GJ, Gonzalez MA, and Smith RL (2014) "Expanding GREENSCOPE beyond the Gate: A Green Chemistry and Life Cycle Perspective," Clean Tech. Env. Policy, 16, 703-717. [http://link.springer.com/article/10.1007/s10098-012-0533-y](http://link.springer.com/article/10.1007/s10098-012-0533-y)

![[Pasted image 20250220054738.png]]




Notes from Papers

# Polymeric membrane production
Assessment of the environmental impact of polymeric membrane production.
Pooja Yadav
Goal: to assess the environmental impact of hollow fiber membrane preparation.
Functional unit: $100m^2$  

System boundary: (i) the preparation of the dope solution by mixing the polymer and the solvent,and (ii) the hollow fiber membrane spinning process (Fig. 4).

Keywords/phrases
Flat sheet and hollow fiber membranes
green solvent or biosolvents

Fossil and bio-based polymers.
polysulfones,
plyvinylidene flouride
cellulose acetate

solvent used for (dope solution)
polar aprotic solvents:( N-Methyl-2-pyrrolidone(NMP),  N, N-dimethylacetamide, dimethylformamide )
alternative green solvent:(ethylene carbonate,tributyl O-acetyl citrate [27], triethylene glycol diacetate (TEGDA) [28], Methyl-5-(dimethylamino)-2-methyl-5-oxopentanoate (RhodiasolvⓇ PolarClean) [29], Cyrene™ [30], and organic carbonates [31]. )

Impact categories
- Global warming
- Marine ecotoxicity
- human carcinogenic
- non-carcinogenic toxicity
- land use potential
- fossil resource scarcity

replacing fossil-based polymers with bio-based polymers or substituting toxic solvents with green alternatives
hotspot in membrane production process.


methods for polymeric membrane fabrication 
sintering, track-etching, stretching, and phase inversion), phase inversion is the most widely used in both industry and academia [22]

phase inversion(steps in preparing)
- prepare a homogeneous polymer solution by dissolving the polymer in a suitable solvent. 
- phase inversion s then induced using an external or internal factor
-  The majority of the used solvent is released during the phase inversion process in the coagu lation/quenching bath.
- Residual solvents are then extracted in the washing bath (known as external coagulation bath) due to their adverse impact on membrane performance.

 External factor methods include nonsolvent-induced precipitation, precipitation from the vapor phase and thermally-induced phase separation

N-metyl-2-pyrrolidone (NMP): the most popular solvent for membrane fabrication.

#fig Frequency of solvents that are commonly used

![[Pasted image 20250224045655.png |400]]

#fig  frequency of polymers
![[Pasted image 20250224050831.png|400]]

the upstream emission of green solvents

natural polymers:  cellulose-based polymers, fossil-based polymers

![[Pasted image 20250224053526.png|400]]


To read
Figoli et al. [32] reviewed the use of green solvents in membrane fabrication.




#idea
material composition and alternative
different configurations
current state of the art and furure alternatives



Critical and Strategic Raw Materials for Electrolysers, Fuel Cells, Metal Hydrides and Hydrogen Separation Technologies. _International Journal of Hydrogen Energy_ **2024**, _71_, 433–464. [https://doi.org/10.1016/j.ijhydene.2024.05.096](https://doi.org/10.1016/j.ijhydene.2024.05.096).

![[Pasted image 20250225132724.png|500]]
Materials selection of PEM electrolysers

Catalyst
Pt, and Pt-based materials , Pd-Pt the state of the art electrocatalyst on cathode side of PEM electrolysers.
platinum nanoparticles (i.e., platinum black powder) supported on a carbon-base (Pt/C).


PTL 
Ti, in the form of screen mesh or sintered powder.
TiN (titanium nitride), Pt, Au (gold), stainless steel materials may be an alternative current collector [73].
future possible candidates as OER substrates are antimony-doped tin oxide (ATO), niobium-doped titanium oxide (NTO), or tungsten doped titanium oxide (WTO) [74].


BIpolar plate
Titanium is the preferred material used for the bipolar plates [41, 75,76], but also nickel, stainless steel and aluminum are considered to be suitable materials [77,78].

2.6.2. Critical raw material supply dynamics

present annual global production volumes of the critical raw materials relevant for electrolysers and fuel cells,

![[Pasted image 20250225133519.png]]

![[Pasted image 20250225133619.png]]
more to milk out









let's make it a 3 objective:

1. efficiency. 2. cost 3. environmental impact

We''ll make the lifetime a constraint that affects the three objective functions

for the efficiency

let's start with making more physics accurate, start with these and improve it

$$

ηenergy = \frac{HHV_{H_2} \cdot r_{H_2}}{V_{\text{cell}} \cdot I_{\text{cell}}. N_{\text{cell}}}

$$

r_h2 - design capty in kg H2/hr

N_cell = design capacity/ H2 per cell produced

H2_cell produced= (i* A_cell* 3600* Mw_h2* Faradaic eff)/2*F

I= i/A

i- current density

vell s a function of Vcell = Voc +Vohm Vact+ Vcon

Vohm= Vohm_membrane + Vohm_catalyst(anode+cathode)

Vohm_membrane= tmem/ sigma(mem)* i

the design capacity into Kg of H2 rate of production

I 0 ann and iO ca are the exchange current densities at the anode and cathode

The limiting current density is assumed equal to 6 A/cm2 (Bessarabov & Millet, 2018).

(Rmem) resistanceof the membraneto the flowof protons

Represents the number of water molecules per sulfonic acid site in the membrane (SO3H)

ρ_el is the material resistivity of the electrode, σ_memis the membrane resistivity, t_el is the electrode thickness, and t_mem is the membrane thickness

cost function

cost of material + manufacturing

Environmental impact

The overall environmental impact is often calculated using the following general equation:

Impact Score=∑i(Qi×CFi)

Where:

Q_i is the quantity of substance i

CF_i is the characterization factor for a substance i for a given impact category

indicator score= (actual -worst)/ (best-worst) * 100%
Envronmental impact
The impacts of membrane production on global warming, marine ecotoxicity, human carcinogenic and non-carcinogenic toxicity, land use potential, and fossil resource scarcity

LCA wlll be connected to openlCA api so use input parameters to set t