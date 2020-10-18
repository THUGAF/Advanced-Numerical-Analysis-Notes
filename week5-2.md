# Week 5-2

## Jacobi和Gauss-Seidel迭代法

### 收敛性定理

GS法收敛：$A$对称正定

J法收敛：$A$对称正定且$2D-A$对称正定

## 超松弛迭代法

### 逐次超松弛迭代法（SOR）

$$x_i^{(k+1)}=\omega\bar{x}_i^{(k+1)}+(1-\omega)x_i^{(k)}$$

矩阵形式
$$(D-\omega L)x^{(k+1)}=[(1-\omega)D+\omega U]x^{(k)}+\omega b$$

$$x^{(k+1)}=(D-\omega L)^{-1}[(1-\omega)D+\omega U]x^{(k)}+\omega(D-\omega L)^{-1}b$$

分裂形式
$$A=M-N=D-L-U$$
$$M=\frac{1}{\omega}(D-\omega L), N=\frac{1}{\omega}[(1-\omega)D+\omega U]$$

若SOR收敛，则$\omega\in(0,2)$

若$A$对称正定，$\omega\in(0,2)$，则SOR收敛

若A是（块）三对角矩阵，对称正定，则
$$\rho(B_G)=\rho(B_J)^2<1 $$
$$\omega_b=\frac{2}{1+\sqrt{1-\rho(B_J)^2}}$$
$$\rho(\mathcal{L}_{\omega_b})=\omega_b-1$$

### 对称超松弛迭代（SSOR）

$$(D-\omega L)x^{(k+\frac{1}{2})}=[(1-\omega)D+\omega U]x^{(k)}+\omega b$$
$$(D-\omega U)x^{(k+1)}=[(1-\omega)D+\omega L]x^{(k+\frac{1}{2})}+\omega b$$

### 共轭梯度法

A为对称正定矩阵，$\phi(x)=\frac{1}{2}(Ax,x)-(x,b)$

$$Ax^*=b\iff \phi(x^*)=\min_x{\phi(x)} $$

#### 一般想法

找到$p^{(k)},\alpha_k$
$$x^{(k+1)}=x^{(k)}+\alpha_kp^{(k)}$$

#### 最速下降法

取$p^{(k)}=-\nabla\phi(x^{(k)})$

$$\alpha_k=\frac{(r^{(k)}, p^{(k)})}{(p^{(k)}, Ap^{(k)})} $$

性质

* 相邻两次搜索方向正交
* 线性收敛，系数为$\frac{\lambda_1-\lambda_n}{\lambda_1+\lambda_n}$
