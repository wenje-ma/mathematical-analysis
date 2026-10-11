# 作业 53

> **命题**（傅里叶系数）以 $2\pi$ 为周期的可积函数 $f\left(x\right)$ 的傅里叶级数为 $f\left(x\right)\sim\frac{a_0}{2}+\displaystyle\sum_{n=1}^\infty\left(a_n\cos nx+b_n\sin nx\right)$，其中

$$
a_n=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\cos nx\,\mathrm{d}x\ \left(n=0,1,2,\cdots\right),\  b_n=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\sin nx\,\mathrm{d}x\ \left(n=1,2,\cdots\right).
$$

### 习题一

（习题 13.2-1-1）设 $y=f\left(x\right)$ 是以 $2\pi$ 为周期的函数，在 $\left[-\pi,\pi\right]$ 中 $f\left(x\right)=x^2$. 试求出 $f\left(x\right)$ 的傅里叶级数.

### 解答 习题一

$f\left(x\right)=x^2$ 为偶函数，故 $b_n=0$. 由**命题**（傅里叶系数），

$$
a_0=\frac1\pi\int_{-\pi}^\pi x^2\,\mathrm{d}x=\frac{2}{\pi}\cdot\frac{\pi^3}{3}=\frac{2\pi^2}{3},
$$

$$
a_n=\frac1\pi\int_{-\pi}^\pi x^2\cos nx\,\mathrm{d}x=\frac{2}{\pi}\int_0^\pi x^2\cos nx\,\mathrm{d}x.
$$

分部积分：$\displaystyle\int_0^\pi x^2\cos nx\,\mathrm{d}x=\left[\frac{x^2\sin nx}{n}\right]_0^\pi-\frac{2}{n}\int_0^\pi x\sin nx\,\mathrm{d}x$，而 $\displaystyle\int_0^\pi x\sin nx\,\mathrm{d}x=-\frac{\pi\cos n\pi}{n}=\frac{\pi\left(-1\right)^{n+1}}{n}$. 故

$$
a_n=\frac{2}{\pi}\cdot\left(-\frac{2}{n}\right)\cdot\frac{\pi\left(-1\right)^{n+1}}{n}=\frac{4\left(-1\right)^n}{n^2}.
$$

于是

$$
x^2\sim\frac{\pi^2}{3}+4\sum_{n=1}^\infty\frac{\left(-1\right)^n}{n^2}\cos nx.
$$

$\blacksquare$

### 习题二

（习题 13.2-1-3）设 $y=f\left(x\right)$ 是以 $2\pi$ 为周期的函数，在 $\left[-\pi,\pi\right]$ 中 $f\left(x\right)=\sin^4 x$. 试求出 $f\left(x\right)$ 的傅里叶级数.

### 解答 习题二

利用三角恒等变换：

$$
\sin^4 x=\left(\sin^2 x\right)^2=\left(\frac{1-\cos2x}{2}\right)^2=\frac{1-2\cos2x+\cos^2 2x}{4}=\frac{3}{8}-\frac12\cos2x+\frac18\cos4x.
$$

这已是三角多项式，由**命题**（傅里叶系数）直接读出其傅里叶系数：$a_0=\frac{3\pi}{2}$（即常数项 $\frac{a_0}{2}=\frac38$），$a_2=-\frac12$，$a_4=\frac18$，其余 $a_n=b_n=0$. 故

$$
\sin^4 x=\frac38-\frac12\cos2x+\frac18\cos4x.
$$

$\blacksquare$

### 习题三

（习题 13.2-1-5）设 $y=f\left(x\right)$ 是以 $2\pi$ 为周期的函数，在 $\left[-\pi,\pi\right]$ 中 $f\left(x\right)=\begin{cases}0,&-\pi\le x<0;\\ x,&0\le x\le\pi.\end{cases}$ 试求出 $f\left(x\right)$ 的傅里叶级数.

### 解答 习题三

