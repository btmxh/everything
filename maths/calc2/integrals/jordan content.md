> jordan measure mf please shut up

## algebra & content
an algebra is a pair $(X, F)$, where $F$ is a family of subsets over $X$, s.t.
- $X \in F$
- $A\in F \implies X\setminus A\in F$ (closed under complementation)
- $A, B \in F \implies A\cap B \in F$

=> one can easily prove that algebras are closed under any arbitary *finite* expression of intersection, union and complementation

content is kind of a *measure* used on an algebra, **but the word measure is reserved for [[sigma-algebra]]s**.

a content is a map $m$ from $F$ to $[0, +\infty]$ (note the $\infty$) s.t.
- $m(\emptyset)=0$
- $m(A \cup B)=m(A)+m(B)$ for non-intersecting $A, B$

## riemann algebra & jordan content
one can define the riemann algebra simply as the set of all sets $A$ such that $\int _{-\infty}^{\infty} 1_{x\in A} \, dx$ exists, and the jordan content, well, is the value of that integral (bruh)

in $\mathbb{R}^{n}$, one can easily define the multidimensional R-al and J-ct by taking the products

> in some funny university, one adds another condition $\mu(A)=S(A)$ for all box $A$, with area $S(A)$ (wtf bruh this is stupid asf)
> the outer jct is the upper darboux sum, denoted $\mu^{*}$, but can also be defined as $\mu^{*}(A)=\inf_{A \subset S}\mu(S)$, with $S$ being a simple set (join of finitely many boxes), or $\mu^{*}(A)=\inf\left\{  \sum_{k=1}^{n} S(A_{k}), A \subset A_{1}\cup A_{2}\cup\dots \cup A_{n}  \right\}$
> the inner jct can be defined similarly, BuT they instead define $\mu_{*}(A)=S(\Delta)-\mu^{*}(\Delta\setminus A)$, for some box $\Delta$ that fully contain $A$
> set $A$ is measurable (or contentable idk) by jct iff $\mu^{*}(A)=\mu_{*}(A)$, and this value is $\mu(A)$, its jordan content
> the set of all jct measurable set form an **algebra**

## rigor
### uniqueness of inner jct
to prove that $\mu_{*}(A)$ does not depend on the bounding hyperbox $\Delta$, one prove $\mu_{*}(A)=\inf_{S \subset A, S \text{ simple}} S(S)$
### jordan content is a content
- $\mu(\emptyset)=0$
	- this is true, because one can always u