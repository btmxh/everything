1. $\vec{f(t)}=\left( te^{ t }, t^{2}\cos t, \frac{1}{t^{2}+1} \right)$ find $\int \vec{f(t)} \, dt$
= $\left( \int te^{ t } \, dt, \int t^{2}\cos t \, dt, \int \frac{1}{t^{2}+1} \, dt \right)$
= $((t-1)e^{ t }, t^{2}\sin t+2t\cos t-2\sin t,\arctan t)+\vec{C}$

2.
a. $\iint_{D} \sqrt{ \frac{1-x^{2}-y^{2}}{1+x^{2}+y^{2}} }dxdy, D: x^{2}+y^{2}\leq 1,x\geq 0,y\leq 0$
let $x=r\cos t,y=r\sin t$, $t\in [-\frac{\pi}{2},0]$, then
$I=\frac{\pi}{2} \int _{0}^{1} r \sqrt{ \frac{1-r^{2}}{1+r^{2}} } \, dr=\frac{\pi}{4} \int _{0}^{1} \sqrt{ \frac{1-x}{1+x} } \, dx$
let $t=\sqrt{ \frac{1-x}{1+x} }$, then $t^{2}=\frac{1-x}{1+x}=\frac{2}{1+x}-1$ => $2tdt=-\frac{2}{(1+x)^{2}}dx$ => $tdt=-\frac{dx}{(1+x)^{2}}=-\frac{dx}{4}(t^{2}+1)^{2}$
=> $dx=\frac{4tdt}{(t^{2}+1)^{2}}$, then
$I=\pi\int _{0}^{1} \frac{t^{2}}{(t^{2}+1)^{2}}  \, dx$
$\int_{0}^{1} \frac{1}{t^{2}+1}\, dt=\frac{t}{t^{2}+1}|_{0}^{1}+2\int _{0}^{1} \frac{t^{2}}{(t^{2}+1)^{2}} \, dt$
=> $\frac{\pi}{4}=\frac{1}{2}+\frac{2}{\pi}I$ => $I=\frac{\pi}{2}\left( \frac{\pi}{4}-\frac{1}{2} \right)=\dots$

b. $\iiint_{D} z\sqrt{ x^{2}+y^{2} }dxdydz, D: y=-\sqrt{ 4x-x^{2} },$$y=0,z=0,z=4$
$D: 0\geq y\geq -\sqrt{ 4-(x-2)^{2} }, 0\leq z\leq 4$
=> $D: (x-2)^{2}+y^{2}\leq 4,y\leq 0,0\leq z\leq 4$

let $C: (x-2)^{2}+y^{2}\leq 4,y\leq 0$, then
$I=8\iint_{C}\sqrt{ x^{2}+y^{2} }dxdy$
then let $x=r\cos t,y=r\sin t$, for $t\in[-\pi,\pi]$ => $r^{2}-4r\cos t\leq 0$ => $r\leq 4\cos t$, then
$I=4\int _{-\pi}^{\pi} dt \int _{0}^{4\cos t} \, r^{2}dr=\frac{256}{3}\int _{-\pi}^{\pi} \cos ^{3}t \, dt=0$

