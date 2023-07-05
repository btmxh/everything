$$
\int_{M} d\omega = \int_{\partial M} \omega 
$$
where
- $M$ is a smooth [[manifold]]
- $\partial$ is the **boundary** operator
- $d$ is the [[ext derv]] operator

## ftc
when the manifold is a segment $[a,b]$ on $\mathbb{R}$, $d\omega$ is the regular derivative of $\omega$, and we have the fundamental theorem of calculus
$$
\int _{a}^{b} \omega(x) \, dx = \int _{[a,b]} d\omega =\int _{\{ a^{-}, b^{+} \}} \, \omega= \omega(b)-\omega(a)
$$

## gradient theorem
simply a generalization of the ftc:
$$
\int _{a}^{b} \nabla f(t)dt =\int _{[a,b]} df=f(b)-f(a) 
$$

## stoke's theorem
$$
\iint _{\Sigma} \nabla \times F\, d\Sigma=\int _{\Sigma} d\omega = \int _{\partial \Sigma} \omega = \oint _{\partial \Sigma} F\,ds
$$
($\omega$ is the 2-form that repr $F$)

## green's theorem
special case of [[generalized stoke's theorem#stoke's theorem|stoke's theorem]] in 2d
$\mathbf{F}=F_{x}\hat{i}+F_{y}\hat{j}$, curve is in the xy-plane (additional conditions: $F_{x},F_{y}$ has continuous partials, so one must handle **singular points**)
=> $\nabla \times \mathbf{F}=d(F_xdx+F_{y}dy)=(\frac{\partial F_{y}}{\partial x}-\frac{\partial F_{x}}{\partial y})dxdy$
$$
\iint_{\Sigma} \left( \frac{\partial F_{y}}{\partial x} -\frac{\partial F_{x}}{\partial y}\right)dxdy=\oint _{\partial\Sigma} Fds=\oint_{\partial \Sigma} (F_{x}dx+F_{y}dy)
$$
> if $C=\partial D$, $D \subset \mathbb{R}^{2}$, then the **positive orientation** is the orientation with $D$ always on the left of $C$

e.g. simple convex region => CCW
e.g. simple convex region - sub convex region => CCW on out bounds, CW on in bounds

"miền đơn liên": a region that could be collapsed into a point (i.e. no holes)

e.g. $I=\int _{C} x^{2}ydx-xy^{2}dy$, $C: x^{2}+y^{2}=1$ CCW
$D: x^{2}+y^{2}\leq 1$ is $\partial C$, so $I=-\iint_{D} (-y^{2}-x^{2})dxdy=\int _{0}^{1} \, rdr\int _{0}^{2\pi} \, d\phi(r^{2})=-\frac{2\pi}{4}=-\frac{\pi}{2}$

e.g. $I=\int _{C} (x-2y)dx+(3x+y)dy, C: |x|+|y|=1$ CW
wrong orientation so
$I=\int _{\partial^{-1}C} (-2-3) \, dxdy=-5S_{\partial^{-1}C}=-10$

e.g. $\int _{C} (x^{2}+y\cos xy)dx+\left( \frac{x^{3}}{3}+xy^{2}-x+x\cos xy \right)dy$, $C: x^{2}+y^{2}=2x, y\leq 0$ CCW
consider the linear path $C'$ from $(2,0)$ to $(0,0)$
=> $I+\int _{C'}\dots=I_{D} \left( \frac{\partial (y\cos xy)}{\partial y} - \frac{\partial \left( \frac{x^{3}}{3}+xy^{2}-x+x\cos xy \right)}{\partial x} \right)dxdy$
the integrand evaluate to $\cos xy-xy\sin xy-x^{2}-y^{2}+1-\cos xy+xy\sin xy$$=1-x^{2}-y^{2}$
and $D=\partial^{-1}(C+C')$
also $\int _{C'}\dots=\int _{2}^{0} x^{2} \, dx=-\frac{8}{3}$ (because $y=dy=0$)
to calc the [[multiint]], we have $I=\frac{4}{3}+\iint_{D}(1-r^{2})dxdy$, and $D: r^{2}\leq 2r\cos \phi$ => $r\leq 2\cos \phi, \phi\in \left[ 0, \frac{\pi}{2} \right]$
=> $I=\frac{8}{3}+\int _{0}^{\pi/2} \, d\phi \int _{0}^{2\cos \phi} \, rdr(1-r^{2})$$=\frac{8}{3}+\int _{0}^{\pi/2} \, d\phi\left( \frac{t^{2}}{2}-\frac{t^{4}}{4} \right)_{t=2\cos \phi}$$=\frac{4}{3}+\int _{0}^{\pi/2} (2\cos ^{2}\phi-4\cos ^{4}\phi) \, d\phi=\frac{8}{3}+2B\left( \frac{1}{2}, \frac{5}{2} \right)-4B\left( \frac{1}{2}, \frac{9}{2} \right)=\frac{\pi}{4}+\frac{8}{3}$
e.g. $P=\frac{-y}{r^{2}},Q=\frac{x}{r^{2}}$ => $P'_{y}=Q'_{x}$, calc $\int _{C} Pdx+Qdy$ with $C: x^{2}+y^{2}=R^{2}$
we can't use green here because (0,0)
but we can use green like so:
$I=\frac{1}{R^{2}}\int _{C} -ydx+xdy=\frac{1}{R^{2}}\iint_{D} 2dxdy=2\pi$

## divergence theorem
$$
\iiint _{\Sigma} \nabla\cdot \mathbf{F}\, d\Sigma = \iint_{\partial \Sigma} \mathbf{F}\cdot d\mathbf{S} 
$$

$\mathbf{S}$ here is a pseudovector (ew), therefore $\mathbf{F}\cdot d\mathbf{S} = F_{x}dS_{x}+\dots$, where $dS_{x}=dydz$ and etc. => $\mathbf{F}\cdot d\mathbf{S}$ is actually $\omega=F_{x}dydz+\dots$ (the order matters here btw)
this is why we should succumb to the math gods and embrace geometric algebra i hate this bullshit

## proof
**WARNING**: this is a very deep rabbit hole
prereqs:
- [[diffeomorphism]]
- [[manifold]]

read these instead of this crap
- https://piazza.com/class_profile/get_resource/iw9lna8pcq84zk/iy3u3tz2pz23hz
- https://math.uchicago.edu/~may/REU2012/REUPapers/Presman.pdf (this proof was heavily based on this paper)
- https://planetmath.org/proofofgeneralstokestheorem

> **formal statement**: let $X$ be a compact k-dim manifold with boundary $\partial X$ is a $k-1$ dim manifold with the boundary orientation. then, for any smooth ($k-1$)-form $\omega$ on $X$:
> $$
\int _{\partial X} \omega = \int _{X} \, d\omega  
$$

since integrating is linear, one can split the manifold and consider the case $m=1$, the manifold has coord chart $(V, \alpha)$ (see [[manifold#rigor def]])
wlog, one may assume $V_{i}$ is either $\mathbb{R}^{k}$ or $H^{k}$, where $H^{k}$ is the **half-positive space** of $\mathbb{R}^{k}$ (last, i.e. k-th coord is positive)
- case 1: $V_{i}$ is $\mathbb{R}^{k}$, then since $\partial \mathbb{R}^{k}=0$, one expect RHS=0, or equivalently $\boxed{\int _{\mathbb{R}^{k}} \, d\omega = 0}$
	- expressing $\omega=\sum_{i=1}^{k}(-1)^{i-1}f_{i}d_{i}$, where $d_{i}=dx_{1}\dots dx_{k}$ but omitting $dx_{i}$
	- then $d\omega$ is the "$k$-dim [[divergence]]", can be calc as $d\omega=\sum_{i=1}^{k}\frac{\partial f_{i}}{\partial x_{i}}dx_{1}dx_{2}\dots dx_{k}$
	- then, the integral evals to $\sum_{i=1}^{k} \int _{\mathbb{R}^{k}} \frac{\partial f_{i}}{\partial x_{i}} \, dx_{1}dx_{2}\dots$
	- for $i=1$, we have $\int _{\mathbb{R}^{k}} \frac{\partial f_{1}}{\partial x_{1}} \, dx_{1}dx_{2}\dots=\int _{\mathbb{R}^{k-1}} \left( \int _{-\infty}^{\infty} \frac{\partial f_{1}}{\partial x_{1}}\, dx_{1} \right) \, dx_{2}dx_{3}\dots$
	- the inner integral is $f_{1}(\mathbf{x_{1}},x_{2},\dots)|_{\mathbf{x_{1}=}-\infty}^{\infty}$ by the [[generalized stoke's theorem#ftc|ftc]], this evaluates to zero because of muh compact support ($f_{1}(a, \dots)=0$ for arbitary large $a$, see additional details for more)
- case 2: $V_{i}$ is $H^{k}$, then this is where shit does not evaluate to zero
	- in this case, the first $k-1$ integrals evaluate to zero, because bla bla compact support
	- the $k$-th one: $(-1)^{k-1}\int _{\mathbb{R}^{k-1}} \left( \int _{0}^{\infty} \frac{\partial f_{k}}{\partial x_{k}}\, dx_{k} \right) \, dx_{1}dx_{2}\dots dx_{k-1}$$=(-1)^{k}\int _{\mathbb{R}^{k-1}} f_{k}(\dots, 0) \, dx_{1}\dots$
	- we will look at the LHS, it's non-zero now, and since $\partial H^{k}=\mathbb{R}^{k-1}$, we have LHS=$\int _{\mathbb{R}^{k-1}} (-1)^{k-1}f_{k-1} \, dx_{1}dx_{2}\dots$ (note that $dx_{k}=0$ for obvious reasons)
	- due to orieorientation bullshit, see additional details, LHS is missing a $-1$ factor ($\mathbb{R}^{k-1}$ and $\partial H^{k}$ has different orientation) => qed

**additional details**
- compact bullshit
	- since $X$ is compact (intuitively bounded), its bounding box can't be infinite => at some point from the origin, the value $\omega$ there doesn't matter in both LHS and RHS => one can let $\omega=0$ there
- orientation
	- the $\mathbb{R}^{k-1}$ space can be considered an upward-oriented hyperplane in $\mathbb{R}^{k}$ space, but $\partial H^{k}$ is pointing downwards (due to $H^{k}$ being the half-**positive** space)

**comments**:
- in case 1, we consider the points inside the manifold, and in non-rigor terms, "the integral cancels out" (see https://en.wikipedia.org/wiki/Divergence_theorem#Informal_derivation), leaving only the points that matter: the boundary. it feels good to actually see what people have been saying "it just cancels bro" actually works out in rigor math