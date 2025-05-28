---
tags: []
aliases:
  - Neural Network Training
  - Optimisation Pipeline
---
### Phase 1: GRNN Training

- Trained on 90% of DoE simulation data
- Normalised parameters (0 to 1)
- Chose spread value for balance of error vs smoothness
- Trained [[Generalized Regression Neural Network]]
- Output: pressure increase

### Phase 2: Genetic Algorithm

- Fitness function defined as difference from target pressure
- Implemented modified [[NSGA-II]] in MATLAB
- Searched for blade parameters that matched required head
- Final solution verified via full CFD Setup simulation
