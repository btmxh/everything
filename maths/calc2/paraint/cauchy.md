## normal
$\exists \lim_{ x \to x_{0} }f(x)$ iff $\lim_{ x_{1}, x_{2} \to x_{0}}|f(x_{1})-f(x_{2})| = 0$

## [[uniconv]]
$f_{i}$ uniconv to some $f$ equivalent to $\lim_{i_1, i_2 \to i_0} \sup_{x\in S} |f_{i_1}(x)-f_{i_2}(x)| = 0$

e.g. $\sum_{n=1}^{\infty}\arctan \frac{2x}{x^{2}+n^{2}}$/$\mathbb R$
$|S_{2n}-S_{n}|=|\sum_{k=n+1}^{2n}\arctan \frac{2x}{x^{2}+n^{2}}|$
letting $x=n$ then it's trivial to see RHS$>n\arctan \frac{2}{5n} \to \frac{2}{5}$ as $n\to\infty$
=> not [[uniconv]]

e.g. $\sum_{n=1}^{\infty}2^{n}\sin \frac{1}{3^{n}x}$/$\mathbb R^{+}$
$|S_{n}-S_{n-1}|=|2^{n}\sin \frac{1}{3^{n}x}|$, letting $x=\frac{2}{3^{n}\pi}$, RHS -> $\infty$
=> not [[uniconv]]

e.g. $\sum_{n=1}^\infty \frac{\sin nx}n$ on $[\varepsilon, 2\pi-\varepsilon], [0, 2\pi]$
- $[\varepsilon, 2\pi-\varepsilon]$
	- use [[dirichlet test]] for uni conv.
	- $b_{n}=\sin nx, a_{n}=\frac{1}{n}$
	- then $\sum_{n=1}^\infty b_{n}=\frac{\sin x}{4\sin\left( \frac{x}{2} \right)^2}$, this sum is bounded by $\frac{1}{4\sin\left( \frac{\varepsilon}{2} \right)^2}$
	- $a_{n}$ monotonic and uni. conv. since it's a const fn
	- => qed
- $[0, 2\pi]$
	- use [[cauchy]] criterion with $m=2n$
	- need to pick $x$ s.t. $\lim_{n\to\infty} |\sum_{k=n+1}^{2n} \frac{\sin kx}{k}| \ne 0$
	- first pick $x$ small s.t. $\sin kx \geq 0 \forall k\in n+1..2n$, aka $x\leq \frac{\pi}{2n}$
	- then the sum $> \frac{1}{2n}\sum_{k=n+1}^{2n} \sin kx$
	- RHS can be evaluated to be $\frac{\sin \frac{3n+1}{2}x\sin \frac{n}{2}x}{2n\sin \frac{x}{2}}$
	- now let $x=\frac{\pi}{2n}$ that expr is now $\frac{\sin \frac{3n+1}{4n}\pi \sin \frac{\pi}{4}}{2n\sin \frac{\pi}{4n}}$ 
	- let $n\to\infty$, the limit approaches $1$, which is clearly greater than 0 => not uni conv.
