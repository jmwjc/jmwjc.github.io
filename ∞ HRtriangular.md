Based upon Hellinger-Reissner theory, the energy functional is given by
$$
\Pi(u) = \int_{\Omega} \frac{1}{2} u_{,i} u_{,i} d\Omega - \int_{\Gamma^g} u_{,i}n_i g d\Gamma
$$
the force boundaries and harmony conditions by Lagrangian multipler methods
$$
\Pi(u,u_{,i}) = \int_{\Omega} \frac{1}{2} u_{,i} u_{,i} d\Omega - \int_{\Gamma^g} u_{,i}n_i g d\Gamma
- \int_{\Gamma^t}u(u_{,i}n_i - t)d\Gamma + \int_{\Omega}u(u_{,ii}+b)d\Omega
- \sum_{C} \int_{\Gamma_C \setminus \Gamma}[uu_{,i}n_i]d\Gamma
$$
after the variational operation, we can obtain the weak form as
$$
\int_{\Omega} \delta u_{,i} u_{,i} d\Omega - \int_{\Gamma^g} \delta u_{,i}n_i g d\Gamma
- \int_{\Gamma^t}\delta u_{,i}n_i ud\Gamma + \int_{\Omega}\delta u_{,ii}ud\Omega
- \sum_{C} \int_{\Gamma_C \setminus \Gamma}[\delta u_{,i}n_i u]d\Gamma = 0
$$
$$
- \int_{\Gamma^t}\delta u(u_{,i}n_i - t)d\Gamma + \int_{\Omega}\delta u(u_{,ii}+b)d\Omega
- \sum_{C} \int_{\Gamma_C \setminus \Gamma}[\delta uu_{,i}n_i]d\Gamma = 0
$$
in which the displacement and its gradients are approximated by
$$
u^h = \sum_{I=1}^{n_p} N_I d_I
$$
$$
u_{,i}^h = \sum_{I=1}^{3} N_I a_{iI}, \quad \text{in} \; \Omega_C
$$
