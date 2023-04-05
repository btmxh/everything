## rough def
env. of a family of [[curve]] is another [[curve]] that's tangent to each member of the family (without redundant points that's not a tangency)
or set of point being the intersection of "infinitesimally adjacent" [[curve|curves]] in a family

## find?
### [[curve#implicit curve|i-curve]]
(2d case below)
let $C(c)$ be the curve given by the equation $F(\mathbf r,c)=0$, 
we need to find the envelope of this family
call this thing $\mathbf r(t)$
then:
- $\forall t, r(t) \in C(c)$ for some c => $F(\mathbf r, c)=0$
- then, $\mathbf r'$ is the [[tangent]] vector of the env., while $F'_r$ is the [[normal]] vector of the curve $C(c)$. in order to make the env. tangent of $C(c)$, we need $\mathbf r' \cdot F'_r = 0$ (1)
- differentiating $F(\mathbf r,c)=0$ we got $F'_\mathbf{r} \cdot \mathbf{r}' + F'_c \cdot c' = 0$, then (1) will happen if $F'_c = 0$ 

=> method
$E'$ is the set of all $\mathbf r$ s.t. there exists $c$ s.t. $F(\mathbf r, c) = F'_c(\mathbf r, c) = 0$
$S$ is the set of all [[singular point]] of the family
then $E = E' \setminus S$ is the env. of the family

e.g. $y=kx+\frac1k$
singularities: none
$F=kx-y+\frac1k=0$
$F'_k=x-\frac1{k^2}=0$ => $x=\frac1{k^2}$ (1)
sub back => $y=\frac2k$ (2)
(1)(2) equiv to $2y=x^2\ne0$

e.g. $\frac{x^{2}}{c^{2}}+\frac{y^{2}}{(5-c)^{2}}=1$
- $F'=0 \iff \frac{x^{2}}{c^{3}}=\frac{y^{2}}{(5-c)^{3}}=t$
- $F=0 \implies ct+(5-c)t=1 \implies c=\frac{1}{5}$
- then $E':$ $x^{2}=\frac{c^{3}}{5}, y^{2}=\frac{(5-c)^{3}}{5}$
- $S = \{ (0,0) \}$ and $(0,0) \not\in E'$
- => $E=E'$ => $E$ does not touch the curve when $c<0$ or $c>5$ => no [[envelope]]
- if the conds $0 < c < 5$ is given, then the [[envelope]] is $x^{2/3}+y^{2/3}=5^{2/3}$
