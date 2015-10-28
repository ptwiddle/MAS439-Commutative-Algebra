---
layout: lecture
title: Lecture 9&#58; Categories, universal properties
Comments: True
---
 
We ended Lecture 8 quickly introducing the universal property of the quotient ring $$R/I$$.  Universal properties are an example of categorical thinking; in this section we briefly introduce categories, and universal properties.

Tom's notes from last year do not contain much material on categories.  Much of what we will do is standard; for instance, some of this material is covered in the module on algebraic topology, see Section 5.3 of the notes <a href="http://greenlees.staff.shef.ac.uk/mas435/AlgTop15Chapters45.pdf"> here</a>.


Categories
-----

A category consists of objects, and maps between objects that you can compose.  The most basic example is where your objects are sets, and the maps between them are functions.

Definition
====

A *category* $$\mathcal{C}$$ consists of 

 - a collection of object $$\textrm{Ob}(\mathcal{C})$$

 - For each pair of objects $$A,B\in\textrm{Ob}(\mathcal{C})$$ a set of morphisms (or maps, or arrows) $$\textrm{Hom}_{\mathcal{C}}(A,B)$$ 

 - A binary operation $$\circ$$ called composition of morphisms

$$\circ:\textrm{Hom}(B,C)\times\textrm{Hom}(A,B)\to\textrm{Hom}(A,C)$$
$$(g,f)\mapsto g\circ f$$

<a href="http://presheaf.com/?d=d2b626v35h5k127024635391e33e49"><img src="http://presheaf.com/cache/d2b626v35h5k127024635391e33e49.png" title="click to go to presheaf.com for editing"/></a>

 - For each object $$A\in\textrm{Ob}(\mathcal{C})$$ an identity morphism $$1_A\in\textrm{Hom}_{\mathcal{C}}(A,A)$$
 
Satisfying:

 - Composition of morphisms is associative:
  $$(f\circ g)\circ h=f\circ (g\circ h)$$
whenever $$f,g,h$$ are morphisms where this is defined; i.e., when
$$h\in \mathrm{Hom}(A,B), g\in \mathrm{Hom}(B,C), h\in \textrm{Hom}(C,D)$$
 - The identity morphisms act as identities: for $$f\in \textrm{Hom}(A,B)$$, we have 

$$1_B\circ f=f=f\circ 1_A$$

Examples
----
Perhaps the most important example 

Most important example: sets
===

The category $$\mathbf{Set}$$, whose objects are sets, and where $$\textrm{Hom}(A,B)$$ is the set of functions from $$A$$ to $$B$$.

Many important examples built on this -- the objects in these categories will be sets with some kind of extra struction, and the morphisms will be functions between the sets that somehow ``preserve'' that structure.

Examples: sets with extra structure
====
 - The catgory $$\textbf{Grp}$$ whose objects are groups, and whose morphisms are group homomorphisms.
 - The category $$\mathbf{Ring}$$ whose objects are rings, and whose morphisms are ring homomorphisms.
 - For $$k$$ a field, the category $$\mathbf{Vect}_k$$, whose objects are vector spaces over $$k$$, and whose morphisms are $$k$$-linear maps
 - The category $$\mathbf{Top}$$, whose objects are topological spaces, and whose morphisms are continuous maps  
 - The category $$\mathbf{Ab}$$, whose objects are abelian groups, and whose morphisms are group homomorphisms

Not every example is of this type.

Examples: Categories with one obect
===

Suppose $$\mathcal{C}$$ is a category with just one object $$C$$.  Then the only  data of the category is the set of morphisms $$\mathrm{Hom}(C,C)$$.   Since all arrows have the same source and target, we can compose any two morphisms; this composition is associative, and has an identity.  Hence $$\mathrm{Hom}(C,C)$$ is a *monoid*.

Similarly, given any monoid $$M$$, we can construct a category with one object by declaring $$\textrm{Hom}(C,C)=M$$.

If, $$\mathcal{C}$$ is a category with one object, and furthermore we have that every morphism is an isomorphism, then every element of $$\textrm{Hom}(C,C)$$ has an inverse, and so this set is a group.



Philosophy
----

One reason category theory is useful is to study maps between categories them -- functors.  We will get to that later.  

For now, we will focus on a more philosophical reason; category theory as a way of thinking.  This philosophy is to understand an object in your category by how it relates to other objects in your category.  Roughly speaking, if you understand the maps into (and/or out of) an object in your category, you should understand the object.  This is sort of a functional way of thinking -- understanding an object based on what it does.

In the homework this week, we will see ways of thinking about injections and surjections of sets without talking about elements of the sets.  Universal properties are another example of this way of thinking.



Definition
====

A morphism $$f:A\to B$$ is an *isomorphism* if there exists a morphism $$g:B\to C$$ with $$g\circ f=1_B$$ and $$f\circ g=1_A$$.

Remark
===

For sets, the notion of isomorphism is that of a bijection.  For groups, rings, vector spaces, topological spaces, this notion of isomorphism gives exactly the standard definitions.

Universal Properties
====

