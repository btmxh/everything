unlike [[const grav]], in (newton's) reality, $\mathbf{g}$ depends on $h_{A}$
**newton's law of gravity**
let $(m_{1}, \mathbf{r_{1}})$ and $(m_{2}, \mathbf{r_{2}})$ be 2 objects, then the gravity by $m_{2}$ asserted on $m_{1}$ is
$$
\mathbf{F_{21}}=Gm_{1}m_{2} \frac{\mathbf{r_{2}}-\mathbf{r_{1}}}{\|\mathbf{r_{2}}-\mathbf{r_{1}}\|^{3}}
$$
in L bozo terms, $F=\frac{Gm_{1}m_{2}}{\|r_{1}-r_{2}\|^{2}}$

(*we will use einstein summation extensively here*)
now consider a system of $n$ masses $(m_{k},\mathbf{r_{k}})$, then one can define the grav field to be $\mathbf{G}(\mathbf{r})=Gm_{k}\frac{\mathbf{r_{k}}-\mathbf{r}}{\|\mathbf{r_{k}}-\mathbf{r}\|^{3}}$, is the gravity force per unit of mass asserted to some point at $\mathbf{r}$

for simplicity, assume $n=1$ and replace the subscript with prime symbols. while we're at it, let $\mathbf{r'}=0$, then $\mathbf{G(r)}=-\frac{Gm'\mathbf{r}}{\mathbf{\|r\|^{3}}}$

now, we'll try to integrate $\frac{\mathbf{r}}{\|\mathbf{r}\|^{3}}$ to get the [[scalar potential]] of this field: $\int  \frac{\mathbf{r}}{\|\mathbf{r}\|^{3}} d\mathbf{r} = \frac{1}{2} \int \frac{d(\mathbf{\|r\|^{2}})}{\|\mathbf{r}\|^{3}}=-\frac{1}{\|\mathbf{r}\|}+C$ (notation provided by the [[generalized stoke's theorem#gradient|gradient theorem]])

let $C=0$, which is equivalent to letting the [[scalar potential]] at infinity ($\|\mathbf{r}\|=\infty$) to be zero, we have our formula for the **gravitational potential**: $V=-\frac{Gm}{\|\mathbf{r}\|}$, $\mathbf{G}=\nabla V$

in the general case, since integrals and gradient operators are linear operators (they are even linear maps in some weird functional vector space), we can just sum it up: $V=- \frac{Gm}{\|\mathbf{r_{k}}-\mathbf{r}\|}$

## [[pe]]
the gravitational potential, $V=-\frac{Gm}{r} + C$ repr the [[pe]] of a point at $\mathbf{r}$, where $C$ is the grav [[pe]] at the point infinity $\mathbf{r}=\infty$

## [[const grav]]
the $g$ in [[const grav]] can be calculated from this thing as
$g(r)=\frac{GM}{r^{2}}=g(r_{0})\cdot\left( \frac{r}{r_{0}} \right)^{2}$

## [[angular momentum]] conservation
if one puts a [[point mass]] at $O$ and do some [[angular momentum]] wrt to that point $O$ (denoted $\vec{\vec{L}}$), one would see that since $\mathbf{r}$ and $\mathbf{F_{g}}$ are parallel, its outer product is zero. hence, the [[torque]] $\mu_{/O}(\mathbf{F_{g}})$ is conserved, and objects will continue to move in a plane represented as the bivector $\vec{\vec{L}}$

## gauss's law

> this can serve as an introduction to maxwell's equations

since gravity is conservative, $\nabla \times \mathbf{G}=0$ (one can use the identity $\nabla \times (\nabla V)=0$ to trivially check this)

the only thing left for us is to calculate $\nabla \cdot \mathbf{G}=\nabla \cdot \left( -\frac{Gm'\mathbf{r}}{\|\mathbf{r}\|^{3}} \right)=-\nabla\left( \frac{1}{\|\mathbf{r}\|^{3}} \right)Gm'\mathbf{r} - \frac{1}{\|\mathbf{r}\|^{3}} \nabla \cdot (Gm'\mathbf{r})$
- we can use the multivar chain rule to calc the first gradient (bla bla bla jacobian): $\nabla\left( \frac{1}{\|\mathbf{r}\|^{3}} \right)=-\frac{3}{\|\mathbf{r}\|^{4}}\nabla \mathbf{r}=-\frac{3\mathbf{r}}{\|\mathbf{r}\|^{5}}$
- the second one is trivial $\nabla \cdot \mathbf{r}=3$
- now we do a little trolling and calculate the divergence  $\nabla\cdot \mathbf{G}=\frac{3Gm'\mathbf{r}^{2}}{\|\mathbf{r}\|^{5}}-\frac{3Gm'}{\mathbf{\|r\|^{3}}}=0$

this divergence is zero, at least for all $\mathbf{r} \neq 0$. at $\mathbf{r}=0$, one sees that $\mathbf{G}$ and $V$ both approaches $\infty$, so we have some singularities. like in complex analysis, to investigate singularities, we investigate stuff that contains it.

- take this funny integral $\iiint_{V} \nabla\cdot \mathbf{G}dV=\text{(\\oiint not supported sadge)} \iint_{\partial V} \mathbf{G}\cdot \mathbf{\hat{n}} dS$
- when $V$ is a sphere, $\mathbf{G}$ and $\mathbf{\hat{n}}$ are parallel and have opposing direction, therefore, the RHS integrand evaluate to $-\frac{Gm'}{r^{2}}$, which since $r$ is const on the sphere, RHS is $-4\pi Gm'$
- (more generally, $\iiint_{V}\nabla\cdot \frac{\mathbf{r}}{\|\mathbf{r}\|^{3}}dV=4\pi$, if $V$ contains the point $\mathbf{r}=0$)

now you can "unwrap" the 3d integral into a 1d integral ($V$ -> some diameter of the sphere for example, since every other point different than $\mathbf{r}=0$ does not contribute to the integral), and woila, you get this familiar expression: $\int _{-r}^{r} \mathbf{G_{1d}}(t) dt$

bla bla bla this is dirac delta bullcrap, so now we finally calculated $\nabla\cdot \mathbf{G}=-4\pi Gm'\delta(\mathbf{r})$

now, we combine $m'$ and the dirac delta into a new thing: the **mass density** $\rho(\mathbf{r})$: $\nabla\cdot \mathbf{G}=-4\pi G\rho(\mathbf{r})$

using mass density, one can restate the gravitational field equation to be more formally into: $\mathbf{G}(\mathbf{r})=\int _{\mathbb{R}^{3}} G\rho(\mathbf{s}) \frac{\mathbf{s-\mathbf{r}}}{\|\mathbf{s}-\mathbf{r}\|^{3}} \, d\mathbf{s}$

and using this formal definition, along with the fact that $\nabla\cdot \frac{\mathbf{r}}{\|\mathbf{r}\|^{3}}=4\pi\delta(\mathbf{r})$, one can re-prove $\nabla\cdot \mathbf{G}=-4\pi G\rho(\mathbf{r})$ (not that the previous "prove" is just by defining $\rho(\mathbf{r})=m'\delta(\mathbf{r})$)

hence, newton's law for gravity can be prove the following three facts:
- $\nabla \times \mathbf{G}=0$
- $\nabla\cdot \mathbf{G}=-4\pi G \rho(\mathbf{r})$
- $\mathbf{G}(\infty)=0$ (boundary conditions)

this three facts, combined are actually equivalent to newton's law, and one can "easily" prove it by integrating the 2nd thing over a radius-1 sphere.