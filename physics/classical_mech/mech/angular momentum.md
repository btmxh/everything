vi: **mômen động lượng**

## motivation and def
- angular momentum $L$ stems from [[angular velocity]] (however a certain university is pepega af :skull: does not talk about this), simply by $\mathbf{L}=m \frac{\vec{\omega}}{r^{2}}$ (or bivector whatever)
- since $\mathbf{r}$ is dependent on an **origin**, the angular momentum is relative to an origin point $O$
- formula: $\mathbf{L}=\mathbf{r}\times m\mathbf{v}=\mathbf{r}\times \mathbf{p}$
- is a vector
	- **origin**: the point $O$
	- p-dir: $\perp$ with the plane that contains $O$, $\mathbf{r}$ and $\mathbf{v}$ (i.e. $O+span \{ \mathbf{r}, \mathbf{p} \}$)
	- c-dir: $(\mathbf{r}, \mathbf{p}, \mathbf{L})$ is positively-oriented

## theorem
we have $\frac{d\mathbf{p}}{dt}=\mathbf{F}\implies \mathbf{r}\times \frac{d\mathbf{p}}{dt}=\mathbf{r}\times \mathbf{F}$

RHS is the [[torque]] of force $\mathbf{F}$, denoted $\mu_{/O}(\mathbf{F})$
LHS is $\frac{d(\mathbf{r}\times \mathbf{p})}{dt}-\frac{d\mathbf{r}}{dt}\times \mathbf{p}=\frac{d\mathbf{L}}{dt}-\mathbf{v}\times m\mathbf{v}=\frac{d\mathbf{L}}{dt}$
=> **the theorem of [[angular momentum]]:** the derv of [[angular momentum]] wrt time and origin $O$ is equal to the [[torque]] of the **net force** wrt origin $O$ on the [[point mass]]

**corollary:** if either $\mathbf{F}=0$ or (stronger) $\mathbf{F}$ is a radial force (vi: lực xuyên tâm), i.e. $\mathbf{F}\parallel\mathbf{r}$ => the plane of rotation is conserved.

e.g. circular motion => $L=mr^{2}\omega$, we denote $I=mr^{2}$ the **moment of inertia** of that [[point mass]] wrt $O$ then $L=I\omega$, or in vector form, $\mathbf{L}=I\vec{\omega}$

> the **moment of inertia** $I$ is formally defined as $\mathbf{I}=\frac{\mathbf{L}}{\omega}$ on [wikipedia](https://en.wikipedia.org/wiki/Moment_of_inertia)