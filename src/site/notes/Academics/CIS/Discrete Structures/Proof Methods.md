---
{"dg-publish":true,"permalink":"/academics/cis/discrete-structures/proof-methods/","created":"2023-11-06T23:13:30.055-05:00","updated":"2025-07-08T10:47:55.483-04:00"}
---

## Logical reasoning
- premise in class, hypothesis in zybook
- argument = entire list of hypothesis
- conclusion = final proposition
- using truth tables
	- in the rows where all the hypothesis are true, conclusion needs to be true
		- if not -> argument is not valid

## Rules of inference with propositions
- famous rules of inferences
	- modus ponens
		- ![[Pasted image 20231106235002.png\|Pasted image 20231106235002.png]]
	- modus tollens
		- ![](https://i.imgur.com/aZNAMnI.png)
	- addition
		- ![](https://i.imgur.com/usnTluv.png)
	- simplification
		- ![](https://i.imgur.com/j5KFlQb.png)
	- conjunction
		- ![](https://i.imgur.com/KZoKbLB.png)
	- hypothetical syllogism
		- ![](https://i.imgur.com/5xL4YKv.png)
	- disjunctive syllogism
		- ![](https://i.imgur.com/tFhCzrK.png)
	- resolution
		- ![](https://i.imgur.com/iHe21Ub.png)
- logical proof
	- is a sequence of steps, each of which consists of a proposition and a justification.
	- ![](https://i.imgur.com/Ji0YI6h.png)
## Rules of inference with quantifiers
- quantifiers
	- = for all, there exists
- to apply the rules of inference to quantified expressions we need to remove the quantifier by plugging in a value from the domain to replace the variables
	- a value that can be plugged in is called an element
		- arbitrary elements of a domain have no special properties
		- particular elements may have properties that other elements of the domain do not
			- set of all integers -> 3 is a particular element, as not every integer is odd like 3
			- Any element defined in a hypothesis is a particular element
- Rules of inference for quantified statements
	- ![](https://i.imgur.com/53Q9CwB.png)
	- ![](https://i.imgur.com/9WLRRCF.png)
	- incorrect use of existential instantiation
		- ![](https://i.imgur.com/fcNjFCY.png)

## Mathematical Definitions
- even and odd
	- An integer x is even if there is an integer k such that x = 2k.
	- An integer x is odd if there is an integer k such that x = 2k+1.
	- parity
		- The parity of a number is whether the number is odd or even. If two numbers are both even or both odd, then the two numbers have the same parity. If one number is odd and the other is even, then the two numbers have opposite parity.
- rational
	- A number r is rational if there exist integers x and y such that y ≠ 0 and r = x/y
- divides
	- An integer x divides an integer y if and only if x ≠ 0 and y = kx, for some integer k
	- The fact that x divides y is denoted x|y
	- If x divides y, then y is said to be a multiple of x, and x is a factor or divisor of y
- prime and composite numbers
	- An integer n is prime if and only if n > 1, and the only positive integers that divide n are 1 and n.
	- An integer n is composite if and only if n > 1, and there is an integer m such that 1 < m < n and m divides n.
- consecutive
	- Two integers are consecutive if one of the numbers is equal to 1 plus the other number
- inequalities
	- ![](https://i.imgur.com/CIGDLbK.png)


## Introduction to proofs
- theorem
	- a statement that can be proven to be true
- proof
	- consists of a series of steps, each of which follows logically from assumptions, or from previously proven statements, whose final step should result in the statement of the theorem being proven
- axioms
	- statements assumed to be true
		- used in proofs
- methods
	- proof by exhaustion
		- if domain is small, can just check every element of the domain
	- universal generalization
		- names an arbitrary object in the domain and proves the statement for that object
	- counterexamples
		- an assignment of values to variables that shows that a universal statement is false
		- for conditional statements
			- must satisfy all the hypotheses and contradict the conclusion.
	- existential statements
		- existence proof
			- A proof that shows that an existential statement is true
		- constructive proof of existence
			- gives a specific example of an element in the domain or a set of directions to construct an element in the domain that has the required properties
		- to disprove
			- prove that every single element of the domain does not have the required properties

## Writing direct proofs
- direct proof of a conditional statement
	- the hypothesis p is assumed to be true and the conclusion c is proven as a direct result of the assumption
		- ![](https://i.imgur.com/Sm2zeaI.png)
## Proof by contrapositive
- called proof by contraposition in lectures
- proves a conditional theorem of the form p → c by showing that the contrapositive ¬c → ¬p is true
	- remember to apply de morgan's to the statements
- with multiple hypothesis
	- ![](https://i.imgur.com/jDhuqcy.png)

## Proof by contradiction
- starts by assuming that the theorem is false and then shows that some logical inconsistency arises as a result of the assumption
	- assumption ¬t and leads to a conclusion r ∧ ¬r
		- r = a and b are positive
		- ![](https://i.imgur.com/KyzfuHa.png)
- sometimes called an indirect proof
- A proof by contrapositive is a special case of a proof by contradiction
	- can be recast as as proof by contradiction
		- Proofs by contradiction are more general than proofs by contrapositive because a proof by contradiction of the theorem p → q could start with the assumption p ∧ ¬q and conclude with a contradiction other than p ∧ ¬p. Also, proof by contrapositive is a proof technique that is specific to proofs of conditional statements, whereas a proof by contradiction can be used to prove theorems that are not of the form p → q.
- the sqrt 2 proof

## Proof by cases
- breaks the domain for the variable into different classes and gives a different proof for each class
	- every value in the domain must be in at least one class
		- can also be include in more than one
		- like odd and even for integers
			- ![](https://i.imgur.com/g7hnqrs.png)
	- proof for each class is called a case
- WLOG
	- without loss of generality
	- if the proofs of 2 cases are similar
		- ![](https://i.imgur.com/g6mzy8N.png)

## Mathematical Induction
- The zyBook uses the terms **_mathematical induction_**, **_inductive proof_**, and **_base case_**, while in class we use the terms **_induction_**, **_proof by induction_**, and **_basis step_** instead.
- Induction is a proof technique that is especially useful for proving statements about elements in a sequence
- two components
	- base case
		- proves the theorem true for the first value
	- inductive step
		- proves that if n is true, then n+1 is also true
		- a compact way to state that an infinite sequence is true
	- ![](https://i.imgur.com/pc6DZ9y.png)
- summation notation
	- ![](https://i.imgur.com/ELA0To7.png)
	- left side means 1 +2 +3 +4 +5