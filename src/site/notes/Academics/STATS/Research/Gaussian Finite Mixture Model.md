---
{"dg-publish":true,"dg-path":"STATS/Research/Gaussian Finite Mixture Model.md","permalink":"/stats/research/gaussian-finite-mixture-model/","created":"2025-05-11T20:49:04.999-04:00","updated":"2025-07-07T17:32:53.473-04:00"}
---

- model based clustering method

Finite mixture models consider the situation that a sample is drawn from a population that consists of a finite number of components/subpopulations

WLOG, we adopt the common form of the pmf for a G-component mixture as
$$
L(\Psi)=\prod_{i=1}^nf(x_i;\Psi)=\prod_{i=1}^n\sum_{g=1}^G\pi_gf_g(x_i;\theta_g),
$$
for $i=1\dots n,\Psi=(\pi_{1},\pi_{2},\dots \pi_{G-1},\theta_{1},\dots ,\theta_{G})'$

57

If we use the conventional [[Academics/STATS/Math Stats 2/Method of maximum likelihood\|Method of maximum likelihood]] we will not obtain an explicit solution for the parameters



$$
\begin{align}
\frac{\partial l}{\partial \pi_{g}}  &  = \sum_{i=1}^n \frac{f(x_{i};\theta_{g})-f_{G}(x_{i};\theta_{G})}{\sum^g \pi_{g}f(x_{i};\theta_{g})} = 0 \\
  & =f(x_{1};\theta_{g})-f(x_{1};\theta)
\end{align}
$$

