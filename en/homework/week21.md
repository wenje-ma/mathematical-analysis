# week21

> **Theorem 2.1 (First Substitution Rule)**<br>If $F'\left(u\right)=f\left(u\right)$ and $u=\varphi\left(x\right)$ is differentiable, then $\int f\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm dx=F\left(\varphi\left(x\right)\right)+C$.

> **Theorem 4.1 (Partial Fraction Decomposition)**<br>Any rational function $\frac{P\left(x\right)}{Q\left(x\right)}$ can be decomposed into a polynomial plus partial fractions of the form $\frac{A}{\left(x-a\right)^k}$ or $\frac{Bx+C}{\left(x^2+px+q\right)^m}$.

---

## 4.4-2

Find $\int\frac{x^3}{x^2+x-6}\,\mathrm dx$.

### Solution 4.4-2

By polynomial division: $x-1+\frac{7x-6}{\left(x+3\right)\left(x-2\right)}$. By **Theorem 4.1 (Partial Fraction Decomposition)**,

$$
\int\frac{x^3}{x^2+x-6}\,\mathrm dx=\frac{x^2}2-x+\frac{27}5\ln\left|x+3\right|+\frac85\ln\left|x-2\right|+C.
$$

$\blacksquare$

---

## 4.4-4

Find $\int\frac{4x^2}{x\left(x+2\right)}\,\mathrm dx$.

### Solution 4.4-4

Since $\frac{4x^2}{x\left(x+2\right)}=4-\frac8{x+2}$,

$$
\int\frac{4x^2}{x\left(x+2\right)}\,\mathrm dx=4x-8\ln\left|x+2\right|+C.
$$

$\blacksquare$

---

## 4.4-6

Find $\int\frac{2x^2-5}{x^4-5x^2+6}\,\mathrm dx$.

### Solution 4.4-6

By **Theorem 4.1 (Partial Fraction Decomposition)**,

$$
\int\frac{2x^2-5}{x^4-5x^2+6}\,\mathrm dx=\frac1{2\sqrt2}\ln\left|\frac{x-\sqrt2}{x+\sqrt2}\right|+\frac1{2\sqrt3}\ln\left|\frac{x-\sqrt3}{x+\sqrt3}\right|+C.
$$

$\blacksquare$

---

## 4.4-8

Find $\int\frac x{\left(x^2+2\right)^2}\,\mathrm dx$.

### Solution 4.4-8

Let $u=x^2+2$. By **Theorem 2.1 (First Substitution Rule)**,

$$
\int\frac x{\left(x^2+2\right)^2}\,\mathrm dx=-\frac1{2\left(x^2+2\right)}+C.
$$

$\blacksquare$

---

## 4.4-10

Find $\int\frac{x^3}{\left(x-1\right)^2}\,\mathrm dx$.

### Solution 4.4-10

Let $u=x-1$. Then

$$
\int\frac{x^3}{\left(x-1\right)^2}\,\mathrm dx=\frac{\left(x-1\right)^2}2+3\left(x-1\right)+3\ln\left|x-1\right|-\frac1{x-1}+C.
$$

$\blacksquare$

---

## 4.4-12

Find $\int\frac{e^t}{e^{2t}+5e^t+6}\,\mathrm dt$.

### Solution 4.4-12

Let $u=e^t$. By **Theorem 4.1 (Partial Fraction Decomposition)**,

$$
\int\frac{e^t}{e^{2t}+5e^t+6}\,\mathrm dt=\ln\frac{e^t+2}{e^t+3}+C.
$$

$\blacksquare$

---

## 4.4-14

Find $\int\frac{\mathrm dx}{\left(x^2+4\right)^2\left(x+1\right)}$.

### Solution 4.4-14

By **Theorem 4.1 (Partial Fraction Decomposition)**,

$$
\int\frac{\mathrm dx}{\left(x^2+4\right)^2\left(x+1\right)}=\frac1{25}\ln\left|x+1\right|-\frac1{50}\ln\left(x^2+4\right)+\frac{13}{400}\arctan\frac x2+\frac{x+4}{40\left(x^2+4\right)}+C.
$$

$\blacksquare$
