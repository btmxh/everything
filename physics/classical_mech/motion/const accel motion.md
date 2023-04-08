the motion with const [[accel.]]/[[angular accel.]]/[[tangent]]/[[normal]]
(ye it's kinda an umbrella term)

## straight motion
in order for the motion to be straight, the initial velocity $\mathbf{v_{0}}$ must be parallel to the const $\mathbf{a}$, then one can introduce a basis $\mathbf{e_{1}}$ for the orbit space
then $\mathbf{x}=xe_{1}, \mathbf{v}=v\mathbf{e_{1}}, \mathbf{a}=a\mathbf{e_{1}}$ => the motion can be modelled by regular scalars
- $v=v_{0}+at \iff \int _{v_{0}}^{v} dv=\int _{0}^{t} adt$
- $s=v_{0}t+\frac{1}{2}at^{2} \iff \int _{0}^{s}ds=\int _{0}^{t}(v_{0}+at)dt$
- $v^{2}-v_{0}^{2}=2as \iff \int _{v_{0}}^{v} vdv=\int _{x_{1}}^{x_{2}} 2adx$

## curved motion
in other cases, $\mathbf{v_{0}}$ does not lie on the same line as $\mathbf{a}$, the motion is curved
we will only investigate the simplest form of this motion: circular motion

**theorem:** the motion is circular, i.e. the orbit is a circle, i.e. $\|\mathbf{r}\|$ const, iff $\mathbf{a}_{n}=-\frac{v^{2}\hat{\mathbf{r}}}{\|r\|}$ and $\mathbf{r} \perp \mathbf{v}$ at $t=0$

**proof**: TODO
- $\mathbf{r}^{2}$ const iff $\mathbf{r}\cdot \mathbf{v}=0$ (at all moments in time)
- this is equivalent to $\mathbf{r_{0}}\perp \mathbf{v_{0}}$ and $d(\mathbf{r}\cdot \mathbf{v})=0$
- the latter is equiv to: $\mathbf{v}^{2}+\mathbf{r}\cdot \mathbf{a}=0$ (1)
- the <= case
	- we have $\mathbf{r}\perp \mathbf{v}$, then $\mathbf{a_{n}}$ is parallel to $\mathbf{r}$
	- then (1) is equiv to $\mathbf{a_{n}}=-\frac{v^{2}\hat{\mathbf{r}}}{\|r\|}$, qed
- the => case
	- $\mathbf{a_{n}}$ is parallel to

in circular motion, there are two new concepts:
- cycle: $T=\frac{2\pi}{\omega }$, where $\omega$ is the [[angular velocity]]
- frequency: $f=\frac{1}{T}=\frac{\omega}{2\pi}$

since $r$ const, one have $\omega=\frac{v}{r}$ (see [[angular velocity#^e26f11]]), then
- $a_{n}=\frac{v^{2}}{r}=r\omega^{2}$
- $a_{t}=\frac{dv}{dt}=r \frac{d\omega}{dt}=r\beta$, where $\beta$ is the [[angular accel.]] of the motion
- when $\beta$ is const,
	- $\omega=\omega_{0}+\beta t$
	- $\theta=w_{0}t+\frac{1}{2}\beta t^{2}$
	- $\omega^{2}-\omega_{0}^{2}=2\beta\theta$, etc.
	- $a_{t}$ const => we can apply the formulas in the [[const accel motion#straight motion|straight motion]] for $(x,v,a_{t})$
	- 
- 

- 
