# week26

> **基础知识: 定积分的定义**<br>设 $f$ 定义在 $\left[a,b\right]$ 上. 若存在常数 $I$, 使得对任意 $\varepsilon> 0$, 存在 $\delta> 0$, 只要分割 $T$ 的细度 $\lambda\left(T\right)< \delta$, 不论中间点 $\xi_k$ 如何取, 都有 $\left|\sum f\left(\xi_k\right)\Delta x_k-I\right|< \varepsilon$, 则称 $I$ 为 $f$ 在 $\left[a,b\right]$ 上的定积分, 记作 $\int_a^b f\left(x\right)\,\mathrm dx$.

> **基础知识: 定积分的比较性质**<br>设 $f,g$ 在 $\left[a,b\right]$ 上可积, 且 $f\left(x\right)\le g\left(x\right)$, 则 $\int_a^b f\left(x\right)\,\mathrm dx\le\int_a^b g\left(x\right)\,\mathrm dx$.

> **定理 1.3 (拉格朗日中值定理)**<br>设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 内可导. 则存在 $c\in\left(a,b\right)$, 使得 $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

---

## 6.1-2

写出函数 $y=x$ 与 $y=x^2$ 在 $\left[0,1\right]$ 中的黎曼和 ($n$ 等分, 右端点), 并求 $n\to\infty$ 时的极限.

### 解答 6.1-2

对 $y=x$, 黎曼和为 $\frac1{n^2}\sum_{k=1}^n k=\frac{n+1}{2n}$. 由**基础知识: 定积分的定义**, $\int_0^1 x\,\mathrm dx=\lim_{n\to\infty}\frac{n+1}{2n}=\frac12$.

对 $y=x^2$, 黎曼和为 $\frac1{n^3}\sum_{k=1}^n k^2=\frac{\left(n+1\right)\left(2n+1\right)}{6n^2}$. 故 $\int_0^1 x^2\,\mathrm dx=\frac13$. $\blacksquare$

---

## 6.1-3

设 $x=\varphi\left(y\right)$ 在 $\left[c,d\right]$ 上连续且 $\varphi\left(y\right)> 0$. 试用定积分表示所围面积; 又设 $c\ge0$, $\varphi$ 严格递增, 求 $\int_c^d\varphi\left(y\right)\,\mathrm dy+\int_a^b\psi\left(x\right)\,\mathrm dx$.

### 解答 6.1-3

(1) 面积为 $S=\int_c^d\varphi\left(y\right)\,\mathrm dy$.

(2) 两部分面积之和等于大矩形面积减去小矩形面积:

$$
\int_c^d\varphi\left(y\right)\,\mathrm dy+\int_a^b\psi\left(x\right)\,\mathrm dx=bd-ac.
$$

$\blacksquare$

---

## 6.1-5

证明: $f$ 在 $\left[a,b\right]$ 上可积的充要条件是 $\lim_{\lambda\to0}\sum m_i\Delta x_i$ 与 $\lim_{\lambda\to0}\sum M_i\Delta x_i$ 存在且相等.

### 解答 6.1-5

**必要性**: 设 $f$ 可积, 积分为 $I$. 对任意 $\varepsilon> 0$, 由**基础知识: 定积分的定义**, 当 $\lambda\left(T\right)$ 充分小时, 任意黎曼和都接近 $I$. 取 $\xi_i^*$ 接近 $m_i$, 得 $\left|\sum m_i\Delta x_i-I\right|< 2\varepsilon$. 同理 $\left|\sum M_i\Delta x_i-I\right|< 2\varepsilon$.

**充分性**: 设两极限均为 $I$. 对任意中间点 $\xi_i$, $m_i\le f\left(\xi_i\right)\le M_i$. 由夹逼定理, $\sum f\left(\xi_i\right)\Delta x_i\to I$. 由**基础知识: 定积分的定义**, $f$ 可积. $\blacksquare$

---

## 6.1-6

证明下列不等式:

(1) $\frac\pi2\le\int_0^{\pi/2}\left(1+\sin x\right)\,\mathrm dx\le\pi$;

(2) $\sqrt2\le\int_0^1\sqrt{2+x-x^2}\,\mathrm dx\le\frac32$.

### 解答 6.1-6

(1) 在 $\left[0,\pi/2\right]$ 上, $1\le1+\sin x\le2$. 由**基础知识: 定积分的比较性质**, $\frac\pi2\le\int_0^{\pi/2}\left(1+\sin x\right)\,\mathrm dx\le\pi$.

(2) 在 $\left[0,1\right]$ 上, $2\le2+x-x^2\le\frac94$. 开方得 $\sqrt2\le\sqrt{2+x-x^2}\le\frac32$. 由**基础知识: 定积分的比较性质**, 得证. $\blacksquare$

---

## 6.1-8

设 $F$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 内可导, $F'\left(x\right)=f\left(x\right)$, 且 $f$ 可积. 证明 $\int_a^b f\left(x\right)\,\mathrm dx=F\left(b\right)-F\left(a\right)$.

### 解答 6.1-8

对 $\left[a,b\right]$ 任作分割 $T$. 则

$$
F\left(b\right)-F\left(a\right)=\sum_{k=1}^n\left[F\left(x_k\right)-F\left(x_{k-1}\right)\right].
$$

在每个小区间上, 由**定理 1.3 (拉格朗日中值定理)**, 存在 $\xi_k\in\left(x_{k-1},x_k\right)$ 使得

$$
F\left(x_k\right)-F\left(x_{k-1}\right)=f\left(\xi_k\right)\Delta x_k.
$$

于是 $F\left(b\right)-F\left(a\right)=\sum f\left(\xi_k\right)\Delta x_k$. 令 $\lambda\left(T\right)\to0$, 由**基础知识: 定积分的定义**, 得 $\int_a^b f\left(x\right)\,\mathrm dx=F\left(b\right)-F\left(a\right)$. $\blacksquare$
