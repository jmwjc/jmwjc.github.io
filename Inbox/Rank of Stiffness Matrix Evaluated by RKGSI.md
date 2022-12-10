## 1D problem with linear RKGSI
RKGSI in a cell $\Omega_C$
$$
\tilde \Psi_{I,x} = qG^{-1}g_{xI} = \frac{1}{L_C}\int_{\Gamma_C} \Psi_I n d\Gamma = \frac{1}{L_C}(\Psi_I(x_{C+1}) - \Psi_I(x_{C})) = \frac{1}{L_C}
\begin{Bmatrix}
    \Psi_{I}(x_{C+1}) & \Psi_{I}(x_{C})
\end{Bmatrix}
\begin{Bmatrix}
    1 \\ -1
\end{Bmatrix}
$$
$$
q = 1,\quad G = L_C,\quad g_{xI} = \Psi_I(x_{C+1}) - \Psi_I(x_{C})
$$
the components of stiffness matrix is evaluated by
$$
\begin{split}
K_{IJ} &= \int_{\Omega}\tilde \Psi_{I,x} \tilde \Psi_{J,x}d\Omega \\
&= \sum_{C} L_C\tilde \Psi_{I,x} \tilde \Psi_{J,x} \\
&= \sum_{C} \frac{1}{L_C}
\begin{Bmatrix}
    \Psi_{I}(x_{C+1}) & \Psi_{I}(x_{C})
\end{Bmatrix}
\begin{bmatrix}
     1 & -1 \\
    -1 &  1
\end{bmatrix}
\begin{Bmatrix}
    \Psi_{J}(x_{C+1}) \\ \Psi_{J}(x_{C})
\end{Bmatrix} \\ &=
\begin{Bmatrix}
    \Psi_{I}(x_{2}) & \Psi_{I}(x_{1})
\end{Bmatrix}
\frac{1}{L_1}
\begin{bmatrix}
     1 & -1 \\
    -1 &  1
\end{bmatrix}
\begin{Bmatrix}
    \Psi_{J}(x_{2}) \\ \Psi_{J}(x_{1})
\end{Bmatrix} \\ &+
\begin{Bmatrix}
    \Psi_{I}(x_{3}) & \Psi_{I}(x_{2})
\end{Bmatrix}
\frac{1}{L_2}
\begin{bmatrix}
     1 & -1 \\
    -1 &  1
\end{bmatrix}
\begin{Bmatrix}
    \Psi_{J}(x_{3}) \\ \Psi_{J}(x_{2})
\end{Bmatrix} \\ &\dots \\ &=
\begin{Bmatrix}
    \Psi_I(x_{1}) \\ \Psi_I(x_{2}) \\ \vdots \\ \Psi_I(x_{n_i})
\end{Bmatrix}^T
\begin{bmatrix}
    \frac{1}{L_1} & -\frac{1}{L_1} & \dots &  \\
    -\frac{1}{L_1} & \frac{1}{L_1}+\frac{1}{L_2} & \dots &  \\
    \vdots & \vdots & \ddots &  \\
     &  &  & 
\end{bmatrix}
\begin{Bmatrix}
    \Psi_J(x_{1}) \\ \Psi_J(x_{2}) \\ \vdots \\ \Psi_J(x_{n_i})
\end{Bmatrix}
\end{split}
$$
stiffness matrix
$$
\boldsymbol K = 
\begin{bmatrix}
    \Psi_1(x_{1}) & \Psi_2(x_{1}) & \dots & \Psi_{n_p}(x_{n_i}) \\
    \Psi_1(x_{2}) & \Psi_2(x_{2}) & \dots & \Psi_{n_p}(x_{n_i}) \\
    \vdots        & \vdots        & \dots        & \vdots        \\
    \Psi_1(x_{n_i}) & \Psi_2(x_{n_i}) & \dots & \Psi_{n_p}(x_{n_i})
\end{bmatrix}^T_{n_p \times n_i}
\begin{bmatrix}
    \frac{1}{L_1} & -\frac{1}{L_1} & \dots &  \\
    -\frac{1}{L_1} & \frac{1}{L_1}+\frac{1}{L_2} & \dots &  \\
    \vdots & \vdots & \ddots &  \\
     &  &  & 
\end{bmatrix}_{n_i \times n_i}
\begin{bmatrix}
    \Psi_1(x_{1}) & \Psi_2(x_{1}) & \dots & \Psi_{n_p}(x_{n_i}) \\
    \Psi_1(x_{2}) & \Psi_2(x_{2}) & \dots & \Psi_{n_p}(x_{n_i}) \\
    \vdots        & \vdots        & \dots        & \vdots        \\
    \Psi_1(x_{n_i}) & \Psi_2(x_{n_i}) & \dots & \Psi_{n_p}(x_{n_i})
\end{bmatrix}_{n_i \times n_p}
$$
# 1D problem with quadratic RKGSI
$$
\boldsymbol q = \{1,\; \xi\}^T, \quad \boldsymbol G = \int_{\Omega_C} \boldsymbol q \boldsymbol q^T d\Omega
$$
$$
\boldsymbol g_{xI} = \int_{\Gamma_C} \Psi_I \boldsymbol q n d\Gamma - \int_{\Omega_C} \Psi_I \boldsymbol q_{,x} d\Omega
$$
