> society if one does not have to touch [[uniconv]] and dumb shit when trying to do feynman's trick

e.g. $I=\int _{0}^{\pi/2} \ln(a^{2}\sin(x)^{2}+b^{2}\cos(x)^{2})\,dx$
- let rhs by $I(a)$, $f(x,a)=\ln(a^{2}\cos(x)^{2}+b^{2}\sin(x)^{2})$
- $f'_{a}(x,a)=\frac{2a\sin(x)^{2}}{a^{2}\cos(x)^{2}+b^{2}\sin(x)^{2}}$
- it's trivial to see that if $ab\neq 0$, both $f$ and $f'_{a}$ are cont/$\left[ 0, \frac{\pi}{2} \right]\times \mathbb{R}$ => you can use the [[paraint]] thing
	- then $I'(a)=\int _{0}^{\pi/2} \frac{2a\sin(x)^{2}}{a^{2}\sin(x)^{2}+b^{2}\cos(x)^{2}} \, dx=\int _{0}^{\pi/2} \frac{2a\tan(x)^{2}}{a^{2}\tan(x)^{2}+b^{2}} \, dx$
	- let $t=\tan(x) \implies dx=\frac{dt}{t^{2}+1}$
	- $I'(a)=\int _{0}^{+\infty} \frac{2at^{2}dt}{(a^{2}t^{2}+b^{2})(t^{2}+1)} \, dt=\int _{0}^{+\infty} \frac{2}{a}\left( \frac{dt}{\left( t^{2}+\frac{b^{2}}{a^{2}} \right)(t^{2}+1)} \right)=$ $\int _{0}^{+\infty} \frac{2}{a\left( \frac{b^{2}}{a^{2}}-1 \right)}\left( \frac{dt}{t^{2}+1}-\frac{dt}{t^{2}+\frac{b^{2}}{a^{2}}} \right)=\frac{2a}{b^{2}-a^{2}}\left( \arctan x-\frac{b}{a}\arctan \frac{ax}{b} \right)|_{x=0}^{+\infty}$ $= \frac{2a}{b^{2}-a^{2}}\left( \frac{\pi}{2} -\frac{a\pi}{2b} \right)=\frac{\pi\left( a-\frac{a^{2}}{b} \right)}{b^{2}-a^{2}}=\frac{\pi}{a+b}$
	- therefore, $I(a)=\pi \ln|a+b|+C$, and since $I(b)=\int _{0}^{\pi/2} 2\ln|b| \, dx=\pi \ln|b|\implies C=\pi \ln|b|-\pi \ln|2b|=-\pi \ln 2$
	- hence, $I(a)=\pi \ln | \frac{a+b}{2}|$
- in the $ab=0$ case, wlog assuming $a=0$, then $I=\int _{0}^{\pi/2} \ln(b^{2}\cos (x)^{2}) \, dx=\pi \ln|b|+2\int _{0}^{\pi/2}\ln\cos x \, dx$
	- to calc $J=\int _{0}^{\pi/2} \ln \cos x \, dx$, first u need $J=\int _{0}^{\pi/2} \ln \sin x \, dx$
	- => $2J=\int _{0}^{\pi/2} \ln(\sin x\cos x) \, dx=\int _{0}^{\pi/2} \ln \sin 2x \, dx -\frac{\pi \ln 2}{2}$
	- simple var sub => $2J=J-\frac{\pi \ln 2}{2} \implies J=-\frac{\pi \ln 2}{2}$ => $I=\pi \ln | \frac{b}{2} |$ (consistent with prev result)

