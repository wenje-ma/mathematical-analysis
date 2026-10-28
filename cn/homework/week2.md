# week2

> **基础知识: 函数的定义**<br>设 $x$ 与 $y$ 是两个变量, 分别在实数集合 $X$ 与 $Y$ 中取值. 假如有一种规则 $f$ 使得对每一个值 $x\in X$ 都能找到一个唯一确定的 $y\in Y$ 与之相对应, 则称 $f$ 是一个函数, 记作 $f:X\to Y$, 并称 $X$ 为 $f$ 的定义域. $Y$ 中一切可能被取到的函数值集合称作 $f$ 的值域, 记作 $f\left(X\right)$.

> **基础知识: 复合函数的定义**<br>假定有两个函数 $f:X\to Y$ 及 $g:Y^*\to Z$, 并假定 $Y\subset Y^*$. 对于每一个点 $x\in X$, 存在唯一的 $y=f\left(x\right)\in Y$, 再由 $g$ 得到 $z=g\left(y\right)$. 这样确定的从 $X$ 到 $Z$ 的对应 $x\mapsto z$, 其中 $z=g\left(f\left(x\right)\right)$, 称为 $f$ 与 $g$ 的复合函数.

> **基础知识: 周期函数的定义**<br>设 $y=f\left(x\right)$ 在 $\mathbb R$ 上有定义, 且存在一个数 $T\ne 0$ 使得 $f\left(x+T\right)=f\left(x\right)$ 对一切 $x\in\mathbb R$ 成立, 则称 $y=f\left(x\right)$ 是周期函数, 其中 $T$ 称作 $f$ 的一个周期.

> **命题 2.1 (有界函数的充要条件)**<br>函数 $f:X\to Y$ 为有界函数的充分与必要条件是存在一个 $M> 0$, 使得 $\left|f\left(x\right)\right|\le M$ 对一切 $x\in X$ 成立.

---

## 1.2-1

求下列函数的定义域:

(1) $y=\sqrt{x^2-16}$;

(2) $y=\frac{1}{\sqrt{x^2-3x+2}}$;

(3) $y=\ln\frac{x^2-2}{2}$;

(4) $y=\arccos\left(2\sin x\right)$.

### 解答 1.2-1

(1) 要使 $\sqrt{x^2-16}$ 有意义, 须 $x^2-16\ge0$, 即 $\left|x\right|\ge4$. 故定义域为 $\left(-\infty,-4\right]\cup\left[4,+\infty\right)$.

(2) 要使 $\frac{1}{\sqrt{x^2-3x+2}}$ 有意义, 须 $x^2-3x+2> 0$, 即 $\left(x-1\right)\left(x-2\right)> 0$, 亦即 $x< 1$ 或 $x> 2$. 故定义域为 $\left(-\infty,1\right)\cup\left(2,+\infty\right)$.

(3) 要使 $\ln\frac{x^2-2}{2}$ 有意义, 须 $\frac{x^2-2}{2}> 0$, 即 $x^2> 2$, 亦即 $\left|x\right|> \sqrt2$. 故定义域为

$$
\left(-\infty,-\sqrt2\right)\cup\left(\sqrt2,+\infty\right).
$$

(4) 要使 $\arccos\left(2\sin x\right)$ 有意义, 须 $\left|2\sin x\right|\le1$, 即 $\left|\sin x\right|\le\frac12$. 这等价于

$$
x\in\left[k\pi-\frac{\pi}{6},k\pi+\frac{\pi}{6}\right],\quad k\in\mathbb Z.
$$

故定义域为 $\displaystyle\bigcup_{k\in\mathbb Z}\left[k\pi-\frac{\pi}{6},k\pi+\frac{\pi}{6}\right]$. $\blacksquare$

---

## 1.2-2

求下列函数 $f$ 的值域 $f\left(X\right)$, 其中 $X$ 为题中指定的定义域:

(1)

$$
f\left(x\right)=\sqrt{1+x^2},\quad X=\left(0,5\right);
$$

(2)

$$
f\left(x\right)=\sin\frac1x,\quad X=\mathbb R\backslash\left\{0\right\};
$$

(3) $f\left(x\right)=\left\{x\right\}$ ($x$ 的小数部分), $X=\mathbb R$;

(4)

$$
f\left(x\right)=x^3+x+1,\quad X=\mathbb R.
$$