3.
a. $\int _{C} (x+y) \, ds, C: \frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}=1$
this is 0 because even/odd bs
b.$\iint_{S}x^{2}dydz+y^{2}dxdz+z^{2}dxdy$, $S: x^{2}+y^{2}+z^{2}\leq a^{2},z\geq 0$, orientation downwards
since $S$ is reflective wrt $x=0,y=0$ (but not $z=0$), the integral is equal to $I=\iint_{S} z^{2}dxdy$
let $D: x^{2}+y^{2}\leq a^{2}$, then $I=-\int _{D} (a^{2}-x^{2}-y^{2})\,dxdy$, since the angle between $\hat{z}$ and $\hat{n}$ is not acute, and use the $r,t$ param, $I=-2\pi\int _{0}^{a} r(a^{2}-r^{2}) \, dr=-\pi\left( a^{4}-\frac{a^{4}}{2} \right)=-\frac{\pi a^{4}}{2}$
4.
a.
$\int _{0}^{e^{ -1 }} \frac{x^{b}e^{ -bx }-x^{a}e^{ -ax }}{-x+\ln x}(-xe^{ x }+e^{ x }) \, dx$
$f(x,t) = x^{t}e^{ -tx }$
$\frac{\partial f}{\partial t}=x^{t}e^{ -tx }\ln x-x\cdot x^{t}e^{ -tx }=x^{t}e^{ -tx }(\ln x-x)$
=> $\frac{x^{b}e^{ -bx }-x^{a}e^{ -ax }}{-x+\ln x}=\frac{f(x,b)-f(x,a)}{-x+\ln x}=\int _{a}^{b} x^{t}e^{ -tx } \, dt$
then $I=\int _{0}^{e^{ -1 }} \int _{a}^{b} \, x^{t}e^{ x(1-t) }(1-x) \, dtdx$
we can swap the integral because it's continuous on $[0,e^{ -1 }]\times[a,b]$, which results in
$I=\int _{a}^{b} \int _{0}^{e^{ -1 }} (x^{t}-x^{t+1})e^{ 1-tx } \, dx \, dt$
we have $\int _{0}^{e^{ -1 }} x^{t+1}e^{ 1-tx } \, dx=\int _{x=0}^{e^{ -1 }} x^{t+1} d\left( \frac{e^{ 1-tx }}{-t} \right)$$=\frac{x^{t+1}e^{ 1-tx }}{t}|_{0}^{e^{ -1 }}+\int _{x=0}^{e^{ -1 }} \frac{t+1}{t}x^{t}e^{ 1-tx } \, dx=$
=> $I=\int _{a}^{b}  \, dx$
sai de

b.
$\int _{0}^{\infty} \frac{\arctan 4x}{x(1+x^{2})} \, dx=\int _{0}^{\infty} \int _{0}^{4} \frac{1}{(1+x^{2})(1+t^{2}x^{2})} \, dt \, dx$
can change the order of integration because
- integrand continuous on $[0,\infty)\times[0,4]$
- integrand less than $\frac{1}{1+x^{2}}$ integratable on $[0,\infty]$

=> $I=\int _{0}^{4} \int _{0}^{\infty} \frac{1}{1-t^{2}}\left( \frac{1}{1+x^{2}}-\frac{t^{2}}{1+t^{2}x^{2}} \right) \, dx \, dt$
$=\int _{0}^{4} \frac{\pi}{2(1-t^{2})} \left( 1-t \right) \, dt=\frac{\pi}{2}\ln 5$

5.
trivial?

6.
a.
$\int _{C} \sqrt{ x^{2}+y^{2} }dx+y(xy+\ln(x+\sqrt{ x^{2}+y^{2} }))dy$, $C:(1,0)$ to $(3,0)$ along $x^{2}+y^{2}+3=4x,y\leq 0$
$P=\sqrt{ x^{2}+y^{2} }$
$Q=y(xy+\ln(x+\sqrt{ x^{2}+y^{2} }))$
$P'_{y}=\frac{y}{\sqrt{ x^{2}+y^{2} }}$, $Q_{x}'=y^{2}+\frac{y}{x^{2}+y^{2}}$
then we have $I=\int _{C} d\left( \frac{1}{2}(x\sqrt{ x^{2}+y^{2} }+y^{2}\ln(x+\sqrt{ x^{2}+y^{2} })) \right) + xy^{2}dy$
$=4+\int _{-\pi}^{0} (2+\cos t)\sin ^{2}t \cos t \, dt=4+\frac{\pi}{8}$
b.
$\int _{C} \frac{z^{2}}{x^{2}y^{2}+z^{4}}\left( ydx+xdy-\frac{2xy}{z}dz \right)$, $z=e^{ \sin \frac{\pi(x^{2}+y^{2})}{2} }+x$, from $(1,0,1+e)$ to $(1,1,2)$
we have the integrand is
$\frac{z^{2}}{(xy)^{2}+z^{4}}\left( d(xy)-\frac{2xy}{z}dz \right)$
$=\frac{z^{2}d(xy)-xyd(z^{2})}{(xy)^{2}+(z^{2})^{2}}=d\arctan\left( \frac{xy}{z^{2}} \right)$
use the gradient theorem, we have $I=\arctan\left( \frac{xy}{z^{2}} \right)|_{x=1,y=0,z=1+e}^{x=y=1,z=2}=\arctan \frac{1}{4}$

**exceptions**
- if $C$ contains points such that $\arctan\left( \frac{xy}{z^{2}} \right)$ is no longer differentiable, rip


1.
envelope of ellipses with area 4 and a common axis

