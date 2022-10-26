---
title: "Bayes' Theorem"
date: 2022-10-25
---

$$P(a \mid b) = \frac{P(a \wedge b)}{P(b)}$$
This is super cool if variables are discrete, but what about continuous variables?
* *Calculus baby!*

## Joint Probability Distribution
Consider:
* $P(\text{rain} \wedge \text{high winds})$
* $P(\text{scholarship} \wedge \text{dean's list})$
* $P(\text{cavity} \wedge \text{rain})$

$$P(\neg{a}) = 1 - P(a)$$
$$P(a \vee b) = P(a) + P(b) - P(a \wedge b)$$
## Marginal Probability
Suppose we have a simple 2 * 2 * 2 distribution:
* Cavity
* Toothache
* Dental pick catches on cavity
We'll perform *marginalization*, or *summing out*, to calculate the marginal probability.

![[images/Pasted image 20221024134153.png]]

$$P(\text{cavity} \mid \text{toothache}) = P(\text{cavity, ache, catch}) \cdot \alpha$$

**THIS ISN'T DONE YET! VIEW SLIDES**

