let $I(y)=\int_{\alpha(y)}^{\beta(y)} f(x,y)dx$
s.t. $f$ R-int wrt $x\in[a,b], \forall y\in[c,d]$

**spaces:**
- x-space: $[a,b]$
- y-space: $[c,d]$

**space conditions:**
- $I$ defined on y-space
- $\alpha,\beta$ maps y-space to x-space

**Q**: when is $I$ cont? diff? R-int8?

## cont
- $f$ cont/xy-space
- $\alpha, \beta$ cont/y-space

see [[dct]]
**NOTE: not applicable for im.int.**, u need to use the [[uniconv]] cont condition

**proof**
$\alpha, \beta$ cont/y-space => $\alpha(y)=\alpha(y_0)+o(y-y_0), \beta(y)=\beta(y_0)+o(y-y_0)$
then
$|I(y)-I(y_0)|=|\int_{\alpha(y)}^{\beta(y)} f(x,y)dx - \int_{\alpha(y_0)}^{\beta(y_0)}f(x,y_0)dx|$
RHS can be rewritten as
$|(\int_{\alpha}^{\beta}(f(x,y)-f(x,y_0))dx) + \int_{\beta}^{\beta+o}f(x,y)dx-\int_{\alpha}^{\alpha+o}f(x,y)dx|$
$\le |\int_{\alpha}^{\beta}(f(x,y)-f(x,y_0))dx| + |\int_{\beta}^{\beta+o}f(x,y)dx| + |\int_{\alpha}^{\alpha+o}f(x,y)dx|$
($\alpha=\alpha(y_0), \beta=\beta(y_0), o=o(y-y_0)$)
$f$ cont/$[a,b]\times[c,d]$ => f **uniform cont** on that
$\forall \varepsilon > 0, \exists \delta > 0$ s.t. $\forall x \in [a,b], y\in [c,d]$ s.t. $|x-x_0|, |y-y_0| \le \delta$ then
$|f(x,y)-f(x,y_0)|\le \frac \varepsilon {2(b-a)}$ ($\delta$ only depends on $\varepsilon$, not $x_{0},y_{0}$)
sub this thing to the integral => first term $\le \frac \varepsilon 2 < \varepsilon$ => qed
since f cont/xy-space => 2nd and 3rd terms conv. to 0 as $y \to y_0$ (take the maximum value of f on xy-space)

e.g. $\int_0^1 \frac{yf(x)}{x^2+y^2}dx$, given $f$: cont/$[0,1]$
- $g(x)=\frac{yf(x)}{x^2+y^2}$ only cont/$[0,1]\times[\varepsilon,M], [0,1]\times[-M,-\varepsilon]$ => $I(y)$ cont / $[\varepsilon, M], [-M, -\varepsilon]$
- problem: $I(y)$ cont? / $y=0$
	- $I(y)$ cont/$y=0$ iff $J(y)=\int_0^\varepsilon \frac{yf(x)}{x^2+y^2}dx$ cont/$y=0$ (obvious reason stfu)
	- at $y=0$: $I(0)=\int_0^\varepsilon 0dx = 0$
	- then two cases:
		- $f(0)\ne0$
			- then there exists $\varepsilon$ s.t. $|f(x)| > 0, \forall x\in[0,\varepsilon]$
			- let $m=\min_{x\in[0,\varepsilon]} |f(x)|>0$, then for $y > 0$, $g(y)\ge \frac {my} {x^2+y^2} \implies I(y)\ge m \arctan{\frac \varepsilon y}$
			- similarly, $I(-y)\le -m\arctan\frac \varepsilon y$
			- => $|I(y)-I(-y)| \ge 2m\arctan\frac \varepsilon y \to m\pi$ as $y \to 0$
			- this means that $I(y)$ discont. at $y=0$
		- $f(0)=0$
			- if $g(x)=\frac{f(x)}{x}$, $|g(x)|$ is R-int8 on $[0,\varepsilon]$, then $|J(y)|=|\int_0^\varepsilon \frac{xy}{x^2+y^2} g(x)dx| \le \frac12 \int_0^\varepsilon |g(x)|dx$
				- by letting $\varepsilon \to 0$, RHS can be arbitary small
			- **TODO**



e.g. $I(y)=\int _{0}^{\pi/2} \frac{dx}{\sqrt{ 1-y^{2}\sin(x)^{2} }}$
- $f(x, y)= \frac{1}{\sqrt{ 1-y^{2}\sin(x)^{2} }}$ cont/$\left[ 0, \frac{\pi}{2} \right]\times[-1+\varepsilon, 1-\varepsilon]$
- at $y=\pm1$, the limit is $\int _{0}^{\pi/2} \frac{dx}{\cos x}$, which diverges => not cont.

