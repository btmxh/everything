algorithm can be thought of as a finite procedure
algos have inputs and may spit out outputs (one can consider the output as a passed by reference input)
algo are
- precise (i.e. computer don't need to figure what to do if it simply don't care about perf and such., in reality it does because muh cache locality, atomic, etc.)
- finite (i.e. algo that loops forever is useless)
- unique (aka pure, the behavior of the algo doesn't change if one doesn't change the input)
- general (one can plug in different inputs to solve different problems, so no `TODO()` allowed)

in algos, "variables" are not constant anymore, unlike in proofs (variables can still be shadowed in order to make things convenient, but it's still const)

## complexity
basically as the input $x$ approaches some $x_{0}$ (usually $n\to \infty$), we denote
- $f=o(g)$ iff $\lim_{ x \to x_{0} } \frac{f}{g}=0$
- $f=O(g)$ iff exists $C,M$ s.t. $\left|\frac{f}{g}\right|\leq C$ for $d(x,x_{0})\leq M$
- $f=\Omega(g)$ iff exists $C,M$ s.t. $\left|\frac{f}{g}\right|\geq C$ for $d(x,x_{0})\leq M$
- $f=\Theta(g)$ iff $f=O(g), \Omega(g)$

e.g. $\log n!=\Theta(n\log n)$
- either $n! \sim \sqrt{ 2\pi n }\left( \frac{n}{e} \right)^{n}$ => $n! = RHS \cdot \Theta(1)$ => $\log n! = \log(RHS)+\log \Theta(1)=n\log n+\Theta(1)=\Theta(n\log n)$
- or
	- $\log n! \leq \log n^{n}=n\log n$ => $\log n! = O(n\log n)$
	- $\log n! \geq \frac{n}{2}\log\left( \frac{n}{2} \right)\geq \frac{n\log n}{4}$ => $\log n! = \Omega(n\log n)$

## generation algo
next-based algo
```python
def generate(first, stop, gen_next):
	model = first() # or null if one want to init in the loop
	
	# stopping condition may depends on multiple params (atm there's only model, but things can get messy, so i will denote '...' as passing any param as needed)
	while not stop(...):
		model = gen_next(model)
		yield model
```

we can make gen_next a wrapper
```python
def gen_next(model):
	model = copy(model)
	gen_next_impure(model)
	return model

# now you can modify the model and not having to return model
def gen_next_impure(model)
```

e.g. binary strings of len n
```python
@cache
# returns a reference/pointer whatever
def last_zero_index(model):
	# & does not mean shit, except
	# as a note that this thing is a reference
	return &model.last(x => x == 0)

def first():
	return [0] * n

def stop(model):
	return last(model) == None

def gen_next_impure(model):
	&lz = last_zero(model)
	# change 0 to 1
	*lz = 1
	# from &lz[1], fill with 0
	[(&lz+1):].fill(0)
```

e.g. enum m-subsets of a set $S=\{ *0..<n \}$
```python
def last_incable(model):
	return &model.last_index(v, i => v == n-1-i)

def stop(model):
	return last_incable(model) == None

def gen_next(model):
	&li = last_incable(model)
	# cache this, since *li is gonna change
	n = *li
	[&li:].fill(&v, i => *v = n+1+i)
```

e.g. permutations of $0..<n$
```python
def last_inc(model):
	return &model.last(_, i => model[i] < (model[i+1] ?? -INF))

def stop(model):
	return last_inc(model) == None

def first():
	return range(n)

# example (+1): 362541
def gen_next(model):
	# ln -> 36[2]541
	ln = last_inc(model)
	# swap_with = 3625[4]1
	swap_with = &model[lni+1:].min(v => v > model[lni])
	# after swap: 364521
	swap(&model[lni], swap_with)
	# basically sorting it too, but it's already in reverse order
	# after reverse: 364125
	reverse(model[lni+1:])
```

## backtracking
```python
# start from empty solution
def backtrack_recursive(solution=**empty**()):
	if **invalid**(solution):
		return
	if **complete**(solution):
		yield solution
	for new_solution in **extend_sol**(solution):
		yield from backtrack_recursive(new_solution)
```

the algorithm in https://en.wikipedia.org/wiki/Backtracking#Pseudocode is when `extend_sol` actually calls `generate` in the above section

e.g. binary seqs
```python
def empty() = []
def invalid() = false
def complete(solution) = len(solution) == n
def extend_sol(solution):
	return [] if complete(solution) else [solution + [0], solution + [1]]
```

e.g. queens
```python
# The board can be modeled using three dicts/arrays
# rows[i] -> col index of queen in row i
# diag1[i] -> true if diagonal x+y=i already has a queen, false otherwise
# diag2[i] -> true ... x-y=i (mod n)
type Board

def empty() = Board:
	rows = [None] * n
	cols = associate_with(range(0, n), False)
	diag1 = associate_with(range(0, 2n-2), False)
	diag2 = associate_with(range(1-n, n), False)

def invalid(s):
	# you can track x for O(1)
	y, x = with_index(s.rows.last(v => v != None))
	# we check (and assign) the diagonal and column
	d1 = &s.diag1[x+y]
	d2 = &s.diag2[x-y]
	c = &s.cols[y]
	defer *d1 = *d2 = *c = True
	return d1 or d2 or c
	
def complete(solution) = solution.count(None) == 0
def extend_sol(s):
	return [] if complete(s) else:
		# you can track x for O(1)
		x = index(s.rows.first(None))
		for y in range(n):
			s = copy(s)
			s.rows[x] = y
			yield s
```
