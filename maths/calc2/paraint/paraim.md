the improper integral $I(y)=\int _{a}^{b_{0}} f(x,y)dx$ (singularity only at $b_{0}$) can be thought as the limit of $I_{b}(y)=\int _{a}^b f(x)dx$ as $b\to b_{0}$

then we can define [[uniconv]] to this shit as
- $I(y)$ conv at $y_{0}$ iff $\exists I(y_{0})$
- $I(y)$ conv on $[c,d]$ iff $I(y)$ conv at all $y_{0} \in [c,d]$
- $I(y)$ [[uniconv]] on $[c,d]$ iff $\forall \varepsilon>0, \exists$ neighborhood $A$ of $b$ s.t. $|\int _{b}^{b_{0}}f(x,y_{0}) \, dx|<\varepsilon$ for all $b \in A, y_{0} \in [c,d]$

## cont
since uniform cont can't be inferred from $[a,\infty]$, we can't just have $f_{n}$ cont => $f$ cont like [[paraint]]
we need one additional cond: [[uniconv]]
proof is at the [[uniconv#properties#cont]]

## int8
cond: $f$ cont/$[a,b_{0})\times$(y-space $Y$) + [[uniconv]]
$$
\int _{Y} I(y)\, dy =\int _{a}^{b_{0}} \int _{Y} f(x,y) \, dy  \, dx 
$$
TODO: nxt's corollary

e.g. $\int _{0}^{+\infty} \frac{e^{ -ax }-e^{ -bx }}{x} \, dx$, for $a,b>0$
- let $f(x,t)=e^{ -tx }$ ($t\geq a$), then $\int _{a}^{b} f(x,t) \, dt=\frac{e^{ -ax }-e^{ -bx }}{x}$, and $f$ cont on $[0,+\infty)\times[a,+\infty)$
- to prove [[uniconv]], one use [[weierstrass m-test]] with $f(x,t)\leq e^{ -ax }$ conv to $\frac{1}{a}$
- then $\int _{0}^{\infty} \frac{e^{ -ax }-e^{ -bx }}{x} \, dx=\int _{0}^{\infty}\int _{a}^{b}e^{ -tx } \, dt \, dx=\int _{a}^{b}\int _{0}^{\infty}e^{ -tx } \, dx \, dt$$=\int _{a}^{b} \frac{1}{t} \, dt=\ln(b)-\ln(a)$

## diff.
cond: $f,f'_{y}$ cont/xy-space (excluding limit point of $x$) + $\int f'_{y}(x,y)dx$ [[uniconv]]  (+ ofc $\int f(x,y)dx$ cont)

e.g. $I(y)=\int _{0}^{\infty} ye^{ -yx } \, dx$ on $[y_{0},+\infty)$, $(0,+\infty)$
- have: $\int _{b}^{\infty} ye^{ -xy } \, dx=e^{ -by }$, then
	- if $y\geq y_{0}$, one can pick $b$ s.t. $e^{ -by }$ is arbitary small (i.e. pick $b$ s.t. $e^{ -by_{0} } < \varepsilon \iff b > -\frac{1}{y_{0}}\ln\varepsilon$)
	- when $y$ can freely accept any value on $(0, +\infty)$, as $y\to 0$, $e^{ -by }\to 1$, which is not zero => not [[uniconv]]

e.g. $I(y)=\int _{0}^{+\infty} e^{ -xy } \frac{1}{y^{2}+\sqrt{ x }} \, dx$
- $a(x,y)=e^{ -xy }, b(x,y)=\frac{1}{y^{2}+\sqrt{ x }}$
- then for $y\geq y_{0}>0$, $\int _{0}^{+\infty}a(x,y) \, dx$ is conv., $b(x,y)$ dec. wrt $x$ and [[uniconv]] to $0$ as $x\to \infty$

e.g. prove diff. $I(y)=\int _{0}^{\infty} \frac{\sin(x^{2}+2y+2)}{1+x^{4}+y^{2}} \, dx$
- $f(x,y)$=integrand => cont
- $f'_{y}(x,y)=\frac{blabla}{(1+x^{4}+y^{2})^{2}}$ cont
- $I(y)$ exists because less than $\frac{1}{1+x^{4}}$
- [[uniconv]]
	- $f'_{y}=\frac{2\cos(x^{2}+2y+2)(1+x^{4}+y^{2})-\sin(x^{2}+2y+2)(2y)}{(1+x^{4}+y^{2})^{2}}$
	- then $|f'_{y}|\leq \frac{2(1+x^{4}+y^{2})+2|y|}{(1+x^{4}+y^{2})^{2}}\leq \frac{3}{1+x^{4}+y^{2}} \leq \frac{3}{1+x^{4}}$uniconv by [[weierstrass m-test]]
e.g. $\lim_{ y \to 0^{+} } \int _{0}^{+\infty}ye^{ -yx } \, dx \neq \int _{0}^{+\infty} \lim_{ y \to 0^{+} } ye^{ -yx } \, dx$
e.g. $\int _{0}^{+\infty} \frac{\arctan(x^{2}+y+1)}{e^{ 2x+y^{2} }} \, dx$
e.g. $\int _{0}^{+\infty} \frac{y^{2}}{x^{2}+y^{2}+1} \, dx$

> diff. under the int. sign manual (useless tbh i knew all of this)
> step 1: find $I'(y)$ by doing stuff: $I'(y)=\int _{a}^{\infty} f'_{y}(x,y) \, dx$
> step 2: then find $I(y)=\int I'(y) \, dy+C$
> step 3: find $C$ by calculating $I(y_{0})$ for some special $y_{0}$

e.g. $\int _{0}^{1} \frac{x^{b}-x^{a}}{\ln x} \, dx$
- $f(x,y)=\frac{x^{y}-x^{a}}{\ln x}$, at $x=1$, value is $b-a$, at $x=0$ value is 0 => cont/$[0,1]\times[a,+\infty)$
- $f'_{y}(x,y)=x^{y}$ cont/$[0,1]\times[a,+\infty)$
- => [[paraint]], $I'(b)=\int _{0}^{1} x^{b} \, dx=\frac{1}{b+1}$=> $I(b)=\ln(b+1)-\ln(a+1)$
e.g. $\int _{0}^{+\infty} \frac{e^{ -ax^{2} }-e^{ -bx^{2} }}{x^{2}} \, dx$
- $f(x,y)=\frac{e^{ -ax^{2} }-e^{ -yx^{2} }}{x^{2}}$, when $x=0$, $f=y-a$ => cont / $[0, +\infty)\times[a,+\infty)$, the int. conv because as $x\to \infty$, $f$ asymp. less than $e^{ -(y+\varepsilon)x^{2} }$ conv
- $f'_{y}=e^{ -yx^{2} }$ cont / $\mathbb{R}^{2}$, less than $e^{ -ax^{2} }$ which conv to $\sqrt{ \frac{\pi}{a} }$ => [[uniconv]] by [[weierstrass m-test]]
- => $I'(y)=\int _{0}^{\infty} e^{ -yx^{2} } \, dx=\sqrt{ \frac{\pi}{y} }$=> $I(y)=2\sqrt{ \pi y }-2\sqrt{ \pi a }$
e.g. $\int _{0}^{\infty} \frac{e^{ -ax }-e^{ -bx }}{x} \, dx$
similarly to the prev e.g., one have $I'(b)=\int _{0}^{\infty} e^{ -bx } \, dx=\frac{1}{b}\implies I(b)=\ln(b)-\ln(a)$
e.g. $\int _{0}^{\infty} \frac{dx}{(x^{2}+y)^{n+1}}$
- let LHS be $I_{n}(y)$, $f_{n}(x,y)=\frac{1}{(x^{2}+y)^{n+1}}$
- we will only talk about $y>0$ => analyze $f_{n}$ on $[0, +\infty) \times [\varepsilon, +\infty)$ => cont, conv by [[comparison test]]
- $f'_{n,y}(x,y)=-\frac{n+1}{(x^{2}+y)^{n+2}}=-(n+1)f_{n+1}(x,y)$, then this cont, but to prove [[uniconv]], one uses [[weierstrass m-test]] to compare $f_{n+1}$ with $\frac{1}{(x^{2}+\varepsilon)^{n+1}}$, which is less than $\frac{1}{x^{2}+\varepsilon}$ as $x\to \infty$ => qed
- then $I'_{n}(y)=-(n+1)I_{n+1}(x,y)\implies I_{n+1}=-\frac{I'_{n}}{n+1}$
- let $n=0$, we have $I(0)=\int _{0}^{\infty} \frac{dx}{x^{2}+y} \, dx=\frac{\pi}{2\sqrt{ y }}$
- **the rest is trivial and left as an exercise for my lecturers**

e.g. $\int _{0}^{\infty} \left( \frac{e^{ -ax }-e^{ -bx }}{x} \right)^{2} \, dx$
- $f(x,y)=\left( \frac{e^{ -ax }-e^{ -yx }}{x} \right)^{2}$, then $f'_{y}=\frac{2(e^{ -ax }-e^{ -yx })}{x}e^{ -yx }$ and $f''_{yy}=-2e^{ -(a+y)x }+4ye^{ -2yx }$
- these things satisfy the conds ig ($f$ cont, asymp. to $e^{ -2(y+\varepsilon)x^{2} }$ conv, similar with $f'_{y}$ and $f''_{yy}$, [[uniconv]] via [[weierstrass m-test]])
- then $I''(y)=\int _{0}^{\infty}(4ye^{ -2yx }-2e^{ -(a+y)x }) \, dx=2-\frac{1}{y+a}$
- taking the integral => $I(y)=x^{2}+(y+a)\ln(y+a)-y+C$
alternatively, one can do
$$
\begin{align}

&\int _{0}^{\infty} \left( \frac{e^{ -ax }-e^{ -bx }}{x} \right)^{2} \, dx \\
=&\int _{0}^{\infty} \frac{e^{ -ax }-e^{ -bx }}{x} \int _{a}^{b} e^{ -yx } \, dy  \, dx  \\
=& \int _{0}^{\infty} \int _{a}^{b} \frac{e^{ -(a+y)x } - e^{ -(b+y)x }}{x} \, dy  \, dx  \\
=& \int _{a}^{b} \int _{0}^{\infty} \frac{e^{ -(a+y)x } - e^{ -(b+y)x }}{x} \, dx  \, dy \text{ (1)}  \\
=& \int _{a}^{b} \int _{0}^{\infty} \int _{a+y}^{b+y} e^{ -zx } \, dz  \, dx  \, dy \\
= & \int _{a}^{b} \int _{a+y}^{b+y} \int _{0}^{\infty} e^{ -zx } \, dz  \, dx  \, dy \text{ (2)}  \\
=& \int _{a}^{b} \int _{a+y}^{b+y} \frac{1}{x} \, dx  \, dy \\
=&\dots 
\end{align}
$$
- we switch the integrating order twice at $(1)$ and $(2)$, here's the clarification (both using [[weierstrass m-test]])
	- 1: we need $\int _{0}^{\infty} \frac{e^{ -(a+y)x }-e^{ -(b+y)x }}{x} \, dx$ to be [[uniconv]] for $y\in [a,b]$, this is true because the (abs) numerator. is less than $e^{ -2ax }$
	- 2: we need $\int _{0}^{\infty} e^{ -zx } \, dx$ to be [[uniconv]] for $z\in [a+y,b+y] \subset[2a,2b]$, this is true because $e^{ -zx } \leq e^{ -2ax }$

e.g. $\int _{0}^{\infty} \frac{e^{ -ax }-e^{ -bx }}{x}\sin mx \, dx$
- use the above trick, integrand = $\int _{a}^{b} e^{ -yx }\sin mx \, dy$
- to change order, we need $\int _{0}^{\infty} e^{ -yx }\sin mx \, dx$ uniconv as $y\in[a,b]$, true by [[weierstrass m-test]]: $\left|\int _{0}^{\infty} e^{ -yx }\sin mx \, dx\right|\leq \int _{0}^{\infty} e^{ -ax } \, dx=\frac{1}{a}$
- then $I=\int _{a}^{b} \int _{0}^{\infty} e^{ -yx }\sin mx \, dx \, dy=\int _{a}^{b} \frac{m}{y^{2}+m^{2}} \, dy$$=\ln \sqrt{ y^{2}+m^{2} }$

e.g. $\lim_{ y \to 0 } \int _{0}^{1} \frac{x}{y^{2}}e^{ -x^{2}/y^{2} } \, dx$, can one switch lim and int?
- let $f(x,y)=\frac{x}{y^{2}}e^{ -x^{2}/y^{2} }$, then:
	- if $y=0$, then either $x=0$ => $f=0$ or $x\neq 0$ => $f=\frac{x}{y^{2}e^{ x^{2}/y^{2} }}\to 0$ as $y \to \infty$, so we will simply let $f(x,0)=0$ for all $x \in[0,1]$
	- now we will prove $f$ is cont
		- $f$ cont is trivial for all points $(x_{0},y_{0})$ with $y_{0}\neq 0$
		- $f$ is cont for point $(x_{0},0)$

e.g. $\int _{0}^{1} \sin \ln \frac{1}{x}\frac{x^{b}-x^{a}}{\ln x} \, dx$
- we have $\frac{x^{b}-x^{a}}{\ln x}=\int _{a}^{b} x^{t} \, dt$ => int = $-\int _{0}^{1} \int_{a}^{b} x^{t}\sin \ln x \, dt \, dx$
- swap int => $\int _{a}^{b} \int _{0}^{1} x^{t}\sin \ln x \, dx \, dt$
	- calc the inner int by let $u = \ln x$ => integrand $e^{ (t+1)u }\sin u$ => integral: $\int _{-\infty}^{0} e^{ (t+1)u }\sin u \, du=-\frac{1}{t^{2}+2t+2}$
	- => integral is $\arctan(a+1)-\arctan(b+1)$ (note the minus sign)
	- this is in fact a [[paraint]], not [[paraim]], so one can change the limit without any problems (u need to introduce a new function tho)

e.g. $\int _{0}^{1} \frac{dx}{\sqrt[n]{ 1-x^{n} }} \, dx$
- let $t=x^{n}$, then $I=\int _{0}^{1} \frac{1}{(1-t)^{1/n}} \, \frac{dt}{nx^{n-1}}=\frac{1}{n}\int _{0}^{1} t^{1/n-1}(1-t)^{-1/n} dt$ => $I=B\left( \frac{1}{n}, 1-\frac{1}{n} \right)=\frac{\pi}{\sin \frac{\pi}{n}}$

e.g. $\int _{0}^{\infty} \frac{\arctan x}{x(1+x^{2})} \, dx$
- we have $\arctan x=\int _{t=0}^{1} d(\arctan tx)=\int _{0}^{1} \frac{x}{1+(tx)^{2}} \, dt$
=> int = $\int _{0}^{\infty} \int _{0}^{1} \frac{1}{(1+x^{2})(1+t^{2}x^{2})} \, dt \, dx$
- swap int => inner int = $\left( \frac{t\arctan tx-\arctan x}{y^{2}-1} \right)|_{0}^{\infty}=\frac{\pi}{2(t+1)}$ => outer int is $\frac{\pi}{2}\ln 2$
- to swap int, we need
	- continuity => ez
	- [[uniconv]]: $\int _{0}^{\infty} \frac{1}{(1+x^{2})(1+t^{2}x^{2})} \, dx$ uniconv as  $t\in[0,1]$: true because [[weierstrass m-test]] with $\frac{1}{1+x^{2}}$

e.g. $\int _{0}^{\infty} \frac{\sin\beta x}{x} \, dx$
- $\beta=0$ trivial, we will only consider $\beta=1$
- we calc $I(a)=\int _{0}^{\infty} \frac{e^{ -ax }\sin x}{x} \, dx$ with $a\in[0,\varepsilon]$ by differentiating
	- $f(a,x)=\frac{e^{ -ax }\sin x}{x}$ cont on $[0,\infty)$, and $f'_{a}=-e^{ -ax }\sin x$ also cont
	- $\int _{0}^{\infty} \frac{e^{ -ax }\sin x}{x} \, dx$ conv because it's less than (we change bounds here) $\int _{\varepsilon}^{\infty} \frac{\sin x}{x} \, dx=\int _{x=\varepsilon}^{\infty} \sin x \, d\left( -\frac{1}{x^{2}} \right)=\dots$ conv
	- $\int _{0}^{\infty} e^{ -ax }\sin x \, dx$ uniconv? (only true with $a>[\varepsilon',\varepsilon]$ sadge)
- then we can differentiate, but with a cost: we need to prove that it's cont at $t=0^{+}$
	- $\int _{0}^{\infty} e^{ -ax }\sin x \, dx=\frac{1}{a^{2}+1}$ =>int = $\frac{\pi}{2}$
	- to prove $I(a)$ cont as $t\to 0^{+}$, we actually just apply the theorem to get $\frac{e^{ -ax }\sin x}{x}$ [[uniconv]], which is trivial because [[weierstrass m-test]] and $\frac{\sin x}{x}$ conv