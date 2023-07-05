## first kind
bla bla bla
- independent wrt orientation
- additive
- integrand odd + surface reflective => 0, ...

calc
$S: z=z(x,y), (x,y)\in D$, then $\iiint_{S} f(x,y,z)ds=\iint_{D} f(x,y,z(x,y))\sqrt{ 1+z_{x}'^{2} +z_{y}'^{2} }dxdy$
(parameterized surface is similar, with $ds= |\mathbf{r'}_{u}\times \mathbf{r'}_{v}|dudv$)

e.g. $\iint_{S} \sqrt{ x^{2}+y^{2} }ds$, $S=\partial \Omega, \Omega: \sqrt{ x^{2}+y^{2} }\leq z\leq 1$
$S_{1}: \sqrt{ x^{2}+y^{2} }\leq z=1$ => $\iint_{x^{2}+y^{2}\leq 1} r^{2} dxdy=\dots$
$S_{2}: \sqrt{ x^{2}+y^{2} }=z\leq 1$ => $\iint_{x^{2}+y^{2}\leq 1} r^{2}\sqrt{ 1+\left( \frac{x}{r} \right)^{2}+\left( \frac{y}{r} \right)^{2} }dxdy=\dots$

e.g. $\iiint zds$, $S: z=3-x-y$ bounded by $x+y=3,3x+2y=6,z=0$
e.g. area of $2z=x^{2}$ on $x-2y=0,y-2x=0,x=2\sqrt{ 2 }$
e.g. area of $z=\sqrt{ x^{2}+y^{2} }$ bounded by $x^{2}+y^{2}+z^{2}=2$
e.g. $x^{2}+y^{2}+z^{2}=4$ bounded by $x=z,z=\sqrt{ 3 }x,x\geq 0$

## second kind
### vector-bivector wedge product
in 3d, 
$$
\begin{align}
&(v_{x}e_{1}+v_{y}e_{2}+v_{z}e_{3})(b_{yz}e_{2}e_{3}+b_{zx}e_{3}e_{1}+b_{xy}e_{1}e_{2}) \\
&=(v_{x}b_{yz}+v_{y}b_{zx}+v_{z}b_{xy})e_{1}e_{2}e_{3} - (\dots)
\end{align}
$$
now, pretend that we are an L bozo down bad blue archive player who does not know the wisdom of [[geometric algebra]], you will describe the bivector as its dual (:skull:), the first term, i.e. the wedge product can be written as $v_{x}b'_{x}+\dots$, aka the dot product between $\mathbf{v}$ and $\mathbf{b}$, but in reality, it's a vec-bivec wedge product

### surface integral
like in [[lineint]] with $d\mathbf{r}=dx+dy+dz$, we "define" $d \vec{\vec{S}}=dxdy+dydz+dzdx$ to be a infinitesimal bivector ($dxdy=dx\wedge dy$, remember geometric products?). then this integral: $\iint_{\Sigma} \mathbf{F}\wedge d\vec{\vec{S}}$, is the surface integral in its original form.

then L bozo, when one let $\mathbf{S}$ to be the dual of $\vec{\vec{S}}$, the integral becomes $\iint_{\Sigma} \mathbf{F}\cdot d\mathbf{S}$ (times $e_{1}e_{2}e_{3}$), the most popular form of this thing.

this thing can be trivially extended to n-dimension but whatever

then one can also write the integral in the form $\iint_{\Sigma} F_{x}dydz+\dots$, much like the [[lineint]], and apply [[generalized stoke's theorem]]
- integrating over $\partial \Sigma$, we need something that have $d\mathbf{f}=F_{x}dydz+\dots$ =>  $\mathbf{f}$ repr something that have $\nabla \times f=\mathbf{F}$ => [[generalized stoke's theorem#stoke's theorem|stoke's theorem]]
- integrating over $\partial^{-1}\Sigma$, we need something to take the [[ext derv]] of the integrand => $\nabla\cdot \mathbf{F}$, the [[generalized stoke's theorem#divergence theorem|div theorem]]

>q: why don't we use the wedge product with the [[lineint]] thing?
>a: then the result will be a bivector => L bozo mindset can't find a use for that


