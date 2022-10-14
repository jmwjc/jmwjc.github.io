## 章节描述
- In this section, a series of numerical tests **ranging from** 1D to 3D are performed to verify the proposed methodology.
- In order to **validate** the proposed accuracy measures for Galerkin meshfree formulation, this Section presents a series of numerical examples which employ

## 描述模型
- The last example is the hollow sphere elasticity problem **depicted** in Fig. 34.
- To further assess the proposed theoretical results, a 3D cubic domain potential problem as shown in Fig. 22 is investigated.
### 几何、材料描述
- The dimensionless geometric and material parameters for this problem are: length
- This hollow cylinder has a height of L = 1 and its inner and outer radii are r i= 1 and r o= 2.

### 边界条件
- As for the boundary conditions **computed from the analytical solution**, the three surfaces of x = 0, y = 0 and y = 0 **are subjected to** the prescribed field variable values, while the rest three surfaces **are under** the prescribed boundary fluxes.
- On the boundary surfaces of x = 0, y = 0, z = 0, essential boundary conditions are applied and the natural boundary conditions are imposed on the rest of surfaces.
- The prescribed boundary values and the source term of this problem is computed according to **following manufactured exact solution**:
- Under the plane stress condition, the analytical solution for this problem  is:
- During the computation, by taking the symmetry advantage, only a finite-size quarter model is analyzed, exact displacement and symmetric boundary conditions are enforced as shown in Fig. 18.
- where the left and the bottom sides are Neumann boundaries, and the right and the top sides are essential boundaries.
- Due to the symmetry, a quarter hollow cylinder is modeled, where natural boundary conditions are applied at x = 0, y = 0, and the rest of surfaces are subjected to essential boundary conditions.
- is subjected to
- 
## 描述离散
- For this problem, meshfree discretizations with 11, 21, 41, 81, 161, and 321 nodes are employed for the convergence study. The normalized support sizes of 2.5 and 3.5 are utilized for the quadratic and cubic meshfree formulations, respectively.
- As shown in Fig. 20, the meshfree discretizations with 5 × 5 × 5, 9 × 9 × 9 and 17 × 17 × 17 nodes are used for the meshfree computation, where normalized support sizes of 2.5 and 3.5 **are employed for** the quadratic and cubic approximation, respectively.
- Six progressively refined meshfree discretizations with 6 × 6, 11 × 11, 21 × 21, 41 × 41, 81 × 81 and 161 × 161 nodes are employed for the convergence assessment of this problem, where the first three discretizations are listed in Fig. 13.
- In the quadratic and cubic meshfree methods, normalized support sizes of 2.5 and 3.5 are adopted for the kernel function.
- The non-uniform meshfree discretizations with 153, 561 and 2145 nodes are illustrated in Fig. 26. For quadratic and cubic basis functions, the normalized support sizes of kernel function **are set to be** 2.7 and 3.8, respectively.
- Due to the three-fold symmetry, only one-eighth of the hollow sphere is modeled and the corresponding nonuniform meshfree discretizations with 113, 428 and 2170 nodes are shown in Fig. 35. The quadratic and cubic meshfree formulations employ normalized support sizes of 2.1 and 3.1 for the kernel function, respectively.
- Meshfree discretizations of 5 × 5 × 5, 7 × 7 × 7, 9 × 9 × 9, 13 × 13 × 13, 17 × 17 × 17, and 25 × 25 × 25 nodes are adopted for the convergence analysis of Galerkin meshfree methods, where the first three node distributions are plotted in Fig. 23.
- For this elastic plate with a circular hole problem, non-uniform meshfree discretizations using 104, 362, 1373, 5345 and 21 089 nodes are utilized for the convergence study, where the first three progressively refined discretizations **are portrayed in** Fig. 19.
- The quadratic basis function with a normalized support size of 2.1 is employed to construct meshfree shape functions.
- The normalized support sizes are 2.1 and 3.1 for quadratic and cubic meshfree formulations.
- The normalized support size of cubic meshfree shape functions is set to be 3.1.

## 说明图例
- Figs. 8–11 present the convergence results referring to the L 2and H 1error norms, where the horizontal axis “s” denotes the support size, and the dashed lines illustrate the numerical CR.
- The convergence results of this 2D square domain potential problem are plotted in Figs. 14 and 15 for the quadratic meshfree formulation, and Figs. 16 and 17 for the cubic meshfree formulation, respectively.
- **The results regarding both convergence and efficiency** are listed in Figs. 16–19, where GI-4, GI-14, NSGSI, QCI and RKGSI are adopted for the quadratic meshfree formulation, and GI-6, GI-16 and the present RKGSI are employed the cubic meshfree formulation, respectively.
- For the efficiency comparisons in Figs. 17 and 19, CPU cost vs. number of particles as well as L 2 error vs. CPU cost are examined.
- 
## 详细描述
- Similar to the previous 1D results, it is apparent from Figs. 14 and 15 that the results of GI-3 and GI-6 are completely governed by the integration errors, even GI-13 only produces better convergent results for very coarse discretizations, and this convergence is lost with refined discretizations.
- It is evident that the Gauss integration rules, such as GI-2, GI-4 and GI-8 for quadratic formulation and GI-3, GI-6 and GI-9 for cubic formulation, could not produce the expected optimal convergence rates for L 2 and H 1 error norms, namely, 3 and 2 for the quadratic case and 4 and 3 for the cubic case, respectively.
- The convergence results of $L_2$ and $H_1$ error are presented in Figs. The results **clearly show that** the conventional Gauss quadrature based meshfree formulations cannot achieve the optimal convergence rates for both quadratic and cubic basis functions, **even though** higher order integration rules of GI-5 and GI-9 are used.
- It is also noted that NSGSI and QCI **yield similar convergence results as** RKGSI for the quadratic meshfree formulation, but the proposed RKGSI **is more preferable due to** its higher efficiency as shown in Fig. 17. Moreover, in Fig. 19 **the efficiency superiority of** RKGSI **is also well demonstrated for** the cubic meshfree formulation.
- The higher efficiency of RKGSI is because it does not involve the derivative computation whose cost grows dramatically with the elevation of basis orders.
- For the cubic case as listed in Figs. 16 and 17, all three GI methods including GI-6, GI-12 and GI-16 **are not capable of** achieving optimally convergent results.
- Figs. 16–17 **also indicate that** the convergence rates of all numerical results by GI’s are approximately 1.5 for L 2-error and 0.5 for H 1-error, no matter what meshfree basis functions and GI quadrature rules are used.

