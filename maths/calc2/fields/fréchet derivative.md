the **fréchet derivative**, the most general form of derivative is defined as:
- let $f: \mathbb{R}^{n}\to \mathbb{R}^{m}$, and $x_{0} \in \mathbb{R}^{n}$, the FD at the point $x_{0}$ is a **linear map** $L_{x_{0}}$ such that
$$
	\lim_{ \Delta x\to 0 } \frac{\|f(x+\Delta x)-f(x)-L_{x_{0}}(\Delta x)\|}{\|\Delta x\|}=0
$$
- this beautiful derivative can also be used in **general metric spaces**, and is not limited to $\mathbb{R}^{n}, \mathbb{C}^{n}$

it's trivial to prove that the derv is unique

e.g. find the derv of $f(\mathbf{r})=\mathbf{r}^{2}$
- numerator is $(\mathbf{r}+\Delta \mathbf{r})^{2}-\mathbf{r}^{2}-L_{\mathbf{r}}(\Delta r)=2\mathbf{r}\cdot\Delta \mathbf{r}-L_{\mathbf{r}}(\Delta \mathbf{r})+o(\Delta \mathbf{r})$
- => pick $L_{r}(\mathbf{t})=2\mathbf{r}\cdot \mathbf{t}$

### chain rule
let $D_{f}(x_{0})$ be the fréchet derv of $f$ at $x_{0}$, then
$$
\boxed{
D_{f \circ g}(x_{0})(\Delta x)=D_{f}(g(x_{0}))(D_{g}(x_{0})(\Delta x))
}
$$
in the [[jacobian]] form:
$$
\boxed{
(f\circ g)'(x_{0})=f'(g(x_{0}))g'(x_{0})
}
$$
or the differential form ($h=f\circ g$)
$$
\boxed{\frac{dh}{dx}=\frac{dh}{dg}\cdot \frac{dg}{dx}}
$$

e.g. prove $\nabla r^{n}=nr^{n-2}\mathbf{r}$
we have $(r^{2})'=2\mathbf{r}^{T}$ (see [[jacobian]])
$$
\begin{align}
\nabla r^{n}&=(r^{n})'^{T} \\
&=(t^{n/2}|_{t=r^{2}})'^{T} \\
&=\left(\left( \frac{n}{2}t^{n/2-1} \right)|_{t=r^{2}}\cdot 2\mathbf{r}^{T}\right)^{T} \\
&=nr^{n-2}\mathbf{r}
\end{align}
$$
