---
{"dg-publish":true,"dg-path":"STATS/Math Stats 2/Test function.md","permalink":"/stats/math-stats-2/test-function/","created":"2025-03-06T19:18:59.723-05:00","updated":"2025-07-07T17:32:42.569-04:00"}
---

$$\phi(x_{1},\dots,x_{n})=\begin{cases}
1\quad \text{if }(x_{1},\dots,x_{n})\in C, \\
0\quad \text{if }(x_{1},\dots,x_{n})\in C^c
\end{cases}
$$
If $\phi(x_{1},\dots,x_{n})=1$, reject $H_{0}$
If $\phi(x_{1},\dots,x_{n})=0$, do not reject $H_{0}$

# Example
$\phi(x_{1},\dots,x_{n})\sim Bernoulli(p)$,  $E(\phi(x_{1},\dots,x_{n}))=p$
$$
\begin{align}
\alpha  &  =P(\text{reject }H_{0}|H_{0} \text{ is true}) \\
 & =P(\phi(x_{1},\dots,x_{n})\in C|H_{0} \text{ is true}) \\
 & =E(\phi(\underset{\sim}{x})|H_{0} \text{ is true}) \\
\beta & =P(\text{do not reject }H_{0}|H_{0} \text{ is false}) \\
 & =P(\phi(x_{1},\dots,x_{n})\in C^c|H_{0} \text{ is false}) \\
 & =1-E(\phi(\underset{\sim}{x})|H_{0}\text{ is false})
\end{align}
$$

