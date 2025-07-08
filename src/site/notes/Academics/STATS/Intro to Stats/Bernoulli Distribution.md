---
{"dg-publish":true,"dg-path":"STATS/Intro to Stats/Bernoulli Distribution.md","permalink":"/stats/intro-to-stats/bernoulli-distribution/","created":"2024-03-29T19:02:39.583-04:00","updated":"2025-07-07T17:21:02.150-04:00"}
---

- [[Academics/STATS/Intro to Stats/Binomial Distribution\|Binomial Distribution]] with only a single [[Academics/STATS/Intro to Stats/Bernoulli Trials\|trial]]
# Probability Distribution Function
A random variable $X$ has a Bernoulli distribution, denoted by $X\sim Bernoulli(p)$ if and only if it has the probability distribution function as
$$
f(x)= p^x(1-p)^{1-x} \quad \quad \text{ for }x=0,1
$$
where $p=P(X=1)$

$$
E(X)=\sum_{x}xf(x)=p
$$
$$\begin{align}
Var(X) & =E(X^2)-[E(X)]^2 \\
 & =p-p^2 \\
 & =p(1-p) \\
\end{align}
$$