---
title: "Type Equivalence"
date: 2022-10-25
---

How do we determine if two things are the same type?
1. **Structural Equivalence**: two types have the same components put together the same way.
2. **Name Equivalence**: types defined by different names are probably meant to be incompatible.

## Name Equivalence

> [!question]
> 
> ```c
> typedef old_type new_type;
> ```
> 
Are `old_type` and `new_type` distinct?


A language in which alias types are considered..
* distinct? ***strict* name equivalence**
* the same? ***loose* name equivalence**

