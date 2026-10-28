# week19

> **Theorem 2.1 (First Substitution Rule)**<br>If $F'\left(u\right)=f\left(u\right)$ and $u=\varphi\left(x\right)$ is differentiable, then $\int f\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm dx=F\left(\varphi\left(x\right)\right)+C$.

> **Theorem 2.2 (Second Substitution Rule)**<br>If $x=\varphi\left(t\right)$ is differentiable with inverse, and $\int f\left(\varphi\left(t\right)\right)\varphi'\left(t\right)\,\mathrm dt=G\left(t\right)+C$, then $\int f\left(x\right)\,\mathrm dx=G\left(\varphi^{-1}\left(x\right)\right)+C$.

---

## 4.2-1-2

Find $\int\sqrt{2x+3}\,\mathrm dx$.

### Solution 4.2-1-2

Let $u=2x+3$. By **Theorem 2.1 (First Substitution Rule)**,

$$
\int\sqrt{2x+3}\,\mathrm dx=\frac13\left(2x+3\right)^{3/2}+C.
$$

$\blacksquare$

---

## 4.2-1-4

Find $\int\frac{\mathrm dx}{\left(x-1\right)^5}$.

### Solution 4.2-1-4

Let $u=x-1$. By **Theorem 2.1 (First Substitution Rule)**,

$$
\int\frac{\mathrm dx}{\left(x-1\right)^5}=-\frac1{4\left(x-1\right)^4}+C.
$$

$\blacksquare$

---

## 4.2-1-6

Find $\int\mathrm{sh}\,x\,\mathrm dx$.

### Solution 4.2-1-6

Since $\left(\mathrm{ch}\,x\right)'=\mathrm{sh}\,x$, $\int\mathrm{sh}\,x\,\mathrm dx=\mathrm{ch}\,x+C$. $\blacksquare$

---

## 4.2-1-8

Find $\int\frac{\mathrm dx}{a^2+b^2x^2}$ ($a,b> 0$).

### Solution 4.2-1-8

Let $u=\frac{bx}{a}$. By **Theorem 2.1 (First Substitution Rule)**,

$$
\int\frac{\mathrm dx}{a^2+b^2x^2}=\frac1{ab}\arctan\frac{bx}{a}+C.
$$

$\blacksquare$

---

## 4.2-1-10

Find $\int\frac{\mathrm dx}{\sin x+\cos x}$.

### Solution 4.2-1-10

Using $\sin x+\cos x=\sqrt2\sin\left(x+\frac\pi4\right)$ and letting $u=x+\frac\pi4$,

$$
\int\frac{\mathrm dx}{\sin x+\cos x}=\frac1{\sqrt2}\ln\left|\csc u-\cot u\right|+C.
$$

$\blacksquare$

---

## 4.2-2-1

Find $\int\sqrt{a^2-x^2}\,\mathrm dx$ ($a> 0$).

### Solution 4.2-2-1

Let $x=a\sin t$. By **Theorem 2.2 (Second Substitution Rule)**,

$$
\int\sqrt{a^2-x^2}\,\mathrm dx=\frac{a^2}2\arcsin\frac xa+\frac x2\sqrt{a^2-x^2}+C.
$$

$\blacksquare$

---

## 4.2-2-3

Find $\int\frac{\mathrm dx}{\sqrt{x^2+a^2}}$ ($a> 0$).

### Solution 4.2-2-3

Let $x=a\tan t$. By **Theorem 2.2 (Second Substitution Rule)**,

$$
\int\frac{\mathrm dx}{\sqrt{x^2+a^2}}=\ln\left(x+\sqrt{x^2+a^2}\right)+C'.
$$

$\blacksquare$

---

## 4.2-2-5

Find $\int\sqrt{x^2-a^2}\,\mathrm dx$ ($a> 0$).

### Solution 4.2-2-5

Let $x=a\sec t$. By **Theorem 2.2 (Second Substitution Rule)**,

$$
\int\sqrt{x^2-a^2}\,\mathrm dx=\frac x2\sqrt{x^2-a^2}-\frac{a^2}2\ln\left|x+\sqrt{x^2-a^2}\right|+C.
$$

$\blacksquare$

---

## 4.2-2-7

Find $\int\frac{\mathrm dx}{x\sqrt{a^2-x^2}}$ ($a> 0$).

### Solution 4.2-2-7

Let $x=a\sin t$. By **Theorem 2.2 (Second Substitution Rule)**,

$$
\int\frac{\mathrm dx}{x\sqrt{a^2-x^2}}=\frac1a\ln\left|\frac{a-\sqrt{a^2-x^2}}x\right|+C.
$$

$\blacksquare$

---

## 4.2-2-9

Find $\int\sqrt{7+x-x^2}\,\mathrm dx$.

### Solution 4.2-2-9

Completing the square: $7+x-x^2=\frac{29}4-\left(x-\frac12\right)^2$. Let $u=x-\frac12$. By **Theorem 2.1 (First Substitution Rule)** and 4.2-2-1,

$$
\int\sqrt{7+x-x^2}\,\mathrm dx=\frac{29}8\arcsin\frac{2x-1}{\sqrt{29}}+\frac{2x-1}4\sqrt{7+x-x^2}+C.
$$

$\blacksquare$

---

## 4.2-2-11

Find $\int\frac{\mathrm dx}{x^2\sqrt{x^2+a^2}}$ ($a> 0$).

### Solution 4.2-2-11

Let $x=a\tan t$. By **Theorem 2.2 (Second Substitution Rule)**,

$$
\int\frac{\mathrm dx}{x^2\sqrt{x^2+a^2}}=-\frac{\sqrt{x^2+a^2}}{a^2x}+C.
$$

$\blacksquare$
