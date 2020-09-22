# Week 1-2

## 数值分析中的典型问题

### 病态问题

输入数据的轻微扰动导致结果出现巨大差异

相对差异
$$|\frac{f(x+h)-f(x)}{x}|\approx |\frac{hf'(x)}{f(x)}|=|\frac{xf'(x)}{f(x)}||\frac{h}{x}|$$

条件数
$$C=|\frac{xf'(x)}{f(x)}|$$

C>>1：病态

### 算法稳定性

误差累积类型

* 线性型：$|\epsilon_n|\approx nC\epsilon_0$
* 指数型：$|\epsilon_n|\approx C^n\epsilon_0$

避免误差的手段

* 避免有效数字损失
* 减少运算次数

## 线性代数基本概念

### 线性空间

线性空间

* 加法
* 数乘

线性相关、基、维数、子空间

### 内积空间

柯西-施瓦茨不等式
$$|(u,v)^2|\leq (u,u)(v,v)$$

Gram-Schmidt正交化
