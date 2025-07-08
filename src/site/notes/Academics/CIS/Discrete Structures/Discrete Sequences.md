---
{"dg-publish":true,"dg-path":"CIS/Discrete Structures/Discrete Sequences.md","permalink":"/cis/discrete-structures/discrete-sequences/","created":"2024-01-10T14:30:52.450-05:00","updated":"2025-07-08T10:47:55.390-04:00"}
---

## Sequences
- subsequences{a,b,c}
	- cant be a rearrengement of a sequence
		- can only "remove" elements from a sequence
	- number of subsequences = 2^n
	- consecutive
		- number = n(n+1)/2 (+1 if including empty)
			- ${n+1\choose 2} =$ choosing 2 positions to be start/end
		- {},{a},{a,b},{b,c}
	- non-consecutive
		- number of = 
		- {a,c}
- properties
	- increasing
		- an+1>an
	- non-increasing
	- decreasing
	- non-decreasing
	- monotonic
		- if its either non-decreasing or non-increasing
		- always increasing or decreasing, no going the other way at any point
- arithmetic sequences
	- common difference between two terms ( +/- )
	- $a_{n}=a_{1}+(n-1)\ d$
- geometric sequence
	- common ratio between two terms ( x / / )
- heron's method
	- a sequence-based algorithm that iteratively calculates square roots
	- ![](https://i.imgur.com/uKHQboq.png)
	- an-1 = first guess
	- x = number trying to be square rooted
- newton's method
	- a sequence-based algorithm that iteratively calculates square roots of functions
	- ![](https://i.imgur.com/yfjwS9T.png)

## Summation and Product Notation
- [[Academics/CIS/Discrete Structures/Summation Notation\|Summation Notation]]
- [[Academics/CIS/Discrete Structures/Product Notation\|Product Notation]]
## Induction
- proof by induction
	- ![](https://i.imgur.com/BGNVuaj.png)
	- basis step
	- inductive hypothesis
		- for (domain of what is being proved), we assume (formula/sequence/recurrance relation)
	- inductive conclusion
		- by IH, 
- proof by strong induction
	- ![](https://i.imgur.com/oHmqbLV.png)
	- difference = can look back more than one step
	- in IH -> i = 1,2,3,...,k
	- in IC -> prove for k
		- all numbers before k are proved


