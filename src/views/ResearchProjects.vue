<template>
    <div class="researchProjects">
        <div class="researchProject">
            <div class="researchProjectText">
                <h1>Diffusion Drying Simulation</h1>
                <h4>Key Words: SPH, LAMMPS, Li-ion Battery, MD</h4>

                <p>Using a custom inter-particle diffusion model built into LAMMPS's SPH implementation, I was able to model the drying of Li-ion Battery solvent during the drying manufacturing step.</p>
                <p>The diagram to the right shows the simulation result used to verify correct behavior using a simple column of pure solvent. Similar verifications were done using the simulated and anaylitcal solution to the Arnold Diffusion cell.</p>
                <p>This model can be used to accurately observe how solvent evaporates through the porous electrode film during drying.</p>
                <p>This model will included in future work published by the Battery Materials Research (BMR) Group at BYU.</p>
            </div>
            <img src="ezgif-6-403fe3f0a529.gif">
        </div>

        <div class="researchProject researchProjectRev">
            <img src="slurry_cropped.png">
            <div class="researchProjectText">
                <h1>Realistic Initial Structure Generator</h1>
                <h4>Key Words: Python, Neighbor List, Algorithm</h4>

                <p>When I first joined the BMR group, the molecular modeling team already had an initial structure generator in use. However, this generator was plagued by horrible wait times and by particles placed on top of neighboring particles.</p>
                <p>After familiarizing myself with the program, I saw several opportunites for improvement. I introduced a novel neightbor tracking algormithm that kept track of particle's positions and neightbors without ever needing to itterate over every particle in the system. This algorithm also allowed for additional parameters to be set to completely eliminate the possiblility of an overlap.</p>
                <p>This reduced the reduced the operation time from quadratic with time to linear, saving countless hours of waiting. Once the user-input parameters are set, this generator can create realistic initial structures that minimize equilibrium simulation time while perfectly matching slurry specifications such as composition, particle size, particle shape, particle orientation, spacial distribution, etc.</p>
                <p>This generator was used in several BMR publications beyond just ones posted in the CV portion of this site.</p>
            </div>

        </div>

        <div class="researchProject">
            <div class="researchProjectText">
                <h1>RESPA Implementation in HOOMD</h1>
                <h4>Key Words: HOOMD, RESPA, DPD, MD</h4>

                <p>One of the greatest limitations of Molecular Dynamics is the inability to simulate large time or spatial scales without absoloutley massive computational resources. While sophisticated neighbor tracking can ease this issue slightly, other solutions are needed. Reversible Reference System Propagator Algorithms (RESPA) allow for multiple time scales to be used to govergn various interactions in an MD simulation.</p>
                <p>However, this is not a current official implementation of RESPA in HOOMD. I've currently been working in the de Pablo Group at the Pritzker School of Molecular Engineering to create one. The implementation is currently undergoing testing to validate it's physical accuracy before it used in to boost the time scale of several DPD simulations.</p>
            </div>
            <img src="CodeSnip.PNG">
        </div>
    </div>
</template>

<style>
.researchProjects {
    width: 100%;
    display: flex;
    flex-direction: column;
    text-align: left;
}

@media only screen and (min-width: 601px) {
    .researchProject {
        width: 100%;
        display: flex;
        flex-direction: row;
        margin-bottom: 40px;
        justify-content: center;
        align-items: center;
    }
    .researchProjectText {
        display: flex;
        flex-direction: column;
        flex-grow: 1;
        flex-basis: 0;
        margin-left: 8px;
        margin-right: 8px;
    }

    .researchProjectText h4 {
        margin-top: 0px;
    }

    .researchProject img {
        max-height: 600px;
        max-width: 50%;
    }
}
@media only screen and (max-width: 600px) {
    .researchProject {
        width: 100%;
        display: flex;
        flex-direction: column;
        margin-bottom: 40px;
        justify-content: center;
        align-items: center;
    }
    .researchProjectText {
        display: flex;
        flex-direction: column;
        flex-grow: 1;
        flex-basis: 0;
        margin-left: 8px;
        margin-right: 8px;
    }
    .researchProjectRev {
        flex-direction: column-reverse;
    }

    .researchProjectText h4 {
        margin-top: 0px;
    }

    .researchProject img {
        margin-top: 15px;
        max-height: 400px;
        flex-grow: 1;
        flex-basis: 0;
    }
}
</style>
