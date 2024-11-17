# week12

> **定理 1.3 (拉格朗日中值定理)**
> 
> 设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 内可导. 则存在 $c\in\left(a,b\right)$, 使得 $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

> **定理 2.1 (上下极限与极限存在)**
> 
> 设 $\left\{a_n\right\}$ 为一个有界序列. 则 $\left\{a_n\right\}$ 有极限之充要条件为其上极限与下极限相等.

> **定理 2.2 (柯西收敛原理)**
> 
> 序列 $\left\{a_n\right\}$ 有极限之充要条件是: 对任意给定的 $\varepsilon>0$, 存在自然数 $N$, 使得 $\left|a_n-a_m\right|<\varepsilon$ (只要 $m,n\ge{N}$).

> **定理 3.2 (有限覆盖定理)**
> 
> 设 $\mathcal{F}=\left\{I_\alpha\right\}$ 是闭区间 $\left[a,b\right]$ 的任意一个开覆盖, 则存在 $\mathcal{F}$ 中的有限个元素 $I_{\alpha_1},\cdots,I_{\alpha_n}$, 使得 $\left[a,b\right]\subset\bigcup_{k=1}^nI_{\alpha_k}$.

## 5.1-7

试利用非空有上界必有上确界的定理推出: 单调递增有上界的序列一定有极限.

### 解答 5.1-7

设 $\left\{a_n\right\}$ 单调递增且有上界. 由上确界存在定理, $E=\left\{a_n:n\ge1\right\}$ 有上确界 $l=\sup{E}$.

对任意 $\varepsilon>0$, 由上确界与下确界的定义, 存在 $N$ 使得 $a_N>l-\varepsilon$. 又因 $\left\{a_n\right\}$ 单调递增, 当 $n>N$ 时 $a_n\ge{a}_N>l-\varepsilon$. 另一方面 $a_n\le{l}<{}l+\varepsilon$. 故 $\left|a_n-l\right|<\varepsilon$. 由序列极限的定义, $\lim_{n\to\infty}a_n=l$.

$\blacksquare$

## 5.1-9

设 $y=R\left(x\right)$ 为黎曼函数, 即 $R\left(x\right)=0$ ($x$ 为无理数), $R\left(x\right)=1/q$ ($x=p/q$ 为既约有理数). 证明:

(1) 对任意有理数 $x=p/q$, $\omega_R\left(x\right)=1/q$;

(2) 对任意无理数 $x$, $\omega_R\left(x\right)=0$.

### 解答 5.1-9

(1) 设 $x_0=p/q$ 为既约有理数, 则 $R\left(x_0\right)=1/q$. 在 $x_0$ 的任意邻域内, 既有无理数 $x$ 使得 $R\left(x\right)=0$, 又有 $x_0$ 本身. 故 $\sup{R}=1/q$, $\inf{R}=0$. 因此 $\omega_R\left(x_0\right)=1/q$.

(2) 设 $x_0$ 为无理数. 对任意 $\varepsilon>0$, 满足 $1/q\ge\varepsilon$ 的正整数 $q$ 只有有限多个, 对应的既约有理数 $p/q$ 也只有有限多个. 因此在 $x_0$ 的某个足够小的邻域内, 其余有理点都满足 $1/q<\varepsilon$. 故 $\sup{R}-\inf{R}<\varepsilon$. 由 $\varepsilon$ 的任意性, $\omega_R\left(x_0\right)=0$. 由**定理 1.3 (连续的充要条件)**, 黎曼函数在无理点连续.

$\blacksquare$

## 5.2-1

利用序列柯西收敛原理证明: 若 $\left\{a_n\right\}$ 收敛, 则 $\left\{\left|a_n\right|\right\}$ 收敛.

### 解答 5.2-1

设 $\lim_{n\to\infty}a_n=l$. 由**定理 2.2 (柯西收敛原理)**, 对任意 $\varepsilon>0$, 存在 $N$, 使得当 $m,n\ge{N}$ 时 $\left|a_n-a_m\right|<\varepsilon$.

由三角不等式, $\left|\left|a_n\right|-\left|a_m\right|\right|\le\left|a_n-a_m\right|<\varepsilon$. 故 $\left\{\left|a_n\right|\right\}$ 满足柯西条件. 由**定理 2.2 (柯西收敛原理)**, $\left\{\left|a_n\right|\right\}$ 收敛.

$\blacksquare$

## 5.2-2

