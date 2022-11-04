---
title: "Predicate Logic"
date: 2022-10-25
wikipedia: https://en.wikipedia.org/wiki/First-order_logic
---

# Overview
Predicate logic allows us to make statements about *categories*
# Features
* Arity:
	* **Arity 0:** $win()$
	* **Arity 1:** $Student(\text{Bill})$
	* **Arity 2:** $Parent(\text{John}, \text{Martha})$
* Also allows us to use existential ($\exists$) and universal ($\forall$) quantifiers
	* *All aliens drive flying saucers*
	* $\forall{x}: \text{Alien}(x) \implies \text{DrivesSaucer}(x)$
	* How would we prove $\neg{(\forall{x}: \text{Alien}(x) \implies \text{DrivesSaucer}(x)})$?
		* Start by putting it in *clausal form*: $p \implies q \equiv \neg{p} \vee q$
		* $\neg{(\forall{x}: \neg{\text{Alien}(x)} \vee \text{DrivesSaucer}(x)})$
		* $\exists{x}: \text{Alien}(x) \wedge \neg{\text{DrivesSaucer}(x)}$
# Resolution (Unification)

> [!NOTE] NOTE
> 
> [[CS461 - Artificial Intelligence/5 - Logic/Propositional Logic]] refers to this as resolution, called *unification* in predicate logic

* **Rule 1:** predicates must match
	* $setting(sun) \wedge \neg{setting(moon)}$ ~ different variables, no relationship

# Example
* All genies ride flying carpets.
	* $\forall x: \text{Genie}(x) \implies \text{FlyingCarpet}(x)$
	* **Clausal form:** $\forall x: \neg{\text{Genie}(x)} \vee \text{FlyingCarpet}(x)$
* Aladdin rides a flying carpet.
	* $\text{FlyingCarpet}(\text{Aladdin})$
* Is Aladdin a genie?
	* Try to find a contradiction, start with $\neg{\text{Genie}(\text{Aladdin})}$
	* We don't have enough information! Need biconditional.
		* $\forall x : G(x) \iff FC(x)$
			* $\forall x : G(x) \implies FC(x)$
				* **1:** $\forall x: \neg{G(x)} \vee FC(x)$
			* $\forall x : FC(x) \implies G(x)$
				* **2:** $\forall x: \neg{FC(x)} \vee G(x)$
			* **3:** $FC(Aladdin)$
			* **4:** $\neg{G(Aladdin)}$
		* Resolution through **2** and **3** produces $G(Aladdin)$
		* Resolution through **4** and **5** produces $\emptyset$ - contradiction
