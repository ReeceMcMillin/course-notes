---
title: "Fuzzy Logic"
date: 2022-10-25
parent: [[CS461 - Artificial Intelligence/Uncertainty/Uncertainty]]
---

# Fuzzy Sets
Crisp set: $\\{0, 1\\}$
Fuzzy set: $\\{0, \dots, 1\\}$

* With a crisp set, we choose a strict cutoff value and make no accomodations.
* Fuzzy sets can have *degrees* of membership.
* $\\{< 5'6, \dots, 6'3 >\\}$ with a ramp function in between

## Fuzzy Set Membership
* $X \cup Y = max(X, Y)$
* $X \cap Y = min(X, Y)$
	* Say someone has membership in...
		* $tall$ of 0.85
		* $rich$ of 0.20
	* What's their membership in the set $tall \cup rich$?
		* $max(tall, rich) = 0.85$
	* What about $tall \cap rich$?
		* $min(tall, rich) = 0.20$
* $\overline{X} = 1 - X$
* What about the symmetric difference?
	* Usually take the definition from crisp sets, $(A \cap \overline{B}) \cup (\overline{A} \cap B)$
	* $A \text{ (tall)} = 0.85, \overline{A} = 0.15$
	* $B \text{ (rich)} = 0.2, \overline{B} = 0.8$
	* $A \oplus B = (0.85 \cap 0.8) \cup (0.15 \cap 0.2) = 0.8 \cup 0.15 = 0.8$

## Law of the Excluded Middle
Always true in crisp sets, but for fuzzy sets it's a *membership function*
* $P \cap \neg{P} = min(P, 1 - P)$

# Fuzzy Inference
* Fuzzy [[CS461 - Artificial Intelligence/6 - Knowledge Representation/Production Systems]] look pretty much like the normal kind, except...
	* the variables are fuzzy
	* the $\text{AND}/\text{OR}$ operations are fuzzy
* So instead of rules firing directly, they fire *to some extent*