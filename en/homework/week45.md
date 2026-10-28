# week45

> **Basic Knowledge: Basic Expansions**<br>$e^x=\sum\frac{x^n}{n!}$; $\ln\left(1+x\right)=\sum\frac{\left(-1\right)^{n-1}x^n}{n}$; $\cos x=\sum\frac{\left(-1\right)^nx^{2n}}{\left(2n\right)!}$.

> **Theorem 4.1 (Taylor Series)**<br>If $f$ has a power series expansion, then the coefficients are uniquely determined: $a_n=\frac{f^{\left(n\right)}\left(x_0\right)}{n!}$.

---

## 11.4-1-3

Expand $e^x$ around $x_0=3$.

### Solution 11.4-1-3

$e^x=e^3\sum\frac{\left(x-3\right)^n}{n!}$. $\blacksquare$

---

## 11.4-1-4

Expand $\ln x$ around $x_0=2$.

### Solution 11.4-1-4

$\ln x=\ln2+\sum\frac{\left(-1\right)^{n-1}}{n\cdot2^n}\left(x-2\right)^n$. $\blacksquare$

---

## 11.4-1-5

Expand $\cos^2x$ around $x_0=0$.

### Solution 11.4-1-5

$\cos^2x=\frac12+\sum\frac{\left(-1\right)^n2^{2n-1}}{\left(2n\right)!}x^{2n}$. $\blacksquare$

---

## 11.4-2

Prove $\sum\frac{x^n}{\left(n+1\right)!}=\frac1x\left(e^x-1\right)$ and $\sum\frac n{\left(n+1\right)!}=1$.

### Solution 11.4-2

From the expansion of $e^x$. $\blacksquare$

---

## 11.4-3

Prove $\sum\frac n{\left(n+2\right)!}=3-e$.

### Solution 11.4-3

By splitting the general term. $\blacksquare$
