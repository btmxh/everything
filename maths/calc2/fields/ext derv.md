basically to calc this, one just need
- 1. $f$ is 0-form => $df$ is the normal differential form
- 2. $d(df)=0$ for 0-form $f$
- 3. $d(a \wedge b)=da \wedge b+(-1)^{p}(a \wedge db)$, for $p$-form $a$

then one can prove, for indep vars $x, y$:
- $dx \wedge dy=-dy \wedge dx$
- corollary: $dx \wedge dx = 0$

## [[field]], [[divergence]] and [[curl]]
in 3d case (div and curl are dumb concepts that only works well in 3d)
scalar field $f$ has itself as an 0-form => $df=\frac{\partial f}{\partial x_{i}}dx_{i}$ => gradient
vec field $f$ has $f_{i}dx_{i}$ as an 1-form => $df$ bla bla bla is the curl
vec field $f$ has $f_{i}dx_{1}dx_{2}\dots dx_{i-1}dx_{i+1}\dots$ as an $3-1=2$-form => $df$ is divergence

then, we can use the [[generalized stoke's theorem]]!!!!

e.g. $f=(f_{x},f_{y},f_{z})$ => 0-form: $\mathbf{f} = f_{x}dx+f_{y}dy+f_{z}dz$ => $d\mathbf{f}=\left( \frac{\partial f_{x}}{\partial x}dx+\frac{\partial f_{x}}{\partial y}dy+\frac{\partial f_{x}}{\partial z}dz \right)dx+\dots$ => expand we have $d\mathbf{f}=\left( \frac{\partial f_{y}}{dx}-\frac{\partial f_{x}}{dy} \right)dx \wedge dy+\dots$ => it's the curl!

e.g. $f=(f_{x}, f_{y}, f_{z})$ => 2-form: $\mathbf{f}=f_{x}dydz+\dots$ => $d\mathbf{f}=\left( \frac{\partial f_{x}}{\partial x}dx+\frac{\partial f_{x}}{\partial y}dy+\frac{\partial f_{x}}{\partial z}dz \right)dydz+\dots$ => $d\mathbf{f}=dxdydz\left( \frac{\partial f_{x}}{\partial x}+\dots \right)$ => it's the divergence!
