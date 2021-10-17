---
Topic:
Status: 📝 🟩
Manager:
Next:
---
`ris:Links`:
`ris:Calendar2`: <%+ tp.file.last_modified_date() %>
`ris:Edit2`:

---

$$
\Pi(u) = \int_\Omega \frac{1}{2}\sigma \varepsilon d\Omega - \int_{\Gamma^t} ut d\Gamma - \int_\Omega ub d\Omega 
$$
$$
\bar{\Pi}(u,\sigma) = \Pi(u,\sigma) - \int_\Omega \frac{1}{2}\sigma(\frac{\sigma}{EA} - \varepsilon) d\Omega - \int_{\Gamma^g} \sigma n (u-g)d\Gamma
$$
$$
\delta \bar{\Pi}(u,\sigma) = \int_\Omega \delta \sigma \varepsilon d\Omega + \int_\Omega \delta \varepsilon \sigma d\Omega - \int_\Omega \frac{1}{EA} \delta \sigma \sigma d\Omega - \int_{\Gamma^t} \delta u t d\Gamma - \int_\Omega \delta u b d\Omega - \int_{\Gamma^g} \delta \sigma n (u-g) d\Gamma - \int_{\Gamma^g} \delta u \sigma n d\Gamma
$$
$$
u = \sum_{I = 1}^{n_p} N_I u_I, \quad u_{,x} = \sum_{I = 1}^{n_p} B_I u_I, \quad \sigma = \sum_{K = 1}^{n_q} N_I^s \sigma_I
$$
$$
\begin{bmatrix}
    0 & \int_\Omega B_I N_L^s d\Omega - \int_{\Gamma^g} N_I N_L^s n d\Gamma \\
    \int_\Omega N_K^s B_J d\Omega - \int_{\Gamma^t} N_K^s N_J n d\Gamma & - \int_\Omega \frac{1}{EA} N_K^s N_L d\Omega
\end{bmatrix}
\begin{Bmatrix}
    u_J \\ \sigma_L
\end{Bmatrix} = 
\begin{Bmatrix}
    \int_{\Gamma^t} N_I t d\Gamma + \int_\Omega N_I b d\Omega \\
    - \int_{\Gamma^g} N_K^s g n d\Gamma
\end{Bmatrix}
$$
