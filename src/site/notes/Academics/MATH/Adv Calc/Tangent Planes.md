---
{"dg-publish":true,"dg-path":"MATH/Adv Calc/Tangent Planes.md","permalink":"/math/adv-calc/tangent-planes/","created":"2024-10-16T13:01:10.740-04:00","updated":"2025-07-08T11:02:46.006-04:00"}
---

A collection of all possible tangent lines to the surface of a multivariable function at a point $(a,b,f(a,b))$ 

$$
\nabla f(x,y,z)(a,b,c) \, \cdot <x-a,y-b,z-c>
$$
The normal vector $\hat{n}=(A,B,C)$ is orthogonal ???

$$
\begin{align}
<x-a,y-b,z-f(a,b)>\cdot<A,B,C>\ =0 \\
A(x-a)+B(y-b)+C(z-f(a,b))=0
\end{align}
$$
So the equation of the tangent plane must be
$$
z=f(a,b)- \frac{A}{C}(x-a)- \frac{B}{C}(y-b),\ \ c\neq0
$$


$$
z=f(a,b)+f_{x}(a,b)(x-a)+f_{y}(a,b)(y-b)
$$

# Taylor Polynomials
Taking the taylor expansion of a multivariable function
$$
\begin{align}
f(x,y)= & f(a,b)+ \frac{f_{x}(a,b)}{1!}(x-a)+ \frac{f_{y}(a,b)}{1!}(y-b) +\\ 
  + & \frac{f_{xx}(a,b)}{2!}(x-a)^2+ \frac{2}{2!}f_{xy}(a,b)(x-a)(y-b) + \frac{f_{yy}(a,b)}{2!}(y-b)^2+\dots
\end{align}
$$
Linear approximation of $f$ at $(a,b)$ is the tangent plane approximation/taylor expansion up to only one derivative
$$
L_{a,b}(\tilde{x})=T_{1,\tilde{a}}(\tilde{x})=f(a,b)+f_{x}(a,b)(x-a)+f_{y}(a,b)(y-b)
$$

