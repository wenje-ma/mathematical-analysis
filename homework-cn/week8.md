# week8

> **命题 1.7 (三角不等式)**
> 
> 对于任意实数 $a,b,c$, $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **定理 5.1 (函数极限四则运算)**
> 
> 若 $\lim f\left(x\right)=l_1$, $\lim g\left(x\right)=l_2$, 则 $\lim\left(f\pm g\right)=l_1\pm l_2$, $\lim\left(f\cdot g\right)=l_1\cdot l_2$, 且当 $l_2\ne0$ 时 $\lim\frac{f}{g}=\frac{l_1}{l_2}$.

> **命题 6.1 (重要极限 $\lim_{x\to0}\frac{\sin x}{x}=1$)**
> 
> $\lim_{x\to0}\frac{\sin x}{x}=1$.

> **定理 6.2 (函数的夹逼定理)**
> 
> 设 $y=f\left(x\right)$, $y=g\left(x\right)$, $y=h\left(x\right)$ 在 $a$ 点的一个空心邻域内有定义, 且 $h\left(x\right)\le f\left(x\right)\le g\left(x\right)$. 若 $\lim g\left(x\right)=\lim h\left(x\right)=l$, 则 $\lim f\left(x\right)=l$.

> **定理 7.2 (复合函数连续性)**
> 
> 若 $y=g\left(u\right)$ 在 $u_0$ 点连续, $u=f\left(x\right)$ 在 $x_0$ 点连续且 $f\left(x_0\right)=u_0$, 则复合函数 $y=g\left(f\left(x\right)\right)$ 在 $x_0$ 点连续.

## 1.6-4-3

求极限: $\lim_{x\to0}\left(\frac{1+x}{1-x}\right)^{1/x}$.

### 解答 1.6-4-3

$$
\left(\frac{1+x}{1-x}\right)^{1/x}=\left[\left(1+\frac{2x}{1-x}\right)^{\frac{1-x}{2x}}\right]^{\frac2{1-x}}.
$$

底数趋于 $e$, 指数 $\frac2{1-x}\to2$. 由重要极限数 $e$ 的函数版本 及**定理 6.2 (函数的夹逼定理)** 相关运算, 极限为 $e^2$. $\blacksquare$

## 1.6-4-5

求极限: $\lim_{y\to0}\left(1-5y\right)^{1/y}$.

### 解答 1.6-4-5

$$
\left(1-5y\right)^{1/y}=\left[\left(1+\frac1{-1/\left(5y\right)}\right)^{-1/\left(5y\right)}\right]^{-5}.
$$

底数趋于 $e$, 指数为 $-5$. 由重要极限数 $e$ 的函数版本, 极限为 $e^{-5}=\frac1{e^5}$. $\blacksquare$

## 1.6-4-6

求极限: $\lim_{x\to\infty}\left(1+\frac1x\right)^{x+100}$.

### 解答 1.6-4-6

$$
\left(1+\frac1x\right)^{x+100}=\left(1+\frac1x\right)^x\cdot\left(1+\frac1x\right)^{100}\to e\cdot1=e.
$$

$\blacksquare$

## 1.6-5

求出常数 $a$ 与 $b$, 使

$$
\lim_{x\to+\infty}\left[\frac{x^2+1}{x+1}-\left(ax+b\right)\right]=0.
$$

试说明几何意义.

### 解答 1.6-5

$$
\frac{x^2+1}{x+1}-ax-b=\frac{x^2+1-\left(ax+b\right)\left(x+1\right)}{x+1}=\frac{\left(1-a\right)x^2-\left(a+b\right)x+1-b}{x+1}.
$$

要使其趋于 $0$, 分子次数必须低于分母次数, 故 $1-a=0$ 且 $a+b=0$. 解得 $a=1$, $b=-1$.

几何意义: 直线 $y=x-1$ 是曲线 $y=\frac{x^2+1}{x+1}$ 当 $x\to+\infty$ 时的斜渐近线. $\blacksquare$

## 1.6-7

证明 $\lim_{x\to+\infty}\left(1+\frac1x\right)^{x^2}=+\infty$.

### 解答 1.6-7

$$
\left(1+\frac1x\right)^{x^2}=\left[\left(1+\frac1x\right)^x\right]^x.
$$

当 $x$ 充分大时 $\left(1+\frac1x\right)^x> 2$ (因趋于 $e> 2$), 故 $\left(1+\frac1x\right)^{x^2}> 2^x\to+\infty$. 因此极限为 $+\infty$. $\blacksquare$

## 1.6-9

设 $\lim_{x\to+\infty}\frac{f\left(x\right)}x=0$, 且 $f\left(x\right)> 0$ ($x> 0$). 证明 $\lim_{x\to+\infty}\left(1+\frac1x\right)^{f\left(x\right)}=1$.

### 解答 1.6-9

取对数:

$$
\left(1+\frac1x\right)^{f\left(x\right)}=e^{f\left(x\right)\ln\left(1+1/x\right)}.
$$

因

$$
0< f\left(x\right)\ln\left(1+\frac1x\right)< f\left(x\right)\cdot\frac1x\to0,
$$

由**定理 6.2 (函数的夹逼定理)**, 指数趋于 $0$. 由 $e^t$ 的连续性, 原极限为 $e^0=1$. $\blacksquare$

## 1.6-10

设 $y=D\left(x\right)$ 为狄利克雷函数. 证明: 对于任意一点 $a\in\mathbb R$, 极限 $\lim_{x\to a}D\left(x\right)$ 不存在.

