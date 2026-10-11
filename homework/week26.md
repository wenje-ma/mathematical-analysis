# 作业 26

> **定义**（定积分）设 $f\left(x\right)$ 定义在区间 $\left[a,b\right]$ 上. 对 $\left[a,b\right]$ 作分割 $T:a=x_0<x_1<\cdots<x_n=b$, 记 $\Delta x_k=x_k-x_{k-1}$, $\lambda\left(T\right)=\max_{1\le k\le n}\Delta x_k$. 若存在常数 $I$, 使得对任意 $\varepsilon>0$, 存在 $\delta>0$, 只要 $\lambda\left(T\right)<\delta$, 不论分割 $T$ 如何取、中间点 $\xi_k\in\left[x_{k-1},x_k\right]$ 如何取, 都有 $\left\lvert\sum_{k=1}^n f\left(\xi_k\right)\Delta x_k-I\right\rvert<\varepsilon$, 则称 $I$ 为 $f\left(x\right)$ 在 $\left[a,b\right]$ 上的定积分, 记作 $\int_a^b f\left(x\right)\,\mathrm{d}x$.

> **性质**（定积分的比较性质）设 $f,g$ 在 $\left[a,b\right]$ 上可积, 且 $f\left(x\right)\le g\left(x\right)$ ($\forall x\in\left[a,b\right]$), 则 $\int_a^b f\left(x\right)\,\mathrm{d}x\le\int_a^b g\left(x\right)\,\mathrm{d}x$. 特别地, $f\left(x\right)\ge0$ 时 $\int_a^b f\left(x\right)\,\mathrm{d}x\ge0$.

### 习题一

（习题 6.1-2）写出函数 $y=x$ 与 $y=x^2$ 在区间 $\left[0,1\right]$ 中的黎曼和, 其中分割为 $n$ 等分, 中间点 $\xi_k$ 取成小区间之右端点. 求出当 $n\to\infty$ 时该黎曼和之极限. （提示: 利用公式 $1^2+2^2+\cdots+n^2=\dfrac{n\left(n+1\right)\left(2n+1\right)}{6}$.)

### 解答 习题一

对 $\left[0,1\right]$ 作 $n$ 等分, 分点 $x_k=k/n$ ($k=0,1,\dots,n$), 则 $\Delta x_k=1/n$, $\lambda\left(T\right)=1/n$, 取中间点 $\xi_k=x_k=k/n$.

对于 $y=x$, 黎曼和为

$$
\sum_{k=1}^n \xi_k\Delta x_k=\sum_{k=1}^n \frac{k}{n}\cdot\frac1n=\frac1{n^2}\sum_{k=1}^n k=\frac1{n^2}\cdot\frac{n\left(n+1\right)}2=\frac{n+1}{2n}.
$$

令 $n\to\infty$, 由**定义**（定积分）得 $\int_0^1 x\,\mathrm{d}x=\lim_{n\to\infty}\dfrac{n+1}{2n}=\dfrac12$.

对于 $y=x^2$, 黎曼和为

$$
\sum_{k=1}^n \xi_k^2\Delta x_k=\sum_{k=1}^n \left(\frac{k}{n}\right)^2\frac1n=\frac1{n^3}\sum_{k=1}^n k^2=\frac1{n^3}\cdot\frac{n\left(n+1\right)\left(2n+1\right)}6=\frac{\left(n+1\right)\left(2n+1\right)}{6n^2}.
$$

令 $n\to\infty$, 由**定义**（定积分）得 $\int_0^1 x^2\,\mathrm{d}x=\lim_{n\to\infty}\dfrac{\left(n+1\right)\left(2n+1\right)}{6n^2}=\dfrac13$. $\blacksquare$

### 习题二

（习题 6.1-3）设函数 $x=\varphi\left(y\right)$ 在 $\left[c,d\right]$ 上连续, 且 $\varphi\left(y\right)>0$. 试用定积分表示由曲线 $x=\varphi\left(y\right)$, $y=c$, $y=d$ 及 $y$ 轴所围图形的面积; 又设 $c\ge0$, 函数 $x=\varphi\left(y\right)$ 在 $\left[c,d\right]$ 上严格递增. 试求积分和 $\int_c^d \varphi\left(y\right)\,\mathrm{d}y+\int_a^b \psi\left(x\right)\,\mathrm{d}x$, 其中 $y=\psi\left(x\right)$ 是 $x=\varphi\left(y\right)$ 的反函数, $a=\varphi\left(c\right)$, $b=\varphi\left(d\right)$.

