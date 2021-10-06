# Generalized Reproducing Kernel Gradient Smoothing Integration

## Reviews of reproducing kernel smoothed gradient

The error of meshfree formulation will be limit by the orders of satisfying with consistency condition and integration constraint. For meshfree method with reproducing kernel approximation, the consistency condition is naturally fulfilled. However, due to the non-ploynomrial meshfree shape functions and their overlopping support, it is hard for meshfree shape functions to satisfy integration constraint. The $p$-th order integration constraint for second-order problems is listed as follow:

$$
\begin{equation}\label{IC}
\int_{\Omega} \Psi_{I,i} \boldsymbol{p}^{[p-1]}\mathrm{d}\Omega = 
\int_{\Gamma} \Psi_{I} \boldsymbol{p}^{[p-1]} n_{i}\mathrm{d}\Gamma - 
\int_{\Omega} \Psi_{I} \boldsymbol{p}_{,i}^{[p-1]}\mathrm{d}\Omega
\end{equation}
$$

where $\Psi_{I,i}$ is the derivative towarding $i$-th direction of shape function at node $\boldsymbol{x}_{I}$.  $\boldsymbol{p}^{[p-1]}$ is the monormial vector with order $(p-1)$. The subscript comma presents the partial differentiation with respect to $i$-th Cartesian coordinate. $\Omega$ and $\Gamma$ denote the problem domain and its boundary. The normal integration rule designed for polynormial integrands can not satisfy with the integration constraint, even for the linear one.

In the framework of reproducing kernel gradient smoothing (RKGS), the traditional gradients of meshfree shape functions are represented by the assumed smoothed gradients as:

$$
\begin{equation}\label{RKSG}
\tilde{\Psi}_{I,i}(\boldsymbol{x}) = \boldsymbol{p}^{[p-1]T}(\boldsymbol{x}) \boldsymbol{a}_{iI}
\end{equation}
$$

in which $\boldsymbol{a}_{iI}$ is a constant coefficient vector that can be got by substituting Eq. $\ref{RKSG}$ into Eq. $\ref{IC}$ as:

$$
\begin{equation}
\boldsymbol{a}_{iI} = \boldsymbol{G}^{-1}\boldsymbol{g}_{iI}
\end{equation}
$$

where $\boldsymbol{G}$ is moment matrix, and $\boldsymbol{g}_{iI}$ is the right hand side of integration constraint in Eq. $\ref{IC}$,

$$
\begin{equation}
\boldsymbol{G} = \int_{\Omega} \boldsymbol{p}^{[p-1]} \boldsymbol{p}^{[p-1]T} \mathrm{d}\Omega
\end{equation}
$$

$$
\begin{equation}\label{RKSG2}
\boldsymbol{g}_{iI} = 
\int_{\Gamma} \Psi_{I} \boldsymbol{p}^{[p-1]} n_{i}\mathrm{d}\Gamma - 
\int_{\Omega} \Psi_{I} \boldsymbol{p}_{,i}^{[p-1]}\mathrm{d}\Omega
\end{equation}
$$

Consequently, the smoothed gradient is evaluated by:

$$
\begin{equation}
\tilde{\Psi}_{I,i}(\boldsymbol{x}) = \boldsymbol{p}^{[p-1]T}(\boldsymbol{x}) \boldsymbol{G}^{-1} \boldsymbol{g}_{iI}
\end{equation}
$$

On the other hand, according to assumed strain methods[^Simo1986], the RK smoothed gradient is belong the assumed strain method. Next, we will verify that the RK smoothed gradient is variational recovered, which ensures the variantional consistency of RKGS. The orthogonal condition for variational gradient recovery is listed as follow:

$$
\begin{equation}\label{OC}
\int_{\Omega} \tilde{\Psi}_{I,i}(\tilde{\Psi}_{J,i} - \Psi_{J,i}) \mathrm{d} \Omega = 0
\end{equation}
$$

Pluging RK smoothed gradient of Eq. $\ref{RKSG}$ into orthogonal condition of Eq. $\ref{OC}$, we can find the RK smoothed gradient is variantional consistent:

$$
\begin{equation}
\begin{split}
\int_{\Omega} \tilde{\Psi}_{I,i}\tilde{\Psi}_{J,i} \mathrm{d} \Omega &=
\boldsymbol{a}_{iI}^{T} \underbrace{\int_{\Omega} \boldsymbol{p}^{[p-1]} \boldsymbol{p}^{[p-1]T} \mathrm{d} \Omega}_{\boldsymbol{G}} \boldsymbol{G}^{-1} \boldsymbol{g}_{iJ} \\ &= 
\boldsymbol{a}_{iI}^{T} \boldsymbol{g}_{iJ} \\ &=
\int_{\Omega} \boldsymbol{a}_{iI}^{T}\boldsymbol{p}^{[p-1]} \Psi_{J,i} \mathrm{d}\Omega \\ &=
\int_{\Omega} \tilde{\Psi}_{I,i} \Psi_{J,i} \mathrm{d} \Omega
\end{split}
\end{equation}
$$

