# week3

> **基础知识: 序列极限的定义**<br>设 $\left\{a_n\right\}$ 是一个给定的序列. 若存在一个实数 $l$, 对于任意给定的正数 $\varepsilon$, 无论它多么小, 都存在一个自然数 $N$, 使得 $\left|a_n-l\right|< \varepsilon$, 只要 $n> N$, 则称 $a_n$ 以 $l$ 为极限, 记作 $\lim_{n\to\infty}a_n=l$.

> **命题 1.6 (绝对值的性质)**<br>对于任意的 $x,y\in\mathbb R$, 有: (1) $\left|x\right|\ge0$, 等号当且仅当 $x=0$ 时成立; (2) $\left|-x\right|=\left|x\right|$; (3) $\left|x+y\right|\le\left|x\right|+\left|y\right|$.

> **命题 1.7 (三角不等式)**<br>对于任意实数 $a,b,c$, 有: (1) $\left|a-b\right|\ge0$, 等号当且仅当 $a=b$; (2) $\left|a-b\right|=\left|b-a\right|$; (3) $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **定理 3.1 (极限四则运算定理)**<br>设 $\left\{a_n\right\}$ 与 $\left\{b_n\right\}$ 都有极限, 分别为 $l_1$ 与 $l_2$, 则 $\lim\left(a_n\pm b_n\right)=l_1\pm l_2$, $\lim\left(a_n\cdot b_n\right)=l_1\cdot l_2$, 且当 $l_2\ne0$ 时 $\lim\frac{a_n}{b_n}=\frac{l_1}{l_2}$.

> **定理 3.2 (实数域完备性)**<br>设 $\left\{a_n\right\}$ 是一个单调递增有上界的实数序列, 则存在 $l\in\mathbb R$, 使得 $\left\{a_n\right\}$ 以 $l$ 为极限. 简言之, 单调递增有上界的序列有极限.

> **例 3.3 (正数的 $n$ 次方根趋于 $1$)**<br>设 $a$ 是任意的正数, 则 $\lim_{n\to\infty}a^{1/n}=1$.

---

## 1.3-1-2

用 $\varepsilon$-$N$ 语言证明: $\lim_{n\to\infty}\frac{2n-5}{3n+100}=\frac23$.

### 解答 1.3-1-2

将通项改写为

$$
\frac{2n-5}{3n+100}=\frac{2-5/n}{3+100/n}.
$$

当 $n\to\infty$ 时, $5/n\to0$, $100/n\to0$ (由**基础知识: 序列极限的定义**, 对任意 $\varepsilon> 0$, 取 $N> 5/\varepsilon$ 则 $\left|5/n\right|< \varepsilon$). 由**定理 3.1 (极限四则运算定理)**,

$$
\lim_{n\to\infty}\frac{2n-5}{3n+100}=\frac{\lim\left(2-5/n\right)}{\lim\left(3+100/n\right)}=\frac23.
$$

$\blacksquare$

---

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

由**基础知识: 序列极限的定义**, $\lim_{n\to\infty}\frac{n!}{n^n}=0$. $\blacksquare$

---

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

---

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

任给 $\varepsilon> 0$, 取 $N=\left[1/\varepsilon^2\right]+1$, 则当 $n> N$ 时 $\frac1{\sqrt n}< \varepsilon$. 由**基础知识: 序列极限的定义**, 原式趋于 $0$. $\blacksquare$

---

## 1.3-2-2

求极限:

$$
\lim_{n\to\infty}\left(\sqrt[n]{1}+\sqrt[n]{2}+\cdots+\sqrt[n]{100}\right).
$$

### 解答 1.3-2-2

由**例 3.3 (正数的 $n$ 次方根趋于 $1$)**, 对每个 $k=1,2,\dots,100$,

$$
\lim_{n\to\infty}\sqrt[n]{k}=1.
$$

由**定理 3.1 (极限四则运算定理)** 的加法推广 (有限项),

