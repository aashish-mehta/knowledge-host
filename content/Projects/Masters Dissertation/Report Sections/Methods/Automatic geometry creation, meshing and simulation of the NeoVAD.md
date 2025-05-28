---
aliases:
  - NeoVAD Automated Simulation
tags:
  - add-code
---
The initial [[impeller]] and [[diffuser]] geometries were generated manually using [[Ansys BladeGen]] and exported as batch files (.bgi) containing all the model information.

This included the curve profile and details of the meridional plane which defined the blade size (radii and lengths). Any required change to the geometry could be done by modifying the .bgi file, therefore, this was used as the core template.

Two MATLAB functions were written to recreate all the necessary information for the .bgi files using the [[NeoVAD Blade Profile Definition#Blade profile equations|blade profile equations]]. The inputs included the five [[Blade Parameters]] to be varied. The functions created a total of 20 CSV files containing the required geometric information.

A template for a Workbench script file (.wbjn) was also generated with the following steps:

1. Change the impeller length parameter (L1)
2. Change the diffuser length parameter (L2)
3. Update the impeller BladeGen cell
4. Update the diffuser BladeGen cell
5. Update the results cell*
6. Export the results to a CSV file

\*updating the results cell also updates the meshes and runs a simulation.

This script could be run by Ansys Workbench through the user interface or the command line.

A set of scripts were written in Python which looped through each line in the file containing the parameters defined by the [[Design of Experiments|DoE]]. It then ran the MATLAB functions which generated the blade geometry information.

The data from each of the CSV files were inserted into their relevant position in the .bgi files. Finally, the Workbench script file was updated with the new impeller/diffuser length parameters. The script created a folder for each experiment containing the two updated .bgi and .wbjn files.

A final script was written in PowerShell which accessed the Ansys BladeGen and Workbench APIs to run the scripts. The script looped over the folders and used the BladeBatch command to convert the .bgi files into native BladeGen files which replaced the existing model. The RunWB2 command was then used to run the Workbench script.

The exported results were combined into a single CSV file with the corresponding parameters.