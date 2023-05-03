the **cond prob** $P(E_{1}|E_{2})$ is defined to be $\frac{P(E_{1}E_{2})}{P(E_{2})}$, i.e. the [[prob]] of $P(E_{1})$ in the sample space $\Omega_{E_{2}}$.

the events $E_{1}$ and $E_{2}$ are indep if $P(E_{1}|E_{2})=P(E_{1})$ and $P(E_{2}|E_{1})=P(E_{2})$, or equivalently, $P(E_{1}E_{2})=P(E_{1})P(E_{2})$ (turned out the two statements in the if part is equivalent!)

the **bayes** rule starts from $P(E_{1}E_{2})=P(E_{1}|E_{2})P(E_{2})=P(E_{2}|E_{1})P(E_{1})$
=> $P(E_{1}|E_{2})=\frac{P(E_{2}|E_{1})P(E_{1})}{P(E_{2})}$

if one can write $E_{all}=E_{1}\cup E_{2}\cup\dots\cup E_{n}$ for mutually-exclusive $E_{k}$'s then since $P(E_{k}|A)P(A)=P(A|E_{k})P(E_{k})$, we have $P(A)=\sum_{k=1}^{n} P(A|E_{k})P(E_{k})$ and knowing that, one finds $P(E_{k}|A)=\frac{P(A|E_{k})P(E_{k})}{P(A)}$

e.g. given
1. $P(\text{married|female physicists})=0.5$
2. $P(\text{married|male physicists})=0.74$
3. $P(\text{M. to physicist|married female physicists})=0.5$
4. $P(\text{M. to scientist|married female physicists})=0.79$
5. $P(\text{M. to physicist|married male physicists})=0.07$
6. $P(\text{M. to scientist|married male physicists})=0.18$
calc $P(\text{female|physicists})$?
- calc $P(\text{M. to phy.|male phy.})$
	- taking the sample space of all male phy., then the prob is equals to $P(\text{M. to phy})=P(\text{M. to phy|married})P(\text{married})$$=0.07\cdot 0.74=0.0518$, 
- calc $P(\text{M. to phy.|female phy.})=0.5\cdot 0.5=0.25$
- now, we have $P(\text{male phy. M. to phy.})=P(\text{M. to phy.|male phy.})P(\text{male phy.})$, and a similar thing for female phy., and note that the LHS of both are equal => $0.0518P(\text{male phy.})=0.25P(\text{female phy.})$ => $P(\text{female phy.})=\frac{0.0518}{0.25 + 0.0518}=17\%$

e.g. there are 2 kids in a family, and we knew that one of them is a boy
1. $P(\text{2 boys})$?
2. $P(\text{2 boys|older is boy})$?

the sample space $\Omega=\{ 1,2,3,4 \}$
- state 1: both is boys
- state 2: both is girls
- state 3: older is boy, younger is girl
- state 4: older is girl, younger is boy
then it's trivial that state 2 is invalid and therefore $(1.)=\frac{1}{3}, (2.)=\frac{1}{2}$
