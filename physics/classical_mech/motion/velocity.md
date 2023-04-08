## avg velocity
consider a [[point mass]] $M(m, \mathbf{r})$, and two moment in time $t_{1}$ and $t_{2}$
now let $s$ be the [[arc length param.]] of $\mathbf{r}$
then, the **avg velocity** between these two moments are
$$
\boxed{
\overline{v}=\frac{\Delta s}{\Delta t}=\frac{s(t_{2})-s(t_{1})}{t_{2}-t_{1}}
}
$$
**meanings:** $\overline{v}$ repr how the average speed of the movement of the object between those periods of time

## inst. velocity
as $t_{2}$ approaches $t_{1}$, the avg velocity approaches a limit, called the **inst. velocity** of the object at $t_{1}$ (now it doesn't depend on $t_{2}$)
$$
\boxed{
v=\lim_{ \Delta t \to 0 } \frac{\Delta s}{\Delta t} = \frac{ds}{dt}
}
$$
**meanings:** the sign of $v$ indicates the direction of motion
- $v>0$ => object follows the *positive* direction of the [[arc length param.]] $s$
- $v<0$ => object follows the *negative* direction of the [[arc length param.]] $s$
- $|v|$ repr how fast/slow the object was moving

## velocity vector
the velocity vector is a vector $\mathbf{v}$ that satisfies:
- p-direction: [[tangent]] to the orbit
- c-direction: the direction of motion
- magnitude: the abs of inst. velocity: $|\mathbf{v}|=|v|=| \frac{ds}{dt}|$

> the direction of a vector already encompasses where it was heading, but my beloved prof. split that information in two parts
> 1. **phương của vectơ**, we'll call it p-direction: the line that passes through the origin which is parallel to the vector
> 2. **chiều của vectơ**, we'll call it the c-direction: decide which "half" of the line the vector should align itself with

then, one can define the *arc differential* $d\mathbf{s}$
- p-dir: [[tangent]] to the orbit
- c-dir: direction of motion
- magnitude: $|d\mathbf{s}|=|ds|$

**theorem:** $\mathbf{v}=\frac{d\mathbf{s}}{dt}$
proof: use the definitions

**fundamental theorem of motion:** $\mathbf{v}=\frac{d\mathbf{r}}{dt}$
denote $\mathbf{r'}$ by $\frac{d\mathbf{r}}{dt}$
then, by the *rough def* of the [[tangent]], $\mathbf{v}$ and $\mathbf{r}'$ has the same p-dir
since $ds=|d\mathbf{r}|$ => $|\mathbf{v}|=|\frac{ds}{dt}|=\left|\frac{||d\mathbf{r}||}{dt}\right|=\left\| \frac{d\mathbf{r}}{dt} \right\|=\|r'\|$
=> $\mathbf{v}$ and $\mathbf{r'}$ has the same mag.
the two vecs also share the same c-dir, it follows from the definition of the "direction of motion" ^a7c26c

**corollary**: when $\mathbf{r}(t)=(x(t),y(t),z(t))$, the velocity $\mathbf{v}(t)=\mathbf{r}'(t)=(x'(t),y'(t),z'(t))$ => $|v(t)|=\sqrt{ \left( \frac{dx}{dt} \right)^{2}+\left( \frac{dy}{dt} \right)^{2}+\left( \frac{dz}{dt} \right)^{2} }$

the [[unit]] of velocity is $LT^{-1}$, in SI: m/s

**NOTE:** $v$ is not simply the magnitude of $\mathbf{v}$, but rather a value that satisfies: $\boxed{\mathbf{v}=v\mathbf{\hat{r}}'}$




