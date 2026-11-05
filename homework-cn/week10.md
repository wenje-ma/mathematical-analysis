# week10

> **定理 2.1 (复合函数求导法则)**
> 
> 设 $y=f\left(u\right)$ 在 $u$ 处可导, $u=g\left(x\right)$ 在 $x$ 处可导, 则复合函数 $y=f\left(g\left(x\right)\right)$ 在 $x$ 处可导, 且 $\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{\mathrm{d}y}{\mathrm{d}u}\cdot\frac{\mathrm{d}u}{\mathrm{d}x}=f'\left(g\left(x\right)\right)g'\left(x\right)$.

> **定理 8.1 (中间值定理)**
> 
> 设 $y=f\left(x\right)$ 在闭区间 $\left[a,b\right]$ 上连续, 且 $f\left(a\right)$ 与 $f\left(b\right)$ 反号, 则存在一点 $c\in\left(a,b\right)$ 使得 $f\left(c\right)=0$. 更一般地, $f$ 可取到 $f\left(a\right)$ 与 $f\left(b\right)$ 之间的一切值.

> **定理 8.2 (有界性定理)**
> 
> 闭区间上的连续函数是有界的, 且达到最大值与最小值.

## 1.8-6

设 $f:\left[0,1\right]\to\left[0,1\right]$ 为连续映射. 证明: 它在 $\left[0,1\right]$ 中至少有一个不动点, 也即存在一个点 $x_0\in\left[0,1\right]$, 使得 $f\left(x_0\right)=x_0$.

### 解答 1.8-6

令 $g\left(x\right)=f\left(x\right)-x$. 则 $g\left(0\right)=f\left(0\right)\ge0$, $g\left(1\right)=f\left(1\right)-1\le0$. 由**定理 8.1 (中间值定理)**, 存在 $x_0\in\left[0,1\right]$ 使 $g\left(x_0\right)=0$, 即 $f\left(x_0\right)=x_0$. $\blacksquare$

## 1.8-7

设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 且 $f\left(a\right)=f\left(b\right)$. 证明: 在 $\left[a,b\right]$ 中一定存在两点 $x_1$ 与 $x_2$, 使得 $\left|x_1-x_2\right|=\frac12\left(b-a\right)$, 且 $f\left(x_1\right)=f\left(x_2\right)$.

### 解答 1.8-7

令 $d=\frac{b-a}2$, 考虑辅助函数 $g\left(x\right)=f\left(x+d\right)-f\left(x\right)$, $x\in\left[a,b-d\right]=\left[a,a+d\right]$. 则

$$
g\left(a\right)=f\left(a+d\right)-f\left(a\right),\quad{g}\left(a+d\right)=f\left(b\right)-f\left(a+d\right)=f\left(a\right)-f\left(a+d\right)=-g\left(a\right).
$$

若 $g\left(a\right)=0$, 则取 $x_1=a$, $x_2=a+d$ 即可. 若 $g\left(a\right)\ne0$, 则 $g\left(a\right)$ 与 $g\left(a+d\right)$ 反号, 由**定理 8.1 (中间值定理)**, 存在 $\xi\in\left(a,a+d\right)$ 使 $g\left(\xi\right)=0$, 即 $f\left(\xi+d\right)=f\left(\xi\right)$. 取 $x_1=\xi$, $x_2=\xi+d$, 则 $\left|x_1-x_2\right|=d=\frac{b-a}2$. $\blacksquare$

## 1.8-8

设 $E$ 为 $\mathbb{R}$ 中一个有界无穷集合. 证明: 存在一点 $c\in\mathbb{R}$, 使得 $c$ 点的任何一个空心邻域 $\left(c-\delta,c+\delta\right)\backslash\left\{c\right\}$ 中都有 $E$ 的点.

### 解答 1.8-8

因 $E$ 有界, 设 $E\subset\left[a,b\right]$. 将 $\left[a,b\right]$ 平分为两个闭区间, 其中至少一个包含 $E$ 的无穷多个点, 记为 $\left[a_1,b_1\right]$. 如此继续, 得区间套 $\left\{\left[a_n,b_n\right]\right\}$, 每个 $\left[a_n,b_n\right]$ 含 $E$ 的无穷多点, 且

$$
b_n-a_n=\frac{b-a}{2^n}\to0.
$$

由区间套原理, 存在唯一 $c\in\bigcap\left[a_n,b_n\right]$. 对任意 $\delta>0$, 当 $n$ 充分大时 $\left[a_n,b_n\right]\subset\left(c-\delta,c+\delta\right)$, 而 $\left[a_n,b_n\right]$ 含 $E$ 的无穷多点, 故 $\left(c-\delta,c+\delta\right)\backslash\left\{c\right\}$ 中必有 $E$ 的点. $\blacksquare$

## 1.8-9

