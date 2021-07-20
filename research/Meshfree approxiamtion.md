In meshfree approximation, a variable $u$ can be approximated by:
$$
u^h(\boldsymbol{x}) = \sum_{I=1}^{n_p} \Psi_I(\boldsymbol{x}) d_I
$$
where $\Psi_I$ and $d_I$ are the shape function and coefficients at node $\boldsymbol{x}_I$. The shape function is constructed to meet the fulfillment of consistency conditions:
$$
\sum_{I=1}^{n_p} \Psi_I(\boldsymbol{x}) \boldsymbol{p}(\boldsymbol{x}_I) = \boldsymbol{p}(\boldsymbol{x})
$$
or
$$
\sum_{I=1}^{n_p} \Psi_I(\boldsymbol{x}) \boldsymbol{p}(\boldsymbol{x}_I-\boldsymbol{x}) = \boldsymbol{p}(\boldsymbol{0})
$$
$$
\Psi_I(\boldsymbol{x}) = 