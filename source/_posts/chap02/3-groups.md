{% admonition gray %}
![](image-20191217233424303.png)
{% endadmonition %}

Remember that a binary operation is just a function defines on two groups $A, B$, where $A$ is a cartesian products of two $B$'s. Note since $\ast$ is a function $G\times G\to G$,  $\ast(g_1,g_2)$ and $\ast(g_2,g_1)$ might be distinct.

We wright $a\ast b$ instead of $\ast(a,b)$ for simplicity.

{% admonition gray %}
![](image-20191217233822564.png)
{% endadmonition %}

We are study the structure of a group. And the structure is given by an binary operator, this is the group. We give some examples for non-groups, the reader can give some examples of groups by fix the non-group examples.

1. $\mathbb Z_8=\{0,1,2,\mod,7\}$ with the operation $\ast:(a,b)\to a\cdot b\mod 8$ is a non-group, because $4$ has no invert.
2. $\mathbb Z$ with operator minus is a non-group, because only element $e\in\mathbb Z$ that makes $x-e=x$ for all $x\in\mathbb Z$ is $0$. But for every $x\neq 0$, $0-x=-x$, so there's no identity in $\mathbb Z$.
3. $\mathbb Z$ with operator multiplication is a non-group, since no elements excepts $\pm 1$ has an inverse.

{% admonition gray %}
![](image-20191219190038243.png)
{% endadmonition %}

Abelian groups are ubiqutious, examples:

- $\mathbb Z$ with operator $+$
- $\mathbb Q$ with operator $\times$
- $\mathbb Z^{n\times m}$ with operator $+$

A group has the following property:

{% admonition gray %}
![](image-20191219190336818.png)
{% endadmonition %}

All these properties are not difficult to be proved.

Associatative law allows us to wright the multiplication of $n$ same elements in a group with exponent.

{% admonition gray %}
![](image-20191219192442594.png)
{% endadmonition %}

We do this only if we denote the operator of the group by multiplication notion. If we use "$+$" as the operator, we right like
$$
\underbrace{a+a+\cdots+a}_{n}=n\cdot a=na
$$
Since the associative law always holds, its easy to show:

{% admonition gray %}
![](image-20191219193040927.png)
{% endadmonition %}

Though this theorem seems intuitively, one has to prove it. The prove can be done by induction:

1. Basic step: The theorem holds when $n=3$

2. Inductive step: If the theorem holds for $n$, then for any $i\in \{1,\cdots n\}$, we have
   $$
   (a_1\cdots a_{i-1})(a_i\cdots a_{n+1})=(a_1\cdots a_i)(a_{i+1}\cdots a_{n+1})
   $$

{% admonition gray %}
![](image-20191219193446521.png)
{% endadmonition %}

Prove sketch: Prove by properties.

{% admonition gray %}
![](image-20191219193516384.png)
{% endadmonition %}

Prove Sketch: Can be induced by **Theorem 2.20**.

