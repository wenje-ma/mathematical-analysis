# week23

> **Theorem 1.3 (Necessary and Sufficient Condition for Continuity)**
> 
> $f$ is continuous at $x_0$ iff $\omega_f\left(x_0\right)=0$.

> **Theorem 2.1 (Upper/Lower Limit and Existence of Limit)**
> 
> A bounded sequence $\left\{a_n\right\}$ has a limit iff its upper and lower limits are equal.

> **Theorem 2.2 (Cauchy Convergence Criterion)**
> 
> A sequence $\left\{a_n\right\}$ has a limit iff for every $\varepsilon>0$ there exists $N$ such that $\left|a_n-a_m\right|<\varepsilon$ for all $m,n\ge{N}$.

## 5.1-7

Prove that a monotone increasing sequence bounded above has a limit.

### Solution to 5.1-7

Let $l=\sup{E}$ where $E=\left\{a_n\right\}$. For any $\varepsilon>0$, there exists $N$ with $a_N>{}l-\varepsilon$. Since $\left\{a_n\right\}$ is increasing, for $n>{}N$, $l-\varepsilon<{}a_n\le{l}$. Hence $\lim_{n\to\infty}a_n=l$. $\blacksquare$

## 5.1-9

Let $R\left(x\right)$ be the Riemann function. Prove:

(1) $\omega_R\left(x\right)=1/q$ for rational $x=p/q$;

(2) $\omega_R\left(x\right)=0$ for irrational $x$.

### Solution to 5.1-9

(1) Any neighborhood of $x_0=p/q$ contains both irrationals ($R=0$) and $x_0$ itself ($R=1/q$). Hence $\omega_R\left(x_0\right)=1/q$.

(2) For any $\varepsilon>0$, only finitely many rationals $p/q$ satisfy $1/q\ge\varepsilon$. Hence in a small enough neighborhood of irrational $x_0$, all rationals have $R<\varepsilon$. Thus $\omega_R\left(x_0\right)=0$. By **Theorem 1.3 (Necessary and Sufficient Condition for Continuity)**, $R$ is continuous at irrationals. $\blacksquare$

## 5.2-1

Prove: if $\left\{a_n\right\}$ converges, then $\left\{\left|a_n\right|\right\}$ converges.

### Solution to 5.2-1

Since $\left|\left|a_n\right|-\left|a_m\right|\right|\le\left|a_n-a_m\right|$, the sequence $\left\{\left|a_n\right|\right\}$ satisfies the Cauchy condition. By **Theorem 2.2 (Cauchy Convergence Criterion)**, it converges. $\blacksquare$

## 5.2-2

Prove:

(1) $\varlimsup\left(a_n+b_n\right)\le\varlimsup{a}_n+\varlimsup{b}_n$;

(2) $\varliminf\left(a_n+b_n\right)\ge\varliminf{a}_n+\varliminf{b}_n$.

### Solution to 5.2-2

(1) Let $A_n=\sup_{k\ge{n}}a_k$, $B_n=\sup_{k\ge{n}}b_k$. Then $a_k+b_k\le{A}_n+B_n$, so $\sup_{k\ge{n}}\left(a_k+b_k\right)\le{A}_n+B_n$. Taking $n\to\infty$ gives the result.

(2) Similarly for infimum. $\blacksquare$

## 5.2-3

Find the upper and lower limits:

(1) $\varlimsup_{x\to0}\sin\frac1x$, $\varliminf_{x\to0}\sin\frac1x$;

(2) $\varlimsup_{x\to\infty}\sin{x}$, $\varliminf_{x\to\infty}\sin{x}$.

### Solution to 5.2-3

(1) $\sin\frac1x$ oscillates infinitely between $-1$ and $1$. Hence $\varlimsup=1$, $\varliminf=-1$.

(2) Similarly, $\varlimsup_{x\to\infty}\sin{x}=1$, $\varliminf_{x\to\infty}\sin{x}=-1$. $\blacksquare$

## 5.2-6

Prove convergence by Cauchy criterion:

(1) $a_n=\sum_{k=1}^n\left(-1\right)^{k-1}\frac1k$;

(2) $a_n=\sum_{k=1}^n\frac{\sin{k}}{k!}$.

### Solution to 5.2-6

(1) $\left|a_m-a_n\right|\le\frac1{n+1}\to0$. By **Theorem 2.2 (Cauchy Convergence Criterion)**, converges.

(2) $\left|a_m-a_n\right|\le\sum_{k=n+1}^m\frac1{k!}\le\frac1{2^n}\to0$. By **Theorem 2.2 (Cauchy Convergence Criterion)**, converges. $\blacksquare$

## 5.2-7

Prove: if $\lim_{n\to\infty}f\left(x_n\right)=l$ exists for $x_n\to{a}$, then $\varliminf_{x\to{a}}f\left(x\right)\le{l}\le\varlimsup_{x\to{a}}f\left(x\right)$.

### Solution to 5.2-7

For any $\delta>0$, $\inf_{\left|x-a\right|<\delta}f\le{f}\left(x_n\right)\le\sup_{\left|x-a\right|<\delta}f$. Taking limits gives the result. $\blacksquare$
