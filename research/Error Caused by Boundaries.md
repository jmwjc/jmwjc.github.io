The following derivations of the error caused by boundaries, especially the comparison to interpolation errors. The main idea of derivation uses the standard polynomial with Galerkin method to make a clear sense about the errors.
Firstly, we consider the 2D potential problem listed follow:
$$
\int_\Omega v_{,i} u_{,i}^h d\Omega = \int_\Gamma v u_{i} n_i d\Omega - \int_\Omega v u_{,ii} d\Omega
$$
where the variables of $v$ and $u^h$ are used by a linear polynomials as:
$$
v = u^h = a_0 + a_1 \xi_1 + a_2 \xi_2
$$
and $u$ is the arbitrary high order polynomial:
$$
u = b_{ij} \xi_1^i \xi_2^j
$$

