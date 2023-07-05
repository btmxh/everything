vi: **tích phân bội**

## simple definition
similar to one-var int, one can define the multiint by
- consider all partitions of the region
- for each subregion, pick a sample point, eval the fn at that point, multiply with the subregion hypervolume, add all of them => tổng riêng
- taking the lim of this sum as the highest diameter of the hypersubregion -> 0, if it conv to a singular value, that's the multiint's value

## general riemannian definition

here's the thing we want to define: $\int _{V} f(\mathbf{r}) \, d\mathbf{r}$

### riemann sum
the riemann sum of the integral a partition $\sigma$ that divide the hypervolume $V$ into m parts $V_{1},V_{2}, \dots$ and a selection $\eta$: $\mathbf{r_{i}}\in V_{i}$  is defined as $s(\sigma, \eta)=\sum_{i=1}^{m} f(\mathbf{r_{i}})\rho(V_{i})$, where $\rho(V)$ is the area of $V$
when $V$ are (half-open) rectangles, i.e. $[a_{1},b_{1})\times\dots$, we have $\rho(V)=|b_{1}-a_{1}|\times\dots$

- if we pick the max in the selection, i.e. $f(\mathbf{r_{i}})\geq f(\mathbf{r})$ for all $\mathbf{r}\in V_{i}$, we ended up with the **upper darboux sum** (denoted $S(\sigma)$)
- if we prefer min value, it's the **lower darboux sum** (denoted $s(\sigma)$)
- a partition $\sigma_{1}$ is consider to be **smoother** than $\sigma_{2}$ iff every hyperrect in $\sigma_{1}$ is enclosed in **one** hyperrect of $\sigma_{2}$
- => smoother partition will be more precise => upper darboux sum dec, lower darboux sum inc

### rectangular region
when $V$ is a rect region, one can always divide it neatly into non-overlapping rectangles with no gap at all (or gaps have [[jordan content]] zero, or internals does not intersect)
like riemann single ints, we will simply take the limit as the **length** of the partition & selection, defined as $l(\sigma)=\max_{i\in 1..m}d(V_{i})$, where $d(V)$ is the *diameter* of the rectangle, defined as its longest length: $d([a_{1},b_{1})\times\dots)=\max_{i\in 0..n}|b_{i}-a_{i}|$ (alternatively one can consider the diagonal but that doesn't matter)

using the darboux sums, one can define the upper and lower integral (use overline, underline to denote), and we have:
- lower darboux <= $\overline{\int \dots \, dx}$ <= $\underline{\int \dots \, dx}$ <= upper darboux)
- $\sup_{\pi\in P(D)}=\underline{\int _{V} f(\mathbf{r}) \, d\mathbf{r}}$
- $\inf_{\pi\in P(D)}=\int _{V} f(\mathbf{r}) \, d\mathbf{r}$

alternatively, one could consider a seq of partition $(\pi_{n})$ that has $\lim_{ n \to \infty } d(\pi_{n})=0$ (dãy phân hoạch chuẩn tắc) => the lower and upper darboux sum is monotonic => conv

### general region
simply defining $g(\mathbf{r})=f(\mathbf{r})\cdot 1_{\mathbf{r \in V}}$, and taking the integral over a bounding hyperbox $B$ of $V$, one can rigorously define the most general form of riemannian multiint

## conditions
- if the int. exists on closed $V$ => $f$ is bounded on $V$
- if $f$ bounded on $\overline{V}$ and $\underline{\int_{V} f(\mathbf{r}) \, d\mathbf{r}}=\overline{\int_{V} f(\mathbf{r}) \, d\mathbf{r}}$ => $f$ R-intbl
	- equivalently, if $f$ is bounded on $\overline{V}$ and for all $\varepsilon>0, \exists \pi\in P(D): S(r)-s(r)<\varepsilon$, $f$ R-intbl
- if $f$ is cont, bounded on $\overline{V}$ (the closure of a rectangular region $V$) then it's R-intbl on $V$
	- if $f$ is cont, bounded on jctable $V$, then $f$ is rintbl on $V$
