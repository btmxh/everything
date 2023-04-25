ideal gas are gases with no interparticle interactions => no $H_{2}, O_{2}$, etc. + atom radius basically 0

## laws
boyle-mariotte: $m$ const, then if $T$ const, $pV$ const
gay-lussac: $m$ const, then
- if $V$ const, $p \propto T$
- if $p$ const, $V \propto T$

=> $pV=nRT$, with $R=8.31 \frac{\text{J}}{\text{mol}\cdot \text{K}}$

## basic eqn
from [[maxwell dist.]], we have $E=KE=\frac{3}{2}kT$ is the energy of ideal gas (since the molecules don't interact, $PE=0$)

(since we're gonna work with momentum here, we will denote pressure by $P$)
assume all particles bouncing in one direction
every time it bounces, the change in momentum (neglecting signs) is $\Delta p=2mv$ => $F=\frac{\Delta p}{\Delta t}$, and since $\Delta t=\frac{2x}{v}$ => $F=\frac{2mv^{2}}{x}, p=\frac{F}{S}=\frac{mv^{2}}{xS}=\frac{mv^{2}}{V}$, taking the sum yields $P=N\frac{m\bar{v^{2}}}{V}$ ($N$ is the number of particles)
in reality, wlog one can assume that $v$ is distributed across all axis $x,y,z$, and notice that for every bounce, only one component of the velocity changes ($\Delta p=2mv_{x}$ or sth), which makes $P=\frac{Nm \bar{v^{2}}}{3V}$

because $mv^{2}=3NkT$, one has $P=\frac{NkT}{V}$, 
=> $PV=NkT$, we have $nR=Nk$, and since $N=nN_{A}$, $\boxed{R=N_{A}k}$

we have $P=\frac{F}{S}$, with $\mathbf{F}=\frac{d\mathbf{p}}{dt}$

a new thing is $n_{0}$, the density of gas, calced by $\frac{n}{V}$, then $p=n_{0}kT$
