---
{"dg-publish":true,"permalink":"/academics/math/differential-equations/integrating-factor/","created":"2024-10-04T14:47:02.768-04:00","updated":"2025-07-08T11:02:52.763-04:00"}
---

# Integrating Factor
Use the Product Rule to convert the DE into a form where we can apply Direct Integration
$$
t^2y^{\prime}+2ty=e^{2t} \to (t^2y)^{\prime}=e^{2t}
$$
For DEs where the Product Rule cannot be applied directly, we can multiply every term by a function of t where product rule works
- need $\frac{d}{dt} \mu(t) = 2\mu(t)$ in this case
$$
y^{\prime}+2y=5 \to \mu(t)y'+2\mu(t)y=5\mu(t)
$$
$\mu$ in this case will be $\mu=ce^{2t}$ after integrating, so any of those possible integrating factors will get the DE in the form required to use Product Rule
$$
e^{2t}y'+2e^{2t}y=5e^{2t}\to (e^{2t}+y)'=5e^{2t}
$$
And then we can Integrate with respect to t:
$$
e^{2t}y=\int5e^{2t}dt=\frac{5}{2}e^{2t}+C
$$
So $y = \frac{5}{2}e^{2t} \frac{1}{e^{2t}}+ \frac{C}{e^{2t}}=\frac{5}{2}+C$

In general, for a first order linear DE in standard form
$$
y'+p(t)y=g(t)
$$
Will always allow us to find an integrating factor $\mu(t)$ as
$$
\mu(t)=e^{\int p(t)dt}
$$

[[Academics/MATH/Differential Equations/Exact Equations\|Exact Equations]]