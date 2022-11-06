---
title: "Counting Sort"
date: 2022-10-27
wikipedia: "https://en.wikipedia.org/wiki/Counting_sort"
tags:
- Algorithm
- Sorting
---

# Overview

**Counting Sort** is a sorting algorithm that uses keys of small positive integers.

# Analysis

Given the following:
* $n$ is the total number of elements
* $k$ is the range of elements (largest element - smallest elements)

Complexity:
* **Time**: $O(n + k)$
* **Space**: $O(k)$

Good to know:
* Worst case is when data is skewed and range is large.
* Best case is when all elements are the same.
* Average case is when $n$ and $k$ are equally dominant.

Counting sort is *typically* [[CS404 - Algorithms/Ideas/Stable (Sorting)|stable]]. The in-place variant of counting sort, however, is not.