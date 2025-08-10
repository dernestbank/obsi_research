


. In this revision, the capital cost objective is reduced to include only the cost of the membrane material and manufacturing, and the durability (lifetime) objective is now complemented by an explicit mechanical strength constraint that relates membrane thickness to stress under operating conditions.

---

## 1. Objective Functions

### 1.1 Energy Efficiency (Maximize)

We define energy efficiency as the ratio of the chemical energy of the produced hydrogen (using its higher heating value) to the electrical energy input:
$$
ηenergy = \frac{HHV_{H_2} \cdot r_{H_2}}{V_{\text{cell}} \cdot I_{\text{cell}}. N_{\text{cell}}}
$$
where

- $HHV_{H_2}$ is the higher heating value of hydrogen (J/mol or J/kg),
- $r_{H_2}$ is the hydrogen production rate (mol/s or kg/s),
- $V_{\text{cell}}$ is the cell voltage (V), and
- $I_{\text{cell}}$ is the cell current (A).

We then define the first objective function as

$\textbf{Maximize } f_1(x) = \eta_{\text{energy}}(x).$

### 1.2 Durability (Maximize)

We represent durability by the membrane lifetime L(x). Although lifetime is influenced by several degradation mechanisms, here we conceptually denote it as:

$\textbf{Maximize } f_2(x) = L(x).$

In subsequent sections we will tie durability to mechanical strength (via membrane thickness).

### 1.3 Cost (Minimize)

Rather than the total system cost, we now focus on the capital cost associated with the membrane itself, which consists of:

- **Material Cost:** The cost of the ionomer (or chosen membrane material) per unit area, which depends on the thickness.
- **Manufacturing Cost:** The cost to produce the membrane, which we assume is proportional to the area produced.

Thus, if:

- $c_{\text{ionomer}}$ is the cost per kilogram of membrane material,
- $\rho$ is the density of the membrane (kg/m³),
- t is the membrane thickness (m), and
- AA is the membrane area (m²),
- $c_{\text{manuf}}$ is the manufacturing cost per unit area (in $/m²),

then the membrane material cost per unit area is given by

 $C_{\text{material}} = c_{\text{ionomer}} \cdot \rho \cdot t$,

and the manufacturing cost is

 $C_{\text{manufacturing}} = c_{\text{manuf}}.$
i may used NREL's manufacturing model
.................

We define the capital cost function as

$f_3(x) = C_{\text{capital}}(x) = C_{\text{material}}(x) + C_{\text{manufacturing}}$,

or, explicitly per unit area,

$f_3(x) = c_{\text{ionomer}} \cdot \rho \cdot t + c_{\text{manuf}}.$

### 1.4 Environmental Impact (Minimize)

We quantify environmental impact via an environmental impact score per unit mass of membrane material. If:

- $c_E$ is the environmental impact factor (e.g., kg CO₂-eq per kg of material),

then for membrane mass per unit area  $m_{\text{membrane}} = \rho \cdot t$, we define

  $$f_4(x) = E_{\text{material}}(x) = c_E \cdot \rho \cdot t.$$

---

## 2. Decision Variables

Let the design vector be

 $x = \{ t, \; \text{IEC}, \; c_{\text{additive}}, \; j, \; \text{others} \},$

where:

- t is the membrane thickness (m),
- IEC is the ion exchange capacity (meq/g),
- $c_{\text{additive}}$ is the concentration of any additives,
- j is the operating current density (A/m²), and
- “others” can include catalyst loading, operating temperature, etc.

These variables affect efficiency, lifetime, cost, and environmental impact.

---

## 3. Constraints

### 3.1 Physical and Operational Constraints

- **Voltage Constraint:** $V_{\min} \leq V_{\text{cell}}(x) \leq V_{\max}$
- **Current Density Constraint:** $j_{\min} \leq j \leq j_{\max}$
- **Thickness Constraint for Manufacturability:** $t \geq t_{\min}$ (set by production capabilities)

### 3.2 Mechanical Durability Constraint

To ensure the membrane can withstand the pressure difference without excessive stress, we employ a simplified stress model. For a thin plate under a pressure difference $\Delta P$, a simplified stress estimate is:

$$
\sigma \approx k \frac{\Delta P \, r^2}{t^2},
$$

where

- $\sigma$ is the estimated stress,
- $r$ is a characteristic dimension (e.g., effective radius of the membrane area),
- $t$ is the membrane thickness, and
- $k$ is a geometric constant.

We require that this stress be below an allowable level defined by the tensile strength $\sigma_{\text{tensile}}$ divided by a safety factor (SF):

$$
\sigma \leq \frac{\sigma_{\text{tensile}}}{SF}.
$$

Substituting our stress estimate, we have:

$$
k \frac{\Delta P \, r^2}{t^2} \leq \frac{\sigma_{\text{tensile}}}{SF}.
$$

Rearrange to obtain a lower bound on thickness:

$$
t \geq r \sqrt{\frac{k\, \Delta P \ SF}{\sigma_{\text{tensile}}}}.
$$

This yields the mechanical durability constraint:

$$
t \geq t_{\text{min, mech}} = r \sqrt{\frac{k\, \Delta P \ SF}{\sigma_{\text{tensile}}}}.
$$

### 3.3 Economic and Environmental Constraints

- **Budget Constraint (if applicable):** $f_3(x) \leq C_{\text{budget}}$.
- **Environmental Impact Constraint:** $f_4(x) \leq E_{\text{max}}$, where $E_{\text{max}}$ is the maximum allowable environmental impact per unit area.

---

## 4. Overall Multiobjective Optimization Formulation

Combining the objectives and constraints, the optimization problem is:

Find $x \in \Omega$ that optimizes

$$
F(x) = \Big[ f_1(x), \; f_2(x), \; f_3(x), \; f_4(x) \Big]
$$

with:

$$
\begin{aligned} 
& f_1(x) = \eta_{\text{energy}}(x) = \frac{HHV_{H_2} \cdot r_{H_2}(x)}{V_{\text{cell}}(x) \cdot I_{\text{cell}}(x)} \quad \text{(Maximize)} \\
& f_2(x) = L(x) \quad \text{(Maximize Lifetime)} \\
& f_3(x) = c_{\text{ionomer}} \cdot \rho \cdot t + c_{\text{manuf}} \quad \text{(Minimize Cost)} \\
& f_4(x) = c_E \cdot \rho \cdot t \quad \text{(Minimize Environmental Impact)}
\end{aligned}
$$

Subject to:

