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

**proof**
$\alpha, \beta$ cont/y-space => $\alpha(y)=\alpha(y_0)+o(y-y_0), \beta(y)=\beta(y_0)+o(y-y_0)$
then
$|I(y)-I(y_0)|=|\int_{\alpha(y)}^{\beta(y)} f(x,y)dx - \int_{\alpha(y_0)}^{\beta(y_0)}f(x,y_0)dx|$
RHS can be rewritten as
$|(\int_{\alpha}^{\beta}(f(x,y)-f(x,y_0))dx) + \int_{\beta}^{\beta+o}f(x,y)dx-\int_{\alpha}^{\alpha+o}f(x,y)dx|$
$\le |\int_{\alpha}^{\beta}(f(x,y)-f(x,y_0))dx| + |\int_{\beta}^{\beta+o}f(x,y)dx| + |\int_{\alpha}^{\alpha+o}f(x,y)dx|$
($\alpha=\alpha(y_0), \beta=\beta(y_0), o=o(y-y_0)$)
$f$ cont/$[a,b]\times[c,d]$ => f uniform cont on that
$\forall \varepsilon > 0, \exists \delta > 0$ s.t. $\forall x \in [a,b], y\in [c,d]$ s.t. $|x-x_0|, |y-y_0| \le \delta$ then
$|f(x,y)-f(x,y_0)|\le \frac \varepsilon {2(b-a)}$
sub this thing to the integral => first term $\le \frac \varepsilon 2 < \varepsilon$ => qed
since f cont/xy-space => 2nd and 3rd terms conv. to 0 as $y \to y_0$ (take the maximum value of f on xy-space)

e.g. $\int_0^1 \frac{yf(x)}{x^2+y^2}dx$, given $f$: cont/$[0,1]$
- $g(x)=\frac{yf(x)}{x^2+y^2}$ only cont/$[0,1]\times[\varepsilon,1]$ => $I(y)$ cont / $[\varepsilon, M], [-M, \varepsilon]$
- problem: $I(y)$ cont? / $y=0$
	- $I(y)$ cont/$y=0$ iff $J(y)=\int_0^\varepsilon \frac{yf(x)}{x^2+y^2}dx$ cont/$y=0$ (obvious reason stfu)
	- then two cases:
		- $f(0)\ne0$
			- then there exists $\varepsilon$ s.t. $|f(x)| > 0, \forall x\in[0,\varepsilon]$
			- let $m=\min_{x\in[0,\varepsilon]} f(x)$, then for $y > 0$, $g(y)\ge \frac {my} {x^2+y^2} \implies I(y)\ge m \arctan{\frac \varepsilon y}$
			- similarly, $I(-y)\le -m\arctan\frac \varepsilon y$
			- => $|I(y)-I(-y)| \ge 2m\arctan\frac \varepsilon y \to m\pi$ as $y \to 0$
			- this means that $I(y)$ discont. at $y=0$
		- $f(0)=0$
			- if $g(x)=\frac{f(x)}{x}$, $|g(x)|$ is R-int8 on $[0,\varepsilon]$, then $|J(y)|=|\int_0^\varepsilon \frac{xy}{x^2+y^2} g(x)dx| \le \frac12 \int_0^\varepsilon |g(x)|dx$
				- by letting $\varepsilon \to 0$, RHS can be arbitary small
			- TODO
	- at $y=0$: $I(0)=\int_0^1 0dx = 0$

## diff
if $f, f'_y$ cont/$[a,b]\times[c,d]$
formula:$I'(y)=f(\beta,y)\beta'-f(\alpha,y)\alpha'+\int_ \alpha ^ \beta f'_y(x,y)dx$

**proof**
$\alpha, \beta$ const case:
	$I'(y_0) = \lim_{y \to y_0} \frac{I(y)-I(y_0)}{y-y_0} = \lim_{y\to y_0} \int_a^b \frac{f(x,y)-f(x,y_0)}{y-y_0}dx$
	let $g(x,y)=\frac{f(x,y)-f(x,y_0)}{y-y_0}$ if $y \ne y_0$ and $f'_y(y_0)$ otherwise
	then $g$ is cont./$[a,b]\times[c,d]$, we can pass the limit into the integral
	then RHS = $\int_a^b f'_y(x, y_0)dx$, qed
if $\alpha, \beta$ not const
	then we get two additional terms in the numerator, one such term is $-\frac1{\Delta y}\int_\alpha^{\alpha+o(\Delta y)}f(x,y)dx=-\frac1{\Delta y} \int_0^{o(\Delta y)} f(\alpha + x, y)dx$
	now expand $o(\Delta y)$ back to its original form $\alpha(y)-\alpha(y_0)=\alpha'\Delta y$
	and use MVT => the integral = $(\alpha(y)-\alpha(y_0))f(\alpha+c,y)$, for some $c\in[0, o(\Delta y)]$
	letting $y \to y_0$, RHS is $-\alpha'f(\alpha,y)$
	doing the same thing to the other term => $\beta f(\beta, y)$
	=> qed

## int
only applicable for $\alpha, \beta$ const, cond: same as cont.
$$
\int_c^d \int_\alpha^\beta f(x,y)dxdy=\int_\alpha^\beta \int_c^d f(x,y)dydx = \iint_{[\alpha,\beta]\times[c,d]} f(x,y)dr
$$
