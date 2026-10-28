# week41

> **Theorem 2.3 (Limit Form of Comparison Test)**<br>If $\lim\frac{a_n}{b_n}=l\in\left(0,+\infty\right)$, both series have the same convergence behavior.

> **Theorem 4.1 (Relation between Infinite Products and Series)**<br>$\prod p_n$ converges iff $\sum\ln p_n$ converges, and $\prod p_n=\exp\left(\sum\ln p_n\right)$.

> **Theorem 4.2 (Same-Sign Infinite Products)**<br>If $\alpha_n\ge0$, then $\prod\left(1+\alpha_n\right)$ converges iff $\sum\alpha_n$ converges.

> **Theorem 4.4 (Absolute Convergence)**<br>$\prod\left(1+\alpha_n\right)$ converges absolutely iff $\sum\left|\alpha_n\right|$ converges.

---

## 10.4-1-2

Discuss $\prod\sqrt{\frac{n^2+1}{n^2-1}}$.

### Solution 10.4-1-2

Converges by comparison with $\sum\frac1{n^2}$. $\blacksquare$

---

## 10.4-1-4

Discuss $\prod\left(1+\frac{x^n}{2^n}\right)$.

### Solution 10.4-1-4

Converges for $\left|x\right|< 2$, diverges otherwise. $\blacksquare$

---

## 10.4-1-6

Discuss $\prod\cos\frac1n$.

### Solution 10.4-1-6

Since $\ln\cos\frac1n\sim-\frac1{2n^2}$, converges. $\blacksquare$

---

## 10.4-1-8

Discuss $\prod\left(1+\frac1{\sqrt n}\right)$.

### Solution 10.4-1-8

Diverges since $\sum\frac1{\sqrt n}$ diverges. $\blacksquare$

---

## 10.4-2

Prove: if $\sum\alpha_n^2$ converges, then $\prod\cos\alpha_n$ converges.

### Solution 10.4-2

Since $\ln\cos\alpha_n\sim-\frac{\alpha_n^2}{2}$. $\blacksquare$

---

## 10.4-3

Prove: if $\sum\left|\alpha_n\right|$ converges, then $\prod\tan\left(\frac\pi4+\alpha_n\right)$ converges absolutely.

### Solution 10.4-3

Since $\left|\tan\left(\frac\pi4+\alpha_n\right)-1\right|\sim2\left|\alpha_n\right|$. $\blacksquare$

---

## 10.4-5

Prove: if $\prod\left(1+\left|\alpha_n\right|\right)$ converges, then $\prod\left(1+\alpha_n\right)$ converges.

### Solution 10.4-5

By absolute convergence. $\blacksquare$
