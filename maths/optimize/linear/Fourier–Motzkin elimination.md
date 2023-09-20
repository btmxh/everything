An elementary problem in LP is to check whether the system $Ax\geq b$ has a solution or not (then we can do the optimizing)
The simplex method also requires a vertex to start from, so finding an arbitrary solution may help.

## Process
- If all coefficients wrt the element $x^{i}$ is 0 (i.e. $A_{i}=0$), we are done
- Otherwise, we can eliminate the variable $x^{i}$ as follows. For every row condition $A^{j}x\geq b^{j}$, if
	- $A^{j}_{i}=0$, then we are done
	- $A^{j}_{i}> 0$, then $A^{j}x-b^{j}=\sum _{i'\neq i} A^{j}_{i'}x_{i'}+A^{j}_{i}x_{i}-b^{j}\geq 0$ iff $x_{i}\geq \frac{1}{A^{j}_{i}}\left( b^{j}-\sum_{i'\neq i}A^{j}_{i'}x_{i'} \right)$, then put this ineq in group $I$
	- $A^{j}_{i}<0$ then $x_{i}\leq \frac{1}{A^{j}_{i}}\left( b_{j}-\sum\dots \right)$, then put this ineq in group $II$
- Then combine every pair $(a,b)\in I\times II$ into $RHS_{b}\geq RHS_{a}$, resulting in $|I|\times|II|$ new inequalities not involving $x_{i}$, then add the ineq from the $A^{j}_{i}=0$ ineqs to get the eliminated system.
- After solving the new system, one can get back $x_{i}$ by simply merging the ranges.
