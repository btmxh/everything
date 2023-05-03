moment generating fn of a randvar $\mathbf{X}$ in $\mathbb{R}^{n}$ is a $\mathbb{R}^{n}\to \mathbb{R}$ fn $\mathbf{M}_{\mathbf{X}}(\mathbf{t})=E\left[e^{ \mathbf{t} ^{T}\mathbf{X}}\right]$
in $n=1$ case, it's simply $M(t)=E(e^{ tX })$

one can use the [[mgf]] to trivially calculate **moments** (and therefore [[meanvar]]), which are $E[X^{n}]=E\left[\frac{d^{n}}{dt^{n}}e^{ tX }|_{t=0}\right]=\frac{d^{n}M}{dt^{n}}(0)$

props:
- $\mathbf{M}_{a\mathbf{X}+\mathbf{b}}(\mathbf{t})=e^{ \mathbf{t}^{T} \mathbf{b}}\mathbf{M}_{\mathbf{X}}(a\mathbf{t})$
- 2 randvars with same mgf correspond to the same [[dist]]
- $\mathbf{M}_{\mathbf{X_{1}+X_{2}}}=\mathbf{M}_{\mathbf{X_{1}}} \times \mathbf{M}_{\mathbf{X_{2}}}$

e.g. using the [[mgf]] of [[geom]] [[dist]], calc the mean and variance?
- the mgf: $M_{X}(t)=\frac{pe^{ t }}{1-qe^{ t }}$
- using my beloved https://www.derivative-calculator.net/, we have
	- $M'_{X}(t)=\frac{pe^{ t }}{(1-qe^{ t })^{2}}$ and $E(X)=M'_{X}(0)=\frac{p}{(1-q)^{2}}=\frac{1}{p}$
	- $M''_{X}(t)=\frac{pe^{ t }(1+qe^{ t })}{(1-qe^{ t })^{3}}$ and $E(X^{2})=M''_{X}(0)=\frac{p(1+q)}{(1-q)^{3}}=\frac{1+q}{p^{2}}$
	- then $V(X)=E(X^{2})-E(X)^{2}=\frac{q}{p^{2}}$
- 
