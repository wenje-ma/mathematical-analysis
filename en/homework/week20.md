# week20

> **Theorem 3.1 (Integration by Parts)**<br>If $u\left(x\right)$ and $v\left(x\right)$ are differentiable, then $\int u\left(x\right)\,\mathrm dv\left(x\right)=u\left(x\right)v\left(x\right)-\int v\left(x\right)\,\mathrm du\left(x\right)$.

---

## 4.3-1-11

Find $\int x\csc^2x\,\mathrm dx$.

### Solution 4.3-1-11

Let $u=x$, $\mathrm dv=\csc^2x\,\mathrm dx$. By **Theorem 3.1 (Integration by Parts)**,

$$
\int x\csc^2x\,\mathrm dx=-x\cot x+\ln\left|\sin x\right|+C.
$$

$\blacksquare$

---

## 4.3-1-13

Find $\int\sqrt{1+9x^2}\,\mathrm dx$.

### Solution 4.3-1-13

Let $u=\sqrt{1+9x^2}$, $\mathrm dv=\mathrm dx$. By **Theorem 3.1 (Integration by Parts)**,

$$
\int\sqrt{1+9x^2}\,\mathrm dx=\frac x2\sqrt{1+9x^2}+\frac16\ln\left(3x+\sqrt{1+9x^2}\right)+C.
$$

$\blacksquare$

---

## 4.3-1-14

Find $\int\sec^3x\,\mathrm dx$.

### Solution 4.3-1-14

Let $u=\sec x$, $\mathrm dv=\sec^2x\,\mathrm dx$. By **Theorem 3.1 (Integration by Parts)** and $\tan^2x=\sec^2x-1$,

$$
\int\sec^3x\,\mathrm dx=\frac12\left(\sec x\tan x+\ln\left|\sec x+\tan x\right|\right)+C.
$$

$\blacksquare$
