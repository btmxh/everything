consider a point mass in 1d with [[force]]s
- harmonic force $F=-kx$ (typically, $k>0$)
- resistance $F=-rv$ (typically $r>0$)
- optional "cưỡng bức" force $F=H\cos \Omega t$

then, we have $-kx-r\dot{x}=H\cos \Omega t=m\ddot{x} \iff m\ddot{x}+r\dot{x}+kx=H\cos \Omega t$
this is a [[2nd order]] [[de]], and one can solve it and get very ugly results
we will only consider some cases

## defs
- dao động (oscillate): motion repeated in time
- general osc.
	- must have stable balanced position
	- when one push the obj away from the bp, there will be a force that pull back
	- => the system has inertia 

## $H=0$
the [[de]]: $m\ddot{x}+r\dot{x}+kx=0$
we already solved the [[de]] in the [[2nd order#const coeffs]], and considering only the two roots $\lambda_{1} \neq \lambda_{2}$ case:
$x=A_{1}e^{ \lambda_{1}t }+A_{2}e^{ \lambda_{2}t }$
the problem here is that $A_{1},A_{2},\lambda_{1}, \lambda_{2}$ may be complex, so one must make it real
first, we split: $\lambda_{1,2}=\beta+\omega j$ ($\beta, \omega$ are real, $j\in\{ 1,i \}$) then
$x=e^{ -\beta t }(A_{1}e^{ \omega j }+A_{2}e^{ -\omega j })$
- in the $j=i$ case, taking the conjugate, we have $x=\bar{x} \iff A_{1}=\bar{A_{2}}$, then if $A_{1}=\frac{1}{2}Ae^{ i\phi }, A_{2}=\frac{1}{2}Ae^{ -i\phi }$, we have $x=Ae^{ \beta t }\cos(\omega t+\phi)$, or $\boxed{x=\mathrm{Re}(z), z=Ae^{ \beta t+i\phi }e^{ i\omega t }=Ce^{ i\omega t }, C=Ae^{ \beta t+i\phi }}$

- using the quadratic formula, $\beta=\frac{r}{2m}$, $\omega j$ is a sqrt of $\frac{r^{2}-4mk}{4m^{2}}=\beta^{2}-\frac{k}{m}=\beta^{2}-\omega_{0}^{2}$, with $\omega_{0}$ being the [[angular velocity]] if $r=0$
- even if $m,r,k>0$, $\lambda_{1,2}$ still can be real (ofc lmfao $x^{2}+5x+6=0$) => the motion will not even reach the balance point (xd) => not a osc. motion (:skull:). this is the case when $\beta ^{2}-\omega_{0}^{2}\geq0 \iff |\beta|\geq|\omega_{0}|$

when $r=0$, we have $\omega j$ is sqrt of $-\frac{k}{m}$ and one can also define $\omega_{0}$ as the [[angular velocity]] if $r=0$ => $\omega^{2}j^{2}=\beta^{2}-\omega_{0}^{2}j^{2} \implies \omega=\sqrt{ \omega_{0}^{2}-\beta^{2} }$ if $j=i$

some relating formulas for $j=i$
$$
\begin{align}
\omega^{2} + \beta^{2} &= \omega_{0}^{2}=\frac{k}{m} \\

\beta&=\frac{r}{2m}

\end{align}
$$

## $H\neq 0$
the equation: $m\ddot{x}+r\dot{x}+kx=H\cos \Omega t$
in this case, one says that the osc. motion is "dao động cưỡng bức", and since [[2nd order]] [[de]] root have: (general root) = (root of eq = 0) + (one root of eq = f(x)), the first term will be insignificant as $t \to \infty$

the other factor is
$$x=\frac{H\cos\left( \Omega t-\arctan \frac{2\beta\Omega}{\Omega^{2}-\omega_{0}^{2}} \right)}{m\sqrt{ (\Omega^{2}-\omega_{0}^{2})^{2}+4\beta^{2}\Omega^{2} }}$$
yeah kinda fucked ngl, but it's still in the form $x=A\cos(\Omega t+\Phi)$ ($\Omega\neq \omega$ tho)

> one can use complex number to simplify this
> $z=Ae^{ i\Phi }e^{ i\Omega t }=Ce^{ i\Omega t }$ => $Ce^{ i\Omega t }(-m\Omega^{2}+ri\Omega+k)=He^{ i\Omega t }$
> => $k-m\Omega^{2}+ri\Omega=\frac{H}{C}$
> => $C=\frac{H}{k-m\Omega^{2}+ri\Omega}=\frac{H}{m\omega_{0}^{2}-m\Omega^{2}+2m\beta \Omega i}=\frac{H}{m(\omega_{0}^{2}-\Omega^{2}+2i\Omega\beta)}$

e.g. verify the 2 formulas with $t=\frac{1}{3}, \omega_{0}=\pi, \Omega=2\pi, \beta=\frac{1}{10}, H=m=1$
- vldc1 formula yields $-0.015617\dots$
- complex formula yields $C=-0.0337\dots-1.4308\dots$ and $x=\mathrm{Re}(Ce^{ i\Omega t })=-0.0189563104$, so there are some sign mismatches
- TODO: fix this (it seems that the vldc1 formula is wrong)
	- one can fix my formula by letting $C=\pm\frac{H}{m(\Omega^{2}-\omega_{0}^{2}+2i\Omega\beta)}$ (idk which sign tho)

now fix everything except $\Omega^{2}$ => $A=|C|$ max iff $|\omega_{0}^{2}-\Omega^{2}+2i\Omega\beta|$ min iff $(\omega_{0}^{2}-\Omega^{2})^{2}+4\beta^{2}\Omega^{2}$ min iff $\Omega^{2}=\omega_{0}^{2}-2\beta^{2}$, and $A=\frac{H}{2m\beta \sqrt{ \omega_{0}^{2}-\beta^{2} }}$

as $\beta$ gets smaller and smaller (assuming $\beta\ll \omega_{0}$), $A\to \infty$

when $A$ max, **resonance** happens (cộng hưởng), and the smaller $\beta$ is, the more powerful this thing is.

