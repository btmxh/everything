basically backtracking for optimization

**problem**: find solution $S$ that minimize $f(S)$ in $D$
$D$ can be backtracked, i.e. $D \subset D^{b}$ and given incomplete heuristic $g: D^{b}\to \mathbb{R}$ s.t. if $d\in D$ has backtrack sequence $d_{1},d_{2},\dots,d_{k}=d$ then $f(d)=g(d_{k})\geq g(d_{i})$

> if maximize, we need $f(d)\leq g(d_{i})$

we caan modify the backtracking algo as follows
```python
record = INF
current_solution

# override invalid_bnb instead
def invalid(partial_sol):
	return g(partial_sol) >= record or invalid_bnb(partial_sol)

for solution in backtracking_recursive(invalid=invalid):
	record = g(solution) # or f(solution)
	current_solution = solution

return current_solution
```



