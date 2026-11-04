# week17

> **命题 3.1 (唯一极值点即全局极值点)**
> 
> 设 $y=f\left(x\right)$ 在区间 $\left(a,b\right)$ (或 $\left[a,b\right]$) 上连续. 若 $x_0$ 是 $\left(a,b\right)$ 中唯一的极值点, 则当 $x_0$ 为极大值点时, $f\left(x_0\right)$ 为最大值; 当 $x_0$ 为极小值点时, $f\left(x_0\right)$ 为最小值.

> **定理 3.1 (极值点第一充分条件)**
> 
> 设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中可导, 且 $x_0\in\left(a,b\right)$ 是 $f$ 的一个稳定点, 即 $f'\left(x_0\right)=0$. 若存在 $r> 0$, 使得当 $x\in\left(x_0-r,x_0\right)$ 时 $f'\left(x\right)> 0$, 当 $x\in\left(x_0,x_0+r\right)$ 时 $f'\left(x\right)< 0$, 则 $f\left(x_0\right)$ 是极大值; 若符号相反, 则 $f\left(x_0\right)$ 是极小值.

> **定理 3.2 (极值点第二充分条件)**
> 
> 设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中可导, $x_0\in\left(a,b\right)$ 是其稳定点, 并假定 $f$ 在 $x_0$ 有二阶导数. 若 $f''\left(x_0\right)> 0$, 则 $x_0$ 为极小值点; 若 $f''\left(x_0\right)< 0$, 则 $x_0$ 为极大值点.

> **定理 4.1 (局部泰勒展开式)**
> 
> 设 $y=f\left(x\right)$ 在 $x_0$ 点附近有定义, 且有 $n$ 阶导数 $f^{\left(n\right)}\left(x_0\right)$. 则 $f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right)$ ($x\to x_0$).

> **定理 4.2 (带拉格朗日余项的泰勒公式)**
> 
> 设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上有 $n$ 阶连续导数, 在 $\left(a,b\right)$ 中有 $n+1$ 阶导数. 则对任意 $x,x_0\in\left[a,b\right]$, 存在介于 $x_0$ 与 $x$ 之间的点 $\xi$, 使得 $f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n+1\right)}\left(\xi\right)}{\left(n+1\right)!}\left(x-x_0\right)^{n+1}$.

## 3.3-5

证明不等式: $x^\alpha-\alpha x+\alpha-1\le0$ 对一切 $x> 0$, 其中 $0< \alpha< 1$.

### 解答 3.3-5

令 $f\left(x\right)=x^\alpha-\alpha x+\alpha-1$ ($x> 0$). 求导得

$$
f'\left(x\right)=\alpha x^{\alpha-1}-\alpha=\alpha\left(x^{\alpha-1}-1\right).
$$

令 $f'\left(x\right)=0$, 得 $x=1$. 当 $0< x< 1$ 时 $f'\left(x\right)> 0$, 当 $x> 1$ 时 $f'\left(x\right)< 0$. 由**定理 3.1 (极值点第一充分条件)**, $x=1$ 为极大值点. 又 $f\left(1\right)=0$. 由**命题 3.1 (唯一极值点即全局极值点)**, $f\left(1\right)=0$ 为最大值. 故 $f\left(x\right)\le0$. $\blacksquare$

## 3.3-6

证明: 设 $a> 0$, $b> 0$, $p> 1$, $q> 1$, 且 $\frac1p+\frac1q=1$, 则 $a^{1/p}b^{1/q}\le\frac{a}{p}+\frac{b}{q}$.

### 解答 3.3-6

在 3.3-5 中取 $\alpha=\frac1p$, 则 $1-\alpha=\frac1q$. 对任意 $x> 0$,

$$
x^{1/p}-\frac1p x+\frac1p-1\le0.
$$

令 $x=\frac{a}{b}$, 代入并两边乘以 $b$, 整理得

$$
a^{1/p}b^{1/q}\le\frac{a}{p}+\frac{b}{q}.
$$

此即杨氏不等式. $\blacksquare$

## 3.3-7

设 $\triangle ABC$ 的边分别为 $a,b$ 与 $c$. 假定 $b=c$, 且 $a+b+c=2l$, 其中 $l$ 为一定数. 问 $\triangle ABC$ 何时面积最大?

### 解答 3.3-7

因 $b=c$, 三角形为等腰三角形. 由 $a+2b=2l$, 得 $b=l-\frac a2$. 面积为

$$
S=\frac12 a\sqrt{b^2-\frac{a^2}{4}}=\frac12 a\sqrt{l^2-la}.
$$

为求最大值, 只需最大化 $S^2=\frac14\left(l^2a^2-la^3\right)$. 求导得

$$
\left(S^2\right)'=\frac{la}{4}\left(2l-3a\right).
$$

令 $\left(S^2\right)'=0$, 得 $a=\frac{2l}{3}$. 当 $0< a< \frac{2l}{3}$ 时 $\left(S^2\right)'> 0$, 当 $\frac{2l}{3}< a< 2l$ 时 $\left(S^2\right)'< 0$. 由**定理 3.1 (极值点第一充分条件)**, $a=\frac{2l}{3}$ 为极大值点. 此时 $b=c=\frac{2l}{3}$, 即三角形为等边三角形时面积最大. $\blacksquare$

## 3.3-8

