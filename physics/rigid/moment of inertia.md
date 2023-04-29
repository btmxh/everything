defined as $I=\frac{L}{\omega}$, with $L$ being the [[angular momentum]], $\omega$ being the [[angular velocity]]

for a point mass, we have $\mathbf{L}=\mathbf{r}\times \mathbf{p}$, and $\omega=\frac{\mathbf{r} \times \mathbf{v}}{r^{2}}$, then $I=mr^{2}$
then, in an object, we have $dI=r^{2}dm$
using this, we can calc the moment of inertia of several objects around some axis that passes through its [[center of mass]]
- bar: $I=\frac{mr^{2}}{12}$ ($r$ is the bar's length)
- disk: $I=\frac{mr^{2}}{2}$
- hollow sphere: $I=\frac{2mr^{2}}{3}$
- solid sphere: $I=\frac{2mr^{2}}{5}$

e.g. prove the last formula
- consider the sphere $V: x^{2}+y^{2}+z^{2}=r^{2}$ with rotation axis $x=y=0$, then $r=|z|$ and
- $I=\iiint_{V} dI=\iiint_{V} z^{2}dm=\rho \iiint_{V}z^{2}dV$
- let $x=a\sin u\sin v, y=a\sin u\cos v, z=a\cos u$, then $|J|=a^{2}\sin u$ and $\frac{I}{\rho}=\iiint_{V'} a^{4}\sin u\cos ^{2}udV$
- this integral is equals to $\frac{I}{\rho}= 8\pi\int _{a=0}^{r} \int _{u=0}^{\pi/2} a^{4} \sin u\cos ^{2}u\, du \, da$$=8\pi \int _{0}^{r} a^{4} \, da\int _{0}^{1} t^{2}\,dt=\frac{8\pi r^{5}}{15}$
- $\rho=\frac{m}{V}=\frac{3m}{4\pi r^{3}}$, then $I=\frac{3m}{4\pi r^{3}} \frac{8\pi r^{5}}{15}=\frac{2mr^{2}}{5}$

to move the axis, one can use the [[parallel axis theorem]] and [[perp axis theorem]]

e.g. solve for $a$, knowing the pulley mass $m$ and radius $r$
![[Pasted image 20230422211314.png]]
we have $m_{1}a=F_{t1}-m_{1}g, m_{2}a=m_{2}g-F_{t2}$ => $F_{t1}=m_{1}(g+a), F_{t2}=m_{2}(g-a)$
the net torque $\tau=r(F_{t2}-F_{t1})=I_{pulley}\beta$
we know
- $r\beta=a$, because bla bla bla
- $I_{pulley}=\frac{1}{2}mr^{2}$
=> $m_{1}(g+a)-m_{2}(g-a)=\frac{1}{2}ma$
=> $a=\frac{m_{2}-m_{1}}{m_{1}+m_{2}+\frac{1}{2}m}g$, $r$ actually does nothing here

e.g. find $a$
![[Pasted image 20230422211943.png]]
let positive dir be $B$ down, the rope [[accel.]] is $a$
- then $m_{B}a=m_{B}g-T_{3}$, $\frac{m_{A}+m_{1}}{2}a=T_{2}+T_{1}-(m_{A}+m_{1})g$
- [[torque]] thingy: $r_{2}(T_{3}-T_{2})=\frac{1}{2}m_{2}r_{2}a, r_{1}(T_{2}-T_{1})=\frac{1}{2}m_{1}r_{1}a$
so
$$
\begin{align}
T_{3}&=m_{B}(g-a) \\
T_{1}+T_{2}&=(m_{A}+m_{1})\left( g+\frac{a}{2} \right) \\
T_{3}-T_{2}&=\frac{1}{2}m_{2}a \\
T_{2}-T_{1}&=\frac{1}{2}m_{1}a
\end{align}
$$
we eliminate the $T$'s: $2(3)+(4)$: $2T_{3}-(T_{1}+T_{2})=a\left( m_{2}+\frac{m_{1}}{2} \right)$
sub $(2)$ and $(1)$: $2m_{B}(g-a)-(m_{A}+m_{1})\left( g+\frac{a}{2} \right)=a\left( m_{2}+\frac{m_{1}}{2} \right)$
=> $a\left( m_{2}+\frac{m_{1}}{2}+2m_{B}+\frac{m_{A}+m_{1}}{2} \right)=(2m_{B}-m_{A}-m_{1})g$
=> $a=\frac{2m_{B}-m_{A}-m_{1}}{m_{1}+m_{2}+2m_{B}+\frac{m_{A}}{2}}g$
idk if this is right but whatever
