## defs
- **sample space** $\Omega$: the space of all possible outcomes (with equal likelihood)
	- e.g. roll a 6-dice => the possible outcomes are characterized by the number on the dice: $\Omega=\{ 1,2,3,4,5,6 \}$
- **event** $E$ is a predicate of outcomes, i.e. a map from $\Omega \to \{ 0,1 \}$
	- e.g. num. on dice is even: $E(n)=(n \operatorname{mod} 2 == 0)$
	- => the set of all favorable outcomes wrt $E$ is $\Omega_{E}=\{ \exists e\in\Omega \,| \,E(e)=1 \}$
	- the null event $E_{null}=E_{\emptyset}$ is the event $E(\omega )=0$ for all $\omega\in\Omega$, its complement is the all event $E_{all}$
- **prob** of an **event** $P(E)$ is the ratio $\frac{m(\Omega_{E})}{m(\Omega)}$, with some [[measure]]/[[content]] $m$
	- if $\Omega$ is finite, $m$ is the cardinality measure: $m(A)=|A|$
	- if $\Omega$ is infinite, $m$ being the lebesgue measure is a nice choice, but it may not work for all cases.
		- e.g. $m(\mathbb{R})=\infty$ even with the lebesgue measure
	- e.g. pick a real number in $[0,1]$, $E:$ the number chosen is rational => $\Omega=[0,1]$, $m(\Omega)=1$ and $\Omega_{E}=\mathbb{Q} \cap [0,1]$, $m(\Omega_{E})=0$ => $P(E)=0$

## ops
- since there is an 121 mapping from event $E$ and its outcome set $\Omega_{E}$, one can characterize an event using its outcome set
- doing ops on the event is now equivalent to doing ops on the outcome set
- $E_{1}\cap E_{2}$, also abbreviated $E_{1}E_{2}$ is the event wrt outcome set $\Omega_{E_{1}}\cap \Omega_{E_{2}}$, i.e. the event: $E_{1}$ and $E_{2}$ are both true
- $E_{1} \cup E_{2}$, $E^{c}=!E=\dots$ can be defined similarly
- if $E_{1}E_{2}=E_{null}$, then one calls $E_{1}$ and $E_{2}$ are **mutually exclusive**

## prob expr
- from the axioms of a measure, one have $P(E^{c})=1-P(E)$, $P(E_{1} \cup E_{2})=P(E_{1})+P(E_{2})-P(E_{1}E_{2})$
- 