This section introduce the symmetric group. We'll see that every group is a subgroup of symmetric group in the future. Therefore, study the structure of symmetric group is quite important.

----------

{% admonition gray %}
![](image-20191208215840660.png)
{% endadmonition %}-

**Permutation** of a countable set means you change the order of the set. First you have to give the set an order, then you change the order of it. For $X=\{a,b,c\}$ one might define the order $1:a, 2:b,3:c$. And then, to permute it, say $1:b,2:c,3:a$. For a fixed original order, every permuted can be represent by an bijection $X\to X$. In our example, we have bijection $f:a\mapsto b,b\mapsto c,c\mapsto a$. For uncoutable sets, for example $Y$, there's no order, but we still say that a bijection $Y\to Y$ is a permutation.

Let $\alpha$ be a permutation on $S$. For any $i\in S$, we say $\alpha$ moves $i$ if $\alpha(i)\neq i$. Otherwise, we say $\alpha$ fixes $i$.

{% admonition gray %}
![](image-20191208221715409.png)
{% endadmonition %}

Define some specific group before giving the definition of group? The author may want to introduce some concrete thing before introduce the abstrate concept.

For bijections (or permuitations) in symmetric group, we simplify the notion of $\beta\circ \alpha$ to $\beta\alpha$.

We define some basic permutations. The following definition are defined on $S_n$ which is a finite symmetric group.

{% admonition gray %}
![](image-20191209134759762.png)
{% endadmonition %}

And a special name for $2$-cycle:

{% admonition gray %}
**Definition** $2$-cycles are also called **transposition**s.
{% endadmonition %}

{% admonition gray %}
![](image-20191209135445699.png)
{% endadmonition %}

We have the fact:

{% admonition gray %}
![](image-20191209135532893.png)
{% endadmonition %}

**Proof Sketch**: Proof for such $\alpha$ and $\beta$ it holds that $\alpha\beta=\beta\alpha$ by showing that for every $i\in S_n$, $\alpha\beta(i)=\beta\alpha(i)$.

{% admonition gray %}
![](image-20191209135712485.png)
{% endadmonition %}

This fact can be seen by the algorithm given the book that factors any permutation into cycles. The algorithm just try to findout cycles in the permutation by simulate the cycle.

{% admonition gray %}
![](image-20191209140012421.png)
{% endadmonition %}

Example: $(1\; 3\;5)$ can be writen into $(1\;3\;5)(2)(4)$.

The next theorem shows the importance of complete factorization.

{% admonition gray %}
![](image-20191209140339309.png)
{% endadmonition %}

**Proof Sketch**: Prove by induction.

- Basic step: the theorem holds for $S_1$. 
- Inductive step: for some $S_n$ suppose there's another factorization $\alpha=\gamma_i\cdots\gamma_s$. Move cycles that move $i_1$ in both factorization to the last (this can be done due to the communication). That is $\gamma_t$ and $\beta_t$ moves $i_1$. Since for all $k\geq 1$, $\gamma_s^k(i_1)=\alpha^k(i_1)=\beta^k_t(i=1)$, then $\gamma_s=\beta_t$, which implies $\gamma_1\cdots \gamma_{s-1}=\alpha\gamma_s^{-1}=\alpha\beta^{-1}_t=\beta_1\cdots\beta_{s-1}$. Due to the basic step, $\gamma_1\cdots \gamma_{s-1}$ and $\beta_1\cdots\beta_{s-1}$ are exactly the same.

{% admonition gray %}
![](image-20191209142539411.png)
{% endadmonition %}

{% admonition gray %}
![](image-20191209142556996.png)
{% endadmonition %}

**Example**: $\alpha=(1\;3\;5)(2\;4\;6)(7\;8)$ and $\beta=(1\;2\;3)(4\;5\;6)(7\;8)$ have the same cycle structure. Because their complete factorizations both have two $3$-cycles and one $2$-cycles.

{% admonition gray %}
![](image-20191209143229189.png)
{% endadmonition %}

**Proof Sketch**: The $\alpha\gamma\alpha^{-1}$ transfers elements by $\alpha(i_1)\mapsto i_1\mapsto i_2\mapsto \alpha(i_2)$. One can see that it just change the elements in each cycle of the complete factorization of $\alpha$. (by changing $\gamma(i_2)$ to some $\gamma(i_2)$). Based on this idea, one can prove by compare cycle to cycle in both permutations.

{% admonition gray %}
![](image-20191209143834627.png)
{% endadmonition %}

**Proof Sketch**: $\Leftarrow$ has been proved in **Lemma 2.7**. For $\Rightarrow$, we put two permutations and their complete factorization together, with each cycle is under a cycle of the same length:
$$
\begin{aligned}
\gamma &= \gamma_1\gamma_2\cdots\gamma_k\cdots\gamma_t \\
\delta &= \delta_1\delta_2\cdots\delta_k\cdots\delta_t
\end{aligned}
$$
Let 
$$
\begin{aligned}
\gamma_k&=(i_1\;i_2\cdots i_n) \\
\delta_k&=(j_1\;j_2\cdots j_n)
\end{aligned}
$$

We can construct some $\alpha_k$ such that $j_1\overset{\alpha^{-1}_k}\to \alpha_k^{-1}(j_1)\overset{\gamma}\to \alpha^{-1}_k(j_2)\overset{\alpha_k}\to j_2$. Such $\alpha_k$ is exactly "downward" function that maps $i_l$ to $j_l$. We do this for all $i\in [t]$, and set $\alpha=\alpha_1\alpha_2\cdots\alpha_t$. Then $\delta = \alpha\gamma\alpha^{-1}$.

{% admonition gray %}
![](image-20191210212029541.png)
{% endadmonition %}

Proof Sketch: Just try to find some method to represent all cycles to product of transpositions. This can be done like
$$
(1\;2\cdots r)=(1\;r)(1\;r-1)\cdots(1\;2)
$$
A permutation $\alpha$ can always be represent by a product of odd or even numbers of transpositions. That means, for some $m,n\in\mathbb Z$, an permutation $\alpha$ cannot be represent by
$$
\begin{aligned}
\alpha &= \beta_1\beta_2\cdots\beta_{2m} \\
\alpha &= \gamma_1\gamma_2\cdots\gamma_{2n+1}
\end{aligned}
$$
where $\gamma_i$ and $\beta_j$ are all transpositions.

I would explain the proof of this fact if I found a good enough one. If you agree with the above fact, we can define:

{% admonition gray %}
![](image-20191210220450602.png)
{% endadmonition %}

{% admonition gray %}
![](image-20191210220459597.png)
{% endadmonition %}

**Theorem 2.3** guarantees the function $\text{sgn}$ is well-defined.

{% admonition gray %}
![](image-20191210220521274.png)
{% endadmonition %}

{% admonition gray %}
![](image-20191210220540718.png)
{% endadmonition %}