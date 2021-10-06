---
Topic:
Status: 📝 🟥
Manager: WuJC
Next: Derive Jacobi 

---
`ris:Links`: [[∞ Local Error Segment and Triangle]]
`ris:Calendar2`: <%+ tp.file.last_modified_date() %>
`ris:Edit2`:

---

Consider a triangular cell $\Omega$ with vertices of $\bm{x}_1, \bm{x}_2, \bm{x}_3$, a new parametric configuration is designated as:
$$
\xi_1 + \xi_2 + \xi_3 = 1
$$
and an arbitrary point $\bm{x}$ in this triangular domain can be express by a linear parametric coordinate configuration as:
$$
\bm{x} = \bm{a}_1 \xi_1 + \bm{a}_2 \xi_2 + \bm{a}_3 \xi_3
$$
where $a_i$'s are the coefficients related to vertices $\bm{x}_i$'s. These coefficients are determined by following relationship:
$$
\int_{\Gamma_i} \bm{x} d\Gamma = \int_{\Gamma_i} \bm{a}_1 \xi_1 + \bm{a}_2 \xi_2 + \bm{a}_3 \xi_3 d\Gamma
$$
or
$$
\bm{a}_i = \frac{1}{L_i} \bm{m}_i
$$
where
$$
\bm{m}_i = \int_{\Gamma_i} \bm{x} d\Gamma
$$
$$
\left \{
\begin{aligned}
    \bm{m}_1 &= \frac{L_1}{2}(\bm{x}_2 + \bm{x}_3) \\
    \bm{m}_2 &= \frac{L_2}{2}(\bm{x}_3 + \bm{x}_1) \\
    \bm{m}_3 &= \frac{L_3}{2}(\bm{x}_1 + \bm{x}_2)
\end{aligned}
\right .
$$

#❗️ equivalent to traditional Lagrangian interpolation
