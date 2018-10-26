---
title: Problem Set 5
duedate: November 2nd
layout: default
---
Question 1: Dimensions of $$\mathbb{C}$$-algebras
=======
Computer the dimensions of the following $$\mathbb{C}$$-algebras (they're all finite dimensional).  In each case give a basis for the algebra as a complex vector space. Give some explanation, but full proofs are unnecessary.

1. $$\mathbb{C}[x,y]/(x^3,xy,y^2)$$
2. $$\mathbb{C}[x,y]/(x^2+y^2, x-y^3)$$

(3 marks)

Question 2: Using Universal Properties
=======

It is annoying to actually check that a given set map is a homomorphism by hand, but if we use the universal properties of polynomial rings and quotient rings we can construct maps we know are homomorphisms without doing the labor of checking it.  Using both of these universal properties, carefully prove that:

1. $$\mathbb{C}[z]$$ is isomorphic to $$\mathbb{C}[x,y]/(y-3)$$
2. For any ring $$k$$, $$k[x]/(x^2-x)$$ is isomorphic to $$k\times k$$.

(The $$k$$-algebra structure on $$k\times k$$ is $$\varphi(r)=(r,r)$$)

In each case you should use the universal properties to construct a homomorphism of algebras from one algebra to the other, and then prove your homomorphism is an isomorphism.

(4 marks)

Question 3: A nonfinitely generated ideal
======

Next week we will prove that if $$k$$ is a field, then every ideal in $$k[x_1,\dots, x_n]$$ is finitely generated.  Before we do so, it may be beneficial to have see an example of an ideal that *isn't* finitely generated.

Let $$R$$ be the ring of continuous functions $$f:\mathbb{R}\to \mathbb{R}$$ with the usual pointwise addition and multiplication.  We say that a function $$f\in R$$ has bounded support if there is a real number $$M>0$$ such that

$$|x|>M\implies f(x)=0$$

1. Prove that the subset $$I\subset R$$ of functions with bounded support is an ideal of $$R$$.
2. Prove that $$I$$ is not finitely generated.

(3 marks)