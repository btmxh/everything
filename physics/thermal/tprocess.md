(the prefix t is used to distinguish this from [[process]])

## iso*
vi: đẳng ...
- $p$ const => isobaric (đẳng áp)
	- work: $W=-\int _{[s_{1},s_{2}]} \, dW=-\int _{[V_{1},V_{2}]} p \, dV=-p\Delta V$
	- heat: $Q=\int _{[s_{1},s_{2}]} nC \, dT=nC\Delta T$
	- we know that $pV=nkN_{A}T$ => $\frac{\Delta V}{\Delta T}=\frac{nkN_{A}}{p}$
	- change in internal energy $\Delta E=W+Q=-p\Delta V+nC\Delta T=\Delta T(nC-nkN_{A})$
	- we have $E=iN \frac{kT}{2}$ => $nC-Nk=\frac{iNk}{2}$ => $nc_{m}=Nk\left( 1 + \frac{i}{2} \right)$ => $C=kN_{A}\left( 1+\frac{i}{2} \right)=R\left( 1+\frac{i}{2} \right)$ 
> 	note: we denote the above value $C_{p}$

- $V$ const => isochoric (đẳng tích)
	- $V$ const, calc $A, Q, \Delta E$ (on the $p-V$ graph, since $V$ const, the process is just a line bruh)
	- work: since $dV=0 \implies dW=0\implies W=W_{0}=0$
	- heat: $Q=\int _{[s_{1},s_{2}]} \, dQ=\int _{[T_{1},T_{2}]} nC \, dT=nC\Delta T$
	- => $\Delta E=nC\Delta T$
	- note that $E=iN \frac{kT}{2}$ => $\Delta E=iN \frac{k\Delta T}{2}$ => $C=\frac{ikN}{2n}=\frac{ikN_{A}}{2}=\frac{iR}{2}$
> 	note: we denote the above value $C_{V}$
- $T$ const => isothermal (đẳng nhiệt)
	- work $W=\int _{[V_{1},V_{2}]} -p \, dV=\int _{[V_{1},V_{2}]} -\frac{kNT}{V} \, dV$$=-kNT\Delta \ln V=kNT\Delta \ln p$
	- internal energy $E=iN \frac{kT}{2}$ does not change => $Q=-W$

the ratio $\gamma=\frac{c_{p}}{c_{V}}>1$ is called the poisson coeff, and it's equals to $1+\frac{2}{i}$ (in reality, $i$ can't accurately model stuff => we use the poisson stuff)

given the poisson coeff, one should not calc $i$ but rather find $C_{V}$ and $C_{p}$ by the formula $c_{p}=R+c_{V}$ (one can easily prove this without using $i$) and $\gamma=\frac{c_{p}}{c_{V}}$

e.g. $\mu=0.03\text{kg/mol}$, $\gamma=1.4$, calc $c_{p}$
- we have $C_{p}=\gamma c_{V}$ and $C_{p}-C_{V}=R$ => $C_{p}=\frac{R}{1-\frac{1}{\gamma}}$
- then $c_{p}=\frac{C_{p}}{\mu}=\frac{R}{\mu\left( 1-\frac{1}{\gamma} \right)}=970.02$

## adiabatic
vi: đoản nhiệt

basically $Q=0$
- then we have $E=iN \frac{kT}{2}$ => $\Delta E=W=iN \frac{k\Delta T}{2}=mC\Delta T$ =>$C=\frac{iNk}{2m}=\frac{ikN_{A}}{2\mu}=\frac{iR}{2\mu}=\frac{C_{V}}{\mu}$, then one can write $\Delta E=nC_{V}\Delta T$
- => then if one give the thing work (nén đoản nhiệt), it will heat up and bla bla (giãn đoản nhiệt)
- now consider this $dE=nC_{V}dT=-pdV=dW$
- we have $pV=kNT$ => $p=\frac{kNT}{V}$ => $nC_{V}dT=-\frac{kNT}{V}dV$, which is equiv to $nC_{V}d\ln T+kNd\ln V=0$ => $C_{V}d\ln T+Rd\ln V=0$
- we have $\gamma=\frac{C_{p}}{C_{V}}=1+\frac{R}{C_{V}}$ => $d\ln T+(\gamma-1)d\ln V=0$ => $d(TV^{\gamma-1})=0$ => $TV^{\gamma-1}$ const
- subbing $V$, $T$ we have this $\boxed{TV^{\gamma-1},Tp^{-1+\gamma^{-1}},pV^{\gamma}=\text{const}}$
- or equivalently, $V\propto T^{(1-\gamma)^{-1}}\propto p^{-\gamma^{-1}}$
- or even better, $V^{-1/C_{V}}\propto p^{1/C_{p}}\propto T^{1/R}$
- using this, one can derive this formula for $W$ (i hate this stop shoving formulas after formulas please this goddamn university please actually teach good information instead of testing the ability to memorize shit fuck this bullcrap) (they're the same thing btw) $W=\frac{(pV=nRT)_{s_{1}}}{\gamma-1}\left(-1+\left(\delta T=\delta V^{1-\gamma}=\delta p^{1-\gamma^{-1}}\right)\right)$

## reversible
vi: quá trình thuận nghịch

for [[gas]], this is a [[balanced state#gas|balanced process]]

after a R [[tprocess]], we have $\Delta E=W=Q=0$ (since begin state = end state)

irreversible [[tprocess]] is self-explanatory

e.g. in reality, there is no reversible [[tprocess]] with non-zero [[work]] (otherwise, a static system may work), because a part of this [[work]] is always converted into [[heat]] 




