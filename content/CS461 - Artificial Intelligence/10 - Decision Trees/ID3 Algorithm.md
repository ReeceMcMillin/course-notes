---
title: "ID3 Algorithm"
date: 2022-11-09
wikipedia: ""
---

Introduced in [[CS461 - Artificial Intelligence/Lectures/2022-11-09]]'s lecture.

Find the variable that comes *closest* to dividing the data into two equal subsets.

Partition set $S$ on attribute $A$.

$$Gain(S, A) = Entropy(S) - \Sigma{\frac{\left|S_v\right|}{\left|S\right|}} \cdot Entropy(S_v)$$