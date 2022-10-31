---
title: "Bayes' Theorem"
date: 2022-10-25
wikipedia: "https://en.wikipedia.org/wiki/Bayes%27_theorem"
parent: [[CS461 - Artificial Intelligence/Uncertainty/Uncertainty]]
---



$$\begin{align*}
P(A \mid B) &= \frac{P(A \cap B)}{P(B)}, \text{ if } P(B) \neq 0\\
&= \frac{P(B \mid A)\cdot P(A)}{P(B)}, \text{ if } P(B) \neq 0
\end{align*}$$
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
Suppose we have a simple $2 \times 2 \times 2$ distribution:
* Cavity
* Toothache
* Dental pick catches on cavity
We'll perform *marginalization*, or *summing out*, to calculate the marginal probability.

![[images/Pasted image 20221024134153.png]]

$$P(\text{cavity} \mid \text{toothache}) = P(\text{cavity, ache, catch}) \cdot \alpha$$

**THIS ISN'T DONE YET! VIEW SLIDES**