Furthermore, in pratice, the problem domain $\Omega$ is partitioned into a set of background integration cells $\{ \Omega_{C} \} _{C=1}^{n_{el}}$, $n_{el}$ is the total number of cells. And the RK gradient smoothing is usually carried out in each background integration cells. For simplex integration domain, the evaluation of RK smoothed gradient is simple and straightforward with the help of  natural coordinates[^Wang2019]. However, this method also maintain some disadvantages:
* The smoothed gradients are evaluated independly in each integration cells, so the smoothed gradient is usually discontinuous.
* For incompressible material, discontinuous gradients will lead more volumetric constraints and cause volumetric locking.
* ...

## Generalized RK gradient smoothing

As mentioned above, in RK framework, the smoothed gradient is discontinuous between each integration cells. In this report, we aim to construct the continuous smoothed gradients in whole domain. Assuming that the RK smoothed gradients are constructed in a general form, which consists of arbitrary basis functions $\boldsymbol{\mathcal{P}}^{[p-1]}$ and coefficient vector $\boldsymbol{a}_{iI}$  as follow:

$$
\begin{equation}
\tilde{\Psi}_{I,i} = \boldsymbol{\mathcal{P}}^{[p-1]T} \boldsymbol{a}_{iI}
\end{equation}
$$

in which the basis functions are required that, can be spanned by $(p-1)$-th order monormials vector $\boldsymbol{p}^{[p-1]}$ and be independent with each other basis functions. In tradtional RK smoothed gradient, the basis functions are chosen as $(p-1)$-th order monormials vector $\boldsymbol{p}^{[p-1]}$, and its coefficient vector $\boldsymbol{a}_{iI}$ is independent in each integration cells, which result the RK smoothed gradients are discontinuous in whole domain. On the constrary, if a set of continuous basis functions is employed, the RK smoothed gradient will be continuous in the whole domain. The simply and straightforward optimal candidate is piecewise finite element shape functions listed as:

$$
\begin{equation}
\boldsymbol{\mathcal{P}} = \{ N_{K} \}_{K=1}^{n_{p}}, \quad 
\boldsymbol{a}_{iI} = \{ \tilde{\Psi}_{I,i}(\boldsymbol{x}_{K}) \}_{K=1}^{n_{p}}
\end{equation}
$$

where $N_{K}$ is the finite element shape function equipped at node $\boldsymbol{x}_{K}$. In this case, the components of coefficient  vector $\boldsymbol{a}_{iI}$ is related between each cells, which can be determined by fulfillment of orthogonal condition Eq. $\ref{OC}$ as:

$$
\begin{equation}
\int_{\Omega} \tilde{\Psi}_{I,i}\tilde{\Psi}_{J,i} \mathrm{d} \Omega = \int_{\Omega} \tilde{\Psi}_{I,i}\Psi_{J,i} \mathrm{d} \Omega
\end{equation}
$$

$$
\begin{equation}
\boldsymbol{G}\boldsymbol{a}_{iI} = \boldsymbol{g}_{iI}
\end{equation}
$$

where the components of moment matrix $\boldsymbol{G}$ and right hand side of integration constraint $\boldsymbol{g}_{iI}$ are represented by:

$$
\begin{equation}\label{momentMatrix}
G_{KL} = \int_{\Omega} N_{K} N_{L} \mathrm{d} \Omega
\end{equation}
$$

$$
\begin{equation}\label{integrationConstraint}
g_{iIK} = \int_{\Gamma} \Psi_{I} N_{K} n_{i}\mathrm{d}\Gamma - 
\int_{\Omega} \Psi_{I} N_{K,i} \mathrm{d}\Omega
\end{equation}
$$

Finally, the generalized reproducing kernel can be expressed as the same form in Eq. $\ref{RKSG2}$ with moment matrix and integration constraint in Eqs. $\ref{momentMatrix}$ and $\ref{integrationConstraint}$.

## Mixed formulation
For isotropic materials, the constitutive equation may be writtena as:

$$
\begin{equation}
\begin{split}
\sigma_{ij} &= \lambda \varepsilon_{kk} \delta_{ij} + 2\mu \varepsilon_{ij} \\
&= (\lambda + \frac{2}{3}\mu) \varepsilon_{kk} \delta_{ij} + 
2\mu (\varepsilon_{ij} - \frac{1}{3} \varepsilon_{kk} \delta_{ij}) \\
&= 3K \varepsilon_{ij}^{dil} + 2G \varepsilon_{ij}^{dev}
\end{split}
\end{equation}
$$

