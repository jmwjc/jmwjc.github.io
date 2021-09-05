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
    u_{,x} &= -\frac{1}{2A}(u_{,1} D_{11} + u_{,2} D_{12}) \\
    u_{,y} &= -\frac{1}{2A}(u_{,1} D_{21} + u_{,2} D_{22})
\end{align}
$$
$$
u = N_1(\bm{\xi}) b_1 + N_2(\bm{\xi}) b_2 + N_3(\bm{\xi}) b_3
$$

$$
test
$$
