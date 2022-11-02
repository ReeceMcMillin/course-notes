---
title: "Heap"
date: 2022-11-01
wikipedia: "https://en.wikipedia.org/wiki/Heap_(data_structure)"
tags:
- "data structure"
---

# Overview

A **heap** is an almost-complete tree that satisfies one of the following heap properties.

## Max Heap
For any given node $C$, if $P$ is a parent of $C$, then the key (the value) of $P$ is **greater than or equal to** the key of $C$.

## Min Heap
For any given node $C$, if $P$ is a parent of $C$, then the key (the value) of $P$ is **less than or equal to** the key of $C$.

# Operations
* `create`
	* $n$ operations
* `heapify`
	* create a heap (restore the heap property) out of a given array.
	* modify the complete [[CS404 - Algorithms/Data Structures/Binary Tree]] to become a heap
	* `sift-up`
		* move a node up in the tree (typically after an insert) until it's at the proper level.
	* `sift-down`
		* move a node *down* in the heap (typically after a delete/replace) until it's at the proper level.

# Types
## Binary Heap

A complete [[CS404 - Algorithms/Data Structures/Binary Tree]] has an interesting property that we can use to find the children and parents of any node.

If the index of any element in the array is $i$, the element at index $2i+1$ is the *left* child and the element at $2i+2$ is the right child.