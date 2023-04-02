$\sum_{n\in I} a_{n}$, where $I$ is indexable ($\exists\,\text{bij}\,\sigma: \mathbb Z_{+} \to I$) and can be infinite
most cases: $I$ is a subset of $\mathbb N$

partial sums: $S_{n}=\sum_{k=1}^{n}a_{\sigma(k)}$
value of series is $\lim_{ n \to \infty } S_{n}$

if value exists => **convergent** (conv)
otherwise => **divergent** (div)

to calc value of series, the basic way is to calc the above limit, but **if you knew that it conv**, u can do some weird-ass series manipulation

or alternatively, u can say fuck it and do this
e.g.
$\sum_{n=2}^\infty \frac{\cos n\pi}{n^2-1}=\sum_{n=2, n \text{ even}}^\infty \frac{1}{n^2-1}-\sum_{n=3, n \text{ odd}}^\infty \frac{1}{n^2-1}$
the first series can be calc-ed:
$S_{1}=\frac{1}{2}\sum_{n=2,n\text{ even}}^\infty\left( \frac{1}{n-1}-\frac{1}{n+1} \right)=\frac{1}{2}$ (telescoping sum)
similarly, $S_{2}=\frac{1}{3}\implies S=\frac{1}{6}$

if $a_{n}>0$ => **positive series** (non-neg series also exists)
if $a_{n}a_{n+1}\leq 0$ => **non-strict-alternating series** (remove equality to make it strict) ^6267d0