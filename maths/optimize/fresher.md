## $\mathbb{R}^{n}$
in optimization, we usually have superscript indices, which is not powers
we also use einstein shit here xddd
- superscripts are used to denote normal vectors
- subscripts are used to denote linear form (i.e. the transpose of a vector)
e.g. $y=\lambda_{i}x^{i}$, with $i\in I$ irrelevant => $\lambda$ is a row vec, while $x$ is a col vec (i.e. traditional vecs)

**inner product**
all inner prods are in the form $\langle x,y\rangle=x^{T}Ay$, with $x,y$ being vectors, $A$ being a matrix, but we only consider the canonical one when $A=I_{n}$

**norm**
euclidean norm of $x$ is $\|x\|=\sqrt{ x^{T}x }$
general norm of a vecsp with scalar set containing $\mathbb{R}$ is some fn $\|\|_{f}$ maps $V \to \mathbb{R}$ s.t.
- $\|x\|\geq 0$ for all $x\in V$
- $\|\lambda x\|"=|\lambda|\|x\|$ for all $x\in V, \lambda\in \mathbb{R}$
- $\|x+y\|\leq\|x\|+\|y\|$ for all $x,y\in V$
then we have the CBS ineq
- $|\langle x,y\rangle|\leq\|x\|\|y\|$ for all vectors $x,y$
- arcosine of the $\frac{LHS}{RHS}$ ratio ($\leq 1$) is the angle between the two vectors

**conv**
seq $(x^{n})_{n\in \mathbb{N}}$ conv to $x^{*}$ iff $\lim_{ n \to \infty } \|x^{n}-x^{*}\|=0$

**topology**
let the distance fn $d(x,y)=\|x-y\|$
open ball: $B(x^{0}, \varepsilon)=\{ x\in\mathbb{R}^{n}, d(x,x^{0})<\varepsilon \}$
$x\in \operatorname{Int}A$ iff $\exists \varepsilon>0, B(x, \varepsilon)\subset A$
$x\in \partial A$ iff $\forall\varepsilon>0, B(x,\varepsilon)\cap A, \mathbb{R}^{n}\setminus A$
$x$ conv pt of $A$ iff all $B(x,\varepsilon)$ contains infty points in $A$
- then if all $B(x,e)$ contains a point $x'\neq x$, then one can lerp to get an infinite amount of new points
- conv pt of $A$ may not be in $A$

$A$ open iff $A=\operatorname{Int}A$, open balls are open
$A$ closed iff $A^{c}=\mathbb{R}^{n}\setminus A$ open
- then $\partial A \subset A$
- $A$ closed iff all limits of seqs on $A$ conv to a pt in $A$

$\emptyset$ and $\mathbb{R}^{n}$ are both open and closed
$\operatorname{Int}A$ is the union of all open subset of $A$
$\bar{A}$, or $cl A$ is the closure of $A$, or $A\cup \partial A$

set $A\subset \mathbb{R}^{n}$ bounded iff exists $\lambda$ st $\|x\|\leq \lambda$ for all $x\in A$
compact set = closed + bounded
- $A$ compact then all seqs in $A$ contains a subset conv to a pt on $A$

**partial order**
one can defined a partial order on $\mathbb{R}^{n}$ by $x>y$ if all $x^{i}>y^{i}$, etc.

## multifn
$f: X\subset \mathbb{R}^{n}\to \mathbb{R}^{m}$ are multiparamfns, with its graph $G$ being the set of all $m+n$-points $(\dots x, \dots f(x))$ for all $x\in X$

level set $L(\alpha,f)=\{ x\in X, f(x)=\alpha \}$
if $m=1$ one can have upper, lower level sets
- upper: $L^{\alpha}(f)=\{ x\in X, f(x)\geq a \}$
- lower: $L_{\alpha}(f)=\{ x\in X, f(x)\leq a \}$

**continuity** is simple, but there are two weaker variants
- **lower semicontinuous** at $x_{0}$ if $\forall \varepsilon>0$ there exists $\delta>0$ s.t. $f(x) \geq f(x_{0})-\varepsilon$ ($f(x)-f(x_{0})\geq-\varepsilon$) for all $x\in B(x_{0},\delta)$
- upper similarly defined

e.g. let $f(0)=0$, assuming the limits exist and $f$ is lowercont, what can one conclude about $a=\lim_{ x \to 0^{-} }f(x)$ and $b=\lim_{ x \to 0^{+} }f(x)$?

