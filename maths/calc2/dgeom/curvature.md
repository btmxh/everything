## rough def
the curvature $\kappa$ is defined as $\dfrac{d\alpha}{ds}$ as well as the length of the vector $\dfrac{d\mathbf{T}}{ds}$
where:
- $\alpha$ is the angle between the tangent vector $\mathbf{r'}$ and some constant vector (like $\hat{\mathbf{i}}$)
- s is the [[arclen]]
- $\mathbf{T}$ is the unit [[tangent]] vector (see [[frenet-serret formulas]])

it's trivial to prove that $d\alpha = |d\mathbf{T}|$, therefore proving the two defs are equivalent

$R = \frac1\kappa$ is the radius of the [[osculating]] circle (aka the [[osculating]] radius)

**NOTE:** only exists for [[singular point|non-singular points]]

## [[curve#parametric curve|p-curve]]
general: 
$$\frac{\sqrt{||r'||^2||r''||^2 - |r' \cdot r''|^2}}{||r'||^3} = \frac{||r'\wedge r''||}{||r'||^3} = \frac{||r' \times r''||}{||r'||^3} \text{(for <=3d curves)}$$
explicit:
$$\frac{|y''|}{(1+y'^2)^{\frac{3}{2}}}$$
polar:
$$\frac{|r^2+2r'^2-rr''|}{(r^2+r'^2)^\frac32}$$

e.g. $\mathbf r(t)=a(\cos(t)^3, \sin(t)^3)$
then $\mathbf r' = 3a\cos(t)\sin(t)(-\cos t,\sin t)$
and $\mathbf r''=3a(2\sin(t)^2\cos t-\cos(t)^3,2\sin t\cos(t)^2-\sin(t)^3)$
$\mathbf r' \times \mathbf r'' = 9a\sin(t)^2\cos(t)^2$
$\|\mathbf r'\| = 3|a\sin t\cos t|$
=> $\kappa = \frac1{3|a\sin t\cos t|}$
**condition**:$\|\mathbf r'\| \ne 0$ iff $t \not\equiv 0 (mod \frac\pi2)$

## [[curve#implicit curve|i-curve]]
e.g. find curvature of curve $x^2-y^2+z^2-1=y^2-2x+z=0$ at $M(1,1,1)$
### method 1: parameterization (safest choice)
param: $x=\frac32\sin t + 1, z=\frac32\cos t-\frac12,y = \sqrt{2x-z}, t=0$
- $r'=(\frac32, \frac32, 0)$
- $r''=(0,-\frac32,-\frac32)$
- $\|r'\times r''\| = \|(-\frac94, \frac94, -\frac94)\| = \frac94\sqrt3$
- $\|r'\| = \frac32\sqrt2$
- $\kappa=\frac1{\sqrt6}$
### method 2: implicit differentiation
=>$xdx-ydy+zdz=2ydy-2dx+dz=0$ (1)
=>$dx^2+xd^2x-dy^2-yd^2y+dz^2+zd^2z=2dy^2+yd^2y-2d^2x+d^2z=0$ (2)
sub x=y=z=1 to (1) => $dx=dy=u,dz=0$
sub that to (2) => $d^2z=-\frac23 u^2, d^2x=v, d^2y=v-\frac23 u^2$ 
=>$ds=u\sqrt2,dr\times d^2r=u(-\frac23u^2+v, \frac23u^2-v,\frac23u^2+v)$
=>idk lmfao **TODO**
### method 3: [[implicit fn theorem]]
- jacobian $$\left|\begin{matrix}
		2x & | & -2y & 2z\\
		-2 & | & 2y & 1
	\end{matrix}\right|$$
- right matrix is invertible for all $(y,z)$ in some neighborhood of $(1,1)$ ($-2y-4yz\ne0$ for $y=z=1$) => we can apply the theorem
- this may not be true tbh **TODO**
### method 4: tranny method
we find the tangent vector = cross product of two normal vecs:
- $\mathbf{n}_1=(2x,-2y,2z)$
- $\mathbf{n}_2=(-2,2y,1)$
- $\mathbf{t} = \mathbf{n}_1 \times \mathbf{n}_2 \| (2yz+y,x+2z,2y-2xy)$
since $\mathbf{t}(x,y,z)$ is cont., there must be a param. in the neighborhood of $M(1,1,1)$ s.t. $\mathbf{r} = \mathbf{t}$, then we can proceed and plug $\mathbf{t}$ in $\mathbf{r'}$'s place in the curvature formula:
- $\mathbf{r} = (1,1,1)$
- $\mathbf{r'} = (3,3,0)$
- $\mathbf{r''} = (2yz'+2y'z+y',x'+2z',2y'-2xy'-2x'y) = (9,3,-6)$
- $||r' \times r''|| = |(-18, 18, -18)| = 18\sqrt3$
- $||r'|| = 3\sqrt2$
- $\kappa = \frac{1}{\sqrt6}$
### method 5: [[arclen]] param. (based on m2)
implicit diff: $xx'-yy'+zz'=2yy'-2x'+z'=0$
=> $z'=0, x'=y'=\frac1{\sqrt2}$
another i.d.: $x'^2-y'^2+z'^2+xx''-yy''+zz''= 2y'^2+2yy'' -2x''+z''=0$
subs => $x''-y''+z''=1+2y''-2x''+z''=0$
=> $z''=-\frac13, x''=\frac13+t, y''=t$
=> $r'\times r''=r' \times (r''-t\sqrt2 r')=\frac1{3\sqrt2} (1, 1, 0) \times (1, 0, -1) = \frac1{3\sqrt2}(-1, 1, -1)$
=> $\kappa=\|r'\times r''\| = \frac1{\sqrt6}$

e.g. $\mathbf{r}=(e^{ -t }\sin t,e^{ -t }\cos t,e^{ t })$ at $t=1$
we have $\mathbf{r'}=(e^{ -t }(\cos t-\sin t), -e^{ -t }(\sin t+\cos t),e^{ t })$, $\mathbf{r''}=(-2e^{ -t }\cos t, 2e^{ -t }\sin t, e^{ t })$
=> $\mathbf{r'}\times \mathbf{r''}$ is $(-3\sin t-\cos t,\sin t-3\cos t,-2e^{ -t })$
=> $|\mathbf{r'}\times \mathbf{r''}|^{2}=4e^{ -2t }+10$ and $|\mathbf{r'}|^{2}=2e^{ -2t }+e^{ 2t }$ => $\kappa=\frac{\sqrt{ 4e^{ -2t }+10 }}{(2e^{ -2t }+e^{ 2t })^{3/2}}$, at $t=1$: $\kappa=\frac{\sqrt{ 4e^{ -2 }+10 }}{(2e^{ -2 }+e^{2})^{3/2}}$



