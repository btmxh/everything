a manifold are sets that can be **locally described** using euclidean space, or more precisely:

## rigor def
let $V_{i}$, $i\in 1..m$ be an open cover of $X \subset \mathbb{R}^{n}$ (i.e. $V_{i}$ are open and the union of them is $X$)
then if
- for each $i$, there exists $U_{i}$ open in $\mathbb{R}^{k}$ ($k$ const, does not depends on $i$), and $\alpha_{i}: U_{i}\to V_{i}$ cont.
- for all $\mathbf{r} \in X$, there is a set $V_{i}$ s.t. $\mathbf{r}\in V_{i}$ and $\alpha_{_{i}}$ is a local [[diffeomorphism]] wrt $\mathbf{r}$
then $X$ is a $k$-dim [[manifold]], $(V_{i}, \alpha_{i})$ is called a **coord chart**

e.g. the sphere surface $x^{2}+y^{2}+z^{2}=0$ can be parameterize as $x=\sin u \sin v, y=\sin u\cos v, z=\cos u$, for $u,v\in[0, 2\pi)$
- one can pick $m=1$, $V_{1}$ is the sphere itself, and $U_{1}=[0,2\pi)^{2}$ but then $\alpha_{1}$ is not local diff. (the inverse does not cont. diff.)
- one divides the sphere into two halves, the $z\geq0$ and the $z\leq 0$ half. for the top half, one can directly map the unit circle $u^{2}+v^{2}=1$ to $x=u,y=v,z=\sqrt{ 1-u^{2}-v^{2} }$ => this turned out to be cont, but $\frac{\partial z}{\partial u}$ is not defined on the "equator" (btw i just noticed that this shit is not even open bruhhhhhhhhhhh)
- to account for the above problem, one divides the sphere into 6 halves: $z>0,z<0,x>0,x<0,y>0,y<0$ => boundaries are not present in the covers => no problems now, and there is no points which lies on all boundaries (which must be $(0,0,0)$)

## boundary

naively, one can use the metric space def for boundary, but topologist does not like this def (they work in [[topological space]]) => we can only comply, even when we are working in $\mathbb{R}^{n}$

e.g. boundary of the triangle (?) $x+y+z=1, x,y,z>0$
first, we need to model this as a [[manifold]]: $V_{i}$ is $u,v>0, u+v < 1$, and $\alpha_{1}$ is the map $x=u,y=v,z=1-u-v$, which clearly satisfy the conditions
now we have several choices
- is the boundary the union of $\alpha_{i}(\partial V_{i})$? => no this make equators and similar lines boundary of a sphere
- embrace the metric... NO WE ARE SUPPOSED TO DESTROY THE METRICFAGS
- or:

the upper half space of dim $k$, denoted $H^{k}$ is the set of all k-dim points $\mathbf{r}$ s.t. $\mathbf{r}\cdot \mathbf{e_{k}}\geq 0$ (i.e. last coord is ge 0)
intuitively, its boundary "is" $\mathbb{R}^{k-1}$

