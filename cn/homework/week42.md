# 作业 42

> **定义**（函数序列的一致收敛）设 $\left\{f_n\left(x\right)\right\}$ 在集合 $X$ 上有定义, $f\left(x\right)$ 为 $X$ 上的函数. 若对任意 $\varepsilon> 0$, 存在自然数 $N$, 使得当 $n> N$ 时, 对一切 $x\in X$ 均有 $\left|f_n\left(x\right)-f\left(x\right)\right|< \varepsilon$, 则称 $\left\{f_n\left(x\right)\right\}$ 在 $X$ 上一致收敛于 $f\left(x\right)$.
> 
> **定理 1.1**（M 判别法）设存在数列 $M_n> 0$, $M_n\to 0$, 使得 $\left|f_n\left(x\right)-f\left(x\right)\right|\le M_n$ 对一切 $x\in X$ 成立, 则 $\left\{f_n\left(x\right)\right\}$ 在 $X$ 上一致收敛于 $f\left(x\right)$.
> 
> **定理 1.2**（极限函数的连续性）设 $\left\{f_n\left(x\right)\right\}$ 在区间 $X$ 上一致收敛于 $f\left(x\right)$, 且每个 $f_n\left(x\right)$ 在 $X$ 上连续, 则 $f\left(x\right)$ 在 $X$ 上连续.

### 习题一

（习题 11.1-1-1）讨论函数序列 $f_n\left(x\right)=\frac{1}{1+nx}$, $x\in\left(0,1\right)$ 的一致收敛性.

### 解答 习题一

对任意固定 $x\in\left(0,1\right)$, 当 $n\to\infty$ 时 $1+nx\to+\infty$, 故 $f_n\left(x\right)\to 0$, 即极限函数 $f\left(x\right)\equiv 0$.

考察

$$
\sup_{0< x< 1}\left|f_n\left(x\right)-0\right|=\sup_{0< x< 1}\frac{1}{1+nx}.
$$

当 $x\to 0^+$ 时 $\frac{1}{1+nx}\to 1$, 故该上确界为 $1$(不趋于 $0$). 取 $\varepsilon_0=\frac12$, 对任意 $n$, 取 $x_n=\frac{1}{n}\in\left(0,1\right)$, 则

$$
\left|f_n\left(x_n\right)-0\right|=\frac{1}{1+1}=\frac12=\varepsilon_0.
$$

由**定义**（函数序列的一致收敛）, 不可能找到 $N$ 使 $n> N$ 时 $\left|f_n\left(x\right)-0\right|< \varepsilon_0$ 对一切 $x\in\left(0,1\right)$ 成立. 故 $\left\{f_n\left(x\right)\right\}$ 在 $\left(0,1\right)$ 上不一致收敛于 $0$. $\blacksquare$

### 习题二

（习题 11.1-1-3）讨论函数序列 $f_n\left(x\right)=\frac{\sin\left(nx+n\right)}{n}$, $x\in\left(-\infty,+\infty\right)$ 的一致收敛性.

### 解答 习题二

对任意 $x\in\mathbb R$, $\left|\sin\left(nx+n\right)\right|\le 1$, 故 $f_n\left(x\right)\to 0$, 极限函数 $f\left(x\right)\equiv 0$. 又

$$
\left|f_n\left(x\right)-f\left(x\right)\right|=\frac{\left|\sin\left(nx+n\right)\right|}{n}\le\frac{1}{n}=M_n,
$$

而 $M_n=\frac1n\to 0$. 由**定理 1.1**（M 判别法）, $\left\{f_n\left(x\right)\right\}$ 在 $\mathbb R$ 上一致收敛于 $0$. $\blacksquare$

### 习题三

（习题 11.1-1-5）讨论函数序列 $f_n\left(x\right)=nxe^{-nx^2}$, $x\in\left[0,1\right]$ 的一致收敛性.

### 解答 习题三

对任意固定 $x\in\left[0,1\right]$, 当 $x=0$ 时 $f_n\left(0\right)=0$; 当 $x> 0$ 时 $nx^2\to+\infty$, 故 $nxe^{-nx^2}\to 0$. 极限函数 $f\left(x\right)\equiv 0$.

