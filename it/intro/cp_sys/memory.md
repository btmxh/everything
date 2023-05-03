usage: store [[data]] and [[program]]
operations:
- read
- write
components:
- internal (bigger is more memory but slower)
	- ![[Pasted image 20230410161209.png]]
	- cpu can directly access internal [[memory]] with high speed, but has low capacity
	- using semiconductor memory: rom (read only mem), ram (random access mem)
	- back then, rom is sustained by some battery => one can discharge it to reset rom
	- two types:
		- main memory
		- cache
			- static, glued to the [[cpu]]
			- high af boys + low storage capacity (at most some MB)
	- sequential access vs random access
		- sequential access is $O(n)$ for an memory access => slow
		- random access is $O(1)$ => fast
- external
	- huge but slow


## address and content
memory can be indexed by addresses and everyone know this shit so i'm not wasting my time
- my prof said that u can modify addresses so there's that (ig he's talking at a memory cell)

e.g. how much ram can u fit onto a 32bit machine
(assuming that every address can be used, even `NULL`)
- `sizeof(size_t)=32/8=4` => u can only use at most 4GB of ram

