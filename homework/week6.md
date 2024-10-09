# week6

> **定理 2.1 (复合函数求导法则)**
> 
> 设 $y=f\left(u\right)$ 在 $u$ 处可导, $u=g\left(x\right)$ 在 $x$ 处可导, 则复合函数 $y=f\left(g\left(x\right)\right)$ 在 $x$ 处可导, 且 $\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{\mathrm{d}y}{\mathrm{d}u}\cdot\frac{\mathrm{d}u}{\mathrm{d}x}=f'\left(g\left(x\right)\right)g'\left(x\right)$.

## 2.3-3-1

计算下列函数在指定点 $x_0$ 的微分: $f\left(x\right)=x^2\arcsin{x}$, $x_0=0$.

### 解答 2.3-3-1

$$
f'\left(x\right)=2x\arcsin{x}+\frac{x^2}{\sqrt{1-x^2}}.
$$

$f'\left(0\right)=0$. 故 $\left.\mathrm{d}f\right|_{x_0=0}=0\cdot\mathrm{d}x=0$.

$\blacksquare$

## 2.3-3-4

计算下列函数在指定点 $x_0$ 的微分: $f\left(x\right)=x\ln\left(1+x\right)$, $x_0=0$.

### 解答 2.3-3-4

$f'\left(x\right)=\ln\left(1+x\right)+\frac{x}{1+x}$. $f'\left(0\right)=0$. 故 $\left.\mathrm{d}f\right|_{x_0=0}=0$.

$\blacksquare$

## 2.3-4-2

求函数的微分: $f\left(x\right)=\ln\left(x+\sqrt{x^2+1}\right)$.

### 解答 2.3-4-2

$$
f'\left(x\right)=\frac1{x+\sqrt{x^2+1}}\cdot\left(1+\frac{x}{\sqrt{x^2+1}}\right)=\frac1{x+\sqrt{x^2+1}}\cdot\frac{\sqrt{x^2+1}+x}{\sqrt{x^2+1}}=\frac1{\sqrt{x^2+1}}.
$$

故 $\mathrm{d}f=\frac1{\sqrt{x^2+1}}\mathrm{d}x$.

$\blacksquare$

## 2.3-4-4

求函数的微分: $f\left(x\right)=\sqrt{1+x^2}+\sqrt{x}\sin{x}$.

### 解答 2.3-4-4

$$
f'\left(x\right)=\frac{x}{\sqrt{1+x^2}}+\frac1{2\sqrt{x}}\sin{x}+\sqrt{x}\cos{x}.
$$

故

$$
\mathrm{d}f=\left(\frac{x}{\sqrt{1+x^2}}+\frac{\sin{x}}{2\sqrt{x}}+\sqrt{x}\cos{x}\right)\mathrm{d}x.
$$

$\blacksquare$

## 2.3-5-1

填空: $\mathrm{d}\left(\right)=x^n\mathrm{d}x$.

### 解答 2.3-5-1

$$
\mathrm{d}\left(\frac{x^{n+1}}{n+1}\right)=x^n\mathrm{d}x\quad\left(n\ne-1\right).
$$

$\blacksquare$

## 2.3-5-3

填空: $\mathrm{d}\left(\right)=\left(e^x+\sin2x\right)\mathrm{d}x$.

### 解答 2.3-5-3

$$
\mathrm{d}\left(e^x-\frac12\cos2x\right)=\left(e^x+\sin2x\right)\mathrm{d}x.
$$

$\blacksquare$

## 2.3-5-5

填空: $\mathrm{d}\left(\right)=\frac{\sin{x}}{\cos{x}}\mathrm{d}x$.

### 解答 2.3-5-5

$\mathrm{d}\left(-\ln\left|\cos{x}\right|\right)=\frac{\sin{x}}{\cos{x}}\mathrm{d}x$.

$\blacksquare$

## 2.3-6

计算 $\tan\left(\frac\pi4+0.01\right)$ 的近似值.

### 解答 2.3-6

令 $f\left(x\right)=\tan{x}$, 取 $x_0=\frac\pi4$, $\Delta{x}=0.01$. $f'\left(x\right)=\sec^2x$, $f'\left(\frac\pi4\right)=2$. 由微分的定义 导出的近似公式

$$
f\left(x_0+\Delta{x}\right)\approx{f}\left(x_0\right)+f'\left(x_0\right)\Delta{x},
$$

$$
\tan\left(\frac\pi4+0.01\right)\approx\tan\frac\pi4+2\times0.01=1+0.02=1.02.
$$

$\blacksquare$

## 2.4-1

求下列函数的 $n$ 阶导数:

(1) $y=x^2e^x$;

(4) $y=x\ln\left(1+x\right)$.

### 解答 2.4-1

由高阶导数的定义, $n$ 阶导数由 $n-1$ 阶导数再求导得到.

(1) 由莱布尼茨公式, 其中 $u=x^2$, $v=e^x$.

$$
u'=2x,\quad{u}''=2,\quad{u}^{\left(k\right)}=0\quad\left(k\ge3\right).
$$

故

$$
y^{\left(n\right)}=x^2e^x+2nxe^x+n\left(n-1\right)e^x=e^x\left[x^2+2nx+n\left(n-1\right)\right].
$$

(4) $y'=\ln\left(1+x\right)+\frac{x}{1+x}$.

$$
y''=\frac1{1+x}+\frac1{\left(1+x\right)^2}=\frac{2+x}{\left(1+x\right)^2}.
$$

一般地, 对 $n\ge2$,

$$
y^{\left(n\right)}=\left(-1\right)^n\frac{\left(n-2\right)!}{\left(1+x\right)^{n-1}}+\left(-1\right)^{n-1}\frac{\left(n-1\right)!}{\left(1+x\right)^n}.
$$

