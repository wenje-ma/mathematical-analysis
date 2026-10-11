# 作业 24

> **定理 2.1**（上下极限与极限存在）设 $\left\{a_n\right\}$ 为一个有界序列. 则序列 $\left\{a_n\right\}$ 有极限之充要条件为其上极限与下极限相等.

> **定理 2.2**（柯西收敛原理）序列 $\left\{a_n\right\}$ 有极限之充要条件是：对任意给定的 $\varepsilon>0$，存在一个自然数 $N$，使得
> $$\left|a_n-a_m\right|<\varepsilon,\ \text{只要 }m\ge N,\ n\ge N.$$

### 习题一

（习题 5.2-1）利用序列柯西收敛原理证明：若 $\left\{a_n\right\}$ 收敛，则 $\left\{\left|a_n\right|\right\}$ 收敛.

### 解答 习题一

设 $\lim\limits_{n\to\infty}a_n=l$. 由柯西收敛原理，对任意 $\varepsilon>0$，存在 $N$，使得当 $m,n\ge N$ 时 $\left|a_n-a_m\right|<\varepsilon$.

由三角不等式，
$$
\left|\right|a_n\left|-\right|a_m\left|\right|\le\left|a_n-a_m\right|<\varepsilon.
$$

故 $\left\{\left|a_n\right|\right\}$ 满足柯西条件. 由**定理 2.2**（柯西收敛原理），$\left\{\left|a_n\right|\right\}$ 收敛. $\blacksquare$

### 习题二

（习题 5.2-2）设 $\left\{a_n\right\}$ 与 $\left\{b_n\right\}$ 为两个有界序列. 证明：
(1) $\varlimsup\left(a_n+b_n\right)\le\varlimsup a_n+\varlimsup b_n$；

(2) $\varliminf\left(a_n+b_n\right)\ge\varliminf a_n+\varliminf b_n$.

### 解答 习题二

（1）记 $A_n=\sup\left\{a_k:k\ge n\right\}$，$B_n=\sup\left\{b_k:k\ge n\right\}$. 则对任意 $k\ge n$，
$$
a_k+b_k\le A_n+B_n.
$$

故 $A_n+B_n$ 是 $\left\{a_k+b_k:k\ge n\right\}$ 的一个上界. 因此
$$
\sup\left\{a_k+b_k:k\ge n\right\}\le A_n+B_n.
$$

令 $n\to\infty$，取极限得
$$
\varlimsup\left(a_n+b_n\right)\le\varlimsup a_n+\varlimsup b_n.
$$

（2）类似地，记 $C_n=\inf\left\{a_k:k\ge n\right\}$，$D_n=\inf\left\{b_k:k\ge n\right\}$. 则对任意 $k\ge n$，
$$
a_k+b_k\ge C_n+D_n.
$$

故 $C_n+D_n$ 是 $\left\{a_k+b_k:k\ge n\right\}$ 的一个下界. 因此
$$
\inf\left\{a_k+b_k:k\ge n\right\}\ge C_n+D_n.
$$

令 $n\to\infty$，取极限得
$$
\varliminf\left(a_n+b_n\right)\ge\varliminf a_n+\varliminf b_n.
$$ $\blacksquare$

### 习题三

（习题 5.2-3）求上下极限：
(1) $\varlimsup\limits_{x\to0}\sin\frac1x$ 及 $\varliminf\limits_{x\to0}\sin\frac1x$；

(2) $\varlimsup\limits_{x\to\infty}\sin x$ 及 $\varliminf\limits_{x\to\infty}\sin x$.

### 解答 习题三

（1）当 $x\to0$ 时，$\frac1x\to\infty$，$\sin\frac1x$ 在 $-1$ 与 $1$ 之间无限次振荡. 在 $0$ 的任意小邻域内，$\sin\frac1x$ 都可以取到 $1$ 和 $-1$（分别在 $\frac1x=2k\pi+\frac{\pi}{2}$ 和 $\frac1x=2k\pi+\frac{3\pi}{2}$ 处）. 故
$$
\varlimsup_{x\to0}\sin\frac1x=1,\ \varliminf_{x\to0}\sin\frac1x=-1.
$$

（2）当 $x\to\infty$ 时，$\sin x$ 同样在 $-1$ 与 $1$ 之间无限次振荡. 在无穷远处的任意邻域内，$\sin x$ 都可以取到 $1$ 和 $-1$. 故
$$
\varlimsup_{x\to\infty}\sin x=1,\ \varliminf_{x\to\infty}\sin x=-1.
$$ $\blacksquare$

### 习题四

（习题 5.2-6）由柯西收敛原理证明下列序列收敛：
(1) $a_n=1-\frac12+\frac13-\cdots+\left(-1\right)^{n-1}\frac1n$；

(2) $a_n=\frac{\sin1}{1!}+\frac{\sin2}{2!}+\cdots+\frac{\sin n}{n!}$.

### 解答 习题四

（1）设 $m>n$. 则
$$
\left|a_m-a_n\right|=\left|\frac{\left(-1\right)^n}{n+1}+\frac{\left(-1\right)^{n+1}}{n+2}+\cdots+\frac{\left(-1\right)^{m-1}}{m}\right|.
$$

这是交错级数的部分和之差. 由莱布尼茨判别法，该交错级数收敛. 用柯西准则表述：
$$
\left|a_m-a_n\right|\le\frac{1}{n+1}.
$$

