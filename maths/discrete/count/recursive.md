## linear seqs
consider the recursive linear relationship $\sum_{k=0}^{m} c_{k}a_{n+k}=0$ and its repr poly. $P(x)=\sum_{k=0}^{m} c_{k}x^{k}$
assuming the poly. has $\beta_{i}$-root $\alpha_{i}$s, then one can find a general formula for $a_{n}$'s as:
- $a_{n}=\sum_i Q_{i}(n)\alpha_{i}^{n}$, with $\deg Q_{i}=\beta_{i}$

## gf
encoding $a_{n}$ using its OGF: $f(x)=\sum_{k=0}^{\infty} a_{k}x^{k}$ turns out to be very funny

gfs are good at problems like count num of $x_{i}$'s s.t. $x_{1}+x_{2}+\dots+x_{n}=k$ and $x_{i}\in A_{i}$, since the result is the coeff of $x^{n}$ in the gf $\prod_{t=1}^{n}\sum_{a\in A_{i}}c(t,a)x^{a}$, with the coeff c(t,a)=1 for the moment, but it can be tweaked to make this method even more powerful (idk maybe some configuration have higher weights?)

gfs can also do linear seqs, since the above linear relationship $\sum_{k=0}^{m} c_{k}a_{n+k}=0$ is equiv to $\sum_{k=}^{m}c_{k}x^{k}f(x)+\dots=0$, with the dots being irrelevant finite stuff

e.g. fibonacci
$f(x)=1+1x+2x^{2}+3x^{3}+5x^{4}\dots$
$xf(x)=1x+1x^{2}+2x^{3}+3x^{4}+\dots$
$x^{2}f(x)=1x^{2}+1x^{3}+2x^{4}+\dots$
=> $f(x)=xf(x)+x^{2}f(x)+1$
=> $f(x)=\frac{1}{1-x-x^{2}}$...

