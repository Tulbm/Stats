---
{"dg-publish":true,"permalink":"/academics/math/adv-calc/series/","created":"2024-09-11T12:58:26.689-04:00","updated":"2025-07-08T11:02:45.999-04:00"}
---

 A series is the sum of the elements in a (in)finite sequence
$$
\sum_{n=1}^\infty a_{n}=a_{1}+a_{2}+\dots
$$
# Partial Sums
The $N^{th}$ partial sum of the series $\sum a_{n}$ is the sum of the first $N$ terms of other series
$$
S_{N}=\sum_{n=1}^Na_{n}=a_{1}+a_{2}+\dots+a_{N}
$$
We can use sequences of partial sums to analyze the original series of a sequence
$$
S_{1},S_{2},S_{3}\dots=\{S_{N}\}_{N=1}^\infty
$$
$$
\lim_{ n \to \infty } S_{N}=S \to \sum_{n=1}^\infty a_{n} \text{ converges to }S
$$
If the sequence of partial sums doesn't have a finite limit, the series diverges

[[Academics/MATH/Adv Calc/Convergence of Series\|Convergence of Series]]
# Geometric Series
$$
\sum _{n=0}^\infty ar^n=a+ar+ar^2+\dots
$$
- $|r|<1\to \sum a_{n}$ converges to $\frac{a}{1-r}$
- $|r|\geq1\to \sum a_{n}$ diverges
(when the series starts at $n = 0$)

Using infinite [[Academics/CIS/Discrete Structures/Summation Notation\|sum rules]] to solve the limits of series 
$\sum_{n=1}^\infty \frac{2^{2n-1}}{3^n}=\sum_{n=0}^\infty \frac{1}{3}\left( \frac{2}{3} \right)^ n$
$\frac{a}{1-r}=1$

Geometric series up to $x:$
$$
\sum_{n=0}^{x} a r^n = \frac{a(1-r^{x+1})}{1-r}
$$
# P-Series
$$
\sum_{n=1}^\infty \frac{1}{n^p}, p>0
$$
Series converges for $p>1$ and diverges for $0<p\leq1$ 
# Collapsing/Telescoping Series
A series in which most terms cancel out

$$
\sum_{n=2}^\infty \frac{1}{n-1}-\frac{1}{n}=1-\frac{1}{2}+\frac{1}{2}-\frac{1}{3}+\frac{1}{3}+\dots+\frac{1}{n}-\frac{1}{n+1}
$$
$$
\lim_{ n \to \infty } S_{n}=1-\frac{1}{n+1}=1
$$
