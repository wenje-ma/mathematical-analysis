# week34

> **Theorem 2.2 (Green's Theorem)**<br>$\oint_{L^+}P\,\mathrm dx+Q\,\mathrm dy=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm dx\mathrm dy$.

> **Theorem 2.4 (Path Independence Condition)**<br>The integral is path-independent iff $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$.

> **Theorem 2.5 (Exact Differential Form)**<br>$P\,\mathrm dx+Q\,\mathrm dy$ is exact iff $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$.

---

## 9.2-1

Compute $\oint_{L^+}x^2\,\mathrm dy-y^2\,\mathrm dx$.

### Solution 9.2-1

By symmetry, the integral is $0$. $\blacksquare$

---

## 9.2-2

Compute the line integral along $y=\left|x\right|$.

### Solution 9.2-2

$\frac{41}{6}$. $\blacksquare$

---

## 9.2-3

Apply Green's theorem.

### Solution 9.2-3

(1) $\frac{\pi R^4}{2}$. (2) $\frac{25}{6}$. (3) $\pi a^2$. $\blacksquare$

---

## 9.2-4

Prove: $\oint_{L^+}f\left(xy\right)\left(y\,\mathrm dx+x\,\mathrm dy\right)=0$.

### Solution 9.2-4

Since $\frac{\partial P}{\partial y}=\frac{\partial Q}{\partial x}$, Green's theorem gives $0$. $\blacksquare$

---

## 9.2-5-3

Compute $\int_{\left(0,0\right)}^{\left(a,b\right)}e^x\cos y\,\mathrm dx-e^x\sin y\,\mathrm dy$.

### Solution 9.2-5-3

Since $d\left(e^x\cos y\right)=e^x\cos y\,\mathrm dx-e^x\sin y\,\mathrm dy$, the result is $e^a\cos b-1$. $\blacksquare$

---

## 9.2-6

Prove: $\oint_{L_r^+}\frac{x\,\mathrm dy-y\,\mathrm dx}{A^2x^2+B^2y^2}=\frac{2\pi}{AB}$.

### Solution 9.2-6

The ellipse area is $\frac{\pi r^2}{AB}$. Hence the integral is $\frac{2\pi}{AB}$. $\blacksquare$

---

## 9.2-7

Prove the same for any closed curve enclosing the origin.

### Solution 9.2-7

By Green's theorem on the doubly connected region, the integral equals that over a small ellipse $L_r$. $\blacksquare$
