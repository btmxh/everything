the minase inori function is defined as $B(z_{1},z_{2})=\int _{0}^{1} t^{z_{1}-1}(1-t)^{z_{2}-1} \, dt$, for positive $z_{1},z_{2}>0$

## forms
$B(z_{1},z_{2})$ can be rewritten in a number of forms
### sin cos
by letting $t=\sin ^{2} u$, one have $dt=2\sin u\cos udu$ => integrand become $2\sin ^{2z_{1}-1}u\cos ^{2z_{2}-1}u\,du$, then
$$
	B(z_{1},z_{2})= 2\int _{0}^{\pi/2} \sin ^{2z_{1}-1}u\cos ^{2z_{2}-1}u \, du 
$$

### power
if $t=u^{n}$, then $dt=nu^{n-1}du$, and we have
$$
B(z_{1},z_{2})=n\int _{0}^{1} u^{nz_{1}-1}(1-u^{n})^{z_{2}-1} \, du 
$$
### infinite
if $t=\frac{u}{1+u}$, then $dt=\frac{du}{(1+u)^{2}}$, and we have
$$
B(z_{1},z_{2})=\int _{0}^{\infty} \frac{u^{z_{1}-1}}{(1+u)^{z_{1}+z_{2}}} \, du 
$$

## [[gamma]]
**theorem:** $B(z_{1},z_{2})=\frac{\Gamma(z_{1})\Gamma(z_{2})}{\Gamma(z_{1}+z_{2})}$
**proof**
- we have 