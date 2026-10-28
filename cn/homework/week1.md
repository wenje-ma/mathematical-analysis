# week1

> **基础知识: 域的概念**<br>粗略地说, 一个数集对加, 减, 乘, 除 (除数不为 $0$) 是封闭的, 并满足交换律, 结合律及分配律, 便称该数集为域.

> **基础知识: 完备性的概念**<br>如果一个有序数域满足下列要求, 则称之为完备的 (或连续的): 对于任何一个单调递增的有界序列 $\left\{x_n\right\}$, 在该数域中都存在一个数 $a$, 使得 $x_n$ 可以无限接近 $a$.

> **基础知识: 有界集的概念**<br>设 $E\subset\mathbb R$. 若存在 $M$ 使 $E$ 中一切点 $x$ 都有 $x\le M$, 则称 $E$ 有上界; 若存在 $m$ 使 $E$ 中一切点 $x$ 都有 $x\ge m$, 则称 $E$ 有下界; 既有上界又有下界的集合称作有界集合.

> **命题 1.3 ($\sqrt2$ 为无理数)**<br>$\sqrt2$ 不是有理数.

> **命题 1.6 (绝对值的性质)**<br>对于任意的 $x,y\in\mathbb R$, 有: (1) $\left|x\right|\ge0$, 等号当且仅当 $x=0$ 时成立; (2) $\left|-x\right|=\left|x\right|$; (3) $\left|x+y\right|\le\left|x\right|+\left|y\right|$.

> **命题 1.7 (三角不等式)**<br>对于任意实数 $a,b,c$, 有: (1) $\left|a-b\right|\ge0$, 等号当且仅当 $a=b$ 时成立; (2) $\left|a-b\right|=\left|b-a\right|$; (3) $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

---

## 1.1-3

证明 $\sqrt2+\sqrt3$ 是无理数.

### 解答 1.1-3

用反证法. 假设 $\sqrt2+\sqrt3$ 是有理数, 则存在 $r\in\mathbb Q$ 使 $\sqrt2+\sqrt3=r$, 于是 $\sqrt3=r-\sqrt2$. 两边平方得

$$
3=r^2-2r\sqrt2+2,
$$

即 $\sqrt2=\frac{r^2-1}{2r}$. 若 $r\ne0$, 则右端 $\frac{r^2-1}{2r}$ 是有理数, 故 $\sqrt2\in\mathbb Q$, 这与**命题 1.3 ($\sqrt2$ 为无理数)** 矛盾. 若 $r=0$, 则 $\sqrt2+\sqrt3=0$, 更不可能. 故 $\sqrt2+\sqrt3$ 不是有理数, 即 $\sqrt2+\sqrt3$ 是无理数. $\blacksquare$

---

## 1.1-4

证明数集合

$$
E=\left\{m+n\sqrt2:m,n\in\mathbb Q\right\}
$$

是一个数域. 又问该数域是否完备?

### 解答 1.1-4

(1) 先证 $E$ 是数域. 对任意 $m_1+n_1\sqrt2$, $m_2+n_2\sqrt2\in E$, 有

$$
\left(m_1+n_1\sqrt2\right)\pm\left(m_2+n_2\sqrt2\right)=\left(m_1\pm m_2\right)+\left(n_1\pm n_2\right)\sqrt2\in E,
$$

$$
\left(m_1+n_1\sqrt2\right)\left(m_2+n_2\sqrt2\right)=\left(m_1m_2+2n_1n_2\right)+\left(m_1n_2+m_2n_1\right)\sqrt2\in E.
$$

故 $E$ 对加, 减, 乘封闭. 若 $m_2+n_2\sqrt2\ne0$, 有理化得

$$
\frac{m_1+n_1\sqrt2}{m_2+n_2\sqrt2}=\frac{m_1m_2-2n_1n_2}{m_2^2-2n_2^2}+\frac{n_1m_2-m_1n_2}{m_2^2-2n_2^2}\sqrt2\in E,
$$

其中 $m_2^2-2n_2^2\ne0$ (否则 $\sqrt2=m_2/n_2\in\mathbb Q$, 与**命题 1.3 ($\sqrt2$ 为无理数)** 矛盾). 又这些运算显然满足交换律, 结合律, 分配律, 故由**基础知识: 域的概念**, $E$ 是数域.

(2) $E$ 不完备. 事实上, $\sqrt3\notin E$: 若 $\sqrt3=m+n\sqrt2$, 平方得 $3=m^2+2n^2+2mn\sqrt2$. 若 $mn\ne0$, 则 $\sqrt2=\frac{3-m^2-2n^2}{2mn}\in\mathbb Q$, 矛盾; 若 $n=0$, 则 $\sqrt3=m\in\mathbb Q$, 矛盾; 若 $m=0$, 则 $\sqrt3=n\sqrt2$, 平方得 $n^2=\frac32\notin\mathbb Q$, 矛盾. 故 $\sqrt3\notin E$.

