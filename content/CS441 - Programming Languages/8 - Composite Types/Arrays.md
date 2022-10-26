---
title: "Arrays"
date: 2022-10-25
---

## Overview
* Arrays are the most common composite type, go back to Fortran I.
* **Idea**: map a discrete index type to a component or element type.
## Slicing

## Dimensions, Bounds, Allocation
* *Static* allocation is pretty simple, just allocate some amount of space at startup which is known at compile time.
* *Dynamic* allocation is a little more tough
	* **Dope Vector**
		* ![[CS441 - Programming Languages/8 - Composite Types/Drawing 2022-10-21 11.35.46.excalidraw.png]]
		* [Dope Vector - Wikipedia](https://en.wikipedia.org/wiki/Dope_vector)

## Heap Allocation
* Arrays that can change size or shape at arbitrary times are said to be *fully dynamic*
* If number of dimensions is statically known, the dope vector can be stored on the *stack*.
* Unless garbage collection is in place, heap memoyr must be reclaimed when space is no longer used.
	* Failing to do so causes a *memory leak*.

## Memory Layout
* 1-Dimensional: elements are layed out contiguously
	* May result in small holes so elements align on word boundaries
* 2-dimensional: can either use *row-major* or *column-major* order.
	* **Row-Major**: Elements of first *row* are laid out contiguously, followed by second row, third, etc.
	* **Column-Major**: Elements of the first *column* are contiguous, followed by second column, third, etc.

### Row-Pointer Layout
* Some languages only requier rows to be contiguous, but each row can be anywhere in memory.
* An auxiliary array of pointers or references is created, one per row.

## Address Calculation
At *some* point we're going to need to translate an array reference to a specific address. #study
