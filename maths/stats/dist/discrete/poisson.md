consider an event that happens randomly (telephone calls, atomic decay) over time, and one consider the number of times $X$ that it happens over a period of time, one can use the poisson [[dist]] to model this
$p(X)=\frac{e^{ -\mu }\mu^{x}}{x!}$
the factor $e^{ -\mu }$ is simply a scaling factor (to make $\sum_{n=0}^{\infty} p(x)=1$), and $\mu$ is the expected value (as well as its variance!) of $X$
the [[mgf]] of this is $M_{X}(t)=\sum_{x=0}^{\infty} \frac{e^{ tx-\mu }\mu^{x}}{x!}=e^{ -\mu }\sum_{x=0}^{\infty}\frac{(e^{ t }\mu)^{x}}{x!}$$=e^{ -\mu }e^{ e^{ t }\mu }=e^{ \mu(e^{ t }-1) }$

then, the sum of two poissons is $M_{X_{1}+X_{2}}=e^{ (\mu_{1}+\mu_{2})(e^{ t }-1) }$, which is another poisson with mean $\mu_{1}+\mu_{2}$