let the common axes be $Ox,Oy$, then the ellipses were
$\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}=1$ with $\pi ab=4$ => $b=\frac{4}{\pi a}$
=> $F(x,y,a)=\frac{x^{2}}{a^{2}}+\frac{\pi^{2}a^{2}y^{2}}{16}-1$
=> no singular points, and $F'_{a}(x,y,a)=-\frac{2x^{2}}{a^{3}}+\frac{\pi^{2}ay^{2}}{8}$ => $16x^{2}=\pi^{2}a^{4}y^{2}$
=> $F(x,y,a)=\frac{\pi^{2}a^{4}y^{2}}{16a^{2}}+\frac{\pi^{2}a^{2}y^{2}}{16}-1=\frac{\pi^{2}a^{2}y^{2}}{8}-1=0$ if $\pi^{2}a^{2}y^{2}=8$
=> $y^{2}=\frac{8}{\pi^{2}a^{2}}$, $x^{2}=\frac{a^{2}}{2}$
=> $x^{2}y^{2}=\frac{4}{\pi^{2}}$: the envelope

2.
a. Area of shape bounded by $x^{2}=2y,x^{2}=3y,y^{2}=3x,y^{2}=4x$
let $u=\frac{x^{2}}{y},v=\frac{y^{2}}{x}$, then
$\frac{D(u,v)}{D(x,y)}=5$
=> $S=\iint_{2\leq u\leq 3, 3\leq v\leq 4} \frac{1}{5}dudv=\frac{1}{5}$

b. Area of sphere $x^{2}+y^{2}+z^{2}=9$ bounded by $(x^{2}+y^{2})^{2}=9(x^{2}-y^{2})$

let $x=3r\cos t,y=3r\sin t$
=> bounded by $81r^{4}=81r^{2}\cos 2t\implies r^{2}=\cos 2t$, with $t\in\left[ -\frac{\pi}{4}, \frac{\pi}{4} \right] \cup [\frac{3\pi}{4}, \frac{5\pi}{4}]$
Denote this 2d thing as $D$, then the surface area is
$S=\iint_{D} \sqrt{ 1+z_{x}'^{2}+z_{y}'^{2}}dxdy$
since $x^{2}+y^{2}+z^{2}$ const, $xdx+ydy+zdz=0$ => $z'_{x}=-\frac{x}{z},z'_{y}=-\frac{y}{z}$ => the sqrt above is $\frac{\sqrt{ x^{2}+y^{2}+z^{2} }}{|z|}=\frac{3}{|z|}$
wlog only consider the first quadrant => $x,y,z>0$, and
$\frac{S}{4}=\iint_{D} \frac{3dxdy}{\sqrt{ 9-x^{2}-y^{2} }}=\int _{-\frac{\pi}{4}}^{\pi/4} \int _{0}^{\sqrt{ \cos 2t }} \frac{r}{\sqrt{ 1-r^{2} }} \, dr \, dt$
$=\int _{-\frac{\pi}{4}}^{\pi/4} \sqrt{ 1-r^{2} }|_{\sqrt{ \cos 2t }}^{0} \, dt$
$=\int _{-\frac{\pi}{4}}^{\pi/4} (1-\sqrt{ 1-\cos 2t }) \, dt$
$=\int _{-\frac{\pi}{4}}^{\pi/4} (1-\sqrt{ 2 }\sin t) \, dt=\frac{\pi}{2}$
=> $S=2\pi$

3.
a.
$\oint_{L} (xy+x+y)dx+(xy+x-y)dy$, $L: x^{2}+y^{2}=6x$
we have $I=\oint_{L} d\left( xy+\frac{1}{2}x^{2}-\frac{1}{2}y^{2} \right)+\oint_{L} xy(dx+dy)$
the first oint is 0, so parameterize $x=3\cos t+3,y=3\sin t$
$I=\int _{0}^{2\pi} (3+3\cos t)\sin t(3\cos t-3\sin t) \, dt=-3\pi$

b.
mass of $S:z=\frac{1}{4}(x^{2}+y^{2}), 0\leq z\leq 1$ with density $\rho(x,y,z)=z$
$I=\iint_{S} zdS=\iint_{D} \frac{1}{4}(x^{2}+y^{2})\sqrt{ 1+\left( \frac{x}{2} \right)^{2}+\left( \frac{y}{2} \right)^{2} }dxdy$, with $D: x^{2}+y^{2}\leq 1$
param. => $I=\frac{\pi}{4}\int_{0}^{2} r^{2}\sqrt{ 4+r^{2} }dr$
sub $r=2\tan t$, then $I=4\pi \int _{0}^{\pi/4} \tan ^{2}t \sec^{3}t \, dt$
idk anymore

