vi: **thông lượng**

to indicate how much fluid is flowing through a unit of surface, one can use **flux**
**flux** is defined as a simple [[surface integral]] of the field over some predefined surface

**definition**: let $S$ be an orientated surface in a vecfield $V$, if $F$ const then $S$ is $S$ is a flat surface with normal $\hat{n}$, area $\Delta S$ => the flux of $F$ through $S$ (over an unit of time) is $\Phi=|F|\cos(\hat{n},F)\Delta S$
using some geometry stuff, we found out that $F\Delta S\cos(\hat{n}, F)=F_{x}dydz+F_{y}dzdx+F_{z}dxdy$

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

### Calculation method
- using [[surfaceint]] type 1
$\iint_{\Sigma} \mathbf{F}\cdot d\mathbf{S}=\iint_{\Sigma} \mathbf{F}\cdot \mathbf{n} d\sigma$

e.g. $\mathbf{F}=(x,y,z), \Sigma: x^{2}+y^{2}+z^{2}=R^{2}$, oriented outwards
param.: $x=\sin u\cos v,y=\sin u\sin v,z=\cos u$
then $\mathbf{r}=\sin u(\cos v \mathbf{\hat{x}}+\sin v \mathbf{\hat{y}})+\cos u \mathbf{\hat{z}}$
=> $\mathbf{r'_{u}}=\cos u(\cos v\mathbf{\hat{x}}+\sin v \mathbf{\hat{y}})-\sin u\mathbf{\hat{z}},$$\mathbf{r'_{v}}=\sin u(-\sin v\mathbf{\hat{x}}+\cos v \mathbf{\hat{y}})+\cos u\mathbf{\hat{z}}$
=> $\mathbf{n}=\frac{\mathbf{r'_{u}}\times \mathbf{r'_{v}}}{|\mathbf{r'_{u}}\times \mathbf{r'_{v}}|}=\dots$

or alternatively, everyone knows that $\mathbf{n}=\frac{(x,y,z)}{R}=\mathbf{F}$ => $\mathbf{F}\cdot \mathbf{n}=R$
flux = $\int_{S} R \, d\sigma=2\pi R^{3}$

$\Sigma: x+y+z=1$ bounded by Ox,Oy,Oz
$I=\iint_{S} (x-y)dydz+zdxdy$

- using [[multiint]]
parameterization: $\mathbf{r}(u,v)$, $(u,v) \in D$
then $\iint_{\Sigma} \mathbf{F}\cdot d\mathbf{S}=\iint_{\Sigma} (F_{x}dydz+\dots)$, with
$\iint_{\Sigma} F_{x}dydz=\pm\iint_{D} F_{x} |\frac{J(y,z)}{J(u,v)}|d^{2}(u,v)$ (note the sign btw)
(usually take $x=u,y=v$ and consider the sign using normal blabla)

e.g. $z=\sqrt{ R^{2}-x^{2}-y^{2} }, I=\iint_{\Sigma} xdydz$
let $y=u,z=v$, then $(y,z)=(u,v)\in(v\geq 0, u^{2}+v^{2}\leq R^{2})$
btw we have two subsurfaces with different orientation, but that **cancels out with the differing signs of $x$** => $I=2\iint_{\Sigma_{+}} xdydz=2\iint_{D} \sqrt{ R^{2}-u^{2}-v^{2} }dudv$, which is a ezaf [[multiint]]

e.g. $x^{2}+y^{2}+z^{2}=R^{2}$, $I=\iint_{\Sigma} xz^{2}dxdy$
now shit actually cancels out => 0

e.g. $z=y^{2}$ bounded by $x^{2}+y^{2}=1$, $I=\iint_{\Sigma} (x+y^{2})dydz+2z\cos ydzdx+zdxdy$

e.g. $x^{2}+y^{2}\leq z\leq 1$
$\iint_{\Sigma} zy^{2}dydz+(y+y^{2})dzdx+x^{2}dxdy$
using divergence theorem => $I=\iiint_{\partial^{-1}\Sigma} (1+2y)d^{3}V=V(\partial^{-1}\Sigma)=\dots$

e.g. $z=x^{2}+y^{2}$ bounded by $z=1$, $I=\iint_{S} zy^{2}dydz+(y+y^{2})dzdx+x^{2}dxdy$

e.g. $z=4-y^{2},x=0,x=4,z=0$$I=\iint_{S} zxdydz+xdzdx+zydxdy$
