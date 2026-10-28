# week47

> **Basic Knowledge: Definition of Improper Integral (Singular Point)**<br>Converges if $\lim_{\eta\to0+}\int_{a+\eta}^b f$ exists.

> **Basic Knowledge: Absolute and Conditional Convergence**<br>Absolute if $\int\left|f\right|$ converges; conditional if $\int f$ converges but $\int\left|f\right|$ diverges.

> **Basic Knowledge: Cauchy Principal Value**<br>The symmetric limit $\lim_{\eta\to0+}\left[\int_a^{c-\eta}f+\int_{c+\eta}^b f\right]$.

> **Example 2.2 (Singular p-Integral)**<br>$\int_a^b\frac{\mathrm dx}{\left(x-a\right)^p}$ converges iff $p< 1$.

---

## 12.2-1-1

Evaluate $\int_0^1\ln x\mathrm dx$.

### Solution 12.2-1-1

$-1$. $\blacksquare$

---

## 12.2-1-3

Evaluate $\int_{-1}^1\frac{\mathrm dx}{\sqrt{1-x^2}}$.

### Solution 12.2-1-3

$\pi$. $\blacksquare$

---

## 12.2-1-5

Discuss $\int_0^1\frac{\mathrm dx}{x\ln^2x}$.

### Solution 12.2-1-5

Diverges. $\blacksquare$

---

## 12.2-2-1

Discuss $\int_0^\infty\frac{\mathrm dx}{\sqrt x\left(1+x\right)}$.

### Solution 12.2-2-1

Converges, value $\pi$. $\blacksquare$

---

## 12.2-2-3

Discuss $\int_0^\infty\frac{\mathrm dx}{x^p+x^q}$.

### Solution 12.2-2-3

Converges iff $\min\left(p,q\right)< 1< \max\left(p,q\right)$. $\blacksquare$

---

## 12.2-2-5

Discuss $\int_0^{\pi/2}\frac{\mathrm dx}{\sin^2x\cos^2x}$.

### Solution 12.2-2-5

Diverges. $\blacksquare$

---

## 12.2-2-7

Discuss $\int_0^1 x^p\left(1-x\right)^q\mathrm dx$.

### Solution 12.2-2-7

Converges for all $p> 0,q> 0$. $\blacksquare$

---

## 12.2-3

Prove: $\int f^2$ convergent implies $\int\left|f\right|$ convergent.

### Solution 12.2-3

By $2\left|f\right|\le1+f^2$. Converse is false. $\blacksquare$

---

## 12.2-4-1

Find the Cauchy principal value of $\int_0^2\frac{\mathrm dx}{x-1}$.

### Solution 12.2-4-1

$0$. $\blacksquare$

---

## 12.2-4-2

Find the Cauchy principal value of $\int_{1/2}^2\frac{\mathrm dx}{x\ln x}$.

### Solution 12.2-4-2

$0$. $\blacksquare$
