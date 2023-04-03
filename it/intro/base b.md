b digit with values from 0 to b-1
n digits => $b^n$ values
blabla

## conversion
### base b -> base 10
$A=(a_{n-1}...a_1a_0.a_{-1}a_{-2}...a_{-m})_b = \sum_{k=-m}^{n-1}a_kb^k$

### base 10 -> base b
1. convert int part: spam divisions and take residues (reverse order)
2. convert frac part: spam multiplications and take floors (same order)

### base 2 <-> base 8, 16
group/expand 3/4 digits from the decimal point


