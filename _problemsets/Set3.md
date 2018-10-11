---
tite: Problem Set 3
duedate: October 19th
layout: default
---

Question 1: Rings with 4 elements (7 marks)
===
We already know three rings with four elements: $$\mathbb{Z}/4, \mathbb{Z}/2\times\mathbb{Z}/2$$ and $$\mathbb{F}_4$$, the field with four elements, which we constructed as quotient ring $$\mathbb{F}_4=\mathbb{Z}/2[x]/(x^2+x+1)$$.

In addition to $$x^2+x+1$$, there are three more quadratic polynomials in $$\mathbb{F}_2[x]$$ ($$\mathbb{F}_2$$ is just what we write for $$\mathbb{Z}_2$$ when we want to emphasize it's a field):

$$f_1=x^2,\quad f_2=x^2+x,\quad f_3=x^2+1$$. 

First, prove that each of the rings $$R_i=\mathbb{F}_2[x]/(f_i)$$ has four elements -- do this for all three at one time.

Then, write down the multiplication tables for each of the rings $$R_i$$, and for each one determine:
 * Is $$R_i$$ reduced?  
 * Is $$R_i$$ an integral domain?
 * Is $$R_i$$ a field?
 * Is $$R_i$$ isomorphic to one of three rings with four elements we already knew?
 
Finally, decide which of the $$R_i$$ are isomorphic to each other, and which are not? 

Completely optional challenge (i.e., for coffee and biscuits, not points): Prove that we've now constructed every ring with four elements.


Question 2: Thinking with morphisms
======
(3 points)

This exercise is some practice in thinking categorically -- in thinking in terms of maps between things, rather than about elements of things.  We use the following definitions:

 Let $$\mathcal{C}$$ be a category.  We say a morphism $$f:A\to B$$ is a

 - *epimorphism* if for any two morphisms $$g:B\to C$$ and $$h:B\to C$$, we have $$g\circ f=h\circ f$$ implies that $$g=h$$.
 - *monomorphism* if for any two morphisms $$d:Z\to A$$ and $$e:Z\to A$$ we have $$f\circ d=f\circ e$$ implies that $$d=e$$
 - *retraction* if there exists $$s:B\to A$$ with $$f\circ s=1_B$$
 - *section* if there exists $$r:B\to A$$ with $$r\circ f=1_A$$.


1. Prove that in any category $$\mathcal{C}$$, any retraction is an epimorphism, and any section is a monomorphism. (Hint: The second part is the first part with "all the arrows reversed")
2. Prove that in the category of sets, with functions as morphisms, that the function $$f:A\to B$$ being a retraction and being an epimorphism are both equivalent to being a surjection.
3. In the category of rings, it is true that surjections and epimorphisms are the same things, but these are no longer equivalent to retractions.  Give an example to show this -- i.e., give a surjective map of rings $$f:R\to S$$ that is not a retraction.  