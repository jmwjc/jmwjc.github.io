In meshfree approximation, a variable $u$ can be approximated by:
$$
u^h(\bm{x}) = \sum_{I=1}^{n_p} \Psi_I(\bm{x}) d_I
$$
where $\Psi_I$ and $d_I$ are the shape function and coefficients at node $\bm{x}_I$. The shape function is constructed to meet the fulfillment of consistency conditions:
$$
\sum_{I=1}^{n_p} \Psi_I(\bm{x}) \bm{p}(\bm{x}_I) = \bm{p}(\bm{x})
$$
or
$$
\sum_{I=1}^{n_p} \Psi_I(\bm{x}) \bm{p}(\bm{x}-\bm{x}_I) = \bm{p}(\bm{0})
$$
$$
\Psi_I(\bm{x}) = \bm{p}^T(\bm{x} - \bm{x}_{I}) \bm{c}(\bm{x}) \phi(\bm{x} - \bm{x}_{I})
$$
