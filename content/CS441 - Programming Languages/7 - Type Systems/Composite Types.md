---
title: "Composite Types"
date: 2022-10-25
---
> [!attention]
> 
 This is covered in significantly more detail in [[CS441 - Programming Languages/8 - Composite Types/]]
## Records
Records were introduced by [[CS441 - Programming Languages/Languages/Cobol]], similar to tuple
* Cartesian product of its components

## Unions
*Variant* records (unions) differ from records
```c
union widget {
	int    n;
	double x;
	char   ch;
}

widget character = 'c';
int x = character + 1; // sure, why not
```
* Problem: compiler doesn't discriminate between members of unions

## Sets
* Powerset of its elements
* Introduced by [[CS441 - Programming Languages/Languages/Pascal]]