### 解答 1.2-2

(1) 当 $x\in\left(0,5\right)$ 时, $x^2\in\left(0,25\right)$, 故 $1+x^2\in\left(1,26\right)$, 从而 $\sqrt{1+x^2}\in\left(1,\sqrt{26}\right)$. 由**基础知识: 函数的定义**, $f\left(X\right)=\left(1,\sqrt{26}\right)$.

(2) 当 $x$ 遍历 $\mathbb R\backslash\left\{0\right\}$ 时, $\frac1x$ 遍历 $\mathbb R\backslash\left\{0\right\}$. 而 $\sin t$ 在 $t\in\mathbb R$ 上的值域为 $\left[-1,1\right]$, 去掉一个点 $t=0$ (对应 $\sin0=0$) 不影响值域 ($0$ 仍可取到, 如 $t=\pi$). 故 $f\left(X\right)=\left[-1,1\right]$.

(3) 对任意 $x\in\mathbb R$, 其小数部分 $\left\{x\right\}=x-\left[x\right]$ 满足 $0\le\left\{x\right\}< 1$. 反之, 对任意 $y\in\left[0,1\right)$, 取 $x=y$ 即得 $\left\{x\right\}=y$. 故 $f\left(X\right)=\left[0,1\right)$.

(4) $f'\left(x\right)=3x^2+1> 0$, 故 $f$ 在 $\mathbb R$ 上严格单调递增. 又当 $x\to-\infty$ 时 $f\left(x\right)\to-\infty$, 当 $x\to+\infty$ 时 $f\left(x\right)\to+\infty$. 故由介值性, $f\left(X\right)=\mathbb R$. $\blacksquare$

---

## 1.2-6

设 $f:\left[a,b\right]\to\left[a,b\right]$ 是满足下列条件的一个函数:

$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|\le k\left|x_1-x_2\right|,\quad\forall x_1,x_2\in\left[a,b\right],
$$

其中 $k< 1$ 为常数. 又设存在一点 $c\in\left(a,b\right)$ 使 $f\left(c\right)=c$. 证明: $\left|f_n\left(x\right)-c\right|\le k^n\left(b-a\right)$, 其中 $f_n$ 为 $f$ 的 $n$ 重复合函数.

### 解答 1.2-6

因 $f\left(c\right)=c$, 由归纳法易得 $f_n\left(c\right)=c$ ($n=1$ 时即 $f\left(c\right)=c$; 若 $f_n\left(c\right)=c$, 则 $f_{n+1}\left(c\right)=f\left(f_n\left(c\right)\right)=f\left(c\right)=c$).

对任意 $x\in\left[a,b\right]$, 反复应用题设的利普希茨条件:

$$
\left|f_n\left(x\right)-c\right|=\left|f_n\left(x\right)-f_n\left(c\right)\right|\le k\left|f_{n-1}\left(x\right)-f_{n-1}\left(c\right)\right|\le\cdots\le k^n\left|x-c\right|.
$$

又因 $x,c\in\left[a,b\right]$, 故 $\left|x-c\right|\le b-a$. 于是

$$
\left|f_n\left(x\right)-c\right|\le k^n\left(b-a\right).
$$

$\blacksquare$

---

## 1.2-10

考虑函数 $y=\left[\frac43\sin^2 x\right]$, 其中 $\left[\ \right]$ 表示括号内的量的整数部分. 证明这函数以 $\pi$ 为周期.

### 解答 1.2-10

由**基础知识: 周期函数的定义**, 只需验证 $y\left(x+\pi\right)=y\left(x\right)$. 因

$$
\sin^2\left(x+\pi\right)=\left(\sin\left(x+\pi\right)\right)^2=\left(-\sin x\right)^2=\sin^2 x,
$$

故

$$
\frac43\sin^2\left(x+\pi\right)=\frac43\sin^2 x,
$$

从而取整数部分后

$$
\left[\frac43\sin^2\left(x+\pi\right)\right]=\left[\frac43\sin^2 x\right].
$$

即 $y\left(x+\pi\right)=y\left(x\right)$. 由**基础知识: 周期函数的定义**, $\pi$ 是 $y$ 的一个周期. $\blacksquare$

---

## 1.2-11

设

