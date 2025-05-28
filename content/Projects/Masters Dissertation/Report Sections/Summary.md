The goal of the project was to optimise the [[Impeller]] and [[Diffuser]] for a novel [[Left Ventricular Assist Device]] (the [[NeoVAD]]) for paediatric patients.

To aid this, an automated framework was generated to create a new geometry, update the mesh, and run a simulation for multiple experiments.

An initial model was created using values obtained from [[mean-line theory]], and a [[Design of Experiments]] (DoE) was generated using the[[ D-optimal]] method.

Steady-state simulations were run using the [[Frozen Rotor]] method, and the [[Pressure Head|pressure head]] results from each experiment were fed into a [[Generalized Regression Neural Network]] (GRNN). This was used within the [[NSGA-II]] [[Genetic Algorithm]] to determine the optimum [[Blade Parameters|blade parameters]] based on the required pressure increase.

The initial simulation run using blade angles determined from theory had an error of 0.5% compared with the expected value. A total of eighty simulations were run as part of the DoE through the automated framework, 5% of which did not mesh successfully. The GRNN was generated with a spread of 0.5, and an error of 5.5% when validated using the training data. 

However, the simulated pressure increase using the parameters determined by the genetic algorithm had an error of 25% compared with the expected value. The likely cause of this was a poorly refined DoE with input ranges that were too wide, and the limited dataset. The automated workflow was created successfully and provided a significant boost in efficiency, doubling the number of simulations run per day. The framework for the optimisation process was generated and verified. A brief investigation into a numerical model to calculate blood [[Haemolysis]] was conducted.

---
[[NeoVAD Masters Dissertation|Master's Dissertation]] | [[Summary]] | [[Aims and Objectives]] | [[Background]] | [[Literature Review]] | [[Methods]] | [[Results and Discussion]] | [[Conclusions]] | [[References]] 