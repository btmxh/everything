$A(-1,2,1)$ $x=t-1,y=2-\sin t,z=e^{ 2t }$
$A$ ung voi gia tri tham so $t=0$
$x'(t)=1,x''(t)=0$
$y'(t)=-\cos t=-1, y''(t)=\sin t=0$
$z'(t)=2e^{ 2t }=2,z''(t)=4e^{ 2t }=4$
=> do cong $\kappa= \frac{\sqrt{ \dots }}{(x'(t)^{2}+y'(t)^{2}+z'(t)^{2})^{3/2}}=\frac{\sqrt{ 32 }}{6^{3/2}}=\dots$

prove $I(y)=\int_{0}^{1} \frac{3^{x}y}{x^{2}+y^{2}} \, dx$ not cont at $y=0$
at $y=0$ => $I(0)=0$
take arbitary small $y=\varepsilon>0$
$I(\varepsilon)\geq \int _{0}^{1} \frac{y}{x^{2}+y^{2}} \, dx=\int _{0}^{1/y} \frac{1}{t^{2}+1} \, d\left( t=\frac{y}{x} \right)=\arctan \frac{1}{\varepsilon}$
=> $I(\varepsilon)$ -> $\frac{\pi}{2}$ as $y \to 0$

1.
mat $F(x,y,z)=x^{2}+y^{2}+z^{2}=5$ co vecto phap tuyen tai $A$ la $(F'_{x}, F'_{y}, F'_{z})=(2x,2y,2z) \parallel(x,y,z)=(2,1,0)$
mat phang $G(x,y,z)=x-2y+3z=0$ co vecto phap tuyen la $(1,-2,3)$
=> vecto tiep tuyen la $(2,1,0)\times(1,-2,3)=(a,b,c)$
=> tiep tuyen $x=2+at,y=1+bt,z=ct$, phap dien $ax+by+cz=2a+b$

2.
$I=\int _{D} (x^{4}-y^{4})dxdy$
do D doi xung qua $Oy$, $x^{4}-y^{4}$ la ham chan nen
$I=2\int _{D+} \, dx$ voi $D+$ la mien co $x^{2}+y^{2}\leq 1,x,y\geq 0$ => $D^{+}$ co vai tro x y nhu nhau => $I=0$

3.
$\iiint_{V} z^{2}dxdydz$, $x^{2}+y^{2}+z^{2}\leq 4$
let $x=r\sin u\cos v,y=r\sin u\sin v,z=r\cos u$
=> $I=\int _{0}^{2} r^{4}dr \int _{0}^{2\pi} \, dv \int _{0}^{\pi} \sin u\cos ^{2}u\, du$
=> $I=\frac{64\pi}{15}$

4.
$\iiint_{V} \frac{z^{3}dxdydz}{(x^{2}+y^{2}+z^{2})^{2}}=2\pi \int _{1}^{\sqrt{ 5 }} dz\int _{0}^{1} dr \frac{z^{3}r}{(r^{2}+z^{2})^{2}}$$=\pi \int _{1}^{\sqrt{ 5 }} z^{3}dz\int _{0}^{1}d\left( -\frac{1}{r^{2}+z^{2}} \right)$
$=\pi \int _{1}^{\sqrt{ 5 }} z^{3}\left( \frac{1}{z^{2}}-\frac{1}{z^{2}+1} \right) \, dz$$=\pi \int _{1}^{\sqrt{ 5 }} \frac{z}{z^{2}+1} \, dz=\frac{\pi}{2}\ln|z^{2}+1||_{1}^{\sqrt{ 5 }}=\dots$

5.
$I=\frac{1}{2}B\left( \frac{9}{4}, \frac{7}{4} \right)=\frac{\frac{1}{2}\Gamma\left( \frac{9}{4} \right)\Gamma\left( \frac{7}{4} \right)}{3!}=\frac{1}{12} \frac{5}{4} \frac{1}{4} \frac{3}{4} \Gamma\left( \frac{1}{4} \right)\Gamma\left( \frac{3}{4} \right)$$=\frac{5}{256} \frac{\pi}{\sin \frac{\pi}{4}}=\frac{5\pi}{128\sqrt{ 2 }}$

6.
$L: x+y=1$ => $y=1-x, dy=-dx$
=> $\int _{0}^{1} ((1-x)(3x-2)-(x+2(1-x))) \, dx$$=\dots$

7.
$\vec{AB}=(-1,2,2)$, do dai $3$
$\vec{\operatorname{grad}}u=\frac{(3,4y,-3z^{2})}{3x+2y^{2}-z^{3}}$ at $A$ $=\frac{(3,-4,-3)}{4}$
=> $\frac{\partial u}{\partial \vec{l}}=\frac{(-1,2,2)}{3}\cdot \frac{(3,-4,-3)}{4}=-\frac{17}{12}$

8.
xet $P(x,y)=8x^{3}-2y\ln(1+x^{2}y^{2})$,$Q(x,y)=5y^{4}-2x\ln(1+x^{2}y^{2})$
=> $Pdx+Qdy=8x^{3}dx+5y^{4}dy-2(ydx+xdy)\ln(1+x^{2}y^{2})$
$=2d(x^{4})+d(y^{5})+2d(xy)\ln(1+x^{2}y^{2})$
goi $F(z)$ la mot tich phan bat dinh cua $2\ln(1+z^{2})$ => $2d(xy)\ln(1+x^{2}y^{2})=d(F(xy))$
=> $Pdx+Qdy=d(2x^{4}+y^{5}+F(xy))$
=> $\vec{F}$ la truong the co ham the vi $u=2x^{4}+y^{5}+F(xy)$ nen cong bang $u(B)-u(A)=1$

9.
ostrogradsky, $V: 9x^{2}+4y^{2}+z^{2}\leq 1$
$I=\iiint_{V} 3(3x+2y+z)^{3}dxdydz=0$ do $F(x,y,z)=-F(-x,-y,-z)$ va V doi xung qua O


$\int _{L} f(x+y)(dx+dy)=\int _{0}^{a+b} f(u) \, du$

10
$\int _{C_{\alpha}} \frac{(x+y)dx+(y-x)dy}{x^{2}+y^{2}}$
$P(x,y)=\frac{x+y}{x^{2}+y^{2}}$ => $P'_{y}(x,y)=\frac{x^{2}+y^{2}-2y(x+y)}{(x^{2}+y^{2})^{2}}=\frac{x^{2}-2xy-y^{2}}{(x^{2}+y^{2})^{2}}$
$Q(x,y)=\frac{y-x}{x^{2}+y^{2}}$ => $Q'_{x}(x,y)=\frac{-x^{2}-y^{2}-2x(y-x)}{(x^{2}+y^{2})^{2}}=\frac{x^{2}-2xy-y^{2}}{(x^{2}+y^{2})^{2}}$
=> $P'_{y}=Q'_{x}$ lien tuc voi moi $(x,y) \neq (0,0)$
xet $L$ la hop cua $C_{\alpha}$ (chieu NKDH) va $C_{1}$ (chieu KDH)
ki hieu $C_{1}^{+}$ la $C_{1}$ theo chieu nguoc kdh va $C_{1}^{-}$ la $C_{1}$ nguoc kdh
khi do mien trong $D$ cua $L$ ko chua $(0,0)$ nen ta co the ap dung ct green => $\int _{L} Pdx+Qdy=\iint_{D} 0dxdy=0$
=> $\int _{C_{\alpha}} Pdx+Qdy+\int _{C_{1}^{-}} Pdx+Qdy=0$ => $\int _{C_{\alpha}} Pdx+Qdy$

$(x^{2}+y^{2})^{2}\leq 2xy^{2}, y\geq 0$
$x=r\cos t,y=r\sin t$
$0\leq r\leq 2\cos t\sin ^{2}t, 0\leq t\leq \pi$

$\int _{0}^{\pi} dt\int _{0}^{2\sin ^{2}t\cos t} rdr=2\int _{0}^{\pi} \sin ^{4}t\cos ^{2}t \, dt=2B\left( \frac{5}{2}, \frac{3}{2} \right)$

I.
1.
$x=e^{ t }\cos t,y=e^{ t }\sin t,z=t-1$
$x'=e^{ t }(\cos t-\sin t),y'=e^{ t }(\sin t+\cos t),z'=1$
tai $t=0$ => $x'=y'=z'=1$
=> tiep tuyen $x=1+t,y=t,z=-1+t$
phap dien $x+y+z=0$
2.
$\vec{AB}=(1,2,-2)$, $U'_{x}=-\frac{x}{\sqrt{ (x^{2}+y^{2}+z^{2})^{3} }},\dots$
=> $gradU= (-\frac{2}{27},-\frac{1}{27}, \frac{2}{27})$
=> $\frac{\partial U(B)}{\partial \vec{AB}}=\left( -\frac{2}{27},-\frac{1}{27}, \frac{2}{27} \right)\cdot \frac{(1,2,-2)}{3}=\dots=-\frac{8}{81}$
max $| \frac{\partial U}{\partial \vec{l}}|=|gradU|=\frac{1}{9}$ khi $\vec{l}$ cung phuong voi vecto gradU (cung huong hoac nguoc huong)

II.
1.
xet mien $D^{+}:0\leq x\leq y\leq 1$
=> $\int _{D} e^{ |x-y| } \, dxdy=2\int _{D^{+}} e^{ y-x } \, dxdy=2\int _{0}^{1} \, dy\int _{0}^{y} e^{ y-x } \, dx$$=2\int _{0}^{1} \,dy(e^{ y }-1)=2(e-2)$

2.
do $x,y,z$ cung vai tro nen $I=\iiint_{V} \frac{x^{2}+y^{2}+z^{2}}{1+x^{2}+y^{2}+z^{2}}dxdydz$
tham so hoa => $I=4\pi\int _{0}^{1} \frac{r^{4}}{1+r^{2}} \, dr=4\pi \int _{0}^{1} \left( r^{2}-1+\frac{1}{1+r^{2}} \right) \, dr$$=4\pi\left( \frac{1}{3}-1+\arctan 1 \right)=4\pi\left( \frac{\pi}{4}-\frac{2}{3} \right)$

III.
2.
AB: $y=1,x\in[1,2]$
BC: $x=2,y\in[1,2]$

$I_{AB}=\int _{1}^{2} x\arctan x \, dx$
$I_{BC}=\int _{1}^{2} \cot ^{-1} \frac{y}{2} \, dy=2\int _{\frac{1}{2}}^{1} \cot ^{-1}t \, dt$
$t=\frac{1}{x}$ => $dt=-\frac{dx}{x^{2}}$
=> $I_{BC} =2\int _{1}^{2} \frac{1}{x^{2}}\arctan x \, dx$
=> $I_{ABC}=\int _{1}^{2} \left( x+\frac{2}{x^{2}} \right)\arctan x \, dx$$=\int _{1}^{2} \arctan x \, d\left( \frac{x^{2}}{2}-\frac{2}{x} \right)$$=\left( \frac{x^{2}}{2}-\frac{2}{x} \right)\arctan x|_{1}^{2}-\int _{1}^{2} \left( \frac{x^{2}}{2}-\frac{2}{x} \right) \frac{1}{x^{2}+1} \, dx$
$=\arctan 2+\frac{3\pi}{8}-\int _{1}^{2} \frac{x^{3}-4}{2x(x^{2}+1)} \, dx$

tinh tich phan con lai:
$\int _{1}^{2} \left( \frac{1}{2} - \frac{1}{2(x^{2}+1)}- \frac{2}{x(x^{2}+1)} \right) \, dx$$=\frac{1}{2}-\frac{1}{2}(\arctan 2-\arctan 1)-\int _{1}^{4} \left( \frac{1}{t}-\frac{1}{t+1} \right) \, d(t=x^{2})$$=\frac{1}{2}-\frac{1}{2}\arctan 2 +\frac{\pi}{8}-\ln \frac{t}{t+1}|_{1}^{4}$$=\frac{1}{2}-\frac{1}{2}\arctan 2+\frac{\pi}{8} -\ln\left( \frac{8}{5} \right)$

=> $I=\frac{3}{2}\arctan 2 +\frac{\pi}{4}-\frac{1}{2}+\ln \frac{8}{5}$

IV.
1.
goc giua vecto phap tuyen voi $\hat{k}$ luon khong tu =>
$=\iint _{D} x^{2}(1-x^{2}) \, dxdy=\iint_{D} x^{2}dxdy-\iint_{D}x^{4}dxdy$
$\iint_{D}x^{2}dxdy=\frac{\pi}{4}$
$\iint_{D} x^{4}dxdy=\int _{0}^{1} r^{5} \, dr\int _{0}^{2\pi} \cos ^{4}t \, dt=\frac{1}{6}B\left( \frac{1}{2}, \frac{5}{2} \right)=\frac{\pi}{16}$
=> $I=\frac{3\pi}{16}$


I.
$F(x,y,z)=2x-e^{ -yz }+\arctan \frac{z}{y}$
=> $F'_{x}(x,y,z)=2$
$F'_{y}(x,y,z)=ze^{ -yz }-\frac{1}{y^{2}} \frac{1}{\left( \frac{z}{y} \right)^{2}+1}=ze^{ -yz }-\frac{z}{y^{2}+z^{2}}=0$
$F'_{z}(x,y,z)=ye^{ -yz }+\frac{y}{y^{2}+z^{2}}=-2$
=> phap tuyen $x=1+t,y=-1,z=-t$
tiep dien $x-z=1$

2.
$U'_{x}=\frac{x}{(1+\sqrt{ x^{2}+y^{2}+z^{2} })\sqrt{ x^{2}+y^{2}+z^{2} }},\dots$
tai A => $gradU=\left( \frac{1}{12}, \frac{1}{6}, -\frac{1}{6} \right)$
$O\vec{A}=(1,2,-2)$
=> $\frac{\partial U}{\partial \vec{OA}}(A)=\frac{(1,2,-2)\cdot(1,2,-2)}{3\cdot 12}=\frac{1}{4}$
max = $abs(gradU)=\frac{3}{12}=\frac{1}{4}$

II.
1.
$I=2\int _{-1}^{1} \, dx \int _{-1}^{x} (x-y) \, dy=2\int _{-1}^{1} \left( x(x-1)-\frac{x^{2}}{2}+\frac{1}{2} \right) \, dx$$=2\int _{-1}^{1} \left( \frac{x^{2}}{2}-x+\frac{1}{2} \right) \, dx$
$=\frac{8}{3}$

2.
$I=4\pi \int _{0}^{\sqrt{ 3 }} \frac{2r^{4}}{1+r^{2}} \, dr=8\pi \int _{0}^{\sqrt{ 3 }} \left( r^{2}-1+\frac{1}{r^{2}+1} \right) \, dr$$=8\pi \arctan \sqrt{ 3 }=\frac{8}{3}\pi^{2}$

III.
1.
2.

$\int _{0}^{\infty} \frac{3^{ax^{2}}-1}{x.3^{x^{2}}} \, dx$
$t=x^{2}$
	=> $I=\frac{1}{2}\int _{0}^{\infty} \frac{3^{at}-1}{t.3^{t}} \, dt=\frac{\ln 3}{2}\int _{0}^{\infty} \int _{-1}^{a-1} 3^{ut} \, du \, dt$
	htd do $a<1$ (luon pick dc $a<a_{0}<1$)
	=> $I=\frac{\ln 3}{2} \int _{-1}^{a-1} \, du \frac{1}{-u\ln 3}=-\frac{1}{2}\ln(1-a)$

$\int _{0}^{\infty} \frac{1-2^{a\sqrt{ x }}}{x.2^{\sqrt{ x }}} \, dx$
$t=\sqrt{ x }$ => $dx=2tdt$
=> $I=2\int _{0}^{\infty} \frac{1-2^{at}}{t.2^{t}} \, dt=2\int _{0}^{\infty} \left( \frac{e^{-yt\ln 2}}{t} \right)|_{1-a}^{1} \, dx$$=2\ln 2\int _{0}^{\infty} \int _{1}^{1-a} e^{ -yt\ln 2 } \, dy \, dt$
$=2\ln 2 \int _{1}^{1-a} \frac{1}{y\ln 2} \, dy=2\ln(1-a)$

we can switch order cuz $e^{ -yt\ln 2 }$ is cont on $[0, \infty) \times$ $[1-a,1]\subset[\varepsilon, 1]$ or $[1,1-a]$, depending on $a<0$ or $a\geq 0$

$-y\leq x^{2}+y^{2}\leq -x$
đặt $x=r\cos t,y=r\sin t$, $r\geq 0, 0\leq t\leq 2\pi$
=> $-\sin t\leq r\leq-\cos t$
=> $\frac{\pi}{2}\leq t\leq \pi$ thì $0\leq r\leq -\cos t$,
$\pi\leq t\leq \frac{3\pi}{2}$ thì $-\sin t\leq r\leq-\cos t$, (các giá trị còn lại của $t$ không có $r$ thỏa mãn)
=> $I=\int _{\pi/2} ^{\pi} \int _{0}^{-\cos t} r^{2}\, dr \, dt+\int _{\pi}^{3\pi/2} \int _{-\sin t}^{-\cos t} r^{2}\, dr \, dt$

I.
1.
$y=-\cosh t,x=\frac{1}{2}\sinh t$
=> $x'=\frac{1}{2}\cosh t,y'=-\sinh t,x''=\frac{1}{2}\sinh t,y''=-\cosh t$
=> $\kappa=\frac{|x'y''-y'x''|}{\sqrt{ (x'^{2}+y'^{2})^{3} }}=\frac{1}{2\sqrt{ (x'^{2}+y'^{2})^{3} }}$

tai $A(0,-1)$ co $t=0$ => $x'=-\frac{1}{2},y'=0$
=> $\kappa=4$

2.
$\int _{0}^{4} dy \int _{\sqrt{ 4y-y^{2} }}^{2\sqrt{ y }} f(x,y) \, dx$

mien lay tp: $D: 0\leq y\leq 4, \sqrt{ 4y-y^{2} }\leq x\leq 2\sqrt{ y }$ (do $2\sqrt{ y }\geq \sqrt{ 4y-y^{2} }$ voi moi $y\geq 0$)
=> $4-(y-2)^{2}\leq x^{2}\leq 4y, 0\leq x\leq 4$
=> $\frac{x^{2}}{4}\leq y$ va $|y-2| \geq \sqrt{ 4-x^{2} }$
ve hinh

II.
1.
$x=r\cos t,y=r\sin t$, $t\in[-\pi,\pi]$
=> $0\leq-\sin t\leq \cos t$ va $\cos t\leq r\leq 2\cos t$
=> $t\in\left[ -\frac{\pi}{4}, 0 \right]$, $\cos t\leq r\leq 2\cos t$
=> $I=\int _{-\frac{\pi}{4}}^{0} \, dt\int _{\cos t}^{2\cos t} \frac{1}{r^{3}}\, dr=\int _{-\pi/4}^{0} \frac{3}{2\cos ^{2}t} \, dt=\frac{3}{2}\tan(t)|_{-\pi/4}^{0}=\frac{3}{8}$
2.
$D$ la hinh chieu cua vat the len Oxz thi $D$ bi gioi han boi cac duong $x+z^{2}=0,2x+z^{2}=0,x^{2}+z=0,x^{2}+2z=0$(trong mat phang nay)
=> $V=\iiint_{V} dxdydz=\int _{-1}^{1} \, dy \iint_{D} dxdz=2\iint_{D} dxdz$
=> D: $\frac{z^{2}}{x}, \frac{x^{2}}{z}\in[-2,-1]$
dat $u=\frac{x}{z^{2}},v=\frac{z}{x^{2}}$ => song anh co jacobi $J^{-1}=\det\left( -\frac{z^{2}}{x^{2}}, \frac{2z}{x}, \frac{2x}{z}, -\frac{x^{2}}{z^{2}} \right)=-3$
=> $S(D)=\frac{1}{3}$
=> $V=\frac{2}{3}$

III.
1.
$I=\int _{0}^{2\pi} ((3(1-\cos t)+4)(1-\cos t)+5(t-\sin t)\sin t) \, dt$
$=\int _{0}^{2\pi} (7-10\cos t+3\cos ^{2}t+5t\sin t-5\sin ^{2}t) \, dt$
$=12\pi+5\int _{0}^{2\pi} t\sin t \, dt=2\pi$

2.
green, $D$ la mien trong cua $C$
$I=\iint_{D} n((x\sin y)^{n-1}\cos y-(y\sin x)^{n-1}\cos x)dxdy$
ma $\iint_{D}x^{n}\sin ^{n-1}y\cos ydxdy=0$ do ham le theo $x$ neu n le, le theo $y$ neu $n$ chan
=> dpcm

IV.
$div F=2x\sqrt{ y^{2}+z^{2} }$
lay $D$ la hinh chieu cua $V$ len $Oyz$: $y^{2}+z^{2}\leq 4$
=> $I=\iiint_{V} 2x\sqrt{ y^{2}+z^{2} }dx=\iint_{D} \int _{0}^{\sqrt{ 1-\frac{y^{2}+z^{2}}{4} }} 2x\sqrt{ y^{2}+z^{2} } \, dx \, dydz$$=\iint_{D} \left( 1-\frac{y^{2}+z^{2}}{4} \right)\sqrt{ y^{2}+z^{2} }dydz$
tham so hoa $y=r\cos t,z=r\sin t$
=> $I=2\pi\int _{0}^{2} r^{2}\left( 1-\frac{r^{2}}{4} \right) \, dr=2\pi\left( \frac{8}{3}-\frac{8}{5} \right)=\frac{32\pi}{15}$

V.
$I=\int _{0}^{\infty}e^{ -y^{3} } \, dy\int _{0}^{\infty} xe^{ -x^{3} } \, dx$
let $u=y^{3},v=x^{3}, dy=\frac{1}{3}u^{-2/3}, dx=\frac{1}{3}v^{-2/3}$
=> $I=\frac{1}{9}\int _{0}^{\infty} u^{-2/3}e^{ -u } \, du\int _{0}^{\infty} v^{-1/3}e^{ -v } \, dv$
$=\frac{\Gamma\left( \frac{1}{3} \right)\Gamma\left( \frac{2}{3} \right)}{9}=\frac{\pi}{9\sin \frac{\pi}{3}}=\frac{2\pi}{9\sqrt{ 3 }}$


$(10x^4+3x^{2}+10xy^{4})dx-(10x^{3}+10y^{4}-4y^{3})dy$
$=10x(x^{3}+y^{4})dx-10(x^{3}+y^{4})dy+d(x^{3}+y^{4})$$=5(x^{3}+y^{4})d(x^{2}-2y)+d(x^{3}+y^{4})$
let $u=x^{3}+y^{4},v=x^{2}-2y$
then $f=\frac{e^{ v }}{5u^{4/5}}(5udv+du)=u^{1/5}d(e^{ v })+e^{ v }d(u^{1/5})=d(e^{ v }u^{1/5})$

$\int _{1}^{\infty} \frac{(\ln x)^{4}}{1+x^{2}} \, dx$
$u=\frac{1}{x}$
=> $dx=-\frac{du}{u^{2}}$ and $I=\int _{0}^{1} \frac{(\ln u)^{4}}{1+\frac{1}{u^{2}}} \, \frac{du}{u^{2}}=\int _{0}^{1} \frac{(\ln x)^{4}}{1+x^{2}} \, dx$

$t=\ln x$
=> $I=\int _{0}^{\infty} \frac{t^{4}e^{ t }}{1+e^{ 2t }} \, dt$

$r=ae^{ b\theta }$
=> $r'=br,r''=b^{2}r$
=> $\kappa=\frac{|r^{2}+2r'^{2}-rr''|}{\sqrt{ (r^{2}+r'^{2})^{3} }}=\frac{r^{2}(1+b^{2})}{r^{3}\sqrt{ (1+b^{2})^{3} }}=\frac{1}{r\sqrt{ 1+b^{2} }}=\frac{1}{ae^{ b\theta }\sqrt{ 1+b^{2} }}$

$\Delta r= \frac{r'^{2}(-r'_{y}, r'_{x})}{r'\times r''}$ or $\Delta r=\frac{(1+y'^{2})(-y',1)}{y''}$




	