---
layout: lecture
title: Lecture 2&#58; Definition
comments: True
---

Definition
----------

The abstract definition of a ring is usually attributed to Emmy Noether.

> A **ring** $$(R,+,*)$$ is a set $$R$$ together with two binary operations $$+$$ and $$*$$ satisfying the following axioms:
>
> 1. $$(R, +)$$ is an abelian group
> 2. $$(R, *)$$ is a monoid
> 3. Addition and multiplication satisfy the distributive law

Expanding this out, point 1. (being an abelian group) means:

a. Addition is commutative and associative:  
$$a+b=b+a,  a+(b+c)=(a+b)+c$$

b. There is a zero element $$0_R$$ such that for all $$a \in R$$ we have $$a+0=a$$
c. Every element $$a\in R$$ has an additive inverse $$-a\in R$$ so that $$a+(-a)=0_R$$

Condition 2, being a monoid, is less familiar, but it means two things:
a.m<ultiplication is associative:
   $$a*(b*c)=(a*b)*c$$
for all $$a, b, c\in R$$.
b.  There is a multiplicative identity $$1_R$$ satisfying $$1_R*a=a=a*1_R$$ for all $$a\in R$$

Finally, the distributive law is the familiar
$$(a+b)*c=a*c+b*c,  a\cdot (b+c)=a\cdot b+a\cdot c$$

*Warning*: There is some disagreement about whether an abstract ring needs to contain a 1. 

A ring is *commutative* if multiplication in that ring is commutative, i.e., if $$x\cdot y = y\cdot x$$ for all $$x$$ and $$y$$ in $$R$$.


Lemma
-----

The zero element $$0_R$$ and the unit element $$1_R$$ are unique.

Proof
-----
Suppose that $$0^\prime$$ was another another $$0$$ element of $$R$$.  That is, $$0^\prime+x=x$$ for all $$x\in R$$.

Then consider $$0_R+0_R^\prime$$.  Since $$0_R$$ is an additive identity, we must have $$0_R+0_R^\prime=0_R^\prime$$.  On the other hand, since $$0_R^\prime$$ is an additive identity we have $$0_R+0_R^\prime=0_R$$.  Hence, we have $$0_R=0_R^\prime$$.



Polynomial Rings and power series rings.
==========

Polynomial rings have a central place in the study of rings.

For $$R$$ a commutative ring, the *power series ring* $$R[[x]]$$ as a set consists of formal sums 

$$a_0+a_1x+a_2x^2+\cdots+a_nx^n+\cdots$$ 

where the $$a_n\in R$$

Multiplication and addition are defined in the familiar way:

$$\left(\sum_{i\geq 0} a_i x^i\right)+\left(\sum_{j\geq 0} b_j x^j\right)=\sum (a_i+b_i)x^i$$

$$\left(\sum_{i\geq 0} a_i x^i\right)\cdot\left(\sum_{j\geq 0} b_j x^j\right)=\sum_{k \geq 0} \sum_{i=0}^k (a_i\cdot b_{k-i}) x^k$$

The *polynomial ring* $$R[x]$$ is the same, except now we only allow *finite* formal sums; alternatively, the $$R[x]$$ is the subring of $$R[[x]]$$ consisting of elements where all but finitely many of the $$a_i$$ are zero.

