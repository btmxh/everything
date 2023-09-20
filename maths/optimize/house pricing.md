Feature matrix $A$, $A^{i}_{j}$ is the j-th feature of the i-th house
Weight vector $x$: $x^{T}a$ is the expected price by our model with features $a$
Price vector $y$, $y^{i}$ is the price of the i-th house

The error of the i-th house is $\varepsilon^{i}=y^{i}-x^{T}(A^{i})^{T}=y^{i}-A^{i}x$
Summing stuff up: $E=\frac{1}{2N}\sum_{i}(y^{i}-A^{i}x)^{2}$