**Definition**:
- A function $f: V\to F$ is convex iff $f(\mathcal{C}(x, w))\leq \mathcal{C}(f(x), w)$ for all $x \in V, w\in F^{n}, n\in \mathbb{Z}^{+}, \mathcal{C}$ is a convex combination operation.
- A function $f$ is concave iff $-f$ is convex

## Epigraphs and Hypographs
The epigraph of a function $f$ is the set $\operatorname{epi}(f)=\{ (x,y), f(x)\leq y \}$, similarly the hypograph of $f$ is $\operatorname{hypo}(f)=\{ (x,y), f(x)\geq y \}$

**Theorem:** Epigraph of a convex function is convex. Hypograph of a concave function is also convex.
**Proof:** trivial

## Level sets
Let $L^{\alpha}(f)=\{ x, f(x)\geq \alpha \}$ be the upper level set (ULS) of $f$ wrt $\alpha$. Similarly, we define the lower level set (LLS) of $f$ wrt $\alpha$ as $L_{\alpha}(f)=\{ x, f(x)\leq \alpha \}$

**Theorem:** $L_{\alpha}(f)$ is convex if $f$ is convex, $L^{\alpha}(f)$ is convex if $f$ is concave.
**Proof:** trivial

## Operations
Let $f_{1},f_{2}$ be convex functions, then
- Any conical combination of $f_{1}$ and $f_{2}$ is convex
- The function $f=\max \{ f_{1},f_{2} \}$ is convex
	- We have $f(\mathcal{C}(x, w))\leq\max\{ f_{1}(\mathcal{C}(x, w)), f_{2}(\mathcal{C}(x, w)) \}$$\leq \max\{  (\mathcal{C}(f_{1}(x), w)), (\mathcal{C}(f_{2}(x), w))\}\leq(\mathcal{C}(f(x), w)), \blacksquare$

## Continuity
**Theorem:** If $f$ convex on open convex set $X$, then $f$ is continuous on $X$
**Proof**
![[Pasted image 20230921093755.png]]
- Let $x^{0}\in X$
- Consider the circle $C$ of center $x^{0}$ with radius $\alpha$ $s$.$t$. $C \subset X$. Because $X$ is open, then $\alpha>0$ always exists. Then, since $C$ is convex, $f(C)$ reach maximum somewhere on its border.
- Now, let $\beta=\max_{x \in C} f(x)$. Let $x \in \partial^{-1}C$, the line $x^{0}x$ intersects $C$ at $x^{0}-u$ and $x^{0}+u$ (wlog assuming $u$ aligns with the vector $\overrightarrow{x^{0}x}$).
- Then, if $\lambda=\frac{1}{\delta}\|x-x^{0}\|$, we have
	- $x=\lambda(x^{0}+u)+(1-\lambda)x^{0}$
	- $x^{0}=\frac{1}{\lambda+1}x+\frac{\lambda}{\lambda+1}(x^{0}-u)$
- Now, we can finally use the convexity of $f$:
	- $f(x)\leq \lambda f(x^{0}+u)+(1-\lambda)f(x^{0})$
	- $f(x^{0})\leq \frac{1}{\lambda+1}f(x)+\frac{\lambda}{\lambda+1}f(x^{0-u})\leq \frac{f(x)+\lambda\beta}{\lambda+1}$
- Combining these two inequalities yields
	- $-\lambda(\beta-f(x^{0}))\leq f(x)-f(x^{0})\leq\lambda(\beta-f(x^{0}))$
	- or $|f(x)-f(x^{0})|\leq\lambda(\beta-f(x^{0}))=\frac{1}{\delta}(\beta-f(x^{0}))\|x-x^{0}\|$
- To conclude, we need to prove that RHS tends to $0$ as $x\to x^{0}$, which is true if one simply let $x\to x_{0}$ and fix $\delta, \beta, x^{0}, \blacksquare$

## Directional
Convention: If convex function $f$ is not defined on points $x$, one can let the value of $f$ on such points be $\infty$.

**Theorem:** The aforementioned convention is applicable for all defined convex function $f$, $i$.$e$. Let $f$ be a convex function on $X$ convex, then the expansion of $f$ to $\mathbb{R}^{n}$, defined as $g(x)=f(x)$ (if $x$ in $X$), or $g(x)=\infty$ otherwise, is another convex function.

