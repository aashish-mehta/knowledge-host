>[!info]
>These are the results from the [[NeoVAD Mesh Convergence Study]]

Simulations were run on the four meshes to be investigated, and it was found that pressure increase varied by less than 4% for all meshes.

![[neovad-mesh-convergence-results.png|center|desc]] The results of the mesh convergence study indicating the relationship between final pressure increase and number of elements.

There was a general downward trend as the number of elements increased, but there was no clear convergence. The first element offset method provided similar results to the proportional method for a lower number of elements.

The proportional method had near-wall expansion rates that were outside of the recommended bounds for both the [[impeller]] and the [[diffuser]], but all other mesh statistics were acceptable. None of the first element offset meshes had unacceptable near-wall expansion rates, but all had a maximum element volume ratio that was too high for the impeller mesh. However, this was limited to <1% of the cells for two most refined meshes.

Due to the computational limitations of the project, the mesh with the highest number of elements was deemed unfeasible as each simulation took significantly longer to run.

Therefore, **mesh 3** (300,780 elements using the first element offset method) was chosen as a compromise between accuracy and size. 

A visual inspection of the mesh and observation of the mesh quality statistics revealed no major issues. It was found that 0.7% of elements had a maximum element volume ratio above the recommended value suggested by Ansys. This decreased as the number of elements increased, however, it was deemed a suitable level of error. It may have been caused by the inflation layer at the blade boundaries, where the mesh increased in size from a refined mesh at the boundary to a coarser mesh near the bulk flow. This is done to capture the near-wall interaction in more detail.

All other mesh measures fell within the acceptable bounds.

![[neovad-chosen-impeller-diffuser.png|center|desc]] The chosen impeller (left) and diffuser (right) meshes in [[TurboGrid]].
![[neovad-impeller-mesh-crossection.png|center|desc]]A cross-sectional view of the impeller mesh (left) and the boundary layer zoomed in (right).


To gain more insight into appropriate mesh sizes and methods, further simulations with a higher number of elements must be run. Additionally, more experiments with the proportional boundary layer method, and with different first element offset sizes could be run for a more thorough comparison.

However, the error caused by a coarse mesh may not be significant compared with the simplifications made to the geometry, and other discrepancies with the experiments.