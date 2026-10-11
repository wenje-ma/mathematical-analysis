# 作业 38

> **定义**（级数收敛）给定数列 $\left\{a_n\right\}$，作部分和 $S_n=\sum_{k=1}^{n}a_k$. 若 $\lim_{n\to\infty}S_n=S$ 存在且有限，则称级数 $\sum_{n=1}^{\infty}a_n$ 收敛，$S$ 称为其和；否则称级数发散.
>
> **定理 1.1**（收敛级数的必要条件）若级数 $\sum_{n=1}^{\infty}a_n$ 收敛，则 $\lim_{n\to\infty}a_n=0$.

### 习题一

（习题 10.1-1）证明等比级数
$$
a_0+a_0q+a_0q^2+\cdots+a_0q^n+\cdots\ \left(a_0\ne 0\right)
$$
当 $\left|q\right|<1$ 时收敛，且有 $a_0+a_0q+\cdots=\frac{a_0}{1-q}$. 当 $\left|q\right|\ge 1$ 时上述级数发散.

### 解答 习题一

该级数的前 $n+1$ 项部分和为

$$
S_n=a_0+a_0q+\cdots+a_0q^n=a_0\cdot\frac{1-q^{n+1}}{1-q},\  q\ne 1.
$$

当 $\left|q\right|<1$ 时，$\lim_{n\to\infty}q^{n+1}=0$，故由**定义**（级数收敛），

$$
\lim_{n\to\infty}S_n=\frac{a_0}{1-q},
$$

级数收敛且其和为 $\frac{a_0}{1-q}$.

当 $q=1$ 时，$S_n=a_0\left(n+1\right)\to\infty$（$a_0\ne 0$），级数发散. 当 $q=-1$ 时，$S_n$ 在 $a_0$ 与 $0$ 之间摆动，不收敛. 当 $\left|q\right|>1$ 时，通项 $a_0q^n$ 不趋于 $0$，由**定理 1.1**（收敛级数的必要条件），级数发散. $\blacksquare$

### 习题二

（习题 10.1-2-1）讨论级数 $\sum_{n=1}^{+\infty}\bigl(\sqrt{n+1}-\sqrt{n}\bigr)$ 的收敛性或发散性.

### 解答 习题二

其部分和为

$$
S_N=\sum_{n=1}^{N}\bigl(\sqrt{n+1}-\sqrt{n}\bigr)=\sqrt{N+1}-1.
$$

当 $N\to\infty$ 时 $S_N\to+\infty$，极限不存在有限值，故由**定义**（级数收敛），该级数发散. $\blacksquare$

### 习题三

（习题 10.1-2-2）讨论级数 $\sum_{n=1}^{+\infty}\frac{1}{\left(2n-1\right)\left(2n+1\right)}$ 的收敛性或发散性.

### 解答 习题三

注意到

$$
\frac{1}{\left(2n-1\right)\left(2n+1\right)}=\frac{1}{2}\left(\frac{1}{2n-1}-\frac{1}{2n+1}\right),
$$

故部分和为

$$
S_N=\frac{1}{2}\sum_{n=1}^{N}\left(\frac{1}{2n-1}-\frac{1}{2n+1}\right)=\frac{1}{2}\left(1-\frac{1}{2N+1}\right).
$$

当 $N\to\infty$ 时 $S_N\to\frac{1}{2}$，故由**定义**（级数收敛），该级数收敛，其和为 $\frac{1}{2}$. $\blacksquare$

### 习题四

（习题 10.1-2-3）讨论级数 $\sum_{n=1}^{+\infty}\ln\frac{n}{n+5}$ 的收敛性或发散性.

### 解答 习题四

通项为 $\ln n-\ln\left(n+5\right)$，故部分和为

$$
\begin{aligned}
S_N&=\sum_{n=1}^{N}\bigl(\ln n-\ln\left(n+5\right)\bigr)\\
&=\ln\left(1\cdot 2\cdot 3\cdot 4\cdot 5\right)-\ln\bigl(\left(N+1\right)\left(N+2\right)\left(N+3\right)\left(N+4\right)\left(N+5\right)\bigr).
\end{aligned}
$$

当 $N\to\infty$ 时后一项的真数趋于 $+\infty$，从而 $S_N\to-\infty$，极限不存在有限值. 故由**定义**（级数收敛），该级数发散. $\blacksquare$

### 习题五

（习题 10.1-2-7）讨论级数 $\sum_{n=1}^{+\infty}\cos^2\frac{\pi}{n}$ 的收敛性或发散性.

### 解答 习题五

当 $n\to\infty$ 时 $\frac{\pi}{n}\to 0$，故

$$
\cos^2\frac{\pi}{n}\to\cos^2 0=1\ne 0.
$$

由**定理 1.1**（收敛级数的必要条件），通项不趋于零，故该级数发散. $\blacksquare$

### 习题六

（习题 10.1-2-8）讨论级数 $\sum_{n=1}^{+\infty}\arctan\frac{1}{2n^2}$ 的收敛性或发散性.

### 解答 习题六

对 $x\ge 0$ 有 $\arctan x\le x$，故

$$
0\le\arctan\frac{1}{2n^2}\le\frac{1}{2n^2}.
$$

又当 $n\ge 2$ 时，

$$
\frac{1}{n^2}\le\frac{1}{n\left(n-1\right)}=\frac{1}{n-1}-\frac{1}{n},
$$

从而

$$
\sum_{n=2}^{N}\frac{1}{n^2}\le\sum_{n=2}^{N}\left(\frac{1}{n-1}-\frac{1}{n}\right)=1-\frac{1}{N}<1.
$$

正项级数 $\sum\frac{1}{2n^2}$ 的部分和有界，故收敛. 又

$$
0\le\sum_{n=1}^{N}\arctan\frac{1}{2n^2}\le\sum_{n=1}^{N}\frac{1}{2n^2}<\frac12,
$$

故 $\sum\arctan\frac{1}{2n^2}$ 的部分和单调递增且有上界，由实数域完备性（第一章**命题 1.5**）其极限存在有限，从而由**定义**（级数收敛），该级数收敛. $\blacksquare$
