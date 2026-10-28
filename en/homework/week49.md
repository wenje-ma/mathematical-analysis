# week49

> **Theorem 4.3 (Weierstrass M-Test for Improper Integrals)**<br>If $\left|f\left(x,y\right)\right|\le F\left(x\right)$ and $\int F$ converges, then $\int f$ converges uniformly.

> **Theorem 4.4 (Abel's Test)**<br>If $\int f$ converges uniformly and $g$ is monotone and uniformly bounded, then $\int fg$ converges uniformly.

> **Example 4.5 (Dirichlet Integral)**<br>$\int_0^\infty\frac{\sin x}x\mathrm dx=\frac\pi2$.

> **Theorem 4.7 (Interchange of Order of Integration)**<br>Under uniform convergence, $\int_c^d\mathrm dy\int_a^\infty f\,\mathrm dx=\int_a^\infty\mathrm dx\int_c^d f\,\mathrm dy$.

> **Theorem 4.8 (Differentiation Under the Integral Sign)**<br>$I'\left(y\right)=\int_a^\infty f_y\,\mathrm dx$ under uniform convergence of $\int f_y$.

---

## 12.4-1-1

Discuss uniform convergence of $\int_0^\infty e^{-\alpha x^2}\mathrm dx$.

### Solution 12.4-1-1

Uniformly convergent by the M-test. $\blacksquare$

---

## 12.4-1-3

Discuss $\int_1^\infty e^{-xy}\frac{\cos x}x\mathrm dx$.

### Solution 12.4-1-3

Uniformly convergent by Abel's test. $\blacksquare$

---

## 12.4-1-5

Discuss $\int_0^\infty e^{-x^2y^2}\cos x\,\mathrm dx$.

### Solution 12.4-1-5

Uniformly convergent by the M-test. $\blacksquare$

---

## 12.4-2-1

Evaluate $\int_0^\infty\frac{e^{-ax}-e^{-bx}}x\mathrm dx$.

### Solution 12.4-2-1

$\ln\frac ba$. $\blacksquare$

---

## 12.4-2-2

Evaluate $\int_0^\infty\frac{\sin\left(\alpha x\right)\cos\left(\beta x\right)}x\mathrm dx$.

### Solution 12.4-2-2

$0$ if $\alpha< \beta$, $\frac\pi4$ if $\alpha=\beta$, $\frac\pi2$ if $\alpha> \beta$. $\blacksquare$

---

## 12.4-2-4

Evaluate $\int_0^\infty\frac{1-\cos\left(\alpha x\right)}x e^{-x}\mathrm dx$.

### Solution 12.4-2-4

$\frac12\ln\left(1+\alpha^2\right)$. $\blacksquare$

---

## 12.4-5

Prove Dini's theorem.

### Solution 12.4-5

By contradiction using compactness and monotonicity. $\blacksquare$
