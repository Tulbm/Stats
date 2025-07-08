---
{"dg-publish":true,"dg-path":"CIS/Discrete Structures/Counting Theorems.md","permalink":"/cis/discrete-structures/counting-theorems/","created":"2024-09-10T16:05:23.646-04:00","updated":"2025-07-08T10:47:55.273-04:00"}
---

# Basic Counting Properties
- $\begin{pmatrix} n\\0 \end{pmatrix} = 1; \begin{pmatrix} n\\n \end{pmatrix} = 1$
- $\begin{pmatrix} n\\k \end{pmatrix}=\begin{pmatrix} n\\n-k \end{pmatrix}\longrightarrow$ pairs
- $\binom{n}k=\frac{n}{k}\binom{n-1}{k-1}$

Number of subsets of a set with size n (power set)
$$\begin{pmatrix} n\\0 \end{pmatrix}+\begin{pmatrix} n\\1 \end{pmatrix}+\begin{pmatrix} n\\2 \end{pmatrix}+\ ...\ +\begin{pmatrix} n\\n \end{pmatrix}=\sum_{k=0}^n\begin{pmatrix} n\\k \end{pmatrix}=2^n$$
Left side is equal to $2^n$ by [[1-Recent/Academics/CIS/Discrete Structures/Bijection\|Bijection]]

# Pascal's Identity
For any integer $n$ and $0\leq k<n$ 
$$\begin{pmatrix} n\\k \end{pmatrix}=\begin{pmatrix} n-1\\k-1 \end{pmatrix}+\begin{pmatrix} n-1\\k \end{pmatrix}\iff\begin{pmatrix} n\\k \end{pmatrix}-\begin{pmatrix} n-1\\k \end{pmatrix}=\begin{pmatrix} n-1\\k-1 \end{pmatrix}$$
$\begin{pmatrix} n-1\\k-1 \end{pmatrix}$ counts the subsets with one element already selected

$\begin{pmatrix} n-1\\k \end{pmatrix}$ counts all subsets where that same element cannot be selected

As they are 2 separate scenarios, we add the possibilities ([[1-Recent/Academics/CIS/Discrete Structures/Counting#Fundamental Counting]\|Sum Rule]])
# Binomial Theorem
$$(x+y)^n=\sum_{k=0}^n\begin{pmatrix} n\\k \end{pmatrix}x^ky^{n-k}=\sum_{k=0}^n\begin{pmatrix} n\\k \end{pmatrix}x^{n-k}y^k$$

For example
$$(x+y)^4=x^0y^4+4x^1y^3+6x^2y^2+4x^3y^1+x^4y^0$$

Therefore the coefficient for $x^k$ is $\begin{pmatrix} n\\k \end{pmatrix}=\begin{pmatrix} n\\n-k \end{pmatrix}$

# Vandermonde's (Zhu Shijie's) Identity
$$\begin{pmatrix} m+n\\r \end{pmatrix}=\sum_{k=0}^r\begin{pmatrix} m\\k \end{pmatrix}\begin{pmatrix} n\\r-k \end{pmatrix}$$
$\begin{pmatrix} m+n\\r \end{pmatrix}$ is the coefficient of $y^r$ when expanding $(1+y)^{m+n}$

$(1+y)^{m+n}= (1+y)^{m}(1+y)^{n}=()$ 


Generalized for any number of $n$s
$$\begin{pmatrix} n_1+...+n_p\\r \end{pmatrix}=\sum_{k_1+...+k_p=r}^r\begin{pmatrix} n_1\\k_1 \end{pmatrix}\begin{pmatrix} n_2\\k_2 \end{pmatrix}\begin{pmatrix} n_p\\k_p \end{pmatrix}$$= $\begin{pmatrix} r+p-1\\p-1 \end{pmatrix}$ = multiset with p groups of r

# Inclusion/Exclusion Principle
- sets = no repeated elements
- $|A|+|B| =|A\cup B|-|A\cap B| = |A|+|B|-|AB|$    
- $$|A_1\cup A_2\ \cup\ ...\ \cup\ A_n|= \sum_{S\neq 0,S\subseteq\{1,...,n\}}(-1)^{|S|-1}|A_S|$$
# Others

$$
n^2\binom{2n-2}{n-2}=\sum_{j=1}^nj(n-j)\binom{n}{j}^2
$$

