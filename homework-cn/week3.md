# week3

> **命题 1.6 (绝对值的性质)**
> 
> 对于任意的 $x,y\in\mathbb R$, 有: (1) $\left|x\right|\ge0$, 等号当且仅当 $x=0$ 时成立; (2) $\left|-x\right|=\left|x\right|$; (3) $\left|x+y\right|\le\left|x\right|+\left|y\right|$.

> **命题 1.7 (三角不等式)**
> 
> 对于任意实数 $a,b,c$, $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **命题 2.1 (有界函数的充要条件)**
> 
> 函数 $f:X\to Y$ 为有界函数的充分与必要条件是存在一个 $M> 0$, 使得 $\left|f\left(x\right)\right|\le M$ 对一切 $x\in X$ 成立.

> **定理 3.1 (极限四则运算定理)**
> 
> 设 $\left\{a_n\right\}$ 与 $\left\{b_n\right\}$ 都有极限, 分别为 $l_1$ 与 $l_2$, 则 $\lim\left(a_n\pm b_n\right)=l_1\pm l_2$, $\lim\left(a_n\cdot b_n\right)=l_1\cdot l_2$, 且当 $l_2\ne0$ 时 $\lim\frac{a_n}{b_n}=\frac{l_1}{l_2}$.

> **定理 3.2 (实数域完备性)**
> 
> 设 $\left\{a_n\right\}$ 是一个单调递增有上界的实数序列, 则存在 $l\in\mathbb R$, 使得 $\left\{a_n\right\}$ 以 $l$ 为极限.

> **例 3.3 (正数的 $n$ 次方根趋于 $1$)**
> 
> 设 $a$ 是任意的正数, 则 $\lim_{n\to\infty}a^{1/n}=1$.

## 1.2-11

设

$$
f\left(x\right)=\begin{cases}e^x,&x\le0,\\ x,&x> 0;\end{cases}\quad g\left(x\right)=\begin{cases}x,&x\le0,\\ -x^2,&x> 0;\end{cases}
$$

求 $f\left(g\left(x\right)\right)$ 及 $g\left(f\left(x\right)\right)$ 的分段表示式, 并计算 $f\left(g\left(1\right)\right)$ 的值.

### 解答 1.2-11

先求 $f\left(g\left(x\right)\right)$. 由复合函数的定义:

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

## 1.3-1-2

用 $\varepsilon$-$N$ 语言证明: $\lim_{n\to\infty}\frac{2n-5}{3n+100}=\frac23$.

### 解答 1.3-1-2

将通项改写为

$$
\frac{2n-5}{3n+100}=\frac{2-5/n}{3+100/n}.
$$

当 $n\to\infty$ 时, $5/n\to0$, $100/n\to0$ (由序列极限的定义, 对任意 $\varepsilon> 0$, 取 $N> 5/\varepsilon$ 则 $\left|5/n\right|< \varepsilon$). 由**定理 3.1 (极限四则运算定理)**,

$$
\lim_{n\to\infty}\frac{2n-5}{3n+100}=\frac{\lim\left(2-5/n\right)}{\lim\left(3+100/n\right)}=\frac23.
$$

$\blacksquare$

## 1.3-1-4

用 $\varepsilon$-$N$ 语言证明: $\lim_{n\to\infty}\frac{n!}{n^n}=0$.

### 解答 1.3-1-4

对 $n\ge1$,

$$
\frac{n!}{n^n}=\frac{1\cdot2\cdots n}{n\cdot n\cdots n}=\frac1n\cdot\frac2n\cdots\frac{n-1}{n}\cdot1\le\frac1n.
$$

任给 $\varepsilon> 0$, 取 $N=\left[\frac1\varepsilon\right]+1$, 则当 $n> N$ 时

$$
\left|\frac{n!}{n^n}-0\right|\le\frac1n< \varepsilon.
$$

由序列极限的定义, $\lim_{n\to\infty}\frac{n!}{n^n}=0$. $\blacksquare$

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

该式共有 $n$ 项, 每一项满足 $\frac1{\left(n+k\right)^{3/2}}\le\frac1{n^{3/2}}$ ($1\le k\le n$), 故

$$
0\le\frac1{\left(n+1\right)^{3/2}}+\cdots+\frac1{\left(2n\right)^{3/2}}\le\frac{n}{n^{3/2}}=\frac1{\sqrt n}.
$$

任给 $\varepsilon> 0$, 取 $N=\left[1/\varepsilon^2\right]+1$, 则当 $n> N$ 时 $\frac1{\sqrt n}< \varepsilon$. 由序列极限的定义, 原式趋于 $0$. $\blacksquare$

## 1.3-2-2

求极限:

$$
\lim_{n\to\infty}\left(\sqrt\left[n\right]{1}+\sqrt\left[n\right]{2}+\cdots+\sqrt\left[n\right]{100}\right).
$$

### 解答 1.3-2-2

由**例 3.3 (正数的 $n$ 次方根趋于 $1$)**, 对每个 $k=1,2,\dots,100$,

$$
\lim_{n\to\infty}\sqrt\left[n\right]{k}=1.
$$

由**定理 3.1 (极限四则运算定理)** 的加法推广 (有限项),

$$
\lim_{n\to\infty}\left(\sqrt\left[n\right]{1}+\sqrt\left[n\right]{2}+\cdots+\sqrt\left[n\right]{100}\right)=\sum_{k=1}^{100}1=100.
$$

$\blacksquare$
