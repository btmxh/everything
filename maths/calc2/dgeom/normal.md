## rough def
[[normal]] is whatever that is perpendicular to [[tangent]]

for [[curve#parametric curve|param curves]], [[normal]] vector can also have the meaning of the normalized derv of the unit [[tangent]] vec (see [[frenet-serret formulas]])

[[normal|normals]] also exist for [[surface|surfaces]]

**NOTE:** only exists for [[singular point|non-singular points]]

## find?
### [[curve#parametric curve|param curves]]
$\mathbf{r'}(t)$ is the dir of tangent => the normal line/plane/... is $\mathbf{r'} \cdot \Delta r = 0$

specific:
$y=f(x) \Rightarrow x - x_0 + f'(x)(y - y_0) = 0$
$x=x(t),y=y(t),z=z(t) \Rightarrow x'\Delta x + y'\Delta y + z'\Delta z = 0$

### [[curve#implicit curve|implicit curves]]
$F'_i$ is a normal vec for all $i \in 1..<n$, so the normal is the span of all $F'_i$'es, which can be repr as a n-1-blade $\wedge_{i=1}^{n-1} F'_i$ in geom algebra => can also be repr as the dual to that blade as a regular vector, which is the [[tangent]] vector

in 3d, this vector is the cross product of $F'_1$ and $F'_2$

### [[surface]]
in the [[surface#implicit surfaces|i-surface]] case, the normal vector is simply $\nabla F$, and for [[surface#parametric surfaces|p-surfaces]], the normal vector can be calc-ed by taking the cross product of the two tangent vectors: $\frac{\partial \textbf{r}}{\partial u}$ and $\frac{\partial \textbf{r}}{\partial v}$
