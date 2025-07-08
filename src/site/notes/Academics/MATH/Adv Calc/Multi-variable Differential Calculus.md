---
{"dg-publish":true,"dg-path":"MATH/Adv Calc/Multi-variable Differential Calculus.md","permalink":"/math/adv-calc/multi-variable-differential-calculus/","created":"2024-10-11T13:05:04.417-04:00","updated":"2025-07-08T11:02:45.932-04:00"}
---

# Partial Derivatives
Derivatives of multivariable functions that only take into account one variable at a time, while keeping the others constant

# Clairaut's Theorem
Let $z=f(x,y)$ be a function with mixed second partial derivatives that are continuous at a point $(a,b)$, then
$$
\frac{\partial^2f}{\partial x\partial y}=\frac{\partial^2f}{\partial y\partial x} \quad \text{ at }(a,b)
$$

# Differentiability
A function $f(x,y)$ is differentiable at $(a,b)$ if and only if
1. $f_{x}(a,b)$ and $f_{y}(a,b)$ exist
2. $\lim_{ \tilde{x} \to \tilde{a} } \frac{|R_{1,\tilde{a}}(\tilde{x})|}{||\tilde{x}-\tilde{a}||}$ 

where $R_{1,\tilde{a}}(\tilde{x})$ denotes the remainder of the first order Taylor approximation of $f$ at $\tilde{a}$

$$
\begin{align} 
R_{1,\tilde{a}} & =f(x,y)-T_{1,\tilde{a}}(\tilde{x}) \\
R_{1,\tilde{a}} & =f(x,y)-(f(a,b)+f_{x}(a,b)(x-a)+f_{y}(a,b)(y-b))
\end{align}
$$

and $|| \cdot||$ denotes the Euclidean norm

If $f(x,y)$ is differentiable at $(a,b)$ then $f(x,y)$ is continuous at $(a,b)$
- contrapositive also true: $f(x,y)$ not continuous at $(a,b)\to$ not differentiable at $(a,b)$

If the partial derivatives $f_{x}$ and $f_{y}$ exist near $(a,b)$ and are continuous at $(a,b)$ then $f$ is differentiable at $(a,b)$

# Formal definition
$$f_{x}=\frac{\partial f}{\partial x}=lim_{h\to0}\frac{f(x+h,y)-f(x,y)}{h}$$

$$f_y=\frac{\partial f}{\partial y}=lim_{h\to0}\frac{f(x,y+h)-f(x,y)}{h}$$
# Chain Rule
If $z=f(x,y)=f(x(t),y(t))$ is a differentiable function with both $x$ and $y$ depending on a different variable

$$
\frac{df}{dt}=\frac{dz}{dt}= \frac{\partial f}{\partial x} \frac{\partial x}{\partial t}+\frac{\partial f}{\partial y} \frac{\partial y}{\partial t}
$$