---
layout: lecture
title: Lecture 7&#58; Quotient rings.  Motivation, definition, and examples
Comments: True
---

Last week we introduced ring homomorphisms and ideals; this week we will show how these concepts are related through the quotient ring.


Motivation
-----

We saw last week that if $$\varphi:R\to S$$ was a ring homomorphism, then $$\ker(\varphi)=\{r\in R \text{ such that } \varphi(r)=0\}$$
is an ideal of $$R$$.  The goal of today's lecture is to show that the converse is true:  given $$I\subset R$$ we construct the *quotient ring* $$R/I$$, and a surjective homomorphism $$p:R\to R/I$$ known as the *quotient map*, so that $$\ker(p)=I$$.

To motivate the definition, let's think about what $$R/I$$ would have to look like.  There is supposed to be a surjective map $$p:R \to R/I$$, so that means we can write any element of $$R/I$$ as $$p(a)$$, for some $$a \in R$$.  But such an $$a$$ need not be unique -- for instance, since $$I$$ is the kernel of $$p$$, we have that $$p(a)=0_{R/I}$$ for any $$a\in I$$.  

We will build $$R/I$$ out of $$R$$, so we can represent any element of $$R/I$$ as an equivalence class of elements of $$R$$ -- namely, element $$a\in R/I$$ will be represented by the set $$p^{-1}(a)$$.  Put another way, two elements will be equivalent if they map to the same thing under $$p$$:  $$a\sim p$$ if and only if $$p(a)=p(b)$$.

So when does $$p(a)=p(b)$$?  Well, this is equivalent to $$p(a-b)=0$$, i.e., that $$a-b$$ is in the kernel of $$p$$, which we are supposing is $$I$$.  So, we see that $$p(a)=p(b)$$ if and only if there is an $$r\in I$$ with $$a=b+r$$.

Addition and multiplication on $$R/I$$ are fixed by the fact that $$p$$ is a surjective homomorphism; if $$x,y$$ are two elemetns of $$R/I$$, write $$x=p(a), y=p(b)$$.  We must have:

$$x+y=p(a)+p(b)=p(a+b)$$ since $$p$$ is a homomorphism.  

Definition
-----

Thus, we are lead to:

Definition / Lemma
====

Let $$I\subset R$$ be an ideal.  The *quotient ring* $$R/I$$, as a set consists of equivalence classes for the relation $$x\sim y$$ if $$x-y\in I$$.  If $$x\in R$$, we denote the equivalence class containing $$x$$ by $$[x]$$.  Then we define addition and multiplication on $$R/I$$ by:

$$[x]+[y]=[x+y]$$

$$[x]\cdot[y]=[x\cdot y]$$

Then $$R/I$$ is a ring, with $$0_{R/I}=[0_R]$$ and $$1_{R/I}=[1_R]$$.

Furthermore, the map $$p:R\to R/I$$ defined by $$p(x)=[x]$$ is a surjective ring homomorphism with kernel $$I$$.

Proof
====

We should check that $$\sim$$ is an equivalence relation, that the $$+$$ and $$\cdot$$ operators on $$R/I$$ are well defined and satisfy the ring axioms, and that $$p$$ is well defined and is a surjective group homomorphism.   

First, we show $$\sim$$ is an equivalence relation.  

1. Reflexive: $$x\sim x$$ as $$x-x=0\in I$$, since any ideal contains $$0$$.
2. Symmetric: $$x\sim y$$ implies $$y\sim x$$, since $$y-x=-(y-x)\in I$$, since $$y-x\in I$$ and ideals are closed under multiplication by arbitrary elements of $$R$$ (here, -1).
3. Transitive: $$x\sim y$$ and $$y\sim z$$ imply $$x\sim z$$, since $$x-z=(x-y)+(y-z)\in I$$ since $$(x-y)$$ and $$(y-z)$$ are both in $$I$$ and $$I$$ is closed under addition.

Note that, although we proved number 2 using multiplication, we have really only used group theory; $$I$$ is a subgroup, and $$(x-y)$$ and $$(y-x)$$ are additive inverses of each other.

In particular, the equivalence classes of $$\sim$$ are exactly the cosets of $$I$$ in $$R$$, and sometimes the equivalence class $$[x]$$ is written $$x+I$$.

Addition and multiplication in $$R/I$$ as stated appear to depend on representatives $$x$$ of an equivalence class; we now show that they don't really depend on this choice; that is, that addition and multiplication on $$R/I$$ are well defined.

Suppose that $$x^\prime, y^\prime$$ were different representatives of $$[x]$$ and $$[y]$$; that is, $$x^\prime=x+i, y^\prime=y+j, i,j\in I$$.  Then we have

$$[x^\prime]+[y^\prime]=[x^\prime+y^\prime]=[x+i+y+j]=[x+y+(i+j)]=[x+y]$$

as since $$i,j\in I$$, and $$I$$ is an ideal, so is $$(i+j)$$.

Similarly, we have

$$[x^\prime]\cdot[y^\prime]=[x^\prime\cdot y^\prime]=[(x+i)\cdot(y+j)]=[x\cdot y+(x\cdot j+y\cdot i+ij)]=[x\cdot y]$$
since $$i,j\in I$$ and $$I$$ is closed under addition and under multiplication by arbitrary elements of $$R$$.

Checking the $$R/I$$ satisfies the ring axioms follows mechanically from the fact that $$R$$ satisfies the ring axioms.  For example, to check the distributive property, we have


$$\begin{eqnarray*}
[a]\cdot\left([b]+[c]\right)=[a]\cdot [b+c]=[a\cdot(b+c)]=[a\cdot b+a\cdot c]=[a\cdot b]+[a\cdot c]=[a]\cdot [b]+[a]\cdot[c]$$




Examples
-----

A few familiar/trivial examples:

Example:  $$R=\mathbb{Z}$$
===
Any ideal of $$\mathbb{Z}$$ is principal, i.e., $$(n)$$.  The quotient ring $$\mathbb{Z}/(n)=\mathbb{Z}/n\mathbb{Z}$$.

Example: General $$R$$
===
Any nontrivial ring has at least two ideals; the ideal $$\{0\}$$, and the ideal $$R$$.  We have $$R/(0)\cong R$$, and $$R/R$$ is the trivial ring.





The most important examples of quotient rings for us will be when $$R$$ is a polynomial ring (particularly over a field); i.e., $$R=k[x_1,\dots, x_n]$$.



Example
====

Let $$R=\mathbb{R}[x]$$, $$I=(x^2)$$.  To understand $$R/I$$, we need to understand the cosets of $$I$$ in $$R$$; to do this, it often helps to pick a unique representative of each coset.


What are the cosets of $$I$$?  Given any polynomial $$p(x)=a_nx^n+\cdots a_2x^2+a_1x+a_0$$, we have $$p(x)=x^2(a_n^{x^{n-2}+\cdots a_3x+a_2)x^2+a_1x+a_0$$, and so $$p(x)\sim a_1x+a_0$$, so every coset of $$I$$ can be represented by a linear polynomial.  Furthermore, this representative is unique.  

So we can view $$R/I$$ as a two dimensional vector space, with basis $$1$$ and $$x$$.  How do these multiply?  


Example
===

