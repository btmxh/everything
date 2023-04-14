the improper integral $I(y)=\int _{a}^{b_{0}} f(x,y)dx$ (singularity only at $b_{0}$) can be thought as the limit of $I_{b}(y)=\int _{a}^b f(x)dx$ as $b\to b_{0}$

then we can define [[uniconv]] to this shit as
- $I(y)$ conv at $y_{0}$ iff $\exists I(y_{0})$
- $I(y)$ conv on $[c,d]$ iff $I(y)$ conv at all $y_{0} \in [c,d]$
- $I(y)$ [[uniconv]] on $[c,d]$ iff $\forall \varepsilon>0, \exists$ neighborhood $A$ of $b$ s.t. $|\int _{b}^{b_{0}}f(x,y_{0}) \, dx|<\varepsilon$ for all $b \in A, y_{0} \in [c,d]$

## cont
since uniform cont can't be inferred from $[a,\infty]$, we can't just have $f_{n}$ cont => $f$ cont like [[paraint]]
we need one additional cond: [[uniconv]]
proof is at the [[uniconv#properties#cont]]

## int8
cond: $f$ cont/$[a,b)\times$(y-space) + [[uniconv]]
TODO: nxt's corollary

## diff.
cond: $f,f'_{y}$ cont/xy-space + $\int f'_{y}(x,y)dx$ [[uniconv]]  (+ ofc $\int f(x,y)dx$ cont)

e.g. $I(y)=\int _{0}^{\infty} ye^{ -yx } \, dx$ on $[y_{0},+\infty)$, $(0,+\infty)$
- have: $\int _{b}^{\infty} ye^{ -xy } \, dx=e^{ -by }$, then
	- if $y\geq y_{0}$, one can pick $b$ s.t. $e^{ -by }$ is arbitary small (i.e. pick $b$ s.t. $e^{ -by_{0} } < \varepsilon \iff b > -\frac{1}{y_{0}}\ln\varepsilon$)
	- when $y$ can freely accept any value on $(0, +\infty)$, as $y\to 0$, $e^{ -by }\to 1$, which is not zero => not [[uniconv]]

e.g. $I(y)=\int _{0}^{+\infty} e^{ -xy } \frac{1}{y^{2}+\sqrt{ x }} \, dx$
- $a(x,y)=e^{ -xy }, b(x,y)=\frac{1}{y^{2}+\sqrt{ x }}$
- then for $y\geq y_{0}>0$, $\int _{0}^{+\infty}a(x,y) \, dx$ is conv., $b(x,y)$ dec. wrt $x$ and [[uniconv]] to $0$ as $x\to \infty$

e.g. $\lim_{ y \to 0^{+} } \int _{0}^{+\infty}ye^{ -yx } \, dx \neq \int _{0}^{+\infty} \lim_{ y \to 0^{+} } ye^{ -yx } \, dx$
e.g. $\int _{0}^{+\infty} \frac{\arctan(x^{2}+y+1)}{e^{ 2x+y^{2} }} \, dx$
e.g. $\int _{0}^{+\infty} \frac{y^{2}}{x^{2}+y^{2}+1} \, dx$