4.
a. $f(x)=\left( \int _{0}^{x} e^{ -t^{2} } \, dt \right)^{2}$, $g(x)=\int _{0}^{1} \frac{e^{ -x^{2}(1+t^{2}) }}{1+t^{2}} \, dt$
calc $f+g$

we calc $f'$ and $g'$:
$f'(x)=2e^{ -x^{2} }\int _{0}^{x}e^{ -t^{2} } \, dt$ (using the FTC)
$g'(x)=\int _{0}^{1} -2te^{ -x^{2}(1+t^{2}) } \, dt=\int _{0}^{x} -2e^{ -x^{2}-u^{2} } \, d(u=tx)$
- paraint, $f(t,x)=\frac{e^{ -x^{2}(1+t^{2}) }}{1+t^{2}}$ is cont on $[0,1]\times \mathbb{R}$
- $f'_{x}$ is also cont on that
=> $f'+g'=0$, which means that $f+g$ const

sub $x=0$ we have $f+g=\int _{0}^{1} \frac{1}{t^{2}+1} \, dt=\frac{\pi}{4}$
sub $x=\infty$ we have $f+g=\left( \int _{0}^{\infty} e^{ -t^{2} } \, dt \right)^{2}$, which implies the gaussian integral thing wtf (really nice exercise btw)

b. $\int _{0}^{\infty} \frac{e^{ -2x }-e^{ -3x }}{x} \, dx$
$I=\int _{0}^{\infty} \int _{2}^{3} e^{ -tx } \, dt \, dx=\int _{2}^{3} \int _{0}^{\infty} e^{ -tx } \, dx \, dt=\int _{2}^{3} \frac{1}{t} \, dt = \ln 3 - \ln 2$
we can reverse because bla bla:
- $f$ cont on $[0,\infty]\times[2,3]$
- $\int f \, dx$ uniconv because less than $e^{ -2x }$

5.
a. $\mathbf{F}=(x^{2}y+y^{2}z)\mathbf{i}+xyz\mathbf{j}+(yz^{2}+xy^{2})\mathbf{k}$
find non-rotating points

=> $\nabla \times \mathbf{F}=(z^{2}+xy)\mathbf{i}-(yz+x^{2})\mathbf{k}$
=> $z^{2}=-xy,x^{2}=-yz$
if $z=0$ then $x=0$, $y\in\mathbb{R}$
if $z\neq 0$ then $x,y\neq 0$
=> normalize $z=1$, then $x^{2}=-y,xy=-1$
=> $x=1,y=-1$ => sol: $x=z=-y$

b. volume bounded by $(x^{2}+y^{2}+z^{2})^{2}=9(x^{2}+y^{2}-z^{2})$
$x=r\cos u\cos v,y=r\cos u\sin v,z=r\sin u$
then, $r^{4}\leq 9r^{2}(\cos ^{2}u-\sin ^{2}u)=9r^{2}\cos 2u$
=> $r\leq \sqrt{ 3\cos 2u }$, $u\in\left[ -\frac{\pi}{4}, \frac{\pi}{4} \right]$

now one do the integral:
$V=\int _{0}^{2\pi} \, dv \int _{-\frac{\pi}{4}}^{\pi/4} \cos u \, du\int _{0}^{\sqrt{ 3\cos 2u }} r^{2}\, dr$
$=4\pi \int _{0}^{\pi/4} \cos u\cos 2u \sqrt{ 3\cos 2u } \, du$
$=4\sqrt{ 3 }\pi \int _{0}^{\pi/4} \cos u \cos ^{3/2} 2u \, du$
$=4\sqrt{ 3 } \pi \int _{0}^{\sqrt{ 2 }/2} (1-2t^{2})^{3/2} \, d(t=\sin u)$
$=4\sqrt{ \frac{3}{2} }\pi \int _{0}^{1} (1-w^{2})^{3/2} \, d(w=t\sqrt{ 2 })$
$=2\sqrt{ 6 }\pi \int _{0}^{\pi/2} \cos ^{4} t \, dt$, $w=\sin t$
$=2\sqrt{ 6 }\pi B\left( \frac{1}{2}, \frac{5}{2} \right)=\frac{3\pi^{2}}{4}\sqrt{ 6 }$

