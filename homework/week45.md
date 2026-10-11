# 作业 45

> **定理 4.1**（泰勒级数）若函数 $f\left(x\right)$ 在 $\left(x_0-R,x_0+R\right)$ 内可展开为幂级数 $f\left(x\right)=\sum_{n=0}^{\infty}a_n\left(x-x_0\right)^n$，则其系数必为
> $$a_n=\frac{f^{\left(n\right)}\left(x_0\right)}{n!},$$
> 即幂级数展开是唯一的，称为 $f$ 在 $x_0$ 处的泰勒级数.
>
> **定义**（基本展开式）在 $x=0$ 处有：$e^x=\sum_{n=0}^{\infty}\frac{x^n}{n!}$（$\left|x\right|<+\infty$）；$\ln\left(1+x\right)=\sum_{n=1}^{\infty}\frac{\left(-1\right)^{n-1}x^n}{n}$（$\left|x\right|<1$）；$\cos x=\sum_{n=0}^{\infty}\frac{\left(-1\right)^n x^{2n}}{\left(2n\right)!}$（$\left|x\right|<+\infty$）.

### 习题一

（习题 11.4-1-3）求 $f\left(x\right)=e^x$ 在 $x_0=3$ 处的幂级数展开式.

### 解答 习题一

由**定义**（基本展开式），$e^t=\sum_{n=0}^{\infty}\frac{t^n}{n!}$. 令 $t=x-3$，则

$$
e^x=e^3\cdot e^{x-3}=e^3\sum_{n=0}^{\infty}\frac{\left(x-3\right)^n}{n!}=\sum_{n=0}^{\infty}\frac{e^3}{n!}\left(x-3\right)^n,\  \left|x-3\right|<+\infty.
$$

由**定理 4.1**（泰勒级数），此即 $e^x$ 在 $x_0=3$ 处的泰勒展开式. $\blacksquare$

### 习题二

（习题 11.4-1-4）求 $f\left(x\right)=\ln x$ 在 $x_0=2$ 处的幂级数展开式.

### 解答 习题二

改写 $\ln x=\ln\bigl(2+\left(x-2\right)\bigr)=\ln 2+\ln\left(1+\frac{x-2}{2}\right)$. 由**定义**（基本展开式），

$$
\ln\left(1+t\right)=\sum_{n=1}^{\infty}\frac{\left(-1\right)^{n-1}t^n}{n},\  \left|t\right|<1.
$$

令 $t=\frac{x-2}{2}$，得

$$
\ln x=\ln 2+\sum_{n=1}^{\infty}\frac{\left(-1\right)^{n-1}}{n}\left(\frac{x-2}{2}\right)^n=\ln 2+\sum_{n=1}^{\infty}\frac{\left(-1\right)^{n-1}}{n\cdot 2^n}\left(x-2\right)^n,
$$

收敛范围为 $\left|\frac{x-2}{2}\right|<1$，即 $0<x<4$. $\blacksquare$

### 习题三

（习题 11.4-1-5）求 $f\left(x\right)=\cos^2 x$ 在 $x_0=0$ 处的幂级数展开式.

### 解答 习题三

利用半角公式 $\cos^2x=\frac{1+\cos 2x}{2}$. 由**定义**（基本展开式），

$$
\cos t=\sum_{n=0}^{\infty}\frac{\left(-1\right)^n t^{2n}}{\left(2n\right)!},\  \left|t\right|<+\infty.
$$

令 $t=2x$，得

$$
\cos^2x=\frac12+\frac12\cos 2x=\frac12+\frac12\sum_{n=0}^{\infty}\frac{\left(-1\right)^n\left(2x\right)^{2n}}{\left(2n\right)!}
=\frac12+\sum_{n=0}^{\infty}\frac{\left(-1\right)^n 2^{2n-1}}{\left(2n\right)!}x^{2n},
$$

收敛范围为 $\left|x\right|<+\infty$. $\blacksquare$

### 习题四

（习题 11.4-2）证明
$$
\sum_{n=0}^{\infty}\frac{x^n}{\left(n+1\right)!}=\frac{1}{x}\left(e^x-1\right),\  x\ne 0,
$$
并由此推出 $\sum_{n=1}^{\infty}\frac{n}{\left(n+1\right)!}=1$.

### 解答 习题四

由**定义**（基本展开式），$e^x=\sum_{n=0}^{\infty}\frac{x^n}{n!}$，故

$$
e^x-1=\sum_{n=1}^{\infty}\frac{x^n}{n!}=x\sum_{n=1}^{\infty}\frac{x^{n-1}}{n!}=x\sum_{n=0}^{\infty}\frac{x^n}{\left(n+1\right)!}.
$$

当 $x\ne 0$ 时，两边除以 $x$ 即得

$$
\sum_{n=0}^{\infty}\frac{x^n}{\left(n+1\right)!}=\frac{1}{x}\left(e^x-1\right).
$$

将上式两端对 $x$ 求导（由**定理 4.1** 及幂级数逐项求导的合法性），得

$$
\sum_{n=1}^{\infty}\frac{nx^{n-1}}{\left(n+1\right)!}=\frac{xe^x-\left(e^x-1\right)}{x^2}=\frac{e^x\left(x-1\right)+1}{x^2}.
$$

令 $x=1$，左端为 $\sum_{n=1}^{\infty}\frac{n}{\left(n+1\right)!}$，右端为 $e\left(0\right)+1=1$. 故

$$
\sum_{n=1}^{\infty}\frac{n}{\left(n+1\right)!}=1.
$$

$\blacksquare$

### 习题五

（习题 11.4-3）利用上题的结果，证明
$$
\sum_{n=1}^{\infty}\frac{n}{\left(n+2\right)!}=3-e.
$$

### 解答 习题五

将通项改写：

$$
\frac{n}{\left(n+2\right)!}=\frac{\left(n+2\right)-2}{\left(n+2\right)!}=\frac{1}{\left(n+1\right)!}-\frac{2}{\left(n+2\right)!}.
$$

于是

$$
\sum_{n=1}^{\infty}\frac{n}{\left(n+2\right)!}=\sum_{n=1}^{\infty}\frac{1}{\left(n+1\right)!}-2\sum_{n=1}^{\infty}\frac{1}{\left(n+2\right)!}.
$$

先算第一个和：$\sum_{n=1}^{\infty}\frac{1}{\left(n+1\right)!}=\sum_{m=2}^{\infty}\frac{1}{m!}=e-1-1=e-2$.

再算第二个和：$\sum_{n=1}^{\infty}\frac{1}{\left(n+2\right)!}=\sum_{m=3}^{\infty}\frac{1}{m!}=e-1-1-\frac12=e-\frac52$.

故

$$
\sum_{n=1}^{\infty}\frac{n}{\left(n+2\right)!}=\left(e-2\right)-2\left(e-\frac52\right)=e-2-2e+5=3-e.
$$

$\blacksquare$
