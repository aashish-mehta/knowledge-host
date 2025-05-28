The principle aim of this project was to optimise the primary [[Impeller]] and [[Diffuser]] of the [[NeoVAD]] to improve [[Haemodynamic]] performance at the [[Heart Pump Operating Conditions|operating conditions]]. 

For this project, optimisation for a 10 kg patient was targeted.

A secondary aim of the project was to create an automated workflow to make the optimisation process more efficient. This allowed the computational resources to be used at full capacity and with minimal manual interaction. It is also directly beneficial for future work conducted on blade optimisation. 

Five parameters were selected to be optimised: 
1.  [[Blade Parameters#Impeller inlet angle (β1)]]
2.  [[Blade Parameters#Impeller outlet angle (β2)]]
3.  [[Blade Parameters#Diffuser inlet angle (α2)]]
4.  [[Blade Parameters#Impeller length (L1)]]
5.  [[Blade Parameters#Diffuser length (L2)]]

Note that the  [[Blade Parameters#Diffuser outlet angle]] was fixed to be zero.

Project Objectives: 

- Generate a model of the pump impeller and diffuser 
- Simulate the model under the relevant flow conditions
- Use a [[Design of Experiments]] (DoE) to determine parameter variations
- Create methods to automate geometry creation, meshing, and simulation
- Use [[Machine Learning]] to train a prediction model to facilitate optimisation
- Use a [[Genetic Algorithm]] as the optimisation method to determine the final geometry
- Implement a [[Haemolysis Index Model]].

---
[[NeoVAD Masters Dissertation|Master's Dissertation]] | [[Summary]] | [[Aims and Objectives]] | [[Background]] | [[Literature Review]] | [[Methods]] | [[Results and Discussion]] | [[Conclusions]] | [[References]] 