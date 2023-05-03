do a buncha [[bernoulli]] trials, then let $X(r)$ be the num of trials s.t. the $r$-th success happens on the last trial (i.e. FFFSSSFS for $r=4$ then $X=8$)

then $X(r)$ is a [[neg binomial]] [[dist]] with $p(n)=C_{n-1}^{r-1}p^{r}q^{n-r}$, and $E(X)=\frac{r}{p}, V(X)=\frac{rq}{p^{2}}$
**proof**
- pmf should be self-explanatory
- to prove the mean and variance formula, we need to prove that $X(r)$ is the same [[dist]] as adding $r$ iid [[geom]] [[dist]]s, which is true because of the definition (but still kinda not rigorous)

the [[mgf]] is $M_{X}(t)=\sum_{n=r}^{\infty} e^{ tn }C_{n-1}^{r-1}p^{r}q^{n-r}$, which is hard to calc, but one can use the additive property of [[mgf]] to derive at $M_{X(r)}(t)=\left( \frac{pe^{ t }}{1-qe^{ t }} \right)^{r}$
