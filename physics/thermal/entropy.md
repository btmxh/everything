entropy is a **fn $S$ of state**, s.t. $\Delta S=\int _{[s_{1},s_{2}]} \frac{dQ}{T}$ ($dQ$ is infinitesimal)
then $dS=\frac{dQ}{T}$
- entropy is additive
- entropy is relative => one usually set $S=0$ at abs zero

unit: J/K

## [[thermo laws#second law|2nd law]]
using [[entropy]], one can restate the 2nd law
since $\oint \frac{dQ}{T}<0$ for [[tprocess#reversible|irev]] procs, split the state curve into 2 parts: $s_{1}\to s_{2}$, $s_{2}\to's_{1}$, then $\oint_{\to}+\oint_{\to'}<0$
now assuming $\to'$ is reversible => $\oint_{\to}<\oint_{\leftarrow'}=\Delta S$
then one has:
$\boxed{\oint_{[s_{1},s_{2}]} \frac{dQ}{T}\leq\Delta S}$

equality holds iff reversible
in other words, $d\Delta S\geq \frac{dQ}{T}$

## increase law
for an isolated system, we have $Q=0$ => $\Delta S\geq 0$
=> entropy of an irrev. isolated system will tends to increase, of an rev. isolated system will stay constant

in other words, an isolated system can't have an identical state twice, and at equilibrium, its entropy is at a local max

> the heat death states that the universe total entropy will reach max, its energy is const => no more transfer of energy
> according to miss ptnh (not to me tho), this is wrong because
> - this contradicts with the conservation of energy: the "năng lượng vận động của vật chất" is $\infty$, can't be destroyed, can only be turned into another form
> - this theory consider the universe to be an isolated system => not true because it's in a potential gravitational field that changes over time, the universe's motion is non-stop

## [[ideal gas]]
we have $\Delta S=\int _{[s_{1},s_{2}]} \frac{dQ}{T}$
and $dQ=\Delta E-W=nC_{V}dT+pdV=nC_{V}dT+nRT \frac{dV}{V}$
=> the entropy $\Delta S=\int _{[s_{1},s_{2}]} (nC_{V}d\ln T+nRd\ln V)$$=nC_{V}\Delta\ln T+nR\Delta \ln V$

for [[tprocess#adiabatic|adia]], $Q=0$ => $\Delta S=0$ => $C_{V}\Delta \ln T+R\Delta \ln V=0$ => one can use this to establish the relationship between $T$ and $V$

e.g.
- isot => $\Delta S=nR\Delta \ln V$
- isoc => $\Delta S=nC_{V}\Delta \ln T$
- isob => $\Delta S=n(C_{V}+R)\Delta \ln V=nC_{p}\Delta \ln V$

introducing a new graph: the $(T,S)$ graph
then one have $Q=Td\Delta S$ => one can calc $Q$ by finding the are below a graph bla bla

## meanings
- [[heat]] can't transfer from cold -> hot + entropy of isolated can't dec
- isolated will transform from unbalanced to balanced and can't go back
- entropy measures how chaotic the movement is
- 