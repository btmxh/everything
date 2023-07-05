## general
general form: $F(x,y,y',y'')=0$
chính tắc form: $y''=f(x,y,y')$

## existence & uniqueness
similarly, if $y''=f(x,y,y')$ with $f, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial y'}$ cont on $D\subset \mathbb{R}^{3}$, with $(x_{0},y_{0},y_{0}') \in D$ then the [[ode]] has unique sol $y$ in a nbhd of $(x_{0},y_{0},y_{0}')$ s.t. $y(x_{0})=y_{0},y'(x_{0})=y_{0}'$

bla bla geom meaning

## without
### $F(x,y',y'')=0$
- let $y'=z$, then solve two [[1st order]] $F(x,z,z')=0$ and $y'=z$

### $F(y,y',y'')=0$
- let $y'=z$, to avoid confusion one let $z=y'_{x}$, $y''_{x}=\frac{dz}{dx}=\frac{dz}{dy}\cdot \frac{dy}{dx}=z'_{y}y'_{x}=pz'_{y}$
- => eq: $F(y,z,z'_{y})=0$, which is [[1st order]]

## e.g.
e.g. $yy''=2xy'^{2}$, with $y(2)=2,y'(2)=\frac{1}{2}$
- $u=\frac{y'}{y}$, then $y'=uy$ => $y''=uy'+u'y$ ($u'$ wrt $x$)
- note: $y\neq 0,y'\neq 0$
- then: $y(uy'+u'y)=2xy'^{2}$ => $y(u^{2}y+u'y)=2xu^{2}y^{2}$ $u^{2}+u'=2xu^{2}$, $u'=u^{2}(2x-1)$ =>$\frac{du}{u^{2}}=(2x-1)dx$ => $-\frac{1}{u}=x^{2}-x+C$ => $4-2+C=-4$ => $C=-6$
- $u=(\ln y)'=-\frac{1}{x^{2}-x-6}=\frac{1}{5} \ln \left| \frac{x-3}{x+2} \right|$ => $y=\sqrt[5]{ \frac{3-x}{2+x} }$ ($-2<x_{0}<3$)

e.g. $y''+y'+2y=xe^{ -x }$
- eq $y''+y'+2y=0$ => $y=e^{ -x/2 }\left( c_{1}\cos \frac{\sqrt{ 7 }}{2}x +c_{2}\sin \frac{\sqrt{ 7 }}{2}x \right)$
- eq $y''+y'+2y=xe^{ -x }$, assuming $y=p(x)e^{ -x }$, then
	- $y'=e^{ -x }(p'-p)$, $y''=e^{ -x }(p''-p'-(p'-p))=e^{ -x }(p''-2p'+p)$
	- then one needs $p''-2p'+p+p'-p+2p=x$ => $p''-p'+2p=x$ => let $p=ax+b$, then $p''=0$, $-a+2(ax+b)=x$ => $a=\frac{1}{2},b=\frac{1}{4}$ => $p=\frac{2x+1}{4}$
	- pick $C=0$, we have $y=\frac{2x+1}{4e^{ x }}$
- => solutions: $y=\frac{2x+1}{4e^{ x }}+e^{ -x/2 }\left( c_{1}\cos \frac{\sqrt{ 7 }}{2}x+c_{2}\sin \frac{\sqrt{ 7 }}{2}x\right)$
- 

e.g. $y''-2y'+y=e^{ x }(2x+\sin 2x)$
- homo sol: $y=e^{ x }(ax+b)$
- sol of $y''-2y'+y=e^{ x }(2x+\sin 2x)$:
	- let $y=e^{ x }p(x)$, then $y'=e^{ x }(p+p')$, $y''=e^{ x }(p''+2p'+p)$
	- then $e^{ x }(p''+2p'+p-2p-2p'+p)=e^{ x }(2x+\sin 2x)$ => $p''=2x+\sin 2x$ => pick $p=\frac{x^{3}}{3}-\frac{\sin 2x}{4}$
- => sol: $y=e^{ x }\left( \frac{x^{3}}{3}-\frac{\sin 2x}{4} +c_{1}x +c_{2}\right)$

e.g. $y''=4yy'$
- let $z=y'$, then $zz'=4yz$ => $z=0$ or $z'=4y$
- if $z=0$, then $y'=c$ and $y=cx+d$, sub back => $c=0$
- if $z'=4y$, then $y'=z=2y^{2}+c$, and we have several cases
	- $c=0$, then $\frac{dy}{2y^{2}}=dx$ => $x+\frac{1}{2y}$ const
	- $c>0$, then $\frac{dy}{2y^{2}+c}=dx$ => $\frac{1}{C\sqrt{ 2 }}\arctan \frac{y\sqrt{ 2 }}{C}=x+C'$ with some $C>0$
	- $c<0$, we have two cases
		- $y=\pm\sqrt{ -\frac{c}{2} }$, then $y'=y''=0$ => sing sol
		- $y \neq \pm \sqrt{ -\frac{c}{2} }$, then $\frac{dy}{2y^{2}+c}=dx$ and $\frac{1}{2\sqrt{ 2 }C}\ln \left| \frac{y-C}{y+C}\right|=x+C'$, with some $C>0$

### $F(x,y,y'')=0$
no general way to solve this xd

## special
### turn the ode into $\frac{d}{dx} f(x,y,y')=g(x,y)$
e.g. $yy''-y'^{2}-2xy^{2}=0$
- if $y\neq 0$, we have $\frac{yy''-y'^{2}}{y^{2}}=2x$ => $\left( \frac{y'}{y} \right)'=2x$ => $(\ln |y|)''=2x$ => $\ln y=\frac{x^{3}}{3}+ax+b$
- if $y=0$, then sing sol

## linear
form: $y''+p(x)y'+q(x)y=f(x)$
### homogenous
- $f(x)=0$
**theorem**: the sols of above eq forms a vector space (i.e. if $y_{1},y_{2}$ sol then $ay_{1}+by_{2}$ also sol)
**def**: two fns $y_{1},y_{2}$ are **LI** on $D$ iff there exists none $a,b\in \mathbb{R}$ s.t. $ay_{1}+by_{2}=0$ and $a^{2}+b^{2}>0$ for all params on $D$, otherwise they're **LD**
**def**: **wronskian** of two fns $y_{1},y_{2}$ is
$$
W(y_{1},y_{2})=
\begin{vmatrix}
y_{1} & y_{2}\\y'_{1} & y'_{2}
\end{vmatrix}
$$
one can use this det to prove/disprove LI/LD:
- if $y_{1},y_{2}$ LD then $W(y_{1},y_{2})=0$ for all $x\in D$
- if $W(y_{1},y_{2}) \neq 0$ for some $x_{0}\in D$, then $y_{1},y_{2}$ LI
**proof**
if $y_{1},y_{2}$ LD then wlog $y_{1}=ay_{2}$, we can easily calc the wronskian
the second statement is basically the reverse (or sth) of the first

**theorem**: let $y_{1},y_{2}$ be two sols of the homo eq, with $W\neq 0$ at some $x_0$ in $D$, and if $p,q$ cont on $D$, then $W(y_{1},y_{2})\neq 0$ for all $x\in D$
**proof**
the **abel's theorem** states that $W(y_{1},y_{2})(x)=Ce^{ -\int p(x) \, dx }$ (with arbitary constant of integration)
we have $W=y_{1}y_{2}'-y_{2}y_{1}'$ and $W'=y_{1}y_{2}''-y_{2}y_{1}''$ => $W'=-p(x)W$, and solving this DE yields $W(x)=Ce^{ -\int p(x) \, dx }$
then, if $p$ cont on $D$, the integral exists and therefore $W$ either is $0$ (if $C=0$) or non-zero (if $C \neq 0$)
**corollary:** $y_{1},y_{2}$ sols of homo eq and LI, then $W(y_{1},y_{2})\neq 0$ for all $x\in D$

**main theorem:** given two LI sols of the homo eq $y_{1},y_{2}$, then the general sol of the eq is $y=ay_{1}+by_{2}$

e.g. $y''-y=0$
we have two sol $y_{1}=e^{ x }$ and $y_{2}=e^{ -x }$, which are LI (one can calc the wronskian) => general sol is $y=C_{1}e^{ x }+C_{2}e^{ -x }$

**liouville**: if $y_{1}$ satisfy homo eq, then $y_{2}=y_{1}\int \frac{1}{y_{1}^{2}}e^{ -\int p(x) \, dx } \, dx$ is also another sol that LI with $y_{1}$
equivalently: $\frac{y_{2}}{y_{1}}=\int \frac{dx}{ay_{1}^{2}}, a=\int e^{ p(x) } \, dx$

some templates
- $y''+y=0$ => $y_{1,2}=\sin (x+\phi)$
- $y''+y'=0$ => $y_{1}=1$
- $p(x)=x$ => $y_{1}=x$
- $1+p+q=0$ for all $x$ => $y_{1}=e^{ x }$
- (basically try $1,x,e^{ x },e^{ ix }$)

### non-homo
assuming $Y$ is a sol of $y''+py'+qy=f$,
then $y_{0}-Y$ is a sol of $y''+py'+qy=0$ iff $y_{0}$ is a sol of $y''+py'+qy=f$
then we can conclude that all sols of $y''+py'+qy=f$ are in the form $y_{homo} + Y$

also, if $y_{1}$ sol of $\dots=f_{1}$, $y_{2}$ sol of $\dots=f_{2}$, then $y_{1}+y_{2}$ sol of $\dots=f_{1}+f_{2}$, so one can split $f$ to make finding $Y$ easier.

**lagrange's varying constant method**
solve $y''+py'+qy=0$ => $y=c_{1}y_{1}+c_{2}y_{2}$
solve $c_{1}'y_{1}+c_{2}'y_{2}=c_{1}'y_{1}'+c_{2}'y_{2}'-f(x)=0$, one can write $c_{1}',c_{2}'$ as functions of $f$: $c_{1}=\phi_{1}(x)+K_{1}, c_{2}=\phi_{2}(x)+K_{2}$, sub back to the above $y=c_{1}y_{1}+c_{2}y_{2}$

e.g. $y''-y'=\frac{2-x}{x^{3}}e^{ x }$
- $y''-y'=0$ => $y_{1}=e^{ x },y_{2}=1$
- let $y=c_{1}y_{1}+c_{2}y_{2}$, with $c_{1},c_{2}$ being functions of $x$
	- then $y'=c_{1}y_{1}'+c_{2}y_{2}'+(c_{1}'y_{1}+c_{2}'y_{2}=0)$
	- and $y''=(c_{1}y_{1}''+c_{2}y_{2}'')+(c_{1}'y_{1}'+c_{2}'y_{2}'=f(x))$
	- then, we can trivially see that $y$ is a solution of the equation.
- solving the system: $c_{1}'e^{ x }+c_{2}'=c_{1}'e^{ x }-\frac{2-x}{x^{3}}e^{ x }=0$
	- => $c_{2}'=\frac{x-2}{x^{3}}e^{ x }$, $c_{1}'=\frac{2-x}{x^{3}}$
	- => $c_{1}=\frac{x-1}{x^{2}}+C_{1}$,$c_{2}=\frac{e^{ x }}{x^{2}}+C_{2}$ (integration by parts)
=> sol: $y=\frac{e^{ x }}{x^{2}}+C_{1}+\left( \frac{x-1}{x^{2}}+C_{2} \right)e^{ x }=C_{1}+\left( \frac{1}{x}+C_{2} \right)e^{ x }$

e.g. $y''+4y=\frac{4}{\cos 2x}$
$y''+4y=0$ => $y_{1}=\sin 2x,y_{2}=\cos 2x$
system: $c_{1}'\sin 2x+c_{2}' \cos 2x=0$ and $2c_{1}'\cos 2x-2c_{2}' \sin 2x-\frac{4}{\cos 2x}=0$
then, $c_{1}'=,c_{2}'=$

### constant $p,q$
**trivial**
basically u solve $t^{2}+pt+q=0$, then we found a solution: $y=e^{ tx }$, with $t$ being a root of the eqn.
to avoid complex roots, one could simply take the real/imaginary part of $y$

e.g. $y''+2y'+2y=e^{ x }$
- solving $y''+2y'+2=0$: $t=-1\pm i$
=> $y=e^{ (-1\pm i)x }=e^{ -x }e^{ \pm ix }=e^{ -x }(\cos x\pm i\sin x)$
- find sol of orig: $y=\frac{e^{ x }}{5}$
- => sol: $y=\frac{e^{ x }}{5}+e^{ -x }(c_{1}\cos x+c_{2}\sin x)$

> when the eq have duplicate roots (i.e. $t^{2}=0$), one can use liouville to get $y_{2}=xy_{1}$

using the previously mentioned method, to solve $y''+py'+qy=f$ ($p,q$ const), we have $y=c_{1}e^{ t_{1}x }+c_{2}e^{ t_{2}x }$, with $c_{1}'e^{ t_{1}x }+c_{2}'e^{ t_{2}x }=c_{1}'t_{1}e^{ t_{1}x }+c_{2}'t_{2}e^{ t_{2}x }-f(x)=0$
- let $\Delta t=\frac{t_{1}-t_{2}}{2}$, then $c_{1}'=ue^{ -x\Delta t },c_{2}'=ue^{ x\Delta t }$, and as a result, $u(t_{1}e^{ x(t_{1}-\Delta t) }+t_{2}e^{ x(t_{2}+\Delta t) })=f$ => $u=\frac{f}{t_{1}+t_{2}}e^{ -x(t_{1}+t_{2})/2 }$
- then $c_{1,2}'=\frac{1}{t_{1}+t_{2}}f(x)e^{ -t_{1,2}x }$

but in the cases when $f$ is nice, we can do stuff like: (let $g(x)=x^{2}+px+q$)
- $f(x)=e^{ \alpha x }g(x)$, then one can let $y=e^{ \alpha x }z$ => $y^{(n)=e^{ \alpha x }(1+\alpha D)^{n}}z$, with $D$ being the *differentiation operator*.
- 

- $(z''+2\alpha z'+\alpha^{2}z) + p(z'+\alpha z)+qz=g(x)$, which may be easier to solve
- $f(x)=e^{ \alpha x }P(x)$, with $P$ being a polynomial
	- we can pick some polynomial $Q$ s.t. $Y(x)=e^{ \alpha x }Q(x)$ is a sol of the eqn.
		- if $\alpha$ k-sol of $t^{2}+pt+q=0$, then $Y(x)=x^{k}e^{ \alpha x }Q(x)$
	- => let $Y=e^{ \alpha x }Q(x)$, then we need $\alpha^{2}Q()$
	> alternatively, $c'_{1,2}=\frac{1}{t_{1}+t_{2}}e^{ (\alpha-t_{1,2})x }P(x)$, and one can proceed with solving this integral :skull: (ig?)
> 	or one can let $y=e^{ \alpha x }z$, ...
- $f(x)=P(x)\cos(\alpha x+\beta)$
	- since $\cos$ is basically $Re\{ e^{ i \text{Id} } \}$, we can apply the same thing: $Y(x)=\cos(\alpha x+\beta')Q(x)$
	- more formally, we write $f(x)=P\cos\alpha x+Q\sin \alpha x$, then we have two cases, assuming $\pm i\alpha$ k-sol ($k\leq 1$) of $t^{2}+pt+q=0$, then $Y=x^{k}(R\cos \alpha x+S\sin\alpha x)$
- $f(x)=e^{ \alpha x }$

e.g. $y''+5y'+6y=e^{ 3x }(x^{2}\sin x+3x\cos x+4)$
let $y=e^{ 3x }z$ => $y'=e^{ 3x }(z'+3z)$, $y''=e^{ 3x }(z''+6z'+9z)$
=> $z''+11z'+30z=x^{2}\sin x+3x\cos x+4$
- $t=z-\frac{2}{15}$, then $t''+11t'+30t=x^{2}\sin x+3x\cos x$
- => trivial: $\bar{y}=c_{1}e^{ -5x }+c_{2}e^{ -6x }$
- let $t=u\sin x+v\cos x$, then $t'=(u'-v)\sin x+(u+v')\cos x$, $t''=(u''-v'-u-v)\sin x+(u'-v+u'+v'')\cos x$
- $x^{2}=u''-u-v'-v+11(u'-v)+30u$ and $3x=2u'+v''-v+11(u+v')+30v$
- let $u,v$ be 2nd order polynomials, we can solve the thing :)))
- (the solution is not nice lmfao)

