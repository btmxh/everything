a [[fn series]] with $a_{n}(x)=c_{n}(x-c)^{n}$


**theorem (abel):** if power series conv at $x_{0}\neq 0$, then it conv for all $x$ s.t. $|x-c|<|x_{0}|$
**proof**
since $|\frac{a_{n+1}}{a_{n}}|=|\frac{c_{n+1}}{c_{n}}x|<| \frac{c_{n+1}}{c_{n}}x_{0}|\leq 1$ (conv at $x_{0}$) + [[ratio test]] => conv at $x$

**corollary:** if power series div at $x_{1}$, then it div for all $x$ s.t. $|x-c|>|x_{1}|$

then let $R=\sup_{x\in X, S(x) \text{ conv}}|x-c|$ be the **radius of conv**, then one can see that $S(x)$ diverges for all $|x-c|>R$, conv for all $|x-c|<R$ (we don't know about the boundary of the conv set tho)

**theorem:** a power series [[abs conv]] on $(c-R, c+R)$

by [[ratio test]] and [[root test]], $R=\lim_{ n \to \infty } \delta c_{n}=\lim_{ n \to \infty } \frac{1}{\sqrt[n]{ c_{n} }}$ (if the limit does not exist, good luck) (see [cauchy hadamard](https://en.wikipedia.org/wiki/Cauchy%E2%80%93Hadamard_theorem) for a better formula for $R$)

**theorem:** if $[a,b]\subset (c-R, c+R)$  => power series [[uniconv]]/$[a,b]$
**proof**
use [[weierstrass m-test]]
have $|a_{n}|\leq |c_{n}\rho^{n}|$, since the power series [[abs conv]] on $(c-R, c+R)$ => qed

**corollary**
- power series is cont/$(c-R,c+R)$
- power series is diff, intbl, etc.
- (all within its radius of conv)
- **NOTE:** boundary points are not included

## power series of analytic fns
e.g. prove that the taylor series of $e^{x}$ is conv everywhere on $\mathbb{R}$
we have $c_{n}=\frac{1}{n!}$, therefore $\delta c_{n}=n+1\to \infty$ as $n\to\infty$ => $R=\infty$ => qed

e.g. power series of $\frac{1}{(1-x)^{2}}?$
we have $\frac{1}{1-x}=\sum_{n=0}^{\infty}x^{n}$ (this only conv on $(-1, 1)$)
=> $\frac{1}{(1-x)^{2}}=\frac{d}{dx}\left( \sum_{n=0}^{\infty} x^{n} \right)=\sum_{n=1}^{\infty} nx^{n-1}=\sum_{n=0}^{\infty}(n+1)x^{n}$

e.g. calc $\sum_{n=1}^{\infty}\frac{1}{(n+1)2^{n+1}}$
$\sum_{n=1}^{\infty} \frac{1}{(n+1)2^{n+1}}=\left( \sum_{n=2}^{\infty} \frac{x^{n}}{n} \right)|_{x=\frac{1}{2}}=\left( \sum_{n=2}^{\infty} \int _{0}^{x} t^{n-1} \, dt \right)|_{x=\frac{1}{2}}$$=\left( \int _{0}^{x} \sum_{n=1}^{\infty} t^{n} \, dt \right)|_{x=\frac{1}{2}}=\int _{0}^{1/2} \frac{t}{1-t} \, dt=\ln(2)-\frac{1}{2}$

**taylor series** of a infinitely-differentiable fn $f(x)$ at c is the power series $\sum_{n=0}^{\infty} \frac{f^{(n)}(c)}{n!}x^{n}$
when $c=0$, it's called the **maclaurin series**

now, if one can prove that the remainder of they taylor series conv to 0 (in a neighborhood of $c$), then the taylor series will conv to $f(x)$ in that neighboorhood
**corollary**: if $f^{(n)}(x)$ is uniformly bounded in some neighborhood $N$ of $c$, then the taylor series conv to $f(x)$ on $N$

everyone know that $f(x)=e^{ -1/x^{2} }$ if $x\neq 0$, $0$ otherwise is the funny non-analytic fn that everyone talk about bla bla bla

some famous taylor things
- $e^{ x }=\sum_{n=0}^{\infty} \frac{x^{n}}{n!}$, conv/$\mathbb{R}$
- $\ln(1-x)=\sum_{n=1}^{\infty} \frac{x^{n}}{n}$, conv/$[-1,1)$
- $\sin x=\sum_{n=1, n \text{ odd}}^{\infty} \frac{(-1)^{(n-1)/2}}{n!}x^{n}$, conv/$\mathbb{R}$
- $\cos x=\sum_{n=0, n\text{ even}}^{\infty} \frac{(-1)^{n/2}}{n!}x^{n}$, conv/$\mathbb{R}$
- $(1+x)^{\alpha}=\sum_{n=0}^{\infty} \frac{\alpha^{(n)}}{n!}x^{n}$, conv/$(-1,1)$
- $\arctan x=\sum_{n=1, n\text{ odd}} \frac{(-1)^{(n-1)/2}}{n!}x^{n}$, conv/$[-1,1]$
- 