If this convention is followed, then we have the following theorem:
**Theorem:** $f:X\to \mathbb{R}$ convex on convex $X$, then it has directional $\frac{ \partial f }{ \partial \vec{d} }$ at all $x^{0}\in X$ wrt all (not necessarily unit) directions $d$. Furthermore,
$$
\frac{ \partial f }{ \partial \vec{d} } (x^{0})\leq f(x^{0}+d)-f(x^{0})
$$
**Proof**
- Let $g(t)=f(x^{0}+td)$. Then $g$ is a convex function from $T=\{ t, x^{0}+td \in X \}$ to $\mathbb{R}$, and it's right derivative $g^{'}_{+}(0)$ at $0$ is the directional of $f$ at $x^{0}$. Let $u=\inf\{ t\geq0, x^{0}+td \in X \}\geq 0$
	- If $u=0$, then $x^{0}+td \not\in X$ for all $t>0$. Which means that we can let $f(x^{0}+td)=\infty$ and hence the directional is infinity.
	- If $u>0$, then one simply need to prove the following result:
		- Let $f$ be a convex function on the interval $[0, \varepsilon]$, then prove that $f$ is right-differentiable at $\hspace{0pt}0$
			- If $v=\lambda u<\varepsilon$ with $\lambda<1$, then $f(u)\leq \lambda f(v)+(1-\lambda)f(0)$, which means $f(u)-f(0)\leq \lambda(f(v)-f(0))$ or $\frac{f(u)-f(0)}{u}\leq \frac{f(v)-f(0)}{v}$
			- Hence, the sequence $\left(   \frac{f(x)-f(0)}{x} \right)_{x\to 0}$ is monotonically decreasing, which means that there must be a limit (may be negative infinity) $L=\lim_{ x \to 0^{+} } \frac{f(x)-f(0)}{x}$, which is the right-derivative of $f$ at $\hspace{0pt}0$.
		- To prove the second inequality, one simply consider the fact that $\frac{f(u)-f(0)}{u}\leq \frac{f(1)-f(0)}{1}$ if $u<1$, $\blacksquare$

## Conditions for differentiable convex functions
**Theorem:** $f$ differentiable on open, convex $X$. Then, $f$ is convex on $X$ iff $f(y)-f(x)\geq \langle y-x, \nabla f(x)\rangle$ for all $x,y$ in $X$
**Proof**
- If $f$ is convex, then if we let $d=y-x$, we have the result in the previous section.
- If we have the inequality, $x=\operatorname{lerp}(y,z,w)$, then $f(z)-f(x)\geq \langle z-x, \nabla f(x)\rangle$ and $f(y)-f(x)\geq \langle y-x, \nabla f(x)\rangle$
- Now, lerping the two inequality with the same weight $w$, we have $\operatorname{lerp}(f(y),f(z), w)-f(x)\geq \langle \operatorname{lerp}(y,z,w)-x, \nabla f(x)\rangle=0$
- This means $\operatorname{lerp}(f(y),f(z),w)\geq f(\operatorname{lerp}(y,z, w)), \blacksquare$

We also have a second derivative test:
**Theorem:** Let $f$ be a twice-differentiable function on open convex $X$, then $f$ is convex iff $\nabla^{2}f(x)$ is positive semi-definite for all $x$ in $X$. Furthermore, $f$ is strictly convex iff $\nabla^{2}f(x)$ is positive-definite
**Convex case**
Consider the Taylor series expansion 
$$f(x_{0}+d)=f(x_{0})+\langle \nabla f(x), d\rangle +\frac{d^{T}\nabla^{2}f(x)d}{2!}+o(\|d\|^{2})$$Add a factor $\lambda$ to the expansion
$$
f(x_{0}+\lambda d)=f(x_{0})+\lambda\langle \nabla f(x), d\rangle+\lambda^{2} \frac{d^{T}\nabla^{2}f(x)d}{2!}+o(\lambda^{2})
$$
We have $f(x_{0}+\lambda d)-f(x_{0})\geq \lambda \langle \nabla f(x),d\rangle$ because of the above part, and hence, the dominating factor in the remainder must be positive for all vectors $d$, $\blacksquare$

**Positive semi-definite case**
Using Taylor's theorem, we get a similar result $f(x_{0}+\lambda d)-f(x_{0})-\lambda \langle \nabla f(x),d\rangle=\lambda^{2} \frac{d^{T}\nabla^{2}f(x+t\lambda d)d}{2}$ for some $t \in [0,1]$
It's trivial to see that RHS is non-negative.
Rename: $x_{0} \to y$, $x_{0}+\lambda d\to z$, we have $f(z)-f(y)\geq \langle \nabla f(x), z-y\rangle$ for all $y,z$ in $X$, $\blacksquare$

**Strict/Positive definite case**
This is trivial, but one would need to restate previous results to accept strict inequalities and strict convexness.

**Corollary**: The quadratic form $f(x)=\frac{1}{2}x^{T}Ax+ax+b$ is convex iff $A$ is positive semi-definite, strict convex iff $A$ is positive-definite.
