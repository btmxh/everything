## general form
the general form of the linear programming model is
$$
\begin{align}
\min\, &f(x)=cx \\
\text{s.t.}\,&Ax\geq b \\
& x\in \mathbb{R}^{n\times 1}
\end{align}
$$
for $A\in \mathbb{R}^{m\times n}, b\in \mathbb{R}^{n\times 1}, c\in \mathbb{R}^{1\times n}$

e.g. $\min f(x)=5x_{1}-6x_{2}+3x_{3}$ s.t. $8x_{1}+6x_{2}+6x_{3}=5$, $3x_{1}-2x_{2}+7x_{3}\geq 7$ and $x_{1},x_{2},x_{3}\geq 0$ has
$$
[A|b]=\begin{bmatrix}
8 & 6 & 6 & 5 \\
-8 & -6 & -6 & -5 \\
3 & -2 & 7 & 7 \\
1 &  &  & 0 \\
 & 1 &  & 0 \\
	 &  & 1 & 0 \\
\end{bmatrix}, c=\begin{bmatrix}
5 & -6 & 3
\end{bmatrix}
$$

## variants
### chính tắc (standard form)
$\min f(x)=cx, Ax\geq b, x\geq 0$

One can always turn a general problem into a chinhtacs problem by expressing a free component $x_{i}$ as $\overline{x_{i}}-\overline{\overline{x_{i}}}$, with the new variables being nonnegative (or the bad way: solving a LP for $x_{i}\geq0$ and another for $x_{i}\leq 0$, but that result in $2^{k}$ split for $k$ free variables)
### chuẩn tắc (augmented form)
$\min f(x)=cx, Ax=b, x\geq 0$
(this is a subvariant of the standard form)

One can always turn a standard form LP into an augmented one by introducing "slack" variables $s=b-Ax$, which turns the problem into $\min f(x,s)=cx, Ax+s=b; x,s\geq 0$


## existence
consider $(LP): \min_{x\in D}f(x)=cx$, with $D: Ax\geq b$

solution exists if
- $D$ is bounded (=> compact) + $f(x)$ continuous (because linear)
- $f(x)$ has a lower bound on $D$
	- repr. theorem => $x=\lambda^{i}x_{i}+\mu _{j}d_{j}$ for vertices $x_{i}$'s and extreme recession directions $d_{j}$'s, $\sum\lambda^{i}=1$, all coeffs are nonnegs
	- hence $f(x)=\lambda _{i}f(x_{i})+\mu _{j}f(d_{j})$, which is lowerly bounded => $f(d_{j})=0$ for all $j$ => $f(x)$ min at $x_{0}$ s.t. $f(x_{0})\leq f(x_{i})$ for all $i$

	- the logic break down here if $f$ is not linear, e.g. $f(x)=e^{ x }$for $x\in \mathbb{R},x\leq 367$

## props of opts.
let $S$ be the set of global optimizers, then
- $S$ is convex
- $S$ is a face of $D$
	- assuming $[yz]\cap S$ at some pt $x_{0}$, then $f(y)$ and $f(z)$ is a NN-lerp of $f(x_{0})$ => both $f(y)$ and $f(z)$ are global opts => qed
- $S$ contains at least a vertex (aka extreme sol) of $D$ (if $D$ has at least a vertex)
	- since $S$ is a face of $D$, $S$ is a convex polytope, has a vertex $v$ that's also a vertex of $D$, qed

**Algorithm 1**: The solution can be solved if $D$ has GO at some vertex, by naively looping over them and taking the most optimal one.
Complexity $O(|V|) \approx O(C^{m}_{n})$ ($m$ faces, n dimensions), so basically factorial (or exponential)
It assumes that $D$ has GO at some vertex, so it may fail in unbounded case ($f$ not bounded and not coercive)