## 验证观点
- These observations can be explained by the inequalities of
- Consequently, following the inequalities of (62) and (70) as well as Table 1, it turns out that the solution errors of GI’s are dominated by the integration error rather than the interpolation error.
- Therefore, the solutions computed by GI’s are eventually controlled by the integration errors because these methods violate the integration consistency condition or integration constraint.
- This is **perhaps due to the fact that** the proposed theoretical development of error estimates relies on the conventional polynomial assumption and the meshfree shape functions actually are rational.
- **This observation is also revealed by** the interpolation error estimate of (28), i.e., the interpolation order is often slightly higher than the basis degree in practice
- Thus, as shown in Figs. 8–11, optimal convergence results regarding both L 2and H 1error norms are achieved by RKGSI, which **fully agree with** the theoretical results in Table 1.
- These results **closely follow** the theoretical predictions in Table 1, which gives 1 and 0 for the slopes of L 2 and H1  errors because GI’s do not meet the integration consistency and q = 0.
- this is supported by
- is consistent with observation from
- this indicates a good agreement between
- identical conclusions were obtained in studies
- coincide with
- in accord with
- agree in

## 粗略概括
### 正面描述
- Among the different methods, the convergence results in Figs. 16 and 18 **systematically exhibit the optimal convergence behavior** of RKGSI.
- The convergence and efficiency results for this 3D potential problem **are summarized in** Figs. 21–24, as consistently evince **the superior performance of the proposed method of RKGSI regarding convergence rates**, accuracy as well as efficiency, compared with the 3D normal Gauss integration rules of GI-4 and GI-11, and the higher order Gauss integration rules of GI-14 and GI-20 for the quadratic and cubic meshfree formulations.
- In contrast, optimal rates of convergence can be achieved by the methods of QCI, NSGSI and the present RKGSI, while RKGSI outperforms other methods when the efficiency is taken into account. 
- Figs. 29 and 30 provide the results for cubic meshfree formulation, as also well testify that the present RKGSI performs superiorly compared with both GI-6 and GI-16.
- The convergence results in Figs. 36 and 38 manifest that optimal convergence rates are consistently attained by the proposed RKGSI for both quadratic (p = 2) and cubic (p = 3) meshfree approximations, which are 3 and 4 for the L 2error, and 2 and 3 for the H 1error, respectively.
- Meanwhile, the numerical results of RKGSI in Figs. 14–17 unanimously support the optimal convergence rates of Galerkin meshfree methods listed in Table 1, namely, (p + 1) and p with respect to L 2 and H 1 errors.
- Meanwhile, the theoretically expected optimal convergent rates for L 2 and H 1 errors are congruently produced by RKGSI for this 3D hollow cylinder potential problem using non-uniform meshfree discretizations.
- A direct comparison in Figs. 20 and 21 shows that optimal convergence rates of 3 and 2 are ensured by RKGSI for both L 2 and H 1 error norms.
- In contrast to GI’s, as demonstrated in Figs. 24–27, RKGSI has the inherent property of integration consistency and yields optimally convergent results for both L 2 and H 1 errors, which signifies the importance of integration consistency for Galerkin meshfree analysis.

### 负面描述
- It can be clearly seen that the convergence rates of GI’s are far below the optimal convergence rates, namely, 4 for the L 2-error and 3 for the H 1-error.
- The results for quadratic meshfree formulation are presented in Figs. 27 and 28, which show that for this problem with non-uniform discretizations, the normal rule of GI-4 even cannot ensure the convergence and the higher order rule like GI-13 still yields pretty low convergence rates.
- The convergence results are presented in Fig. 20 for the L 2-error and in Fig. 21 for the H 1 -error, which again confirm that GI’s lose the optimal convergence and this issue cannot **be well remedied by** just increasing the number of Gauss integration points.
- The convergence results for this 3D cubic domain potential problem are given in Figs. 24–27, which reveal that for both quadratic and cubic meshfree formulations, high order Gauss integration rules such as GI-14 and GI-20 exhibit the same convergence behaviors as the relatively lower order rules GI-4 and GI-11 for quadratic and cubic cases, since all of them **fail to meet** the integration consistency condition.
- Once again, the results produced by GI-11, GI-14 and GI-20 show the same convergence trends as the meshfree models are progressively refined, which agree with the theoretical results stated in Table 1 and further assert that the convergence characteristics of meshfree formulation with GI’s are deteriorated by the integration error.