设 $f\left(x\right)=\sin^p x+\cos^p x$, 求它在 $\left[0,\frac\pi2\right]$ 上的最大值与最小值.

### 解答 3.3-8

求导得

$$
f'\left(x\right)=p\sin x\cos x\left(\sin^{p-2}x-\cos^{p-2}x\right).
$$

令 $f'\left(x\right)=0$, 在 $\left(0,\frac\pi2\right)$ 内得 $x=\frac\pi4$. 计算各点函数值:

- $f\left(0\right)=1$,
- $f\left(\frac\pi4\right)=2^{1-p/2}$,
- $f\left(\frac\pi2\right)=1$.

当 $p> 2$ 时, $2^{1-p/2}< 1$. 故最大值为 $1$ (在端点处达到), 最小值为 $2^{1-p/2}$ (在 $x=\frac\pi4$ 处达到). $\blacksquare$

## 3.4-1-2

写出函数 $y=\frac1{1-x}$ 在 $x=0$ 点的局部泰勒公式.

### 解答 3.4-1-2

对 $f\left(x\right)=\frac1{1-x}$ 求各阶导数: $f^{\left(n\right)}\left(x\right)=\frac{n!}{\left(1-x\right)^{n+1}}$. 故 $f^{\left(n\right)}\left(0\right)=n!$. 由**定理 4.1 (局部泰勒展开式)**,

$$
\frac1{1-x}=1+x+x^2+\cdots+x^n+o\left(x^n\right)\quad\left(x\to0\right).
$$

$\blacksquare$

## 3.4-1-4

写出函数 $y=\arctan x$ 在 $x=0$ 点的局部泰勒公式 (展开至 $x^5$ 为止).

### 解答 3.4-1-4

计算得 $f\left(0\right)=0$, $f'\left(0\right)=1$, $f''\left(0\right)=0$, $f'''\left(0\right)=-2$, $f^{\left(4\right)}\left(0\right)=0$, $f^{\left(5\right)}\left(0\right)=24$. 由**定理 4.1 (局部泰勒展开式)**,

$$
\arctan x=x-\frac{x^3}{3}+\frac{x^5}{5}+o\left(x^5\right)\quad\left(x\to0\right).
$$

$\blacksquare$

## 3.4-1-5

写出函数 $y=\tan x$ 在 $x=0$ 点的局部泰勒公式 (展开至 $x^3$ 为止).

### 解答 3.4-1-5

计算得 $f\left(0\right)=0$, $f'\left(0\right)=1$, $f''\left(0\right)=0$, $f'''\left(0\right)=2$. 由**定理 4.1 (局部泰勒展开式)**,

$$
\tan x=x+\frac{x^3}{3}+o\left(x^3\right)\quad\left(x\to0\right).
$$

$\blacksquare$

## 3.4-4

将 $y=\sin\left(x+\alpha\right)$ 在 $\alpha=0$ 点展开成带拉格朗日余项的泰勒公式, 并估计余项大小.

### 解答 3.4-4

将 $x$ 视作常数, 对 $\alpha$ 求导: $\frac{\mathrm d}{\mathrm d\alpha}\sin\left(x+\alpha\right)=\cos\left(x+\alpha\right)$, $\frac{\mathrm d^2}{\mathrm d\alpha^2}\sin\left(x+\alpha\right)=-\sin\left(x+\alpha\right)$. 在 $\alpha=0$ 处, $\sin x$ 与 $\cos x$. 由**定理 4.2 (带拉格朗日余项的泰勒公式)**,

$$
\sin\left(x+\alpha\right)=\sin x+\left(\cos x\right)\alpha-\frac{\sin\left(x+\xi\right)}2\alpha^2,
$$

其中 $\xi$ 介于 $0$ 与 $\alpha$ 之间. 余项 $r\left(\alpha\right)=-\frac{\sin\left(x+\xi\right)}2\alpha^2$, 故 $\left|r\left(\alpha\right)\right|\le\frac{\alpha^2}2$. $\blacksquare$

## 3.4-5

将 $y=x+\frac{x^3}3$ 在 $x=\pm1$ 点展成泰勒公式. 说明: 任何多项式 $P_n\left(x\right)$ 在任何一点 $a$ 的 $n$ 次泰勒展开式之余项为 $0$.

### 解答 3.4-5

$f'\left(x\right)=1+x^2$, $f''\left(x\right)=2x$, $f'''\left(x\right)=2$, $f^{\left(4\right)}\left(x\right)=0$.

在 $x=1$ 处: $f\left(1\right)=\frac43$, $f'\left(1\right)=2$, $f''\left(1\right)=2$, $f'''\left(1\right)=2$. 由**定理 4.1 (局部泰勒展开式)**,

$$
x+\frac{x^3}3=\frac43+2\left(x-1\right)+\left(x-1\right)^2+\frac13\left(x-1\right)^3.
$$

在 $x=-1$ 处:

$$
x+\frac{x^3}3=-\frac43+2\left(x+1\right)-\left(x+1\right)^2+\frac13\left(x+1\right)^3.
$$

对于一般多项式 $P_n\left(x\right)$, $P_n^{\left(n+1\right)}\left(x\right)\equiv0$. 由**定理 4.2 (带拉格朗日余项的泰勒公式)**, 余项 $R_n\left(x\right)=0$. 即多项式的泰勒展开式是精确的. $\blacksquare$
