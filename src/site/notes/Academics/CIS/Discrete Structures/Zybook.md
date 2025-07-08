---
{"dg-publish":true,"permalink":"/academics/cis/discrete-structures/zybook/","created":"2023-09-16T22:34:09.024-04:00","updated":"2025-07-08T10:47:55.461-04:00"}
---

## Strings
- A sequence of characters is called a string.
- The set of characters used in a set of strings is called the alphabet
- the length of the string xxyxyx is 6.
- binary string is a string whose alphabet is {0, 1}.
- string of length n = n-bit string
- The empty string( λ ) is the unique string whose length is 0.
	- Since {0, 1}0 is the set of all binary strings of length 0, {0, 1}0 = {λ}.
- concatenation of s and t (denoted st)
	- If s = 010 and t = 11, then st = 01011
	- concatenate a string and a single symbol: t0 = 110
	- Concatenating any string x with the empty string gives back x: xλ = x.

## Functions
- Discrete mathematics is often concerned with functions that map between other kinds of sets
	- such as binary strings or a set of tasks.
	- an assignment of people to teams, or of guests to hotel rooms, are also examples of functions.
- Definition
	- A function f that maps elements of a set X to elements of a set Y, is a subset of X × Y such that for every x ∈ X, there is _exactly one_ y ∈ Y for which (x, y) ∈ f.
- f: X → Y
	- notation to express the fact that f is a function from X to Y.
		- x = domain
		- y = codomain/target
			- not the range
			- codomain is just the list of possible values(all the employess)
				- but the function might not promote every single one of them
	- can also be denoted as (x, y) ∈ f
- arrow diagram
	- ![](https://i.imgur.com/aPuKktN.png)
	- there is exactly one arrow pointing out of every element in the domain
- well-defined functions
	- ![](https://i.imgur.com/bonsLhC.png)
	- range = {a,c,d}
		- not using all the elements is fine
	- purple arrow is the one making the function not well-defined
		- there can only be one possible value from each input
- equality(f = g)
	- f and g are equal if f and g have the same domain and target, and f(x) = g(x) for every element x in the domain.



