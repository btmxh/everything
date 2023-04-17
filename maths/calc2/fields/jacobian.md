the matrix representing the [[fréchet derivative]] (it's a linear map => it must have a matrix repr wrt the standard basis)
for $f: \mathbb{R}^{n}\to \mathbb{R}^{m}$, it's a $n\times m$ matrix, called the **jacobian matrix**, denoted as $f'(x_{0})$
- if $f=(f_{1},f_{2},\dots,f_{m}), x=(x_{1},x_{2},\dots,x_{n})$, the jacobian matrix is represented as a matrix of partials
$$
\left[ 
\begin{matrix}
\frac{\partial f_{1}}{\partial x_{1}} & \frac{\partial f_{1}}{\partial x_{2}} & \dots & \frac{\partial f_{1}}{\partial x_{n}} & \\
\frac{\partial f_{2}}{\partial x_{1}} & \frac{\partial f_{2}}{\partial x_{2}} & \dots & \frac{\partial f_{2}}{\partial x_{n}} & \\
\dots & \dots & \dots & \dots\\
\frac{\partial f_{m}}{\partial x_{1}} & \frac{\partial f_{m}}{\partial x_{2}} & \dots & \frac{\partial f_{m}}{\partial x_{n}} & \\
\end{matrix}
\right]
$$
- **and these partials can be defined using this matrix**, using linear algebra stuff, one easily can derive the original definition of partials (i'm not doing that because i'm lazy asf)

e.g. when $f(\mathbf{r})=\mathbf{r}^{2}$, the derv is $2\mathbf{r}\cdot \mathbf{t}=2\mathbf{r}^{T}\mathbf{t}$ => the jacobian is $2\mathbf{r}^{T}$
