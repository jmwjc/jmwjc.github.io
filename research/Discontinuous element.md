$$
\begin{equation}
\int_{\Omega_K} v_{,i} u_{,i} d\Omega = \int_{\Gamma_K} v u_{,i} n_i d\Gamma -
\int_{\Omega_K} v u_{,ii} d\Omega
\end{equation}
$$

$$
\begin{equation}
\sum_{K} \int_{\Omega_K} v_{,i} u_{,i} d\Omega =
\sum_{K} \int_{\Gamma_K} v u_{,i} n_i d\Gamma -
\sum_{K} \int_{\Omega_K} v u_{,ii} d\Omega
\end{equation}
$$

$$
\begin{equation}
\int_{\Omega} v_{,i} u_{,i} d\Omega =
\sum_{K} \int_{\Gamma_K} v u_{,i} n_i d\Gamma -
\int_{\Omega} v u_{,ii} d\Omega
\end{equation}
$$

1 element:
$$
\begin{equation}
\int_{\Omega} v_{,i} u_{,i} d\Omega = \int_{\Gamma^t} v td\Gamma +
\int_{\Omega} v b d\Omega + \int_{\Gamma^g} \gamma (u - g)d\Gamma +
\int_{\Gamma^g} v \lambda d\Gamma
\end{equation}
$$

Approximation:
$$
\begin{equation}
u = \sum_I N_I d_I, \quad v = \sum_I N_I \delta d_I
\end{equation}
$$

$$
\begin{equation}
\lambda = \sum_I \bar{N}_I \lambda_I, \quad \gamma = \sum_I \bar{N}_I \delta \lambda_I
\end{equation}
$$

$$
\begin{equation}
\begin{bmatrix}
\boldsymbol{K} & \boldsymbol{G} \\ \boldsymbol{G} & \boldsymbol{0}
\end{bmatrix} =
\begin{Bmatrix}
\boldsymbol{f} \\ \boldsymbol{g}
\end{Bmatrix}
\end{equation}
$$

$$
\begin{equation}
K_{IJ} = \int_\Omega N_{I,i} N_{J,i} d\Omega
\end{equation}
$$

$$
\begin{equation}
G_{IK} = - \int_{\Gamma^g} \bar{N}_I N_K d\Gamma
\end{equation}
$$

$$
\begin{equation}
f_I = \int_{\Gamma^t} N_I t d\Gamma + \int_\Omega N_I b d\Omega
\end{equation}
$$

$$
\begin{equation}
g_K = - \int_{\Gamma^g} \bar{N}_I g d\Gamma
\end{equation}
$$

$$
\begin{equation}
\boldsymbol{K} = \frac{1}{A}
\begin{bmatrix}
D_{1i}^2 & D_{1i}D_{2i} & D_{1i}D_{3i} \\
D_{2i}D_{1i} & D_{2i}^2 & D_{2i}D_{3i} \\
D_{3i}D_{1i} & D_{3i}D_{2i} & D_{3i}^2
\end{bmatrix}
\end{equation}
$$
$$
\begin{equation}
\boldsymbol{G} = \begin{bmatrix}

\end{bmatrix}
\end{equation}
$$
