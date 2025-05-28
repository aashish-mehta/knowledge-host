---
tags:
  - equation
  - biology
  - engineering
---
A power-law model used to estimate blood damage from shear stress.
## Equations

### Power-Law Haemolysis model
$$HI \left(\%\right) = C \tau_s^\alpha t_{exp}^\beta$$
Where:
- `HI` is the Haemolysis Index
- $\tau_s$ is the local [[Shear Stress]]
- $t_{exp}$ is the exposure time of the red blood cells to the local shear stress
-  α, β, and C are empirical constants

*For the [[NeoVAD Master's Dissertation|NeoVAD Master's Dissertation]], C = 3.62e-5, α = 0.785, β = 2.416 from literature [[References#53]]*

### Eulerian form

This can be linearised and used as a [[Transport Equation]].

$$\frac{∂H {I} ^ {'}}  {∂t}  + v ∙ ∇H {I} ^ {'} =S$$
Where:
- $HI' = [HI]^{1/\beta}$
- $S = (C\tau_s^\alpha)^{1/\beta}$
- $v$ is the blood velocity

From this, the Haemolysis index can be calculated as $HI = [HI’]^\beta$.