设 $\left\{a_n\right\}$ 与 $\left\{b_n\right\}$ 为两个有界序列. 证明:

(1) $\varlimsup\left(a_n+b_n\right)\le\varlimsup{a}_n+\varlimsup{b}_n$;

(2) $\varliminf\left(a_n+b_n\right)\ge\varliminf{a}_n+\varliminf{b}_n$.

### 解答 5.2-2

(1) 记 $A_n=\sup\left\{a_k:k\ge{n}\right\}$, $B_n=\sup\left\{b_k:k\ge{n}\right\}$. 则 $a_k+b_k\le{A}_n+B_n$. 故 $\sup\left\{a_k+b_k:k\ge{n}\right\}\le{A}_n+B_n$. 令 $n\to\infty$, 得 $\varlimsup\left(a_n+b_n\right)\le\varlimsup{a}_n+\varlimsup{b}_n$.

(2) 同理, 记 $C_n=\inf\left\{a_k:k\ge{n}\right\}$, $D_n=\inf\left\{b_k:k\ge{n}\right\}$. 则 $a_k+b_k\ge{C}_n+D_n$. 令 $n\to\infty$, 得 $\varliminf\left(a_n+b_n\right)\ge\varliminf{a}_n+\varliminf{b}_n$.

$\blacksquare$

## 5.2-3

求上下极限:

(1) $\varlimsup_{x\to0}\sin\frac1x$ 及 $\varliminf_{x\to0}\sin\frac1x$;

(2) $\varlimsup_{x\to\infty}\sin{x}$ 及 $\varliminf_{x\to\infty}\sin{x}$.

### 解答 5.2-3

(1) 当 $x\to0$ 时, $\sin\frac1x$ 在 $-1$ 与 $1$ 之间无限次振荡. 在 $0$ 的任意小邻域内, $\sin\frac1x$ 都可以取到 $1$ 和 $-1$. 故 $\varlimsup_{x\to0}\sin\frac1x=1$, $\varliminf_{x\to0}\sin\frac1x=-1$.

(2) 当 $x\to\infty$ 时, $\sin{x}$ 同样在 $-1$ 与 $1$ 之间无限次振荡. 故 $\varlimsup_{x\to\infty}\sin{x}=1$, $\varliminf_{x\to\infty}\sin{x}=-1$.

$\blacksquare$

## 5.2-6

由柯西收敛原理证明下列序列收敛:

(1) $a_n=1-\frac12+\frac13-\cdots+\left(-1\right)^{n-1}\frac1n$;

(2) $a_n=\frac{\sin1}{1!}+\frac{\sin2}{2!}+\cdots+\frac{\sin{n}}{n!}$.

### 解答 5.2-6

(1) 设 $m>n$. 则 $\left|a_m-a_n\right|\le\frac1{n+1}$. 对任意 $\varepsilon>0$, 取 $N>\frac1\varepsilon$, 则 $\left|a_m-a_n\right|<\varepsilon$. 由**定理 2.2 (柯西收敛原理)**, $\left\{a_n\right\}$ 收敛.

(2) 设 $m>n$. 则 $\left|a_m-a_n\right|\le\frac1{\left(n+1\right)!}+\cdots+\frac1{m!}\le\frac1{2^n}$. 对任意 $\varepsilon>0$, 取 $N$ 使得 $2^N>\frac1\varepsilon$. 由**定理 2.2 (柯西收敛原理)**, $\left\{a_n\right\}$ 收敛.

$\blacksquare$

## 5.2-7

设 $f\left(x\right)$ 在 $a$ 点的空心邻域中有定义且有界. 设 $\left\{x_n\right\}$ 以 $a$ 为极限. 证明: 若 $\lim_{n\to\infty}f\left(x_n\right)$ 存在, 则 $\varliminf_{x\to{a}}f\left(x\right)\le\lim_{n\to\infty}f\left(x_n\right)\le\varlimsup_{x\to{a}}f\left(x\right)$.

### 解答 5.2-7

记 $l=\lim_{n\to\infty}f\left(x_n\right)$. 对任意 $\delta>0$, 当 $n$ 充分大时 $x_n$ 在空心邻域中. 故

$$
\inf\left\{f\left(x\right):0<\left|x-a\right|<\delta\right\}\le{f}\left(x_n\right)\le\sup\left\{f\left(x\right):0<\left|x-a\right|<\delta\right\}.
$$

