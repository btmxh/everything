affine combination is the sublinear combination that requires the sum of the elements in its weight vector to be $1$.

**Theorem:** Affine sets containing the origin is a linear space.

## Parallel linear space
**Theorem:** Affine sets can be represented as the sum of a linear space and a vector: $M=L+a$
**Proof**
- Take $a\in M$, then one can trivially prove that $L=M-a$ is a linear space $\blacksquare$

Hence, affine sets can be thought of as translated vector spaces, which makes **affine transformations** capable of translation (unlike linear transformations).
The linear space $L$ in the above theorem is said to be **parallel** to the affine space $M$. An important thing to note is the fact that $L$ is unique (but $a$ is not). In fact, one can let $L=M-M$
- $M=L_{1}+a_{1}=L_{2}+a_{2}$, then $L_{2}=L_{1}+a$ for $a=a_{1}-a_{2}$. Because the linear spaces are invariant under translation, $\blacksquare$.

**Theorem:** Affine transformations can be written as a linear transformation followed by a translation: $T(x)=Lx+a$
**Proof**
- Let $a=T(0)$, then $T(x)-a$ is a linear transformation, $\blacksquare$.

## Matrix representation
Only considering real vector spaces, then all affine set can be defined using a matrix-vector pair $(A, b)$: $M=\{ x\in \mathbb{R}^{n}, Ax=b \}$
**Proof**
It's trivial that RHS is an affine space.
Consider the affine set $M$ and its corresponding linear space $L$. Take the perpendicular linear space $L^{\perp}$, which is perpendicular to $M$.
Rigorously, $M=L+a$, $L \perp L^{\perp}$, and let $(B_{i})_{i\in 1..n}$ (the column vectors of matrix $B$) be a basis of $L^{\perp}$, then all vectors in $\langle l, B_{i}\rangle=B_{i}^{T}l=0$ for all $l\in L$, then $B_{i}^{T}m=B_{i}^{T}a$ for all $m\in M$.
Hence, $B^{i}m=B^{i}a$ or $Bm=Ba$ for all $m\in M$. Let $A=B$ and $b=Ba$, $M$ is now a subset of RHS.
Now, if $m'\in RHS$, $m'-a$ is in the linear space $Ax=0$. If $m'$ is not in $M$, then $m'-a\notin L$ => $m'-a\in L^{\perp}$, then $Ax>0$ because of obvious reasons.
>Alternatively, one could simply prove like this
>$L=(L^{\perp})^{\perp}=\{ x, B^{i}x=0 \}=\{ x, Bx=0 \}$
>=> $M=\{ x, Bx=Ba=b \}, \blacksquare$

**Corollary**: An affine set is an intersection of finitely many hyperspaces.

Consider the affine set of dimension $n$ that is a subset of $\mathbb{R}^{N}$ ($0<n<N$).
Now, if the affine set is described as $Ax = b$, with $A$ being a $m\times n$-matrix, $x$ and $b$ are $n$-vectors.
Then, $A$ has nullity $n$ and rank $k=N-n$, then one can solve the system and express $k$ coordinates of $x$ as LCs of the remaining $n$ coords. This yields the **Tucker representation** of the given affine set:
$$
x^{n+i}=\alpha^{i}_{j}x^{j}+\alpha^{i}_{0}, i \in 1..k
$$

**Theorem:** Let $L$ be a linear space, then:
- the Tucker representation of $L$ is in the form $x^{n+i}=\alpha^{i}_{j}x_{j}$
- the Tucker representation of $L^{\perp}$ (transposed) is in the form $-x_{j}=x_{n+i}\alpha^{i}_{j}, j\in 1..n$
**Proof**
- Since $0\in L$, then $\alpha^{i}_{0}$ must be $0$
- Split $x=(y,z)$, with $y$ being the first $n$ components and $z$ being the remaining ones, then one now sees that $L$ turns out to be the graph of the linear transformation $f(x)=\alpha x$ (since $z=\alpha y$).
- Now, see [[linear#Orthogonal complement of graph of a linear transformation]], we have $L^{\perp}$ will have the equation $y+\alpha^{T} z=0$, which means that the Tucker representation of $L^{\perp}$ is $-y=\alpha^{T}z$, or $-y^{j}=(\alpha^{T})^{j}_{i}z^{i}$
- Taking the transpose of the above expression: $-y^{T}_{j}=z^{T}_{i}\alpha^{i}_{j}$, which can be expanded into the above form, $\blacksquare$.

>This theorem gave a easy process to convert between Tucker representation of a linear space and its orthogonal complement, which is useful for proving stuff I think.

## Affinely Independence
Since $0$ does not satisfies the weight condition, sublinear independence is not defined for affine spaces. However, one can simply introduce a new definition.

Vectors $x_{0},x_{1},x_{2},\dots,x_{n}$ is AI iff the affine hull of these vectors is $n$-dimensional.

**Theorem:** The definition is equivalent to $(x_{i}-x_{0})_{i\in 1..n}$ is LI
**Proof**
The affine hull of these vectors is $L+x_{0}$ with $L$ being the linear span of $(x_{i}-x_{0})_{i\in 1..n}$, which has dimension $\operatorname{dim} L$. Since $\operatorname{dim} L=n$ iff $(x_{i}-x_{0})_{i\in 1..n}$ is LI, $\blacksquare$.

## Affine primitives
Affine primitives are points (degenerate case), lines, planes and hyperplanes in general.