e.g. $y''+9y=\cos (x)^{2}$
trivial $\bar{y}=a\cos 3x+b\sin 3x$
we have $\cos(x)^{2}=\frac{1}{2}\cos 2x+\frac{1}{2}$
- $\frac{1}{2}$ => $Y_{1}=\frac{1}{18}$
- $\cos 2x$ => let $y=u\sin 2x+v \cos 2x$
	- => $y'=(u'-2v)\sin 2x+(v'+2u) \cos 2x$
	- => $y''=(u''-2v'-2(v'+2u))\sin 2x+(v''+2u'+2(u'+2v)) \cos 2x$$=(u''-4v'-4u)\sin 2x+(v''+4u'+4v) \cos 2x$
	- let $u,v$ be const, then: $y''=-4u \sin 2x+2v\cos 2x$ => LHS is $5u \sin 2x+11 \cos 2x$ => $Y_{2}=\frac{1}{22} \cos 2x$
	- (btw it should be $Y_{2}=\frac{1}{5}\cos 2x$) lmfao

e.g. $y''+3y'+2y=e^{ x }\cos(2x)$
> LHS is $\mathrm{Re}\{ e^{ x }e^{ i 2x} \}=\mathrm{Re}\{ e^{ x(1+2i) } \}$, so we will test $z=1+2i$ is whether a sol of $g(x)=x^{2}+3x+2$ or not (not) => multipliers is degree $0$

