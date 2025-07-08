---
{"dg-publish":true,"dg-path":"MATH/Adv Calc/Power Series.md","permalink":"/math/adv-calc/power-series/","created":"2024-09-25T12:59:56.784-04:00","updated":"2025-07-08T11:02:45.981-04:00"}
---

A series
$$
\sum_{n=0}^\infty b_{n}(x-a)^n
$$
Where x is a variable, $b_{n}$ a real-valued coefficient, and the series is centered about $x=a$
- If $x=a,$ all terms but the first one are zero, so the series always converges $x=a$

A power series may converge for some $x$'s and diverge for others

As $x=a$ always converges, we can find a symmetric radius $R$ around $x=a$ such that a power series converges if $|x-a|<R$ and diverges for $|x-a|>R$
- $R\text{ is called the radius of convergence}$

All values of $x$ within $R$ units of $x=a$ produce a convergent series
$$|x-a|<R\to a-R<x<a+R$$

The [[1-Recent/Academics/MATH/Adv Calc/Convergence of Series#Ratio Test\|Ratio Test]] is often used to find $R$ since it produces a relationship involving $|x-a|$
- Convergence will occur when the limit in the ratio test is $<1,$ and the limit will involve $x$

The interval of convergence consists of all values of $x$ within the radius of convergence and will always be at least $(a-R, a+R)$ but may also include one or both endpoints of this interval 
- Ratio Test in inconclusive for $\lim_{ n \to \infty }=1$, so it does not provide information about the endpoints of the interval
- needs to be manually checked


Knowing that $\sum ar^n$ converges to $\frac{a}{1-r}$, we can manipulate the function $\frac{1}{1-x}$ to build power series to other functions
$$
\frac{1}{1-x}=\sum_{n=0}^\infty x^n,\  |x|<1
$$
$$
f(x)=\frac{x^3}{1+4x^2}=\frac{1}{1-(-4x^2)}\cdot x^3 =\sum_{n=0}^\infty (-4x^2)^nx^3 \ ,|-4x^2| < 1 \to \sum_{n=0}^\infty(-1)^n4^nx^{2n+3},\ |x|< \frac{1}{2}
$$

We can also integrate, differentiate, etc to manipulate the functions
