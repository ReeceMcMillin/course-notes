---
title: "Quiz 2"
date: 2022-10-26
---

<details>
<summary>What is the complexity of linear search?</summary>

> The recurrence relation of linear search is $T(n) = T(n - 1) + 1$. This is basically just iteration - at each step, you have a comparison in $\Theta{1}$.
$$T(n) \in \Theta{n}$$

</details>

<hr>

<details> <summary>(T/F): Any polynomial in $n$ of degree $k$ is $\Theta(n^2)$.</summary>

> False, it's actually in $\Theta(n^k)$.
> 
> A good way to think about this problem is envisioning a polynomial like $$3n^5 + n^4 + \dots + 1$$
> This is obviously in $\Theta(n^5)$, not $\Theta(n^2)$
</details>

<hr>

<details>
<summary>(T/F): $\lg{(n!)} \in \Theta{(n \lg{n})}$</summary>

> True

</details>

<hr>

<details>
<summary>(T/F): $\lg{(n!)} \in \Omega{(n \lg{n})}$</summary>

> True

</details>

<hr>

<details><summary>What is the recurrence relation and run time of binary search?</summary>

> This is relatively easy to memorize, but you can use the [[CS404 - Algorithms/Divide and Conquer/Master Theorem]] to verify if you like.
> 
> $$T(n) = T\left(\frac{n}{2}\right) + 1 \in O(\lg{n})$$

</details>

<hr>

<details>
<summary>(T/F): $1 + 2 + 3 + \dots + n \in O(n^2)$</summary>

> True

</details>

<hr>

<details>
<summary>$1^k + 2^k + 3^k + \dots + n^k \in O(n^{k + 1})$</summary>

> True

</details>

<hr>

<details>
<summary>What's the complexity of the MaxMin algorithm?</summary>

> $O(n)$

</details>

<hr>

<details>
<summary>What's the recurrence relation that describes the MaxMin algorithm?</summary>

> $$T(n) = 2T\left(\frac{n}{2}\right)$$

</details>

<hr>

<details>
<summary>What's the big-oh complexity of $1 + \frac{1}{2} + \frac{1}{3} + \dots + \frac{1}{n}$?</summary>

> I'm not sure this is a totally rigorous explanation, but I estimated it like this:
> 
> $$\sum_{i=1}^n{\frac{1}{i}} \approx \int_1^n{\frac{1}{x}} \mathrm{dx} = \lg{n} + c$$
> 
> which would give $O(\lg{n})$.

</details>

<hr>

<details><summary>List the big-oh complexity of $\sum_{i=1}^{n}{\lg{i}}$.</summary>

> $O(n \lg n)$

</details>

<hr>

<details>
<summary>List the big-oh complexity of $\sum_{i=1}^{n}{i}$</summary>


> This is just the Euler sum.
> $$\frac{n(n+1)}{2} \in O(n^2)$$
</details>

<hr>

<details>
<summary>What's the recurrence relation of insertion sort?</summary>

> $$T(n) = T(n - 1) + n$$

</details>

<hr>

<details>
<summary>List the big-oh complexity of $T(n) = 2T(n-1)$, where $T(0) = 1$.</summary>

> $$T(n) = T(n - 1) + n \in O(2^n)$$

</details>

<hr>

<details>
<summary>List the big-oh complexity of the following: $\sum_{i=1}^{n}{\frac{1}{2^i}}$</summary>

> The sum works out to $$2-\frac{1}{2^n} \in O(1)$$

</details>