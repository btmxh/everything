## def
let $I$ be an interval in $\mathbb{R}$
the map $r: I \to \mathbb{R}^n$ is called a **vec fn** on $I$

## limits, continuity
defined using the metric space definition:
- $\lim_{t \to t_0} \mathbf{r}(t) = a$ iff $\lim_{t \to t_0} ||\mathbf{r}(t) - a|| = 0$
- $\mathbf{r}(t)$ cont at $t_0 \in I$ iff $\lim_{t \to t_0} \mathbf{r}(t) = \mathbf{r}(t_0)$ => $\mathbf{r}(t)$ cont at $I' \subset I$ iff $\mathbf{r}(t)$ cont at all $t_0 \in I'$ (special rules applies to points on the boundary $\partial I'$)

## derivative
since $\dim(I) = 1$, we can use the regular defs:
$\mathbf{r'}(t_0) = \dfrac{dr}{dt}(t_0) = \lim_{t \to t_0} \frac{\mathbf{r}(t)  - \mathbf{r}(t_0)}{t - t_0}$

## components
**theorem**:
$\mathbf{r}(t)$ cont iff $x = r \cdot \hat{\mathbf{i}}$,  $y = r \cdot \hat{\mathbf{j}}$, ... are all cont
$\mathbf{r'}(t) = x'(t)\hat{\mathbf{i}} + y'(t)\hat{\mathbf{j}} + ...$ , this derv. only exists if all components are differentiable.

