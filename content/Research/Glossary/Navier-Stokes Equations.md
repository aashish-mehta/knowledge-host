---
tags:
  - equation
  - fluid-mechanics
  - engineering
---
The **Navier-Stokes equations** describe the motion of viscous fluids. They represent conservation of momentum for a fluid element, accounting for [[pressure]] forces, viscous forces, and body forces.

## Equations

$$\frac{\partial \rho u_k}{\partial x} +  \nabla ∙ (\rho \space u \space u_k - \mu \space \nabla  u_k) = \frac{-\partial p}{\partial x_s} + F_k$$
Where:
- $\rho$ = fluid density
- $u_k$ = quantity of interest
- $v$ = [[velocity]] vector
- $p$ = pressure
- $μ$ = dynamic viscosity
- $F_k$ = sources

### Vector Form
$$\rho \frac{D\vec{v}}{Dt} = -\nabla p + \mu \nabla^2 \vec{v} + \rho \vec{g}$$

### Component Form (x-direction)
$$\rho \left(\frac{\partial u}{\partial t} + u\frac{\partial u}{\partial x} + v\frac{\partial u}{\partial y} + w\frac{\partial u}{\partial z}\right) = -\frac{\partial p}{\partial x} + \mu \left(\frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} + \frac{\partial^2 u}{\partial z^2}\right) + \rho g_x$$

## Notes

 **Left Side (Acceleration)**:
- **∂v/∂t**: Local acceleration (unsteady flow)
- **v·∇v**: Convective acceleration (velocity changes with position)

**Right Side (Forces per unit volume)**:
- **-∇p**: Pressure force
- **μ∇²v**: Viscous force
- **ρg**: Body force (gravity)

Navier-Stokes reduces to [[Bernoulli's Equation]] when viscous terms are negligible.

Navier-Stokes must be solved simultaneously with the [[Continuity Equation]]. Together, they form a complete system for velocity and pressure.

For Steady State flows, **∂v/∂t = 0**.

**Low [[Reynolds Number]] (Stokes Flow)**:
- Neglect convective terms: **v·∇v ≈ 0**
- Linear equations, easier to solve
- Valid for very viscous or very slow flows

**High Reynolds Number**:
- Viscous effects confined to boundary layers
- Can use inviscid flow theory in core regio
## Related
- [[Reynolds Number]]
- [[Bernoulli's Equation]]
- [[Continuity Equation]]