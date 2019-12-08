# Set

There's no definition for sets in mathematics, we simply say a set is a collection of some elements.

Some easy symbols you have to understand before study this section:

- $x\in X$, for $X$ being a set
- $X=Y$, for $X$ and $Y$ being sets
- $R\subseteq X$, $S\subsetneq X$ for $R,S$ and $X$ being sets
- $|X|$, for $X$ being some set, denotes the order of $X$

{% admonition gray %}
![](image-20191208153919722.png)
{% endadmonition %}

$(x,y)=(x',y')$ iff $x=x, y=y'$.

Cartesian product can be defined for multiple sets:

{% admonition gray %}
![](image-20191208212316131.png)
{% endadmonition %}

Note that $I$ can be any set, and is called the index set. $I$ can be infinite or even uncountable sets.

# Functions

## Definition of Function

**Functions** can be regarded as a special category of cartesian product.

{% admonition gray %}
![](image-20191208154252703.png)
{% endadmonition %}

There are some names:

- For each $(a,b)\in f$, denote $f(a)=b$ and call $b$ the value of $f$ at $a$. We also right $f:a\mapsto b$.
- $X$ is the **domain** of $f$
- $Y$ is the **codomain** (or the **target**) of $f$
- The subset $\{y\in Y|\exists x\in X: (x,y)\in f\}$ of $Y$ is called the image of $f$, denoted by $\text{im} f$.
- The set $f\subseteq X\times Y$ itself is called the graph of the function. 

Note that the whole function should be written as $f:X\to Y$ (the graph, the domain, and the codomain), but we usually denote the function by $f$ for simplicity.

![](function.png)
The definition of **domain**, **codomain**(**target**), **image** can be read from the picture.

{% admonition gray %}
![](image-20191208161455431.png)
{% endadmonition %}

In short (might be ambigious but friendly): Equal functions are equal subset of cartesian product of equal sets. Or we say two functions are equal iff they have same domains, same codomains and same graphs.

<u>***Some Special Functions***</u>

**Identity Function**: $1_X: X\to X$ is the function such that  $\forall x\in X: f(x)=x$.

**Ristriction**: For $f:X\to Y$, a ristriction on $S\subseteq X$ denoted by $f|S: S\to Y$ is defined by $(f|S)(s)=f(s)$ for all $s\in S$.

**Inclusion**: For $S\subseteq X$, inclusion $i:S\to X$ is defined as $i(s)=s$ for all $s\in S$.

The next proposition gives us a tool to prove the equality of functions.

{% admonition gray %}
![](image-20191208190949264.png)
{% endadmonition %}

One might think this proposition is redundant. This definition is necessary due to our way of defining function.

Function can often be defined by showing the way of mapping. For example, $f$ such that $f(x)=x+1$ could define a function $f:\mathbb R\to\mathbb R$. This definition is complete only if $f$ gives the unique function. We say $f$ is well-defined if $f$ gives the unique function. 

**Example** $g(a/b)=ab$ is not well-defined. There are many ways to write a fraction. Since $1/2=3/6$, $g(1/2)=1\cdot 2\neq 3\cdot 6=g(3/6)$.

## Surjection and Injection

{% admonition gray %}
![](image-20191208192845117.png)
{% endadmonition %}

{% admonition gray %}
![](image-20191208192900958.png)
{% endadmonition %}

There are other names, in conclusion:

| Projective Name | Preposition Name | Morphic Name |
| --------------- | ---------------- | ------------ |
| surjection      | onto             | epimorphism  |
| injection       | one-to-one       | monomorphism |

The understand the meaning behind the name **surjection**, one have to imagine. For $f:X\to Y$, one can imagine that $X$ and $Y$ are two piece of papers, and by putting $X$ on $Y$, suppose any $y\in Y$ is covered by $x\in X$ such that $f(x)=y$. Since any $y\in Y$ has been covered by some $x\in X$, then the whole $Y$ is covered by $X$, we say $X$ is on $Y$. As for **one-to-one** $f:X\to Y$, any $x\in X$ has unique $y\in Y$ such that $f(x)=y$. Then $(x,y)$ are paired (though some $y\in Y$ has not been paired to any $x$), the name "one-to-one" is straightforward.

