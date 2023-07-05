## first kind
no one cares, just plain summation
e.g. $\int _{C}2 \, ds$, $C: x^{2}+y^{2}=9$ from $(0,-3)$ to $(0,3)$
trivial, it's twice the [[arclen]] => $3\pi$

calc: simply using $\int _{C} f(\mathbf{r}) \, ds=\int _{C} f(\mathbf{r})\|\mathbf{r'}\|dt$

## second kind
this is where shit happens
let $\mathbf{F}: \mathbb{R}^{n} \to \mathbb{R}^{n}$ is a n-dim [[field#vector field|vec field]], then one can define the 2nd kind lineint $\int _{C} \mathbf{F(\mathbf{r})} \cdot d\mathbf{r}$ by
- FIRST, $C$ needs a direction, so do that
- second, take the riemann sum of the expr $\mathbf{F}(\mathbf{r})\cdot\Delta \mathbf{r}$ and bla bla bla
since $d\mathbf{s}$ is basically $d\mathbf{r}$, they also write $\int _{C} \mathbf{F}(\mathbf{r}) \cdot d\mathbf{s}$, but it's misleading asf
and we can also write that lineint as $\int _{C} F_{i} \, dx_{i}$ (einstein)
**orientation convention: counterclockwise**

to calc lineint via the [[generalized stoke's theorem]], we have two ways
- by $\partial C$ => we need some $f$ s.t. $df=F_{i}dx_{i}$ => $\nabla f=F$ ([[generalized stoke's theorem#gradient theorem|gradient theorem]])
- by $\partial^{-1}C$ => by $d(F_{i}dx_{i})$, which is the curl of $F_{i}$ ([[generalized stoke's theorem#stoke's theorem|stoke's theorem]], [[generalized stoke's theorem#green's theorem|green's theorem]])

**Theorem:** $P,Q$ and their partials cont on $D$ open, connected, single, then the following statements are equivalent:
- $\exists U$ s.t. $dU=Pdx+Qdy$
- $\oint_{C} Pdx+Qdy=0$ for all closed $C$
- $\int _{C} Pdx+Qdy \, dx$ only depends on $\partial C$ (endpoints)
- $\frac{\partial P}{\partial y}=\frac{\partial Q}{\partial x}$
