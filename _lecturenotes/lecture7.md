---
layout: lecture
title: Lecture 7&#58; Writing tips.  Quotient rings&#58;  Motivation, definition.
Comments: True
---

Last week we introduced ring homomorphisms and ideals; this week we will show how these concepts are related through the quotient ring.

Writing
----
I spent longer than I meant on this.

General philosophy
====


Writing mathematics is hard; there is a large tension between being *clear* and being *concise*, between actually *communicating* how to think about what's going on to somebody else, and being completely mathematically rigorous and precise.

For example, a standard $$\varepsilon-\delta$$ proof from analysis often begins ``Take $$\delta=\varepsilon^3+\varepsilon/3$$, which is pulled completely out of a magic hat.  But the calculations that follow do completely what was wanted with no extra effort.

You could instead begin a proof by explaining how that choice of $$\varepsilon$$ was reached; but these are often heuristic, intuitive calculations, and then you'd want to append the first proof *after* this to be precise, but that gets long.  

You could try to write it so that your deduction of the value of $$\varepsilon$$ was itself also a rigorous proof that it works, but this is often tricky to do in a way that makes sure you aren't assuming what you were trying to do.

The point is you should be thinking about these things, especially as you're writing your fourth year projects.  When to give intuitive "this is what's going on" things, which details of proofs you need to spell out completely and when you can say something like, "Playing around with the definitions shows", or "By a similar argument, we have".  These questions very much depend on your audience.


Practical tips
===

 - Please restate the question on homework questions
 - Don't use shorthand symbols.  This is for formally written work; these symbols have their place in your notes or scratchwork, or when writing on a board in a lecture, for instance.  

For example, $$\implies$$ to be mean "implies" can usually be replaced with "so" or "and so" or "therefore" or "we see that", etc.  Similarly, just write "exists" or "for all" out instead of using $$\exists$$ and $$\forall$$.

When using $$\implies$$ to denote which half of an equivalence you are proving, write out which half of the equivalence are proving.  i.e., "We first prove that if $$a_0$$ is a unit in $$R$$, then $$a_0+a_1x+a_2x^2+\cdots$$ is a unit in the power series ring $$R[[x]]$$".

Note that these first two suggestions make things less concise, but they do improve clarity; for instance, if both of these are skipped, then you wind up with solutions that begin:

> Question 2: Let 
>
> $$b=b_0+b_1x+b_2x^2+\cdots$$ 
>
> where
>
> $$b_n=-b_0\sum_{k=1}^n a_kb_{n-k}$$ 
>
> Then ...

Here the reader has no clue what's going on because we've jumped straight into the middle of things.  

 - Avoid case by case analyses when they are unnecessary.  There was a lot of this on the last homework.  Sometimes this makes it feel like you're being more clear -- in a way, you're illustrating more examples.  But if all the cases really work the same way, you're being *less* clear; you're making it look like they behave differently, but really the same thing is happening.  You're certainly making things less concise.

In a way, this is exactly what the abstract method in mathematics is all about.  A good abstract definition (like commutative rings, for instance) shows that things that look differend (number rings, polynomial rings) which look different really have a lot in common.  Treating them uniformly is a satisfying way of seeing "what's really going on" as opposed to a long, case by case analysis that can be followed easily but doesn't really add to your understanding.

 - Don't repeat yourself; It's valuable to motivate things and explain your thinking, but when you do this and then immediately go over all the formal details afterwards it gets long.  I may do this in lecture sometimes, but that's a different audience than you writing up homework for me.  If you can work an explanation of "what's really going on" into the details of a formal proof, rather than having one right after the other, that's better all around; if I don't do it in class it's because *it's hard*.





Motivation
-----

We saw last week that if $$\varphi:R\to S$$ was a ring homomorphism, then $$\ker(\varphi)=\{r\in R \text{ such that } \varphi(r)=0\}$$
is an ideal of $$R$$.  The goal of today's lecture is to show that the converse is true:  given $$I\subset R$$ we construct the *quotient ring* $$R/I$$, and a surjective homomorphism $$p:R\to R/I$$ known as the *quotient map*, so that $$\ker(p)=I$$.

To motivate the definition, let's think about what $$R/I$$ would have to look like.  There is supposed to be a surjective map $$p:R \to R/I$$, so that means we can write any element of $$R/I$$ as $$p(a)$$, for some $$a \in R$$.  But such an $$a$$ need not be unique -- for instance, since $$I$$ is the kernel of $$p$$, we have that $$p(a)=0_{R/I}$$ for any $$a\in I$$.  

