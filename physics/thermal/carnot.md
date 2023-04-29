## [[tprocess]]
the carnot tproc is a [[tprocess#reversible|reversible]] proc consists of some subprocs
- 1->2: [[tprocess#iso*|isothermal]] recv $Q$
- 2->3: [[tprocess#adiabatic|adiabatic]] decreasing $T$: $T_{1}\to T_{2}$
- 3->4: [[tprocess#iso*|isothermal]] send $Q'$
- 4->1: [[tprocess#adiabatic|adiabatic]] increasing $T: T_{2}\to T_{1}$
![[Pasted image 20230424131503.png]]

e.g. for [[ideal gas]] we have
- $Q_{1\to 2}=kNT_{1}\Delta (\ln V)_{1\to 2}$, $Q_{3\to 4}=kNT_{2}\Delta(\ln V)_{3\to 4}$
- the first $Q_{1\to 2}$ acts as the amount of [[heat]] given to system => $Q=Q_{1\to 2}$, similarly $Q'=-Q_{3\to 4}$
- we look at the two [[tprocess#adiabatic|adia.]] proc 2->3, 4->1: $V\propto T^{(1-\gamma)^{-1}}$ (note that $p$ const) => $\delta V=\delta T^{(1-\gamma)^{-1}}$ => $\Delta \ln V=\frac{\Delta \ln T}{1-\gamma}$ => $\Delta (\ln V)_{2\to 3}+\Delta(\ln V)_{4\to 1}$$=\Delta(\ln T)_{1\to 2}+\Delta(\ln T)_{2\to 1}=0$ => $a$
- then efficiency $\eta=1-\frac{Q'}{Q}=1+\frac{T_{2}\Delta(\ln V)_{3\to 4}}{T_{1}\Delta(\ln V)_{1\to 2}}=1-\frac{T_{2}}{T_{1}}$

this $1-\frac{T_{2}}{T_{1}}$ thing is denoted by $\eta_{c}$

## theorem
**present**: the eff of all [[tprocess#reversible|reversible]] engines using [[carnot]] process with same $T_{2}$ ([[temperature]] of hot src) and $T_{1}$ ([[temperature]] of cold src) are equal, and non-carnot engines will have less than $\eta_{c}$ efficiency

**corollary**
- since $T_{2}>0$ (no abs zero), $\eta_{c}<1$ we can't convert $100\%$ [[heat]] into [[work]]
- $\eta$ inc if one inc $T_{1}$, dec $T_{2}$

=> to make some engine more efficient, one needs to change src temps and make the thing similar to a [[carnot]] engine
