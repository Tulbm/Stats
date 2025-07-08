---
{"dg-publish":true,"dg-path":"CIS/Discrete Structures/Subgraphs.md","permalink":"/cis/discrete-structures/subgraphs/","created":"2024-03-28T16:31:01.812-04:00","updated":"2025-07-08T10:47:55.471-04:00"}
---

- Let $G= ( V, E)$ be a graph.
	- A subgraph of $G$ is a pair $H=(W,F)$, such that $W\subseteq V, F\subseteq E,$ and $H$ is a graph.
	- A subgraph $H$ is **proper** if $H\neq(\emptyset,\emptyset)$ and $H\neq(V,E).$
		- not empty or not the same
	- A subgraph $H=(W,F)$ is **spanning** if $W= V$, $i.e$ H contains all the vertices of $G$
	- A subgraph $H=(W,F)$ is **induced** if $F=\{e\in E:e\subseteq W\}$, i.e
		- $H$ contains all the edges of $G$ that have both ends in $W$. Sometimes we say this is the subgraph of $G$ induced by $W\subseteq V,$ and denote this $G[ W]$
		- $W=$ set of the edges we want in the induced subgraph, only the edges that make sense will be carried over
- Let $f: G\to H$ be an [[Academics/CIS/Discrete Structures/Graph Theory/Isomorphism\|isomorphism]] between $G$ and $H,$ then
	1. For all $v\in V( G) ,$ if $f( v) = w$ then the subgraph of $G$ induced by the neighbors of $v$ is isomorphic to the subgraph of $H$ induced by the neighbors of $w,$ i.e.  $G[N_{G}(v)]\simeq H[N_{H}(w)].$
	2. For any $d\in\mathbb{N}$, the subgraph of $G$ induced by vertices of degree $d$ of $v$ is isomorphic to the subgraph of $H$ induced by vertices of degree $d.$
