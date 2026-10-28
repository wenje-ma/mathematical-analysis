# week42

> **Basic Knowledge: Definition of Uniform Convergence**<br>$\left\{f_n\right\}$ converges uniformly to $f$ on $X$ if for every $\varepsilon> 0$, there exists $N$ such that $\left|f_n\left(x\right)-f\left(x\right)\right|< \varepsilon$ for all $n> N$ and all $x\in X$.

> **Theorem 1.1 (Weierstrass M-Test)**<br>If $\left|f_n\left(x\right)-f\left(x\right)\right|\le M_n$ and $M_n\to0$, then the convergence is uniform.

> **Theorem 1.2 (Continuity of the Limit Function)**<br>If $\left\{f_n\right\}$ converges uniformly to $f$ and each $f_n$ is continuous, then $f$ is continuous.

---

## 11.1-1-1

Discuss $f_n\left(x\right)=\frac1{1+nx}$ on $\left(0,1\right)$.

### Solution 11.1-1-1

Not uniformly convergent since $\sup\left|f_n\right|=1\not\to0$. $\blacksquare$

---

## 11.1-1-3

Discuss $f_n\left(x\right)=\frac{\sin\left(nx+n\right)}n$ on $\mathbb R$.

### Solution 11.1-1-3

Uniformly convergent by the M-test. $\blacksquare$

---

## 11.1-1-5

Discuss $f_n\left(x\right)=nxe^{-nx^2}$ on $\left[0,1\right]$.

### Solution 11.1-1-5

Not uniformly convergent since $\sup\left|f_n\right|\to\infty$. $\blacksquare$

---

## 11.1-2

Prove the interchange of limits.

### Solution 11.1-2

Using the Cauchy criterion and triangle inequality. $\blacksquare$

---

## 11.1-3

Prove $\left(1+\frac xn\right)^n$ does not converge uniformly to $e^x$ on $\left[0,+\infty\right)$.

### Solution 11.1-3

Since $\left|\left(1+1\right)^n-e^n\right|\to+\infty$. $\blacksquare$

---

## 11.1-4

Prove uniform convergence on $\left[0,A\right]$.

### Solution 11.1-4

By the M-test with $M_n=\frac{A^2e^A}{2n}$. $\blacksquare$

---

## 11.1-5

Prove: uniform convergence iff $M_n=\max\left|f_n-f\right|\to0$.

### Solution 11.1-5

Direct from the definition. $\blacksquare$
