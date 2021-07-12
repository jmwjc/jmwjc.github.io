# Mixed formulation
Condier the following elliptic variational problem:

$$
\begin{equation}
J(v) = \frac{1}{2} a(v,v) - f(v)
\end{equation}
$$

We now verify that boundary value problem is equivalent to minimization problem, yeilds:

$$
\begin{equation}
\begin{split}
J(u+v) &= \frac{1}{2}a(u+v,u+v) - f(u+v) \\
&= \frac{1}{2}a(u,u) - f(u) + a(v,u) - f(v) + \frac{1}{2}a(v,v) \\
&= J(u) + a(v,u) - f(v) + \frac{1}{2}a(v,v)
\end{split}
\end{equation}
$$

$$
\begin{equation}
L(v,q) = J(v) + b(v,q) - g(q)
\end{equation}
$$

$$
\begin{equation}
\begin{split}
L(u+v,p) &= J(u+v) + b(u+v,p) - g(p) \\
&= J(u) + a(v,u) - f(v) + b(u,p) -g(p) + b(v,p) + \frac{1}{2}a(v,v)\\
&= L(u,p) + a(v,u) - f(v) + b(v,p) + \frac{1}{2}a(v,v)
\end{split}
\end{equation}
$$

$$
\begin{equation}
\begin{split}
L(u,p+q) &= J(u) + b(u,p)+b(u,q)-g(p)-g(q)\\
&= L(u,p) + b(u,q) - g(q)
\end{split}
\end{equation}
$$
