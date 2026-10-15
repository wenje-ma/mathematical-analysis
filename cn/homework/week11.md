# 作业 11

> **定义**（高阶导数）若 $y=f\left(x\right)$ 的导函数 $f'\left(x\right)$ 在 $x_0$ 点可导, 则其导数称为 $f$ 的二阶导数, 记作 $f''\left(x_0\right)$ 或 $\frac{\mathrm d^2f}{\mathrm dx^2}$. 一般地, $n$ 阶导数 $f^{\left(n\right)}\left(x\right)$ 由 $n-1$ 阶导数再求导得到.

### 习题一

（习题 2.4-1）求下列函数的 $n$ 阶导数: 
(1) $y=x^2e^x$;

(4) $y=x\ln\left(1+x\right)$.

### 解答 习题一

由**定义**（高阶导数）, $n$ 阶导数由 $n-1$ 阶导数再求导得到.(1)由莱布尼茨公式

$$
\left(uv\right)^{\left(n\right)}=\sum_{k=0}^n\binom nk u^{\left(k\right)}v^{\left(n-k\right)},
$$
其中 $u=x^2$, $v=e^x$.

$$
u'=2x,u''=2,u^{\left(k\right)}=0\left(k\ge3\right).
$$

故

$$
y^{\left(n\right)}=x^2e^x+2nx e^x+n\left(n-1\right)e^x=e^x\left[x^2+2nx+n\left(n-1\right)\right].
$$

(4)$y'=\ln\left(1+x\right)+\frac{x}{1+x}$.

$$
y''=\frac1{1+x}+\frac1{\left(1+x\right)^2}=\frac{2+x}{\left(1+x\right)^2}.
$$

一般地, 对 $n\ge2$,

$$
y^{\left(n\right)}=\left(-1\right)^n\frac{\left(n-2\right)!}{\left(1+x\right)^{n-1}}+\left(-1\right)^{n-1}\frac{\left(n-1\right)!}{\left(1+x\right)^n}.
$$

化简得

$$
y^{\left(n\right)}=\left(-1\right)^n\frac{\left(n-2\right)!}{\left(1+x\right)^{n-1}}\cdot\frac{x}{1+x}\left(n\ge2\right).
$$

$\blacksquare$

### 习题二

（习题 2.4-4）设有函数

$$
y=\begin{cases}e^{-1/x^2},&x\ne0,\0,&x=0.\end{cases}
$$

试证明: 该函数在 $0$ 点的一阶导数与二阶导数均为 $0$.

### 解答 习题二

一阶导数:

$$
f'\left(0\right)=\lim\limits_{x\to0}\frac{e^{-1/x^2}-0}{x}=\lim\limits_{t\to\infty}\frac{t}{e^{t^2}}=0\ \left(\text{令}t=1/x\text{, 指数增长快于幂函数}\right).
$$

二阶导数: 对 $x\ne0$, $f'\left(x\right)=\frac2{x^3}e^{-1/x^2}$. 故

$$
f''\left(0\right)=\lim\limits_{x\to0}\frac{f'\left(x\right)-0}{x}=\lim\limits_{x\to0}\frac{2e^{-1/x^2}}{x^4}=\lim\limits_{t\to\infty}\frac{2t^4}{e^{t^2}}=0.

$$

$\blacksquare$
### 习题三

（习题 2.4-6）设 $y=\frac{ax+b}{cx+d}$, 其中 $ad-bc=1$. 证明: 
(1) $y'=\frac1{\left(cx+d\right)^2}$;

(2) $y^{\left(n\right)}=\left(-1\right)^{n+1}\cdot\frac{n!\,c^{n-1}}{\left(cx+d\right)^{n+1}}$.

### 解答 习题三

(1)

$$
y'=\frac{a\left(cx+d\right)-c\left(ax+b\right)}{\left(cx+d\right)^2}=\frac{ad-bc}{\left(cx+d\right)^2}=\frac1{\left(cx+d\right)^2}.
$$

(2)对 $n$ 归纳. $n=1$ 时即(1). 假设 $y^{\left(n\right)}=\left(-1\right)^{n+1}\frac{n!c^{n-1}}{\left(cx+d\right)^{n+1}}$, 则

$$
y^{\left(n+1\right)}=\left(-1\right)^{n+1}n!c^{n-1}\cdot\left(-\left(n+1\right)\right)c\cdot\left(cx+d\right)^{-\left(n+2\right)}=\left(-1\right)^{n+2}\frac{\left(n+1\right)!c^n}{\left(cx+d\right)^{n+2}}.
$$

归纳完成. $\blacksquare$

### 习题四

（习题 2.4-7）设 $f_{ij}\left(x\right)\left(i,j=1,2\right)$ 在 $\left(a,b\right)$ 中无穷次可导. 令

$$
W\left(x\right)=\begin{vmatrix}f_{11}\left(x\right)&f_{12}\left(x\right)\f_{21}\left(x\right)&f_{22}\left(x\right)\end{vmatrix}.
$$
证明

$$
W'\left(x\right)=\begin{vmatrix}f'_{11}&f'_{12}\f_{21}&f_{22}\end{vmatrix}+\begin{vmatrix}f_{11}&f_{12}\f'_{21}&f'_{22}\end{vmatrix},
$$

并给出 $W^{\left(n\right)}\left(x\right)$ 的公式.

### 解答 习题四

$W=f_{11}f_{22}-f_{12}f_{21}$. 求导得

$$
W'=f'_{11}f_{22}+f_{11}f'_{22}-f'_{12}f_{21}-f_{12}f'_{21}=\begin{vmatrix}f'_{11}&f'_{12}\f_{21}&f_{22}\end{vmatrix}+\begin{vmatrix}f_{11}&f_{12}\f'_{21}&f'_{22}\end{vmatrix}.
$$

一般地, 由莱布尼茨公式, 

$$
W^{\left(n\right)}\left(x\right)=\sum_{k=0}^n\binom nk\begin{vmatrix}f_{11}^{\left(k\right)}&f_{12}^{\left(n-k\right)}\f_{21}&f_{22}\end{vmatrix}+\sum_{k=0}^n\binom nk\begin{vmatrix}f_{11}&f_{12}\f_{21}^{\left(k\right)}&f_{22}^{\left(n-k\right)}\end{vmatrix}.
$$

或更简洁地:

$$
W^{\left(n\right)}=\displaystyle\sum_{k=0}^n\binom nk\begin{vmatrix}f_{11}^{\left(k\right)}&f_{12}^{\left(k\right)}\f_{21}^{\left(n-k\right)}&f_{22}^{\left(n-k\right)}\end{vmatrix}.
$$

$\blacksquare$
