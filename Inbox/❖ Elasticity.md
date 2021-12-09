
$$
\left \{
\begin{array}{l}
\nabla \cdot \bm{\sigma} + \bm{b} = \mathbf{0} & \text{in} \; \Omega \\
\bm{\sigma} \cdot \bm{n} = \bm{t} & \text{on} \; \Gamma^{t} \\
\bm{u} = \bm{g} & \text{on} \; \Gamma^{u}
\end{array} \right .
$$

$$
\left \{
\begin{array}{l}
\sigma_{ij,j} + \bar{b}_{i} = 0 & \text{in} \; \Omega \\
\sigma_{ij} n_{j} = \bar{t}_{i} & \text{on} \; \Gamma^{t} \\
u_{i} = \bar{u}_{i} & \text{on} \; \Gamma^{u}
\end{array} \right .
$$

Constitutive equation

$$
\bm{\sigma} = \bm{C} : \bm{\varepsilon}
$$

$$
\sigma_{ij} = C_{ijkl} \varepsilon_{kl}
$$

Fourth-order elasticity tensor

$$
C_{ijkl} = \lambda \delta_{ij}\delta_{kl} + \mu (\delta_{ik}\delta_{jl} + \delta_{il}\delta_{jk})
$$

Lamé coefficient

$$
\lambda = \frac{E\nu}{(1+\nu)(1-2\nu)}, \quad \mu = \frac{E}{2(1+\nu)}
$$

Strain tensor

$$
\bm{\varepsilon} = \frac{1}{2}(\nabla \cdot \bm{u} + \bm{u} \cdot \nabla)
$$

$$
\varepsilon_{ij} = \frac{1}{2}(u_{i,j} + u_{j,i})
$$

Approximation

$$
\bm{u}^{h} = \sum_{I=1}^{n_{p}} N_{I} \bm{d}_{I}
$$

Matrix form

$$
\begin{Bmatrix}
\sigma_{11} \\ \sigma_{22} \\ \sigma_{33} \\ \sigma_{12} \\ \sigma_{13} \\ \sigma_{23}
\end{Bmatrix} = 
\frac{E}{(1+\nu)(1-2\nu)}
\begin{bmatrix}
1-\nu &   \nu &   \nu & 0 & 0 & 0 \\
  \nu & 1-\nu &   \nu & 0 & 0 & 0 \\
  \nu &   \nu & 1-\nu & 0 & 0 & 0 \\
    0 &     0 &     0 & \frac{(1-2\nu)}{2} & 0 & 0 \\
    0 &     0 &     0 & 0 & \frac{(1-2\nu)}{2} & 0 \\
    0 &     0 &     0 & 0 & 0 & \frac{(1-2\nu)}{2}
\end{bmatrix}
\begin{Bmatrix}
\varepsilon_{11} \\ \varepsilon_{22} \\ \varepsilon_{33} \\ 2\varepsilon_{12} \\ 2\varepsilon_{13} \\ 2\varepsilon_{23}
\end{Bmatrix}
$$

$$
\begin{Bmatrix}
\varepsilon_{11} \\ \varepsilon_{22} \\ \varepsilon_{33} \\ 2\varepsilon_{12} \\ 2\varepsilon_{13} \\ 2\varepsilon_{23}
\end{Bmatrix} =
\begin{Bmatrix}
u_{,x} \\ v_{,y} \\ w_{,z} \\ v_{,x} + u_{,y} \\ w_{,x} + u_{,z} \\ w_{,y} + v_{,z}
\end{Bmatrix} = \sum_{I=1}^{n_{p}}
\begin{bmatrix}
N_{I,x} & 0 & 0 \\ 0 & N_{I,y} & 0 \\ 0 & 0 & N_{I,z} \\
N_{I,y} & N_{I,x} & 0 \\ N_{I,z} & 0 & N_{I,x} \\ 0 & N_{I,z} & N_{I,y} 
\end{bmatrix}
\begin{Bmatrix}
d_{xI} \\ d_{yI} \\ d_{zI}
\end{Bmatrix}
$$

$$
\bm{K}_{IJ} = \int_\Omega \begin{bmatrix}
    N_{I,x} & 0 & 0 \\ 0 & N_{I,y} & 0 \\ 0 & 0 & N_{I,z} \\
    N_{I,y} & N_{I,x} & 0 \\ N_{I,z} & 0 & N_{I,x} \\ 0 & N_{I,z} & N_{I,y}
\end{bmatrix}^T
\begin{bmatrix}
1-\nu &   \nu &   \nu & 0 & 0 & 0 \\
  \nu & 1-\nu &   \nu & 0 & 0 & 0 \\
  \nu &   \nu & 1-\nu & 0 & 0 & 0 \\
    0 &     0 &     0 & \frac{(1-2\nu)}{2} & 0 & 0 \\
    0 &     0 &     0 & 0 & \frac{(1-2\nu)}{2} & 0 \\
    0 &     0 &     0 & 0 & 0 & \frac{(1-2\nu)}{2}
\end{bmatrix}
\begin{bmatrix}
    N_{I,x} & 0 & 0 \\ 0 & N_{I,y} & 0 \\ 0 & 0 & N_{I,z} \\
    N_{I,y} & N_{I,x} & 0 \\ N_{I,z} & 0 & N_{I,x} \\ 0 & N_{I,z} & N_{I,y}
\end{bmatrix}d\Omega
$$
Dilatation part and deviatoric part

$$
\begin{Bmatrix}
\sigma_{11} \\ \sigma_{22} \\ \sigma_{33} \\ \sigma_{12} \\ \sigma_{13} \\ \sigma_{23}
\end{Bmatrix} = 
\frac{E}{1-2\nu}
\begin{Bmatrix}
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}+\varepsilon_{33}) \\ 
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}+\varepsilon_{33}) \\ 
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}+\varepsilon_{33}) \\ 
0 \\ 0 \\ 0
\end{Bmatrix} + 
\frac{E}{1+\nu}
\begin{Bmatrix}
 \frac{2}{3}\varepsilon_{11} - \frac{1}{3}\varepsilon_{22} - \frac{1}{3}\varepsilon_{33} \\
