**general form**: minimize (or maximize) $f(x)$ for $x\in D$

$f$: objective function (obj fn)
$D$: feasible set/constrained set: set of all acceptable solutions

**global optimal sol** (GOS):
- $x^{0}$ optimal iff $f(x^{0})\leq f(x)$ for all $x\in D$
- $x^{0}$ strictly optimal iff above equality only hold iff $x=x^{0}$

if $D$ is a topological space, then one have the concepts of neighborhoods, open, closed, compact sets
>we will only consider $D\subset \mathbb{R}^{n}$ in this subject

then:
**locally optimal sol** (LOS):
- $x^{0}$ locally optimal iff $f(x^{0})\leq f(x)$ for all $x\in D \cap N$ for some neighborhood $N$ of $x^{0}$ (i.e. some open set containing $x^{0}$)
- $x^{0}$ strictly locally optimal iff equality only holds iff $x^{0}=x$

e.g. local and global optimizer sets of
- min $\sin x$, $x\in R$
	- since $\sin x\in[-1,1]$, $\sin x=-1$ iff $x\equiv-\frac{\pi}{2} \text{ (mod } 2\pi)$, then the set $-\frac{\pi}{2}+\mathbb{Z}2\pi$ is the set of all global optimizers, which is infinite => not strict
	- $f(x)=\sin x$ is infinitely-differentiable and $f'(x)=\cos x$ => $f'(x)=0$ iff $x=\frac{\pi}{2}+k\pi$
		- if $k$ is odd then we have the maxima, irrelevant
		- if $k$ is even, then we got the global optimizers
			- these are strict local because one can just take the open ball with radius $r<2\pi$ to make equality happens only when $x=x_{0}$
- min $\sin x+\max\left\{  0, \left\lfloor  \frac{x}{2\pi}  \right\rfloor  \right\}$, $x\in R$
	- when $x\leq0$ we have the same global optimizers (note that the additional term is always nonneg)
		- hence, global optimizer set is the set s.t. the max term is 0 and $\sin x=0$, i.e. $-\frac{\pi}{2}+(1-\mathbb{N})2\pi$
	- the fn is differentiable around every pts except for the discontinuities $x=k2\pi$, and by simple observations, one can trivially check if whether these points are not optimizers, hence, we can just do funny derivative like the prev question => local set is like the above: $-\frac{\pi}{2}+\mathbb{Z}2\pi$
- min $x_{2}$, $|x_{2}|\geq 2$, $x_{1}^{2}+x_{2}^{2}\leq 9$
	- we have $x_{2}\geq-3$ so one can easily get the strict min opt. $x_{1}=0,x_{2}=-3$, which is also a strict local opt.
	- assuming $(x_{1}^{0},x_{2}^{0})$ is a local opt., then we have some cases
		- $x^{0}_{2}=2$, then $x_{1}$ can lie on some range, and to prove this is a local opt., we can see the ball $B(x^{0}, 1)$ contains no point with $x_{2}$ less than 0 => all $x_{2}\geq 2$
			- this thing is not strict becauseu one can always find another $x_{2}=2,x_{1}=\dots$ pt in any neighborhood of $x^{0}$
		- $x^{0}_{2}>2$ and consider the open ball $B(x^{0},\varepsilon)$, let $x_{2}=x_{2}^{0}-\delta\geq2$ and now one need to find $\delta$ s.t. exists $x_{1}$ s.t.
			- $x_{1}^{2}+x_{2}^{2}\leq 9$
			- $\delta^{2}+(x^{0}_{1}-x_{1})^{2}\leq\varepsilon^{2}$
			- let $x_{1}=x^{0}_{1}$, then we need $\delta<\varepsilon$ and the first cond is true because $x_{2}<x^{0}_{2}$ => qed, it's not a local opt.
- min $x_{2}$, $x_{1}x_{2}\leq 0$
	- there is no global opt.
	- if $x^{0}_{2}=0$, then
		- if $x^{0}_{1}=0$, then the combination-of-2-disc-quarter $x_{1}^{2}+x_{2}^{2}\leq\varepsilon,x_{1}x_{2}\leq 0$ always have point with negative $x_{2}$, so not local
		- if $x_{1}^{0}>0$, then the arbitary-close point $(x^{0}_{1}, -\varepsilon)$ is a better solution
		- if $x^{0}_{1}<0$, then one can always take an open ball $B$ not intersecting the $x_{1}=0$ axis, and in that open ball (intersected with $D$), $x_{1}$ has the same negative sign, and therefore $x_{2}\geq 0$ for all $x_{2}$ in the intersection => local opt., not strict because ACP ($x^{0}_{1}-\varepsilon,0$)
	- if $x^{0}_{2} > 0$ then $x^{0}_{1}\leq 0$ => ACP $(x^{0}_{1},x^{0}_{2}-\varepsilon)$ s.t. $\varepsilon<x^{0}_{2}$
	- if $x^{0}_{2}<0$ then $x^{0}_{1}\geq 0$ => ACP ($x^{0}_{1}, x^{0}_{2}+\varepsilon$) s.t. $x^{0}_{2}+\varepsilon<0$

