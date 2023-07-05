$\lim_{ n \to \infty }\sqrt[n]{ | a_{n}| } = L\in R$ then
- if $L<1$, $sa_{n}$ abs conv
- if $L>1$, $sa_n$ div
- otherwise, the test is inconclusive

**NOTE**: if $L=\infty$, then u gotta manually do the $L>1$ case

**proof**
if $L<1$, there exists $n_{0}$ s.t. $\sqrt[n]{ |a_{n}| }<q<1$ for every $n>n_{0}$
then $|a_{n}|<q^n$ => $s|a_{n}|$ [[geom series]] conv.
if $L>1$, $\lim_{ n \to \infty } a_{n}>\lim_{ n \to \infty }L^n=\infty$ violate the [[n term test]]

e.g. conv region of $\sum_{n=1}^{\infty} \frac{x^{n^{2}}}{2^{n}}$
- we have $\sqrt[n]{ \frac{x^{n^{2}}}{2^{n}} }=\frac{x^{n}}{2}$, which conv to <1 iff $|x|<1$
- if $|x|>1$, one can simply use [[n term test]] => div
- if $x=\pm 1$, then $x^{n^{2}}=(\pm1)^{n}$ => series is $\sum_{n=1}^{\infty} (\pm \frac{1}{2})^{n}$ conv
- => region $[-1,1]$

e.g. conv region of $\sum_{n=1}^{\infty} \frac{(-1)^{n}}{(x+n)^{p}}$
- by [[n term test]], $\lim_{ n \to \infty } (x+n)^{p}=\infty$, and since $\lim_{ n \to \infty }(x+n)=\infty$, $p>0$
- then this [[conv]] by [[leibnitz test]] if $p>0$
- the abs series is asympt to $\sum_{n=1}^{\infty} \frac{1}{n^{p}}$, which conv iff $p>1$ => [[abs conv]] iff $p>1$

e.g. $\sum_{n=1}^{\infty} (e-\left( 1+\frac{1}{n} \right)^{n})^{x}$
we have $\frac{\left( 1+\frac{1}{n} \right)^{n}}{e}=\exp \left( n\ln\left( 1+\frac{1}{n} \right)-1 \right)=\exp (-\frac{1}{2n}+o\left( \frac{1}{n} \right))$
=> base is $e^{ x }\left( 1-\exp\left( -\frac{1}{2n} +o\left( \frac{1}{n} \right) \right) \right)^{x} \sim (\frac{e}{2n})^{x}$
then this thing conv if $x>1$

e.g. $\sum_{n=1}^{\infty} \ln\left( 1+\frac{(-1)^{n}}{n^{x}} \right)$
- [[n term test]] => $x>0$
- we have $a_{n}(x)=\frac{(-1)^{n}}{n^{x}}-\frac{1}{n^{2x}}(1+o(1))$
	- the first thing conv because of [[leibnitz test]]
	- the second thing conv iff $2x>1 \iff x> \frac{1}{2}$