-\frac{1}{3}\varepsilon_{11} + \frac{2}{3}\varepsilon_{22} - \frac{1}{3}\varepsilon_{33} \\
-\frac{1}{3}\varepsilon_{11} - \frac{1}{3}\varepsilon_{22} + \frac{2}{3}\varepsilon_{33} \\ 
\varepsilon_{12} \\ \varepsilon_{13} \\ \varepsilon_{23}
\end{Bmatrix}
$$

$$
\begin{Bmatrix}
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}+\varepsilon_{33}) \\ 
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}+\varepsilon_{33}) \\ 
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}+\varepsilon_{33}) \\ 
0 \\ 0 \\ 0
\end{Bmatrix} = \sum_{I=1}^{n_{p}}
\begin{bmatrix}
\frac{1}{3}N_{I,x} & \frac{1}{3}N_{I,y} & \frac{1}{3}N_{I,z} \\
\frac{1}{3}N_{I,x} & \frac{1}{3}N_{I,y} & \frac{1}{3}N_{I,z} \\
\frac{1}{3}N_{I,x} & \frac{1}{3}N_{I,y} & \frac{1}{3}N_{I,z} \\
0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 
\end{bmatrix}
\begin{Bmatrix}
d_{xI} \\ d_{yI} \\ d_{zI}
\end{Bmatrix}
$$

$$
\begin{Bmatrix}
 \frac{2}{3}\varepsilon_{11} - \frac{1}{3}\varepsilon_{22} - \frac{1}{3}\varepsilon_{33} \\
