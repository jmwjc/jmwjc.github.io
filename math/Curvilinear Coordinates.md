## Dual and Irregular bases
In the Cartesian system, the position can be expressed by Cartesian coordinates $(x_1,x_2,x_3)$ or other parametric coordinates $(\xi^1,\xi^2,\xi^3)$ :
$$
\begin{equation}
\begin{split}
\boldsymbol{x} &= x_1 \boldsymbol{e}_1 + x_2 \boldsymbol{e}_2 + x_3 \boldsymbol{e}_3 \\ &=
\xi^1 \boldsymbol{g}_1 + \xi^2 \boldsymbol{g}_2 + \xi^3 \boldsymbol{g}_3 
\end{split}
\end{equation}
$$
Similarly, a variable $u$ can be depicted by  Cartesian coordinates:
$$
\begin{equation}
u = d_1 \boldsymbol{e}_1 + d_2 \boldsymbol{e}_2 + d_3 \boldsymbol{e}_3
\end{equation}
$$
where $d_i$ is the constant coefficient, $\boldsymbol{e}_i$ is **orthogonal** basis vector, and has the following properties:
$$
\begin{equation}
\boldsymbol{e}_1 = \begin{Bmatrix}
1 \\ 0 \\ 0
\end{Bmatrix}, \quad
\boldsymbol{e}_2 = \begin{Bmatrix}
0 \\ 1 \\ 0
\end{Bmatrix}, \quad
\boldsymbol{e}_3 = \begin{Bmatrix}
0 \\ 0 \\ 1
\end{Bmatrix}, \quad
\end{equation}
$$
$$
\begin{equation}
\boldsymbol{e}_1 \cdot (\boldsymbol{e}_2 \times \boldsymbol{e}_3) = 1
\end{equation}
$$
$$
\begin{equation}
\boldsymbol{e}_i \cdot \boldsymbol{e}_j = \delta_{ij}
\end{equation}
$$
where $\delta_{ij}$ is Kronecker operator defined by:
$$
\begin{equation}
\delta_{ij} = \left \{
\begin{array}{l}
1,\quad i = j \\
0,\quad i \neq j
\end{array} \right.
\end{equation}
$$
For an irregular domain, a non-orthogonal basis vector is facilitated for deformation, yields:
$$
\begin{equation}
u = u^1 \boldsymbol{g}_1 + u^2 \boldsymbol{g}_2 + u^3 \boldsymbol{g}_3 = u_1 \boldsymbol{g}^1 + u_2 \boldsymbol{g}^2 + u_3 \boldsymbol{g}^3 
\end{equation}
$$
where $\boldsymbol{g}_i$ is the covariant basis vector, and $u^i$ is the corresponding coefficient. On the contrary, $\boldsymbol{g}^i$ and $u_i$ are the contravariant basis vector and coefficient, and the covariant and contravariant coordinates are defined by:
$$
\begin{equation}
\boldsymbol{g}_i = \frac{\partial \boldsymbol{x}}{\partial \xi^i}, \quad
\boldsymbol{g}^i = \frac{\partial \xi^i}{\partial \boldsymbol{x}}
\end{equation}
$$
$$
\begin{equation}
\boldsymbol{g}^1 = \frac{1}{J}\boldsymbol{g}_2 \times  \boldsymbol{g}_3, \quad
\boldsymbol{g}^2 = \frac{1}{J}\boldsymbol{g}_3 \times  \boldsymbol{g}_1, \quad
\boldsymbol{g}^3 = \frac{1}{J}\boldsymbol{g}_1 \times  \boldsymbol{g}_2
\end{equation}
$$
where
$$
\begin{equation}
J = \boldsymbol{g}_1 \cdot (\boldsymbol{g}_2 \times \boldsymbol{g}_3)
\end{equation}
$$
For the definition of the covariant and contravariant coordinates, the orthogonality exists between covariant and contravariant coordinates as:
$$
\begin{equation}
\boldsymbol{g}_i \cdot \boldsymbol{g}^j = \delta_i^j = \left \{
\begin{array}{l}
1,\quad i = j \\
0,\quad i \neq j
\end{array} \right.
\end{equation}
$$
and the *covariant metric coefficients* are defined by:
$$
\begin{equation}
g_{ij} = \boldsymbol{g}_i \cdot \boldsymbol{g}_j
\end{equation}
$$
the *contravariant metric coefficients* are that:
$$
\begin{equation}
g^{ij} = \boldsymbol{g}^i \cdot \boldsymbol{g}^j
\end{equation}
$$
and the following relationship holds true:
$$
\begin{equation}
[g_{ij}] = [g^{ij}]^{-1}
\end{equation}
$$
The transformation between $\boldsymbol{g}_{i}$ and $\boldsymbol{g}^{j}$ is carried out by metric coefficients as:
$$
\boldsymbol{g}_{i} = g_{ij} \boldsymbol{g}^{j}
$$
Along the same path, the contravariant basis can be solved by:
$$
\boldsymbol{g}^{i} = g^{ij} \boldsymbol{g}_{j}
$$
$$
g^{ik}g_{kj} = g^{ki}g_{kj} = g^{ik}g_{jk} = g^{ki}g_{jk} = \delta_{j}^{i}
$$
## Derivatives
**Gradient of covariant and contravariant basis**
We introduce the $\boldsymbol{\Gamma}_{ij}$, $\Gamma_{ij}^{k}$ namely the first and second kind of the ***Christoffel Symbols*** evaluated by:
$$
\boldsymbol{\Gamma}_{ij} = \frac{\partial^{2} \boldsymbol{x}}{\partial \xi^{i} \partial \xi^{j}} = \frac{\partial \boldsymbol{g}_i}{\partial \xi^j} = \frac{\partial \boldsymbol{g}_j}{\partial \xi^i}
$$
$$
\Gamma_{ij}^{k} = \boldsymbol{g}^{k} \cdot \boldsymbol{\Gamma}_{ij}, \quad 
\boldsymbol{\Gamma}_{ij} = \Gamma_{ij}^{k} \boldsymbol{g}_{k}
$$
**Gradient of scale**
The gradient(nabla) operator in curvilinear coordinates is defined as:
$$
\begin{equation}
\nabla = \frac{\partial}{\partial \boldsymbol{x}} = 
\frac{\partial}{\partial x_i} \boldsymbol{e}_i = \frac{\partial}{\partial \xi^i} \boldsymbol{g}^i
\end{equation}
$$
**Gradient of first order tensor**
$$
\begin{split}
\nabla \boldsymbol{u} &= \frac{\partial \boldsymbol{u}}{\partial \xi^{i}} \boldsymbol{g}^{i}
= \frac{\partial(u^{j} \boldsymbol{g}_{j})}{\partial \xi^{i}} \boldsymbol{g}^{i} \\
&= \frac{\partial u^{j}}{\partial \xi^{i}} \boldsymbol{g}^{i} \otimes \boldsymbol{g}_{j} + 
\frac{\partial \boldsymbol{g}_{j}}{\partial \xi^{i}} u^{j} \boldsymbol{g}^{i}
\end{split}
$$

  
such that
$$
\nabla \boldsymbol{u} = (\frac{\partial u^{j}}{\partial \xi^{i}} + \Gamma_{ik}^{j} u^{k})
\boldsymbol{g}^{i} \otimes \boldsymbol{g}_{j} = u^{j}|_{i} \boldsymbol{g}^{i} \otimes \boldsymbol{g}_{j}
$$
On the contrary,
$$
\begin{split}
\nabla \boldsymbol{u} &= \frac{\partial \boldsymbol{u}}{\partial \xi^{i}} \boldsymbol{g}^{i}
= \frac{\partial(u_{j} \boldsymbol{g}^{j})}{\partial \xi^{i}} \boldsymbol{g}^{i} \\
&= \frac{\partial u_{j}}{\partial \xi^{i}} \boldsymbol{g}^{i} \otimes \boldsymbol{g}^{j} + 
\frac{\partial \boldsymbol{g}^{j}}{\partial \xi^{i}} u_{j} \boldsymbol{g}^{i} \\
\end{split}
$$
due to the following relationship hold true:
$$
\frac{\partial (\boldsymbol{g}^{k} \cdot \boldsymbol{g}_{j})}{\partial \xi^{i}}
= \frac{\partial \boldsymbol{g}^{k}}{\partial \xi^{i}} \cdot \boldsymbol{g}_{j} + \boldsymbol{g}^{k} \cdot \frac{\partial \boldsymbol{g}_{j}}{\partial \xi^{i}} = 0
$$
  
$$
P_{ij}^{k} = \frac{\partial \boldsymbol{g}^{k}}{\partial \xi^{i}} \cdot \boldsymbol{g}_{j} = - \boldsymbol{g}^{k} \cdot
\frac{\partial \boldsymbol{g}_{j}}{\partial \xi^{i}} = - \Gamma_{ij}^{k}
$$
  
such that
$$
\begin{split}
\nabla \boldsymbol{u} &= (\frac{\partial u_{j}}{\partial \xi^{i}} + P_{ij}^{k} u_{k})
\boldsymbol{g}^{i} \otimes \boldsymbol{g}^{j}\\
&= (\frac{\partial u_{j}}{\partial \xi^{i}} - \Gamma_{ij}^{k} u_{k})
\boldsymbol{g}^{i} \otimes \boldsymbol{g}^{j} \\
&= u_{j}|_{i} \boldsymbol{g}^{i} \otimes \boldsymbol{g}^{j} 
\end{split}
$$
The **Gauss-Ostrogradsky theorem** can be recast as:
$$
\begin{equation}
\begin{split}
\int_{\Omega} \nabla v u d\Omega &= 
\int_{\Omega} \frac{\partial v}{\partial \xi^i} \boldsymbol{g}^i u d\Omega \\ &=
\int_{\Gamma} vu n_i \boldsymbol{g}^i d\Gamma -
\int_{\Omega} v \frac{\partial (\boldsymbol{g}^i u)}{\partial \xi^i} d\Omega \\ &=
\int_{\Gamma} vu \boldsymbol{n} d\Gamma - \int_{\Omega} v (\frac{\partial u}{\partial \xi^i} + uP_{ji}^j) \boldsymbol{g}^id\Omega \\ &=
\int_{\Gamma} vu \boldsymbol{n} d\Gamma - \int_{\Omega} v (\frac{\partial u}{\partial \xi^i} - u\Gamma_{ji}^j) \boldsymbol{g}^id\Omega
\end{split}
\end{equation}
$$
$$
\begin{equation}
\begin{split}
\int_{\Omega} \nabla \boldsymbol{v} : \boldsymbol{u} d\Omega &= 
\int_{\Omega} \frac{\partial \boldsymbol{v}}{\partial \xi^i}\cdot \boldsymbol{u} \cdot \boldsymbol{g}^i d\Omega \\ &=
\int_{\Gamma} \boldsymbol{v} \cdot \boldsymbol{u} \cdot \boldsymbol{n} d\Gamma -
\int_{\Omega} \boldsymbol{v} \cdot \frac{\partial (\boldsymbol{u} \cdot \boldsymbol{g}^i)}{\partial \xi^i} d\Omega \\ &=
\int_{\Gamma} \boldsymbol{v} \cdot \boldsymbol{u} \cdot \boldsymbol{n} d\Gamma - 
\int_{\Omega} \boldsymbol{v} \cdot \boldsymbol{u} \cdot (\nabla + \boldsymbol{P}_j^j) d\Omega \\ &=
\int_{\Gamma} \boldsymbol{v} \cdot \boldsymbol{u} \cdot \boldsymbol{n} d\Gamma - 
\int_{\Omega} \boldsymbol{v} \cdot \boldsymbol{u} \cdot \boldsymbol{g}^i (\frac{\partial}{\partial \xi^i} + P_{ji}^j) d\Omega 
\end{split}
\end{equation}
$$
$$
\begin{equation}
\begin{split}
\int_{\Omega} \nabla \times \boldsymbol{v} \cdot \boldsymbol{u} d\Omega &= 
\int_{\Omega} \boldsymbol{g}^i \times \frac{\partial \boldsymbol{v}}{\partial \xi^i}\cdot \boldsymbol{u}d\Omega \\ &=
\int_{\Gamma} \boldsymbol{v} \cdot \boldsymbol{u} \times \boldsymbol{n} d\Gamma -
\int_{\Omega} (\boldsymbol{v} \cdot \frac{\partial \boldsymbol{u}}{\partial \xi^i} \times \boldsymbol{g}^i + \boldsymbol{v} \cdot \boldsymbol{u} \times \boldsymbol{P}_j^j) d\Omega  \\ &=
\int_{\Gamma} \boldsymbol{v} \cdot \boldsymbol{u} \times \boldsymbol{n} d\Gamma -
\int_{\Omega} (\boldsymbol{v} \cdot \frac{\partial \boldsymbol{u}}{\partial \xi^i} + P_{ji}^j \boldsymbol{v} \cdot \boldsymbol{u})  \times \boldsymbol{g}^i d\Omega  
\end{split}
\end{equation}
$$