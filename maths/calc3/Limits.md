(some new notations i made up in class xd)

## def of limits
Suppose we have two topological spaces $X$ and $Y$

Let $f: X' \to Y'$, where $X'\subset X, Y' \subset Y$ 
(e.g. $f(x)=\frac{1}{x}$ is $\mathbb{R}^{*} \to \mathbb{R}$)

If there is some value $y \in Y$ such that **for any neighboorhood $N_{Y} \subset Y'$ of $y$**, there **exists some neighborhood $N_{X} \subset X'$ of $x_{0}$** such that $f$ maps $N_{X}'=N_{X} \setminus \{ x_{0} \} \subset X'$ to a subset of $N_{Y}$, $y$ is called **A** limit of $f(x)$ as $x$ approaches $x_{0}$.

if one can prove that the limit is unique (not true for general topological spaces), one can write $\lim_{ x \to x_{0} } f(x)=y$

- this makes you wonder, *should the limit expression be a set? the set of all limits of $f(x)$ as x tends to $x_{0}$?*
- and then you suddenly remember the thing called **subsequential limits** (which can be defined NOT USING subsequences), and think that maybe they could be useful after all
- what if we combine the two thought to introduce a concept named "**the limit set**", denoted $\text{Lim}_{x\to x_{0}} f(x)$, which is the set of **all subsequential limits of $f(x)$ as $x$ tends to $x_{0}$**?

## sublims and condlims
- one problem with using subsequential limits directly is the fact that in general topological spaces, sequential limit and neighbor limit is not the same thing
- so, we need to remodel sublims into something else that is somewhat more "neighbory", which i called the conditional limits

## condlims
$y$ is a sublim of $f(x)$ as $x\to x_{0}$ wrt to a subset $X''$ of $X'$ iff for every neighborhood $N_{Y}$ of $y$, one can find some neighborhood $N_{X}$ of $x_{0}$ such that $N'_X=N_{X}\cap X''\setminus \{ x_{0} \} \subset X'$ and $f$ maps $N_{X}'$ to a subset of $N_{Y}$

e.g. $X=Y=\overline{\mathbb{R}}, Y'=[-1,1]$, find all condlims of $f(x)=\sin x$ as $x\to \infty$ when
- $X'=\mathbb{R}$, we will consider some cases
	- if $|y|>1$, then there exists some neighborhood $N_{Y}$ of $y$ that does not intersect the set $[-1, 1]$ => $f$ can't map some nonempty set $N_{X} \setminus \{ x_{0} \}$ to $N_{Y}$
	- if $|y|\leq 1$, then one can simply pick $X''=\arcsin(y)+\mathbb{Z}\tau$, then for any neighborhood $N_{Y}$ of y (which must have $y \in N_{Y}$) all neighborhood $N_{X}$ of $\infty$, i.e. something like $[a, +\infty]$ or $(a, +\infty]$ will have $N'_{X} \subset X''$ and therefore $f$ maps $N'_{X}$ to $\{ y \}$, which is a subset of $N_{Y}$

## the Limit
unlike regular $\lim$s, the $\text{Lim}$ does not yield a single value (and fail if the value does not exist or it is not unique, so bad omegalul). instead, its output is the set of all condlims, which may be $\emptyset$, the set with only one element (aka the regular lim) or $Y$ itself

the notation will be $\text{Lim}_{x\to x_{0}}f(x)$
to denote the set of all condlims wrt some set $X''$, one can simply add the condition like so: $\text{Lim}_{x\to x_{0}, x\in X''}f(x)$, this can also be done for arbitary conditions, i.e. $\text{Lim}_{ n \to \infty, n \text{ even} } \sin(n\pi)$

## back to the real world (or complex idk)
originally, i didn't intend to go as far as to the world of topology just to define the Limit, but the concept of $\lim_{ x \to \infty }$ is not defined in metric spaces.

now that's all out of the way, we have some rigorous definition for the Limit, we can now do stuff in the real world

