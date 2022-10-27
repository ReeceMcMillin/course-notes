---
title: "Insertion Sort"
date: 2022-10-27
wikipedia: https://en.wikipedia.org/wiki/Insertion_sort
tags:
- Algorithm
- Sorting
---

# Explanation

The general strategy is to maintain an unsorted and a sorted section of the input array. At each stage, select the last element from the *unsorted* portion and place it into the correct position in the *sorted* portion.

# Pseudocode

```
for i = 1 to n
	key = A[i]
	j = i - 1

	while j >= 0 and A[j] > key:
		A[j + 1] = A[j]
		j = j - 1
	end while
	A[j + 1] = key
end for
```

# Analysis

**Worst Case**
$$
\begin{align*}
T(2) &= 1\\
T(n) &= T(n - 1) + (n - 1)\\
T(n) &\in O(n^2)
\end{align*}
$$

**Best Case**
$$
\begin{align*}
T(2) &= 1\\
T(n) &= T(n - 1) + 1\\
T(n) &\in O(n)
\end{align*}
$$