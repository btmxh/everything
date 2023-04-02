$(f*g)(\tau)=\int_{-\infty}^{\infty} f(t)g(\tau-t)dt$
**discrete** ver.: $(a*b)_{n}=\sum_{k=k_{0}}^{n-k_{0}}a_{k}b_{n-k}$ ($k_{0}$ usually is 0 or 1)

## convo theorem
$$
\int_{-\infty}^{\infty}(f*g)(\tau)d\tau=\int_{-\infty}^{\infty}f(x)dx \int_{-\infty}^{\infty} g(x)dx 
$$
**proof**
$$
LHS=\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} f(t)g(\tau-t) dt d\tau = \int_{-\infty}^{\infty}\int_{-\infty}^{\infty} f(t)g(\tau-t) d\tau dt = \int_{-\infty}^{\infty}dtf(t)\int_{-\infty}^{\infty} g(\tau-t) d\tau = RHS
$$

**discrete** ver: $\sum_{n=0}^{N}(a*b)_{n}=\sum_{n=0}^{N}a_{n}\sum_{n=0}^{N}b_{n}$
if one want $N=\infty$ ([[series]]), you need to make $sa_{n}, sb_{n}$ [[abs conv]]