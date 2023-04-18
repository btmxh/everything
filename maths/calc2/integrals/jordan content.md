> jordan measure mf please shut up

## algebra & content
an algebra is a pair $(X, F)$, where $F$ is a family of subsets over $X$, s.t.
- $X \in F$
- $A\in F \implies X\setminus A\in F$ (closed under complementation)
- $A, B \in F \implies A\cap B \in F$

=> one can easily prove that algebras are closed under any arbitary expression of intersection, union and complementation

content is kind of a *measure* used on an algebra, **but the word measure is reserved for [[sigma-algebra]]s**.

a content is a map $m$ from $F$ to $[0, +\infty]$ (note the $\infty$) s.t.
- $m(\emptyset)=0$
- $m(A \cup B)=m(A)+m(B)$ for non-intersecting $A, B$

## riemann algebra & jordan content
one can define the riemann algebra simply as the set of all sets $A$ such that $\int _{-\infty}^{\infty} 1_{x\in A} \, dx$ exists, and the jordan content, well, is the value of that integral (bruh)

in $\mathbb{R}^{n}$, one can easily define the multidimensional R-al and J-ct by taking the products