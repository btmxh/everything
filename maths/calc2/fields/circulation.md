vi: **hoàn lưu**, **lưu số**

basically the same thing as flux but for curves

formula: $\int_{C} \mathbf{F} \, ds=\int_{C} F_{x}dx+F_ydy+F_zdz$
RHS can be transformed in two way using [[generalized stoke's theorem]]
- if $F_{x}dx+\dots=dG$, then it evaluates to $\int_{\partial C} G=G(c_{1})-G(c_{0})$, where $c_{1}$ and $c_{0}$ are the endpoint and the begin point respectively ([[scalar potential]])
- **more useful**: the integrand is 1-form of $\mathbf{F}$ => we can get the [[curl]] => RHS = $\int _{\partial^{-1}C} \nabla \times \mathbf{F}$ ([[generalized stoke's theorem#stoke's theorem|stoke's theorem]])

e.g. calc circulation $\mathbf{F}=(y,z,x)$, along $\mathbf{r}(t)=(\cos t, \sin t, t)$ from $t=0$ to $t=1$
- bxd: $\int_{L} ydx+zdy+xdz$$=\int _{L} (\sin t(-\sin t)+t\cos t+\cos t) \, dt$$=\frac{\pi}{4}$

e.g. $\omega=(y+z)dx+(x+z)dy+(x+y)dz$, curve $C: \mathbf{r}=a(\sin ^{2}t, 2\sin t\cos t, \cos ^{2}t)$
then $C$ is a part of the sphere $(O, a^{2})$ as well as the plane $x+z=a$ => it's the disk $x^{2}+y^{2}+z^{2}=a^{2}, x+z=a$ (useless information btw)
- using [[generalized stoke's theorem#stoke's theorem|stoke's theorem]], one evaluates $d\omega=(dy+dz)dx+(dx+dz)dy+(dx+dy)dz=0$ => [[field#conservative vector field|conservative vec field]] => integral evals to 0

e.g. 