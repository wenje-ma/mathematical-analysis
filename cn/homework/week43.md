# 作业 43

> **定理 2.2**（魏尔斯特拉斯 M 判别法）设 $\left|u_n\left(x\right)\right|\le a_n$ 对一切 $x\in X$ 及充分大的 $n$ 成立, 且 $\sum a_n$ 收敛, 则函数项级数 $\sum u_n\left(x\right)$ 在 $X$ 上一致收敛.
> 
> **定理 2.4**（狄利克雷判别法）设函数项级数 $\sum a_n\left(x\right)b_n\left(x\right)$ 中, $\sum a_n\left(x\right)$ 的部分和序列在 $X$ 上一致有界, $b_n\left(x\right)$ 对每个 $x\in X$ 关于 $n$ 单调, 且 $b_n\left(x\right)$ 在 $X$ 上一致趋于零, 则 $\sum a_n\left(x\right)b_n\left(x\right)$ 在 $X$ 上一致收敛.
> 
> **定理 2.5**（和函数的连续性）设 $u_n\left(x\right)$ 在区间 $X$ 上连续, 且 $\sum u_n\left(x\right)$ 在 $X$ 上一致收敛, 则其和函数 $S\left(x\right)$ 在 $X$ 上连续.
> 
> **定理 2.7**（逐项求导定理）设 $\sum u_n\left(x\right)$ 在 $\left[a,b\right]$ 上收敛于 $S\left(x\right)$, $u_n\left(x\right)$ 在 $\left[a,b\right]$ 上有连续导数, 且 $\sum u_n'\left(x\right)$ 在 $\left[a,b\right]$ 上一致收敛, 则 $S\left(x\right)$ 在 $\left[a,b\right]$ 上可导, 且 $S'\left(x\right)=\sum u_n'\left(x\right)$.

### 习题一

（习题 11.2-1-2）讨论级数 $\sum_{n=1}^{+\infty}\frac{\left(-1\right)^{n+1}}{x^2+n}$ 在 $x\in\left(-\infty,+\infty\right)$ 上的一致收敛性.

### 解答 习题一

令 $a_n\left(x\right)=\left(-1\right)^{n+1}$, $b_n\left(x\right)=\frac{1}{x^2+n}$. 部分和 $\sum_{k=1}^{N}a_k\left(x\right)$ 在 $-1$ 与 $0$ 之间摆动, 一致有界. 对每个固定 $x$, $b_n\left(x\right)$ 关于 $n$ 单调递减; 且

$$
\left|b_n\left(x\right)\right|\le\frac{1}{n}\to 0
$$

关于 $x\in\mathbb R$ 一致. 由**定理 2.4**（狄利克雷判别法）, 该级数在 $\mathbb R$ 上一致收敛. $\blacksquare$

### 习题二

（习题 11.2-1-4）讨论级数 $\sum_{n=1}^{+\infty}\frac{x}{\left(1+\left(n-1\right)x\right)\left(1+nx\right)}$ 在 $x\in\left(-\infty,+\infty\right)$ 上的一致收敛性.

### 解答 习题二

注意到

$$
\frac{x}{\left(1+\left(n-1\right)x\right)\left(1+nx\right)}=\frac{1}{1+\left(n-1\right)x}-\frac{1}{1+nx},
$$

故部分和为

$$
S_N\left(x\right)=1-\frac{1}{1+Nx}.
$$

当 $x> 0$ 时, $S_N\left(x\right)\to 1$; 当 $x=0$ 时, $S_N\left(0\right)=0$; 当 $x< 0$ 时, $1+Nx$  eventually 取 $0$ 或负值, 级数在 $x< 0$ 时无定义或发散. 故和函数在 $x=0$ 处不连续(右极限为 $1$, 而函数值为 $0$). 由于各项 $\frac{x}{\left(1+\left(n-1\right)x\right)\left(1+nx\right)}$ 在 $\left(0,+\infty\right)$ 上连续, 由**定理 2.5**（和函数的连续性）, 若级数在 $\left(0,+\infty\right)$ 上一致收敛则和函数必连续, 矛盾. 故该级数在 $\left(0,+\infty\right)$ 上不一致收敛. $\blacksquare$

### 习题三

（习题 11.2-1-6）讨论级数 $\sum_{n=1}^{+\infty}\frac{1}{n^2+x^2}$ 在 $x\in\left[0,+\infty\right)$ 上的一致收敛性.

### 解答 习题三

对一切 $x\in\left[0,+\infty\right)$, 

