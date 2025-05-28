---
tags:
  - fluid-mechanics
  - equation
  - engineering
---
Bernoulli's Equation is a fundamental principle in fluid mechanics that describes the conservation of energy along a streamline for an ideal fluid. 

It states that the total mechanical energy per unit volume remains constant in steady, incompressible, inviscid flow.

## Equations

### Basic Form
$$P + \frac{1}{2}\rho v^2 + \rho gh = \text{constant}$$

Where:
- **P** = Static pressure
- **ρ** = Fluid density  
- **v** = Flow velocity
- **g** = Gravitational acceleration
- **h** = Elevation head

### Per unit mass (specific energy)
$$\frac{P}{\rho} + \frac{v^2}{2} + gh = \text{constant}$$

### Head form (per unit weight)
$$\frac{P}{\rho g} + \frac{v^2}{2g} + h = H_{\text{total}}$$

Where:
- - **H** = Total head

### With Energy Losses
$$\frac{P_1}{\rho g} + \frac{v_1^2}{2g} + h_1 = \frac{P_2}{\rho g} + \frac{v_2^2}{2g} + h_2 + h_L$$

Where $h_L$ = head loss due to [[Friction]] and minor losses

### With Energy Addition
$$\frac{P_1}{\rho g} + \frac{v_1^2}{2g} + h_1 + h_{\text{pump}} = \frac{P_2}{\rho g} + \frac{v_2^2}{2g} + h_2 + h_L$$

Where $h_{pump}$ = head added by [[Pump]]
## Energy Components

### Static Pressure Energy
- **P/ρ**: Pressure energy per unit mass
- Energy due to fluid pressure at a point
- Can do work by pushing against surfaces

### Kinetic Energy  
- **v²/2**: Kinetic energy per unit mass
- Energy due to fluid motion
- Increases with velocity squared

### Potential Energy
- **gh**: Gravitational potential energy per unit mass
- Energy due to elevation above reference level
- Constant for horizontal flow

## Assumptions & Limitations

### Valid When:
- **Steady flow**: No time-dependent changes
- **Incompressible fluid**: Constant density (ρ)
- **Inviscid flow**: No viscous losses
- **No energy addition/removal**: No pumps, turbines, or heat transfer
- **Along a streamline**: Energy balance applies to same fluid particle

### Invalid When:
- High-speed compressible flow (Mach > 0.3)
- Significant viscous effects ([[Viscosity]])
- Unsteady flow conditions
- Energy input/output devices present
- Across streamlines in rotational flow

---
## Related
- [[Navier-Stokes Equations]]
