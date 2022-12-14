---
title: "Midterm 2 Review"
date: 2022-10-28
parent: [[CS441 - Programming Languages/Overview]]
---


> [!NOTE] More Study Material
> 
> A lot of this is blank, but I've transcribed the textbook's Check Your Understanding questions [here](https://docs.google.com/document/d/1ZgcKM5S-UDpNt3W2zfN1GRL4OKKvxSPegRuUUzRs-uM/edit?usp=sharing). If you're looking for more study material, that's the best place to start.
> 
> It's read-only, so go ahead and make a copy to fill in yourself. I'd love to share answers, but it *really* sticks better when you write them yourself.


# Chapter 6

* **Value Model**: a variable is just a *named container* for a value
	- **l-value**: a left-hand side expression representing a *location*
	- **r-value**: a left-hand side expression representing a *value*
- **Reference Model**: a variable is a *named reference* to a value

# Chapter 7

> todo

# Chapter 8
* Describe the purpose of a [[CS441 - Programming Languages/8 - Composite Types/Dope Vector|dope vector]] and what information it typically contains.
* Know how to calculate array bounds
1. Describe the following [[CS441 - Programming Languages/8 - Composite Types/Garbage Collection|garbage collection]] strategies:
	* Tombstones
	* Locks and Keys
	* Mark and Sweep
	* Stop and Copy
	* Generational Collection
2. Describe *conservative* garbage collection
	* If it looks like a pointer, leave it alone
3. What are two problems associated with reference-counting garbage collectors?
4. Describe the difference between the *reference* and *value* models of variables when it comes to pointers and recursive types.

# Chapter 9
1. Describe the actions taking during the calling sequence.
	* Prologue
	* Epilogue
2. Draw and label the stack frame diagram.
3. Describe the four steps of a typical calling sequence.
4. What is the difference between *formal* parameters and *actual* parameters?
5. How does *inline expansion* differ from *macro expansion*?
6. Describe the difference between **pass-by-value** and **pass-by-reference**.
7. What are the benefits of pass-by-reference? What are the dangers?



# Brain Dump

In a stack frame, addressing is done relative to the **frame pointer** because the compiler can't know the exact memory address of the frame until runtime.