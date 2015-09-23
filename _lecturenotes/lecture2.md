---
layout: lecture
title: Lecture 2&#58; Definition
comments: True
---

Definition
----------

The abstract definition of the

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
Although 