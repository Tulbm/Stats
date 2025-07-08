---
{"dg-publish":true,"dg-path":"MATH/Adv Calc/Critical Points.md","permalink":"/math/adv-calc/critical-points/","created":"2024-11-01T12:51:02.143-04:00","updated":"2025-07-08T11:02:45.866-04:00"}
---

The critical point can be a maximum, minimum or neither
- slope changes from increasing to decreasing, point is a local maximum
- slope changes from decreasing to increasing, point is a local minimum

If $f$ is differentiable at $x=a$ that attains a maximum or minimum value at $x=a$, then $f'(a)=0$

If $f$ is twice differentiable at a critical point $(a,f(a))$ then:
- if $f''(a)>0\to(a,f(a))$ is a local minimum
- if $f''(a)<0\to (a,f(a))$ is a local maximum

# Multi-Variable

If $f(x,y)$ has continuous first partial derivatives and $(a,b)$ is a local maximum or minimum of $f(x,y)$ then $f_x(a,b)=0$ and $f_y(a,b)=0$

### Hessian matrix

$$
Hf(x,y)=\begin{pmatrix}
f_{xx}(x,y) & f_{xy}(x,y) \\
f_{yx}(x,y) & f_{yy}(x,y)
\end{pmatrix}
$$
#### Second derivative test
Suppose that $f(x,y)$ has continuous second partial derivatives near$(a,b)$ and  $f_{x}(a,b)$ $=f_{y}(a,b)=0$ (critical point)

If $Hf(a,b)$ is
1. positive definite then $(a,b)$ is a local minimum of $f$
- det$(Hf(a,b))>0,\quad f_{xx}(a,b)>0$
2. negative definite then $(a,b)$  is a local maximum of $f$
- det($Hf(a,b))>0,\quad f_{xx}(a,b)<0$
3. indefinite then $(a,b)$ is a saddle point of $f$
- $\det(Hf(a,b))<0$


