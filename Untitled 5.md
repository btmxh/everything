$\sum_{n=1}^{\infty}\frac{1}{1+u^{n}}$
- để chuỗi hội tụ thì cần $\lim_{ n \to \infty } \frac{1}{1+u^{n}}=0$ =>$\lim_{ n \to +\infty } |1+u^{n}|=+\infty$ =>$\lim_{ n \to \infty } |u|^{n}=+\infty$ => $|u|>1$
- với $|u|>1$ thì ta có $\frac{1}{1+u^{n}} \sim \frac{1}{u^{n}}$ là chuỗi cấp số nhân có $\left|\frac{1}{u}\right|<1$ nên hội tụ
- vậy chuỗi hội tụ với mọi $|u|>1$
	- nếu $u=\tan x$ thì $|u|>1 \iff \exists k\in \mathbb{Z}, \frac{\pi}{4}<x-k\pi< \frac{\pi}{2}$
	- nếu $u=\cot x$ thì $|u|>1 \iff \exists k\in \mathbb{Z}, 0<x-k\pi< \frac{\pi}{4}$
	- nếu $u=\ln x$ thì $|x|>1 \iff x\in (-\infty, \frac{1}{e}) \cup(e,+\infty)$
	- nếu $u=e^{ x }$ thì $|u|>1 \iff x>0$
