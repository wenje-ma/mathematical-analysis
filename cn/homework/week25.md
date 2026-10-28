# week25

> **基础知识: 一致连续的定义**<br>设 $y=f\left(x\right)$ 在区间 $X$ 上有定义. 如果对任意 $\varepsilon> 0$, 存在 $\delta> 0$, 使得 $X$ 中任意两点 $x_1,x_2$, 只要 $\left|x_1-x_2\right|< \delta$, 就有 $\left|f\left(x_1\right)-f\left(x_2\right)\right|< \varepsilon$, 则称 $f$ 在 $X$ 上一致连续.

> **定理 1.3 (拉格朗日中值定理)**<br>设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 内可导. 则存在 $c\in\left(a,b\right)$, 使得 $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

> **定理 3.2 (有限覆盖定理)**<br>设 $\mathcal{F}=\left\{I_\alpha\right\}$ 是闭区间 $\left[a,b\right]$ 的任意一个开覆盖, 则存在 $\mathcal{F}$ 中的有限个元素 $I_{\alpha_1},\cdots,I_{\alpha_n}$, 使得 $\left[a,b\right]\subset\bigcup_{k=1}^n I_{\alpha_k}$.

---

## 5.3-2

设 $f\left(x\right)=\frac1x$ ($0< x< 1$). 直接从定义出发, 证明 $f$ 在 $\left(0,1\right)$ 中不一致连续.

### 解答 5.3-2

取 $\varepsilon_0=1$. 对任意 $\delta> 0$, 取 $x_1=\frac\delta2$, $x_2=\frac\delta3$. 则 $\left|x_1-x_2\right|=\frac\delta6< \delta$, 但

$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|=\left|\frac2\delta-\frac3\delta\right|=\frac1\delta.
$$

当 $\delta< 1$ 时, $\frac1\delta> 1=\varepsilon_0$. 故 $f$ 在 $\left(0,1\right)$ 中不一致连续. $\blacksquare$

---

## 5.3-3

设集合 $E=\left\{\frac1n:n=1,2,\cdots\right\}$. 试构造 $E$ 的一个开覆盖, 但不能从中选出有限个元素覆盖住 $E$.

### 解答 5.3-3

对每个 $n$, 取开区间 $I_n=\left(\frac1n-\frac1{4n^2},\frac1n+\frac1{4n^2}\right)$. 显然 $\frac1n\in I_n$, 故 $E\subset\bigcup_{n=1}^\infty I_n$.

但任意有限个 $I_{n_1},\cdots,I_{n_k}$ 只能覆盖有限个点. 设 $N=\max\left\{n_1,\cdots,n_k\right\}$, 则当 $n> N$ 时 $\frac1n\notin\bigcup_{i=1}^k I_{n_i}$. 故不能选出有限子覆盖. $\blacksquare$

---

## 5.3-4

证明: 对集合 $E=\left\{\frac1n\right\}\cup\left\{0\right\}$, 其任意开覆盖都存在有限子覆盖.

### 解答 5.3-4

设 $\mathcal{F}$ 是 $E$ 的任意开覆盖. 因 $0\in E$, 存在 $I_0\in\mathcal{F}$ 使得 $0\in I_0$. 因 $I_0$ 是开集, 存在 $\delta> 0$ 使得 $\left(-\delta,\delta\right)\subset I_0$.

取 $N$ 使得 $\frac1N< \delta$. 则当 $n> N$ 时 $\frac1n\in I_0$. 对每个 $n=1,\cdots,N$, 存在 $I_n\in\mathcal{F}$ 使得 $\frac1n\in I_n$.

于是 $\left\{I_0,I_1,\cdots,I_N\right\}$ 是有限子覆盖. $\blacksquare$

---

## 5.3-5

证明: $y=\sin x$ 在 $\mathbb R$ 上一致连续.

### 解答 5.3-5

对任意 $x_1,x_2\in\mathbb R$, 由**定理 1.3 (拉格朗日中值定理)**,

$$
\left|\sin x_1-\sin x_2\right|=\left|\cos\xi\right|\cdot\left|x_1-x_2\right|\le\left|x_1-x_2\right|.
$$

对任意 $\varepsilon> 0$, 取 $\delta=\varepsilon$. 由**基础知识: 一致连续的定义**, $\sin x$ 在 $\mathbb R$ 上一致连续. $\blacksquare$

---

## 5.3-6

证明: $y=\cos x$ 在 $\mathbb R$ 上一致连续.

### 解答 5.3-6

由**定理 1.3 (拉格朗日中值定理)**, $\left|\cos x_1-\cos x_2\right|\le\left|x_1-x_2\right|$. 取 $\delta=\varepsilon$. 由**基础知识: 一致连续的定义**, $\cos x$ 在 $\mathbb R$ 上一致连续. $\blacksquare$

---

## 5.3-7

证明: $y=\sin 3x+5x+1$ 在 $\mathbb R$ 上一致连续.

### 解答 5.3-7

由三角不等式,

$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|\le\left|\sin3x_1-\sin3x_2\right|+5\left|x_1-x_2\right|\le3\left|x_1-x_2\right|+5\left|x_1-x_2\right|=8\left|x_1-x_2\right|.
$$

取 $\delta=\frac\varepsilon8$. 由**基础知识: 一致连续的定义**, $f$ 在 $\mathbb R$ 上一致连续. $\blacksquare$

---

## 5.3-8

设 $f$ 在 $\left(a,b\right)$ 中满足 $\left|f\left(x_1\right)-f\left(x_2\right)\right|\le H\left|x_1-x_2\right|^\alpha$ ($0< \alpha\le1$). 证明:

(1) 赫尔德连续的函数必一致连续;

(2) 若 $f$ 可导且导数有界, 则 $f$ 满足 $\alpha=1$ 的赫尔德条件.

### 解答 5.3-8

(1) 对任意 $\varepsilon> 0$, 取 $\delta=\left(\frac\varepsilon H\right)^{1/\alpha}$. 则 $\left|f\left(x_1\right)-f\left(x_2\right)\right|\le H\delta^\alpha=\varepsilon$. 由**基础知识: 一致连续的定义**, $f$ 一致连续.

(2) 设 $\left|f'\left(x\right)\right|\le M$. 由**定理 1.3 (拉格朗日中值定理)**,

$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|=\left|f'\left(\xi\right)\right|\cdot\left|x_1-x_2\right|\le M\left|x_1-x_2\right|.
$$

此即 $\alpha=1$ 的赫尔德条件, $H=M$. $\blacksquare$
