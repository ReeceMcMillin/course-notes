---
title: "Quicksort"
date: 2022-10-25
wikipedia: https://en.wikipedia.org/wiki/Quicksort
tags:
- algorithm
- sorting
---

# Overview

* **Best Case**: $O(n \lg{n})$
* **Average Case**: $O(n \lg n)$
* **Worst Case**: $O(n^2)$

Quicksort divides an array into subarrays by selecting a pivot element using [[CS404 - Algorithms/Ideas/Divide and Conquer]].

While dividing the array, the pivot element should be positioned in such a way that elements less than the pivot are kept on the left side and elements greater than the pivot are kept on the right side.

The left and right subarrays are also divided using the same approach. This process continues until each subarray contains a single element, which is *trivially sorted*.

Finally, subarrays are recombined to form a sorted array.

# Complexity

To analyze quicksort, we need to consider the best- and worst-case *partition* behavior.

Given perfectly balanced partitions at each stage, we get the following recurrence relation:
$$T(n) = 2T\left(\frac{n}{2}\right) + \Theta(n)$$
By the [[CS404 - Algorithms/Divide and Conquer/Master Theorem]], this gives $T(n) = \Theta(n \lg{n})$.

In the worst case, partitioning could produce one subproblem of size $(n - 1)$ and another of size $0$. This would produce the following recurrence relation:
$$T(n) = T(n-1) + \Theta(n)$$
Using the [[CS404 - Algorithms/Divide and Conquer/Substitution Method|subsitution method]], we get $T(n) = \Theta(n^2)$.


# Explanation

You can think of the *pivot* as the only sorted element.
* We know that numbers to the left are less than the pivot, but they may as well be unsorted. Same for the right.

1. Choose the highest index value as pivot
2. Take two variables to point to the left/right of the list (excluding pivot)
3. Left points to the *low* index
4. Right point sto the high index
5. While value at left is less than pviot, move right
6. While value at right is greater than pivot, move left

# Notes
1. Quicksort is **in-place**
2. Quicksort is **not** [[CS404 - Algorithms/Ideas/Stable (Sorting)|stable]].[^1]

[^1]: This depends on the partitioning scheme.