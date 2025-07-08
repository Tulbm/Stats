---
{"dg-publish":true,"permalink":"/academics/cis/discrete-structures/bipartite-graphs/","created":"2024-03-28T16:52:36.805-04:00","updated":"2025-07-08T10:47:55.282-04:00"}
---

$\operatorname{Let}G=(V,E)$ be a graph. A bipartition of $G$ is an ordered pair $(A,B)$ of subsets of $V$ with the properties:
- $A\cup B= V$ and $A\cap B= \emptyset$ 
- For every $e\in E, e\cap A\neq\emptyset$ and $e\cap B\neq\emptyset$
- i.e. splitting the graph in a way where all edge connections are severed
- if $G$ is bipartite then every [[Academics/CIS/Discrete Structures/Subgraphs\|subgraph]] of $G$ is bipartite
Between graphs  
- if $G \simeq H,$ then $G$ is bipartite $\iff H$ is bipartite
With Cycles
-  $C_{n}$ is [[Academics/CIS/Discrete Structures/Bipartite Graphs\|bipartite]] $\iff$ n is even, for $n\geq 3$
- if $G$ contains an odd [[Academics/CIS/Discrete Structures/Graph Theory/Graph Walks#Cycles\|cycle]], then $G$ is not bipartite