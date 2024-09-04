# week1

> **命题 1.3 ($\sqrt2$ 为无理数)**
> 
> $\sqrt2$ 不是有理数.

> **命题 1.6 (绝对值的性质)**
> 
> 对于任意的 $x,y\in\mathbb{R}$, 有: (1) $\left|x\right|\ge0$, 等号当且仅当 $x=0$ 时成立; (2) $\left|-x\right|=\left|x\right|$; (3) $\left|x+y\right|\le\left|x\right|+\left|y\right|$.

> **命题 1.7 (三角不等式)**
> 
> 对于任意实数 $a,b,c$, $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

## 1.1-3

证明 $\sqrt2+\sqrt3$ 是无理数.

### 解答 1.1-3

用反证法. 假设 $\sqrt2+\sqrt3$ 是有理数, 则存在 $r\in\mathbb{Q}$ 使 $\sqrt2+\sqrt3=r$, 于是 $\sqrt3=r-\sqrt2$. 两边平方得

$$
3=r^2-2r\sqrt2+2,
$$

即 $\sqrt2=\frac{r^2-1}{2r}$. 若 $r\ne0$, 则右端 $\frac{r^2-1}{2r}$ 是有理数, 故 $\sqrt2\in\mathbb{Q}$, 这与**命题 1.3 ($\sqrt2$ 为无理数)** 矛盾. 若 $r=0$, 则 $\sqrt2+\sqrt3=0$, 更不可能. 故 $\sqrt2+\sqrt3$ 不是有理数, 即 $\sqrt2+\sqrt3$ 是无理数.

$\blacksquare$

## 1.1-4

证明数集合

$$
E=\left\{m+n\sqrt2:m,n\in\mathbb{Q}\right\}
$$

是一个数域. 又问该数域是否完备?

### 解答 1.1-4

(1) 先证 $E$ 是数域. 对任意 $m_1+n_1\sqrt2$, $m_2+n_2\sqrt2\in{E}$, 有

$$
\left(m_1+n_1\sqrt2\right)\pm\left(m_2+n_2\sqrt2\right)=\left(m_1\pm{m}_2\right)+\left(n_1\pm{n}_2\right)\sqrt2\in{E},
$$

$$
\left(m_1+n_1\sqrt2\right)\left(m_2+n_2\sqrt2\right)=\left(m_1m_2+2n_1n_2\right)+\left(m_1n_2+m_2n_1\right)\sqrt2\in{E}.
$$

故 $E$ 对加, 减, 乘封闭. 若 $m_2+n_2\sqrt2\ne0$, 有理化得

$$
\frac{m_1+n_1\sqrt2}{m_2+n_2\sqrt2}=\frac{m_1m_2-2n_1n_2}{m_2^2-2n_2^2}+\frac{n_1m_2-m_1n_2}{m_2^2-2n_2^2}\sqrt2\in{E},
$$

其中 $m_2^2-2n_2^2\ne0$ (否则 $\sqrt2=m_2/n_2\in\mathbb{Q}$, 与**命题 1.3 ($\sqrt2$ 为无理数)** 矛盾). 又这些运算显然满足交换律, 结合律, 分配律, 故由域的概念, $E$ 是数域.

(2) $E$ 不完备. 事实上, $\sqrt3\notin{E}$: 若 $\sqrt3=m+n\sqrt2$, 平方得 $3=m^2+2n^2+2mn\sqrt2$. 若 $mn\ne0$, 则 $\sqrt2=\frac{3-m^2-2n^2}{2mn}\in\mathbb{Q}$, 矛盾; 若 $n=0$, 则 $\sqrt3=m\in\mathbb{Q}$, 矛盾; 若 $m=0$, 则 $\sqrt3=n\sqrt2$, 平方得 $n^2=\frac32\notin\mathbb{Q}$, 矛盾. 故 $\sqrt3\notin{E}$.

取 $\sqrt3$ 的 $n$ 位不足近似小数 $x_n$, 则 $x_n\in\mathbb{Q}\subset{E}$ (取 $m=x_n$, $n=0$), 且 $\left\{x_n\right\}$ 单调递增, 有上界 (如 $x_n<2$), 但 $\left\{x_n\right\}$ 无限接近 $\sqrt3\notin{E}$. 于是由完备性的概念, $E$ 不是完备的.

$\blacksquare$

## 1.1-6

设

$$
E_1=\left\{x:\left|x-a\right|>r_1\right\},\quad{E}_2=\left\{x:\left|x-b\right|<{}r_2\right\}.
$$

问 $a,b,r_1,r_2$ 满足怎样的条件使 $E_1\cap{E}_2\ne\emptyset$?

### 解答 1.1-6