tbh we should use complex numbers to solve this:
$y''+3y'+2y=e^{ x(1+2i) }$, then let $y=Ae^{ x(1+2i) }$, and $(1+2i)^{2}+3(1+2i)+2=\frac{1}{A}$
=> $A=\frac{1}{2+10i}$
back to the reals: $y=\mathrm{Re}\left\{  \frac{e^{ x(1+2i) }}{2+10i}  \right\}=\frac{e^{ x }}{52}(5\sin 2x+\cos 2x)$

### euler
$x^{2}y''+pxy'+qy=0$
then we let $t=\ln|x|$ => $\frac{dy}{dx}=\frac{dy}{dt}\cdot \frac{dt}{dx}=\frac{1}{x}y'_{t}$ => $xy'_{x}=y'_{t}$
=> $\frac{d^{2}y}{dx^{2}}=-\frac{1}{x^{2}}y'_{t}+\frac{1}{x}\cdot \frac{d(y'_{t})}{dx}$ => $x^{2}y''_{xx}=-y'_{t}+y''_{tt}$ (note $\frac{d(y'_{t})}{dx}=y''_{t}\cdot \frac{dt}{dx}=\frac{1}{x}y''_{tt}$)
=> $y''_{tt}+(p-1)y'_{t}+qy=0$