$$
\begin{aligned} 
& V_{\min} \leq V_{\text{cell}}(x) \leq V_{\max}, \quad j_{\min} \leq j \leq j_{\max}, \\
& t \geq t_{\text{min}}, \\
& t \geq r \sqrt{\frac{k\, \Delta P \ SF}{\sigma_{\text{tensile}}}}, \\
& C_{\text{capital}}(x) \leq C_{\text{budget}}, \\
& E_{\text{material}}(x) \leq E_{\text{max}}, \\
& \text{and any additional equality constraints } h_j(x) = 0 \text{ (e.g., material balances)}.
\end{aligned}
$$

In practice, because we are simultaneously maximizing efficiency and lifetime while minimizing cost and environmental impact, we may reformulate the maximization objectives as minimization of their negative (or use a Pareto front approach).

---

## 5. Underlying Physics and Data Sources

- **Physics Models:**
    - The cell voltage $V_{\text{cell}}(x)$ is modeled considering activation, ohmic, and mass transport losses. For ohmic losses, the relation
      $$V_{\text{ohm}} = \frac{I_{\text{cell}} \cdot t}{\sigma(x) \cdot A}$$
      is used, where $\sigma(x)$ is a function of IEC, water content, and additives.
    - The hydrogen production rate $r_{H_2}(x)$ is obtained via Faraday’s law.
    - The stress-based durability model uses the simplified expression:
      $$\sigma \approx k \frac{\Delta P \, r^2}{t^2}.$$

- **Data Sources:**
    - Material parameters ($c_{\text{ionomer}}, \rho, \sigma_{\text{tensile}}, c_E$) are drawn from supplier datasheets and LCA databases.
    - Operational parameters ($\Delta P, j_{\min}, j_{\max}$, etc.) are taken from experimental reports and industry standards.
    - Manufacturing costs and equipment amortization factors are sourced from industry cost models and reports.

---

## 6. Next Steps

To finalize this model, further steps include:

- Collecting experimental and literature data to numerically parameterize each function.
- Validating the stress model and degradation predictions with mechanical testing data.
- Implementing the multiobjective optimization using suitable solvers (e.g., genetic algorithms for the discrete parts and gradient-based methods for continuous variables).
- Refining the model by incorporating additional constraints (such as operational temperature and humidity) and by performing sensitivity analysis to quantify the impact of uncertainties.









le't improve the model

let's make it a 3 objective, 1. efficiency . 2. cost 3. environmental impact

we''ll make lifetime a constraint that affects the three objective functions

for the efficiency

$$

ηenergy = \frac{HHV_{H_2} \cdot r_{H_2}}{V_{\text{cell}} \cdot I_{\text{cell}}}

$$

vell s a function of Vell = Vcell + 


# Efficiency function

## 1. Open-Circuit Voltage

A simplified Nernst equation for the water-splitting half‐reactions can be written as:

Voc(T,pan,pcat)  =  ΔGr0z F  +  R Tz F ln⁡ ⁣(aH2αH2  aO2αO2aH2OαH2O),V_{\text{oc}}(T, p_{\text{an}}, p_{\text{cat}}) \;=\; \frac{\Delta G_r^0}{z\,F} \;+\; \frac{R\,T}{z\,F}\,\ln\!\Biggl(\frac{a_{H_2}^{\alpha_{H_2}} \; a_{O_2}^{\alpha_{O_2}}}{a_{H_2O}^{\alpha_{H_2O}}}\Biggr),Voc​(T,pan​,pcat​)=zFΔGr0​​+zFRT​ln(aH2​OαH2​O​​aH2​αH2​​​aO2​αO2​​​​),

where

- ΔGr0\Delta G_r^0ΔGr0​ is the standard Gibbs free energy of reaction (J/mol),
- zzz is the number of electrons transferred per molecule of H2\mathrm{H_2}H2​ produced (for water splitting, z=2z=2z=2),
- F≈96485 C/molF\approx96485\,\mathrm{C/mol}F≈96485C/mol is Faraday’s constant,
- RRR is the universal gas constant, TTT is the cell temperature (K),
- aH2,aO2,aH2Oa_{H_2}, a_{O_2}, a_{H_2O}aH2​​,aO2​​,aH2​O​ are the activities (or partial pressures) of H2\mathrm{H_2}H2​, O2\mathrm{O_2}O2​, and H2O\mathrm{H_2O}H2​O, raised to stoichiometric coefficients αH2\alpha_{H_2}αH2​​, αO2\alpha_{O_2}αO2​​, αH2O\alpha_{H_2O}αH2​O​.  
    For typical PEM electrolysis, water activity is often ≈1\approx 1≈1, and partial pressures of H2\mathrm{H_2}H2​ and O2\mathrm{O_2}O2​ may differ at anode/cathode.

---

## 2. Activation Overpotential

The activation overpotentials at the anode and cathode (ΔVact, an\Delta V_{\text{act, an}}ΔVact, an​ and ΔVact, cat\Delta V_{\text{act, cat}}ΔVact, cat​) often follow Tafel‐type or Butler–Volmer equations. For simplicity, a Tafel‐like form is:

ΔVact, an(i)  =  R Tαan z F ln⁡ ⁣(ii0,an),ΔVact, cat(i)  =  R Tαcat z F ln⁡ ⁣(ii0,cat),\Delta V_{\text{act, an}}(i) \;=\; \frac{R\,T}{\alpha_{\text{an}}\,z\,F}\,\ln\!\Bigl(\frac{i}{i_{0,\text{an}}}\Bigr), \quad \Delta V_{\text{act, cat}}(i) \;=\; \frac{R\,T}{\alpha_{\text{cat}}\,z\,F}\,\ln\!\Bigl(\frac{i}{i_{0,\text{cat}}}\Bigr),ΔVact, an​(i)=αan​zFRT​ln(i0,an​i​),ΔVact, cat​(i)=αcat​zFRT​ln(i0,cat​i​),

where

- iii is the operating current density (A/cm2^22),
- i0,an,i0,cati_{0,\text{an}}, i_{0,\text{cat}}i0,an​,i0,cat​ are the exchange current densities at the anode and cathode,
- αan,αcat\alpha_{\text{an}}, \alpha_{\text{cat}}αan​,αcat​ are the charge‐transfer (symmetry) coefficients for anode and cathode.

Hence, the total activation overpotential is:

ΔVact(i)=ΔVact, an(i)+ΔVact, cat(i).\Delta V_{\text{act}}(i) = \Delta V_{\text{act, an}}(i) + \Delta V_{\text{act, cat}}(i).ΔVact​(i)=ΔVact, an​(i)+ΔVact, cat​(i).

---

## 3. Ohmic Overpotential

