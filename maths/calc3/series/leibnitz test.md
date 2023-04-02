let $sa_{n}$ be an [[series#^6267d0|non-strict-alt series]], then if
- $\lim_{ n \to \infty } a_{n}=0$
- $|a_{n}|$ (non-strict)dec.
then this [[series]] conv to $S$
and if $a_{1}>0$, $S\leq a_{1}$

**proof**
wlog assuming strict alt and $a_{1}>0$
then it's trivial that $a_{2n}$ inc and $a_{2n+1}$ dec while both are being bounded in $[0, a_{1}]$
=> they both conv. to $A=\lim_{ n \to \infty }a_{2n}$ and $B=\lim_{ n \to \infty }b_{2n+1}$
and since $B=A+\lim_{ n \to \infty }a_{2n+1}=A$ => qed

e.g. $\sum_{n=1}^\infty \sin \pi \sqrt{ n^2+k^{2} }$
$= \sum_{n=1}^\infty (-1)^n\sin \frac{k^{2}\pi}{\sqrt{ n^{2}+k^{2} } + n}$
the thing in the sin fn is a monotonic dec fn that conv to 0
=> for large n, this pass the [[leibnitz test]] => conv

e.g. $\sum_{n=2}^\infty \frac{1}{(\ln n)^2}\cos \frac{\pi n^{2}}{n+1}$
$=\sum_{n=2}^\infty (-1)^{n-1} \frac{1}{(\ln n)^2}\cos \frac{\pi}{n+1}$
we can directly apply the [[leibnitz test]] but the derv. looks like shit
or alternatively, use maclaurin:
$=\sum_{n=2}^\infty(-1)^{n-1} \frac{1}{(\ln n)^2}\left( 1-\frac{1}2 \left( \frac{\pi}{n+1} \right)^2+o\left( \left( \frac{\pi}{n+1} \right)^2 \right) \right)$
$=\sum_{n=2}^\infty (-1)^{n-1} \frac{1}{(\ln n)^2} + \sum_{n=2}^\infty (-1)^{n-1} \frac{1}{(\ln n)^2} \frac{1}{2} \left(\left( \frac{\pi}{n+1} \right)^2+o\left( \left( \frac{\pi}{n+1} \right)^2 \right) \right)$
the first one conv using [[leibnitz test]]
the second one abs conv (remove the -1 bs then compare with $\frac{1}{n^2}$)
=> conv

e.g. $\sum_{n=2}^\infty \frac{(-1)^{n}}{(n^{\alpha}+(-1)^{n})^{\beta}}$
[[n term test]] => $\alpha, \beta>0$
$$
a_{n}=(-1)^{n}n^{-\alpha\beta}\left( 1+(-1)^n n^{-\alpha} \right)^{-\beta}
$$
$$
=(-1)^{n}n^{-\alpha\beta}\left( 1-\beta(-1)^{n}n^{-\alpha}+o\left( \frac{1}{n^{\alpha}} \right) \right)
$$
$$
= (-1)^{n}n^{-\alpha\beta} - O(n^{-\alpha\beta-\alpha})
$$
=> split into 2 series: the first one conv. using [[leibnitz test]], the second one conv. iff $\alpha\beta+\alpha>1$
**conclusion**: conv iff $\alpha\beta+\alpha>1$ and $\alpha,\beta>0$

**NOTE: u can use this to prove [[uniconv]]**
**proof**
similar reasoning => $|S(x)-S_{n}(x))|\leq|f_{n+1}(x)|\to 0$ as $n\to\infty$
=> the sup tends to 0 => qed

e.g. $\sum_{n=1}^{\infty} \frac{(-1)^{n}}{x+n}$/$\mathbb R^{+}$
