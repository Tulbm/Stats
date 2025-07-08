---
{"dg-publish":true,"dg-path":"CIS/Discrete Structures/Discrete Distributions.md","permalink":"/cis/discrete-structures/discrete-distributions/","created":"2024-03-29T19:13:31.371-04:00","updated":"2025-07-08T10:47:55.409-04:00"}
---

# [[1-Recent/Academics/STATS/Math Stats 1/Discrete Uniform Distribution\|Discrete Uniform Distribution]]
- $f(x)=\frac{1}{b-a+1}$
- $f(x)=$ pdf
	- probability that we get x = function
# [[1-Recent/Academics/STATS/Intro to Stats/Hypergeometric Distribution\|Hypergeometric Distribution]]
- without replacement
- $f(x)=\frac{\binom rx\binom{N-r}{n-x}}{\binom Nn}$
	- $N =$ total, $n =$ sample size, $x =$ target, $r=$ group we choose x from
- expectation
	- $E[X]=\left( \frac{r n}{N} \right)$
		- expectation of the value of X in a group of size n
# [[1-Recent/Academics/STATS/Intro to Stats/Binomial Distribution\|Binomial Distribution]]
- independent trials/with replacement
- $f(x)=\binom nxp^x(1-p)^{n-x}$
	- n = total, x = number of successes, p = probability of success
- expectation
	- $np$
# [[1-Recent/Academics/STATS/Intro to Stats/Negative Binomial Distribution\|Negative Binomial Distribution]]
- binomial until a set number of successes occur
	- independent trials/with replacement
- $f(x)=\binom{x+k-1}xp^k(1-p)^x$
	- k = number of successes
	- $x=$ number of failures before the kth success
	- $k-1$ as the last success is already set at last spot
- expectation
	- $E|X|=\frac{k(1-p)}{p}$ 
# [[1-Recent/Academics/STATS/Intro to Stats/Poisson Distribution\|Poisson Distribution]]
- $f(x)=e^{-\mu}\frac{\mu^x}{x!},x=0,1,2,...$
- $P(X=x)=\frac{\lambda
{ #xe}
^{-\lambda}}{x!}$
- $\mu = E(X)$, use $E(X)$ formula from
- conditions of a poisson
	- independence
		- number of occurrences in non-overlapping intervals need to be independent
	- individuality
		- events can only have one occurrence at a time 
		- for sufficiently short time periods of length $\Delta t$, the probability of 2 or more events occurring in the interval is close to zero i.e. events occur singly not in clusters. More precisely, as $\Delta t\to0$, the probability of two or more events in the interval of length $\Delta t$ must go to zero faster than $\Delta t\to0$
	- uniformity
		- events occur at a uniform or homogenous rate $\lambda$ over time so that the probability of one occurrence in an interval $(\vec{t},t+\Delta t)$ is approximately $\lambda\Delta t$ for any value of t





