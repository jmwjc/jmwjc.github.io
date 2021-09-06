---
File  : ∞ Derivation of linear triangular domain
Topic : localerror
Status: #✏️
---
Last modify data: <%+ tp.file.last_modified_date() %>
Logs: 
-  #❗️ (2021-09-05) Initial derivation
	- [ ] Check the possibility for local error of triangular element

---
$$
\int_\Omega v_{,i} u_{,i} d\Omega = \int_\Gamma v u_{,i} n_i d\Gamma - \int_\Omega v u_{,ii} d\Omega
$$

$$
u = a_0 + a_1 \xi_1 + a_2 \xi_2
$$

$$
\left \{
\begin{align}
    x &= \xi_1 x_1 + \xi_2 x_2 + \xi_3 x_3 \\
    y &= \xi_1 y_1 + \xi_2 y_2 + \xi_3 y_3
\end{align}
\right .
$$

$$
\begin{bmatrix}
    D_{11} & D_{21} & D_{31} \\
    D_{12} & D_{22} & D_{23}
\end{bmatrix} =
\begin{bmatrix}
    y_3 - y_2 & y_1 - y_3 & y_2 - y_1 \\
    x_2 - x_3 & x_3 - x_1 & x_1 - x_2
\end{bmatrix} 
$$
$$
\begin{align}
    u_{,x} &= u_{,1} \xi_{1,x} + u_{,2} \xi_{2,x} \\
    u_{,y} &= u_{,1} \xi_{1,y} + u_{,2} \xi_{2,y}
\end{align}
$$

$$
\begin{align}
    u_{,x} &= -\frac{1}{2A}(a_1 D_{11} + a_2 D_{12}) \\
    u_{,y} &= -\frac{1}{2A}(a_1 D_{21} + a_2 D_{22})
\end{align}
$$
$$
u = N_1(\bm{\xi}) b_1 + N_2(\bm{\xi}) b_2 + N_3(\bm{\xi}) b_3
$$

- #❗️  (2021-09-06) 还没推到完成
$$
\begin{Bmatrix}
    N_1 \\ N_2 \\ N_3
\end{Bmatrix} =
\begin{Bmatrix}
    b_{10} + b_{11} \xi_1 + b_{12} \xi_2 \\
    b_{20} + b_{21} \xi_1 + b_{22} \xi_2 \\
    b_{30} + b_{31} \xi_1 + b_{32} \xi_2
\end{Bmatrix} 
$$
总共9个未知数，单位分解性和对称性可得：
$$
\begin{align}
    b_{10} &= b_{20} = b_{30} = \frac{1}{3} \\
    b_{11} &= b_{22} \\
    b_{12} &= b_{21} \\

\end{align}
$$

$$
\bm{K} = 
\begin{Bmatrix}
    \delta a_1 \\ \delta a_2
\end{Bmatrix} 
\begin{bmatrix}
    D_{11}^2 & D_{11}D_{12} \\
    D_{12}D_{22} & D_{22}^2
\end{bmatrix} 
\begin{Bmatrix}
    a_1 \\ a_2
\end{Bmatrix}
$$
