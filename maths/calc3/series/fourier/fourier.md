see [[intro]]

we have: $f(x)=\frac{a_{0}}{2}+\sum_{n=1}^{\infty}(a_{n}\cos nx+b_{n}\sin nx)$, then to calc $a_{n},b_{n}$, one takes the **inner product** of $f(x)$ with the basis vectors
- $a_{0}=\sqrt{ 2 }\left\langle  f, \frac{1}{\sqrt{ 2 }} \right\rangle=\langle f, 1\rangle=\frac{1}{\pi}\int _{-\pi}^{\pi} f(x) \, dx$
- $a_{n}=\langle f,\cos nx\rangle=\frac{1}{\pi}\int _{-\pi}^{\pi} f(x)\cos nx \, dx$
- $b_{n}=\langle f,\sin nx\rangle=\frac{1}{\pi}\int _{-\pi}^{\pi} f(x)\sin nx \, dx$

hence, one also get this important result, as a conseq of the pythagorean theorem
$$
\frac{a_{0}^{2}}{2}+\sum_{n=1}^{\infty}(a_{n}^{2}+b_{n}^{2})=\langle f,f\rangle=\frac{1}{\pi}\int _{-\pi}^{\pi} f(x)^{2} \, dx 
$$

## convergence
the series on the RHS is called a fourier series of $f(x)$
now given seqs $a_{n},b_{n}$, the fourier series MAY NOT converge, and even if one calc $a_{n},b_{n}$ from a $f(x)$, the fourier series still MAY NOT converge, and if it converge, it MAY NOT converges to $f(x)$

**def**: a fn $f(x)$ is said to be "able to be expressed as a fourier series" if its [[fourier]] series conv to $f(x)$, with no exceptions

so when does it conv?
see [[dirichlet condition]]

e.g. $f(x)=\frac{\pi}{4}\operatorname{sgn}(x)$ on $[-\pi,\pi]$
- this is an odd fn => $a_{n}=0$ for all $n$
- then, by the symmetry of $f$, one can calc $b_{n}$ by $b_{n}=\frac{2}{\pi}\int _{0}^{\pi} \frac{\pi}{4}\sin nx \, dx=\frac{1}{2}\cos nx|_{\pi}^{0}=\frac{1}{2}(1-(-1)^{n})$
- hence $f(x)=\sum_{n=1, n\text{ odd}}^{\infty} \frac{\sin nx}{n}$ ($f$ satisfies the discont conditions btw)
- plugging $x=1$, one have $\sum_{n=1, n \text{ odd}} \frac{\sin n}{n}=\frac{\pi}{4}$

## arbitary period

in order to replace $\pi$ by $l$, one have the arbitary period form of the fourier series
$f(x)=\frac{a_{0}}{2}+\sum_{n=1}^{\infty}\left( a_{n}\cos \frac{n\pi x}{l}+b_{n}\sin \frac{n\pi x}{l} \right)$, coeffs $a_{0}=\frac{1}{2l}\int _{-l}^{l}f(x) \, dx$ and etc. (replace $\pi$ by $l$)