### 3.1 Membrane Ohmic Loss

The membrane ohmic drop is governed by the membrane thickness tmemt_{\text{mem}}tmem​ and its conductivity σmem(T,λ)\sigma_{\text{mem}}(T,\lambda)σmem​(T,λ), where λ\lambdaλ might represent water content or hydration. A typical relationship is:

ΔVohm, mem=i tmemσmem(T,λ).\Delta V_{\text{ohm, mem}} = i \,\frac{t_{\text{mem}}}{\sigma_{\text{mem}}(T,\lambda)}.ΔVohm, mem​=iσmem​(T,λ)tmem​​.

The membrane conductivity can be an Arrhenius‐type function of temperature or a more specific empirical correlation, e.g.,

σmem(T)=(0.0013 S/cm−0.00032 S/cm)exp⁡{1.26 (1303−1T)},\sigma_{\text{mem}}(T) = \Bigl(0.0013\,\mathrm{S/cm} - 0.00032\,\mathrm{S/cm}\Bigr)\exp\Bigl\{1.26\,\bigl(\tfrac{1}{303} - \tfrac{1}{T}\bigr)\Bigr\},σmem​(T)=(0.0013S/cm−0.00032S/cm)exp{1.26(3031​−T1​)},

or any other data-based correlation.

### 3.2 Electrode Ohmic Loss

The electrodes (anode/cathode) also contribute ohmic resistance. If each electrode has thickness telt_{\text{el}}tel​ and electrical conductivity σel\sigma_{\text{el}}σel​, the electrode ohmic drop is:

ΔVohm, el=i(telσel),\Delta V_{\text{ohm, el}} = i \left(\frac{t_{\text{el}}}{\sigma_{\text{el}}}\right),ΔVohm, el​=i(σel​tel​​),

summing anode + cathode. Alternatively, a total electrode resistance Rel=telAcell ρelR_{\text{el}} = \frac{t_{\text{el}}}{A_{\text{cell}}}\,\rho_{\text{el}}Rel​=Acell​tel​​ρel​ can be used if ρel\rho_{\text{el}}ρel​ is the resistivity. Summing these yields the total ohmic overpotential:

ΔVohm=ΔVohm, mem+ΔVohm, an+ΔVohm, cat.\Delta V_{\text{ohm}} = \Delta V_{\text{ohm, mem}} + \Delta V_{\text{ohm, an}} + \Delta V_{\text{ohm, cat}}.ΔVohm​=ΔVohm, mem​+ΔVohm, an​+ΔVohm, cat​.

---

## 4. Concentration Overpotential

At higher current densities, mass transport limitations can cause a concentration or mass‐transfer overpotential. A simplified form (for oxygen or hydrogen) might be:

ΔVconc(i)=R Tz αconc Fln⁡(ilim−iilim),\Delta V_{\text{conc}}(i) = \frac{R\,T}{z\,\alpha_{\text{conc}}\,F} \ln\Bigl(\frac{i_{\text{lim}} - i}{i_{\text{lim}}}\Bigr),ΔVconc​(i)=zαconc​FRT​ln(ilim​ilim​−i​),

where ilimi_{\text{lim}}ilim​ is the limiting current density (e.g., 6 A/cm2^22), and αconc\alpha_{\text{conc}}αconc​ is an empirical factor. This term grows significantly as i→ilimi \to i_{\text{lim}}i→ilim​.

---

## 5. Total Cell Voltage

Combining all terms, the cell voltage is:

Vcell(i,tmem,T)  =  Voc(T,pan,pcat)  +  ΔVact(i)  +  ΔVohm(i,tmem,T)  +  ΔVconc(i).V_{\text{cell}}(i, t_{\text{mem}}, T) \;=\; V_{\text{oc}}(T, p_{\text{an}}, p_{\text{cat}}) \;+\; \Delta V_{\text{act}}(i) \;+\; \Delta V_{\text{ohm}}(i, t_{\text{mem}}, T) \;+\; \Delta V_{\text{conc}}(i).Vcell​(i,tmem​,T)=Voc​(T,pan​,pcat​)+ΔVact​(i)+ΔVohm​(i,tmem​,T)+ΔVconc​(i).

---

## 6. Energy Efficiency Objective

Given the hydrogen production rate m˙H2\dot{m}_{H_2}m˙H2​​ and the total electrical power, the energy efficiency is:

ηenergy=HHVH2 m˙H2Vcell⋅Icell⋅Ncell.\eta_{\text{energy}} = \frac{HHV_{H_2}\,\dot{m}_{H_2}}{V_{\text{cell}} \cdot I_{\text{cell}} \cdot N_{\text{cell}}}.ηenergy​=Vcell​⋅Icell​⋅Ncell​HHVH2​​m˙H2​​​.

For a single cell of area AcellA_{\text{cell}}Acell​, if Icell=i⋅AcellI_{\text{cell}} = i \cdot A_{\text{cell}}Icell​=i⋅Acell​, the mass flow rate m˙H2\dot{m}_{H_2}m˙H2​​ is

m˙H2=i Acell⋅3600⋅MWH2⋅ηF2 F,\dot{m}_{H_2} = \frac{i\,A_{\text{cell}} \cdot 3600 \cdot MW_{H_2} \cdot \eta_F}{2\,F},m˙H2​​=2FiAcell​⋅3600⋅MWH2​​⋅ηF​​,

and for a stack of NcellN_{\text{cell}}Ncell​ in series, the same current flows through each cell. Simplifying, we get:

ηenergy(i,t)=HHVH2⋅3600⋅MWH2⋅ηF2F (Vcell(i,t)⋅i⋅Acell).\eta_{\text{energy}}(i,t) = \frac{HHV_{H_2} \cdot 3600 \cdot MW_{H_2} \cdot \eta_F}{2F \,\Bigl(V_{\text{cell}}(i,t) \cdot i \cdot A_{\text{cell}}\Bigr)}.ηenergy​(i,t)=2F(Vcell​(i,t)⋅i⋅Acell​)HHVH2​​⋅3600⋅MWH2​​⋅ηF​​.

In a multiobjective minimization setting, we define:

f1(x)=− ηenergy(x).f_1(x) = -\,\eta_{\text{energy}}(x).f1​(x)=−ηenergy​(x).




# Cost function

### 1. Capital Recovery Factor (CRF)

For an interest rate iii (as a decimal) and a lifetime of nnn years, the capital recovery factor is given by

CRF(i,n)=i (1+i)n(1+i)n−1.CRF(i,n) = \frac{i\,(1+i)^n}{(1+i)^n - 1}.CRF(i,n)=(1+i)n−1i(1+i)n​.

