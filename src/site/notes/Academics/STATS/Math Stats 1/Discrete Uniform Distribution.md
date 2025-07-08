---
{"dg-publish":true,"permalink":"/academics/stats/math-stats-1/discrete-uniform-distribution/","created":"2024-11-14T16:14:37.768-05:00","updated":"2025-07-07T18:02:31.305-04:00"}
---

A random variable $X$ has a discrete uniform distribution iff each possible value of $X$ is equally likely
$$
f(x)=\frac{1}{k}\quad \quad \text{for }x=x_{1},x_{2},\dots,x_{k}
$$
where no 2 values are the same

$$\begin{align}
E(X) & =\sum _{x}xf(x)  \\
 & =\sum_{x=1}^n x \frac{1}{n} \\
 & = \frac{1}{n} \frac{n(n+1)}{2} \\
 \mu& =\frac{n+1}{2}
\end{align}
$$

$$\begin{align}
Var(X) & =E(X^2)-[E(X)]^2 \\
 & = \frac{1}{n}\sum_{x=1}^nx^2 -\left( \frac{n+1}{2} \right)^2 \\
 & =\frac{1}{n} \frac{n(n+1)(2n+1)}{6} - \left( \frac{n+1}{2} \right)^2 \\
 \sigma^2& =\frac{n^2-1}{12}
\end{align}
$$

