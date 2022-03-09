
# [[❖ Elasticity|Elasticity]]

Consider the following strong form:
$$
\left \{
\begin{array}{ll}
    \sigma_{ij,j} + b_{i} = 0 & \text{on} \; \Omega \\
    \sigma_{ij}n_{j} = t_{i} & \text{in} \; \Gamma^t \\
    u_i  = g_i & \text{in} \; \Gamma^g 
\end{array}
\right .
$$
the Hellinger-Reissner potential energy functional is given by:
$$
\Pi(\sigma_{ij}) = \int_\Omega W(\sigma_{ij}) d\Omega - \int_{\Gamma^g} \sigma_{ij}n_{j}g_{i} d\Gamma 
$$
where $W$ is the energy density, stress and strain has the following relation:
$$
\frac{\partial W}{\partial \sigma_{ij}} = \frac{1}{2}(u_{i,j} + u_{j,i})
$$
the external force and body force are applied by Lagrangian multipliers as:
$$
\begin{align}
    \bar{\Pi}(\sigma_{ij}) &= \Pi(\sigma_{ij}) + \int_{\Omega} u_i (\sigma_{ij,j} + b_i) d\Omega - \int_{\Gamma^t} u_i(\sigma_{ij}n_j+t_i)d\Gamma \\
    &= \int_\Omega W(\sigma_{ij}) d\Omega - \int_{\Gamma^g} \sigma_{ij}n_{j}g_{i} d\Gamma  + \int_{\Omega} u_i (\sigma_{ij,j} + b_i) d\Omega - \int_{\Gamma^t} u_i(\sigma_{ij}n_j+t_i)d\Gamma
\end{align}
$$
with variational operator, the weak form can be expressed as:
$$
\begin{multline}
    \delta \bar{\Pi}(\sigma_{ij}) = \int_{\Omega} \delta \sigma_{ij} \frac{\partial W}{\partial \sigma_{ij}} d\Omega - \int_{\Gamma^g} \delta \sigma_{ij}n_j g_i d\Gamma + \int_{\Omega} \delta \sigma_{ij,j} u_i d\Omega - \int_{\Gamma^t} \delta \sigma_{ij}n_j u_i d\Gamma \\
    + \int_{\Omega} \delta u_i (\sigma_{ij,j} + b_i) d\Omega - \int_{\Gamma^t} \delta u_i(\sigma_{ij}n_j+t_i)d\Gamma
\end{multline}
$$

# [[❖ Kirchhoff-Love Plate|Kirchhoff-Love Plate]]

Consider the strong form of Kirchhoff-Love plate:
$$
\left \{
\begin{array}{ll}
    M_{\alpha \beta, \alpha \beta} = \bar{q} & \text{in} \; \Omega \\
    w = \bar{w} & \text{on} \; \Gamma^w \\
    w_{,\alpha} n_{\alpha} = \bar{\theta}_\bm{n} & \text{on} \; \Gamma^{\theta} \\
    Q_\bm{n} + M_{\bm{ns},\bm{s}} = \bar{V}_\bm{n} & \text{on} \; \Gamma^{V} \\
    M_{\bm{nn}} = \bar{M}_{\bm{nn}} & \text{on} \; \Gamma^{M} \\
\end{array}
\right .
$$
where
$$
Q_{\bm{n}} = M_{\alpha \beta, \beta} n_{\alpha}, \qquad M_{\bm{nn}} = M_{\alpha \beta} n_\alpha n_\beta, \qquad M_{\bm{ns},\bm{s}} = M_{\alpha \beta, \gamma}s_{\alpha} n_{\beta} s_{\gamma}
$$
and the $n_{\alpha}$ and $s_{\alpha}$ are the components of outward normal and tangential vectors, and the following relation holds true:
$$
\delta_{\alpha \beta} = n_{\alpha}n_{\beta} + s_{\alpha}s_{\beta}
$$
the Hellinger-Reissner potential energy functional lists as follow:
$$
\begin{multline}
    \Pi(M_{\alpha \beta}) = \int_{\Omega} \frac{1}{2D(1-\nu^2)}((M_{11} + M_{22})^2 + 2(1+\nu)(M^2_{12}-M_{11}M_{22}))d\Omega \\
    - \int_{\Gamma^w}\bar{w} M_{\alpha \beta} n_{\alpha} n_{\beta} d\Gamma + \int_{\Gamma^\theta} \bar{\theta}_{\bm{n}} M_{\bm{nn}}d\Gamma
\end{multline}
$$
in which, the relation of $\bar{\theta}_{\bm{s}} = w_{,\alpha}s_{\alpha} = 0$ is embedded. Follow the same path, the external force and body force are applied by Lagrangian multipliers:
$$
\begin{align}
    \bar{\Pi}(M_{\alpha \beta}) = \Pi(M_{\alpha \beta}) + \int_{\Omega} w(M_{\alpha \beta, \alpha \beta} + \bar{q})d\Omega + \int_{\Gamma^M}w_{,\bm{n}}(M_{\bm{nn}} - \bar{M}_{\bm{nn}})d\Gamma - \int_{\Gamma^V} w(V_{\bm{n}} - \bar{V}_{\bm{n}})d\Gamma
\end{align}
$$
the corresponding weak form can be gotten by:
$$
\delta \bar{\Pi}(M_{\alpha \beta}) = \delta \Pi (M_{\alpha \beta}) + \int_{\Omega} \delta M_{\alpha \beta, \alpha \beta} w d\Omega + \int_{\Gamma^M} \delta M_{\alpha \beta} n_{\alpha} n_{\beta} w_{,\gamma} n_{\gamma} d\Gamma - \int_{\Gamma^V} \delta V_{\bm{n}} w d\Gamma
$$

