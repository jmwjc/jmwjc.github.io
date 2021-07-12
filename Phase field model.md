## Phase field model
Phase field model(PFM) firstly is constructed for tracking the phase transformation of some physical phenomenon, or finding the boundaries for graphs. This ability of PFM will thank to $\Gamma$ convergence performed in PFM. We consider the energy of second order PFM as follow:
$$
\mathcal{D} = \int_\Omega k (\frac{(1-v)^2}{4l} + l \vert \nabla v \vert ^2) d\Omega
$$
and the corresponding profile in 1D is given by:
$$
v = 1 - e^{-\frac{\vert x-x_c \vert}{2l}}
$$
where $x_c$ is a constant, and this will be the location of the crack in PFM fracture model. We can check this result by substituting Eq.$\ref{profile}$ into Eq.$\ref{pfmenergy}$, yields:
$$
\begin{split}
\mathcal{D} &= \int_\Omega k(\frac{e^{-\frac{\vert x-x_c \vert}{l}}}{4l} + l\vert \frac{e^{-\frac{\vert x-x_c \vert}{2l}}}{2l}\vert ^2)d\Omega \\
&= \int_\Omega k(\frac{1}{4l}e^{-\frac{\vert x-x_c \vert}{l}} + \frac{1}{4l}e^{-\frac{\vert x-x_c \vert}{l}})d\Omega \\
&= \int_\Omega k \frac{1}{2l}e^{-\frac{\vert x-x_c \vert}{l}}d\Omega \\
&= k
\end{split}
$$
## PFM modeling fracture
Consider a field $\Omega$ with a crack $\Gamma^c$, the loss of the energy caused by crack, namely surface energy functional of crack $\mathcal{D}$, can be integrated along with the crack:
$$
\mathcal{D} = \int_{\Gamma^c} k d\Gamma = k \Gamma^c
$$
where $k$ is the critical energy release rate. And the crack $\Gamma^c$ can depicted by PFM as:
$$
\Gamma^c = \int_\Omega \gamma d\Omega = \int_\Omega \frac{(1-v)^2}{4l} + l \vert \nabla v \vert ^2 d\Omega
$$
take Eq.$\ref{gamma}$ in to Eq.$\ref{crack}$:
$$
\mathcal{D}(v) = k\int_\Omega \frac{(1-v)^2}{4l} + l \vert \nabla v \vert ^2 d\Omega
$$
so we reconsider the variation functional energy $\Pi$:
$$
\Pi(\boldsymbol{u},v) = \int_\Omega \psi(\boldsymbol{u},v) d\Omega + \mathcal{D}(v) + \mathcal{F}(\boldsymbol{u})