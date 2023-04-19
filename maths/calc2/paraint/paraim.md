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
cond: $f,f'_{y}$ cont/xy-space + $\int f'_{y}(x,y)dx$ [[uniconv]]  (+ ofc $\int f(x,y)dx$ cont)

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

