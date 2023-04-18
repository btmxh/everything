
see: https://people.math.harvard.edu/~knill/teaching/math22b2019/handouts/lecture30.pdf
**dirichlet criterion:** let $f: [-\pi,\pi]\to \mathbb{R}$ be a piecewise smooth fn on $[-\pi,\pi]$, s.t. if $f$ discont at $x_{0}$, then $f(x_{0})=\frac{1}{2}(f(x_{0}^{+})+f(x_{0}^{-}))$= > it can be expressed as a fourier series
> denote $f(x_{0}^{+}), f(x_{0}^{-})$ to be the left and right limit of $f$ as $x\to x_{0}$

**proof**
- the partial sum $S_{n}$ can be expressed as $S_{n}(x)=\int _{-\pi}^{\pi} D_{n}(x-y)f(y) \, dy)$, for $D_{n}(t)=\frac{1}{\pi}\left( \frac{1}{2}+\sum_{k=1}^{n} \cos kt \right)$ (dirichlet kernel)
	- this is simply plugging the coeffs utilizing the above formulas:$$\begin{align}

S_{n}(x)&=\int _{-\pi}^{\pi} \left( \frac{1}{2\pi}f(y)+\frac{1}{\pi} \sum_{k=1}^{n} \left(f(y)\cos ky\cos kx+f(y)\sin ky\sin kx \right)\right) \, dy  \\
&=\int _{-\pi}^{\pi} f(y)\left( \frac{1}{2\pi}+\frac{1}{\pi}\sum\cos(k(x-y)) \right) \, dy  \\
&=\int _{-\pi}^{\pi} D_{n}(x-y)f(y) \, dy 
\end{align}
$$
- one can easily calc $D_{n}(t)=\frac{1}{2\pi}\, \frac{\sin\left( \left( n+\frac{1}{2} \right)t \right)}{\sin \frac{t}{2}}$ (see that [[uniconv]] exercise), and we have $\int _{-\pi}^{\pi}D_{n}(x) \, dx=1$ (the cosines vanish)
-  since $f(x)=\int _{-\pi}^{\pi}D_{n}(y)f(x_{0}) \, dy$, and by simply changing vars, $S_{n}(x)=\int _{-\pi}^{\pi} D_{n}(y)f(x+y) \, dy$, we can calc the difference between $f$ and $S_{n}$: $$
\boxed{(S_{n}-f)(x)=\int _{-\pi}^{\pi} D_{n}(y)(f(x+y)-f(y)) \, dy }
$$
- let $F(x,y)=\frac{f(x+y)-f(x)}{2\sin \frac{y}{2}}$, at $y=0$, we make the fn cont by letting $F(x,0)=f'(x)$, then if $f$ piecewise cont, $F$ is cont and $2\pi$-periodic wrt y => RHS is now $\int _{-\pi}^{\pi} F(x,y)\sin\left( \left( n+\frac{1}{2} \right)y \right) \, dx$
- expand $\sin\left( \left( n+\frac{1}{2} \right)y \right)=\cos \frac{ny}{2}\sin ny+\sin \frac{ny}{2}\cos ny$, let $G(x,y)=F(x,y)\cos \frac{ny}{2}, H(x,y)=F(x,y)\sin \frac{ny}{2}$, then $(S_{n}-f)(x)=\int _{-\pi}^{\pi} (G(x,y)\sin ny+H(x,y)\cos ny) \, dy$
- using the **riemann-lebesgue lemma**, one can prove that integrals like $A_{n}=\int _{-\pi}^{\pi} g(x)\cos nx \, dx$ (and the sine variant) will tend to 0 as $n\to \infty$ => qed

## discontinuities


## r-l lemma
**theorem**: let $f: \mathbb{R}\to \mathbb{R}$ be a lebesgue-measurable fn, then $\lim_{ n \to \infty } \int _{-\infty}^{\infty} f(x)\cos nx \, dx=0$

we will only prove the riemann formula, since we would need to define the lebesgue integral as well as the whole machinery of measure theory to prove the above theorem

**theorem (weakened)**: $f$ R-intbl on $[a,b]$, then $\lim_{ n \to \infty } \int _{a}^{b}f(x)\cos nx \, dx=0$
- one may estimate $f(x)$ via a step function $\phi(x)$, $\phi\leq f$ and $\|\phi-f\|\leq\varepsilon$ (using the integral norm), then $\|\phi(x) \cos nx-f(x)\cos nx\|\leq\varepsilon$, and if we have $\|\phi(x)\cos nx\|=0$, we have qed => wlog assuming $f$ is a step fn (only depends on $\varepsilon$, not in $n$)
- then, one may write $f(x)=\sum_{i=1}^{N} 1_{x\in I_{i}}c_{i}$ ($I_{i}$ is a partition of $[a,b]$) => $\|\phi(x)\cos nx\|\leq \sum_{i=1}^{N}\left|\int _{I_{i}} c_{i}\cos nx \, dx\right|\leq\sum_{i=1}^{N} \frac{2|c_{i}|l(I_{i})}{n}\leq \frac{2|c_{max}|(b-a)}{n}$
- RHS conv to 0 because $a,b,c_{max}$ const, $n\to \infty$
