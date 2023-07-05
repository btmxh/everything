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
- if $x=f(y')$, one let $t=y'=\frac{dy}{dx}$ => $x=f(t)$, $y=\int tf'(t) \, dt$
### 1o without $x$
general form: $F(y,y')=0$
let $y=f(t)$ => $y'=g(t)$ => $x=\int \frac{f'(t)}{g(t)} \, dt$ ($y=f, \frac{dy}{dx}=g$ => $dx=\frac{df}{g}$)
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
- if one can find $u$ s.t. $\frac{\partial u}{\partial x}=p, \frac{\partial u}{\partial x}=q$ => $u(x,y)=C$ is the general sol. (this happens if $(p,q)$ has a [[scalar potential]] $u$ iff the curl = 0, or $\frac{\partial p}{\partial y}=\frac{\partial q}{\partial x}$) (then one calls this the *real* total form), root formula: $\int _{x_{0}}^{x} p(t,y_{0}) \, dt+\int _{y_{0}}^{y} q(x,t) \, dt=C$ (this repr the [[lineint]] along the path $(x_{0},y_{0})\to (x,y_{0})\to(x,y)$)
- otherwise, one needs to find a multiplier $a$ s.t. $(ap,aq)$ has a [[scalar potential]] iff $\frac{\partial}{\partial x}(aq)=\frac{\partial}{\partial y}(ap)$
	- if $a=m(x)n(y)$ then $m'nq+mn \frac{\partial q}{\partial x}=mn'p+mn \frac{\partial p}{\partial y}$ => $\frac{m'}{m}q-\frac{n'}{n}p=\nabla \times(p,q)$ => $(\ln m)'q-(\ln n)'p=\nabla \times(p,q)$
	- one can denote $\alpha=(\ln m)', \beta=(\ln n)'$ => $\alpha q-\beta p=\nabla \times(p,q)$
	- if $n=1$, then $m=e^{ \frac{1}{q}\nabla \times(p,q) }$
*actually* $\nabla \times(p,q)=q'_{x}-p'_{y}$, so we would have $p\beta(y)-q\alpha(x)=\nabla \times(p,q)$

e.g. $2xydx+(x^{2}-y^{2})dy=0$
- $\nabla \times(f,g)=0$ => we does not need to care about multiplier: $\frac{\partial u}{\partial x}=2xy, \frac{\partial u}{\partial y}=x^{2}-y^{2}$ => $u=x^{2}y-\frac{y^{3}}{3}$ => sol: $x^{2}y-\frac{y^{3}}{3}$ const

e.g. $(x+y^{2})dx-2xydy=0$
- $\nabla \times (f,g)=2y+2y=4y$
- => $\alpha(-2xy)-\beta(x+y^{2})=4y$ => pick $\alpha=-\frac{2}{x},\beta=0$ => $m=\frac{1}{x^{2}}$, $n=1$
- => $\frac{\partial u}{\partial x}=\frac{1}{x}+\frac{y^{2}}{x^{2}}, \frac{\partial u}{\partial y}=-\frac{2y}{x}$ => $u=\ln|x|-\frac{y^{2}}{x}$ const

e.g. (k66) $(x^{2}-y)dx+x(y+1)dy=0$
- first, we calc the $\nabla \times(p,q)=-y-2$
=> we need to find $\alpha(x),\beta(y)$:
$\alpha(x^{2}-y)-\beta(xy+x)+y+2=0$
(basically impossible)

- eqn equiv to $x^{2}dx+xydy=ydx-xdy$ => $dx+\frac{dy}{x}=-\frac{xdy-ydx}{x^{2}}=-d\left( \frac{y}{x} \right)$
- let $t = \frac{y}{x}$, then $\frac{dy}{x}=dt+\frac{tdx}{x}$
=> $dx+dt+\frac{tdx}{x}=-dt$ => $dx+\frac{tdx}{x}=-2dt$ => $(x+t)dx+2xdt=0$
- now we cook $\nabla \times(f,g)=1-2=-1$
	- => need $2\alpha x-\beta (x+t)=-1$
	=> pick $\alpha=0$, $\beta=-\frac{1}{2x}$ => $m=1, n=\frac{1}{\sqrt{ |x| }}$
	=> pick $\alpha=-\frac{1}{2x}$, $\beta=0$ => $m=\frac{1}{\sqrt{ |x| }}, n=1$
	- (wlog assume $x>0$), then we have $\frac{\partial u}{\partial x}=\sqrt{ x }+\frac{t}{\sqrt{ x }}$, $\frac{\partial u}{\partial t}=2\sqrt{ x }$ => $u=2t\sqrt{ x }+\frac{3x^{3/2}}{2}$
	- sub $y=tx$ => $\frac{4y}{\sqrt{ x }}+\frac{3x\sqrt{ x }}{2}=\frac{3x^{2}+8y}{2\sqrt{ |x| }}$ const is the solution of the de (TODO: what if $x\leq0$)
- or alternatively, let $t'$ be the derv of $t$ wrt $x$, then $2xt'+x+t=0$ => $t'+\frac{1}{2x}t=-\frac{1}{2}$ =>  $p=\frac{1}{2x},q=-\frac{1}{2}$ 
	- => $a=e^{ \int p(x) \, dx }=e^{ 1/2 \ln |x| }=\sqrt{ |x| }$
	- => $t=\frac{1}{\sqrt{ |x| }}\left( -\int \frac{\sqrt{ |x| }}{2}  \, dx +C \right)$
	- wlog $x>0$, then $t=\frac{1}{2\sqrt{ |x| }}\left( C-\frac{3x^{3/2}}{2} \right)$, or $2t\sqrt{ x }+\frac{3x^{3/2}}{2}=C$ => the two answers matches!

e.g. derive the $y=\frac{1}{a}\left( \int aq \, dx+C \right)$ formula using this method
- the equation $y'+py=q$ can be rewritten as $\frac{dy}{dx}+py=q$ => $(py-q)dx+dy=0$
- $\nabla \times(py-q,1)=\frac{\partial(py-q)}{\partial y}=p$
	- then $\alpha+\beta(py-q)=p$ => pick $\alpha(x)=p(x), \beta(y)=0$
	- then $n=1, m=a=e^{ \int p(x) \, dx }$, we have $\frac{\partial u}{\partial x}=a(py-q), \frac{\partial u}{\partial y}=a$ => $u=a(x)y+b(x)$, then $\frac{\partial u}{\partial x}=a'(x)y+b'(x)=apy-aq$ => $a'=ap, b'=-aq$
	- => $b=-\int aq \, dx$ (the former expr is true because of the definition of $a$) => $u=ay+b=C$ const => $y=\frac{1}{a}(C-b)=\frac{1}{a}\left( C+\int aq \, dx \right)$, qed

## examples
### "phương trình ko giải đc đvs đạo hàm"
e.g. $y'^{2}-y^{2}=0$
- then $y'=\pm y$ => $\ln|y|=\pm x+C$ => $|y|=e^{ \pm x+C }$
- since $y$ is cont (existence of $y'$), $y\neq 0$ for all $x$, then we know that the sign of $y$ does not change
- wlog assuming $y>0$, then if the $\pm$ sign above is not constant, then there must be a partition of $\mathbb{R}=A \cup B$ s.t. $y=e^{ x+C }$ for some $x\in A$, $y=e^{ -x+C }$ for some $x\in B$
- now, if $A$ is not closed, then $A\cup \partial A$ is closed, which means that $\partial A \setminus A \neq \emptyset$, then there are seq $a_{n}\subset A$,$b_{n}\subset B$ that both conv to $x_{0}\in\partial A \setminus A$, then one can calc $y'(x_{0})=\frac{de^{ x+C }}{dx}(x_{0})=\frac{de^{ -x+C }}{dx}(x_{0})$, the two expr does not coincides, which is a contradiction
- from the definition of a closed set, we know $B$ is open. we can do the same thing and get $A$ is open, then $\mathbb{R}$ can be partitioned into two disjoint open set, and by definition of connectedness, $\mathbb{R}$ is disconnected
- from https://math.stackexchange.com/questions/70415/showing-that-mathbbr-is-connected => we know that either $A$ or $B$ must be an empty set, which means that we have arrived at our final solution: either $y=e^{ x+C }$ for all $x$ or $y=e^{ -x+C }$ for all x
	- the proof mentioned is direct, we pick $a\in A,b\in B$ wlog $a<b$, then one consider the set $X=\{ \exists x\in[a,b], [a,x]\subset A \}\subset A$ and let $u=\sup X$, which is finite because $X$ is bounded
	- consider $J(\varepsilon)=B(u,\varepsilon)=(u-\varepsilon,u+\varepsilon)$
		- if $u>a$, we know $X\cap(u-\varepsilon,u]$ => $A \cap J(\varepsilon)$ then $J(\varepsilon) \not\subset B$, and since $B$ is open, $u \notin B$
		- if $u<b$, take $v=\min\{ u+\varepsilon,b \}\notin X, v>u$, then since $v\notin X$, we know $[a,v] \cap B$ => $[a,v]\setminus[a,u)=[u,v] \subset J(\varepsilon)$ intersect with $B$ => $J(\varepsilon) \not\subset A$ => $u \notin A$
	- if $u=a$, then by the second thing, $u\notin A$, contradiction
	- if $u=b$, then by the first thing, also contradiction
- nice ode lmfao
	- jk maybe our teachers will allow us to avoid this shithole

e.g. $8y'^{3}=27y$
let $y=8t^{3}$, then $\frac{dy}{dx}=3t$, then $\frac{dx}{dt}=\frac{dx}{dy}\cdot \frac{dy}{dt}=\frac{1}{3t}\cdot 24t^{2}=8t$ => $x=4t^{2}+C$

e.g. $(y'+1)^{3}=27(x+y)^{2}$
let $u(x)=x+y$ => $u'=y'+1$, then $u'^{3}=27u^{2}$, then let $u=t^{3}, u'=3t^{2}$ => $x=\int \frac{d(t^{3})}{3t^{2}dt} \, dt=t$

e.g. $y^{2}(y'^{2}+1)=1$
let $y=\cos t$, then $y'=\tan t$, $x=\int \frac{(\cos t)'}{\tan t} \, dt=-\sin t+C$

e.g. $xy'^{2}=y$
- let $u=y'$, then $y=u^{2}x$ => $dy=udx=u^{2}dx+2uxdu$ then $(u^{2}-u)dx+2uxdu=0 \implies(u-1)dx+2xdu=0$ ($y=0$ is a singular root idk)
- $\nabla_{x,u} \times(u-1,2x)=-1$ => pick $\alpha=-\frac{1}{2x},\beta=0$ => $mn=\frac{1}{\sqrt{ x }}$ =>$\frac{u-1}{\sqrt{ x }}dx+2\sqrt{ x }du=0$ => $d(2\sqrt{ x }(u-1))=0$ => $y'=1+\frac{C_{1}}{2\sqrt{ x }}$ => $y=x+C_{1}\sqrt{ x }+C_{2}$
- sub back: $x\left( 1+\frac{C_{1}}{2\sqrt{ x }} \right)^{2}=x+C_{1}\sqrt{ x }+C_{2}$ =>$C_{2}=\frac{C_{1}^{2}}{4}$

e.g. $y'^{3}+y^{2}=yy'(y'+1)$
then $y^{2}-y'^{2}y+y'^{3}-yy'=0\implies y(y-y'^{2})+y'(y'^{2}-y)=0$ => $(y-y')(y-y'^{2})=0$, which yields two roots $y_{1}=ke^{ x }, y_{2}=\frac{(x+C)^{2}}{4}$
- but muh continuity crap stfu no one cares anymore

e.g. $y'^{4}=y^{4}-y^{2}$
- let $t=y$ then $y'=\pm\sqrt[4]{ t^{2}-t^{4} }$ (wlog take $y>0$, $x=\int \frac{1}{\sqrt[4]{ t^{2}-t^{4} }} \, dt$ (complicated af integral)
- write $y'^{4}=\left( y^{2}-\frac{1}{2} \right)^{2}-\frac{1}{4}$=>$\left( 2y^{2}-1 \right)^{2}-(2y'^{2})^{2}=1$ => $2y^{2}-1=\cosh t,2y'^{2}=\sinh t$ => $y=\cosh \frac{t}{2},y'=\sqrt{ \frac{\sinh t}{2} }$
	- then $x=\int \frac{\frac{1}{2}\cosh \frac{t}{2}}{\sqrt{ \frac{\sinh t}{2} }} \, dt=\frac{1}{2}\int \frac{\cosh \frac{t}{2}}{\sqrt{ \sinh \frac{t}{2}\cosh \frac{t}{2} }} \, dt$$=\int \sqrt{ \coth \frac{t}{2} } \, d\left( \frac{t}{2} \right)$, still shit lmfao
	- => $x=\frac{1}{2}\ln \left| \frac{\sqrt{ \coth \frac{t}{2} } + 1}{\sqrt{ \coth \frac{t}{2} } - 1} \right|-\arctan \coth \frac{t}{2}+C$

e.g. $(xy'+3y)^{2}=7x$
then $(x^{3}y'+3x^{2}y)^{2}=7x^{7}$ => $(x^{3}y)'=\sqrt{ 7x^{7} }$ => $x^{3}y=\frac{9\sqrt{ 7 }x^{9/2}}{2}$ => $y=\frac{9\sqrt{ 7 }}{2}x^{3/2}$

e.g. $x=y'^{3}+y'$
let $u=y'=\frac{dy}{dx}$, then $x=u^{3}+u$, $y=\int dy=\int u \, dx=\int u(3u^{2}+1) \, du=\frac{3u^{4}}{4}+\frac{u^{2}}{2}+C$ bla bla

e.g. $y'=e^{ xy'/y }$
let $y'=u$, then $u=e^{ ux/y }$=>$\frac{ux}{y}=\ln u$ => $y=\frac{\ln u}{ux}$
=> $dy=udx=-\frac{\ln u}{ux^{2}}dx-\frac{\ln u-1}{u^{2}x}du$
=> $\left( u+\frac{\ln u}{ux^{2}} \right)du+\frac{\ln u-1}{u^{2}x}dx=0$ bruh
alternatively, we have $x=\frac{y\ln u}{u}$ => $dx=\frac{\ln u}{u}dy -\frac{y(\ln u-1)}{u^{2}}$
sub $dx=\frac{dy}{u}$, we have $\frac{\ln u-1}{u}dy-\frac{y(\ln u-1)}{u^{2}}du=0$
=> $u=e$ or $udy=ydu$
- $u=e$ idc
- $d(\ln u)=d(\ln |y|)$ => $u=y'=k|y|$, $x=\frac{y\ln k|y|}{k|y|}$, $y=\frac{u}{k}$, assuming $y>0$ then $x=\frac{\ln k+\ln y}{k}$ => $ky=e^{ kx }$ => $y=\frac{1}{k}e^{ kx }$

## mid-term
e.g. $2x^{2}y'=y^{2}(2xy'-y)$
we have $y^{3}dx-2x(y^{2}-x)dy=0$
- use total derv thing:
	- $\nabla \times(y^{3},2x(y^{2}-x))=3y^{2}-2y^{2}-4x=y^{2}-4x$
	- find $\alpha,\beta: \alpha(y)\cdot 2x(y^{2}-x)-\beta(x)\cdot y^{3}=y^{2}-4x$
	- hard
- let $x=u^{2}$
	- then $2y^{3}udu-2u^{2}(y^{2}-u^{2})dy=0$ => ezclap
	- $u=0$ => bla bla
	- otherwise: $y^{3}du-u(y^{2}-u^{2})dy=0$, now let $y=tu$, $t^{3}u^{3}du-u^{3}(t^{2}-1)(udt+tdu)=0$ => $t^{3}du-(t^{2}-1)(udt+tdu)=0$ => $tdu=(t^{2}-1)udt$ => $\frac{du}{u}=\frac{(t^{2}-1)dt}{t}$ => $\ln|u|=\frac{t^{2}}{2}-\ln|t| +C$ => $\frac{|ut|}{e^{ t^{2}/2 }}=C$ => $|y|=Ce^{ y^{2}/2x }$
- (if one wants to avoid $x>0$) let $u=y^{2}$, then $du=2ydy$ => $dy=\frac{du}{2y}$
	- $y^{4}dx-2xy(y^{2}-x)dy=0$ => $u^{2}dx-x(u-x)du=0$
	- let $u=tx$, then $t^{2}dx-(t-1)(xdt+tdx)=0$
	- => $tdx=(t-1)xdt$ => $\frac{dx}{x}=\frac{(t-1)dt}{t}$ => $\ln|x|=t-\ln|t|+C$ => $\frac{|xt|}{e^{ t }}=C$ => $\frac{y^{2}}{e^{ y^{2}/x }}=C$=> $y^{2}=Ce^{ y^{2}/x }$
	- edgecases:
		- $x=0$ => y=0, singular point
		- $y=0$, $y'=0$ singular solution

e.g.$y'^{3}-y'e^{ 2x }=0$
- if $y'=0$ => $y$ const sing. sol
- $y'^{2}=e^{ 2x }$ => either $y'=e^{ x }$ or $y'=-e^{ x }$ => $y=\pm e^{ x }+C$

e.g. $\left( 1+\frac{y}{x^{2}} \right)dx+\left( \frac{1}{x}+\frac{2y}{x^{2}} \right)dy=0$
- we have $(x^{2}+y)dx+(x+2y)dy=0$ => $d\left( \frac{x^{3}}{3} \right)+d(xy)+d(y^{2})=0$ => $\frac{x^{3}}{3}+xy+y^{2}$ const

e.g. $(\sin(y)^{2}+x\cot y)y'=1$
then $y'\neq 0$ => $x'=\frac{dx}{dy}$ exists and $\sin(y)^{2}+x\cot y=x'$ or $x'-x\cot y=\sin(y)^{2}$
- $a=e^{ \int \cot y \, dy }=e^{ \ln|\sin y|+C }=\sin y$ (pick)
- $x=\frac{1}{\sin y}\int \sin(y)^{3} \, dy=-\csc y \int (1-\cos(y)^{2}) \, d(\cos y)$$=\csc y\left( \frac{\cos(y)^{3}}{3}-\cos y \right)=\cot y\left( \frac{\cos(y)^{2}}{3}-1 \right)$

e.g. $(x^{2}-y)dx+x(y+1)dy=0$
- => $x^{2}dx+xydy=ydx-xdy$=> $dx+\frac{y}{x}dy=\frac{ydx-xdy}{x^{2}}=d\left( \frac{y}{x} \right)$
	- let $t=\frac{y}{x}$, then $y=xt$ => $dy=xdt+tdx$ => $dx+t(xdt+tdx)=dt$ => $(t^{2}+1)dx+(xt-1)dt=0$
	- we have $\nabla_{x,t}\times(t^{2}+1,xt-1)=2t-t=t$ => pick $\alpha=0,\beta=-\frac{t}{t^{2}+1}=(\ln n)'$ => $mn=\frac{1}{\sqrt{ t^{2}+1 }}$ => $\sqrt{ t^{2}+1 }dx+ \frac{xt-1}{\sqrt{ t^{2}+1 }}dt=0$ => $x\sqrt{ t^{2}+1 }-\operatorname{arsinh} t+C$ const
- => solution: $\sqrt{ x^{2}+y^{2} }-\operatorname{arcsinh}\left( \frac{y}{x} \right)$ const (and sing. sol $x=0$)
e.g. $y'=\frac{y}{3x-y^{2}}$
- if $y'=0$, then $y=0$ ok
- otherwise $x'$ exists, and $x'-\frac{3}{y}x=-y$
- $a=e^{ \int -3/y \, dy }=e^{ -3\ln y }=\frac{1}{y^{3}}$
- => $x=y^{3}\int -\frac{1}{y^{2}} \, dy=y^{3}\left( \frac{1}{y}+C \right)=y^{2}+Cy^{3}$

e.g. $(2x^{2}y\ln y-x)y'=y$
we have $(2x^{2}y\ln y-x)dy=ydx$ => $2x^{2}y\ln ydy=d(xy)$ =>
let $u=xy$ => $ydu=2u^{2}\ln ydy$ => $\frac{\ln y\,dy}{y}=\frac{du}{2u^{2}}$ => $\frac{1}{2}\ln|y|^{2}=-\frac{1}{2u}+C$ => $\ln|y|^{2}+\frac{1}{xy}$ const

e.g. $(xy'-y)^{2}=x^{2}-y^{2}$
we have $\left( \frac{xy'-y}{x^{2}} \right)^{2}=1-\frac{y^{2}}{x^{2}}$ => $\left( \frac{y}{x} \right)'^{2}=1-\frac{y^{2}}{x^{2}}$
let $t=\frac{y}{x}$ => $t'^{2}=1-t^{2}$ => $t^{2}+t'^{2}=1$ => $t=\sin u,t'=\cos u$, $x=\int \frac{(\sin u)'}{\cos u} \, dx=u$ => $t=\sin x$ =>$y=x\sin x$

e.g. $3e^{ x }\tan ydx+(2-e^{ x })(1+\tan(y)^{2})dy=0$
$\nabla \times(p,q)=\frac{3e^{ x }}{\cos ^{2}y}+e^{ x }(1+\tan (y)^{2})=4e^{ x }(1+\tan(y)^{2})$
$\alpha q-\beta p=4e^{ x }(1+\tan(y)^{2})$ => pick $\beta=0$, $\alpha=\frac{4e^{ x }}{2-e^{ x }}$ => $mn=e^{ \int 4/(2-t) \, d(t=e^{ x }) }=e^{ -4\ln(2-e^{ x }) }=\frac{1}{(2-e^{ x })^{4}}$
=> $\frac{3e^{ x }}{(2-e^{ x })^{4}}\tan ydx+ \frac{1}{\cos(y)^{2}(2-e^{ x })^{3}}dy=0$
=> $u=\frac{\tan y}{(2-e^{ x })^{3}}$ const
if $e^{ x }=2$, then $dx=0$ => singular sol.

e.g. $y'+\tan y=\frac{x}{\cos y}$
=> $y'\cos y+\sin y=x$
=> $(\sin y)'+\sin y=x$ => $u=\sin y$
- $u'+u=0$ => $u=Ce^{ -x }$
- $u'+u=x$ we have $u=x-1$
- => sol $\sin y=Ce^{ -x }+x-1$

e.g. $y'=cos(y-x)$
$u=y-x$ => $u'-1=\cos u$ => $\frac{du}{\cos u+1}=dx$


