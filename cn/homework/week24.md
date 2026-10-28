# week24

> **定理 2.1 (上下极限与极限存在)**<br>设 $\left\{a_n\right\}$ 为一个有界序列. 则 $\left\{a_n\right\}$ 有极限之充要条件为其上极限与下极限相等.

> **定理 2.2 (柯西收敛原理)**<br>序列 $\left\{a_n\right\}$ 有极限之充要条件是: 对任意给定的 $\varepsilon> 0$, 存在自然数 $N$, 使得 $\left|a_n-a_m\right|< \varepsilon$ (只要 $m,n\ge N$).

---

## 5.2-1

利用序列柯西收敛原理证明: 若 $\left\{a_n\right\}$ 收敛, 则 $\left\{\left|a_n\right|\right\}$ 收敛.

### 解答 5.2-1

设 $\lim_{n\to\infty}a_n=l$. 由**定理 2.2 (柯西收敛原理)**, 对任意 $\varepsilon> 0$, 存在 $N$, 使得当 $m,n\ge N$ 时 $\left|a_n-a_m\right|< \varepsilon$.

由三角不等式, $\left|\left|a_n\right|-\left|a_m\right|\right|\le\left|a_n-a_m\right|< \varepsilon$. 故 $\left\{\left|a_n\right|\right\}$ 满足柯西条件. 由**定理 2.2 (柯西收敛原理)**, $\left\{\left|a_n\right|\right\}$ 收敛. $\blacksquare$

---

## 5.2-2

设 $\left\{a_n\right\}$ 与 $\left\{b_n\right\}$ 为两个有界序列. 证明:

(1) $\varlimsup\left(a_n+b_n\right)\le\varlimsup a_n+\varlimsup b_n$;

(2) $\varliminf\left(a_n+b_n\right)\ge\varliminf a_n+\varliminf b_n$.

### 解答 5.2-2

(1) 记 $A_n=\sup\left\{a_k:k\ge n\right\}$, $B_n=\sup\left\{b_k:k\ge n\right\}$. 则 $a_k+b_k\le A_n+B_n$. 故 $\sup\left\{a_k+b_k:k\ge n\right\}\le A_n+B_n$. 令 $n\to\infty$, 得 $\varlimsup\left(a_n+b_n\right)\le\varlimsup a_n+\varlimsup b_n$.

(2) 同理, 记 $C_n=\inf\left\{a_k:k\ge n\right\}$, $D_n=\inf\left\{b_k:k\ge n\right\}$. 则 $a_k+b_k\ge C_n+D_n$. 令 $n\to\infty$, 得 $\varliminf\left(a_n+b_n\right)\ge\varliminf a_n+\varliminf b_n$. $\blacksquare$

---

## 5.2-3

求上下极限:

(1) $\varlimsup_{x\to0}\sin\frac1x$ 及 $\varliminf_{x\to0}\sin\frac1x$;

(2) $\varlimsup_{x\to\infty}\sin x$ 及 $\varliminf_{x\to\infty}\sin x$.

### 解答 5.2-3

(1) 当 $x\to0$ 时, $\sin\frac1x$ 在 $-1$ 与 $1$ 之间无限次振荡. 在 $0$ 的任意小邻域内, $\sin\frac1x$ 都可以取到 $1$ 和 $-1$. 故 $\varlimsup_{x\to0}\sin\frac1x=1$, $\varliminf_{x\to0}\sin\frac1x=-1$.

(2) 当 $x\to\infty$ 时, $\sin x$ 同样在 $-1$ 与 $1$ 之间无限次振荡. 故 $\varlimsup_{x\to\infty}\sin x=1$, $\varliminf_{x\to\infty}\sin x=-1$. $\blacksquare$

---

## 5.2-6

由柯西收敛原理证明下列序列收敛:

(1) $a_n=1-\frac12+\frac13-\cdots+\left(-1\right)^{n-1}\frac1n$;

(2) $a_n=\frac{\sin1}{1!}+\frac{\sin2}{2!}+\cdots+\frac{\sin n}{n!}$.

### 解答 5.2-6

