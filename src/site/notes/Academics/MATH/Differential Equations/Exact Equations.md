---
{"dg-publish":true,"permalink":"/academics/math/differential-equations/exact-equations/","created":"2024-10-04T14:46:56.993-04:00","updated":"2025-07-08T11:02:52.773-04:00"}
---

# Exact Equations
Multivariable functions

A DE in the form of:
$$
M(x,y)+N(x,y) \frac{dy}{dx}=0
$$
is called exact if there exists a function $\varphi(x,y)$ such that
$$
(\text{total derivative}){\frac{d\varphi}{dx}}=M(x,y)+N(x,y){\frac{dy}{dx}}
$$
Exact equations
- the solutions are given by $\varphi(x,y)=C$
- $M(x,y)=\frac{\partial\varphi}{\partial x}$
- $N(x,y)=\frac{\partial\varphi}{\partial y}$

We can find $\varphi(x,y)$ by integrating $M$ with respect to x, or $N$ with respect to y
- $M$ and $N$ may not contain all the information about the variable not integrated wrt 

Aligning $M$ and $N$ to find the missing terms we get the full form of $\varphi$ 
[[Academics/MATH/Differential Equations/Total Derivative\|Total Derivative]]

## Using Integrating Factors to Transform "Almost Exact" DEs into Exact

Start with a non-exact DE:
$$
M(x,y)+N(x,y) \frac{dy}{dx}=0
$$
Multiplying by an integrating factor $\mu(x,y)$:
$$
\mu(x,y)M(x,y)+\mu(x,y)N(x,y)\frac{dy}{dx}=0
$$
For the DE to be exact, we need:
$$
\frac{\partial}{\partial y}\left(\mu(x,y)M(x,y)\right)=\frac{\partial}{\partial x}\left(\mu(x,y)N(x,y)\right)
$$

### Case 1
If $\mu$ is a function of $x$ only

### Case 2