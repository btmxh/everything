## Orthogonal complement of graph of a linear transformation
Let $T:\mathbb{R}^{n}\to \mathbb{R}^{m}: x\to Ax$ be a linear transformation and $L$ be the graph of $T$.
Then, $L^{\perp}$, the orthogonal complement of $L$, is given by $L^{\perp}=\{ (x',y')|x'+Ay'=0 \}$

**Proof**
If $z'=(x',y')\in L^{\perp}$, then $\langle z,z'\rangle=0$ for all $z\in L$
We have $\langle z,z'\rangle=z^{T}z'=x^{T}x'+y^{T}y'=x^{T}x'+(Ax)^{T}y'$,
then $x^{T}x'+x^{T}A^{T}y'=0$ for all $x,y$, and hence $x'+A^{T}y'=0, \blacksquare$
