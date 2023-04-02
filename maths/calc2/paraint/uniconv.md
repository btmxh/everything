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

## proving
- [[cauchy]]
- [[weierstrass m-test]]
- [[dirichlet test]]


