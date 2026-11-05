# week23

> **定理 1.3 (连续的充要条件)**
> 
> 设 $y=f\left(x\right)$ 在 $x_0$ 点附近为有界函数. 则 $f$ 在 $x_0$ 点连续的充要条件是 $\omega_f\left(x_0\right)=0$.

> **定理 2.1 (上下极限与极限存在)**
> 
> 设 $\left\{a_n\right\}$ 为一个有界序列. 则 $\left\{a_n\right\}$ 有极限之充要条件为其上极限与下极限相等.

> **定理 2.2 (柯西收敛原理)**
> 
> 序列 $\left\{a_n\right\}$ 有极限之充要条件是: 对任意给定的 $\varepsilon>0$, 存在自然数 $N$, 使得 $\left|a_n-a_m\right|<\varepsilon$ (只要 $m,n\ge{N}$).

## 5.1-7

试利用非空有上界必有上确界的定理推出: 单调递增有上界的序列一定有极限.

### 解答 5.1-7

设 $\left\{a_n\right\}$ 单调递增且有上界. 由上确界存在定理, $E=\left\{a_n:n\ge1\right\}$ 有上确界 $l=\sup{E}$.

对任意 $\varepsilon>0$, 由上确界与下确界的定义, 存在 $N$ 使得 $a_N>{}l-\varepsilon$. 又因 $\left\{a_n\right\}$ 单调递增, 当 $n>{}N$ 时 $a_n\ge{a}_N>{}l-\varepsilon$. 另一方面 $a_n\le{l}<{}l+\varepsilon$. 故 $\left|a_n-l\right|<\varepsilon$. 由序列极限的定义, $\lim_{n\to\infty}a_n=l$. $\blacksquare$

## 5.1-9

设 $y=R\left(x\right)$ 为黎曼函数, 即 $R\left(x\right)=0$ ($x$ 为无理数), $R\left(x\right)=1/q$ ($x=p/q$ 为既约有理数). 证明:

(1) 对任意有理数 $x=p/q$, $\omega_R\left(x\right)=1/q$;

(2) 对任意无理数 $x$, $\omega_R\left(x\right)=0$.

### 解答 5.1-9

(1) 设 $x_0=p/q$ 为既约有理数, 则 $R\left(x_0\right)=1/q$. 在 $x_0$ 的任意邻域内, 既有无理数 $x$ 使得 $R\left(x\right)=0$, 又有 $x_0$ 本身. 故 $\sup{R}=1/q$, $\inf{R}=0$. 因此 $\omega_R\left(x_0\right)=1/q$.

(2) 设 $x_0$ 为无理数. 对任意 $\varepsilon>0$, 满足 $1/q\ge\varepsilon$ 的正整数 $q$ 只有有限多个, 对应的既约有理数 $p/q$ 也只有有限多个. 因此在 $x_0$ 的某个足够小的邻域内, 其余有理点都满足 $1/q<\varepsilon$. 故 $\sup{R}-\inf{R}<\varepsilon$. 由 $\varepsilon$ 的任意性, $\omega_R\left(x_0\right)=0$. 由**定理 1.3 (连续的充要条件)**, 黎曼函数在无理点连续. $\blacksquare$

## 5.2-1

利用序列柯西收敛原理证明: 若 $\left\{a_n\right\}$ 收敛, 则 $\left\{\left|a_n\right|\right\}$ 收敛.

### 解答 5.2-1

设 $\lim_{n\to\infty}a_n=l$. 由**定理 2.2 (柯西收敛原理)**, 对任意 $\varepsilon>0$, 存在 $N$, 使得当 $m,n\ge{N}$ 时 $\left|a_n-a_m\right|<\varepsilon$.

由三角不等式, $\left|\left|a_n\right|-\left|a_m\right|\right|\le\left|a_n-a_m\right|<\varepsilon$. 故 $\left\{\left|a_n\right|\right\}$ 满足柯西条件. 由**定理 2.2 (柯西收敛原理)**, $\left\{\left|a_n\right|\right\}$ 收敛. $\blacksquare$

## 5.2-2

设 $\left\{a_n\right\}$ 与 $\left\{b_n\right\}$ 为两个有界序列. 证明:

(1) $\varlimsup\left(a_n+b_n\right)\le\varlimsup{a}_n+\varlimsup{b}_n$;

