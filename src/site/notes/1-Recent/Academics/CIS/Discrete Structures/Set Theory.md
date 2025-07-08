---
{"dg-publish":true,"dg-path":"CIS/Discrete Structures/Set Theory.md","permalink":"/cis/discrete-structures/set-theory/","created":"2023-11-19T02:08:52.374-05:00","updated":"2025-07-08T10:47:55.436-04:00"}
---

## Sets
- set = collection of objects (called elements)
	- roster notation -> A = {x,y,z}
	- order and multiplicity dont matter
- symbols
	- ∈ is used to indicate that an element is in a set, as in 2 ∈ A (2 is an element of A, 2 belongs to A, A contains 2)
	- ∉ indicates that an element is not in a set, as in 5 ∉ A 
- The set with no elements is called the empty set/null set and is denoted by the symbol ∅ / { }.
- The cardinality of a finite set A, denoted by |A|, is the number of distinct elements in A. 
	- If A = { 2, 4, 6, 10 }, then |A| = 4. The cardinality of the empty set |∅| is zero.
- ellipses (...) are used to denote a long (possibly infinite) sequence of numbers.
- Common Sets (integers etc)
 #### ![](https://i.imgur.com/Hn2NAr6.png)
- **R**+ = set of all positive real numbers
- **Z**- = set of all negative integers.
- R* = set of all nonzero real numbers
- subsets and supersets
	- If every element in A is also an element of B, then A is a subset of B, denoted as A ⊆ B. If there is an element of A that is not an element of B, then A is not a subset of B, denoted as A ⊈ B.
	- If A ⊆ B and there is an element of B that is not an element of A (i.e., A ≠ B), then A is a proper subset of B, denoted as A ⊂ B.


- ![](https://i.imgur.com/uWwaNy4.png)
	- ![](https://i.imgur.com/N5z5FRo.png)
- power sets
	- ![](https://i.imgur.com/bjMxeeS.png)
	- 2^elements
- different operators
	- difference
		- ![](https://i.imgur.com/ehwyXhm.png)
	- symmetric difference
		- A ⊕ B = ( A - B ) ∪ ( B - A )
		- ![](https://i.imgur.com/GTKncAd.png)
	- complement
		- ![](https://i.imgur.com/WSiTqL0.png)
- set identities
	- ![](https://i.imgur.com/h8itRKM.png)
- disjoint
	- 2 sets whose intersection is empty = are disjoint
- pairwise disjoint
	- every pair of distinct sets in a sequence is disjoint
- artition
	- a collection of non-empty subsets of a set such that every element is in exactly one of the subsets 
		- slicing the pie