This factor annualizes an initial capital expense over the asset’s lifetime.

---

### 2. Equipment and Building Costs

**Equipment Cost:**  
Assume that the manufacturing facility requires SreqS_{\text{req}}Sreq​ production lines. The equipment cost is

Cequipment=Sreq⋅Cmfg_line⋅(1+Rinstallation),C_{\text{equipment}} = S_{\text{req}} \cdot C_{\text{mfg\_line}} \cdot (1+R_{\text{installation}}),Cequipment​=Sreq​⋅Cmfg_line​⋅(1+Rinstallation​),

where

- Cmfg_lineC_{\text{mfg\_line}}Cmfg_line​ is the base cost per manufacturing line, and
- RinstallationR_{\text{installation}}Rinstallation​ is the installation overhead (expressed as a fraction).

**Building Cost:**  
Similarly, the building cost is given by

Cbuilding=Sreq⋅Rbuildings⋅Mfootprint,C_{\text{building}} = S_{\text{req}} \cdot R_{\text{buildings}} \cdot M_{\text{footprint}},Cbuilding​=Sreq​⋅Rbuildings​⋅Mfootprint​,

where

- RbuildingsR_{\text{buildings}}Rbuildings​ is the cost per unit area of the building (e.g., $/m²), and
- MfootprintM_{\text{footprint}}Mfootprint​ is the required footprint per line (m²).

The annualized capital cost is then:

Ccapital=CRFequipment⋅Cequipment  +  CRFbuilding⋅Cbuilding.C_{\text{capital}} = CRF_{\text{equipment}} \cdot C_{\text{equipment}} \;+\; CRF_{\text{building}} \cdot C_{\text{building}}.Ccapital​=CRFequipment​⋅Cequipment​+CRFbuilding​⋅Cbuilding​.

---

### 3. Operating Costs

**Energy Cost:**  
Let each production line consume energy at a rate of ElineE_{\text{line}}Eline​ (kWh/year) and the cost of electricity is PenergyP_{\text{energy}}Penergy​ ($/kWh). Then

Cenergy=Sreq⋅Eline⋅Penergy.C_{\text{energy}} = S_{\text{req}} \cdot E_{\text{line}} \cdot P_{\text{energy}}.Cenergy​=Sreq​⋅Eline​⋅Penergy​.

**Labor Cost:**  
If each line requires NworkersN_{\text{workers}}Nworkers​ workers, operating at a wage rate RlaborR_{\text{labor}}Rlabor​ ($/hour), for a fraction MutilizationM_{\text{utilization}}Mutilization​ of the 8760 hours per year, then

Clabor=Sreq⋅Nworkers⋅Mutilization⋅8760⋅Rlabor.C_{\text{labor}} = S_{\text{req}} \cdot N_{\text{workers}} \cdot M_{\text{utilization}} \cdot 8760 \cdot R_{\text{labor}}.Clabor​=Sreq​⋅Nworkers​⋅Mutilization​⋅8760⋅Rlabor​.

**Materials Cost:**  
For the membrane itself, if each cell has an area AcellA_{\text{cell}}Acell​ (m²) and thickness ttt (m), with material density ρmem\rho_{\text{mem}}ρmem​ (kg/m³) and ionomer cost cionomerc_{\text{ionomer}}cionomer​ ($/kg), then the cost per cell is

Cmaterials, cell=cionomer⋅ρmem⋅t⋅Acell.C_{\text{materials, cell}} = c_{\text{ionomer}} \cdot \rho_{\text{mem}} \cdot t \cdot A_{\text{cell}}.Cmaterials, cell​=cionomer​⋅ρmem​⋅t⋅Acell​.

If the facility produces Ncells,annualN_{\text{cells,annual}}Ncells,annual​ cells per year, then the total materials cost is

Cmaterials=Ncells,annual⋅Cmaterials, cell.C_{\text{materials}} = N_{\text{cells,annual}} \cdot C_{\text{materials, cell}}.Cmaterials​=Ncells,annual​⋅Cmaterials, cell​.

Often, annual production is expressed in terms of total area produced:

Aannual=Ncells,annual⋅Acell.A_{\text{annual}} = N_{\text{cells,annual}} \cdot A_{\text{cell}}.Aannual​=Ncells,annual​⋅Acell​.

Then, the materials cost per unit area is simply

Cmaterials∗=cionomer⋅ρmem⋅t.C_{\text{materials}}^{*} = c_{\text{ionomer}} \cdot \rho_{\text{mem}} \cdot t.Cmaterials∗​=cionomer​⋅ρmem​⋅t.

---

### 4. Throughput and Number of Production Lines

If each manufacturing line has a production capacity of

Lcap=A˙line⋅8760⋅Mutilization(m²/year),L_{\text{cap}} = \dot{A}_{\text{line}} \cdot 8760 \cdot M_{\text{utilization}} \quad \text{(m²/year)},Lcap​=A˙line​⋅8760⋅Mutilization​(m²/year),

and the total annual production area required is

Aannual=Ncells,annual⋅Acell,A_{\text{annual}} = N_{\text{cells,annual}} \cdot A_{\text{cell}},Aannual​=Ncells,annual​⋅Acell​,

then the required number of lines is

Sreq=AannualLcap.S_{\text{req}} = \frac{A_{\text{annual}}}{L_{\text{cap}}}.Sreq​=Lcap​Aannual​​.

---

### 5. Full Annualized Cost Function

Combining all the components, the total annualized cost is:

Cannualized=  CRFequipment⋅[Sreq⋅Cmfg_line⋅(1+Rinstallation)]  +  CRFbuilding⋅[Sreq⋅Rbuildings⋅Mfootprint]+  Sreq⋅Eline⋅Penergy  +  Sreq⋅Nworkers⋅Mutilization⋅8760⋅Rlabor  +  Ncells,annual⋅Cmaterials, cell.\begin{aligned} C_{\text{annualized}} = \; & CRF_{\text{equipment}} \cdot \Bigl[S_{\text{req}} \cdot C_{\text{mfg\_line}} \cdot (1+R_{\text{installation}})\Bigr] \;+\; CRF_{\text{building}} \cdot \Bigl[S_{\text{req}} \cdot R_{\text{buildings}} \cdot M_{\text{footprint}}\Bigr] \\ & +\; S_{\text{req}} \cdot E_{\text{line}} \cdot P_{\text{energy}} \;+\; S_{\text{req}} \cdot N_{\text{workers}} \cdot M_{\text{utilization}} \cdot 8760 \cdot R_{\text{labor}} \;+\; N_{\text{cells,annual}} \cdot C_{\text{materials, cell}}. \end{aligned}Cannualized​=​CRFequipment​⋅[Sreq​⋅Cmfg_line​⋅(1+Rinstallation​)]+CRFbuilding​⋅[Sreq​⋅Rbuildings​⋅Mfootprint​]+Sreq​⋅Eline​⋅Penergy​+Sreq​⋅Nworkers​⋅Mutilization​⋅8760⋅Rlabor​+Ncells,annual​⋅Cmaterials, cell​.​

