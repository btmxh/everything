consider a randvar $X: \Omega\to \Omega'$, with $\Omega'$ being a vector space (or something that can be multiplied with a scalar and have a norm)
the **mean** is defined as $E(X)=\mu=\int _{\Omega'} xf(x) \, dx$
the **mean** wrt fn $g$ is $E(g(X))=\int_{-\infty}^{\infty} g(x)f(x) \, dx$
the **variance** $V(X)=E\left[ \|x-\mu\|^{2} \right]$ and its sqrt the **stddev** $\sigma(X)=\sqrt{ V(X) }$
(we only care about these values when they are a scalar, so no one talks about variance of 2d randvar)

**theorem**: $E(aX+b)=aE(X)+b$
corollaries: $V(aX+b)=a^{2}V(X)$, $\sigma(aX+b)=|a|\sigma(X)$
**proof**
trivial: we have $E(aX+b)=\int _{-\infty}^{\infty} (ax+b)p(x) \, dx=aE(X)+b$

**theorem:** $V(X)=E(X^{2})-E(X)^{2}$
**proof**
we have $V(X)=E((X-\mu)^{2})=\int _{-\infty}^{\infty} (x^{2}-2x\mu+\mu^{2})p(x) \, dx$$=E(X^{2})-2\mu E(X)+E(X)^{2}=E(X^{2})-E(X)^{2}$, qed

## cond
ofc this shit have conditional version, basically we have $E(X|Y=y)=\int _{-\infty}^{\infty} xf(x|y) \, dx$
and etc. etc.

## 2 var case
we have the **mean**: $E(g(X,Y))=\int _{-\infty}^{\infty} \int _{-\infty}^{\infty} g(x,y)f(x,y) \, dx \, dy$
and the **covariance**:
$Cov(X,Y)=E\left[(X-\mu_{X})(Y-\mu_{Y})\right]$
> the cov. repr how $X$ tends to change as $Y$ changes and rev. (positive if $X$ inc as $Y$ inc

also this gives us $V(X)=Cov(X,X)$
the **correlation coeff** is a dimensionless scalar: $corr(X,Y)=\frac{Cov(X,Y)}{\sqrt{ V(X)V(Y) }}$

**theorem**: $E(X+Y)=E(X)+E(Y)$, $E(kX)=kE(X)$
**proof**
$E(X+Y)=\int_{\mathbb{R}^{2}} (x+y)f(x,y)  \, dxdy$$=\int _{-\infty}^{\infty} xdx \int _{-\infty}^{\infty} f(x,y) \, dy+\dots=\int _{-\infty}^{\infty} xdxf_{X}(x) \, dx+\dots$$=E(X)+E(Y)$
the latter identity is trivial

**theorem:** $E(XY)=E(X)E(Y)+Cov(X,Y)$
we have $Cov(X,Y)=E\left[(X-\mu_{X})(Y-\mu_{Y})\right]$$=E(XY-Y\mu _{X}-X\mu_{Y}+\mu_{X}\mu_{Y})=E(XY)-E(X)E(Y)$, qed

**theorem:** $V(X+Y)=V(X)+V(Y)+2Cov(X,Y)$
we have LHS=$E((X+Y)^{2})-E(X+Y)^{2}$$=E(X^{2})+E(Y^{2})+2E(XY)-E(X)^{2}-E(Y)^{2}-2E(X)E(Y)$$=V(X)+V(Y)+2Cov(X,Y)$
**more generally:** $V\left( \sum_{k=1}^{n} X_{k} \right)=\sum_{i,j=1}^{n} Cov(X_{i},X_{j})$

## law of total
$$
\begin{align}
E(X)&=E(E(X|Y)) \\
V(X)&=E(V(X|Y))+V(E(X|Y))
\end{align}
$$
**proof**
- $E(E(X|Y))=\int _{-\infty}^{\infty} E(X|Y=y)f_{Y}(y) \, dy$$=\int _{-\infty}^{\infty}\int _{-\infty}^{\infty} xf(x|y)f_{Y}(y) \, dxdy=$$=\int _{-\infty}^{\infty}\int _{-\infty}^{\infty} xf(x,y)\,dxdy=E(X)$
- $V(X)=E(X^{2})-E(X)^{2}$
	- we have $E(X^{2})=E(E(X^{2}|Y))$$=E(V(X^{2}|Y)+E(X|Y)^{2})$$=E(V(X^{2}|Y))+E(E(X|Y)^{2})$
	- and $E(X)^{2}=E(E(X|Y))^{2}$, combined with $E(E(X|Y)^{2})$ we have $V(E(X|Y))$ => qed

**corollary**:
- $E(XY)=E(E(XY|Y))=E(YE(X|Y))$
- $V(XY)=E(V(XY|Y))+V(E(XY|Y))$$=E(YV(X|Y))+V(YE(X|Y))$
- if $X,Y$ [[independent]], then
	- $E(X|Y)=E(X)$ => $E(XY)=E(X)E(Y)$
	- $V(XY)=E(Y)V(X)+V(Y)E(X)$
