im not redefining this

- vertices $u,v$ are adj in simple graph $G$ iff $uv\in E$
- neighbor of a vertex $v$ in simple $G$, $N_{G}(v)$ is the set $\{ u\in V(G), uv\in E(G) \}$
- degree of a vertex $v$ in $G$, $\deg_{G}(v)$ or $\deg(v)$ if one doesn't give shit about $G$, is $|N_{G}(v)|$
- **theorem**: $\sum_{v\in V}\deg(v)=2|E|$
	- **corollary**: num of $v$ with odd deg is even

- $u,v$ adj in directed $G$ iff $uv$ or $vu$ in $E$
- $N^{+}_{G}(v)$ is the set $\{ u\in V, vu\in E \}$, $N^{-}_{G}(v)$ is $\{ u\in V, uv\in E \}$, $\deg^{+},\deg^{-}$ you know the drill

## subgraph
$H$ subgraph $G$ if $V(H)\subset V(G)$, $E(H) \subset E(G)$
$H$ **isomorphically** subgraph $G$ if $H$ is isomorphic to $H'$ subgraph $G$

a graph configuration can be thought of as a constructor of a graph, e.g. $K_{3}, \dots$, or a graph with default vertices
one can construct a variant of such configurations by providing the vertex (ordered) set: $K_{3}(V)$, but in some cases unordered set are allowed (complete graphs)
graph configuration isomorphically subgraph graph $G$ it has one configuration $H$ subgraph $G$

graph constructor $\operatorname{Gr}(V, E)$ give the graph with vertices $V$, edges $E$
vertex and edge subtraction:
$G\setminus_{V}(V')=Gr(V(G)\setminus V', E(G))$
$G\setminus_{E}(E')=Gr(V(G), E(G)\setminus E')$

## path
walk is a seq of vertices, denoted as $v_{1}v_{2}\dots v_{k}$ s.t. $v_{i}v_{i+1}\in E$ for all $i\in 1..<k$, its length is $k-1$, the num of edge in the path (this work for both undirected and directed)
- trail: walk with no repeated edges
- path: walk with no repeated vertices (hence also trail)
- cycle: non-empty trail with $v_{k}=v_{1}$
if $v_{k}=v_{1}$ it's a cycle
path/cycle is simple if no **edges** are repeated

a graph is connected iff for all $u,v\in V$, there exists a path from $u$ to $v$
one can always divide a graph into multiple subgraphs that's all connected
connected components (CC) of a graph $G$ are maximal connected subgraphs of $G$
num of connected comps (NoCC) is the num of CCs in a graph

$v$ is a **separating vertex** iff $G\setminus_{V}\{ v \}$ has more CCs than $G$
e is a **bridge** iff $G \setminus_{E}\{ e \}$ has more CCs than $G$
a graph is $k$-vertex-connected (kVC) iff one can remove arbitary $(k-1)$ vertices and the graph remains connected
same for $k$-edge-connected (kEC)

### 2ECG
a graph is 2ECGs iff it's/it has:
1. bridgeless
2. every edge is a part of a cycle
3. or between $u$ and $v$ there are two edge-disjoint paths
4. have an ear decomp
	- **definition**: ear is maximal path s.t. internal vertices have deg 2
5. can be made into a strongly connected directed graph

**proof**
1. by definition of bridge and kEC
2. 2 parts
- if 2ECG: consider edge $uv$, remove it and graph still connected, let the new path from $u$ to $v$ be $uC_{1}v$ => the cycle is $uC_{1}vu$
- if 2.: $uv$ is a part of the cycle $uC_{1}vu$, then one can remove $uv$ and the connectivity stay the same
3. 2 parts:
- 3. => consider the edge $uv$ then since there are 2 EDPs between $u$ and $v$, there must exist some path $uC_{1}v$...
- 2ECGs => let $uC_{1}v$ be the shortest path with no other path $uC_{2}v$ which is edge-disjointed with $uC_{1}v$
	- if $C_{1}$ is empty, this is the same as the 2. thing
	- if $C_{1}=w_{1}w_{2}\dots w_{k}$, may as well $u=w_{0},v=w_{k+1}$, then we gaming
		- between $w_{i}$ and $w_{i+1}$ must have 2 paths $w_{i}C^{i}_{1}w_{i+1}$ and $w_{i}C^{i}_{2}w_{i+1}$ (shorter path lmfao)
	- then one can make 2 EDPs from $u$ to $v$
		- $uC^{0}_{1}w_{1}C^{1}_{1}w_{2}\dots v$ and $uC^{0}_{2}w_{1}C^{1}_{2}w_{2}\dots v$ => qed or invalid idc
4. idk
5. let $G'$ be the directed graph
- if $G'$ exists, then to prove edge $uv$ (wlog assuming $uv \in E(G')$) is on a cycle, we simply get the shortest path from $v$ to $u$, then you just go $v\dots uv$ and we are done
- otherwise, we can use either
	- ear decomposition (above but idk)
	- using DFS we find a DFS tree
	- some weird algo
		- let $C$ be a cycle and rng the orientation of $C$
		- if every edges are oriented, done
		- pick $e$ as an unoriented edge which shares an edge with $e$, then one can find a cycle $C'$ containing $e$, and one oriented $C'$ to make stuff work
		- idk why this does not fail tho

directed graphs are
- weakly connected iff its resp. undirected is connected
- strongly connected iff for all $u,v\in V$, there exists a path from $u$ to $v$

**theorem**: given a (simple) undirected connected $G$, then
- there exists (simple) directed $G'$ with respundirected $G$ is strongly directed iff every edge is on a cycle

**proof**
- if $G'$ exists, 
- if every edge is on a cycle, we need an algo to "synchronize" these cycles
	- first, we see that there are no bridges on the graph
		- consider an edge $uv$, we prove that there is a way to go from $u$ to $v$ without having to go thru the edge
		- true, since $uv$ is on the cycle $uC_{1}vu$, and because definition, $uv$ can't be in $C_{1}$, so qed

## special graphs
- complete $K_{n}$
- cyclic $C_{n}$
- wheel $W_{n}$ ($C_{n}$ and a vertex that connects to all remaining vertices)
- cuboid $Q_{n}$
	- $V$ is the set of all $n$-bit binary strings
	- $uv\in E$ if they differs from each other by one bit
- biparte $K_{m,n}$
	- $V$ can be partitioned into $V_{1}$ and $V_{2}$ s.t. all edges are from a vertex in $V_{1}$ to another in $V_{2}$
	- $m=|V_{1}|,n=|V_{2}|$

**theorem**: $G$ is biparte iff it does not have odd-length cycles

**proof**
necessary is self-explanatory
let $G$ be a graph with no odd-length cycles
pick a vertex $v$ and let $d(v')$ be the min distance of a path from $v$ to $v'$
then $V_{1}=\{ v', 2|d(v') \}$, $V_{2}=\{ v', 2\not{|} d(v') \}$
- assuming there is some $a\in V_{1},b\in V_{2}$ with paths $vC_{1}a,vC_{2}b$ and $ab\in E$ => $|C_{1}|$ even, $|C_{2}|$ odd
- then one consider the cycle $vC_{1}abC_{2}v$, which is odd-length($1+|C_{1}|+3+|C_{2}|$) => qed

- planar graphs: graphs can be drawn on a plane with no intersecting edges (ykwim)

**theorem**: $G$ planar iff it does not have $K_{3,3}$ or $K_{5}$ homomorphic subgraph


