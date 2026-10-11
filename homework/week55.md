# 作业 55

> **定理 4.1**（贝塞尔不等式）设 $f\left(x\right)$ 在 $\left[-\pi,\pi\right]$ 上黎曼可积，其傅里叶系数为 $a_n,b_n$，则 $\frac{a_0^2}{2}+\displaystyle\sum_{n=1}^\infty\left(a_n^2+b_n^2\right)\le\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x$，特别地 $\displaystyle\sum_{n=1}^\infty a_n^2$ 与 $\displaystyle\sum_{n=1}^\infty b_n^2$ 均收敛.

> **定理 4.2**（封闭性方程/Parseval 等式）设 $f\left(x\right)$ 在 $\left[-\pi,\pi\right]$ 上黎曼可积且平方可积，则 $\frac1\pi\displaystyle\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x=\frac{a_0^2}{2}+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right)$.

### 习题一

（习题 13.4-1）设 $f\left(x\right)$ 在 $\left[-\pi,\pi\right]$ 上黎曼可积，且 $f\left(x\right)\sim\frac{a_0}{2}+\displaystyle\sum_{n=1}^\infty\left(a_n\cos nx+b_n\sin nx\right)$. 证明 $\displaystyle\sum_{n=1}^\infty\frac{a_n}{n}$ 及 $\displaystyle\sum_{n=1}^\infty\frac{b_n}{n}$ 收敛.

### 解答 习题一

由**定理 4.1**（贝塞尔不等式），$\displaystyle\sum_{n=1}^\infty\left(a_n^2+b_n^2\right)<\infty$. 又 $\displaystyle\sum_{n=1}^\infty\frac1{n^2}<\infty$. 由柯西-施瓦茨不等式，

$$
\sum_{n=1}^\infty\left\lvert\frac{a_n}{n}\right\rvert\le\left(\sum_{n=1}^\infty a_n^2\right)^{1/2}\left(\sum_{n=1}^\infty\frac1{n^2}\right)^{1/2}<\infty,
$$

故 $\sum\frac{a_n}{n}$ 绝对收敛. 同理 $\sum\frac{b_n}{n}$ 绝对收敛. $\blacksquare$

### 习题二

（习题 13.4-2）说明级数 $\frac{a_0}{2}+\displaystyle\sum_{n=1}^\infty\frac{1}{\ln n\cdot\ln\ln n}\cos nx$ 处处收敛，但不是任何在 $\left[-\pi,\pi\right]$ 上可积函数的傅里叶级数.

### 解答 习题二

**收敛性**：记 $a_n=\frac{1}{\ln n\cdot\ln\ln n}$. 数列 $\left\{a_n\right\}$ 单调递减趋于 $0$. 对任意固定 $x\not\equiv0\pmod{2\pi}$，部分和

$$
\sum_{n=1}^N\cos nx=\frac{\sin\left(Nx/2\right)\cos\left(\left(N+1\right)x/2\right)}{\sin\left(x/2\right)}
$$

关于 $N$ 有界. 由狄利克雷判别法，该级数处处收敛.

**不是傅里叶级数**：由习题 13.4-1，任何在 $\left[-\pi,\pi\right]$ 上可积函数的傅里叶级数都必须使 $\displaystyle\sum_{n=1}^\infty\frac{a_n}{n}$ 收敛. 而此处

$$
\sum_{n=1}^\infty\frac{a_n}{n}=\sum_{n=1}^\infty\frac{1}{n\ln n\cdot\ln\ln n}.
$$

由积分判别法，

$$
\int_3^{+\infty}\frac{\mathrm{d}x}{x\ln x\cdot\ln\ln x}
=\ln\ln\ln x\Big|_3^{+\infty}=+\infty,
$$

故 $\displaystyle\sum_{n=1}^\infty\frac{a_n}{n}$ 发散，不满足可积函数傅里叶系数的必要条件. 因而该级数不是任何在 $\left[-\pi,\pi\right]$ 上可积函数的傅里叶级数. $\blacksquare$

