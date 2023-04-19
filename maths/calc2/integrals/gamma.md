the gamma function is defined simply as a [[paraim]]: $\Gamma(z)=\int _{0}^{\infty} t^{z-1}e^{ -t } \, dt$, for all $z>0$ (one can extend the gamma function to $\mathbb{R}_{-}\setminus \mathbb{Z}_{-}$, but that is not consistent with the [[paraim]] definition)

**theorem**: $\Gamma(z)$ is defined for all $z > 0$
split the int into two [[paraim]], $\int _{0}^{1}$ and $\int _{1}^{\infty}$
- for $z>1$, the first one is actually [[paraint]] => conv, and if $z<1$, the integrand is asymptotic to $t^{z-1}$ as $t\to 0$ => trivially [[abs conv]]
- the second integral trivially [[abs conv]] by using the [[comparison test]] with $e^{ -(1-\varepsilon)t }$, which obviously conv

## basic

**theorem:** $\Gamma(z+1)=z\Gamma(z)$ for all $z>0$
we have $\Gamma(z+1)=\int _{0}^{\infty} t^{z}e^{ -t } \, dt=\int _{0}^{\infty}t^{z}\,d(-e^{ -t })=t^{z}e^{ -t }|_{\infty}^{0}+\int _{0}^{\infty} zt^{z-1}e^{ -t } \, dt$
the first term is zero, due to $z>0$, and the second term is just $z\Gamma(z)$ => qed

**corollary:** $\Gamma(z+1)=z!$ for $z\in \mathbb{N}$
this is due to the fact that $\Gamma(1)=\int _{0}^{\infty} e^{ -t } \, dt=1$

we also have $\Gamma\left( \frac{1}{2} \right)=\int _{0}^{\infty} \frac{e^{ -t }}{\sqrt{ t }} \, dt=\int _{0}^{\infty} 2e^{ -x^{2} } \, dx=\int _{-\infty}^{\infty }e^{ -x^{2} } \, dx=\sqrt{ \pi }$, so one can trivially calc the gamma function for all "half integers" (positive only ig)

## derivative

the gamma function has a derivative, and one can use [[uniconv]] stuff to prove that $\Gamma^{(k)}(z)=\int _{0}^{\infty}t^{z-1}\ln(t)^{k}e^{ -t } \, dt$
**proof**
denote the partial derv gamma function $\Gamma_{a,b}^{k}(z)=\int _{a}^{b} t^{z-1}\ln(t)^{k}e^{ -t } \, dx$ (omitting $a,b$ is equivalent to setting $a=0, b=\infty$), we will prove that 
- $\Gamma_{a,b}^{k}$ conv to $\Gamma^{k}$ as $a\to 0, b\to \infty$ (by definition of impropers)
- $\Gamma_{a,b}^{k}$ has cont derv $\Gamma_{a,b}^{k+1}$, which is [[uniconv]] as $a\to 0, b\to \infty$
	- the integrand and its derv, $t^{z-1}\ln(t)^{k+1 \text{ (or k)}}e^{ -t }$ is clearly cont on $[a,b]$ for all $a>0, b<\infty$ => use the [[paraint]] thing, $(\Gamma^{k}_{a,b})'=\Gamma_{a,b}^{k+1}$ cont
	- the main thing, [[uniconv]] can be proven via [[weierstrass m-test]]
		- first, split the integral like in the first theorem (we should do that instead of this $a,b$ bullshit)
		- as $t\to \infty$, $t^{z-1}\ln(t)^{k}e^{ -t }$ is less than $Me^{ -(1-\varepsilon)t }$, which conv (prove by limit)
		- as $t\to 0$, $t^{z-1}\ln(t)^{k}e^{ -t }$ is less than $\frac{M'}{t^{1-\varepsilon}}$, which also conv
hence, using the [[uniconv]] diff thing, qed

## euler's reflection formula

**theorem:** for non-integers $z$, $\Gamma(z)\Gamma(1-z)=\frac{\pi}{\sin \pi z}$
representing $e^{ -t }$ in the integrand by $\lim_{ n \to \infty } (1-\frac{t}{n})^{n}$, one transform $\Gamma(z)$ into the limit of polynomial integral
$$
\begin{align}
\Gamma(z)&=\int _{0}^{\infty} t^{z-1}e^{ -t } \, dt =
\int _{0}^{\infty}\lim_{ n \to \infty } t^{z-1}\left( 1-\frac{t}{n} \right)^{n} \, dt 
\end{align}
$$
- pulling out the limit and actually do the integral (reason provided later), one have $\Gamma(z)=\lim_{ n \to \infty } \frac{n!}{n^{n}}\prod_{k=0}^{n}(z+k)^{-1}n^{z+n}$, which can be rewritten as $\lim_{ n \to \infty } \frac{n^{z}}{z} \prod_{k=1}^{n} \frac{1}{1+\frac{z}{k}}$
- this can be used to evaluate the LHS (as $-z\Gamma(z)\Gamma(-z)$) as $\lim_{ n \to \infty } \frac{1}{z} \prod_{k=1}^{n} \frac{1}{1-\frac{z^{2}}{k^{2}}}$
- to prove that this expr equals RHS, it's outside of the scope, :tf: (you can prove that ig)

e.g. $\int _{0}^{1} x^{20}(\ln x)^{30} \, dx$
- let $t =\ln x$, $I=\int _{-\infty}^{0} e^{ 20t } t^{30}\,e^{ t }dt=\int _{-\infty}^{0}t^{30}e^{ 21t } \, dt=\int _{0}^{\infty} t^{30}e^{ -21t } \, dt$
- let $u=21t$ => $I=\int _{0}^{\infty} \left( \frac{u}{21} \right)^{30} e^{ -u } \, \frac{du}{21}=\frac{1}{21^{31}}\Gamma(31)=\frac{30!}{21^{31}}$
