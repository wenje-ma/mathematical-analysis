# 作业 46

> **定义**（无穷积分的收敛）设函数 $f\left(x\right)$ 在 $\left[a,+\infty\right)$ 上有定义，且在任意闭区间 $\left[a,A\right]$ 上可积. 若极限 $\lim_{A\to+\infty}\int_a^A f\left(x\right)\,\mathrm{d}x$ 存在，则称无穷积分 $\int_a^{+\infty} f\left(x\right)\,\mathrm{d}x$ 收敛，并把这个极限定义为该无穷积分的值；否则称其发散.

> **例 1.2**（$p$-积分）无穷积分 $\int_1^{+\infty}\frac{\mathrm{d}x}{x^p}$ 当 $p>1$ 时收敛，当 $p\le 1$ 时发散.

> **定理 1.1**（无穷积分的柯西收敛原理）设 $f\left(x\right)$ 在 $\left[a,+\infty\right)$ 上有定义，且在任意闭区间 $\left[a,A\right]$ 上可积. 则 $\int_a^{+\infty} f\left(x\right)\,\mathrm{d}x$ 收敛的充要条件是：对任意给定的 $\varepsilon>0$，存在 $X>0$，使得 $\bigl\lvert\int_{A'}^{A''} f\left(x\right)\,\mathrm{d}x\bigr\rvert<\varepsilon$，只要 $A'>X,\ A''>X$.

> **定理 1.3**（比较判别法）设 $f\left(x\right)$ 及 $g\left(x\right)$ 在 $\left[a,+\infty\right)$ 上有定义，且在任意闭区间 $\left[a,A\right]$ 上可积. 又设存在 $X_0>a$，使得 $0\le f\left(x\right)\le g\left(x\right)\ \left(\forall x\ge X_0\right)$. 则若 $\int_a^{+\infty}g\left(x\right)\,\mathrm{d}x$ 收敛，必有 $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ 收敛；若 $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ 发散，必有 $\int_a^{+\infty}g\left(x\right)\,\mathrm{d}x$ 发散.

> **定理 1.6**（狄利克雷判别法）设 $f\left(x\right)$ 与 $g\left(x\right)$ 在 $\left[a,+\infty\right)$ 上有定义，且在任意区间 $\left[a,A\right]$ 上可积. 若 $f\left(x\right)$ 在 $\left[a,+\infty\right)$ 上单调，且 $\lim_{x\to+\infty}f\left(x\right)=0$；又对任意 $A>a$，积分 $\int_a^A g\left(x\right)\,\mathrm{d}x$ 有界，则无穷积分 $\int_a^{+\infty}f\left(x\right)g\left(x\right)\,\mathrm{d}x$ 收敛.

> **定义**（绝对收敛与条件收敛）若 $\int_a^{+\infty}\bigl\lvert f\left(x\right)\bigr\rvert\,\mathrm{d}x$ 收敛，则称无穷积分 $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ 绝对收敛；若 $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ 收敛，但 $\int_a^{+\infty}\bigl\lvert f\left(x\right)\bigr\rvert\,\mathrm{d}x$ 发散，则称其为条件收敛.

### 习题一

（习题 12.1-1-1）判别无穷积分 $\displaystyle\int_1^{+\infty}\frac{\ln x}{x^2}\,\mathrm{d}x$ 是否收敛，如果收敛，求出其值.

### 解答 习题一

对任意 $A>1$，分部积分（取 $u=\ln x,\ \mathrm{d}v=\frac{\mathrm{d}x}{x^2}$）得

$$
\int_1^A \frac{\ln x}{x^2}\,\mathrm{d}x=\left[-\frac{\ln x}{x}\right]_1^A+\int_1^A\frac{\mathrm{d}x}{x^2}=-\frac{\ln A}{A}+1-\frac1A.
$$

由 $\lim_{A\to+\infty}\frac{\ln A}{A}=0$ 及 $\frac1A\to0$，上式右端趋于 $1$. 故由**定义**（无穷积分的收敛），该无穷积分收敛，其值为 $1$. $\blacksquare$

### 习题二

（习题 12.1-1-2）判别无穷积分 $\displaystyle\int_1^{+\infty} e^{-ax}\,\mathrm{d}x$（$a>0$）是否收敛，如果收敛，求出其值.

### 解答 习题二

对任意 $A>1$，

$$
\int_1^A e^{-ax}\,\mathrm{d}x=\left[-\frac{e^{-ax}}{a}\right]_1^A=\frac{e^{-a}-e^{-aA}}{a}.
$$

因 $a>0$，故 $e^{-aA}\to0\ \left(A\to+\infty\right)$，上式右端趋于 $\frac{e^{-a}}{a}$. 故由**定义**（无穷积分的收敛），该无穷积分收敛，其值为 $\frac{e^{-a}}{a}$. $\blacksquare$

### 习题三

（习题 12.1-1-3）判别无穷积分 $\displaystyle\int_0^{+\infty}\frac{\mathrm{d}x}{1+x^2}$ 是否收敛，如果收敛，求出其值.

### 解答 习题三

对任意 $A>0$，

$$
\int_0^A\frac{\mathrm{d}x}{1+x^2}=\bigl[\arctan x\bigr]_0^A=\arctan A.
$$

当 $A\to+\infty$ 时 $\arctan A\to\frac{\pi}{2}$. 故由**定义**（无穷积分的收敛），该无穷积分收敛，其值为 $\frac{\pi}{2}$. $\blacksquare$

### 习题四

（习题 12.1-1-4）判别无穷积分 $\displaystyle\int_0^{+\infty}x e^{-x}\,\mathrm{d}x$ 是否收敛，如果收敛，求出其值.

### 解答 习题四

对任意 $A>0$，分部积分（取 $u=x,\ \mathrm{d}v=e^{-x}\,\mathrm{d}x$）得

$$
\int_0^A x e^{-x}\,\mathrm{d}x=\bigl[-x e^{-x}\bigr]_0^A+\int_0^A e^{-x}\,\mathrm{d}x=-A e^{-A}+1-e^{-A}.
$$

当 $A\to+\infty$ 时 $A e^{-A}\to0$，$e^{-A}\to0$，上式右端趋于 $1$. 故由**定义**（无穷积分的收敛），该无穷积分收敛，其值为 $1$. $\blacksquare$

### 习题五

（习题 12.1-2-1）讨论无穷积分 $\displaystyle\int_1^{+\infty}\frac{\sin x}{x^p}\,\mathrm{d}x$ 的绝对收敛性与条件收敛性.

### 解答 习题五

分三种情形讨论.

（1）$p>1$. 因 $\bigl\lvert\frac{\sin x}{x^p}\bigr\rvert\le\frac1{x^p}$，而由**例 1.2**（$p$-积分），$\int_1^{+\infty}\frac{\mathrm{d}x}{x^p}$ 收敛. 由**定理 1.3**（比较判别法），$\int_1^{+\infty}\bigl\lvert\frac{\sin x}{x^p}\bigr\rvert\,\mathrm{d}x$ 收敛，故原无穷积分绝对收敛.

（2）$0<p\le1$. 首先，$f\left(x\right)=\frac1{x^p}$ 在 $\left[1,+\infty\right)$ 上单调递减且趋于 $0$；而对任意 $A>1$，$\bigl\lvert\int_1^A\sin x\,\mathrm{d}x\bigr\rvert=\bigl\lvert\cos1-\cos A\bigr\rvert\le2$ 有界. 由**定理 1.6**（狄利克雷判别法），$\int_1^{+\infty}\frac{\sin x}{x^p}\,\mathrm{d}x$ 收敛.

其次，它不绝对收敛. 事实上，

$$
\frac{\bigl\lvert\sin x\bigr\rvert}{x^p}\ge\frac{\sin^2 x}{x^p}=\frac{1-\cos2x}{2x^p}=\frac{1}{2x^p}-\frac{\cos2x}{2x^p}.
$$

由**例 1.2**（$p$-积分），$\int_1^{+\infty}\frac{\mathrm{d}x}{x^p}$ 当 $p\le1$ 时发散；而 $\int_1^{+\infty}\frac{\cos2x}{2x^p}\,\mathrm{d}x$ 由**定理 1.6**（狄利克雷判别法）收敛（$\frac1{x^p}$ 单调趋于 $0$，$\int_1^A\cos2x\,\mathrm{d}x$ 有界）. 故 $\int_1^{+\infty}\bigl\lvert\frac{\sin x}{x^p}\bigr\rvert\,\mathrm{d}x$ 发散. 由**定义**（绝对收敛与条件收敛），原无穷积分条件收敛.

（3）$p\le0$. 此时 $x^{-p}\ge1\ \left(x\ge1\right)$. 取 $A'_n=2n\pi-\frac{\pi}{4}$，$A''_n=2n\pi+\frac{\pi}{4}$，则在 $\left[A'_n,A''_n\right]$ 上 $\sin x\ge\frac{\sqrt2}{2}$，从而

