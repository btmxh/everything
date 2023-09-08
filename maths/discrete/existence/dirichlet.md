given $n$ objects and $m$ labels => at least $\operatorname{ceil}(\frac{n}{m})$ has the same label

## SDR
sys of distinct reprs of a class of set $S_{k}$ is a set $\{ s_{k}\in S_{k} \}$ s.t. $s_{i} \neq s_{j}$ for all i != j

- if SDR exists, union of k arbitary sets in the class have at least k elems (in SDR)
- **Hall's theorem**: if the above is true, then SDR exists, and let $t$ be the min card of a set, $m$ be the num of sets
	- $H(t,m)$ as a lower bound of the num of SDRs, with
		- if $t\leq m$, $H(t,m)= t!$
		- if $t\geq m$, $H(t,m)=\frac{t!}{(t-m)!}$
**proof**
- m=1 => we have t SDRs => $H(t,1) = t!$ qed
- consider the general version $H(t,m)$
	- peel an element $e$ from S1 and its copies from S2, S3, etc., then the system satisfy the above conditions(1) => have $H(t-1,m-1)$ SDRs for S2...Sm => add e to get a new SDR
	- => $H(t,m)=|S_{1}|H(t-1,m-1)=tH(t-1,m-1)$ => qed
- (1) only happens if union of k ... have **more** than k elems, assuming this ideal case does not happen, for example |S1 u S2 u ... u Sk|=k for some $k\leq m$
	- if $k < m$, then $t\leq k<m$, $H(t, k)$ -> can find $t!$ SDRs of $S_{1}\dots S_{k}$, let one such SDR be $s_{1},s_{2},\dots,s_{k}$, then we remove all of these elements from $S_{k+1}$ to $S_{m}$ -> $S'_{k+1}\dots S'_{m}$
		- the class set $S'_{k+1}\dots S'_{m}$ satisfy the initial conditions => we can find an SDR for that, combine with S1...Sk => t! SDRs
			- assuming there are $k'$ sets in the class with card union less than $k'$, then the original sets + S1...Sk have card union less than k+k' (k from the SDR and <k' from the union) => invalid
	- if $k=m$?


