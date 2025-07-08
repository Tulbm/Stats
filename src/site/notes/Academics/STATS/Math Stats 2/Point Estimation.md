---
{"dg-publish":true,"dg-path":"STATS/Math Stats 2/Point Estimation.md","permalink":"/stats/math-stats-2/point-estimation/","created":"2025-01-23T12:30:31.529-05:00","updated":"2025-07-07T17:32:42.509-04:00"}
---

Using a point estimator $\hat{\theta}$ to estimate $\theta$
$$
P(\hat{\theta}=\theta)=0
$$
Suppose a random sample $X_{1},\dots,X_{n}$ is collected from a population and it is assumed that $X_i\overset{iid}{\sim}f(x;\theta)$ 
Let the estimator of $\theta$ be $\hat{\theta}=\hat{\theta}(X_{1},\dots,X_{n})$ be a function of $X_{i}'$s meant to estimate $\theta$

[[Academics/STATS/Math Stats 2/Finding point estimators\|Finding point estimators]]
# Evaluation
Properties of a good estimator:
1. [[Academics/STATS/Math Stats 2/Unbiasedness\|Unbiasedness]]: $E(\hat{\theta})=E(\hat{\theta}(X_{1},\dots,X_{n}))=\theta$
2. [[Academics/STATS/Math Stats 2/Efficiency\|Efficiency]]: $var(\hat{\theta}(X_{1},\dots,X_{n}))$ is as small as possible (more efficient per sample size)
3. [[Academics/STATS/Math Stats 2/Consistency\|Consistency]]: $\hat{\theta}(X_{1},\dots,X_{n})\to \theta$ as $n\to \infty$
4. [[Academics/STATS/Math Stats 2/Sufficiency\|Sufficiency]]: Does $\hat{\theta}$ utilize all the information contained in the data to estimate $\theta$?
5. Likeliness: $\hat{\theta}(X_{1},\dots,X_{n})$ is the most likely value of $\theta$ give the data ($\hat{\theta}$ is the choice with highest probability for the data)
6. Robustness: $\hat{\theta}(X_{1},\dots,X_{n})$ has a sampling distribution that is not too adversely affected by violations of assumptions made in the model/analysis

An estimator $\hat{\theta}(X_{1},\dots,X_{n})$ is [[Academics/CIS/Algorithms/Analysis\|asymptotically]] unbiased for $\theta$ if
$$
\lim_{ n \to \infty } bias(\hat{\theta}(X_{1},\dots,X_{n}))=0
$$
$E(\hat{\theta})\to \theta$ as $n\to \infty$

If $\hat{\theta}$ is unbiased for $\theta$, and $\lim_{ n \to \infty } \frac{Var(\hat{\theta})}{CRLB}=1$, then $\hat{\theta}$ is **asymptotically efficient**

