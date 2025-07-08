---
{"dg-publish":true,"dg-path":"MATH/Adv Calc/Optimization.md","permalink":"/math/adv-calc/optimization/","created":"2024-11-04T11:05:49.292-05:00","updated":"2025-07-08T11:02:45.962-04:00"}
---

Using derivatives to locate maxima and minima of a surface

For a function $f:R^2\to R$, 
- $f(a,b)$ is the global maximum of $f$ if $f(x,y)\leq f(a,b)\forall(x,y)\in R^2$
- $f(a,b)$ is the global minimum of $f$ if $f(x,y)\geq f(a,b)\forall(x,y)\in R^2$

# Finding possible global extrema
Start with the interior of $D$
1. Find all critical points of $f$ existing on the interior of $D$
2. Evaluate $f$ at those points
Work on the boundary of $D$
3. Evaluate $f$ along the boundaries of $D$ to determine if there are any extrema there
4. Evaluate $f$ along any endpoints formed by the boundary of $D$
-  if there are no critical points ($\frac{d}{dx}\neq 0$ everywhere), then endpoints will be max/min of the line 
Conclusion
5. The global maximum is the biggest value found in 2-4, global minimum is the smallest value found in 2-4

# Lagrange Multipliers

Lagrangian function
$$
L(x,y,\lambda)=f(x,y)-\lambda g(x,y)
$$
Critical Points of the Lagrangian are found by solving $\nabla L=\tilde{0}$
- the scalar $\lambda$ is called the lagrangian multiplier (?)

Lagrangian can be extended to multiple constraints
$$
L(x_{1},x_{2},\dots,x_{n},\lambda_{1},\lambda_{2},\dots,\lambda _{n})=f(x_{1},\dots,x_{n})-\sum_{k=1}^n\lambda_{k}g_{k}(x_{1},\dots,x_{n})
$$
