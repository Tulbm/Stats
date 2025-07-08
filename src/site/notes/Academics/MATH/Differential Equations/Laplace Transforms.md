---
{"dg-publish":true,"dg-path":"MATH/Differential Equations/Laplace Transforms.md","permalink":"/math/differential-equations/laplace-transforms/","created":"2024-11-01T14:54:35.653-04:00","updated":"2025-07-08T11:02:52.778-04:00"}
---

$$
F(s)
$$

Converting functions into Laplace Transforms makes them easier to manipulate, which can then be untransformed 
- works for finding DEs/integrals of difficult functions
$$
\begin{align}
\mathcal{L}\{c\} & =\frac{c}{s} \, \, \, \, \text{(constant)}\\
\mathcal{L}\{e^{at}\} & =\frac{1}{s-a} \\
\mathcal{L}\{\cos(wt)\} & =\frac{s}{s^2+w^2} \\
\mathcal{L}\{\sin(wt)\} & =\frac{w}{s^2+w^2} \\
\mathcal{L}\left\{ \frac{e^x-e^{-x}}{2} \right\}=\mathcal{L}\{h\sin(wt)\} & =\frac{w}{s^2-w^2} \\
\end{align}
$$
Transforms of derivatives:
$$
\begin{align} \\
\mathcal{L}\{f'(t)\} & =s\mathcal{L}\{f(t)\}-f(0) \\
\mathcal{L}\{f^{(n)}(t)\} & =s^n\mathcal{L}\{f(t)\}-s^{n-1}f(0)-s^{n-2}f'(0)-\dots sf^{(n-2)}(0)-f^{(n-1)}(0)
\end{align}
$$
Transforms of powers:
$$
\mathcal{L}\{t^n\}=\frac{n!}{s^{n+1}}, \quad s>0, n\in\mathcal{N}
$$
- Doesn't work for negative powers, as the integrals needed for the definition of the laplace transform doesn't converge
- for non-integers, $\gamma$ function is used to calculate the exponential of fractions

Transform of $e^{at}f(t)$
$$
\mathcal{L}\{e^{at}f(t)\}=F(s-a)
$$
- $F(s)$ is the laplace transform for $f(t)$

Solution obtained is only valid for $t\geq0$
# Inverse Laplace Transforms
$$
\mathcal{L}^{-1}\{F(s)\}=f(t)
$$
The inverse Laplace Transform is also a linear operator
$$
\mathcal{L}^{-1}\left\{\frac{1}{(s-1)^2}+ \frac{10}{s-1}\right\}=t e^t+10e^t
$$
This can be used with factoring, [[Academics/MATH/Calculus/Partial Fractions\|Partial Fractions]] and other techniques to simplify the inversing

# Laplace Transforms of Heaviside Functions
$$
u(t)=\begin{cases}
0\quad, t<0 \\
1\quad,t>0
\end{cases}
$$
$$
\mathcal{L}\{u(t-a)f(t-a)\}=e^{-as}F(s)
$$
- $\mathcal{L}\{f(t)\} = F(s)$
$$
\mathcal{L}^{-1}\{e^{-as}F(s)\} = u(t-a)f(t-a)
$$
- $f(t)=\mathcal{L}^{-1}\{F(s)\}$

# Dirac Delta
An impulse function representing instantaneous behaviour
$$
\delta_{\epsilon}(t)=\begin{cases}
\frac{1}{2\epsilon} \quad \text{if}-\epsilon<t<\epsilon \\
0 \quad \,\,\text{ if }|t|\geq\epsilon
\end{cases}
$$

$\int \delta(t)dt=1$