c. $\int _{(1,\pi)}^{(3,3\pi)} \left( 1-\frac{y^{2}}{x^{2}}\cos \frac{y}{x} \right)dx+\left( \sin \frac{y}{x}+\frac{y}{x}\cos \frac{y}{x} \right) \, dy$, along an arbitary path that does not cross $Oy$
$P'_{y}=-\frac{2y}{x^{2}}\cos \frac{y}{x}+\frac{y^{2}}{x^{3}} \sin \frac{y}{x}$
$Q'_{x}=-\frac{y}{x^{2}}\cos \frac{y}{x}-\frac{y}{x^{2}}\cos \frac{y}{x}+\frac{y}{x} \frac{-y}{x^{2}} (-\sin \frac{y}{x})$
basically they are equal, so we will integrate along $y=\pi x$
$\int _{1}^{3} (1-\pi^{2}\cos \pi)dx + (\sin \pi+\pi \cos \pi) \, dy$$=\int _{1}^{3} (1+\pi^{2}-\pi^{2}) \, dx=2$

1. envelope $y=c^{2}(x-c)^{2}$
single point: none
$F'(c)=2c(c-x)^{2}+2c^{2}(c-x)=2c(c-x)(2c-x)$

$c=0|x=c$ => $y=0$
$x=2c$ => $y=c^{4}$ => $x^{4}=16y$
=> $x^4=16y$ join $y=0$

2. switch order $\int _{0}^{a} \int _{\frac{a^{2}-x^{2}}{2a}}^{\sqrt{ a^{2}-x^{2} }}f(x,y) \, dy \, dx$
wlog assuming $a>0$
we have $0\leq x\leq a$, $y_{1}=\frac{a^{2}-x^{2}}{2a}\leq y\leq \sqrt{ a^{2}-x^{2} }=y_{2}$, or $y_{2}\leq y\leq y_{1}$
but since $y_{1}\leq y_{2}$ for all $x$, the task is ez
- $x^{2}+y^{2}\leq a^{2}$
- $a^{2}-x^{2}\leq 2ay$ => $x^{2}\geq a^{2}-2ay$

=> $a^{2}-2ay\leq x^{2}\leq a^{2}-y^{2}$
since $x\geq0$, $\sqrt{ a^{2}-2ay }\leq x\leq \sqrt{ a^{2}-y^{2} }$
we also have $y_{1,min}=0$, $y_{2,max}=a$
=> $0\leq y\leq a$
=> trivial

3. $x^{2}+y^{2}+z^{2}=4$ bounded by $(x^{2}+y^{2})^{2}=4(x^{2}-y^{2})$

4. $f(u,v)$ has cont partials on $\mathbb{R}^{2}$, $\frac{d}{da} \int _{0}^{a} f(x+a,x-a) \, dx$, $a\in \mathbb{R}$
- bound fns are $\alpha(a)=0, \beta(a)=a$ are cont and diff cont
- $f, f(x+a,x-a)'_{a}=f'_{u}(x+a,x-a)-f'_{v}(x+a,x-a)$ cont on $\mathbb{R}^{2}$
- => $I=\int _{0}^{a} (f'_{u}-f'_{v})(x+a,x-a) \, dx+f(2a,0)$
- we know that $\int _{0}^{a} (f'_{u}+f'_{v})(x+a,x-a) \, dx=\int _{0}^{a} f(x+a,x-a)'_{x} \, dx$
$=f(2a,0)-f(a,-a)$
=> $I-f(a,-a)=2\int _{0}^{a} f'_{u}(x+a,x-a) \, dx$...?

5. uniconv? $\int _{0}^{\infty} e^{ -xt^{2} } \, dt$ on $(0,\infty)$
assuming uniconv, then for $\varepsilon>0$, there exists $b$ s.t.
$\int _{b}^{\infty} e^{ -xt^{2} } \, dt <\varepsilon$ (well the integral decreases wrt $b$ so we can simplify like that)
the integrand is decreasing, so it's greater than $\int _{b}^{c} e^{ -xt^{2} } \, dt > (c-b)e^{ -xc^{2} }$ for all $c>b$
to make rhs > $\varepsilon$, we need $e^{ -xc^{2} } > \frac{\varepsilon}{c-b}$
pick $c$ s.t. rhs is less than 1, then one can always find $x$ s.t. lhs is greater than rhs => not uniconv

