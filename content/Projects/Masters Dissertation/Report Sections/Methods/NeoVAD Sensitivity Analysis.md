
>[!info]
>See [[NeoVAD Sensitivity Analysis Results]] for the results of this study

A [[sensitivity analysis]] was conducted to determine the effect of the five [[blade parameters]] for a simulation of the [[NeoVAD]].

The [[Creating the initial model#Impeller and diffuser blade models|initial blade parameters]] found from theory were used as a control experiment. Each parameter was varied by a factor of two relative to the control.

| **Experiment number** | **β1 (degrees)** | **β2 (degrees)** | **α2 (degrees)** | **L1 (mm)** | **L2 (mm)** |
| --------------------- | ---------------- | ---------------- | ---------------- | ----------- | ----------- |
| **Control**           | 7.5              | 46.7             | 8.5              | 8           | 8.5         |
| **1**                 | _**15**_         | 46.7             | 8.5              | 8           | 8.5         |
| **2**                 | 7.5              | _**23.35**_      | 8.5              | 8           | 8.5         |
| **3**                 | 7.5              | 46.7             | _**17**_         | 8           | 8.5         |
| **4**                 | 7.5              | 46.7             | 8.5              | _**16**_    | 8.5         |
| **5**                 | 7.5              | 46.7             | 8.5              | 8           | _**17**_    |

The resultant pressure increase for each of the experiments was compared with both the control experiment and the expected [[pressure head]].

The upper and lower bounds and the required refinement for each parameter were determined based on their effects on the pressure increase. Parameters that caused the biggest changes were refined more by adding more levels, meaning more values for that parameter were tested.

Conversely, parameters that caused little change had a lower level of refinement. The bounds of each parameter were determined by how close each experiment was to the required pressure. If any experiment was close, the bounds encompassed the values used for it.

Experiments that caused a significant change in pressure were investigated further in [[Computational Fluid Dynamics|CFD]] post, and the results were analysed and justified.

This was used to generate the [[Design of Experiments]], which was created in MATLAB using the [[D-optimal]] method. The parameters were then exported as a CSV file, which could be read by other programs.