
简支方板的精确解为:

板面内的纵向荷载:
$$
\bar q=-\bar D(\frac{\pi^2}{a^2}+\frac{\pi^2}{b^2})\sin(\frac{\pi}{a}x)\sin(\frac{\pi}{b}y)
$$

$$
w=-\sin(\frac{\pi}{a}x)\sin(\frac{\pi}{b}y)
$$
其中$a=1,b=1$，抗弯刚度$\bar D=1$,泊松比$\nu=0.3$

挠度方程的求导:
$$
\begin{align}
w_{,1}&=-\cos(\pi x)\pi \sin(\pi y)\\
w_{,2}&=-\sin(\pi x)\pi \cos(\pi y)\\
w_{,11}&=\pi^2 \sin(\pi x)\sin(\pi y)\\
w_{,22}&=\pi^2\sin(\pi x)\sin(\pi y)\\
w_{,12}&=-\pi^2\cos(\pi x)\cos(\pi y)\\
w_{,111}&=\pi^3\cos(\pi x)\sin(\pi y)\\
w_{,112}&=\pi^3\sin(\pi x)\cos(\pi y)\\
w_{,122}&=\pi^3\cos(\pi x)\sin(\pi y)\\
w_{,222}&=\pi^3\sin(\pi x)\cos(\pi y)\\
w_{,111}&=\pi^3\cos(\pi x)\sin(\pi y)\\
w_{,1111}&=-\pi^4\sin(\pi x)\sin(\pi y)\\
w_{,1122}&=-\pi^4\sin(\pi x)\sin(\pi y)\\
w_{,2222}&=-\pi^4\sin(\pi x)\sin(\pi y)\\
\end{align}
$$




转角$\bar\theta_n$
$$
\bar\theta_n=w_{,\bm{n}}=w_{,1}n_{1}+w_{,2}n_2
$$
弯矩：
$$
\begin{align}
\left\{\begin{matrix}
M_{11}\\
M_{22}\\
M_{33}
\end{matrix}\right\}&=D
\left[\begin{matrix}
1&\nu&0\\
\nu&1&0\\
0&0&\frac{1-\nu}{2}
\end{matrix}\right]
\left\{\begin{matrix}
w_{,11} \\ w_{,22} \\ 2w_{,12}
\end{matrix}\right\}\\&=
\left\{\begin{matrix}
Dw_{,11} + \nu w_{,22}\\
D \nu w_{,11} + w_{,22}\\
(1-\nu) w_{,12}
\end{matrix}\right\}
\end{align}
$$


弯矩$\bar M_{nn}$：
$$
\bar M_{nn}=M_{nn}=M_{11}n_1n_1+M_{22}n_2n_2+2M_{12}n_1n_2
$$
角点处$P_j=\bar P_j\quad j=1,2,3 \dots$：
$$
P_j=M_{12}(s_1^1n_2^1-s_1^2n_2^2)
$$
边界条件：
$y = 0,s_1 = 1,s_2 = 0,n_1 = 0,n_2 = -1$:
$$
\begin{cases}
w = - \sin(\pi x) \sin(\pi y) = 0 \\
\theta_{\bm{n}} = w_{,1} n_1 + w_{,2} n_2 = \sin(\pi x) \\
w_k = 0 \\
M_{\bm{nn}} = M_{22} = D(\nu w_{,11} + w_{,22}) = 0 \\
\end{cases}
$$
