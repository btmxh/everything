given a sys of eq in the form
$\mathbf F(\mathbf y, \mathbf z) = 0$

where $\mathbf F: \mathbb{R}^{n+m} \to \mathbb{R}^m$ is cont. diff., fix $y_0 \in \mathbb{R}^n, z_0 \in \mathbb{R}^m$

the jacobian of $\mathbf F$ can be split into two submatrices, denoted $\mathbf F'_y$ and $\mathbf F'_z$ (note that $\mathbf F'_z$ is a square matrix), then:

**STATEMENT:**
if $F'_z(y_0, z_0)$ is invertible, then there exists a neighborhood $N$ of $(\mathbf y, \mathbf z)$ and a function $\mathbf G: N \to \mathbb{R}^m$ such that $\mathbf F(\mathbf y, \mathbf G(\mathbf y)) = 0$ for every $y\in N$

the derivative of $\mathbf G$ at $(\mathbf y_0, \mathbf z_0)$ can be found using implicit differentiation $\mathbf G' = -\mathbf F_{z}^{'-1}F'_y$


