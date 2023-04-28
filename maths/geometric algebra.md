the superior way to do vector stuff
see here: https://www.youtube.com/watch?v=60z_hpEAtD8

## proj. motion model
start with $\mathbf{s}=\mathbf{v_{0}}t+\frac{1}{2}\mathbf{g}t^{2}$, let $\mathbf{\hat{x}}, \mathbf{\hat{y}}$ be the basis vectors of the motion plane and $\mathbf{i}=\mathbf{\hat{x}}\mathbf{\hat{y}}$
- when is $y$ max?
	- when $y$ max, $\frac{dy}{dt}=0$, i.e. $\mathbf{v}\cdot \mathbf{\hat{y}}=0$
	- sub $\mathbf{v}=\mathbf{v_{0}}+\mathbf{g}t$ and $\mathbf{g}=-g\mathbf{\hat{y}}$, one have $\mathbf{v_{0}}\cdot \mathbf{\hat{y}}-g\mathbf{\hat{y}}^{2}t=0\implies t=\frac{\mathbf{v_{0}}\cdot \mathbf{\hat{y}}}{g}=\mathbf{v_{0}}\cdot \mathbf{g}^{-1}$
	- sub that back => $\mathbf{s}=\mathbf{v_{0}}t+\frac{1}{2}\mathbf{g}t^{2}=t(\mathbf{v_{0}}\cdot \mathbf{\hat{x}})\mathbf{\hat{x}}+t(\mathbf{v_{0}}\cdot \mathbf{\hat{y}})\mathbf{\hat{y}}-\frac{1}{2}gt^{2}\mathbf{\hat{y}}$$=(\mathbf{v_{0}}\cdot \mathbf{\hat{x}})t\mathbf{\hat{x}}+gt^{2}\mathbf{\hat{y}}-\frac{1}{2}gt^{2}\mathbf{\hat{y}}=(\mathbf{v_{0}\cdot \mathbf{\hat{x}}})t\mathbf{\hat{x}}+\frac{1}{2}g\left( \frac{\mathbf{v_{0}}\cdot \mathbf{\hat{y}}}{g} \right)^{2}\mathbf{\hat{y}}$$=\frac{(\mathbf{v_{0}}\cdot \mathbf{\hat{x}})(\mathbf{v_{0}}\cdot \mathbf{\hat{y}})}{g}\mathbf{\hat{x}}+\frac{(\mathbf{v_{0}}\cdot \mathbf{\hat{y}})^{2}}{2g}\mathbf{\hat{y}}$
- without the inclusion of coord axes, one can do
	- $0=\mathbf{s}\wedge\mathbf{s}=t\left( \mathbf{v_{0}}+\frac{1}{2}\mathbf{g}t \right)\wedge\mathbf{s}$
	- hence, if $t\neq 0$, $\mathbf{v_{0}}\wedge\mathbf{s}=\frac{1}{2}t\mathbf{s}\wedge\mathbf{g}$
	- one can solve for $t$ by: $t=\frac{2\mathbf{v_{0}}\wedge\mathbf{s}}{\mathbf{s}\wedge\mathbf{g}}=\frac{\mathbf{v_{0}\wedge\mathbf{\hat{s}}}}{\mathbf{\hat{s}}\wedge\mathbf{g}}$
	- the bivec mul part only depends on the direction of surface $\mathbf{\hat{s}}$ (representing $\mathbf{x_{0}}$), the inital velocity $\mathbf{v_{0}}$ and the gravitational accel. $\mathbf{g}$ (representing $\mathbf{y_{0}}$).
	- to get even more info from this, one wedges $\mathbf{s}$ with another vector: $\mathbf{s}\wedge\mathbf{g}=t\mathbf{v_{0}}\wedge\mathbf{g}$ => $s=t\frac{\mathbf{v_{0}}\wedge\mathbf{g}}{\mathbf{\hat{s}}\wedge\mathbf{g}}=\frac{2(\mathbf{v_{0}}\wedge\mathbf{\hat{s}})(\mathbf{v_{0}}\wedge\mathbf{g})}{(\mathbf{\hat{s}}\wedge\mathbf{g})^{2}}$
e.g. calc $s$ for $\mathbf{v_{0}}=5\mathbf{\hat{x}}e^{ i\pi/6 },\mathbf{g}=-10\mathbf{\hat{y}},\mathbf{\hat{s}}=\mathbf{\hat{x}}$
- we have $\mathbf{v_{0}}=\frac{5}{2}(\sqrt{ 3 },1), \mathbf{\hat{s}}=(1,0),\mathbf{g}=(0,-10)$
- then $\mathbf{v_{0}}\wedge\mathbf{\hat{s}}=-\frac{5}{2}\mathbf{i}, \mathbf{v_{0}} \wedge\mathbf{g}=-25\sqrt{ 3 }\mathbf{i}, \mathbf{\hat{s}}\wedge\mathbf{g}=-10\mathbf{i}$
- => $s=\frac{2\left( -\frac{5}{2} \right)(-25\sqrt{ 3 })\mathbf{i^{2}}}{(-10\mathbf{i})^{2}}=\frac{5\sqrt{ 3 }}{4}\approx2.165$
- verify: $s=\frac{5^{2}\sin\frac{\pi}{3}}{10}=\frac{5\sqrt{ 3 }}{4}$ true

e.g. when is the range max? ($v_{0}$ fixed)
we have $2(\mathbf{v_{0}\wedge\mathbf{\hat{s}}})(\mathbf{v_{0}}\wedge\mathbf{g})=v_{0}^{2}\mathbf{g}\cdot \mathbf{\hat{s}}-\mathbf{g}\cdot(\mathbf{v_{0}\mathbf{\hat{s}}\mathbf{v_{0}}})$
- the first term is const, but the second term is the inner product between $\mathbf{g}$ and $\mathbf{v_{0}}\mathbf{\hat{s}}\mathbf{v_{0}}$, which is the reflection of $\mathbf{\hat{s}}$ along $\mathbf{v_{0}}$
- to make the range max, one needs $\mathbf{g}$ and the reflection vector to have opposing direction, this only happens when $\mathbf{v_{0}}$ is the angle bisector of the angle made of 2 vectors $\mathbf{\hat{s}}$ and $-\mathbf{g}$
![[Pasted image 20230419113713.png]]
