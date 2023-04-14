## common def
let $f_i: I \to (S \to \mathbb C)$ be a seq. of fn that conv. pointwise to $f$ as $i \to i_0$
(index set $I$ does not need to be a subset of $\mathbb Z$)
then this conv. is uni iff $\forall \varepsilon > 0$ there exists a neighbor $N$ of $i_0$ s.t.
$\forall i\in N, x\in S, |f_i(x)-f_{i_0}(x)| < \varepsilon$

or equivalently, $\lim_{i\to i_0} \sup_{x\in S}|f_i(x)-f_{i_0}(x)| = 0$

## [[series]]
consider this series $f(x)=\sum_{n=1}^{\infty} g(n, x)$
is the pointwise limit of $f_i(x)=\sum_{n=1}^i g(n, x)$ as $i\to \infty$

=> the series uni. conv. iff $\lim_{i \to \infty} \sup_{x\in S}|\sum_{n=i+1}^\infty g(n,x)|=0$

## [[paraim]]
consider this im. int. $I(y)=\int_a^\infty g(x,y)dx$
is the pl of $I_t(y)=\int_a^t g(x,y)dx$ as $t \to \infty$

=> the im.int. uni.conv. iff $\lim_{t\to\infty}\sup_{y\in S} |\int_t^\infty g(x,y)dx| = 0$

**NOTE:** [[paraint]] DOES NOT automatically [[uniconv]]

## proving
- [[cauchy]]
- [[weierstrass m-test]]
- [[dirichlet test]]
- [[leibnitz test]]
- [[abel test]]

e.g. $\sum_{n=1}^\infty x^n$/$[0,1-\varepsilon]$ and $[0,1]$
$S_{n}=\frac{x-x^{n+1}}{1-x}$
$S=\frac{x}{1-x}$
then $|S_{n}-S|=\frac{x^{n+1}}{1-x}\to\infty$ as $x\to 1$, and bounded by $\frac{1}{1-\varepsilon}$ in the first case => conclusion: uni. conv and not uni. conv

## properties
### cont
**theorem**: $f_{i}$ cont, [[uniconv]] to $f$ then $f$ cont
**proof**
$0\leq|f(x)-f(x_{0})|\leq|f(x)-f_{i}(x)|+|f_{i}(x)-f_{i}(x_{0})|+|f_{i}(x_{0})-f(x_{0})|$
$\leq 2\sup_{x\in S}|f(x)-f(x_{0})|+|f_{i}(x)-f_{i}(x_{0})|$
using the definition of [[uniconv]] and cont => RHS tends to 0 as $x\to x_{0}$ => qed

### int8
**theorem**: $f_{i}$ cont, [[uniconv]] to $f$ then $f$ R-int8
$$
\int_{a}^b f(x)dx =\lim_{ i \to i_{0} } \int _{a}^{b}f_{i}(x)dx 
$$
using last theorem => $f$ cont => R-int8 => LHS exists
then it's suffices to prove that
$$
\lim_{ i \to i_{0} } \left|\int _{a}^{b} f(x)-f_{i}(x)dx\right|=0
$$
LHS $\leq \lim_{ i \to i_{0} } \int _{a}^{b} |f(x)-f_{i}(x)|dx$
$\leq \lim_{ i \to i_{0} } (b-a)\sup_{x\in S}|f(x)-f_{i}(x)|$
$=(b-a)\lim_{ i \to i_{0} }\sup_{x\in S}|f(x)-f_{i}(x)| = 0$, qed

>if $f_{i}$ is not cont but rather R-int8, one can still prove that $f$ is R-int8 and achieve the same result above
- we only need to prove $f$ is R-int8, then we can use the proof above
- we start with $f_{n}$ is R-int8 => there exists two step functions $u_{n},v_{n}$ (that's R-int8) s.t. $u_{n}\leq f_{n}\leq v_{n}$ and $\int_{a}^{b}|v_{n}(x)-u_{n}(x)|dx < \varepsilon_{1}$, we will construct two fns $a,b$ that's also R-int8 and $a\leq f\leq b$ and $\int _{a}^{b}|u(x)-v(x)|dx$ arbitarily small, which will prove that $f$ is R-int8
- using [[uniconv]], then *insert epsilon-delta thingy here* $|f_{n}(x)-f(x)|\leq \varepsilon_{2}$
- then to achieve $u\leq f\leq v$, one takes: $u=u_{n}-\varepsilon_{2}, v=v_{n}+\varepsilon_{2}$
- now we have $\int _{a}^{b}|u(x)-v(x)|dx=\int _{a}^b (v_{n}(x)-u_{n}(x)+2\varepsilon_{2})dx$$<\varepsilon_{1}+4(b-a)\varepsilon_{2}$: arbitarily small => qed

e.g. prove that if $f_{i}$ cont, [[uniconv]] to $f$ ($S=[a,b]$), then
$$
\lim_{ i \to i_{0} } \int _{a}^b \left( \int _{a}^xf_{i}(t)dt\right)dx = \int _{a}^b\left( \int _{a}^x f(t)dt  \right) dx 
$$
let $F_{i}(x)=\int _{a}^xf_{i}(t)dt$ , and $F(x)=\int _{a}^xf(t)dt$
then $F_{i},F$ are cont, now we need to prove that $F_{i}$ uni conv to $F$
$$
0\leq\lim_{ i \to i_{0} } \sup_{x\in [a,b]} |F_{i}(x)-F(x)|\leq\lim_{ i \to i_{0} } \sup_{x\in[a,b]}\int _{a}^x  \left|f_{i}(x)-f(x)\right|dx 
$$
$$
\leq \lim_{ i \to i_{0} } \sup_{x\in[a,b]}(x-a)\sup_{x'\in[x,a]}|f_{i}(x')-f(x')|$$
$$\leq (b-a)\lim_{ i \to i_{0} } \sup_{x\in[a,b]}|f_{i}(x)-f(x)| = 0
$$
=> qed using the squeeze theorem

### diff
$S=(a,b)$, $f'_{i}$ cont, $f'_{i}$ [[uniconv]] and $f_{i}$ conv to $f$ then $f'(x)=\lim_{ i \to i_{0} }f'_{n}(x)$
**proof**
let $f'_{i}$ [[uniconv]] to $g$ => $g$ cont and
$\int_{a}^x g(t)dt=\lim_{ n \to \infty }\int _{a}^xf'_{n}(t)dt=\lim_{ n \to \infty }(f_{n}(x)-f_{n}(a))=f(x)-f(a)$
taking the derv. of two sides => $g(x)=f'(x)$ => qed

- e.g. $\sum_{n=1}^{\infty}(-1)^{n-1} \frac{1}{\sqrt{ n+1 }}\arctan \frac{x}{\sqrt{ n+1 }}$
	- $f_{n}(x)=(-1)^{n-1} \frac{1}{\sqrt{ n+1 }}\arctan \frac{x}{\sqrt{ n+1 }}$
	- then $f'_{n}(x)=(-1)^{n-1}\left( \frac{1}{n+1} \frac{1}{1+\frac{x^{2}}{n+1}} \right)=\frac{(-1)^{n-1}}{n+1+x^{2}}$ cont/$\mathbb R$
	- $\sum_{n=1}^\infty f_{n}(x)$ conv due to [[leibnitz test]] (notice the sign of $f'_{n}(x)$)
	- $\sum_{n=1}^\infty f'_{n}(x)$ [[uniconv]] yet again due to [[leibnitz test]]
	- => $f'(x)=\sum_{n=1}^\infty \frac{(-1)^{n-1}}{n+1+x^{2}}$

