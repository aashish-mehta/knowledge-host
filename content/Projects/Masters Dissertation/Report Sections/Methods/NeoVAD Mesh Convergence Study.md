---
tags: []
---
>[!info]
>See [[NeoVAD Mesh Convergence Results]] for the results of this study


This is a [[mesh convergence study]] for the modelled geometries in the [[NeoVAD]] (as defined in [[Creating the initial model]]).
## Inlet and outlet meshes

The meshes for the inlet and outlet domains were less than 5% the size of the [[impeller]] and [[diffuser]] meshes and involved no significant flow interactions. Therefore, the default meshes were deemed appropriate.

![[neovad-inlet-outlet-meshes.png|center|desc]] The inlet (left) and outlet (right) meshes.


## Impeller and diffuser meshes

The size and quality of the impeller and diffuser meshes were investigated.

Four meshes were investigated in total; one with the boundary layer refinement method as ‘Proportional to mesh size’, and three with the method based on a first element offset. The offset size was set to 0.69 mm for the impeller and 0.49 mm for the diffuser.

| **Mesh number** | **Boundary layer refinement method** | **Number of elements** |
| --------------- | ------------------------------------ | ---------------------- |
| **1**           | Proportional to mesh size            | 427,181                |
| **2**           | First element offset                 | 108,415                |
| **3**           | First element offset                 | 300,780                |
| **4**           | First element offset                 | 978,612                |

The pressure increase was monitored for each mesh and plotted against the number of elements. The following mesh statistics were recorded in each domain:

- Minimum and maximum face angles
- Maximum element volume ratio
- Minimum volume
- Maximum edge length ratio
- Maximum connectivity number
- Near-wall expansion rates

Each of these measures was monitored, and the percentage of mesh cells that had a value outside of the recommended bounds (according to [[Ansys CFX]]) was noted.

A mesh size that provided a suitable compromise between accuracy and computational resources was selected.