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
- differentiating $F(\mathbf r,c)=0$ we got $F'_r \cdot r' + F'_c \cdot dc = 0$, then (1) will happen if $F'_c = 0$ 

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
