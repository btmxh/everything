consider a [[bernoulli]] randvar $B$, we can define a [[binomial]] randvar $X$ wrt $B$ by sampling $B$ $n$ times: $X_{1}, X_{2},\dots,X_{n}$ => $p(x)$ is the [[prob]] of $x$ being the number of successes, i.e. num of $k \in 1..n$ s.t. $X_{k}=1$
=> then one can calc $p(x)=C_{n}^{k}p^{k}q^{n-k}$, and as a conseq of the [[meanvar]] theorems, $E(X)=np, V(X)=npq$

