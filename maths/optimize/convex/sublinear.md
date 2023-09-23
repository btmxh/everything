## Linear combination
The linear combination of vectors $v_{1},v_{2},\dots,v_{n}$ wrt weights $w^{1},w^{2}, \dots,w^{n}$ is the vector $v_{i}w^{i}$ (Einstein notation).
Now, let $v$ be the matrix with $v_{1},v_{2},\dots$ be its column, then the matrix-vector product $vw$ is the matrix form of a LC.

## General definition
A sublinear combination of vectors $v_{1}, v_{2},\dots,v_{n}$ wrt weights $w^{1},w^{2},\dots,w^{n}$ is the linear combination $v_{i}w^{i}$, but this is only defined if the weight vector $w$ satisfies certain conditions.
- Linear combination is the sublinear combination with condition $w\in F^{n}$ (for scalar field $F$)
- Cone combination is the sublinear combination with condition $w\geq 0$
- Affine combination is the sublinear combination with condition $\sum w^{i}=1$
- Convex combination is a sublinear combination that is both "conical" and "affinic"

A sublinear space is a space that is closed under a certain sublinear combination operation.
e.g. Linear spaces (traditionally vector spaces), cone space (or simply cones), affine spaces, convex spaces (or convex sets), etc.

The sublinear hull of a set $S$ is the minimal (i.e. the intersection of all) sublinear spaces containing $S$. Sublinear hulls are 

Vectors $v_{1},v_{2},\dots,v_{n}$ are sublinearly independent iff the only sublinear combination of the zero vector corresponding to the zero weight vector. Sublinearly independent is not defined when $w=0$ does not satisfy the sublinear condition.

## Properties
- All sublinear spaces are a subset of the linear span of its element, which is called their **corresponding linear space**.
	- The dimension of a sublinear space is defined to be equal the dimension of its corresponding linear space.
- All linear spaces are sublinear spaces, but the converse is generally false.
- Cone spaces are closed under non-negative uniform scaling (if $v\in S$ then $kv\in S$ because it's a cone combination of $v$ wrt weight $k$)
- Intersection of all sublinear spaces (of the same kind) is another sublinear space (of the same kind). In the different kind case, it's still a sublinear space, but the kind is a completely new kind (weight condition is AND of all weight conditions of the original sublinear spaces).

## Sublinear transformation
Denote $\mathcal{C}(X, w)$ as the sublinear combination function (sublinear combination of $X_{i}$ wrt weights $w$)
A function $f: S\to S'$ is sublinear iff $f(\mathcal{C}(X, w))=\mathcal{C}(f(X), w)$, with:
- $f(X)$ be the matrix gotten from applying $f$ repeatedly to the column vectors of $X$. Note that this is simply an notational expansion of $f$, which does not force $f$ to be linear or something.

>Note: Every linear function is also sublinear.

**Theorem:** Sublinear transformation preserve sublinear spaces (of the same kind)