$$
\left \{
\begin{array}{l}
\bar{u}_{\alpha}(\boldsymbol{x}) = u_{\alpha}(x_1,x_2) - x_3 w_{,\alpha} \\
\bar{u}_{3}(\boldsymbol{x}) = w(x_1,x_2)
\end{array}
\right .
,\quad \alpha = 1,2
$$
$$
\left \{
\begin{aligned}
\varepsilon_{\alpha \beta} &=\frac{1}{2}(u_{\alpha, \beta}+u_{\beta, \alpha})-x_{3}w_{, \alpha \beta} \\
\varepsilon_{\alpha 3} &=\frac{1}{2}\left(w_{, \alpha}-w_{,\alpha}\right) = 0 \\
\varepsilon_{33} &=0
\end{aligned}
\right .
$$
$$
\begin{align}
\begin{Bmatrix}
\sigma_{11} \\ \sigma_{22} \\ \sigma_{33} \\ \sigma_{12} \\ \sigma_{13} \\ \sigma_{23}
\end{Bmatrix} &= 
\frac{E}{(1+\nu)(1-2\nu)}
\begin{bmatrix}
1-\nu &   \nu &   \nu & 0 & 0 & 0 \\
  \nu & 1-\nu &   \nu & 0 & 0 & 0 \\
  \nu &   \nu & 1-\nu & 0 & 0 & 0 \\
    0 &     0 &     0 & \frac{(1-2\nu)}{2} & 0 & 0 \\
    0 &     0 &     0 & 0 & \frac{(1-2\nu)}{2} & 0 \\
    0 &     0 &     0 & 0 & 0 & \frac{(1-2\nu)}{2}
\end{bmatrix}
\begin{Bmatrix}
u_{1,1} - x_3 w_{,11} \\ u_{2,2} - x_3 w_{,22} \\ 0 \\ u_{1,2}+u_{2,1}-2x_3 w_{,12} \\ 0 \\ 0
\end{Bmatrix} \\ &=
\begin{Bmatrix}
u_{1,1} - x_3 w_{,11} \\ u_{2,2} - x_3 w_{,22} \\ 0 \\ u_{1,2}+u_{2,1}-2x_3 w_{,12} \\ 0 \\ 0
\end{Bmatrix}
\end{align}
$$

# Strong form

$$
\left \{
\begin{array}{ll}
    M_{\alpha\beta,\alpha\beta}+\bar{q}=0 & \text{in} \; \Omega \\
    w = \bar{w} & \text{on} \; \Gamma^w \\
    w_{,\bm{n}} = \bar{\theta}_{\bm{n}} & \text{on} \; \Gamma^\theta \\
    M_{\bm{nn}} = \bar{M}_{\bm{nn}} & \text{on} \; \Gamma^M \\
    Q_{\bm{n}} + M_{\bm{ns},\bm{s}} = \bar{V}_{\bm{n}} & \text{on} \; \Gamma^V \\
    w_{i} = \bar{w}_{i} & i=1,2,\dots \\
    P_{j} = \bar{P}_{j} & j=1,2,\dots
\end{array}
\right .
$$
where
$$
w_{,\bm{n}} = w_{,\alpha} n_{\alpha}, \; M_{\bm{nn}} = M_{\alpha\beta} n_{\alpha} n_{\beta}, \; Q_{\bm{n}} = M_{\alpha\beta,\beta} n_{\alpha}, \; M_{\bm{ns},\bm{s}} = M_{\alpha\beta,\gamma} s_{\alpha} n_{\beta} s_{\gamma}, \; P_{j} = - \Delta_{j} M_{\bm{ns}}
$$
$$
\begin{Bmatrix}
    M_{11} \\ M_{22} \\ M_{12}
\end{Bmatrix} = -D
\begin{bmatrix}
    1 & \nu & 0 \\
    \nu & 1 & 0 \\
    0 & 0 & \frac{1-\nu}{2}
\end{bmatrix}
\begin{Bmatrix}
    w_{,11} \\ w_{,22} \\ 2w_{,12}
\end{Bmatrix}
$$
$$
D=\frac{h^3E}{12(1-\nu^2)}
$$

# Weak form

Energy functional:
$$
\Pi(M_{\alpha\beta}) = \int_{\Omega} \frac{1}{2} M_{\alpha\beta} d_{\alpha\beta\gamma\eta}M_{\gamma\eta}d\Omega - 
\int_{\Gamma^w} V_{\bm{n}} \bar{w} d\Gamma +
\int_{\Gamma^\theta} M_{\bm{nn}} \bar{\theta}_{\bm{n}} d\Gamma - \sum_i P_i \bar{w}_i
$$
$$
\begin{multline}
\Pi'(M_{\alpha\beta},w) = \Pi(M_{\alpha\beta}) + \int_{\Omega} w (M_{\alpha\beta,\alpha\beta}+\bar{q})d\Omega \\ +
\int_{\Gamma^M} w_{,\bm{n}}(M_{\bm{nn}} - \bar{M}_{\bm{nn}}) d\Gamma -
\int_{\Gamma^V} w(V_{\bm{n}} - \bar{V}_{\bm{n}}) d\Gamma - \sum_{j} w_j (P_j-\bar{P}_j)
\end{multline}
$$
weak form:
$$
\begin{align}
\int_\Omega \delta M_{\alpha\beta} d_{\alpha\beta\gamma\eta}M_{\gamma\eta} d\Omega + 
\int_{\Omega} \delta M_{\alpha\beta,\alpha\beta} w d\Omega +
\int_{\Gamma^M} \delta M_{\bm{nn}} w_{,\bm{n}} d\Gamma -
\int_{\Gamma^V} \delta V_{\bm{n}} w d\Gamma - \sum_{j} \delta P_j w_j =
\int_{\Gamma^w} \delta V_{\bm{n}} \bar{w} d\Gamma -
\int_{\Gamma^\theta} \delta M_{\bm{nn}} \bar{\theta}_{\bm{n}} d\Gamma + \sum_i \delta P_i \bar{w}_i \\
-\int_{\Omega} \delta w M_{\alpha\beta,\alpha\beta}d\Omega -
\int_{\Gamma^M} \delta w_{,\bm{n}}M_{\bm{nn}} d\Gamma +
\int_{\Gamma^V} \delta w V_{\bm{n}} d\Gamma + \sum_{j} \delta w_j P_j = 
\int_{\Omega} \delta w \bar{q}d\Omega -
\int_{\Gamma^M} \delta w_{,\bm{n}}\bar{M}_{\bm{nn}} d\Gamma +
\int_{\Gamma^V} \delta w \bar{V}_{\bm{n}} d\Gamma + \sum_{j} \delta w_j \bar{P}_j
\end{align}
$$