we have $D(e^{ ax }f(x))=e^{ ax }(D+a)f(x)$ => $D^{n}(e^{ ax }f(x))=e^{ ax }(D+a)^{n}f(x)$


e.g. $y''-9y=e^{ 3x }\cos x$ (NO COMPLEX)
- $\bar{y}=c_{1}e^{ 3x }+c_{2}e^{ -3x }$
- $a=3,b=1 \implies z=3+i$ not sol of $x^{2}-9=0$ => $Y=e^{ 3x }(A\cos x+B\sin x)$
- => $Y'=\dots$
- anyways, we should do this instead
	- let $y=e^{ 3x }z$ => $y'=e^{ 3x }(z'+3z)$ => $y''=e^{ 3x }(D+3)^{2}z$
	- => $y''-9y=e^{ 3x }z((D+3)^{2}-9)=e^{ 3x }(D^{2}+6D)z$
	- then, we have $z''+6z'=\cos x$
	- pick $z=A\sin x+B\cos x$ => $z'=-B\sin x+A\cos x$, $z''=-A\sin x-B\cos x$ => $z''+6z'=-(A+6B)\sin x+(6A-B)\cos x=\cos x$ => $A=\frac{6}{37},B=-\frac{1}{37}$
	- => $y_{0}=\frac{e^{ 3x }}{37}(6\sin x-\cos x)$
