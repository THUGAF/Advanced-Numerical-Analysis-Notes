# Week 2-2

## 赋范线性空间

### 矩阵范数

* 正定性：$||A||\geq 0$
* 齐次性：$||\alpha A||=|\alpha|\cdot||A||$
* 三角不等式：$||A+B||\leq||A||+||B||$
* 乘法相容性：$||AB||\leq||A||\cdot||B||$

Frobenius范数
$$||A||_F=\sqrt{\mathrm{Tr}(A^{\top} A)}$$

Cuachy-Schwarz不等式
$$||AB||_F^2\leq||A||_F^2||B||_F^2$$

向量范数与矩阵范数相容
$$||Ax||\leq||A||\cdot||x||$$

### 算子范数

$$||A||=\max_{x\neq 0}{\frac{||Ax||}{||x||}}=\max_{||x||=1}||Ax||$$

* 1范数：列范数
  $$||A||_1=\max_j\sum_{i=1}^n|a_{ij}|$$
* 无穷范数：行范数
  $$||A||_{\infty}=\max_i\sum_{j=1}^n|a_{ij}|$$
* 2范数：谱范数
  $$||A||_2=\sqrt{\rho(A^{\top} A)}$$
* 非奇异矩阵P的诱导范数
  $$||x||_\alpha=||Px||_\alpha$$
  $$||A||_{P,\alpha}=||PAP^{-1}||_\alpha$$