Dividing by the total annual membrane area AannualA_{\text{annual}}Aannual​ yields the cost per unit area:

f2(x)=CannualizedAannual.f_2(x) = \frac{C_{\text{annualized}}}{A_{\text{annual}}}.f2​(x)=Aannual​Cannualized​​.

In many cases, for a simplified membrane cost model, one might approximate the cost per m² as

f2(x)≈cionomer ρmem t+cmanuf,f_2(x) \approx c_{\text{ionomer}}\,\rho_{\text{mem}}\, t + c_{\text{manuf}},f2​(x)≈cionomer​ρmem​t+cmanuf​,

where cmanufc_{\text{manuf}}cmanuf​ is an effective manufacturing cost per m² that aggregates the capital, building, energy, and labor components normalized by the production area.

---

### 6. Summary of the Cost Objective Function

The complete cost objective function is:

f2(x)=CRFequipment⋅[Sreq⋅Cmfg_line⋅(1+Rinstallation)]+CRFbuilding⋅[Sreq⋅Rbuildings⋅Mfootprint]+Sreq⋅Eline⋅Penergy+Sreq⋅Nworkers⋅Mutilization⋅8760⋅Rlabor+Ncells,annual⋅(cionomer⋅ρmem⋅t⋅Acell)Ncells,annual⋅Acell.\boxed{ f_2(x) = \frac{CRF_{\text{equipment}} \cdot \Bigl[S_{\text{req}} \cdot C_{\text{mfg\_line}} \cdot (1+R_{\text{installation}})\Bigr] + CRF_{\text{building}} \cdot \Bigl[S_{\text{req}} \cdot R_{\text{buildings}} \cdot M_{\text{footprint}}\Bigr] + S_{\text{req}} \cdot E_{\text{line}} \cdot P_{\text{energy}} + S_{\text{req}} \cdot N_{\text{workers}} \cdot M_{\text{utilization}} \cdot 8760 \cdot R_{\text{labor}} + N_{\text{cells,annual}} \cdot \Bigl(c_{\text{ionomer}} \cdot \rho_{\text{mem}} \cdot t \cdot A_{\text{cell}}\Bigr)}{N_{\text{cells,annual}} \cdot A_{\text{cell}}}. }f2​(x)=Ncells,annual​⋅Acell​CRFequipment​⋅[Sreq​⋅Cmfg_line​⋅(1+Rinstallation​)]+CRFbuilding​⋅[Sreq​⋅Rbuildings​⋅Mfootprint​]+Sreq​⋅Eline​⋅Penergy​+Sreq​⋅Nworkers​⋅Mutilization​⋅8760⋅Rlabor​+Ncells,annual​⋅(cionomer​⋅ρmem​⋅t⋅Acell​)​.​

Where:

- CRFequipment=CRF(ieq,neq)CRF_{\text{equipment}} = CRF(i_{eq}, n_{eq})CRFequipment​=CRF(ieq​,neq​) and CRFbuilding=CRF(ibuild,nbuild)CRF_{\text{building}} = CRF(i_{build}, n_{build})CRFbuilding​=CRF(ibuild​,nbuild​) are computed from their respective interest rates and lifetimes.
- Sreq=AannualLcapS_{\text{req}} = \dfrac{A_{\text{annual}}}{L_{\text{cap}}}Sreq​=Lcap​Aannual​​ with Lcap=A˙line⋅8760⋅MutilizationL_{\text{cap}} = \dot{A}_{\text{line}} \cdot 8760 \cdot M_{\text{utilization}}Lcap​=A˙line​⋅8760⋅Mutilization​.
- Aannual=Ncells,annual⋅AcellA_{\text{annual}} = N_{\text{cells,annual}} \cdot A_{\text{cell}}Aannual​=Ncells,annual​⋅Acell​.
- Cmfg_lineC_{\text{mfg\_line}}Cmfg_line​, RinstallationR_{\text{installation}}Rinstallation​, RbuildingsR_{\text{buildings}}Rbuildings​, MfootprintM_{\text{footprint}}Mfootprint​, ElineE_{\text{line}}Eline​, PenergyP_{\text{energy}}Penergy​, NworkersN_{\text{workers}}Nworkers​, MutilizationM_{\text{utilization}}Mutilization​, RlaborR_{\text{labor}}Rlabor​ are facility-specific parameters.
- cionomerc_{\text{ionomer}}cionomer​, ρmem\rho_{\text{mem}}ρmem​, ttt, and AcellA_{\text{cell}}Acell​ define the membrane material cost.

For a simplified model that considers only the direct materials and an aggregated manufacturing cost per area, one can use:

f2(x)≈cionomer ρmem t+cmanuf,f_2(x) \approx c_{\text{ionomer}}\,\rho_{\text{mem}}\, t + c_{\text{manuf}},f2​(x)≈cionomer​ρmem​t+cmanuf​,

where cmanufc_{\text{manuf}}cmanuf​ is a lump-sum manufacturing cost per m² derived from the more detailed model.

from IPython.display import Markdown

