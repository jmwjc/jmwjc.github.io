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
$$
## Tensile-compressive splitting model
$$
\psi(\bm{\varepsilon},v) = g(v) \psi_{0}^{+}(\bm{\varepsilon}) + \psi_{0}^{-}(\bm{\varepsilon})
$$

$$
\psi^{\pm}_{0}(\bm{\varepsilon}) = \frac{1}{2}\lambda \langle \pm \mathrm{tr}(\bm{\varepsilon}) \rangle ^{2} + \mu \bm{\varepsilon}^{\pm}:\bm{\varepsilon}^{\pm}
$$

where $\langle \cdot \rangle$ is the Macaulay bracket defined as $\langle x \rangle = \frac{\vert x \vert + x}{2}$. The tensile and compressive parts of strain tensor $\bm{\varepsilon}$, denoted by $\bm{\varepsilon}^{+}$ and $\bm{\varepsilon}^{-}$, are given by spectral decomposition of strain tensor:

$$
\bm{\varepsilon}^{+} = \sum_{\alpha = 1}^{3} \langle \varepsilon_{\alpha} \rangle \bm{e}_{\alpha} \otimes \bm{e}_{\alpha}, \quad
\bm{\varepsilon}^{-} = \sum_{\alpha = 1}^{3} - \langle -\varepsilon_{\alpha} \rangle \bm{e}_{\alpha} \otimes \bm{e}_{\alpha}
$$

## Stress decomposition in frictional interfaces
Consider the friction in damaged region, the stress tensor is interpolated by bulk stress, $\bm{\sigma}_{\text{bulk}}$, and interface stress, $\bm{\sigma}_{\text{interface}}$:
$$
\bm{\sigma} = g(v) \bm{\sigma}_{\text{bulk}} + (1-g(v))\bm{\sigma_{\text{interface}}}
$$

$$
\dot{\bm{\sigma}}_{\text{bulk}} = \bm{C}:\dot{\bm{\varepsilon}}
$$

We define the contact normal strain, $\varepsilon_{nn}$:
$$
\varepsilon_{nn} = \bm{\varepsilon}:(\bm{n}\otimes \bm{n})
$$
For the strain-softening material, the stress in interface region is evaluated by:
$$
\dot{\bm{\sigma}}_{\text{interface}} = \bm{C}:(\dot{\bm{\varepsilon}} - \dot{\bm{\varepsilon}}^{p})
$$
Assume that
$$
\dot{\bm{\varepsilon}}^{p} = \gamma \bm{r}(\bm{\sigma})
$$
The yield function is given by:
$$
f(\bm{\sigma}_{\text{interface}}):= \vert \tau \vert - \tau_{Y} \le 0
$$
where
$$
\tau:= \frac{1}{2}\bm{\sigma}:\bm{\alpha}, \quad \bm{\alpha} = \bm{m} \otimes \bm{n} + \bm{n} \otimes \bm{m}
$$
$$
\tau_{Y} = - \mu \sigma_{nn}, \quad \sigma_{nn} = \bm{\sigma}:\bm{\beta},\quad \bm{\beta} = \bm{n}\otimes \bm{n}
$$
Kuhn-Tucker conditions:
$$
\text{if} f(\bm{\sigma}) = 0\; \text{and} \; \gamma \ne 0, \quad
\gamma \dot{f} = 0
$$

$$
\begin{align}
    \dot{f} &= \frac{\partial f}{\partial \bm{\sigma}}: \dot{\bm{\sigma}} \\
      &= \frac{\partial f}{\partial \bm{\sigma}}: \bm{C}:(\dot{\bm{\varepsilon}} - \dot{\bm{\varepsilon}}^{p}) \\
      &= \frac{\partial f}{\partial \bm{\sigma}}: \bm{C}:(\dot{\bm{\varepsilon}} - \gamma \bm{r}) \\
      &= 0
\end{align}
$$
$$
\gamma = \frac{\partial_{\bm{\sigma}} f:\bm{C}:\dot{\bm{\varepsilon}}}{\partial_{\bm{\sigma}} f:\bm{C}:\bm{r}}
$$
$$
\begin{align}
    \partial_{\bm{\sigma}}f &= \frac{\partial (\vert \tau \vert - \tau_{Y})}{\partial \bm{\sigma}} \\
           &= \frac{\partial (\vert \frac{1}{2}\bm{\sigma}:\bm{\alpha} \vert + \mu \bm{\sigma}:\bm{\beta})}{\partial \bm{\sigma}} \\
           &= \frac{1}{2}\text{sign}(\tau)\bm{\alpha} + \mu \bm{\beta}
