---
title: "Translation Schemes"
date: 2022-10-25
---

# General Categories
* **Oblivious**: exploits no special knowledge of the parse tree or attribute grammar.
* **Dynamic**: tails attribute evaluation order to the *structure* of a given parse tree.
	* Typically performs a topological sort of the attribute flow graph and then invokes evaluation rules in an order consistent with the sort.
* **Static**: based on analysis of the structure of the attribute grammar.

## Action Routines
* **Action routines** are semantic functions that the programmar instructs the compiler to execute at a particular point in the parse.
* 