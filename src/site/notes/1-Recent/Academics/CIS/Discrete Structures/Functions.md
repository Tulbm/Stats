---
{"dg-publish":true,"dg-path":"CIS/Discrete Structures/Functions.md","permalink":"/cis/discrete-structures/functions/","created":"2024-10-02T13:02:09.735-04:00","updated":"2025-07-08T10:47:55.423-04:00"}
---


- Discrete mathematics is often concerned with functions that map between other kinds of sets
	- such as binary strings or a set of tasks.
	- an assignment of people to teams, or of guests to hotel rooms, are also examples of functions.
- Definition
	- ![](https://i.imgur.com/5IKnxBr.png)

f = (U,V,G)
U = Domain
V = Codomain
G = Graph
# Domain
- an element from the domain cant have more than 1 image (can have 0 tho)
	- image = value from V that the function returns → f(u) = v
# Codomain
- not the range
- elements of codomain can have >1 preimages
	- preimage = element of U that when put into the function outputs the element from V
- codomain is just the list of possible values(all the employess)
	- but the function might not promote every single one of them
# Graph 
= subset of U x V
- the 2-tuple with a the element from U and its respective image
- if G = { }
	- still a function
	- the function just doesnt give any V elements with the U inputs
	- illustration
		- ![](https://i.imgur.com/P58FLOt.png)
- arrow diagram
	- ![](https://i.imgur.com/aPuKktN.png)
	- there is exactly one arrow pointing out of every element in the domain
	- if there are no arrows, it is still a function, because there are no counter-examples to the definition
- (Co)Domain of Definition
	- domain 
		- the elements of U that have an image in V(corresponding value in V)
	- codomain/range
		- the elements of V that have a preimage(corresponding value in U)
- well-defined functions
	- ![](https://i.imgur.com/bonsLhC.png)
	- range = {a,c,d}
		- not using all the elements is fine
	- purple arrow is the one making the function not well-defined
		- there can only be one possible value from each input
- equality
	- f and g are equal if f and g have the same domain and target, and f(x) = g(x) for every element x in the domain.