$E_1$ 即数轴上到 $a$ 的距离大于 $r_1$ 的点集, $E_2$ 即到 $b$ 的距离小于 $r_2$ 的开区间 $\left(b-r_2,b+r_2\right)$.

先求 $E_1\cap{E}_2=\emptyset$ 的条件. 当且仅当 $E_2\subset\left[a-r_1,a+r_1\right]$ 时 $E_2$ 与 $E_1$ 无交, 即

$$
a-r_1\le{b}-r_2,\quad{b}+r_2\le{a}+r_1,
$$

亦即 $r_2\le{r}_1-\left|a-b\right|$. 故 $E_1\cap{E}_2\ne\emptyset$ 当且仅当

$$
r_2>r_1-\left|a-b\right|.
$$

$\blacksquare$

## 1.1-7

解下列不等式:

(1) $\left|x^2-1\right|<8$;

(2) $\left|x-1\right|<\left|x\right|$;

(3) $\left|x-1\right|<\left|x+1\right|$;

(4) $\left|x+2\right|<1$.

### 解答 1.1-7

(1) 由 $\left|x^2-1\right|<8$ 得 $-8<{}x^2-1<8$, 即 $-7<{}x^2<9$. 因 $x^2\ge0$ 恒成立, 故只须 $x^2<9$, 由**命题 1.6 (绝对值的性质)** 得 $\left|x\right|<3$, 即 $-3<{}x<3$.

(2) 由**命题 1.6 (绝对值的性质)**(3) 与两边平方的等价性, $\left|x-1\right|<\left|x\right|$ 当且仅当 $\left(x-1\right)^2<{}x^2$, 即 $x^2-2x+1<{}x^2$, 解得 $x>\frac12$.

(3) 同理, $\left|x-1\right|<\left|x+1\right|$ 当且仅当 $\left(x-1\right)^2<\left(x+1\right)^2$, 即

$$
x^2-2x+1<{}x^2+2x+1,
$$

解得 $x>0$.

(4) 由**命题 1.6 (绝对值的性质)**(1)(3), $\left|x+2\right|<1$ 即 $-1<{}x+2<1$, 解得 $-3<{}x<-1$.

$\blacksquare$

## 1.1-9

证明下列不等式:

(1)

$$
\left|a+2b+c\right|\le\left|a+b\right|+\left|b+c\right|;
$$

(2)

$$
\left|a-b\right|\ge\left|\left|a-c\right|-\left|b-c\right|\right|.
$$

### 解答 1.1-9

(1) 将 $a+2b+c$ 写成 $\left(a+b\right)+\left(b+c\right)$, 由**命题 1.6 (绝对值的性质)**(3) 得

$$
\left|a+2b+c\right|=\left|\left(a+b\right)+\left(b+c\right)\right|\le\left|a+b\right|+\left|b+c\right|.
$$

(2) 由**命题 1.6 (绝对值的性质)**(3) 及**命题 1.7 (三角不等式)**(2), 有

$$
\left|a-c\right|=\left|\left(a-b\right)+\left(b-c\right)\right|\le\left|a-b\right|+\left|b-c\right|,
$$

故 $\left|a-b\right|\ge\left|a-c\right|-\left|b-c\right|$. 同理, 交换 $a,c$ 的位置得 $\left|a-b\right|\ge\left|c-b\right|-\left|a-b\right|$, 即 $\left|a-b\right|\ge\left|b-c\right|-\left|a-c\right|$. 两式合写为

$$
\left|a-b\right|\ge\left|\left|a-c\right|-\left|b-c\right|\right|.
$$

$\blacksquare$

## 1.1-11

判断下列集合 $E$ 是否是有上界, 有下界及有界集合:

(1) $E=\left\{e^n:n\in\mathbb{N}_+\right\}$;

(2) $E=\left\{\frac{n^2+10^{10}}{n^2+1}:n\in\mathbb{N}\right\}$;

(3)

$$
E=\left\{\sqrt{x+1}-\sqrt{x}:x\ge1\right\};
$$

(4)

$$
E=\left\{\left(-1\right)^nn^2-n:n\in\mathbb{N}\right\}.
$$

### 解答 1.1-11

(1) $E=\left\{e,e^2,e^3,\dots\right\}$. 因 $e^n\ge{e}$, 故 $E$ 有下界 (如 $m=e$); 而 $e^n$ 随 $n$ 无限增大, 故 $E$ 无上界. 由有界集的概念, $E$ 有下界, 无上界, 不是有界集合.

(2) 对 $n\in\mathbb{N}$, $\frac{n^2+10^{10}}{n^2+1}=1+\frac{10^{10}-1}{n^2+1}$. 因 $n^2+1\ge1$, 故 $1<\frac{n^2+10^{10}}{n^2+1}\le10^{10}$, 即 $E\subset\left(1,10^{10}\right]$. 故 $E$ 有上界也有下界, 由有界集的概念, $E$ 是有界集合.