e.g. $\lim_{ y \to 0 } \int _{0}^{2} x^{2}\cos xydx$
- $f(x, y)=x^{2}\cos xy$, cont/$[0,2]\times[-1,1]$
- => $I(y)=\int _{0}^{2} x^{2}\cos xydx$ cont/$[-1,1]$
- => $\lim_{ y \to 0 } \int _{0}^{2} x^{2}\cos xydx=\int _{0}^{2} \lim_{ y \to 0 }(x^{2}\cos xy)dx=\int _{0}^{2}x^{2}dx=\frac{8}{3}$

e.g. $\lim_{ y \to 0 } \int _{0}^{1} \frac{xdx}{x^{4}(1+y^{6})+3(y^{2}+2)}$
- $f(x,y)=\frac{x}{x^{4}(1+y^{6})+3y^{2}+6}$ cont/$[0,1]\times[-1,1]$
- => $I(y)=\int _{0}^{1} \frac{xdx}{x^{4}(1+y^{6})+3y^{2}+6}$ cont/$[-1,1]$
- => $\lim_{ y \to 0 } \int _{0}^{1} \frac{xdx}{x^{4}(1+y^{6})+3y^{2}+6}=\int _{0}^{1} \lim_{ y \to 0 }\left( \frac{x}{x^{4}(1+y^{6})+3y^{2}+6} \right)dx=\int _{0}^1 \frac{xdx}{x^{4}+6}$
- evaluating the integral $I=\frac{1}{2} \int \frac{dt}{t^{2}+6}= \frac{1}{2\sqrt{ 6 }} \arctan \frac{1}{\sqrt{ 6 }}, t=x^{2}$

e.g. $\lim_{ \alpha \to 0 }\int _{\alpha}^{\alpha+1} \frac{dx}{1+x^{2}+\alpha^{2}}$
- $\alpha+1, \alpha$ are cont wrt $\alpha$/$\mathbb R$
- $L=\int _{0}^{1} \frac{dx}{1+x^{2}}$
- the second and third integral tends to 0 (easily proven because the integrand is bounded)
- the first one is cont => lim = $\frac{\pi}{2}$

e.g. $\lim_{ y \to 0 } \int _{\cos y}^{\sin y} \frac{\arctan(x+y)}{1+x^{2}+y^{2}}dx$
- cont cond
	- integrand cont/$\mathbb R^2$
	- bound fns cont/$\mathbb R$
	- => cont
- => lim = $\int _{1}^{0} \frac{\arctan x}{1+x^{2}} dx=\int _{1}^{0} \arctan x d(\arctan x)=-\frac{1}{2} \arctan(1)^{2}=-\frac{\pi^{2}}{32}$