6. $\iint_{S} x^{3}dydz+y^{3}dzdx+z^{3}dxdy, S=\partial(\Sigma: x^{2}+y^{2}+z^{2}=4)$
divergence => $\iiint_{\Sigma}(x^{2}+y^{2}+z^{2})d^{3}\mathbf{r}$
sub => $\int _{0}^{2\pi} \, dv\int _{0}^{\pi} \sin u \, du \int _{0}^{2} r^{2} \, dr=\frac{32\pi}{3}$

7. $\vec{F}=-\frac{m}{r^{3}}\vec{r}$, $r=|\vec{r}|$ in 3d is a scalar potential field?
we need to find $u$ s.t. $\nabla u=-\frac{m}{r^{3}}\vec{r}$
we have $\nabla r^{2}=2\vec{r}$
$\nabla r^{n}=\nabla (r^{2})^{n/2}=\frac{n}{2}(r^{2})^{n/2-1}\nabla r^{2}=nr^{n-2}\vec{r}$
we would want $n-2=-3$ => $n=-1$
=> $\nabla\left( \frac{1}{r} \right)=-\frac{1}{r^{3}}\vec{r}$
=> $u=\frac{m}{r}$

=> not a scalar potential field because not well defined at $r=0$, but whatever

8. volume $(x^{2}+y^{2}+z^{2})^{2}=27x$
$x=r\cos t,y=r\sin t\sin u,z=r\sin t\cos u$
=> $r^{4}\leq 27r\cos t$
=> $r\leq 3 \sqrt[3]{ \cos t }$
$V=\int _{0}^{2\pi} \, du\int _{0}^{\pi/2} \sin tdt \int _{0}^{\sqrt[3]{ \cos t }} r^{2} \, dr$
$=\frac{2\pi}{3} \int _{0}^{\pi/2} \sin t\cos t \, dt=\frac{4\pi}{3}$

9. fuck you
10. $\int _{0}^{\infty} \frac{e^{ -at^{2} }-e^{ -bt^{2} }}{t} \, dt$
let $x=t^{2}$, then $I=\int _{0}^{\infty} \frac{e^{ -ax }-e^{ -bx }}{x} \, dx=\int _{0}^{\infty} \int _{a}^{b} e^{ -tx } \, dt \, dx$$=\int _{a}^{b} \int _{0}^{\infty} e^{ -tx } \, dx \, dt=\int _{a}^{b} \frac{1}{t} \, dt=\ln\left( \frac{b}{a} \right)$

1. $\iint_{S} (\frac{dydz}{x}+\dots)$, $S: \frac{x^{2}}{a^{2}}+\dots=1$, orientated outwards
consider $\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}+\frac{z^{2}}{c^{2}}=1$
=> $\frac{xx'}{a^{2}}+\frac{yy'}{b^{2}}+\frac{zz'}{c^{2}}=0$
=> $(x',y',z') \perp (\frac{x}{a^{2}}, \frac{y}{b^{2}}, \frac{z}{c^{2}})$
=> normal is $\left( \frac{x}{a^{2}}, \frac{y}{b^{2}}, \frac{z}{c^{2}} \right)$
=> $I=\int _{S} \left( \frac{1}{a^{2}}+\frac{1}{b^{2}}+\frac{1}{c^{2}} \right) \, dS=\left( \frac{1}{a^{2}}+\frac{1}{b^{2}}+\frac{1}{c^{2}} \right)S(S)$, with $S(S)$ being the surface area of the ellipsoid (not calculatable???)

2. volume $\left( \frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}} \right)^{n} +\frac{z^{2n}}{c^{2n}}=\frac{z}{h}\left( \frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}} \right)^{n-2}$
$x=ar\sin u\cos v,y=br\sin u\sin v,z=cr\cos u$
=> $r^{2n}(\sin ^{2n}u+\cos ^{2n}u)=\frac{c}{h}r^{1+2(n-2)}\cos u \sin ^{2(n-2)}u$
=> $r^{3}\leq \frac{c}{h} \frac{\sin ^{2n-4}u\cos u}{\sin ^{2n}u+\cos ^{2n}u}$

$V=\int _{0}^{2\pi} \, dv\int _{0}^{\pi/2} \sin u \, du\int _{0}^{\dots} r^{2} \, dr$
$=\frac{2\pi c}{3h} \int _{0}^{\pi/2} \frac{\sin ^{2n-3}\cos u}{\sin ^{2n}u+\cos ^{2n}u} \, du$
$=\dots$


