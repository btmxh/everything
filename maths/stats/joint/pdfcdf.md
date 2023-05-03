consider $n$ randvars: $X_{1},X_{2},\dots,X_{n}: \Omega\to \mathbb{R}$
then one can package $X=(X_{1},X_{2},\dots,X_{n})$ as a randvar from $\Omega\to \mathbb{R}^{n}$
then, this randvar can be defined as a [[cont]] (or maybe [[discrete]]) randvar by the pdf $f$ s.t. $P(X\in A)=\int _{A} f(\mathbf{r}) \, d\mathbf{r}$ for all subset $A$ of $\mathbb{R}^{n}$

## margin
the marginal pdf of $X_{k}$ is defined as $f_{X_{k}}(x)=\int _{A_{k}(x)} f(\mathbf{r}) \, d\mathbf{r}$, with $A_{k}(x)$ being the region in $\mathbb{R}^{n}$ s.t. $\mathbf{r}\cdot \mathbf{e_{k}}=x$, or if $n=2$, $f_{X}(x)=\int _{-\infty}^{\infty} f(x,y) \, dy$

## cond
consider the case $n=2$, we can define the cond pdf $p(x|y)$ as $p(x|y)=\frac{f(x,y)}{f_{Y}(y)}$