# week38

> **Basic Knowledge: Definition of Convergent Series**<br>If the partial sums $S_n=\sum_{k=1}^n a_k$ converge to a finite limit $S$, then $\sum a_n$ converges.

> **Theorem 1.1 (Necessary Condition for Convergence)**<br>If $\sum a_n$ converges, then $\lim_{n\to\infty}a_n=0$.

---

## 10.1-1

Prove the geometric series converges for $\left|q\right|< 1$ and diverges otherwise.

### Solution 10.1-1

Partial sums $S_n=a_0\frac{1-q^{n+1}}{1-q}$. For $\left|q\right|< 1$, $S_n\to\frac{a_0}{1-q}$. For $\left|q\right|\ge1$, by **Theorem 1.1 (Necessary Condition for Convergence)**, the series diverges. $\blacksquare$

---

## 10.1-2-1

Discuss $\sum\left(\sqrt{n+1}-\sqrt n\right)$.

### Solution 10.1-2-1

$S_N=\sqrt{N+1}-1\to+\infty$. Diverges. $\blacksquare$

---

## 10.1-2-2

Discuss $\sum\frac1{\left(2n-1\right)\left(2n+1\right)}$.

### Solution 10.1-2-2

Telescoping gives $S_N\to\frac12$. Converges. $\blacksquare$

---

## 10.1-2-3

Discuss $\sum\ln\frac n{n+5}$.

### Solution 10.1-2-3

$S_N\to-\infty$. Diverges. $\blacksquare$

---

## 10.1-2-7

Discuss $\sum\cos^2\frac\pi n$.

### Solution 10.1-2-7

The general term tends to $1\ne0$. By **Theorem 1.1 (Necessary Condition for Convergence)**, diverges. $\blacksquare$

---

## 10.1-2-8

Discuss $\sum\arctan\frac1{2n^2}$.

### Solution 10.1-2-8

Since $0\le\arctan\frac1{2n^2}\le\frac1{2n^2}$ and $\sum\frac1{n^2}$ converges, the series converges. $\blacksquare$
