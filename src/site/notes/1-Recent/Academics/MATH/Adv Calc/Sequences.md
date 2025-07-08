---
{"dg-publish":true,"dg-path":"MATH/Adv Calc/Sequences.md","permalink":"/math/adv-calc/sequences/","created":"2024-09-06T12:53:23.940-04:00","updated":"2025-07-08T11:02:45.990-04:00"}
---

Any ordered list of numbers

Can be represented by a function using a general term
$\{a_{n}\}_{n=1}^{\infty}$
- even = 2n
- odd = 2n+1/2n-1

Most notable(well-known) sequences are [[1-Recent/Academics/CIS/Discrete Structures/Discrete Sequences\|Discrete Sequences]]
# Limits of Sequences
$$
\lim_{ n \to \infty } a_{n}=L
$$
For every, $\epsilon >0$, there exists N>0 such that if $n\geq N$, then $a_{n}-L<\epsilon$

Limit laws applied to sequences
- $\lim_{ n \to \infty }a_{n}^p=(\lim_{ n \to \infty }a_{n})^p$
- $\lim_{ i \to \infty }a_{n}$ and $f$ is continuous at $L$ $\to$ $\lim_{ n \to \infty }f(a_{n})=f(L)$
- $\lim_{ n \to \infty }|a_{n}|=0 \to \lim_{ n \to \infty }a_{n}=0$
- $\lim_{ n \to \infty }a_{2n}=L$ and $\lim_{ n \to \infty }a_{2n+1} =L \to$ $a_{n}$ converges to $L$
- [[1-Recent/Academics/MATH/Calculus/L'Hopital's Rule\|L'Hopital's Rule]]
- [[1-Recent/Academics/MATH/Calculus/Theorems#Squeeze Theorem\|Squeeze Theorem]]
# Recursive Sequences
$$
a_{n+1}=f(a_{n},a_{n-1},a_{n-2},\dots)
$$
Sequences like the fibonnaci or the geometric sequence where there is one common ratio between all the terms $r$
- $a_{n+1}=ra_{n}$

Qualitative information is used to determine the limits of a recursive sequence
- $a_{n}<a_{n+1}$ for all $n\geq1$$\to \{a_{n}\}$ is monotone **increasing**
- $a_{n}>a_{n+1}$ for all $n\geq1$$\to \{a_{n}\}$ is monotone **decreasing**

Which can be extracted using inequalities and calculus
- derivatives
- [[1-Recent/Academics/CIS/Discrete Structures/Discrete Sequences#Induction\|Discrete Sequences#Induction]]

# Bounds

$\{a_{n}\}$ is bounded above if $\exists M \in {R}$ such that $\forall$ n, $M\geq a_{n}$
$\{a_{n}\}$ is bounded below if $\exists m \in {R}$ such that $\forall$ n, $m\leq a_{n}$

# Monotone Increasing/Decreasing Sequence Theorem
- If a sequence is monotone increasing/decreasing and they have a bound below or above, $L \leq M$ / $L \geq M$ (inc/dec)






