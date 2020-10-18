# Week 5-1

## 线性方程的迭代解法

### 研究对象和目标

原因

* 直接解法必须运行完所有的步骤才能得到准确解
* n很大时，直接解法很慢

分类

* 多步迭代
* 单步迭代
* 单步定常线性迭代：$x^{(k+1)}=Bx^{(k)}+f_k$

## 迭代基本概念

### 向量极限

$$\lim_{k\rightarrow\infty}\|x^{(k)}-x\|=0$$

Cauchy序列
$$\forall\epsilon>0, \exists N\in\Z, s.t.|x_n-x_m|\leq\epsilon,\forall n,m>N$$

### 矩阵极限

$$\lim_{k\rightarrow\infty}\|A^{(k)}-A\|=0\iff \lim_{k\rightarrow\infty}\|a_{ij}^{(k)}-a_{ij}\|=0$$

等价命题

* $\lim_{k\rightarrow\infty}A^k=0$
* $\lim_{k\rightarrow\infty}a_{ij}^k=0$
* $\rho(A)<1$
* $\|A\|<1$

性质
$$\lim_{k\rightarrow\infty}\|B^k\|^\frac{1}{k}=\rho(B)$$

### 迭代公式构造

$$Ax=b\iff x=M^{-1}Nx+M^{-1}b$$
$$A=M-N, B=M^{-1}N, f=M^{-1}b$$
$$B=I-M^{-1}A$$

### 收敛性分析

算法收敛等价于残差收敛到0
$$\lim_{k\rightarrow\infty}e^{(k)}=\lim_{k\rightarrow\infty}x^{(k)}-x^*=0$$

性质
$$\|x^{(k)}-x^{(k-1)}\|=\frac{q^k}{1-q}\|x^{(1)}-x^{(0)}\|,\|B\|=q<1$$

$$k\geq\frac{-\ln\epsilon}{-\ln\|B^k\|^\frac{1}{k}}$$

平均收敛率
$$R_k(B)=-\ln\|B^k\|^\frac{1}{k}$$

渐近收敛率
$$R(B)=-\ln\rho(B)$$

### Jacobi迭代法

$$A=D-L-U$$
D是对角，-L，-U是严格下、上三角部分
$$M=D,N=L+U$$
$$B_J=D^{-1}(L+U),f_J=D^{-1}b$$

### Gauss-Seidel迭代法

$$A=D-L-U$$
$$M=D-L,N=U$$
$$B_G=(D-L)^{-1}U,f_G=(D-L)^{-1}b$$


