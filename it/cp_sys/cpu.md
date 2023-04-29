control the computer (no other thing can do this, including GPU, etc.)

- the brain of the system: control everything of the computer system
- [[it/intro/process]] [[data]]
- operations
	- recv instruction from main [[memory]]
	- translate the instruction into microcode/etc.
	- recv operands (`eax, rcx, etc.` idk)
	- execute the operation
	- return value
	- components
	- ![[Pasted image 20230410154723.png]]

## speed and frequency

- speed of cpu: measured in MIPS (million instructions per sec) => hard to benchmark
- clock cycle, rate (chu kì, tần số xung nhịp)
	- clock is used to synchronize the cpu => clock rate (partially) determine how fast the cpu can do stuff
	- then one can use the clock rate to measure time in cpu
- ![[Pasted image 20230410160224.png]]
- $T_{0}$: the clock cycle => every instruction approx. takes $kT_{0}$ time, where $k$ is an integer and the clock rate $f_{0}=\frac{1}{T_{0}}$: the rate of cpu
	- e.g. pentium iv 2GHz => $f_{0}=2\cdot 10^{9} Hz, T_{0}=0.5ns$
	- 