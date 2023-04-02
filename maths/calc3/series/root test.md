$\lim_{ n \to \infty }\sqrt[n]{ | a_{n}| } = L\in R$ then
- if $L<1$, $sa_{n}$ abs conv
- if $L>1$, $sa_n$ div
- otherwise, the test is inconclusive

**NOTE**: if $L=\infty$, then u gotta manually do the $L>1$ case

**proof**
if $L<1$, there exists $n_{0}$ s.t. $\sqrt[n]{ |a_{n}| }<q<1$ for every $n>n_{0}$
then $|a_{n}|<q^n$ => $s|a_{n}|$ [[geom series]] conv.
if $L>1$, $\lim_{ n \to \infty } a_{n}>\lim_{ n \to \infty }L^n=\infty$ violate the [[n term test]]