令 $u=\sqrt{n}\,x$, 则

$$
f_n\left(x\right)=\sqrt n\,u\,e^{-u^2}, u\in\left[0,\sqrt n\right].
$$

函数 $u e^{-u^2}$ 在 $u=\frac{1}{\sqrt2}$ 处取最大值 $\frac{1}{\sqrt{2e}}$. 取 $x_n=\frac{1}{\sqrt{2n}}\in\left[0,1\right]$, 则

$$
\left|f_n\left(x_n\right)-0\right|=\sqrt n\cdot\frac{1}{\sqrt2}e^{-1/2}=\sqrt{\frac{n}{2e}}\to+\infty.
$$

故 $\sup_{x\in\left[0,1\right]}\left|f_n\left(x\right)-0\right|\not\to 0$, 由**定义**（函数序列的一致收敛）, $\left\{f_n\left(x\right)\right\}$ 在 $\left[0,1\right]$ 上不一致收敛于 $0$. $\blacksquare$

### 习题四

（习题 11.1-2）设 $f_n\left(x\right)$ 在 $\left(a,b\right)$ 内一致收敛于 $f\left(x\right)$. 又设对每一个 $n$, 极限 $\lim_{x\to x_0}f_n\left(x\right)$ 存在, 其中 $x_0\in\left(a,b\right)$. 假定 $\lim_{x\to x_0}f\left(x\right)$ 存在, 证明
$$
\lim_{x\to x_0}f\left(x\right)=\lim_{n\to\infty}\left(\lim_{x\to x_0}f_n\left(x\right)\right).
$$

### 解答 习题四

本题是**定理 1.2**（极限函数的连续性）在 $f_n$ 未必连续, 仅在 $x_0$ 处有极限时的推广, 证明思路与**定理 1.2** 相同. 记 $A_n=\lim_{x\to x_0}f_n\left(x\right)$. 对任意 $\varepsilon> 0$, 由 $\left\{f_n\left(x\right)\right\}$ 在 $\left(a,b\right)$ 内一致收敛于 $f\left(x\right)$, 存在 $N$, 当 $n> N$ 时, 对一切 $x\in\left(a,b\right)$ 有

$$
\left|f_n\left(x\right)-f\left(x\right)\right|< \frac{\varepsilon}{3}.
$$

取定 $m,n> N$. 令 $x\to x_0$, 由极限的保序性得

$$
\left|A_m-A_n\right|=\lim_{x\to x_0}\left|f_m\left(x\right)-f_n\left(x\right)\right|\le\frac{2\varepsilon}{3}< \varepsilon.
$$

故 $\left\{A_n\right\}$ 为柯西列, 从而存在有限极限 $A=\lim_{n\to\infty}A_n$.

再证 $\lim_{x\to x_0}f\left(x\right)=A$. 取 $n> N$ 固定, 由 $A_n=\lim_{x\to x_0}f_n\left(x\right)$, 存在 $\delta> 0$, 当 $0< \left|x-x_0\right|< \delta$ 时

$$
\left|f_n\left(x\right)-A_n\right|< \frac{\varepsilon}{3}.
$$

于是当 $0< \left|x-x_0\right|< \delta$ 时, 

$$
\left|f\left(x\right)-A\right|\le \left|f\left(x\right)-f_n\left(x\right)\right|+\left|f_n\left(x\right)-A_n\right|+\left|A_n-A\right|< \frac{\varepsilon}{3}+\frac{\varepsilon}{3}+\frac{\varepsilon}{3}=\varepsilon.
$$

故

$$
\lim_{x\to x_0}f\left(x\right)=A=\lim_{n\to\infty}\left(\lim_{x\to x_0}f_n\left(x\right)\right).
$$

$\blacksquare$

### 习题五

（习题 11.1-3）证明 $f_n\left(x\right)=\left(1+\frac{x}{n}\right)^n$ 在 $\left[0,+\infty\right)$ 上不一致收敛于极限函数 $e^x$.

### 解答 习题五

对任意固定 $x\in\left[0,+\infty\right)$, $\lim_{n\to\infty}\left(1+\frac{x}{n}\right)^n=e^x$, 故极限函数为 $f\left(x\right)=e^x$.

