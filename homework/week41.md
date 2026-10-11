# 作业 41

> **定理 4.1**（无穷乘积与级数的关系）设 $p_n>0$（$n=1,2,\dots$），则无穷乘积 $\prod_{n=1}^{\infty}p_n$ 收敛的充要条件是级数 $\sum_{n=1}^{\infty}\ln p_n$ 收敛，且此时
> $$\prod_{n=1}^{\infty}p_n=\exp\left(\sum_{n=1}^{\infty}\ln p_n\right).$$
>
> **定理 4.2**（同号项无穷乘积）设 $\alpha_n\ge 0$（或 $\alpha_n\le 0$），则无穷乘积 $\prod_{n=1}^{\infty}\left(1+\alpha_n\right)$ 收敛的充要条件是级数 $\sum_{n=1}^{\infty}\alpha_n$ 收敛.
>
> **定理 4.4**（绝对收敛）设 $\alpha_n\ne -1$，则无穷乘积 $\prod_{n=1}^{\infty}\left(1+\alpha_n\right)$ 绝对收敛的充要条件是级数 $\sum_{n=1}^{\infty}\left|\alpha_n\right|$ 收敛.

### 习题一

（习题 10.4-1-2）讨论无穷乘积 $\prod_{n=2}^{\infty}\sqrt{\dfrac{n^2+1}{n^2-1}}$ 的收敛性.

### 解答 习题一

改写通项：

$$
\sqrt{\frac{n^2+1}{n^2-1}}=\left(1+\frac{2}{n^2-1}\right)^{1/2}.
$$

令 $\alpha_n=\dfrac{2}{n^2-1}>0$. 因 $\alpha_n\sim\dfrac{2}{n^2}$，而 $\sum\dfrac{1}{n^2}$ 为 $p=2>1$ 的 $p$ 级数，收敛，故由上一章**定理 2.3**（比较判别法的极限形式），$\sum\alpha_n$ 收敛. 由**定理 4.2**（同号项无穷乘积），$\prod\left(1+\alpha_n\right)$ 收敛. 再由**定理 4.1**，$\ln\sqrt{\left(n^2+1\right)/\left(n^2-1\right)}=\dfrac12\ln\left(1+\alpha_n\right)$ 所成级数收敛，故原无穷乘积收敛. $\blacksquare$

### 习题二

（习题 10.4-1-4）讨论无穷乘积 $\prod_{n=1}^{\infty}\left(1+\dfrac{x^n}{2^n}\right)$ 的收敛性.

### 解答 习题二

令 $\alpha_n=\dfrac{x^n}{2^n}=\left(\dfrac{x}{2}\right)^n$. 当 $\left|x\right|<2$ 时，$\left|x/2\right|<1$，$\sum\alpha_n$ 为收敛的等比级数，由**定理 4.2**（同号项无穷乘积），原无穷乘积收敛.

当 $\left|x\right|>2$ 时，$\left|\alpha_n\right|=\left|x/2\right|^n$ 不趋于零，从而 $\prod\left(1+\alpha_n\right)$ 的通项 $1+\alpha_n$ 不趋于 $1$，无穷乘积发散.

当 $x=2$ 时，$\alpha_n=1$，$1+\alpha_n=2$，部分乘积趋于 $+\infty$，发散. 当 $x=-2$ 时，$\alpha_n=\left(-1\right)^n$，$1+\alpha_n$ 交替为 $0$ 与 $2$，部分乘积为 $0$，不趋于非零有限极限，发散.

综上，原无穷乘积当且仅当 $x\in\left(-2,2\right)$ 时收敛. $\blacksquare$

### 习题三

（习题 10.4-1-6）讨论无穷乘积 $\prod_{n=1}^{\infty}\cos\dfrac{1}{n}$ 的收敛性.

### 解答 习题三

令 $p_n=\cos\dfrac1n>0$. 由**定理 4.1**，考察 $\sum\ln\cos\dfrac1n$. 当 $x\to 0$ 时，

$$
\ln\cos x=\ln\left(1-2\sin^2\left(x/2\right)\right)\sim -2\sin^2\left(x/2\right)\sim-\frac{x^2}{2}.
$$

