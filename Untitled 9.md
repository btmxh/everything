radius of conv $f(x)=\sum_{n}a_{n}x^{n}$ is $1$
$\lim_{ n \to \infty } a_{n} = 0$
prove $\lim_{ x \to 1^{-} } f(x)(1-x)=0$

we have $|f(x)(1-x)|=|\sum_{n} (a_{n}-a_{n-1})x^{n}|\leq \sum_{n}|\Delta a_{n}||x|^{n}$
since $\lim_{ n \to \infty } a_{n}=0$, for large $n>n_{0}$, $a_{n}<\varepsilon$ => $\Delta a_{n}<2\varepsilon$ => LHS < $\sum_{n=0}^{n_{0}} |\Delta a_{n}|$
