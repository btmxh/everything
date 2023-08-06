## dhcd
### accel

project $\vec{a}$ along tangent and normal directions of the orbit => $\vec{a}=\vec{a_{t}}+\vec{a_{n}}$
meaning:
- $a_{t}$: dac trung cho su bien thien ve do lon cua vecto van toc
- $a_{n}$: dac trung cho su bien thien ve huong cua vecto van toc
chars
- $a_{t}$
	- pdir: $\parallel$ orbit
	- cdir: sim with $\vec{v}$ if faster vv
	- $a_{t}=\frac{dv}{dt}$
- $a_{n}$
	- pdir: perp orbit
	- cdir: towards center of osc. circ, point to the convex part
	- $a_{n}=\frac{v^{2}}{R}$ ($R$ is osc. circ rad)


vecto van toc goc: pdir nam tren truc duong tron quy dao, cdir: thuan chieu voi chieu quay cd, do lon $\omega=| \frac{d\theta}{dt}|$
$\vec{v}=\vec{\omega}\times \vec{R}$

vecto gia toc goc $\vec{\beta}=\frac{d\vec{\omega}}{dt}$, pdir nam tren truc duong tron quy dao, cung chieu voi chieu quay neu cd nhanh dan, ..., do lon $\beta=\frac{d\omega}{dt}=\frac{d^{2}\theta}{dt^{2}}$

vecto dong luong 1 chat diem la tich cua khoi lluong voi vecto van toc chat diem do: $\vec{K}=m\vec{v}$
cua mot he chat diem la tong cac vecto dong luong cua cac chat diem trong he $K=K_{1}+K_{2}+\dots$

dinh ly 1: dao ham cua vecto dong luong theo thoi gian bang ngoai luc tac dong len chat diem, dinh ly 2: do bien thien cua vecto dong luong bang xung cua ngoai luc tac dong len vat trong khoang thoi gian do

y nghia dong luong: ket hop cua m va v, dac trung cho chat diem ve mat dong luc hoc, trong cac va cham dac trung cho kha nang truyen cd

y nghia xung luong: dac trung cho tac dong cua luc trong time period, luc lon time nho thi it a huong hon luc do trong khoang tg lau hon, tac dong cua luc len cd con phu thuoc time tac dong

btdl:
- tong dong luong he chat diem co lap dc bao toan
- neu tong ngoai luc tac dong len mot he chat diem chieu theo 1 phuong bang 0 thi tong dong luong he chat diem theo phuong do duoc bao toan

trong co hoc newton
- thoi gian la abs: time do boi moi clock deu bang nhau
- khong gian co tinh tuong doi: $x=x'+oo',y=y',z=z'$
- khoang khong gian abs: xet thuoc...

xet he quy chieu 0xyz va 0'x'y'z', he 0' dang cd tren truc 0x voi van toc v => $\bar{oo'}=vt$
phep bd toa do tu 0 sang 0': $x=x'+vt,y=y',z=z',t=t'$
va tu o' sang o... la cac phep bd galileo

NLTDG
- moi hqc cdtd voi hqcqt deu la hqcqt
- trong moi hqcqt thi cac pt dong luc hoc deu co dang giong nhau
- cac dl co hoc deu xra giong nhau trong moi hqcqt

hqcqt la hqc gan lien voi cac vat co lap, tai do dl newton 1 nghiem dung
hqckqt la hqc chuyen dong co gia toc so voi hqcqt
luc qt la luc can phai xet them trong hqckqt, bang -mA voi A la gia toc cua hqckqt
- la luc ao chi q sat dc trong hqckqt
- cung phuong nguoc chieu voi gia toc cua hqc
- do lon f=ma

luc qt ly tam la dang dac biet cua lqt xuat hien khi hqckqt chuyen dong tron xq mot hqcqt
- la luc ao
- nguoc chieu voi chieu huong vao hqcqt lay lam tam
- f=mv2/r

mdl cua chat diem tai M doi voi goc O la $L=mr\times v$ voi $r=\vec{OM}$, $v$ la vec to van toc, m la kl
dl1: d/dt Lvec bang momen cua luc tac dong len cd do
dlbt: Lvec cua chat diem ko chiu tac dong ngoai luc or ngoai luc di qua goc O thi bao toan
vidu: chuyen dong tron deu

