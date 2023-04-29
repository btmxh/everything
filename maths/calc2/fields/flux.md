vi: **thông lượng**

to indicate how much fluid is flowing through a unit of surface, one can use **flux**
**flux** is defined as a simple [[surface integral]] of the field over some predefined surface

e.g. $\mathbf{F}=(xy^{2}+z)\hat{i}+(x^{2}y+z)\hat{j}$, $S$ is the surface of $z=x^{2}+y^{2}, z\leq 1$, **direction of flux upwards**
using the [[generalized stoke's theorem#divergence|div theorem]]:
![[Pasted image 20230417103459.png]]
to make $S$ closed, we add the disk $x^{2}+y^{2}\leq z=1$ to the surface, then the flux is equal to the div integral - the added flux
- div integral: $\iiint_{V}\nabla\cdot \mathbf{F}dV=\iiint_{V}(x^{2}+y^{2})dV=\int _{0}^{1}\iint_{C(z)}dCdz$
	- ($C(z)$ is the disk $x^{2}+y^{2}=z$, which has area $\pi z$)
	- hence, the integral evaluates to $\int _{0}^{1} \pi z \, dz=\frac{\pi}{2}$
- added flux thing: $\iint_{C(1)}\mathbf{F}\cdot \hat{k}dC=\iint_{C(1)}0dC=0$
- => result is $\frac{\pi}{2}$, or is it?
- the problem is when we use the [[generalized stoke's theorem#divergence|div theorem]], we used the WRONG direction
	- the direction of normal is upwards at $C(1)$, but it's not true on the bottom half of the thing => we need to flip the sign (note that the addex flux thing is 0): result is $-\frac{\pi}{2}$
when $\nabla\cdot \mathbf{F}=0$ at all points, it's a [[field#solenoidal vector field|solenoidal vec field]], since by the [[generalized stoke's theorem#divergence|div theorem]], one can see that flux is 0 for every closed surfaces