(3) 对 $x\ge1$, 有理化得

$$
\sqrt{x+1}-\sqrt{x}=\frac{1}{\sqrt{x+1}+\sqrt{x}}.
$$

因 $x\ge1$ 时 $0<\sqrt{x+1}+\sqrt{x}$, 故

$$
0<\sqrt{x+1}-\sqrt{x}\le\sqrt2-1\,\left(x=1\text{~时取最大值}\right),
$$

故 $E\subset\left(0,\sqrt2-1\right]$, 有上界也有下界, $E$ 是有界集合.

(4) 当 $n$ 为偶数时 $\left(-1\right)^nn^2-n=n^2-n$, 其绝对值为 $n^2-n$; 当 $n$ 为奇数时 $\left(-1\right)^nn^2-n=-n^2-n$, 其绝对值为 $n^2+n$. 无论如何, 绝对值均随 $n$ 无限增大而趋于无穷, 故 $E$ 既无上界也无下界, 不是有界集合.

$\blacksquare$

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

故定义域为 $\displaystyle\bigcup_{k\in\mathbb{Z}}\left[k\pi-\frac{\pi}{6},k\pi+\frac{\pi}{6}\right]$.

$\blacksquare$

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

(4) $f'\left(x\right)=3x^2+1>0$, 故 $f$ 在 $\mathbb{R}$ 上严格单调递增. 又当 $x\to-\infty$ 时 $f\left(x\right)\to-\infty$, 当 $x\to+\infty$ 时 $f\left(x\right)\to+\infty$. 故由介值性, $f\left(X\right)=\mathbb{R}$.

$\blacksquare$

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

即 $y\left(x+\pi\right)=y\left(x\right)$. 由周期函数的定义, $\pi$ 是 $y$ 的一个周期.

$\blacksquare$

## 1.2-11

设

$$
f\left(x\right)=\begin{cases}e^x,&x\le0,\\x,&x>0;\end{cases}\quad{g}\left(x\right)=\begin{cases}x,&x\le0,\\-x^2,&x>0;\end{cases}
$$

求 $f\left(g\left(x\right)\right)$ 及 $g\left(f\left(x\right)\right)$ 的分段表示式, 并计算 $f\left(g\left(1\right)\right)$ 的值.

### 解答 1.2-11

先求 $f\left(g\left(x\right)\right)$. 由复合函数的定义:

- 当 $x\le0$ 时, $g\left(x\right)=x\le0$, 故 $f\left(g\left(x\right)\right)=f\left(x\right)=e^x$;
- 当 $x>0$ 时, $g\left(x\right)=-x^2<0$, 故

$$
f\left(g\left(x\right)\right)=f\left(-x^2\right)=e^{-x^2}.
$$

因此

$$
f\left(g\left(x\right)\right)=\begin{cases}e^x,&x\le0,\\e^{-x^2},&x>0.\end{cases}
$$

再求 $g\left(f\left(x\right)\right)$:

- 当 $x\le0$ 时, $f\left(x\right)=e^x>0$ (因 $x\le0$ 时 $0<{}e^x\le1$), 故

$$
g\left(f\left(x\right)\right)=g\left(e^x\right)=-\left(e^x\right)^2=-e^{2x};
$$

- 当 $x>0$ 时, $f\left(x\right)=x>0$, 故 $g\left(f\left(x\right)\right)=g\left(x\right)=-x^2$.

因此

$$
g\left(f\left(x\right)\right)=\begin{cases}-e^{2x},&x\le0,\\-x^2,&x>0.\end{cases}
$$

最后, $g\left(1\right)=-1^2=-1$, 故

$$
f\left(g\left(1\right)\right)=f\left(-1\right)=e^{-1}=\frac1e.
$$

$\blacksquare$

## 1.2-14

判断下列函数是否为有界函数:

(1) $y=5\sin{e}^x+10^{10}$;

(2)

$$
y=\sqrt{x+10}-\sqrt{x}\quad\left(x>0\right);
$$

(3) $y=\operatorname{ch}x$;

(4)

$$
y=\ln\left(x+\sqrt{x^2+1}\right)\quad\left(x>0\right).
$$

### 解答 1.2-14

(1) 对任意 $x\in\mathbb{R}$, $\left|\sin{e}^x\right|\le1$, 故 $\left|5\sin{e}^x\right|\le5$, 从而

$$
\left|y\right|=\left|5\sin{e}^x+10^{10}\right|\le5+10^{10}.
$$

取 $M=5+10^{10}$, 由**命题 2.1 (有界函数的充要条件)**, $y=5\sin{e}^x+10^{10}$ 是有界函数.

(2) 对 $x>0$, 有理化得

$$
\sqrt{x+10}-\sqrt{x}=\frac{10}{\sqrt{x+10}+\sqrt{x}}.
$$

