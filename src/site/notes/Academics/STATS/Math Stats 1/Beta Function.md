---
{"dg-publish":true,"dg-path":"STATS/Math Stats 1/Beta Function.md","permalink":"/stats/math-stats-1/beta-function/","created":"2024-11-28T16:16:09.574-05:00","updated":"2025-07-07T17:59:20.868-04:00"}
---


$$
B(\alpha,\beta)=\left[ \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)} \right]^{-1}
$$

Inverse to denote the relationship with [[Academics/CIS/Discrete Structures/Counting Theorems\|combinatorics]], [[Academics/STATS/Math Stats 1/Gamma function\|Gamma function]] is the continuous factorial, so it is like the inverse of ${ n\choose k }$ 

If the gamma function was not weirdly shifted by one, it would look like

$$
B(\alpha,\beta)=\frac{\Gamma(\alpha)\Gamma(\beta)}{\Gamma(\alpha+\beta)(\alpha+\beta+1)}
$$

which is one argument for the weird gamma function. Another one is the fact that $\Gamma(0)=-1!=\infty$