e.g. $\int _{0}^{\pi} \ln(1-2a\cos x+a^{2}) \, dx$
- let RHS be $I(a)$, $f(x,a)=\ln(1-2a\cos x+a^{2})$
- $f$ not cont. at 2 points: $(x=0,a=1)$ and $(x=\pi,a=-1)$
- first, we notice that $I(-a)=\int _{0}^{\pi} \ln(1+2a\cos x+a^{2}) \, dx=I(a)$ (sub bla bla)
- 3 cases
	- $a=1$ => $I=\int _{0}^{\pi} \ln(2-2\cos x) \, dx=\int _{0}^{\pi} \ln\left( 4\sin\left( \frac{x}{2} \right)^{2} \right) \, dx$$=\pi \ln 4+2\int _{0}^{\pi}\ln |\sin \frac{x}{2}| \, dx=\pi \ln 4-2\pi \ln 2=0$ (see prev e.g.)
	- $a=-1$ then $I=0$ because of the above case
	- $a\neq \pm 1$
		- then there is a neighborhood of $a$ where $f$ and $f'_{a}$ are both cont (with $x$ ofc)
		- then $I(a)+I(-a)=\int _{0}^{\pi} \ln((1+a^{2})^{2}-4a^{2}\cos(x)^{2}) \, dx$$=\int _{0}^{\pi}\ln(1-2a^{2}\cos 2x+a^{4}) \, dx=I(a^{2})$ (some sub and even gaming)
		- therefore, $I(a)=\frac{I(a^{2})}{2}=\frac{I(a^{2^{n}})}{2^{n}}$
		- to make it approaches stuff, one would need $I(a)$ to be cont., which is true since $f$ cont / $[0,\pi]\times[a-\varepsilon,a+\varepsilon]$
		- now, 2 cases:
			- if $|a|<1$, then as $n\to \infty$, $RHS\to 0$ => $I(a)=0$
			- if $|a|> 1$, then one rewrite $I(a)$ as $I(a)=\int _{0}^{\pi} \ln\left( \frac{1}{a^{2}} + \frac{2}{a}\cos x+1 \right) \, dx + 2\pi \ln a=I\left( \frac{1}{a} \right) + 2\pi \ln a=2\pi \ln a$
- or u can do the traditional way: $I'(a)=\int _{0}^{\pi} \frac{2a-2\cos x}{1-2a\cos x+a^{2}} \, dx=\frac{\pi}{a}+\int _{0}^{\pi} \frac{a^{2}-1}{1-2a\cos x+a^{2}} \, dx$
- weierstrass sub $t=\tan \frac{x}{2}, \cos x=\frac{1-t^{2}}{1+t^{2}}, dt=\frac{2dx}{1+t^{2}}$
- $I'(a)=\frac{\pi}{a}+\frac{2}{a}\int _{0}^{\pi} \frac{a^{2}-1}{(1-a)^{2}+(1+a)^{2}t^{2}} \, dx=\frac{\pi}{a}+\frac{2}{a} \arctan\left( \frac{a-1}{(a+1)t^{2}} \right)|_{t=0}^{\infty}$$=\frac{\pi}{a}(1+sgn(a^{2}-1))$
- now, since $I(0)=0$ (ez to eval), one can see $I(a)=0$ for all $a \in (-1,1)$, then u consider the two special cases too
- for $|a|>1$, one can do the $I\left( \frac{1}{a} \right)$ trick like above or prove that $I(a)$ cont at $a=\pm 1$ (idk how tho)

e.g. $I(n,m)=\int _{0}^{1}x^{n-1}\ln(x)^{m} \, dx$

- let $t=\ln x$, then $I(n,m)=\int _{-\infty}^{0} t^{m} e^{ nt } \, dt$
- in an ideal world, $I'_{m}(n,m)=m\int _{-\infty}^{0} t^{m-1}e^{ nt } \, dx=mI(n,m-1)$
- snaps back to reality: we need to prove some [[uniconv]] shit
	- first, the derv $mt^{m-1}e^{ nt }$ is cont on $\mathbb{R}^{2}$, so that's done
	- secondly, $\int _{-\infty}^{0} t^{m}e^{nt} \, dx$ conv iff bla bla conditions
	- 


