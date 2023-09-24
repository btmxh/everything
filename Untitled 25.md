Xét một vecto cột $x$ đại diện cho $\hspace{0pt}1$ điểm dữ liệu. Khi đó giá trị $g(x)=w^{T}x+w_{0}$ sẽ bằng $\hspace{0pt}0$ nếu như điểm này nằm trên mặt phẳng. Hơn nữa, mặt phẳng chia không gian thành $\hspace{0pt}2$ phần, có bất phương trình là $g(x)>0$ và $g(x)<0$.

Xét hàm
$$
\sigma(x)=\begin{cases}
1,  & \text{nếu }x > 0 \\
-1  & \text{nếu }x < 0 \\
0  & \text{nếu }x = 0 \\
\end{cases}
$$, thì ta có thể lấy độ chênh lệch giữa kết quả thực $y$ và kết quả dự đoán là $\sigma(g(x))$: $e=|y-\sigma(g(x))|$

Khi đó, ta có thể tính tổng chênh lệch là $E=\frac{1}{N}\sum_{i=1}^{N}|y-\sigma(g(x))|$.

Ta được bài toán sau:
$$
\begin{align}
\min\, &E=\frac{1}{N}\sum_{i=1}^{N}|y^{i}-\sigma(w^{T}X^{i}+w_{0})|\\
\text{vđk}\  & w, w_{0} \in  \mathbb{R}^{d}
\end{align}
$$

Để hàm mục tiêu khả vi, ta cần thêm hai chỉnh sửa nhỏ sau:
- Thay hàm $\sigma$ bởi $\hspace{0pt}1$ hàm khả vi: một hàm hay dùng trong trường hợp này là hàm sigmoid: $S(x)=\frac{1}{1+e^{ -x }}$, có đồ thị như sau:![[Pasted image 20230924193437.png]]
- Tương tự bài toán dự đoán giá nhà, thay vì tính tổng giá trị tuyệt đối, ta tính tổng bình phương của độ chênh lệch.


Ta được bài toán liên tục sau:
$$
\begin{align}
\min\, &E=\frac{1}{2N}\sum_{i=1}^{N}(y^{i}-S(w^{T}X^{i}+w_{0}))^{2}\\
\text{vđk}\  & w, w_{0} \in  \mathbb{R}^{d}
\end{align}
$$
với $S(x)=\frac{1}{1+e^{ -x }}$

Viết dưới dạng ma trận:
$$
\begin{align}
\min\, &E=\frac{1}{2N}\|y-S(w^{T}X+w_{0})\|^{2}\\
\text{vđk}\  & w, w_{0} \in  \mathbb{R}^{d}
\end{align}
$$
với $S([x_{1}, x_{2}, \dots, x_{n}])=[S(x_{1}), S(x_{2}), \dots, S(x_{n})]$

