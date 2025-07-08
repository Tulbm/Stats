---
{"dg-publish":true,"permalink":"/academics/cis/discrete-structures/graph-theory/graph-properties/","created":"2024-03-26T16:09:19.812-04:00","updated":"2025-07-08T10:47:55.362-04:00"}
---

Let $G=(V,E)$ be a graph 
# Handshake Lemma (HL)
- $G=(V,E)$
- $|S|=\sum_{v \in V}deg(v)=2\cdot |E|$
	- sum of the degrees of all vertices is twice the number of edges
### Handshake Lemma Corollary
- $G=(V,E)$
- $G$ has an even number of vertices of odd degree
# Pairwise Disjoint
- a set of graphs $A_{1}, A_{2},\dots,A_{k}$ is called **pairwise disjoint** if
	- for any pair of graphs $A_{i}, A_{j}$, $j,i\in[1,k],j\neq i$ $\to A_{i}\cap A_{j}=\varnothing$
- i.e. none of these graphs share any elements ()
# Completeness
- complete graph
	- $Kv=(V,E)$ where $E$ contains all two element subsets of $V$
	- no way to introduce a new edge
	- $|E|=\frac{z(z-1)}{2}={z\choose_{2}}$
# Degree sequence
- degree sequence
	- multiset of degrees of the vertices of G
	- typically represented as a sequence of |V| integers sorted into weakly decreasing order
# Reachability
- For vertices $v, u\in V$ we say that $u$ is **reachable** from $v$ if there exists a walk from $u$ to $v.$
- Reachability is an equivalence relation (reflexive, symmetric, transitive)
- $C(G)$ = number of **connected components**
	- disjoint non-empty sets of vertices such that in each component all vertices are reachable from each other 
	- If $C(G)=1$ we say $G$ is connected
# Neighbours
two vertices $v,w$ are **adjacent/neighbours** 
- if $\{v,w\}\in E$ is an edge in $G$
- $vw\to$ notation for $\{v,w\}$
# Neighbourhood
- neighbourhood of a vertex $v\in V$ is the set $N(v)=\{w\in V:vw\in E\}$
# Incident
 a vertex $v\in V$ is **incident** with some edge $e \in E$ if $v\in e$
  1. **ends**
	- the two ends of some edge $e\in E$ if $v \in e$
  5. **degree**
	- the number of edges **incident** with it
	- $deg(v)=|\{e\in E:v\in e\}|=|N(v)|$ 
  6. **regular** 
	- $G$ is regular if all of its vertices have the same degree
	- we call a regular graph with all vertices of degree d: d-regular

