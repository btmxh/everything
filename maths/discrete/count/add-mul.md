add principle (NL+): $|A\cup B|=|A|+|B|$ if $A\cap B=\emptyset$
- expanded: $|A_{1}\cup A_{2}\cup\dots \cup A_{n}|=\sum_{k=1}^{n} |A_{k}|$
- subtract: $|A|=|B|-|B \setminus A|$ if $A\subset B$
- butru (NBT): $|A\cup B|=|A|+|B|-|A\cap B|$
	- GNBT: $|\cup_{k=1}^{n} A_{k}|=\sum_{k=1}^{n} (-1)^{k-1}\sum_{1\leq i_{1}<\dots<i_{k}\leq n}|A_{i_{1}}\cap \dots \cap A_{i_{k}}|$
	- we can let $N_{k}$ to be the k-th sigma expr
	- **proof**
		- considering an element $e$ in sets $A_{j_{1}},A_{j_{2}},\dots,A_{j_{m}}$
		- wlog assuming $j_{k}=k$ (we are free to reorder the labels)
		- then we count the number of times we counted $e$ on the RHS
			- fix $k$, num of times we counted it equals num of $(i_{1},\dots,i_{k})$ s.t. $e$ is in all $A_{i_{l}}$ for $l$ from 1 to $k$
			- => $1\leq k\leq m$ and the number is $C_{m}^{k}$
			- => we counted it $\sum_{k=1}^{m}(-1)^{k-1}C_{k}^{m}$
			- add the $k=0$ factor and we have $(1-1)^{m}=0$, and since the added factor is $-1C_{k}^{0}=-1$ => qed
mul prin. (NLx): $|A\times B|=|A|\times|B|$
- power: $|A^{n}|=|A|^{n}$

