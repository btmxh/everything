$f(x)=2+3\int _{0}^{x} tf(t) \, dt$
$F(x)=\int _{0}^{x} tf(t) \, dt$
=> $F'(x)=xf(x)$
=> $F'(x)=x(2+3F(x))$
$y'=(2+3y)x, y(0)=0$

$\frac{\cos n}{\sqrt{ n } +\cos n}=\frac{x}{1+x}$, with $x=\frac{\cos n}{\sqrt{ n }}$
=> $\frac{x}{1+x}=x-x^{2}+x^{3}+o(x^{3})$
$\sum x=\sum \frac{\cos n}{\sqrt{ n }}$ conv due to dirichlet's test
$\sum x^{2}=\sum \frac{\cos ^{2}n}{n}=\sum \frac{1-\cos 2n}{n}$ diverges because $\sum \frac{1}{n}$ div and $\sum \frac{\cos 2n}{n}$ conv due to dirichlet's test
$\sum O(x^{3})$ conv due to comparison with $\frac{1}{n^{3/2}}$
=> diverges