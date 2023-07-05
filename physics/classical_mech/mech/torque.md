the torque of a [[force]] on sth wrt an origin point $O$ is defined as
$$
\mu_{/O}(\mathbf{F})=\mathbf{r}\times \mathbf{F}
$$
one can decompose $\mathbf{F}$ into two components: $\mathbf{F}=\mathbf{F_{t}}+\mathbf{F_{n}}$, where $\mathbf{F_{n}}$ always points to $O$ => $\mathbf{F_{n}}\perp$ plane of rotation => $\mu(\mathbf{F}) = \mu(\mathbf{F_{t}})=\pm rF_{t}$

the torque is a pseudovector, with
- p-dir: dir of the rotation axis
- c-dir: $(\mathbf{r}, \mathbf{F}, \mu)$ is positively-oriented
- $|\mu|=rF\sin\alpha=rF_{t}$

> one can also define the [[torque]] wrt an axis $\Delta$, then one must remove the parallel component $\mathbf{F_{n}}$ from $\mathbf{F}$: $\mu_{/\Delta}(\mathbf{F})=\mathbf{r}\times(\mathbf{F}-\mathbf{F_{n}})$

## geometric algebra approach

- one can define [[torque]] as [[work]] per unit angle, i.e. $\frac{dW}{d\theta}$
- consider a 3d rotation on a 2d plane: $\mathbf{r}=r(\mathbf{\hat{u}}\cos \theta+\mathbf{\hat{v}}\sin \theta)=r\mathbf{\hat{u}}(\cos \theta+\mathbf{i}\sin \theta)=r\mathbf{\hat{u}}e^{ \mathbf{i}\theta }$, where $\mathbf{i}=\mathbf{\hat{u}}\mathbf{\hat{v}}$ is an unit bivector that repr the plane of rotation
- then $\tau=\frac{dW}{d\theta}=\frac{\mathbf{F}\cdot d\mathbf{r}}{d\theta}=\mathbf{F}\cdot(r\mathbf{\hat{u}}\mathbf{i}e^{ \mathbf{i}\theta })=\mathbf{F\cdot(\mathbf{ri})}$
- in general, $\mathbf{F}$ may not lie on $\mathbf{i}$ => we need to replace $\mathbf{F}$ in the above expr by its projection onto $\mathbf{i}$, i.e. 
