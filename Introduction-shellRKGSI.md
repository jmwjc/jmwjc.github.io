
Thin shell structure is a typical class in engineering practice, amount of work has been developed for static and dynamic analysis[]. 
With the Kirchhoff assumption, the thin shell neglects the shear deformation, which leads to a membrane strain with second order difference of displacement. 
Accordingly, the $C^1$ continuity is require in Galerkin formulation, and the traditional finite element methods [] suffer a severe difficult and complex in shell formulation.
In last decades, the meshfree methods is grow fast, since it has high order smoothing shape function.
Thanks to its high order smoothing shape functions, meshfree methods is suitable for shell problems.
Among of them, reproducing kernel approximation and 
reproducing kernel approximation meets the reproducing consistency which severe a basis in accuracy analysis.
Meshfree methods is suitable for shell problems.

Galerkin meshfree methods use Gauss integration rule within weak form.
We partition the whole domain into background integration cell, and apply Gauss integration in each background cell.
Meshfree shape functions are non-polynomials.
Gauss integration is not suitable for integrating non-polynomial functions.
The supports of meshfree shape functions and the background integration cells do not have the coincide boundaries.
Meshfree shape functions are piecewise functions in each integration cell.
Gauss integration is designated for continuous functions.
The stiffness matrix and force vector can not exactly integrate with Gauss integration rule.
Higher order Gauss integration rule will lower the error caused by numerical integration, but it will also leads to a low efficiency.
Higher order Gauss integration still has integration error limit the accuracy of Galerkin methods.
Various numerical integration rules has been developed for meshfree numerical integration.
Among of them, a group of integration rules satisfy the so-call integration constraint, which said consistent integration rules.
This class of consistent integration rules can maintain optimal error convergence rate of meshfree formulations
Wu develop the relation between orthogonality and integration constraint.


Chen developed integration constraint condition, SCNI 
Duan developed QCI
Chen VCI
Wu NSGSI RKGSI

The developed consistent integration rules for Galerkin meshfree analysis are , and do not has a general standard decide how many order of integration consistency should be satisfied.

In this work, we proposed the error estimates of energy norm for shell problems, where the reproducing consistency and the integration consistency cooperatively limit the error convergence rate.

The remainder of this paper is organized as follows. Section 2 introduces the preliminaries about thin shell problems. Section 3 discusses the energy error estimate accounting to integration error. Section 4 develops a consistency integration rule for shell problems. The numerical examples is demonstrated the validity of our proposed methods in section 5. The conclusion is coming at the section 6.

