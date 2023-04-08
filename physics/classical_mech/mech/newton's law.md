## first law
- *isolated*: not affected by any outside forces
- $L_{1}$: "a isolated [[point mass]] will continue to be static if it was static, will follow straight uniform motion if it was moving"
- $L_{1}$ is only true in a special class of [[frame of ref]]s: [[inertial frame of ref]]s
- to be more rigorous: **axiom 1: in classical mechanics, the set of [[frame of ref]] that $L_{1}$ stays true in is non-empty, elements of which are called [[inertial frame of ref]]**

> $L_{1}$ is called the first law, but it does not necessarily have to be true (no one states that "laws" should be always true), but the above **axiom 1** is a "mathematical axiom", which is considered to be always true (in the scope of classical mechanics at least)

**theorem:** let $O_{1}$ and $O_{2}$ are two [[frame of ref]], assuming $O_{1}$ is [[inertial frame of ref|inertial]], then $O_{2}$ has const [[velocity]] wrt $O_{1}$ [[frame of ref]] iff $O_{2}$ is another [[inertial frame of ref]]

**theorem:** a [[frame of ref]] that's attached to an isolated object is an [[inertial frame of ref]]
(this doesn't prove the existence of [[inertial frame of ref]]s, since there is no concept of an isolated object in real life)

**proof**: see [[relative]]

## second law
- $L_{2}$: "motion of a [[point mass]] that's affected by many forces with the net force $\mathbf{F}\neq 0$ is a motion with acceleration. that acceleration is proportional to the force and the inverse of its mass"
$$
\boxed{\mathbf{a}=\frac{\mathbf{F}}{m}}
$$
- once again, $L_{2}$ only holds true in [[inertial frame of ref]]s
- its equivalent form: $\boxed{\mathbf{F}=m\mathbf{a} \iff \mathbf{F}=m \frac{d^{2}\mathbf{r}}{dt^{2}}}$ is called the elementary equation of Newtonian mechanics

- like [[accel.]], one can decompose $\mathbf{F}$ into two parts: the [[tangent]] force $\mathbf{F_{t}}$ and the [[normal]] force $\mathbf{F_{n}}$, by $\mathbf{F_{n}}=m\mathbf{a_{n}}$ and $\mathbf{F_{t}}=m\mathbf{a_{t}}$

## third law
- $L_{3}$: "when object A exert a force $\mathbf{F}$ to object B, object B would also exert another force $\mathbf{F'}=-\mathbf{F}$ on object A"
- this law holds in all [[frame of ref]]
- in a system of objects that's isolated (i.e. only inside forces are present), denote $\mathbf{F}_{i,j}$ be the interaction force between object $i$ and object $j$, then it follows from $L_{3}$ that: $\mathbf{F}_{i,j}=-\mathbf{F}_{j,i} \implies \sum_{i,j}\mathbf{F}_{i,j}=0$ => **the sum of all inside forces is zero**
