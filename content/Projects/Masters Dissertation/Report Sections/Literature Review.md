---
tags: []
aliases:
  - Lit Review
---
A review of available literature and tools to decide what would be used in the [[NeoVAD Master's Dissertation|NeoVAD Master's Dissertation]].

## Summary
- [[Computational Fluid Dynamics]] was used for simulations, and [[Ansys CFX]] was chosen to solve the [[Navier-Stokes Equations]].
- The [[k-omega SST Model|k-ω SST]] model was chosen to model turbulence.
- The [[Frozen Rotor]] method was chosen to model the rotational interface between the [[Impeller]] and the [[Diffuser]].
- A [[D-optimal]] [[Design of Experiments]] approach was selected to determine the values of the [[Blade Parameters]] to simulate.
- The [[NSGA-II]] [[Genetic Algorithm]] was chosen for optimal blade geometry selection.
- It was decided to create a custom automated workflow for simulating geometries using [[Ansys BladeGen]]. 

## Computational Fluid Dynamics Review

This project will use [[Computational Fluid Dynamics|CFD]] to model blood flow through the pump, reducing the number of physical experiments required. 

The key equations to solve are the governing [[Navier-Stokes Equations]].

[[Ansys CFX]] was used to solve the equations.

### Turbulence modelling

Blood flow through a pump is likely to be [[Turbulence|turbulent]], so two turbulence models were explored:
- [[k-epsilon Model|k-ε]] 
- [[k-omega SST Model|k-ω SST]]

k-ω SST provides reasonable accuracy and is better suited for boundary layer analysis than the pure k-ε model.

An investigation of various turbulence models compared with experimental data for a clinical [[Ventricular Assist Device|VAD]] showed that the k-ε and Reynolds Stress models were the most accurate ([[References#30]]). However, the analysis was performed on a [[Centrifugal Pump]] with an [[Impeller]] radius over five times the size of the [[NeoVAD]] impeller. Furthermore, the Reynolds Stress model is computationally expensive and was not feasible given the timescale of the project.

Due to the small size of the model, the effect of the boundary layer on the simulation result may be significant. Therefore, the k-ω SST turbulence model was chosen.

### Interface model

The interface between the [[Impeller]] and [[Diffuser]] can be complex, and the interaction between the two must be modelled. Two models were explored:
- [[Frozen Rotor]]
- [[Sliding Mesh]]

The frozen-rotor method matched experimental data well in cases that were directly relevant to the [[NeoVAD]] (an axial blood pump) ([[References#19]]). However, this method assumes that the flow is steady-state, and will not account for any transient variations of the impeller blades ([[References#32]]).

The sliding mesh method, had a similar level of accuracy to the frozen-rotor method but required significantly more computational time ([[References#19]]). 

**The frozen-rotor method was used to model the rotational interface.**

## Design of Experiments Review

There were five [[Blade Parameters]] to be investigated, each of which can be constrained between two values (a minimum and a maximum). 

A [[Design of Experiments]] can provide a representative set of parameters combinations to reduce the total number of simulations. Two strategies were explored:
- [[Central Composite]]
- [[D-optimal]]

**D-Optimal was chosen** due to the resource constraints of the project.

## Machine Learning Review
### Predictive model

The [[Design of Experiments]] and [[Computational Fluid Dynamics|CFD]] analysis can be used to train a [[Machine Learning]] model. A trained model can give an insight to the relationship of the [[Blade Parameters]] to the flow properties, reducing the need for expensive simulations.

Three predictive models were explored
- [[Generalized Regression Neural Network]] 
- [[Levenberg-Marquardt]]
- [[Learning Vector Quantization]]

Of the three, GRNN was chosen for its lower average error, and the proven success of similar feed-forward neural network systems against CFD simulations ([[References#38]], [[References#41]]).

### Genetic Algorithm

Given a predictive model, a Multi-objective [[Genetic Algorithm]] (MOGA) can be used to determine the final, optimal [[NeoVAD]] [[Blade Parameters]].

Two algorithms were compared:
- [[NSGA-II]]
- [[SPEA2DSE]]

An investigation of two deduced that NSGA-II  was able to find a better spread of solutions and better convergence towards to [[Pareto Optimality|Pareto Optimal]] solution ([[References#48]]). Furthermore, a comparison between the two methods for the relevant case of optimisation using CFD revealed that NSGA-II produced better designs ([[References#49]]). Therefore, **the NSGA-II algorithm was chosen as the more accurate and viable option.**
## Automated Workflow Review

There will be many parameter combinations produced by the [[Design of Experiments]], so an investigation was conducted into automation capabilities to reduce the burden of simulating them all.

Three options were considered:
- No automated workflow (manually run simulations)
- A commercial software: [[Simcenter HEEDS]]
- [[Ansys Design Modeller]]
- [[Ansys BladeGen]]

Manually created solutions are safe, but costly in the long term, and not scalable. Given the academic nature of the project, a new commercial project would not have been feasible, and interfacing it with existing technology may prove challenging. Design modeller was an older, inflexible solution, so Ansys BladeGen was selected as the geometry creation tool. A custom pipeline would be created to support automation.

---
[[NeoVAD Master's Dissertation|Master's Dissertation]] | [[Summary]] | [[Aims and Objectives]] | [[Background]] | [[Literature Review]] | [[Methods]] | [[Results and Discussion]] | [[Conclusions]] | [[References]] 