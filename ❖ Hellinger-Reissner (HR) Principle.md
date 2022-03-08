
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
the external force and body force are applied by Lagrangian mutiplers as:
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

# [[❖ bar, beam, plate|Kirchhoff-Love Plate]]

