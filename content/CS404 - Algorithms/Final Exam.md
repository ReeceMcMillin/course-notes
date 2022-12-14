---
title: "Final Exam"
date: 2022-12-14
---

# Misc From Quizzes

* Analyzing algorithms refers to the time and space required to execute algorithms.
* An algorithm is a step-by-step method of solving some problems.
* Pseudocode is so named because it resembles the actual code of computer languages such as C++ and Java.
* Any polynomial in $n$ of degree $k$ is $p(n) \in \Theta{(n^2)}$.

# Growth Ordering

* $(\lg{n})^{5\lg{n}} < 5^n$
* $n^4 < 5^n$
* $n^4 < n^\frac{n}{4}$
* $n^\frac{n}{4} \sim (\frac{n}{4})^\frac{n}{4}$
* $n^{\lg{n}} < n^\frac{n}{4}$
* $5^n < 5^{5n}$
* $4\lg{\lg{n}} < 4\lg{n}$

# Pseudocode Examples

```c
int y = 0;
for (int j=1; j*j<=n; j++) {
	// simple statement
}
```
$$T(n) \in \Theta(\sqrt{n})$$

--- 

```pascal
for i = 1 to n:
	for j = 1 to n:
		for k = 1 to i:
			x = x + 1
```
$$T(n) \in \Theta(n^3)$$

---

```pascal
for i = 1 to n:
	for j = 1 to i:
		x = x + 1
```
$$T(n) \in \Theta{(n^2)}$$

---

```c
for (int i=0; i<n; i++) {
	for (int j=i+1; j<n; j++) {
		// simple statement
	}
}
```
$$T(n) = \frac{n(n-1)}{2} \in \Theta{(n^2)}$$


# Facts

* $\lg{(n!)} \in \Theta{(n\lg{n})}$
* $\frac{(n+1)(n+3)}{n+2} \in \Theta(n)$


# Sums

|               Sum               |                        Expanded                         |  Complexity  |
|:-------------------------------:|:-------------------------------------------------------:|:------------:|
|    $$\sum_{i=1}^n{\lg{i}}$$     |           $\lg{1} + \lg{2} + \dots + \lg{n}$            | $O(n\lg{n})$ |
| $$\sum_{i=0}^n{\frac{1}{2^i}}$$ | $1 + \frac{1}{2} + \frac{1}{4} + \dots + \frac{1}{2^n}$ |    $O(1)$    |
|  $$\sum_{i=0}^n{\frac{1}{i}}$$  |  $1 + \frac{1}{2} + \frac{1}{3} + \dots + \frac{1}{n}$  | $O(\lg{n})$  |
|       $$\sum_{i=1}^n{i}$$       |                 $1 + 2 + 3 + \dots + n$                 |   $O(n^2)$   |
| $$\sum_{i=1}^n{i^k}$$|$1^k + 2^k + 3^k + \dots + n^k$|$O(n^{k+1})$|

# Searching

|   Algorithm   | Time Complexity | Recurrence Relation |
|:-------------:|:---------------:|:----------------:|
| Linear Search |       $O(n)$          |          $T(n) = T(n-1) + 1$        |
| Binary Search |        $O(\lg{n})$         |        $T(n) = T(\frac{n}{2}) + 1$          |
| Max-Min              |    $O(n)$             | $T(n) = 2T(\frac{n}{2}) + 2$ |

# Sorting

|   Algorithm    | Time Complexity |       Recurrence Relation       |     Stable     |
|:--------------:|:---------------:|:-------------------------------:|:--------------:|
|  Bubble Sort   |    $O(n^2)$     |     $T(n) = T(n-1) + O(n)$      |       ✅       |
| Insertion Sort |    $O(n^2)$     |     $T(n) = T(n-1) + O(n)$      |       ✅       |
| Selection Sort |    $O(n^2)$     |     $T(n) = T(n-1) + O(n)$      | not by default |
|   Merge Sort   |  $O(n\lg{n})$   | $T(n) = 2T(\frac{n}{2}) + O(n)$ |       ✅       |
|   Heap Sort    |  $O(n\lg{n})$   |   $T(n) = T(n-1) + O(\lg{n})$   |       ❌       |
|   Quicksort    |  $O(n\lg{n})$   | $T(n) = 2T(\frac{n}{2}) + O(n)$ |       ❌       |
| Counting Sort  |   $O(n + k)$    |               N/A               |       ✅       |
|   Radix Sort   |     $O(nk)$     |               N/A               |       ✅       |


# Graphs

|    Algorithm    | Time Complexity | Space Complexity | Greedy |       Facts       |
|:---------------:|:---------------:|:----------------:|:------:|:-----------------:|
|   Dijkstra's    |    $O(V^2)$     |                  |   ✅   | Similar to Prim's |
|  Prim's (MST)   |  $O(E\lg{V})$   |                  |   ✅   |   Vertex-based    |
| Kruskal's (MST) |  $O(E \lg{V})$  |                  |   ✅   |    Edge-based     |
| Ford-Fulkerson (flow) |      Complicated           |                  | ✅ |                   |
