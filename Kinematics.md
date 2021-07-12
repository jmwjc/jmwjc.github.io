## Kinematics
Firstly, we introduce the material coordinates $\boldsymbol{X}$, which is depicted the reference state, so $\boldsymbol{X}$ is also called referential coordinates. After a deformation, the physical space is prescribed by spatial coordinates $\boldsymbol{x}$, and the displacement can be expressed by $\boldsymbol{x}$ and $\boldsymbol{X}$:
$$
\boldsymbol{u} = \boldsymbol{x} - \boldsymbol{X}
$$
The conventional describing of motion is established by the magnitude squared of the distance between, as:
$$
\begin{split}
d\boldsymbol{x} \cdot d\boldsymbol{x} - d\boldsymbol{X} \cdot d\boldsymbol{X} &= (x_{i,I}x_{i,J} - \delta_{IJ}) dX_I dX_J \\
&= 2E_{IJ} dX_I dX_J \\
&= d\boldsymbol{X} \cdot 2\boldsymbol{E} \cdot d\boldsymbol{X}
\end{split}
$$
where $\delta_{ij}$ is Kronecker delta, $\boldsymbol{E}$ is called the Green's deformation tensor:
$$
\begin{split}
E_{IJ} &= \frac{1}{2}(x_{i,I}x_{i,J} - \delta_{IJ}) \\
&= \frac{1}{2}((u_{i,I} + \delta_{iI})(u_{i,J} + \delta_{iJ}) - \delta_{IJ})\\
&= \frac{1}{2}(u_{I,J} + u_{J,I} + u_{i,I} u_{i,J})
\end{split}
$$
For the infinitesimal deformation theory, the high order term is neglected. And the material and spatial coordinates are assumed as the same:
$$
\varepsilon_{ij} = \frac{1}{2}(u_{i,j} + u_{j,i})
$$
Because the strain tensor are all symmetric, second order tensors. In order to be flexible for describing material, the strain tensor are expressed as a matrix form, and the strain invariants are listed as:
$$
\begin{split}
I_{1} &= \mathrm{tr}(\boldsymbol{\varepsilon}) = \varepsilon_{ii} \\
I_{2} &= \frac{1}{2} (\varepsilon_{ii} \varepsilon_{jj} - \varepsilon_{ij} \varepsilon_{ji}) \\
I_{3} &= \epsilon_{ijk} \varepsilon_{1i} \varepsilon_{2j} \varepsilon_{3k} \end{split} 
$$
where $\epsilon_{ijk}$ is the levi-Civita symbol.
## Hookean and non-hookean material
The material properties are developed by strain energy density $W(I_1,I_2,I_3)$, and the stress are defined as:
$$
\sigma_{ij} = \frac{\partial W}{\partial \varepsilon_{ij}}
$$
For the Hooke's law, the strain energy density is defined by:
$$
W = \frac{1}{2} C_{ijkl} \varepsilon_{ij} \varepsilon_{kl}
$$
where $C_{ijkl}$ is the fourth order elasticity tenor:
$$
C_{ijkl} = \lambda \delta_{ij} \delta_{kl} + \mu(\delta_{ik}\delta_{jl} + \delta_{il}\delta_{jk})
$$
in which $\lambda, \mu$ are Lamé constants:
$$
\begin{equation}
\lambda = \frac{E\nu}{(1+\nu)(1-2\nu)}, \quad \mu = \frac{E}{2(1+\nu)}
\end{equation}
$$