-\frac{1}{3}\varepsilon_{11} + \frac{2}{3}\varepsilon_{22} - \frac{1}{3}\varepsilon_{33} \\
-\frac{1}{3}\varepsilon_{11} - \frac{1}{3}\varepsilon_{22} + \frac{2}{3}\varepsilon_{33} \\ 
\varepsilon_{12} \\ \varepsilon_{13} \\ \varepsilon_{23}
\end{Bmatrix} = \sum_{I=1}^{n_{p}}
\begin{bmatrix}
 \frac{2}{3}N_{I,x} & -\frac{1}{3}N_{I,y} & -\frac{1}{3}N_{I,z} \\
-\frac{1}{3}N_{I,x} &  \frac{2}{3}N_{I,y} & -\frac{1}{3}N_{I,z} \\
-\frac{1}{3}N_{I,x} & -\frac{1}{3}N_{I,y} &  \frac{2}{3}N_{I,z} \\
 \frac{1}{2}N_{I,y} &  \frac{1}{2}N_{I,x} & 0 \\
 \frac{1}{2}N_{I,z} & 0 & \frac{1}{2}N_{I,x} \\
 0 & \frac{1}{2}N_{I,z} & \frac{1}{2}N_{I,y} 
\end{bmatrix}
\begin{Bmatrix}
d_{xI} \\ d_{yI} \\ d_{zI}
\end{Bmatrix}
$$

Plane strain

$$
\varepsilon_{13} = \varepsilon_{23} = \varepsilon_{33} = 0
$$

$$
\begin{split}
\begin{Bmatrix}
\sigma_{11} \\ \sigma_{22} \\ \sigma_{12} \\ \sigma_{33}
\end{Bmatrix} &= \frac{E}{(1+\nu)(1-2\nu)}
\begin{bmatrix}
1-\nu &   \nu & 0 \\
  \nu & 1-\nu & 0 \\
    0 &     0 & \frac{(1-2\nu)}{2} \\
  \nu &   \nu & 0 \\
\end{bmatrix}
\begin{Bmatrix}
\varepsilon_{11} \\ \varepsilon_{22} \\ 2\varepsilon_{12}
\end{Bmatrix} \\ 
&= 
\frac{E}{1-2\nu}
\begin{Bmatrix}
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}) \\ 
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}) \\ 
0 \\
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}) \\ 
\end{Bmatrix} + 
\frac{E}{1+\nu}
\begin{Bmatrix}
 \frac{2}{3}\varepsilon_{11} - \frac{1}{3}\varepsilon_{22} \\
-\frac{1}{3}\varepsilon_{11} + \frac{2}{3}\varepsilon_{22} \\
\varepsilon_{12} \\
-\frac{1}{3}\varepsilon_{11} - \frac{1}{3}\varepsilon_{22} \\ 
\end{Bmatrix}
\end{split}
$$

$$
\begin{Bmatrix}
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}) \\ 
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}) \\ 
0 \\
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}) \\ 
\end{Bmatrix} = \sum_{I=1}^{n_{p}}
\begin{bmatrix}
\frac{1}{3}N_{I,x} & \frac{1}{3}N_{I,y} \\
\frac{1}{3}N_{I,x} & \frac{1}{3}N_{I,y} \\
0 & 0 \\
\frac{1}{3}N_{I,x} & \frac{1}{3}N_{I,y} \\
\end{bmatrix}
\begin{Bmatrix}
d_{xI} \\ d_{yI} 
\end{Bmatrix}
$$


$$
\begin{Bmatrix}
 \frac{2}{3}\varepsilon_{11} - \frac{1}{3}\varepsilon_{22} \\
-\frac{1}{3}\varepsilon_{11} + \frac{2}{3}\varepsilon_{22} \\
\varepsilon_{12} \\
-\frac{1}{3}\varepsilon_{11} - \frac{1}{3}\varepsilon_{22} \\ 
\end{Bmatrix} = \sum_{I=1}^{n_{p}}
\begin{bmatrix}
 \frac{2}{3}N_{I,x} & -\frac{1}{3}N_{I,y} \\
