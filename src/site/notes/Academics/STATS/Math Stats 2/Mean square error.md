---
{"dg-publish":true,"dg-path":"STATS/Math Stats 2/Mean square error.md","permalink":"/stats/math-stats-2/mean-square-error/","created":"2025-01-30T12:01:22.889-05:00","updated":"2025-07-11T04:17:34.551-04:00"}
---

The mean square error of an estimator $\hat{\theta}$ of the parameter $\theta$ is given by
$$\begin{align}
MSE(\hat{\theta}) & =E[(\hat{\theta}-\theta)^2] \\
 & = E[(\hat{\theta}-E(\hat{\theta})+E(\hat{\theta})-\hat{\theta})^2] \\
 & = E[(\hat{\theta}-E(\hat{\theta})^2+ 2(\hat{\theta}-E(\hat{\theta}))(E(\hat{\theta}-\theta))+(E(\hat{\theta})-\theta)^2)] \\
 & =E((\hat{\theta}-E(\hat{\theta}))^2)+2E((\hat{\theta}-E(\hat{\theta}))(E(\hat{\theta})-\theta))+E((E(\hat{\theta}-\theta))^2) \\
 & =var(\hat{\theta})+2(E(\hat{\theta})-\theta)(E(\hat{\theta})-E(\hat{\theta}))+bias^2(\hat{\theta}) \\
 & =var(\hat{\theta})+0+bias^2(\hat{\theta}) \\
 & =var(\hat{\theta})+[E(\hat{\theta})-\theta]^2
\end{align}
$$
So basically
$$
E[(\bar{X}-\mu)^{2}]= Var(\bar{X})=\frac{\sigma^{2}}{n}
$$
