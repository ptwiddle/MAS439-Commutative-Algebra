---
title: Problem Set 3
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

Question 2: A non-finitely generated ideal (3 marks)
===

Let $$R$$ be the ring of continuous functions $$f:\mathbb{R}\to\mathbb{R}$$ with the usual pointwise operations.  Recall that we say $$f\in R$$ has *compact support* (or bounded support) if there is a real number $$M>0$$ so that:

$$|x|>M\implies f(x)=0$$

1. Prove that the subset $$I\subset R$$ consisting of functions with compact support is an ideal.
2. Prove that $$I$$ is not finitely-generated.

