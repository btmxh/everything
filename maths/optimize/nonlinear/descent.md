Consider the [[optimize problem]] min $f(x)$ for $x \in \mathbb{R}^{n}$

If for every $x \in \mathbb{R}^{n}$, one can either conclude $x$ is optimal or pick some $x'$ that is more optimal than $x$, then we have the following algorithm:
- Start with the point $x_{0}$, if $x_{0}$ is optimal, end.
- Otherwise, pick $x_{1}$ more optimal that $x_{0}$
- Assign $x_{1}$ to $x_{0}$, repeat.

The algorithm has many major flaws and modifications that one can add to:
- One can't be sure that $x_{0}$ is optimal or not. For example, the gradient condition $\nabla f(x_{0})=0$ does not necessarily imply that $x_{0}$ is optimal. Hence, you can modify the algorithm as such:
	- When the algorithm halts, the output may not be optimal.
	- Picking $x_{1}$ may not necessarily be more optimal than $x_{0}$, as we want to use $x_{1}$ somewhat like a gamble.

## Backtracking
**Armijo conditions:** Let $f$ be a differentiable function, a point $x$ and a vector $d$ such that $f'(x)d<0$. Then for every $0<m<1$, there exists some $t_{0}>0$ such that
$$
f(x+td)\leq f(x)+mtf'(x)d
$$
for all $t \in [0, t_{0}]$

**Proof**
We have $f(x+td)=f(x)+tf'(x)d+o(t)$, then $\frac{f(x+td)-f(x)}{tf'(x)d}=1+ o(1)$, which means that there exists $t_{0}$ such that $\frac{f(x+td)-f(x)}{tf'(x)d}\leq m$ for all $m \in (0,1), t \in [0, t_{0}]$. Note that $f'(x)d<0$, we have $\blacksquare$

**Backtracking Algorithm**:
Input: point $x$, direction $d$ as the decreasing direction from $x$
Output: point $x'=x+td$ more optimal than $x$
$\hspace{0pt}1$. Pick $m$ and some $\alpha \in (0,1)$. Let $t:=1$
$\hspace{0pt}2$. Calculate $x'=x+td$ and $f(x')$
$\hspace{0pt}3$. If $x'$ satisfies the output conditions, then return
$\hspace{0pt}4$. Otherwise, let $t:=\alpha t$ and go to the second step.

Because of the existence of $t_{0}$, the algorithm will halt at some point.
## Gradient descent
First, we have $\frac{ \partial u }{ \partial \vec{d} }(x)=u'(x)\vec{d}$, which means that if $\vec{d}$ and $\nabla u(x)$ has the same direction, which means that we can fill in the blanks:
- $x_{0}$ is (considered to be) optimal if $\nabla f(x_{0})=0$
- $x_{1}=x_{0}+t\nabla f(x_{0})$ may be more optimal than $x_{0}$, with $t$ being the step length.

### Step length
The naive way to calculate step length is simply letting step length a predefined number.

A more optimal way (which is "pure descent") is to let $t= \operatorname{argmin}\{ f(x_{0}+t\nabla f(x_{0})), t\geq 0 \}$
Let $\phi(t)=f(x_{0}+t\nabla f(x_{0}))$, then one can use the derivatives to find $t$.

$e$.$g$. Find $t$ for $f(x)=\frac{1}{2}x^{T}Ax+bx+c$ for symmetric $A$
Let $v=\nabla f(x_{0})$, then:
$\phi(t)=f(x_{0}+tv)=\frac{1}{2}(x_{0}+tv)^{T}A(x_{0}+tv)+b(x_{0}+tv)+c$
$f(x)=\frac{1}{2}x^{T}Ax+bx+c$, then $f'(x)=x^{T}A+b$
$\frac{d\phi}{dt}=\frac{d\phi}{d(x_{0}+tv)} \frac{d(x_{0}+tv)}{dt}=f'(x_{0}+tv)v$$=2((x_{0}+tv)^{T}A+b)v$
Solving $\phi'(t)=0$ yields
$x_{0}^{T}Av+tv^{T}Av+bv=0$, or $t=-\frac{bv+x_{0}^{T}Av}{v^{T}Av}=-\frac{(b+x_{0}^{T}A)v}{v^{T}Av}=-\frac{f'(x_{0})v}{v^{T}Av}\geq 0$