An object $$A$$ has a universal property if it is defined in terms of maps in and out of it.  

Definition: Universal property of products
====

Let $$A,B\in \textrm{Ob}(\mathcal{C})$$.  The *product* of $$A$$ and $$B$$, sometimes denoted $$A\times B$$, is an object $$C\in \mathcal{C}$$, together with two maps $$\pi_1:A\times B\to A$$ and  $$\pi_2:A\times B \to B$$, satisfying the following universal property:

For any object $$C\in\textrm{Ob}(\mathcal{C})$$, and pair of morphisms $$f:C\to A$$ and $$g:C\to B$$, there is a unique morphism $$h:C\to A\times B$$ making the following diagram commute:



<a href="http://www.presheaf.com/?d=d2v5p2pd646sk2s1h531dd2k3ec"><img src="http://presheaf.com/cache/d2v5p2pd646sk2s1h531dd2k3ec.png" title="click to go to presheaf.com for editing"/></a>

It is not hard to check that for the category of sets, the usual definition of $$A\times B$$ satisfies the universal property given above.

For a given category $$\mathcal{C}$$, and two objects $$A, B$$, an object $$A\times B$$ satisfying this universal property may or may not exist.  However, if they exist, objects satisfying a universal property are almost always unique up to unique isomorphism for tautological reasons.

We illustrate this now with the product.

Lemma
====
Products are unique up to unique isomorphism. More explicitly, suppose that $$A, B\in\textrm{Ob}(\mathcal{C})$$ are arbitrary elements, and $$X$$ and $$Y$$ were two objects that each satisfied the universal property of $$A\times B$$, with structure maps $$\pi_i^X$$ and $$\pi_i^Y$$.  

  Then there are unique isomorphisms $$\varphi:X\to Y$$ and $$\psi:Y\to X$$ that commute with the projection maps.

Proof
===

Let us first construct maps $$\varphi:X\to Y$$ and $$\psi:Y\to X$$ that commute with the projection maps.

Since $$Y$$ satisfies the universal property of $$A\times B$$, to give a map $$\varphi:X\to Y$$ is the same as giving maps $$f:X\to A$$ and $$g:X\to B$$.  But since $$X$$ satisfies the universal property of $$A\times B$$, and $$X$$ comes with maps $$\pi_1^X:X\to A$$ and $$\pi_2^X:X\to B$$.  Applying the universal property of $$Y$$ to these maps out of $$X$$ gives us a unique map $$\varphi:X\to Y$$ making the following diagram commute:

<a href="http://www.presheaf.com/?d=d5si252i4502q44394732rn4z471c"><img src="http://presheaf.com/cache/d5si252i4502q44394732rn4z471c.png" title="click to go to presheaf.com for editing"/></a>

Switching the roles of $$X$$ and $$Y$$ in the above argument, similarly we construct a unique map $$\psi:Y\to X$$ that makes the following diagram commute:

<a href="http://www.presheaf.com/?d=d4c5w5h4l6h530314i4i5h5t2p294313"><img src="http://presheaf.com/cache/d4c5w5h4l6h530314i4i5h5t2p294313.png" title="click to go to presheaf.com for editing"/></a>


We now need to show that the maps $$\varphi$$ and $$\psi$$ we have defined are isomorphisms.  To see, for instance, that $$\psi\circ\varphi=1_X$$, we will use the universal property of $$X$$ one more time.  We begin by looking at the following diagram, made by pasting together the previous two diagrams:

<a href="http://www.presheaf.com/?d=d4g5r251hz163n2586z2v2t142t4i2e"><img src="http://presheaf.com/cache/d4g5r251hz163n2586z2v2t142t4i2e.png" title="click to go to presheaf.com for editing"/></a>

Looking at the outside square and the composition of the two vertical mnaps, we see that the following diagram commutes:

<a href="http://www.presheaf.com/?d=d3ir1u143i1hdk3v02xa26223c"><img src="http://presheaf.com/cache/d3ir1u143i1hdk3v02xa26223c.png" title="click to go to presheaf.com for editing"/></a>

This is exactly the diagram for the universal property of $$X$$, obtained with the maps $$f=\pi_1^X$$ and $$g=\pi_2^X$$.  Thus, we know that $$\psi\circ\varphi$$ is the *unique* such map making the diagram commute.  However, it is immediate that we could get another commutative diagram by putting $$1_X:X\to X$$ in the middle arrow, as such:

<a href="http://www.presheaf.com/?d=d116j6k1n4r4u3m3h6m2u1ni6t446h1i"><img src="http://presheaf.com/cache/d116j6k1n4r4u3m3h6m2u1ni6t446h1i.png" title="click to go to presheaf.com for editing"/></a>

Thus, $$1_X$$ and $$\psi\circ\varphi$$ both make the diagram commute; since $$X$$ satisfies the universal property of $$A\times B$$, there is a unique morphism making the diagram commute, and so we must have $$\psi\circ\varphi=1_X$$.

Interchanging the roles of $$X$$ and $$Y$$ gives that $$\varphi\circ\psi=1_Y.\quad\square$$