To use the [[Academics/STATS/Research/Expectation-Maximization Algorithm\|Expectation-Maximization Algorithm]] we twist this problem as an incomplete-data problem. The observed data is $X$ and the unobserved data is the component membership of each observation
$$
z=(z_{1}',\dots, z'_{n})'
$$
$$
y_{i}=(x_{i, z'_{i}})'
$$

The complete-data log-likelihood for $\Psi$ has the form
$$
Z_{ig}= \begin{cases}
1, & \text{if the }i^{ th} \text{ obs is from }g^{th} \text{ component} \\
0 &  \text{otherwise}
\end{cases}
$$
$Z_{i}$ follows a multinomial$(1,\underset{\sim}{P_{i}})$, prior, posterior something

Now the complete-data likelihood for $\Psi$ has the form
$$\begin{align}
L_{c}  & =\prod_{i=1}^n f(y_{i};\Psi)= \prod_{i=1}^n f(x_{i},z_{i};\Psi) \\
 & = \\
L_{c}(\Psi;y)  & = \prod_{i=1}^n \prod_{g=1}^G [\pi _{g}f_{g}(x_{i};\theta_{g})]^{z_{ig}}
\end{align}
$$

Now we can formulate a general E-step and M-step for fitting a mixture model
$$
l_{c}(\Psi;y)= \sum_{i=1}^n \sum_{g=1}^G Z_{ig}\log[\pi _{g}f_{g}(x_{i};\theta_{g})] = \sum_{i=1}^n\sum_{g=1}^G Z_{ig}[\log \pi_{g}+\log f_{g}(x_{i};\theta_{g})]
$$
# E-step
Given $\Psi^{(i)}=(\underset{\sim}{\pi}^{(i)}, \theta^{(i)})$, estimate $Z_{ig}^{(i+1)}$ using [[Academics/STATS/Math Stats 1/Conditional probability#Bayes Theorem\|Bayes Theorem]]
$$
\begin{align*}
Z_{ig}^{(1)}   = E(Z_{ig}|\underset{\sim}{\pi}^{(0)}, \underset{\sim}{\theta}^{(0)})&= P(Z_{ig} = 1 \mid x_i, \Psi) \\
&= \frac{P(x_i \mid Z_{ig} = 1, \Psi) \cdot P(Z_{ig} = 1 \mid \Psi)}{P(x_i \mid \Psi)} \\
Z_{ig}^{(1)}&= \frac{\pi_g \cdot f_g(x_i; \theta_g) }{\sum_{h=1}^G \pi_h f_h(x_i; \theta_h)}
\end{align*}
$$
Which is necessary in the $Q$ formula:
$$\begin{align}
Q(\Psi;\Psi^{(0)}) & = E(l_{c}(\Psi;\underset{\sim}{y})|Psi^{(0)}) \\
 & = E \left(\sum_{i=1}^n\sum_{g=1}^G Z_{ig}[\log \pi_{g}+\log f_{g}(x_{i};\theta_{g})] |\underset{\sim}{\pi}^{(0)},\theta^{(0)} \right) \\
 & =\sum_{i=1}^n\sum_{g=1}^G E(Z_{ig}[\log \pi_{g}+\log f_{g}(x_{i};\theta_{g})]|\underset{\sim}{\pi}^{(0)},\theta^{(0)}) \\
 & =\sum_{i=1}^n \sum_{g=1}^G E(Z_{ig}|\underset{\sim}{\pi}^{(0)},\theta^{(0)}) [\log \pi_{g}+\log f_{g}(x_{i};\theta_{g})] \\
Z_{ig}^{(1)}  & = E(Z_{ig}|\underset{\sim}{\pi}^{(0)}, \underset{\sim}{\theta}^{(0)})= \frac{\pi_{g}^{(0)}f(x_{i};\underset{\sim}{\theta_{g}}^{(0)})}{\sum_{g=1}^G \pi_{g}^{(0)}f(x_{i};\underset{\sim}{\theta_{g}}^{(0)})}
\end{align}
$$
# M-step
find $\Psi=(\pi,\theta)$ that maximizes $Q(\Psi;\Psi^{(i)})$ based on $\underset{\sim}{Z_{ig}}^{(i)}$
$$\begin{align}
Q(\Psi;\Psi^{(0)})  & = \sum_{i=1}^n \sum_{g=1}^G Z_{ig}^{(1)}[\log \pi_{g}+ \log f_{g}(x_{i};\underset{\sim}{\theta _{g}})] \\
	 & = \sum_{i=1}^n \sum_{g=1}^G Z_{ig}^{(1)} \log \pi_{g} +  \sum_{i=1}^n \sum_{g=1}^G Z_{ig}^{(1)} \log f_{g}(x_{i};\underset{\sim}{\theta _{g}}) \\
 & =Q_{1}(\underset{\sim}{\pi};\pi^{(0)}\underset{\sim}{}) + Q_{2}(\underset{\sim}{\theta} ;\underset{\sim}{\theta^{(0)}})
\end{align}
$$

## Maximizing $Q_{1}$
$$
\begin{align}
Q_{1} & =\sum_{i=1} ^{n } \sum_{g=1}^G Z_{ig}^{(i)} \log \pi _{g} +\lambda(1-\sum_{g=1}^{G}\pi _{g})
\end{align}
$$
with a scalar $\lambda$ to find a solution, as $\sum_{g}\pi _{g}=1, 1-\sum_{g}\pi _{g}=0$

Then maximizing $Q_{1}$ we get the values of $\pi _{g}$ based on $Z_{ig}^{(i)}:$
$$
\frac{ \partial Q_{1} }{ \partial \pi _{g} } = \sum_{i=1}^{n}Z_{ig}^{(i)}-\lambda =0\to \pi _{g}=\frac{\sum_{i=1}^{n}Z_{ig}^{(i)}}{\lambda}
$$
- terms in the $\sum_{g}$ of a different $g$ go to 0

$\lambda$ is also an unknown variable, so to find the value of it that maximizes $Q_{1}:$
$$
\frac{ \partial Q_{1} }{ \partial \lambda } =1-\sum_{g=1}^{G}\pi _{g}=0\to 1 - \frac{\sum_{g=1}^{G}\sum_{i=1}^{n}Z_{ig}}{\lambda}=1- \frac{\sum_{i=1}^{n}\sum_{g=1}^{G}Z_{ig}}{\lambda}=1- \frac{\sum_{i=1}^{n}1}{\lambda} = 1- \frac{n}{\lambda}
$$
$\therefore$  $\hat{\lambda}=n$ and 
$$
\hat{\pi}_{g}=\frac{\sum_{i=1}^{n}Z_{ig}^{(i)}}{n}, \quad g=1,\dots ,G
$$
- intuitive result, use the estimate of $Z$ over the groups to find the share that should be from a certain population
- $Z^{(i)}$ is expectation, continuous number 0-1, not binary as the real unknown data


## Maximizing $Q_{2}$

$$
Q_{2}=\sum_{i=1}^n \sum_{g=1}^G Z_{ig}^{(1)} \log f_{g}(x_{i};\underset{\sim}{\theta _{g}}) 
$$
$$
\begin{align}
Q_{2} &= \sum_{g=1}^{G} \sum_{i=1}^{n}Z_{ig} \log f(y_{i};\underset{\sim}{x_{i}},\underset{\sim}{\beta _{g}},\sigma _{g}^{2}) \\
 & =\sum_{g=1}^{G}\sum_{i=1}^{n}Z_{ig}\log\left( \frac{1}{\sqrt{ 2\pi \sigma _{g}^{2} }}\exp\left({\frac{-(y_{i}-\underset{\sim}{x_{i}}\underset{\sim}{\beta _{g}})^{2}}{2\sigma _{g}^{2}}}\right) \right)  \\
 & =\sum_{g=1}^{G}\sum_{i=1}^{n}Z_{ig}^{(1)}\left( - \frac{1}{2}\log(2\pi) - \frac{1}{2} \log \sigma _{g}^{2} - \frac{(y_{i}-\underset{\sim}{x_{i}}\underset{\sim}{\beta _{g}})^{2}}{2\sigma_{g}^{2}} \right)
\end{align}
$$
### Estimating $\tilde{\beta}:$

as $\tilde{\beta}_{g}=(\beta _{0g},\beta _{1g},\dots,\beta _{pg})$ for $p$ covariates and an intercept:
$$
\frac{ \partial Q_{2} }{ \partial \tilde{\beta}_{g} } =\left[ \frac{ \partial Q_{2} }{ \partial \beta _{0g} } ,\frac{ \partial Q_{2} }{ \partial \beta _{1g} } ,\dots,\frac{ \partial Q_{2} }{ \partial \beta _{pg} }  \right]^{T}
$$
Let $j=0,1,\dots,p:$
$$
\begin{align} 
\frac{ \partial Q_{2} }{ \partial \beta _{jg} }  & = \sum_{i=1}^{n}Z_{ig}^{(1)} \frac{ \partial  }{ \partial \beta _{jg} } \left( \frac{-(y_{i}-\tilde{x}_{i}\tilde{\beta}_{g})^{2}}{2\sigma _{g}^{2}} \right) \\
 & = \frac{1}{\sigma _{g}^{2}} \sum_{i=1}^{n}Z_{ig}^{(1)} (y_{i}-\tilde{x}_{i}\tilde{\beta}_{g})x_{ij}=0 \\
 & \to\sum_{i=1}^{n}[Z_{ig}^{(1)}y_{i}x_{ij}-Z_{ig}^{(1)}\tilde{x}_{i}\tilde{\beta}_{g}x_{ij}]=0 \\
\end{align}
$$
Then bringing it back to vector form for all $\beta$'s:
$$
\begin{align}
\frac{ \partial Q_{2} }{ \partial \tilde{\beta}_{g} } &  = \sum_{i=1}^{n}[Z_{ig}^{(1)}(y_{i}-\tilde{x}_{i}\tilde{\beta}_{i})\tilde{x}_{i}^{T}]=0 \\
 & \to \sum_{i=1}^{n} Z_{ig}^{(1)} y_{i}\tilde{x}_{i}^{T}-\sum_{i=1}^{n} Z_{ig}^{(1)} \tilde{x}_{i}\tilde{\beta}_{g}\tilde{x}_{i}^{T} \\
 & \to \sum_{i=1}^{n} Z_{ig}^{(1)} y_{i} \tilde{x}_{i}^{T}=\sum_{i=1}^{n}Z_{ig}^{(1)}\tilde{x}_{i}\tilde{\beta}_{g}\tilde{x}_{i}^{T} \\
\end{align}
$$
Rewriting it in matrix form:
$$\begin{align}
\mathbf{X}Z_{g}^{(1)}\tilde{Y} & =(\mathbf{X}^{T}Z_{g}^{(1)}\mathbf{X})\tilde{\beta}_{g} \\
\tilde{\beta}_{g}^{(1)} = \underset{\sim}{\hat{\beta}_{g}}  & = (\mathbf{X}^{T}Z_{g}^{(1)}\mathbf{X})^{-1} \mathbf{X}^{T}Z_{g}^{(1)}\tilde{Y}
\end{align}
$$
where $Z_{g}^{(1)}=diag(Z_{1g}^{(1)},\dots,Z_{ng}^{(1)})$
$$
=\begin{bmatrix}
Z_{1g}^{(1)}  &0 & 0 & 0 & \dots \\
0 & Z_{2g}^{(1a)} & 0 & 0 & \dots \\
0 & 0 & \dots & 0  & \dots\\
0 & \dots & \dots & Z_{n-1 g}^{(1)} & \dots \\
0 & \dots & \dots & \dots & Z_{ng}^{(1)}
\end{bmatrix}
$$
### Estimating $\sigma _{g}^{2}:$ 

Differentiating with respect to $\sigma _{g}^{2}$ we get isolate $g$ and work with only one sum:
$$
\begin{align}
\frac{ \partial Q_{2} }{ \partial \sigma _{g}^{2} }  & = \sum_{i=1}^{n} Z_{ig}^{(1)} \left[  \left( - \frac{1}{2} \right) \frac{1}{\sigma _{g}^{2}}+ \frac{(y_{i}-\underset{\sim}{x_{i}}\underset{\sim}{\beta _{g}})^{2}}{2(\sigma _{g}^{2})^{2}} \right] \\
 & =\sum_{i=1}^{n}Z_{ig}^{(1)}\left[ \frac{(y_{i}-\underset{\sim}{x_{i}}\underset{\sim}{\beta _{g}})^{2}-\sigma _{g}^{2}}{2\sigma} \right] = 0 \\
  & \to \sum_{i=1}^{n}Z_{ig}^{(1)}(y_{i}-\tilde{x}_{i}\tilde{\beta}_{g})^{2} - \sum Z_{ig}^{(1)}\sigma _{g}^{2} =0 \\
 & \to \sigma _{g}^{2} = \frac{\sum_{i=1}^{n}Z_{ig}^{(1)}(y_{i}-\tilde{x}_{i}\tilde{\beta}_{g})^{2}}{\sum_{i=1}^{n}Z_{ig}^{(1)}}
\end{align}
$$
Plugging in the result for $\tilde{\beta}_{g}^{(1)}$ from the previous step we have:
$$
{\sigma _{g}^{2}}^{(1)}=\hat{\sigma}_{g}^{2}=(Y-\mathbf{X}\tilde{\beta}_{g}^{(1)})\mathbf{Z}_{g}^{(1)}(Y-\mathbf{X}\tilde{\beta}_{g}^{(1)})\text{trace}^{-1}(\mathbf{Z}_{g}^{(1)})
$$
where the trace sums all $Z_{ig}$'s back