the evolute is the set of all [[osculating]] centers of a [[curve]]

**remember to eliminate [[singular point]]**

## find?
trivial

e.g. $\frac{x^2}{a^2}-\frac{y^2}{b^2} = 1$
param: $\mathbf r(t)=(a\cosh t, b\sinh t) = \mathbf r''(t)$
$r'(t)=(a\sinh t, b\cosh t)$
$\|r'\|= a^2\sinh(t)^2+b^2\cosh(t)^2$
$\mathbf r' \times \mathbf r'' = ab$
=>evo.: $r(t) = (a\cosh t, b\sinh t) + \frac{(a^2\sinh(t)^2+b^2\cosh(t)^2)(-b\cosh t, a\sinh t)}{ab}$
simplifying, we get: $x(t)=\frac{a^2+b^2}{a}\cosh(t)^3$, $y(t)=-\frac{a^2+b^2}{b}\sinh(t)^3$

## properties

**theorem:** the [[tangent]] of the [[evolute]] is the [[normal]] of the [[curve]]

using [[arclen]] param.
we have $\mathbf c = \mathbf r + \Delta \mathbf r = \mathbf r + \rho \mathbf n$, where $\rho$ is the [[osculating]] radius, $\mathbf n$ is the [[normal]] (which needs to be correctly directed)

then: $\mathbf c' = \mathbf r' + \rho ' \mathbf n + \rho \mathbf n'$
because [[frenet-serret formulas]], 2d case, this reduces to 
$$
\mathbf c' = \rho' \mathbf n
$$
$\mathbf c'$ is the [[tangent]] vec of the [[evolute]], $\mathbf n$ is the [[normal]] of the [[curve]], qed

**corollary**: the [[evolute]] is the [[envelope]] of [[normal]] lines
(the theorem implies that the evolute is tangent to all normal lines)

**theorem: the [[arclen]] of an [[evolute]] arc (without [[singular point]]) is the difference between [[osculating]] radiuses of the endpoints**

since $dc=\mathbf n d\rho$, then $\|dc\| = \|n\| |d\rho| = d\rho$,
arclen of evo. arc = $\int_{t_0}^{t_1} \|dc\| = \int_{t_0}^{t_1} d\rho=\rho(t_1)-\rho(t_0)$

**theorem:** a curve is [[evolute]] of all its [[involute|involutes]]
this follow directly from the [[involute]] equation