设 $E$ 为 $\mathbb{R}$ 中非空有上界的集合. 证明: $E$ 的上界中有最小上界, 也即存在 $M_0$, $M_0$ 本身是 $E$ 的上界, 而对于 $E$ 的任意一个上界 $M$, 都有 $M_0\le{M}$.

### 解答 1.8-9

设 $E\subset\left[a,b\right]$, 其中 $b$ 为 $E$ 的一个上界. 将 $\left[a,b\right]$ 平分为两个闭区间. 若右半区间含 $E$ 的上界, 则取右半; 否则取左半 (此时左半右端点为新的上界). 如此继续, 得区间套 $\left\{\left[a_n,b_n\right]\right\}$, 每个 $b_n$ 为 $E$ 的上界, 每个 $a_n$ 不是 $E$ 的上界.

由区间套原理, 存在唯一 $M_0\in\bigcap\left[a_n,b_n\right]$. 因 $b_n\to{M}_0$ 且 $b_n$ 为上界, 对任意 $x\in{E}$, $x\le{b}_n$, 令 $n\to\infty$ 得 $x\le{M}_0$, 即 $M_0$ 为上界. 又若 $M$ 为任一上界, 则 $M\ge{a}_n$ 对一切 $n$ (因 $a_n$ 不是上界, 存在 $x\in{E}$ 使 $x>{}a_n$, 而 $M\ge{x}$), 故 $M\ge{M}_0$. $\blacksquare$

## 1.8-11

设 $y=f\left(x\right)$ 在 $a$ 点附近有定义, 且有极限 $\lim_{x\to{a}}f\left(x\right)=0$. 又设 $y=g\left(x\right)$ 在 $a$ 点附近有定义, 且是有界函数. 证明: $\lim_{x\to{a}}f\left(x\right)g\left(x\right)=0$.

### 解答 1.8-11

设 $\left|g\left(x\right)\right|\le{M}$. 任给 $\varepsilon>0$, 因 $f\left(x\right)\to0$, 存在 $\delta>0$ 使得当 $0<\left|x-a\right|<\delta$ 时 $\left|f\left(x\right)\right|<\varepsilon/M$. 于是

$$
\left|f\left(x\right)g\left(x\right)\right|\le{M}\left|f\left(x\right)\right|<\varepsilon.
$$

故 $\lim{f}\left(x\right)g\left(x\right)=0$. $\blacksquare$

## 2.2-2

设 $f\left(x\right)=1+x^2$, 求 $f'\left(\sin{x}\right)$ 及 $\left[f\left(\sin{x}\right)\right]'$.

### 解答 2.2-2

$f'\left(x\right)=2x$, 故 $f'\left(\sin{x}\right)=2\sin{x}$.

由**定理 2.1 (复合函数求导法则)**,

$$
\left[f\left(\sin{x}\right)\right]'=f'\left(\sin{x}\right)\cdot\left(\sin{x}\right)'=2\sin{x}\cos{x}=\sin2x.
$$

$\blacksquare$

## 2.2-3-2

求导函数: $y=\sqrt{1+x^2}$.

### 解答 2.2-3-2

$$
y'=\frac1{2\sqrt{1+x^2}}\cdot\left(1+x^2\right)'=\frac{2x}{2\sqrt{1+x^2}}=\frac{x}{\sqrt{1+x^2}}.
$$

$\blacksquare$

## 2.2-3-4

求导函数: $y=\frac12\sqrt{a^2-x^2}$.

### 解答 2.2-3-4

$$
y'=\frac12\cdot\frac1{2\sqrt{a^2-x^2}}\cdot\left(-2x\right)=-\frac{x}{2\sqrt{a^2-x^2}}.
$$

$\blacksquare$

## 2.2-3-6

求导函数: $y=\frac12\left(e^x-e^{-x}\right)$.

### 解答 2.2-3-6

$$
y'=\frac12\left(e^x-\left(-e^{-x}\right)\right)=\frac12\left(e^x+e^{-x}\right).
$$

$\blacksquare$

## 2.2-3-8

求导函数: $y=\sqrt{x^3+x+1}$.

### 解答 2.2-3-8

$$
y'=\frac1{2\sqrt{x^3+x+1}}\cdot\left(3x^2+1\right)=\frac{3x^2+1}{2\sqrt{x^3+x+1}}.
$$

$\blacksquare$

## 2.2-3-10

求导函数: $y=e^x+e^{x^2}+\cos{x}^2$.

### 解答 2.2-3-10

$$
y'=e^x+e^{x^2}\cdot2x-\sin{x}^2\cdot2x=e^x+2xe^{x^2}-2x\sin{x}^2.
$$

$\blacksquare$

## 2.2-3-12

求导函数: $y=\arctan{x}^2$.

### 解答 2.2-3-12

$$
y'=\frac1{1+\left(x^2\right)^2}\cdot2x=\frac{2x}{1+x^4}.
$$

$\blacksquare$
