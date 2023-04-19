consider an object $V$ with mass density at position $\mathbf{r}$ to be $\rho(\mathbf{r})$, then the center of mass is the point $\mathbf{r_{0}}=\frac{1}{m}\int _{V} \rho(\mathbf{r})\mathbf{r} \, dV$, where $m$ is the actual mass of $V$: $m=\int_{V} \rho(\mathbf{r}) \, dV$

in the discrete case, $\rho(\mathbf{r})=m_{i}\delta(\mathbf{r}-\mathbf{r_{i}})$, where $\delta$ is the dirac delta, one has $\mathbf{r_{0}}=\frac{1}{m}m_{i}\mathbf{r_{i}}$, or in coord-free form: $m_{i}\vec{\mathbf{r_{i}r_{0}}}=0$

## velocity
if a rigid body was moving with **velocity** at some time $t$ $\mathbf{v}(\mathbf{r})$, then the center of mass $\mathbf{\mathbf{r_{0}}}$ will also move, and $\frac{d\mathbf{r_{0}}}{dt}=\frac{1}{m}\frac{d}{dt}\int _{V} \rho(\mathbf{r})\mathbf{r} \, dV=\frac{1}{m}\int _{V} \rho(\mathbf{r})\frac{d\mathbf{r}}{dt} \, dV=\frac{1}{m}\int _{V}\rho(\mathbf{r})\mathbf{v} \, dV$ (assuming that $\rho(\mathbf{r})$ is const, since the mass is also moving)

## momentum
hence, if one use the center of mass to calc the [[momentum]], $\mathbf{p}=m\frac{d\mathbf{r_{0}}}{dt}=\int _{V} \rho(\mathbf{r})\mathbf{v} \, dV$. since $\rho dV=dm$m $\mathbf{v}dm=dp$ ($\mathbf{v}$ const), one have $\mathbf{p}=\int _{V}d\mathbf{p(\mathbf{r})}$, i.e. $\mathbf{p}$ is the sum of all infinitesimal momentum $d\mathbf{p}(\mathbf{r})$, or in the discrete case:
> the sum of [[momentum]] of the system = the momentum of a [[point mass]] at the c.o.m, with mass = system mass, velocity = velocity of c.o.m

=> the c.o.m. can repr the system as a [[point mass]] in some cases

## accel & force
do one more diff., one can see that the acceleration of c.o.m. is $\mathbf{a_{0}}=\frac{1}{m}\int _{V} \, d\mathbf{F}$, where $\mathbf{F}$ is the force [[field]] of the object => we can rewrite this like the [[newton's law#second law|2nd law]] by defining the net force $\mathbf{F_{0}}=\int _{V} \, d\mathbf{F} \implies \mathbf{F_{0}}=m\mathbf{a_{0}}$

=> the c.o.m. moves like a [[point mass]] with the mass = system mass, force = sum of all external forces


