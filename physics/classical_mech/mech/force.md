in classical mechanics, there are 2 kinds of forces
- field forces: like gravity and electromagnetic forces
- contact forces: normal, friction, etc.

## field forces
field forces, despite their funny calc 2 bullcrap, are straightforward
they propagate through a field (vector field) and use the language of field theory to describe their behavior

there are 2 kinds of field forces (ignoring the funny nuclear forces that can only be described by quantum shitposting)
- [[gravity]]
- [[electromagnetic]]

## contact forces
contact forces, at first glance, are easy to understand
but they are not
they are the embodiment of "dude, trust me bro" and "source is that i made the fuck up" in classical mechanics
ill try to make them more mathematical and rigorous i guess

according to the [[newton's law#third law|third law]], when object $A$ exert a force $\mathbf{F}$ on object $B$, object $B$ will exert another force $\mathbf{F'}=-\mathbf{F}$ on object $A$ => this force $\mathbf{F'}$ can be decomposed into two forces: $\mathbf{F_{n}}$: the normal force and $\mathbf{F_{fric}}$ the friction force

### normal
the normal force $\mathbf{F_{n}}$ is the projection of $\mathbf{F'}$ on the [[normal]] direction of object $B$ at the point of contact
![[Pasted image 20230408191044.png]]
=> $\mathbf{F_{n}}=(\mathbf{F'}\cdot \mathbf{\hat{n}})\mathbf{\hat{n}}$
(here, we assume that object $B$ has a [[surface]], therefore making the [[normal]] space has dim 1)

### friction
friction $\mathbf{F_{fric}}=\mathbf{F'}-\mathbf{F_{n}}$ is the remaining force

### relationship
we starts from this inequality
$$
F_{fric}\leq\mu F_{n}
$$
where $\mu$ is the coeff. of friction (depending only on the kind of surfaces)

we'll derive the more general form of that (in vector language)
let $\mathbf{\hat{v}}$ be the unit velocity vector, $\mathbf{F_{n}}$ be the normal force vector
then one can write $\mathbf{F_{fric}}=-\alpha\mu F_{n}\mathbf{\hat{v}}$, with $\alpha \in [0,1]$
equality of the above ineq. holds when the object is moving (friction will try to stop the motion with all its might), i.e. $\mathbf{\hat{v}} \neq 0$, therefore, one can replace $\alpha \mathbf{\hat{v}}$ with $\mathbf{\hat{v}}$, with an additional condition that $\mathbf{\hat{v}}=0$ if the object is static (it's now no longer an *unit* velocity vector, and it has become discont.)

therefore, we have the equation of friction
$$
\boxed{\mathbf{F_{fric}}=-\mu F_{n}\mathbf{\hat{v}}}
$$

e.g. describe a motion of a box of mass $m$ on a ramp
[[Drawing 2023-04-08 20.14.15.excalidraw]]
![[Pasted image 20230408202108.png]]
with
- $\alpha$ is the ramp angle
- $\mu$ is the coeff of friction

initially, there is only gravity $\mathbf{F_{g}}$ that acts on $m$
then, it exert a force on the ramp (which may not be $\mathbf{F_{g}}$) => it's now affected by another force $\mathbf{F'}=\mathbf{F_{frict}}+\mathbf{F_{n}}$
then, we have: $\mathbf{F_{frict}}=-\mu F_{n}\mathbf{\hat{v}}$
using the [[newton's law#second law|2nd law]], we have $m\mathbf{a}=\mathbf{F_{frict}}+\mathbf{F_{n}}+m\mathbf{g}$
set up the coord sys $=\{ \mathbf{e_{1}}, \mathbf{e_{2}} \}=$ like the figure, then
- $\mathbf{F_{n}}=F_{n}\mathbf{e_{2}}$
- $\mathbf{F_{frict}}=-\mu F_{n}sgn(v)\mathbf{e_{1}}$ ($sgn(x)=1$ if $x>0$, $0$ if $x=0$ and $-1$ otherwise)
- $\mathbf{F_{g}}=mg(\mathbf{e_{1}}\cos\alpha-\mathbf{e_{2}}\sin \alpha)$
then, we have $\boxed{m\mathbf{\dot{v}}=(mg\cos \alpha-\mu F_{n}sgn(v))\mathbf{e_{1}}+(F_{n}-mg\sin\alpha)\mathbf{e_{2}}}$
we will assume that $\mathbf{a}, \mathbf{v}$ are parallel to $\mathbf{e_{2}}$ (it can't fly to the sky or penetrate into the ramp), which is reasonable but tbh i kinda want to prove that using this mathematical framework (but i can't).
then $F_{n}=mg\sin\alpha$ and $\mathbf{\dot{v}}=(g\cos\alpha-\mu g\ sgn(v)\sin\alpha )\mathbf{e_{1}}$, or in the scalar form, $\dot{v}=g(\cos\alpha-\mu sgn(v)\ \sin \alpha)$
now's the funny part
- case 1: $\cot \alpha > \mu$
	- then $\dot{v}>0$ => the object will starts to move => $sgn(v)=1$ for all $t>0$
	- then we will have $\dot{v}=g(\cos\alpha-\mu \sin\alpha)$, this is the acceleration of the object
- case 2: $\cot \alpha < \mu$
	- if at any moment $v\neq0$, then $\dot{v}<0$ and the motion will slow down => it can be thought of as in a "harmonic" state, however, due to the discont. nature of $sgn(v)$, the "period" is 0, therefore the motion is static
	- the motion is something like this
		- at $t=0$, $v=0, \dot{v}>0$ => it will speed up
		- at $t=\varepsilon_{1}$, $v>0, \dot{v}<0$ => it will slow down
		- at $t=\varepsilon_{1}+\varepsilon_{2}$, $v=0, \dot{v}>0$ => it will speed up (note: $v$ can't be less than 0)
		- ...
		- the numbers $\varepsilon_{1}, \varepsilon_{2}$ are "infintesimals", therefore one can consider the motion to be static

**conclusion:**
- from the above problem, we can conclude that our model for friction is still stupid, but the fact that classical mechanics failed in the quantum scale is not a coincidence
- the *more correct* model of friction should also depends on other factors, but no professors talks about that crap in physics 1 (skill issue tbh)
- unlike the mid l bozo model of physics 1, we can derive differential equations and solve them to get our motions (truly a W and gaming experience)
- we also have to assume less (we can "prove" that the box won't go up the ramp for some reason, unlike physicists who just said "obviously it won't go up are you braindead?" kekw)
- lesson: "dude trust me bro" and "source: i made it the fuck up" can't be turned into rigorously definitions and laws xd

**"theorem"**: if $\dot{v}<0$ if $v \neq 0$ and $\dot{v}>0$ if $v=0$, then the motion is considered "*unstable*" and will result in static motion ($v=0$)

e.g. the wood piece is "sandwiched" between to plate with $\mu=0.2$
given the pressure force (the wood piece acts on each plate) is $\mathbf{F_{pr}}$ and gravity $\mathbf{F_{p}}$
to move the piece up/downwards, how much force must be exerted?
![[Pasted image 20230408210750.png]] ![[Pasted image 20230408211500.png]]

- let the exerted force by $\mathbf{F}=F\mathbf{e_{1}}$ (in the figure's case, $F<0$)
- similarly we take $v$ by $\mathbf{v}=v\mathbf{e_{1}}$, but we are sure that $F_{p}>0$
- skipping the vector part, then $m \dot{v}=F_{p}-2\mu F_{pr}sgn(v)+F$
- we will consider the "stability" of this motion:
	- if $v>0, sgn(v)=1$, then $m \dot{v}=F_{p}-2\mu F_{pr}+F$ (1)
	- if $v=0, sgn(v)=0$ then $m \dot{v}=F_{p}+F$ (2)
	- if $v<0, sgn(v)=-1$ then $m \dot{v}=F_{p}+2\mu F_{pr}+F$ (3)
- by hypothesis, the object was initially static, which means that when $F=0$, the motion is unstable, then RHS(2) is positive, therefore RHS(1) must be non-positive, i.e. $F_{p}\leq 2\mu F_{pr}$ (in the original exercise, $F_{p}=49N, F_{pr}=147N$, this is true)
- now we will investigate the two cases:
	- if $F>0$ (pull the thing down), then RHS(2) is still positive, and now we need RHS(1) > 0, or $F\geq 2\mu F_{pr}-F_{p}$
	- if $F<0$ (sth the thing up), then RHS(1) is negative and we have another 2 cases:
		- RHS(2) is non-negative => unstable => no motion
		- RHS(2) is negative => $v$ will have negative sign => the motion will go to the (3) state. to make it stable we need RHS(3) is negative, or $F\geq-F_{p}-2\mu F_{pr}$, or $|F|\geq 2\mu F_{pr}+F_{p}$

### tension
if you thought friction is already funny, oh no no no no
in a beautiful day, mr streamer decided to kill himself and hang himself (let's gooooooo)
instead of cheering (even though celebrating my death is never enough), let's dive in the physics of me dying xddddd
![[Pasted image 20230408214915.png]]

now, for the 2 people who finds myself joking about my death offensive (maybe quite an overexaggeration, denote $m$ my body. $m$ has a force of gravity pulling it downwards: $m\mathbf{g}$, but its [[accel.]] is still zero => there must be another force: the tension that was balancing gravity

to understand tension, we will look at the microscopic scale, the rope can be considered to be a line of atoms that bonds with each other, the tension can be considered the bonding force between atoms
![[Pasted image 20230408222127.png]]
the object will pull the lowest atom downwards, then the bonding force will propagate that force to the ceiling

you can also say that **I DON'T HAVE ANY IDEA HOW TO MODEL THIS FORCE** XDDDDDDDDDDDDDDD

e.g.1. the blob want to go up/down (aka accelerate the platform) using a pulley system. know the sum of the blob and the platform's mass and the system's acceleration, calc the tension force

- i want to kms
- if the rope is not connected to a pulley system, then the man can still climb up, since the tension force acted on him
- if he does not climb up, and someone else pull the thing for him, then the tension force would still act on him
- in this case, the tension force **acted twice** on the blob-platform system, then
	- $M(g+a)=2F_{t} \implies F_{t}=\frac{M(g+a)}{2}$
- TODO: deliver a more convincing argument for why it acts twice

e.g. man (mass $m$) climbing a rope on a pulley to lift an object of mass $M$ with acceleration $a$ wrt rope => $M$ was lifted with [[accel.]] $a_{2}$. calc $a$ by $a_{2}$
![[Pasted image 20230410125502.png]]
- when the man climb the rope, the tension force $F_{t}$ can be considered the force that's responsible for the action of climbing => the rope got pulled down by a force $-F_{t}$ => ended up lifting up $M$ by a force $F_{t}$
- by [[newton's law#second law|2nd law]], we have
	- $ma_{1}=F_{g_{1}}+F_{t}=mg+F_{t} \implies a_{1}=g+\frac{F_{t}}{m}$
	- $Ma_{2}=F_{g_{2}}+F_{t}=Mg+F_{t} \implies a_{2}=g+\frac{F_{t}}{M}$
- $a=a_{1}+a_{2}=2g+F_{t}\left( \frac{1}{m}+\frac{1}{M} \right)$ is the [[accel.]] of $m$ wrt rope
- we have $a_{2}=g+\frac{F_{t}}{M}\implies F_{t}=M(a_{2}-g)$
- then $a=2g+F_{t}\left( \frac{1}{m}+\frac{1}{M} \right)=2g+M(a_{2}-g)\left( \frac{1}{m}+\frac{1}{M} \right)=\left( 1-\frac{M}{m} \right)g+\left( 1+\frac{M}{m} \right)a_{2}$
- to lift the object, i.e. $a_{2}\leq0 \implies a\leq\left( 1-\frac{M}{m} \right)g$, or in magnitude form (case $M>m$), $|a|\geq\left( \frac{M}{m}-1 \right)g$