化简得

$$
y^{\left(n\right)}=\left(-1\right)^n\frac{\left(n-2\right)!}{\left(1+x\right)^{n-1}}\cdot\frac{x}{1+x}\quad\left(n\ge2\right).
$$

$\blacksquare$

## 2.4-4

设有函数

$$
y=\begin{cases}e^{-1/x^2},&x\ne0,\\0,&x=0.\end{cases}
$$

试证明: 该函数在 $0$ 点的一阶导数与二阶导数均为 $0$.

### 解答 2.4-4

一阶导数:

$$
f'\left(0\right)=\lim_{x\to0}\frac{e^{-1/x^2}-0}{x}=\lim_{t\to\infty}\frac{t}{e^{t^2}}=0\quad\left(\text{令~}t=1/x,\text{~指数增长快于幂函数}\right).
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

归纳完成.

$\blacksquare$

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
W^{\left(n\right)}\left(x\right)=\sum_{k=0}^n\binom{n}k\begin{vmatrix}f_{11}^{\left(k\right)}&f_{12}^{\left(n-k\right)}\\f_{21}&f_{22}\end{vmatrix}+\sum_{k=0}^n\binom{n}k\begin{vmatrix}f_{11}&f_{12}\\f_{21}^{\left(k\right)}&f_{22}^{\left(n-k\right)}\end{vmatrix}.
$$

或更简洁地:

$$
W^{\left(n\right)}=\sum_{k=0}^n\binom{n}k\begin{vmatrix}f_{11}^{\left(k\right)}&f_{12}^{\left(k\right)}\\f_{21}^{\left(n-k\right)}&f_{22}^{\left(n-k\right)}\end{vmatrix}.
$$

$\blacksquare$

## 2.5-1-2

求下列参变量函数的导数 $\frac{\mathrm{d}y}{\mathrm{d}x}$: $\begin{cases}x=t\ln{t},\\y=e^t.\end{cases}$

### 解答 2.5-1-2

$\frac{\mathrm{d}x}{\mathrm{d}t}=\ln{t}+1$, $\frac{\mathrm{d}y}{\mathrm{d}t}=e^t$. 由**定理 5.1 (参变量函数求导公式)**,

$$
\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{e^t}{\ln{t}+1}.
$$

$\blacksquare$

## 2.5-1-4

求下列参变量函数的导数 $\frac{\mathrm{d}y}{\mathrm{d}x}$: $\begin{cases}x=\cos^4t,\\y=\sin^4t.\end{cases}$

### 解答 2.5-1-4

$\frac{\mathrm{d}x}{\mathrm{d}t}=-4\cos^3t\sin{t}$, $\frac{\mathrm{d}y}{\mathrm{d}t}=4\sin^3t\cos{t}$. 由**定理 5.1 (参变量函数求导公式)**,

$$
\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{4\sin^3t\cos{t}}{-4\cos^3t\sin{t}}=-\tan^2t.
$$

$\blacksquare$

## 2.5-3

设曲线方程为 $\begin{cases}x=1-t^2,\\y=t-t^2.\end{cases}$ 求在 $t=1$ 及 $t=\frac{\sqrt2}2$ 时曲线的切线方程.

### 解答 2.5-3

$\frac{\mathrm{d}x}{\mathrm{d}t}=-2t$, $\frac{\mathrm{d}y}{\mathrm{d}t}=1-2t$, $\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{1-2t}{-2t}=\frac{2t-1}{2t}$.

当 $t=1$ 时: $x=0$, $y=0$, 斜率 $k=\frac{2-1}{2}=\frac12$. 切线方程: $y=\frac12x$.

当 $t=\frac{\sqrt2}2$ 时: $x=1-\frac12=\frac12$, $y=\frac{\sqrt2}2-\frac12=\frac{\sqrt2-1}2$, 斜率 $k=\frac{\sqrt2-1}{\sqrt2}=1-\frac{\sqrt2}2$. 切线方程:

$$
y-\frac{\sqrt2-1}2=\left(1-\frac{\sqrt2}2\right)\left(x-\frac12\right).
$$

$\blacksquare$

## 2.5-4

设 $x=\varphi\left(t\right)$, $y=\psi\left(t\right)$ 在 $t_0$ 点可导, 且 $\varphi'\left(t_0\right)\ne0$. 令 $\Delta{t}\ne0$,

$$
\Delta{x}=\varphi\left(t_0+\Delta{t}\right)-\varphi\left(t_0\right),\quad\Delta{y}=\psi\left(t_0+\Delta{t}\right)-\psi\left(t_0\right).
$$

试证明 $\lim_{\Delta{t}\to0}\frac{\Delta{y}}{\Delta{x}}=\frac{\psi'\left(t_0\right)}{\varphi'\left(t_0\right)}$.

### 解答 2.5-4

$$
\frac{\Delta{y}}{\Delta{x}}=\frac{\psi\left(t_0+\Delta{t}\right)-\psi\left(t_0\right)}{\varphi\left(t_0+\Delta{t}\right)-\varphi\left(t_0\right)}=\frac{\frac{\psi\left(t_0+\Delta{t}\right)-\psi\left(t_0\right)}{\Delta{t}}}{\frac{\varphi\left(t_0+\Delta{t}\right)-\varphi\left(t_0\right)}{\Delta{t}}}.
$$

当 $\Delta{t}\to0$ 时, 分子趋于 $\psi'\left(t_0\right)$, 分母趋于 $\varphi'\left(t_0\right)\ne0$. 由极限四则运算,

$$
\lim_{\Delta{t}\to0}\frac{\Delta{y}}{\Delta{x}}=\frac{\psi'\left(t_0\right)}{\varphi'\left(t_0\right)}.
$$

$\blacksquare$
