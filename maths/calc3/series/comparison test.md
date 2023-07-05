let $sa_{n}$ be positive series
then
- if $\exists b_{n}>0$ s.t. $a_{n}\geq b_{n}$ for arbitrarily large n's and $sb_{n}$ div then $sa_{n}$ div
- if $\exists b_{n}>0$ s.t. $a_{n}\leq b_{n}$ for ... and $sb_{n}$ conv then $sa_{n}$ conv

**corollary**
if $c = \lim_{ n \to \infty } \frac{a_{n}}{b_{n}}$ finite then $sa_{n}$ conv iff $sb_{n}$ conv

## arbitary signs
remove the positive series condition from the corollary, now we need $\frac{a_{n}}{b_{n}}$ is monotonic for large n's

then
- ($c$ may equals 0) $b_{n}$ conv => $a_{n}$ conv
- if $c\ne 0$, the two series being [[abs conv]]/[[cond conv]]/div are equivalent

**proof**
let $c_{n}=\frac{a_{n}}{b_{n}}$, then $a_{n}=b_{n}c_{n}$, this is basically [[abel test]]

e.g. $\sum_{n=1}^{\infty} \frac{1}{\ln^{2} \sin \frac{1}{n}}$
- we know $\sin \frac{1}{n} \sim \frac{1}{n}$, then $\ln^{2} \sin \frac{1}{n} \sim \ln^{2} \frac{1}{n}=\ln^{2} n < n$ => div

e.g. $\sum_{n=1}^{\infty} (1+\frac{1}{n})^{n^{2}}x^{n}$
- using [[root test]], conv for all $\left( -\frac{1}{e}, \frac{1}{e} \right)$, div for $|x|> \frac{1}{e}$
- at $x=\frac{1}{e}$: $\lim_{ n \to \infty } \frac{\left( 1+\frac{1}{n} \right)^{n^{2}}}{e^{n}}=\lim_{ n \to \infty } \left( \frac{\left( 1+\frac{1}{n} \right)^{n}}{e} \right)^{n}$$=e^{ \lim_{ n \to \infty } n\ln \frac{(1+1/n)^{n}}{e} }=e^{ \lim_{ n \to \infty } n (n\ln(1+1/n)-1) }$
	- exponent is $n\left( n\left( \frac{1}{n}-\frac{1}{2n^{2}}+o\left( \frac{1}{n^{2}} \right) \right) - 1 \right)=-\frac{1}{2}+o(1)$ => limit is $e^{ -1/2 }$, which is clearly not 0 =>fail the [[n term test]]
- at $x=-\frac{1}{e}$, the same shit

e.g. prove $0<\int _{0}^{\infty} \frac{x}{e^{ x }-1} \, dx-\sum_{n=1}^{2016} \frac{1}{n^{2}} < \frac{1}{2016}$
- we just need to prove: $\int _{0}^{\infty} \frac{x}{e^{ x }-1} \, dx=\sum_{n=1}^{\infty} \frac{1}{n^{2}}$
- we have $\int _{0}^{\infty} \frac{x}{e^{ x }-1} \, dx$ => $\int _{0}^{\infty} \frac{xe^{ -x }}{1-e^{ -x }} \, dx=\int _{0}^{1} -\frac{\ln(1-x)}{x} \, dx$
- now, we have $-\ln(1-x)=\sum_{n=1}^{\infty} \frac{x^{n}}{n}$, which means that the integral is $\int _{0}^{1} \sum_{n=1}^{\infty} \frac{x^{n-1}}{n} \, dx$
	- the maclaurin holds true for all $x\in [0,1)$, so there is only a difference at the singularity $x=1$, no problem
	- to swap integral, one needs to prove that the series $\sum_{n=1}^{\infty} \frac{x^{n-1}}{n}$ is [[uniconv]] (and some irrelevant cont bs), which is totally true because it's a [[power series]]
	- => the integral is $\sum_{n=1}^{\infty} \int _{0}^{1} \frac{x^{n-1}}{n} \, dx=\sum_{n=1}^{\infty} \frac{1}{n^{2}}$, qed