$$
\left|\frac{1}{n^2+x^2}\right|\le\frac{1}{n^2}=a_n,
$$

而 $\sum\frac{1}{n^2}$ 为 $p=2> 1$ 的 $p$ 级数, 收敛. 由**定理 2.2**（魏尔斯特拉斯 M 判别法）, 该级数在 $\left[0,+\infty\right)$ 上一致收敛. $\blacksquare$

### 习题四

（习题 11.2-9）讨论级数 $\sum_{n=1}^{+\infty}\left(-1\right)^n\frac{n+x^2}{n^2}$ 的一致收敛性: 
(i) $x\in\left[a,b\right]$; 

(ii) $x\in\left(-\infty,+\infty\right)$.

### 解答 习题四

(i)令 $a_n\left(x\right)=\left(-1\right)^n$, $b_n\left(x\right)=\frac{n+x^2}{n^2}=\frac1n+\frac{x^2}{n^2}$. 部分和 $\sum_{k=1}^{N}\left(-1\right)^k$ 一致有界. 对每个固定 $x$, $b_n\left(x\right)$ 关于 $n$ 单调递减(因 $\frac1n$ 与 $\frac{x^2}{n^2}$ 均递减). 又对 $x\in\left[a,b\right]$, $x^2\le C=\max\left(a^2,b^2\right)$, 故

$$
0\le b_n\left(x\right)\le\frac1n+\frac{C}{n^2}\to 0
$$

关于 $x\in\left[a,b\right]$ 一致. 由**定理 2.4**（狄利克雷判别法）, 级数在 $\left[a,b\right]$ 上一致收敛.

(ii)在 $\mathbb R$ 上, 通项

$$
u_n\left(x\right)=\left(-1\right)^n\left(\frac1n+\frac{x^2}{n^2}\right)
$$

的绝对值在 $x=\sqrt n$ 处取到 $\frac1n+\frac1n=\frac2n$, 但 $\sup_{x\in\mathbb R}\frac{x^2}{n^2}=+\infty$, 故通项不一致趋于零. 由**定理 2.1**（柯西收敛原理）的推论(通项一致趋于零为一致收敛之必要条件), 级数在 $\mathbb R$ 上不一致收敛. $\blacksquare$

### 习题五

（习题 11.2-10）讨论级数 $\sum_{n=1}^{+\infty}\left(-1\right)^{n-1}x^2e^{-nx^2}$($-\infty< x< +\infty$)的一致收敛性.

### 解答 习题五

令 $a_n\left(x\right)=\left(-1\right)^{n-1}$, $b_n\left(x\right)=x^2e^{-nx^2}$. 对每个固定 $x$, $b_n\left(x\right)$ 关于 $n$ 单调递减(因 $e^{-nx^2}$ 递减). 又

$$
\left|b_n\left(x\right)\right|=x^2e^{-nx^2}.
$$

令 $t=x^2\ge 0$, 则 $te^{-nt}$ 关于 $t$ 的最大值在 $t=\frac1n$ 处取到, 最大值为 $\frac1n e^{-1}=\frac{1}{en}\to 0$, 且该估计关于 $x$ 一致. 故 $b_n\left(x\right)$ 在 $\mathbb R$ 上一致趋于零. 部分和 $\sum_{k=1}^{N}\left(-1\right)^{k-1}$ 一致有界. 由**定理 2.4**（狄利克雷判别法）, 级数在 $\mathbb R$ 上一致收敛. $\blacksquare$

### 习题六

（习题 11.2-11）讨论级数 $\sum_{n=1}^{+\infty}\frac{\sin x\cdot\sin nx}{\sqrt{n^2+x^2}}$($0\le x\le 2\pi$)的一致收敛性.

### 解答 习题六

令 $a_n\left(x\right)=\sin nx$, $b_n\left(x\right)=\frac{\sin x}{\sqrt{n^2+x^2}}$. 先证 $\sum_{k=1}^{N}a_k\left(x\right)$ 与 $\sin x$ 之积在 $\left[0,2\pi\right]$ 上一致有界. 由公式

$$
\sum_{k=1}^{N}\sin kx=\frac{\cos\frac{x}{2}-\cos\left(Nx+\frac{x}{2}\right)}{2\sin\frac{x}{2}},
$$

两边乘 $\sin x=2\sin\frac{x}{2}\cos\frac{x}{2}$, 得

$$
\sin x\sum_{k=1}^{N}\sin kx=\cos\frac{x}{2}\left(\cos\frac{x}{2}-\cos\left(Nx+\frac{x}{2}\right)\right).
$$

