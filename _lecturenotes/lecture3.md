---
layout: lecture
title: Lecture 3&#58; Roadmap.  Types of elements, types of rings
Comments: True
---



In this lecture we first introduce three types of elements of rings: units, zero divisors, and nilpotent elements, and then based on these, three types of rings: fields, integral domains, and reduced rings.  We then continue the discussion of subrings

Three types of elements
----

Definition
====

Let $$R$$ be a commutative ring.  We say a nonzero element of $$r\in R$$ is

1. A *unit*, if there exists $$s\in R$$ with $$r\cdot s=1$$.
2. A *zero divisor* if there exists $$s\in R, s\neq 0$$ with $$r\cdot s=0$$
3. *Nilpotent* if there exists a postive integer $$n$$ with $$r^n=0$$

Remark
===
You have to be slightly careful about whether you want to consider $$0$$ to be nilpotent or a zero-divisor.


Example: $$\mathbb{Z}/12\mathbb{Z}$$
===
Let us classify which elements of $$\mathbb{Z}/12\mathbb{Z}$$ are units, zero divisors, or nilpotent.

For $$[k]$$ to be a zero divisor, we need $$[k]\neq 0$$, and so 12 doesn't divide $$k$$, and we need another nonzero element $$[\ell]$$ with $$[k]\cdot [\ell]=0$$.  Thus, we need that 12 doesn't divide $$\ell$$ or $$k$$, but it does divide $$k\cdot \ell$$.  We see that if $$k$$ has a common factor $$f$$ with 12, say, $$k=f\cdot q$$, then $$[k]$$ is a zero divisor, because 

$$[k]\cdot [12/f]=[fq\cdot 12/f]=[12q]=0$$

So, 2,3,4,6,8,9,10 are all zero divisors in $$\mathbb{Z}/12\mathbb{Z}$$.

On the other hand, if $$k$$ does not have a common factor with 12, then by the Euclidean Algorithm we can find $$a, b\in \mathbb{Z}$$ with $$ak+12b=1$$, and hence $$ak=1-12b$$, and so $$[a]\cdot [k]=[1]$$ in $$\mathbb{Z}/12\mathbb{Z}$$ and $$k$$ is a unit in $$\mathbb{Z}/12{Z}$$.  

So 1,5,7,11 are all units in $$\mathbb{Z}/12\mathbb{Z}$$.

To see if $$[k]$$ is nilpotent, we can repeatedly multiply $$k$$ by itself and see what happens -- it turns out only $$[6]$$ is nilpotent, since $$6^2=36 \quad\square$$

In general, an element does not have to be of any of these three types -- for example, in $$\mathbb{Z}$$, there are no zero divisors or nilpotent elements, but the only units are $$\pm 1$$.

Lemma
====

Every nilpotent element is a zero divisor.

Proof
====

Suppose that $$r\in R$$ is a nilpotent element.  Then there is some *minimal* $$n>1$$ so that $$r^n=0$$ but $$r^{n-1}\neq 0$$.  Then $$r\cdot r^{n-1}=r^n=0$$, and so $$r$$ is a zero divisor. $$\quad\square$$

Three types of rings
----

Definition
====

We say that a commutative ring $$R$$ is:

1. a *field* if every nonzero $$r\in R$$ is a unit
2. an *integral domain* if $$R$$ has no zero divisors
3. *reduced* if $$R$$ has no nilpotent elements


Lemma
---
$$R$$ is a field implies $$R$$ is an integral domain implies $$R$$ is reduced.

Proof
----

Suppose $$R$$ is a field. Then if $$r\neq 0$$, since $$R$$ is a field there exists $$u\in R$$ with $$ur=1$$.  Now, suppose that $$s\in R$$ with $$0=rs$$.  Multiplying both sides by $$u$$, we have 

$$0=u(rs)=(ur)s=1s=s$$

and so $$s=1$$, and $$R$$ is an integral domain.

To see the second implication, note that we have already shown that any nilpotent element is a zero divisor.  So if $$R$$ does not have any zero divisors, it cannot have any nilpotent elements.  $$\quad\square$$


Examples of fields
----
 - $$\mathbb{Q}\subset\mathbb{R}\subset \mathbb{C}$$ are all fields
 - If $$p$$ is a prime, then $$\mathbb{Z}/p\mathbb{Z}$$ is a field.  
 - Let $$k$$ be a field; the set of *rational functions* with coefficients in $$k$$ is a field.  A rational function is an expression of the form

$$\frac{P(X)}{Q(X)}$$ 

where $$P(x),Q(x)\in k[x]$$ are polynomials, and $$Q\neq 0$$.

Examples of integral domains
=====

 - The ring $$\mathbb{Z}$$ is an integral domain, but not a field.
 - The ring $$R[x]$$ is an integral domain if and only if $$R$$ is

Examples of reduced rings
====

 - The ring $$\mathbb{Z}/6\mathbb{Z}$$ is reduced, but not an integral domain.
 - The ring $$\mathbb{Z}\times\mathbb{Z}$$ is reduced, but not an integral domain.
 - The ring $$R[X]$$ is reduced if and only if $$R$$ is.

