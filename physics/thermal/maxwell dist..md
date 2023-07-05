the maxwell [[dist]] is a distribution used to model the molecular velocities of a certain [[gas]]

## formula
$\frac{dn}{n}=\left( \frac{m}{2\pi kT} \right)^{3/2}e^{ -mv^{2}/2kT }d^{3}v$ is the probability of a molecule's velocity is in the box desc. by $v$ and $d^{3}v$

now, one can find the PDF wrt v
- prob. vel. in the $v_{0}<v<v_{0}+dv$ range: $dn=n\left( \frac{m}{2\pi kT} \right)^{3/2}e^{ -mv^{2}/2kT }4\pi v^{2}dv$
- => PDF $f(v)=\frac{dn}{n}=\left( \frac{m}{2\pi kT} \right)^{3/2}e^{ -mv^{2}/2kT }4\pi v^{2}=\sqrt{ \frac{2}{\pi} } \frac{v^{2}e^{ -v^{2}/2a^{2} }}{a^{3}}$ for $a^{2}=\frac{kT}{m}$ (the a-form is the mathematical form of the distribution)

the CDF is related to the error function, so yay we don't need to care about that.

PDF max when $v^{2}e^{ -v^{2}/2a^{2} }$ max, calcing the derv yields $v^{2}=\frac{1}{2a^{2}}=\frac{2kT}{m} \implies v_{xs}=a\sqrt{ 2 }$

one can rewrite the PDF as $f(u)=\frac{4}{\sqrt{ \pi }} u^{2}e^{ -u^{2} }$ with $u=\frac{v}{v_{xs}}=\frac{v}{a\sqrt{ 2 }}$

## derivation
TODO

## mean
the mean velocity is $\bar{v}=E[v]=\int _{0}^{\infty} \sqrt{ \frac{2}{\pi} } \frac{v^{3}e^{ -v^{2}/2a^{2} }}{a^{3}} \, dx=a\sqrt{ \frac{8}{\pi} }$
the mean velocity squared is $E[v^{2}]=3a^{2}$ (gaussian integral bullshit)
=> avg [[ke]]: $\bar{W}=\frac{m \bar{v^{2}}}{2}=\frac{3kT}{2}$
- "vận tốc căn quân phương": $v_{c}=\sqrt{ \bar{v^{2}} }=a\sqrt{ 3 }$

=> we have $\bar{v},v_{c}, v_{xs} \propto a$ and $v_{xs}<v_{c}<\bar{v}$
![[Pasted image 20230423214612.png]]

