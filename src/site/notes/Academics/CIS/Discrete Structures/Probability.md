---
{"dg-publish":true,"dg-path":"CIS/Discrete Structures/Probability.md","permalink":"/cis/discrete-structures/probability/","created":"2024-02-29T16:44:52.477-05:00","updated":"2025-07-08T10:50:45.186-04:00"}
---

The [[Academics/STATS/Intro to Stats/Probabilities concepts#Probabilities of Events\|probabilities of events]] will always be between 0 and 1 (the probability of the total sample space)

$$
0\leq P(A)\leq1
$$
# Axioms of Probability

$P(S) = 1$ 
- the total sample space (all events) has probability 1(100%)

$P(A\cup B\cup C) = P(A)+P(B)+P(C)-P(AB)-P(AC)-P(BC)+P(ABC)$ 

If $A\cap B=\emptyset$ then the 2 events are **mutually exclusive** (no elements in common)

For $A_{1},A_{2},\dots$ all mutually exclusive, $P(A_1\cup A_2\cup\cdots)=P(A_1)+P(A_2)+\cdots$
- $A_{i}\cap A_{j}=\emptyset$

$0 \leq P(A\cap B) \leq min(P(A),P(B))$
- intersection will always output a smaller set

[[Academics/STATS/Math Stats 1/Conditional probability\|Conditional probability]]


# Rule of total Probability
If the sample space S can be partitioned into events $B_{1},B_{2},\dots B_{k}$  and $P(B_{k})\neq 0$ $\forall i=1,2\dots k$ 
Then for any event A in S:
$$
P(A)=P(A|B_{1})P(B_{1})+P(A|B_{2})P(B_{2})+\dots+P(A|B_{k})P(B_{k})=\sum_{i=1}^kP(A|B_{i})P(B_{i})
$$

or rule of average conditional probability




Probability/Cumulative Discrete Distribution Functions
	- PDF
	- CDF
	- a
- Expectation
- Variance




[[Academics/CIS/Discrete Structures/Discrete Distributions\|Discrete Distributions]]
