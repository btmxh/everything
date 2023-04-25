## internal energy
### deg of freedom
see https://www.youtube.com/watch?v=nqGtji3ZjoI, too lazy to describe
- single atom => # of deg = 3
- 2 atoms => # of deg = 5
- \>=3 atoms => # of deg = 6 (ig)

if [[ideal gas]] has $i=3$, $IE=N\frac{3kT}{2}$, we can extend this to if gas has $i$ deg of freedom => avg IE: $IE=iN \frac{kT}{2}$

## van der waals
we have $pV=nRT$, and because atoms has volume we can make 2 modifications to this to make thing more realistic
- decrease $V$ by a factor of $\beta$ (decrease $a$ per mole, then $\beta=na$: cộng tích)
	- (this represent the pushing of atoms)
	- notice that the distance between the center of 2 atoms must not be less than the diameter $d$ of one gas atom (no intersecting spheres) => the actual volume occupied by **two** atom is the volume of the sphere with radius $d$ => $v=\frac{4}{3}\pi d^{3}$ => $N$ atoms will have $v=\frac{2}{3}N\pi d^{3}$ => $\beta=\frac{2}{3}N\pi d^{3}=\frac{16}{3}N\pi r^{3}=4V_{a}$, with $V_{a}$ being the total molecular volume
- increase $p$ by a factor of $\alpha$ (nội áp)
	- (this represent the pulling of atoms)
	- this $\alpha$ is caused by the intermolecular forces acting on the gas atoms
	- we know that 2 atoms will pull each other if they're too near each other, assuming homogeneity, the number of atoms in **one** atom's too-near zone is propto the molecular density $\frac{n}{V}$, to get the entire system's, one need to square => $\alpha \propto \left( \frac{n}{V} \right)^{2}$
- then, one arrives at the van der waals eqn$$
\left( p+a \frac{n^{2}}{V^{2}} \right)(V-nb)=nRT
$$ with $b=4V_{a}$

then, one has $p=\frac{nRT}{V-nb}-a\frac{n^{2}}{V^{2}}$
![[Pasted image 20230425124522.png]]

## isotherm
fixing $T$, one can describe the relationship between $p$ and $V$ as a curve in the $p-V$ space

### critical
the most common crit.pt is the **liquid-vapor** cp, and it's a state of real gases (or real liquid idk), with params $p_{c}, V_{c}, T_{c}$

in this state, for some reason (idk see [[gas#andrew|andrew]] maybe, we have $\frac{\partial p}{\partial V}=\frac{\partial^{2}p}{\partial V^{2}}=0$

one can solve the eqns to get
$$
\begin{align}
T_{c}&=\frac{8a}{27Rb} \\
V_{c}&=3nb \\
p_{c}&=\frac{a}{27b^{2}}
\end{align}
$$

using this, one can calculate $a,b$ by $T_{c}$ and $p_{c}$:
$$
\begin{align}
a&=\frac{27R^{2}T_{c}^{2}}{64p_{c}} \\
b&=\frac{RT_{c}}{8p_{c}}
\end{align}
$$

### analysis
we have $\frac{\partial p}{\partial V}=-\frac{RT}{(V-b)^{2}}+\frac{2a}{V}$, $\frac{\partial^{2}p}{\partial V^{2}}=\frac{2RT}{(V-b)^{3}}-\frac{6a}{V^{4}}$
using desmos (kek) we have:
- $T=T_{c}$ => one inflection point is exactly the critical point (of a graph)
- $T>T_{c}$ => the isother line kinda look like [[ideal gas]]'
- $T<T_{c}$ => the isother line has a convex section and a concave section

## andrew
andrew perform some gaming with $CO_{2}$, which has $T_{c}=304K$
- if $T<T_{c}$, then the graph is like this
- ![[Pasted image 20230425123705.png]]
	- first, as one increase the volume, the pressure increase
	- in BC, there is both liquid and vapor in the thing ("hơi bão hòa", vapor saturation) with dynamic balancing ($\Delta \text{vapor to liquid}=\Delta \text{liquid to vapor}$), and at B, the pressure is saturated ($p_{B}$ is called the vapor saturation pressure)
	- after all of that, it somewhat follow the general rules
	- as $T \to T_{c}$, one will see that $BC\to 0$ and ultimately turned into a singular point, the critical point
	- we also can see by taking $B,C$ of all $T<T_{c}$, one can form a "bell"-like curve (here's the phase diagram of $CO_{2}$)
	- ![[Pasted image 20230425124314.png]]
- if $T>T_{c}$, then there's no liquid, the diagram is similar to [[ideal gas]]

> note: the $BC$ thing does not exist in the van der waals pv thing, due to the fact that that model does not take liquid into account

## joule-thompson
### ie
the internal energy of [[gas]] is $IE=IE_{ideal}+PE$, this [[pe]] is caused by the interaction force field inside the system

this extra $PE$ is the main cause of the **joule-thompson effect**

### le effec
![[Pasted image 20230425130043.png]]
- $M$ is a sponge, i.e. only allowing gas to slowly pass through it => the two regions have different $p$
- now one move the pistons (1 and 2) s.t. every state is a [[balanced state]] and the left region has const pressure $p_{1}$, right region has const $p_{2}$, and this is a [[tprocess#adiabatic|adia]] proc (insulate stuff)
- then, we have $\Delta E_{left}=W_{1}=-p_{1}(0-V_{1})$, $\Delta E_{right}=W_{2}=-p_{2}(V_{2}-0)$ => $\Delta E=p_{1}V_{1}-p_{2}V_{2}$
	- now, if [[ideal gas]], since $\Delta E=nC_{V}\Delta T$ and $pV=nRT$, we have $\Delta E=-nR\Delta T$ => $(C_{V}+R)\Delta T=0$ => no changes in temperature
	- for real gases, $pV\neq nRT$ and $\Delta E$ also depends on other factors (e.g. $p$ because the less pressure there is, the less PE it will have, or more tbh idk)
	- according to van der waals
		- if the internal pressure  represented by $a$ is small, one can let $a=0$ and only care about $b$: responsible for pushing atoms apart. as $V$ inc, the repelling force decrease => $PE$ dec => $KE$ inc => $T$ inc, negative effect
		- if $b=0$, as $V$ inc similarly $T$ dec, positive effect
- effect
	- the effect's primary goal is to change the temperature of the gas, it's mostly used to cool down => **positive effect** is when $T_{2}<T_{1}$, and **negeffect** is the opposite, if $T_{2}=T_{1}$, it's called "điểm đảo", which forms the "đường cong đảo"
	- the result of the effect depends on $p$, $V$ and $T$. fixing $V$, one can represent on the $p-T$ graph where the effect is pos, neg and zero
	- ![[Pasted image 20230425133208.png]]

the main usage of this thing is to freeze gases, thus turning them into liquid
if the gases are in a negeff state, one must make them poseff, by lowering their temperature