# week22

> **Theorem 5.1 (Integrals of Rational Trigonometric Expressions)**<br>The integral of $R\left(\sin x,\cos x\right)$ can always be rationalized by the substitution $t=\tan\frac x2$, with $\sin x=\frac{2t}{1+t^2}$, $\cos x=\frac{1-t^2}{1+t^2}$, $\mathrm dx=\frac{2\mathrm dt}{1+t^2}$.

---

## 4.5-1-1

Find $\int\frac{\mathrm dx}{2+\sin x}$.

### Solution 4.5-1-1

By **Theorem 5.1 (Integrals of Rational Trigonometric Expressions)** with $t=\tan\frac x2$,

$$
\int\frac{\mathrm dx}{2+\sin x}=\frac2{\sqrt3}\arctan\frac{2\tan\left(x/2\right)+1}{\sqrt3}+C.
$$

$\blacksquare$

---

## 4.5-1-3

Find $\int\cos^2x\,\mathrm dx$.

### Solution 4.5-1-3

Using $\cos^2x=\frac{1+\cos2x}2$,

$$
\int\cos^2x\,\mathrm dx=\frac x2+\frac{\sin2x}4+C.
$$

$\blacksquare$

---

## 4.5-1-5

Find $\int\cot^2x\,\mathrm dx$.

### Solution 4.5-1-5

Using $\cot^2x=\csc^2x-1$,

$$
\int\cot^2x\,\mathrm dx=-\cot x-x+C.
$$

$\blacksquare$

---

## 4.5-1-7

Find $\int\frac{\mathrm dx}{\sin x+2\cos x}$.

### Solution 4.5-1-7

Writing the denominator as $\sqrt5\sin\left(x+\varphi\right)$,

$$
\int\frac{\mathrm dx}{\sin x+2\cos x}=\frac1{\sqrt5}\ln\left|\csc\left(x+\varphi\right)-\cot\left(x+\varphi\right)\right|+C.
$$

$\blacksquare$

---

## 4.5-1-9

Find $\int\sin^2x\cos^2x\,\mathrm dx$.

### Solution 4.5-1-9

Using $\sin^2x\cos^2x=\frac{1-\cos4x}8$,

$$
\int\sin^2x\cos^2x\,\mathrm dx=\frac x8-\frac{\sin4x}{32}+C.
$$

$\blacksquare$

---

## 4.5-1-11

Find $\int\frac{\mathrm dx}{x+2}$.

### Solution 4.5-1-11

$$
\int\frac{\mathrm dx}{x+2}=\ln\left|x+2\right|+C.
$$

$\blacksquare$

---

## 4.5-1-13

Find $\int\frac{\mathrm dx}{e^x-1}$.

### Solution 4.5-1-13

Let $t=e^x$. Then

$$
\int\frac{\mathrm dx}{e^x-1}=\ln\left|1-e^{-x}\right|+C.
$$

$\blacksquare$

---

## 4.5-2

Prove that $\int R\left(\sin^2x,\cos^2x\right)\,\mathrm dx$ can be rationalized by $t=\tan x$.

### Solution 4.5-2

Let $t=\tan x$. Then $\sin^2x=\frac{t^2}{1+t^2}$, $\cos^2x=\frac1{1+t^2}$, $\mathrm dx=\frac{\mathrm dt}{1+t^2}$. The integrand becomes a rational function of $t$. $\blacksquare$
