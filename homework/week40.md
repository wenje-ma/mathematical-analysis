# 作业 40

> **定理 3.2**（狄利克雷判别法）设数列 $\left\{b_n\right\}$ 单调趋于零，且级数 $\sum a_n$ 的部分和序列有界，则级数 $\sum a_nb_n$ 收敛.
>
> **定理 3.3**（阿贝尔判别法）设数列 $\left\{b_n\right\}$ 单调有界，且级数 $\sum a_n$ 收敛，则级数 $\sum a_nb_n$ 收敛.

### 习题一

（习题 10.3-2）证明：$\sum_{n=1}^{+\infty}\frac{\cos nx}{n^p}$（$0<x<2\pi$）当 $p>1$ 时绝对收敛，当 $0<p\le 1$ 时条件收敛.

### 解答 习题一

（1）当 $p>1$ 时，$\left|\frac{\cos nx}{n^p}\right|\le\frac{1}{n^p}$，而 $\sum\frac{1}{n^p}$ 为 $p>1$ 的 $p$ 级数，收敛. 由上一章**定理 2.2**（比较判别法），$\sum\left|\frac{\cos nx}{n^p}\right|$ 收敛，故原级数绝对收敛.

（2）当 $0<p\le 1$ 时，先证不绝对收敛. 注意到

$$
\left|\cos nx\right|\ge\cos^2 nx=\frac{1+\cos 2nx}{2},
$$

故

$$
\frac{\left|\cos nx\right|}{n^p}\ge\frac{1}{2n^p}+\frac{\cos 2nx}{2n^p}.
$$

右端第一项 $\sum\frac{1}{2n^p}$ 当 $p\le 1$ 时发散，第二项 $\sum\frac{\cos 2nx}{2n^p}$ 本身收敛（见下文），从而若 $\sum\frac{\left|\cos nx\right|}{n^p}$ 收敛则将迫使 $\sum\frac{1}{2n^p}$ 收敛，矛盾. 故原级数不绝对收敛.

再证原级数收敛. 对 $0<x<2\pi$，有

$$
\sum_{n=1}^{N}\cos nx=\frac{\sin\bigl(Nx+\frac{x}{2}\bigr)}{2\sin\frac{x}{2}}-\frac12,
$$

由于 $\sin\frac{x}{2}\ne 0$ 且有界，故 $\sum\cos nx$ 的部分和序列有界. 又 $\frac{1}{n^p}$ 当 $p>0$ 时单调趋于零. 由**定理 3.2**（狄利克雷判别法），$\sum\frac{\cos nx}{n^p}$ 收敛. 综上，$0<p\le 1$ 时原级数条件收敛. $\blacksquare$

### 习题二

（习题 10.3-4）$\sum_{n=1}^{+\infty}\frac{a_n}{n^x}$ 称为狄利克雷级数，证明：若 $\sum_{n=1}^{\infty}\frac{a_n}{n^{x_0}}$ 收敛（发散），则当 $x>x_0$（$x<x_0$）时，$\sum_{n=1}^{\infty}\frac{a_n}{n^x}$ 也收敛（发散）.

### 解答 习题二

先证收敛情形. 设 $x>x_0$，令

$$
\frac{a_n}{n^x}=\frac{a_n}{n^{x_0}}\cdot\frac{1}{n^{x-x_0}}.
$$

由假设 $\sum\frac{a_n}{n^{x_0}}$ 收敛. 又 $x-x_0>0$，故数列 $\left\{\frac{1}{n^{x-x_0}}\right\}$ 单调递减趋于零，从而单调有界. 由**定理 3.3**（阿贝尔判别法），$\sum\frac{a_n}{n^x}$ 收敛.

再证发散情形. 设 $x<x_0$ 而 $\sum\frac{a_n}{n^{x_0}}$ 发散. 反设 $\sum\frac{a_n}{n^x}$ 收敛. 令 $y=x_0-x>0$，则

$$
\frac{a_n}{n^{x_0}}=\frac{a_n}{n^x}\cdot\frac{1}{n^y}.
$$

由反设 $\sum\frac{a_n}{n^x}$ 收敛，而 $\left\{\frac{1}{n^y}\right\}$ 单调有界（递减趋于零）. 由**定理 3.3**（阿贝尔判别法），$\sum\frac{a_n}{n^{x_0}}$ 应收敛，与假设矛盾. 故 $\sum\frac{a_n}{n^x}$ 发散. $\blacksquare$

### 习题三

（习题 10.3-5）设 $h_n=\sum_{k=1}^{n}\frac{1}{k},\ S_n=\sum_{k=1}^{n}\frac{\left(-1\right)^{k-1}}{k}$.
(1) 证明 $S_{2n}=h_{2n}-h_n$；

(2) 利用 $h_n-\ln n\to\gamma$（$n\to\infty$），证明 $S_{2n}\to\ln 2$（$n\to\infty$）；

(3) 证明 $\sum_{n=1}^{+\infty}\frac{\left(-1\right)^{n-1}}{n}=\ln 2$.

### 解答 习题三

（1）直接计算偶数项部分和：

$$
\begin{aligned}
S_{2n}&=1-\frac12+\frac13-\frac14+\cdots+\frac{1}{2n-1}-\frac{1}{2n}\\
&=\left(1+\frac12+\frac13+\cdots+\frac{1}{2n}\right)-2\left(\frac12+\frac14+\cdots+\frac{1}{2n}\right)\\
&=h_{2n}-\left(1+\frac12+\cdots+\frac1n\right)=h_{2n}-h_n.
\end{aligned}
$$

（2）由假设 $h_n=\ln n+\gamma+o\left(1\right)$，故

$$
S_{2n}=h_{2n}-h_n=\bigl(\ln\left(2n\right)+\gamma+o\left(1\right)\bigr)-\bigl(\ln n+\gamma+o\left(1\right)\bigr)=\ln 2+o\left(1\right),
$$

即 $S_{2n}\to\ln 2$（$n\to\infty$）.

（3）再看奇数项部分和：

$$
S_{2n-1}=S_{2n}+\frac{1}{2n}\to\ln 2+0=\ln 2.
$$

偶数项与奇数项部分和均趋于同一极限 $\ln 2$，故 $\lim_{n\to\infty}S_n=\ln 2$，即

$$
\sum_{n=1}^{\infty}\frac{\left(-1\right)^{n-1}}{n}=\ln 2.
$$

$\blacksquare$
