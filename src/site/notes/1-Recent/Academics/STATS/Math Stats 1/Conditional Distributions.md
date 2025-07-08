---
{"dg-publish":true,"dg-path":"STATS/Math Stats 1/Conditional Distributions.md","permalink":"/stats/math-stats-1/conditional-distributions/","created":"2024-10-22T16:25:02.062-04:00","updated":"2025-07-07T18:02:31.286-04:00"}
---


$$
\begin{align}
f_{X|Y}(x|y)  =P(A|B) & =\frac{P(A\cap B)}{P(B)} \\
   & =\frac{P(X=x,Y=y)}{P(Y=y)} \\
   f_{X|Y}(x|y)& =\frac{f_{X,Y}(x,y)}{f_{Y}(y)}
\end{align}
$$
And:
$$
f_{Y|X}(y|x)=\frac{f_{X,Y}(x,y)}{f_{X}(x)}
$$

- $f_{X,Y}(x,y)$ is the [[1-Recent/Academics/STATS/Math Stats 1/Multivariable Distributions\|joint pmf/pdf]] of $X$ and $Y$
- $f_{Y}(y)$ is the [[1-Recent/Academics/STATS/Math Stats 1/Marginal Distributions\|marginal distribution]] of  $Y$
- $f_{X}(x)$ is the marginal distribution of $X$

$$
f(x,y)=\frac{\partial F(x)}{\partial x} \frac{\partial F(y)}{\partial y}
$$
# [[1-Recent/Academics/STATS/Math Stats 1/Independency\|Independency]]

If $X$ and $Y$ are independent:

$$
\begin{align}
f_{X,Y}=
\end{align}
$$
# Conditional Cumulative Distribution Functions
The conditional cumulative distributions of $X$ given $y$ 

$$
\begin{align}
F_{X|Y}(x|y) & =P(X\leq x|Y=y) \\
 & =\begin{cases}
\sum_{t\leq x}f_{X|Y}(t|y) \, \,\,\, \,\,\,\, \,  \text{ discrete case} \\
\int_{-\infty}^xf_{X|Y}(t|y)dt \, \, \, \, \,\,\, \text{ continuous case}
\end{cases}
\end{align}
$$

