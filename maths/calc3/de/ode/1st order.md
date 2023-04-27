the [[ode]] of 1st order is the [[ode]] in the form $F(x,y,y')=0$

its other form is $y'=f(x,y)$

## existence and uniqueness
**theorem**: $f$ cont/$D\subset \mathbb{R}^{2}$, $(x_{0},y_{0})\in D$ then the ode $f(x,y,y')=f(x_{0})-y_{0}=0$ will
- have at least one solution
- if $\frac{\partial f}{\partial y}$ cont/$D$ then the solution is unique

see: http://www.math.toronto.edu/mpugh/Teaching/MAT267_19/Existence_and_Uniqueness_notes.pdf

## solve
the cauchy problem is this ode: $y'=f(x,y)$
the **general sol.** of this [[ode]] is $y=\varphi(x,C)$ s.t.
- $\varphi'=f(x,\varphi)$ for all $C$
- $\forall (x_{0},y_{0})\in D, \exists C=C_{0}, \varphi(x_{0},C_{0})=y_{0}$
the **general sol in integral/implicit form** is $\varphi(x,y,C)=0$
sols that can't be expressed as a general sol is called singular sols (nghiệm kì dị)

subbing $C=C_{0}$, one turn from a general sol => a specific sol

### 1o without $y$
general form: $F(x,y')=0$
- if $y'=f(x)$ => one can use integral to do the trick
- if $x=f(y')$, one let $t=y'$ => $x=f(t)$, $y=\int tf'(t) \, dt$
### 1o without $x$
general form: $F(y,y')=0$
let $y=f(t)$ => $y'=g(t)$ => $x=\int \frac{f'(t)}{g(t)} \, dt$
>note:  one can let $t=y$ or $t=y'$ to further simplify this)

e.g. $y^{2}+y'^{2}=4$
let $y=2\sin t$, $y'=2\cos t$
- if $\cos t\neq 0$ => $x=\int 1 \, dt=t+C$ => $y=2\sin(x+C)$ (general sol.)
- if $\cos t=0$ => $y'=0,y=\pm 2$ (singular sol.)

### phân ly biến số
if the [[ode]] is equiv to $f(y)dy=g(x)dx$ one can take the integral of both sides
e.g. $2\sqrt{ x }y'=\sqrt{ 1-y^{2} }$
- if $y=\pm 1$ => $y'=0$ => 2 singular sols
- otherwise
	- at $x=0$ => $y=\pm 1$
	- then $\frac{dy}{\sqrt{ 1-y^{2} }}=\frac{dx}{2\sqrt{ x }}$ => $\arcsin y=\sqrt{ x }+C$ (we can integrate because $x=0\in \partial D$)
	- to make $y$ cont (because $y'$ exists), we need $\arcsin y=C$ at $x=0$

e.g. $f(x)=1+2\int _{0}^{x} tf(t) \, dt$
denote thhe integral by $y(x)$ => $y'=xf(x)$
=> the eqn is equiv to $\frac{dy}{dx}=x(1+2y)$ => $\frac{dy}{1+2y}=xdx$ => ...

### thuần nhất
form: $y'=f\left( \frac{y}{x} \right)$
let $t=\frac{y}{x}$ => $y'=xt'+t$ => $x \frac{dt}{dx}+t=f(t)$ => $\frac{dt}{f(t)-t}=\frac{dx}{x}=d(\ln |x|)$
e.g. $2y'+\left( \frac{y}{x} \right)^{2}=-1$
we have $y'=-\frac{1+t^{2}}{2}$
using the formula, we have $\frac{dt}{-\frac{1+t^{2}}{2}-t}=d\ln |x|$
=> $\ln |x|=-\int \frac{2}{t^{2}+2t+1} \, dx=\frac{2}{1+t}+C=\frac{2x}{x+y}+C$

### linear
form: $y'+py=q$
#### using product rule
(this will give general sol.)
we need a fn $a$ s.t. $ay'+apy=(ay)'$, which means that $a'=ap$ => $\boxed{a=e^{ \int p(x) \, dx }}$
then $ay=\int aq(x) \, dx+C$ => $\boxed{y=\frac{1}{a}\left(\int aq \, dx+C\right)}$
(the integral denotes **an arbitary antiderivative**, not the set of all antidervs)

e.g. $xy'+y=x\sin x$, $y\left( \frac{\pi}{2} \right)=0$
we only care for $x$ in a neighborhood of $x=\frac{\pi}{2}$ => $x>0$
$p=\frac{1}{x}, q=\sin x$
we have $a=e^{ \int dx/x }=x$ => $y=\frac{1}{x}\left( \int x\sin x \, dx + C \right)=\frac{\sin x-x\cos x-1}{x}$

#### biến thiên hằng số
- find the sol $y_{1}$ of $y'+py=q$ ($y=\frac{C}{a}$)
- make $C$ deps on $x$ and sub => $C=\int aq \, dx+C_{0}$
this method sucks, u should use the above formula tbh

### bernoulli
form: $y'+py=qy^{\alpha}$
=> sub $v=y^{1-\alpha}$ it's linear: $v'+(1-\alpha)pv=(1-\alpha)q$

#### total derv. form
form: $pdx+qdy=0$, with $p,q$ depends on both $x,y$
- if one can find $u$ s.t. $\frac{\partial u}{\partial x}=p, \frac{\partial u}{\partial x}=q$ => $u(x,y)=C$ is the general sol. (this happens if $(p,q)$ has a [[scalar potential]] $u$ iff the curl = 0, or $\frac{\partial p}{\partial y}=\frac{\partial q}{\partial x}$)
- otherwise, one needs to find a multiplier $a$ s.t. $(ap,aq)$ has a [[scalar potential]] iff $\frac{\partial}{\partial x}(aq)=\frac{\partial}{\partial y}(ap)$
	- if $a=m(x)n(y)$ then $m'nq+mn \frac{\partial q}{\partial x}=mn'p+mn \frac{\partial p}{\partial y}$ => $\frac{m'}{m}q-\frac{n'}{n}p=\nabla \times(p,q)$ => $(\ln m)'q-(\ln n)'p=\nabla \times(p,q)$
	- one can denote $\alpha=(\ln m)', \beta=(\ln n)'$ => $\alpha q-\beta p=\nabla \times(p,q)$
	- if $n=1$, then $m=e^{ \frac{1}{q}\nabla \times(p,q) }$
e.g. (k66) $(x^{2}-y)dx+x(y+1)dy=0$
first, we calc the $\nabla \times(p,q)=-y-2$
=> we need to find $\alpha(x),\beta(y)$:
$\alpha(x^{2}-y)-\beta(xy+x)+y+2=0$
- let $\alpha=x$, $\beta=1$ => 
- 

