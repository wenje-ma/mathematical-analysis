# week18

> **Basic Knowledge: Definition of Antiderivative and Indefinite Integral**<br>If $F'\left(x\right)=f\left(x\right)$ on $\left(a,b\right)$, $F$ is an antiderivative of $f$. The collection $F\left(x\right)+C$ is the indefinite integral, denoted $\int f\left(x\right)\,\mathrm dx=F\left(x\right)+C$.

> **Theorem 1.3 (Linearity of Indefinite Integral)**<br>If $f$ and $g$ have antiderivatives, then $\int\left[af\left(x\right)+bg\left(x\right)\right]\mathrm dx=a\int f\left(x\right)\,\mathrm dx+b\int g\left(x\right)\,\mathrm dx$.

---

## 4.1-1-1

Find $\int\left(x^3+4\right)\,\mathrm dx$.

### Solution 4.1-1-1

By **Theorem 1.3 (Linearity of Indefinite Integral)**,

$$
\int\left(x^3+4\right)\,\mathrm dx=\frac{x^4}4+4x+C.
$$

$\blacksquare$

---

## 4.1-1-4

Find $\int\tan^2x\,\mathrm dx$.

### Solution 4.1-1-4

Using $\tan^2x=\sec^2x-1$ and **Theorem 1.3 (Linearity of Indefinite Integral)**,

$$
\int\tan^2x\,\mathrm dx=\tan x-x+C.
$$

$\blacksquare$

---

## 4.1-1-6

Find $\int\left(3^x-4^{-x}\right)^2\,\mathrm dx$.

### Solution 4.1-1-6

Expanding: $9^x-2\left(\frac34\right)^x+16^{-x}$. By **Theorem 1.3 (Linearity of Indefinite Integral)** and $\int a^x\,\mathrm dx=\frac{a^x}{\ln a}+C$,

$$
\int\left(3^x-4^{-x}\right)^2\,\mathrm dx=\frac{9^x}{\ln9}-2\cdot\frac{\left(3/4\right)^x}{\ln\left(3/4\right)}-\frac{16^{-x}}{\ln16}+C.
$$

$\blacksquare$

---

## 4.1-1-8

Find $\int\frac{x^2}{1+x^2}\,\mathrm dx$.

### Solution 4.1-1-8

Since $\frac{x^2}{1+x^2}=1-\frac1{1+x^2}$,

$$
\int\frac{x^2}{1+x^2}\,\mathrm dx=x-\arctan x+C.
$$

$\blacksquare$

---

## 4.1-1-10

Find $\int\left(a\,\mathrm{sh}\,x+b\,\mathrm{ch}\,x\right)\,\mathrm dx$.

### Solution 4.1-1-10

Since $\left(\mathrm{sh}\,x\right)'=\mathrm{ch}\,x$ and $\left(\mathrm{ch}\,x\right)'=\mathrm{sh}\,x$,

$$
\int\left(a\,\mathrm{sh}\,x+b\,\mathrm{ch}\,x\right)\,\mathrm dx=a\,\mathrm{ch}\,x+b\,\mathrm{sh}\,x+C.
$$

$\blacksquare$

---

## 4.1-1-11

Find $\int\frac1{\sin^2x\cos^2x}\,\mathrm dx$.

### Solution 4.1-1-11

Since $\frac1{\sin^2x\cos^2x}=\sec^2x+\csc^2x$,

$$
\int\frac1{\sin^2x\cos^2x}\,\mathrm dx=\tan x-\cot x+C.
$$

$\blacksquare$

---

## 4.1-1-12

Find $\int\sin^2\frac x2\,\mathrm dx$.

### Solution 4.1-1-12

Using $\sin^2\frac x2=\frac{1-\cos x}2$,

$$
\int\sin^2\frac x2\,\mathrm dx=\frac x2-\frac{\sin x}2+C.
$$

$\blacksquare$

---

## 4.1-2

Prove: $\int\frac{\mathrm dx}{x^2+a^2}=\frac1a\arctan\frac xa+C$ ($a> 0$).

### Solution 4.1-2

Differentiating the right side:

$$
\left(\frac1a\arctan\frac xa\right)'=\frac1{a^2+x^2}.
$$

By **Basic Knowledge: Definition of Antiderivative and Indefinite Integral**, this is an antiderivative. $\blacksquare$

---

## 4.1-4

Prove: $\int\frac{\mathrm dx}{\sqrt{a^2-x^2}}=\arcsin\frac xa+C$ ($a> 0$).

### Solution 4.1-4

Differentiating:

$$
\left(\arcsin\frac xa\right)'=\frac1{\sqrt{a^2-x^2}}.
$$

By **Basic Knowledge: Definition of Antiderivative and Indefinite Integral**, this is an antiderivative. $\blacksquare$
