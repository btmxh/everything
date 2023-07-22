field is basically just a map (usually differentiable) from a (subset of a) vector set ($\mathbb{R}^{3}, \mathbb{R}^{4}$) to another scalar/vector set ($\mathbb{R}, \mathbb{R}^{3}, \mathbb{R}^{4}$)

## scalar field
fields that maps to a scalar set like $\mathbb{R}$
level curve: $S=\{ \mathbf{r}|f(\mathbf{r})=a \}$
gradient $\nabla f$
directional $\frac{\partial f}{\partial \hat{u}}=\nabla f \cdot \hat{u}$

## vector field
fields that maps to a vector set like $\mathbb{R}^{3}$
"đường dòng" $C$: for all $\mathbf{r}\in C$, $\mathbf{r}+\alpha \mathbf{f}(\mathbf{r})$ is a tangent line to $C$ => xác định hệ ptvp cho field
qua mỗi điểm có duy nhất 1 đường dòng
divergence: độ phân hoạch/phân tán
- điểm nguồn: div > 0
- điểm rò: div < 0
- trường ống => div = 0 for all pts
hoàn lưu/lưu số: type 2 [[lineint]]
curl: vecto xoáy
- $\vec{rot}\mathbf{F}=\left( \frac{\partial F_{z}}{\partial y}-\frac{\partial F_{y}}{\partial z},\frac{\partial F_{x}}{\partial z}-\frac{\partial F_{z}}{\partial x},\frac{\partial F_{y}}{\partial x}-\frac{\partial F_{x}}{\partial y} \right)$
- điểm xoáy => rot != 0

### conservative vector field
these following statements are equivalent:
- $\mathbf{F}$ is conservative
- $\nabla \times \mathbf{F}=0$
- $\oint \mathbf{F}\cdot d\mathbf{s}=0$ along all closed path
- there exists some [[field#scalar field|scalar field]] $\phi$ (called the [[scalar potential]] of $\mathbf{F}$) such that $\mathbf{F}=\nabla \phi$

### solenoidal vector field
basically there are no sources (div > 0) or sinks (div < 0) in the field, i.e. div = 0 everywhere, or $\nabla\cdot \mathbf{F}=0$)

**scalar fields** are fields that maps to a scalar set like $\mathbb{R}$, and **vector fields** are fields that maps to a vector set like $\mathbb{R}^{3}$ ^55c459

