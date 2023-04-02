do [[gramm-schmidt]] to the first n dervs of $\mathbf r$ (assuming that they're LD, n is the dimension of $\mathbf r$)
$\mathbf e_1 = normalize(\mathbf r')$
$\mathbf e_2 = normalize(GS(\mathbf r'', \mathbf e_1))$
...

then this matrix equation holds
![[Pasted image 20230401203721.png]]
(the variable s does not imply that $\mathbf r$ is a [[arclen]] param of the curve)

## proof
since $\mathbf e_i$'s are perp. and normalized, the matrix $\mathbf Q$ with its i-th rows being $\mathbf e_i$ is an ortho. matrix, i.e. $\mathbf Q^T = \mathbf Q^{-1} \implies \mathbf Q \mathbf Q^T = I$
using the product rule:
![[Pasted image 20230401204147.png]]
=> LHS is skew-symmetric

idk how to proceed xd
## 2d case
we have $\mathbf n' = -\kappa \mathbf t$ as a consequence of this

**non-complicated-generalized proof**
we have
$\mathbf t^2=\mathbf n^2=1, \mathbf t \cdot \mathbf n = 0$
then $\mathbf t'\cdot \mathbf n+\mathbf t\cdot \mathbf n'=0$ and $\mathbf n\cdot \mathbf n' = 0$ (1)
since $\mathbf t' = \kappa \mathbf n$, $\mathbf t \cdot \mathbf n' = -\kappa$ (2)
from (1) and (2) we have qed

## 3d case
no one cares tbh