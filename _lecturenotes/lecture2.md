---
layout: lecture
title: Lecture 2&#58; Definition; new rings from old
comments: True
---

In this lecture we give the formal definition of an abstract ring and derive a few basic properties.  We then discuss a few ways to build new rings out of old ones: products of rings, polynomial rings and their cousins, and subrings.


Definition of a ring
----


 A **ring** $$(R,+,\cdot)$$ is a set $$R$$ together with two binary operations $$+$$ and $$\cdot$$ satisfying the following axioms:

 1. $$(R, +)$$ is an abelian group
 2. $$(R, \cdot)$$ is a monoid
 3. Addition and multiplication satisfy the distributive law

Expanding this out Point 1. (being an abelian group) means:

 - Addition is commutative and associative:  
$$a+b=b+a,  a+(b+c)=(a+b)+c$$
 - There is a zero element $$0_R$$ such that for all $$a \in R$$ we have $$a+0=a$$
 - Every element $$a\in R$$ has an additive inverse $$-a\in R$$ so that $$a+(-a)=0_R$$

Condition 2, being a monoid, is less familiar, but it means two things:
 - multiplication is associative:
   
$$a\cdot(b\cdot c)=(a\cdot b)\cdot c$$

for all $$a, b, c\in R$$.
 -  There is a multiplicative identity $$1_R$$ satisfying $$1_R\cdot a=a=a\cdot 1_R$$ for all $$a\in R$$

Finally, the distributive law is the familiar
$$(a+b)\cdot c=a\cdot c+b\cdot c, \quad a\cdot (b+c)=a\cdot b+a\cdot c$$

Remarks
====

The abstract definition of a ring is usually attributed to Emmy Noether.

*Warning*: There is some disagreement about whether an abstract ring needs to contain a 1 or not; Noether's original definition did not. 

A ring is *commutative* if multiplication in that ring is commutative, i.e., if $$x\cdot y = y\cdot x$$ for all $$x$$ and $$y$$ in $$R$$.

A small piece of notation
=======

For any element $$r\in R$$ of a commutative ring and any positive integer $$n$$, we use the notation

$$nr=\underbrace{r+r+\cdots+r}_{n\textrm{ times}}$$

$$r^n=\underbrace{r\cdot r\cdot r \dots\cdot r}_{n\textrm{ times}}$$




Basic properties
---------------

We derive a few extremely simple properties of rings.

Lemma
====

The zero element $$0_R$$ and the unit element $$1_R$$ are unique.
For any element $$r\in R$$, the element $$-r$$ is unique.

Proof
====
Suppose that $$0^\prime$$ was another another $$0$$ element of $$R$$.  That is, $$0^\prime+x=x$$ for all $$x\in R$$.

Then consider $$0_R+0_R^\prime$$.  Since $$0_R$$ is an additive identity, we must have $$0_R+0_R^\prime=0_R^\prime$$.  On the other hand, since $$0_R^\prime$$ is an additive identity we have $$0_R+0_R^\prime=0_R$$.  Hence, we have $$0_R=0_R^\prime$$.

The proof that $$1_R$$ is unique is comletely analogous, and the proof that $$-r$$ is unique is basically the same (and is identical to the proof that $$g^{-1}$$ is unique in a group), as $$(R, +)$$ is a group).$$\quad\square$$



Lemma
===
let $$R$$ be a ring; for any $$r\in R$$, we have
$$0_R\cdot r=0_R$$

$$(-1)\cdot r=-r$$

Proof
===
For the first statement, we have

$$0_R\cdot r=(0_R+0_R)\cdot r=0_R\cdot r+0_R\cdot r$$

Subtracting $$0_R\cdot r$$ from each side gives the desired result.

We have to be a little careful about what these terms mean; $$-r$$ is the (unique, by the previous lemma) element with $$(-r)+r=0$$, and so $$-1$$ is the element with $$(-1)+1=0$$.

Thus, we need to check that $$(-1)\cdot r$$ satisfies the defining property of $$-r$$:

$$(-1)\cdot r+r=(-1)\cdot r+1\cdot r=(-1+1)\cdot r=0\cdot r=0\quad\square$$

A pathological example
====

There is one ring, called the *trivial ring* with one element.  It is in many ways pathological.  In this ring, we have $$1_r=0_r$$.  In fact, we have:

Lemma
====

If $$R$$ is a ring with $$0_R=1_R$$, then $$R$$ is the trivial ring.

Proof
===

We must show that $$R$$ has one element; that is, that any element $$r\in R$$ is $$0_R$$.

We have:

$$r=1_R\cdot r=0_R\cdot r=0_R\quad\square$$



New rings from old
-----

We now introduce several ways to build new rings out of old ones.

Products of rings
====

If $$R$$ and $$S$$ are two rings, the product $$R\times S$$ is a ring.  The underlying set is the product of the two sets, and addition and multiplication is done component-wise.

$$(r_1,s_1)+(r_2,s_2)=(r_1+r_2,s_1+s_2)$$

