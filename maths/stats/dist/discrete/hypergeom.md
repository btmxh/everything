**hypergeom experiment:** one pick $n$ objects in $N$ objects, in which there are $k$ successes and $N-k$ failures => $X$ successes
then, $X \leq n,k$ and the pmf $p(x)=\frac{C_{k}^{x}C_{N-k}^{n-x}}{C_{N}^{n}}$

the mean is$$
\begin{align}
E(X)&=\sum_{x=0}^{min\{ n,k \}}  \frac{xC_{k}^{x}C_{N-k}^{n-x}}{C_{N}^{n}} \\
&=\frac{nk}{N} \sum_{x=1}^{min\{ n,k \}} \frac{C_{k-1}^{x-1}C_{N-k}^{n-1-x}}{C_{N-1}^{n-1}}
\end{align}
$$
the sum is $1$ because it's a sum of pmf of another [[hypergeom]] [[dist]] => $E(X)=\frac{nk}{N}$

the variance is
$$
\begin{align}
V(X)&=E(X^{2})-E(X)^{2}=\sum_{x=0}^{min\{ n,k \}} \frac{x^{2}C_{k}^{x}C_{N-k}^{n-x}}{C_{N}^{n}}-\mu^{2} \\
\end{align}
$$
the sum can be calculate by adding 2 sums that look like $\frac{xCC}{C}$ and $\frac{x(x-1)CC}{C}$, which is a mess so $V(X)=\mu\cdot \left( 1-\frac{k}{N} \right) \frac{N-n}{N-1}$
