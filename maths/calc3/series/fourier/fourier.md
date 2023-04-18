see [[intro]]

we have: $f(x)=\frac{a_{0}}{2}+\sum_{n=1}^{\infty}(a_{n}\cos nx+b_{n}\sin nx)$, then to calc $a_{n},b_{n}$, one takes the **inner product** of $f(x)$ with the basis vectors
- $a_{0}=\left\langle  f, \frac{1}{2} \right\rangle=\frac{1}{2\pi}\int _{-\pi}^{\pi} f(x) \, dx$
- $a_{n}=\langle f,\cos nx\rangle=\frac{1}{\pi}\int _{-\pi}^{\pi} f(x)\cos nx \, dx$
- $b_{n}=\langle f,\sin nx\rangle=\frac{1}{\pi}\int _{-\pi}^{\pi} f(x)\sin nx \, dx$

## convergence
the series on the RHS is called a fourier series of $f(x)$
now given seqs $a_{n},b_{n}$, the fourier series MAY NOT converge, and even if one calc $a_{n},b_{n}$ from a $f(x)$, the fourier series still MAY NOT converge, and if it converge, it MAY NOT converges to $f(x)$

**def**: a fn $f(x)$ is said to be "able to be expressed as a fourier series" if its [[fourier series]] conv to $f(x)$, with no exceptions

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