### 解答 习题二

（1）曲线 $x=\varphi\left(y\right)$, $y=c$, $y=d$ 与 $y$ 轴所围图形, 可沿 $y$ 轴方向分割为水平窄条: 在高度 $y$ 处窄条宽为 $\varphi\left(y\right)$, 高为 $\mathrm{d}y$, 面积微元为 $\varphi\left(y\right)\,\mathrm{d}y$. 由**定义**（定积分）, 所围面积为 $\displaystyle S=\int_c^d \varphi\left(y\right)\,\mathrm{d}y$.

（2）因 $x=\varphi\left(y\right)$ 在 $\left[c,d\right]$ 上严格递增且 $c\ge0$, 故其反函数 $y=\psi\left(x\right)$ 在 $\left[a,b\right]$ 上亦严格递增, 其中 $a=\varphi\left(c\right)\ge0$, $b=\varphi\left(d\right)$.

考虑矩形 $\left[0,b\right]\times\left[0,d\right]$ 与 $\left[0,a\right]\times\left[0,c\right]$. 区域 $\left[0,b\right]\times\left[0,d\right]\setminus\left[0,a\right]\times\left[0,c\right]$ 被曲线 $x=\varphi\left(y\right)$ (即 $y=\psi\left(x\right)$) 分为两部分: 曲线左侧介于 $y=c$ 与 $y=d$ 之间的部分, 面积为 $\int_c^d \varphi\left(y\right)\,\mathrm{d}y$; 曲线下方介于 $x=a$ 与 $x=b$ 之间的部分, 面积为 $\int_a^b \psi\left(x\right)\,\mathrm{d}x$. 两部分面积之和等于大矩形面积减去小矩形面积, 即

$$
\int_c^d \varphi\left(y\right)\,\mathrm{d}y+\int_a^b \psi\left(x\right)\,\mathrm{d}x=bd-ac.
$$

$\blacksquare$

### 习题三

（习题 6.1-5）设函数 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上有定义, 并且假定 $y=f\left(x\right)$ 在任何闭子区间上有最大值与最小值. 对于任意一个分割 $T:a=x_0<x_1<\cdots<x_n=b$, 记 $m_i$ 为 $y=f\left(x\right)$ 在 $\left[x_{i-1},x_i\right]$ 中的最小值, $M_i$ 为最大值. 证明: $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上可积的充要条件是极限 $\lim_{\lambda\left(T\right)\to0}\sum_{i=1}^n m_i\Delta x_i$ 与 $\lim_{\lambda\left(T\right)\to0}\sum_{i=1}^n M_i\Delta x_i$ 存在并且相等.

### 解答 习题三

**必要性** 设 $f$ 在 $\left[a,b\right]$ 上可积, 积分为 $I$. 对任意 $\varepsilon>0$, 由**定义**（定积分）, 存在 $\delta>0$, 使当 $\lambda\left(T\right)<\delta$ 时, 对任意中间点 $\xi_i\in\left[x_{i-1},x_i\right]$ 都有

$$
\left\lvert\sum_{i=1}^n f\left(\xi_i\right)\Delta x_i-I\right\rvert<\varepsilon.
$$

对每个小区间 $\left[x_{i-1},x_i\right]$, 因 $m_i$ 是 $f$ 在其上的最小值, 故存在 $\xi_i^*\in\left[x_{i-1},x_i\right]$ 使 $f\left(\xi_i^*\right)<m_i+\dfrac{\varepsilon}{b-a}$. 于是

$$
\sum_{i=1}^n m_i\Delta x_i\le\sum_{i=1}^n f\left(\xi_i^*\right)\Delta x_i<\sum_{i=1}^n m_i\Delta x_i+\varepsilon.
$$

结合 $\left\lvert\sum f\left(\xi_i^*\right)\Delta x_i-I\right\rvert<\varepsilon$ 得 $\left\lvert\sum m_i\Delta x_i-I\right\rvert<2\varepsilon$. 同理, 取 $\xi_i^{**}\in\left[x_{i-1},x_i\right]$ 使 $f\left(\xi_i^{**}\right)>M_i-\dfrac{\varepsilon}{b-a}$, 得 $\left\lvert\sum M_i\Delta x_i-I\right\rvert<2\varepsilon$. 故两极限均存在且等于 $I$.

