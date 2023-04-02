$sa_{n}$ abs conv iff $s|a_{n}|$ conv

**theorem**: abs conv implies conv
**proof**
$0\leq s(a_{n}+|a_{n}|)\leq 2s|a_{n}|$ => MHS conv => $sa_{n}=MHS-s|a_{n}|$ conv

**theorem**: rearranging abs conv [[series]] does not modify the sum
**proof**
- let $\sigma$ be a rearrangment, i.e. a bijection from the index set $I$ to itself
- case positive series
	- have: $sa_{n}\leq sa_{\infty}=S$ => $s(a_{\sigma(n)})_{n} \leq S$ => the rearranged series conv to $S'\leq S$
	- but using $\sigma^{-1}$, we can prove that $S\leq S'$
	- therefore $S=S'$
- $a_{n}^{+}=\max\{a_{n},0\}, a_{n}^{-}=-\min\{a_{n},0\}$ then
	- $sa_{\infty}=sa_{\infty}^{+}-sa_{\infty}^{-}=sa_{\sigma(\infty)}^{+}-sa_{\sigma(\infty)}^{-}=sa_{\sigma(\infty)}$, qed
