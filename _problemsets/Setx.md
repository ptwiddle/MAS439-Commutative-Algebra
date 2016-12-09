---
title: Problem Set 10
duedate: 19th December
layout: default
---




Question 1
======
(4 points)

The first exercise is some practice in thinking categorically -- in thinking in terms of maps between things, rather than about elements of things.  We use the following definitions:

 Let $$\mathcal{C}$$ be a category.  We say a morphism $$f:A\to B$$ is a

 - *epimorphism* if for any two morphisms $$g:B\to C$$ and $$h:B\to C$$, we have $$g\circ f=h\circ f$$ implies that $$g=h$$.
 - *monomorphism* if for any two morphisms $$d:Z\to A$$ and $$e:Z\to A$$ we have $$f\circ d=f\circ e$$ implies that $$d=e$$
 - *retraction* if there exists $$s:B\to A$$ with $$f\circ s=1_B$$
 - *section* if there exists $$r:B\to A$$ with $$r\circ f=1_A$$.



1. Prove that in any category $$\mathcal{C}$$, any retraction is an epimorphism, and any section is a monomorphism.
2. Prove that in the category of sets, with functions as morphisms, that the function $$f:A\to B$$ being a retraction and being an epimorphism are both equivalent to being a surjection.
3. In the category of rings, it is true that surjections and epimorphisms are the same things, but these are no longer equivalent to retractions.  Give an example to show this -- i.e., give a surjective map of rings $$f:R\to S$$ that is not a retraction.  

Question 2: Duality (3 points)
=====

We discussed the notion of duality in categories obtained by "reversing all the arrows"; this is often done with   In category theory, the [product](https://en.wikipedia.org/wiki/Product_(category_theory)) $$A\prod B$$ of two objects is defined very generally in terms of a universal property (check out the link for the precise details), and the dual notion of [coproduct](https://en.wikipedia.org/wiki/Coproduct) $$A\amalg B$$ does just reverse all the arrows.

1. Wikipedia claims that the product and coproduct in the category of sets are the cartesian product and disjoint union, respectively.  Proof this by showing cartesian product and disjoint unions of sets satisfy the appropriate conditions.
2. Wikipedia further claims that for vector spaces, the product $$A\prod B$$ and coproduct $$A\amalg B$$ are both just direct sum of vector spaces $$A\oplus B$$.  Prove this.  (Note this is false we take infinitely many vector spaces $$A_i$$ and..)

Question for thought:  Does the category of rings have a coproduct?

Question 3: Fraction fields (3 points)
=====

Let $$\mathcal{C}$$ be the category whose objects are integral domains, and whose morphisms $$\varphi:R\to S$$ are just ring homomorphisms from $$R$$ to $$S$$.  Let $$\mathcal{F}$$ be the category whose objects are fields, and whose morphisms are ring homomorphisms between fields.

1. Explain why the map that sends an integral domain to its fraction field cannot be made into a functor from $$\mathcal{C}$$ to $$\mathcal{F}$$. 
2. Let $$\mathcal{D}$$ be the category whose objects are integral domains and whose morphisms are injective ring homomorphisms.  Show that the map sending $$R$$ to its fraction field $$K(R)$$ can be made into a function for $$\mathcal{D}$$ to $$\mathcal{F}$$.

