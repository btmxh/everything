[[series]] but now $a_{n}$ is a function of $x$

**properties**
- cont if $a_{n}(x)$ cont + [[uniconv]]
	- see https://web.archive.org/web/20130823173253/http://scipp.ucsc.edu/~profumo/teaching/phys116A_12/hw/uniform_convergence.pdf
- R-int8 if cont
- diff. if $a_{n}(x)$ cont diff + $\sum a'_{n}$ [[uniconv]]

**NOTE:** tập hội tụ (set of conv.) != miền hội tụ (region of conv.): region must be connected
=> the series is a fn from the set of conv. to $\mathbb R$ or $\mathbb C$

- e.g. find set of conv. $\sum_{n=1}^{\infty}x^{n-1}$
	- set of existence (tập xđ): $\mathbb R$
	- for $x_{0}\in \mathbb R\setminus \{ \pm 1 \}$, the series $\sum_{n=1}^{\infty}x^{n-1}$ have partial sum $S_{n} = \frac{1-x^{n}}{1-x}$
	- $\implies\lim_{ n \to \infty } S_{n} = \frac{1}{1-x}$ if $|x_{0}|<1$, $\infty$ otherwise
	- if $x_{0}=1 \implies S_{n}=n \implies \lim_{ n \to \infty } S_{n}=\infty \implies$ div
	- if $x_{0}=-1 \implies S_{n}=1$ if n odd, $0$ otherwise $\implies \not\exists \lim_{ n \to \infty } S_{n}$
	=> set of conv.: $(-1, 1)$

- e.g. set of conv. $\sum_{n=1}^{\infty} \frac{e^{ nx }}{n^{2}+n+1}$
	- set of existence: $\mathbb R$
	- for $x\in\mathbb R$, we consider the series $\sum_{n=1}^{\infty} \frac{e^{ nx }}{n^{2}+n+1}$
	- $\frac{a_{n+1}}{a_{n}} \to e^{ x_{0} }$, as $n\to\infty$
	- if $x_{0}=0$, then the series is now $\sum_{n=1}^{\infty} \frac{1}{n^{2}+n+1}$ conv
	- otherwise, the series conv iff $e^{ x_{0} } < 1$ iff $x_{0} < 0$
	- => set of conv. $(-\infty, 0]$