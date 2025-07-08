---
{"dg-publish":true,"dg-path":"CIS/Discrete Structures/Counting.md","permalink":"/cis/discrete-structures/counting/","created":"2024-02-01T17:06:17.102-05:00","updated":"2025-07-08T10:47:55.318-04:00"}
---

## Fundamental Counting
- Sum Rule
	- or = +
- Product Rule
	- and = $\cdot$
	- with replacement = $8^3$ 
	- without replacement = $8\cdot 7\cdot 6$
# Lists
An ordered arrangement of the elements of some set S
- S = {a,n,p}
- all possible lists are: anp, apn, nap, npa, pna, pan $6 = 3!$
# Permutations
A list containing the elements of a set

A permutation $P_n:a_1a_2...a_n$ can be interpreted as a function 
- $P_n : \{1,2,...,n\}\longrightarrow\{1,2,...,n\},\ P_n(i)=a_i$:
- a mapping from a set to a specific list

$L = {1,2,3...}$ = identity permutation (the order doesn't change)

Number of full permutations of a set S = $|S| !$
- |S| = number of elements of S (cardinality)

Permutations of size $k$ 
- a partial list of size 3 from a set with 5 elements = $5\cdot4\cdot 3=\frac{n!}{(n-k)!}={}_{n}P_{k}$

Circle Permutations (starting positions don't matter)
- $n!$ possible permutations with n different starting positions = $\frac{n!}{n}=(n-1)!$ 

Permutations where k of the n elements are indistinguishable
- $n!$ total permutations, number of possible orderings of the k elements = $k!$ $\to \frac{n!}{k!}$ 
# Combinations
Combinations with sets of distinct elements
- i.e. how many subsets of size n can we make from S
$$\frac{n!}{(n-k)!k!}= \begin{pmatrix} n\\k \end{pmatrix}={}_{n}C_{k}=\frac{{}_{n}P_{k}}{k!}$$

If we have k groups $\to \frac{n!}{n_{1}!n_{2}!\dots n_{k}!}= \begin{pmatrix} n\\n_{1} \end{pmatrix}\begin{pmatrix} n-n_{1}\\n_{2} \end{pmatrix}\dots\begin{pmatrix} n-n_{1}-\dots-n_{k-1}\\n_{k} \end{pmatrix}$ 
- $n_{i}=$ number of elements in the $i$th group ($n_{1}+n_{2}+\dots+n_{k}=n$)
- when $k=2$, we get the binomial coefficient $\frac{n!}{k_{1}!k_{2}!} {}_{n}C_{k}=\frac{n!}{(n-k)!k!}$
- both sides represent the same ([[Academics/CIS/Discrete Structures/Bijection\|Bijection]])

# Division Rule
- if B is a finite set and $f:A\longrightarrow B$ maps precisely k items of A to every item of B then A has k times as many items as B
	- $|A|=k|B|$
# Multisets
- a sequence of non-negative integers with k-different element types
- $(a_1,a_2,...,a_k)\longrightarrow$ all different types of elements
- $a_1+a_2+...+a_k=n\longrightarrow$ n = total elements in the multiset
- number of n-element multisets of k types
	-  $\begin{pmatrix} n+k-1\\k-1 \end{pmatrix}$ 

[[Academics/CIS/Discrete Structures/Counting Theorems\|Counting Theorems]]
