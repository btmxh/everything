- in the infinite dimension vecsp of all periodic fns on with one period $T=2\pi$, one takes some vectors (i.e fns) $f_{n}(x)=\cos nx, g_{n}(x)=\sin nx$
- since $g_{0}\equiv 0$ => we need to exclude $g_{0}$
- then, we look at the span of these vectors, i.e. $\text{span}\{ f_{n\geq 0}, g_{n\geq 0} \}$ we have

**theorem:** $\{ f_{n\geq 0}, g_{n>0} \}$ is LI
one can use the LI definition to prove this, but this is the normie way
instead, we use this inner product $\langle f,g \rangle=\frac{1}{\pi}\int _{-\pi}^{\pi} f(x)g(x) \, dx$, then these vectors are in fact **orthogonal** => LI

- since these vectors are orthogonal, one would like no make it **orthonormal** too, and by calculating the norms, one see that
	- $\|f_{0}\|=2$
	- $\|f_{n}\|= \|g_{n}\|=1$

=> the orthonormal basis is $\set{\frac{1}{\sqrt{ 2 }}, \cos x,\sin x, \cos 2x, \sin 2x, \dots}$, and if a fn $f$ has coords $(a_{0}\sqrt{ 2 },a_{1},b_{1},a_{2},b_{2}, \dots)$, then one can write $f(x)=\frac{a_{0}}{2}+\sum_{n=1}^{\infty} (a_{n}\cos nx+b_{n}\sin nx)$, i.e. the [[fourier]] series repr of $f$ (ik it's weird)