取 $\sqrt3$ 的 $n$ 位不足近似小数 $x_n$, 则 $x_n\in\mathbb Q\subset E$ (取 $m=x_n$, $n=0$), 且 $\left\{x_n\right\}$ 单调递增, 有上界 (如 $x_n< 2$), 但 $\left\{x_n\right\}$ 无限接近 $\sqrt3\notin E$. 于是由**基础知识: 完备性的概念**, $E$ 不是完备的. $\blacksquare$

---

## 1.1-6

设

$$
E_1=\left\{x:\left|x-a\right|> r_1\right\},\quad E_2=\left\{x:\left|x-b\right|< r_2\right\}.
$$

问 $a,b,r_1,r_2$ 满足怎样的条件使 $E_1\cap E_2\ne\varnothing$?

### 解答 1.1-6

$E_1$ 即数轴上到 $a$ 的距离大于 $r_1$ 的点集, $E_2$ 即到 $b$ 的距离小于 $r_2$ 的开区间 $\left(b-r_2,b+r_2\right)$.

先求 $E_1\cap E_2=\varnothing$ 的条件. 当且仅当 $E_2\subset\left[a-r_1,a+r_1\right]$ 时 $E_2$ 与 $E_1$ 无交, 即

$$
a-r_1\le b-r_2,\quad b+r_2\le a+r_1,
$$

亦即 $r_2\le r_1-\left|a-b\right|$. 故 $E_1\cap E_2\ne\varnothing$ 当且仅当

$$
r_2> r_1-\left|a-b\right|.
$$

$\blacksquare$

---

## 1.1-7

解下列不等式:

(1) $\left|x^2-1\right|< 8$;

(2) $\left|x-1\right|< \left|x\right|$;

(3) $\left|x-1\right|< \left|x+1\right|$;

(4) $\left|x+2\right|< 1$.

### 解答 1.1-7

(1) 由 $\left|x^2-1\right|< 8$ 得 $-8< x^2-1< 8$, 即 $-7< x^2< 9$. 因 $x^2\ge0$ 恒成立, 故只须 $x^2< 9$, 由**命题 1.6 (绝对值的性质)** 得 $\left|x\right|< 3$, 即 $-3< x< 3$.

(2) 由**命题 1.6 (绝对值的性质)**(3) 与两边平方的等价性, $\left|x-1\right|< \left|x\right|$ 当且仅当 $\left(x-1\right)^2< x^2$, 即 $x^2-2x+1< x^2$, 解得 $x> \frac12$.

(3) 同理, $\left|x-1\right|< \left|x+1\right|$ 当且仅当 $\left(x-1\right)^2< \left(x+1\right)^2$, 即

$$
x^2-2x+1< x^2+2x+1,
$$

解得 $x> 0$.

(4) 由**命题 1.6 (绝对值的性质)**(1)(3), $\left|x+2\right|< 1$ 即 $-1< x+2< 1$, 解得 $-3< x< -1$. $\blacksquare$

---

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

---

## 1.1-11

判断下列集合 $E$ 是否是有上界, 有下界及有界集合:

(1) $E=\left\{e^n:n\in\mathbb N_+\right\}$;

(2) $E=\left\{\frac{n^2+10^{10}}{n^2+1}:n\in\mathbb N\right\}$;

(3)

$$
E=\left\{\sqrt{x+1}-\sqrt{x}:x\ge1\right\};
$$

(4)

$$
E=\left\{\left(-1\right)^nn^2-n:n\in\mathbb N\right\}.
$$

### 解答 1.1-11

(1) $E=\left\{e,e^2,e^3,\dots\right\}$. 因 $e^n\ge e$, 故 $E$ 有下界 (如 $m=e$); 而 $e^n$ 随 $n$ 无限增大, 故 $E$ 无上界. 由**基础知识: 有界集的概念**, $E$ 有下界, 无上界, 不是有界集合.

(2) 对 $n\in\mathbb N$, $\frac{n^2+10^{10}}{n^2+1}=1+\frac{10^{10}-1}{n^2+1}$. 因 $n^2+1\ge1$, 故 $1< \frac{n^2+10^{10}}{n^2+1}\le10^{10}$, 即 $E\subset\left(1,10^{10}\right]$. 故 $E$ 有上界也有下界, 由**基础知识: 有界集的概念**, $E$ 是有界集合.

(3) 对 $x\ge1$, 有理化得

$$
\sqrt{x+1}-\sqrt{x}=\frac{1}{\sqrt{x+1}+\sqrt{x}}.
$$

因 $x\ge1$ 时 $0< \sqrt{x+1}+\sqrt{x}$, 故

$$
0< \sqrt{x+1}-\sqrt{x}\le\sqrt2-1\ \left(x=1\text{ 时取最大值}\right),
$$

故 $E\subset\left(0,\sqrt2-1\right]$, 有上界也有下界, $E$ 是有界集合.

(4) 当 $n$ 为偶数时 $\left(-1\right)^nn^2-n=n^2-n$, 其绝对值为 $n^2-n$; 当 $n$ 为奇数时 $\left(-1\right)^nn^2-n=-n^2-n$, 其绝对值为 $n^2+n$. 无论如何, 绝对值均随 $n$ 无限增大而趋于无穷, 故 $E$ 既无上界也无下界, 不是有界集合. $\blacksquare$
