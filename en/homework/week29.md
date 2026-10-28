# week29

> **Basic Knowledge: Comparison Property of Double Integrals**<br>If $f\le g$ on $D$, then $\iint_D f\le\iint_D g$.

> **Theorem 2.1 (Reduction to Iterated Integrals)**<br>$\iint_D f\,\mathrm dx\mathrm dy=\int_a^b\mathrm dx\int_{\varphi_1\left(x\right)}^{\varphi_2\left(x\right)}f\left(x,y\right)\,\mathrm dy$.

> **Theorem 2.2 (Double Integrals in Polar Coordinates)**<br>$\iint_D f\,\mathrm dx\mathrm dy=\iint_{D^*}f\left(r\cos\theta,r\sin\theta\right)\,r\,\mathrm dr\mathrm d\theta$.

---

## 8.2-2

Change the order of integration.

### Solution 8.2-2

(1) $\int_0^1\mathrm dx\int_{x^2}^x f\,\mathrm dy$.

(2) $\int_1^2\mathrm dy\int_1^y f\,\mathrm dx+\int_2^4\mathrm dy\int_{y/2}^2 f\,\mathrm dx$.

(3) $\int_0^5\mathrm dy\int_0^y f\,\mathrm dx+\int_5^{10}\mathrm dy\int_0^{10-y}f\,\mathrm dx$.

(4) $\int_1^e\mathrm dy\int_0^{\ln y}f\,\mathrm dx$. $\blacksquare$

---

## 8.2-3

Compute.

### Solution 8.2-3

(1) $\frac\pi4$. (2) $\frac{33}{140}$. (3) $\frac12$. (4) $\frac16$. $\blacksquare$

---

## 8.2-4

Compute.

### Solution 8.2-4

(1) $2$. (2) $4-\sin4$. $\blacksquare$

---

## 8.2-5

Use polar coordinates.

### Solution 8.2-5

(1) $\pi\left(1-\ln2\right)$. (2) $2$. (3) $\frac\pi4\left[\left(1+R^2\right)\ln\left(1+R^2\right)-R^2\right]$. $\blacksquare$

---

## 8.2-6

Compute $\iint_D e^{-x^2-y^2}$ on the quarter annulus.

### Solution 8.2-6

$\frac\pi4\left(e^{-1}-e^{-4}\right)$. $\blacksquare$

---

## 8.2-7

Compute.

### Solution 8.2-7

(1) $-6\pi^2$. (2) $\frac\pi2$. (3) $\frac{\pi a^4}{8}$. (4) $4-\pi^2$. $\blacksquare$

---

## 8.2-8

Prove:

(1) $\left[I\left(a\right)\right]^2=\iint_{R_a}e^{-x^2-y^2}$;

(2) $J\left(a\right)\le\left[I\left(a\right)\right]^2\le J\left(\sqrt2 a\right)$;

(3) $\lim_{a\to\infty}\int_0^a e^{-x^2}\,\mathrm dx=\frac{\sqrt\pi}2$.

### Solution 8.2-8

(1) By **Theorem 2.1 (Reduction to Iterated Integrals)**.

(2) Since $D_a\subset R_a\subset D_{\sqrt2 a}$, by **Basic Knowledge: Comparison Property of Double Integrals**.

(3) $J\left(a\right)=\frac\pi4\left(1-e^{-a^2}\right)$. Squeeze theorem gives the result. $\blacksquare$
