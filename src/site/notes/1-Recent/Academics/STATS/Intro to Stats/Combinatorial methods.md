---
{"dg-publish":true,"permalink":"/1-recent/academics/stats/intro-to-stats/combinatorial-methods/","created":"2024-03-29T19:10:34.066-04:00","updated":"2025-07-07T17:28:36.579-04:00"}
---

In [[1-Recent/Academics/CIS/Discrete Structures/Probability\|Probability]] and [[1-Recent/Academics/STATS/Math Stats 1/Statistics\|Statistics]], it is an important first step to determine all the possible outcomes of an experiment using [[1-Recent/Academics/CIS/Discrete Structures/Counting\|Counting]] and [[1-Recent/Academics/MATH/Number Theory/Combinatorial Number Theory\|Combinatorial Number Theory]] methods
- direct enumeration
- permutations
- combinations

# combination formula/binomial coefficient
- gives us the number of ways of choosing x items (w/o replacement) from n distinct items if order of selection is not important
- choose(n,x) on [[1-Recent/Academics/STATS/R\|R]]
- $$  \begin{pmatrix}   n\\   x   \end{pmatrix}= \frac{n!}{x!(n-x)!}$$
- example
	- lotto 6/49, buyers pick 6 numbers from 1-49
	- how many different tickets are possible
	- $$  \begin{pmatrix}   49\\ 6 \end{pmatrix}= \frac{49!}{6!(49-6)!}$$