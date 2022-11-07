---
title: "CS404 Midterm Study"
date: 2022-10-27
parent: [[CS404 - Algorithms/Overview]]
---

1. Must know recurrence relation and time complexity of the following:
	* [[CS404 - Algorithms/Algorithms/Bubble Sort]]
	* [[CS404 - Algorithms/Algorithms/Insertion Sort]]
	* [[CS404 - Algorithms/Algorithms/Merge Sort]]
	* [[CS404 - Algorithms/Algorithms/Quicksort]]
	* [[CS404 - Algorithms/Algorithms/Counting Sort]]
2. Be able to find the big O complexity of functions using the following methods.
	* [[CS404 - Algorithms/Divide and Conquer/Recursion Tree Method]]
	* [[CS404 - Algorithms/Divide and Conquer/Substitution Method]]
	* [[CS404 - Algorithms/Divide and Conquer/Master Theorem]]
3. Memorize common sums and series along with their big O complexities.
4. Make sure you understand how to solve all problems on each quiz.
	* [[CS404 - Algorithms/Quiz Problems/Quiz 1]]
	* [[CS404 - Algorithms/Quiz Problems/Quiz 2]]

# Sunday Night Review

* Iterative substitution
	* $T(n) = 2T(n - 1)$, $T(1) = 1$
	* $T(n) = 2^2 \cdot T(n-2)$
	* $T(n) = 2^3 \cdot T(n-3)$
	* $\vdots$
	* Let $k = n-1$
	* $T(n) = 2^k \cdot T(n-(n-1)) = 2^k \cdot T(1)$

## Algorithm Analysis
* Definitions
	* Algorithm: a step-by-step method for solving some problem
		* Name
		* Input
		* Output
		* Steps (pseudocode)
	* Computational problem
	* Data structure
	* Program
	* Pseudocode
		* preferred due to its precision, structure, and universality
		* properties:
			* compact
			* easier to read/understand
			* can be used to prove correctness
	* Scalability: ability of a program to 
	* Analyzing an algorithm
		* Running time is natural measure re: scalability
		* Why coul
* Worst, average, best-case
* asymptotic growth: a measure of how fast the output $f(n)$ grows as the input $n$ grows
* memory complexity = space complexity
* Specific algorithms
	* linear search
* Geometric sums
* *lots of logarithm identities in slides*
* floor and ceiling

* Data structures - know operations and *time complexity* of each, *go over zybooks questions*
	* array
	* queue (with circular array implementation)
	* buffer
	* stack
	* linked lists
	* trees
	* 

Big O: $f(n) \leq c \cdot g(n)$
Big Omega: $f(n) \geq c \cdot g(n)$

$$1 + a + a^2 + \dots + a^n = \frac{1=a^{n+1}}{1-a}$$
$$1 + 2 + 4 + 8 + \dots + 2^{n-1} = 2^n - 1 \in O(2^n)$$
sum 1 to n of $i^2 \in O(n^3)$

1. What properties make up the description of an algorithm?
2. What benefits does pseudocode have over actual program code?
3. What are some properties of good pseudocode?
4. What are some primitive operations considered in algorithmic analysis?
5. Why do we typically prefer to consider worst-case running time?
6. Why is it difficult to measure average-case running time?
7. What does it mean for a recurrence relation to be in *closed form*?
8. Prove $20n^3 + 10n\lg{n}+ 5 = O(n^3)$.
9. Prove $n^3 + 2n + 5 = \Omega(n^3)$.
10. Prove that $4n^2 + 3n + 1 = \Theta(n^2)$.
11. For each of the following algorithms, provide the steps, recurrence relation, and complexity.
	1. Linear search
	2. Merge Sort
12. What does it mean for a binary tree to be...
13. For different sorting algorithms, know:
	* stability
	* in-place
	* recurrence relation (for both worst/best case)

# Algorithms
* maxmin
* linear search
* binary search

Just want to clarify, when you ask for pseudocode

8-9 questions, 5 pages, 


Write T(n)

```
for i = 0, i < n-1, i++
```

# Big Questions
* Definition for every algorithm
* Pseudocode
	* name
	* input
	* output
	* steps
* Time complexity
* Recurrence relation