# Create Obsidian-compatible markdown with $ $ and $$ $$ for equations
obsidian_markdown = """
# Efficiency Function

## 1. Open-Circuit Voltage

A simplified Nernst equation for the water-splitting half‐reactions:

$$
V_{\\text{oc}}(T, p_{\\text{an}}, p_{\\text{cat}}) = \\frac{\\Delta G_r^0}{zF} + \\frac{RT}{zF} \\ln\\left(\\frac{a_{H_2}^{\\alpha_{H_2}} a_{O_2}^{\\alpha_{O_2}}}{a_{H_2O}^{\\alpha_{H_2O}}}\\right)
$$

Where:
- \\( \\Delta G_r^0 \\): standard Gibbs free energy (J/mol)
- \\( z \\): electrons per \\( H_2 \\) molecule (typically 2)
- \\( F \\approx 96485 \\): Faraday's constant
- \\( R \\): universal gas constant
- \\( T \\): temperature (K)
- \\( a_{H_2}, a_{O_2}, a_{H_2O} \\): activities or partial pressures

---

## 2. Activation Overpotential

Simplified Tafel expressions for anode and cathode:

$$
\\Delta V_{\\text{act, an}}(i) = \\frac{RT}{\\alpha_{\\text{an}} zF} \\ln\\left(\\frac{i}{i_{0,\\text{an}}}\\right), \\quad
\\Delta V_{\\text{act, cat}}(i) = \\frac{RT}{\\alpha_{\\text{cat}} zF} \\ln\\left(\\frac{i}{i_{0,\\text{cat}}}\\right)
$$

Total activation overpotential:

$$
\\Delta V_{\\text{act}}(i) = \\Delta V_{\\text{act, an}}(i) + \\Delta V_{\\text{act, cat}}(i)
$$

---

## 3. Ohmic Overpotential

### 3.1 Membrane

$$
\\Delta V_{\\text{ohm, mem}} = i \\cdot \\frac{t_{\\text{mem}}}{\\sigma_{\\text{mem}}(T,\\lambda)}
$$

Empirical form for \\( \\sigma_{\\text{mem}}(T) \\):

$$
\\sigma_{\\text{mem}}(T) = (0.0013 - 0.00032) \\exp\\left(1.26\\left(\\frac{1}{303} - \\frac{1}{T}\\right)\\right)
$$

### 3.2 Electrodes

$$
\\Delta V_{\\text{ohm, el}} = i \\cdot \\left(\\frac{t_{\\text{el}}}{\\sigma_{\\text{el}}}\\right)
$$

Total ohmic loss:

$$
\\Delta V_{\\text{ohm}} = \\Delta V_{\\text{ohm, mem}} + \\Delta V_{\\text{ohm, an}} + \\Delta V_{\\text{ohm, cat}}
$$

---

## 4. Concentration Overpotential

$$
\\Delta V_{\\text{conc}}(i) = \\frac{RT}{z \\alpha_{\\text{conc}} F} \\ln\\left(\\frac{i_{\\text{lim}} - i}{i_{\\text{lim}}}\\right)
$$

---

## 5. Total Cell Voltage

$$
V_{\\text{cell}}(i, t_{\\text{mem}}, T) = V_{\\text{oc}} + \\Delta V_{\\text{act}} + \\Delta V_{\\text{ohm}} + \\Delta V_{\\text{conc}}
$$

---

## 6. Energy Efficiency

Hydrogen mass flow:

$$
\\dot{m}_{H_2} = \\frac{i A_{\\text{cell}} \\cdot 3600 \\cdot MW_{H_2} \\cdot \\eta_F}{2F}
$$

Energy efficiency:

$$
\\eta_{\\text{energy}} = \\frac{HHV_{H_2} \\cdot \\dot{m}_{H_2}}{V_{\\text{cell}} I_{\\text{cell}} N_{\\text{cell}}}
$$

In optimization:

$$
f_1(x) = -\\eta_{\\text{energy}}(x)
$$

---

# Cost Function

## 1. Capital Recovery Factor

$$
CRF(i,n) = \\frac{i(1+i)^n}{(1+i)^n - 1}
$$

---

## 2. Equipment & Building Costs

Equipment:

$$
C_{\\text{equipment}} = S_{\\text{req}} C_{\\text{mfg\\_line}} (1 + R_{\\text{installation}})
$$

Building:

$$
C_{\\text{building}} = S_{\\text{req}} R_{\\text{buildings}} M_{\\text{footprint}}
$$

Annualized capital:

$$
C_{\\text{capital}} = CRF_{\\text{equipment}} C_{\\text{equipment}} + CRF_{\\text{building}} C_{\\text{building}}
$$

---

## 3. Operating Costs

Energy:

$$
C_{\\text{energy}} = S_{\\text{req}} E_{\\text{line}} P_{\\text{energy}}
$$

Labor:

$$
C_{\\text{labor}} = S_{\\text{req}} N_{\\text{workers}} M_{\\text{utilization}} 8760 R_{\\text{labor}}
$$

Materials per cell:

$$
C_{\\text{materials, cell}} = c_{\\text{ionomer}} \\rho_{\\text{mem}} t A_{\\text{cell}}
$$

Total:

$$
C_{\\text{materials}} = N_{\\text{cells,annual}} \\cdot C_{\\text{materials, cell}}
$$

---

## 4. Production Line Sizing

Line capacity:

$$
L_{\\text{cap}} = \\dot{A}_{\\text{line}} \\cdot 8760 \\cdot M_{\\text{utilization}}
$$

Lines required:

$$
S_{\\text{req}} = \\frac{A_{\\text{annual}}}{L_{\\text{cap}}}
$$

---

## 5. Annualized Cost Function

$$
\\begin{aligned}
f_2(x) = \\; & \\frac{
CRF_{\\text{equipment}} \\cdot \\Big[S_{\\text{req}} C_{\\text{mfg\\_line}} (1+R_{\\text{installation}})\\Big]
+ CRF_{\\text{building}} \\cdot \\Big[S_{\\text{req}} R_{\\text{buildings}} M_{\\text{footprint}}\\Big] \\\\
& + S_{\\text{req}} E_{\\text{line}} P_{\\text{energy}}
+ S_{\\text{req}} N_{\\text{workers}} M_{\\text{utilization}} 8760 R_{\\text{labor}}
+ N_{\\text{cells,annual}} c_{\\text{ionomer}} \\rho_{\\text{mem}} t A_{\\text{cell}}
}{
N_{\\text{cells,annual}} A_{\\text{cell}} }
\\end{aligned}
$$

Simplified:

$$
f_2(x) \\approx c_{\\text{ionomer}} \\rho_{\\text{mem}} t + c_{\\text{manuf}}
$$
"""

Markdown(obsidian_markdown)




# Environmental impact model

formulation for the environmental impact objective—designed for a cradle‐to‐gate life‐cycle analysis (LCA) of the PEM electrolyser manufacturing process. This formulation details the key input parameters, the corresponding characterization factors, and shows how these data can be combined into an overall environmental impact indicator. 
This formulation is intended to be used later with the openLCA Python IPC API for automated impact assessments.

---

## Environmental Impact Model for Cradle-to-Gate Analysis

### 1. General Formulation

For cradle‐to‐gate LCA, the overall environmental impact is calculated as an aggregated impact score:

Impact Score=∑iQi×CFi,\text{Impact Score} = \sum_{i} Q_i \times CF_i,

where:

- QiQ_i is the quantity of material or energy flow for input ii (e.g., in kg, kWh, m3^3).
- CFiCF_i is the characterization factor for input ii (e.g., kg CO2_2-eq per unit), which represents the environmental burden (global warming potential, acidification, etc.) per unit of that input.

