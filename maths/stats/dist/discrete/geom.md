we will also sample [[bernoulli]] [[dist]], and stop if there is a success, the number of trials we need to make is represented in the [[geom]] [[dist]] $X$ with $p(x)=q^{x-1}p$

- the mean: $E(X)=\sum_{n=1}^{\infty} np(n)=\sum_{n=1}^{\infty} npq^{n-1}$
	- to calc this sum, one sees that this is a [[power series]] => [[uniconv]]
	- we have $\sum_{n=1}^{\infty} npq^{n-1}=p \frac{d}{dq} \sum_{n=1}^{\infty}q^{n}=p \frac{d}{dq}\left( \frac{q}{1-q} \right)=\frac{1}{p}$
	- => $E(X)=\frac{1}{p}$
- the variance can be calc similarly: $V(X)=\frac{q}{p^{2}}$
- this is the [[neg binomial]] in the case $r=1$
- the [[mgf]]: $E(e^{ tX })=\sum_{n=1}^{\infty} e^{ tn }pq^{n-1}=\frac{p}{q}\sum_{n=1}^{\infty}(qe^{ t })^{n}=\frac{p}{q}\cdot \frac{qe^{ t }}{1-qe^{ t }}=\frac{pe^{ t }}{1-qe^{ t }}$
- 