$$
\biggl\lvert\int_{A'_n}^{A''_n}\frac{\sin x}{x^p}\,\mathrm{d}x\biggr\rvert\ge\frac{\sqrt2}{2}\cdot\frac{\pi}{2}=\frac{\sqrt2\pi}{4}>0,
$$

该下界为与 $n$ 无关的正常数，不随 $A'_n,A''_n\to+\infty$ 而趋于 $0$. 由**定理 1.1**（柯西收敛原理），原无穷积分发散. $\blacksquare$

### 习题六

（习题 12.1-2-3）讨论无穷积分 $\displaystyle\int_1^{+\infty}\frac{\sqrt x\cos x}{x+3}\,\mathrm{d}x$ 的绝对收敛性与条件收敛性.

### 解答 习题六

令 $f\left(x\right)=\frac{\sqrt x}{x+3}$. 当 $x>3$ 时，

$$
f'\left(x\right)=\frac{\left(x+3\right)-2x}{2\sqrt x\,\left(x+3\right)^2}=\frac{3-x}{2\sqrt x\,\left(x+3\right)^2}<0,
$$

故 $f\left(x\right)$ 在 $\left[3,+\infty\right)$ 上单调递减；又 $f\left(x\right)\sim\frac1{\sqrt x}\to0\ \left(x\to+\infty\right)$. 而对任意 $A>1$，$\bigl\lvert\int_1^A\cos x\,\mathrm{d}x\bigr\rvert=\bigl\lvert\sin A-\sin1\bigr\rvert\le2$ 有界. 由**定理 1.6**（狄利克雷判别法），原无穷积分收敛.

其次，它不绝对收敛. 对 $x\ge1$，$x+3\le4x$，故 $f\left(x\right)=\frac{\sqrt x}{x+3}\ge\frac1{4\sqrt x}$，于是

$$
\frac{\sqrt x\,\bigl\lvert\cos x\bigr\rvert}{x+3}\ge\frac{\bigl\lvert\cos x\bigr\rvert}{4\sqrt x}\ge\frac{\cos^2 x}{4\sqrt x}=\frac{1}{8\sqrt x}+\frac{\cos2x}{8\sqrt x}.
$$

由**例 1.2**（$p$-积分），$\int_1^{+\infty}\frac{\mathrm{d}x}{\sqrt x}$ 发散（$p=\frac12\le1$）；而 $\int_1^{+\infty}\frac{\cos2x}{8\sqrt x}\,\mathrm{d}x$ 由**定理 1.6**（狄利克雷判别法）收敛. 故 $\int_1^{+\infty}\frac{\sqrt x\,\bigl\lvert\cos x\bigr\rvert}{x+3}\,\mathrm{d}x$ 发散. 由**定义**（绝对收敛与条件收敛），原无穷积分条件收敛. $\blacksquare$

### 习题七

（习题 12.1-2-5）讨论无穷积分 $\displaystyle\int_0^{+\infty}\sin x^2\,\mathrm{d}x$ 的绝对收敛性与条件收敛性.

### 解答 习题七

在 $\left[0,1\right]$ 上 $\sin x^2\sim x^2$，是可积的. 对 $\left[1,+\infty\right)$ 作代换 $t=x^2$，则 $\mathrm{d}x=\frac{\mathrm{d}t}{2\sqrt t}$，于是

$$
\int_1^{+\infty}\sin x^2\,\mathrm{d}x=\frac12\int_1^{+\infty}\frac{\sin t}{\sqrt t}\,\mathrm{d}t.
$$

函数 $\frac1{\sqrt t}$ 在 $\left[1,+\infty\right)$ 上单调递减且趋于 $0$，而 $\int_1^B\sin t\,\mathrm{d}t=\cos1-\cos B$ 有界. 由**定理 1.6**（狄利克雷判别法），右端积分收敛，故原无穷积分收敛.

其次，它不绝对收敛. 同样代换得

$$
\int_1^{+\infty}\bigl\lvert\sin x^2\bigr\rvert\,\mathrm{d}x=\frac12\int_1^{+\infty}\frac{\bigl\lvert\sin t\bigr\rvert}{\sqrt t}\,\mathrm{d}t,
$$

而 $\bigl\lvert\sin t\bigr\rvert/\sqrt t\ge\sin^2 t/\sqrt t=\frac{1}{2\sqrt t}-\frac{\cos2t}{2\sqrt t}$，其中 $\int_1^{+\infty}\frac{\mathrm{d}t}{\sqrt t}$ 由**例 1.2**（$p$-积分）发散，$\int_1^{+\infty}\frac{\cos2t}{2\sqrt t}\,\mathrm{d}t$ 由**定理 1.6**收敛. 故右端积分发散，原无穷积分不绝对收敛. 由**定义**（绝对收敛与条件收敛），原无穷积分条件收敛. $\blacksquare$

### 习题八

（习题 12.1-3）令 $\displaystyle I_1\left(x\right)=\int_0^{+\infty}e^{-xt}\sin t\,\mathrm{d}t,\ I_2\left(x\right)=\int_0^{+\infty}e^{-xt}\cos t\,\mathrm{d}t$，其中 $x\in\left(0,+\infty\right)$. 证明这两个无穷积分绝对收敛，并求出其值.

### 解答 习题八

先证绝对收敛. 对 $t\ge0$ 有 $\bigl\lvert e^{-xt}\sin t\bigr\rvert\le e^{-xt}$，$\bigl\lvert e^{-xt}\cos t\bigr\rvert\le e^{-xt}$，而

$$
\int_0^{+\infty}e^{-xt}\,\mathrm{d}x=\lim_{A\to+\infty}\frac{1-e^{-xA}}{x}=\frac1x
$$

收敛. 由**定理 1.3**（比较判别法），$I_1\left(x\right)$ 与 $I_2\left(x\right)$ 均绝对收敛.

再求其值. 对 $I_2$ 分部积分（取 $u=\cos t,\ \mathrm{d}v=e^{-xt}\,\mathrm{d}t$），注意到 $e^{-xt}\cos t\big|_{0}^{+\infty}=0-\left(-\frac1x\right)=\frac1x$，得

$$
I_2\left(x\right)=\frac1x-\frac1x I_1\left(x\right).
$$

对 $I_1$ 分部积分（取 $u=\sin t,\ \mathrm{d}v=e^{-xt}\,\mathrm{d}t$），注意 $e^{-xt}\sin t\big|_0^{+\infty}=0$，得

$$
I_1\left(x\right)=\frac1x I_2\left(x\right).
$$

将第二式代入第一式：$I_2=\frac1x-\frac1{x}\cdot\frac{I_2}{x}$，即 $\left(1+\frac1{x^2}\right)I_2=\frac1x$，解得 $I_2\left(x\right)=\frac{x}{x^2+1}$，再代回得 $I_1\left(x\right)=\frac1{x^2+1}$. 故

$$
I_1\left(x\right)=\frac{1}{x^2+1},\  I_2\left(x\right)=\frac{x}{x^2+1}.
$$

$\blacksquare$

### 习题九

（习题 12.1-4）设 $f\left(x\right)$ 在 $\left(-\infty,+\infty\right)$ 上连续，且 $\displaystyle\int_{-\infty}^{+\infty}f\left(x\right)\,\mathrm{d}x$ 收敛. 证明：
(1) $\displaystyle\int_{-\infty}^{+\infty}f\left(-x\right)\,\mathrm{d}x=\int_{-\infty}^{+\infty}f\left(x\right)\,\mathrm{d}x$;

(2) $\displaystyle\int_{-\infty}^{+\infty}f\left(x+a\right)\,\mathrm{d}x=\int_{-\infty}^{+\infty}f\left(x\right)\,\mathrm{d}x\ \left(a\in\mathbb R\right)$.

### 解答 习题九

（1）作代换 $u=-x$，则 $\mathrm{d}x=-\mathrm{d}u$，于是

$$
\int_{-B}^{A}f\left(-x\right)\,\mathrm{d}x=\int_{B}^{-A}f\left(u\right)\left(-\mathrm{d}u\right)=\int_{-A}^{B}f\left(u\right)\,\mathrm{d}u.
$$

令 $A,B\to+\infty$，由**定义**（无穷积分的收敛）及 $\int_{-\infty}^{+\infty}f\left(u\right)\,\mathrm{d}u$ 的收敛性，右端趋于 $\int_{-\infty}^{+\infty}f\left(u\right)\,\mathrm{d}u$，左端趋于 $\int_{-\infty}^{+\infty}f\left(-x\right)\,\mathrm{d}x$，故两者相等.

（2）作代换 $u=x+a$，则 $\mathrm{d}x=\mathrm{d}u$，于是

$$
\int_{-B}^{A}f\left(x+a\right)\,\mathrm{d}x=\int_{a-B}^{a+A}f\left(u\right)\,\mathrm{d}u.
$$

令 $A,B\to+\infty$，积分上下限分别独立趋于 $+\infty$ 与 $-\infty$，由所设无穷积分收敛，右端趋于 $\int_{-\infty}^{+\infty}f\left(u\right)\,\mathrm{d}u$. 故 $\int_{-\infty}^{+\infty}f\left(x+a\right)\,\mathrm{d}x=\int_{-\infty}^{+\infty}f\left(x\right)\,\mathrm{d}x$. $\blacksquare$

### 习题十

（习题 12.1-5）设 $f\left(x\right)$ 在 $\left[1,+\infty\right)$ 上有定义，并在任意区间 $\left[1,A\right]$ 上可积，假定 $\lim_{x\to+\infty}f\left(x\right)=0$，并令 $a_n=\displaystyle\int_n^{n+1}f\left(x\right)\,\mathrm{d}x,\ n=1,2,\cdots$. 证明 $\displaystyle\int_1^{+\infty}f\left(x\right)\,\mathrm{d}x$ 收敛的充要条件是 $\displaystyle\sum_{n=1}^{\infty}a_n$ 收敛.

### 解答 习题十

记 $F\left(A\right)=\int_1^A f\left(x\right)\,\mathrm{d}x$. 对任意正整数 $N$，有

$$
\sum_{n=1}^{N}a_n=\sum_{n=1}^{N}\int_n^{n+1}f\left(x\right)\,\mathrm{d}x=\int_1^{N+1}f\left(x\right)\,\mathrm{d}x=F\left(N+1\right).
$$

（$\Rightarrow$）若 $\int_1^{+\infty}f\left(x\right)\,\mathrm{d}x$ 收敛，即 $F\left(A\right)\to L\ \left(A\to+\infty\right)$，则 $F\left(N+1\right)\to L$，亦即级数 $\sum_{n=1}^{\infty}a_n$ 收敛，其和为 $L$.

（$\Leftarrow$）若 $\sum_{n=1}^{\infty}a_n$ 收敛，即 $F\left(N+1\right)\to L\ \left(N\to+\infty\right)$. 现证 $F\left(A\right)\to L$ 对任意 $A\to+\infty$ 成立. 对任意 $A\ge1$，取 $N=\left[A\right]$，则 $N\le A<N+1$，于是

$$
F\left(A\right)-L=\bigl(F\left(N+1\right)-L\bigr)+\bigl(F\left(A\right)-F\left(N+1\right)\bigr)=\bigl(F\left(N+1\right)-L\bigr)-\int_A^{N+1}f\left(x\right)\,\mathrm{d}x.
$$

由 $f\left(x\right)\to0\ \left(x\to+\infty\right)$，对任意 $\varepsilon>0$，存在 $X>0$，使当 $x>X$ 时 $\bigl\lvert f\left(x\right)\bigr\rvert<\varepsilon$. 当 $N$ 充分大时 $\left[A,N+1\right]\subset\left[X,+\infty\right)$，故

$$
\biggl\lvert\int_A^{N+1}f\left(x\right)\,\mathrm{d}x\biggr\rvert\le\int_A^{N+1}\bigl\lvert f\left(x\right)\bigr\rvert\,\mathrm{d}x<\varepsilon\,\left(N+1-A\right)\le\varepsilon.
$$

同时 $F\left(N+1\right)-L\to0$. 因此 $F\left(A\right)-L\to0$，即 $F\left(A\right)\to L$. 由**定义**（无穷积分的收敛），$\int_1^{+\infty}f\left(x\right)\,\mathrm{d}x$ 收敛. $\blacksquare$