(2) $\varliminf\left(a_n+b_n\right)\ge\varliminf{a}_n+\varliminf{b}_n$.

### 解答 5.2-2

(1) 记 $A_n=\sup\left\{a_k:k\ge{n}\right\}$, $B_n=\sup\left\{b_k:k\ge{n}\right\}$. 则 $a_k+b_k\le{A}_n+B_n$. 故 $\sup\left\{a_k+b_k:k\ge{n}\right\}\le{A}_n+B_n$. 令 $n\to\infty$, 得 $\varlimsup\left(a_n+b_n\right)\le\varlimsup{a}_n+\varlimsup{b}_n$.

(2) 同理, 记 $C_n=\inf\left\{a_k:k\ge{n}\right\}$, $D_n=\inf\left\{b_k:k\ge{n}\right\}$. 则 $a_k+b_k\ge{C}_n+D_n$. 令 $n\to\infty$, 得 $\varliminf\left(a_n+b_n\right)\ge\varliminf{a}_n+\varliminf{b}_n$. $\blacksquare$

## 5.2-3

求上下极限:

(1) $\varlimsup_{x\to0}\sin\frac1x$ 及 $\varliminf_{x\to0}\sin\frac1x$;

(2) $\varlimsup_{x\to\infty}\sin{x}$ 及 $\varliminf_{x\to\infty}\sin{x}$.

### 解答 5.2-3

(1) 当 $x\to0$ 时, $\sin\frac1x$ 在 $-1$ 与 $1$ 之间无限次振荡. 在 $0$ 的任意小邻域内, $\sin\frac1x$ 都可以取到 $1$ 和 $-1$. 故 $\varlimsup_{x\to0}\sin\frac1x=1$, $\varliminf_{x\to0}\sin\frac1x=-1$.

(2) 当 $x\to\infty$ 时, $\sin{x}$ 同样在 $-1$ 与 $1$ 之间无限次振荡. 故 $\varlimsup_{x\to\infty}\sin{x}=1$, $\varliminf_{x\to\infty}\sin{x}=-1$. $\blacksquare$

## 5.2-6

由柯西收敛原理证明下列序列收敛:

(1) $a_n=1-\frac12+\frac13-\cdots+\left(-1\right)^{n-1}\frac1n$;

(2) $a_n=\frac{\sin1}{1!}+\frac{\sin2}{2!}+\cdots+\frac{\sin{n}}{n!}$.

### 解答 5.2-6

(1) 设 $m>{}n$. 则 $\left|a_m-a_n\right|\le\frac1{n+1}$. 对任意 $\varepsilon>0$, 取 $N>\frac1\varepsilon$, 则 $\left|a_m-a_n\right|<\varepsilon$. 由**定理 2.2 (柯西收敛原理)**, $\left\{a_n\right\}$ 收敛.

(2) 设 $m>{}n$. 则 $\left|a_m-a_n\right|\le\frac1{\left(n+1\right)!}+\cdots+\frac1{m!}\le\frac1{2^n}$. 对任意 $\varepsilon>0$, 取 $N$ 使得 $2^N>\frac1\varepsilon$. 由**定理 2.2 (柯西收敛原理)**, $\left\{a_n\right\}$ 收敛. $\blacksquare$

## 5.2-7

设 $f\left(x\right)$ 在 $a$ 点的空心邻域中有定义且有界. 设 $\left\{x_n\right\}$ 以 $a$ 为极限. 证明: 若 $\lim_{n\to\infty}f\left(x_n\right)$ 存在, 则 $\varliminf_{x\to{a}}f\left(x\right)\le\lim_{n\to\infty}f\left(x_n\right)\le\varlimsup_{x\to{a}}f\left(x\right)$.

### 解答 5.2-7

记 $l=\lim_{n\to\infty}f\left(x_n\right)$. 对任意 $\delta>0$, 当 $n$ 充分大时 $x_n$ 在空心邻域中. 故

$$
\inf\left\{f\left(x\right):0<\left|x-a\right|<\delta\right\}\le{f}\left(x_n\right)\le\sup\left\{f\left(x\right):0<\left|x-a\right|<\delta\right\}.
$$

令 $n\to\infty$, 再令 $\delta\to0$, 得 $\varliminf_{x\to{a}}f\left(x\right)\le{l}\le\varlimsup_{x\to{a}}f\left(x\right)$. $\blacksquare$
