---
{"dg-publish":true,"dg-path":"MATH/Adv Calc/Multi-variable Functions.md","permalink":"/math/adv-calc/multi-variable-functions/","created":"2024-04-10T19:04:20.730-04:00","updated":"2025-07-08T11:02:45.942-04:00"}
---

[[1-Recent/Academics/CIS/Discrete Structures/Functions\|1-Recent/Academics/CIS/Discrete Structures/Functions]]

$z=f(x,y)$
$f: X\to Y$
where X will be a cartesian product of sets
- like $R^{n},\ n>1$

Domain is the set of the tuples inside $X$ for which $f:X\to Y$ is defined
Codomain will be the set of the values obtained when using the domain

$z=\sqrt{ 3x-y-2 }$\
- Domain = $\{(x,y);\ y\leq3x-2\}$

# Limits and Continuity

A $\lim_{ x \to a }f(x)=L$ can have its relation between $x$ and $f(x)$ measured by changes in distances $\delta$ and $\epsilon$
- $|x-a|<\delta\to a-\delta<x<a+\delta$
- $|f(x)-L|<\epsilon\to L-\epsilon<f(x)<L+\epsilon$

So $\lim_{ x \to a}f(x)=L$ means
$$
\forall \epsilon >0, \exists \delta>0 \ \text{such that }|x-a|<\delta\to|f(x)-L|<\varepsilon
$$

For multivariable functions:
- distance from a point $(a,b)=||(x,y)-(a,b)||=||\tilde{x}-\tilde{a}||=\sqrt{ (x-a)^2+(y-b)^2 })$
- $0<||\tilde{x}-\tilde{a}||<\delta\to0< (x-a)^2+(y-b)^2<\delta^2$
- $|f(x,y)-L|<\epsilon$

## Uniqueness of Limits
If $\lim_{ \tilde{x} \to \tilde{a} }f(\tilde{x})=L_{1}$ along one path and $\lim_{ \tilde{x} \to \tilde{a} }f(\tilde{x})=L_{2}$ along a different path then $\lim_{ \tilde{x} \to \infty }\tilde{a}f(\tilde{x})$ does not exist
- paths can be any $y=mf(x)$ or $x=mf(y)$, since we don't know the relationship between the values of x and y

Only useful to prove that limit does not exist
## Plug in Limits
A function $f:R^n\to R$ is continuous at $\tilde{a}\in R^n$ if
1. $f$ is defined at $\tilde{a}$
2. $\lim_{ \tilde{x} \to \tilde{a} }f(\tilde{x})$ exists
3. $\lim_{ \tilde{x} \to \tilde{a} }f(\tilde{x})=f(\tilde{a})$

So if $f$ is continuous, we can find $\lim_{ \tilde{x} \to \tilde{a} }f(\tilde{x})$ by just plugging in $\tilde{a}$

[[1-Recent/Academics/MATH/Calculus/L'Hopital's Rule\|L'Hopital's Rule]] doesn't work in multivariables, but we can still:
- factor
- multiply by a conjugate
- common denominators
## Squeeze Theorem
If $0\leq|f(\tilde{x})-L|\leq M(\tilde{x})\quad\forall \tilde{x}\neq \tilde{a}$ in some neighborhood of $\tilde{a}$ and $\lim_{ \tilde{x} \to \tilde{a} }M(\tilde{x})=0$ then $\lim_{ \tilde{x} \to \tilde{a} }f(\tilde{x})$ exists and equals $L$
- the mutivariable function $M(\tilde{x})$ whose limit is easy to calculate binds $f(\tilde{x})$ at 0

Can be used instead of the $\delta- \epsilon$ proofs

Cannot prove that a limit does not exist