---
title: Problem Set 5
duedate: 2nd November
layout: default
---

Introduction
======
Completing the exercises this week does not require category theory at all.  However, the result they build to is best understood as something about the functor $$\textbf{Fun}_k:\textbf{Set}\to k\textbf{--alg}$$, in particular that it is *full*; so we discuss this briefly as motivation.

A functor $$F:\mathcal{C}\to\mathcal{D}$$ is called *full* if it is surjective on the sets of morphisms; it is called *faithful* if it is injective on the set of morphisms.

More precisely, let $$F$$ be a contravariant functor from $$\mathcal{C}\to\mathcal{D}$$.  For any two objects $$A,B$$ of $$\mathcal{C}$$, the functor $$F$$ gives a function from $$Hom_{\mathcal{C}}(A,B)\to Hom_{\mathcal{D}}(F(B), F(A))$$.  We say $$F$$ is full if this map is surjective for every $$A, B$$, and we say $$F$$ is faithful if this map is injective for every $$A, B$$.  

It turns out that being an isomorphism of categories is far too strong, the right notion of two categories being "the same" is called an equivalence of categories.  Any reasonable notion of a functor $$F$$ as being an equivalence should require it to be full and faithful; it turns out there's just one more condition.


Question 1: Collecting some lemmas (6 marks)
===
Let $$X$$ be a finite set, and $$k$$ an integral domain.  Then $$\textrm{Fun}(X, k)$$, the set of functions of $$X$$ to $$k$$, is an $$k$$-algebra, with pointwise addition and multiplication, and structure map $$\varphi:k\to\textrm{Fun}(X,k)$$ the inclusion of $$k$$ as the constant functions.

An *idempotent* in a ring $$R$$ is an element $$e\in R$$ s.t. $$e^2=e$$.  A set of idempotents $$e_1,e_2, \dots, e_n$$ are *orthogonal* if $$e_i\cdot e_i=0_R$$ for $$i\neq j$$.  A set of orthogonal idempotents $$e_1,e_2,\cdots, e_n$$ is called *complete* if $$\sum e_i=1_R$$.


1. Prove that an element of $$\textrm{Fun}(X,k)$$ is idempotent if and only if it is the characteristic function of a subset of $$X$$.  Recall that if $$S\subset X$$, the characteristic function $$\chi_S(x)$$ is given by $$\chi_S(x)=1_k$$ if $$x\in S$$ and $$\chi_S(x)=0_k$$ if $$x\notin S$$.

2. Prove that a set of idempotents $$\chi_{S_i}$$ in $$\textrm{Fun}(X,k)$$ are orthogonal if and only if the subsets $$S_i$$ are disjoint.

3. Prove that an orthogonal set of idempotents $$\chi_{S_i}$$ in $$\textrm{Fun}(X,k)$$ is complete if and only if the union of the $$S_i$$ is $$X$$.


Question 2: Classifying algebra maps between $$\textrm{Fun}(X,k)$$. (4 marks)
===

Again, assume $$k$$ an integral domain.  Let $$f:X\to Y$$ a map between finite sets.  We define a map $$f^*:\textrm{Fun}(Y,k)\to \textrm{Fun}(X,k)$$ by $$f^*(g)=g\circ f$$; that is, the value of $$f^*(g)$$ on a point $$x\in X$$ is $$g(f(x))$$.  In lecture, we called this map $$\textbf{Fun}(f)$$.  


1. Prove that $$f^*$$ is a morphism of $$k$$-algebras.

2. Prove that every $$k$$-algebra morphism from $$\textrm{Fun}(Y,k)$$ to $$\textrm{Fun}(X,k)$$ is of the form $$f^*$$ for some $$f:X\to Y$$.  (Hint: This question is the hard one.  Suppose we have some $$k$$-algebra homomorphism $$\varphi:\textrm{Fun}(Y,k)\to\textrm{Fun}(X,k)$$.  From $$\varphi$$ we need to cook up a function $$f:X\to Y$$ with $$f^*=\varphi$$.  Use Question 1...)

3. Give an example of an integral domain $$k$$, finite sets $$X, Y$$ and a *ring* homomorphism $$\textrm{Fun}(Y,k)$$ to $$\textrm{Fun}(X,k)$$ that is *not* of the form $$f^*$$ for any $$f:X\to Y$$.  (Hint: Maybe take $$X$$ and $$Y$$ to each be a point, and $$k=\mathbb{C}$$, and you may have an example at hand...)

