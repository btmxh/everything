## first law
the change in a system is equals to the sum of [[heat]] and [[work]]: $\Delta E=Q+W$
wlog the mechanical energy (sum of KE and PE) does not change, then $\Delta ME=Q+W$

an isolated system => $\Delta E=Q=W=0$
conservation of heat: $Q_{1}+Q_{2}+\dots=0$

if $\Delta E=0$ (a cycle) => $Q=-W$

this law is basically the [[energy#conservation of energy|conservation of energy]] law applied in thermodynamics

- machine works in cycles => $Q=-W=W'$ => there can't be any thing that create work without input heat etc. etc.
- no infinite engine of type I
according to first law, these can be true
- heat transfers from cold object to hot object
- $Q$ can be 100% turned into $W$

=> **limitations**
- idk the transfer process' direction
- no differences in the conversion between $W$ and $Q$
- one can't rate the **heat quality** (idk wtf this is)

## second law
- clausius:
	- [[heat]] can't transfer from a cold obj to a hotter obj
	- or there could be no processes with the only result being the transfer of heat from a cold obj to a hotter one
- thompson
	- one can't create a periodic machine continuously convert [[heat]] into [[work]] (via freezing something) without any outside interjection
	- or no infinite engine of type II
	- (one can't convert all [[heat]] into [[work]], just some of it)
- formula
	- by the [[carnot]] thing, one has $\eta\leq 1-\frac{T_{2}}{T_{1}}$, and by the definition of $\eta=\frac{Q-Q'}{Q}$, we have $\frac{Q'}{Q}> \frac{T_{2}}{T_{1}}$
	- or in vldc notation: $\frac{Q_{1}}{T_{1}}+\frac{Q_{2}}{T_{2}}\leq 0$
	- for a generalized [[carnot]] [[tprocess]] , we have $\sum_{i=1}^{n} \frac{Q_{i}}{T_{i}} \leq 0$
	- taking this further, one has $\oint_{C} \frac{dQ}{T}\leq 0$ for a continuous [[carnot]] [[tprocess]]
=> the second law provides
- the direction of thermodynamic processes
- the law of conversion between $W$ and $Q$ => very useful for heat machines
- the **heat quality**: the higher $T$ is, the more $W$ it can convert from its $Q$

> **heat machine**: a system that converts $Q$ to $W$ or $W$ to $Q$
> 2 types: heat engine ([[heat]] -> [[work]]), freezer ([[work]] ->[[heat]])
> parts: tác nhân (shit makes thing work), heat source (nguồn nóng, nguồn lạnh)

bla bla im not an engineer
![[Pasted image 20230424125922.png]]
**efficiency** of heat engine $\eta=\frac{W'}{Q}$ 
- $W'$ is the amt of work that the **env** recv, is equal to $-W$ relative to the "tác nhân"
- $Q$ is the amt of heat that the hot src gives to tác nhân => $Q'$ is the amt of heat that tác nhân gives to the cold src => $W'=Q-Q'$ and $\eta=1-\frac{Q'}{Q}$

e.g. some amt of [[ideal gas]] produces work by doing a [[tprocess]] cycle: [[tprocess#adiabatic|adia]] + [[tprocess#iso*|isobaric]] + [[tprocess#iso*|isochoric]], after the first subprocess $V_{2}=2V_{1}$, find $\eta$
![[Pasted image 20230424142742.png]]
from the graph, we find out that $T_{1},T_{2}>T_{3}$
the amt of [[heat]] added to the system is $Q_{3\to 1}$, and removed from the system is $-Q_{2\to 3}$
=> $\eta=1+\frac{Q_{2\to 3}}{Q_{3\to 1}}$
we have $Q_{2\to 3}=nC_{p}\Delta T_{2\to 3}$, $Q_{3\to 1}=nC_{V}\Delta T_{3\to 1}$ => $\eta=1-\frac{C_{p}}{C_{V}}=1-\gamma \frac{T_{2}-T_{3}}{T_{1}-T_{3}}$
now, in the adia proc, $V\propto T^{(1-\gamma)^{-1}}$ => $2^{1-\gamma}=\frac{T_{2}}{T_{1}}$
and in the 2-3 proc, $T\propto V$ => $\frac{T_{2}}{T_{3}}=\frac{V_{2}}{V_{1}}=2$ => wlog assuming $T_{1}=1, T_{2}=2^{1-\gamma}, T_{3}=2^{-\gamma}$
=> $\eta=1-\gamma \frac{2^{1-\gamma}-2^{-\gamma}}{1-2^{-\gamma}}=1-\frac{\gamma}{2^{\gamma}-1}$

e.g. [[ideal gas]] produce [[work]] by a process: isob + adia + isot, before isot, temp was max $\Theta$, and $\Theta=n\theta$ with $\theta$ being the min temp of the proc, calc $\eta$

> how to draw diagram
> isob: $y=c_{0}$
> adia: $yx^{1-\gamma}=c_{1}$
> isot: $xy=c_{2}$
> pick coeffs s.t. it looks like this (order: blue -> red -> green)
> ![[Pasted image 20230424145421.png]]

(if u pick the upper half)
![[Pasted image 20230424145644.png]]
(wlog one can reorder)

we have $Q_{3 \to 1}=0$, $Q_{1\to  2}=-kNT_{1}\Delta (\ln p)_{1\to 2}$, $Q_{2\to 3}=mC_{p}\Delta T$
we can see that $Q_{1\to 2}>0, Q_{2 \to 3}<0$ then $\eta=1-\frac{mC_{p}(T_{3}-T_{2})}{kNT_{1}(\ln p_{2}-\ln p_{1})}$
we have $T_{1}=T_{2}=nT_{3}$, then $T_{2}-T_{3}=\frac{n-1}{n}T_{1}$
=> $\eta=1-\left( 1-\frac{1}{n} \right)\frac{C_{p}}{R\left( \ln \frac{p_{2}}{p_{1}} \right)}$
=> $\eta=1+\left( 1-\frac{1}{n} \right) \frac{C_{p}}{R(\ln p_{2}-\ln p_{1})}$
in 3-1 proc, we have $V\propto T^{(1-\gamma)^{-1}}\propto p^{-\gamma^{-1}}$ => $p\propto T^{-\gamma(1-\gamma)^{-1}}$ and $p_{2}=p_{3}$=> $\ln p_{2}-\ln p_{1}=-\frac{\gamma\ln n}{1-\gamma}$
then $\eta=1-\left( 1-\frac{1}{n} \right) \frac{C_{p}(1-\gamma)}{R\gamma\ln n}$
we have $C_{p}-C_{V}=R$, $\frac{C_{p}}{C_{V}}=\gamma$ => $C_{p}=\frac{R\gamma}{1-\gamma}$ => $\eta=1-\frac{1-\frac{1}{n}}{\ln n}$