- => done

e.g. $y^{(4)}-5y^{(2)}+4y=0$
e.g. $y''-5y'+4y=4x^{2}e^{ 2x }$
$y_{0}=c_{1}e^{ x }+c_{2}e^{ 4x }$
we have $y=ze^{ 2x }$ => $y^{(n)}=e^{ 2x }(D+2)^{n}z$
=> $((D+2)^{2}-5(D+2)+4)z=4x^{2}$
=> $(D^{2}-D-2)z=4x^{2}$
let $z=Ax^{2}+Bx+C$ => $D^{2}z=2A,Dz=2Ax+B$
=> $2A-2Ax-B-2Ax^{2}-2Bx-2C=4x^{2}$
=> $A=-2,B=2,C=-3$, $y=e^{ 2x }(-2x^{2}+2x-3)$

e.g. $y''-2y'+2y=(x+e^{ x })\sin x$
we will use lagrange here (doing the other thing is too time-consuming btw)
$y_{1}=e^{ x }\sin x,y_{2}=e^{ x }\cos x$
=> $y=e^{ x }(c_{1}\sin x+c_{2}\cos x)$ with:
- $c_{1}'y_{1}+c_{2}'y_{2}=0$ => $c_{1}'=k\cos x,c_{2}'=-k\sin x$
- $c_{1}'y_{1}'+c_{2}'y_{2}'=(x+e^{ x })\sin x$ => $ke^{ x }(\cos x(\sin x+\cos x)-\sin x(\cos x-\sin x))=(x+e^{ x })\sin x$
- => $k=\frac{(x+e^{ x })\sin x}{e^{ x }}=e^{ -x }x\sin x+\sin x$
- $c_{1}'=e^{ -x }x\sin x\cos x+\sin x\cos x$ => $c_{1}=\frac{e^{ -x }}{50}((5x-3)\sin 2x+(10x+4)\cos 2x)+C$
bla bla bla long ass functions

