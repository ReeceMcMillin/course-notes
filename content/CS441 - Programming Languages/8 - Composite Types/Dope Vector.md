---
title: "Dope Vector"
date: 2022-11-10
wikipedia: "https://en.wikipedia.org/wiki/Dope_vector"
---

**Dope vectors** are used by the compiler to hold information about the sizing and memory layout of data objects (especially [[CS441 - Programming Languages/8 - Composite Types/Arrays|arrays]], or composite types which *contain* arrays).

Say we have an array of 10 elements, each 8 bytes. We need $10 \cdot 8 = 80$ bytes to store the array in memory, but the array itself doesn't have any place to hold that information. That's where the *dope vector* comes in. Putting this sort of structure in place can also 