(1) 设 $m> n$. 则 $\left|a_m-a_n\right|\le\frac1{n+1}$. 对任意 $\varepsilon> 0$, 取 $N> \frac1\varepsilon$, 则 $\left|a_m-a_n\right|< \varepsilon$. 由**定理 2.2 (柯西收敛原理)**, $\left\{a_n\right\}$ 收敛.

(2) 设 $m> n$. 则 $\left|a_m-a_n\right|\le\frac1{\left(n+1\right)!}+\cdots+\frac1{m!}\le\frac1{2^n}$. 对任意 $\varepsilon> 0$, 取 $N$ 使得 $2^N> \frac1\varepsilon$. 由**定理 2.2 (柯西收敛原理)**, $\left\{a_n\right\}$ 收敛. $\blacksquare$

---

## 5.2-7

设 $f\left(x\right)$ 在 $a$ 点的空心邻域中有定义且有界. 设 $\left\{x_n\right\}$ 以 $a$ 为极限. 证明: 若 $\lim_{n\to\infty}f\left(x_n\right)$ 存在, 则 $\varliminf_{x\to a}f\left(x\right)\le\lim_{n\to\infty}f\left(x_n\right)\le\varlimsup_{x\to a}f\left(x\right)$.

### 解答 5.2-7

记 $l=\lim_{n\to\infty}f\left(x_n\right)$. 对任意 $\delta> 0$, 当 $n$ 充分大时 $x_n$ 在空心邻域中. 故

$$
\inf\left\{f\left(x\right):0< \left|x-a\right|< \delta\right\}\le f\left(x_n\right)\le\sup\left\{f\left(x\right):0< \left|x-a\right|< \delta\right\}.
$$

令 $n\to\infty$, 再令 $\delta\to0$, 得 $\varliminf_{x\to a}f\left(x\right)\le l\le\varlimsup_{x\to a}f\left(x\right)$. $\blacksquare$

---

## 5.2-8

假定 $f\left(x\right)$ 在 $a$ 点的一个空心邻域内有界. 证明: 存在序列 $\left\{x_n'\right\}$ 与 $\left\{x_n''\right\}$, 使得 $x_n'\to a$, $x_n''\to a$, 且 $\lim_{n\to\infty}f\left(x_n'\right)=\varlimsup_{x\to a}f\left(x\right)$, $\lim_{n\to\infty}f\left(x_n''\right)=\varliminf_{x\to a}f\left(x\right)$.

### 解答 5.2-8

记 $L=\varlimsup_{x\to a}f\left(x\right)$. 对任意 $n$, 在 $\left\{x:0< \left|x-a\right|< 1/n\right\}$ 中存在 $x_n'$ 使得

$$
\sup\left\{f:0< \left|x-a\right|< 1/n\right\}-\frac1n< f\left(x_n'\right)\le\sup\left\{f:0< \left|x-a\right|< 1/n\right\}.
$$

令 $n\to\infty$, 由夹逼定理, $\lim_{n\to\infty}f\left(x_n'\right)=L$. 下极限的情形类似. $\blacksquare$

---

## 5.2-9

利用上述两题证明: 当 $x\to a$ 时, $f\left(x\right)$ 有极限的充要条件是: 对任意点列 $x_n\to a$, 极限 $\lim_{n\to\infty}f\left(x_n\right)$ 都存在且相等.

### 解答 5.2-9

**必要性**: 设 $\lim_{x\to a}f\left(x\right)=l$. 对任意 $x_n\to a$, 由函数极限与序列极限的关系, $\lim_{n\to\infty}f\left(x_n\right)=l$.

**充分性**: 由 5.2-8, 存在 $x_n'\to a$ 使得 $\lim f\left(x_n'\right)=\varlimsup f\left(x\right)$, 存在 $x_n''\to a$ 使得 $\lim f\left(x_n''\right)=\varliminf f\left(x\right)$. 由假定, 这两个极限相等, 即 $\varlimsup_{x\to a}f\left(x\right)=\varliminf_{x\to a}f\left(x\right)$. 由**定理 2.1 (上下极限与极限存在)**, $\lim_{x\to a}f\left(x\right)$ 存在. $\blacksquare$
