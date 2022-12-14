---
title: "Bubble Sort"
date: 2022-10-27
wikipedia: https://en.wikipedia.org/wiki/Bubble_sort
tags:
- algorithm
- sorting
---

**Bubble Sort** (also known as *sinking sort*) works by repeatedly swapping adjacent elements until the full list is sorted.

# Analysis

**Recurrence Relation**: $T(n) = T(n - 1) + (n - 1)$

| | Worst Case | Average Case | Best Case | 
|-|-|-|-| 
| Comparisons | $O(n^2)$ | $O(n^2)$ | $O(n)$ |
| Swaps | $O(n^2)$ | $O(n^2)$ | $O(1)$ |
| Space | $O(n)$ | | |

Bubble sort is typically [[CS404 - Algorithms/Ideas/Stable (Sorting)|stable]].