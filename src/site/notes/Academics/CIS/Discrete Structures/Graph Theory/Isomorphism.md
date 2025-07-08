---
{"dg-publish":true,"permalink":"/academics/cis/discrete-structures/graph-theory/isomorphism/","created":"2024-03-28T15:13:16.961-04:00","updated":"2025-07-08T10:47:55.378-04:00"}
---

### Definition
- an **isomorphism** from a graph G to a graph H is a bijective function $f:V(G)\to V(H)$ from the vertices of G to the vertices of H:
	- $\{f(v),f(w)\in E(H)\ \text{if and only if}\ \{v,w\}\in E(G)$
	- a function that will map a vertex of a graph to the equivalent one from the other graph
- G is isomorphic to H if there is an isomorphism from/between G and H
	- $G \simeq H$
### Equivalence Relations
- For any graph $G,G\simeq G.$ 
- if $G\simeq H$ then $H\simeq G$
	- For any graphs $G$ and $H$, if there is an isomorphism $f:G\to H$ such that $G\simeq H$ then there exists $f^{-1}:H\to G$ such that $H\simeq G.$
- if $G\simeq H$ and $H\simeq J$ then $G\simeq J.$
	- For any graphs $G, H, \text{ and }I$ if there are isomorphisms $f: G\to H$ and $k: H\to J$ $\text{then } k\circ f:G\to J$ is an isomorphism.
### Degrees
- with $f:G\to H$ being an isomorphism between G and H
	1. $\forall v\in V(G), \text{deg}_{H}(f(v))=\text{deg}_{G}(v)$
	2. Graphs G and H have the same degree sequence
	3. $\forall v\in V(G), \text{ if } f(v)=w$ then the degree sequence of $N_{G}(v)$ is equal to the degree sequence of $N_{H}(w)$
### Finding an Isomorphism
1. denote the vertices of each graph separately
2. $F:G\to H$
	- each vertex from a graph mapped to a specific one from the other graph
3. look at the neighborhood of the vertex in G to have and idea of how the neighborhood of H should look like
	- $G_{1}$ could map to $H_{1}$ or $H_{2}$ , just hold the information like a sudoku
4. list all the edges of a graph and their respective mapping
