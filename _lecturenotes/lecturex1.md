---
layout: lecture
title: Lecture 11&#58; Isomorphism theorem, Algebras
Comments: True
---
 
In this lecture we begin by paying off some debts that I owe you, and declaring bankruptcy on others.  We then define algebras and look at some examples.


Debts
----

First, a lemma we never proved:

Lemma
====
 $$R/I$$ is a field if and only if $$I$$ is a maximal ideal.

Proof
===


Begin by noting that $$R/I$$ is a field if and only if for each $$[x]\neq 0\in R/I$$, there is a $$[y]\in R/I$$ with $$[x]\cdot [y]=[1]\in R/I$$.

Lifting this to $$R$$, we see that $$[x]\neq 0$$ is equivalent to $$x\notin I$$, and $$[x]\cdot [y]=[1]$$ is equivalent to $$x\cdot y=1+r$$, where $$r\in I$$, which is equivalent to $$1\in (x, I)$$.  

But the ideal $$I$$ being maximal is equivalent to $$(x,I)=R$$ for any $$x\notin I$$, or equivalently $$1\in (x,I)$$ for any $$x\notin I\quad \square$$.

In Tom's notes, this lemma is proved using one of the isomorphism theorems, which I will declare bankruptcy on and not prove.  However, we state them here:

Lemma (First isomorphism theorem / Universal property of quotient ring)
===
Let $$I\subset R$$ an ideal, and suppose that $$f:R\to S$$ is a ring homomorphism, with $$I\subset \ker(f)$$.  Then there exists a unique homomorphism $$\overline{f}:R/I$$ so that $$f=\overline{f}\circ p$$.


<a href="http://presheaf.com/?d=d24w694i1u1c2a15a165r514s37024"><img src="http://presheaf.com/cache/d24w694i1u1c2a15a165r514s37024.png" title="click to go to presheaf.com for editing"/></a>
$$\square$$


Lemma (Second isomorphism theorem)
====

There is a one to one correspondence between the ideals of $$R/I$$ and ideals of $$R$$ that contain $$I \quad \square$$

Note that the second isomorphism immeediately gives another proof that $$R/I$$ is a field if and only $$I$$ is maximal.


Lemma (third isomorphism theorem)
===

Let $$I\subset J$$ be ideals of $$R$$. There is a natural isomorphism 

$$R/J\cong (R/I)/(J/I)$$.

Algebras
----

We now define the category $$R-\bf{Alg}$$ of $$R$$-algebras.

Definition
====
Let $$R$$ be a ring.  An $$R$$-algebra is a pair $$(S,\varphi)$$ where $$S$$ isa  ring and $$\varphi:R\to S$$ is a morphism. A morphism of $$R$$-algebras $$f:(S, \varphi)\to (T,\psi)$$ is a map of rings $$f:S\to T$$ so that $$\varphi=\psi f$$, i.e., the following diagram commutes:

<a href="http://www.presheaf.com/?d=d3v1l4v1n3t4wr12m3s2b2567i3a23"><img src="http://presheaf.com/cache/d3v1l4v1n3t4wr12m3s2b2567i3a23.png" title="click to go to presheaf.com for editing"/></a>


Example: $$R[x]$$
===

The most important example is that $$R[x]$$ is an $$R$$-algebra, with structure map $$\varphi:R\to R[x]$$ that includes $$R$$ as the constant map.

Example: $$R$$ is a field
===
Usually we will take $$R$$ to be field, say, $$k$$.  Then, since any map $$\varphi:k\to S$$ for a nontrivial ring $$S$$ is injective, any nontrivial $$k$$-algebra contains a copy of $$k$$ in it (namely, $$\varphi(k)$$.  

Furthermore, if $$\lambda in k$$ and $$s \in S$$, we have a way of multiplying them together to get an element $$\lambda s\in S$$, namely $$\varphi(\lambda)\cdot s$$.  This turns $$S$$ into a vector space over $$k$$, and the multiplication map is bilinear.

Example: $$\mathbb{Z}$$-algebras
===

The category of $$\mathbb{Z}$$ algebras is just the same thing as the category of rings.  

This boils down to the fact that $$\mathbb{Z}$$ is the initial object in the category of rings, that is, there is a unique morphism $$\mathbb{Z}\to R$$ for any ring $$R$$.  Thus, for any ring $$R$$, there is a unique way to turn it into a $$\mathbb{Z}$$-algebra.  

Furthermore, any map of rings is automatically a map of $$\mathbb{Z}$$-algebras, because the two composition $$f \varphi$4 and $$\psi$$ must be equal.


Example: Complex conjugation as an algebra map.
===

The complex numbers $$\mathbb{C}$$ are a $$\mathbb{C}$$ algebra, with structure map just the identity.

Consider the complex conjugation $$z\mapsto \overline{z}$$ as a map from $$\mathbb{C}$$ to $$\mathbb{C}$$.  This is a ring homomorphism, since $$\overline{z+w}=\overline{z}+\overline{w}$$ and $$\overline{z\dot w}=\overline{z}\cdot \overline{w}$$.  

However, it is *not* a map of $$\mathbb{C}$$ algebra from $$\mathbb{C}$$ to itself.


The complex numbers are also an $$\mathbb{R}$$ algebra, with structure map the natural inclusion of $$\mathbb{R}\to\mathbb{C}$$.  Since any real number $$r$$ is fixed under complex conjugation $$\overline{r}=r$$, complex conjugation *is* a map of $$\mathbb{R}$$-algebras.