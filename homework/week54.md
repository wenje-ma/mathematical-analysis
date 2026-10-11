# 作业 54

> **定理 3.1**（狄利克雷收敛定理）设 $f\left(x\right)$ 以 $2\pi$ 为周期且在 $\left[-\pi,\pi\right]$ 上逐段单调有界，则其傅里叶级数在每点 $x$ 收敛于 $\frac{f\left(x+0\right)+f\left(x-0\right)}{2}$；在 $f$ 的连续点收敛于 $f\left(x\right)$，在间断点收敛于左右极限的平均值.

> **命题**（傅里叶系数）以 $2\pi$ 为周期的可积函数 $f\left(x\right)$ 的傅里叶系数为 $a_n=\frac1\pi\displaystyle\int_{-\pi}^\pi f\left(x\right)\cos nx\,\mathrm{d}x$，$b_n=\frac1\pi\displaystyle\int_{-\pi}^\pi f\left(x\right)\sin nx\,\mathrm{d}x$.

> **定理**（封闭性方程）设 $f\left(x\right)$ 的傅里叶系数为 $a_n,b_n$，则 $\frac1\pi\displaystyle\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x=\frac{a_0^2}{2}+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right)$.

### 习题一

（习题 13.3-1）设 $f\left(x\right)$ 是以 $2\pi$ 为周期的函数，在 $\left(-\pi,\pi\right]$ 上 $f\left(x\right)=\begin{cases}0,&x\in\left(-\pi,0\right];\\ 1,&x\in\left(0,\pi\right].\end{cases}$ 证明：当 $0<x<\pi$ 时，$\displaystyle1=\frac12+\frac2\pi\sum_{n=0}^\infty\frac{\sin\left(2n+1\right)x}{2n+1}$，并由此推出 $\displaystyle\frac\pi4=\sum_{n=0}^\infty\frac{\left(-1\right)^n}{2n+1}$.

### 解答 习题一

由**命题**（傅里叶系数），$a_0=\frac1\pi\displaystyle\int_0^\pi1\,\mathrm{d}x=1$，$a_n=\frac1\pi\displaystyle\int_0^\pi\cos nx\,\mathrm{d}x=0$（$n\ge1$），且

$$
b_n=\frac1\pi\int_0^\pi\sin nx\,\mathrm{d}x=\frac{1-\left(-1\right)^n}{n\pi}.
$$

故 $n$ 为偶数时 $b_n=0$，$n$ 为奇数时 $b_n=\frac{2}{n\pi}$. 于是

$$
f\left(x\right)\sim\frac12+\frac2\pi\sum_{n=0}^\infty\frac{\sin\left(2n+1\right)x}{2n+1}.
$$

当 $0<x<\pi$ 时 $f$ 连续且 $f\left(x\right)=1$，由**定理 3.1**（狄利克雷收敛定理），

$$
1=\frac12+\frac2\pi\sum_{n=0}^\infty\frac{\sin\left(2n+1\right)x}{2n+1}.
$$

取 $x=\frac\pi2$，则 $\sin\frac{\left(2n+1\right)\pi}{2}=\left(-1\right)^n$，得

$$
1=\frac12+\frac2\pi\sum_{n=0}^\infty\frac{\left(-1\right)^n}{2n+1},\ \text{即}\;\frac\pi4=\sum_{n=0}^\infty\frac{\left(-1\right)^n}{2n+1}.
$$

$\blacksquare$

### 习题二

（习题 13.3-3）设 $f\left(x\right)$ 是以 $2\pi$ 为周期的函数，在 $\left[-\pi,\pi\right]$ 上 $f\left(x\right)=\left(\pi-\lvert x\rvert\right)^2$. 求该函数的傅里叶级数，并利用它求出 $\displaystyle\sum_{n=1}^\infty\frac1{n^2}$ 与 $\displaystyle\sum_{n=1}^\infty\frac1{n^4}$ 的值.

### 解答 习题二

