## linear
if $f(x)=cx$ is linear, then $\nabla f=c$ at every $x$
also, level sets of $f$: $L_{\alpha}(f)$ are hyperplanes $cx=\alpha$, which are all parallel to each other
hence, one can use "*geometric* gradient descent":
- draw $D$, $c$ and the level curve $L_{\alpha}(f)$ as the hyperplane $cx=\alpha$
- take arbitary $x\in D$ and draw a hyperplane $L$ passing through $x$ and parallel to the above hyperplane
- move $L$ in the same (max) or opposite (min) until $L$ barely touches $D$, the intersection(s) is/are the global optimizers.
![[Pasted image 20230919114439.png]]
