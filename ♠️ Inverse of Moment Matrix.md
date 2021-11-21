$$
\bm{A}^{-1} = \begin{bmatrix}
    a_{11} & a_{12} & a_{13} \\
    a_{12} & a_{22} & a_{23} \\
    a_{13} & a_{23} & a_{33}
\end{bmatrix}
$$
$$
\bm{A}_{,x} = \begin{bmatrix}
    b_{11} & b_{12} & b_{13} \\
    b_{12} & b_{22} & b_{23} \\
    b_{13} & b_{23} & b_{33}
\end{bmatrix}
$$
$$
\bm{A}^{-1}\bm{A}_{,x} = \begin{bmatrix}
    a_{1i}b_{1i} & a_{1i}b_{2i} & a_{1i}b_{3i} \\
    a_{2i}b_{1i} & a_{2i}b_{2i} & a_{2i}b_{3i} \\
    a_{3i}b_{1i} & a_{3i}b_{2i} & a_{3i}b_{3i}
\end{bmatrix}
$$
$$
\bm{A}^{-1}\bm{A}_{,x}\bm{A}^{-1} = \begin{bmatrix}
    a_{1i}b_{ij}a_{j1} & a_{1i}b_{ij}a_{j2} & a_{1i}b_{ij}a_{j3} \\
    a_{2i}b_{ij}a_{j1} & a_{2i}b_{ij}a_{j2} & a_{2i}b_{ij}a_{j3} \\
    a_{3i}b_{ij}a_{j1} & a_{3i}b_{ij}a_{j2} & a_{3i}b_{ij}a_{j3}
\end{bmatrix}
$$
$$
\bm{A} = \bm{L}\bm{L}^{T} = \bm{U}^{T}\bm{U}
$$
$$
\bm{A}^{-1} = \bm{L}^{-T}\bm{L}^{-1} = \bm{U}^{-1}\bm{U}^{-T}
$$
$$
\bm{A}^{-1}\bm{A}_{,x}\bm{A}^{-1} = \bm{U}^{-1}\bm{U}^{-T}\bm{A}_{,x}\bm{U}^{-1}\bm{U}^{-T}
$$
$$
\bm{U}^{-1} = \begin{bmatrix}
    c_{11} & c_{12} & c_{13} \\
     & c_{22} & c_{23} \\
     &  & c_{33}
\end{bmatrix}
$$
$$
\bm{U}^{-T}\bm{A}_{,x} = \begin{bmatrix}
    c_{11}b_{11} & c_{11}b_{12} & c_{11}b_{13} \\
    c_{k2}b_{k1} & c_{k2}b_{k2} & c_{k2}b_{k3} \\
    c_{3i}b_{i1} & c_{3i}b_{i2} & c_{3i}b_{i3}
\end{bmatrix}
$$
$$
\bm{U}^{-T}\bm{A}_{,x}\bm{U}^{-1} = \begin{bmatrix}
    c_{11}b_{11}c_{11} & c_{11}b_{11}c_{12} + c_{11}b_{12}c_{22}  & c_{11}b_{11}c_{13} + c_{11}b_{12}c_{23} + c_{11}b_{13}c_{33} \\
    c_{12}b_{11}c_{11} + c_{22}b_{21}c_{11} & c_{12}b_{11}c_{12} + c_{22}b_{21}c_{12} + c_{12}b_{12}c_{22} + c_{22}b_{22}c_{22} & c_{12}b_{11}c_{13} + c_{22}b_{21}c_{13} + c_{12}b_{22}c_{23} + c_{22}b_{22}c_{23} + c_{12}b_{13}c_{33} + c_{22}c_{23}c_{33} \\
    c_{3i}b_{i1} & c_{3i}b_{i2} & c_{3i}b_{i3}
\end{bmatrix}
$$
$$
\bm{A}^{-1} = \bm{U}^{-1}\bm{U}^{-T} = \begin{bmatrix}
    c_{11}c_{11} + c_{12}c_{12} + c_{13}c_{13} & c_{12}c_{22} + c_{13}c_{23} & c_{13}c_{33} \\
     & c_{22}c_{22} + c_{23}c_{23} & c_{23}c_{33} \\
     &  & c_{33}c_{33}
\end{bmatrix}
$$
$$
\bm{U}^{-T}\bm{U}^{-1} = \begin{bmatrix}
    c_{11}c_{11} & c_{11}c_{12} & c_{11}c_{13} \\
     & c_{12}c_{12} + c_{22}c_{22} & c_{12}c_{13} + c_{22}c_{23} \\
     &  & c_{13}c_{13} + c_{23}c_{23} + c_{33}c_{33}
\end{bmatrix}
$$