### 解答 1.6-10

取有理序列 $\left\{r_n\right\}$ 和无理序列 $\left\{s_n\right\}$, 均以 $a$ 为极限 (由有理数与无理数的稠密性). 则 $D\left(r_n\right)=1\to1$, $D\left(s_n\right)=0\to0$. 两子序列极限不同, 由函数极限与序列极限的归结原则, $\lim_{x\to a}D\left(x\right)$ 不存在. $\blacksquare$

## 1.6-11

求极限: $\lim_{x\to+\infty}\frac{\left(\ln x\right)^5}{x}$.

### 解答 1.6-11

作变量替换 $y=\ln x$, 则 $x=e^y$, 当 $x\to+\infty$ 时 $y\to+\infty$. 原式化为 $\lim_{y\to+\infty}\frac{y^5}{e^y}=0$ (指数函数增长快于任何幂函数). $\blacksquare$

## 1.7-1

指出下列函数的间断点及其类型:

(1) $y=\operatorname{sgn}\left(\sin x\right)$;

(2)

$$
y=f\left(x\right)=\begin{cases}x^2e^x,&x> 0,\\sin\frac{\pi}{1+x^2},&x< 0,\\1,&x=0;\end{cases}
$$

(3) $y=\cos\left\{\left(x-\left[x\right]\right)\pi\right\}$;

(4)

$$
y=f\left(x\right)=\begin{cases}e^{\sin\frac1x},&x\ne0,\\0,&x=0.\end{cases}
$$

### 解答 1.7-1

(1) 当 $x=k\pi$ ($k\in\mathbb Z$) 时 $\sin x=0$, $\operatorname{sgn}\left(\sin x\right)$ 左右极限分别为 $1$ 与 $-1$ (或反之), 为第一类间断点 (跳跃间断点). 其余点连续.

(2) $x\to0+0$ 时 $f\left(x\right)=x^2e^x\to0$; $x\to0-0$ 时

$$
f\left(x\right)=\sin\frac{\pi}{1+x^2}\to\sin\pi=0.
$$

但 $f\left(0\right)=1$, 故 $x=0$ 为可去间断点 (第一类).

(3) $x-\left[x\right]=\left\{x\right\}$ 为小数部分, 在整数点处左右极限分别为 $\cos0=1$ 与 $\cos\pi=-1$, 故整数点为跳跃间断点 (第一类). 其余点连续.

(4) $x\to0$ 时 $\frac1x$ 振荡, $\sin\frac1x$ 在 $\left[-1,1\right]$ 内振荡, $e^{\sin\left(1/x\right)}$ 在 $e^{-1}$ 与 $e$ 之间振荡, 极限不存在, 故 $x=0$ 为第二类间断点 (振荡间断点). $\blacksquare$

## 1.7-2-2

试用 $\varepsilon$-$\delta$ 语言证明: 若 $y=f\left(x\right)$ 在 $a$ 点连续, 则 $y=\left|f\left(x\right)\right|$ 在 $a$ 点连续.

### 解答 1.7-2-2

由连续函数的定义, 任给 $\varepsilon> 0$, 存在 $\delta> 0$, 使得当 $\left|x-a\right|< \delta$ 时 $\left|f\left(x\right)-f\left(a\right)\right|< \varepsilon$. 由**命题 1.7 (三角不等式)**,

$$
\left|\left|f\left(x\right)\right|-\left|f\left(a\right)\right|\right|\le\left|f\left(x\right)-f\left(a\right)\right|< \varepsilon.
$$

故 $\left|f\left(x\right)\right|$ 在 $a$ 点连续. $\blacksquare$

## 1.7-3

利用初等函数的连续性求下列极限:

(1) $\lim_{x\to0}\cos\left(\sqrt{1+x^2}-1\right)$;

(2) $\lim_{x\to0}e^{\frac{\sin x}{\sin2x}}$;

(3) $\lim_{x\to\infty}\arctan\frac{\sqrt{x^4+2}}{1+x^2}$;

(4) $\lim_{x\to5}x^{\sqrt x}$;

(5) $\lim_{x\to\infty}\left(1+\frac1x+\frac1{x^2}\right)^{x+\sqrt x}$.

### 解答 1.7-3

(1) 由**定理 7.2 (复合函数连续性)**, $\lim_{x\to0}\left(\sqrt{1+x^2}-1\right)=0$, 故原式 $=\cos0=1$.

(2) $\frac{\sin x}{\sin2x}\to\frac12$, 由 $e^u$ 的连续性, 原式 $=e^{1/2}=\sqrt e$.

(3) $\frac{\sqrt{x^4+2}}{1+x^2}\to1$, 由 $\arctan u$ 的连续性, 原式 $=\arctan1=\frac\pi4$.

(4) $x^{\sqrt x}=e^{\sqrt x\ln x}$, $\sqrt x\ln x\to\sqrt5\ln5$, 由连续性, 原式 $=e^{\sqrt5\ln5}=5^{\sqrt5}$.

(5)

$$
\left(1+\frac1x+\frac1{x^2}\right)^{x+\sqrt x}=\left[\left(1+\frac{x+1}{x^2}\right)^{\frac{x^2}{x+1}}\right]^{\frac{\left(x+\sqrt x\right)\left(x+1\right)}{x^2}}.
$$

底数趋于 $e$, 指数趋于 $1$, 故原式 $=e$. $\blacksquare$