\end{align}
$$
$$
\begin{align}
    \dot{\bm{\sigma}} &= \bm{C}:(\dot{\bm{\varepsilon}}-\dot{\bm{\varepsilon}}^{p}) \\
            &= \bm{C}:(\dot{\bm{\varepsilon}}-\gamma \bm{r}) \\
            &= (\bm{C} - \frac{\bm{C}:\bm{r}\otimes\bm{C}:\partial_{\bm{\sigma}} f}{\partial_{\bm{\sigma}} f:\bm{C}:\bm{r}}):\dot{\bm{\varepsilon}}
\end{align}
$$
Tangent elastoplastic moduli tensor
$$
\bm{C}^{\text{ep}} = \left \{
\begin{array}{l}
    \bm{C} & \text{if} \; \gamma = 0 \\
    \bm{C} - \frac{\bm{C}:\bm{r}\otimes\bm{C}:\partial_{\bm{\sigma}} f}{\partial_{\bm{\sigma}} f:\bm{C}:\bm{r}} & \text{if} \; \gamma > 0
    
\end{array}
\right .
$$
Associative case
$$
\bm{r} = \partial_{\bm{\sigma}}f
$$
$$
\bm{r}:\frac{\bm{C}:\bm{r}}{\bm{r}:\bm{C}:\bm{r}},\quad \bm{r}:\mathrm{sign}(\tau)\bm{\alpha} = 1 \Rightarrow \frac{\bm{C}:\bm{r}}{\bm{r}:\bm{C}:\bm{r}} = \mathrm{sign}(\tau)\bm{\alpha}
$$
$$
\bm{C}^{\text{ep}} = \left \{
\begin{array}{l}
    \bm{C} & \text{if} \; \gamma = 0 \\
    \bm{C} - \mathrm{sign}(\tau)\bm{\alpha}\otimes\bm{C}:\bm{r} & \text{if} \; \gamma > 0
    
\end{array}
\right .
$$
$$
\dot{\bm{\sigma}}_{\text{interface}} = \left \{
    \begin{array}{l}
    \bm{0} & \text{if open}(\varepsilon_{nn}>0) \\
    \dot{\bm{\sigma}}_{\text{bulk}} & \text{if stick} (\varepsilon_{nn}\le 0,\; f<0)\\
    \dot{\bm{\sigma}}_{\text{friction}} + \dot{\bm{\sigma}}_{\text{no-penetration}} & \text{if slip} (\varepsilon_{nn}\le0,\;f=0)
    \end{array}
\right .
$$
$$
\bm{\sigma} = \left \{
    \begin{array}{l}
    g(v)\bm{\sigma}_{\text{bulk}} & \text{if open}(\varepsilon_{nn}>0) \\
    \bm{\sigma}_{\text{bulk}} & \text{if stick} (\varepsilon_{nn}\le 0,\; f<0)\\
    \bm{\sigma}_{\text{bulk}} - (1-g(v))\tau_{\text{bulk}}\bm{\alpha} + (1-g(v))\tau_{r}\bm{\alpha} & \text{if slip} (\varepsilon_{nn}\le0,\;f=0)
    \end{array}
\right .
$$
where
$$
\tau_{\text{bulk}} = \frac{1}{2} \bm{\sigma}:\bm{\alpha},\quad \tau_{\text{r}} = - \mathrm{sign}(\tau_{\text{bulk}})\mu \bm{\sigma}:\bm{\beta}

$$
## Weak form
$$
\delta \Pi(\bm{u},v) = \int_{\Omega} g(v)\delta\bm{\sigma}:\bm{\varepsilon}d\Omega + \int_{\Omega}\delta v g_{,v}(v)\frac{1}{2}\bm{\sigma}:\bm{\varepsilon}d\Omega + k \int_{\Omega} \frac{\delta v(v-1)}{2l} + 2 l \nabla \delta v \cdot \nabla v d\Omega + \delta \mathcal{F}(\bm{u})
$$

