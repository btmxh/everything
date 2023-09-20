$(x^{2}-y)dx+xdy=0$
=> $x^{2}dx=ydx-xdy$
if $y=0$ => $dy=0$ => $x=0$
$t^{2}dx=dt$, with $t=\frac{x}{y}$
=> $t=0$ then ok
oth $dx=\frac{dt}{t^{2}}$
=> $x+\frac{1}{t}=x+\frac{y}{x}$ const

$x'=4x-y-z+t$
$y'=x+2y-z$
$z'=x-y+2z$
$u=y+z$
$x'=4x-u+t$
$u'=2x+u$
=> $u=4x-x'+t$
=> $4x'-x''+1=2x+4x-x'+t$
=> $x''-5x'+6x=1-t$
$x=-\frac{1}{6}t+\frac{1}{36}+Ae^{ 2t }+Be^{ 3t }$
$u=4x-x'+t=2Ae^{ 2t }+Be^{ 3t }+\frac{t}{3}+\frac{5}{18}$
=> $y'=x+2y-z=x+3y-u$, with $x-u=-Ae^{ 2t }-\frac{t}{2}-\frac{1}{4}$
=> $y'-3y=-Ae^{ 2t }-\frac{t}{2}-\frac{1}{4}$
=> $y=Ce^{ 3t }+Ae^{ 2t }+\frac{1}{6}t+\frac{5}{36}$
$z=u-y=Ae^{ 2t }+(B-C)e^{ 3t }+\frac{1}{6}t+\frac{5t}{36}$

$x^{2}(1-x)y''-x(1+x)y'+y=0$
$y=\sum_{n=0}^{\infty} a_{n}x^{n}$
=> $\sum_{n=1}^{\infty} a_{n}(n(n-1)(1-x)-n(1+x)+1)x^{n}+a_{0}=0$
=> $\sum_{n=1}^{\infty} a_{n}((n-1)^{2}-n^{2}x)x^{n}+a_{0}=0$
=> $\sum_{n=1}^{\infty} a_{n}(n-1)^{2}x^{n}-\sum_{n=1}^{\infty} a_{n}n^{2}x^{n+1}+a_{0}=0$
=> $\sum_{n=1}^{\infty} (a_{n+1}-a_{n})n^{2}x^{n+1}+a_{0}=0$
=> $a_{n}=a_{n+1}$ for all $n\geq 1$ and $a_{0}=0$
=> $y=x+x^{2}+x^{3}+\dots=\frac{1}{1-x}$

liouville
$\frac{y_{2}}{y_{1}}=\int \frac{dx}{ay_{1}^{2}}$
with $p=\frac{1+x}{x(1-x)}=\frac{1}{x}+\frac{2}{1-x}$, $a=e^{ \int p(x) \, dx }=e^{ \ln x-2\ln|1-x| }=\frac{x}{(1-x)^{2}}$
=> $\frac{y_{2}}{y_{1}}=\int \frac{(1-x)^{4}dx}{x}=\int \left( x^{3}-4x^{2}+6x-4+\frac{1}{x} \right) \, dx$
=> $y_{2}=\frac{\frac{x^{4}}{4}-\frac{4}{3}x^{3}+3x^{2}-4x+\ln|x|}{1-x}$

$\sum_{n=2}^{\infty} \frac{\ln^{2}n}{n^{3/2}}$ conv due to less than $\frac{1}{n^{5/4}}$
$\sum_{n=1}^{\infty} \frac{\cos n}{\sqrt{ n }+\cos n}$
$a_{n}=\frac{x}{1+x}$ with $x=\frac{\cos n}{\sqrt{ n }}$
=> $a_{n}=x^{2}-x^{3}+o(x^{3})=\frac{\cos^{2}n}{n}-\frac{\cos^{3}n}{n^{3/2}}+o\left( \frac{1}{n^{3/2}} \right)$

last two series conv
the first one: $\frac{1-\cos 2n}{n}$
$\frac{\cos 2n}{n}$ conv due to dirichlet:
- $\sum \cos kn$ is bounded, $\frac{1}{n}$ mono dec cov to 0
=> 1/n not conv => div

$x=\sigma^{2}$ then $S(\sigma^{2})=\cosh \sigma$
if $x=-\sigma^{2}$ then $S(x)=S((i\sigma)^{2})=\cosh i\sigma=\cos \sigma$

$f^{(n)}(0)=n^{2}$ for all $n$
=> $f(x)=\sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^{n}=\sum_{n=1}^{\infty} \frac{n}{(n-1)!}x^{n}$
$=\sum_{n=2}^{\infty} \frac{x^{n}}{(n-2)!}+\sum_{n=1}^{\infty} \frac{x^{n}}{(n-1)!}$
$=x^{2}e^{ x }+xe^{ x }=(x^{2}+x)e^{ x }$

$$





