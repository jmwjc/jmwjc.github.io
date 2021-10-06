---
Topic : localerror
Status: ️🖍 🟨
Manager: WuJC
---
Last modify data: <%+ tp.file.last_modified_date() %>
Logs: 
-  #❗️ (2021-09-05) Initial derivation
	- [ ] Check the possibility for local error of triangular element
- #❗️ (2021-09-06) Assume a simply form of shape function
	- [ ] $N_i = c_0 + c_1 \xi_i$
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
u^h = N_1(\bm{\xi}) b_1 + N_2(\bm{\xi}) b_2 + N_3(\bm{\xi}) b_3
$$

$$
\begin{Bmatrix}
    N_1 \\ N_2 \\ N_3
\end{Bmatrix} =
\begin{Bmatrix}
    c_{10} + c_{11} \xi_1 + c_{12} \xi_2 \\
    c_{20} + c_{21} \xi_1 + c_{22} \xi_2 \\
    c_{30} + c_{31} \xi_1 + c_{32} \xi_2
\end{Bmatrix} 
$$

$$
\begin{bmatrix}
    N_{1,1} & N_{1,2}\\ N_{2,1} & N_{2,2} \\ N_{3,1} & N_{3,2}
\end{bmatrix} =
\begin{bmatrix}
    c_{11} & c_{12} \\
    c_{21} & c_{22} \\
    c_{31} & c_{32}
\end{bmatrix} 
$$

$$
\begin{align}
    u_{,x}^h &= -\frac{1}{2A}(b_1 c_{11} + b_2 c_{21} + b_3 c_{31}) \\
    u_{,y}^h &= -\frac{1}{2A}(b_1 c_{12} + b_2 c_{22} + b_3 c_{32})
\end{align}
$$

$$
\int_\Omega v_{,x}^h u_{,x}^h d\Omega = \frac{1}{4A}
\begin{Bmatrix}
    \delta b_1 \\ \delta b_2 \\ \delta b_3
\end{Bmatrix} 
\begin{bmatrix}
    c_{11}^2 & c_{11}c_{21} & c_{11}c_{31}\\
    c_{21}c_{11} & c_{21}^2 & c_{21}c_{31} \\
    c_{31}c_{11} & c_{31}c_{21} & c_{31}^2
\end{bmatrix} 
\begin{Bmatrix}
    b_1 \\ b_2 \\ b_3
\end{Bmatrix}
$$

$$
\int_\Omega v u_{,xx} d\Omega =
\begin{Bmatrix}
    \delta b_1 \\ \delta b_2 \\ \delta b_3
\end{Bmatrix} 
$$

$$
\int_\Gamma v u_{,x} d\Gamma = 
\begin{Bmatrix}
    \delta b_1 \\ \delta b_2 \\ \delta b_3
\end{Bmatrix} \int_\Gamma 
\begin{Bmatrix}
    N_1 u_{,x} n_x \\
    N_2 u_{,x} n_x \\
    N_3 u_{,x} n_x 
\end{Bmatrix} d\Gamma =
\begin{Bmatrix}
    \delta b_1 \\ \delta b_2 \\ \delta b_3
\end{Bmatrix} 
\left (
\int_\Gamma 
\begin{Bmatrix}
    c_{10} \\
    c_{20} \\
    c_{30} 
\end{Bmatrix} u_{,x} n_x d\Gamma + \int_\Gamma 
\begin{Bmatrix}
    c_{11} \xi_1 \\
    c_{22} \xi_2 \\
    c_{33} \xi_3
\end{Bmatrix} u_{,x} n_x d\Gamma
\right )
$$

---

$$
\begin{Bmatrix}
    N_1 \\ N_2 \\ N_3
\end{Bmatrix} = 
\begin{Bmatrix}
    c_0 + c_1 \xi_1 \\ c_0 + c_1 \xi_2 \\ c_0 + c_1 \xi_3
\end{Bmatrix} 
$$

$$
\begin{bmatrix}
    N_{1,1} & N_{1,2} \\
    N_{2,1} & N_{2,2} \\
    N_{3,1} & N_{3,2}
\end{bmatrix} = 
\begin{bmatrix}
    c_1  & 0 \\
    0    & c_2 \\
    -c_1 & -c_1
\end{bmatrix} 
$$

$$
\bm{K} = \int_\Omega v_{,x} u_{,x} d\Omega = 
$$
