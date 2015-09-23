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
 - residue rings, e.g. ``clock arithmetic'' $$\mathbb{Z}/12\mathbb{Z}$$
 - The ring $$C(I,\mathbb{R})$$ of continuous functions from the unit interval $$I$$ to $$\mathbb{R}$$

Why?
----

The development of ring theory is tied to solutions of *Fermat's Last Theorem*.  Recall that Fermat claimed that $$x^n+y^n=z^n$$ had no solutions with $$x,y,z$$ integers and $$n\geq 2$$.  

Gaussian integers $$\mathbb{Z}[i]$$ 


For more on the history of ring theory, see this [MacTutor page](http://www-history.mcs.st-and.ac.uk/HistTopics/Ring_theory.html)

Algebraic Geometry
------------------

Algebraic geometry studies the zero loci of polynomials; for instance, you know that the set of points in $$\mathbb{R}^2$$ satisfying $$x^2+y^2=1$$ is a circle.  

An example you might not be as familiar with is the set of points in $$\mathbb{C}^2$$ satisfying $$z^2=x^3-x$$ -- it turns out that this looks like the surface of a donut with a point missing.

The usual set-up in algebraic geometry is to take a field $$\mathbb{k}$$, and $$f_1, f_2,...,f_n$$ polynomials in $$m$$ variables, and consider $$V(f_1, f_2,...f_n)$$ the set of points in $$k^m$$ where all the $$f_i$$ are zero.  These zero sets are called affine varieties.

Connection
----------

It may seem that the two topics of commutative algebra and algebraic geometry, as described above, are completely unrelated.  But one of the key points of algebraic geometry is to study a variety $$X$$ by studying the ring of polynomial or rational functions on it.  

Modern algebraic geometry, developed largely by Grothendieck, takes this further, and views more general rings as though they *were* rings of functions on a space $$X$$.  Ideas in this vein were crucial to Wiles' proof of Fermat's last theorem.




