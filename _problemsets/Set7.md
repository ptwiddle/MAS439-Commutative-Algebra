---
title: Problem Set 7
duedate: November 23rd
layout: default
---
Question 1 The Nullstellensatz in dimension one. (3 points)
===
Recall that $$r$$ is a root of a polynomial $$f$$ if $$f(r)=0$$; a field $$k$$ is algebraically closed if every nonconstant polynomial $$f\in k[x]$$ has a root $$r\in k$$.

1. Prove that if $$k$$ is algebraically closed, and $$f\in k[x]$$, then $$f$$ factors completely into linear factors $$f=a(x-r_1)(x-r_2)\cdots(x-r_n)$$.
2. Prove the Nullstellensatz in dimension 1: if $$k$$ is algebraically closed and $$I\subset k[x]$$, then $$I(V(I))=\sqrt{I}$$.



Question 2 Doing a difficult question right (4 points)
=======

The last problem set asked you to show that $$x-y\notin (x^2+y^2-2, xy-1)$$, which was a difficult question.  Many of you argued that this isn't possible since the generators have no linear terms; this argument is not sufficient because since $$x^2+y^2-2$$ has a constant term, we can get an $$x-y$$ by multiplying it by $$-1/2(x-y)$$.  The result will have higher order terms, but maybe these could be cancelled with other terms.  We first give an example where this happens, to show the naive argument is not sufficient:

Part 1: Show that $$x-y\in (x^2+y^2-2, x^2-y^4, x^3-y^5)$$, in fact:

$$x-y=f(x,y)(x^2+y^2-2)+g(x,y)(x^2-y^4)+h(x,y)(x^3-y^5)$$

where:

$$f(x,y)=\frac{1}{4}(-xy^2+y^3-2x+2y)$$

$$g(x,y)=\frac{1}{4}(-y^3-x-2y)$$

and you need to find $$h(x,y)$$.

Part 2. We outline a careful proof that $$(x-y)\notin (x^2+y^2-2, xy-1)$$, motivated with some geometric intution.  First, show that $$x+y=2$$ is the tangent line to both $$x^2+y^2-2$$ and $$xy-1$$ at $$(1,1)$$.

Now, observe that if $$(x-y)=2z$$ (the two is for convenience), and $$x+y=2$$, then $$x=z+1$$ and $$y=1-z$$; making these change of variables should make our picture "look like" the nonradical ideal $$(z^2)$$.

Part 3.  Finally, prove $$(x-y)\notin (x^2+y^2-2, xy-1)$$ as follows: suppose that we have $$x-y=f(x,y)(x^2+y^2-2)+g(x,y)(xy-1)$$, apply the homomorphism $$\varphi:k[x,y]\to k[z]$$ defined by $$\varphi(x)=z+1, \varphi(y)=z-1$$, and obtain a contradiction.

Bonus for fun: prove that $$(x-y)\in (x^2+y^2-2, x^3-y^5, y^3-x^5)$$.  You do *not* want to try to do this by hand; this problem is an excuse to take a look at a computer algebra system like Sage.


Question 3 A reducible algebraic set (3 points)
====

Let $$I=(x^2-yz, xy-zw)$$.  By considering the cases $$z=0$$ and $$z\neq 0$$, prove that $$V(I)=V(x,z)\cup V(x^2-yz, xy-zw, y^2-xw)$$.  Then show that $$V(x,z)$$ and $$V(x^2-yz, xy-zw, y^2-xw)$$ are both proper subsets of $$V(I)$$ by finding points that are in one but not the other.