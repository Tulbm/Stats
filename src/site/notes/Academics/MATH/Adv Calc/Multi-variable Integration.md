---
{"dg-publish":true,"dg-path":"MATH/Adv Calc/Multi-variable Integration.md","permalink":"/math/adv-calc/multi-variable-integration/","created":"2024-11-11T12:52:18.895-05:00","updated":"2025-07-08T11:02:45.952-04:00"}
---



Definition with the riemman sums
$$
\lim_{ n,m \to \infty, }\sum_{j=1}^n\sum_{k=1}^mf(x_{j}y_{k})\nabla x_{j}\nabla y_{k}=\int

$$


Fubini's Theorem
If $f$ is continuous on the rectangle $R=\{a\leq x\leq b,c\leq y\leq d\}$ then
$$
\int_{a}^b \int_{c}^df(x,y) \,dy\,dx=\int_{c}^d \int_{a}^b f(x,y)\, dx\, dy
$$
# Bounded by regions
If no constant bound is given, they can be found by looking at the intersections of the binding functions

The order of the integrals in interchangeable, but some combination of functions are much easier to be integrated when doing a different order of integrals
### Bounded by x
Regions bounded by functions of x (type 1 region)
$$\begin{align}
R & =\{a\leq x\leq b,g_{1}(x)\leq y\leq g_{2}(x)\} \\
\text{Area} &= \int_{a}^b\int_{g_{1}(x_)}^{g_{2}(x)}f(x,y)\,dy\,dx
\end{align}
$$
### Bounded by y
Regions bounded by functions of y (type 2 region)
$$\begin{align}
R & =\{c\leq y\leq d,h_{1}(y)\leq x\leq h_{2}(y)\} \\
\text{Area} &= \int_{c}^d\int_{h_{1}(y_)}^{h_{2}(y)}f(x,y)\,dx\,dy
\end{align}
$$
# Properties of Double Integrals
1. $$\int \int _{R} f(x,y) \pm g(x,y)\, dA =  \int\int _{R}f(x,y) \, dA   \pm \int \int_{R} g(x,y) \, dA
$$
2. $$\int \int_{R}cf(x,y) \, dA = c \int \int_{R}f(x,y) \, dA  
$$
3. If $f(x,y)\geq g(x,y),\quad \forall(x,y) \in R^2$ then
$$\int \int_{R}f(x,y) \, dA \geq \int \int_{R}g(x,y) \, dA  
$$
4. $\int \int_{R} 1 \, dA$
5. If $m\leq f(x,y)\leq M, \quad\forall(x,y)\in R^2$ then
$$mA(R)\leq \int \int_{R}f(x,y) \, dA \leq MA(R) 
$$
6. If $R=R_{1}\cup R_{2},\, R_{1}\cap R_{2}=\emptyset$ then
$$
\int \int_{R}f(x,y)dA \, dA=\int \int_{R_{1}}f(x,y) \, dA +\int \int_{R_{2}}f(x,y) \, dA   
$$

[[Academics/MATH/Adv Calc/Multi-variable Change of Variables\|Multi-variable Change of Variables]]