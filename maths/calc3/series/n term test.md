series $sa_{n}$ conv to $S$ then $\lim_{ n \to \infty }a_{n}=0$

**proof**
the limit = $\lim_{ n \to \infty } (S_{n+1}-S_{n})=S-S=0$

e.g. $\sum_{n=1}^\infty \sin(n^2)$
bUt cLeArLy lIm sIn(X^2) dOeS nOt eXiSt aS x tEnDs tO iNfInItY
stfu we gotta prove it here
assuming $\lim_{ n \to \infty }\sin(n^2)=0$, then
$$
\lim_{ n \to \infty } \sin((n+1)^{2})=\lim_{ n \to \infty } (\sin(n^{2})\cos(2n+1)+\cos(n^{2})\sin(2n+1))=0
$$
we must have $\lim_{ n \to \infty } \sin(2n+1)=0$ (since $\cos(n^2)$ must not conv to 0)
once again, then 
$$\lim_{ n \to \infty } \sin(2n+3)=\lim_{ n \to \infty } (\sin(2n+1)\cos(2)+\cos(2n+1)\sin(2)) =0$$
then $\cos(2n+1)=0$ => contradiction
=> this lim is not zero => div