- if $\mu(D)=0$, $f$ bounded on $D$ then $\int _{D} f(\mathbf{r}) \, d\mathbf{r}=0$
- if $g$ bounded on $\overline{V}$, cont on $C \subset V$ s.t. $E = V \setminus C$ is empty wrt the [[jordan content]] (one can avoid this content by using the hypervolume of $E$ is 0) and $f=g$ on $C$, $f$ R-intbl on $D$, then $g$ is R-intbl on $D$ and $\int _{D} f(\mathbf{r}) \, d\mathbf{r}=\int _{D} g(\mathbf{r}) \, d\mathbf{r}$
- **mvt**: if $f$ cont, bounded on $D$ jct measurable, then there is some $\mathbf{r_{0}}\in D$ s.t. $f(\mathbf{r_{0}})\mu(D)=\int _{D}f(\mathbf{r}) \, d\mathbf{r}$, or $\gamma\in[m,M]$ s.t. $\gamma \mu(D)=\int _{D} f(\mathbf{r}) \, d\mathbf{r}$ with $m,M$ being the min and max of $f$ on $D$, respectively
## props
- the r-multiint is additive wrt $V$ ([[jordan content]] of intersection is 0), linear and order preserving wrt $f$
- if $f\geq 0$ bounded on $D$ bounded, then the set $A=\{ \exists(\mathbf{r},z), \mathbf{r} \in D, 0\leq z\leq f(\mathbf{r}) \}$ has [[jordan content]] and hypervolume $|A|=\int_{D} f(\mathbf{r}) \, d\mathbf{r}$ iff the integral exists
- let $D$ be a bounded region, then $D$ has [[jordan content]] and hypervolume $|D|=\int _{D} d\mathbf{r}$
## r-intbl
- $D$ *jordan-contentable* f cont, bounded in $D$
- $f$ r-intbl wrt $D$, $g = f$ on the set $E$ s.t. $\rho(D \setminus E)=0$, where $\rho$ is the [[jordan content]]
## fubini
the fubini's theorem connects [[multiint]] with repeated integrals, it's trivial so see https://en.wikipedia.org/wiki/Fubini's_theorem, read the lecture notes for more detail (trivial asf bruh)

