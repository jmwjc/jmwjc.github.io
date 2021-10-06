`ris:Links`: [[❖ Elasticity]], [[❖ Curvilinear Coordinates]]
`ris:Calendar2`: <%+ tp.file.last_modified_date() %>
`ris:Bookmark`:

---
Firstly, we introduce the material coordinates $\bm{X}$, which is depicted the reference state, so $\bm{X}$ is also called referential coordinates. After a deformation, the physical space is prescribed by spatial coordinates $\bm{x}$, and the displacement can be expressed by $\bm{x}$ and $\bm{X}$:
$$
\bm{u} = \bm{x} - \bm{X}
$$
The conventional describing of motion is established by the magnitude squared of the distance between, as:
$$
\begin{aligned}
ds^2 &= d\bm{x} \cdot d\bm{x} - d\bm{X} \cdot d\bm{X} \\
&= (x_{i,I}x_{i,J} - \delta_{IJ}) dX_I dX_J \\
&= 2E_{IJ} dX_I dX_J \\
&= d\bm{X} \cdot 2\bm{E} \cdot d\bm{X}
\end{aligned}
$$
where $\delta_{ij}$ is Kronecker delta, $\bm{E}$ is called the Green's deformation tensor:
$$
\begin{aligned}
E_{IJ} &= \frac{1}{2}(x_{i,I}x_{i,J} - \delta_{IJ}) \\
&= \frac{1}{2}((u_{i,I} + \delta_{iI})(u_{i,J} + \delta_{iJ}) - \delta_{IJ})\\
&= \frac{1}{2}(u_{I,J} + u_{J,I} + u_{i,I} u_{i,J})
\end{aligned}
$$
For the infinitesimal deformation theory, the high order term is neglected. And the material and spatial coordinates are assumed as the same:
$$
\varepsilon_{ij} = \frac{1}{2}(u_{i,j} + u_{j,i})
$$
Because the strain tensor are all symmetric, second order tensors. In order to be flexible for describing material, the strain tensor are expressed as a matrix form, and the strain invariants are listed as:
$$
\begin{aligned}
I_{1} &= \mathrm{tr}(\bm{\varepsilon}) = \varepsilon_{ii} \\
I_{2} &= \frac{1}{2} (\varepsilon_{ii} \varepsilon_{jj} - \varepsilon_{ij} \varepsilon_{ji}) \\
I_{3} &= \epsilon_{ijk} \varepsilon_{1i} \varepsilon_{2j} \varepsilon_{3k} \end{aligned} 
$$
where $\epsilon_{ijk}$ is the levi-Civita symbol.
