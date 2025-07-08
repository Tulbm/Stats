---
{"dg-publish":true,"permalink":"/academics/math/adv-calc/applications-of-partial-derivatives/","created":"2024-10-30T13:05:06.796-04:00","updated":"2025-07-08T11:02:45.879-04:00"}
---

# Critical points 
A point $(a,b)$ is called a critical point of $f:R^2\to R$ if $\nabla f(a,b)=\tilde{0}$ (or if at least one of $f_{x}(a,b)/f_{y}(a,b)$ does not exist, but $f$ does)

- DNE = vertical tangent
- 0 = horizontal tangent

Unlike single variable functions, we need to solve a system of equations when working with multi-variables
$$
\nabla f=\tilde{0}=\begin{cases}
f_{x}(x,y)=0 \\
f_{y}(x,y)=0
\end{cases}
$$
[[Academics/MATH/Adv Calc/Critical Points\|Critical Points]] of multi-variable functions are an extension of the theory with single variable functions

A critical point of a multivariable function can be:
- global maximum ()
- global minimum
- neither

### Fermat's Theorems
If $f(x,y)$ has continuous first partial derivatives and $(a,b)$ is a local maximum or minimum of $f(x,y)$ then $f_{x}(a,b)=0$ and $f_{y}(a,b)=0$

$$
Hf(x,y)=\begin{pmatrix}
f_{xx}  & f_{xy} \\
f_{yx} & f_{yy}
\end{pmatrix}
$$
 Suppose that $f(x,y)$ has continuous second partial derivatives near $(a,b)$ and $f_{x}(a,b)=f_{y}(a,b)=0$. If $Hf(a,b)$ is
 1. positive definite then $(a,b)$ is a local minimum of $f$
 2. negative definite then $(a,b)$ is a local maximum of $f$
 3. 

With Eigenvalues:
1. 

Quadratic forms:
A function $Q(x,y)$ can be expressed as
$$
Q(x,y)=(x-a,y-b)\begin{pmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{pmatrix}
\begin{pmatrix}
x-a \\
y-b
\end{pmatrix}
$$
A quadratic form is:
1. positive definite if $Q>0o$