$$(r_1,s_1)\cdot(r_2,s_2)=(r_1\cdot r_2,s_1\cdot s_2)$$

What are zero and one in the product ring?


Polynomial Rings and their cousins
----

Polynomial rings have a central place in the study of commutative rings.

For $$R$$ any commutative ring, the polynomial ring $$R[x]$$ as a set consists of finite formal sums 

$$a_0+a_1x+a_2x^2+\cdots+a_nx^n$$ 

where the $$a_n\in R$$

The elements of $$R[x]$$ are called *polynomials*.

Multiplication and addition are defined in the familiar way:

$$\left(\sum_{i\geq 0} a_i x^i\right)+\left(\sum_{j\geq 0} b_j x^j\right)=\sum_{k\geq 0} (a_k+b_k)x^k$$

$$\left(\sum_{i\geq 0} a_i x^i\right)\cdot\left(\sum_{j\geq 0} b_j x^j\right)=\sum_{k \geq 0} \sum_{i=0}^k (a_i\cdot b_{k-i}) x^k$$

Example
=====

In $$(\mathbb{Z}/\mathbb{5Z})[x]$$, we have $$(x^2+4x+3)\cdot (x^2+x+3)=x^4+4\quad\square$$


We can *evaluate* a polynomial $$p(x)\in R[x]$$ at an element $$r\in R$$ and get an element of $$R$$, by substituting $$r$$ in for $$x$$.

Example
====

If we evaluate the polynomial $$x^2+1\in (\mathbb{Z}/5\mathbb{Z})[x]$$ at the element $$2\in \mathbb{Z}/5\mathbb{Z}$$, we get $$0\quad\square$$ 



Example
===

To get polynomials in more than one variable, we can iterate this construction: $$R[x,y]$$, polynomials in two variables, can be viewed as polynomials in $$y$$ with coefficients in the ring $$R[x]$$ (or vice-versa).

E.g., we can write $$x^2+2xy+y^2-y+x+2=y^2+(2x-1)y+(x^2+x+2)$$



Variations
===

There are several variations on polynomials rings that will play a role later in the course.  

The power series ring $$R[[x]]$$ drops the condition that only finitely many of the coefficients are zero.

In $$R[x,x^{-1}]$$ we allow negative powers of $$x$$.

Questions for discussion / exercises to check
===

Are these variations still rings?  Do we lose anything in these compared to polynomial rings?  Can we allow both negative powers and infinitely many nonzero terms and still be a ring?  

If $$R$$ is the trivial ring, what is $$R[x]$$?


We began some discussion of these in lecture; please continue them in comments.

Subrings
---

Definition
===

A *subring* $$S$$ of a ring $$R$$ is a subset of $$R$$ that is also a ring, where all the structure of the ring is ``inherited'' from $$R$$.  Namely:
 - $$0_S=0_R$$
 - $$1_S=1_R$$
 - $$+_S=+_R$$
 - $$\cdot_S=\cdot_R$$

Many of the properties of a ring (associativity, the distribution law) are thus automatically satisified for subrings.  To check that something is a subring, it is only really required that it's closed under the various operations.

Lemma
=====

A subset $$S\subset R$$ is a subring of $$R$$ if and only if

 1. $$S$$ contains one: $$1_R\in S$$
 2. $$S$$ is closed under additive inverses: If $$s\in S$$, then $$-s\in S$$
 3. $$S$$ is closed under addition and multiplication: If $$s_1, s_2\in S$$, then $$s_1+s_2$$ and $$s_1\cdot s_2$$ are in $$S$$.

$$\square$$




Examples
=======

 - We have the chain of subrings $$\mathbb{Z}\subset\mathbb{Q}\subset\mathbb{R}\subset\mathbb{C}$$
 - The Gaussian integers $$\mathbb{Z}[i]\subset \mathbb{C}$$ is a subset of the complex numbers.
 - The subset of $$a_0+a_1x+a_2x^2+\cdots\in \mathbb{Z}[x]$$ so that $$a_i$$ is divisible by 2 is *not* a subring; but if we allow $$a_0$$ to be odd and require $$a_i$$ to be even for $$i\geq 1$$, then we *do* have a subring.
 - The set of elements $$(r,0)\subset R\times S$$ in the product of two rings is *not* a ring.


Example
====

Let's classify the subrings of $$\mathbb{Z}$$.  Suppose that $$S\subset \mathbb{Z}$$ is a subring.  We have from that axioms that $$1\in S$$.  Since $$S$$ is closed under addition, we have $$1+1=2\in S$$, and then $$1+2=3\in S$$, and by induction we see $$S$$ contains all positive integers.  Since $$S$$ is closed under additive inverses, we see it must contain all negative integers as well, and so $$S=\mathbb{Z}$$.  Hence the only subring of $$\mathbb{Z}$$ is $$\mathbb{Z}$$ itself. $$\quad\square$$

Question for discussion
=====

What are the subrings of $$\mathbb{Z}\times(\mathbb{Z}/2\mathbb{Z})?$$