## conversion of coords
to u-sub
- introduce a map $g: \mathbb{R}^{n}\to \mathbb{R}^{n}$ that does not have zero derv at all points in $V$
- calc the [[jacobian]] determinant, denoted with $\det(g'(x))$
- then
$$
\int _{V} f(\mathbf{r}) \, d\mathbf{r} = \int _{g^{-1}(V)} f(g(\mathbf{r'}))|\det g'(\mathbf{r'})| \, d\mathbf{r'} 
$$
one can denote $\det g'(\mathbf{r'})=\frac{\partial \mathbf{r}}{\partial \mathbf{r'}}$, which may be calculated as $\left( \frac{\partial \mathbf{r'}}{\partial \mathbf{r}} \right)^{-1}$ (which is regularly more straightforward than calculating the former jacobian)

**rigorous theorem:**
**conds**:
- $V$ jct, compact (closed + bounded)
- $g^{-1}$ exists imply $g$ is bij
- $g,g'$ (jacobian) cont on $g^{-1}(V)$
- $\det(g'(x))\neq 0$ for all $x\in \operatorname{Int} V=V \setminus \partial V$
**then**
- $g^{-1}(V)$ is jct, compact
- for all $f: V \to \mathbb{R}$ cont on $V$, then
	- $\int _{V} f(\mathbf{r}) \, d\mathbf{r}=\int _{g^{-1}(V)} f(g(\mathbf{r'}))|\det(g'(\mathbf{r'}))|\, d\mathbf{r'}$

### scale, translation
trivial

### 2d
polar coords: $x=r\cos \theta, y=r\sin \theta$ then $f'(r, \theta)=\det((\cos \theta, \sin \theta), (-r\sin \theta, r\cos \theta))=r$
=> $\iint_{R} f(x,y)dxdy=\iint_{R'} f(r\cos \theta,r\sin \theta) rdrd\theta$

## 3d
### spherical :skull: coords:
you can calculate the determinant on your own, im just grabbing that shit from the lecture notes
if $x=r\sin \theta \cos \phi, y=r\sin \theta \sin \phi, z=r\cos \theta$, then the determinant is $\boxed{r^{2}\sin \theta}$

### cylinder coords:
if $x=r\cos \theta, y=r\sin \theta, z=z$, the determinant is $r$ (one row of the matrix is $[0,0,1]$)

e.g. $\iint_{D} (x^{2}+y^{2}) \, d^{2}\mathbf{r}$, $D: x^{4}+y^{4}\leq 1$
sub $x=r\cos\alpha,y=r\sin\alpha$, then condition: $r^{4}(\sin ^{\times4}+\cos ^{\times4})(\alpha)\leq 1$ => $r^{4}\leq \frac{1}{\sin(\alpha)^{4}+\cos(\alpha)^{4}}$
then iint = $4\int _{0}^{\pi/2} \int _{0}^{1/(\sin(\alpha)^{4}+\cos(\alpha)^{4})} r^{2}\, dr \, d\alpha=\int _{0}^{\pi/2} \frac{1}{\sin(\alpha)^{4}+\cos(\alpha)^{4}} \, d\alpha=\frac{\pi}{\sqrt{ 2 }}$

## symmetry
let $S$ be a symmetric transformation ($\det S'=\pm1$) and $D=D_{1} \cup D_{2}$ with $\mu(D_{1} \cap D_{2})=0$, $D_{2}=S(D_{1})$ then
- if $f$ was invariant wrt $S$, then $\int _{D} f(\mathbf{r}) \, d\mathbf{r}=2\int _{D_{1}} f(\mathbf{r}) \, d\mathbf{r}$
- if $f \circ S=-f$, then the above LHS is 0

e.g. area of region limited by $y=x^{2},2y=x^{2},x=y^{2},2x=y^{2}$
let $u=\frac{y^{2}}{x},v=\frac{x^{2}}{y}$ => $| \frac{J(u,v)}{J(x,y)}|=|u'_{x}v'_{y}-u'_{y}v'_{x}|=|1-4|=3$
then we have $S=\iint _{R} \, d(x,y)=\frac{1}{3}\iint_{[1,2]\times[1,2]} \,d(u,v)=\frac{1}{3}$

e.g. $x^{2}+y^{2}=2x$,$x^{2}+y^{2}=4x$, $y=0$, $x=y$
draw figure (im lazy xd) and convert to $r,\theta$:
$r=(2\to 4)\cos \theta, \theta=0 \to \frac{\pi}{4}$
=> $S=\int _{0}^{\pi/4} \int _{2\cos \theta}^{4\cos \theta} r\, dr \, d\theta=\int _{0}^{\pi/4} 6\cos(x)^{2} \, dx=\dots$

e.g. $r=1,r=\frac{2}{\sqrt{ 3 }} \cos \phi$
- we have two pieces: $1\leq r\leq \frac{2}{\sqrt{ 3 }}\cos \phi$ and the $\frac{2}{\sqrt{  3}}\cos \phi\leq r\leq 1$
- wlog we calc the first piece, then we have $\cos \phi\geq \frac{\sqrt{ 3 }}{2}$, or $\phi\in\left[ -\frac{\pi}{3}, \frac{\pi}{3} \right]$

e.g. $r^{4}=2a^{2}xy, a>0$
e.g. $x^{3}+y^{3}=axy$
e.g $r=a(1+\cos \phi)$

e.g. $3x+y\geq 1,y\geq 0,3x+2y\leq 2,0\leq z\leq 1-x-y$
=> $0\leq y\leq 1$, $\frac{1-y}{3}\leq x\leq \frac{2-2y}{3}$
let $1-y=u$ => $V=\int _{0}^{1} \int _{u/3}^{2u/3} (u-x) \, dx \, du=\int _{0}^{1} \frac{u^{2}}{3} \, du=\frac{1}{9}$

e.g. $z=4-x^{2}-y^{2}$, $2z=2+x^{2}+y^{2}$
=> intersection $\partial D$: $r^{2}=2$
=> r-theta: $V=\int _{0}^{2\pi} \int _{0}^{\sqrt{ 2 }} \left( 4-r^{2}-1-\frac{r^{2}}{2} \right)r \, dr \, d\theta=2\pi \int _{0}^{\sqrt{ 2 }} \left( 3-\frac{3r^{2}}{2} \right)r \, dr=3\pi$

e.g. $0\leq z\leq 1-x^{2}-y^{2}$, $y\geq x,y\leq \sqrt{ 3 }x$
e.g. $r^{2}\leq 4a^{2}$, $x^{2}+y^{2}-2ay\leq 0$
e.g. $z=\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}},z=0, \frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}=\frac{2x}{a}$

**area of surface**
given the **smooth + injective** surface $\mathbf{r}(u,v)$, $(u,v) \in D$ ($D$ compact), we can calculate its area as follows:
$$
S=\iint_{D} |\mathbf{r'_{u}}\times \mathbf{r'_{v}}| \, d(u,v)
$$
> **smooth surface:** a surface $\mathbf{r}$ s.t. $\mathbf{r}$ has continuous partials, $\mathbf{r'_{u}}$ and $\mathbf{r'_{v}}$ LI for all $(u,v) \in D$
> **injective surface parameterization**: $\mathbf{r}$ is an injective fn

call $dS=|\mathbf{r'_{u}\times \mathbf{r'_{v}}}|d(u,v)$ "yếu tố diện tích của mặt"
when $\mathbf{r}(u,v)=(u,v,f(u,v))$ (aka $z=f(x,y)$), then $|\mathbf{r'_{u}}\times \mathbf{r'_{v}}|=\sqrt{ 1+f'^{2}_{u}+ f'^{2}_{v}}$

e.g. $x=r\cos \phi,y=r\sin \phi,z=h\phi, 0\leq r\leq a, 0\leq \phi\leq 2\pi$
e.g. $z=1-x^{2}-y^{2}$ in $x^{2}+y^{2}=1$
e.g. $x^{2}+y^{2}=R^{2}$ between $z=mx,z=nx$ ($m>n>0$)

## fubini
let $D$ be a jct-measurable set on $\mathbb{R}^{2}$, then$\iiint_{B} f(x,y,z)dxdydz=\iint_{D} \psi(x,y)dxdy=\iint_{D}(\int _{z_{1}(x,y)}^{z_{2}(x,y)} f(x,y,z)\, dz) \,dxdy$, with $B$ being the region specified by $(x,y,z), (x,y)\in D, z_{1}(x,y)\leq z\leq z_{2}(x,y)$

e.g. $\iiint_{\Omega} 2zdxdydz$, $\Omega: x,y\geq 0, x^{2}+y^{2}\leq z\leq 4$
e.g. $\iiint_{\Omega} (x+y)dxdydz$, $\Omega: y=x^{2},y+z=1,z=0$
e.g. $\iiint_{\Omega} ydxdydz, \Omega: x=0,y=0,z=0,2x+2y+z=4$
e.g. $\iiint_{\Omega}x^{2}e^{ y }dxdydz, \Omega: z=1-y^{2},z=0,x=1,x=-1$
e.g. $\iiint_{\Omega} xydxdydz, \Omega: y=x^{2},x=y^{2},z=0,z=x+y$
e.g. $\iiint_{\Omega} xdxdydz, \Omega: x=4(y^{2}+z^{2}), x=4$


e.g. $\iiint_{V} \sqrt{ x^{2}+y^{2} }dxdydz$, $x^{2}+y^{2}=z^{2},z=1$
e.g. $\iiint_{V} \frac{dxdydz}{\sqrt{ x^{2}+y^{2}+(z-2)^{2} }}$, $x^{2}+y^{2}\leq 1, |z|\leq 1$
