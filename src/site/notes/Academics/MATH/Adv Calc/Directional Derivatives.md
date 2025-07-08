---
{"dg-publish":true,"dg-path":"MATH/Adv Calc/Directional Derivatives.md","permalink":"/math/adv-calc/directional-derivatives/","created":"2024-10-25T12:54:42.642-04:00","updated":"2025-07-08T11:02:45.915-04:00"}
---

Normal derivatives are taken with respect to one variable, i.e. going along its axis

Directional Derivatives are taken with respect to directions beside the standard horizontal and vertical axis

The direction will be defined by a vector
- as there are infinite vectors, we default to an unit vector (length one for each direction
$$
||\tilde{u}||=\sqrt{ u_{1}^2 +u_{2}^2}=1
$$

The slope of the tangent line to the intersection of a plane in the direction with the surface at $(x,y)$ is the directional derivative of $f(x,y)$ in the direction $\tilde{u}$
$$
D_{\tilde{u}}f(x,y)
$$

$$
D_{\tilde{u}}f(a,b)=\lim_{ h \to 0 } \frac{f(\tilde{a}+h\tilde{u})}{h}=\lim_{ h \to 0 } \frac{f(a+hu_{1},b+hu_{2})-f(a,b)}{h}
$$


If $f$ is a differentiable function of $x$ and $y$ then $f$ has a directional derivative in the direction of any unit vector $\tilde{u}=(u_{1},u_{2})$ given by
$$
D_{\tilde{u}}f(a,b)=f_{x}(a,b)\cdot u_{1}+f_{y}(a,b)\cdot u_{2}
$$

Rewriting it using a dot product
$$
D_{\tilde{u}}f(a,b)=<f_{x}(a,b),f_{y}(a,b)> \cdot <u_{1},u_{2}>
$$
The derivatives can be thought of as a [[Academics/MATH/Adv Calc/Gradient Vector\|Gradient Vector]]
$$
D_{\tilde{u}}f(a,b)=\nabla f(a,b) \cdot \tilde{u}
$$
# Largest Derivative Direction
If $f$ has continuous first partials at $\tilde{a}$ and $\nabla f(\tilde{a})\neq\tilde{0}$ then the largest value of the directional derivative $D_{\tilde{u}}f(\tilde{a})$ is $||\nabla f(\tilde{a})||$ and it occurs when $\tilde{u}$ has the same direction as the gradient vector $\nabla f(\tilde{a})$
- gradient always points in the direction of steepest ascent ($-\nabla f$ points to steepest descent)


# Level curves/surfaces
If $f(x,y)$ has continuous first partial derivatives at $(a,b)$ and $\nabla f(a,b)\neq \tilde{0}$ then $\nabla f(a,b)$ is orthogonal to the level curve $f(x,y)=k$ at $(a,b)$

