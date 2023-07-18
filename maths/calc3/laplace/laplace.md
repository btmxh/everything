laplace transform is yet another time-frequency bla bla transform
$$
\mathcal{L}\{ f \}(s)=\int _{0}^{\infty} f(t)e^{ -st }  \, dt 
$$
because i'm lazy, i will use operational calculus extensively here:
- $I$: identity operator (denote the original function $f$)
- $D$: the differentiation operator
- $D^{-1}|^{b}_{a}$: integrate from $a$ to $b$
- $T$: the translation operator, with $Tf(x)=f(x+1)$, and $T^{k}f(x)=f(x+k)$ for all $k\in \mathbb{R}$
- $\times$: to denote regular multiplication of two functions
- $L$: the laplace transform
- $S$: scale operator: $S_{a}(f)(x)=f(ax)$
- $\exp$: exponential function: $\exp x=e^{ x }$
- $X_{s}$: the variable of the function, with $s$ being a helpful label
note that the order of function **transform** is **right to left**
e.g. $f(ax+b)=f\left( a\left( x+\frac{b}{a} \right) \right)=T^{b/a}S_{a}f$, or $f(ax+b)=S_{a}T^{b}f$, hence $S_{a}T^{b}=T^{b/a}S_{a}$

then, we have:
$$
Lf(s)=D^{-1}|^{\infty}_{0}\{ f\times S(-s)\exp \}
$$
## Translation properties
### Frequency translation
- we have $Lf(s+k)=\int _{0}^{\infty} e^{ -(s+k)t }f(t) \, dt=L\{ e^{ -kt }f(t) \}$, then $T^{k}Lf=L(f\times S_{-k}\exp)$ => $\boxed{L^{-1}T^{-k}f=L^{-1}f\times S_{k}\exp}$
e.g. know $L\sin(s)=\frac{1}{s^{2}+1}$, what's $L^{-1}\left( s\to \frac{1}{s^{2}+2s+2} \right)$
we have $f(s)=\frac{1}{s^{2}+2s+2}=\frac{1}{(s+1)^{2}+1}=L\sin(s+1)=TL\sin(s)$
hence, $L^{-1}f=L^{-1}TL\sin=\sin \times S_{-1}\exp=t\to e^{ -t }\sin t$

- another thing: $\boxed{L(f\times S_{k}\exp)=T^{-k}Lf}$
e.g. $L(t\to e^{ at })=T^{-a}L(1)=T^{-a}\left( s\to \frac{1}{s} \right)=s\to\frac{1}{s-a}$