-\frac{1}{3}N_{I,x} &  \frac{2}{3}N_{I,y} \\
 \frac{1}{2}N_{I,y} &  \frac{1}{2}N_{I,x} \\
-\frac{1}{3}N_{I,x} & -\frac{1}{3}N_{I,y} \\
\end{bmatrix}
\begin{Bmatrix}
d_{xI} \\ d_{yI}
\end{Bmatrix}
$$

Plane stress

$$
\sigma_{13} = \sigma_{23} = \sigma_{33} = 0, \quad 
\varepsilon_{33} = -\frac{\nu}{1-\nu}(\varepsilon_{11} + \varepsilon_{22})
$$

$$
\begin{split}
\begin{Bmatrix}
\sigma_{11} \\ \sigma_{22} \\ \sigma_{12}
\end{Bmatrix} &= \frac{E}{(1+\nu)(1-2\nu)}
\begin{bmatrix}
1-\nu &   \nu & 0 & \nu \\
  \nu & 1-\nu & 0 & \nu \\
    0 &     0 & \frac{(1-2\nu)}{2} & 0\\
\end{bmatrix} 
\begin{Bmatrix}
\varepsilon_{11} \\ \varepsilon_{22} \\ 2\varepsilon_{12} \\ \varepsilon_{33}
\end{Bmatrix} \\ &= \frac{E}{1-\nu^{2}}
\begin{bmatrix}
  1 & \nu & 0\\
\nu &   1 & 0\\
  0 &   0 & \frac{1-\nu}{2}\\
\end{bmatrix} 
\begin{Bmatrix}
\varepsilon_{11} \\ \varepsilon_{22} \\ 2\varepsilon_{12}
\end{Bmatrix} \\ &=
\frac{E}{1-2\nu}
\begin{Bmatrix}
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}+\varepsilon_{33}) \\ 
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}+\varepsilon_{33}) \\ 
0
\end{Bmatrix} + 
\frac{E}{1+\nu}
\begin{Bmatrix}
 \frac{2}{3}\varepsilon_{11} - \frac{1}{3}\varepsilon_{22} - \frac{1}{3}\varepsilon_{33} \\
-\frac{1}{3}\varepsilon_{11} + \frac{2}{3}\varepsilon_{22} - \frac{1}{3}\varepsilon_{33} \\
\varepsilon_{12}
\end{Bmatrix} \\ &=
\frac{E}{1-\nu}
\begin{Bmatrix}
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}) \\ 
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}) \\ 
0
\end{Bmatrix} + 
\frac{E}{1-\nu^{2}}
\begin{Bmatrix}
 \frac{2-\nu}{3}\varepsilon_{11} - \frac{1-2\nu}{3}\varepsilon_{22}\\
-\frac{1-2\nu}{3}\varepsilon_{11} + \frac{2-\nu}{3}\varepsilon_{22}\\
(1-\nu)\varepsilon_{12}
\end{Bmatrix} \\ &= \frac{E}{1-\nu^{2}}
\begin{bmatrix}
  1 & \nu & 0\\
\nu &   1 & 0\\
  0 &   0 & \frac{1-\nu}{2}\\
\end{bmatrix} 
\left (
\begin{Bmatrix}
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}) \\ 
\frac{1}{3}(\varepsilon_{11}+\varepsilon_{22}) \\ 
0
\end{Bmatrix} + 
\begin{Bmatrix}
 \frac{2}{3}\varepsilon_{11} - \frac{1}{3}\varepsilon_{22}\\
-\frac{1}{3}\varepsilon_{11} + \frac{2}{3}\varepsilon_{22}\\
2\varepsilon_{12}
\end{Bmatrix}
\right )
\end{split}
$$

## Cantilever beam problem (plane stress)

Displacement

