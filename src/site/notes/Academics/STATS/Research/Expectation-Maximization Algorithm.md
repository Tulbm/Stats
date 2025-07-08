---
{"dg-publish":true,"permalink":"/academics/stats/research/expectation-maximization-algorithm/","created":"2025-05-11T20:49:04.783-04:00","updated":"2025-07-07T17:32:53.466-04:00"}
---

Broadly used algorithm in situations where the observed data is considered incomplete when finding [[Academics/STATS/Math Stats 2/Method of maximum likelihood\|Method of maximum likelihood]]
- standard tool for mixture models

The complete data $y$ 
$$
y=(x',z')'
$$
consists of observed data $x$ (which is incomplete) and unobserved data $z$

# Formulation
Suppose we have the pdfs or pmfs for the complete data $f_{c}(y;\theta)$ and the incomplete data $f(x;\theta)$

The complete-data log-likelihood could be formed for $\theta$ if $y$ are fully observed and available
 $$
\log L_{c}(\theta)=\log f_{c}(y;\theta)=\log(f_{c}(x,z;\theta))
$$

In the first iteration, the E-step finds the expectation of the complete-data log likelihood given $\theta^{(0)}$, the initial value for $\theta$
$$
Q(\theta;\theta^{0})=E[\log L_{c}(\theta;x,z)|\theta^{(0)}]
$$
The M-step is to find the value of $\theta$ that maximizes the $Q(\theta;\theta^{(0)})$, $\theta^{(1)}$ such that
$$
Q(\theta^{ (1)};\theta^{(0)}) \geq Q(\theta; \theta^{(0)})
$$
for all possible $\theta$

On the $(i+1)^{th}$ iteration, we define:
**E-Step**: Calculate
$$
Q(\theta;\theta^{(1)})=E[\log L_{c}]
$$
M-Step: Find $\underset{\sim}{\theta}^{(i+1)}$ that maximizes $Q(\theta;\theta^{(i)})$, that is
$$
Q(\theta^{(i+1)};\theta^{(i)})\geq Q(\theta;\theta^{(i)})
$$
for all $\theta$

# Stopping Criteria

The pdf of the incomplete data is given by integrating out z and getting the marginal of x
$$
f(x;\theta)= \int f_{c}(y;\theta)dz=\int f_{c}(x,z;\theta)dz=\sum_{z}f_{c}(x,z;\theta)
$$

Repeat both the E and M steps alternatively until convergence as the difference of the incomplete-data likelihood $L(\theta^{(1)})-L(\theta^{(i)})$ is very small and less than a pre-specified tolerance amount. 
$$
L(\theta^{(i)})=\prod f(x_{i};\theta)
$$

