---
title: Problem Set 3
duedate: 19th October
layout: default
---


Question 1: Rings with 4 elements (6 marks)
===
We already know three rings with four elements: $$\mathbb{Z}/4$$ and $$\mathbb{Z}/2\times\mathbb{Z}/2$$  being the easy two; in class we constructed a third, $$\mathbb{F}_4=\mathbb{Z}/2[x]/(x^2+x+1)$$.

In addition to $$x^2+x+1$$, there are three more quadratic polynomials in $$\mathbb{F}_2[x]$$ ($$\mathbb{F}_2$$ is just what we write for $$\mathbb{Z}_2$$ when we want to emphasize it's a field):

$$ f_1=x^2,\quad f_2=x^2+x,\quad f_3=x^2+1$$. 

 Prove that each of the rings $$R_i=\mathbb{F}_2[x]/(f_i)$$ has four elements.  Write down the multiplication tables for each of the rings $$R_i$$.  Are the $$R_i$$ reduced?  Integral domains?  Fields?  Which of the $$R_i$$ are isomorphic to each other, and which are not?  Which ones are isomorphic to one of the three rings with 4 elements we already knew, and which are not?

Completely optional challenge (i.e., for biscuits, not points): Prove that we've constructed every ring with four elements.


Question 2: Eisenstein integers (2 marks)
===

Let $$\omega=e^{2\pi i/3}=(-1+i\sqrt{3})/2$$.  

Let $$S=\langle\omega\rangle \subset \mathbb{C}$$ be the subring of $$\mathbb{C}$$ generated by $$\omega$$.  

Let $$R=\mathbb{Z}[x]/(x^2+x+1)$$.  

We claimed briefly in an early lecture that these two rings are isomorphic.  I want you to carefully justify that statement i.e. to prove that $$S\cong R$$.

It's certainly possible to do this "by hand", but I want you to use some of the machinery from class (for practice, and because it should make it easier).  Specifically, construct a homomorphism $$\varphi:\mathbb{Z}[x]\to\mathbb{C}$$ with $$\textrm{Im}(\varphi)=S$$ and $$\ker(\varphi)=(x^2+x+1)$$.  Then apply the first isomorphism theorem to $$\varphi$$.  Make sure you prove $$\varphi$$ has all the desired properties...


Question 3: Getting our hands dirty (2 marks)
====

So far, when we've worked with a quotient ring $$R/I$$, we've either gotten distinct representatives of each equivalence class by using the division algorithm, or we've side-stepped the issue of finding distinct representatives entirely and used the isomorphism theorem to describe $$R/I$$ instead.  The point of this question is that the above methods shouldn't work, and so you are forced to actually think about how to find distinct representatives "by hand". 

Your task is to describe the quotient ring $$\mathbb{Z}[x]/(2x-1)$$.  Specifically, find a "nice" description of unique representatives of each equivalence class, and describe how to add and multiply your representatives.  Note that we can't use the division algorithm as we have in our previous examples.

This is a little vague, so it may help to *think* in terms of Question 2: $$\mathbb{Z}[x]/(2x-1)$$ is isomorphic to a certain subring $$S\subset \mathbb{Q}$$.  Proving this using the isomorphism theorem as in Question 2 is a bit subtle and not recommended.  But if you figure out what this subring $$S$$ "should be", it will help you find a system of representatives and "what's really going on" when you add and multiply these representatives.  

In particular, a good answer to this question will make clear "by hand", (that is, straight from the definition, not using the isomorphism theorem or other complicated machinery) that $$\mathbb{Z}[x]/(2x-1)$$ is isomorphic to a particular subring of $$\mathbb{Q}$$.