{% admonition gray %}
![](image-20191208193219181.png)
{% endadmonition %}

## Composition and Inverse

{% admonition gray %}
![](image-20191208193336951.png)
{% endadmonition %}

Remember if you see notions like $(f_1\circ f_2\circ\cdots \circ f_n)(x)$, you have to compute from right to left. That is, compute $x_n=f_n(x)$ first, and then $x_{n-1}=f_{n-1}(x_n)$, etc.

{% admonition gray %}
![](image-20191208202958959.png)
{% endadmonition %}
Proof Sketch: Use **Proposition 1.43**.

{% admonition gray %}
![](image-20191208203358569.png)
{% endadmonition %}

The deninition of inverse here is quite wired, but it makes things clear. In the definition $f$ and $g$ are inverse of each other. One could denote the inverse of $f$ by $f^{-1}$ (this noting comes from the group theory). For a person like me, only cares about the following proposition:

{% admonition gray %}
![](image-20191208203741864.png)
{% endadmonition %}

Notice that for $f$ and $g$ being inverse of each other, $(a,b)\in f$ iff $(b,a)\in g$.

Inverse of function also gives us a new method of prove a function is a bijection: prove by finding a well-defined inverse of it.

{% admonition gray %}
![](image-20191208204218050.png)
{% endadmonition %}

The theorem will be straightforward after learning permutation group.

Note that we often abuse the notion. For $f:X\to Y$ and $S\subseteq X, Y\subseteq W$, we denote

- $f(S)=\{y\in Y| \exists s\in S: f(s)=y\}$
- $f^{-1}(y)=\{x\in X|f(x)=y\}$
- $f^{-1}(W)=\{x\in X|f(x)\in W\}$

It shows that the notion $f^{-1}$ not always denote the inverse of $f$. All these notions has to be computed from right to left.

{% admonition gray %}
![](image-20191208205002850.png)
{% endadmonition %}

**Proof Sketch**: 

1. The first half is straigforward and the second half follows the first half.

2. Since $f$ is surjection, any $u\in U$ is covered by some $x\in X$. Then if follows $ff^{-1}(U)=U$. 

3. Just a game of notion. Refer to the book for more information.

4. "$\subseteq$" is straightforward, we give a example of strict inclusion.

   For $f:\mathbb R\to \mathbb C$ defined by $x\mapsto e^{2\pi i x}$. If $S=\{0\}$, then $f(S)=1$, and $f^{-1}f(1)=\mathbb Z$.

   The strict inclusion happens if some $s\in S$ has $f(s)=y\in Y$ but $S$ doesn't contain all such $s$.

# Relation
{% admonition gray %}
![](image-20191208212608686.png)
{% endadmonition %}

The basic idea for relation itself is straighforward or most readers. Here we stressen that relation is noting but a subset of a cartesian product of two sets. Relations that $X=Y$ is used more often.

## Equivalence

{% admonition gray %}
![](image-20191208212854406.png)
{% endadmonition %}

Note that equivalence relation are always defined on one set $X$. It is a subset of $X\times X$.

Equivalence relation can devide the set it defines on into equivalence classes.

{% admonition gray %}
![](image-20191208213212150.png)
{% endadmonition %}

{% admonition gray %}
![](image-20191208213304925.png)
{% endadmonition %}
**Proof Sketch**: Can be proved by using definition.

{% admonition gray %}
![](image-20191208213359166.png)
{% endadmonition %}
**Proof Sketch**: Prove that every two equivalence classes has no intersection, which can be proved by showing that no $x\in X$ lies in two equivalence classes.