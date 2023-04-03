msb: sign bit (0 - positive, 1 - negative)
repr neg nums by the 2's complement of the corresponding pos nums

(-1 <-> 0xffffff)

value = unsigned value - $a_{n-1}2^n$ => value = uvalue mod 2^n

pos -> neg num => invert + plus 1
e.g.: 1 = 0x0001 => 0xfffe => 0xffff



