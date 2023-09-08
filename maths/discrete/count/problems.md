## menage
n pairs of kano-nayutas, 2n seats in a roundtable pogpega
=> how many arrangements (no one cares about cyclic bs) st kanos don't sit next to kanos, no kano-nayuta pair sit next to each other

**solution**
### intro
label kanos and nayus by k_i and n_i
NoA for kanos: 2n! (2 for 2 sets of seats, n! for n kanos), wlog k_i sit at index i (of the first set)
NoA for nayus = num($\phi$ maps 1..n to 1..n s.t. $A(\phi)$ and $B(\phi)$), $\phi(i)$ is the seat index for $n_{i}$ (of the second set)
k1 n1, k2 n2, k3 n3, ..., kn, nn => $\phi(i)=i$
k1 n2, k2 n3, ... => $\phi(i)=i+1$
=> both are undesirable so:
- $A(\phi)$ is $\phi(k) \neq k$ (k does not sit next to kth nayu)
- $B(\phi)$ is $\phi(k) \neq k+1$ (kth nayu does not sit prev to k+1 kano)

### GNBT
let $P_{i}(\phi)=(\phi(i)=i)$ and $Q_{i}(\phi)=(\phi(i)=i+1)$
and make it a seq by letting $P_{n+i}=Q_{i}$
also let $N$ by the set of all arrangements of nayus
=> NoA for nayus = |N - union(i=1..n, P_i)| = |N| - sum(k=1..n, N_k) for N_k be the nums in the GNBT formula
btw |N|=n!

### N_k
now we calc N_k
when we pick i1, i2, ..., i_k there are two cases:
- there are 2 incompatible conditions => result is 0
- no incompatibility => phi is fixed at k positions => result is (n-k)!

=> count the number of non-incompatible groups g(k) then N_k=g(k)(n-k)!

### incomp?
to count g(k), we investigate when there could be incomp.:
- consider P_3, it's incomp with
	- Q_3 (3 != 4)
	- Q_2 (3rd seat has 2 nayus)
- => conclusion: P_k incomp with Q_k and Q_(k-1) (cyclic subtraction)

we can line up the P and Q's like such:
P1 Q1, P2 Q2, ..., Pn Qn (cyclic back to P1 Q1)

### g(k)
#### line
ignoring cyclic sub, we count g(k) if the above seq is a line
using the bar-and-star crap, we use k bars to split stuff, with a striking difference being the bars indicate the items themselves (not the gaps) => 2n-k stars left
also the first k-1 bars have to be followed by a star (or the last k-1 ones having to be precedented with a star, same thing) => merge this star with the bar, leaving only 2n-k-k+1 stars left
now we are free to place k bars in 2n-k-k+1 + k positions (each position is either bar or star, so num of positions = num of bars + num of stars) => result = $C_{2n-k+1}^{k}$

(btw it also work if 2n is odd, so we can use induction)

#### circle
- in the case that P1 is not selected, we are gaming $C_{(2n-1)-k+1}^{k}=C_{2n-k}^{k}$
- if P1 is selected, then rip Qn and we are also gaming $C_{(2n-1)-k+1}^{k-1}=C_{2n-k}^{k-1}$
- combining we have: $g(k)=\frac{2n}{2n-k}C_{2n-k}^{k}$

### conclusion
$g(k)=\frac{2n}{2n-k}C_{n-k}^{k}$
=> $N_{k}=\frac{2n}{2n-k}C_{2n-k}^{k}(n-k)!$
=> NoAs for nayus = $n!+\sum_{k=1}^{n}(-1)^{k} \frac{2n}{2n-k}C_{2n-k}^{k}(n-k)!$, this times 2n! yields the result

## lines
n lines (no colinear idk the terms and stuff) how many sections?
basically a new line intersect n-1 lines => n sections
S_n=S_(n-1)+n...

## catalan
$C_{n}$: the num of parentheses seqs including n open and n close par. s.t. "it makes sense"

### wtf makes sense
basically stuff only stop making sense when "there is that red close paren",
```python
((())))
```
i.e. `string.substr(0, k)` has more ) than ( for some k
we can model such a substr as a pair $(u,v)$ of parens, with the condition being $u\geq v$
every time we can either add to u or to v (add to v ofc only when u>v)

hence, catalan nums (C_n) represent:
- parens bullshit, and more generally https://en.wikipedia.org/wiki/Dyck_word
- NoW of multiply association order for n+1 things (i.e. matrices): ((())) -> (a(b(cd))), (()())() -> (((ab)c)d), etc. (the mapping rules are somewhat complex tho)
- num of full binary trees with n+1 leaves (n internal nodes)
- monotonic [lattice paths](https://en.wikipedia.org/wiki/Lattice_path "Lattice path") along the edges of a grid with _n_ × _n_ square cells, which do not pass above the diagonal (see the uv thing above)
- NoW to divide (n+2)-convex-polygon into n triangles s.t. no intersecting divides (ykwim), also why?
- NoW to tile stairshape of height n with n rects

### dyck
we know that a str starts with (, and this ( will be terminated by some ) somewhere, so the string is in the form (X)Y with X, Y being dyck words
=> NoW: $N(n)=\sum_{|X|=0}^{n-1} N(|X|)N(n-1-|X|)$, or $N(n+1)=\sum_{a+b=n}N(a)N(b)$

let OGF of $N(n)$ be $f(x)$, then $f(x)f(x)=\sum_{k=0}^{n}\sum_{a+b=k}N(a)N(b)x^{k}=\sum_{k=0}^{n}N(k+1)x^{k}$
=> $xf(x)^{2}=f(x)-N(0)$
=> $f(x)=\frac{1\pm \sqrt{ 1-4x }}{2}$
doing funny lim shit, we must have the pm be -
=> $f(x)=\frac{1-\sqrt{ 1-4x }}{2}$ => $N(n)=\frac{1}{n+1}C_{2n}^{n}$

