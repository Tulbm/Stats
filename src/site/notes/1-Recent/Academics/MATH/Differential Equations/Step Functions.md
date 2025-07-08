---
{"dg-publish":true,"dg-path":"MATH/Differential Equations/Step Functions.md","permalink":"/math/differential-equations/step-functions/","created":"2024-11-08T15:10:26.910-05:00","updated":"2025-07-08T11:02:52.871-04:00"}
---

Used in [[1-Recent/Academics/MATH/Differential Equations/Differential Equations\|Differential Equations]] that have discontinuities on the right hand side

Heaviside Step Function
$$
u(t)=\begin{cases}
0, \quad t<0 \\
1, \quad t\geq 0
\end{cases}
$$
For a constant $a$:
$$
u(t-a)=\begin{cases}
0,\quad  t-a<0 \\
1,\quad t-a\geq 0
\end{cases} = \begin{cases}
0, \quad t<a \\
1, \quad t\geq a
\end{cases}
$$
- denoted $H(t-a)$ or $u_{a}(t)$

[[1-Recent/Academics/MATH/Differential Equations/Laplace Transforms\|Laplace Transforms]] of the Heaviside Function
$$
\mathcal{L}\{u(t-a)\} = \int_0^\infty e^{-st}u(t-a)dt =\frac{e^{-sa}}{s}
$$
