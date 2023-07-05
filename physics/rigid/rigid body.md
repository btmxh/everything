rigid bodies are objects that does not change shape
> alternatively, rb are systems of [[point mass]] with constant relative position among them

in a rigid body, there are multiple [[field]]s
- mass density field: basically the mass density, what do you expect? this is a [[field#scalar field|scalar field]]
- velocity field: repr the [[velocity]] of each infinitesimal part of the rigid body (i.e. atoms), this is a [[field#vector field|vec field]]
- accel & force field: basically the same shit but [[accel.]] and [[force]] => [[field#vector field|vec field]]

in the discrete case, these fields are just sum of finite dirac deltas

## motion decomposition
subtracting the [[center of mass]]'s velocity from the vel field, one decompose the velocity field into two fields
- the constant field: $\mathbf{v_{t}}=\mathbf{v_{0}}$, called the translation field => one can model the motion caused by this field as a [[point mass]]
- the rotational field $\mathbf{v_{r}}=\mathbf{v}-\mathbf{v_{0}}$, which have $\int _{V} \mathbf{v_{r}}\rho \, dV=0$

in many cases, the rot field can be modelled as a simple rotation along an axis $\Delta$

## the motion model of rotation
- at a point $\mathbf{r}$ in the rigid body, there is a force $\mathbf{F}(\mathbf{r})$, which can be decomposed into three vectors using the basis $\{ \mathbf{e_{t}}, \mathbf{e_{n}}, \vec{\Delta} \}$, where $\mathbf{e_{n}}=\mathbf{r-r_{0}}, \mathbf{e_{t}}$ is the tangent to the surface at $\mathbf{r}$ (if $\mathbf{r}$ does not lie on the surface, use the tangent at $\mathbf{r'}$, the intersection of $\vec{\mathbf{r_{0}r}}$ with the surface or sth, the lecture notes does not talk about this)
- then the force along the basis $\mathbf{e_{n}}$ and $\vec{\Delta}$ does not make the point rotate along the axis (assuming that it only moves along the plane orthogonal to the axis)
- to quantify this rotation, one use the concept of [[torque]]: $\tau=\mathbf{r}\times \mathbf{F_{t}} \neq \mathbf{r}\times \mathbf{F}$ (note the $\mathbf{e_{n}}$ component)

- we have $\mathbf{F_{t}}=m\mathbf{a_{rot}}\implies \mathbf{r\times \mathbf{F_{t}}=\mathbf{r}}\times m\mathbf{a_{rot}}\implies \tau=m\mathbf{r}\times \mathbf{a_{rot}}$
- since $\mathbf{a_{rot}}=\mathbf{a_{t}}=\vec{\beta}\times \mathbf{r}\implies \mathbf{r}\times \mathbf{a_{rot}}=\mathbf{r}\times(\vec{\beta}\times \mathbf{r})$
	- we have $a\times(b\times c)=a\times(b \wedge c)^{*}=(a\wedge(b\wedge c)^{*})^{*}$$=-a\cdot(b\wedge c)$
	- if $c=a$, then $a\cdot(b\wedge c)=abc=aba=-a^{2}b$ => RHS evals to $r^{2}\beta$
- then, one have $d\mu(\mathbf{r})=\mathbf{r}^{2}\vec{\beta} dm$