**Theorem**: in [fc space](https://en.wikipedia.org/wiki/First-countable_space), condlims and sublims are equivalent
- sublim is condlim
	- consider a seq $x_{n}$ conv to $x_{0}$ and $f(x_{n})$ conv to $y$, then by choosing $X''=\{ x_{n}, n \in \mathbb{Z}_{+} \}$, $f(x)$ conv to $y$ wrt $X''$
- condlim is sublim
	- $\overline{\mathbb{R}}$ is first-countable:
		- $x_{0} \in \mathbb{R}$, then $N_{i}(x_{0})=B\left( x_{0}, \frac{1}{i} \right)$
		- $x_{0}=+\infty$, then $N_{i}(x_{0})=[i, +\infty]$
		- $x_{0}=-\infty$, then $N_{i}(x_{0})=[-\infty, -i]$
	- now we will use the $N_{i}$ to our advantage. because fc, every neighborhood $N_{X}$ of $x_{0}$ is contained in some $N_{i}(x_{0})$
	- now suppose $y$ is a condlim of $f(x)$ as $x\to x_{0}$ wrt $X''$, which means that for every $N_{Y}$ we have some $N_{X}$ bla bla => there is some $i\in \mathbb{Z}_{+}$ s.t. $N_{i}(x_{0}) \subset N_{X}$ => pick $x_{i} \in N_{i}(x_{0}) \subset N_{i-1}(x_{0}) \subset\dots$ (wlog assuming $N_{m} \subset N_{n}$ for $m>n$)
	- then $f(x_{n})$ conv to $y$ as $n \to \infty$, since for every $N_{Y}$ we have some $i$ such that for all $n>i$, $x_{n} \in N_{n}(x_{0}) \subset \dots \subset N_{i}(x_{0})$ and $f(x_{n}) \in N_{Y}$ (topological def of limits for sequences)

- now, we know for sure that what other people said about sublims has to be true, MUST be true for our beloved condlims in the context of first-countable space (which is basically everything that matters). HOWEVER, it's a terrible way to prove results, since that's just covering the ugly case analysis with our beautiful Limit, we need to prove those things ourselves!
- fuck FC spaces mean that we still need to touch $\mathbb{N}$, this is so sad can we get an F in the chat

**Theorem**: $\text{Lim}_{x\to x_{0}} f(x)$ is closed in FC spaces
(why tf am i still doing topological bullcrapery ffs)
fuck u see here: https://math.stackexchange.com/questions/672000/the-set-of-subsequential-limits-is-closed and use the above theorem
i'm not doing sequence analysis b\*tch

**Theorem:** Let $f_{1}, f_{2}, \dots, f_{n}$ be fn from $X$ to $Y$, $g$ is a fn that's cont on $Y^{n}$ ($X,Y$ are subsets of $\mathbb{R}$), then:
- 1. $\text{Lim}_{x\to x_{0}}(f+g)(x) \subset \text{Lim}_{x\to x_{0}}f(x)+\text{Lim}_{x\to x_{0}}g(x)$, this also works for mul and div (with != 0 conds ofc)
- 2. $\text{Lim}_{x\to x_{0}} kf(x)=k\text{Lim}_{x\to x_{0}}f(x)$ (we can say that $0 \times \infty=0$ here skull)

**Proof**
- to prove 1., let $L$ be a condlim of $f(x)+g(x)$ as $x\to x_{0}$ wrt $X''$, then $\boxed{\text{Lim}_{x\to x_{0}, x\in X''}=\{ L \}}$ take $L_{1}\in \text{Lim}_{x\to x_{0}, x \in X''} f(x)$, then it's a condlim of $f(x)$ as $x\to x_{0}$ wrt $X'''\subset X''$
	- hence, wrt $X'''$, one basically have $\lim_{ x \to x_{0} }f(x)=L_{1}, \lim_{ x \to x_{0} }(f+g)(x)=L$, now using L limits, one can easily verify that $\lim_{ x \to x_{0} }g(x)=L-L_{1}$ => qed
	- but imagine using normie limits here
	- take $L_{2} \in \text{Lim}_{x \to x_{0}, x\in X'''} g(x)$, we will now prove that $L_{1}+L_{2}$ is a condlim of $(f+g)(x)$ wrt $X'''$
	- for all neighborhood $B(L_{1}+L_{2}, \varepsilon)$ of $L_{1}+L_{2}$, using the definition of condlims, one can find neighborhoods $N_{1}, N_{2} \subset X'''$ such that $f$ maps $N_{1}$ to some subset of $B\left( L_{1}, \frac{\varepsilon}{2} \right)$, $f$ maps $N_{2}$ to $B\left( L_{2}, \frac{\varepsilon}{2} \right)$ => $f+g$ maps $N_{1}\cap N_{2}$ to some subset of $B\left( L_{1}, \frac{\varepsilon}{2} \right) + B\left( L_{2}, \frac{\varepsilon}{2} \right) \subset B(L_{1}+L_{2}, \varepsilon)$, qed (special handling for infinities fuck)
	- hence, $L_{1}+L_{2}$ must be $L$ => $L \in \text{Lim}_{x\to x_{0}}f(x)+\text{Lim}_{x\to x_{0}}g(x)$, qed
- to prove 2, it's trivial as fuck bruh, just use the same $X''$, divide the $\varepsilon$ thing by $k$ (or if $k=0$ it's not even a fucking question)

**Theorem**: if $f(x)\leq g(x)$ for all $x$, then $\text{Lim}_{x\to x_{0}}f(x) \leq \text{Lim}_{x\to x_{0}}g(x)$
**Proof**
- we have $\text{Lim}_{x\to x_{0}}g(x) \subset \text{Lim}_{x\to x_{0}}f(x)+\text{Lim}_{x\to x_{0}}(g-f)(x)$
qed is equiv to proving the 2nd Lim is nonneg, or equivalently the special case when $f(x)=0$ for all x
- consider some value $L<0$, then there is a neighborhood $N$ of $L$ that does not intersect $[0, +\infty)$ => bla bla qed

**Theorem**: in $Y=\overline{\mathbb{R}}$, $\text{Lim}_{x\to x_{0}}f(x)$ is never empty
**Proof**
bla bla bla

## application: proving [[uniconv]]
e.g. prove $\sum_{n=1}^{\infty} \arctan \frac{2x}{x^{2}+n^{2}}$ not uniconv on $\mathbb{R}$
use [[cauchy]]:
$$
\begin{align}
&\underset{m,n\to \infty}{\operatorname{Lim}} \sup_{x\in \mathbb{R}} \left|\sum_{k=n+1}^{m}\arctan \frac{2x}{x^{2}+k^{2}}\right|  \\
\supset &\underset{m,n\to \infty, m=2n}{\operatorname{Lim}} \sup_{x\in [0, +\infty]} \sum_{k=n+1}^{2n} \arctan \frac{2x}{x^{2}+k^{2}}\\
\geq &\underset{n\to \infty}{\operatorname{Lim}} \sum_{k=n+1}^{2n} \arctan \frac{2n}{n^{2}+k^{2}}  \\
\geq &\underset{n\to \infty}{\operatorname{Lim}} n \arctan \frac{2}{5n}=\left\{  \frac{2}{5}  \right\}
\end{align}
$$
due to the last theorem, all Lims here are non-empty sets => the first Lim can't be $\{ 0 \}$ => not uniconv

- truly an amazing proof, no signs of epsilon and delta, all in one super duper linear expression