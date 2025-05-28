---
tags:
  - add-code
---
>[!info]
>See [[NeoVAD Genetic Algorithm Results]]


A [[fitness function]] was defined with the five [[blade parameters]] as input, and an error as the output.

The function used the [[Modelling the NeoVAD using a GRNN|trained neural network]] to estimate the pressure increase and calculated the absolute difference compared with the required pressure head.

A script was written in MATLAB to initialise a [[genetic algorithm]] with the fitness function, and the parameter bounds specified for the DoE.

This worked by using initial guesses of each parameter and inputting them to the objective function to determine how close they were. The guesses were altered, as per the genetic algorithm, and the solution eventually converged to a final guess with an error below the tolerance (1e-4). The genetic algorithm used was a slight modification to the [[NSGA-II]] algorithm and was run using the default settings. A final CFD simulation was run using these parameters, and the results were compared with the expected value.