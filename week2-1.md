# Week 2-1

## 线性代数基本概念

### 赋范线性空间

范数映射的性质

* 正定性
* 齐次性
* 三角不等式

向量范数

* 1范数：$||x||_1=|x_1|+\cdots+|x_n|$
* 2范数：$||x||_2=\sqrt{x_1^2+\cdots+x_n^2}$
* 无穷范数：$||x||_{\infty}=\max{(|x_1|,\cdots,|x_n|)}$

### 矩阵特征值

特征值
$$Ax=\lambda x$$

谱半径
$$\rho(A)=\max{\{|\lambda|\mid\lambda\in\sigma(A)\}}$$

迹
$$\mathrm{Tr}(A)=\sum_{i=1}^n a_{ii} = \sum_{i=1}^n\lambda_i$$

特征多项式
$$\det(\lambda I-A)=\prod_{i=1}^n(\lambda-\lambda_i)^{n_i}$$

对角化

* 代数重数：$n_i$为$\lambda_i$的代数重数
* 几何重数：$m_i$为$\lambda_i$的特征向量张成线性空间的维数
* 显然，几何重数$\leq$代数重数
* 可对角化$\iff$几何重数=代数重数


