---
{"dg-publish":true,"dg-path":"MATH/Differential Equations/Second-Order Linear DEs.md","permalink":"/math/differential-equations/second-order-linear-d-es/","created":"2024-10-09T14:52:58.115-04:00","updated":"2025-07-08T11:02:52.847-04:00"}
---

# Second-Order Linear DEs
Can always be arranged into the form
$$
y''+p(t)y'+q(t)y=g(t)
$$
where $p,q$ and $g$ are continuous on at least some open interval

With operator notation, we can rewrite the DEs as:
$$\begin{align}
L & =D^2+pD+q  \\
L[y] & =g(t)
\end{align}
$$


# Superposition Principle of Solution to Linear Homogeneous ODEs

brahbrahbrah
wronskian

[[1-Recent/Academics/MATH/Differential Equations/Linear Dependence\|Linear Dependence]]

# Homogeneous Linear Second-Order DEs with Constant Coefficients

$$
ay''(x)+by'(x)+cy(x)=0
$$



$$
ar^2+br+c=0
$$
This polynomial is called the **characteristic equation** of the DE
$$
r=\frac{-b\pm\sqrt{ b^2-4ac }}{2a}
$$

Case 1: $r_{1}$ and $r_{2}$ are real roots, $r_{1}\neq r_{2}$
$y_{1}=c_{1}e^{r_{1}x}, y_{2}=c_{2}e^{r_{2}x}$
$$
y(x)=c_{1}e^{r_{1}x}+c_{2}e^{r_{2}x}
$$
Case 2: $r_{1}$ and $r_{2}$ are real roots, $r_{1}=r_{2}$
$b^2-4ac=0\to r_{1}=e^{}$# Homogeneous Linear Second-Order DEs with Constant Coefficients

$$
ay''(x)+by'(x)+cy(x)=0
$$



$$
ar^2+br+c=0
$$
This polynomial is called the **characteristic equation** of the DE
$$
r=\frac{-b\pm\sqrt{ b^2-4ac }}{2a}
$$

Case 1: $r_{1}$ and $r_{2}$ are real roots, $r_{1}\neq r_{2}$
$y_{1}=c_{1}e^{r_{1}x}, y_{2}=c_{2}e^{r_{2}x}$
$$
y(x)=c_{1}e^{r_{1}x}+c_{2}e^{r_{2}x}
$$
Case 2: $r_{1}$ and $r_{2}$ are real roots, $r_{1}=r_{2}$
$b^2-4ac=0\to r_{1}=e^{}$

Case 3: $r_{1}$ and $r_{2}$ are a complex pair
$r=\alpha\pm i\beta$

$y=c_{1}e^{\alpha+i\beta x}+c_{2}e^{\alpha-i\beta x}$

$$
\begin{align}

e^{\alpha+i\beta x}=e^{\alpha x}e^{i\beta x}=e^{\alpha x}(\cos(\beta x)+i\sin(\beta x)) \\

e^{\alpha-i\beta x}=e^{\alpha x}e^{i(-\beta x)}=e^{\alpha x}(\cos(-\beta x)+i\sin(-\beta x))
\end{align}
$$

$$
y=e^{\alpha x}[(c_{1}+c_{2})\cos(\beta x)+(c_{1}-c_{2})i\sin(\beta x)]
$$