$$
\left \{
\begin{array}{l}
u = -\frac{Py}{6EI}[(6L-3x)x + (2+\nu)(y^2 - \frac{D^2}{4})] \\
v = \frac{P}{6EI}[3\nu y^2(L-x) + (4+5\nu)\frac{D^2x}{4} + (3L-x)x^2]
\end{array}
\right .
$$

$$
I=\frac{D^3}{12}
$$

Strain

$$
\begin{Bmatrix}
\varepsilon_{xx} \\ \varepsilon_{yy} \\ 2\varepsilon_{xy}
\end{Bmatrix} = 
\begin{Bmatrix}
u_{,x} \\ v_{,y} \\ u_{,y} + v_{,x}
\end{Bmatrix} 
= \frac{P}{EI}
\begin{Bmatrix}
-(L-x)y \\
\nu(L-x)y \\
(1+\nu)(\frac{D^2}{4} - y^2)
\end{Bmatrix}
$$
Stress

$$
\begin{split}
\begin{Bmatrix}
\sigma_{xx} \\ \sigma_{yy} \\ \sigma_{xy}
\end{Bmatrix} &=
\frac{E}{1-\nu^2}
\begin{bmatrix}
  1 & \nu & 0 \\
\nu &   1 & 0 \\
  0 &   0 & \frac{1-\nu}{2}
\end{bmatrix}
\begin{Bmatrix}
\varepsilon_{xx} \\ \varepsilon_{yy} \\ 2\varepsilon_{xy}
\end{Bmatrix} \\ &=
\begin{Bmatrix}
-\frac{P(L-x)y}{I} \\ 0 \\ \frac{P}{2I}(\frac{D^2}{4} - y^2)
\end{Bmatrix}
\end{split}
$$

Traction

$$
\begin{Bmatrix}
\bar{t}_{x} \\ \bar{t}_{y}
\end{Bmatrix} = 
\begin{Bmatrix}
\sigma_{xx}n_{x} + \sigma_{xy}n_{y} \\
\sigma_{yx}n_{x} + \sigma_{yy}n_{y}
\end{Bmatrix}
$$

Body force

$$
\bm{\bar{b}} = -
\begin{Bmatrix}
\sigma_{xx,x} + \sigma_{xy,y} \\
\sigma_{yx,x} + \sigma_{yy,y}
\end{Bmatrix} = \mathbf{0}
$$

Boundary condition

$$
\left \{
\begin{array}{l}
x = 0: u = -\frac{Py}{6EI}(2+\nu)(y^2 - \frac{D^2}{4}), \;
v = \frac{\nu Py^2L}{2EI} \\
x = L: \bm{\bar{t}} = 
\begin{Bmatrix}
0 \\
\frac{P}{2I}(\frac{D^2}{4} - y^2)
\end{Bmatrix}\\
y = \pm \frac{D}{2}:\bm{\bar{t}} = \mathbf{0} \\
\bm{\bar{b}} = \mathbf{0}
\end{array}
\right .
$$

## Hollow cylinder under  inner and outer pressures

Displacement (plane stress)

$$
\left \{
\begin{array}{l}
u_{r} = \frac{1}{E(b^{2} - a^{2})}[(1-\nu)(a^{2}P_{i} - b^{2}P_{o})r + (1+\nu)\frac{a^{2}b^{2}(P_{i} - P_{o})}{r}] \\
u_{\theta} = 0
\end{array}
\right .
$$

Displacement (plane strain)

$$
\left \{
\begin{array}{l}
u_{r} = \frac{1+\nu}{E(b^{2} - a^{2})}[(1-2\nu)(a^{2}P_{i} - b^{2}P_{o})r + \frac{a^{2}b^{2}(P_{i} - P_{o})}{r}] \\
u_{\theta} = 0
\end{array}
\right .
$$

$$
\left \{
\begin{array}{l}
u = u_{r}\cos \theta = \frac{x}{r} u_{r}  \\
v = u_{r}\sin \theta = \frac{y}{r} u_{r} 
\end{array}
\right .
$$

Strain (plane stress)

$$
\begin{Bmatrix}
\varepsilon_{xx} \\ \varepsilon_{yy} \\ 2\varepsilon_{xy}
\end{Bmatrix} = 
\begin{Bmatrix}
u_{,x} \\ v_{,y} \\ u_{,y} + v_{,x}
\end{Bmatrix} 
= \frac{1}{E(b^{2} - a^{2})}
\begin{Bmatrix}
(1-\nu)(a^{2}P_{i} - b^{2}P_{o}) + (1+\nu)\frac{a^{2}b^{2}(P_{i} - P_{o})(y^2-x^2)}{r^4}\\
(1-\nu)(a^{2}P_{i} - b^{2}P_{o}) - (1+\nu)\frac{a^{2}b^{2}(P_{i} - P_{o})(y^2-x^2)}{r^4} \\
-(1+\nu)\frac{4a^{2}b^{2}(P_{i} - P_{o})xy}{r^4}
\end{Bmatrix}
$$

Strain (plane strain)

$$
\begin{Bmatrix}
\varepsilon_{xx} \\ \varepsilon_{yy} \\ 2\varepsilon_{xy}
\end{Bmatrix} = 
\begin{Bmatrix}
u_{,x} \\ v_{,y} \\ u_{,y} + v_{,x}
\end{Bmatrix} 
= \frac{1+\nu}{E(b^{2} - a^{2})}
\begin{Bmatrix}
(1-2\nu)(a^{2}P_{i} - b^{2}P_{o}) + \frac{a^{2}b^{2}(P_{i} - P_{o})(y^2-x^2)}{r^4}\\
(1-2\nu)(a^{2}P_{i} - b^{2}P_{o}) - \frac{a^{2}b^{2}(P_{i} - P_{o})(y^2-x^2)}{r^4} \\
-\frac{4a^{2}b^{2}(P_{i} - P_{o})xy}{r^4}
\end{Bmatrix}
$$

Stress

$$
\begin{split}
\begin{Bmatrix}
\sigma_{xx} \\ \sigma_{yy} \\ \sigma_{xy}
\end{Bmatrix} &=
\frac{E}{1-\nu^2}
\begin{bmatrix}
  1 & \nu & 0 \\
\nu &   1 & 0 \\
  0 &   0 & \frac{1-\nu}{2}
\end{bmatrix}
\begin{Bmatrix}
\varepsilon_{xx} \\ \varepsilon_{yy} \\ 2\varepsilon_{xy}
\end{Bmatrix} \\ &= \frac{1}{b^{2}-a^{2}}
\begin{Bmatrix}
a^{2}P_{i}-b^{2}P_{o}+\frac{a^{2}b^{2}(P_{i}-P_{o})(y^{2}-x^{2})}{r^{4}} \\
a^{2}P_{i}-b^{2}P_{o}-\frac{a^{2}b^{2}(P_{i}-P_{o})(y^{2}-x^{2})}{r^{4}} \\ 
-\frac{2a^{2}b^{2}(P_{i} - P_{o})xy}{r^4}
\end{Bmatrix}
\end{split}
$$

Traction

$$
\begin{Bmatrix}
\bar{t}_{x} \\ \bar{t}_{y}
\end{Bmatrix} = 
\begin{Bmatrix}
\sigma_{xx}n_{x} + \sigma_{xy}n_{y} \\
\sigma_{yx}n_{x} + \sigma_{yy}n_{y}
\end{Bmatrix} 
$$

Body force

$$
\bm{\bar{b}} = -
\begin{Bmatrix}
\sigma_{xx,x} + \sigma_{xy,y} \\
\sigma_{yx,x} + \sigma_{yy,y}
\end{Bmatrix} = \mathbf{0}
$$

Boundary condition

$$
\left \{
\begin{array}{l}
x = 0: u = 0, \; \bar{t}_{y} = 0 \\
y = 0: v = 0, \; \bar{t}_{x} = 0 \\
r = a: \bm{\bar{t}} = 
-\frac{P_{i}}{a}
\begin{Bmatrix}
x \\
y
\end{Bmatrix}\\
r = b: \bm{\bar{t}} = 
-\frac{P_{o}}{b}
\begin{Bmatrix}
x \\
y
\end{Bmatrix}\\
\bm{\bar{b}} = \mathbf{0}
\end{array}
\right .
$$

## Manufactorized solution for hollow cylinder problem

Displacement

$$
\begin{Bmatrix}
u \\ v \\ w 
\end{Bmatrix} = 
\begin{Bmatrix}
\sin(\pi \frac{r-r_{i}}{r_{o}-r_{i}}) f(z) \\ \sin(\pi \frac{r-r_{i}}{r_{o}-r_{i}}) f(z)  \\ g(z)
\end{Bmatrix}
$$

$$
\begin{Bmatrix}
\varepsilon_{11} \\ \varepsilon_{22} \\ \varepsilon_{33} \\ 2\varepsilon_{12} \\ 2\varepsilon_{13} \\ 2\varepsilon_{23}
\end{Bmatrix} =
\begin{Bmatrix}
u_{,x} \\ v_{,y} \\ w_{,z} \\ v_{,x} + u_{,y} \\ w_{,x} + u_{,z} \\ w_{,y} + v_{,z}
\end{Bmatrix} =
\begin{Bmatrix}
\frac{\pi x}{(r_{o}-r_{i})r}\cos(\pi \frac{r-r_{i}}{r_{o}-r_{i}}) f(z) \\
\frac{\pi y}{(r_{o}-r_{i})r}\cos(\pi \frac{r-r_{i}}{r_{o}-r_{i}}) f(z) \\
g'(z) \\
\frac{\pi (x+y)}{(r_{o}-r_{i})r}\cos(\pi \frac{r-r_{i}}{r_{o}-r_{i}}) f(z) \\
\sin(\pi \frac{r-r_{i}}{r_{o}-r_{i}}) f'(z) \\
\sin(\pi \frac{r-r_{i}}{r_{o}-r_{i}}) f'(z) \\
\end{Bmatrix}
$$

$$
\begin{split}
\begin{Bmatrix}
\sigma_{11} \\ \sigma_{22} \\ \sigma_{33} \\ \sigma_{12} \\ \sigma_{13} \\ \sigma_{23}
\end{Bmatrix} &= 
\frac{E}{(1+\nu)(1-2\nu)}
\begin{Bmatrix}
(1-\nu)\varepsilon_{11} + \nu \varepsilon_{22} + \nu \varepsilon_{33} \\
\nu\varepsilon_{11} + (1-\nu) \varepsilon_{22} + \nu \varepsilon_{33} \\
\nu\varepsilon_{11} + \nu \varepsilon_{22} + (1-\nu) \varepsilon_{33} \\
\frac{(1-2\nu)}{2}2\varepsilon_{12} \\ \frac{(1-2\nu)}{2}2\varepsilon_{13} \\ \frac{(1-2\nu)}{2}2\varepsilon_{23}
\end{Bmatrix} \\
&= \frac{E}{(1+\nu)(1-2\nu)}
\begin{Bmatrix}
\frac{\pi ((1-\nu)x + \nu y)}{(r_{o}-r_{i})r}\cos(\pi \frac{r-r_{i}}{r_{o}-r_{i}}) f(z) + \nu g'(z) \\
\frac{\pi (\nu x + (1-\nu)y)}{(r_{o}-r_{i})r}\cos(\pi \frac{r-r_{i}}{r_{o}-r_{i}}) f(z) + \nu g'(z) \\
\frac{\pi \nu (x + y)}{(r_{o}-r_{i})r}\cos(\pi \frac{r-r_{i}}{r_{o}-r_{i}}) f(z) + (1-\nu) g'(z) \\
\frac{(1-2\nu)}{2}\frac{\pi (x+y)}{(r_{o}-r_{i})r}\cos(\pi \frac{r-r_{i}}{r_{o}-r_{i}}) f(z) \\
\frac{(1-2\nu)}{2}\sin(\pi \frac{r-r_{i}}{r_{o}-r_{i}}) f'(z) \\
\frac{(1-2\nu)}{2}\sin(\pi \frac{r-r_{i}}{r_{o}-r_{i}}) f'(z) \\
\end{Bmatrix}
\end{split}
$$

$$
\sigma_{11,1} = \frac{E}{(1+\nu)(1-2\nu)}(\frac{\pi}{r_{o}-r_{i}} \frac{(1-\nu)y^2 - \nu xy}{r^3} \cos(\pi \frac{r-r_{i}}{r_{o}-r_{i}})
- \frac{\pi^2}{(r_{o}-r_{i})^2} \frac{(1-\nu)x^2 + \nu xy}{r^2} \sin(\pi \frac{r-r_{i}}{r_{o}-r_{i}})) f(z)\\
\sigma_{12,2} = \frac{E}{(1+\nu)(1-2\nu)}\frac{(1-2\nu)}{2}(\frac{\pi}{r_{o}-r_{i}} \frac{x^2-xy}{r^3}\cos(\pi \frac{r-r_{i}}{r_{o}-r_{i}})
- \frac{\pi^2}{(r_{o}-r_{i})^2}\frac{xy+y^2}{r^2}\sin(\pi \frac{r-r_{i}}{r_{o}-r_{i}})) f(z)\\
\sigma_{13,3} = \frac{E}{(1+\nu)(1-2\nu)}\frac{(1-2\nu)}{2}\sin(\pi \frac{r-r_{i}}{r_{o}-r_{i}}) f''(z)
$$

$$
\begin{split}
\begin{Bmatrix}
b_{1} \\ b_{2} \\ b_{3}
\end{Bmatrix} &= 
\begin{Bmatrix}
\sigma_{11,1} + \sigma_{12,2} + \sigma_{13,3} \\
\sigma_{21,1} + \sigma_{22,2} + \sigma_{23,3} \\
\sigma_{31,1} + \sigma_{32,2} + \sigma_{33,3}
\end{Bmatrix} \\
&= \begin{Bmatrix}
\end{Bmatrix}
\end{split}
$$

## Plate with a hole
Displacement

$$
\begin{Bmatrix}
\varepsilon_{11} \\ \varepsilon_{22} \\ \varepsilon_{33} \\ 2\varepsilon_{12} \\ 2\varepsilon_{13} \\ 2\varepsilon_{23}
\end{Bmatrix} =
\begin{Bmatrix}
u_{,x} \\ v_{,y} \\ w_{,z} \\ v_{,x} + u_{,y} \\ w_{,x} + u_{,z} \\ w_{,y} + v_{,z}
\end{Bmatrix} = 
\begin{Bmatrix}
u_{,x} \\ v_{,y} \\ w_{,z} \\ v_{,x} + u_{,y} \\ w_{,x} + u_{,z} \\ w_{,y} + v_{,z}
\end{Bmatrix}
$$

$$
\left \{
\begin{split}
u(r,\theta) &= \frac{Pr_{i}(1+\nu)}{2E}[\frac{r}{r_{i}}\frac{2}{1+\nu}\cos\theta + \frac{r_{i}}{r}(\frac{4}{1+\nu}\cos\theta + \cos3\theta) - \frac{r_{i}^{3}}{r^{3}}\cos3\theta] \\
v(r,\theta) &= \frac{Pr_{i}(1+\nu)}{2E}[-\frac{r}{r_{i}}\frac{2\nu}{1+\nu}\sin\theta - \frac{r_{i}}{r}(\frac{2-\nu}{1+\nu}\sin\theta + \sin3\theta) - \frac{r_{i}^{3}}{r^{3}}\sin3\theta]
\end{split}
\right .
$$
