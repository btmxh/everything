# most general form
let $n\in N$, $k\times n$ matrix $A$ (weight), constraint ($k\times 1$matrix) vector $m$, objective $1\times n$ matrix $M$ (all elements of these matrices are positive)
then find vector $v\in Z_{0+}^{n}$ s.t.
- all elements of $m-Av$ are non-negative
- $f(v)=Mv$ max

## k=1 case
let $A=[a_{1},a_{2},\dots,a_{n}]$, $M=[m_{1},m_{2},\dots,m_{n}]$, $v=[v_{1},v_{2},\dots,v_{n}]^{T}$
=> needs $a_{1}v_{1}+\dots+a_{n}v_{n}\leq m$ and $m_{1}v_{1}+\dots+m_{n}v_{n}$ max

**optimal**
if we let $v_{2}=\dots=v_{n}=0$ and maximize (not caring about integer and stuff), $v_{1}=\frac{m}{a_{1}}$ => $f(v_{0})=\frac{mm_{1}}{a_{1}}$
we will find the condition so that the above $v_{0}$ is the optimal solution
consider $v=[v_{1},v_{2},\dots,v_{n}]^{T}$, we want $\sum m_{i}v_{i}\leq \frac{mm_{1}}{a_{1}}$
<= $\sum m_{i}v_{i}\leq \frac{m_{1}}{a_{1}}\sum a_{i}v_{i}$ <= $\sum v_{i}\left( m_{i}-\frac{m_{1}}{a_{1}}a_{i} \right)\leq 0$
now since $v_{i}$ are arbitary, we basically need $m_{i}-\frac{m_{1}}{a_{1}}a_{i}\leq 0 \iff \frac{m_{i}}{a_{i}}\leq \frac{m_{1}}{a_{1}}$ for all $i$, so a natural way to get this is **adding the assumption** that $\left( \frac{m_{i}}{a_{i}} \right)_{i\in 1..n}$ is a decreasing sequence

[[bnb]]
to solve this with bnb, we need an upper bound $g$ for incomplete solutions
basically we will idealize the remaining of a incomplete sol as such
- assuming we have an incomplete sol $v'=[v_{1},v_{2},\dots,v_{k-1}]^{T}$
- we know that the optimal way to do stuff is just spamming the $k$-th item, i.e. letting $v_{k}=\frac{m-\sum_{i=1..<k} a_{i}v_{i}}{a_{k}}$
- and $g(v'')=\sum_{i=1..k} m_{i}v_{i}=f(v')+\frac{m_{k}(m-\operatorname{cost}(v'))}{a_{k}}$
=> one can keep track of $g(v')$ and $\operatorname{cost}(v')$ for $O(1)$ calculation of $g(v'')$

**algorithm**
```python
class solution(RecordClass):
	val, f = 0, cost = 0, k = 0, ovk = 0
	# ovk: optimal_vk

def empty() = solution(val = [])
# simplified, need check for sol.k == n
def g(sol) = sol.f + (m_tot - sol.cost) / a[sol.k]
def invalid_bnb() = False
def extend_sol(sol):
	vk = (m_tot - last_cost)/a[k]
	for vk in reversed(range(int(sol.ovk))):
		s = copy(sol)
		s.val += [vk]
		s.f += m[s.k]vk
		s.cost += a[s.k]vk
		s.k += 1
		s.ovk = 
		yield sol + [vk]
```