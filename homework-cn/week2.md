# week2

> **命题 2.1 (有界函数的充要条件)**
> 
> 函数 $f:X\to{Y}$ 为有界函数的充分与必要条件是存在一个 $M>0$, 使得 $\left|f\left(x\right)\right|\le{M}$ 对一切 $x\in{X}$ 成立.

## 1.2-1

求下列函数的定义域:

(1) $y=\sqrt{x^2-16}$;

(2) $y=\frac{1}{\sqrt{x^2-3x+2}}$;

(3) $y=\ln\frac{x^2-2}{2}$;

(4) $y=\arccos\left(2\sin{x}\right)$.

### 解答 1.2-1

(1) 要使 $\sqrt{x^2-16}$ 有意义, 须 $x^2-16\ge0$, 即 $\left|x\right|\ge4$. 故定义域为 $\left(-\infty,-4\right]\cup\left[4,+\infty\right)$.

(2) 要使 $\frac{1}{\sqrt{x^2-3x+2}}$ 有意义, 须 $x^2-3x+2>0$, 即 $\left(x-1\right)\left(x-2\right)>0$, 亦即 $x<1$ 或 $x>2$. 故定义域为 $\left(-\infty,1\right)\cup\left(2,+\infty\right)$.

(3) 要使 $\ln\frac{x^2-2}{2}$ 有意义, 须 $\frac{x^2-2}{2}>0$, 即 $x^2>2$, 亦即 $\left|x\right|>\sqrt2$. 故定义域为

$$
\left(-\infty,-\sqrt2\right)\cup\left(\sqrt2,+\infty\right).
$$

(4) 要使 $\arccos\left(2\sin{x}\right)$ 有意义, 须 $\left|2\sin{x}\right|\le1$, 即 $\left|\sin{x}\right|\le\frac12$. 这等价于

$$
x\in\left[k\pi-\frac{\pi}{6},k\pi+\frac{\pi}{6}\right],\quad{k}\in\mathbb{Z}.
$$

故定义域为 $\displaystyle\bigcup_{k\in\mathbb{Z}}\left[k\pi-\frac{\pi}{6},k\pi+\frac{\pi}{6}\right]$. $\blacksquare$

## 1.2-2

求下列函数 $f$ 的值域 $f\left(X\right)$, 其中 $X$ 为题中指定的定义域:

(1)

$$
f\left(x\right)=\sqrt{1+x^2},\quad{X}=\left(0,5\right);
$$

(2)

$$
f\left(x\right)=\sin\frac1x,\quad{X}=\mathbb{R}\backslash\left\{0\right\};
$$

(3) $f\left(x\right)=\left\{x\right\}$ ($x$ 的小数部分), $X=\mathbb{R}$;

(4)

$$
f\left(x\right)=x^3+x+1,\quad{X}=\mathbb{R}.
$$

### 解答 1.2-2

(1) 当 $x\in\left(0,5\right)$ 时, $x^2\in\left(0,25\right)$, 故 $1+x^2\in\left(1,26\right)$, 从而 $\sqrt{1+x^2}\in\left(1,\sqrt{26}\right)$. 由函数的定义, $f\left(X\right)=\left(1,\sqrt{26}\right)$.

(2) 当 $x$ 遍历 $\mathbb{R}\backslash\left\{0\right\}$ 时, $\frac1x$ 遍历 $\mathbb{R}\backslash\left\{0\right\}$. 而 $\sin{t}$ 在 $t\in\mathbb{R}$ 上的值域为 $\left[-1,1\right]$, 去掉一个点 $t=0$ (对应 $\sin0=0$) 不影响值域 ($0$ 仍可取到, 如 $t=\pi$). 故 $f\left(X\right)=\left[-1,1\right]$.

(3) 对任意 $x\in\mathbb{R}$, 其小数部分 $\left\{x\right\}=x-\left[x\right]$ 满足 $0\le\left\{x\right\}<1$. 反之, 对任意 $y\in\left[0,1\right)$, 取 $x=y$ 即得 $\left\{x\right\}=y$. 故 $f\left(X\right)=\left[0,1\right)$.

(4) $f'\left(x\right)=3x^2+1>0$, 故 $f$ 在 $\mathbb{R}$ 上严格单调递增. 又当 $x\to-\infty$ 时 $f\left(x\right)\to-\infty$, 当 $x\to+\infty$ 时 $f\left(x\right)\to+\infty$. 故由介值性, $f\left(X\right)=\mathbb{R}$. $\blacksquare$

## 1.2-6

设 $f:\left[a,b\right]\to\left[a,b\right]$ 是满足下列条件的一个函数:

$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|\le{k}\left|x_1-x_2\right|,\quad\forall{x}_1,x_2\in\left[a,b\right],
$$

其中 $k<1$ 为常数. 又设存在一点 $c\in\left(a,b\right)$ 使 $f\left(c\right)=c$. 证明: $\left|f_n\left(x\right)-c\right|\le{k}^n\left(b-a\right)$, 其中 $f_n$ 为 $f$ 的 $n$ 重复合函数.

### 解答 1.2-6

因 $f\left(c\right)=c$, 由归纳法易得 $f_n\left(c\right)=c$ ($n=1$ 时即 $f\left(c\right)=c$; 若 $f_n\left(c\right)=c$, 则 $f_{n+1}\left(c\right)=f\left(f_n\left(c\right)\right)=f\left(c\right)=c$).

对任意 $x\in\left[a,b\right]$, 反复应用题设的利普希茨条件:

$$
\left|f_n\left(x\right)-c\right|=\left|f_n\left(x\right)-f_n\left(c\right)\right|\le{k}\left|f_{n-1}\left(x\right)-f_{n-1}\left(c\right)\right|\le\cdots\le{k}^n\left|x-c\right|.
$$

又因 $x,c\in\left[a,b\right]$, 故 $\left|x-c\right|\le{b}-a$. 于是

$$
\left|f_n\left(x\right)-c\right|\le{k}^n\left(b-a\right).
$$

$\blacksquare$

## 1.2-10

考虑函数 $y=\left[\frac43\sin^2x\right]$, 其中 $\left[\,\right]$ 表示括号内的量的整数部分. 证明这函数以 $\pi$ 为周期.

### 解答 1.2-10

由周期函数的定义, 只需验证 $y\left(x+\pi\right)=y\left(x\right)$. 因

$$
\sin^2\left(x+\pi\right)=\left(\sin\left(x+\pi\right)\right)^2=\left(-\sin{x}\right)^2=\sin^2x,
$$

故

$$
\frac43\sin^2\left(x+\pi\right)=\frac43\sin^2x,
$$

从而取整数部分后

$$
\left[\frac43\sin^2\left(x+\pi\right)\right]=\left[\frac43\sin^2x\right].
$$

即 $y\left(x+\pi\right)=y\left(x\right)$. 由周期函数的定义, $\pi$ 是 $y$ 的一个周期. $\blacksquare$
