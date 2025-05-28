The [[NeoVAD Master's Dissertation|project]] aimed to determine the optimum [[impeller]] and [[diffuser]] blade geometries for a novel heart pump, the [[NeoVAD]], to match the physiological [[Heart Pump Operating Conditions|operating conditions]] of a paediatric patient. 

The five [[blade parameters]] varied were impeller inlet angle (β1), impeller outlet angle (β2), diffuser inlet angle (α2), impeller length (L1), and diffuser length (L2). 

Furthermore, an [[Automatic geometry creation, meshing and simulation of the NeoVAD|automated simulation framework]] was generated to aid the optimisation.

To do this, an initial model was generated in [[Ansys BladeGen]] using blade angles obtained from mean-line theory with a simple [[haemolysis index model]] implemented. A [[NeoVAD Mesh Convergence Study|mesh convergence stufy]] was run to obtain the optimum mesh, and a sensitivity analysis was run to gauge the effects of each parameter on the solution. A [[Design of Experiments]] (DoE) was generated accordingly.

The automated framework was created using a combination of MATLAB, Python and PowerShell scripts and functions, and covered the work of generating geometries and running simulations for all experiments. A [[Generalized Regression Neural Network]] (GRNN) was trained and analysed using the experimental data, and a [[genetic algorithm]] was used to determine an estimate for the optimum geometry.

The blade angles obtained from [[mean-line theory]] and the initial guesses for L1 and L2 resulted in a simulation with an error of 0.5% compared with the expected value. The sensitivity analysis revealed that the impeller outlet angle (β2) caused the biggest change in pressure increase. The automated workflow was created successfully and required little to no manual interaction. The GRNN was generated with an error of 5.5% when validated with the training data, but the optimised geometry suggested by the genetic algorithm had an error of 25% compared with the expected value. It was suspected that the range of inputs was too high given the limited dataset. A brief investigation of the [[haemolysis]] index revealed that it was highest at the tip of the diffuser blades. The optimum geometry was taken to be the one determined from mean-line theory.

Overall, the generation of a workflow to generate the NeoVAD impeller and diffuser geometries, and perform multiple simulations was successful. Furthermore, the framework for the machine learning optimisation was created, but the implementation needed improvement. The parameter input range and correspondingly low number of simulations were the likely cause of the error.

---
[[NeoVAD Master's Dissertation|Master's Dissertation]] | [[Summary]] | [[Aims and Objectives]] | [[Background]] | [[Literature Review]] | [[Methods]] | [[Results and Discussion]] | [[Conclusions]] | [[References]] 