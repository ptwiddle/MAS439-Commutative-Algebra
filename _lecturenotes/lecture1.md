---
layout: lecture
title: Lecture 1&#58; Introduction
comments: True
---

Introduction / Motivation
=========================

*Commutative Algebra* is the study of commutative rings.  Roughly speaking, a ring a ring is a set with two operations, addition (written +) and multiplication, (written * or by juxtaposition) that behave like addition and multiplication that we are familiar with.   

Examples
--------

You are already familiar with many different rings:

 - the integers $$\mathbb{Z}$$
 - the rational numbers $$\mathbb{Q}$$
 - the real numbers $$\mathbb{R}$$
 - the complex numbers $$\mathbb{C}$$
 - Polynomials in any number of variables over any of the above, e.g. $$\mathbb{Z}[X], \mathbb{C}[x,y,z]$$
 - residue rings, e.g. *clock arithmetic* $$\mathbb{Z}/12\mathbb{Z}$$
 - The *Gaussian integers* $$\{a+bi\subset \mathbb{C} \text{ with } a,b\in\mathbb{Z}\}$$
 - The ring $$C(I,\mathbb{R})$$ of continuous functions from the unit interval $$I$$ to $$\mathbb{R}$$, with ``pointwise'' addition and multiplication:

$$(f+g)(x)=f(x)+g(x)$$

$$(f\cdot g)(x)=f(x)\cdot g(x)$$ 



 
Why rings?  Number Theory
----

One of the major forces driving the initial study of rings was *Fermat's Last Theorem*.  Around 1630, Fermat claimed that $$x^n+y^n=z^n$$ had no solutions with $$x,y,z$$ positive integers and $$n\geq 2$$, but didn't give a proof, although he was able to prove it for $$n=4$$ easily.    

Lamé proved Fermat's last theorem for $$n=7$$, and claimed in 1847 that he could prove it for all $$n$$, and sketched the proof.  The main idea was the following: if we allow ourselves certain complex roots of unity, then we can factor both sides of Fermat's last theorem into linear factors.  For example, if $$w\in \mathbb{C}$$ is a cube root of unity $$w^3=1$$, then we have

$$a^3+b^3=(a+b)(a+wb)(a+w^2b)$$

Then if $$a^3+b^3=c^3$$ was a solution to Fermat's last theorem, then we would have two different factorizations of $$c^3$$.  If factorizations were unique, then this would give very strong constraints on $$a, b, c$$, that hopefully would lead to there being no solutions.  This strategy, in fact, works for $$n=3$$.

However, it turns that when we add certain roots of unity to the integers, there is no longer unique factorizations into primes -- Kummer had already published an example of this in 1844, and introduced  *ideal complex numbers* (the precursor to ideals) to fix some cases of this in 1846.  Using these ideas, Kummer was able to prove Fermat's last theorem for all $$n<100$$ except for 37, 59, 67, and 74.  Some people suspect that Fermat's `proof' is something similar to Lamé's idea.

For more on the history of ring theory, see this [MacTutor page](http://www-history.mcs.st-and.ac.uk/HistTopics/Ring_theory.html)

Why rings?  Algebraic Geometry
------------------

At its most basic, algebraic geometry is the study of the shapes of zero loci of polynomials.  For example, the set of points in $$\mathbb{R}^2$$ satisfying $$x^2+y^2=1$$ is a circle.  

An example you might not be familiar with is that set of points in $$\mathbb{C}^2$$ satisfying $$z^2=x^3-x$$ is a torus (surface of a donut) with one point missing.

More formally, let $$\mathbb{k}$$ be a field, and $$f_1, f_2,...,f_n$$ polynomials in $$m$$ variables  $$x_1,\dots, x_m$$.  Consider  the set of points  $$a=(a_1,\dots, a_m)\in k^m$$ where all of the $$f_i$$ are zero -- that is, $$f_i(a)=0$$ for all $$i$$.  Such a set is denoted $$V(f_1,\dots, f_n)$$, and is called an *affine varieties* and is denoted $$V(f_1, f_2,...f_n)$$.  Studying these sets is the starting point of algebraic geometry.

Connection
----------

It may seem that the two topics of commutative algebra and algebraic geometry, as described above, are completely unrelated.  But one of the key points of algebraic geometry is to study an affine variety $$X=V(f_1,f_2,\dots, f_n)$$ by studying the ring of polynomial functions on it.  One of our main results, Hilbert's *Nullstellensatz*, will describe the ring in terms of the polynomials $$(f_1,\dots, f_n)$$ that cut $$X$$ out.


$$
\begin{array}{cc} \text{Geometry} & \text{Algebra} \\
\hline
X & \text{ring of functions on } X
\end{array}
$$






 

Modern algebraic geometry, developed largely by Grothendieck, takes this further, and views more general rings as though they *were* rings of functions on a space $$X$$.  Ideas in this vein were crucial to Wiles' proof of Fermat's last theorem.