$$
\lim_{n\to\infty}\left(\sqrt[n]{1}+\sqrt[n]{2}+\cdots+\sqrt[n]{100}\right)=\sum_{k=1}^{100}1=100.
$$

$\blacksquare$

---

## 1.3-2-4

求极限: $\lim_{n\to\infty}\frac{\frac12+\frac1{2^2}+\cdots+\frac1{2^n}}{\frac13+\frac1{3^2}+\cdots+\frac1{3^n}}$.

### 解答 1.3-2-4

分子为等比级数:

$$
\sum_{k=1}^n\frac1{2^k}=\frac12\cdot\frac{1-\left(1/2\right)^n}{1-1/2}=1-\left(\frac12\right)^n\to1.
$$

分母为等比级数:

$$
\sum_{k=1}^n\frac1{3^k}=\frac13\cdot\frac{1-\left(1/3\right)^n}{1-1/3}=\frac12\left[1-\left(\frac13\right)^n\right]\to\frac12.
$$

由**定理 3.1 (极限四则运算定理)**,

$$
\lim_{n\to\infty}\frac{\text{分子}}{\text{分母}}=\frac1{1/2}=2.
$$

$\blacksquare$

---

## 1.3-2-6

求极限: $\lim_{n\to\infty}\frac{n^3+3n^2-100}{4n^3-n+2}$.

### 解答 1.3-2-6

分子分母同除以 $n^3$:

$$
\frac{n^3+3n^2-100}{4n^3-n+2}=\frac{1+3/n-100/n^3}{4-1/n^2+2/n^3}.
$$

当 $n\to\infty$ 时 $3/n\to0$, $100/n^3\to0$, $1/n^2\to0$, $2/n^3\to0$. 由**定理 3.1 (极限四则运算定理)**,

$$
\lim_{n\to\infty}\frac{n^3+3n^2-100}{4n^3-n+2}=\frac14.
$$

$\blacksquare$

---

## 1.3-2-8

求极限: $\lim_{n\to\infty}\left(1+\frac1n\right)^{-2n}$.

### 解答 1.3-2-8

$$
\left(1+\frac1n\right)^{-2n}=\frac1{\left[\left(1+\frac1n\right)^n\right]^2}.
$$

由**定理 3.2 (实数域完备性)**, 单调递增有上界的序列 $\left\{\left(1+\frac1n\right)^n\right\}$ 有极限, 记为 $e$. 由**定理 3.1 (极限四则运算定理)**,

$$
\lim_{n\to\infty}\left(1+\frac1n\right)^{-2n}=\frac1{e^2}=e^{-2}.
$$

$\blacksquare$

---

## 1.3-2-10

求极限: $\lim_{n\to\infty}\sin\left(\pi\sqrt{n^2+1}\right)$.

### 解答 1.3-2-10

$$
\sin\left(\pi\sqrt{n^2+1}\right)=\sin\left(n\pi+\pi\left(\sqrt{n^2+1}-n\right)\right)=\left(-1\right)^n\sin\left(\pi\left(\sqrt{n^2+1}-n\right)\right).
$$

由 $\left|\sin t\right|\le\left|t\right|$,

$$
\left|\sin\left(\pi\sqrt{n^2+1}\right)\right|=\left|\sin\left(\pi\left(\sqrt{n^2+1}-n\right)\right)\right|\le\pi\left(\sqrt{n^2+1}-n\right)=\frac{\pi}{\sqrt{n^2+1}+n}\to0.
$$

由**命题 1.6 (绝对值的性质)** 及夹逼思想, $\lim_{n\to\infty}\sin\left(\pi\sqrt{n^2+1}\right)=0$. $\blacksquare$

---

## 1.3-3

根据极限的定义证明下列事实:

(1) 若 $\lim_{n\to\infty}a_n=l$, 则对于任意正整数 $k$, 都有

