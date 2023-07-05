## motivation
- rewrite unix for many archs => can't use asm, need new lang
- born in bell lab of AT&T
	- initial: 1970, complete: 72
	- based on BCPL & B
	- BWK & DR
- props
	- system lang
	- lenient
	- strong in many kinds of processing
- usage extent
	- system programs
	- drivers
	- computer vision
- we use c89 wtf

## components
- char set
- keywords
- identifier
- data types
- const, var, function, expr, stmt, comments

### charset
- `[A-Za-z0-9]`
- +-\*/<>=
- `.,:; \t`
- `()[]{}`
- special symbols: `_?$&#^\!'"~.`...

### keywords
`interrupt` wtf is this shit xdddddd

### int lit
`0x` prefix for hex
`0` prefix for oct (bruh lmfao)

### bitwise
```
&: and
|: or
^: xor
~: not
<<: shift left (mul 2^n)
>>: shift right (div 2^n)
```
SHL/SHR is undefined for negative values
The first 4 is somewhat implementation-defined (more precisely, the impl can choose between 2's compl, 1's compl or sign-magnitude)

### weird operators
- comma (eval first and discard, eval second and return) (i.e. return last value and **NOT LAZY**)
- suffix inc/dec (`++x/--x/x++/x--`)
	- **NOTE:** prefix inc/dec have higher precedence than suffix inc/dec

**precedents** (left 2 right except noted otherwise)
- `->, .[], (), ++x, --x`
- `x++, x--, ~x, !x, +x -x *x &x () sizeof` (right-to-left)
- `* / %`
- `+ -`
- `>> <<`
- `< <= >= >`
- `== !=`
- `&`
- `^`
- `|`
- `&&`
- `||`
- `?:` (right-to-left)
- `a=b, a+=b, ...` (right-to-left)

## stdio.h
- MUST HAVE:
	- `int fread(char* buf, size_t size, size_t count, FILE* stream);`
	- `int fwrite(const char* buf, size_t size, size_t count, FILE* stream);`
	- `FILE* stdin, stdout, stderr;`
- formatted output
	- `int scanf(const char* fmt, ...);`
	- `int printf(const char* fmt, ...);`
- cool to know
	- `int getc(FILE* stream);`
	- `int ungetc(FILE* stream);`
	- `int [f]puts([FILE* stream = stdout], const char* str);`
- **Format string**
	- percent sign `%`
	- **prefixes** (only <C99)
		- `l`: only available for `%d/%o/%x/%X` => `[unsigned] long`
		- `L`: only available for `%f/%e` => `long double`
	- format flags
		- `-`: left-justified (default is right)
		- `+`: always include signs of number
		- ` `: prepend space for positive numbers
		- `0`: pad leading zeroes using `0` char
	- format types (prepended with `%` to look nice)
		- `%%`: raw percent sign
		- `%s`: string, `%c`: char
		- `%d`: decimal (TIL `%i` exists)
		- `%o`: octal (**UNSIGNED ONLY**)
		- `%x/%X`: hex/HEX (**UNSIGNED ONLY**)
		- `%f/F`: float
		- `%e/E`: scientific float (the case matters)
	- num pad
		- `%m.n`: left pad $m$, right-pad (float nums) $n$
		- e.g. $12.345$ with `%5.2f` => `   12.35`, `%05.2f` => `00012.35`
- `scanf` with `%s` terminates at whitespace characters, i.e.
```sh
echo "hello chat" | crepl 'char buf[100]; scanf("%s", buf); printf("%s\n", buf);'
> hello
```

## math.h
- we don't have `M_PI` in standard
- `if(x) if(y) z; else w;` is `if(x) {if(y) z; else w;}`
- 