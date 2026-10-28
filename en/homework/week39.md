# week39

> **Theorem 2.2 (Comparison Test)**<br>If $0\le a_n\le b_n$ and $\sum b_n$ converges, then $\sum a_n$ converges. If $\sum a_n$ diverges, then $\sum b_n$ diverges.

> **Theorem 2.3 (Limit Form of Comparison Test)**<br>If $\lim\frac{a_n}{b_n}=l\in\left(0,+\infty\right)$, then both series converge or both diverge.

> **Theorem 2.6 (d'Alembert's Ratio Test)**<br>If $\lim\frac{a_{n+1}}{a_n}=r< 1$, the series converges; if $r> 1$, it diverges.

> **Theorem 2.9 (Integral Test)**<br>If $f$ is positive and decreasing on $\left[1,+\infty\right)$, then $\sum f\left(n\right)$ and $\int_1^\infty f\left(x\right)\,\mathrm dx$ have the same convergence behavior.

---

## 10.2-1-15

Discuss $\sum\frac{\left(n!\right)^2}{\left(2n\right)!}$.

### Solution 10.2-1-15

$\frac{a_{n+1}}{a_n}\to\frac14< 1$. Converges by ratio test. $\blacksquare$

---

## 10.2-1-18

Discuss $\sum\frac1{n\left(\ln\ln n\right)^q}$.

### Solution 10.2-1-18

Since $\frac1{n\left(\ln\ln n\right)^q}> \frac1{n\ln n}$ and $\sum\frac1{n\ln n}$ diverges by the integral test, the series diverges. $\blacksquare$

---

## 10.2-2

Discuss $\sum\frac1{n\ln^p n\left(\ln\ln n\right)^q}$.

### Solution 10.2-2

Converges if $p> 1$, or $p=1$ and $q> 1$. Diverges otherwise. $\blacksquare$

---

## 10.2-6

Prove: if $\lim na_n=l\in\left(0,+\infty\right)$, then $\sum a_n^2$ converges but $\sum a_n$ diverges.

### Solution 10.2-6

By the limit comparison test with $\frac1n$ and $\frac1{n^2}$. $\blacksquare$

---

## 10.2-7

Prove: if $\sum a_n^2$ and $\sum b_n^2$ converge, then $\sum\left|a_nb_n\right|$, $\sum\left(a_n+b_n\right)^2$, and $\sum\frac{\left|a_n\right|}{n}$ all converge.

### Solution 10.2-7

Using $2\left|a_nb_n\right|\le a_n^2+b_n^2$ and the comparison test. $\blacksquare$
