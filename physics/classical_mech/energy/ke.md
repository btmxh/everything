kinetic energy: the [[energy]] related to motion of objects
e.g. an object move from $A$ to $B$ under the effect of force $\mathbf{F}$, then
- the amount of work: $W=\int _{A}^{B} \mathbf{F}d\mathbf{s}=\int _{A}^{B}m \frac{d\mathbf{v}}{dt} \, d\mathbf{s}=\int _{A}^{B}m \frac{d\mathbf{s}}{dt} d\mathbf{v}=\int _{A}^{B}m\mathbf{v} \, d\mathbf{v}=\frac{1}{2}(mv_{2}^{2}-mv_{1}^{2})$
- since work = diff of [[energy]], we have $W=E_{2}-E_{1}$
- due to the [[relative]]-vity of [[energy]], one can let $E_{1}=\frac{1}{2}mv_{1}^{2}, E_{2}=\frac{1}{2}mv_{2}^{2}$
- (or alternatively, one can see that $E -\frac{mv^{2}}{2}$ does not depend on the motion, which will be called the [[potential energy]])

=> the **kinetic energy** of a [[point mass]] with mass $m$, velocity $v$ is $KE=\frac{1}{2}mv^{2}$

## theorem
by the prev e.g, one can see that $KE_{2}-KE_{1}=W$, or alternatively **the change in KE of a [[point mass]] in some path is equals to the [[work]] caused by the outside [[force]] exerted on that [[point mass]] during that path**
then, if $W>0, KE_{2}>KE_{1}$ => $\mathbf{F}$ give energy to the [[point mass]], and conversely etc.

e.g. collision

- in collisions, [[momentum#conservation of momentum|conservation of momentum]] always hold:
	- $m_{1}\mathbf{v_{1}}+m_{2}\mathbf{v_{2}}=m_{1}\mathbf{v_{1}'}+m_{2}\mathbf{v_{2}'} \implies m_{1}\Delta \mathbf{v_{1}}=-m_{2}\Delta \mathbf{v_{2}}$ (1)
- conservation of [[ke]] does not always hold, but if it does:
	- $m_{1}v_{1}^{2}+m_{2}v_{2}^{2}=m_{1}v_{1}'^{2}+m_{2}v_{2}'^{2}$
	- then $m_{1}\Delta(\mathbf{v_{1}^{2}})=-m_{2}\Delta(\mathbf{v_{2}^{2}})$ (2)
	- diving (2) by (1) then $\boxed{v_{1}+v_{1}'=v_{2}+v_{2}'}$ => **total velocity is conserved**
	- (one can proceed by solving some dumb linear sys of eq)
- if $v'=v_{1}'=v_{2}'$ (collide into one huge object), then $v'=\frac{m_{1}v_{1}+m_{2}v_{2}}{m_{1}+m_{2}}$, and $Q=E_{2}-E_{1}$ (diff. of energy) can be calculated: $Q=-\frac{m_{1}m_{2}}{2(m_{1}+m_{2})}(v_{1}-v_{2})^{2}$ (energy is lost to deform the objects

## [[rigid body]]
we have $dW=\mu d\theta$ => $dW=I\beta d\theta=I\beta \omega dt=I\omega d\omega$, integrating yield $KE=\frac{1}{2}I\omega^{2}$
when the axis is moving with velocity $v$, one will have the full [[ke]]: $KE=\frac{1}{2}(mv^{2}+I\omega^{2})$
if object is rolling (without sliding), $v=r\omega$, then $KE=\frac{1}{2}v^{2}\left( m+\frac{I}{r^{2}} \right)$

## [[gas]]
gases, much alike [[rigid body]] have their ke split into 2
- the common ke of the system
- the internal energy of the system
