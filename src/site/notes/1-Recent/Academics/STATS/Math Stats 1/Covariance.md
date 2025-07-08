---
{"dg-publish":true,"dg-path":"STATS/Math Stats 1/Covariance.md","permalink":"/stats/math-stats-1/covariance/","created":"2024-11-12T17:49:16.001-05:00","updated":"2025-07-07T18:02:31.300-04:00"}
---

The covariance of $X$ and $Y$ is the  [[1-Recent/Academics/STATS/Math Stats 1/Product of Moments\|Product of Moments]] about the mean
$$\begin{align}
\sigma_{XY}=cov(X,Y) & =E((X-\mu_{X})(Y-\mu_{Y})) \\
 & =E(XY) -E(X)\mu_{Y}-\mu_{X}E(Y)+\mu_{X}\mu_{Y} \\
 & =E(XY)-\mu_{X}\mu_{Y}  \\
 & =E(XY)-E(X)E(Y)
\end{align}
$$
Which is useful for calculating the variance of [[1-Recent/Academics/STATS/Math Stats 1/Independency#Measures\|independent]] variables
$$
\begin{align} 
Var(X+Y) & =E[(X+Y)^2] -[E(X+Y)]^2\\
& =E(X^2)+2E(XY)+E(Y^2)-\left( [E(X)]^2 +2E(XY)+[E(Y)]^2\right) \\
 & =Var(X)+Var(Y)+2E(XY)-2E(X)E(Y) \\
 Var(X+Y) & =Var(X)+Var(Y)+2cov(X,Y)
\end{align}
$$

Covariance measures the relation between the variables
- Expectations are inversely related when covariance is negative, and directly related when it is positive
- negative $\to$ positive change in $X\to$ negative change in $Y$ 