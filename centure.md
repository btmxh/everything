$$
\begin{align}
S_{n}&=\sum_{k=1}^{n} q^{k}\cos kx \\
	&=\sum_{k=1}^{n} q^{k} \mathrm{Re}\{ e^{ ikx } \} \\
&=\mathrm{Re}\left\{  \sum_{k=1}^{n} (qe^{ ix })^{k}  \right\} \\
&= \mathrm{Re}\left\{  \frac{1-(qe^{ ix })^{n+1}}{1-qe^{ x }}  \right\} \\
&=\mathrm{Re}\left\{  \frac{1}{1-qe^{ ix }}  \right\} -\mathrm{Re}\left\{  \frac{(qe^{ ix })^{n+1}}{1-qe^{ ix }}  \right\}=A-B_{n}
\end{align}
$$
- ta có $|B_{n}|\leq \frac{q^{n+1}}{|1-qe^{ x }|}\to 0$ khi $n\to +\infty$ nên $\lim_{ n \to \infty } S_{n}=\mathrm{Re}\left\{  \frac{1}{1-qe^{ ix }}  \right\}$
- mà $\frac{1}{1-qe^{ ix }}=\frac{1-qe^{ -ix }}{(1-qe^{ ix })(1-qe^{ -ix })}=\frac{1-q(\cos x-i\sin x)}{q^{2}-2q\cos x+1}$ => chuỗi bằng $\frac{1-q\cos x}{q^{2}-2q\cos x+1}$

xét $f(x,y)=ye^{ -yx }$ trên $[0, +\infty)\times[y_{0}, +\infty]$ có
- $f'_{y}(x,y)=e^{ -yx }-xye^{ -yx }=e^{ -yx }(1-xy)$
- $f'_{y}=0$ khi $y=\frac{1}{x}$, vẽ bbt suy ra đạt cực đại nên có
	- nếu $\frac{1}{x} \leq y_{0}$ thì $f$ giảm theo y nên $f(x,y)\leq f(x,y_{0})=y_{0}e^{ -y_{0}x }$
- khi đó ta có $I(y)=\int _{0}^{\infty} ye^{ -yx } \, dx=\int _{0}^{1/y_{0}} f(x,y) \, dx+\int_{1/y_{0}}^{\infty} f(x,y) \, dx$
	- tp đầu có $f(x,y)=ye^{ -yx }\leq y$ => 
	- tp sau có $x\geq \frac{1}{y_{0}}$ => $\frac{1}{x}\leq y_{0}$ => dùng weierstrass: $f(x,y)\leq \frac{1}{x}$ và có $\int _{1/y_{0}}^{\infty} \frac{1}{x} \, dx=$
- 

e.g. $I(y)=\int _{0}^{\pi} \ln(1+y\cos x) \, dx$
- nếu $y=0$ => $I(0)=0$
- nếu $y>1$ => $I(y)$ không xác định vì $1+y\cos x < 0$ trên một khoảng
- dễ thấy $I(y)$ chẵn => ta chỉ xét $y\in (0, 1]$

- ta có $\ln(1+y\cos x)=\int _{0}^{y} \frac{\cos x}{1+t\cos x} \, dt$ => $I(y)=\int _{0}^{\pi} \int _{0}^{y} \frac{\cos x}{1+t\cos x} \, dt \, dx$
- để đối thứ tự lấy tp:
	- nếu $0<y<1$, ta có hàm số $f(x,t)=\frac{\cos x}{1+t\cos x}$ liên tục trên $[0,\pi]\times[\varepsilon, 1-\varepsilon]$ (với mọi $\varepsilon>0$) nên là tích phân xác định => tính được ra $I(y)=\pi \ln \frac{1+\sqrt{ 1-y^{2} }}{2}$

- th $y=1$ tính riêng:
	- ta có $t=\tan \frac{x}{2}$ => $\ln(1+\cos x)dx=\frac{2}{1+t^{2}}\ln\left( 1+ \frac{1-t^{2}}{1+t^{2}} \right)=\frac{2(\ln 2 - \ln(1+t^{2}))}{1+t^{2}}$
	- => $I(y)=\int _{0}^{\infty} \frac{2\ln 2}{1+t^{2}} \, dt-2\int _{0}^{\infty} \frac{\ln(1+t^{2})}{1+t^{2}} \, dt$
		- tp đầu bằng $\pi \ln 2$
		- tp sau cho $t=\tan x$ (coi như đây là biến $x$ mới) => $I_{2}=-4\int _{0}^{\pi/2} \ln|\cos x|dx$
		- ta có $-\frac{I_{2}}{4}=\int _{0}^{\pi/2} \ln(\cos x) \, dx=\int _{0}^{\pi/2} \ln(\sin x) \, dx$ (đổi biến $x'=\frac{\pi}{2}-x$)
		- nên $-I_{2}=2\int _{0}^{\pi/2} \ln(\sin x\cos x)\, dx$$=2\int _{0}^{\pi/2} \ln\left( \frac{\sin 2x}{2} \right) \, dx$$=2\int _{0}^{\pi/2} \ln(\sin 2x) \, dx-\pi \ln 2$$=\int _{0}^{\pi} \ln(\sin u) \, du-\pi \ln 2$$=2\int _{0}^{\pi/2} \ln(\sin u) \, du-\pi \ln 2=-\frac{I_{2}}{2}-\pi \ln 2$
		- => $I_{2}=\pi \ln 2$
	- vậy $I(1)=\pi \ln 2-2\pi \ln 2=-\pi \ln 2$
