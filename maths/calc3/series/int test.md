let $f$ cont, positive, monotonic dec / $[1,\infty]$
then [[series]] $\sum_{n=1}^\infty f(n)$ conv iff $I = \int _{1}^\infty f(x)dx$ conv

**proof**
it's trivial to prove that:
$$
f(n+1)\leq \int _{n}^{n+1}f(x)dx  \leq f(n)
$$
which leads to
$$
\sum_{n=2}^N f(n) \leq \int _{1}^N f(x)dx \leq \sum_{n=1}^N f(n)
$$
qed

e.g. $\sum_{n=2}^\infty \frac{1}{n(\ln n)^p(\ln \ln n)^q}$
- change the start index to 10 to make the integral not type-2-improper
- integral = $\int_{10}^\infty \frac{d(\ln x)}{(\ln x)^p(\ln \ln x)^q} = \int_{\ln 10}^\infty \frac{dt}{t^p(\ln t)^q}$
- [[n term test]] (of integral) => conv if $\lim_{ t \to \infty } \frac{1}{t^p(\ln t)^q} = 0$ => 
- cases:
	- p<p'<1 => as $t \to \infty$, $\frac{1}{t^p(\ln t)^q}> \frac{1}{t^{p'}}$ div.
	- p>p'>1 => as $t \to \infty$, $\frac{1}{t^p(\ln t)^q} < \frac{1}{t^{p'}}$ conv
	- p=1
		- the integral = $\int_{\ln \ln_{10}}^\infty \frac{1}{(\ln v)^q}dv$ => conv if q > 1
- conclusion: conv iff either p > 1 or q>p=1

**Q:** can one use this to prove [[uniconv]]?
- if it has a [[uniconv]] variant, it should be $\sum_{n} f(n,x)$ [[uniconv]] iff $\int f(n,x) \, dx$
- now we'll attempt to prove that ig
- we have: $\sum_{n=2}^N f(n) \leq \int _{1}^N f(x)dx \leq \sum_{n=1}^N f(n)$
- or equivalently $S_{N}(x)-C\leq I_{N}(x)\leq S_{N}(x)$ (wlog assume the series and integral starts at $n=x=1$)
- use [[cauchy]]?
- TODO