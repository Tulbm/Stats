---
{"dg-publish":true,"dg-path":"STATS/Math Stats 1/Moments.md","permalink":"/stats/math-stats-1/moments/","created":"2024-11-05T16:37:05.823-05:00","updated":"2025-07-07T18:02:31.366-04:00"}
---

The *rth* moment of a [[1-Recent/Academics/STATS/Math Stats 1/Random Variables\|random variable]] $X$ ($\mu'$) is the expected value of $X^r$
$$
\begin{align}
\mu_{r}^{\prime}=E(X^{r})  =\sum_{x}x^{r}f(x) & \quad(discrete)\\ 
\mu_{r}^{\prime}=E(X^{r})  =\int_{-\infty}^{\infty}x^{r}f(x)dx & \quad(continuous)
\end{align}
$$
for $r=0,1,2\dots$
- $\mu_{0}'=E(X^0)=1$
- $\mu_{1}'=E(X)$, the mean
- $\mu_{2}'=E(X^2)$
### Central Moments
The *rth* moment about the mean of a random variable $X$ ($\mu _r$) is $E[(X-\mu)^r]$
$$
\begin{align}
\mu_r=E[(X-\mu)^r]=\sum_x(x-\mu)^r\cdot f(x) & \quad (discrete)\\
\mu_r=E[(X-\mu)^r]=\int_{-\infty}^\infty(x-\mu)^r\cdot f(x)dx & \quad(continuous)
\end{align}
$$
- $\mu_{0}$ =1 and $\mu_{1}=0$ provided that $\mu$ is a number ($|\mu|<\infty$)

The second central moment is the *variance* of $X$
$$
\text{var}(X)=\sigma^2=\mu_{2}=E[(X-\mu)^2]=E(X^2)-[E(X)]^2
$$
- $E(X^2-2X\mu + \mu^2)= E{(X^2)-2E(X)\mu+\mu^2}=E(X^2)-[E(X)]^2$ as $\mu=E[X]$
# Properties
$$
\text{var}(aX+b)=a^2[E(X^2)-[E(X)]^2]=a^2\sigma^2=a^2\text{var}(X)
$$
$$
var(aX+bY)=a^2var(X)+2ab\text{cov}(X,Y)+b^2var(Y)
$$
If $X$ and $Y$ are independent, the [[1-Recent/Academics/STATS/Math Stats 1/Covariance\|Covariance]] is 0, and the variance simplifies

[[1-Recent/Academics/STATS/Math Stats 1/Chebyshev's Theorem\|Chebyshev's Theorem]]

[[1-Recent/Academics/STATS/Math Stats 1/Moment Generating Functions\|Moment Generating Functions]]