取 $x_n=n\in\left[0,+\infty\right)$, 则

$$
\left|f_n\left(x_n\right)-e^{x_n}\right|=\left|\left(1+1\right)^n-e^n\right|=\left|2^n-e^n\right|=e^n-2^n\to+\infty.
$$

故

$$
\sup_{x\in\left[0,+\infty\right)}\left|f_n\left(x\right)-e^x\right|\not\to 0,
$$

由**定义**（函数序列的一致收敛）, $\left\{f_n\left(x\right)\right\}$ 在 $\left[0,+\infty\right)$ 上不一致收敛于 $e^x$. $\blacksquare$

### 习题六

（习题 11.1-4）证明 $f_n\left(x\right)=\left(1+\frac{x}{n}\right)^n$ 在任一闭区间 $\left[0,A\right]$ 上一致收敛于 $e^x$, 其中 $A> 0$.

### 解答 习题六

对固定 $x\in\left[0,A\right]$, 极限函数为 $f\left(x\right)=e^x$. 由不等式 $e^\top\ge 1+t$($t\ge 0$), 有

$$
0\le e^x-\left(1+\frac{x}{n}\right)^n.
$$

利用展开 $\ln\left(1+t\right)\le t$, 得

$$
n\ln\left(1+\frac{x}{n}\right)\le x,
$$

从而 $\left(1+\frac{x}{n}\right)^n\le e^x$. 又由

$$
\ln\left(1+t\right)=t-\frac{t^2}{2\left(1+\xi\right)^2}\ge t-\frac{t^2}{2}\ \left(\xi\in\left[0,t\right]\right),
$$

对 $x\in\left[0,A\right]$,

$$
n\ln\left(1+\frac{x}{n}\right)\ge n\left(\frac{x}{n}-\frac{x^2}{2n^2}\right)=x-\frac{x^2}{2n}\ge x-\frac{A^2}{2n}.
$$

于是

$$
0\le e^x-\left(1+\frac{x}{n}\right)^n\le e^x\left(1-e^{-A^2/\left(2n\right)}\right)\le e^A\cdot\frac{A^2}{2n}=M_n,
$$

其中 $M_n=\frac{A^2e^A}{2n}\to 0$. 由**定理 1.1**（M 判别法）, $\left\{f_n\left(x\right)\right\}$ 在 $\left[0,A\right]$ 上一致收敛于 $e^x$. $\blacksquare$

### 习题七

（习题 11.1-5）设 $f\left(x\right)$ 及 $f_n\left(x\right)$ 均是 $\left[a,b\right]$ 上的连续函数. 令
$$
M_n=\max_{x\in\left[a,b\right]}\left|f_n\left(x\right)-f\left(x\right)\right|,
$$
证明: 当且仅当 $M_n\to 0$($n\to\infty$)时, $f_n\left(x\right)$ 在 $\left[a,b\right]$ 上一致收敛于 $f\left(x\right)$.

### 解答 习题七

(1)必要性. 设 $\left\{f_n\left(x\right)\right\}$ 在 $\left[a,b\right]$ 上一致收敛于 $f\left(x\right)$. 对任意 $\varepsilon> 0$, 存在 $N$, 当 $n> N$ 时, 对一切 $x\in\left[a,b\right]$ 有 $\left|f_n\left(x\right)-f\left(x\right)\right|< \varepsilon$. 由连续性, 最大值在某点 $x_n\in\left[a,b\right]$ 处取到, 故

$$
M_n=\left|f_n\left(x_n\right)-f\left(x_n\right)\right|< \varepsilon.
$$

由 $\varepsilon$ 的任意性, $M_n\to 0$.

(2)充分性. 设 $M_n\to 0$. 对任意 $\varepsilon> 0$, 存在 $N$, 当 $n> N$ 时 $M_n< \varepsilon$. 于是对一切 $x\in\left[a,b\right]$, 

$$
\left|f_n\left(x\right)-f\left(x\right)\right|\le M_n< \varepsilon.
$$

由**定义**（函数序列的一致收敛）, $\left\{f_n\left(x\right)\right\}$ 在 $\left[a,b\right]$ 上一致收敛于 $f\left(x\right)$. $\blacksquare$
