---
Topic:handbook
Status: 📝 🟩
Manager: WuJC, WuXY
Next: Finish all sections

---
`ris:Links`:
`ris:Calendar2`: <%+ tp.file.last_modified_date() %>
`ris:Edit2`:

---

# 一维伽辽金法
## 拉压杆问题
不是一般性，考虑如图所示一维拉压杆问题，其中杆长为$L$，杆件的拉压刚度为$EA$，$E$为杨氏模量，$A$为杆件横截面积。杆件左端固定，右端受到外力$t$的作用，同时在单位杆件内部施加体力$b$。此时，该杆在外力荷载下位移的微分控制方程为：
$$
\left \{
\begin{array}{ll}
    EAu_{,xx} + b = 0 & x \in (0,L) \\
    u = 0             & x = 0 \\
    EAu_{,x} = t      & x = L \\
\end{array}
\right .
$$
上式在伽辽金法中也称为强形式(strong form)。
## 伽辽金法与加权残值法
## 伽辽金法与最小势能原理
## 伽辽金法与最小二乘法
## [一维有限元程序](file:///~/program/fem1d/main.jl)