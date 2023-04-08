## time and space in classical mech
- consider two coordinate system with their own [[frame of ref]] $Oxyz$, $O'x'y'z'$
- then according to newton:
	- time is absolute
		- time in the two [[frame of ref]] is the same: $t=t'$
	- space is relativistic
		- assuming $OO'$ aligns with the $Ox$ and all the axes of the two f.o.r coincident, then one can derive the equations
		- $x=x'+\overline{OO'}$
		- $y=y'$
		- $z=z'$
		- or in vector form $\boxed{\mathbf{r}=\mathbf{r'}+\vec{OO'}}$
	- however, *space interval* is absolute: $\Delta x= x_{1}-x_{2}=(x_{1}'-\overline{OO'})-(x_{2}'-\overline{OO'})=x_{1}'-x_{2}'=\Delta x'$
- therefore, one can use [[galilean transformation]] to go from a [[frame of ref]] to another

## [[velocity]] and [[accel.]]
we have $\mathbf{r}=\mathbf{r'}+\vec{OO'}$
then $\frac{d\mathbf{r}}{dt}=\frac{d\mathbf{r'}}{dt}+\frac{d\vec{OO'}}{dt}$, the same goes for the second derv.
=> $\mathbf{v}=\mathbf{v'}+\mathbf{V}$ and $\mathbf{a}=\mathbf{a'}+\mathbf{A}$

## [[newton's law]]
consider a [[inertial frame of ref]] $O$ and another [[frame of ref]] $O'$
we will prove the theorems presented in the [[newton's law#first law|first law]] section
**theorem:** let $O_{1}$ and $O_{2}$ are two [[frame of ref]], assuming $O_{1}$ is [[inertial frame of ref|inertial]], then $O_{2}$ has const [[velocity]] wrt $O_{1}$ [[frame of ref]] iff $O_{2}$ is another [[inertial frame of ref]]

**proof**
consider a point mass moving with const [[velocity]] $\mathbf{v}$ in $O_{1}$, then
- if $O_{2}$ is [[inertial frame of ref|inertial]], it must moves with const [[velocity]] $\mathbf{v'}$ in $O_{2}$ (first law), then by $\mathbf{v}=\mathbf{v'}+\mathbf{V}$ => $\mathbf{V}$ must be const
- if $O_{2}$ has const [[velocity]] wrt $O_{1}$, then by $\mathbf{v}=\mathbf{v'}+\mathbf{V}$, $\mathbf{v'}$ must be const => that point mass has const [[velocity]] wrt $O_{2}$ => all point masses has const [[velocity]] in $O_{1}$ will have const [[velocity]] in $O_{2}$ => $O_{2}$ is [[inertial frame of ref|inertial]]

**theorem:** a [[frame of ref]] that's attached to an isolated object is an [[inertial frame of ref]]
**proof**
consider a [[frame of ref]] $O'$ with $O'$ being the position of an isolated object
we'll prove that this [[frame of ref]] satisfies the first law
now let $O$ be an [[inertial frame of ref]], then since $O'$ is attached with an isolated object, therefore moving with a const [[velocity]] w.r.t $O$, thus $O'$ must also be an [[inertial frame of ref]]

the second law is *well-defined*, and therefore $L_{2}$ is true for all [[inertial frame of ref]]
- present:
	- an [[frame of ref]] that moves with const [[velocity]] wrt an [[inertial frame of ref]] is [[inertial frame of ref|inertial]]
		- (mọi hqc ch động th đều vs 1 hqc q tính cũng là 1 hqc q tính)
	- all mechanical equations are consistent in all [[inertial frame of ref]]s
		- (các pt động lực học trong các hqc q tính có dạng như nhau)
	- all mechanical laws are consistent in all [[inertial frame of ref]]s
		- (các đl cơ học đều xảy ra như nhau trong những hqc q tính)

## fictitious force
consider an [[inertial frame of ref]] $O$ and another non-[[inertial frame of ref]] $O'$
if $O'$ moves with [[accel.]] $\mathbf{A}$ wrt $O$, then from $\mathbf{a}=\mathbf{a'}+\mathbf{A}$, we have $m\mathbf{a}=m\mathbf{a'}+m\mathbf{A} \implies m\mathbf{a'}=\mathbf{F}-m\mathbf{A}$ (1)
now, we imagine that there is another force: the **fictitious force** (lực quán tính) $\mathbf{F}_{fict}=-m\mathbf{A}$, then the true net force in $O'$ is $\mathbf{F'}=\mathbf{F}+\mathbf{F}_{fict}=m\mathbf{a'}$
therefore, the elementary equation of mechanics still holds for non-[[inertial frame of ref]]s:
$$
\boxed{m\mathbf{a}=\mathbf{F}+\mathbf{F}_{fict}=\mathbf{F'}}
$$
the fictitious force $\mathbf{F}_{fict}$ is
- an imaginary force, only exists in non-[[inertial frame of ref]]
- always have the opposite direction with the [[accel.]] vector $\mathbf{A}$
- magnitude: $\|\mathbf{F}_{fict}\|=m\|\mathbf{A}\|$

if $O'$ is moving in a circular motion wrt $O$, then in the simplest case (uniform motion), the fictitious force is called the **centrifugal force** (lực li tâm, lực quán tính li tâm), simply calculated using: $F_{ctr}=\frac{mv^{2}}{r}$

e.g. classical elevator problem
- if the elevetor is accelerating with [[accel.]] $\mathbf{A}$, then in the non-[[inertial frame of ref]] of the elevator, consider a point mass $m$, which was affected by the normal [[force]] and [[gravity]] we have: $m\mathbf{a'}=\mathbf{F_{g}}+\mathbf{F_{n}}+\mathbf{F_{fict}} \implies \mathbf{F_{n}}=m(\mathbf{a'}+\mathbf{A}-\mathbf{g})$
- if the object is static in the elevator [[frame of ref]], i.e. $\mathbf{a'} = 0$, then $\mathbf{F_{n}}=m(\mathbf{A}-\mathbf{g})$
- let $\mathbf{e_{1}}$ be the unit vector that points downwards, then $\mathbf{g}=g\mathbf{e_{1}}$
	- if it was accelerated upwards, $\mathbf{A}=-A\mathbf{e_{1}}$, then $\mathbf{F_{n}}=-m(A+g)\mathbf{e_{1}}$, which points downwards and has higher magnitude than the usual normal force that's equal to $mg$ => $m$ felt heavier
	- otherwise, we have $\mathbf{F_{n}}=-m(g-\mathbf{A})\mathbf{e_{1}}$, which means that bla bla bla $m$ felt lighter

