---
{"dg-publish":true,"dg-path":"MATH/Adv Calc/Multi-variable Change of Variables.md","permalink":"/math/adv-calc/multi-variable-change-of-variables/","created":"2024-12-08T15:40:57.314-05:00","updated":"2025-07-08T11:02:45.888-04:00"}
---

Using the transformation $T$ to go from variables $(f(x),f(y))$ to something simpler to integrate in the form $(u,v)$

Checking in a transformation is [[1-Recent/Academics/CIS/Discrete Structures/Functions\|injective]] (invertible) is done using the Jacobian Matrix

If $(u,v)=\tilde{T}(x,y)$ then the Jacobian of $\tilde{T}$ is
$$
\Huge J_{\tilde{T}} = \frac{\partial(u,v)}{\partial(x,y)} = \begin{pmatrix} \frac{\partial u}{\partial x} & \frac{\partial u}{\partial y} \\ \frac{\partial v}{\partial x} & \frac{\partial v}{\partial y} \end{pmatrix}
$$

# Inverse Transformation
Let $\tilde{T}:R^2\to R^2$ be a continuously differentiable ($C^1$) vector-valued function that maps $R_{xy}$ to $R_{uv}$ 

If the inverse transformation $\tilde{T}^{-1}$ exists and is $C^1$ at $\tilde{u}\in R_{uv}$ and 
$$\Huge\begin{align}
(J_{\tilde{T}^{ -1}})(J_{\tilde{T}}) & =I_{2\times2} \\
J_{\tilde{T}^{{ -1}}} & =(J_{\tilde{T}})^{-1}
\end{align}$$
Jacobian of the inverse map $\tilde{T}^{-1}$ is equal to the inverse of the Jacobian of the map $\tilde{T}$


- If $\tilde{T}$ has an inverse map, then det$(J_{\tilde{T}})\neq0$ 
Contrapositive:
- If $\huge\det(J_{\tilde{T}})=0$ then $\huge\tilde{T}$ does not have an inverse map

## Inverse Function Theorem

Suppose $(u,v)=\tilde{T}(x,y)=(T_{1}(x,y),T_{2}(x,y)),$  and $T_{1},T_{2}$ have continuous first partials in some neighbourhood of $(x,y)=(a,b)$

If $\huge\det(J_{\tilde{T}}(a,b))\neq 0$ then there is a neighbourhood of $(a,b)$ in which $\tilde{T}$ has an inverse function given by $(x,y)=\tilde{T}^{ -1}(u,v)$, where $T_{1}^{-1}$ and $T_{2}^{ -1}$ have continuous first partials

# Change of variables Theorem
Let $\tilde{T}$ be a continuously differentiable ($C^1$), one-to-one map with $\det(J_{\tilde{T}})\neq 0$ 

Suppose that $\tilde{T}$ maps a region $R_{xy}$ onto a region $R_{uv}$, where both regions are [[1-Recent/Academics/MATH/Adv Calc/Multi-variable Integration#Bounded by regions\|type 1/2]]
If $f$ is continuous on $R_{xy}$ then
$$
\huge\int _{R_{xy}}\int  f(x,y)\, dA = \int _{R_{uv}}\int f(u,v)  \left|\det(J_{\tilde{T}^{ -1}})\right|\, dA  
$$
The $\det(J_{\tilde{T}})$ indicates what kind of transformation the transformation will cause on the regions
- $\det(J_{\tilde{T}})>1\longrightarrow A_{xy}<A_{uv}$
- $\det(J_{\tilde{T}})=1\longrightarrow A_{xy}=A_{uv}$
- $0<\det(J_{\tilde{T}})<1\longrightarrow A_{xy}>A_{uv}$
- $\det(J_{\tilde{T}})<0\longrightarrow$ transformation causes a flip in the boundaries of the area

By drawing and interpreting the new transformed region, we "reflip" the bounds back to the wanted result, so only the absolute value is used for the correction
