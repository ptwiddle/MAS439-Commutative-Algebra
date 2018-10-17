---
layout: bulletin
title: Week 3 Bulletin - Quotient Rings
comments: true
---

Marking
----

After handing back the first homework from week 1, it was pointed out to me that I didn't explicitly ask you to justify your answers for parts 1 and 3.  I thought that in a pure maths module this would be obvious, but I was wrong -- for instance, on an exam, a question worth one point would not require justification at all; and most of you haven't had much, if any, pure maths module assessed coursework.

I will add back any points removed for lacking justification on these questions using the copies of the homework I made for the external examainers.  Although these points aren't reflected on the homework I handed back to you, you should be able to figure out how many you'll get added back by my comments, and you can always come and ask to see exactly how many it is.

Special Colloquium
----

I spent some time advertising colloquim and seminars in the department.

the postgraduates here run several seminars / reading groups that could possibly be accessible to you, and that fourth year students have attended in previous years; keep a lookout for them or ask me if you're interested.

Additionally, the pure maths colloquium meets most Wednesdays at 2.  In *theory*, the talks in the colloquium are supposed to be accessible to postrgraduates in any area of pure maths; in *practice* they're often at a much higher level.

However, this weeks colloquium, by Kevin Buzzard, is explicitly supposed to be accessible to undergraduates, is on a topic of very general mathematical interest, and looks to take a bit of a provocative stance.  It's essentially about machine verified proofs -- proofs are supposed to logically flow step by step from basic rules, but writing this out in full detail becomes burdensome for humans to write, and unenlightening for humans to read.  However, without this level of detail, in long complicated proofs it can be difficult to ensure the proof is actually correct.

One potential solution to this is machine verified proofs, where the proof is coded into the computer at an intermediary level -- more rigorous than usual human written proofs, but not completely step by step -- and then the computer fills out the rest of the details and verifies that every single step follows logically.  Kevin Buzzard has begun experimenting with this, including having undergraduates use and work with these languages.

I mentioned two recent or ongoing mathematically controversies that will almost certainly be mentioned and play a background in his talk; I'll link to a pop-math article about each here:

- The Kepler Conjecture, which posits that the densest way to pack three dimensional spheres is the way oranges are stacked in a grocers, was proved by Thomas Hales and his graduate student, using lots of computer calculations, but after much work the referees were unable to verify every single step.  Hales then, with the help of many collaborators, spent several years coding the proof into a machine verifiable form.  Here's an [article about it in the New Scientiest](https://www.newscientist.com/article/dn26041-proof-confirmed-of-400-year-old-fruit-stacking-problem/)
- The ABC conjecture is a number theory conjecture that implies Fermat's Last Theorem.  In 2012, Shinichi Mochizuki posted a series of papers online spanning several hundred pages that calimed to prove the ABC conjecture.  However, his main idea "Inter-universal Teichmueller Theory" were extremely novel and abstract, and he spent less time than usual visiting other mathematicians to explain his work in practice; for many years nobody could really make heads or tails of the proof; there was no specific errors found, but at the same time nobody really knew where the "work" of the proof was happening.  Recently, Peter Scholze, who just won the Fields Medal, posted an article calling a specific gap in the proof.  Here's an [article about it in Quanta Magazine](https://www.quantamagazine.org/titans-of-mathematics-clash-over-epic-proof-of-abc-conjecture-20180920/)

Quotient Rings
----

In class we're going a little slower than one chapter of the notes a day this week, both because students usualy find the concept of quotient rings to be difficult, and because the notes are implicitly starting to use concepts from category theory, and I want to take the time to make this explicit.

So, we spent one lecture motiviating quotient rings, defining them, and proving they were actually a ring, and in the second lecture we looked at several examples of how to actually understand quotient rings, and gave the definition of a category and started to introduce category theory as a philosophy -- that the maps between things were as important, if not *more* important, than the things themselves.  In particular, we tried to spend some time teasing out what the Universal Property of Quotient rings was actually saying.

Category Theory
---

We will slowly develop category theory notions in parallel to the contents of the notes, with the following goal -- Algebraic Geometry, in its name, should relate algebra and geometry, which seem to be two very different things.  Our main result this semester could be vaguely stated that doing a certain kind of algebra is "the same" as doing a certain kind of geometry.  Category theory gives us a way to make this precise -- we will construct functors between algebraic and geometric categories, and these functors will be equivalences.

I wanted to give a few weeks to some accessible readings on category theory now -- as we progress I will give you some specific sources that do exactly what we need, but in the meantime these are extra sources just if you're interested.

Category theory has a reputation for being super pure, abstract, and having nothing to do with the real world.  [Tai-Danae Bradley](https://www.math3ma.com/about) is a PhD student doing applied category theory who has put a lot of work into mathematical exposition; in particular her blog has a lot of posts introducing notions from category theory at a very basic level:

- [What is Category Theory](https://www.math3ma.com/blog/what-is-category-theory-anyway)
- [What is a Category?](https://www.math3ma.com/blog/what-is-a-category)
- [What is a Functor?](https://www.math3ma.com/blog/what-is-a-functor-part-1)
- [What is a Natural Transformation?](https://www.math3ma.com/blog/what-is-a-natural-transformation)

At a slightly higher level of difficulty, [Emily Riehl](http://www.math.jhu.edu/~eriehl/)'s book [Category Theory in Context](http://www.math.jhu.edu/~eriehl/context/) is an excellent introduction to Category Theory that does much more than we'll need (and much that I only barely "know").  The book is published by Dover and hence cheap, and by special arrangement the pdf is available freely and legally online [here](http://www.math.jhu.edu/~eriehl/context.pdf).