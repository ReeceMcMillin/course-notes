---
title: "Pointers and Recursive Types"
date: 2022-10-25
parent: [[CS441 - Programming Languages/8 - Composite Types/Overview]]
---

Records of some type $T$ can easily contain a reference to another record of $T$.
* Reference model? No big deal, variables are *already* references
* Value model? This is when you need the idea of a *pointer*, introduced in [[CS441 - Programming Languages/Languages/PL-I]]

## Pointers & Arrays in C

```c
int n;      // integer
int *p, *q; // 2 pointers to integer
int b[20];  // integer array
```

## Stack Smashing
C's lack of bounds checking is a *major* source of program bugs and security holes.
* **Buffer overrun** attacks
* **Stack-smashing** attacks

## Dangling References
A **dangling reference** is a live pointer to an object that's no longer valid.

### Tombstones
* When an object is reclaimed, the indirection word is marked with a value invalidating future references to it.
### Locks and Keys
* Every pointer and object on the heap has a word added to it.
* These words must match for the pointers to be valid.
* This is simple to implement, but only works for objects on the heap.