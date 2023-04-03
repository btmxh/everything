## add/sub [[unsigned]]
- add: 1+0=0+1=1, 0+0=1+1=0 (borrow 1)
- => may overflow (overflow bit is also called the carry-out bit)
- subtract: same or add with negative
- => may underflow

## add/sum [[signed]]
- add/sum: same
	- if 2 signs differs => result is true even if over/underflow
	- otherwise, if signs of sum/diff differs from operands => result is false
	- e.g. (9-bit)
		- 0x1 + 0x1 = 0x2: true
		- 0x1 + 0x1ffff = 0x0: true
		- 0xffff + 0xffff = 0x1fffe: false
## mul/div [[unsigned]]
- like normal
- ![[Pasted image 20230403155229.png]]
- ![[Pasted image 20230403155247.png]]


## logic ops
- and
- or
- xor
- not

=> **one can clear bits using and, set bits using or** => **masks**

## add/sub [[float]]
$F_{1}=M_{1}R^{E_{1}}, F_{2}=M_{2}R^{E_{2}}$ then
- $F_{1}\pm F_{2}=(M_{1}R^{E_{1}-E_{2}}\pm M_{2})R^{E_{2}}$, assuming $E_{1}\geq E_{2}$

## mul/div [[float]]
same floats as above
- $F_{1}F_{2}=(M_{1}M_{2})R^{E_{1}+E_{2}}$
- $\frac{F_{1}}{F_{2}}=\left( \frac{M_{1}}{M_{2}} \right)R^{E_{1}-E_{2}}$

e.g. $\pi+2.3 \cdot10^{1} e$ (round to 2 digits, $R=10$)
- $2.3e=(2.3\cdot 2.71)10^{1+0}=6.233\cdot 10^1$
- $\pi+2.3 \cdot 10^1e=3.14\cdot 10^0+6.233\cdot 10^1=(3.14+62.33)\cdot 10^0=65.47$
