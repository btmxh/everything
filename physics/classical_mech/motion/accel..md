similar to [[velocity]], there are two types acceleration (which are both vectors)
- avg. accel.: $\mathbf{a}_{avg}=\frac{\Delta \mathbf{v} }{\Delta t}$
- inst. accel: $\mathbf{a}=\frac{d\mathbf{v}}{dt}$

**meaning**: $\mathbf{a}$ repr how the rate of change of the [[velocity]] vector $\mathbf{v}$

**theorem:** $\mathbf{a}=\frac{d^{2}\mathbf{r}}{dt^{2}}$
**proof**easily inferred from the [[velocity#^a7c26c|ftm]]

**corollary**: if $\mathbf{r}=(x,y,z)$, then $\mathbf{a}=(\ddot{x},\ddot{y}, \ddot{z})$ and $|a|=\sqrt{ \ddot{x}^{2}+\ddot{y}^{2}+\ddot{z}^{2} }$

## components of accel

one can decompose the acceleration vector into two parts:
- the **tangent accel**, which can be defined as $\mathbf{a}_{t}=(\mathbf{a} \cdot \hat{\mathbf{v}})\hat{\mathbf{v}}$
- the **normal accel**, which is the remaining part of the accel vector: $\mathbf{a}_{n}=\mathbf{a}-\mathbf{a}_{t}$

### t-accel
- p-dir: [[tangent]] to the orbit
- c-dir: two cases
	- speeding up => same as $\mathbf{v}$
	- slowing down => same as $-\mathbf{v}$
- mag: $\|\mathbf{a_{t}}\|=|\frac{dv}{dt}|\neq \|\frac{d\mathbf{v}}{dt}\|$

**proof**
- the dir is trivial
- we have $v^{2}=\mathbf{v}^{2} \implies 2vdv=2\mathbf{v}\cdot \mathbf{a}dt\implies \frac{dv}{dt}=\frac{\mathbf{v}\cdot \mathbf{a}}{v}=\pm\mathbf{\hat{v}}\cdot \mathbf{a}=\pm\|\mathbf{a}_{t}\|$ (note that $v$ and $|\mathbf{v}|$ may not be the same thing), qed

**meaning**: repr the change in *magnitude* of $\mathbf{v}$

## n-accel
- p-dir: points towards [[osculating]] center, [[normal]] to the orbit
- c-dir: points towards the convex part of the orbit
- mag: $\|a_{n}\|=\frac{v^{2}}{R}$, where $R$ is the [[osculating]] radius

**meaning:** repr the change in *direction* of $\mathbf{v}$

**proof**
- the dir is not trivial, but it somewhat follows from the math definitions
- mag
	- using the [[curvature]] formula, RHS is equiv to
		- $\frac{v^{2}}{R}=\frac{\|\mathbf{r}'|^{2}\sqrt{ \mathbf{r'}^{2}\mathbf{r'}^{2}-(\mathbf{r'}\cdot \mathbf{r''})^{2} }}{\|\mathbf{r'}\|^{3}}=\frac{\sqrt{  v^{2}a^{2}-(\mathbf{v}\cdot \mathbf{a})^{2}}}{|v|}=|a^{2}-(\hat{\mathbf{v}}\cdot \mathbf{a})^{2}|=|a^{2}-a_{t}^{2}|=|a_{n}|$, qed

so, one can calculate both $a_{t}$ and $a_{n}$ from the pseudo-magnitude of vectors, without having to touch the vectors, and same goes for $a$: $\|\mathbf{a}\|=\sqrt{ a_{t}^{2}+a_{n}^{2} }=\sqrt{ \left( \frac{dv}{dt} \right)^{2}+ \frac{v^{2}}{R} }$