we have $\forall\varepsilon>0$, exists $\delta_{1}>0$ s.t. $\|f(x)-a\|<\varepsilon$ for all $x\in B(0,\delta_{1})$ and $\delta_{2}>0$ s.t. $f(x)\geq f(0)-\varepsilon$ for all $x\in B(0, \delta_{2})$
take min delta and then we have $f(x)\geq -\varepsilon$ and $\|f(x)-a\|<\varepsilon$, or $f(x)\in [-\varepsilon, +\infty) \cap(a-\varepsilon, a+\varepsilon)$, which means that $-\varepsilon<a+\varepsilon$, or $a>-2\varepsilon$, i.e. $a\geq 0$
$b\geq 0$ for similar reasons

more generally, we have alt defs for semicont:
- $f$ uppersemicont at $x_{0}$ iff $\liminf_{ x \to x_{0} }f(x)\geq f(x_{0})$
- $f$ lowersemicont at $x_{0}$ iff $\limsup_{ x \to x_{0} }f(x)\leq f(x_{0})$

with liminf, limsup defined as
- $\limsup_{ x \to x_{0} } f(x)=\lim_{ \varepsilon \to 0 } \sup f(B(x_{0}, \varepsilon))$
- similarly for inf

**partials**

let $f:\mathbb{R}^{n}\to \mathbb{R}^{m}$ differentiable
**jacobian** of $f$ is the matrix $J=\frac{df}{dx}$ s.t. $\left( \frac{df}{dx} \right)_{j}^{i}=\frac{ \partial f_{i} }{ \partial x_{j} }$
if $m=1$
- transpose of jacobian is the **gradient** $\nabla f^{i}=\frac{ \partial f }{ \partial x_{i} }$
- jacobian of $\nabla f$ is the **hessian** $\nabla^{2}f^{i}_{j}=\frac{ \partial^{2} f }{ \partial x_{i}\partial x_{j} }$

**differentiable**
- 1-diff iff $f(x+d)=f(x)+Jf\, d+o(\|d\|)$
- 2-diff iff $m=1$ and $f(x+d)=f(x)+\langle \nabla f(x),d\rangle + \frac{1}{2}d^{T}\nabla^{2}f(x)d+o(\|d\|^{2})$
	- then $\nabla^{2}f$ is symmetric

**chain rule** $\frac{df}{dx}=\frac{df}{dg}\cdot \frac{dg}{dx}$
if $f: \mathbb{R}^{m}\to \mathbb{R}$ then $\frac{df}{dx}=\left\langle  \nabla_{g} f, \frac{dg}{dx} \right\rangle$
- consider a level set $L(\alpha,f)$ as a curve $x=x(t)$, then we have
	- $0=\frac{df}{dt}=\frac{df}{dx}\cdot \frac{dx}{dt}=\langle \nabla_{x}f, x'(t)\rangle$, which is basically a weaker form of IFT

## newshit
**affine set**
affine fn = linear fn + offset
- $f$ linear iff $f(ax^{1}+bx^{2})=af(x^{1})+bf(x^{2})$
- $f$ affine iff $f(ax^{1}+bx^{2})=af(x^{1})+bf(x^{2})$ for all $a+b=1$

consider 2 pts $x^{1},x^{2}$ and the line between them: $x=\lambda x^{1}+(1-\lambda)x^{2}$ for all $\lambda\in\mathbb{R}$

a set $M$ is affine if it contains every line created from 2 points in $M$ (closed under lerp)

the concept of affine combination is similar to linear comb. but to vectors, $x=\lambda_{i}x^{i}$ s.t. $\sum\lambda_{i}=1$
affine span/holl of points (set $E$) is set of all pts that are a affine comb of the given pts: $\operatorname{aff} E$

e.g.
sol of $Ax=0$ forms an linear space $\operatorname{ker}A$
sol of $Ax=b$ forms an affine space $S$ with "parallel linear space" $\operatorname{ker} A$

the num of dims of $M \subset \mathbb{R}^{n}$, $\operatorname{dim} M$ is the dim of its affine hull
relative interior of $M\subset \mathbb{R}^{n}$, $\operatorname{ri}M$ is the set of all $a\in M$ s.t. $(B(a, \varepsilon)\cap \operatorname{aff}M) \subset M$ for some $\varepsilon>0$
$M$ full dim iff $\operatorname{dim}M=n$

> Motivation
> the original definition of $\operatorname{Int}$ is not consistent, since the interior of a circle is the inner circle in 2d, but it's empty in 3d (every neighbor touch the z!=0 part)
> hence, we only check for intersection with the affine hull instead of the full space

we have these
- $\operatorname{ri}\subset \operatorname{Int}$
- int = empty for all nonfulldim $M$

**convex set**
$x=\lambda x^{1}+(1-\lambda)x^{2}$ for $\lambda\in[0,1]$ is the segment $[x^{1}x^{2}]$
convex set contains every segment with endpoints in it