dong nang la nang luong gan vs cd cua vat
xet m di chuyen voi van toc v tu 1 den 2
cong cua ngoai luc la $\int_{1}^{2} \vec{F} d\vec{s}=\int _{1}^{2} m \frac{d\vec{v}}{dt} \, d\vec{s}=\int _{1}^{2} m \frac{d\vec{s}}{dt} \, d\vec{v}=\int _{1}^{2} m\vec{v} \, d\vec{v}=\dots$
bieu dien su bien thien cua co nang (o day chi co dong nang)
nen ta cho $Wd=\frac{mv^{2}}{2}$

DLDN: do bien thien cua dong nang bang cong cua ngoai luc tac dong len vat trong qtcd $\Delta Wd=A$
dlbtcn trong gf: co nang trong trong truong duoc bao toan $W_{c}=\frac{mv^{2}}{2}+mgz =const$

xet qua trinh di chuyen rat nho PQ
quang duong di duoc la PQarc xap xi PQ
vi phan cong: dA = F nhan PQ nhan cos alpha
lay chieu duong tu O->P
ma ta co PQ cos alpha = -PH
PH=OH-OPxxOQ-OP=r+dr-r=dr
=> dA=Fxdr=GMm/r^2 dr
=> A=@D-GMm/r
=> cong ko phu thuoc vao duong di tu r1 den r2 ma chi phu thuoc diem dau diem cuoi nen truong hap dan co la truong the va the nang tai diem r la -GMm/r+C
C chon tuy y, bang the nang tai infty

nho hon v1 => roi xuong
v=v1 quy dao tron
v1<v<v2 => quy dao xq trai dat elip
v>v2=> thoat khoi kq td

tinh
v1: gs vat quay xq td quy dao tron thi ta co tl luc h tam => F=mvsr/R=GMm/R2 => v=sqrt(GM/r)=sqrt(Rg0)
v2: vat thoat dc luc hut trai dat => btcn => co nang bd = co nang tai +vc => mvsr/2=-GMm/r => v=v1sq2

chuyen dong tinh tien
- quy dao giong nhau
- **vec** van gia same
chuyen dong quay quanh truc
- quy dao xq truc
- cung time => cung quay dc 1 angle
- van gia goc same
- $\vec{v}=\vec{\omega}\times \vec{r},\vec{a}=\vec{\beta}\times \vec{r}$

tac dong luc
- tach theo truc f=f1: song song+f2: vuong goc
- tach f2: fn + ftt
- ftt chuyen dong quay
- f1, fn ko effect
- chi co thanh phan luc dat tiep tuyen tai diem dat moi co tac dung trong cdq

momen: $M=r\times F_{t}$ cua F voi delta = Ft voi delta
- phuong: phuong truc
- chieu: thuan chieu quay tu r sang ft
- do lon: M=rFt
=> bang 0 neu delta dong phang voi F or F=0
=> momen of Ft voi delta = voi 0

xet ...
$ri\times F_{ti}=M_{i}$
=> $r_{i}\times m(\beta \times r_{i})=M_{i}$
=> $\beta(r_{i} . r_{i})-r_{i}(r_{i}.\beta)=\beta r_{i}^{2}$
=> $I\beta=M$

$a\times (b\times c)=(a.c)b-(a.b)c$

$I\beta=M$
I: momen quan tinh doi voi truc quay: dai luong cho quan tinh cua vat ran trong chuyen dong quay
$I=mr^{2}$
truc/12, dia/2, cau 2/5, /1
beta: vecto gia toc goc
M: tong momen ngoai luc

$L=mr\times v=mr\times (\omega \times r)=m((rr)\omega-(r\omega)r)=mr^{2}\omega=I\omega$
dl1: d/dt Lvec = momen ngoai luc tac dong
dl2: @d Lvec = xung luong cua momen ngoai luc
dlbt: ko chiu nl or tong momen = 0 => Lvec const

cong: A=Fds=Frdtheta=Mdtheta
consuat: P=Momega
dA=Mdtheta=Idomega/dtdtheta=Iomegadomega=Iomegasr/2

xet con lac => chiu luc dan hoi $F=-kx$
=> $m\ddot{x}+kx=0$
=> $x=c_{1}\cos \omega t+c_{2}\sin \omega t=C\cos(\omega t+\phi)$
ve...
chu ky dao dong: la khoang thoi gian de vat tro lai trang thai ban dau
tan so dao dong: so dao dong vat thuc hien trong 1 don vi thoi gian
chiu luc can $F=-rv$ => $m\ddot{x}+r\dot{x}+kx=0$
>$\omega_{0}^{2}=\frac{k}{m}$
>$\beta=\frac{r}{2m}$
>sol: $t=\frac{-r\pm i\sqrt{ 4km-r^{2} }}{2m}=-\frac{r}{2m}\pm i\sqrt{ \frac{k}{m}-\frac{r^{2}}{4m^{2}} }$
>=> $t=-\beta+i\sqrt{ \omega_{0}^{2}-\beta^{2} }$

