---
{"dg-publish":true,"dg-path":"MATH/Differential Equations/Differential Equations.md","permalink":"/math/differential-equations/differential-equations/","created":"2024-09-06T15:04:34.343-04:00","updated":"2025-07-08T11:02:52.748-04:00"}
---

An equation that provides a relationship between a function and its derivatives with respect to 1+ variables
$$
x''(t)+x(t)=e^t
$$
- one possible solution $\to x(t)=\frac{1}{2}e^t$

Solving the Differential Equation is the process of determining which functions $y(x)$ will satisfy the DE
# Dependent/Independent Variables
Using $x''(t)+x(t)=e^t$ :
- x is the dependent variable
- t is the independent variable

The value of x depends on the value of t
- variables being differentiated with respect to are the independent variables

Ordinary Differential Equations (ODEs) only contain one dependent variable and one independent variable
$\frac{dy}{dx}\left( y+\frac{dy}{dx} \right)=y\to y'(x)(y(x)+y'(x))=y(x)$
- y is dependent, x is independent
$\frac{d}{dt}\left( x \frac{dx}{dt} \right)=\arctan(t)$
- x is dependent, t is independent

Partial Differential Equations (PDEs) contain one dependent variable and 1+ independent variable (contains partial derivatives)
$$
r\frac{\partial^2r}{\partial\theta^2}=\frac{\partial r}{\partial t}
$$
# Order of a DE
The order is a number equal to the order of the highest derivative that appears in the equation
$\frac{d^3y}{dt^3}-t\frac{dy}{dt}+7y^4=0$
- order = 3
$Dy = \sec^ 2(t)$
- order = 1
- $D^n$ means nth derivative
[[1-Recent/Academics/MATH/Differential Equations/Linear DEs\|Linear DEs]]