where $K$ and $G$ are bulk modulus and shear modulus, respectively. $\lambda$ and $\mu$ are Lamé coefficients,  listed as:


$$
\begin{equation}
K = \lambda + \frac{2}{3}\mu, \quad G = \mu
\end{equation}
$$

$$
\begin{equation}
\lambda = \frac{E\nu}{(1+\nu)(1-2\nu)}, \quad \mu = \frac{E}{2(1+\nu)}
\end{equation}
$$

In the case of incompressible elasticity, i.e. $\nu \rightarrow 0.5$, the bulk modulus becomes unbounded, as $K \rightarrow \infty$. A new formulation will be employed for this problem as follow:

$$
\begin{equation}
\sigma_{ij} = -p \delta_{ij} + 2\mu \varepsilon_{ij}^{dev}
\end{equation}
$$

where $p$ is the hydrostatic pressure, in this circumstance, an additional equation will be introduced to strong form, namely **kinematic condtion of incompressibility** as:

$$
\begin{equation}
\nabla \cdot \boldsymbol{u} + \frac{p}{3K}= u_{k,k} + \frac{p}{3K}= 0
\end{equation}
$$

the corresprongding weak form of this system can be rewritten as:

$$
\begin{equation}\label{weak}
\int_{\Omega} \delta \varepsilon_{ij} \sigma_{ij} \mathrm{d} \Omega - \int_{\Omega} \delta p(u_{k,k} + \frac{p}{3K}) \mathrm{d} \Omega 
= \int_{\Gamma^{t}} \delta u_{i} \bar{t}_{i} \mathrm{d} \Gamma + \int_{\Omega} \delta u_{i} \bar{b}_{i} \mathrm{d} \Omega
\end{equation}
$$

Invoking approximations to displacement $\boldsymbol{u}$ and hydrostatic pressure $p$ leads to:

$$
\begin{equation}\label{approximation}
\boldsymbol{u}^{h} = \sum_{I=1}^{n_{p}} \Psi_{I} \boldsymbol{d}_{I}, \quad
p^{h} = \sum_{I=1}^{n_{p}} N_{I} p_{I}
\end{equation}
$$

It is noted that in order to get the optimal constraint ratio for suppress volumetric locking, the number of freedoms for hydrostatic pressure is chosen as the same with that of displacment.  Pluging $\ref{approximation}$ into Galerkin weak form $\ref{weak}$ can get the discrete governing equation:

$$
\begin{equation}
\begin{bmatrix}
\bar{\boldsymbol{K}} & \boldsymbol{G} \\
\boldsymbol{G}^{T} & \boldsymbol{M}
\end{bmatrix}
\begin{Bmatrix}
\boldsymbol{d} \\ \boldsymbol{p}
\end{Bmatrix} = 
\begin{Bmatrix}
\boldsymbol{f} \\ \boldsymbol{0}
\end{Bmatrix}
\end{equation}
$$

where components of matrices are given by:

$$
\begin{equation}
\bar{\boldsymbol{K}}_{IJ} = \int_{\Omega} \boldsymbol{B}_{I}^{devT} \boldsymbol{D} \boldsymbol{B}_{J}^{dev} \mathrm{d} \Omega
\end{equation}
$$

$$
\begin{equation}
\boldsymbol{G}_{IK} = \int_{\Omega} \boldsymbol{B}_{I}^{dilT} N_{K} \mathrm{d} \Omega
\end{equation}
$$


$$
\begin{equation}
M_{KL} = \int_{\Omega} \frac{1}{3K} N_{K} N_{L} \mathrm{d} \Omega
\end{equation}
$$

$$
\begin{equation}
\int_{\Omega} \delta p^{h}(u_{k,k}^{h} + \frac{p^{h}}{3K}) \mathrm{d} \Omega
\end{equation}
$$


## Numerical examples
### Comparison of various shape functions

### Varifying consistency condition
### Hollow cylinder under  inner and outer pressures



[^Simo1986]:Simo, J.C., Hughes, T.J.R., 1986. On the Variational Foundations of Assumed Strain Methods. Journal of Applied Mechanics 53, 51–54. https://doi.org/10.1115/1.3171737
[^Wang2019]:Wang, D., Wu, J., 2019. An inherently consistent reproducing kernel gradient smoothing framework toward efficient Galerkin meshfree formulation with explicit quadrature. Computer Methods in Applied Mechanics and Engineering 349, 628–672. https://doi.org/10.1016/j.cma.2019.02.029