因分母 $\sqrt{x+10}+\sqrt{x}>\sqrt{10}$ ($x>0$), 故 $0<{}y<\frac{10}{\sqrt{10}}=\sqrt{10}$. 取 $M=\sqrt{10}$, 由**命题 2.1 (有界函数的充要条件)**, $y=\sqrt{x+10}-\sqrt{x}$ 是有界函数.

(3) $y=\operatorname{ch}x=\frac{e^x+e^{-x}}2$. 当 $x\to+\infty$ 时 $e^x\to+\infty$, 故 $y\to+\infty$, 不存在常数 $M>0$ 使 $\left|y\right|\le{M}$ 对一切 $x\in\mathbb{R}$ 成立. 由**命题 2.1 (有界函数的充要条件)**, $y=\operatorname{ch}x$ 不是有界函数.

(4) 当 $x\to+\infty$ 时, $x+\sqrt{x^2+1}\sim2x$, 故

$$
y=\ln\left(x+\sqrt{x^2+1}\right)\sim\ln\left(2x\right)\to+\infty,
$$

不存在常数 $M>0$ 使 $\left|y\right|\le{M}$ 对一切 $x>0$ 成立. 由**命题 2.1 (有界函数的充要条件)**, $y=\ln\left(x+\sqrt{x^2+1}\right)$ 不是有界函数.

$\blacksquare$

## 1.3-1-2

用 $\varepsilon$-$N$ 语言证明: $\lim_{n\to\infty}\frac{2n-5}{3n+100}=\frac23$.

### 解答 1.3-1-2

将通项改写为

$$
\frac{2n-5}{3n+100}=\frac{2-5/n}{3+100/n}.
$$

当 $n\to\infty$ 时, $5/n\to0$, $100/n\to0$ (由序列极限的定义, 对任意 $\varepsilon>0$, 取 $N>5/\varepsilon$ 则 $\left|5/n\right|<\varepsilon$). 由**定理 3.1 (极限四则运算定理)**,

$$
\lim_{n\to\infty}\frac{2n-5}{3n+100}=\frac{\lim\left(2-5/n\right)}{\lim\left(3+100/n\right)}=\frac23.
$$

$\blacksquare$

## 1.3-1-4

用 $\varepsilon$-$N$ 语言证明: $\lim_{n\to\infty}\frac{n!}{n^n}=0$.

### 解答 1.3-1-4

对 $n\ge1$,

$$
\frac{n!}{n^n}=\frac{1\cdot2\cdots{n}}{n\cdot{n}\cdots{n}}=\frac1n\cdot\frac2n\cdots\frac{n-1}{n}\cdot1\le\frac1n.
$$

任给 $\varepsilon>0$, 取 $N=\left[\frac1\varepsilon\right]+1$, 则当 $n>N$ 时

$$
\left|\frac{n!}{n^n}-0\right|\le\frac1n<\varepsilon.
$$

由序列极限的定义, $\lim_{n\to\infty}\frac{n!}{n^n}=0$.

$\blacksquare$

## 1.3-1-6

用 $\varepsilon$-$N$ 语言证明: $\lim_{n\to\infty}\frac{n^2+1}{2n^2-7n}=\frac12$.

### 解答 1.3-1-6

将通项改写为

$$
\frac{n^2+1}{2n^2-7n}=\frac{1+1/n^2}{2-7/n}.
$$

当 $n\to\infty$ 时 $1/n^2\to0$, $7/n\to0$. 由**定理 3.1 (极限四则运算定理)**,

$$
\lim_{n\to\infty}\frac{n^2+1}{2n^2-7n}=\frac{\lim\left(1+1/n^2\right)}{\lim\left(2-7/n\right)}=\frac12.
$$

$\blacksquare$

## 1.3-1-8

用 $\varepsilon$-$N$ 语言证明:

$$
\lim_{n\to\infty}\left(\frac1{\left(n+1\right)^{3/2}}+\cdots+\frac1{\left(2n\right)^{3/2}}\right)=0.
$$

### 解答 1.3-1-8

该式共有 $n$ 项, 每一项满足 $\frac1{\left(n+k\right)^{3/2}}\le\frac1{n^{3/2}}$ ($1\le{k}\le{n}$), 故

$$
0\le\frac1{\left(n+1\right)^{3/2}}+\cdots+\frac1{\left(2n\right)^{3/2}}\le\frac{n}{n^{3/2}}=\frac1{\sqrt{n}}.
$$

任给 $\varepsilon>0$, 取 $N=\left[1/\varepsilon^2\right]+1$, 则当 $n>N$ 时 $\frac1{\sqrt{n}}<\varepsilon$. 由序列极限的定义, 原式趋于 $0$.

$\blacksquare$
