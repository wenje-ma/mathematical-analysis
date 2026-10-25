# 作业 25

> **定义**（一致连续）设 $y=f\left(x\right)$ 在一个区间 $X$ 上有定义. 如果对任意给定的 $\varepsilon> 0$, 存在一个 $\delta> 0$, 使得 $X$ 中的任意两点 $x_1$ 与 $x_2$, 都有 $\left|f\left(x_1\right)-f\left(x_2\right)\right|< \varepsilon$ (只要 $\left|x_1-x_2\right|< \delta$), 则称 $y=f\left(x\right)$ 在 $X$ 中一致连续.

> **定理 3.2**（有限覆盖定理）设 $\mathcal{F}=\left\{I_\alpha:\alpha\in A\right\}$ 是闭区间 $\left[a,b\right]$ 的任意一个开覆盖, 则存在 $\mathcal{F}$ 中的有限个元素 $I_{\alpha_1},\cdots,I_{\alpha_n}$, 使得 $\left[a,b\right]\subset\bigcup\limits_{k=1}^n I_{\alpha_k}$.

### 习题一

（习题 5.3-2）设 $f\left(x\right)=\frac1x$($0< x< 1$). 直接从定义出发, 证明 $f\left(x\right)$ 在 $\left(0,1\right)$ 中不一致连续.

### 解答 习题一

要证明 $f\left(x\right)=\frac1x$ 在 $\left(0,1\right)$ 中不一致连续, 即存在 $\varepsilon_0> 0$, 对于任意 $\delta> 0$, 都存在 $x_1,x_2\in\left(0,1\right)$, 使得
$$
\left|x_1-x_2\right|< \delta,\text{但}\;\left|f\left(x_1\right)-f\left(x_2\right)\right|\ge\varepsilon_0.
$$

取 $\varepsilon_0=1$. 对任意 $\delta> 0$, 取 $x_1=\frac{\delta}{2}$, $x_2=\frac{\delta}{3}$. 则
$$
\left|x_1-x_2\right|=\frac{\delta}{6}< \delta,
$$

但
$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|=\left|\frac{2}{\delta}-\frac{3}{\delta}\right|=\frac1\delta\to\infty\left(\delta\to0\right).
$$

当 $\delta< 1$ 时, $\frac1\delta> 1=\varepsilon_0$. 故 $f\left(x\right)=\frac1x$ 在 $\left(0,1\right)$ 中不一致连续. $\blacksquare$

### 习题二

（习题 5.3-3）设集合 $E=\left\{\frac1n:n=1,2,\cdots\right\}$. 试构造集合 $E$ 的一个开覆盖, 但不能从中选出有限个元素覆盖住 $E$.

### 解答 习题二

对每个 $n$, 取开区间 $I_n=\left(\frac1n-\frac{1}{4n^2},\frac1n+\frac{1}{4n^2}\right)$. 显然 $\frac1n\in I_n$, 故 $E\subset\bigcup\limits_{n=1}^\infty I_n$, 即 $\left\{I_n\right\}$ 是 $E$ 的一个开覆盖.

但任意有限个 $I_{n_1},\cdots,I_{n_k}$ 只能覆盖有限个点 $\frac1{n_1},\cdots,\frac1{n_k}$. 设 $N=\max\left\{n_1,\cdots,n_k\right\}$, 则当 $n> N$ 时 $\frac1n\in E$ 但 $\frac1n\notin\bigcup\limits_{i=1}^k I_{n_i}$(因 $I_{n_i}$ 的中心为 $\frac1{n_i}$, 半径为 $\frac{1}{4n_i^2}$, 不包含 $\frac1n$).

故不能从中选出有限个元素覆盖住 $E$. $\blacksquare$

### 习题三

（习题 5.3-4）证明: 对集合

$$
E=\left\{\frac1n:n=1,2,\cdots\right\}\cup\left\{0\right\},
$$

其任意开覆盖都存在有限子覆盖.

### 解答 习题三

本题是**定理 3.2**（有限覆盖定理）在紧致点集 $E=\left\{1/n\right\}\cup\left\{0\right\}$ 上的具体应用, 其证明思路与该定理一致: 先覆盖聚点 $0$, 再覆盖其余有限个孤立点.

设 $\mathcal{F}$ 是 $E$ 的任意一个开覆盖. 因 $0\in E$, 故存在 $I_0\in\mathcal{F}$ 使得 $0\in I_0$. 因 $I_0$ 是开区间, 故存在 $\delta> 0$ 使得 $\left(-\delta,\delta\right)\subset I_0$.

取 $N$ 使得 $\frac1N< \delta$. 则当 $n> N$ 时, $0< \frac1n< \delta$, 即 $\frac1n\in\left(-\delta,\delta\right)\subset I_0$. 故 $I_0$ 覆盖了 $E$ 中除 $\frac11,\frac12,\cdots,\frac1N$ 以外的所有点.

对每个 $n=1,2,\cdots,N$, 因 $\frac1n\in E$, 存在 $I_n\in\mathcal{F}$ 使得 $\frac1n\in I_n$.

