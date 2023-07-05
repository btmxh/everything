osc. circle is the extension of [[tangent]] for 2nd derv. (lines has null 2nd derv., so we now need a circle)

**NOTE:** only exists for [[singular point|non-singular points]]

## find osc. center
from the [[curvature]] section, it's common knowledge that $R = \frac1\kappa$
to find the direction from $\mathbf r$ to the osc. center, one would use the [[normal]] vector, which can be found dep on the kind of curve we're investigating in

the problem is now which direction do we go (we only know the direction is parallel to the [[normal]] vector)

denote the to osc. center vector (= osc center - $\mathbf r$) by $\Delta \mathbf r$, then the center can be calc. as $\mathbf c = \mathbf r + \Delta \mathbf r$

to find the direction, there are multiple intuitive methods
- convexity of $y=f(x)$
- physics thing ($\mathbf r'' \cdot \Delta \mathbf r \ge 0$)

we will use the physics thing
**observation**: accel. always point "towards" the osc. center ($\mathbf r'' \cdot \Delta \mathbf r \ge 0$) (centripetal acceleration is a thing)
the reason stems from the convexity thing but no one cares

let $\Delta \mathbf r = \frac s {\|\mathbf r'\|\kappa}(-r'_y, r'_x)^T$, $s$ be the sign variable
then $\mathbf r'' \cdot \Delta \mathbf r = \frac s {\|\mathbf r'\|\kappa} r' \times r''$ => $s = sgn(\mathbf r' \times \mathbf r'')$

now, sub the [[curvature]] formula: $\Delta \mathbf r = \frac{sgn(\mathbf r' \times \mathbf r'')\|r'\|^2(-r'_y, r'_x)}{\|\mathbf r' \times \mathbf r''\|}$
eliminating the absolute value sign
$$
\Delta \mathbf r = \frac{\|\mathbf r'^2\|(-r'_y, r'_x)}{\mathbf r' \times \mathbf r''}
$$

if $y=f(x)$, then 
$$\Delta \mathbf r = \frac{(1+y'^2)(-y', 1)}{y''}$$
or
$$
\Delta x = -\frac{y'(1+y'^2)}{y''}, \Delta y = \frac{1+y'^2}{y''}
$$

e.g. $x^{3}+y^{4}=2$ at $(1,1)$
let $y=(2-x^{3})^{1/4}$ then $\Delta\mathbf{r}=\frac{(1+y'^{2})(-y', 1)}{y''}$
with $y'(1)=-\frac{3}{4}, y''(1)=-\frac{51}{16}$... => $\mathbf{r}=\frac{25\left( \frac{3}{4},1 \right)}{-51}+(1,1)$ => ...




## evolute

e.g. $y=x^{2}$
$\mathbf{\Delta r}=\frac{(1+4x^{2})(-2x,1)}{2}$ => $\mathbf{C}(x)=(x,x^{2})+\frac{1+4x^{2}}{2}(-2x,1)=\left( -4x^{3},3x^{2}+\frac{1}{2} \right)$