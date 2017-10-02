---
layout: bulletin
title: Week 1 Bulletin - Rings and homomorphisms
comments: true
---

General overview
-----
This week a lot of time was spent covering the philosophy of the course (which is slightly different than what you've used to) and administrative matters.

Content wise, we reviewed the definition of a ring and many examples in the first lecture.

In the second, we began by introducing three types of elements, and the corresponding three types of ring:

* a *field* is a ring in which every nonzero element is a *unit*
* an *integral domain* is a ring which has no nonzero *zero divisors*
* a ring is *reduced* if it has no *nilpotent* elements

We then introduced the definition of a homomorphism of a ring (preserves all structure, but you only need to check that it preserves addition, multiplication, and the multiplicative unit), looked at some examples and non-examples, got the idea of the proof that there's exactly one ring homomorphism from the integers $$\mathbb{Z}$$ to any other ring, and got a quick look at isomorphisms.

Slides:
=======
* [Slides Lecture 1](../slides/Lecture1.pdf)
* [Slides Lecture 2](../slides/Lecture2.pdf)

Just note that the administrative side of things took slightly longer than I expected and we were running slow the whole time, so we didn't reach the end of the slides for Lecture 2; we will pick that up next week.

Where we are in the notes
-----
The material in the notes was from Sections 2, 3 and 4, though we didn't cover everything.  I'd particularly like to highlight Lemma 3.8 and Example 3.9 at the end of Section 3, which tell us when $$\mathbb{Z}/n\mathbb{Z}$$ is a field, an integral domain, and/or reduced.

We will pick up in Week 2 with some more discussion of isomorphism and the definition of an image and kernel of a homomorphism from the end of Section 4.

General remarks on pace
-------------

The first few sessions are always a little fast because it should be the most basic review, but I did feel a little harried week one, probably because I spent too long on the administrative part; it should feel like we slow down a bit in the coming weeks.  In particular, I know when I hand back the first homework I'm going to want to have a little time to talk about writing, and we didn't make as far as we expected, so I'm slowing down a little from the roughly 1 Section a day pace the next two weeks.

Thanks to those of you who said it felt a little fast -- in a small class like this, I really value communication like that and will explicitly asking you from time to time.

But I also want to stress again that, perhaps in contrast to what you're used to, I am expecting you to be reading the notes as we go along, perhaps giving them a quick look before lecture, but certainly reviewing them after lecture.  It will probably always feel fast if you do not look at the notes.

Suitcases and lectures vs. notes
--------

Since I spent too long talking about lectures vs. reading in class, I want to highlight something intentionally done different: the discussion that there's one homomorphism from $$\mathbb{Z}$$ to anything.

In Lecture, I posed this as a specific problem: what are the homomorphisms from $$\mathbb{Z}$$ to $$M_3(\mathbb{R})$$; you all quickly came up with one, and then after some thought we came to see why this is the only one -- the identity has to go to the identity, and then preserving addition tells us where all the positive integers had to go, and then preserving inverses tells us where all the negative numbers had to go. We then quickly waved our hands at pointing out the same argument worked for homomorphisms from $$\varphi:\mathbb{Z}\to R$$ for any ring $$R$$.

Compare this to the treatment in the notes, Lemma 4.4 on page 11.  In terms of succintness and rigor it is far better.  But as a trade-off, it's harder to figure out what's going on the first time, harder to develop the intuition from.

The definition of $$f(n)$$ given appears pulled from thin air -- of course, it's developed naturally from the definition of a ring homomorphism, but you couldn't tell that from the way its presented until later in the proof.

Perhaps it's a bit like suitcases: if you want to get your clothes from point A to point B, it's much easier if they're nicely put away and folded and sealed in your bag, but then it's a major effort to change socks: you've got to open the suitcase and dig around to find them sitting on the bottom.

In contrast, if all your clothes are just spread around it's a cinch to find your socks, but if you want to get them all the train you're probably going to be dropping things on the platform.

The notes have all the information you need for the course packed away very neatly; in lectures I intend to open up the case, rooting around and making a big mess, but showing you what you need and getting you comfortable with everything in there.  


