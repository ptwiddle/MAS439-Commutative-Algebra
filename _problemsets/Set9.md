---
title: Problem set 9
duedate: December 7th
layout: default
---



Question 1 (7 points): 
====
Let $$k$$ be an algebraic closed field, and let $$X\subset \mathbb{A}^n_k$$ and $$Y\subset \mathbb{A}^m_k$$ be algebraic sets.  Let $$\varphi:X\to Y$$ be a polynomial map and let $$\varphi^*:k[Y]\to k[X]$$ be the corresponding map between coordinate rings.

1. Prove that if $$\varphi$$ is surjective, then $$\varphi^*$$ is injective.
2. Prove that if $$\varphi^*$$ is surjective, then $$\varphi$$ is injective.
3. Show that the converses of parts 1 and 2 don't hold. 
4. If $$V\subset Y$$ is an algebraic subset, prove that $$\varphi^{-1}(V)\subset X$$ is also an algebraic subset.  
5. If $$W\subset X$$ is an algebraic subset, give an example to show that $$\varphi(W)\subset Y$$ need not be an algebraic subset.

**Hints:** Two polynomials are the same if and only if they take on the same value at every point. Two points $$p$$ and $$q$$ are different if and only if there is a polynomial that takes on different values at $$p$$ and $$q$$. For 3 and 5, consider the map $$V(xy-1)\to \mathbb{A}_k^1$$ given by $$(a,b)\mapsto a$$.


Question 2 (3 points):
====
The *nodal cubic* is the algebraic set $$X=V(y^2-x^3-x^2)$$.  

1. Show that the map $$\varphi:\mathbb{A}_{\mathbb{C}}^1\to \mathbb{A}^2_{\mathbb{C}}$$ given by $$\varphi(t)=(t^2-1, t^3-t)$$ lands inside $$X$$.
2. Show that the map $$\varphi$$ is surjective onto $$X$$.  Where does $$\varphi$$ fail to be injective?   
3. Prove that $$X$$ is irreducible.  Using $$\varphi$$ or $$\varphi^*$$ might help...

Note (not necessary to do the problem, but fun and potentially helpful)
----- 

Sketch the real part of $$X$$ (maybe by considering how it's related to the graph of $$y=x^3+x^2$$).

The map $$\varphi$$ has the following geometric interpretation, which may be enlightening.  Consider the line through the origin with slope $$t$$, i.e., $$y=tx$$.  If we restrict $$y^2-x^3-x^2$$ to this line, it will be a cubic polynomial in one variable, and hence have three roots.  The origin will always be a double root, and hence there will be one more root.  Geometrically, this means the line $$y=tx$$ intersects $$X$$ at the origin with multiplicity two, and at one *other* point.  This other point is $$\varphi(t)$$.  
