---
{"dg-publish":true,"dg-path":"MATH/Differential Equations/Higher-Order DEs.md","permalink":"/math/differential-equations/higher-order-d-es/","created":"2024-10-09T14:32:45.775-04:00","updated":"2025-07-08T11:02:52.788-04:00"}
---

# Functional Notation

A **functional** is an operator or map whose domain and range are in the space of functions 

$$
H[f]=g \ \ \ \ \ \ \ \text{  if f and g are functions}
$$
A **linear operator** $L$ is a functional for which the following property holds: 
- $L[c_{1}f_{1}+c_{2}f_{2}]=c_{1}L[f_{1}]+c_{2}L[f_{2}]$ for constants $c$ and functions $f$

(like derivative)

A **differential operator** $D^n[y]$ is a **linear operator** that can be used to represent the $n^{th}$ derivative of a dependent variable with respect to an independent variable
$$
Dy=D[y]=\frac{dy}{dx}
$$

Linear operators can distribute just like variables
$$
\begin{align} 
D^4y-y=1 \\
(D^4-1)y=1 \\
(D-1)(D+1)(D^2+1)y=1
\end{align}
$$

[[1-Recent/Academics/MATH/Differential Equations/Reduction of Order\|Reduction of Order]]

# Higher order DEs with constant coefficients

Same method from [[1-Recent/Academics/MATH/Differential Equations/Second-Order Linear DEs\|Second-Order Linear DEs]]
$$
a_{n}y^{(n)}(x)+a_{n-1}y^{(n-1)}(x)+\dots+a_{1}y(x)+a_{0}y(x)=0
$$

Case: $r_{1},r_{2},\dots,r_n$ are real and distinct
- General Solution is the linear combination of all of the corresponding exponential functions
$$
y=c_{1}e^{r_{1}x}+c_{2}e^{r_{2}x}+\dots+c_{n}e^{r_{n}x}
$$

Case: Some of $r_{1},r_{2},\dots,r_{n}$ are repeated
- General Solution is the 
Case: Some of $r_{1},r_{2},\dots r_{n}$ are complex
$$
y=e^{\alpha x}(c_1\cos(\beta x)+c_2\sin(\beta x))
$$
Case: Repeated complex roots

