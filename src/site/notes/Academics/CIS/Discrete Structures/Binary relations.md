---
{"dg-publish":true,"permalink":"/academics/cis/discrete-structures/binary-relations/","created":"2023-11-21T10:21:28.384-05:00","updated":"2025-07-08T10:47:55.291-04:00"}
---

## Definition
- a binary relation between 2 sets is the subset of AxB
	- number of possible relations = cardinality of the power set of AxB
		- power set = 2^(|A| x |B|)
- arrow diagram
	- ![](https://i.imgur.com/pWg6BwI.png)
- matrix
	- first term of the tuple = height
	- second term = length
	- ![](https://i.imgur.com/VpVTEvO.png)
- self-loop
	- leaves the element and comes back to it
	- ![](https://i.imgur.com/oGrSIDt.png)

## Properties
- reflexivity
	- a binary relation is reflexive when for every x, xRx
		- (every element goes back to itself) 
	- anti-reflexive
		- if its not true that for every x, xRx
			- a relation where the element never points back to itself
	- ![](https://i.imgur.com/LDXEBha.png)
- symmetry
	- symmetric
		- R is symmetric if and only if for every pair, x and y ∈ A, xRy if and only if yRx.
			- if xRy and yRx are both true
			- or Neither xRy nor yRx is true
		- ![](https://i.imgur.com/JtfC2TV.png)
	- anti-symmetric
		- R is anti-symmetric if and only if for every pair, x and y ∈ A, if x ≠ y then it can not be the case that xRy and yRx are both true.
			- xRy, but it is not true that yRx
			- or yRx, but it is not true that xRy
			- or Neither xRy nor yRx is true
		- showing that it's anti-symmetric
			- take an arbitrary pair of elements in the domain, x and y, and show that the assumptions xRy and yRx necessarily imply that x = y.
		- example
			- Person x is related to person y if x is taller than person y. This relation is anti-symmetric because it is impossible for there to be two different people, x and y, where x is taller than y and y is taller than x.
			- ![](https://i.imgur.com/Q4bASmz.png)
- transitive
	- R is transitive if and only if for **every** three elements, x, y, z ∈ A, if xRy and yRz, then it must also be the case that xRz
		- dont have to be distinct elements
	- example
		- Person x is related to person y if x is taller than person y. This relation is transitive because if x is taller than y and y is taller than z, then it must also be the case that x is taller than z.
		- ![](https://i.imgur.com/SxdeVcO.png)
		- ![](https://i.imgur.com/gf2ACoS.png
- ![](https://i.imgur.com/fKGQ6RP.png)

## Composition
- S ο R
	- composition of relations R and S on set A is another relation on A
		- The pair (a, c) ∈ S ο R if and only if there is a b ∈ A such that (a, b) ∈ R and (b, c) ∈ S.
		- ![](https://i.imgur.com/NuXNwse.png)
		- S o R -> first one = R