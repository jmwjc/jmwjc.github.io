$$
\begin{align}
    \int_{\Gamma}\sigma_{ij}n_{j}u_{i}d\Gamma &= \int_{\Gamma}\sigma_{11}n_{1}u_{1}+\sigma_{12}n_{2}u_{1}+\sigma_{21}n_{1}u_{2}+\sigma_{22}n_{2}u_{2}d\Gamma \\
    &= \int_{\Gamma} C_{1111}\varepsilon_{11}n_{1}u_{1} + C_{1122}\varepsilon_{22}n_{1}u_{1} \\
    &+ C_{1212}\varepsilon_{12}(n_{1}u_{2}+n_{2}u_{1}) \\
    &+ C_{2211}\varepsilon_{11}n_{2}u_{2} + C_{2222}\varepsilon_{22}n_{2}u_{2}d\Gamma \\
    &= \begin{Bmatrix}
        v_{1I} \\ v_{2I}
    \end{Bmatrix}^T \int_{\Gamma} \begin{bmatrix}
        C_{1111}N_{I,1}n_{1}N_{I}+C_{1212}N_{I,2}n_{2}N_{I}
        & C_{2211}N_{I,1}n_{2}N_{I}+C_{1212}N_{I,2}n_{1}N_{I} \\
        C_{1122}N_{I,2}n_{1}N_{I}+C_{1212}N_{I,1}n_{2}N_{I}
        & C_{2222}N_{I,2}n_{2}N_{I}+C_{1212}N_{I,1}n_{1}N_{I}
    \end{bmatrix} \begin{Bmatrix}
        u_{1I} \\ u_{2I}
    \end{Bmatrix}
\end{align}
$$
$$
\begin{align}
    \int_{\Gamma}\sigma_{ij}n_{j}g_{i}d\Gamma &= \int_{\Gamma}\sigma_{11}n_{1}g_{1}+\sigma_{12}n_{2}g_{1}+\sigma_{21}n_{1}g_{2}+\sigma_{22}n_{2}g_{2}d\Gamma \\
    &= \int_{\Gamma} C_{1111}\varepsilon_{11}n_{1}g_{1} + C_{1122}\varepsilon_{22}n_{1}g_{1} \\
    &+ C_{1212}\varepsilon_{12}(n_{1}g_{2}+n_{2}g_{1}) \\
    &+ C_{2211}\varepsilon_{11}n_{2}g_{2} + C_{2222}\varepsilon_{22}n_{2}g_{2}d\Gamma \\
    &= \begin{Bmatrix}
        v_{1I} \\ v_{2I}
    \end{Bmatrix}^T \int_{\Gamma} \begin{Bmatrix}
        (C_{1111}N_{I,1}n_{1}+C_{1212}N_{I,2}n_{2})g_{1} + (C_{2211}N_{I,1}n_{2}+C_{1212}N_{I,2}n_{1})g_{2} \\
        (C_{1122}N_{I,2}n_{1}+C_{1212}N_{I,1}n_{2})g_{1} + (C_{2222}N_{I,2}n_{2}+C_{1212}N_{I,1}n_{1})g_{2}
    \end{Bmatrix} d\Gamma
\end{align}
$$
$$
\begin{align}
    \int_{\Gamma}\sigma_{ij}n_{j}n_{ik}u_{k}d\Gamma &= \int_{\Gamma}
    (\sigma_{11}n_{1}n_{11}u_{1}+\sigma_{11}n_{1}n_{12}u_{2} \\
    &+\sigma_{12}n_{2}n_{11}u_{1}+\sigma_{12}n_{2}n_{12}u_{2} \\
    &+\sigma_{21}n_{1}n_{21}u_{1}+\sigma_{21}n_{1}n_{22}u_{2} \\
    &+\sigma_{22}n_{2}n_{21}u_{1}+\sigma_{22}n_{2}n_{22}u_{2}d\Gamma \\
    &= \begin{Bmatrix}
        v_{1I} \\ v_{2I}
    \end{Bmatrix}^T \int_{\Gamma} \begin{bmatrix}
        (C_{1111}n_{1}n_{11}+C_{2211}n_{2}n_{12})N_{I,1}N_{I}
        +(C_{1212}n_{1}n_{12}+C_{1212}n_{2}n_{11})N_{I,2}N_{I}
        & (C_{1111}n_{1}n_{12}+C_{2211}n_{2}n_{22})N_{I,1}N_{I}
        +(C_{1212}n_{2}n_{12}+C_{1212}n_{1}n_{22})N_{I,2}N_{I} \\
        (C_{1212}n_{1}n_{12}+C_{1212}n_{2}n_{11})N_{I,1}N_{I}
        +(C_{1122}n_{1}n_{11}+C_{2222}n_{2}n_{12})N_{I,2}N_{I}
        & (C_{1212}n_{2}n_{12}+C_{1212}n_{1}n_{22})N_{I,1}N_{I}
        +(C_{1122}n_{1}n_{12}+C_{2222}n_{2}n_{22})N_{I,2}N_{I}
    \end{bmatrix} \begin{Bmatrix}
        u_{1I} \\ u_{2I}
    \end{Bmatrix}
\end{align}
$$