In our model for the manufacturing of a PEM electrolyser, the key inputs can be grouped into several categories.

---

### 2. Key Input Categories and Parameters

#### A. **Raw Material Inputs**

1. **Ionomer (Membrane Material):**
    
    - QionomerQ_{\text{ionomer}} [kg/m²]: The mass of ionomer required per unit area. This is given by:
        
        Qionomer=ρmem×t,Q_{\text{ionomer}} = \rho_{\text{mem}} \times t,
        
        where:
        
        - ρmem\rho_{\text{mem}} is the density of the membrane material (kg/m³),
        - tt is the membrane thickness (m).
    - CFionomerCF_{\text{ionomer}} [kg CO2_2-eq/kg]: Characterization factor for the production of the ionomer (from cradle to gate).
        
2. **Catalyst Materials:**
    
    - QcatQ_{\text{cat}} [kg/m²]: The mass of catalyst (e.g., platinum or alternative catalyst) used per unit area. This value depends on catalyst loading (mg/cm²) and cell area.
    - CFcatCF_{\text{cat}} [kg CO2_2-eq/kg]: Characterization factor for the catalyst production (including extraction, refining, etc.).
3. **Additives and Fillers:**
    
    - QaddQ_{\text{add}} [kg/m²]: Quantity of any additional additives (e.g., ceramic fillers) per unit area.
    - CFaddCF_{\text{add}} [kg CO2_2-eq/kg]: Their associated environmental impact.

#### B. **Energy Consumption**

1. **Electricity:**
    
    - QelecQ_{\text{elec}} [kWh/m²]: Electricity consumption per unit area of membrane produced.
    - CFelecCF_{\text{elec}} [kg CO2_2-eq/kWh]: Emission factor for the electricity mix used in manufacturing.
2. **Thermal Energy (Fuel Use):**
    
    - QfuelQ_{\text{fuel}} [MJ/m²] or [kWh/m²]: Energy used for heating (if applicable).
    - CFfuelCF_{\text{fuel}} [kg CO2_2-eq per MJ or per kWh]: Characterization factor for the fuel used.

#### C. **Water Consumption**

- QwaterQ_{\text{water}} [m3^3/m²]: Volume of water used per unit area of membrane produced.
- CFwaterCF_{\text{water}} [impact units per m3^3]: Characterization factor (this could address water scarcity, energy for water treatment, etc.).

#### D. **Manufacturing Infrastructure**

1. **Capital Equipment:**
    
    - Embedded impacts of manufacturing equipment might be expressed as an impact per unit area of production. For simplicity, one might define:
        
        Qequip(e.g., kg CO2-eq/m²)Q_{\text{equip}} \quad \text{(e.g., kg CO\(_2\)-eq/m²)}
        
        or use a corresponding CFequipCF_{\text{equip}}.
        
2. **Building and Infrastructure:**
    
    - Similar to equipment, the construction and operation of the facility can be characterized per unit production area:
        
        Qbuild(impact per m²).Q_{\text{build}} \quad \text{(impact per m²)}.

#### E. **Transportation**

- QtransQ_{\text{trans}} [kg CO2_2-eq/m²]: Impact from transporting raw materials to the facility and finished membranes to subsequent assembly. This can be aggregated as a per-area impact with an appropriate CFtransCF_{\text{trans}}.

#### F. **Waste and Recycling**

- **Waste Generation:**
    - QwasteQ_{\text{waste}} [kg/m²] with a corresponding waste treatment factor CFwasteCF_{\text{waste}} (if significant).
- **Recycling/By-product Credits:**
    - These might be subtracted if the process recovers materials.

---

### 3. Environmental Impact Objective Function

Assuming the total annual membrane production is based on an area AannualA_{\text{annual}} (m²), the environmental impact per m² (our objective f3(x)f_3(x)) can be written as the sum of impacts from all key inputs, normalized by the production area:

f3(x)=  CFionomer⋅Qionomer+CFcat⋅Qcat+CFadd⋅Qadd+CFelec⋅Qelec+CFfuel⋅Qfuel+CFwater⋅Qwater+Qequip+Qbuild+Qtrans+CFwaste⋅Qwaste.\begin{aligned} f_3(x) = \; & CF_{\text{ionomer}} \cdot Q_{\text{ionomer}} + CF_{\text{cat}} \cdot Q_{\text{cat}} + CF_{\text{add}} \cdot Q_{\text{add}} \\ & + CF_{\text{elec}} \cdot Q_{\text{elec}} + CF_{\text{fuel}} \cdot Q_{\text{fuel}} \\ & + CF_{\text{water}} \cdot Q_{\text{water}} \\ & + Q_{\text{equip}} + Q_{\text{build}} + Q_{\text{trans}} + CF_{\text{waste}} \cdot Q_{\text{waste}}. \end{aligned}

Where:

- Qionomer=ρmem⋅tQ_{\text{ionomer}} = \rho_{\text{mem}} \cdot t (kg/m²),
- QcatQ_{\text{cat}}, QaddQ_{\text{add}} are determined from material loadings per m²,
- QelecQ_{\text{elec}}, QfuelQ_{\text{fuel}}, QwaterQ_{\text{water}} are based on process energy and resource consumption (units per m²),
- Qequip,Qbuild,Qtrans,QwasteQ_{\text{equip}}, Q_{\text{build}}, Q_{\text{trans}}, Q_{\text{waste}} are either directly given or calculated on a per-m² basis from the overall facility production capacity.

Each CFiCF_i should be obtained from life-cycle databases or literature (e.g., Ecoinvent, USLCI) and reflect the cradle-to-gate impacts.

---

### 4. Summary of Parameters for the Environmental Impact Model

For later integration with the openLCA Python IPC API, the following parameters (with units) should be defined:

1. **Raw Materials:**
    
    - ρmem\rho_{\text{mem}} (kg/m³): Density of membrane material.
    - tt (m): Membrane thickness (decision variable).
    - cionomerc_{\text{ionomer}} – Already used in cost; here we use its impact factor:
        - CFionomerCF_{\text{ionomer}} (kg CO2_2-eq/kg).
    - Catalyst loading:
        - QcatQ_{\text{cat}} (kg/m²) and CFcatCF_{\text{cat}} (kg CO2_2-eq/kg).
    - Additives:
        - QaddQ_{\text{add}} (kg/m²) and CFaddCF_{\text{add}} (kg CO2_2-eq/kg).
