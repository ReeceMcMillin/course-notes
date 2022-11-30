---
title: "Dynamic Programming"
date: 2022-11-27
wikipedia: "https://en.wikipedia.org/wiki/Dynamic_programming"
tags:
- idea
- algorithms
---

# Characteristics

1. **Simple Subproblems**: there should be a way to break the global problem into simple subproblems, each having a similar structure to the original.
2. **Subproblem Optimality**: an optimal solution to the global problem ==must== be a composition of optimal subproblem solutions.
3. **Subproblem Overlap**: optimal solutions to unrelated subproblems can share common subproblems. This is actually a benefit because we can *cache* those solutions in case we need them again.

**Memoization** is an optimization that allows us to avoid repeated recursive calls by storing intermediate values.

