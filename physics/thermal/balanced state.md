some system at state $S$ is considered to be stable/balanced if this state does not change with time, i.e. $\frac{dS}{dt}=0$

- a system not interacting with outside will tend to some balanced state (yeah let's pretend that $\lim_{ n \to \infty } n$ and $\lim_{ n \to \infty } (-1)^{n}$ exist why not)
- to make a BS unbalanced, one must interact with the system by giving them work/heat
## [[gas]]
- a BS can be specified by properties like $V$, $p$, $T$
- one can repr the BS on the $(p,V)$ graph using a point (one can easily infer $T$ using $pV=nkN_{A}T$)

a balanced [[tprocess]] is a process with all state balanced
e.g. [[ideal gas]] $p(t)=t+1, V(t)=\frac{1}{t+1}, n=\frac{1}{kN_{A}T}$, then since $pV=nkN_{A}T$ for all $t$, this is a balanced process

in a balanced process, energy is not conserved, because u can always give the system work/heat.

### work
e.g. compressing air using piston
- in this way, we are exerting a force $\mathbf{F}$ to compress the gas
- work $dW=-Fdl$ (minus sign is because $dl<0$, why? ask miss ptnh)
- loss in volume: $dV=Sdl$
- now since the process is balanced => the force $\mathbf{F}$ balances with $\mathbf{F'}$ caused by air pushing back the piston, and $F'=pS$ (definition of pressure)
- then, one have $dW=-pSdl=-pdV$ (assuming gas is in a rectangular box)
- integrating over $V$, one find the total $W$ (not trivial, since $p$ depends on $V$): $W=\int _{[s_{1},s_{2}]} dW=\int _{[V_{1},V_{2}]} -p \, dV$

the formula $\boxed{dW=-pdV}$ still holds in general

now, if in a cycle, which can be parameterized using time: $V(t), p(t)$, from $t=t_{0}$ to $t=t_{1}$ with $s(t_{0})=s(t_{1})$
=> the total work $W$ is the difference between the two integrals like above, but at $t_{0}$ and $t_{1}$, which is actually the area of the curve made by $V(t)$ and $p(t)$
hence, one can use stuffs from [[multiint]] and [[generalized stoke's theorem]] to execute some gaming
> note: sign will be positive (the system took energy) if ![[Pasted image 20230424020016.png]]