e.g. $f(x)=x$ on $(a,a+2l)$
- we have $f(x)=a+(x-a) \operatorname{mod} 2l$ for all $x\in \mathbb{R}$ (except $a+2l\mathbb{Z}$ ig)
- take $a'\in(-l,l)$ s.t. $a-a'\in 2l\mathbb{Z}$, then $f(x)=a+(x-a') \operatorname{mod} 2l$, which can be calc as $a+x-a'$ if $x\geq a'$, or $a+x-a'+2l$ if $x<a'$
- so $f(x)=a+x-a'+1_{x<a'}\cdot 2l$
- we will now calc the coeffs
	- $a_{0}=\frac{1}{l}\left( \int _{-l}^{l} (a+x-a') \, dx + \int _{-l}^{a'} 2l \, dx \right)$$=\frac{1}{l}((a-a')2l+(a'+l)2l)=2a+2l$
	- $a_{n}=\frac{1}{2l}\left( \int _{-l}^{l} (a+x-a')\cos \frac{n\pi x}{l} \, dx +\int _{-l}^{a'} 2l\cos \frac{n\pi x}{l} \, dx\right)$$=\frac{1}{l}\left( \frac{l(a-a')}{n\pi}\sin \frac{n\pi x}{l}|_{-l}^{l} \right)+2\int _{-l}^{a'} \cos \frac{n\pi x}{l} \, dx=\frac{2l}{n\pi}\sin \frac{n\pi x}{l}|_{-l}^{a'}$$=\frac{2l}{n\pi}\sin \frac{n\pi a'}{l}=\frac{2l}{n\pi}\sin \frac{n\pi a}{l}$
	- $b_{n}=\frac{1}{2l}\left( \int _{-l}^{l} (a+x-a')\sin \frac{n\pi x}{l} \, dx + \int _{-l}^{a'} 2l\sin \frac{n\pi x}{l} \, dx \right)$$=\frac{a-a'}{2l}\int _{-l}^{l}  x\sin \frac{n\pi x}{l} \, dx+2\int _{-l}^{a'} \sin \frac{n\pi x}{l} \, dx$
		- the first integral can be calculated easily using int. by parts
			- signs: $+ \to - \to +$
			- $D: x\to 1\to 0$
			- $I: \sin \frac{n\pi x}{l}\to \frac{l}{n\pi}\cos \frac{n\pi x}{l}\to-\left( \frac{l}{n\pi} \right)^{2}\sin \frac{n\pi x}{l}$
			- => $I_{1}=\left( \frac{xl}{n\pi}\cos \frac{n\pi x}{l}-\left( \frac{l}{n\pi} \right)^{2}\sin \frac{n\pi x}{l} \right)|_{-l}^{l}=\frac{2l^{2}}{n\pi}(-1)^{n}$
			- mul with $\frac{a-a'}{2l}$: $\frac{l(a-a')}{n\pi}(-1)^{n}$
		- the second one is trivial $I_{2}=\frac{l}{n\pi}\cos \frac{n\pi x}{l}|_{-l}^{a'}$$=\frac{l}{n\pi}\left( \cos \frac{n\pi a}{l}-(-1)^{n} \right)$
		- => $b_{n}=\frac{l}{n\pi}\left( (-1)^{n}(a-a'-1)+\cos \frac{n\pi a}{l} \right)$
(pretty weird formula if you ask me ngl)

e.g. calc $\sum_{n=1}^{\infty} \frac{1}{n^{4}}$
we try stuff
- let $b_{n}=0$, $a_{n}=\frac{1}{n^{2}}$
	- then one needs something that has $\frac{2}{\pi}\int _{0}^{\pi} f(x)\cos nx \, dx=\frac{1}{n^{2}}$ ($f$ even)
	- by rng (and tbh it's the most natural choice), try to take $f(x)=x$, then the integral evals to $\frac{(-1)^{n}-1}{n^{2}}$, almost good
	- however, this thing still works, since we have $a_{n}=0$ for even n's, and $a_{n}=-\frac{4}{\pi n^{2}}$ for odd n's, which is actually very nice!
	- $a_{0}=\frac{1}{\pi}\int _{0}^{\pi}x \, dx=\frac{\pi}{2}$
- then we calc $\langle f,f\rangle=\frac{1}{\pi}\int _{-\pi}^{\pi} x^{2} \, dx=\frac{x^{3}}{3\pi}|_{-\pi}^{\pi}=\frac{2\pi^{2}}{3}$
- use the parseval thing: $\frac{\pi^{2}}{4}+\sum_{n=1, n \text{ odd}} \left( \frac{4}{\pi n^{2}} \right)^{2}=\frac{2\pi^{2}}{3}$ => $\sum_{n=1, n \text{ odd}} \frac{1}{n^{4}}=\left( \frac{2\pi^{2}}{3}-\frac{\pi^{2}}{2} \right) \frac{\pi^{2}}{16}=\frac{\pi^{4}}{96}$
- to get the traditional result, one can easily prove that the even+odd sum is conv using the odd sum, and if it conv to $S$, one have $\frac{\pi^{4}}{96}=S-\frac{S}{16}\implies S=\frac{\pi^{4}}{90}$, qed

- TODO: can one generalize this, i.e. calc $\sum_{n=1}^{\infty} \frac{1}{n^{k}}$ for all $k$ (at least for even $k's$) (probably not tbh)

## arbitary fn at some interval
the [[fourier]] series of an arbitary fn (must satisfy dirichlet cond, so $f$ piecewise monotonic, bounded) $f$ wrt some interval $[a,b]$, one find periodic $g$ with period $b-a$ s.t. $f=g$ on $[a,b]$ and simply find the [[fourier]] series of $g$

e.g. $f(x)=x$ has fourier series $F(x)$ wrt $[1.5, 3.5]$, calc $F(-0.5)$
we have $g(x)=x$ on $[1.5, 3.5]$ => $g(-0.5^{+})=g(1.5^{+})=1.5$ and $g(-0.5^{-})=g(1.5^{-})=g(3.5^{-})=3.5$ => $F(-0.5)=\frac{1}{2}(1.5+3.5)=2.5$

e.g. fourier series of $f(x)$, with $f(x)$ being the distance between $x$ and the nearest integer, i.e. $f(x)=\left|\{ x \}-\frac{1}{2}\right|$, with $b_{n}=0$ for all n's (cos only fourier series)
- $f$'s period is $T=1$, and it's indeed an even fn, $l=\frac{1}{2}$
- $a_{n}=\frac{1}{l}\int _{0}^{l} f(x)\cos \frac{n\pi x}{l} \, dx=2\int _{0}^{1/2} f(x) \cos \tau nx\, dx$$2\int _{0}^{1/2} x\cos \tau nx \, dx$
	- $a_{0}=1$
	- for $n>0$, $a_{n}=\frac{(-1)^{n}-1}{4\pi^{2}n^{2}}$

e.g. $f(x)=x\sin x$ on $(-\pi,\pi)$
- this thing is even, so $b_{n}=0$ for all $n>0$
- $a_{n}=\frac{1}{\pi}\int _{0}^{\pi} x\sin x\cos nx \, dx=$$\frac{1}{2\pi}\int _{0}^{\pi} x(\sin(n+1)x-\sin(n-1)x)\, dx$$=-\frac{\pi(-1)^{n}}{n^{2}-1}$ for $n\neq 1$
- $a_{1}=\frac{1}{\pi}\int_{0}^{\pi} x\sin x\cos x \, dx=-\frac{\pi}{4}$

