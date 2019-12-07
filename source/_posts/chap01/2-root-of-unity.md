# Real Number 

Real number can be defined by many ways. The most famous definition is to define it as $\mathbb C=\{(a,b)|a,b\in\mathbb R\}$ and write $(a,b)$ into $a+bi$. By define

$$
\begin{aligned}
(a,b)+(c,d)&=(a+c,b+d) \\
(a,b)\cdot (c,d) &= (ac-bd,ad+bc)
\end{aligned}
$$

 one can induce that $i^2=-1$.

{% admonition gray %}
**Definition** The modulus $|z|$ of $z=a+bi\in\mathbb C$ is defined as $|z|=\sqrt{a^2+b^2}$.
{% endadmonition %}

Triangle Inequality for Complex: For any $z,w\in\mathbb C$, $|z+w|\leq |z|+|w|$.

{% admonition gray %}
![](image-20191207194556815.png)
{% endadmonition %}

**An Geometric Explaination**: Since any $z\in\mathbb C$ can be represented by a point on the complex plane, this fact can be seen directly.
**What to Proof**: Figure out what exactly $r$ equals to and prove there is such $\theta$ satisfy our decompose with our $r$.

{% admonition gray %}
**Definition** The **complex conjugate** (or just **conjugate**) of a complex number $z=a+bi$ is $\bar z=a-bi$.
{% endadmonition %}

Properties for Complex Conjugate:

- $z^{-1}=\frac{\bar z}{|z|}$
- $\overline{z+w}=\bar z+\bar w$
- $\overline{zw}=\bar z\bar w$
- $\bar{\bar z}=z$
- $\bar z=z$ iff $z\in\mathbb R$

{% admonition gray %}
![](image-20191207195041133.png)
{% endadmonition %}
Proof can be done by using trigonometry.

The next 2 proposition can be proved by using trigonometry as well, we list them here without proving.
{% admonition gray %}
![](image-20191207195340068.png)
{% endadmonition %}

{% admonition gray %}
![](image-20191207195504131.png)
{% endadmonition %}

The next fact can be proved by series $e^x=1+x+\frac{x^2}{2!}+\frac{x^3}{3!}+\cdots$.
{% admonition gray %}
![](2image-20191207202058225.png)
{% endadmonition %}

# Root of Unity

{% admonition gray %}
![](/image-20191207202323867.png)
{% endadmonition %}

The basic idea of root of unity can be illustrated:

![](image-20191207202502001.png)

And its to read out from the last image that:
{% admonition gray %}
![](image-20191207202532737.png)
{% endadmonition %}

{% admonition gray %}
**Definition** An $n$th root of unity $\zeta$ is an primitive $n$th root of unity if for all $m<n$, $\zeta$ is not a $m$th root of unity.
{% endadmonition %}

For example, $i$ is a $8$th root of unity, but it is not a primitive $8$th root of unity since $i$ is a $4$th root of unity.

The next lemma can also be read out from the previous image:

{% admonition gray %}
![](image-20191207203029592.png)
{% endadmonition %}
Proof Sketchy: Prove by division algorithm.

{% admonition gray %}
![](image-20191207203206188.png)
{% endadmonition %}

{% admonition gray %}
![](image-20191207204139986.png)
{% endadmonition %}
**Proof**: Notice the fact that
$$
\prod_{d|n}\Phi_{d}(x)=\prod_{i=1}^n(x-\zeta^i)
$$
where $\zeta=e^{\frac{2\pi}{n}}$. Since all $\zeta^i$ are roots for $x^n-1$ and $x^n-1$ has at most $n$ roots (this fact will be proved in **CHAP 03**), then there must be $x^n-1=\prod_{i=1}^n(x-\zeta^i)$. QED.

{% admonition gray %}
![](image-20191207214936988.png)
{% endadmonition %}

**Proof**: We prove by induction. The base step holds, for $\Phi_1(x)=x-1$. For inductive step, assume all $d<n$ the proposition holds. Since $x^n-1=\prod_d \Phi_d(x)$, we have
$$
x^n-1=\Phi_n(x)\cdot f(x)
$$
where $f(x)$ is the product of all $\Phi_d(x)$ such that $d<n$ and $d|n$. Then $f(x)$ is a monic polynomial with integer coefficients. By division algorithm, $\Phi_n(x)=(x^n-1)/f(x)$ is also such a polynomial.

The next corollary will be used in **CHAP 08** to prove **Wedderburn's Theorem**.

{% admonition gray %}
![](image-20191207215609186.png)
{% endadmonition %}

**Proof**: Setting $x=q$ in $x^n-1=\Phi_n(x)\cdot f(x)$ proves $\Phi_d(q)$ is a divisor of $q^n-1$. If $d$ is a divisor of $n$, then $f(x)=(x^d-1)g(x)$ for some $g(x)$ be a monic polyoniaml with integer coefficients (this fact holds that we can find all $(x-\zeta^i)$ in $f(x)$ where $\zeta=e^{\frac{2\pi}{d}}$ ). Then
$$
\Phi_n(x)g(x)=\frac{x^n-1}{x^d-1}
$$
Let $x=q$, one can prove the proposition.

# Euler Function

Euler has too equivalent definitions: 
{% admonition gray %}
![](image-20191207212223878.png)
{% endadmonition %}
{% admonition gray %}
![](image-20191207212215759.png)
{% endadmonition %}
The value of $\deg(\Phi_d)$ is the number of primitive $n$th root of unity, and is equal to the number of integers $1\leq k\leq n$ such that $\gcd(k,n)=1$.
{% admonition gray %}
![](image-20191207212830685.png)
{% endadmonition %}