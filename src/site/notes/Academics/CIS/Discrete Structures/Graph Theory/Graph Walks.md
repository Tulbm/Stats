---
{"dg-publish":true,"dg-path":"CIS/Discrete Structures/Graph Theory/Graph Walks.md","permalink":"/cis/discrete-structures/graph-theory/graph-walks/","created":"2024-03-31T11:55:05.318-04:00","updated":"2025-07-08T10:47:55.336-04:00"}
---

Let $G= ( V, E)$ be a graph.
# Walks
- A **walk** in $G$ is a sequence of vertices $\{v_1,v_2,v_3,...,v_n\}$ in $V(G)$, such that each consecutive pair of vertices in the walk $\{v_i,v_{i+1}\}$ , form an edge in $E(G).$ 
	- The **length** of a walk is the number of steps, i.e. the number of **edges** in the walk.
	- no restrictions, can have $\infty$ length
	- Edge and Vertices both can be repeated.
# Path
- A **path** in $G$ is a walk where no vertices are repeated
	- edges can be repeated 
# Trails
- A **trail** is a walk where no edges are repeated
	- vertices can be repeated
# Cycles
- A **cycle** in $G$ is a walk with $\mathrm{length\geq 3,}$ where the first and last vertex are the same, but no other vertices are the same.
	- loop
	- $C_{n}$ is [[Academics/CIS/Discrete Structures/Bipartite Graphs\|bipartite]] $\iff$ n is even, for $n\geq 3$
	- if $G$ contains an odd cycle, then $G$ is not bipartite
# Concatenation
- Two walks can be concatenated by concatenating their respective sequences.
- If walks $W=\{v_1,v_2,v_3,...,v_n\},K=\{u_1,u_2,u_3,...,u_m\}$ their concatenation $WK=\{v_1,v_2,v_3,...,v_n,u_1,u_2,u_3,...,u_m\}$. 
	- Note that order of concatenation matters, it is not a commutative operation
- might not be a path if there are repeated vertices

