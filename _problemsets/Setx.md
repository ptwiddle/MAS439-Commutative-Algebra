---
title: Problem Set 10
duedate: 14th December
layout: default
---


Question 1: An almost inverse 
=======
(2 points)

In question 1 from the previous week, we constructed a surjective map $$\varphi:\mathbb{A}^1_{\mathbb{C}}\to X=V(y^2-x^3-x^2)$$.  Construct a rational map $$\psi:V\to\mathbb{A}^1$$ that is the inverse to this.  Where does $$\psi$$ fail to be regular?



Question 2: Finishing an example in class
=======
(2 points)

1. Let $$X$$ be an algebraic variety and $$f\in k(X)$$ a rational function on $$X$$.  Show that if $$f$$ has representative of the form $$f=g/h$$, with $$g, h\in k[X]$$, and $$h(p)=0$$ but $$g(p)\neq 0$$, then $$f$$ is not regular at $$p$$.

2. Find the domain of $$x/z$$ on $$V(xy-zw)$$.  (Hint: what we did in class together with Part 1 almost does everything; the last point can be dealt with using the fact that the locus where any rational function isn't well defined is an algebraic subset)


Question 3: Some category theory
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


Question 3: Category Theory and fraction fields (2 points)
=====

Let $$\mathcal{C}$$ be the category whose objects are integral domains, and whose morphisms $$\varphi:R\to S$$ are just ring homomorphisms from $$R$$ to $$S$$.  Let $$\mathcal{F}$$ be the category whose objects are fields, and whose morphisms are ring homomorphisms between fields.

1. Explain why the map that sends an integral domain to its fraction field cannot be made into a functor from $$\mathcal{C}$$ to $$\mathcal{F}$$. 
2. Let $$\mathcal{D}$$ be the category whose objects are integral domains and whose morphisms are injective ring homomorphisms.  Show that the map sending $$R$$ to its fraction field $$K(R)$$ can be made into a function for $$\mathcal{D}$$ to $$\mathcal{F}$$. (Hint -- use the universal property of fraction fields in the notes)
