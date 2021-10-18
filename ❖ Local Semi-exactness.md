---
Topic: localerror
Status: 📝 🟩
Manager: WuJC
Next:
---
`ris:Links`:
`ris:Calendar2`: <%+ tp.file.last_modified_date() %>
`ris:Edit2`:

---

$$
\min \int_\Omega (v_{,i}^h - f_{,i}(u)) \cdot (v_{,i}^h - f_{,i}(u)) d\Omega
$$
$$
\begin{aligned}
    v^h &= (\xi_2 + \xi_3 - \xi_1) d_1 \\
    &+ (\xi_3 + \xi_1 - \xi_2) d_2 \\
    &+ (\xi_1 + \xi_2 - \xi_3) d_3
\end{aligned}
$$
$$
\begin{aligned}
    x &= \xi_1 x_1 + \xi_2 x_2 + \xi_3 x_3 \\
    y &= \xi_1 y_1 + \xi_2 y_2 + \xi_3 y_3
\end{aligned}
$$
$$
u = \sum_{i+j = 0}^n a_{ij} \xi_1^i \xi_2^j
$$
$$
\begin{aligned}
    u_1 &= \sum_{i=0}^n a_{0i}\xi_2^i \\
    u_2 &= \sum_{i=0}^n a_{i0}\xi_1^i \\
    u_3 &= \sum_{i+j = 0}^n a_{ij} \xi_1^i (1-\xi_1))^j
\end{aligned}
$$
$$
u_{,i} = \sum_{I = 1}^{\infty} P_I p_I
$$
$$
p_I = \int_{\Gamma} P_I u_{,i} d\Gamma
$$