3. $D: (x^{2}+y^{2})^{2}\leq 2a^{2}(x^{2}-y^{2})$ and $x^{2}+y^{2}\geq a^{2}$
$x=ar\cos t,y=ar\sin t$
=> $a^{4}r^{4}\leq 2a^{4}\cos 2t, r\geq 1$
=> $1\leq r\leq 2\cos 2t$
=> $\cos 2t\geq \frac{1}{2}$ => $2t=k2\pi+\exists\left[ -\frac{\pi}{3}, \frac{\pi}{3} \right]$
=> $t=k\pi+\exists\left[ -\frac{\pi}{6}, \frac{\pi}{6} \right]$

limit to $t\in\left[ 0, \frac{\pi}{6} \right]$ and take 4x the area
=> $S=4\int _{0}^{\pi/6} \int _{0}^{2\cos 2t} r\, dr \, dt=\dots$

4. tu lam
5. $\oint_{C: x^{2}+y^{2}=R^{2}} \frac{ydx-xdy}{(x^{2}+y^{2}+xy)^{2}}$ ($C$ positive orientation)
let $x=R\cos t,y=R\sin t$
=> $I=\int _{0}^{2\pi} \frac{-R^{2}}{(R^{2}+R^{2}\sin t\cos t)^{2}} \, dt$
$=-\frac{1}{R^{2}}\int _{0}^{2\pi} \frac{1}{(1+\sin t\cos t)^{2}} \, dt=\frac{16\pi}{3^{3/2}}$

