---
title: "Dijkstra's Shortest Path"
date: 2022-12-01
wikipedia: ""
parent: ""
tags:
- algorithm
- graph
- greedy
---

# Idea

Use the [[CS404 - Algorithms/Ideas/Greedy]] method to generated a shortest path between any two vertices of a graph.

This is very similar to [[CS404 - Algorithms/Algorithms/MST - Prim|Prim's Algorithm]] to find a minimum spanning tree.

![[images/Dijkstra Graph.svg]]

* **Relaxation**
	* $\textbf{if } D[u] + w((u, z)) < D[z] \textbf{ then}$
		* $D[z] \gets D[u] + w((u, z))$

1. Set distance to the source vertex as 0 and all other distances to $\infty$
2. Relax all other vertices adjacent to the current vertex
3. Choose the closest vertex as the next *current* vertex
4. Repeat steps 2 and 3 until the queue is empty or you reach the destination.

# Example

![[images/Dijkstra Example.svg]]
Find the shortest path from $A$ to $F$.

|     |   A   |     B      |     C      |     D      |     E      |     F      |
|:---:|:-----:|:----------:|:----------:|:----------:|:----------:|:----------:|
|INITIAL| $0_A$ | $\infty_A$ | $\infty_A$ | $\infty_A$ | $\infty_A$ | $\infty_A$ |
|  A  |       |   $2_A$    |   $4_A$    | $\infty_A$ | $\infty_A$ | $\infty_A$ |
|  B  |       |            |   $3_B$    |   $6_B$    |   $4_B$    | $\infty_A$ |
|  C  |       |            |            |   $6_B$    |   $4_B$    | $\infty_A$ |
|  E  |       |            |            |            |   $6_B$    |   $6_E$    |
|  D  |       |            |            |            |            |   $6_E$    |
|  F  |       |            |            |            |            |            |

# Complexity

* Worst case: $O(n^2)$
* Can be improved to $O(E \cdot \log{V})$ by using heap sort.