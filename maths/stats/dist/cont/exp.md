another rather simple [[cont]] [[dist]] is the [[exp]] [[dist]] with support $\mathbb{R}^{+}$, pdf $f(x)=\frac{1}{\beta}e^{ -x/\beta }$ and cdf $F(x)=1-e^{ -x/\beta }$

one can let $\lambda=\frac{1}{\beta}$ to get $f(x)=\lambda e^{ -\lambda x }$
the [[mgf]] is $M_{X}(t)=\int _{0}^{\infty} \lambda e^{ x(t-\lambda) } \, dx=\frac{\lambda}{\lambda-t}=\frac{1}{1-\beta t}$

then one can calc [[meanvar]] without integrating (i'm lazy lol)
- $E(X)=M'_{X}(0)=\beta$
- $E(X^{2})=M''_{X}(0)=2\beta^{2}$ => $V(X)=\beta^{2}$
