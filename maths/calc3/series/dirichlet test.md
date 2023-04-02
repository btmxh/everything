$S = \sum_{n=1}^\infty a_{n}b_{n}$ conv if
- $a_{n}$ monotonic, conv. at 0
- $sb_{n}$ bounded for all (large) n's

## proof
summation by parts
$$
S_{n} = \sum_{k=1}^n a_{k}b_{k} = \sum_{k=1}^{n-1}\Delta a_{k} sb_{k} + a_{n}sb_{n}
$$
since $sb_{n} \leq M$, abs of RHS is le to $M\left( \sum_{k=1}^{n-1}|\Delta a_{k}|\right) + Ma_{n}$
as $n\to \infty$, $Ma_{n} \to 0$ and since $a_{n}$ monotonic, we can extend the abs sign to the whole sum, giving us a nice telescoping sum which reduces to $M|a_{1}-a_{n}| \to Ma_{1}$
therefore we have qed

## uni conv.
if $a_{n}$ uni conv. to 0, we can conclude that $S$ uni conv. too
**proof**
we prove that both $\sum_{k=1}^{n-1}\Delta a_{k} sb_{k}$ and $a_{n}sb_{n}$ uni conv. as $n\to \infty$, using cauchy criterion
- let the first thing be $A_{n}=\sum_{k=1}^{n-1}\Delta a_{k}sb_{k}$, then
	- $|A_{n}-A_{m}|=|\sum_{k=m}^{n-1}\Delta a_{k}sb_{k}|\le M|\sum_{k=m}^{n-1}\Delta a_{k}|\le M|a_{m}-a_{n}|$
	- RHS $\to 0$ as $m,n\to\infty$
- the second thing also uni. conv. for more obvious reasons
	- $|a_{n}sb_{n}-a_{m}sb_{m}|\le M(a_{n}+a_{m}) \to 0$ as $n, m\to\infty$
- sum of two uni conv. thing is uni conv. using the limit thing

e.g. $\sum_{n=1}^\infty \frac{\ln(n)^{100}}{n} \sin \frac{\pi n}{4}$
$a_{n}=f(n)= \frac{\ln(n)^{100}}{n}$ then $\lim_{ n \to \infty }a_{n}=0$ and $f'(x)=\frac{\ln(x)^{99}(100-\ln x)}{x^{2}}$, which is negative for all large $x$'s, therefore making $a_{n}$ dec.
$b_{n}=\sin \frac{\pi n}{4}$ clearly satisfies $sb_{n}$ is bounded
=> conv using [[dirichlet test]]
(another way is to split the series into 4 series by $n\ \text{mod}\ 4$)

