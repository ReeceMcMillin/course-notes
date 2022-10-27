---
title: "Quiz 2"
date: 2022-10-26
---

<details>
<summary>What is the complexity of linear search?</summary>

> The recurrence relation of linear search is $T(n) = T(n - 1) + 1$.
> 
> This is basically just iteration - at each step, you just have a constant-time - $\Theta(1)$ - comparison.
> $$T(n) \in \Theta(n)$$

</details>

<hr>

<details> <summary>True or false: Any polynomial in $n$ of degree $k$ is $\Theta(n^2)$.</summary>

> False, it's actually in $\Theta(n^k)$.
> 
> A good way to think about this problem is envisioning a polynomial like the following:
> $$3n^5 + n^4 + \dots + 1$$
> This is obviously in $\Theta(n^5)$, not $\Theta(n^2)$.
> 
> For a more rigorous proof, see [[CS404 - Algorithms/Math/Proofs#Any polynomial in $n$ of degree $k$ is $ Theta(n k)$.|here]].
</details>

<hr>

<details>
<summary>True or false: $\lg{(n!)} \in \Theta{(n \lg{n})}$</summary>

> True, see [[CS404 - Algorithms/Math/Proofs#lg{(n!)} in Theta(n lg{n})|here]] for proof.

</details>

<hr>

<details>
<summary>True or false: $\lg{(n!)} \in \Omega{(n \lg{n})}$</summary>

> True by way of the above answer:
> $$\lg{(n!)} \in \Theta{(n \lg{n})}$$
> Proof [[CS404 - Algorithms/Math/Proofs#lg{(n!)} in Theta(n lg{n})|here]] if you're not convinced.

</details>

<hr>

<details><summary>What is the recurrence relation and complexity of binary search?</summary>

> This is relatively easy to memorize, but you can use the [[CS404 - Algorithms/Divide and Conquer/Master Theorem]] to verify if you like.
> 
> $$\begin{align*}
T(n) &= T\left(\frac{n}{2}\right) + 1\\
T(n) &\in O(\lg{n})
\end{align*}$$

</details>

<hr>

<details>
<summary>True or false: $1 + 2 + 3 + \dots + n \in O(n^2)$</summary>

> True.
> 
> $$1 + 2 + 3 + \dots + n = \frac{n(n+1)}{2} \in \Theta(n^2)$$
> 
> Since the sum is in $\Theta(n^2)$, it's also in $O(n^2)$.

</details>

<hr>

<details>
<summary>$1^k + 2^k + 3^k + \dots + n^k \in O(n^{k + 1})$</summary>

> True, see [[CS404 - Algorithms/Math/Proofs#$1 k + 2 k + 3 k + dots + n k in O(n {k + 1})$|here]] for proof.

</details>

<hr>

<details>
<summary>What's the complexity of the MaxMin algorithm?</summary>

> This is described better in the textbook, but the idea behind the algorithm is to iterate through an array *once*, making two comparisons against the current max/min at each stage for a total of $2n-2$ comparisons in the basic version.
> 
> $$T(n) \in O(n)$$

</details>

<hr>

<details>
<summary>What's the recurrence relation that describes the MaxMin algorithm?</summary>

> $$T(n) = 2T\left(\frac{n}{2}\right) + 2$$
> 
> I don't remember covering a recursive version of this algorithm, but the shape of the above relation is pretty much in line with the "linear + 2 comparisons" idea above.

</details>

<hr>

<details>
<summary>What's the big O complexity of $1 + \frac{1}{2} + \frac{1}{3} + \dots + \frac{1}{n}$?</summary>

> I'm not sure this is a totally rigorous explanation, but I estimated it like this:
> 
> $$\sum_{i=1}^n{\frac{1}{i}} \approx \int_1^n{\frac{1}{x}} \mathrm{dx} = \lg{n} + c$$
> 
> which would give $O(\lg{n})$.
> 
> More rigorously, this is a partial sum of the [Harmonic series](https://en.wikipedia.org/wiki/Harmonic_series_(mathematics)). We can describe the $n^{th}$ Harmonic number (the partial sum of the series at some $n$) like this:
> $$H_n = \ln{n} + \gamma + \frac{1}{2n} - \epsilon_n$$
> * $\gamma$ (gamma) is a constant.
> * $\frac{1}{2n}$ grows to 0.
> * $0 \leq \epsilon_n \leq \frac{1}{8n^2}$, which also grows to 0.
> 
> That means $\ln{n}$ defines the growth rate. Changing the base back to 2 and picking $n_0$ and $c$ to prove this is $O(\lg{n})$ and $\Omega(\lg{n})$ (and therefore also $\Theta(\lg{n})$) should be straightforward.

</details>

<hr>

<details><summary>List the big O complexity of $\sum_{i=1}^{n}{(\lg{i})}$.</summary>

> $O(n \lg n)$
> 
> I haven't taken the time to write out either proof yet, but I think this is just the $\lg{(n!)}$ problem in disguise.

</details>

<hr>

<details>
<summary>List the big O complexity of $\sum_{i=1}^{n}{(i)}$.</summary>


> This is just the Euler sum.
> $$\frac{n(n+1)}{2} \in O(n^2)$$
</details>

<hr>

<details>
<summary>What's the recurrence relation of [[CS404 - Algorithms/Algorithms/Insertion Sort]]?</summary>

> $$T(n) = T(n - 1) + n$$
> 
> This is *slightly* different in the notes, given as $T(n) = T(n - 1) + (n - 1)$. That's not meaningful for the overall complexity of $O(n^2)$.

</details>

<hr>

<details>
<summary>List the big O complexity of $T(n) = 2T(n-1)$, where $T(0) = 1$.</summary>

> I envisioned this as a binary tree where $T(0)$ was the root. That'd give $T(n)$ describe the total number of nodes present *up to and including* level $n$. Since a binary tree of height $h$ can have a maximum of $2^h - 1$ nodes, this would fall on the order of $O(2^n)$.
>
> $$T(n) \in O(2^n)$$

</details>

<hr>

<details>
<summary>List the big O complexity of the following: $\sum_{i=1}^{n}{\left[\left(\frac{1}{2}\right)^i\right]}$</summary>

> There are a few different ways to approach this. The one I like best is multiplying the whole series by 2 and rearranging things.
> $$
	\begin{align*}
			s_n &= \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \dots + \frac{1}{2^n}\\\\
			2s_n &= \frac{2}{2} + \frac{2}{4} + \frac{2}{8} + \dots + \frac{2}{2^n}\\\\
			&= 1 + \left[ \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \dots + \frac{1}{2^{n-1}}\right]\\\\
	\end{align*}
	$$
> Notice how that last term is just $s_n$ minus the last term, so...
> $$
	\begin{align*}
		2s_n &= 1 + \left[ s_n - \frac{1}{2^n} \right]\\\\
		s_n &= 1 - \frac{1}{2^n}
	\end{align*}
	$$
> As $n$ goes to infinity, $\frac{1}{2^n} \sim 0$, so our overall complexity trends towards 1 as $n$ gets larger. Since that's a constant, the overall complexity is $\Theta(1)$!
</details>