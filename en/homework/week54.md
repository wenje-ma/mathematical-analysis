# week54

> **Theorem 3.1 (Dirichlet's Convergence Theorem)**<br>The Fourier series converges to $\frac{f\left(x+0\right)+f\left(x-0\right)}2$ at every point.

> **Proposition (Fourier Coefficients)**<br>$a_n=\frac1\pi\int_{-\pi}^\pi f\cos nx$, $b_n=\frac1\pi\int_{-\pi}^\pi f\sin nx$.

> **Theorem (Parseval's Identity)**<br>$\frac1\pi\int_{-\pi}^\pi f^2=\frac{a_0^2}2+\sum\left(a_n^2+b_n^2\right)$.

---

## 13.3-1

Prove $1=\frac12+\frac2\pi\sum\frac{\sin\left(2n+1\right)x}{2n+1}$ and $\frac\pi4=\sum\frac{\left(-1\right)^n}{2n+1}$.

### Solution 13.3-1

By the Dirichlet theorem and setting $x=\frac\pi2$. $\blacksquare$

---

## 13.3-3

Find the Fourier series of $\left(\pi-\left|x\right|\right)^2$ and compute $\sum\frac1{n^2}$, $\sum\frac1{n^4}$.

### Solution 13.3-3

$\sum\frac1{n^2}=\frac{\pi^2}6$, $\sum\frac1{n^4}=\frac{\pi^4}{90}$. $\blacksquare$

---

## 13.3-4

Use $x^2$ Fourier series to compute $\sum\frac{\left(-1\right)^{n+1}}{n^2}$ and $\sum\frac1{n^2}$.

### Solution 13.3-4

$\sum\frac1{n^2}=\frac{\pi^2}6$, $\sum\frac{\left(-1\right)^{n+1}}{n^2}=\frac{\pi^2}{12}$. $\blacksquare$