1. curvature $x^{2}=2z,y^{2}=4z$ at $(\sqrt{ 2 },2,1)$
$\mathbf{r}=(\sqrt{ 2 },2,1)$
parameterize: $x=t,y=t\sqrt{ 2 },z=\frac{t^{2}}{2}$
=> $\mathbf{r'}=(1,\sqrt{ 2 },t)=(1,\sqrt{ 2 },\sqrt{ 2 })$ => $r'=\sqrt{ 5 }$
=> $\mathbf{r''}=(0,0,1)$
=> $|\mathbf{r'}\times \mathbf{r''}|=\sqrt{ 3 }$
=> $\kappa=\frac{\sqrt{ 3 }}{5^{3/2}}=\dots$

2. switch order $\int _{0}^{4} \, dx \int _{\sqrt{ 4x-x^{2} }}^{\sqrt{ 8x }} f(x,y) \, dy$
we have $\sqrt{ 8x }>\sqrt{ 4x-x^{2} }$ for all $x\in[0,4]$
=> $y\in [0,4\sqrt{ 2 }]$, and $\sqrt{ 4x-x^{2} }\leq y \leq \sqrt{ 8x }$
=> $(x-2)^{2}+y^{2}\geq 4, x\geq \frac{y^{2}}{8}$
=> $x\geq \frac{y^{2}}{8}$ and ($x\geq 2+\sqrt{ 4-y^{2} }$ or $x\leq 2-\sqrt{ 4-y^{2} }$)
=> we need to split into three parts
- $0\leq y\leq 2$
	- $\frac{y^{2}}{8}\leq x\leq 2-\sqrt{ 4-y^{2} }$ => $\int _{0}^{2} \int _{y^{2}/8}^{2-\sqrt{ 4-y^{2} }} f(x,y) \, dx \, dy$
	- $x\geq \frac{y^{2}}{8}, 2+\sqrt{ 4-y^{2} }$ => $\int _{0}^{2} \, dy\int _{2+\sqrt{ 4-y^{2} }}^{4} f(x,y) \, dx$
- $2\leq y\leq 4\sqrt{ 2 }$
	- => $\int _{2}^{4\sqrt{ 2 }} \, dy \int _{y^{2}/8}^{2} f(x,y) \, dx$

3. volume $x^{2}+y^{2}=2x,x^{2}+y^{2}=2y,z=x+2y,z=0$
$x=r\cos t,y=r\sin t$
=> $r^{2}\leq 2r\sin t,2r\cos t$
=> $r\leq 2\sin t,2\cos t$

=> $V=\int _{0}^{\pi/2}  \, dt\int _{0}^{\min\{\sin t,\cos t\}} r^{2}(\cos t+2\sin t)\, dr$
$=\int _{0}^{\pi/2} (2\sin t+\cos t) \frac{\min \{ \sin t,\cos t \}^{3}}{3} \, dt$
$=\frac{1}{3}\int _{0}^{\pi/4} ((2\sin t+\cos t)\cos ^{3}t+(\sin t+2\cos t)\sin ^{3}t) \, dx$
$=\dots$

4. $\int _{0}^{1} \frac{dx}{\sqrt[30]{ 1-x^{30} }}$
$t=x^{30}$ => $x=t^{1/30}$ => $dx=\frac{1}{30}t^{-29/30}dt$
=> $I=\int _{0}^{1} \frac{t^{-29/30}dt}{30(1-t)^{1/30}}=\frac{1}{30}\int _{0}^{1} t^{-29/30}(1-t)^{-1/30} \, dt=\frac{1}{30}B\left( \frac{1}{30}, \frac{29}{30} \right)$
$=\frac{\pi}{30 \sin \frac{\pi}{30}}$

5. $\int _{0}^{1} \frac{x^{3}-x^{4}}{\ln x} \, dx$
let $x=e^{ -t }$, then $I=-\int _{0}^{+\infty} \frac{e^{ -3t }-e^{ -4t }}{ t } \, e^{ -t }dt=-\int _{0}^{+\infty} \int _{4}^{5} e^{ -at } \, da \, dt$
$=-\int _{4}^{5} \frac{1}{a} \, da=\ln 5 - \ln 4$

6.$\iint_{S} y^{2}zdxdz+xzdydz+x^{2}ydxdy$, $\partial S: z=x^{2}+y^{2},x^{2}+y^{2}=1,x=0,y=0,z=0$
$\nabla \cdot f=2yz+z$
=> $\iiint_{V} (2yz+z)dxdydz$, $S=\partial V$
param. $x=r\cos t,y=r\sin t,z=z$
=> $t\in\left[ 0, \frac{\pi}{2} \right]$, $0\leq z\leq r\leq 1$
=> $I=\iiint_{V}z(2r\sin t+1)rdrdtdz=\dots$

7. $\vec{F}=(x^{2}y+y^{2}z,xyz,yz^{2}+xy^{2})$
find "điểm xoáy"
$\nabla \times \vec{F}=(xy+z^{2},0,-x^{2}-yz)$
=> not $xy+z^{2}=x^{2}+yz=0$
=> not ...

10. $\int _{C} e^{ x^{2}y }\left( \left( 2xy\sqrt{ x+y^{2} }+\frac{1}{2\sqrt{ x+y^{2} }} \right)dx+\left( x^{2}\sqrt{ x+y^{2} }+\frac{y}{\sqrt{ x+y^{2} }} \right)dy \right)$
$C: y^{3}=1+x^{5}$, from $(0,1)$ to $(1,\sqrt[3]{ 2 })$
first, we have
$\frac{1}{2\sqrt{ x+y^{2} }}dx+\frac{y}{\sqrt{ x+y^{2} }}dy=d\sqrt{ x+y^{2} }$, let $z=\sqrt{ x+y^{2} }$
=> $e^{ x^{2}y }(2xyzdx+dz+x^{2}zdy)=e^{ x^{2}y }dz+ze^{ x^{2}y }(2xydx+x^{2}dy)$
$=e^{ x^{2}y }dz+ze^{ x^{2}y }d(x^{2}y)$
let $t=x^{2}y$, then $=e^{ t }dz+ze^{ t }dt=d(ze^{ t })$
Hence, the integral is path-independent, and one can calculate the integral as $ze^{ t }|_{z=1,t=0}^{z=\sqrt{ 1+\sqrt[3]{ 4 } },t=\sqrt[3]{ 2 }}=\dots$

1. tangent & normal at $(1,\sqrt{ 2 },3)$
of curve $2(x-1)^{2}+3y^{2}=6,z=x^{2}+y^{2}$

implicit diff.
$2(x-1)x'+6yy'=2xx'+2yy'-z'=0$
=> $y'=0,2x'-z'=0$
=> tangent vector: $(1,0,2)$

=> tangent: $\mathbf{r}=(1,\sqrt{ 2 },3)+(1,0,2)t$
normal: $(\mathbf{r}-(1,\sqrt{ 2 },3)) \cdot(1,0,2)=0$

2. $\iint_{S} (x^{2}y^4+e^{ x^{2}+y^{4} }\sin y^{5})dxdy$, $S: 3x^{2}+2y^{2}\leq 6$
second term odd wrt y and $S$ reflective wrt $y=0$
calc first term via letting $x=\sqrt{ 2 }r\cos t,y=\sqrt{ 3 }r\sin t$

1. 