故 $\ln\cos\dfrac1n\sim-\dfrac{1}{2n^2}$. 因 $\sum\dfrac{1}{n^2}$ 收敛，由上一章**定理 2.3**（比较判别法的极限形式），$\sum\ln\cos\dfrac1n$ 收敛. 由**定理 4.1**，原无穷乘积收敛. $\blacksquare$

### 习题四

（习题 10.4-1-8）讨论无穷乘积 $\prod_{n=1}^{\infty}\left(1+\dfrac{1}{\sqrt n}\right)$ 的收敛性.

### 解答 习题四

令 $\alpha_n=\dfrac{1}{\sqrt n}>0$. 因 $\sum\dfrac{1}{\sqrt n}$ 为 $p=\dfrac12<1$ 的 $p$ 级数，发散. 由**定理 4.2**（同号项无穷乘积），原无穷乘积发散. $\blacksquare$

### 习题五

（习题 10.4-2）设 $0<\alpha_n<\dfrac{\pi}{2}$，$\sum_{n=1}^{\infty}\alpha_n^2$ 收敛，证明 $\prod_{n=1}^{\infty}\cos\alpha_n$ 收敛.

### 解答 习题五

由**定理 4.1**，只须证明 $\sum\ln\cos\alpha_n$ 收敛. 当 $\alpha\to 0$ 时，

$$
\ln\cos\alpha=\ln\left(1-2\sin^2\left(\alpha/2\right)\right)\sim-2\sin^2\left(\alpha/2\right)\sim-\frac{\alpha^2}{2}.
$$

故

$$
\lim_{n\to\infty}\frac{\ln\cos\alpha_n}{\alpha_n^2}=-\frac12.
$$

由上一章**定理 2.3**（比较判别法的极限形式），$\sum\ln\cos\alpha_n$ 与 $\sum\alpha_n^2$ 同收敛. 由假设 $\sum\alpha_n^2$ 收敛，故 $\sum\ln\cos\alpha_n$ 收敛. 再由**定理 4.1**，$\prod\cos\alpha_n$ 收敛. $\blacksquare$

### 习题六

（习题 10.4-3）设 $\left|\alpha_n\right|<\dfrac{\pi}{4}$，且 $\sum_{n=1}^{\infty}\left|\alpha_n\right|$ 收敛，证明 $\prod_{n=1}^{\infty}\tan\left(\dfrac{\pi}{4}+\alpha_n\right)$ 绝对收敛.

### 解答 习题六

由**定理 4.4**，只须证明 $\sum\left|\tan\left(\dfrac{\pi}{4}+\alpha_n\right)-1\right|$ 收敛. 计算：

$$
\tan\left(\frac{\pi}{4}+\alpha_n\right)=\frac{1+\tan\alpha_n}{1-\tan\alpha_n},
$$

故

$$
\tan\left(\frac{\pi}{4}+\alpha_n\right)-1=\frac{2\tan\alpha_n}{1-\tan\alpha_n}.
$$

因 $\alpha_n\to 0$（由 $\sum\left|\alpha_n\right|$ 收敛），$\tan\alpha_n\sim\alpha_n$，且 $1-\tan\alpha_n\to 1$，从而

$$
\left|\tan\left(\frac{\pi}{4}+\alpha_n\right)-1\right|\sim 2\left|\alpha_n\right|.
$$

由上一章**定理 2.3**（比较判别法的极限形式），$\sum\left|\tan\left(\dfrac{\pi}{4}+\alpha_n\right)-1\right|$ 与 $\sum\left|\alpha_n\right|$ 同收敛. 由假设其收敛，故由**定理 4.4**，原无穷乘积绝对收敛. $\blacksquare$

### 习题七

（习题 10.4-5）设 $\alpha_n\ne -1$（$n=1,2,\dots$）. 证明：若 $\prod_{n=1}^{\infty}\left(1+\left|\alpha_n\right|\right)$ 收敛，则 $\prod_{n=1}^{\infty}\left(1+\alpha_n\right)$ 收敛.

### 解答 习题七

由 $\left|\alpha_n\right|\ge 0$ 及**定理 4.2**（同号项无穷乘积），$\prod\left(1+\left|\alpha_n\right|\right)$ 收敛蕴含 $\sum\left|\alpha_n\right|$ 收敛. 再由**定理 4.4**（绝对收敛），$\prod\left(1+\alpha_n\right)$ 绝对收敛，从而必收敛. $\blacksquare$
