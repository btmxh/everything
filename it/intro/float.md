a float can be repr as a triplet: $(R, M, E)$, its value is $V=MR^{E}$
- $R$: radix (2 => float, double; 10 => decimal)
- $\mathbf{M}$: mantissa, satisfies: $-R < M < R$, stored as fixed point format
- $E$: exponent

[ieee 754](https://en.wikipedia.org/wiki/IEEE_754) layouts
- single precision `float` (32 bit)
	![[Pasted image 20230403164849.png]]
- double precision `double` (64 bit)
	![[Pasted image 20230403164909.png]]
- extended precision `long double` (80 bit)
	![[Pasted image 20230403164918.png]]

and
- $M=(-1)^{S} \cdot \overline{1.m}$
- $E=e-b$, $b$: bias $2^{|e|-1}-1$ (denote $|e|$ the number of bits for $e$)
- => $V=(-1)^{S}\ 2^{e-b}\ \overline{1.m}_{2}$

e.g. $V=2$
- $e=E+b=128$
- $m=0$
- $S=0$
=>`float` repr: `0b0_10000000_000..(18 more)..00`

e.g. `e=0b1000001, m=1011_00..(15 more)..00, S=0, R=2`
- conversion: $e=129 \implies E=2, \overline{1.m}=1.1011_{2}, S=0$
- $V=2^{2}\ 1.1011_{2}=110.11_2=4+2+\frac{1}{2}+\frac{1}{4}=6.75$

e.g. $V=0.1$ (base 10)
- $E=e-b=-4 \implies e=123$
- $\overline{1.m}_{2}=1.6=1.10011001100110011001 1001_{2}$
- => $m=1001\ 1001\ 1001\ 1001\ 1001 \ 1001 \ 100$
- => `float` repr: `0b0_01111011_10011001100110011001100`

**NOTE:** the value range of $E$ in a `float` is $[-127,128]$ != the value range of a `i8`: $[-128,127]$

**special values**
- if $e=00..00_{(2)}, m=00..00_{(2)}$, then $V$ is either **positive zero** or **negative zero** (the sign bit decides the sign of zero)
- if $e=00..00_{(2)}, m\neq 00..00_{(2)}$, then $V$ is a [subnormal number](https://en.wikipedia.org/wiki/Subnormal_number)
- if $e=11..11_{(2)}, m=00..00_{(2)}$, then $V$ is either **positive infinity** or **negative infinity**
- if $e=11..11_{(2)}, m\neq 00..00_{(2)}$, then $V$ is `NaN`

e.g. in a `f32`, the smallest positive non-zero, non-`NaN` value is $2^{-126}$

## calc?