series in the form of $f(x)=a_{0}+\sum_{n=1}^{\infty}(a_{n}\cos nx+b_{n}\sin nx)$

this is what nxt talk about, but for more details, see [[intro]]

**theorem:** $f(x)$ [[uniconv]] if $sa_{n},sb_{n}$ [[abs conv]]
this can be easily proven with [[weierstrass m-test]]

one can determine the coeffs of this series by taking these definite integrals
- $a_{0}=\frac{1}{\pi}\int _{-\pi}^{\pi} f(x) \, dx$
- $a_{n}=\frac{1}{2\pi}\int _{-\pi}^{\pi} f(x)\cos nx \, dx$
- $b_{n}=\frac{1}{2\pi}\int _{-\pi }^{\pi}f(x)\sin nx \, dx$
- 