2. **Energy:**
    
    - QelecQ_{\text{elec}} (kWh/m²): Electricity consumption per m².
    - CFelecCF_{\text{elec}} (kg CO2_2-eq/kWh).
    - QfuelQ_{\text{fuel}} (MJ/m² or kWh/m²): Thermal energy consumption.
    - CFfuelCF_{\text{fuel}} (kg CO2_2-eq/MJ or per kWh).
3. **Water:**
    
    - QwaterQ_{\text{water}} (m³/m²): Water usage per m².
    - CFwaterCF_{\text{water}} (impact units/m³).
4. **Infrastructure:**
    
    - QequipQ_{\text{equip}} (kg CO2_2-eq/m²): Embedded impact for equipment.
    - QbuildQ_{\text{build}} (kg CO2_2-eq/m²): Embedded impact for building construction.
5. **Transportation:**
    
    - QtransQ_{\text{trans}} (kg CO2_2-eq/m²): Impact due to transportation.
6. **Waste:**
    
    - QwasteQ_{\text{waste}} (kg/m²): Waste material generated per m².
    - CFwasteCF_{\text{waste}} (kg CO2_2-eq/kg): Impact factor for waste treatment.
7. **Production Throughput:**
    
    - AannualA_{\text{annual}} (m²/year): Total membrane area produced annually.
    - Other parameters (e.g., line capacity, utilization) used to compute AannualA_{\text{annual}} if needed.

---

### 5. Final Environmental Impact Objective

Thus, the environmental impact objective per unit area is:

f3(x)=CFionomer ρmem t  +  CFcat Qcat  +  CFadd Qadd  +  CFelec Qelec  +  CFfuel Qfuel  +  CFwater Qwater  +  Qequip  +  Qbuild  +  Qtrans  +  CFwaste Qwaste.\boxed{ f_3(x) = CF_{\text{ionomer}}\,\rho_{\text{mem}}\,t \;+\; CF_{\text{cat}}\,Q_{\text{cat}} \;+\; CF_{\text{add}}\,Q_{\text{add}} \;+\; CF_{\text{elec}}\,Q_{\text{elec}} \;+\; CF_{\text{fuel}}\,Q_{\text{fuel}} \;+\; CF_{\text{water}}\,Q_{\text{water}} \;+\; Q_{\text{equip}} \;+\; Q_{\text{build}} \;+\; Q_{\text{trans}} \;+\; CF_{\text{waste}}\,Q_{\text{waste}}. }

All terms are expressed per unit production area (m²). This formulation can then be used within a cradle-to-gate LCA framework—for example, via the openLCA Python IPC API—to automatically calculate the environmental impact based on user-specified parameters and process data.

---

### Conclusion

This detailed environmental impact model defines all necessary parameters for a cradle-to-gate analysis of the manufacturing process for a PEM electrolyser. It includes raw material inputs, energy and water usage, infrastructure impacts, transportation, and waste treatment impacts. These parameters, along with their corresponding characterization factors, provide a complete basis for integrating the environmental impact into the overall multiobjective optimization and for later use with the openLCA Python IPC API.

## Parameter List for Cradle-to-Gate Analysis

Below is a summary table of the parameters (with suggested units):

| Parameter                       | Symbol                                          | Unit                | Description                                        |
| ------------------------------- | ----------------------------------------------- | ------------------- | -------------------------------------------------- |
| Ionomer mass per unit area      | QionomerQ_{\text{ionomer}}Qionomer​             | kg/m²               | ρmem⋅t\rho_{\text{mem}} \cdot tρmem​⋅t             |
| Ionomer impact factor           | CFionomerCF_{\text{ionomer}}CFionomer​          | kg CO₂-eq/kg        | Environmental impact per kg of ionomer production  |
| Catalyst mass per unit area     | QcatQ_{\text{cat}}Qcat​                         | kg/m²               | Mass of catalyst per membrane area (if applicable) |
| Catalyst impact factor          | CFcatCF_{\text{cat}}CFcat​                      | kg CO₂-eq/kg        | Impact per kg of catalyst production               |
| Additives mass per unit area    | QaddQ_{\text{add}}Qadd​                         | kg/m²               | Mass of fillers or additives used                  |
| Additives impact factor         | CFaddCF_{\text{add}}CFadd​                      | kg CO₂-eq/kg        | Impact per kg of additives                         |
| Electricity consumption         | QenergyQ_{\text{energy}}Qenergy​                | kWh/m²              | Electricity usage per m² of membrane production    |
| Electricity impact factor       | CFenergyCF_{\text{energy}}CFenergy​             | kg CO₂-eq/kWh       | Emission factor for electricity                    |
| Thermal energy consumption      | QheatQ_{\text{heat}}Qheat​                      | MJ/m²               | Thermal energy used per m²                         |
| Thermal energy impact factor    | CFheatCF_{\text{heat}}CFheat​                   | kg CO₂-eq/MJ        | Impact per MJ of thermal energy                    |
| Solvent usage                   | QsolventQ_{\text{solvent}}Qsolvent​             | L/m² or kg/m²       | Solvent volume or mass per m²                      |
| Solvent impact factor           | CFsolventCF_{\text{solvent}}CFsolvent​          | kg CO₂-eq/(L or kg) | Impact per unit solvent                            |
| Process chemicals usage         | QchemQ_{\text{chem}}Qchem​                      | kg/m²               | Mass of other chemicals used                       |
| Process chemicals impact factor | CFchemCF_{\text{chem}}CFchem​                   | kg CO₂-eq/kg        | Impact per kg of chemicals                         |
| Transportation raw materials    | Qtrans,matQ_{\text{trans,mat}}Qtrans,mat​       | kg·km/m²            | Mass-distance factor for raw materials             |
| Transportation impact factor    | CFtrans,matCF_{\text{trans,mat}}CFtrans,mat​    | kg CO₂-eq/(kg·km)   | Emission factor for transport of raw materials     |
| Transportation chemicals        | Qtrans,chemQ_{\text{trans,chem}}Qtrans,chem​    | kg·km/m²            | Mass-distance factor for chemicals                 |
| Transportation impact factor    | CFtrans,chemCF_{\text{trans,chem}}CFtrans,chem​ | kg CO₂-eq/(kg·km)   | Emission factor for transport of chemicals         |
| Waste generated                 | QwasteQ_{\text{waste}}Qwaste​                   | kg/m²               | Waste per m² from production                       |
| Waste treatment impact factor   | CFwasteCF_{\text{waste}}CFwaste​                | kg CO₂-eq/kg        | Impact per kg of waste disposed                    |

These parameters (or a subset of them) form the basis for a cradle-to-gate analysis that you can later incorporate using the openLCA Python IPC API.


