let $X$ be a randvar in $\mathbb{R}$ ([[discrete]] or [[cont]]) with mean $\mu$ and stddev $\sigma$, then $P(|X-\mu|\geq k\sigma)\leq \frac{1}{k^{2}}$

**proof**
we have
$$
\begin{align}

\sigma^{2}&=E\left[(X-\mu)^{2}\right] \\
&\geq E\left[ (X-\mu)^{2}|(X-\mu)^{2}\geq k^{2}\sigma^{2} \right]P((X-\mu)^{2}\geq k^{2}\sigma^{2}) \\
&= k^{2}\sigma^{2} P(|x-\mu|\geq k\sigma)
\end{align}
$$
=> qed
(the second inequality stems from $E(X)=E(X|E_{1})P(E_{1})+E(X|E_{2})P(E_{2})\geq E(X|E_{1})P(E_{1})$)

**corollary**: weak law of large nums
$\lim_{ n \to \infty } P(|\bar{X}_{n}-E(X)| < \varepsilon) = 0$, with $\bar{X}_{n}$ being the sample avg over $n$ samples
**proof** (assuming finite $\sigma$)
- we have $V(\bar{X}_{n})=\frac{1}{n^{2}}V(X_{1}+X_{2}+\dots+X_{n})=\frac{n\sigma^{2}}{n^{2}}=\frac{\sigma^{2}}{n}$
- then using the ineq, we have $0\leq P(|\bar{X}_{n}-\mu|\geq\varepsilon)\leq \frac{1}{k^{2}}=\frac{\sigma^{2}}{n\varepsilon^{2}} \to 0$ as $n \to \infty$ => qed