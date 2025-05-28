---
tags:
  - add-code
---

To support the [[Automatic geometry creation, meshing and simulation of the NeoVAD]], several functions must be created to generate a blade profile.

## Blade profile equations

The [[Design of Experiments|DoE]] provides five [[blade parameters]]. To create the geometry in Ansys, a more defined blade profile is required with angles specified along the blade length. 

Two MATLAB functions were written to create a curve defining the relationship between blade angle, _β_, and the distance along the blade, _M_.

The fit was exponential for the [[impeller]]:

$$β = {- e} ^ {- (aM+b)} + {f*β}_{2}$$
Where:
- $f$ is a factor of accuracy (set to 0.99)
- $b=-ln(f*\beta_2 - \beta_1$)
- $a= \frac{-ln  {((f-1) * {β}_{2} ) +b} } {{L}_{1}}$

And quadratic for the [[diffuser]]:
$$β = a * {(M- {L}_{2} )} ^ {2}$$
Where:
- $a=\frac{{β}_{1}}{{X2} ^ {2}}$

## Wrap angles

The wrap angle, _θ_, defines the blade’s revolution around the hub. This was monitored to ensure the blade did not make an excessive number of revolutions using the relationship between _θ, β_ and _M_ ([[References#54]]).

$$\tan {(\beta)} = r * \frac{\delta \theta}{δM}$$
Where:
- $r$ is the mean radius

The angles were modified to align with the definition set in [[Ansys BladeGen]] compared with the definition used in the theory.

For the impeller:
$${\beta} ^ {\prime} = -(90- \beta)$$

For the diffuser:
$${\beta} ^ {\prime} = (90- \beta)$$
Where:
- $\beta^\prime$ is the angle input into BladeGen.
- $\beta$ is the angle defined by theory.

The inputs to the functions were the blade inlet and outlet angles, lengths, and the number of points used for fitting (which was 30 throughout the project).