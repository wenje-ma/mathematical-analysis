# week24

> **Theorem 2.1 (Upper/Lower Limit and Existence of Limit)**<br>A bounded sequence $\left\{a_n\right\}$ has a limit iff its upper and lower limits are equal.

> **Theorem 2.2 (Cauchy Convergence Criterion)**<br>A sequence $\left\{a_n\right\}$ has a limit iff for every $\varepsilon> 0$ there exists $N$ such that $\left|a_n-a_m\right|< \varepsilon$ for all $m,n\ge N$.

---

## 5.2-1

Prove: if $\left\{a_n\right\}$ converges, then $\left\{\left|a_n\right|\right\}$ converges.

### Solution 5.2-1

Since $\left|\left|a_n\right|-\left|a_m\right|\right|\le\left|a_n-a_m\right|$, the sequence $\left\{\left|a_n\right|\right\}$ satisfies the Cauchy condition. By **Theorem 2.2 (Cauchy Convergence Criterion)**, it converges. $\blacksquare$

---

## 5.2-2

Prove:

(1) $\varlimsup\left(a_n+b_n\right)\le\varlimsup a_n+\varlimsup b_n$;

(2) $\varliminf\left(a_n+b_n\right)\ge\varliminf a_n+\varliminf b_n$.

### Solution 5.2-2

(1) Let $A_n=\sup_{k\ge n}a_k$, $B_n=\sup_{k\ge n}b_k$. Then $a_k+b_k\le A_n+B_n$, so $\sup_{k\ge n}\left(a_k+b_k\right)\le A_n+B_n$. Taking $n\to\infty$ gives the result.

(2) Similarly for infimum. $\blacksquare$

---

## 5.2-3

Find the upper and lower limits:

(1) $\varlimsup_{x\to0}\sin\frac1x$, $\varliminf_{x\to0}\sin\frac1x$;

(2) $\varlimsup_{x\to\infty}\sin x$, $\varliminf_{x\to\infty}\sin x$.

### Solution 5.2-3

(1) $\sin\frac1x$ oscillates infinitely between $-1$ and $1$. Hence $\varlimsup=1$, $\varliminf=-1$.

(2) Similarly, $\varlimsup_{x\to\infty}\sin x=1$, $\varliminf_{x\to\infty}\sin x=-1$. $\blacksquare$

---

## 5.2-6

Prove convergence by Cauchy criterion:

(1) $a_n=\sum_{k=1}^n\left(-1\right)^{k-1}\frac1k$;

(2) $a_n=\sum_{k=1}^n\frac{\sin k}{k!}$.

### Solution 5.2-6

(1) $\left|a_m-a_n\right|\le\frac1{n+1}\to0$. By **Theorem 2.2 (Cauchy Convergence Criterion)**, converges.

(2) $\left|a_m-a_n\right|\le\sum_{k=n+1}^m\frac1{k!}\le\frac1{2^n}\to0$. By **Theorem 2.2 (Cauchy Convergence Criterion)**, converges. $\blacksquare$

---

## 5.2-7

Prove: if $\lim_{n\to\infty}f\left(x_n\right)=l$ exists for $x_n\to a$, then $\varliminf_{x\to a}f\left(x\right)\le l\le\varlimsup_{x\to a}f\left(x\right)$.

### Solution 5.2-7

For any $\delta> 0$, $\inf_{\left|x-a\right|< \delta}f\le f\left(x_n\right)\le\sup_{\left|x-a\right|< \delta}f$. Taking limits gives the result. $\blacksquare$

---

## 5.2-8

Prove: there exist sequences $x_n'\to a$ and $x_n''\to a$ such that $\lim f\left(x_n'\right)=\varlimsup_{x\to a}f$ and $\lim f\left(x_n''\right)=\varliminf_{x\to a}f$.

### Solution 5.2-8

Choose $x_n'$ in $\left\{x:0< \left|x-a\right|< 1/n\right\}$ close to the supremum. The squeeze theorem gives the result. Similarly for infimum. $\blacksquare$

---

## 5.2-9

Prove: $f\left(x\right)$ has a limit as $x\to a$ iff $\lim_{n\to\infty}f\left(x_n\right)$ exists and is the same for every sequence $x_n\to a$.

### Solution 5.2-9

**Necessity**: follows directly from the definition of functional limit.

**Sufficiency**: by 5.2-8, there exist sequences realizing the upper and lower limits. If all sequence limits agree, then upper and lower limits are equal. By **Theorem 2.1 (Upper/Lower Limit and Existence of Limit)**, the functional limit exists. $\blacksquare$
