given a complete graph $G(V, E)$ and a cost mapping $c: E\to [mc, \infty]$ (with $mc$ being the `min_cost` (usually $0$), $\infty$ denote that the edge is basically impossible to pass), find the cycle $v_{1}v_{2}\dots v_{n}v_{1}$ s.t. the total cost $C=f(v_{1}v_{2}\dots v_{n}v_{1})=c(v_{1}v_{2})+c(v_{2}v_{3})+\dots+c(v_{n}v_{1})$ min

## complete formulation
if one allows $c: E\to \mathbb{R}^{0+} \cup \{ \infty \}$, then one can make $G$ complete by letting $c(e)=\infty$ for all $e$ not originally in $E$

## naive bnb
fix the first vertex (it doesn't matter) as $v_{1}$
basically we have a incomplete path $P=v_{1}v_{2}\dots v_{k}$
=> we need another $n-k+1$ edges, so the ideal case for the full path would have total cost $g(P)=f(v_{1}\dots v_{k})+(n-k+1)mc$, done

## bnb2
the idea is we use this
```python
def extend_sol(sol):
	i, j = pick_best_edge_to_split()
	yield from sol_with_edge(i, j)
	yield from sol_without_edge(i, j)
```

the funny thing is that we find $i,j$ s.t. the $g$-value of paths yielded from `sol_without_edge` is big, which basically eliminate that in the case when `sol_with_edge` exits with a good result

hence, in `pick_best_edge_to_split`, we need to find the edge s.t.
- `sol_with_edge` may have a good result
- `sol_without_edge` have high g-value

one now consider the edge weight matrix thing:
![[Pasted image 20230906095749.png]]

our path is basically picking n numbers in the matrix s.t. the sum of the numbers are minimal + no nums in same rows/cols
ofc we need to pick a num in all rows, all cols, so we can *normalize* by finding the min value of each row and subtract (`r[i]`), and then doing the same shit for cols (`s[j]`)
> this does not change the path, but it change the lower bound, so keep track of that

adding all numbers, we find out that the subtracted amount is $\sum r[i]+\sum s[j]$ (81 in the example) => this is the lower bound

![[Pasted image 20230906100321.png]]
now we pick the best edge as some edge with 0, (3,6) for example:
- lower bound of the `sol_with_edge` remains as 0 (most ideal)
- lower bound of the `sol_without_edge` is the lower bound of the matrix after modifying the 0 to infty and normalize again
	- ![[Pasted image 20230906100501.png]]
	- (reduced 48 from the 3rd col)
	- => in the example: lower bound = 81 + 48

=> our strat:
- pick edge with 0
- such that sum of its 2 minimal "neighbors" (48 in this case) is max => keep track of the 2nd best entry in all rows and cols

```python
def pick_best_edge_to_split():
	coords = zip(range(n), range(n))
	coord, delta_lb = coords
	  # only taking 0-edges
	  .filter(x,y => matrix[x,y] == 0)
	  # max by sum of its minimal neighbors
	  .max_by(x,y => {
		  minr = matrix[x,_!=y].min()
		  minc = matrix[_!=x,y].min()
		  # this value is assigned to delta_lb
		  minr + minc
	  })
	return corord, delta_lb
```

and the original algo become
```python
# we also pass the lower bound value as `lb`
def extend_sol(sol, lb):
	lb += normalize()
	(i,j), delta_lb = pick_best_edge_to_split()
	yield from sol_with_edge(i, j, lb=lb)
	yield from sol_without_edge(i, j, lb=lb + delta_lb)
```