$\operatorname{Argmin}(P)=\operatorname{Argmin}_{x\in D}(f(x))=\operatorname{Argmin}\{ f(x),x\in D \}$ is the set of global sols to the problem (argmax if one talks about the maximization problem)
the lowercase version $\operatorname{argmin}P$ is the element in Argmin iff the Argmin set has only one elem (i.e. strict global opt.)

## convex OP
if the obj fn and the domain (the other names are mouthful af) $D$ is convex, then 
- if $x$ is LOS => $x$ is GOS
- if $x$ is SLOS or $f$ strictly convex => x is the only SGOS
**Proof**
- if $x$ LOS and $x$ is not GOS, then there exists some $x'$ more optimal than $x$, i.e. $f(x')\leq f(x)$, then
	- $f(\operatorname{lerp}(x,x',t))\leq \operatorname{lerp}(f(x),f(x'),t)\leq f(x)$ for all $t\in[0,1]$
	- let $t\to 0$, then $\operatorname{lerp}(x,x',t)$ approaches $x$, which means for all neighborhood of $x$ one can always find a lerp pt that is more optimal than $x$ => contradiction.
- since $x$ LOS => $x$ GOS, if other GOSes exists then take $x'$ as one of such GOS ($x\neq x'$), using the same logic, we find all lerps of $x$ and $x'$ is as optimal as $x$ and $x'$ (i.e. they are GOS), so the segment $[xx']$ is full of LOS => $x$ can't be a SLOS
	- the $f$ strictly convex case: all lerps are now more optimal, instant contradiction
>Note: the domain being convex is used to make sure the lerped points are all in the domain

## condition for minimizers
consider the set $T=f(D)_{+}$ of all $t$ s.t. $t\geq f(x)$ for all $x\in D$
then it's trivial to see that the problem $P: \min_{x\in D} f(x)$ has a global minimizer iff $T$ has a min value, i.e. $\inf T\in T$, or equivalently $T$ is closed and $\inf T \in \mathbb{R}$ (not infinity) (note that $T$ is always in the form $[a, +\infty)$, which is closed)

one can expand the weierstrass theorem into
$D$ compact + $f$ lowersemicont => $P$ has solution
>Lowersemicont: $f(x)-f(x_{0})\geq-\varepsilon$ for all $x\in B(x_{0}, \delta)$ or $\liminf_{x\to x_{0}}f(x)\geq f(x_{0})$

**Proof**
Let $t_{0}=\inf f(D)$, then exists a nontrivial seq converging to $t_{0}$: $f(x_{1}),f(x_{2}),\dots$: $\lim_{ n \to \infty } f(x_{n})=t_{0}$ and $f(x_{i})\geq t_{0}$ for all $i\in Z^{+}$
since $D$ compact, a subset of $(x_{n})$ (denoted $x_{n}$ for $n\in I$) conv to some $x_{0}$, then $f$ lowersemicont => $x_{0}=\lim_{ n \to \infty, n\in I } x_{n}$ => $t_{0} = \lim_{ n \to \infty }f(x_{n})=\lim_{ n \to \infty, n\in I } f(x_{n})\geq \liminf_{ n \to \infty } f(x_{n})\geq f(x_{0})\in D$=> qed

if one replaces $D$ being bounded by the condition of $f$ being **coercive** on $D$: $f(x)\to +\infty$ as $\|x\|\to +\infty$, then the solution also exist

**Proof**
Consider $x_{0}\in D$, then the lowerlevelset $L=L_{f(x_{0})}(f)$ can be proven to be compact
- $\partial L=f^{-1}(f(x_{0}))\subset L$, so $L$ is closed
- $\lim_{ \|x\| \to \infty } f(x)=+\infty$ then $f(x)>f(x_{0})$ for all $\|x\|>M$, then $L$ is bounded by $M$
Applying the above theorem, $L$-optimizer exists and it can trivially be seen to be the global optimizer.

## Convex and Polytope
Let $D$ be a bounded convex polytope set (convex polyhedron), $f$ be a convex function on $D$. Then $f$ maximizes on some vertex of $D$.

**Proof**
Using the polytope decomposition theorem, we can decompose $f$ as a convex combination of $D$'s vertices, qed.