We will build $$R/I$$ out of $$R$$, so we can represent any element of $$R/I$$ as an equivalence class of elements of $$R$$ -- namely, element $$a\in R/I$$ will be represented by the set $$p^{-1}(a)$$.  Put another way, two elements will be equivalent if they map to the same thing under $$p$$:  $$a\sim p$$ if and only if $$p(a)=p(b)$$.

So when does $$p(a)=p(b)$$?  Well, this is equivalent to $$p(a-b)=0$$, i.e., that $$a-b$$ is in the kernel of $$p$$, which we are supposing is $$I$$.  So, we see that $$p(a)=p(b)$$ if and only if there is an $$r\in I$$ with $$a=b+r$$.

Addition and multiplication on $$R/I$$ are fixed by the fact that $$p$$ is a surjective homomorphism; if $$x,y$$ are two elemetns of $$R/I$$, write $$x=p(a), y=p(b)$$.  We must have:

$$x+y=p(a)+p(b)=p(a+b)$$ since $$p$$ is a homomorphism.  

Definition
-----

Thus, we are lead to:

Definition / Lemma
====

Let $$I\subset R$$ be an ideal.  The *quotient ring* $$R/I$$, as a set consists of equivalence classes for the relation $$x\sim y$$ if $$x-y\in I$$.  If $$x\in R$$, we denote the equivalence class containing $$x$$ by $$[x]$$.  Then we define addition and multiplication on $$R/I$$ by:

$$[x]+[y]=[x+y]$$

$$[x]\cdot[y]=[x\cdot y]$$

Then $$R/I$$ is a ring, with $$0_{R/I}=[0_R]$$ and $$1_{R/I}=[1_R]$$.

Furthermore, the map $$p:R\to R/I$$ defined by $$p(x)=[x]$$ is a surjective ring homomorphism with kernel $$I$$.

Proof
====

We should check that $$\sim$$ is an equivalence relation, that the $$+$$ and $$\cdot$$ operators on $$R/I$$ are well defined and satisfy the ring axioms, and that $$p$$ is well defined and is a surjective group homomorphism.   

First, we show $$\sim$$ is an equivalence relation.  

1. Reflexive: $$x\sim x$$ as $$x-x=0\in I$$, since any ideal contains $$0$$.
2. Symmetric: $$x\sim y$$ implies $$y\sim x$$, since $$y-x=-(y-x)\in I$$, since $$y-x\in I$$ and ideals are closed under multiplication by arbitrary elements of $$R$$ (here, -1).
3. Transitive: $$x\sim y$$ and $$y\sim z$$ imply $$x\sim z$$, since $$x-z=(x-y)+(y-z)\in I$$ since $$(x-y)$$ and $$(y-z)$$ are both in $$I$$ and $$I$$ is closed under addition.

Note that, although we proved number 2 using multiplication, we have really only used group theory; $$I$$ is a subgroup, and $$(x-y)$$ and $$(y-x)$$ are additive inverses of each other.

In particular, the equivalence classes of $$\sim$$ are exactly the cosets of $$I$$ in $$R$$, and sometimes the equivalence class $$[x]$$ is written $$x+I$$.

Addition and multiplication in $$R/I$$ as stated appear to depend on representatives $$x$$ of an equivalence class; we now show that they don't really depend on this choice; that is, that addition and multiplication on $$R/I$$ are well defined.

Suppose that $$x^\prime, y^\prime$$ were different representatives of $$[x]$$ and $$[y]$$; that is, $$x^\prime=x+i, y^\prime=y+j, i,j\in I$$.  Then we have

$$[x^\prime]+[y^\prime]=[x^\prime+y^\prime]=[x+i+y+j]=[x+y+(i+j)]=[x+y]$$

as since $$i,j\in I$$, and $$I$$ is an ideal, so is $$(i+j)$$.

Similarly, we have

$$[x^\prime]\cdot[y^\prime]=[x^\prime\cdot y^\prime]=[(x+i)\cdot(y+j)]=[x\cdot y+(x\cdot j+y\cdot i+ij)]=[x\cdot y]$$
since $$i,j\in I$$ and $$I$$ is closed under addition and under multiplication by arbitrary elements of $$R$$.

Checking the $$R/I$$ satisfies the ring axioms follows mechanically from the fact that $$R$$ satisfies the ring axioms.  For example, to check the distributive property, we have


$$
\begin{eqnarray*}
[a]\cdot\left([b]+[c]\right)&=&[a]\cdot [b+c] \\
&=&[a\cdot(b+c)] \\
&=&[a\cdot b+a\cdot c] \\
&=&[a\cdot b]+[a\cdot c] \\
&=&[a]\cdot [b]+[a]\cdot[c]
\end{eqnarray*}
$$




