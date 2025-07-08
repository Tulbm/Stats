---
{"dg-publish":true,"permalink":"/academics/stats/research/penalized-likelihood/","created":"2025-05-27T17:31:22.262-04:00","updated":"2025-07-07T17:32:53.488-04:00"}
---

When a large number of variables/predictors are avaialable for predicting the response, the conventional MLE/Least Square Error

1.
2.

Used when we want to penlize the model complexity to encourage a more simpler model
$$
l_{p}(\theta;x)=l(\theta;x)-\lambda P(\theta)
$$




# Ridge Regression

$$
Y_{i}=\beta_{0}+\beta_{1}x_{i1}
$$

$$
\begin{align}
\hat{\beta}=(X ^{T}X)^{-1}X^{T}Y  &  & var(\hat{B}) & =var(X^{T}X)^{-1}X^{T}Y\\
var(Y)=\sigma^{2}  &  & & = \\
var(\hat{y}) & =var(X\hat{\beta}) & =var(X(X^{T}X)^{-1}X^{T}Y)     &  \\
 & =Xvar(\hat{\beta})X^{T}=\sigma^{2}(X(X^{T}X)^{-1}X^{T})
\end{align}
$$

The ordinary least square estimate $\hat{\beta}^{0}$ of $\beta$ is the solution that minimizes the residual sum of aquare

$$
=argmin\left\{ \sum_{i=1}^{n} \epsilon_{i} \right\}
$$

$$\begin{align}
\hat{\beta}_\text{ridge} & =\underset{\beta}{\text{argmin}} \left\{  \sum \times x +\lambda \sum \beta_{j}^{2}  \right\} \\
 & = \\
 & = (X^{T}X+\lambda I)^{-1}X^{T}y
\end{align}
$$
Minimizing the terms of error + square betas, we minimize the effect of relying on specific betas to explain y (overfitting). The act of minimizing $\hat{\beta}_\text{ridge}$ approximates all the betas with its dimensions to a circle/ x-d spheres

$$
\frac{ \partial -l_{p}(\beta) }{ \partial \beta_{j}} |_{\beta=\beta}
$$

$$
\begin{align}
\lambda\in \{ \lambda _\text{min},\dots,\lambda _\text{max} \} \\
\lambda _\text{max} = \text{min }\lambda \text{ s.t. all }\beta_{j}=0, j\neq0
\end{align}
$$


show $Var(\hat{\beta}_\text{ridge})\leq var(\hat{\beta}undsim)$


# Least Absolute Shrinkage and Selection Operation (LASSO)