对任意 $\varepsilon>0$，取 $N>\frac1\varepsilon$，则当 $m,n>N$ 时 $\left|a_m-a_n\right|<\varepsilon$. 由**定理 2.2**（柯西收敛原理），$\left\{a_n\right\}$ 收敛.

（2）设 $m>n$. 则
$$
\left|a_m-a_n\right|=\left|\frac{\sin\left(n+1\right)}{\left(n+1\right)!}+\cdots+\frac{\sin m}{m!}\right|\le\frac{1}{\left(n+1\right)!}+\cdots+\frac{1}{m!}.
$$

当 $n$ 充分大时，$\left(n+1\right)!>2^{n+1}$，故
$$
\left|a_m-a_n\right|\le\frac{1}{2^{n+1}}+\frac{1}{2^{n+2}}+\cdots=\frac{1}{2^n}.
$$

对任意 $\varepsilon>0$，取 $N$ 使得 $2^N>\frac1\varepsilon$，则当 $m,n>N$ 时 $\left|a_m-a_n\right|<\varepsilon$. 由**定理 2.2**（柯西收敛原理），$\left\{a_n\right\}$ 收敛. $\blacksquare$

### 习题五

（习题 5.2-7）设 $f\left(x\right)$ 在 $a$ 点的空心邻域中有定义且有界. 设 $\left\{x_n\right\}$ 是一个序列，且以 $a$ 为其极限. 证明：若 $\lim\limits_{n\to\infty}f\left(x_n\right)$ 存在，则有
$$\varliminf_{x\to a}f\left(x\right)\le\lim_{n\to\infty}f\left(x_n\right)\le\varlimsup_{x\to a}f\left(x\right).$$

### 解答 习题五

记 $l=\lim\limits_{n\to\infty}f\left(x_n\right)$. 对任意 $\delta>0$，当 $n$ 充分大时 $x_n\in\left\{x:0<\left|x-a\right|<\delta\right\}$. 故
$$
\inf\left\{f\left(x\right):0<\left|x-a\right|<\delta\right\}\le f\left(x_n\right)\le\sup\left\{f\left(x\right):0<\left|x-a\right|<\delta\right\}.
$$

令 $n\to\infty$，得
$$
\inf\left\{f\left(x\right):0<\left|x-a\right|<\delta\right\}\le l\le\sup\left\{f\left(x\right):0<\left|x-a\right|<\delta\right\}.
$$

再令 $\delta\to0$，由上下极限的定义，
$$
\varliminf_{x\to a}f\left(x\right)\le l\le\varlimsup_{x\to a}f\left(x\right).
$$ $\blacksquare$

### 习题六

（习题 5.2-8）假定 $f\left(x\right)$ 在 $a$ 点的一个空心邻域内有界. 证明：存在序列 $\left\{x_n'\right\}$ 与 $\left\{x_n''\right\}$，使得 $x_n'\to a$（$n\to\infty$），$x_n''\to a$（$n\to\infty$），且有
$$\lim_{n\to\infty}f\left(x_n'\right)=\varlimsup_{x\to a}f\left(x\right),\ \lim_{n\to\infty}f\left(x_n''\right)=\varliminf_{x\to a}f\left(x\right).$$

### 解答 习题六

记 $L=\varlimsup_{x\to a}f\left(x\right)$. 由上极限的定义，对任意 $n$，在 $\left\{x:0<\left|x-a\right|<1/n\right\}$ 中存在 $x_n'$ 使得
$$
f\left(x_n'\right)>\sup\left\{f\left(x\right):0<\left|x-a\right|<1/n\right\}-\frac1n.
$$

显然 $x_n'\to a$（$n\to\infty$）. 又
$$
\sup\left\{f\left(x\right):0<\left|x-a\right|<1/n\right\}-\frac1n<f\left(x_n'\right)\le\sup\left\{f\left(x\right):0<\left|x-a\right|<1/n\right\}.
$$

令 $n\to\infty$，由夹逼定理，$\lim\limits_{n\to\infty}f\left(x_n'\right)=L$.

下极限的情形类似，取 $x_n''$ 使得 $f\left(x_n''\right)<\inf\left\{f\left(x\right):0<\left|x-a\right|<1/n\right\}+\frac1n$ 即可. $\blacksquare$

### 习题七

（习题 5.2-9）利用上述两题证明：当 $x\to a$ 时，$f\left(x\right)$ 有极限的充要条件是：对任意一串点列 $x_n\to a$（$n\to\infty$），极限 $\lim\limits_{n\to\infty}f\left(x_n\right)$ 都存在且相等.

### 解答 习题七

**必要性** 设 $\lim\limits_{x\to a}f\left(x\right)=l$. 对任意 $x_n\to a$，由函数极限与序列极限的关系，$\lim\limits_{n\to\infty}f\left(x_n\right)=l$.

**充分性** 假定对任意 $x_n\to a$，$\lim f\left(x_n\right)$ 都存在且相等. 由习题六（第 8 题），存在 $x_n'\to a$ 使得 $\lim f\left(x_n'\right)=\varlimsup f\left(x\right)$，存在 $x_n''\to a$ 使得 $\lim f\left(x_n''\right)=\varliminf f\left(x\right)$. 由假定，这两个极限相等，即
$$
\varlimsup_{x\to a}f\left(x\right)=\varliminf_{x\to a}f\left(x\right).
$$

由**定理 2.1**（上下极限与极限存在），$\lim\limits_{x\to a}f\left(x\right)$ 存在. $\blacksquare$
