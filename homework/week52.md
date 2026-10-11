# 作业 52

> **定义**（内积与范数）在 $R\left[-\pi,\pi\right]$ 中定义内积 $\left\langle f,g\right\rangle=\frac1\pi\displaystyle\int_{-\pi}^\pi f\left(x\right)g\left(x\right)\,\mathrm{d}x$，范数 $\lVert f\rVert=\sqrt{\left\langle f,f\right\rangle}=\left(\frac1\pi\displaystyle\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x\right)^{1/2}$.

> **命题**（三角函数系的正交性）三角函数系 $1,\cos x,\sin x,\cos2x,\sin2x,\cdots$ 在 $\left[-\pi,\pi\right]$ 上两两正交，即任意两个不同元素之积在 $\left[-\pi,\pi\right]$ 上的积分为 $0$；且 $\displaystyle\int_{-\pi}^\pi1\,\mathrm{d}x=2\pi$，$\displaystyle\int_{-\pi}^\pi\cos^2 nx\,\mathrm{d}x=\int_{-\pi}^\pi\sin^2 nx\,\mathrm{d}x=\pi\ \left(n=1,2,\cdots\right)$.

### 习题一

（习题 13.1-1）证明在本节中定义的内积 $\left\langle f,g\right\rangle$ 有下列性质：
(1) $\left\langle f,g\right\rangle=\left\langle g,f\right\rangle\ \left(\forall f,g\in R\left[-\pi,\pi\right]\right)$;

(2) $\forall\,\lambda,\mu\in\mathbb R$，及 $f,g,h\in R\left[-\pi,\pi\right]$ 都有 $\left\langle\lambda f+\mu g,h\right\rangle=\lambda\left\langle f,h\right\rangle+\mu\left\langle g,h\right\rangle$.

### 解答 习题一

（1）由**定义**（内积与范数）及乘积交换律，

$$
\left\langle f,g\right\rangle=\frac1\pi\int_{-\pi}^\pi f\left(x\right)g\left(x\right)\,\mathrm{d}x=\frac1\pi\int_{-\pi}^\pi g\left(x\right)f\left(x\right)\,\mathrm{d}x=\left\langle g,f\right\rangle.
$$

（2）由积分的线性性，

$$
\begin{aligned}
\left\langle\lambda f+\mu g,h\right\rangle
&=\frac1\pi\int_{-\pi}^\pi\left(\lambda f\left(x\right)+\mu g\left(x\right)\right)h\left(x\right)\,\mathrm{d}x\\
&=\lambda\cdot\frac1\pi\int_{-\pi}^\pi f\left(x\right)h\left(x\right)\,\mathrm{d}x+\mu\cdot\frac1\pi\int_{-\pi}^\pi g\left(x\right)h\left(x\right)\,\mathrm{d}x\\
&=\lambda\left\langle f,h\right\rangle+\mu\left\langle g,h\right\rangle.
\end{aligned}
$$

$\blacksquare$

### 习题二

（习题 13.1-2）设 $f,g\in R\left[-\pi,\pi\right]$ 是任意两个函数，证明 $\lvert\left\langle f,g\right\rangle\rvert\le\lVert f\rVert\cdot\lVert g\rVert$.

### 解答 习题二

对任意实数 $\lambda$，由范数的非负性 $\lVert f-\lambda g\rVert^2\ge0$. 展开：

$$
\lVert f-\lambda g\rVert^2=\left\langle f-\lambda g,f-\lambda g\right\rangle=\lVert f\rVert^2-2\lambda\left\langle f,g\right\rangle+\lambda^2\lVert g\rVert^2\ge0\ \left(\forall\lambda\in\mathbb R\right).
$$

这是关于 $\lambda$ 的二次三项式，恒非负，故其判别式不大于 $0$：

$$
4\left\langle f,g\right\rangle^2-4\lVert f\rVert^2\lVert g\rVert^2\le0,
$$

即 $\left\langle f,g\right\rangle^2\le\lVert f\rVert^2\lVert g\rVert^2$，开方得 $\lvert\left\langle f,g\right\rangle\rvert\le\lVert f\rVert\cdot\lVert g\rVert$. $\blacksquare$

### 习题三