intersection of convex sets is convex, not sureable for unions
convex comb exist wtf (strict convex comb: every coeff is greater than 0)

$M$ is convex iff it contains all convex comb of its element
**proof**
- <=: true becuz convex comb of 2 elems is a segment
- => $x$ is convex comb of $b_{1..k}$, then we induction on $k$, qed

$M$ convex then
- $\alpha M$ (uniform scaling) convex
- $M_{1}+M_{2}$ convex (pairwise addition)

convex hull: minimal convex set spans sth $\operatorname{conv} E$ => contains all conv comb of elements in $E$

$M$ convex then its extreme points are points $x$ that could not be repr as a strict conv comb of any 2 elems of $M$

>Then, extreme points could not be internal points
>assuming $x$ is an internal point, then one take a diameter in $CB(x,\varepsilon)\subset B(x,\varepsilon')\subset M$ and boom a strict conv comb

=> every extreme points lie on $\partial M$,
e.g. square:
- inner => internal
- vertices: ex. pts
- remaining border: neither int nor x

**theorem**: nonempty closed convex set $M$ has xpts iff it can't contain any line
**proof**
consider a line $l$ goes thru two points $a$ and $b$ in the set $M$
considering only the direction $a$ to $b$, then let $x$ be the furthest point from $a$ (with sup shit and etc., so $x$ does not necessarily to be in $M$, but $x\in M$ actually true since $M$ closed)
then $x$ (if it exist) would be an xpt => contradiction
hence the ray $ab$ is in $M$ and similarly qed

**Krein-Milman Theorem**: compact set $M\subset \mathbb{R}^{n}$ (or any "[Hausdorff](https://en.wikipedia.org/wiki/Hausdorff_space "Hausdorff space") [locally convex](https://en.wikipedia.org/wiki/Locally_convex_topological_vector_space "Locally convex topological vector space") [topological vector space](https://en.wikipedia.org/wiki/Topological_vector_space)") is the convex hull of its xpts

hyperplanes, (open and closed) halfspaces: ez to define
consider $M\subset \mathbb{R}^{n}$, vector $a\in\mathbb{R}^{n}\setminus \{ 0 \}$ and real $\alpha$
the hyperplane $H: \langle a,x\rangle=\alpha$ is the supporting hyperplane of $M$ at $x^{0}\in M$ iff $x^{0}\in H$ and $\langle a,x\rangle\leq\alpha$ (or geq idc) for all $x\in M$ (basically tangent but not just local)
=> $x^{0}$ lies on $\partial M$

**Theorem**:
- for all $x^{0}\in \partial M$, $M$ convex sbst $\mathbb{R}^{n}$, there exists some SH of $M$ at $x^{0}$
- nonempty closed convex $M \subset \mathbb{R}^{n}$ is the intersection of all its SHs
**Proof**
- we need $a$ s.t. $a^{T}x\leq\alpha=a^{T}x^{0}$, i.e. $a^{T}(x-x^{0})\leq 0$ for all $x$
- let $M'=M-x^{0}$, then we need to find $a$ s.t. $a^{T}v\leq 0$ for all $v\in M'$, which is convex
TODO

**cones**
cones are sets closed under arbitary uniform scaling: $x\in M$ then $\lambda x\in M$
cones always contain origin, and a set is convex cone iff it contains all of its non-negative LCs

hence
- linear space => linear comb => span (linear hull)
- affine space => affine comb => affine hull
- convex set => convex comb => convex hull
- cone => cone comb (nonneg LCs) => cone hull

**directions**
$d$ is a recession dir of nonempty convex $D\subset \mathbb{R}^{n}$ iff $x+\mathbb{R}^{0+}d\subset D$ for all $x\in D$
recession dir $d$ is extreme iff it's not a LC of two other recession dirs

**Theorem**: Set of all recession dirs of $M$ form a cone (with 0 ofc), which is denoted as $\operatorname{rec} M$

e.g. $M=\{ (x_{1},x_{2})\in \mathbb{R}^{2}| -x_{1}+x_{2}\leq 5,x_{1}+2x_{2}\geq 10,x_{1}\geq 0,x_{2}\geq 3 \}$![[Pasted image 20230917203514.png]]

**theorems** kek
- consider subsets of space $C,D$ and hyper plane $ax=\alpha$, $H$ separates $C$ and $D$ iff $ax\leq\alpha\leq ay$ for all $x\in C,y\in D$, strictly-separate if ykwim
	- Theorem I: if $C,D$ nonempty nonintersecting than $H$ exists
	- Theorem II: further more if either of $C$ or $D$ is compact, then there is a strict $H$
	- Farkas Lemma (corollary): given n-dim vec $a$ and mxn-mat $A$, then $a^{T}x\geq 0$ for all $x$ with $Ax\geq 0$ iff $a=A^{T}y$ for some m-dim nonneg vec $y$
	- **proof**
		- the <= part is piss easy
		- the => part is the shit:
		- consider the cone $C(A)=\{ Ay,y\geq 0 \}$
		- if $a\in C(A)$ we are done kek
		- otherwise, $\{ a \}$ and $C(A)$ are separate subsets (one is compact btw), then we can split them using some vector $x$: wlog $x^{T}a < \alpha < x^{T}y$ for all $y\in C(A)$
		- because conelinearshit one can let $\alpha=0$ (not sure) and we have $x^{T}a<0$ for $x^{T}A>0$
		- **alt interprets**
			- $Ax\leq b$ unsolvable then $y^{T}A=0,y^{T}b=-1,y\geq 0$ has sols
e.g.
- proof farkas for
$$
A=
\begin{bmatrix}
6 & 4 \\
3 & 0
\end{bmatrix}
$$
according to farkas, then either
1. $a=A^{T}y=(6y^{1}+3y^{2})e^{1}+4y^{1}e^{2}$
2. or there exists some $x$ with $Ax\geq 0$, or $6x^{1}+4x^{2}\geq0$ and $3x^{1}\geq0$ (or simply $x^{1},3x^{1}+2x^{2}\geq 0$) that satisfies $a^{T}x<0$, or $a^{1}x^{1}+a^{2}x^{2}<0$

- if 1, then $a^{1}x^{1}+a^{2}x^{2}=(6y^{1}+3y^{2})x^{1}+4y^{1}x^{2}$, trivially nonneg
- if 2, then wlog let $a^{1}x^{1}+a^{2}x^{2}=-1$, then $x^{2}=-\frac{1}{a^{2}}(1+a^{1}x^{1})$
	- then now we need to find $x^{1}\geq 0$ s.t. $3x^{1}-\frac{2}{a^{2}}(1+a^{1}x^{1})\geq 0$
	- or $x^{1}\left( 3-\frac{2a^{1}}{a^{2}} \right)\geq \frac{2}{a^{2}}$
	- or $\left(x^{1}- \frac{2}{3a^{2}-2a^{1}}\right)\left( 3-\frac{2a^{1}}{a^{2}} \right)\geq 0$, one can either chose $x^{1}\to +\infty$ or $x^{1}\to-\infty$ for the desired behavior (also edge case $a^{2}=0$ no one cares)

**convex polytope**
basically $Ax\geq b$, or expanded as $(e_{i}A^{i})x\geq b$, $e_{i}(A^{i}x)\geq b$ or $A^{i}x\geq b$ for all $i$'s
it's convex and closed
if $A^{i_{0}}x^{0}=b$ for some $i_{0}$, then $x^{0}$ strictly stf the $i_{0}$ condition, and the set of all $i_{0}$ for a given $x^{0}$, $I_{A}(x^{0})$ is the set of strictstfindices
an extreme pt of convex polytope is called a **vertex**
a nonempty convex subset $F$ is a **face** iff $(\operatorname{ri}[yz])\cap F$ then $[yz]\subset F$

>one now will be curious about the relationship between the "segment"-faces and the "constraint"-faces
>- "constraint"-faces may not be a "segment"-face, because it got omegakek'd by another face
>- "segment"-face seems to always be a "constraint"-face, and the following theorem proves that

**Theorem**: Let $F$ is a face of the convex polytope $P: Ax\geq b$ iff there exists subset $I$ of the row indices set and $F: Ax\geq A^{\dots I}x = b^{\dots I}$
**Proof**
- $F:Ax\geq A^{\dots I}x=b^{\dots I}$ is a face
	- if $[yz]\cap F$ at at least some pt $x$, then since $Ay,Az\geq b$ ($y,z\in P$), we just need $A^{\dots I}y=A^{\dots I}z=b$
	- this is true because $b^{i}=(A^{\dots I}x)^{i} \in[(A^{\dots I}y)^{i},(A^{\dots I}z)^{i}]$ for every index $i$, which forces either side of the range to be equal to $b^{i}$ => because line qed
- if $F$ face
	- if $F$ divides $P$ into two parts (not counting the boundary), then one take $y,z$ from the two parts and now $[yz]\cap F$ so both $y,z$ are in $F$, contradiction
	- TODO: generalize this to the affine hull of $F$ => qed
	- we also have $\operatorname{dim}F=n-\operatorname{rank}a^{\dots I}$












