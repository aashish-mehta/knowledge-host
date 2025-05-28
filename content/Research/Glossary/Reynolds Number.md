---
tags:
  - fluid-mechanics
  - engineering
  - glossary
---
## Definition
The **Reynolds number** is a dimensionless parameter that characterizes the flow regime in fluid mechanics. It represents the ratio of inertial forces to viscous forces.

## Mathematical Expression
$$Re = \frac{\rho v L}{\mu} = \frac{v L}{\nu}$$

Where:
- **ρ** = fluid density
- **v** = characteristic velocity
- **L** = characteristic length
- **μ** = dynamic [[Viscosity]]
- **ν** = kinematic viscosity (μ/ρ)

## Notes

- **High Re**: Inertial forces dominate → **Turbulent flow**
- **Low Re**: Viscous forces dominate → **Laminar flow**
- **Transition region**: Mixed characteristics

### Flow Regimes

#### Pipe Flow
- **Re < 2300**: Laminar flow
- **2300 < Re < 4000**: Transition zone
- **Re > 4000**: Turbulent flow

#### Flow Over Flat Plate
- **Re < 500,000**: Laminar boundary layer
- **Re > 500,000**: Turbulent boundary layer

#### Flow Around Sphere
- **Re < 1**: Stokes flow (creeping flow)
- **Re > 1000**: Turbulent wake formation

### Characteristic Lengths

#### Pipe Flow
- **L = D** (pipe diameter)
- **Re = ρvD/μ**

#### External Flow
- **L = plate length** or **object diameter**
- Context-dependent definition

## Related
- [[Navier-Stokes Equations]]
- [[Turbulence]]
