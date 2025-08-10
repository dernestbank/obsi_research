


Independent Variables

Temperature - The operational temperature of the electrolyzer, which can affect the reaction rate and efficiency.

Membrane Type - The choice of membrane can affect the ion conductivity and therefore the efficiency of the electrolysis.

Electrolyte Composition - The type and concentration of electrolytes used can influence the conductivity and the overall efficiency.

Electrode Material and Surface Area - Different materials and surface areas can affect the catalytic activity and the current density.

Flow Rate of Water - The rate at which water is supplied to the electrolyzer can impact the efficiency and output of hydrogen


### Membrane ancillary

The net water flow through the membrane can be expressed in terms of three processes: diffusion, electro-osmotic drag and hydraulic pressure effect.

the net molar flow rate of water
$$
\dot{N}_{H_2O}^{mem} = \dot{N}_{H_2O}^{diff} + \dot{N}_{H_2O}^{eod} - \dot{N}_{H_2O}^{pe}
$$


In practice, electro-osmotic drag is the dominant mechanism, in which water molecules are coordinated around the migrating H3Oþ species and dragged to the cathode.(Abdin et al., 2015) @abdinModellingSimulationProton2015

$$
\dot{N}_{H_2O}^{diff} = \frac{A D_w}{\delta_{mem}} \left( C_{H_2O,mem}^{cat} - C_{H_2O,mem}^{an} \right)
$$

Membrane thickness

The range of membrane thickness for PEM electrolyzers varies depending on the specific application and optimization goals. In the context of polymer electrolyte membrane water electrolysis (PEMWE), membrane thicknesses have been explored in the range of 60 µm [1] to as low as 0.0127 mm [2]. Additionally, studies have investigated the impact of membrane thickness on PEM fuel cell (PEMFC) performance, where thicknesses of perfluorosulfonic acid (PFSA) membranes ranged from 8 to 25 µm [3]. These variations in membrane thickness are crucial for achieving high efficiency and durability in PEM electrolyzer systems, with thinner membranes potentially leading to enhanced current density and efficiency, while thicker membranes may offer improved chemical durability and reduced gas crossover [4] [5].

`The current range of (perfluorosulfonic acid) PFSA membrane thicknesses employed for commercial applications range from 8 -25 µm. As with most adjustable materials parameters, there are a host of properties (cost, gas permeability, proton conductivity, etc.) that require co-optimization to provide the overall preferred position. For example, thin membranes will minimize proton resistance, facilitating high power densities, but will simultaneously allow increased gas crossover fluxes that can contribute to both reduced fuel efficiency and increased oxidative stress. On the other end of the spectrum, thick membranes will decrease gas crossover fluxes, offering improved fuel efficiency while simultaneously decreasing power density.`  @comsPFSAMembraneThickness2022
Coms et al., 2022)



To calculate the effective area of an electrolyser

To calculate the effective area of an electrolyzer, different methods are proposed based on the type of electrolyzer and catalyst used. For instance, in the case of iridium oxide catalysts in PEM electrolyzers, a method was developed to determine the electrochemically active surface area (ECSA) by correlating pseudocapacitive charge with the ECSA[1] [2]. This method resulted in a constant value of 601 mC/cm2 for powder electrocatalysts. Similarly, for sizing an electrolyzer for stand-alone applications, optimizing the current density and active area of the membrane is crucial to achieve thermal self-sustaining mode without the need for external heating[3]. Additionally, electrolyzers designed for the recovery of valuable metals focus on increasing the contact specific surface area by arranging anodes and cathodes to enhance metal recovery efficiency[4


Catalyst layer

Catalyst for HER

The options for catalysts for the Hydrogen Evolution Reaction (HER) on the cathode of Proton Exchange Membrane (PEM) electrolyzers include various materials such as platinum group metal (PGM)-free catalysts, Mo-based nanomaterials like 1T′-MoS2, Co-MoS2, and β-Mo2C, Pd-based architectures, and PGM-free transition metal oxides derived from metal-organic frameworks. These catalysts have shown promising performance in driving the HER with low overpotentials, high efficiency, and excellent stability under acidic conditions. (Piñeiro García et al., 2023; Zhang et al., 2023) @zhangAccurateEfficientMachine2023; @pineirogarciaBenchmarkingMolybdenumBasedMaterials2023

1 2 3 4 5 . The development of these catalysts aims to reduce the dependency on expensive noble metals like platinum, enhance the efficiency of hydrogen production, and improve the overall cost-effectiveness of PEM electrolysis for green hydrogen generation.