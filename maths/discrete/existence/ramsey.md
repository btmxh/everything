$R(r,s)$ is the num s.t.
- for every complete [[graph]] with $R(r,s)$ vertices and an arbitary red-blue edge coloring of such graph, there is either
	- a red $r$-clique
	- or a blue $s$-clique
=> $R(r,s)=R(s,r)$

also $r,s\leq 1$ cases are meaningless, so one only consider $r,s\geq 2$

colorless: graph $G$ with $\geq R(r,s)$ vertices will have either:
- $G$ has a $r$-clique, or
- $\bar{G}$ has a $s$-clique

## $R(r,s) < \infty$
this can be simply proven by establishing an explicit bound: $R(r,s)\leq R(r-1,s)+R(r,s-1)$
(and the initial conditions for small r,s)

- $R(2,n)=R(n,2)=n$ is finite for all $n\geq 2$
	- if one colors an edge red => 2-clique
	- if no red edges => blue n-clique
- consider the coloring of a graph $G=G_{1}+G_{2}$ with $G_{1}$having $R(r-1,s)$ vertices and $G_{2}$ having $R(r,s-1)$
- consider a vertex $v$ of $G$, partition its neighbor set $N(v)$ into $A,B$ by edge colors ($va$ red, $vb$ blue for $a\in A,b\in B$)
	- => $|A|+|B|=|G|-1\geq R(r-1,s)+R(r,s-1)-1$
	- then either
		- $|A|\geq R(r-1,s)$ => we either has a red $r-1$ clique that also has red edges to $v$ => done, or we have a blue $s$-clique => also done
		- $|B|\geq R(r,s-1)$ => same shit

The above bound can be strengthened into $R(r,s)\leq R(r-1,s)+R(r,s-1)-1$ if $R(r-1,s)$ and $R(r,s-1)$ are both even
- $p=R(r-1,s),q=R(r,s-1),t=p+q-1$
- we let $G$ be a graph with $t$ vertices and we prove the same shit
- now, $t$ odd => hand shaking lemma: $\sum_{v\in V(G)} d_{G^{blue}}(v)=2t$ => pick $v$ s.t. $d_{G^{blue}}(v)$ is even
- => $|A|, |B|$ even s.t. $|A|+|B|\geq p+q-2$ => qed

## $R(3,3,3)$
for $R(r,s,t, \dots)$ one add more colors

label the colors as $1,2,3$ and denote $N_{k}(v)$ as the k-colored neighborhood of $v$
if there are 2 vertices in $N_{k}(v)$ are connected to each other by color $k$, then we form a triangle => invalid => all edges must have color in $\{ 1,2,3 \} \setminus \{ k \}$, i.e. has 2 color => $|N_{k}(v)| < R(3,3)=6$
=> $V= 1+|N_{1}(v)|+|N_{2}(v)|+|N_{3}(v)|\leq 16$

> $R(3,3)=6$ due to the upper bound and that star graph invalidate the ramsey stuff for $n=5$

show an example of a 16-vertex graph... (this is the hard part)
=> $R(3,3,3)=17$


### generalized
we even have $R(r,s,t, \dots; k)$ if we no longer color edges, but $k$-cliques
now consider the case $k=1$: we color vertices
$R(i_{1}+1,i_{2}+1,\dots;1)=\sum i_{j}+1$

this is true since
- graph with $n=\sum i_{j}-k$ vertices can be colored as such: $i_{j}$ vertices with color $j$ for j from 1 to ...
- if we have more, it's trivial why stuff break

the result $R(2,2,\dots;1)=n+1$ is a generalization of [[maths/discrete/existence/dirichlet|dirichlet]]
