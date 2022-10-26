---
title: "Merge Sort"
date: 2022-10-25
parent: [[CS404 - Algorithms/Algorithms/]]
tags:
- algorithm
- sorting
---

**Merge Sort** uses [[CS404 - Algorithms/Ideas/Divide and Conquer]] to sort arrays.

At each step, the original array is divided into two halves. This continues recursively until the size of each subarray becomes 

## Analysis

**Worst Case**: $\Theta(n \lg{n})$

## Pseudocode

```python
def MergeSort(A, p, r):
	midpoint = 
	if p < r:
		mid = floor((p + r) / 2)
	else:
		mid = 
	MergeSort(A, p, mid)
	MergeSort(A, mid + 1, r)
	MergeSort(A, p, mid, r)
```