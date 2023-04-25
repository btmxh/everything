a fn to model [[mech wave]] and [[light]]
assuming that the wave is $y=A\cos \omega t$ at the wavesrc
after $t$ time, the wave travelled a dist. of $vt$ => pts with $x=vt$ is now at its peak => $y=A\cos \omega\left( t-\frac{x}{v} \right)$

we have $\frac{\omega}{v}=\frac{\tau f}{v}=\frac{\tau}{\lambda}$ and $\omega=\frac{\tau}{T}$ => $y=A\cos \tau\left( \frac{t}{T}-\frac{x}{\lambda} \right)=A\cos \tau(ft-\tilde{v}x)$, with $\tilde{v}=\frac{1}{\lambda}$

the most convenient form is arguably $y=A\cos(\omega t-kx)$, with $k=\frac{2\pi}{\omega}$
or in complex form $x=\mathrm{Re}(z), z=Ae^{ -i\omega t }e^{ ikx }$

one can also use $\mathbf{k}$ and replace $kx$ by $\mathbf{k}\cdot \mathbf{r}$

=> wavefn is periodic wrt both time (period $T$) and space (period $\lambda$)

## diminishing
in general, $A$ will also depend on $x$
e.g. assuming sphere wave propagate uniformly and energy is conserved, find wave fn
- since the propagation is uniform => it follows the inverse square law => wave energy at $E(r) \propto \frac{1}{r^{2}}$
- since $E(x) \propto A^{2}$,we have $A(x)=\frac{k}{x}$ => wavefn $y(x,t)=\frac{kA}{x}e^{ -i\omega t }e^{ ikr }$ (yes it seems that the two $k$ are the same thing)

## wave eqn
in general, waves satisfy the wave eqn: $\Delta \psi=\frac{1}{v^{2}} \frac{\partial^{2} \psi}{\partial t^{2}}$, with $\Delta$ being the [[laplacian]]

## wave [[energy]]
the energy is divided into [[ke]] and [[pe]]
in a large area, one can approximate $KE \approx PE$ (since $KE=\dots \cos(\dots), PE=\dots \sin(\dots)$)
we have $KE=\iiint_{V} \frac{1}{2}y'^{2}dm$, so $E=\iiint_{V} y'^{2}dm$, and since $y'=-A\omega\sin(\omega t-kx)$, $dE=A^{2}\omega^{2}\sin ^{2}(\omega t-kx)dm$

the **energy density** (energy / volume) is $w=\frac{dE}{dV}=\rho A^{2}\omega^{2}\sin ^{2}(\omega t-kx)$, and integrating this with time over a period, one gets the avg energy density $\bar{w}=\frac{1}{2}\rho A^{2}\omega^{2}$

### wave energy [[flux]]
the amt of energy passing thru a surface $S$ is called wave energy flux (năng thông sóng): $P=wSv$

- avg in period $\bar{P}=\frac{1}{2}\rho A^{2}\omega^{2}Sv$
- avg wrt $S$: the wave energy flux density $\Phi=\frac{\bar{P}}{S}=\bar{w}v=\frac{1}{2}\rho A^{2}\omega^{2}v$

=> the **umov-poynting vec**: $\vec{\Phi}=\bar{\omega}\mathbf{v}$ repr the propagation of energy