令 $n\to\infty$, 再令 $\delta\to0$, 得 $\varliminf_{x\to{a}}f\left(x\right)\le{l}\le\varlimsup_{x\to{a}}f\left(x\right)$.

$\blacksquare$

## 5.2-8

假定 $f\left(x\right)$ 在 $a$ 点的一个空心邻域内有界. 证明: 存在序列 $\left\{x_n'\right\}$ 与 $\left\{x_n''\right\}$, 使得 $x_n'\to{a}$, $x_n''\to{a}$, 且 $\lim_{n\to\infty}f\left(x_n'\right)=\varlimsup_{x\to{a}}f\left(x\right)$, $\lim_{n\to\infty}f\left(x_n''\right)=\varliminf_{x\to{a}}f\left(x\right)$.

### 解答 5.2-8

记 $L=\varlimsup_{x\to{a}}f\left(x\right)$. 对任意 $n$, 在 $\left\{x:0<\left|x-a\right|<1/n\right\}$ 中存在 $x_n'$ 使得

$$
\sup\left\{f:0<\left|x-a\right|<1/n\right\}-\frac1n<{}f\left(x_n'\right)\le\sup\left\{f:0<\left|x-a\right|<1/n\right\}.
$$

令 $n\to\infty$, 由夹逼定理, $\lim_{n\to\infty}f\left(x_n'\right)=L$. 下极限的情形类似.

$\blacksquare$

## 5.2-9

利用上述两题证明: 当 $x\to{a}$ 时, $f\left(x\right)$ 有极限的充要条件是: 对任意点列 $x_n\to{a}$, 极限 $\lim_{n\to\infty}f\left(x_n\right)$ 都存在且相等.

### 解答 5.2-9

必要性: 设 $\lim_{x\to{a}}f\left(x\right)=l$. 对任意 $x_n\to{a}$, 由函数极限与序列极限的关系, $\lim_{n\to\infty}f\left(x_n\right)=l$.

充分性: 由 5.2-8, 存在 $x_n'\to{a}$ 使得 $\lim{f}\left(x_n'\right)=\varlimsup{f}\left(x\right)$, 存在 $x_n''\to{a}$ 使得 $\lim{f}\left(x_n''\right)=\varliminf{f}\left(x\right)$. 由假定, 这两个极限相等, 即 $\varlimsup_{x\to{a}}f\left(x\right)=\varliminf_{x\to{a}}f\left(x\right)$. 由**定理 2.1 (上下极限与极限存在)**, $\lim_{x\to{a}}f\left(x\right)$ 存在.

$\blacksquare$

## 5.3-2

设 $f\left(x\right)=\frac1x$ ($0<{}x<1$). 直接从定义出发, 证明 $f$ 在 $\left(0,1\right)$ 中不一致连续.

### 解答 5.3-2

取 $\varepsilon_0=1$. 对任意 $\delta>0$, 取 $x_1=\frac\delta2$, $x_2=\frac\delta3$. 则 $\left|x_1-x_2\right|=\frac\delta6<\delta$, 但

$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|=\left|\frac2\delta-\frac3\delta\right|=\frac1\delta.
$$

当 $\delta<1$ 时, $\frac1\delta>1=\varepsilon_0$. 故 $f$ 在 $\left(0,1\right)$ 中不一致连续.

$\blacksquare$

## 5.3-3

设集合 $E=\left\{\frac1n:n=1,2,\cdots\right\}$. 试构造 $E$ 的一个开覆盖, 但不能从中选出有限个元素覆盖住 $E$.

### 解答 5.3-3

对每个 $n$, 取开区间 $I_n=\left(\frac1n-\frac1{4n^2},\frac1n+\frac1{4n^2}\right)$. 显然 $\frac1n\in{I}_n$, 故 $E\subset\bigcup_{n=1}^\infty{I}_n$.

但任意有限个 $I_{n_1},\cdots,I_{n_k}$ 只能覆盖有限个点. 设 $N=\max\left\{n_1,\cdots,n_k\right\}$, 则当 $n>N$ 时 $\frac1n\notin\bigcup_{i=1}^kI_{n_i}$. 故不能选出有限子覆盖.

$\blacksquare$

## 5.3-4

证明: 对集合 $E=\left\{\frac1n\right\}\cup\left\{0\right\}$, 其任意开覆盖都存在有限子覆盖.

### 解答 5.3-4

设 $\mathcal{F}$ 是 $E$ 的任意开覆盖. 因 $0\in{E}$, 存在 $I_0\in\mathcal{F}$ 使得 $0\in{I}_0$. 因 $I_0$ 是开集, 存在 $\delta>0$ 使得 $\left(-\delta,\delta\right)\subset{I}_0$.

取 $N$ 使得 $\frac1N<\delta$. 则当 $n>N$ 时 $\frac1n\in{I}_0$. 对每个 $n=1,\cdots,N$, 存在 $I_n\in\mathcal{F}$ 使得 $\frac1n\in{I}_n$.

于是 $\left\{I_0,I_1,\cdots,I_N\right\}$ 是有限子覆盖.

$\blacksquare$

## 5.3-5

证明: $y=\sin{x}$ 在 $\mathbb{R}$ 上一致连续.

### 解答 5.3-5

对任意 $x_1,x_2\in\mathbb{R}$, 由**定理 1.3 (拉格朗日中值定理)**,

$$
\left|\sin{x}_1-\sin{x}_2\right|=\left|\cos\xi\right|\cdot\left|x_1-x_2\right|\le\left|x_1-x_2\right|.
$$

对任意 $\varepsilon>0$, 取 $\delta=\varepsilon$. 由一致连续的定义, $\sin{x}$ 在 $\mathbb{R}$ 上一致连续.

$\blacksquare$

## 5.3-6

证明: $y=\cos{x}$ 在 $\mathbb{R}$ 上一致连续.

### 解答 5.3-6

由**定理 1.3 (拉格朗日中值定理)**, $\left|\cos{x}_1-\cos{x}_2\right|\le\left|x_1-x_2\right|$. 取 $\delta=\varepsilon$. 由一致连续的定义, $\cos{x}$ 在 $\mathbb{R}$ 上一致连续.

$\blacksquare$

## 5.3-7

证明: $y=\sin3x+5x+1$ 在 $\mathbb{R}$ 上一致连续.

### 解答 5.3-7

由三角不等式,

$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|\le\left|\sin3x_1-\sin3x_2\right|+5\left|x_1-x_2\right|\le3\left|x_1-x_2\right|+5\left|x_1-x_2\right|=8\left|x_1-x_2\right|.
$$

取 $\delta=\frac\varepsilon8$. 由一致连续的定义, $f$ 在 $\mathbb{R}$ 上一致连续.

$\blacksquare$

## 5.3-8

设 $f$ 在 $\left(a,b\right)$ 中满足 $\left|f\left(x_1\right)-f\left(x_2\right)\right|\le{H}\left|x_1-x_2\right|^\alpha$ ($0<\alpha\le1$). 证明:

(1) 赫尔德连续的函数必一致连续;

(2) 若 $f$ 可导且导数有界, 则 $f$ 满足 $\alpha=1$ 的赫尔德条件.

### 解答 5.3-8

(1) 对任意 $\varepsilon>0$, 取 $\delta=\left(\frac\varepsilon{H}\right)^{1/\alpha}$. 则 $\left|f\left(x_1\right)-f\left(x_2\right)\right|\le{H}\delta^\alpha=\varepsilon$. 由一致连续的定义, $f$ 一致连续.

(2) 设 $\left|f'\left(x\right)\right|\le{M}$. 由**定理 1.3 (拉格朗日中值定理)**,

$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|=\left|f'\left(\xi\right)\right|\cdot\left|x_1-x_2\right|\le{M}\left|x_1-x_2\right|.
$$

此即 $\alpha=1$ 的赫尔德条件, $H=M$.

$\blacksquare$

## 6.1-2

写出函数 $y=x$ 与 $y=x^2$ 在 $\left[0,1\right]$ 中的黎曼和 ($n$ 等分, 右端点), 并求 $n\to\infty$ 时的极限.

### 解答 6.1-2

对 $y=x$, 黎曼和为 $\frac1{n^2}\sum_{k=1}^nk=\frac{n+1}{2n}$. 由定积分的定义, $\int_0^1x\,\mathrm{d}x=\lim_{n\to\infty}\frac{n+1}{2n}=\frac12$.

对 $y=x^2$, 黎曼和为 $\frac1{n^3}\sum_{k=1}^nk^2=\frac{\left(n+1\right)\left(2n+1\right)}{6n^2}$. 故 $\int_0^1x^2\,\mathrm{d}x=\frac13$.

$\blacksquare$