$$
f\left(x\right)=\begin{cases}e^x,&x\le0,\\ x,&x> 0;\end{cases}\quad g\left(x\right)=\begin{cases}x,&x\le0,\\ -x^2,&x> 0;\end{cases}
$$

求 $f\left(g\left(x\right)\right)$ 及 $g\left(f\left(x\right)\right)$ 的分段表示式, 并计算 $f\left(g\left(1\right)\right)$ 的值.

### 解答 1.2-11

先求 $f\left(g\left(x\right)\right)$. 由**基础知识: 复合函数的定义**:

- 当 $x\le0$ 时, $g\left(x\right)=x\le0$, 故 $f\left(g\left(x\right)\right)=f\left(x\right)=e^x$;
- 当 $x> 0$ 时, $g\left(x\right)=-x^2< 0$, 故

$$
f\left(g\left(x\right)\right)=f\left(-x^2\right)=e^{-x^2}.
$$

因此

$$
f\left(g\left(x\right)\right)=\begin{cases}e^x,&x\le0,\\ e^{-x^2},&x> 0.\end{cases}
$$

再求 $g\left(f\left(x\right)\right)$:

- 当 $x\le0$ 时, $f\left(x\right)=e^x> 0$ (因 $x\le0$ 时 $0< e^x\le1$), 故

$$
g\left(f\left(x\right)\right)=g\left(e^x\right)=-\left(e^x\right)^2=-e^{2x};
$$

- 当 $x> 0$ 时, $f\left(x\right)=x> 0$, 故 $g\left(f\left(x\right)\right)=g\left(x\right)=-x^2$.

因此

$$
g\left(f\left(x\right)\right)=\begin{cases}-e^{2x},&x\le0,\\ -x^2,&x> 0.\end{cases}
$$

最后, $g\left(1\right)=-1^2=-1$, 故

$$
f\left(g\left(1\right)\right)=f\left(-1\right)=e^{-1}=\frac1e.
$$

$\blacksquare$

---

## 1.2-14

判断下列函数是否为有界函数:

(1) $y=5\sin e^x+10^{10}$;

(2)

$$
y=\sqrt{x+10}-\sqrt{x}\quad\left(x> 0\right);
$$

(3) $y=\operatorname{ch}x$;

(4)

$$
y=\ln\left(x+\sqrt{x^2+1}\right)\quad\left(x> 0\right).
$$

### 解答 1.2-14

(1) 对任意 $x\in\mathbb R$, $\left|\sin e^x\right|\le1$, 故 $\left|5\sin e^x\right|\le5$, 从而

$$
\left|y\right|=\left|5\sin e^x+10^{10}\right|\le5+10^{10}.
$$

取 $M=5+10^{10}$, 由**命题 2.1 (有界函数的充要条件)**, $y=5\sin e^x+10^{10}$ 是有界函数.

(2) 对 $x> 0$, 有理化得

$$
\sqrt{x+10}-\sqrt{x}=\frac{10}{\sqrt{x+10}+\sqrt{x}}.
$$

因分母 $\sqrt{x+10}+\sqrt{x}> \sqrt{10}$ ($x> 0$), 故 $0< y< \frac{10}{\sqrt{10}}=\sqrt{10}$. 取 $M=\sqrt{10}$, 由**命题 2.1 (有界函数的充要条件)**, $y=\sqrt{x+10}-\sqrt{x}$ 是有界函数.

(3) $y=\operatorname{ch}x=\frac{e^x+e^{-x}}2$. 当 $x\to+\infty$ 时 $e^x\to+\infty$, 故 $y\to+\infty$, 不存在常数 $M> 0$ 使 $\left|y\right|\le M$ 对一切 $x\in\mathbb R$ 成立. 由**命题 2.1 (有界函数的充要条件)**, $y=\operatorname{ch}x$ 不是有界函数.

(4) 当 $x\to+\infty$ 时, $x+\sqrt{x^2+1}\sim2x$, 故

$$
y=\ln\left(x+\sqrt{x^2+1}\right)\sim\ln\left(2x\right)\to+\infty,
$$

不存在常数 $M> 0$ 使 $\left|y\right|\le M$ 对一切 $x> 0$ 成立. 由**命题 2.1 (有界函数的充要条件)**, $y=\ln\left(x+\sqrt{x^2+1}\right)$ 不是有界函数. $\blacksquare$