e.g. $\int _{0}^{1} \frac{\ln(1-a^{2}x^{2})}{x^{2}\sqrt{ 1-x^{2} }} \, dx$, for $a\in[-1,1]$
to differentiate the thing, one would need $f(x,a)=\frac{\ln(1-a^{2}x^{2})}{x^{2}\sqrt{ 1-x^{2} }}$, $f'_{a}(x,a)=\frac{-2a}{(1-a^{2}x^{2})\sqrt{ 1-x^{2} }}$
- $f,f'_{a}$ cont on $(0,1)\times[-1+\varepsilon,1-\varepsilon]$ (not cont at $a=\pm 1$ tho)
- original paraim conv: the numerator is bounded as $b\in [-1+\varepsilon,1-\varepsilon]$ and since $\int _0^{1} \frac{1}{x^{2}\sqrt{ 1-x^{2} }}\,dx$ conv => the original integral conv
- the derv paraim [[uniconv]]: $-\frac{2a}{1-a^{2}x^{2}}$ is bounded => [[weierstrass m-test]]
=> $I'(a)=\int _{0}^{1} -\frac{2a}{(1-a^{2}x^{2})\sqrt{ 1-x^{2} }} \, dx=-2a\int _{0}^{\pi/2} \frac{1}{1-a^{2}\sin ^{2}t} \, dt$$=-2a\int _{0}^{\infty} \frac{1}{\frac{1}{\sin ^{2}t}-a^{2}} \, d(\cot t)=-2a\int _{0}^{\infty} \frac{1}{u^{2}-a^{2}+1}\, du=-\frac{2a}{\sqrt{ 1-a^{2} }}$
=> $I(a)=2\sqrt{ 1-a^{2} }$

- for $a=\pm 1$: $\int _{0}^{1} \frac{\ln(1-x^{2})}{x^{2}\sqrt{ 1-x^{2} }} \, dx$
	- let $x=\sin t$ => $\int _{0}^{\pi/2} \frac{\ln \cos x}{\sin(x)^{2}} \, dx$
	- let $u = \ln\cos x$ => $du=-\tan xdx$ => ...t hiểu r

$I(a)=\int _{0}^{\infty} \frac{\ln(a^{2}+x^{2})}{b^{2}+x^{2}} \, dx$
- we have $f(x,a)=\frac{\ln(x^{2}+a^{2})}{x^{2}+b^{2}}$, $f'_{a}(x,a)=\frac{2a}{(x^{2}+a^{2})(x^{2}+b^{2})}$
	- with $f,f'_{a}$ cont/ $[0,+\infty)\times(\varepsilon, M)$
	- $\int f(x,a) \, dx$ conv because $\frac{\ln(a^{2}+x^{2})}{b^{2}+x^{2}}< \frac{1}{x^{3/2}}$ for large $x$
	- $\int _{0}^{\infty} \frac{2a}{(x^{2}+a^{2})(x^{2}+b^{2})} \, dx$ because integrand < $\frac{2M}{\varepsilon^{2}(x^{2}+b^{2})}$ conv
- then $I'(a)=\int _{0}^{\infty} \frac{2a}{(x^{2}+a^{2})(x^{2}+b^{2})} \, dx=\frac{2a}{b^{2}-a^{2}}\int _{0}^{\infty} \left(\frac{1}{x^{2}+a^{2}}-\frac{1}{x^{2}+b^{2}}\right) \, dx$$=\frac{2a}{b^{2}-a^{2}}\cdot \frac{\pi}{2}\left( \frac{1}{a}-\frac{1}{b} \right)=\frac{\pi}{b(a+b)}$ => $I(a)=\frac{\pi \ln(a+b)}{b}-C(b)$
- with $a=b$, we have $\frac{\pi \ln 2b}{b}-C(b)=\int _{0}^{\infty} \frac{\ln(x^{2}+b^{2})}{x^{2}+b^{2}} \, dx$
	- sub $x=b\tan t$, $x^{2}+b^{2}=b\sec(t)^{2}$ and $dx=b \sec(t)^{2}dt$, then RHS is $\int _{0}^{\pi/2} \ln(b\sec(t)^{2}) \, dt=\frac{\pi \ln b}{2}-2\int _{0}^{\infty} \ln \cos t \, dt=\frac{\pi \ln b}{2}-\pi \ln 2$
- => $C(b)=\pi \ln  2$ for all $b>0$