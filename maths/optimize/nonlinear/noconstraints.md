**Problem statement**: min $f(x), x \in \mathbb{R}^{n}$ for some $f: \mathbb{R}^{n}\to \mathbb{R}$

## conditions for optimality
**First-order condition**: If $f$ differentiable on $\mathbb{R}^{n}$, then if $x_{0}$ is a LOS, $f'(x_{0})=0$
**Proof**
Assuming the Jacobian $f'(x_{0})$ is non-zero, then there is some $i$ $s$.$t$. $f'(x_{0})_{i}$ is non-zero. Let $d=\mathbf{e}_{i}$, the $i$-th standard basis vector.
Now, since $x_{0}$ is optimal, $g(x)=f(x_{0}+td)$ has a extrema at $t=0$, which means that $g'(0)=0$. By the chain rule, $g'(0)=\frac{dg}{dt}(0)=\frac{dg}{d(x_{0}+td)} \frac{d(x_{0}+td)}{dt}=f'(x_{0}+td)\mathbf{e}_{i}=f'(x_{0})_{i}\neq 0$, which is a contradiction, $\blacksquare$

Moreover, if $f$ is convex, then $f'(x_{0})=0$ iff $x_{0}$ is a GOS.
**Proof**
- If $x_{0}$ is a GOS, then $f'(x_{0})=0$
- If $f'(x_{0})=0$, then we have $f(y)-f(x)\geq \langle y-x, f'(x)\rangle$ for all $x,y$. Substitute $x=x_{0}$, we have $f(y)-f(x)\geq 0$ for all $y$, which implies $x_{0}$ is a GOS.

Now, go back to the function $f(x)=\frac{1}{2}x^{T}Ax+bx+c$, which is convex when $A$ is positive semi-definite, then the function reach GOS iff $f'(x)=0$
Calculating yields $f'(x)=\frac{1}{2}(x^{T}Ax)'+b=\frac{1}{2}((x^{T})'Ax+x^{T}(Ax)')+b$$=Ax+b$ (or one can just remember that $(x^{T}Ax)'=2Ax$)
Hence, the optimal solution to the optimizing problem is the $x=-A^{-1}b$

**Second-order conditions:** Assuming $f$ is twice-continuously-differentiable. Let $H$ be the Hessian matrix of $f$ as $x_{0}$. Then:
- If $x_{0}$ is a LOS, then $f'(x_{0})=0$ and $H$ is positive semi-definite
- If $f'(x_{0})=0$ and $H$ is positive-definite, then $x_{0}$ is a SLOS of min $f$

**Proof**
$f(x_{0}+\Delta x)=f(x_{0})+f'(x_{0})\Delta x+\frac{\Delta x^{T}\nabla^{2}f(x_{0}+t\Delta x)\Delta x}{2}$ for some $t \in [0,1]$.
Or: $f(x_{0}+\Delta x)-f(x_{0})=\frac{1}{2}\Delta x^{T}\nabla^{2}f(x_{0}+t\Delta x)\Delta x$. 
- If $x_{0}$ is LOS, then we can let $\Delta x=\theta\vec{d}$  and RHS is now $\frac{1}{2}\theta^{2}\vec{d}^{T}\nabla^{2}f(x_{0}+t\theta \vec{d})\vec{d}$
	- This thing is non-negative for all $\theta$, hence $\vec{d}^{T}\nabla^{2}f(x_{0}+t\theta \vec{d})\vec{d}$ is non-negative for all $\theta\neq 0$. Because continuity, one can remove this condition and substitute $\theta=0$ and get $\vec{d}^{T}\nabla^{2}f(x_{0})\vec{d}$ is non-negative for all direction $d$, $\blacksquare$
- If $\nabla^{2}f(x_{0})$ is positive-definite, then one can prove that rewrite RHS as $\frac{1}{2}\theta^{2}\vec{d}^{T}\nabla^{2}f(x_{0}+t\theta \vec{d})\vec{d}$
	- 
- If there is some $\Delta x$ $s$.$t$. the RHS is negative, consider the smooth function $g(t)=\Delta x^{T}\nabla^{2}f(x_{0}+t\Delta x)\Delta x$, with $g(t)<0$ and $g(0)\geq 0$ (or $g(0)>0$ in the positive definite case).
	- If $g(0)>0$, then there is $\delta$ such that $g(t)>0$ for all $|t|<\varepsilon$. 