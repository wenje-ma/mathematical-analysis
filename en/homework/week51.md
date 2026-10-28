# week51

> **Basic Knowledge: Gamma Function**<br>$\Gamma\left(\alpha\right)=\int_0^\infty t^{\alpha-1}e^{-t}\mathrm dt$. Recurrence: $\Gamma\left(\alpha+1\right)=\alpha\Gamma\left(\alpha\right)$, $\Gamma\left(\frac12\right)=\sqrt\pi$.

> **Basic Knowledge: Beta Function**<br>$\Beta\left(p,q\right)=\int_0^1 t^{p-1}\left(1-t\right)^{q-1}\mathrm dt=\frac{\Gamma\left(p\right)\Gamma\left(q\right)}{\Gamma\left(p+q\right)}$.

> **Proposition (Integral Forms)**<br>$\int_0^\infty\frac{x^{a-1}}{\left(1+x\right)^{a+b}}\mathrm dx=\Beta\left(a,b\right)$; $\int_0^{\pi/2}\sin^m x\cos^n x\,\mathrm dx=\frac12\Beta\left(\frac{m+1}2,\frac{n+1}2\right)$.

---

## 12.6-1-1

Evaluate $\int_0^\infty\frac{4\sqrt x}{\left(1+x\right)^2}\mathrm dx$.

### Solution 12.6-1-1

$2\pi$. $\blacksquare$

---

## 12.6-1-2

Evaluate $\int_0^\infty x^{-1/2}e^{-\alpha x}\mathrm dx$.

### Solution 12.6-1-2

$\sqrt{\frac\pi\alpha}$. $\blacksquare$

---

## 12.6-1-3

Evaluate $\int_0^1 x^8\sqrt{1-x^3}\mathrm dx$.

### Solution 12.6-1-3

$\frac{16}{315}$. $\blacksquare$

---

## 12.6-1-4

Evaluate $\int_0^{\pi/2}\sin^6x\cos^4x\,\mathrm dx$.

### Solution 12.6-1-4

$\frac{3\pi}{512}$. $\blacksquare$

---

## 12.6-1-9

Evaluate $\int_0^1\frac{\mathrm dx}{\sqrt{1-x^4}}$.

### Solution 12.6-1-9

$\frac14\Beta\left(\frac14,\frac12\right)$. $\blacksquare$

---

## 12.6-1-10

Evaluate $\int_0^\infty\frac{\mathrm dx}{1+x^3}$.

### Solution 12.6-1-10

$\frac13\Gamma\left(\frac13\right)\Gamma\left(\frac23\right)$. $\blacksquare$

---

## 12.6-2

Prove $\Gamma\left(\alpha\right)$ does not converge uniformly on $\left(0,+\infty\right)$.

### Solution 12.6-2

By choosing $\alpha_n=\frac1n$. $\blacksquare$
