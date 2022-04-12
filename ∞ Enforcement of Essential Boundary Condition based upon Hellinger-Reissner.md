
![[❖ Hellinger-Reissner (HR) Principle#❖ Elasticity Elasticity]]

# Discretization

$$
\sigma_{ij} = \sum_{K=1}^{n_q} N_{K} \sigma_{ijK}, \qquad u_i = \sum_{I=1}^{n_p} \Psi_I u_{iI}
$$
substituting it into weak form yields:
$$
\begin{Bmatrix}
    \delta \sigma_{ijK} \\ \delta u_{iI}
\end{Bmatrix}^T
\begin{bmatrix}
    -\int_{\Omega} N_K C_{ijkl}^{-1} N_L d\Omega & \int_{\Gamma^t} N_K n_j \Psi_J d\Gamma - \int_{\Omega} N_{K,j} \Psi_J d\Omega \\
    \int_{\Gamma^t} \Psi_I n_j N_L d\Gamma - \int_{\Omega} \Psi_I N_{L,j} d\Omega &
\end{bmatrix}
\begin{Bmatrix}
    \sigma_{ijL} \\ u_{iJ}
\end{Bmatrix} =
\begin{Bmatrix}
    -\int_{\Gamma^g} N_K n_j g_i d\Gamma \\ \int_{\Gamma^t} \Psi_I t_i d\Gamma + \int_{\Omega} \Psi_I b_i d\Omega
\end{Bmatrix}
$$
$$
\begin{Bmatrix}
    \delta \sigma_{ijK} \\ \delta u_{iI}
\end{Bmatrix}^T
\begin{bmatrix}
    -\int_{\Omega} N_K C_{ijkl}^{-1} N_L d\Omega & \int_{\Gamma} N_K n_j \Psi_J d\Gamma - \int_{\Omega} N_{K,j} \Psi_J d\Omega - \int_{\Gamma^g} N_K n_j \Psi_J d\Gamma \\
    \int_{\Gamma} \Psi_I n_j N_L d\Gamma - \int_{\Omega} \Psi_I N_{L,j} d\Omega - \int_{\Gamma^g} \Psi_I n_j N_L d\Gamma &
\end{bmatrix}
\begin{Bmatrix}
    \sigma_{ijL} \\ u_{iJ}
\end{Bmatrix} =
\begin{Bmatrix}
    -\int_{\Gamma^g} N_K n_j g_i d\Gamma \\ \int_{\Gamma^t} \Psi_I t_i d\Gamma + \int_{\Omega} \Psi_I b_i d\Omega
\end{Bmatrix}
$$

![[❖ Hellinger-Reissner (HR) Principle#❖ Kirchhoff-Love Plate Kirchhoff-Love Plate]]

# Discretization

$$
M_{\alpha \beta} = \sum_{K=1}^{n_p} N_K M_{\alpha \beta K}, \qquad w = \sum_{I=1}^{n_p} \Psi_I w_I
$$
substituting it into weak form yields:
$$
\begin{align}
    \int_{\Gamma^M} \delta M_{\bm{nn}} w_{,\bm{n}} d\Gamma - \int_{\Gamma^V} (\delta Q_{\bm{n}} + \delta M_{\bm{ns},\bm{s}}) w d\Gamma &=
    \int_{\Gamma} \delta M_{\bm{nn}} w_{,\bm{n}} d\Gamma - \int_{\Gamma^\theta} \delta M_{\bm{nn}} w_{,\bm{n}} d\Gamma
    - \int_{\Gamma} (\delta Q_{\bm{n}} + \delta M_{\bm{ns},\bm{s}}) w d\Gamma + \int_{\Gamma^w} (\delta Q_{\bm{n}} + \delta M_{\bm{ns},\bm{s}}) w d\Gamma \\
    &= \int_{\Gamma} \delta M_{\alpha \beta} n_{\beta} w_{,\alpha} d\Gamma - \int_{\Gamma} \delta M_{\alpha \beta,\beta} n_{\alpha} w d\Gamma \\
    &- \int_{\Gamma} \delta M_{\bm{ns}} w_{,\bm{s}} d\Gamma - \int_{\Gamma} \delta M_{\bm{ns},\bm{s}} w d\Gamma \\
    &- \int_{\Gamma^\theta} \delta M_{\bm{nn}} w_{,\bm{n}} d\Gamma + \int_{\Gamma^w} (\delta Q_{\bm{n}} + \delta M_{\bm{ns},\bm{s}}) w d\Gamma \\
    &= \int_{\Gamma} \delta M_{\alpha \beta} n_{\beta} w_{,\alpha} d\Gamma - \int_{\Gamma} \delta M_{\alpha \beta,\beta} n_{\alpha} w d\Gamma \\
    &- \int_{\Gamma^\theta} \delta M_{\bm{nn}} w_{,\bm{n}} d\Gamma + \int_{\Gamma^w} (\delta Q_{\bm{n}} + \delta M_{\bm{ns},\bm{s}}) w d\Gamma
\end{align}
$$
according to fundamental theorem for line integrals, we have:
$$
\int_{\Gamma} \delta M_{\bm{ns}} w_{,\bm{s}} d\Gamma + \int_{\Gamma} \delta M_{\bm{ns},\bm{s}} w d\Gamma = \int_{\Gamma}(\delta M_{\bm{ns}} w)_{,\bm{s}} d\Gamma
$$

