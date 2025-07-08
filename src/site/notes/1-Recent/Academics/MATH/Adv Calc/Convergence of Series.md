---
{"dg-publish":true,"dg-path":"MATH/Adv Calc/Convergence of Series.md","permalink":"/math/adv-calc/convergence-of-series/","created":"2024-09-13T12:57:13.927-04:00","updated":"2025-07-08T11:02:45.897-04:00"}
---

Checking convergence of a series comes down to
- finding a general expression for $S_{n}$
- determining if $\lim_{ n \to \infty }S_{n}$ exists and is finite

For most series, finding a general expression for $S_{n}$ is not possible, so we use different methods to determine if the series diverges or converges: 
- using tests
- manipulating the series to get a [[1-Recent/Academics/MATH/Adv Calc/Series\|basic series]]

Letting $\sum a_{n}$ and $\sum b_{n}$ be series wit positive terms:
# Divergence Test
Or $n^{th}$ Term Test

$\lim_{ n \to \infty }a_{n}\neq 0$ or $\lim_{ n \to \infty }a_{n}$ does not exist $\to$ $\sum_{n=1}^\infty a_{n}$ diverges
# Integral Test
Defining the general term of the series $\sum a_{n}$ as a function $f(x)$ where $a_{n}=f(n)$

If $f$ is continuous, positive and decreasing on the interval from the series $\to$ $\sum a_{n}$ is convergent $\iff$ $\int_{1}^\infty f(x)dx$  is convergent, i.e.
- $\int_{1}^\infty f(x)dx$ converges $\iff$ $\sum_{1}^\infty a_{n}$ converges
- $\int_{1}^\infty f(x)dx$ diverges $\iff \sum_{n=1}^ \infty a_{n}$ diverges
# Comparison Tests
(Direct) Comparison Tests exploit the monotone increasing/decreasing [[1-Recent/Academics/MATH/Adv Calc/Sequences#Monotone Increasing/Decreasing Sequence Theorem\|sequence theorems]]
$$
0<a_{n}\leq b_{n} ,\ \forall n\geq1 \to \text{if } \sum b_{n} \text{ converges then} \sum a_{n} \text{ converges}
$$
$$
0<b_{n}\leq a_{n} ,\ \forall n\geq1 \to \text{if } \sum b_{n} \text{ diverges then} \sum a_{n} \text{ diverges}
$$
# Limit Comparison Test
$$
\text{If} \lim_{ n \to \infty } \frac{a_{n}}{b_{n}} =c, 0<c<\infty \to \text{both series converge or diverge}
$$
- if $c=0$ and $\sum b_{n}$ converges, $\to \sum a_{n}$ converges
- if $c=\infty$ and $\sum b_{n}$ diverges, $\to \sum a_{n}$ diverges

# Alternating Series (Leibniz) Test
Series with terms that are positive and/or negative
- like alternating between positive and negative
$$
\{a_{n}\} \text{ is a positive, decreasing series with} \lim_{ n \to \infty } a_{n}=0\to \sum_{n=1}^\infty (-1)^{n-1}a_{n}\text{ converges}
$$
If $\sum|a_{n}|$ converges, then $\sum a_{n}$ converges
## Absolutely Convergent Series
A series $\sum a_{n}$ where $\sum|a_{n}|$ converges
- $\sum \frac{(-1)^n}{n^2}$
## Conditionally Convergent Series
A series where $\sum a_{n}$ converges, but $\sum|a_{n}|$ diverges
- $\sum \frac{(-1)^n}{n}$ converges but $\sum \frac{1}{n}$ diverges ([[1-Recent/Academics/MATH/Adv Calc/Series#P-Series\|p=1]])
# Ratio Test
With $\sum a_{n}$ and $L=\lim_{ n \to \infty }| \frac{a_{n+1}}{a_{n}}|$
- $L<1 \to \sum a_{n}$ converges absolutely
- $L>1\to \sum a_{n}$ diverges
- $L=1\to$ Ratio Test is inconclusive
# Root Test
With $\sum a_{n}$ and $L=\lim_{ n \to \infty }\sqrt[^n]{|a_{n}|  }$
- $L<1 \to \sum a_{n}$ converges absolutely
- $L>1\to \sum a_{n}$ diverges
- $L=1\to$ Root Test is inconclusive

<!--⚠️Imgur upload failed, check dev console-->
![[Pasted image 20241015185558.png\|Pasted image 20241015185558.png]]