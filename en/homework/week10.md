# week10

> **Basic Knowledge: Definition of Differential**<br>Let $y=f\left(x\right)$ be defined near $x_0$. If there exists a constant $A$ such that $\Delta y=A\Delta x+o\left(\Delta x\right)$, then $f$ is differentiable at $x_0$, $\mathrm dy=A\Delta x$ is the differential, and $A=f'\left(x_0\right)$.

> **Basic Knowledge: Definition of Higher-Order Infinitesimal**<br>If $\lim_{x\to0}\frac{\alpha\left(x\right)}{\beta\left(x\right)}=0$, then $\alpha\left(x\right)=o\left(\beta\left(x\right)\right)$.

---

## 2.3-1-2

As $x\to0$, determine the order of the infinitesimal $y=\left(\sqrt{2+x}-\sqrt2\right)x$.

### Solution 2.3-1-2

$$
\sqrt{2+x}-\sqrt2=\frac{x}{\sqrt{2+x}+\sqrt2}\sim\frac{x}{2\sqrt2}.
$$

Thus $y\sim\frac{x^2}{2\sqrt2}$; by **Basic Knowledge: Definition of Higher-Order Infinitesimal**, $y$ is a second-order infinitesimal in $x$. $\blacksquare$

---

## 2.3-1-4

As $x\to0$, determine the order of the infinitesimal $y=\ln\left(1+x^2\right)+x^3$.

### Solution 2.3-1-4

$\ln\left(1+x^2\right)\sim x^2$ and $x^3=o\left(x^2\right)$. By **Basic Knowledge: Definition of Higher-Order Infinitesimal**, $y\sim x^2$, which is second-order. $\blacksquare$

---

## 2.3-3-1

Compute the differential at $x_0$: $f\left(x\right)=x^2\arcsin x$, $x_0=0$.

### Solution 2.3-3-1

$$
f'\left(x\right)=2x\arcsin x+\frac{x^2}{\sqrt{1-x^2}}.
$$

$f'\left(0\right)=0$. Hence $\mathrm df\big|_{x_0=0}=0\cdot\mathrm dx=0$. $\blacksquare$

---

## 2.3-3-4

Compute the differential at $x_0$: $f\left(x\right)=x\ln\left(1+x\right)$, $x_0=0$.

### Solution 2.3-3-4

$f'\left(x\right)=\ln\left(1+x\right)+\frac{x}{1+x}$. $f'\left(0\right)=0$. Hence $\mathrm df\big|_{x_0=0}=0$. $\blacksquare$

---

## 2.3-4-2

Find the differential: $f\left(x\right)=\ln\left(x+\sqrt{x^2+1}\right)$.

### Solution 2.3-4-2

$$
f'\left(x\right)=\frac1{x+\sqrt{x^2+1}}\cdot\left(1+\frac{x}{\sqrt{x^2+1}}\right)=\frac1{x+\sqrt{x^2+1}}\cdot\frac{\sqrt{x^2+1}+x}{\sqrt{x^2+1}}=\frac1{\sqrt{x^2+1}}.
$$

Hence $\mathrm df=\frac1{\sqrt{x^2+1}}\mathrm dx$. $\blacksquare$

---

## 2.3-4-4

Find the differential: $f\left(x\right)=\sqrt{1+x^2}+\sqrt x\sin x$.

### Solution 2.3-4-4

$$
f'\left(x\right)=\frac{x}{\sqrt{1+x^2}}+\frac1{2\sqrt x}\sin x+\sqrt x\cos x.
$$

Hence

$$
\mathrm df=\left(\frac{x}{\sqrt{1+x^2}}+\frac{\sin x}{2\sqrt x}+\sqrt x\cos x\right)\mathrm dx.
$$

$\blacksquare$

---

## 2.3-5-1

Fill in: $\mathrm d\left(\right)=x^n\mathrm dx$.

### Solution 2.3-5-1

$$
\mathrm d\left(\frac{x^{n+1}}{n+1}\right)=x^n\mathrm dx\quad\left(n\ne-1\right).
$$

$\blacksquare$

---

## 2.3-5-3

Fill in: $\mathrm d\left(\right)=\left(e^x+\sin2x\right)\mathrm dx$.

### Solution 2.3-5-3

$$
\mathrm d\left(e^x-\frac12\cos2x\right)=\left(e^x+\sin2x\right)\mathrm dx.
$$

$\blacksquare$

---

## 2.3-5-5

Fill in: $\mathrm d\left(\right)=\frac{\sin x}{\cos x}\mathrm dx$.

### Solution 2.3-5-5

$\mathrm d\left(-\ln\left|\cos x\right|\right)=\frac{\sin x}{\cos x}\mathrm dx$. $\blacksquare$

---

## 2.3-6

Compute the approximate value of $\tan\left(\frac\pi4+0.01\right)$.

### Solution 2.3-6

Let $f\left(x\right)=\tan x$, $x_0=\frac\pi4$, $\Delta x=0.01$. $f'\left(x\right)=\sec^2x$, $f'\left(\frac\pi4\right)=2$. By the approximation formula from **Basic Knowledge: Definition of Differential**,

$$
f\left(x_0+\Delta x\right)\approx f\left(x_0\right)+f'\left(x_0\right)\Delta x,
$$

$$
\tan\left(\frac\pi4+0.01\right)\approx\tan\frac\pi4+2\times0.01=1+0.02=1.02.
$$

$\blacksquare$