e.g. $y''-3y'+2y=\frac{1}{e^{ x }+1}$
$y_{1}=e^{ x },y_{2}=e^{ 2x }$
$c_{1}'e^{ x }+c_{2}'e^{ 2x }=0$ => $c_{1}'=-e^{ x }c_{2}'$
$c_{1}'e^{ x }+2c_{2}'e^{ 2x }=\frac{1}{e^{ x }+1}$ => $c_{2}'e^{ 2x }=\frac{1}{e^{ x }+1}$ => $c_{2}'=\frac{1}{e^{ 2x }(e^{ x }+1)}$, $c_{1}'=-\frac{1}{e^{ x }(e^{ x }+1)}$
solve e.g. $c_{1}=-\int \frac{1}{e^{ x }(e^{ x }+1)} \, dx=-\int \frac{1}{t^{2}(t+1)} \, d(t=e^{ x })=-\int \left( \frac{1}{t^{2}}-\frac{1}{t}+\frac{1}{t+1} \right) \, dt$$=\frac{1}{t}+\ln \frac{t+1}{t}=e^{ -x }+\ln(e^{ x }+1)-x$

e.g. $y''-2y'+y=\frac{e^{ x }}{x}$
$y_{1}=e^{ x }, y_{2}=xe^{ x }$ => $c_{1}'=-xc_{2}'$
=> $c_{1}'+(x+1)c_{2}'=\frac{1}{x}$ => $c_{2}=\ln |x|+C_{1}, c_{1}=-x+C_{2}$
=> $y=(\ln|x|+C_{1})xe^{ x }+(C_{2}-x)e^{ x }$

e.g. $(2x+1)y''+4xy'-4y=0$
$p=\frac{4x}{2x+1},q=-\frac{4}{2x+1}$
$y_{1}=x$ sol => liouville $y_{2}=y_{1}\int \frac{1}{y_{1}^{2}}e^{ -\int p \, dx } \, dx$
with $e^{ -\int p \, dx }=2x-\ln|2x+1|$ => integrand $\frac{e^{ -2x }(1+2x)}{x^{2}}dx=\frac{e^{ -2x }}{x^{2}}dx+\frac{2e^{ -2x }}{x}dx=e^{ -2x }d\left( -\frac{1}{x} \right)+\left( -\frac{1}{x} \right)d(e^{ -2x })$$=d\left( -\frac{e^{ -2x }}{x} \right)$ => $y_{2}=-e^{ -2x }$
=> $y=c_{1}x+c_{2}e^{ -2x }$

$x+y+z=0,x^{2}+y^{2}+z^{2}=4$
=> $z=-x-y,x^{2}+y^{2}+(x+y)^{2}=4$
=> $x^{2}+y^{2}+xy=2$
=> $\left( x+\frac{y}{2} \right)^{2}+\frac{3y^{2}}{4}=2$
=> $x+\frac{y}{2}=\sqrt{ 2 }\cos t, \frac{y\sqrt{ 3 }}{2}=\sqrt{ 2 }\sin t, z=-x-y$