$f\left(x\right)=\left(\pi-\lvert x\rvert\right)^2$ 为偶函数，故 $b_n=0$. 由**命题**（傅里叶系数），

$$
a_0=\frac{2}{\pi}\int_0^\pi\left(\pi-x\right)^2\,\mathrm{d}x=\frac{2\pi^2}{3},
$$

$$
a_n=\frac{2}{\pi}\int_0^\pi\left(\pi-x\right)^2\cos nx\,\mathrm{d}x.
$$

令 $u=\pi-x$，则 $\cos nx=\cos\left(n\pi-nu\right)=\left(-1\right)^n\cos nu$，于是

$$
a_n=\frac{2\left(-1\right)^n}{\pi}\int_0^\pi u^2\cos nu\,\mathrm{d}u=\frac{2\left(-1\right)^n}{\pi}\cdot\frac{2\pi\left(-1\right)^n}{n^2}=\frac{4}{n^2}.
$$

故
$$
f\left(x\right)\sim\frac{\pi^2}{3}+4\displaystyle\sum_{n=1}^\infty\frac{\cos nx}{n^2}.
$$

在 $x=0$ 处 $f$ 连续，由**定理 3.1**（狄利克雷收敛定理），$f\left(0\right)=\pi^2=\frac{\pi^2}{3}+4\displaystyle\sum_{n=1}^\infty\frac1{n^2}$，解得 $\displaystyle\sum_{n=1}^\infty\frac1{n^2}=\frac{\pi^2}{6}$.

再由**定理**（封闭性方程），

$$
\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x=\frac{a_0^2}{2}+\sum_{n=1}^\infty a_n^2.
$$

左端 $=\frac{2}{\pi}\displaystyle\int_0^\pi\left(\pi-x\right)^4\,\mathrm{d}x=\frac{2\pi^4}{5}$；右端 $=\frac12\left(\frac{2\pi^2}{3}\right)^2+\displaystyle\sum_{n=1}^\infty\frac{16}{n^4}=\frac{2\pi^4}{9}+16\sum\frac1{n^4}$. 故

$$
16\sum_{n=1}^\infty\frac1{n^4}=2\pi^4\left(\frac15-\frac19\right)=\frac{8\pi^4}{45},\ \sum_{n=1}^\infty\frac1{n^4}=\frac{\pi^4}{90}.
$$

$\blacksquare$

### 习题三

（习题 13.3-4）利用 $f\left(x\right)=x^2$（$\lvert x\rvert\le\pi$）的傅里叶级数求 $\displaystyle\sum_{n=1}^\infty\frac{\left(-1\right)^{n+1}}{n^2}$ 及 $\displaystyle\sum_{n=1}^\infty\frac1{n^2}$.

### 解答 习题三

由第 13 章**命题**（傅里叶系数），$f\left(x\right)=x^2$ 为偶函数，其傅里叶级数为（见习题 13.2-1-1）

$$
x^2\sim\frac{\pi^2}{3}+4\sum_{n=1}^\infty\frac{\left(-1\right)^n}{n^2}\cos nx.
$$

由**定理 3.1**（狄利克雷收敛定理），在连续点等式成立.

取 $x=\pi$：$\pi^2=\frac{\pi^2}{3}+4\displaystyle\sum_{n=1}^\infty\frac{\left(-1\right)^n}{n^2}\cdot\left(-1\right)^n=\frac{\pi^2}{3}+4\sum\frac1{n^2}$，解得

$$
\sum_{n=1}^\infty\frac1{n^2}=\frac{\pi^2}{6}.
$$

取 $x=0$：$0=\frac{\pi^2}{3}+4\displaystyle\sum_{n=1}^\infty\frac{\left(-1\right)^n}{n^2}$，解得 $\displaystyle\sum_{n=1}^\infty\frac{\left(-1\right)^n}{n^2}=-\frac{\pi^2}{12}$，即

$$
\sum_{n=1}^\infty\frac{\left(-1\right)^{n+1}}{n^2}=\frac{\pi^2}{12}.
$$

$\blacksquare$
