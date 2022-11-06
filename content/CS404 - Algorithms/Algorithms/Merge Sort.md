---
title: "Merge Sort"
date: 2022-10-25
wikipedia: https://en.wikipedia.org/wiki/Merge_sort
tags:
- algorithm
- sorting
---

**Merge Sort** uses the [[CS404 - Algorithms/Ideas/Divide and Conquer|divide and conquer]] paradigm to sort arrays.

At each step, the original array is divided into two halves. This continues recursively until the size of each subarray becomes 1.

## Analysis

Given a list of $n$ items:
* It takes $\Theta(1)$ time to split the list into two lists of (approximate) size $\frac{n}{2}$.
* It takes $\Theta(n)$ time to *merge* the lists back together.
This gives us a total problem size of $T(n) = 2T(\frac{n}{2}) + \Theta(n)$.

**Worst Case**: $\Theta(n \lg{n})$

Merge sort is typically [[CS404 - Algorithms/Ideas/Stable (Sorting)|stable]].

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