$S = \sum_{n=1}^\infty a_{n}b_{n}$ ([[uniconv|uniformly]]) conv if
- $sa_{n}$ ([[uniconv|uniformly]]) conv.
- $b_{n}$ monotonic, (uniformly) bounded

## proof
### dbrr ver
wlog assuming $b_{n}$ dec (if inc we can take $b'_{n} = -b_{n}$ dec)
also translating $b_n$ so that this seq is non-neg

let $x_{n}=a_{m+n},y_{n}=b_{m+n}$
then we do summation by parts to $x_{n}$ and $y_{n}$
$$
|S_{n+m}-S_{m}|=\left|\sum_{k=m+1}^{n+m}a_{k}b_{k}\right| = \left|\sum_{k=1}^{n}x_{k}y_{k}\right|
$$
$$
= \left|\sum_{k=1}^{n-1}sx_{k}\Delta y_{k}+sx_{n}y_{n}\right|
$$
let $A_{m}$ be an upper bound of $sx_{n}$
(note: $sx_{n}=sa_{m+n}-sa_{m}$ conv. as $n\to\infty$)
$RHS \leq 2A_{m}y_{1}$ (monotonic telescoping)
now, since $A_{m}\to 0$ ([[cauchy]]) and $y_{1}=b_{m+1}$ is bounded => RHS tends to 0 as $m \to \infty$

=> conv by [[cauchy]]

### gigachad bxd ver
summation by parts
$$
S_{n} = \sum_{k=1}^n a_{k}b_{k} = \sum_{k=1}^{n-1}\Delta b_{k} sa_{k} + sa_{n}b_{n}
$$
the left [[series]] is [[abs conv]] because its abs [[series]] is trivially bounded
the right summand is conv due to obvious reasons

## [[paraim]]
e.g. $\int _{0}^\infty \frac{e^{ -tx }}{x^{2}+\sqrt{ t }} dt$, $x\in[x_{0}>0,+\infty)$
$a(t)=e^{ -tx }\leq e^{ -tx_{0} }$ and $\int _{0}^{\infty}e^{ -tx_{0} }dx=\frac{1}{x_{0}}$ conv => using [[weierstrass m-test]] "$sa(t)$" [[uniconv]]
> alternatively, one can use the definition
$\lim_{ b \to \infty } \sup_{x\in[x_{0},+\infty]}\int _{b}^\infty e^{-tx} dx=\lim_{ b \to \infty }\sup_{x\in[x_{0},+\infty]} \frac{1}{xe^{ bx }} = \lim_{ b \to \infty } \frac{1}{x_{0}e^{bx_{0}}} = 0$
$b(t)=\frac{1}{x^{2}+\sqrt{ t }}$ => monotonic dec bounded in $\left[ 0, \frac{1}{x_{0}^{2}} \right]$
=> uniconv
