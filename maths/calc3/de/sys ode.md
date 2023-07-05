- "Chuẩn tắc" system of $n$ differential equations:
$$
\begin{align}
y_{1}'&=f_{1}(x,y_{1},y_{2},\dots,y_{n})\\
y_{2}'&=f_{2}(x,y_{1},y_{2},\dots,y_{n}) \\
\dots \\
y'_{n}&=f_{n}(x,y_{1},y_{2},\dots,y_{n})
\end{align}
$$
- **Theorem:** If all $f_{i}$'s and their partials are continuous on some $D\subset \mathbb{R}^{n+1}$, then for each $(x_{0},y_{1}^{0},y_{2}^{0},\dots,y_{n}^{0})\in D$, the system above has an unique solution (defined on a neighborhood $U_{\varepsilon}(x_{0})$ of $x_{0}$) s.t. $y_{i}(x_{0})=y_{i}^{0}$ for all $i\in 1..n$
- General sol: $(y_{1},y_{2},\dots,y_{n})$, with $y_{i}=\phi_{i}(x,c_{1},c_{2},\dots,c_{n})$ is a **general sol** of the above [[sys ode]] iff
	- satisfies the sys for all $c_{1..n}\subset \mathbb{R}^{n}$
	- for each $(x_{0},y_{1}^{0},\dots,y_{n}^{0})$ satisfies the above theorem, one can find $c_{i}=c_{i}^{0}$ s.t. $y_{i}(x_{0})=y_{i}^{0}$
- Specific sol: General sol + specific values for $c_{1..n}$

## Solve methods
- Turn into regular [[ode]]

## Linear
- basically $f_{i}$'s are linear functions
- one can write in matrix form as $Y'=A(x)Y+B(x)$
- using matrix exponential, one can trivially solve this
- (but we don't have that here)

### Elimination method
### Operator method
### Eigenmethod
