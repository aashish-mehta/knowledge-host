---
tags:
  - fluid-mechanics
  - equation
  - engineering
---
The **continuity equation** expresses the conservation of mass in fluid flow. It states that mass cannot be created or destroyed within a flow field.

## Equations

### General Form
$$\frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \vec{v}) = 0$$
### Steady Flow
$$\nabla \cdot (\rho \vec{v}) = 0$$
### Incompressible Flow
$$\nabla \cdot \vec{v} = 0$$
### One-Dimensional Steady Flow
$$\rho_1 A_1 v_1 = \rho_2 A_2 v_2 = \dot{m}$$
Where:
- **ρ** = fluid density
- **v** = velocity vector
- **A** = cross-sectional area
- **ṁ** = mass flow rate
## Notes

- **Mass in = Mass out** for any control volume
- If area decreases → velocity increases (for constant density)
- If density changes → velocity adjusts to conserve mass
- **Assumes no mass sources or sinks**
- **Valid for all fluids** (compressible and incompressible)
- **Steady vs unsteady** forms depend on time dependence
- **Compressible effects** important at high speeds

## Related
- [[Navier-Stokes Equations]]
- [[Bernoulli's Equation]]