Subrings and generating
----

In our motivating discussion of Fermat's last theorem, we discussed certain subrings of $$\mathbb{C}$$ obtained by taking $$\mathbb{Z}$$ and ``adding'' extra elements of $$\mathbb{C}$$; namely   It's not immediately clear what these rings look like, or even that they are rings.  We first define formally what we mean by this, and show that such subrings exist.  Our initial approach will be rather abstract and non-constructive, so we then give a more hands-on characterization.

Lemma
===
Subrings are closed under arbitrary intersection.  More formally, suppose that $$R$$ is a commutative ring, and that $$\{S_i, i\in I\}$$ is a set of subrings $$S_i\in R$$, indexed by an arbitrary set $$I$$.  Then $$\cap_{i\in I} S_i$$ is a subring of $$R$$.

Proof
====

We must show that $$\cap_{i\in I} S_i$$ contains the identity, and is closed under addition, taking negatives, and multiplication.

Since each $$S_i$$ are subrings, we have $$1\in S_i$$ for all $$i\in I$$, and hence $$1\in \cap S_i$$.

The other arguments are similar; we show that $$\cap_{i\in I} S_i$$ is closed under multiplication.  Suppose that $$r,s\in\cap_{i\in I} S_i$$; we must show $$r\cdot s \in\cap_{i\in I} S_i$$.  Pick an arbitrary $$i\in I$$.  Since $$r,s\in\cap_{i\in I} S_i$$, we have $$r,s\in S_i$$.  Since $$S_i$$ is a subring, we have $$r\cdot s\in S_i$$.  Since $$r\cdot s\in S_i$$ for all $$i$$, we have $$r\cdot s\in \cap_{i\in I} S_i\quad \square$$

Definition
=====

Let $$R$$ be a ring and $$T\subset S$$ a set.  Then the *subring of $$R$$ generated by $$T$$*, denoted $$\langle T\rangle$$, is the intersection of all subrings $$S\subset R$$ containing $$T$$.

It follows from this definition that the subring $$\langle T\rangle$$ is the smallest subring of $$R$$ containing $$T$$.    


Another characterization
----

Although above definition is elegant and useful for proofs, it is not particularly constructive: for any given $$r\in R$$, it is not clear directly from the definition whether or not $$r\in \langle T\rangle$$.  We now build $$\langle T\rangle T$$ from the inside out.

The idea is as follows: since $$\langle T\rangle $$ contains $$T$$ and is a subring, it must contain all sums of elements of $$T$$, and all products of elements we obtain in this way, and all sums of those, and all negatives of elements obtained in that way.  But because of the distributive rule, we can expand these out, and really all we need are sums 

Lemma
===

Let $$M(T)$$ denote the of all *monomials* of elements in $$T$$; that is

$$M(T)=\left\{ \prod_{i=1}^r t_i \text{ with } t_i\in T\right\}$$

Then 

$$\langle T \rangle =\left\{ \sum_{j=1}^s \pm m_j \text{ with } m_j\in M(t)\right\}$$


Proof
===

Let
$$[T] =\left\{ \sum_{j=1}^s \pm m_j \text{ with } m_j\in M(t)\right\}$$

Since $$\langle T\rangle$$ is the smallest subring containing $$T$$, to show $$[T]=\langle T\rangle $$ we show $$[T]\subset \langle T\rangle $$ and that $$[T]$$ is a subring of $$R$$ containing $$T$$.

Since $$\langle T\rangle$$ is defined to be the intersection of all subrings containing $$T$$, to show $$[T]\subset \langle T\rangle $$, we must show that if $$S$$ is any subring of $$R$$ containing $$T$$, then $$[T]\subset S$$.  

By the definition of $$S$$, we have $$T\subset S$$.  Since $$S$$ is a subring, it is closed under products, and so $$M(T)\subset S$$.  Further since $$S$$ is a subring, it is closed under taking negatives and sums, and so $$[T]\subset S$$.


We now show $$[T]$$ is a subring of $$R$$ containing $$T$$.  Taking one element products, we have $$T\subset M(T)$$, and taking one element sums, we have $$T\subset [T]$$, and so $$T\subset [T]$$; it remains to show $$[T]$$ is a subring of $$R$$.

The silliest (trickiest?) bit is showing $$1\in [T]$$.  The *empty product* is $$1$$, and so is in $$M(T)$$, and hence in $$[T]$$.  We must then show $$[T]$$ is closed under taking negatives and addition, which is immediate, and that $$[T]$$ is closed under products, which requires slightly more work: namely, that the product of any two elements of $$M(T)$$ is again in $$M(T)$$, and the use of the distributive property:

$$\left(\sum_{i=1}^r m_i\right)\cdot\left(\sum_{j=1}^s n_j\right)=\sum_{i=1}^r\sum_{j=1}^s m_i\cdot n_j \quad\square$$

