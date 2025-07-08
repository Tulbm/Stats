---
{"dg-publish":true,"dg-path":"STATS/Intro to Stats/Negative Binomial Distribution.md","permalink":"/stats/intro-to-stats/negative-binomial-distribution/","created":"2024-04-14T19:01:13.473-04:00","updated":"2025-07-07T17:21:02.413-04:00"}
---

[[Academics/STATS/Intro to Stats/Binomial Distribution\|Binomial Distribution]] until a set number of successes occur
- [[Academics/STATS/Intro to Stats/Bernoulli Trials\|independent trials]] (with replacement)
# Probability Distribution Function
A random variable $X$ has a negative binomial distribution $X\sim NB(k,p)$ if and only if it has the pdf
$$
f(x;k,p)={x-1\choose k-1}p^k(1-p)^{x-k}
$$
for $x\geq k$
1. $f(x)\geq 0$
2. $\sum_{x=k}^\infty f(x)=\sum_{x=k}^\infty{x-1\choose k-1}p^k(1-p)^{x-k}=1$

- k = number of successes
- $x=$ number of failures before the kth success
- $k-1$ as the last success is already set at last spot

$$E|X|=\frac{k(1-p)}{p} / \frac{k}{p}??$$
$$
\sigma^2=\frac{k}{p}\left( \frac{1}{p}-1 \right)
$$

$$f(x;k,p)=\binom{x+k-1}xp^k(1-p)^x$$