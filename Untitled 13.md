$e^{ at }f(t)\implies F(s-a)$
$u(t-a)f(t-a)\implies e^{ -as }F(s)$
$(f\ast g)(t)\implies F(s)G(s)$

$t^{n}f(t) \implies (-1)^{n} \frac{d^{n}}{ds^{n}}F(s)$
$\frac{f(t)}{t} \implies \int _{s}^{\infty} F(\sigma) \, d\sigma$

$f^{(n)}(t) \implies s^{n}F(x)-\sum_{k=0}^{n-1} s^{k}f^{(n-1-k)}(0)$
$\int _{0}^{t} f(\tau) \, d\tau \implies \frac{F(s)}{s}$

e.g. $f(t)=u(t-2)u(4-t)\cos \pi t$
=> $Lf$?

- $f(t)=T^{-2}(u(t)u(2-t)\cos \pi t)$
=> $Lf=LT^{-2}(u\times (u(2-t)\cos \pi t))=e^{ -2s }L(u(2-t)\cos \pi t)$
$L(u(2-t)\cos \pi t)=L((1-u(t-2))\cos \pi t)$$=L(\cos \pi t)-LT^{-2}(u\times S_{\pi}\cos)$
$=\frac{s}{s^{2}+\pi^{2}}-e^{ -2s }\left( \frac{s}{s^{2}+\pi^{2}} \right)$
=> $Lf=e^{ -2s }(1-e^{ -2s }) \frac{s}{s^{2}+\pi^{2}}$


$I=\iint_{S} \text{curl} F.nds=\int _{C} F \, dl=\int _{C} (-yzdx+zxdy+xydz)$
với $C$ là biên của $S$, do $S$ hướng lên trên nên $C$ có chiều ngược KĐH
tham số hóa $C$: $x=\frac{3}{\sqrt{ 2 }}\cos t,y=3\sin t,z=3\left( 1-\frac{1}{\sqrt{ 2 }}\cos t \right)$
=> $x'=-\frac{3}{\sqrt{ 2 }}\sin t,y'=3\cos t,z'=\frac{3}{\sqrt{ 2 }}\sin t$