### Time translation
- we have $L(T^{k}(f\times u))=\int _{k}^{\infty} e^{ -st }f(t-k) \, dt$$=e^{ sk }\int _{0}^{\infty} e^{ -st' }f(t') \, dt'=e^{ sk }Lf(s)$
- $LT^{k}f(s)=\int _{0}^{\infty} e^{ -st }f(t+k) \, dt=\int _{k}^{\infty} e^{ -s(t'-k) }f(t') \, d(t'=t+k)$$=e^{ ks }L\{ f\times uT^{-k} \}$, hence $LT^{k}f=\exp kX_{s}\times L(f\times uT^{-k})$
- and hence:
	- $LT^{k}(f\times u)=Lf\times S_{k}\exp$
	- $L^{-1}(f\times S_{k}\exp)=T^{k}(L^{-1}f\times u)$

There are some similarities between the formulas:
- $L^{-1}T^{k}f=L^{-1}f\times S_{-k}\exp$
- $LT^{-k}(f\times u)=Lf\times S_{-k}\exp$

## Scaling property
- let $S_{a}(x)=ax$, then
- $Lf(aX_{t})(s)=\int _{0}^{\infty} e^{ -st }f(at) \, dt=\frac{1}{a}Lf\left( \frac{s}{a} \right)$
=> $\boxed{S_{a}^{-1}L=aLS_{a}}$

e.g. $L\sin(s)=\frac{1}{s^{2}+1}$, then $L^{-1}\left( s\to \frac{1}{s^{2}+a^{2}} \right)$
- $L^{-1}\left( s\to \frac{1}{s^{2}+a^{2}} \right)=\frac{1}{a^{2}}L^{-1}\left( s\to \frac{1}{\left( \frac{s}{a} \right)^{2}+1}  \right)$$=S^{-2}L^{-1}\left( \left( s\to \frac{1}{s^{2}+1} \right)S^{-1} \right)=S^{-2}L^{-1}((L\sin)S^{-1})$$=S^{-2}S\sin S=S^{-1}\sin S=t\to \frac{1}{a}\sin at$
e.g. what if $a=-1$?
we have $S_{-1}(x)=-x$, $S^{-1}_{-1}=S_{-1}$, then
$S_{-1}L=-LS_{-1}$ => $L^{-1}(t\to f(-t))(s)=-L^{-1}(t\to f(t))(-s)$
then
- $f$ even => $f=S^{-1}f$ and hence $Lf$ odd
- $f$ odd => $Lf$ similarly even
## Derivative property
using integration by parts, one have $LDf=I\times Lf-Df(0)$
more generally, $LD^{n}f=P(n)\times Lf-\sum_{k=0}^{n-1} X_{s}^{k}D^{n-1-k}f(0^{-})$

(using integration by parts, one have:
$\mathcal{L}\{ f' \}(s)=\int _{0}^{\infty}f'(t)e^{ -st } \, dt=f(t)e^{ -st }|_{0}^{\infty}+s \int _{0}^{\infty} f(t)e^{ -st } \, dt$$=s\mathcal{L}\{ f \}(s)-f(0^{-})$)

e.g. solve $y''+y=(t\geq \pi)t$ (the boolean expr yields 1 if true, 0 if false), $y=y'=0$ at $t=0$

- take the laplace of two sides $(s^{2}+1)Ly-sy'(0^{-})-y(0^{-})=L(X\times uT^{-\pi})$
- one can calc RHS by manually calculating the integral $\int _{\pi}^{\infty} te^{ -st } \, dx=e^{ -\pi s }\left( \frac{1}{s^{2}}+\frac{\pi}{s} \right)=e^{ -\pi s } \frac{\pi s+1}{s^{2}+1}$
- then, $Ly(s)=e^{ -\pi s } \frac{\pi s+1}{s^{2}(s^{2}+1)}=e^{ -\pi s }\left( \frac{\pi}{s}+\frac{1}{s^{2}}-\frac{\pi s+1}{s^{2}+1} \right)$
- $y=L^{-1}\left( s\to e^{ -\pi s }\left( \frac{\pi}{s}+\frac{1}{s^{2}}-\frac{\pi s+1}{s^{2}+1} \right) \right)$$=L^{-1}\left( \exp(-\pi X_{s})\times\left( \frac{\pi}{s}+\frac{1}{s^{2}}-\frac{\pi s+1}{s^{2}+1} \right) \right)$$=\left(L^{-1}\left( \frac{\pi}{s}+\frac{1}{s^{2}}-\frac{\pi s+1}{s^{2}+1} \right)\times u\right)T^{-\pi}$$u(t-\pi)(\pi+(t-\pi)+\pi \cos(t-\pi)+\sin(t-\pi))$$=u(t-\pi)(t+\pi \cos t+\sin t)$

## Integral property
let $F(t)=\int _{0}^{t} f(x) \, dx$
then $Lf(s)=LF'(s)=sLF(s)-F(0)$
=> $LF(s)=\frac{1}{s}Lf(s)$ and

e.g. find inv laplace of $\frac{1}{s}$
$Lf(s)=1$ => $f=\delta$
=> $F=\int _{0}^{t} \delta(x) \, dx=1$ => $L^{-1}\left( s\to \frac{1}{s} \right)=1$

## Laplace of stuff
We have
- $L(1)(s)=\frac{1}{s}$
- $L(t\to u(t-1))=\frac{e^{ -s }}{s}$
- $L(X^{n})=\int _{0}^{\infty}e^{ -st }t^{n} \, dt=\frac{\Gamma(n+1)}{s^{n+1}}$
Then
- $L(\exp)=L(\exp \times 1)=T^{-1}L(1)=\frac{1}{s-1}$
- $LI=\frac{1}{s^{2}}$, $I$ is the identity function
Using the scaling property:
- $L(t\to e^{ at })=L(\exp S(a))=S^{-1}(a)(L\exp)S^{-1}(a)$$=\frac{1}{a}\cdot \frac{1}{\frac{s}{a}-1}=\frac{1}{s-a}$
- $L\cos S(a)=\mathrm{Re}Le^{ aiX }=\mathrm{Re}L(\exp S(ai))=\mathrm{Re} \frac{1}{ai\left( \frac{s}{ai}-1 \right)}$$=\mathrm{Re}\frac{s+ai}{s^{2}+a^{2}}=\frac{s}{s^{2}+a^{2}}$
- $L\sin S(a)=\frac{a}{s^{2}+a^{2}}$ (similar reasons)
- $L\cosh S(a)=\frac{s}{s^{2}-a^{2}}$
- $L\sinh S(a)=\frac{a}{s^{2}-a^{2}}$
- $L(t\to u(t-a))=\frac{e^{ -as }}{s}$
## Laplace conditions
- "Liên tục từng khúc": $f$ LTTK on $I$ if there is a partition $I_{1},I_{2},\dots,I_{n}$ s.t. $f$ continuous on $I_{k}$ for every $k \in 1..n$
- $f$ is exponentially-bounded if $f(x)\leq Me^{ cx }$ for all large $x$'s
- If $f$ LTTK, exponentially-bounded by $Me^{ cx }$, then $f$ has [[laplace]] transform $F$ well-defined on $(c, +\infty)$
- **corollary**: $F(s)\to0$ as $s\to \infty$
=> every rational function (with deg of numerator < deg of denominator) has a laplace transform

## Inverse Laplace
One can trivially prove that the inverse laplace transform of a function $F$ is unique (if it exists) in a sense like so:
- If $Lf_{1}=Lf_{2}=F$, then $f_{1}=f_{2}$ at points when both $f_{1}$ and $f_{2}$ is continuous.

e.g. $L^{-1}\left( s\to \frac{1}{s^{3}+s} \right)$
- $\frac{1}{s^{3}+s}=\frac{(s^{2}+1)-s^{2}}{s(s^{2}+1)}$$=\frac{1}{s}-\frac{s}{s^{2}+1}=L(t\to 1)-L(t\to \cos t)=L(t\to 1-\cos t)$
- => $L^{-1}\left( s\to \frac{1}{s^{3}+s} \right)=t\to1-\cos t$

### Weird ways to calculate Laplace
#### $f(t)=tg(t)$
e.g. $L(t\to te^{ at })$
- ye we can use $L(I\times \exp S(a))=T^{-a}LI$$=T^{-a}\left( s\to \frac{1}{s^{2}} \right)=\frac{1}{(s-a)^{2}}$
- but it would be cool to do this instead
	- $f'(t)=g(t)+tg'(t)=e^{ at }+af(t)$
	- taking the laplace of two sides $Lf'=\frac{1}{s-a}+aLf$ => $sLf-f(0)=\frac{1}{s-a}+aLf$ => $Lf(s)=\frac{1}{(s-a)^{2}}$

e.g. $L(t\to t\cosh at)$
$f(t)=t\cosh at=\frac{1}{2}(te^{ at }+te^{ -at })$$=\frac{1}{2}\left( \frac{1}{(s-a)^{2}}+\frac{1}{(s+a)^{2}} \right)=\frac{s^{2}+a^{2}}{(s^{2}-a^{2})^{2}}$

e.g. $L(t\to t\sin at)$
- ye we can do the complex thing
- $f''(t)=2a\cos at-f(t)$
- => $s^{2}Lf-sf(0)-f'(0)=\frac{2as}{s^{2}+a^{2}}-a^{2}Lf$
- => $Lf=\frac{2as}{(s^{2}+a^{2})^{2}}$

## Of integral
If $f$ has exp-order bla bla, $F=Lf$, then we have:
$$
\boxed{L\left( t\to\int _{0}^{t} f(\tau) \, d\tau  \right)(s)=\frac{F(s)}{s}}
$$
**proof**: using the derivative rule (and u need to prove LHS exists btw)

e.g. $L^{-1}\left( s\to \frac{1}{s^{2}(s-a)} \right)$
we have (if $a\neq 0$): $L^{-1}\left( s\to \frac{1}{s(s-a)} \right)=\frac{1}{a}L^{-1}\left( s\to \frac{1}{s-a} -\frac{1}{s}\right)$$=\frac{1}{a}(e^{ at }-1)$
=> $L^{-1}\left( s\to \frac{1}{s^{2}(s-a)} \right)=\int _{0}^{t} \frac{1}{a}(e^{ a\tau  }-1) \, d\tau$$=\frac{1}{a^{2}}(e^{ at }-1)-\frac{t}{a}=\frac{e^{ at }-at-1}{a^{2}}$

e.g. $L^{-1}\left( s\to \frac{13s+14}{(s+2)^{2}(s-1)} \right)$
$F(s)=\frac{13s+14}{(s+2)^{2}(s-1)}=\frac{9}{(s+2)(s-1)}+\frac{4}{(s+2)^{2}}$$=\frac{3}{s-1}-\frac{3}{s+2}+\frac{4}{(s+2)^{2}}$
=> $F=3(T^{-1}-T^{2})\left( s\to \frac{1}{s} \right)+4T^{2}\left( s\to \frac{1}{s^{2}} \right)$
=> $F=3(T^{-1}-T^{2})L(1)+4T^{2}L(t\to t)$
=> $L^{-1}F=3(t\to e^{ t }-e^{ -2t })+4(t\to te^{ -2t })$$=t\to 3e^{ t }+(4t-3)e^{ -2t }$

e.g. $x'''-2x''+16x=0, x(0)=x'(0)=x''(0)-20=0$
we have $L(D^{3}-2D^{2}+16)x(s)=0$
=> $(s^{3}-2s^{2}+16)Lx(s)=20$ => $x=s\to \frac{20}{(s+2)((s-2)^{2}+4)}=\frac{A}{s+2}+\frac{Bx+C}{(s-2)^{2}+4}$, with $A=1,B=-1,C=6$
=> $Lx=s\to \frac{1}{s+2}-\frac{(s-2)}{(s-2)^{2}+4}+\frac{4}{(s-2)^{2}+4}$$=T^{2}L(1)-T^{-2}\left( s\to \frac{s}{s^{2}+4} - \frac{4}{s^{2}+4} \right)$$=L(S_{-2}\exp \times 1) -L(S_{2}\times \exp (t\to\cos 2t + 2\sin 2t))$
=> $x=e^{ -2t }-e^{ 2t }(\cos 2t-2\sin 2t )$

## Operations on Laplace

### Convolution
we have $L(f \ast g)=Lf\times Lg$, with $\ast$ denoting convolution, i.e. $(f\ast g)(\tau)=\int _{0}^{\tau} f(t)g(\tau-t) \, dt$ (actually the bounds are wrong but whatever), so:
e.g. prove $L^{-1}\left( F=s\to \frac{s}{(s^{2}+k^{2})^{2}} \right)=\frac{1}{2k}t\sin kt$
we have $s\to \frac{s}{(s^{2}+1)^{2}}=L\cos \times L\sin=L(\sin \ast \cos)$, which is

$(\sin \ast \cos)(\tau)=\int _{0}^{\tau} \sin(t)\cos(\tau-t) \, dt=\int _{0}^{\tau} \frac{\sin(\tau)+\sin(2t-\tau)}{2} \, dt$$=\frac{1}{2}\tau \sin \tau$(the other term cancels)

letting $s=\frac{s'}{k}$, we have $\frac{s}{(s^{2}+1)^{2}}=\frac{k^{3}s'}{(s'^{2}+k^{2})^{2}}=k^{3}F(ks)=k^{3}S_{k}F(s)$ => $L\left( t\to\frac{1}{2}t\sin t \right)=k^{3}S_{k}F(s)$ and $L^{-1}(k^{3}S_{k}F)=k^{3}L^{-1}S_{k}F$

we have $S_{a}^{-1}L=aLS_{a}$ => $L^{-1}S_{\frac{1}{a}}L=aS_{a}$ => $L^{-1}S_{a}=\frac{1}{a}S_{a}^{-1}L^{-1}$, or $L^{-1}S_{a}^{-1}=aS_{a}L^{-1}$
=> $RHS=k^{2}S_{\frac{1}{k}}L^{-1}F=t\to \frac{1}{2}t\sin t$
=> $S_{\frac{1}{k}}L^{-1}F=t\to\frac{1}{2k^{2}}t\sin t$ => $L^{-1}F=t\to \frac{1}{2k^{2}}(kt)\sin kt=\frac{1}{2k}t\sin kt$, qed

e.g. prove $L^{-1}\left( s\to \frac{1}{(s^{2}+k^{2})^{2}} \right)=\frac{1}{2k^{3}}(\sin kt-kt\cos kt)$
similarly, we directly calculate:
$s\to \frac{1}{(s^{2}+k^{2})^{2}}=\frac{1}{k^{2}}LS_{k}\sin \times LS_{k}\sin=\frac{1}{k^{2}}L(S_{k}\sin \ast S_{k}\sin)$
with $(S_{k}\sin\ast S_{k}\sin)(t)=\int _{0}^{t} \sin(k\tau)\sin(k(t-\tau)) \, d\tau=\int _{0}^{t} \frac{\cos k(2\tau-t)-\cos(kt)}{2} \, d\tau$$=\dots=\frac{1}{2k}\sin kt-\frac{1}{2k}t\cos kt$ => qed

### Derivative
- (piecewise cont
- exp bounded)
$Lf(s)=\int _{0}^{\infty} e^{ -st }f(t) \, dt$
=> $\frac{d}{ds}Lf(s)=\int _{0}^{\infty} -e^{ -st }tf(t) \, dx=-L(X \times f)$ (assuming one can take the integral like this, blabla [[uniconv]])
=> $DLf+L(X\times f)=0$
=> $D^{n}Lf=L((-X)^{\times n}\times f)$
=> $L^{-1}D^{n}F=(-X)^{\times n}\times L^{-1}F$
=> $L^{-1}D^{n}Lf=(-X)^{\times n}f$ => $L^{-1}D^{n}F=(-X)^{\times n}\times L^{-1}F$
=> $L^{-1}F=\frac{L^{-1}D^{n}F}{(-X)^{\times n}}$
e.g. we have $L\sin =s\to \frac{1}{s^{2}+1}$
=> $\frac{d}{ds} \frac{1}{s^{2}+1}+L(t\sin t)=0$ => $L(t\sin t)=\frac{2s}{(s^{2}+1)^{2}}$

e.g. $L^{-1} \arctan \frac{1}{X}=\frac{L^{-1} \frac{d}{ds} \arctan \frac{1}{s}}{-t}=\frac{1}{t}L^{-1} \frac{1}{s^{2}+1}=\frac{\sin t}{t}$
### Integral
Similarly, we have $L\left( \frac{f}{X} \right)=s\to\int _{s}^{\infty} Lf(\sigma) \, d\sigma$
(needs additional condition: $\lim_{ t \to 0^{+} } \frac{f(t)}{t}$ finite and exists)

=> $L^{-1}F(t)=tL^{-1}\left( \int _{s}^{\infty}F(s_{1}) \, ds_{1} \right)(t)$

$Lf?, f(t)=\int _{0}^{t} \sin(t-x)\cos 2x \, dx$
$a=\sin,b=S_{2}\cos$ => $f=a \ast b$
=> $L(a\ast b)=LaLb= \frac{1}{s^{2}+1}\cdot \frac{s}{s^{2}+4}=\frac{s}{(s^{2}+1)(s^{2}+4)}$

e.g. $L^{-1}\left( s \to \arctan \frac{3}{s+2} \right)=-\frac{1}{t}L\left( s\to -\frac{3}{(s+2)^{2}+9} \right)=-\frac{1}{t}e^{ -2t }\sin 3t$
e.g. $tx''+(t-3)x'+2x=0$, $x(0)=0$
we have:
- $L(tx'')=-\frac{d}{ds}L(x'')=-\frac{d}{ds}(s^{2}Lx-sx(0)-x'(0))$$=-2sLx-s^{2}(Lx)'=-2sX-s^{2}X'$
- $L(tx')=-\frac{d}{ds}L(x')=-\frac{d}{ds}(sX)$$=-X-sX'$
- $L(-3x')=-3sX$
- $L(2x)=2X$

=> $-2sX-s^{2}X'-X-sX'-3sX+2X=0$
=> $(1-5s)X=(s^{2}+s)X'$
=> $\frac{1-5s}{s^{2}+s}ds=\frac{dX}{X}$
=> $\ln|X|=\ln|s|-6\ln|s+1|+C$
=> $|X|(s+1)^{6}=C|s|$
remove the abs signs
=> $\frac{X}{C}=\frac{s}{(s+1)^{6}}=\frac{1}{(s+1)^{5}}-\frac{1}{(s+1)^{6}}=T\left( \frac{1}{s^{5}}-\frac{1}{s^{6}} \right)$
=> $x = Ce^{ -t }\left( \frac{t^{4}}{24}-\frac{t^{5}}{120} \right)$

$L\left( t \to \frac{\sinh t}{t} \right)$
**limit $\frac{\sinh t}{t}=1$ as $t\to 0^{+}$**
$L = \int _{s}^{\infty} \frac{1}{x^{2}-1} \, dx=\frac{1}{2}\ln \left| \frac{1-x}{1+x} \right||_{s}^{\infty}=\frac{1}{2}\ln \left| \frac{1+s}{1-s} \right|$

e.g. $L^{-1}\left( \frac{2s}{(s^{2}-1)^{2}} \right)$
int8 the thing:
$\int _{s}^{\infty} \frac{2s}{(s^{2}-1)^{2}} \, ds=\frac{1}{1-s^{2}}|_{s}^{\infty}=\frac{1}{s^{2}-1}=L\sinh t$
=> answer: $t\sinh t$

## piecewise

- piecewise can always be turn into sum of functions like $u(t-a)f(t)$, so we just need to calc laplace of that
- using this formula: $LT^{a}(f\times u)=S_{a}\exp \times Lf$ ($a<0$)

e.g. $L(2tu(t-2))$
$F=L(T^{-2}(u\times (t\to 2t+4)))=S_{-2}\exp \times L(t \to 2t+4)$$=e^{ -2s }\left( \frac{2}{s^{2}}+\frac{4}{s} \right)$

