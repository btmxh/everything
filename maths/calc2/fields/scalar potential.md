if [[field#vector field|vec field]] $\mathbf{F}$ has a [[field#scalar field|scalar field]] $u$ s.t. $\mathbf{F}=-\nabla u$ (called its [[scalar potential]], negative sign is by physics mfs) => by the [[generalized stoke's theorem#gradient theorem|grad theorem]], one have $\int _{AB} \mathbf{F} \, d\mathbf{r}=u(A)-u(B)$ does not depend on the path $AB$, but only the endpoints. in the case $A\equiv B$, the integral is zero => $\oint\mathbf{F}d\mathbf{r}=0$ for all closed path

if a vecfield has scalar potential, it's called to be **conservative**

**theorem**: $\mathbf{F}$ conservative iff $\nabla \times \mathbf{F}=0$ at all points in the field
**proof**
- if $\nabla \times \mathbf{F}=0$ => pick a stationary point $\mathbf{r_{0}}$, one will let $u(\mathbf{r})=\int _{[\mathbf{r_{0},\mathbf{r}}]} \mathbf{F} \, d\mathbf{r}$ (integrating via the straight path), now we'll prove that $\mathbf{F}=\nabla u$, i.e. $\nabla\int _{[\mathbf{r_{0}},\mathbf{r}]} \mathbf{F} \, d\mathbf{r}=\mathbf{F}$
	- to calc $LHS$, one calc the [[directional]] by $\frac{\partial LHS}{\partial \hat{v}}=\lim_{ t \to 0 } \frac{LHS(\mathbf{r}+t\hat{v})-LHS(\mathbf{r})}{t}$
	- if we have $\oint\mathbf{F}d\mathbf{r}=0$ for all closed path, numerator will be $\int _{[\mathbf{r},\mathbf{r}+t\hat{v}]} \mathbf{F}\, d\mathbf{x}$, and we can calc this integral by parameterize the line between the two points: $\mathbf{x}=\mathbf{r}+u\hat{v}$, for $u\in[0,t]$ => $d\mathbf{x}=\hat{v}du$ (note that $\mathbf{r}$ const) => int evals to $\int _{0}^{t} \mathbf{F}(\mathbf{r}+u\hat{v}) \cdot \hat{v} \, du$
		- why is that oint 0? it's because of the [[generalized stoke's theorem#stoke's theorem|stoke's theorem]], that oint is $\iint_{\Sigma} \nabla \times \mathbf{F}$, which is obviously 0
	- => the limit is $\lim_{ t \to 0 } \frac{1}{t}\int _{0}^{t} \mathbf{F}(\mathbf{r}+u\hat{v}) \cdot \hat{v} \, du$
	- now, note that if one let $f(t)$ to be the integral, then the limit is now $\lim_{ t \to 0 } \frac{1}{t}(f(t)-f(0))$ (note that $f(0)=0$ due to $\int _{0}^{0} \dots \, dx=0$) => the limit is the derivative of $f$ at $u=0$, and due to the [[generalized stoke's theorem#ftc|ftc]], it's $\mathbf{F}(\mathbf{r})\cdot \hat{v}$
	- then, since the [[directional]] wrt $\hat{v}$ is $\nabla u$ for any scalar field $u$ => qed
- if $\mathbf{F}=\nabla u$, then one can easily prove $\nabla \times \nabla u=0$ => qed

## application
in physics, a potential force field (trường lực thế) is a force [[field]], s.t. it satisfies the above thing => the [[work]] of the field on a moving particle from $A$ to $B$ only deps on the endpoint $A$ and $B$, not the path $AB$
=> $\oint\mathbf{F}d\mathbf{s}=0$

the [[scalar potential]] of that field is then used to define the [[pe]]
- since $\int _{AB} \mathbf{F} \, d\mathbf{r}=u(A)-u(B)=KE_{B}-KE_{A}$ => $KE_{A}+u(A)=KE_{B}+u(B)$ => [[energy]] conservation!

we also have the relationship between the [[force]] $\mathbf{F}$ and the [[pe]] $u$: $\mathbf{F}=-\nabla u$ (i did not notice this at first)