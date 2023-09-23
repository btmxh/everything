$$E=\frac{\sigma}{2\varepsilon\varepsilon_{0}}\left( 1-\frac{1}{\sqrt{ 1+\frac{R^{2}}{h^{2}} }} \right)$$
**Proof**
We integrate twice:
- First, consider the ring $x<R<x+dx$

Let $R \to \infty$ then $E\to \frac{\sigma}{2\varepsilon\varepsilon_{0}}$: electric field of uniformly charged plane


## Electric field line
- EFL: đường cong có tiếp tuyến tại $\hspace{0pt}1$ điểm $M$ trùng với phương của vecto điện trường tại $M$. Chiều của đường sức điện trường là chiều của vecto cường độ điện trường.
- Tập nhiều EFL là điện phổ
- EFL có thể đi từ điện tích dương (hoặc vô cùng) đến điện tích âm (hoặc vô cùng). Các EFL là đường hở, không cắt nhau.
- Điện phổ cho biết phương, chiều, độ lớn của điện trường từ từng điểm.

## Vecto cảm ứng điện $\vec{D}$
Ta có $E \propto \frac{1}{\varepsilon}$ nên tại điểm phân cách giữa $\hspace{0pt}2$ môi trường, E biến đổi đột ngột, phổ các đường sức điện bị gián đoạn trên mặt phân cách
Dùng ĐL vật lý khác ko phụ thuộc vào môi trường: $\vec{D}=\varepsilon\varepsilon_{0}\vec{E}$
Khi đó D ko phụ thuộc mtrg, ví dụ $\vec{D}=\frac{|q|}{4\pi r^{2}} \frac{\vec{r}}{r}$ trong điện trường một điện tích điểm.
Đường cảm ứng điện: đường cong có tiếp tuyến tại mỗi điểm của nó trùng với phương của vecto cảm ứng điện tại điểm đó, có chiều là chiều của $\vec{D}$
>Quy ước: Vẽ số đường cảm ứng điện qua $\hspace{0pt}1$ đơn vị diện tích đặt vuông góc với đường cảm ứng điện tỷ lệ với giá trị của D

## Điện thông
Giả sử có diện tích S trong điện trường bất kỳ D
Chia S thành những phần vô cùng bé diện tích nhỏ có thể coi là có điện trường bằng nhau tại mỗi điểm trong $\hspace{0pt}1$ phầ$n$.
Điện thông gửi qua toàn bộ diện tích S bằng $\Phi_{e}=\int_{S} d\Phi_{e}=\int_{S} \vec{D}d\vec{S}=\int_{S} D_{n}dS$
$D_{n}=D\cos\alpha$ với $\alpha$ là góc giữa D và pháp tuyến n
D_n là hình chiếu của D lên pháp tuyến n

Điện thông là đại lượng đại số, có dấu phụ thuộc vào chiều chọn cho n
Với mặt kín quy ước cho n hướng ra ngoài
- D hướng vào mặt kín thì $d\Phi_{e}<0$, ngược lại...

dS_n=|dScos alpha| là hình chiếu của dS lên mặt phẳng vuông góc với các đường cảm ứng điện. Do đó Phi_e=DdS_n
Điện thông qua diện tích dS là $\hspace{0pt}1$ đại lượng có đô lớn tỉ lệ với số đường cảm ứng điện vẽ qua điện tích đó.

## Định lý Ostrogradsky-Gauss
### Góc khối
Góc khối $d\Omega=\frac{dS\cos \alpha}{r^{2}}$, là đại lượng vô hướng, dương khi alpha nhọn, n hướng ra xa $O$ và ngược lại.
dScos alpha: hình chiếu dS lên mặt phẳng vuông góc với OM tại M => góc khối bằng dSigma với Sigma là phần mặt cầu (đơn vị) nằm trong nón đỉnh O tựa trên chu vi dS.
dS_n là $\hspace{0pt}2$ mặt đồng dạng phối cảnh
Tính góc khối qua tính tích phân $\Omega=\int_{S} \frac{dS\cos\alpha}{r^{2}}$
Góc "toàn bộ" (nhìn cả mặt cầu) là $\Omega=4\pi$ (nếu hướng trong thì $-4\pi$)

