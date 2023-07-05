
$I(a)=\int _{0}^{1} \frac{\ln(1-a^{2}x^{2})}{\sqrt{ 1-x^{2} }} \, dx$
- giả sử $a\geq0$
- $f(x,a)=\frac{\ln(1-a^{2}x^{2})}{x^{2}\sqrt{ 1-x^{2} }}$, $f'_{a}(x,a)=\frac{-2ax^{2}}{(1-a^{2}x^{2})\sqrt{ 1-x^{2} }}$ liên tục trên $[0,1)\times[0,1-\varepsilon]$ (với $0<\varepsilon<1$)
- khi $x\to 1$, $f \sim \frac{\ln(1-a^{2})}{\sqrt{ 2(1-x) }}$ có TP hội tụ (với mọi $|a|<1$)
- $f'_{a}\leq \frac{2}{\sqrt{ 1-x^{2} }}$ có TP hội tụ => tp h tụ đều với mọi $|a|<1$
- => $I'(a)=\int _{0}^{1} \frac{-2ax^{2}}{(1-a^{2}x^{2})\sqrt{ 1-x^{2} }} \, dx$ với mọi $|a|<1$
- => $I'(a)=\int _{0}^{1} -\frac{-2a}{(1-a^{2}x^{2})\sqrt{ 1-x^{2} }} \, dx$
- tính TP: $x=\sin t$ => $I'(a)=\int _{0}^{\pi/2} \frac{-2a}{1-a^{2}\sin(t)^{2}} \, dt=\int _{0}^{\pi/2} \frac{-2a}{\frac{1}{\sin ^{2}t}-a^{2}} \, \frac{dx}{\sin ^{2}t}$, đặt $u=\cot t$ => $I'(a)=\int _{0}^{+\infty} \frac{-2a}{u^{2}+1-a^{2}} \, du=-\frac{\pi a}{\sqrt{ 1-a^{2} }}$
- => $I(a)=\pi\sqrt{ 1-a^{2} }+c$, mà $I(0)=0$ => $I(a)=\pi(\sqrt{ 1-a^{2}}-1)$ với $|a|<1$
- xét riêng TH $a=1$ ($a=-1$ y hệt):
	- $I(1)=\int _{0}^{1} \frac{\ln(1-x^{2})}{x^{2}\sqrt{ 1-x^{2} }} \, dx$, đặt $x=\sin t$ => $I(1)=\int _{0}^{\pi/2} \frac{\ln \cos t}{\sin(t)^{2}} \, dx$$=(-\cot t \ln \cos t)|_{0}^{\pi/2}-\int _{0}^{\pi/2} -\tan t\cot t \, dt=-\pi$

