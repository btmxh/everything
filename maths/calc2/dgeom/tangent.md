## rough def
tangent $T$ of a [[curve]] $C$ at a point $r_0$ is a line s.t.
- $r_0 \in T$
- in a neighborhood $N$ of $r_0 \subset C$, $T \cap N = \{r_0\}$
(the true def is outside of the scope)

the vector points at the [[tangent]] direction is called the tangent vec

[[tangent|tangents]] also exist for [[surface|surfaces]]

**NOTE:** only exists for [[singular point|non-singular points]]

## find?
### [[curve#parametric curve|param curve]]
$\mathbf{r}'(t_0)$ is parallel to the [[tangent]] of the curve at $t_0$
=> fn: $\Delta r(t) = \mathbf{T}(t) - \mathbf{r}(t) = \mathbf{r'}(t_0)t$

specific:
$y=f(x) \Rightarrow T(x) = y_0 + f'(x_0)(x - x_0)$ 
$x=x(t), y=y(t), z=z(t) \Rightarrow T_x(t) = x_0 + x'(t_0)(t - t_0), ...$

### [[curve#implicit curve|implicit curve]]
the [[tangent]] is found using the [[normal]]

specific:
$F(x,y)=0 \Rightarrow F'_x\Delta x + F'_y\Delta y = 0$
$F(x,y,z)=G(x,y,z)=0 \Rightarrow A\Delta x + B\Delta y + C\Delta z = 0$, where $(A, B, C) = \nabla{F} \times \nabla{G}$

### [[surface]]
a tangent to a $n$-manifold has $n$ dimensions => this tangent is a plane, which is the span of two vectors $\frac{\partial \mathbf{r}}{\partial u}$ and $\frac{\partial \mathbf{r}}{\partial v}$, with the origin placed at $\mathbf{r}$ ([[surface#parametric surfaces|p-surface]] case)

in the other case ([[surface#implicit surfaces|i-surface]]), the plane is defined using the [[normal]] vector $\nabla F$

e.g. [[tangent]] and [[normal]] at $(-2,1,6)$ wrt [[curve]] $2x^{2}+3y^{2}+z^{2}-47=x^2+2y^{2}-z=0$
- let lhs be $F(x,y,z)$, mhs be $G(x,y,z)$
- normal wrt $F=0$ is $\nabla F(-2,1,6) \parallel(-4,3,6)$
- normal wrt $G=0$ is $\nabla G(-2,1,6) \parallel (-4, 4, 1)$
- => tangent vector $(-4,3,6)\times(-4,4,1)=\dots$
- 
