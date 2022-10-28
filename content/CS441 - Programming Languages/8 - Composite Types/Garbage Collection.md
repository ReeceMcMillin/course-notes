---
title: "Garbage Collection"
date: 2022-10-26
parent: [[CS441 - Programming Languages/8 - Composite Types]]
---

# Reference Counting

**Idea**: keep a count of references pointing to objects in memory, deallocate the memory once that count reaches 0.[^1].

Reference counts can work well if we're using a **tombstone** system.

[^1]: This isn't so simple! Cyclic pointers break basic reference counts.

# Smart Pointers
* `unique_ptr` guarantees no other name points to the object.
* `shared_ptr` manages reference counting
* `weak_ptr` does **not** use reference counting

# Other Methods

## Tracing Collectors

### Mark and Sweep

**Idea**: start at some pointer and follow it through the heap

1. Initially mark **everything** as potentially garbage.
2. Walk through the whole reference tree.
3. At the end of the process, anything you haven't been able to reach is *still* garbage - go ahead and deallocate!

![[Excalidraw/Drawing 2022-10-26 11.23.45.excalidraw.png]]

**Problems**: requires a stack as large as the longest path through the heap #study

### Pointer Reversal

**Problems**: doesn't do anything about fragmentation

### Stop and Copy

1. Divide the heap into two areas of roughly equal size
2. Use one half for **all** allocation.
	* When this half is nearly full, perform a mark/sweep
3. Copy each *reachable* block into the other half.
	* Since we have total knowledge over what's reachable, we can accomplish allocation with no external fragmentation
	* Overhead is proportional to the number of non-garbage blocks we have.