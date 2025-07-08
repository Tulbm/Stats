---
{"dg-publish":true,"dg-path":"MATH/Differential Equations/Solution to DEs.md","permalink":"/math/differential-equations/solution-to-d-es/","created":"2024-09-09T15:11:54.992-04:00","updated":"2025-07-08T11:02:52.880-04:00"}
---

Solutions to DEs are functions instead of a number

The solution is a function that when subbed in place of the dependent variable makes the right and left side equal
$$
y''(t)+y(t)=0
$$
- $y = \cos(t)$ is one of the solutions to the DE ($-\cos(t)+\cos(t)=0$), but not the only one

The **general solution** of this DE is
$$
y(t)=C_{1}\cos(t)+C_{2}\sin(t)
$$
- $C_{1}$ and $C_{2}$ are arbitrary constants

# Initial Value Problems
IVPs are differential equations paired with a set of initial conditions
- conditions are used to narrow all infinite possible solution into one
- gives a solution that can be represented by a single solution curve (**solution trajectory**)
$$
\begin{align}
&y''(t)+y(t) = 0 \\
&y(0) = -3 \\
&y'(0) = 0
\end{align}
$$
Solving the DE with the conditions gives
$$
y(t)=-3\cos(t)+0\sin(t)
$$
## Existence and Uniqueness of Solutions to IVPs Theorem
A $n^{th}$ order linear equation
$$
y^{(n)}(t)+f_{n-1}(t)y^{(n-1)}(t)\ldots+f_2(t)y^{\prime\prime}(t)+f_1(t)y^{\prime}(t)+f_0(t)y(t)=g(t)
$$
With $n$ initial conditions
$$
\begin{align} \\
y(t_0)  & = y_0\\y^{\prime}(t_0)  & = y_0^{\prime}\\ & \cdots\\y^{(n-1)}(t_0)  & = y_0^{(n-1)}

\end{align}
$$
- $t_{0}$ needs to be the same in all conditions
- $y_{0}$ are constants

If $f_{0},f_{1}\dots,f_{{n-1}}$ and $g$ are continuous on $t_{0}$ on an open interval $\to$ $\exists$ one unique solution $y=\varphi(t)$
- theorem only proves that the solution exists throughout the interval open $(a,b)$
- p. 21+22