（习题 13.1-3）设 $f\left(x\right)$ 与 $g\left(x\right)$ 在 $\left[-\pi,\pi\right]$ 中连续且不恒为零. 证明：当且仅当存在一个实数 $\lambda$，使得 $\lambda f\left(x\right)\equiv g\left(x\right)$ 时，$\displaystyle\left(\frac1\pi\int_{-\pi}^\pi f\left(x\right)g\left(x\right)\,\mathrm{d}x\right)^2=\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x\cdot\frac1\pi\int_{-\pi}^\pi g^2\left(x\right)\,\mathrm{d}x$.

### 解答 习题三

右端即 $\lVert f\rVert^2\lVert g\rVert^2$，左端即 $\left\langle f,g\right\rangle^2$，故要证等号成立当且仅当 $f,g$ 线性相关.

（$\Leftarrow$）若存在 $\lambda$ 使 $g\equiv\lambda f$，则

$$
\left\langle f,g\right\rangle=\left\langle f,\lambda f\right\rangle=\lambda\lVert f\rVert^2,\  \lVert g\rVert=\sqrt{\lambda^2\left\langle f,f\right\rangle}=\lvert\lambda\rvert\cdot\lVert f\rVert,
$$

于是 $\left\langle f,g\right\rangle^2=\lambda^2\lVert f\rVert^4=\lVert f\rVert^2\lVert g\rVert^2$，等号成立.

（$\Rightarrow$）若等号成立，即 $\left\langle f,g\right\rangle^2=\lVert f\rVert^2\lVert g\rVert^2$. 由习题二，二次三项式 $\lVert f\rVert^2\lambda^2-2\left\langle f,g\right\rangle\lambda+\lVert g\rVert^2$ 的判别式为 $0$，故存在二重根 $\lambda_0=\frac{\left\langle f,g\right\rangle}{\lVert f\rVert^2}$，使 $\lVert f-\lambda_0 g\rVert^2=0$. 因 $f,g$ 连续，$\displaystyle\int_{-\pi}^\pi\left(f\left(x\right)-\lambda_0 g\left(x\right)\right)^2\,\mathrm{d}x=0$ 推出 $f\left(x\right)-\lambda_0 g\left(x\right)\equiv0$，即 $f\equiv\lambda_0 g$. $\blacksquare$

### 习题四

（习题 13.1-7）设 $c_1+c_2\cos x+c_3\sin x\equiv0$，其中 $c_1,c_2,c_3$ 为常数. 利用三角函数系正交性证明 $c_1=c_2=c_3=0$，并将此结果推广成下列结论：函数系（1.2）中任意有穷个元素线性无关.

### 解答 习题四

在等式 $c_1+c_2\cos x+c_3\sin x\equiv0$ 两端分别乘以 $1,\cos x,\sin x$，再在 $\left[-\pi,\pi\right]$ 上积分. 由**命题**（三角函数系的正交性），交叉项积分均为 $0$，得

$$
\int_{-\pi}^\pi\left(c_1+c_2\cos x+c_3\sin x\right)\,\mathrm{d}x=2\pi c_1=0,
$$

$$
\int_{-\pi}^\pi\left(c_1+c_2\cos x+c_3\sin x\right)\cos x\,\mathrm{d}x=\pi c_2=0,
$$

$$
\int_{-\pi}^\pi\left(c_1+c_2\cos x+c_3\sin x\right)\sin x\,\mathrm{d}x=\pi c_3=0.
$$

故 $c_1=c_2=c_3=0$.

推广：设函数系 $1,\cos x,\sin x,\cos2x,\sin2x,\cdots$ 中有穷个元素的线性组合恒为零：

$$
\frac{a_0}{2}+\sum_{n=1}^N\left(a_n\cos nx+b_n\sin nx\right)\equiv0.
$$

两端同乘 $\cos mx$（$0\le m\le N$）或 $\sin mx$（$1\le m\le N$）并在 $\left[-\pi,\pi\right]$ 上积分. 由**命题**（三角函数系的正交性），除被乘项外其余各项积分均为 $0$，于是分别得 $2\pi a_0=0$、$\pi a_m=0$、$\pi b_m=0$，即所有系数均为 $0$. 故该函数系中任意有穷个元素线性无关. $\blacksquare$