右端绝对值不超过 $2$, 故 $\sum_{k=1}^{N}\sin x\cdot\sin kx$ 关于 $N$ 与 $x\in\left[0,2\pi\right]$ 一致有界.

又 $b_n\left(x\right)=\frac{\sin x}{\sqrt{n^2+x^2}}\le\frac{1}{n}$, 关于 $x$ 一致趋于零, 且对固定 $x$ 关于 $n$ 单调递减. 由**定理 2.4**（狄利克雷判别法）, 原级数在 $\left[0,2\pi\right]$ 上一致收敛. $\blacksquare$

### 习题七

（习题 11.2-5）证明函数
$$
f\left(x\right)=\sum_{n=1}^{\infty}2^n\sin\frac{x}{3^n}
$$
在 $\left(-\infty,+\infty\right)$ 上处处有连续的导函数.

### 解答 习题七

各项 $u_n\left(x\right)=2^n\sin\frac{x}{3^n}$ 在 $\mathbb R$ 上连续可导. 形式逐项求导得

$$
u_n'\left(x\right)=2^n\cdot\frac{1}{3^n}\cos\frac{x}{3^n}=\left(\frac23\right)^n\cos\frac{x}{3^n}.
$$

对一切 $x\in\mathbb R$, 

$$
\left|u_n'\left(x\right)\right|\le\left(\frac23\right)^n,
$$

而 $\sum\left(\frac23\right)^n$ 为收敛的等比级数. 由**定理 2.2**（魏尔斯特拉斯 M 判别法）, $\sum u_n'\left(x\right)$ 在 $\mathbb R$ 上一致收敛.

又原级数 $\sum u_n\left(x\right)$ 对任意 $x$ 收敛(因

$$
\left|u_n\left(x\right)\right|\le 2^n\left|x/3^n\right|=\left|\frac{2x}{3}\right|
$$

之后由比值法控制). 由**定理 2.7**（逐项求导定理）, $f\left(x\right)$ 在任意闭区间 $\left[a,b\right]$ 上可导, 且

$$
f'\left(x\right)=\sum_{n=1}^{\infty}\left(\frac23\right)^n\cos\frac{x}{3^n}.
$$

右端各项连续, 且由 M 判别法知其在任意 $\left[a,b\right]$ 上一致收敛, 故由**定理 2.5**（和函数的连续性）, $f'\left(x\right)$ 连续. 由 $\left[a,b\right]$ 的任意性, $f\left(x\right)$ 在 $\mathbb R$ 上处处有连续的导函数. $\blacksquare$

### 习题八

（习题 11.2-6）设 $\zeta\left(x\right)=\sum_{n=1}^{\infty}\frac{1}{n^x}$($x> 1$), 证明 $\zeta\left(x\right)$ 的导数存在, 并给出其表达式.

### 解答 习题八

对任意 $x_0> 1$, 取 $a$ 满足 $1< a< x_0$. 在区间 $\left[a,+\infty\right)$ 上考察形式逐项求导级数: 

$$
\sum_{n=1}^{\infty}\left(\frac{1}{n^x}\right)'=-\sum_{n=1}^{\infty}\frac{\ln n}{n^x}.
$$

对 $x\ge a$, 

$$
\left|\frac{\ln n}{n^x}\right|\le\frac{\ln n}{n^a}.
$$

因 $a> 1$, 取 $\varepsilon> 0$ 使 $a-\varepsilon> 1$, 则

$$
\frac{\ln n}{n^a}=\frac{\ln n}{n^\varepsilon}\cdot\frac{1}{n^{a-\varepsilon}}\le C\cdot\frac{1}{n^{a-\varepsilon}},
$$

而 $\sum\frac{1}{n^{a-\varepsilon}}$ 收敛, 故 $\sum\frac{\ln n}{n^a}$ 收敛. 由**定理 2.2**（魏尔斯特拉斯 M 判别法）, 求导级数在 $\left[a,+\infty\right)$ 上一致收敛.

又原级数 $\sum\frac{1}{n^x}$ 在 $x> 1$ 时收敛. 由**定理 2.7**（逐项求导定理）, $\zeta\left(x\right)$ 在 $\left[a,+\infty\right)$ 上可导, 且

$$
\zeta'\left(x\right)=-\sum_{n=1}^{\infty}\frac{\ln n}{n^x}.
$$

由 $x_0> 1$ 的任意性, $\zeta\left(x\right)$ 在 $\left(1,+\infty\right)$ 上导数存在, 表达式为上式. $\blacksquare$