## diff
if $f, f'_y$ cont/$[a,b]\times[c,d]$
aka [leibniz's rule](https://en.wikipedia.org/wiki/Leibniz_integral_rule)
formula:$I'(y)=\beta'f(\beta,y)-\alpha'f(\alpha,y)+\int_ \alpha ^ \beta f'_y(x,y)dx$

**proof**
$\alpha, \beta$ const case:
	$I'(y_0) = \lim_{y \to y_0} \frac{I(y)-I(y_0)}{y-y_0} = \lim_{y\to y_0} \int_a^b \frac{f(x,y)-f(x,y_0)}{y-y_0}dx$
	let $g(x,y)=\frac{f(x,y)-f(x,y_0)}{y-y_0}$ if $y \ne y_0$ and $f'_y(y_0)$ otherwise
	then $g$ is cont./$[a,b]\times[c,d]$, we can pass the limit into the integral
	then RHS = $\int_a^b f'_y(x, y_0)dx$, qed
if $\alpha, \beta$ not const
	then we get two additional terms, one such term is $-\frac1{\Delta y}\int_\alpha^{\alpha+o(\Delta y)}f(x,y)dx=-\frac1{\Delta y} \int_0^{o(\Delta y)} f(\alpha + x, y)dx$
	now expand $o(\Delta y)$ back to its original form $\alpha(y)-\alpha(y_0)$
	and use MVT => the integral = $(\alpha(y)-\alpha(y_0))f(\alpha+c,y)$, for some $c\in[0, o(\Delta y)]$
	letting $y \to y_0$, RHS is $-\alpha'f(\alpha,y)$
	doing the same thing to the other term => $\beta f(\beta, y)$
	=> qed

e.g. $I(y)=\int _{0}^{1} \cos(x^{2}+xy+y^{2})dx$, calc $I'(0)$
integrand cont and obv its derv $-\sin(x^{2}+xy+y^{2})(2y+x)$ cont on $\mathbb R^2$
=> $I'(0)=\int _{0}^{1} -x\sin (x^{2})dx=-\frac{1}{2} \int_{0}^{1}\sin tdt=\frac{1-\cos 1}{2}$

e.g. $\int _{0}^{1} \frac{x^{b}-x^{a}}{\ln x}dx$ ($0<a<b$)
- $f(x,y)=\frac{x^y-x^{a}}{\ln x}$ if $x \neq 1$, $b-a$ otherwise
- then $f$ is cont/$[0,1]\times[a,b]$
- and $f'_{y}(x,y)=x^y$ cont/$[0,1]\times[a,b]$
- => use the thing: $I(y)=\int _{0}^{1} f(x,y)dx, I(a)=0$
- => $I'(y)=\int _{0}^{1}x^{y}dx=\frac{1}{y+1}$
- => $I(y)=\ln(y+1)+C$ and $C=-\ln(a+1)$
- => result: $\ln \frac{b+1}{a+1}$

e.g. $I(y)=\int _{0}^{1} \arctan\frac{x}{y} dx$
- $f(x,y)=\arctan \frac{x}{y}$ cont/$[0,1]\times[\varepsilon, M], [0,1]\times[-M, -\varepsilon]$
- $f'_{y}(x,y)=-\frac{1}{x^{2}+y^{2}}$ cont/$[0,1]\times[\varepsilon, M], [0,1]\times[-M, -\varepsilon]$
- $I'(y)=\int _{0}^{1} -\frac{1}{x^{2}+y^{2}} \, dx=-\frac{1}{y}\arctan \frac{1}{y}$

e.g. $I_{n}(a)=\int _{0}^{1} x^{a}\ln(x)^{n}dx$
- if $a\leq-1$ then the integral diverges (integrand > $\frac{1}{x^{1+\varepsilon}}$ div in the $a<-1$ case, > $\ln(x)$ which div to $\frac{\ln(x)^{2}}{2}$ in the $a=-1$ case)
- if $a>-1$ then the integral conv. (integrand < $\frac{1}{x^{1-\varepsilon}}$ conv)
- 
- if $a<0$ then $|x^{a}\ln(x)^{n}| > |\ln(x)^{n}| > k$ as $x \to 0$ => 
- integral conv iff $\lim_{ x \to 0 } x^{a}\ln(x)^{n}=0$ iff $a>0$ => $I_{n}$ is only defined on $\mathbb R^{+}$
- then this is no longer [[paraim]] since 

e.g. $I(y)=\int _{\sin y}^{\cos y} e^{ yx^{2} }dx$
- integrand cont/$\mathbb R^{2}$
- integrand'y = $x^{2}e^{ yx^{2} }$
- $I'(y)=\int _{\sin y}^{\cos y} x^{2}e^{ yx^{2} } dx-e^{ y\cos(y)^{2} }\sin y-e^{ y\sin(y)^{2} }\cos y$

## int
only applicable for $\alpha, \beta$ const, cond: same as cont.
aka [fubini's theorem](https://en.wikipedia.org/wiki/Fubini's_theorem)

$$
\int_c^d \int_\alpha^\beta f(x,y)dxdy=\int_\alpha^\beta \int_c^d f(x,y)dydx = \iint_{[\alpha,\beta]\times[c,d]} f(\mathbf{r})d\mathbf{r}
$$

e.g. $\int _{0}^{1} \frac{x^{b}-x^{a}}{\ln x}dx$ ($0<a<b$)
- $I(b)=\int _{0}^{1} \frac{x^{b}-x^{a}}{\ln x} \, dx=\int _{0}^{1} \int _{a} ^{b} x^{y}dydx$
- if conds are satisfied, it's trivial to achieve the result $\int _{a}^{b} \frac{dy}{y+1} = \ln \frac{b+1}{a+1}$
- cond: $x^{y}$ cont / $[0,1]\times$y-space
- take y-space to be $[a,b]$ => qed

anti-e.g. $f(x,y)=\frac{y^{2}-x^{2}}{(x^{2}+y^{2})^{2}}$ on $[0,1]\times[0,1]$
