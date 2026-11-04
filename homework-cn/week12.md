# week12

> **定理 5.1 (参变量函数求导公式)**
> 
> 设 $x=\varphi\left(t\right)$, $y=\psi\left(t\right)$ 在 $t_0$ 点可导, 且 $\varphi'\left(t_0\right)\ne0$, 则参变量函数的导数为 $\frac{\mathrm dy}{\mathrm dx}=\frac{\psi'\left(t\right)}{\varphi'\left(t\right)}$.

## 2.4-4

设有函数

$$
y=\begin{cases}e^{-1/x^2},&x\ne0,\\0,&x=0.\end{cases}
$$

试证明: 该函数在 $0$ 点的一阶导数与二阶导数均为 $0$.

### 解答 2.4-4

一阶导数:

$$
f'\left(0\right)=\lim_{x\to0}\frac{e^{-1/x^2}-0}{x}=\lim_{t\to\infty}\frac{t}{e^{t^2}}=0\quad\left(\text{令 }t=1/x,\text{ 指数增长快于幂函数}\right).
$$

二阶导数: 对 $x\ne0$, $f'\left(x\right)=\frac2{x^3}e^{-1/x^2}$. 故

$$
f''\left(0\right)=\lim_{x\to0}\frac{f'\left(x\right)-0}{x}=\lim_{x\to0}\frac{2e^{-1/x^2}}{x^4}=\lim_{t\to\infty}\frac{2t^4}{e^{t^2}}=0.
$$

$\blacksquare$

## 2.4-6

设 $y=\frac{ax+b}{cx+d}$, 其中 $ad-bc=1$. 证明:

(1) $y'=\frac1{\left(cx+d\right)^2}$;

(2) $y^{\left(n\right)}=\left(-1\right)^{n+1}\cdot\frac{n!\,c^{n-1}}{\left(cx+d\right)^{n+1}}$.

### 解答 2.4-6

(1)

$$
y'=\frac{a\left(cx+d\right)-c\left(ax+b\right)}{\left(cx+d\right)^2}=\frac{ad-bc}{\left(cx+d\right)^2}=\frac1{\left(cx+d\right)^2}.
$$

(2) 对 $n$ 归纳. $n=1$ 时即 (1). 假设 $y^{\left(n\right)}=\left(-1\right)^{n+1}\frac{n!c^{n-1}}{\left(cx+d\right)^{n+1}}$, 则

$$
y^{\left(n+1\right)}=\left(-1\right)^{n+1}n!c^{n-1}\cdot\left(-\left(n+1\right)\right)c\cdot\left(cx+d\right)^{-\left(n+2\right)}=\left(-1\right)^{n+2}\frac{\left(n+1\right)!c^n}{\left(cx+d\right)^{n+2}}.
$$

归纳完成. $\blacksquare$

## 2.4-7

设 $f_{ij}\left(x\right)$ ($i,j=1,2$) 在 $\left(a,b\right)$ 中无穷次可导. 令

$$
W\left(x\right)=\begin{vmatrix}f_{11}\left(x\right)&f_{12}\left(x\right)\\f_{21}\left(x\right)&f_{22}\left(x\right)\end{vmatrix}.
$$

证明

$$
W'\left(x\right)=\begin{vmatrix}f'_{11}&f'_{12}\\f_{21}&f_{22}\end{vmatrix}+\begin{vmatrix}f_{11}&f_{12}\\f'_{21}&f'_{22}\end{vmatrix},
$$

并给出 $W^{\left(n\right)}\left(x\right)$ 的公式.

### 解答 2.4-7

$W=f_{11}f_{22}-f_{12}f_{21}$. 求导得

$$
W'=f'_{11}f_{22}+f_{11}f'_{22}-f'_{12}f_{21}-f_{12}f'_{21}=\begin{vmatrix}f'_{11}&f'_{12}\\f_{21}&f_{22}\end{vmatrix}+\begin{vmatrix}f_{11}&f_{12}\\f'_{21}&f'_{22}\end{vmatrix}.
$$

一般地, 由莱布尼茨公式,

$$
W^{\left(n\right)}\left(x\right)=\sum_{k=0}^n\binom nk\begin{vmatrix}f_{11}^{\left(k\right)}&f_{12}^{\left(n-k\right)}\\f_{21}&f_{22}\end{vmatrix}+\sum_{k=0}^n\binom nk\begin{vmatrix}f_{11}&f_{12}\\f_{21}^{\left(k\right)}&f_{22}^{\left(n-k\right)}\end{vmatrix}.
$$

或更简洁地:

$$
W^{\left(n\right)}=\sum_{k=0}^n\binom nk\begin{vmatrix}f_{11}^{\left(k\right)}&f_{12}^{\left(k\right)}\\f_{21}^{\left(n-k\right)}&f_{22}^{\left(n-k\right)}\end{vmatrix}.
$$

$\blacksquare$

## 2.5-1-2

求下列参变量函数的导数 $\frac{\mathrm dy}{\mathrm dx}$: $\begin{cases}x=t\ln t,\\y=e^t.\end{cases}$

### 解答 2.5-1-2

$\frac{\mathrm dx}{\mathrm dt}=\ln t+1$, $\frac{\mathrm dy}{\mathrm dt}=e^t$. 由**定理 5.1 (参变量函数求导公式)**,

$$
\frac{\mathrm dy}{\mathrm dx}=\frac{e^t}{\ln t+1}.
$$

$\blacksquare$

## 2.5-1-4

求下列参变量函数的导数 $\frac{\mathrm dy}{\mathrm dx}$: $\begin{cases}x=\cos^4t,\\y=\sin^4t.\end{cases}$

### 解答 2.5-1-4

$\frac{\mathrm dx}{\mathrm dt}=-4\cos^3t\sin t$, $\frac{\mathrm dy}{\mathrm dt}=4\sin^3t\cos t$. 由**定理 5.1 (参变量函数求导公式)**,

$$
\frac{\mathrm dy}{\mathrm dx}=\frac{4\sin^3t\cos t}{-4\cos^3t\sin t}=-\tan^2t.
$$

$\blacksquare$

## 2.5-3

设曲线方程为 $\begin{cases}x=1-t^2,\\y=t-t^2.\end{cases}$ 求在 $t=1$ 及 $t=\frac{\sqrt2}2$ 时曲线的切线方程.

### 解答 2.5-3

$\frac{\mathrm dx}{\mathrm dt}=-2t$, $\frac{\mathrm dy}{\mathrm dt}=1-2t$, $\frac{\mathrm dy}{\mathrm dx}=\frac{1-2t}{-2t}=\frac{2t-1}{2t}$.

当 $t=1$ 时: $x=0$, $y=0$, 斜率 $k=\frac{2-1}{2}=\frac12$. 切线方程: $y=\frac12x$.

当 $t=\frac{\sqrt2}2$ 时: $x=1-\frac12=\frac12$, $y=\frac{\sqrt2}2-\frac12=\frac{\sqrt2-1}2$, 斜率 $k=\frac{\sqrt2-1}{\sqrt2}=1-\frac{\sqrt2}2$. 切线方程:

$$
y-\frac{\sqrt2-1}2=\left(1-\frac{\sqrt2}2\right)\left(x-\frac12\right).
$$

$\blacksquare$

## 2.5-4

设 $x=\varphi\left(t\right)$, $y=\psi\left(t\right)$ 在 $t_0$ 点可导, 且 $\varphi'\left(t_0\right)\ne0$. 令 $\Delta t\ne0$,

$$
\Delta x=\varphi\left(t_0+\Delta t\right)-\varphi\left(t_0\right),\quad\Delta y=\psi\left(t_0+\Delta t\right)-\psi\left(t_0\right).
$$

试证明 $\lim_{\Delta t\to0}\frac{\Delta y}{\Delta x}=\frac{\psi'\left(t_0\right)}{\varphi'\left(t_0\right)}$.

### 解答 2.5-4

$$
\frac{\Delta y}{\Delta x}=\frac{\psi\left(t_0+\Delta t\right)-\psi\left(t_0\right)}{\varphi\left(t_0+\Delta t\right)-\varphi\left(t_0\right)}=\frac{\frac{\psi\left(t_0+\Delta t\right)-\psi\left(t_0\right)}{\Delta t}}{\frac{\varphi\left(t_0+\Delta t\right)-\varphi\left(t_0\right)}{\Delta t}}.
$$

当 $\Delta t\to0$ 时, 分子趋于 $\psi'\left(t_0\right)$, 分母趋于 $\varphi'\left(t_0\right)\ne0$. 由极限四则运算,

$$
\lim_{\Delta t\to0}\frac{\Delta y}{\Delta x}=\frac{\psi'\left(t_0\right)}{\varphi'\left(t_0\right)}.
$$

$\blacksquare$