由**命题**（傅里叶系数），

$$
a_0=\frac1\pi\int_0^\pi x\,\mathrm{d}x=\frac{\pi}{2},
$$

$$
a_n=\frac1\pi\int_0^\pi x\cos nx\,\mathrm{d}x=\frac1\pi\left(\left[\frac{x\sin nx}{n}\right]_0^\pi-\frac1n\int_0^\pi\sin nx\,\mathrm{d}x\right)=\frac{\left(-1\right)^n-1}{n^2\pi},
$$

即 $n$ 为偶数时 $a_n=0$，$n$ 为奇数时 $a_n=-\frac{2}{n^2\pi}$. 又

$$
b_n=\frac1\pi\int_0^\pi x\sin nx\,\mathrm{d}x=\frac1\pi\left(\left[-\frac{x\cos nx}{n}\right]_0^\pi+\frac1n\int_0^\pi\cos nx\,\mathrm{d}x\right)=\frac{\left(-1\right)^{n+1}}{n}.
$$

故

$$
f\left(x\right)\sim\frac{\pi}{4}-\frac{2}{\pi}\sum_{k=0}^\infty\frac{\cos\left(2k+1\right)x}{\left(2k+1\right)^2}+\sum_{n=1}^\infty\frac{\left(-1\right)^{n+1}}{n}\sin nx.
$$

$\blacksquare$

### 习题四

（习题 13.2-7）设 $y=f\left(x\right)$ 在 $\left[-\pi,\pi\right]$ 中满足下列条件：
(i) $f\left(x+\pi\right)=f\left(x\right)$，

或 (ii) $f\left(x+\pi\right)=-f\left(x\right)$.
证明在条件 (i) 下，$a_{2n-1}=b_{2n-1}=0\ \left(n=1,2,\cdots\right)$，而在条件 (ii) 下，$a_{2n}=b_{2n}=0\ \left(n=1,2,\cdots\right)$.

### 解答 习题四

将系数积分拆为 $\left[-\pi,0\right]$ 与 $\left[0,\pi\right]$ 两段. 在第一段中作代换 $x=t-\pi$，则

$$
\int_{-\pi}^0 f\left(x\right)\cos nx\,\mathrm{d}x=\int_0^\pi f\left(t-\pi\right)\cos\left(n\left(t-\pi\right)\right)\,\mathrm{d}t=\cos n\pi\int_0^\pi f\left(t-\pi\right)\cos nt\,\mathrm{d}t,
$$

其中用到 $\cos\left(n\left(t-\pi\right)\right)=\left(-1\right)^n\cos nt$（$\sin n\pi=0$）. 同理对 $\sin nx$ 有相同代换.

**条件 (i)** $f\left(t-\pi\right)=f\left(t\right)$：

$$
a_n=\frac1\pi\bigl[\left(-1\right)^n+1\bigr]\int_0^\pi f\left(t\right)\cos nt\,\mathrm{d}t,\  b_n=\frac1\pi\bigl[\left(-1\right)^n+1\bigr]\int_0^\pi f\left(t\right)\sin nt\,\mathrm{d}t.
$$

当 $n$ 为奇数时 $\left(-1\right)^n+1=0$，故 $a_n=b_n=0$，即 $a_{2n-1}=b_{2n-1}=0$.

**条件 (ii)** $f\left(t-\pi\right)=-f\left(t\right)$：

$$
a_n=\frac1\pi\bigl[1-\left(-1\right)^n\bigr]\int_0^\pi f\left(t\right)\cos nt\,\mathrm{d}t,\  b_n=\frac1\pi\bigl[1-\left(-1\right)^n\bigr]\int_0^\pi f\left(t\right)\sin nt\,\mathrm{d}t.
$$

当 $n$ 为偶数时 $1-\left(-1\right)^n=0$，故 $a_n=b_n=0$，即 $a_{2n}=b_{2n}=0$. $\blacksquare$
