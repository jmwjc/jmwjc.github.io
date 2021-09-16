## Kinematics on surface
Suppose that a specific point at shell can be expressed by material coordinates $\boldsymbol{X}$ or spatial coordinates $\boldsymbol{x}$ as follows:
$$
\begin{equation}
\boldsymbol{X}(\xi^1,\xi^2,\xi^3) = \boldsymbol{\varrho} (\xi^1,\xi^2) +
\xi^3 \boldsymbol{N}(\xi^1,\xi^2)
\end{equation}
$$
$$
\begin{equation}
\boldsymbol{x}(\xi^1,\xi^2,\xi^3) = \boldsymbol{\rho}(\xi^1,\xi^2) +
\xi^3 \boldsymbol{n}(\xi^1,\xi^2)
\end{equation}
$$
$$
\begin{equation}
\boldsymbol{\rho} = \boldsymbol{\varrho} + \boldsymbol{v}, \quad
\boldsymbol{n} = \boldsymbol{N} + \boldsymbol{\vartheta}
\end{equation}
$$
$$
\begin{equation}
\boldsymbol{N} = \frac{1}{J_0} \boldsymbol{\varrho}_{,1} \times
\boldsymbol{\varrho}_{,2}
\end{equation}
$$
$$
\begin{equation}
J_0 = \Vert \boldsymbol{\varrho}_{,1} \times \boldsymbol{\varrho}_{,2} \Vert
\end{equation}
$$
$$
\begin{equation}
\begin{split}
\boldsymbol{n} &= \frac{1}{J} \boldsymbol{\rho}_{,1} \times
\boldsymbol{\rho}_{,2} \\
&= \frac{1}{J}(\boldsymbol{\varrho}_{,1} \times
\boldsymbol{v}_{,2} + \boldsymbol{v}_{,1} \times \boldsymbol{\varrho}_{,2} +
\boldsymbol{v}_{,1} \times \boldsymbol{v}_{,2}) + \boldsymbol{N}
\end{split}
\end{equation}
$$
$$
\begin{equation}
J = \Vert \boldsymbol{\rho}_{,1} \times \boldsymbol{\rho}_{,2} \Vert
\end{equation}
$$
$$
\begin{equation}
\boldsymbol{\vartheta} \approx \frac{1}{J} (\boldsymbol{\varrho}_{,1} \times
\boldsymbol{v}_{,2} + \boldsymbol{v}_{,1} \times \boldsymbol{\varrho}_{,2})
\end{equation}
$$
$$
\begin{equation}
\boldsymbol{n} \cdot \boldsymbol{n} = 1, \quad
\boldsymbol{N} \cdot \boldsymbol{N} = 1
\end{equation}
$$
$$
\begin{equation}
\boldsymbol{n}_{,\alpha} \cdot \boldsymbol{n} = 0, \quad
\boldsymbol{N}_{,\alpha} \cdot \boldsymbol{N} = 0
\end{equation}
$$
**Displacement**
$$
\begin{equation}
\boldsymbol{x} = \boldsymbol{u} + \boldsymbol{X}
\end{equation}
$$
$$
\begin{equation}
\boldsymbol{u} = \boldsymbol{v} + \xi^3 \boldsymbol{\vartheta}
\end{equation}
$$
**Strain Measure**
$$
\begin{equation}
\begin{split}
ds^2 - dS^2 &= d\boldsymbol{x} \cdot d\boldsymbol{x} - d\boldsymbol{X} \cdot d\boldsymbol{X} \\ &=
\boldsymbol{g}_i \cdot \boldsymbol{g}_j d\xi^i d\xi^j -
\boldsymbol{G}_i \cdot \boldsymbol{G}_j d\xi^i d\xi^j \\ &=
(g_{ij} - G_{ij}) d\xi^i d\xi^j \\ &=
d\boldsymbol{\xi} \cdot 2 \boldsymbol{E} \cdot d\boldsymbol{\xi}
\end{split}
\end{equation}
$$
where, according to [[❖ Curvilinear Coordinates]], the covariant basis vectors and metric coefficient are defined by:
$$
\begin{equation}
d\boldsymbol{x} = \boldsymbol{g}_i d\xi^i, \quad
d\boldsymbol{X} = \boldsymbol{G}_i d\xi^i
\end{equation}
$$
$$
\begin{equation}
g_{ij} = \boldsymbol{g}_i \cdot \boldsymbol{g}_j, \quad
G_{ij} = \boldsymbol{G}_i \cdot \boldsymbol{G}_j
\end{equation}
$$
and $\boldsymbol{E}$ is the strain tensor, and its components are given by:
$$
\begin{equation}
E_{ij} = \frac{1}{2}(g_{ij} - G_{ij})
\end{equation}
$$
with
$$
\begin{equation}
\boldsymbol{g}_\alpha = \boldsymbol{\rho}_{,\alpha} +
\xi^3 \boldsymbol{n}_{,\alpha}, \quad
\boldsymbol{g}_3 = \boldsymbol{n}
\end{equation}
$$
$$
\begin{equation}
\boldsymbol{G}_\alpha = \boldsymbol{\varrho}_{,\alpha} +
\xi^3 \boldsymbol{N}_{,\alpha}, \quad
\boldsymbol{G}_3 = \boldsymbol{N}
\end{equation}
$$
$$
\begin{equation}
\begin{split}
\boldsymbol{g}_\alpha &= \boldsymbol{\varrho}_{,\alpha} + \boldsymbol{v}_{,\alpha} +
\xi^3 (\boldsymbol{N}_{,\alpha} + \boldsymbol{\vartheta}_{,\alpha}) \\ &=
\boldsymbol{u}_{,\alpha} + \boldsymbol{G}_{\alpha}
\end{split}
\end{equation}
$$
$$
\begin{equation}
\begin{split}
g_{\alpha \beta} &= \boldsymbol{g}_{\alpha} \cdot \boldsymbol{g}_{\beta} \\
&= (\boldsymbol{\rho}_{,\alpha} + \xi^3 \boldsymbol{n}_{,\alpha}) \cdot
(\boldsymbol{\rho}_{,\beta} + \xi^3 \boldsymbol{n}_{,\beta}) \\
&= \boldsymbol{\rho}_{,\alpha} \cdot \boldsymbol{\rho}_{,\beta} +
(\boldsymbol{\rho}_{,\alpha} \cdot \boldsymbol{n}_{,\beta} +
\boldsymbol{n}_{\alpha} \cdot \boldsymbol{\rho}_{,\beta}) \xi^3 +
\boldsymbol{n}_{,\alpha} \cdot \boldsymbol{n}_{,\beta} (\xi^3)^2
\end{split}
\end{equation}
$$
$$
\begin{equation}
\begin{split}
g_{\alpha 3} &= \boldsymbol{g}_{\alpha} \cdot \boldsymbol{g}_3 \\
&= (\boldsymbol{\rho}_{,\alpha} + \xi^3 \boldsymbol{n}_{,\alpha}) \cdot
\boldsymbol{n} \\
&= 0
\end{split}
\end{equation}
$$
$$
\begin{equation}
g_{33} = \boldsymbol{g}_3 \cdot \boldsymbol{g}_3
= \boldsymbol{n} \cdot \boldsymbol{n} = 1
\end{equation}
$$
$$
\begin{equation}
\begin{split}
G_{\alpha \beta} &= \boldsymbol{G}_{\alpha} \cdot \boldsymbol{G}_{\beta} \\
&= \boldsymbol{\varrho}_{,\alpha} \cdot \boldsymbol{\varrho}_{,\beta} +
(\boldsymbol{\varrho}_{,\alpha} \cdot \boldsymbol{N}_{,\beta} +
\boldsymbol{N}_{\alpha} \cdot \boldsymbol{\varrho}_{,\beta}) \xi^3 +
\boldsymbol{N}_{,\alpha} \cdot \boldsymbol{N}_{,\beta} (\xi^3)^2
\end{split}
\end{equation}
$$
$$
\begin{equation}
G_{\alpha 3} = \boldsymbol{G}_{\alpha} \cdot \boldsymbol{G}_3 = 0
\end{equation}
$$
$$
\begin{equation}
G_{33} = \boldsymbol{G}_3 \cdot \boldsymbol{G}_3
= \boldsymbol{N} \cdot \boldsymbol{N} = 1
\end{equation}
$$
$$
\begin{equation}
\begin{split}
E_{\alpha \beta}
&= \frac{1}{2}
(\boldsymbol{\rho}_{,\alpha} \cdot \boldsymbol{\rho}_{,\beta} -
\boldsymbol{\varrho}_{,\alpha} \cdot \boldsymbol{\varrho}_{,\beta})\\
&+ \frac{1}{2}
(\boldsymbol{\rho}_{,\alpha} \cdot \boldsymbol{n}_{,\beta} +
\boldsymbol{n}_{\alpha} \cdot \boldsymbol{\rho}_{,\beta} -
\boldsymbol{\varrho}_{,\alpha} \cdot \boldsymbol{N}_{,\beta} -
\boldsymbol{N}_{\alpha} \cdot \boldsymbol{\varrho}_{,\beta}) \xi^3 \\
&+ \frac{1}{2}
(\boldsymbol{n}_{,\alpha} \cdot \boldsymbol{n}_{,\beta} -
\boldsymbol{N}_{,\alpha} \cdot \boldsymbol{N}_{,\beta})(\xi^3)^2 \\
&= \frac{1}{2}
(\boldsymbol{\varrho}_{,\alpha} \cdot \boldsymbol{v}_{,\beta} +
\boldsymbol{v}_{,\alpha} \cdot \boldsymbol{\varrho}_{,\beta} +
\boldsymbol{v}_{,\alpha} \cdot \boldsymbol{v}_{,\beta}) \\
&+ \frac{1}{2}
(\boldsymbol{N}_{,\alpha} \cdot \boldsymbol{v}_{,\beta} +
\boldsymbol{v}_{,\alpha} \cdot \boldsymbol{N}_{,\beta} +
\boldsymbol{\varrho}_{,\alpha} \cdot \boldsymbol{\vartheta}_{,\beta} +
\boldsymbol{\vartheta}_{,\alpha} \cdot \boldsymbol{\varrho}_{,\beta} +
\boldsymbol{v}_{,\alpha} \cdot \boldsymbol{\vartheta}_{,\beta} +
\boldsymbol{\vartheta}_{,\alpha} \cdot \boldsymbol{v}_{,\beta}) \xi^3 \\
&+ \frac{1}{2}
(\boldsymbol{N}_{,\alpha} \cdot \boldsymbol{\vartheta}_{,\beta} +
\boldsymbol{\vartheta}_{,\alpha} \cdot \boldsymbol{N}_{,\beta} +
\boldsymbol{\vartheta}_{,\alpha} \cdot \boldsymbol{\vartheta}_{,\beta})
(\xi^3)^2 \\
&\approx \varepsilon_{\alpha \beta} =
\epsilon_{\alpha \beta} + \kappa_{\alpha \beta} \xi^3
\end{split}
\end{equation}
$$
$$
\begin{equation}
\epsilon_{\alpha \beta} = \frac{1}{2}
(\boldsymbol{\varrho}_{,\alpha} \cdot \boldsymbol{v}_{,\beta} +
\boldsymbol{v}_{,\alpha} \cdot \boldsymbol{\varrho}_{,\beta})
\end{equation}
$$
$$
\begin{equation}
\kappa_{\alpha \beta} = \frac{1}{2}
(\boldsymbol{N}_{,\alpha} \cdot \boldsymbol{v}_{,\beta} +
\boldsymbol{v}_{,\alpha} \cdot \boldsymbol{N}_{,\beta} +
\boldsymbol{\varrho}_{,\alpha} \cdot \boldsymbol{\vartheta}_{,\beta} +
\boldsymbol{\vartheta}_{,\alpha} \cdot \boldsymbol{\varrho}_{,\beta})
\end{equation}
$$
$$
\begin{equation}
E_{3\alpha} = 0
\end{equation}
$$
$$
\begin{equation}
E_{33} = 0
\end{equation}
$$