**充分性** 设 $\lim_{\lambda\left(T\right)\to0}\sum m_i\Delta x_i=\lim_{\lambda\left(T\right)\to0}\sum M_i\Delta x_i=I$. 对任意中间点 $\xi_i\in\left[x_{i-1},x_i\right]$, 由 $m_i\le f\left(\xi_i\right)\le M_i$ 得

$$
\sum_{i=1}^n m_i\Delta x_i\le\sum_{i=1}^n f\left(\xi_i\right)\Delta x_i\le\sum_{i=1}^n M_i\Delta x_i.
$$

令 $\lambda\left(T\right)\to0$, 由夹逼定理, $\sum f\left(\xi_i\right)\Delta x_i\to I$. 由**定义**（定积分）, $f$ 在 $\left[a,b\right]$ 上可积. $\blacksquare$

### 习题四

（习题 6.1-6）证明下列不等式（假定其中函数均可积）:
(1) $\dfrac{\pi}{2}\le\int_0^{\pi/2}\left(1+\sin x\right)\,\mathrm{d}x\le\pi$;

(2) $\sqrt2\le\int_0^1\sqrt{2+x-x^2}\,\mathrm{d}x\le\dfrac32$.

### 解答 习题四

（1）在 $\left[0,\pi/2\right]$ 上, $0\le\sin x\le1$, 故 $1\le1+\sin x\le2$. 由**性质**（定积分的比较性质）,

$$
1\cdot\frac{\pi}{2}\le\int_0^{\pi/2}\left(1+\sin x\right)\,\mathrm{d}x\le2\cdot\frac{\pi}{2}=\pi.
$$

（2）在 $\left[0,1\right]$ 上, $2+x-x^2=2+x\left(1-x\right)$. 因 $0\le x\left(1-x\right)\le\dfrac14$ (在 $x=\dfrac12$ 取最大值), 故

$$
2\le2+x-x^2\le\frac94.
$$

开方得 $\sqrt2\le\sqrt{2+x-x^2}\le\dfrac32$. 由**性质**（定积分的比较性质）,

$$
\sqrt2\cdot1\le\int_0^1\sqrt{2+x-x^2}\,\mathrm{d}x\le\frac32\cdot1.
$$

$\blacksquare$

### 习题五

（习题 6.1-8）设 $F\left(x\right)$ 在 $\left[a,b\right]$ 中连续, 在 $\left(a,b\right)$ 中可导, 且 $F'\left(x\right)=f\left(x\right)$. 假定 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 中可积, 则 $\int_a^b f\left(x\right)\,\mathrm{d}x=F\left(b\right)-F\left(a\right)$. （提示: 对 $\left[a,b\right]$ 中任意一个分割 $T$, 有 $F\left(b\right)-F\left(a\right)=\sum_{k=1}^n\left[F\left(x_k\right)-F\left(x_{k-1}\right)\right]$, 对 $F\left(x_k\right)-F\left(x_{k-1}\right)$ 使用微分中值定理.）

### 解答 习题五

对 $\left[a,b\right]$ 任作分割 $T:a=x_0<x_1<\cdots<x_n=b$. 则

$$
F\left(b\right)-F\left(a\right)=\sum_{k=1}^n\bigl[F\left(x_k\right)-F\left(x_{k-1}\right)\bigr].
$$

在每个小区间 $\left[x_{k-1},x_k\right]$ 上, $F$ 满足拉格朗日中值定理条件 (连续、可导), 故存在 $\xi_k\in\left(x_{k-1},x_k\right)$ 使

$$
F\left(x_k\right)-F\left(x_{k-1}\right)=F'\left(\xi_k\right)\left(x_k-x_{k-1}\right)=f\left(\xi_k\right)\Delta x_k.
$$

于是 $F\left(b\right)-F\left(a\right)=\sum_{k=1}^n f\left(\xi_k\right)\Delta x_k$, 这是 $f$ 的一个黎曼和. 因 $f$ 在 $\left[a,b\right]$ 上可积, 令 $\lambda\left(T\right)\to0$, 由**定义**（定积分）, 该黎曼和趋于 $\int_a^b f\left(x\right)\,\mathrm{d}x$. 故

$$
\int_a^b f\left(x\right)\,\mathrm{d}x=F\left(b\right)-F\left(a\right).
$$

$\blacksquare$
