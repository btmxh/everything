**def**: a finite seq of commands/statements to instruct sth to solve a program, it's a **method** to solve a [[problem]]
e.g. find max of an `Iterable<number>`
1. let the temp max be the first num
2. if iterable no longer yields, go to step 5
3. compare the following number with the temp max (if greater than reassign max to this value)
4. repeat step 2
5. return the temp max

**"characterisitics"**
- scope of problem
	- input/output
- basic char.
	- definiteness (no ambiguity in the steps)- 
	- finiteness (code is finite, must stop after some finite time)
- high-level, luxury bs
	- efficiency
	- generality

## algo repr
one typically repr algos using these 4 langs
- natural lang
	- easy to use
	- long
	- not concise, one can't see the ideas clearly
- diagram lang (ew)
	- use nodes and "arcs" to repr the algo
	- start/end node: top and bottom rsptvly, **round shape**
	- input/output node: parallelograms
	- rhombus node: conditional, branches into two new nodes (or more idk)
	- ![[Pasted image 20230515162702.png]]
- pseudocode
	- use standardized statements
	- still somewhat uses natural langs
		- still uses math eqs
		- procedural
	- statement kinds
		- assignment: ``` `variable` := `value` ```
		- branching: ```if (`cond`) then (`action`) [else (`action`)] ``` 
		- loop, jump
			- ```while cond do stuff```
			- ```repeat stuff until cond```
			- ```for var <- first value to last value do stuff```
- programming lang
	- have a syntax, with complicated structures
	- many types

## useful algos
- recursive
- heuristic
	- use "approximations" to speed up the algorithm
	- these approxs can be a intuitive assumption, numerical approximation, randomized approximations, etc.
- some other useful algos
	- number theoretic
		- swap
		- prime, prime factoring
		- find gcd, lcm, fraction
		- perfect nums
	- seqs
		- i/o seq
		- accumulate seq (sum, max, min)
		- sort
		- 
		- 