similar to [[velocity]] and [[accel.]], there are two types of ang. vel.
- avg. av $\overline{\omega}$
- inst. av $\omega$

this can also be *vectorized* (more like bivectorized), as the cross (outer) product of $\mathbf{r}$ and $\mathbf{v}$, divided by the square length of $\mathbf{v}$:
$$
\boxed{\vec{\vec{\omega}}=\frac{\mathbf{r} \wedge \mathbf{v}}{r^{2}}, \vec{\omega}=\frac{\mathbf{r}\times\mathbf{v}}{r^{2}}=\vec{\vec{\omega}}I^{-1}}
$$
**corollary:** $\mathbf{v}=\vec{\omega} \times \mathbf{r}$
- $\vec{\omega} \times \mathbf{r}=(\vec{\omega}\wedge \mathbf{r})I^{-1}=-(\mathbf{r}\wedge\vec{\omega})I^{-1}=-\mathbf{r}\cdot \vec{\vec{\omega}}=-\frac{\mathbf{r \cdot(\mathbf{r}\wedge \mathbf{v})}}{r^{2}}=\mathbf{v}$

then $\omega$ is a vector
![[Pasted image 20230408102926.png]]
- p-dir: axis of rotation
- c-dir: $(\mathbf{r}, \mathbf{v}, \vec{\omega})$ is positively-oriented
- magnitude: $\|\vec{\omega}\|=|\omega|$ (the inst. av) $= |\frac{d\theta}{dt}|$ (only in the $r$ const case) ^e26f11

proof
- the dir are trivial
- for the magnitude, the general rotation proof is somewhat outside of the scope, we'll only do the 2d proof
	- equivalent to $|\omega|=|\frac{v}{r}|$
	- **let** $\mathbf{r}=re^{ i\theta }$, then $\mathbf{v}=e^{ i\theta } \frac{dr}{dt}+r e^{ i\theta }\omega \implies |v|=| \frac{dr}{dt}+r\omega|$
	- qed since $r$ const

**unit:** rad/s or Hz (if one doesn't consider rad to be a scalar)
