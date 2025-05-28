---
tags:
  - add-code
---
>[!info]
>See [[NeoVAD GRNN Results]]

From the [[Automatic geometry creation, meshing and simulation of the NeoVAD|NeoVAD Automated Simulations]], a [[Generalized Regression Neural Network]] was created.

A script was written in MATLAB to generate a [[neural network]] with the five [[blade parameters]] as inputs and the [[Pressure Head|pressure increase]] as the output. The parameters from the DoE and the simulation results were loaded into MATLAB and normalised (between 0 and 1), and 90% of the data was used to train the neural network. 

A mapping scheme relating the raw parameters to the normalised ones was generated. The only other input required to generate the GRNN was the ‘spread’. A large spread value results in a smoother approximation ([[References#55]]). Analysis was conducted on the effect of the spread on the model result, and a suitable value was subsequently chosen.

The remaining 10% was used to calculate the error of the model. This was calculated by taking the average absolute error between the neural network output and the simulation result. The trained network was saved in a .mat file along with a variable defining the expected pressure increase, and the mapping scheme. The mapping scheme would be required to convert the GRNN output back into the raw pressure increase.