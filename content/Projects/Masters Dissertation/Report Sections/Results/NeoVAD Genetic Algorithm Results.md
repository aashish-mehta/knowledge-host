> [!info]
> These are the results from [[Finding optimal NeoVAD geometries using a Genetic Algorithm]]


Using the [[NeoVAD GRNN Results|trained GRNN]] with the full dataset and a spread of 0.5, the [[genetic algorithm]] was run, and a parameter estimate with an error below the tolerance was outputted.
 
|**Parameter**|**Value**|
|---|---|
|**β1 (degrees)**|4.0|
|**β2 (degrees)**|40.0|
|**α2 (degrees)**|24.2|
|**L1 (mm)**|15.3|
|**L2 (mm)**|18.0|

This was simulated using [[Computational Fluid Dynamics|CFD]].

The maximum wrap angle for the impeller with these parameters was 719 degrees. This is because of the steep inlet angle and relatively long inlet length, which forced a large wrap angle gradient (see [[NeoVAD Blade Profile Definition#Wrap angles]]).

![[neovad-ga-selected-model.png|center|desc]]The impeller (left) and diffuser (right) geometries for the parameters determined by the genetic algorithm.

The [[Pressure Head|pressure increase]] for the geometry was simulated to be 75 mmHg, which had a significant error of 25% compared with the expected pressure increase.

The reason for this inaccuracy is likely the large range of input parameters from the [[NeoVAD Sensitivity Analysis Results]] . The GRNN was 95% accurate when comparing a known set of inputs to expected outputs. However, the genetic algorithm works by selecting random input parameters to match an expected output. 

There may have been many inputs that provided the required pressure head according to the GRNN which include both accurate and inaccurate solutions. The genetic algorithm may have converged on one of the inaccurate solutions. Validating the training data was not sufficient to prevent this, as it only tested a limited number of inputs. 

This could be mitigated by obtaining a larger dataset and limiting the input range.

Additionally, other variables which may improve the effectiveness of the genetic algorithm were not investigated. These include the [[Elite Count]], and the [[Crossover Fraction]] ([[References#58]]).

Refining these values may have resulted in a more robust genetic algorithm.

The [[Creating the initial model|initial model's]] blade angles retrieved for [[impeller]] and [[diffuser]] lengths were sufficiently accurate, so were taken as the optimum geometries. Therefore, the [[NeoVAD Initial Simulation Results]] was also relevant for the final geometry. 

All further analysis also used these values.

> [!note]
> This would not be feasible if the geometry were to be optimised for multiple [[Flow Rate|flow rates]] and [[Pressure Head|pressure heads]], so the optimisation method must be improved.

| **β1 (degrees)** | **β2 (degrees)** | **α2 (degrees)** | **L1 (mm)** | **L2 (mm)** |
| ---------------- | ---------------- | ---------------- | ----------- | ----------- |
| **7.5**          | 46.7             | 8.5              | 8           | 8.5         |
