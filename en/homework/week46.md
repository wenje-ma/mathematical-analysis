# week46

> **Basic Knowledge: Definition of Improper Integral Convergence**<br>$\int_a^{+\infty}f\left(x\right)\mathrm dx$ converges if $\lim_{A\to+\infty}\int_a^A f\left(x\right)\mathrm dx$ exists.

> **Basic Knowledge: Absolute and Conditional Convergence**<br>Converges absolutely if $\int\left|f\right|$ converges; converges conditionally if $\int f$ converges but $\int\left|f\right|$ diverges.

> **Theorem 1.1 (Cauchy Criterion)**<br>The integral converges iff for every $\varepsilon> 0$, there exists $X$ such that $\left|\int_{A'}^{A''}f\right|< \varepsilon$ for $A',A''> X$.

> **Example 1.2 (p-Integral)**<br>$\int_1^\infty\frac{\mathrm dx}{x^p}$ converges iff $p> 1$.

> **Theorem 1.3 (Comparison Test)**<br>If $0\le f\le g$, then $\int g$ convergent implies $\int f$ convergent.

> **Theorem 1.6 (Dirichlet's Test)**<br>If $f$ is monotone tending to $0$ and $\int_a^A g$ is bounded for all $A$, then $\int fg$ converges.

---

## 12.1-1-1

Evaluate $\int_1^\infty\frac{\ln x}{x^2}\mathrm dx$.

### Solution 12.1-1-1

Integration by parts gives $1$. $\blacksquare$

---

## 12.1-1-2

Evaluate $\int_1^\infty e^{-ax}\mathrm dx$.

### Solution 12.1-1-2

$\frac{e^{-a}}a$. $\blacksquare$

---

## 12.1-1-3

Evaluate $\int_0^\infty\frac{\mathrm dx}{1+x^2}$.

### Solution 12.1-1-3

$\frac\pi2$. $\blacksquare$

---

## 12.1-1-4

Evaluate $\int_0^\infty xe^{-x}\mathrm dx$.

### Solution 12.1-1-4

$1$. $\blacksquare$

---

## 12.1-2-1

Discuss $\int_1^\infty\frac{\sin x}{x^p}\mathrm dx$.

### Solution 12.1-2-1

Absolutely convergent for $p> 1$, conditionally for $0< p\le1$, divergent for $p\le0$. $\blacksquare$

---

## 12.1-2-3

Discuss $\int_1^\infty\frac{\sqrt x\cos x}{x+3}\mathrm dx$.

### Solution 12.1-2-3

Conditionally convergent. $\blacksquare$

---

## 12.1-2-5

Discuss $\int_0^\infty\sin x^2\mathrm dx$.

### Solution 12.1-2-5

Conditionally convergent. $\blacksquare$

---

## 12.1-3

Evaluate $I_1=\int_0^\infty e^{-xt}\sin t\mathrm dt$ and $I_2=\int_0^\infty e^{-xt}\cos t\mathrm dt$.

### Solution 12.1-3

$I_1=\frac1{x^2+1}$, $I_2=\frac x{x^2+1}$. $\blacksquare$

---

## 12.1-4

Prove translation and reflection invariance.

### Solution 12.1-4

By substitution. $\blacksquare$

---

## 12.1-5

Prove: $\int_1^\infty f$ converges iff $\sum a_n$ converges, where $a_n=\int_n^{n+1}f$.

### Solution 12.1-5

By partial sums and $f\left(x\right)\to0$. $\blacksquare$