$\omega =\sqrt{ \omega_{0}^{2}-\beta^{2} }$, $\frac{r}{2m}=\beta$
$x=A_{0}e^{ -\beta t }\cos(\omega t+\phi)$

ve...
giam luong loga: $\delta=\ln\frac{A(t)}{A(t+T)}=\beta T$

thuyet dong luc hoc phan tu
- cac chat cau tao gian doan gom phan tu
- phan tu chuyen dong hlkn
- cuong do chd bieu hien temp he
- cac phan tu khi nho so vs dist => chat diem
- cac ptk ko interact tru khi vc

ptcb: $P=n_{0}kT$
- ($n_{0}$: so hat trong 1kmol gas)
pttt: $PV=nRT$, $R=N_{A}k$

dof of 1 vat
- so toa do can thiet de xac dinh vi tri cua vat do trong space
dl pb deu: dong nang tb cua chat khi duoc phan bo deu vao cac bac tu do va nang luong 1 bac la kt/2
=> ikt/2

$\frac{dn}{n}=\left( \frac{m}{2\pi kT} \right)^{3/2}e^{ -\frac{m|v|^{2}}{2kT} }dv_{x}dv_{y}dv_{z}$
=> $\frac{dn}{n}=\left( \frac{m}{2\pi kT} \right)^{3/2}e^{ -\frac{mv^{2}}{2kT} }4\pi v^{2}dv$
=> vxs=sq(2kT/m), vtb=sq(8kT/pim), vcqp=sq(3kT/m)
y nghia
- vxs: la van toc xac suat lon nhat nhieu p tu khi co van toc nay
- vtb: la van toc trung binh, bieu dien van toc trung binh cua cac p tukhi

boltzmann
2 diem do cao z va z+dz co chenh lech ap suat bang
trong luong 1 cot khi chieu cao dz, day 1 dvdt: $dP=-\rho gdz$
ma $PV=\frac{M}{\mu}RT$ => $\rho=\frac{M}{V}=\frac{\mu P}{RT}$
=> $\frac{dP}{P}=-\frac{\mu g}{RT}dz$
=> $n_{0}\propto P \propto e^{ -\frac{\mu g}{RT}z }$
$\frac{\mu}{R}=\frac{m}{k}$ voi m la kl phan tu khi, $mgz$: the nang tai diem z
=> $n_{0} \propto e^{ -W_{t}/kT }$

ttcb: la trang thai ko doi theo thoi gian voi tinh bat bien ko phu thuoc dk cua ngoai vat
qtcb: la 1 qtr bien doi gom 1 chuoi lien tiep cac ttcb
qt bien doi vo cung cham trong do tai moi diem co the coi la deu co cung cac thong so (p,V,T) thi co the coi la 1 qtcb,

dang nhiet => $A=-\int p \, dV=-\int \frac{M}{\mu}RT \, \frac{dV}{V}=\frac{M}{\mu}RT\ln \frac{V_{1}}{V_{2}}$

khi ly tuong la khi tuan theo dl boyle-mariotte va dl gay-lussac

pt co ban cua dong luc hoc pt: $P=n_{0}kT$
$n_{0}=\frac{N}{V}$
=> $PV=NkT$ => so sanh pt mendelev-claperon => R=Nk

NL I:
- do bien thien tong nang luong cua he trong 1 qua trinh bien doi vi mo co gia tri bang tong cong va nhiet he nhan vao
- do bien thien noi nang trong mot qua trinh thay doi trang thai bang con + nhiet
- $\Delta W=A+Q$, $\Delta U=Q+A$ (co nang ko doi)

he qua
- neu 2 vat trao doi nhiet (ko cong) => $Q=0=Q_{1}+Q_{2}$ => ...
- he co lap => $A=Q=0$ => $\Delta U=0$: he co lap ko trao doi nhiet voi ben ngoai
- chu trinh => $\Delta U=0$ => $A=-Q=Q'$: chu trinh co cong nhan vao bang luong nhiet sinh ra
- qtr bien doi cuc nho $dU=\delta A+\delta Q$

y nghia
- d
- may hoat dong theo chu trinh thi $A'=Q$ nen ko co dong co nao sinh cong ko nhan nhiet/sinh cong lon hon nhiet
- ko co dcvc loai 1