于是 $\left\{I_0,I_1,\cdots,I_N\right\}$ 是 $\mathcal{F}$ 的有限子集, 且覆盖了 $E$. $\blacksquare$

### 习题四

（习题 5.3-5）证明: $y=\sin x$ 在 $\left(-\infty,+\infty\right)$ 中一致连续.

### 解答 习题四

对任意 $x_1,x_2\in\mathbb R$, 由拉格朗日中值定理, 
$$
\left|\sin x_1-\sin x_2\right|=\left|\cos\xi\right|\cdot\left|x_1-x_2\right|\le\left|x_1-x_2\right|,
$$

其中 $\xi$ 介于 $x_1$ 与 $x_2$ 之间.

对任意 $\varepsilon> 0$, 取 $\delta=\varepsilon$. 则当 $\left|x_1-x_2\right|< \delta$ 时, 
$$
\left|\sin x_1-\sin x_2\right|\le\left|x_1-x_2\right|< \delta=\varepsilon.
$$

由**定义**（一致连续）, $y=\sin x$ 在 $\mathbb R$ 上一致连续. $\blacksquare$

### 习题五

（习题 5.3-6）证明: $y=\cos x$ 在 $\left(-\infty,+\infty\right)$ 中一致连续.

### 解答 习题五

对任意 $x_1,x_2\in\mathbb R$, 由拉格朗日中值定理, 
$$
\left|\cos x_1-\cos x_2\right|=\left|-\sin\xi\right|\cdot\left|x_1-x_2\right|\le\left|x_1-x_2\right|,
$$

其中 $\xi$ 介于 $x_1$ 与 $x_2$ 之间.

对任意 $\varepsilon> 0$, 取 $\delta=\varepsilon$. 则当 $\left|x_1-x_2\right|< \delta$ 时, 
$$
\left|\cos x_1-\cos x_2\right|\le\left|x_1-x_2\right|< \delta=\varepsilon.
$$

由一致连续的定义, $y=\cos x$ 在 $\mathbb R$ 上一致连续. $\blacksquare$

### 习题六

（习题 5.3-7）证明: $y=\sin 3x+5x+1$ 在 $\left(-\infty,+\infty\right)$ 中一致连续.

### 解答 习题六

对任意 $x_1,x_2\in\mathbb R$, 
$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|=\left|\sin3x_1-\sin3x_2+5\left(x_1-x_2\right)\right|.
$$

由三角不等式及习题四($\sin x$ 一致连续), 
$$
\left|\sin3x_1-\sin3x_2\right|\le3\left|x_1-x_2\right|.
$$

故
$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|\le3\left|x_1-x_2\right|+5\left|x_1-x_2\right|=8\left|x_1-x_2\right|.
$$

对任意 $\varepsilon> 0$, 取 $\delta=\frac{\varepsilon}{8}$. 则当 $\left|x_1-x_2\right|< \delta$ 时, $\left|f\left(x_1\right)-f\left(x_2\right)\right|< \varepsilon$. 由一致连续的定义, $f\left(x\right)$ 在 $\mathbb R$ 上一致连续. $\blacksquare$

### 习题七

（习题 5.3-8）设 $f\left(x\right)$ 在 $\left(a,b\right)$ 中有定义, 且满足下列条件: 
$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|\le H\left|x_1-x_2\right|^\alpha,\forall x_1,x_2\in\left(a,b\right),
$$
其中 $H> 0$, $0< \alpha\le1$ 是常数. 这时称 $f\left(x\right)$ 在 $\left(a,b\right)$ 中赫尔德(Hölder)连续. 证明: 在 $\left(a,b\right)$ 中赫尔德连续的函数必一致连续. 再证明: 当 $f\left(x\right)$ 在 $\left(a,b\right)$ 中可导且其导数有界时, $f\left(x\right)$ 在 $\left(a,b\right)$ 中满足赫尔德条件, 其中 $\alpha=1$.

### 解答 习题七

**第一部分**: 设 $f$ 满足赫尔德条件, 指数为 $\alpha$. 对任意 $\varepsilon> 0$, 取 $\delta=\left(\frac{\varepsilon}{H}\right)^{1/\alpha}$. 则当 $\left|x_1-x_2\right|< \delta$ 时, 
$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|\le H\left|x_1-x_2\right|^\alpha< H\delta^\alpha=\varepsilon.
$$

由一致连续的定义, $f$ 在 $\left(a,b\right)$ 中一致连续.

**第二部分**: 设 $f'\left(x\right)$ 在 $\left(a,b\right)$ 中有界, 即存在 $M> 0$ 使得 $\left|f'\left(x\right)\right|\le M$($\forall x\in\left(a,b\right)$). 对任意 $x_1,x_2\in\left(a,b\right)$, 由拉格朗日中值定理, 
$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|=\left|f'\left(\xi\right)\right|\cdot\left|x_1-x_2\right|\le M\left|x_1-x_2\right|,
$$

其中 $\xi$ 介于 $x_1$ 与 $x_2$ 之间. 这正是 $\alpha=1$ 时的赫尔德条件, $H=M$. $\blacksquare$