### 习题三

（习题 13.4-5）利用 $f\left(x\right)=x^2$（$\lvert x\rvert\le\pi$）的傅里叶级数的 Parseval 等式求和 $\displaystyle\sum_{n=1}^\infty\frac1{n^4}$.

### 解答 习题三

由习题 13.2-1-1，$x^2\sim\frac{\pi^2}{3}+4\displaystyle\sum_{n=1}^\infty\frac{\left(-1\right)^n}{n^2}\cos nx$，即 $a_0=\frac{2\pi^2}{3}$，$a_n=\frac{4\left(-1\right)^n}{n^2}$，$b_n=0$.

由**定理 4.2**（封闭性方程/Parseval 等式），

$$
\frac1\pi\int_{-\pi}^\pi x^4\,\mathrm{d}x=\frac{a_0^2}{2}+\sum_{n=1}^\infty a_n^2.
$$

左端 $=\frac{1}{\pi}\cdot\frac{2\pi^5}{5}=\frac{2\pi^4}{5}$；右端 $=\frac12\left(\frac{2\pi^2}{3}\right)^2+\displaystyle\sum_{n=1}^\infty\frac{16}{n^4}=\frac{2\pi^4}{9}+16\sum\frac1{n^4}$. 故

$$
16\sum_{n=1}^\infty\frac1{n^4}=2\pi^4\left(\frac15-\frac19\right)=\frac{8\pi^4}{45},\ \sum_{n=1}^\infty\frac1{n^4}=\frac{\pi^4}{90}.
$$

$\blacksquare$

### 习题四

（习题 13.4-7）利用函数 $f\left(x\right)=\begin{cases}x,&x\in\left[0,\pi\right];\\ -x,&x\in\left[-\pi,0\right)\end{cases}$（即 $f\left(x\right)=\lvert x\rvert$）的傅里叶级数的 Parseval 等式，求和 $\displaystyle\sum_{n=1}^\infty\frac{1}{\left(2n-1\right)^4}$.

### 解答 习题四

$f\left(x\right)=\lvert x\rvert$ 为偶函数，故 $b_n=0$. 计算傅里叶系数：

$$
a_0=\frac1\pi\int_{-\pi}^\pi\lvert x\rvert\,\mathrm{d}x=\frac{2}{\pi}\int_0^\pi x\,\mathrm{d}x=\pi,
$$

$$
a_n=\frac{2}{\pi}\int_0^\pi x\cos nx\,\mathrm{d}x=\frac{2}{\pi}\cdot\frac{\cos n\pi-1}{n^2}=\frac{2\bigl(\left(-1\right)^n-1\bigr)}{\pi n^2}.
$$

即 $n$ 为偶数时 $a_n=0$，$n$ 为奇数时 $a_n=-\frac{4}{\pi n^2}$.

由**定理 4.2**（封闭性方程/Parseval 等式），

$$
\frac1\pi\int_{-\pi}^\pi x^2\,\mathrm{d}x=\frac{a_0^2}{2}+\sum_{n=1}^\infty a_n^2.
$$

左端 $=\frac{2\pi^2}{3}$；右端 $=\frac{\pi^2}{2}+\displaystyle\sum_{n\text{ 奇}}\frac{16}{\pi^2 n^4}=\frac{\pi^2}{2}+\frac{16}{\pi^2}\sum_{n=1}^\infty\frac{1}{\left(2n-1\right)^4}$. 故

$$
\frac{16}{\pi^2}\sum_{n=1}^\infty\frac{1}{\left(2n-1\right)^4}=\frac{2\pi^2}{3}-\frac{\pi^2}{2}=\frac{\pi^2}{6},
$$

解得

$$
\sum_{n=1}^\infty\frac{1}{\left(2n-1\right)^4}=\frac{\pi^4}{96}.
$$

$\blacksquare$