### Điện thông từ điện tích điểm
Xét điện tích $q$ tại $O$
Xét diện tích $dS$, gọi $n$ là vec pháp tuyến của dS, hướng ra xa O, độ dài đơn vị
$d\Phi_{e}=\vec{D}d\vec{S}=\frac{q}{4\pi} \frac{\vec{r}}{r^{3}}d\vec{S}=\frac{q}{4\pi r^{3}}\vec{r}.\vec{n}dS=\frac{q}{4\pi} \frac{\cos\alpha dS}{r^{2}}=\frac{q}{4\pi}d\Omega$
Qua mat kin $S$ bao quanh $q$: $\Phi_{e}=\frac{q}{4\pi}\oint_{S}d\Omega=q$
Qua mat kin $S$ nam ngoai $q$ (ko bao quanh $q$)
$\Phi_{e}=\frac{q}{4\pi} \oint_{S}d\Omega$ tach $S$ thanh $S_{1}$ va $S_{2}$, mot cai huong trong mot cai huong ngoai thi co $\Phi_{e}=\frac{q}{4\pi}(\Delta \Sigma-\Delta\Sigma)=0$

Dien thong do dien tich $q$ gay ra mat kin $S$ co gia tri bang $q$ neu $q$ nam trong mat kin va bang $\hspace{0pt}0$ neu $q$ nam ngoai mat kin $S$.
Trong truong hop he dien tich q1 q2 ... qn: Dien thong qua mat kin $S$ bang tong dien thong do tung dien tich gay ra nam trong mat kin
**Dinh ly O-G**: Dien thong gui qua mat kin $S$ bang tong dai so dien tich chua trong mat kin ay
$\Phi_{e}=\oint_{S}\vec{D}d\vec{S}=\sum q_{i}$
Dang vi phan: $\oint_{S}\vec{D}d\vec{S}=\int_{V} \operatorname{div}\vec{D}dV$, $\sum q_{i}=\int_{V}\rho dV$ => $\int_{V} \operatorname{div}\vec{D}dV=\int_{V} \rho dV$ => $\operatorname{div}\vec{D}=\rho$

### Ung dung
Tim dien truong mat cau $(O, R)$ tich dien deu
Xac dinh dien truong tai $M$ cach $O$ khoang $r>R$

Xet mat cau $(O, r)$ co dien thong do mat cau $(O, R)$ gay ra la $\Phi_{e}=\oint_{S} \vec{D}d\vec{S}=\oint_{S} D_{n}dS=D \oint_{S}dS=4\pi r^{2}D=q$=> $D=\frac{q}{4\pi r^{2}}$
Neu $M$ trong mat cau: $\Phi_{e}=4\pi r^{2}D=0$ do $q=0$ nen $D=0, E=0$

Mat phang vo han tich dien deu
Xet tai diem $M$, ve qua $M$ mat tru co $\hspace{0pt}2$ day song song cach deu mat phang
$\vec{D}$ vuong goc mat phang
- Tai mat day: $D_{n}=D$ const
- Tai mat ben: $D_{n}=0$ do $n$ vuong goc

$\sigma S=\sum q_{i}=\Phi_{e}=\oint_{S}D_{n}dS=\int_{day} D_{n}dS=D\int_{day}dS=2DS_{day}$ (do co $\hspace{0pt}2$ day) => $D=\frac{\sigma}{2}, E=\frac{\sigma}{2\varepsilon\varepsilon_{0}}$

$\hspace{0pt}2$ mat phang mang dien deu trai dau
Giua $\hspace{0pt}2$ mat phang $D_{1}$ va $D_{2}$ cung chieu nen chong chat $D=D_{1}+D_{2}=\sigma$
Ngoai $\hspace{0pt}2$ mp thi triet tieu nhau $D=0$

Mat tru thang dai vo han ban kinh $R$ tich dien deu co mat do dien mat $\sigma$

