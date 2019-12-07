This section is a review of number theory. This section is quite important, it cares about the accurate definition of conceptions that you ignores, which will be generalized to algebraic structures.

-----



# Notions

Rotman denotes the greastest commnon divisior of $a,b$ as $(a,b)$. Since $(a,b)$ has too many meanings, I prefer use $\gcd(a,b)$. And for least common multiple of $a,b$, I prefer $\text{lcm}(a,b)$.

# Axiom of Nature Numbers

We starts from **natural number**. Natural numbers can be defined by [Peano Axioms]( https://en.wikipedia.org/wiki/Peano_axioms ). In our whole course, natural numbers starts from 0, that is
$$
\mathbb N=\{0,1,2,\cdots\}
$$


**Least Integer Axiom**: There is a smallest integer in every nonempty subset of $\mathbb N$.

{% admonition gray %}
![](1573048398593.png)
{% endadmonition %}

This is the definition of prime number. But I think it's better to define them in another way.

{% admonition gray %}
**Definition.** A number $p$ is ***prime*** if $p\geq 2$ and for any $a,b\in\mathbb N$ if $p\mid ab$ then $p\mid a$ or $p\mid b$.
{% endadmonition %}


One can prove that the above two definitons are equal, but we are going to use the 2nd one to define prime elements in rings. As for the first one, a similar definition in ring is for irreducible elements.

We have "irreducible numbers" $\iff$ prime numbers.

For us, it is better to remember the 2nd definition as the def of prime numbers and regard the 1st def as a property.

{% admonition gray %}
![](1573110825990.png)
{% endadmonition %}

Proof Sketch: Use the least integer axiom to argue that the set $C$ containing all integers which the property is false should be $\emptyset$.

We list 2 mathematical induction here without proofs.

{% admonition gray %}
![](1573110949954.png)
{% endadmonition %}

{% admonition gray %}
![](1573110970162.png)
{% endadmonition %}

Both theorems can be proved by useing least integer axioms.



# Division and Properties of Prime Numbers

One should be very careful when reviewing this part, since it will be used frequently in rings.

{% admonition gray %}
![](1573111063264.png)
{% endadmonition %}

Proof Sketch: The theorem can be proved by contradiction.

{% admonition gray %}
![](1573111118736.png)
{% endadmonition %}

:warning: Warning! The division algorithm makes sense, in particular, when $b$ is negative. Divided by same $a$, $b$ and $-b$ usually leave different remaiders.

{% admonition gray %}
![](1573111288171.png) 
{% endadmonition %}

There are many proofs of this corollary, the most famous one is Euclid's. More proof's can be found in Hardy's impressive book.

{% admonition gray %}
![](1573111379887.png)
{% endadmonition %}

**Divisibility** cares about whether $b$ is a multiple of $b$, but cares nothing about which multiple $b$ is.

{% admonition gray %}
![](1573111665514.png)
{% endadmonition %}

{% admonition gray %}
![](1573111716880.png)
{% endadmonition %}

The next theorem is quite important. We write down the whole proof.

{% admonition gray %}
![](1573111808358.png)
{% endadmonition %}

Proof Sketch: The proof uses a basic idea in ring, the ideal. By find the smallest positive $d$ in $I=\{sa+tb|s,t\in\mathbb Z\}$, one can prove that $I=(d)$.

**Proof**: Let $I=\{sa+tb|s,t\in\mathbb Z\}$, then $I\neq \{0\}$. Since $a\in I\iff -a\in I$, $I$ must contain a least positive integer, we call it $d$. We now prove $I=(d)=\{kd|k\in\mathbb Z\}$.

- Clearly, $(d)\subseteq I$, since $d=sa+tb$ for some $s,t\in \mathbb Z$ then $kd=(ks)a+(kt)d$.
- $I\subseteq (d)$. For any $e\in I$, $e=dq+r$ where $0\leq r< d$  for some $d,r$. Since $e,dq\in I\Rightarrow r=e-dq\in I$, then $r=0$.

Then $d$ could devide $a$ and $b$. Can there be some $d'\geq d$ that $d'$ devides $a$ and $b$ lies in $I$? No, if positive $d'$ devides $a$ and $b$ and larger than $d$, then $sa+tb$ would be a multiple of $d'$ —— we could never reach $d$.

{% admonition gray %}
![](1573112839304.png)
{% endadmonition %}

{% admonition gray %}
![](1573113565337.png)
{% endadmonition %}

$I$ is the ideal of $\mathbb Z$ generated by $d$.

{% admonition gray %}
![](1573113672759.png)
{% endadmonition %}

This can be induced by our definition of prime numbers.

{% admonition gray %}
![](1573113758349.png)
{% endadmonition %}

{% admonition gray %}
![](1573113798846.png)
{% endadmonition %}

{% admonition gray %}
![](1573113832637.png)
{% endadmonition %}

This proposition can be proved by [Binomial Theorem]( https://en.wikipedia.org/wiki/Binomial_theorem ).

{% admonition gray %}
![](1573113936311.png)
{% endadmonition %}

This proposition can be proved by using **Theorem 1.7**.



The next proposition talks about base.

{% admonition gray %}
![](1573114008887.png)
{% endadmonition %}

The proposition can be proved by division algorithm and least integer axiom.





Fundamental theorem of arithmetic talks about the  unique fractorization of a integer $a\geq 2$.

{% admonition gray %}
![](1573114159930.png)
{% endadmonition %}

Proof Sketch: This theorem can be proved by induction and Euclid's Lemma.

{% admonition gray %}
![](1573114263039.png)
{% endadmonition %}

{% admonition gray %}
![](1573218044602.png)
{% endadmonition %}

Proof Sketch: I prefer proof by contradiction, since it's straightforward.



# Modulo Algorithm

{% admonition gray %}
![](1573218259126.png)
{% endadmonition %}

The modulo algorithm on integers is straightforward, we have to stress that it can be explain by the language of group or ring. And modulo algorithm can be generalized to groups and rings.

{% admonition gray %}
![](1573218455861.png)
{% endadmonition %}

These just say a modulo relationship is a congruence.

{% admonition gray %}
![](1573218650230.png) 
{% endadmonition %}

{% admonition gray %}
![](1573218785967.png)
{% endadmonition %}

We now introduce some very important inductions. They are quite powerful and frequently used in cryptography, thought easy to be proved.

{% admonition gray %}
![](1573219335276.png)
{% endadmonition %}

Proof Sketch: Again use the binomial theory.

{% admonition gray %}
![](1573219375780.png)
{% endadmonition %}

I prefer to use group theory to prove Fermat theory. It  can also be proved by mathematical induction.

{% admonition gray %}
![](1573219807052.png)
{% endadmonition %}

Proof Sketch: Use Fermat Theory (1.24).

## Solving Modulo Equation

{% admonition gray %}
![](1573220036651.png)
{% endadmonition %}

The solution in the theorem can be checked easily. For different solutions $x_1,x_2$, there is $a(x_1-x_2)\equiv 0\mod m$. Since $\gcd(a,m)=1$, there must be $x_1-x_2\equiv 0\mod m$.

{% admonition gray %}
![](image-20191206213909947.png)
{% endadmonition %}

The next old theorem is quite important. We are going to talk about the ring version of it when study communitive ring.
{% admonition gray %}
![](image-20191206214005002.png)
{% endadmonition %}
We left the proof of this theorem in the notes of number theory.