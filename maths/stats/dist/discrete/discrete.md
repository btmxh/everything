**[[prob]] mass fn** $p: \Omega\to[0,1]$ is a fn that characterize the [[dist]] of a randvar $X$, defined as $p(x)=P(X=x)$
=> $\sum_{x\in\Omega}p(x)=1$
if $\Omega$ is ordered, we can define the **cdf**
**cumulative dist. fn** $F: \Omega \to [0,1]$, $F(x)=P(X\leq x)$
=> $F$ is non-dec, $\lim_{ x \to \infty }F(x)=1$, $\lim_{ x \to -\infty } F(x)=0$, ...
**expected value**: $E(g(X))=\sum_{x\in\Omega} g(x)p(x)$, $\mu=E(X)$
**variance**: $V(X)=E((X-\mu)^{2})$, **stddev** $\sigma(X)=\sqrt{ V(X) }$ (these two formulas still hold in cont [[dist]]s)

one can let $f(t)=\sum_{x\in \Omega}\delta(t-x) p(x)$ to be the pdf of a [[cont]] that behaves exactly like this discrete dist.