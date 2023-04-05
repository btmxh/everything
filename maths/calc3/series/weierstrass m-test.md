prove [[uniconv]] + [[abs conv]]
[[series]] case: $|g(n,x)|\leq a_{n}$ and $\sum a_{n}$ conv
[[paraim]] case: $|g(x,y)|\leq h(x)$ and $\int h(x) dx$ conv
(the proof is trivial af)

e.g. $\sum_{n=1}^{\infty}x^{2}e^{ -nx }$/$[0,+\infty)$
$g(x)=x^{2}e^{ -nx } \implies g'(x)=e^{ -nx }(2x-nx^{2})$
=> max at $x=\frac{2}{n}$ and $g(x)\leq \frac{4e^{ -2 }}{n^{2}}$ => [[uniconv]]

e.g. $\sum_{n=1}^{\infty} \int _{0}^{1/n} \frac{\sqrt[3]{ t }}{\sqrt[4]{ 1+\sin (t)^{2} }} dt \cos nx$
the abs operand is $\leq \int _{0}^{1/n} \sqrt[3]{ t } dt=O\left( \frac{1}{n^{4/3}} \right)$ [[abs conv]] => [[uniconv]]

e.g. $\sum_{n=1}^{\infty} \frac{x^{n}}{n}$/$[-1,0]$
- m1: [[dirichlet test]]
	- $b_{n}=x^n$ => $sb_{n}$ bounded
	- $a_{n}=\frac{1}{n}$ => $a_{n}$ mono. dec. conv. to 0
- m2: 
