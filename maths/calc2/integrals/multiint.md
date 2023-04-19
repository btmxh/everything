vi: **tích phân bội**

## general riemannian definition

here's the thing we want to define: $\int _{V} f(\mathbf{r}) \, d\mathbf{r}$

### riemann sum
the riemann sum of the integral a partition $\sigma$ that divide the hypervolume $V$ into m parts $V_{1},V_{2}, \dots$ and a selection $\eta$: $\mathbf{r_{i}}\in V_{i}$  is defined as $s(\sigma, \eta)=\sum_{i=1}^{m} f(\mathbf{r_{i}})\rho(V_{i})$, where $\rho(V)$ is the area of $V$
when $V$ are (half-open) rectangles, i.e. $[a_{1},b_{1})\times\dots$, we have $\rho(V)=|b_{1}-a_{1}|\times\dots$

- if we pick the max in the selection, i.e. $f(\mathbf{r_{i}})\geq f(\mathbf{r})$ for all $\mathbf{r}\in V_{i}$, we ended up with the **upper darboux sum**
- if we prefer min value, it's the **lower darboux sum**

### rectangular region
when $V$ is a rect region, one can always divide it neatly into non-overlapping rectangles with no gap at all (or gaps have [[jordan content]] zero)
like riemann single ints, we will simply take the limit as the **length** of the partition & selection, defined as $l(\sigma)=\max_{i\in 1..m}d(V_{i})$, where $d(V)$ is the *diameter* of the rectangle, defined as its longest length: $d([a_{1},b_{1})\times\dots)=\max_{i\in 0..n}|b_{i}-a_{i}|$

### general region
simply defining $g(\mathbf{r})=f(\mathbf{r})\cdot 1_{\mathbf{r \in V}}$, and taking the integral over a bounding hyperbox $B$ of $V$, one can rigorously define the most abstract form of riemannian multiint

## conditions
- if the int. exists on closed $V$ => $f$ is bounded on $V$
- if $f$ is bounded on $\overline{V}$ (the closure of $V$) then it's R-intbl on $V$
- if $f$ bounded on $\overline{V}$, cont on $C \subset V$ s.t. $E = V \setminus C$ is empty wrt the [[jordan content]]

## props
- the r-multiint is additive wrt $V$, linear and order preserving wrt $f$

## r-intbl
- $D$ *jordan-contentable* f cont, bounded in $D$
- $f$ r-intbl wrt $D$, $g = f$ on the set $E$ s.t. $\rho(D \setminus E)=0$, where $\rho$ is the [[jordan content]]

## conversion of coords
to u-sub
- introduce a map $g: \mathbb{R}^{n}\to \mathbb{R}^{n}$ that does not have zero derv at all points in $V$
- calc the [[jacobian]] determinant, denoted with $\det(g'(x))$
- then
$$
\int _{V} f(\mathbf{r}) \, d\mathbf{r} = \int _{f^{-1}(V)} f(g(\mathbf{r'}))g'(\mathbf{r'}) \, d\mathbf{r'} 
$$

### 2d
polar coords: $x=r\cos \theta, y=r\sin \theta$ then $f'(r, \theta)=\det((\cos \theta, \sin \theta), (-r\sin \theta, r\cos \theta))=r$
=> $\iint_{R} f(x,y)dxdy=\iint_{R'} f(r\cos \theta,r\sin \theta) rdrd\theta$

## 3d
### spherical :skull: coords:
you can calculate the determinant on your own, im just grabbing that shit from the lecture notes
if $x=r\sin \theta \cos \phi, y=r\sin \theta \sin \phi, z=r\cos \theta$, then the determinant is $\boxed{r^{2}\sin \theta}$

### cylinder coords:
if $x=r\cos \theta, y=r\sin \theta, z=z$, the determinant is $r$ (one row of the matrix is $[0,0,1]$)