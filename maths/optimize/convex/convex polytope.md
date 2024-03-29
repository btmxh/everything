## Hyperplane
A hyperplane is a shape with equation $wx=b, x \in L$ for some linear space $L$. It splits $L$ into two half-spaces: $wx\geq b,x \in L$ and $wx\leq b, x \in L$

## Polytope
Polytopes are shapes that can be formed by combining logic operations (intersection, union) on half-spaces (generated by hyperplanes).

## Convex polytope
A convex polytope is a polytope that is [[convex]].

**Theorem**: A polytope is convex iff it can be represented as the intersection of many half-spaces. (The column vectors)
**Proof**
The intersection of many half-spaces can be represented as the matrix form $Ax\geq b,x \in \mathbb{R}^{n}$, which is convex.
Expanding the logic operations yield the expanded form of the equation as an union of many intersections of half-spaces.
TODO

**Corollary** All convex polytopes can be represented in the form $Ax\geq b,x \in \mathbb{R}^{n}$ ($A$ depends on $n$, but that's irrelevant here)


## Faces
A subset $F$ of the convex polytope (CP) $P$ is called a **face** if for every line segment $[xy] \cap P$ at points other than the endpoints, then $[xy]\subset P$.

**Theorem:** A face of the convex polytope $Ax\geq b,x \in \mathbb{R}^{n}$, has the following form, for indices (ordered) set $I\subset 1..m$ ($m$ is the number of rows of $A$): $Ax\geq b, A_{I}x^{I}=b^{I}, x \in \mathbb{R}^{n}$
**Proof**
- $F: Ax\geq b, A_{I}x^{I}=b^{I},x \in \mathbb{R}^{n}$ is a face
	- If $[yz] \cap F$ at proper convex combination $x$ of $y$ and $z$, then $Ax$ is a convex combination of (and hence bounded by) $Ay$ and $Az$ (component-wise).
	- Then, because $A_{I}x^{I}=b^{I}$, $A_{I}y^{I}\geq b^{I}$ and $A_{I}z^{I}\geq b^{I}$, then we can easily verify that $A_{I}y^{I}=A_{I}z^{I}=b^{I}$, $\blacksquare$
- A face could be expressed in the form mentioned above
	- if $F$ divides $P$ into two parts (not counting the boundary), then one take $y,z$ from the two parts and now $[yz]\cap F$ so both $y,z$ are in $F$, contradiction
	- TODO: generalize this to the affine hull of $F$ => qed
	- we also have $\operatorname{dim}F=n-\operatorname{rank}a^{\dots I}$

## Representation Theorem
**Theorem:** Let $P$ be a convex polytope. Then every $x \in P$ can be represented as the sum of a convex combination of $P$'s extreme points and an affine combination of $P$'s extreme recession directions.

Let $P'$ be the convex hull of $P$'s extreme points. Consider $x \in P$, WLOG assuming $x=0$  and consider the cone $C=\{ x-td,t\geq 0, d \text{ is a recession direction of} P \}$.
If $C$ intersects $P'$, then we are done. Otherwise, using the hyperplane separation theorem, $P'$ and $C$ is separated by the hyperplane $H$. TODO:???