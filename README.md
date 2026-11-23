# Kinetic Monte Carlo Method for Simulating Deoxidation and Oxidation in Resistive RAMs with Embedded Conductive Nanocrystals

If you use this information, please :), cite: https://doi.org/10.3390/nano13142124 or https://doi.org/10.3390/chips4010011.

Typically, the oxides in the semiconductor industry are used as insulators or “gate oxides”. When a high electric field is applied to this material, it can produce a dielectric breakdown,  meaning the material becomes conductive. But, if this breakdown is reversible? This is the idea behind the neuromorphic computing through deoxidation-oxidation process.

## Deoxidation Process

<img src="AttachmentsREADME/kMC_SetProcess.gif" alt="Set-GIF" width="600"/>

The deoxidation process in a thin film oxide can generate lattice conductive sites that form conductive filaments. One way to simulate this process is with the Kinetic Monte Carlo method (kMC), which is based on Harmonic Transition State Theory (hTST) and can calculate the probability of generating a conductive defect (https://doi.org/10.3390/chips4010011). 

$$
P_{ijk}^G=\frac{t}{t_0}\exp{\left(-\frac{E_{Oe} - q \gamma a F_{ij}^{nH}}{k T_r}\right)}
$$

These defects can be oxygen vacancies ($V_O$), which are represented in the animation as orange cubes. The oxygen ions (red balls), which have a negative charge, can escape their equilibrium sites due to the electric field ($F^{nH}$), which reduces the effective potential barrier. The right side of the animation shows the journey of an oxygen ion from generating an oxygen vacancy to reaching the top electrode.

## Oxidation Process

<img src="AttachmentsREADME/kMC_ResetProcess.gif" alt="Reset-GIF" width="600"/>

The oxidation process in a thin film oxide can “erase” conductive sites that form conductive filaments. The kMC simulation can calculate the probability of recombination with conductive defects (https://doi.org/10.3390/chips4010011). 

$$
P_{ijk}^R=\frac{t}{t_0} \beta_R f_k \exp{\left(-\frac{|v| t}{L_O}\right)} \exp{\left(-\frac{E_{Oe}}{k T_J}\right)}
$$

The oxygen ions (red balls) can escape their equilibrium sites due to the electric field ($F^H$), which reduces the effective potential barrier near the top electrode and increase the velocity ($v$). The right side of the animation shows the journey of an oxygen ion from the top electrode to reaching the oxygen vacancy in the (4, j) site.

## Effect of the Embedded Conductive Nanocrystals

<img src="AttachmentsREADME/With_without_NC.gif" alt="Reset-GIF" width="600"/>

Experimental and simulation results of oxides such as titanium oxide, zinc oxide and tin oxide have demonstrated the resistive switching (RS) phenomenon, whereby the resistivity changes when different polarity of electrical field is applied. In the semiconductor industry, silicon oxide is the most common oxide, but this material does not exhibit RS due to the high electrical field required to achieve dielectric breakdown, which prevents the reversibility of this phenomenon. To overcome this problem, silicon nanocrystals (shown in blue in the simulation) embedded in the oxide can reduce the effective distance, and conductive defects (orange cubes) are less likely to cause the device to return to low current values.

We explain this phenomenon in more detail in the papers https://ieeexplore.ieee.org/document/9908188 and https://doi.org/10.3390/chips4010011, and we present the experimental and 2D simulation in https://doi.org/10.3390/nano13142124.
The 2D simulation program is available as a release in my GitHub repository.: https://github.com/JuanFedericoRamirezRios/2D-simulation-bipolar-RS-NCs 
The python implementation of 3D simulation  is available in: https://github.com/JuanFedericoRamirezRios/3D-simulation-bipolar-RS-NCs 
