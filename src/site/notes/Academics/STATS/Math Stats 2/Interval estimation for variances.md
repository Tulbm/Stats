---
{"dg-publish":true,"dg-path":"STATS/Math Stats 2/Interval estimation for variances.md","permalink":"/stats/math-stats-2/interval-estimation-for-variances/","created":"2025-02-27T20:01:29.141-05:00","updated":"2025-07-07T17:32:42.454-04:00"}
---



## Examples
$X_{1},\dots,X_{n}\sim N(\mu,\sigma^2)$, $\mu$ is known: use [[Academics/STATS/Intro to Stats/Sampling Distributions\|Sampling Distributions]] of $\chi_{n}^2$
$$
\begin{align}
P(\sigma^2_{l}\leq \sigma^2 \leq \sigma^2_{u})=1-\alpha \\
P\left( \sum \frac{(x_{i}-\mu)^2}{\sigma^2_{u}} \leq \frac{(x_{i}-\mu)^2}{\sigma^2_{u}} \leq \frac{(x_{i}-\mu)^2}{\sigma^2_{l}} \right) & 
\end{align}
$$
If $\mu$ is unknown
$$
\begin{align}
 & \dots \\
 & CI \text{ for }\sigma^2: \left( \frac{\sum(x_{i}-\bar{x})^2}{\chi^2_{1- \frac{\alpha}{2},n-1}}, \frac{\sum(x_{i}-\bar{x})^2}{\chi^2_{\frac{\alpha}{2},n-1}} \right) =   \left( \frac{(n-1)s^2}{\chi^2_{1- \frac{\alpha}{2},n-1}}, \frac{(n-1)s^2}{\chi^2_{\frac{\alpha}{2},n-1}} \right) 
\end{align}
$$