$$
\lim_{n\to\infty}a_{n+k}=l;
$$

(2) 若 $\lim_{n\to\infty}a_n=l$, 则有

$$
\lim_{n\to\infty}a_{2n-1}=l,\quad\lim_{n\to\infty}a_{2n}=l.
$$

### 解答 1.3-3

(1) 任给 $\varepsilon> 0$, 由**基础知识: 序列极限的定义**, 存在自然数 $N$ 使得当 $n> N$ 时 $\left|a_n-l\right|< \varepsilon$. 取 $N'=\max\left(1,N-k+1\right)$, 则当 $n> N'$ 时 $n+k> N$, 从而 $\left|a_{n+k}-l\right|< \varepsilon$. 故 $\lim_{n\to\infty}a_{n+k}=l$.

(2) 任给 $\varepsilon> 0$, 由**基础知识: 序列极限的定义**, 存在自然数 $N$ 使得当 $n> N$ 时 $\left|a_n-l\right|< \varepsilon$. 取 $N'=\left[N/2\right]+1$, 则当 $n> N'$ 时 $2n> N$ 且 $2n-1> N$, 从而 $\left|a_{2n}-l\right|< \varepsilon$ 且 $\left|a_{2n-1}-l\right|< \varepsilon$. 故两子序列均以 $l$ 为极限. $\blacksquare$

---

## 1.3-4

设 $\lim_{n\to\infty}a_n=l$, 证明: $\lim_{n\to\infty}\left|a_n\right|=\left|l\right|$.

### 解答 1.3-4

由**命题 1.7 (三角不等式)**, $\left|\left|a_n\right|-\left|l\right|\right|\le\left|a_n-l\right|$. 任给 $\varepsilon> 0$, 由**基础知识: 序列极限的定义**, 存在 $N$ 使得当 $n> N$ 时 $\left|a_n-l\right|< \varepsilon$. 于是当 $n> N$ 时

$$
\left|\left|a_n\right|-\left|l\right|\right|\le\left|a_n-l\right|< \varepsilon.
$$

由**基础知识: 序列极限的定义**, $\lim_{n\to\infty}\left|a_n\right|=\left|l\right|$. $\blacksquare$

---

## 1.3-5

令 $x_1> \sqrt2$, $x_{n+1}=\frac12\left(x_n+\frac2{x_n}\right)$, $n=1,2,\cdots$. 证明:

(1) $x_n\ge\sqrt2$;

(2) $\left\{x_n\right\}$ 单调递减;

(3) $\lim_{n\to\infty}x_n$ 存在, 且 $\lim_{n\to\infty}x_n=\sqrt2$.

### 解答 1.3-5

(1) 由算术-几何平均不等式,

$$
x_{n+1}=\frac12\left(x_n+\frac2{x_n}\right)\ge\sqrt{x_n\cdot\frac2{x_n}}=\sqrt2.
$$

由归纳法, $x_n\ge\sqrt2$ 对一切 $n$ 成立 ($x_1> \sqrt2$ 为基始).

(2)

$$
x_{n+1}-x_n=\frac12\left(\frac2{x_n}-x_n\right)=\frac{2-x_n^2}{2x_n}.
$$

由 (1) $x_n^2\ge2$, 故 $x_{n+1}-x_n\le0$, 即 $\left\{x_n\right\}$ 单调递减.

(3) $\left\{x_n\right\}$ 单调递减且有下界 $\sqrt2$, 由**定理 3.2 (实数域完备性)** 的递减版本, $\lim_{n\to\infty}x_n$ 存在, 设为 $l$. 在 $x_{n+1}=\frac12\left(x_n+\frac2{x_n}\right)$ 两边取极限, 由**定理 3.1 (极限四则运算定理)** 得

$$
l=\frac12\left(l+\frac2l\right),
$$

即 $l^2=2$. 又 $l\ge\sqrt2> 0$, 故 $l=\sqrt2$. $\blacksquare$