qua trinh doan nhiet: qtr ko trao doi nhiet voi ben ngoai
$dU=nC_{V}dT, dA=-PdV=-nRT \frac{dV}{V}$
=> $C_{V} \frac{dT}{T}+R \frac{dV}{V}=0$
=> $TV^{\gamma-1}=const$

$PV^{\gamma}$ const doc hon $PV$ const do $\gamma>1$ va:
- khi nen doan nhiet thi nhiet do tang => di len nhanh hon dang nhiet
- ...

han che nl1
- ko cho biet chieu dien bien cua cac qtr truyen nhiet trong tht
- ko neu len khac nhau qtr truyen nhiet -> cong va cong -> nhiet
- ko d gia dc chat lg nhiet

phat bieu
- clausius:
	- nhiet ko the truyen tu nong <- lanh
	- ko the xra qtr kq duy nhat la truyen nl duoi dang nhiet tu vat lanh => nong hon
- thompson
	- ko tao dc may tuan hoan bd lien tuc nhiet thanh cong nho lam lanh 1 vat ma xq ko chiu su bien doi dong thoi nao
	- ko the che tao d co vinh cuu loai 2

y nghia
- c to cac qtr ktn chi d ra theo 1 chieu hg chu ko d ra theo chieu ngc lai trong dk tu phat ko co a hg ben ngoai, dam bao he tien den ttcb, khi cb roi ko tro nen kcb dc
- qttn ko nhan cong, nhiet
- qtktn phai thu Q or thu A cua mtr
- => nen lam giong voi qttn 
- dcvc 2

$\eta=\frac{A}{Q}$
2-3 nen dang $Q=nRT_{2}\Delta \ln V$

can $\frac{P_{1}}{P_{2}}=\frac{P_{4}}{P_{3}}$ do doan nhiet

dl carnot
- moi dong co nhiet thuan nghich co cung nguon nong lanh deu co hieu suat = 1-t2/t1... ko phu thuoc cau tao va tac nhan may
- moi dcnktn deu co hs < dcntn
=>
- nhiet ko the hoan toan bien thanh cong
- hs cang lon if temp nong cang cao, temp lanh cang cao => Q tu vat temp cao co temp quality cao hon vat temp thap
- muon tang
	- tang giam t, 
	- che tao gan giong dctn

ham entropy la ham S cua trang thai sao cho bien thien entropy giua hai trang thai bang tich phan $\int \frac{\delta Q}{T}$ tu tt1 den tt2 theo 1 qttn nao do
- t/c
	- la fn of state
	- co tinh cong duoc
	- dc xd sai kem 1 hang so cong
	- q uoc S_0 tai vi tri T=0K
- $\Delta S\geq \int \frac{\delta Q}{T}$
trong moi qua trinh nhiet dong xay ra thuc te trong he co lap thi entropy luon tang
1 he co lap ko the 2 lan di qua cung 1 trang thai
he dat ttcb tai diem entropy max

khi lt ko tuon tac tru vc, kich thuoc pt ko dang ke
khi thuc co luc tuong tac, kich thuoc pt ko bo qua dc

thiet lap pt
- cong tich
	- the tich chuyen dong tu do < the tich thuc, can them so hang bo goi la cong tich: $V+b=V_{t}$, $b$ bang 4 lan tong the tich cac phan tu: $b=4N\left( \frac{1}{6}\pi d^{3} \right)$
- noi ap
	- cac p tu khi chuan bi dap vao thanh binh bi cac p tu ben trong keo lai nen gay ra luc nho hon, ap suat khi thuc nho hon ap suat klt
	- => noi ap la so hang bo them ve ap suat $P=P_{t}+P_{i}$
	- $P_{i} \propto n_{0}^{2}$ vi lop I lop II cac kieu, $P_{i}=\frac{a}{V^{2}}$
- => pt: $\left( P_{t}+\frac{a}{V^{2}} \right)(V-b)=RT$
- cho nhieu mol: $\left( P_{t}+\frac{M^{2}}{\mu^{2}} \frac{a}{V^{2}} \right)\left( V-\frac{M}{\mu}b \right)=\frac{M}{\mu}RT$

duong dang nhiet VDV
$T<T_{K}$: co mot doan loi lom
$T>T_{K}$ gan giong cua klt
$T=T_{K}$ co diem uon tai $K$: diem toi han

duong dang nhiet thuc nghiem
$T<T_{K}$ co 2 doan giam, giua la 1 doan ngang
$T>T_{K}$ gan giong klt
$T=T_{K}$ doan nam ngang bien thanh diem toi han
