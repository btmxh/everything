$\lim_{ n \to \infty } |\frac{a_{n+1}}{a_{n}}| = L\in R$ then
- if $L<1$, $sa_{n}$ abs conv
- if $L>1$, $sa_n$ div
- otherwise, the test is inconclusive

**NOTE**: if $L=\infty$, then u gotta manually do the $L>1$ case

**proof**
we prove that $\lim_{ n \to \infty } \sqrt[n]{ |a_{n}| } = L$ and then proceed with the [[root test]]
$\forall \varepsilon>0, \exists n_{0}$ s.t. $L-\varepsilon<|\frac{a_{n+1}}{a_{n}}|<L+\varepsilon, \forall n\geq n_{0}$
then $|a_{n_{0}}|(L-\varepsilon)^{n-n_{0}} < |a_{n}| < |a_{n_{0}}|(L+\varepsilon)^{n-n_{0}}$
taking the nth-root => $L-\varepsilon\leq\lim_{ n \to \infty } \sqrt[n]{ |a_{n}| }\leq L+\varepsilon$ => qed
