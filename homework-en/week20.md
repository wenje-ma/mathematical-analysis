# week20

> **Theorem 1.3 (Linearity of Indefinite Integral)**
> 
> If $f$ and $g$ have antiderivatives, then $\int\left[af\left(x\right)+bg\left(x\right)\right]\mathrm dx=a\int f\left(x\right)\,\mathrm dx+b\int g\left(x\right)\,\mathrm dx$.

> **Theorem 2.1 (First Substitution Rule)**
> 
> If $F'\left(u\right)=f\left(u\right)$ and $u=\varphi\left(x\right)$ is differentiable, then $\int f\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm dx=F\left(\varphi\left(x\right)\right)+C$.

> **Theorem 2.2 (Second Substitution Rule)**
> 
> If $x=\varphi\left(t\right)$ is differentiable with inverse, and $\int f\left(\varphi\left(t\right)\right)\varphi'\left(t\right)\,\mathrm dt=G\left(t\right)+C$, then $\int f\left(x\right)\,\mathrm dx=G\left(\varphi^{-1}\left(x\right)\right)+C$.

## 4.1-1-6

Find $\int\left(3^x-4^{-x}\right)^2\,\mathrm dx$.

### Solution to 4.1-1-6

Expanding: $9^x-2\left(\frac34\right)^x+16^{-x}$. By **Theorem 1.3 (Linearity of Indefinite Integral)** and $\int a^x\,\mathrm dx=\frac{a^x}{\ln a}+C$,

$$
\int\left(3^x-4^{-x}\right)^2\,\mathrm dx=\frac{9^x}{\ln9}-2\cdot\frac{\left(3/4\right)^x}{\ln\left(3/4\right)}-\frac{16^{-x}}{\ln16}+C.
$$

$\blacksquare$

## 4.1-1-8

Find $\int\frac{x^2}{1+x^2}\,\mathrm dx$.

### Solution to 4.1-1-8

Since $\frac{x^2}{1+x^2}=1-\frac1{1+x^2}$,

$$
\int\frac{x^2}{1+x^2}\,\mathrm dx=x-\arctan x+C.
$$

$\blacksquare$

## 4.1-1-10

Find $\int\left(a\,\mathrm{sh}\,x+b\,\mathrm{ch}\,x\right)\,\mathrm dx$.

### Solution to 4.1-1-10

Since $\left(\mathrm{sh}\,x\right)'=\mathrm{ch}\,x$ and $\left(\mathrm{ch}\,x\right)'=\mathrm{sh}\,x$,

$$
\int\left(a\,\mathrm{sh}\,x+b\,\mathrm{ch}\,x\right)\,\mathrm dx=a\,\mathrm{ch}\,x+b\,\mathrm{sh}\,x+C.
$$

$\blacksquare$

## 4.1-1-11

Find $\int\frac1{\sin^2x\cos^2x}\,\mathrm dx$.

### Solution to 4.1-1-11

Since $\frac1{\sin^2x\cos^2x}=\sec^2x+\csc^2x$,

$$
\int\frac1{\sin^2x\cos^2x}\,\mathrm dx=\tan x-\cot x+C.
$$

$\blacksquare$

## 4.1-1-12

Find $\int\sin^2\frac x2\,\mathrm dx$.

### Solution to 4.1-1-12

Using $\sin^2\frac x2=\frac{1-\cos x}2$,

$$
\int\sin^2\frac x2\,\mathrm dx=\frac x2-\frac{\sin x}2+C.
$$

$\blacksquare$

## 4.1-2

Prove: $\int\frac{\mathrm dx}{x^2+a^2}=\frac1a\arctan\frac xa+C$ ($a> 0$).

### Solution to 4.1-2

Differentiating the right side:

$$
\left(\frac1a\arctan\frac xa\right)'=\frac1{a^2+x^2}.
$$

By Definition of Antiderivative and Indefinite Integral, this is an antiderivative. $\blacksquare$

## 4.1-4

Prove: $\int\frac{\mathrm dx}{\sqrt{a^2-x^2}}=\arcsin\frac xa+C$ ($a> 0$).

### Solution to 4.1-4

Differentiating:

$$
\left(\arcsin\frac xa\right)'=\frac1{\sqrt{a^2-x^2}}.
$$

By Definition of Antiderivative and Indefinite Integral, this is an antiderivative. $\blacksquare$

## 4.2-1-2

Find $\int\sqrt{2x+3}\,\mathrm dx$.

### Solution to 4.2-1-2

Let $u=2x+3$. By **Theorem 2.1 (First Substitution Rule)**,

$$
\int\sqrt{2x+3}\,\mathrm dx=\frac13\left(2x+3\right)^{3/2}+C.
$$

$\blacksquare$

## 4.2-1-4

Find $\int\frac{\mathrm dx}{\left(x-1\right)^5}$.

### Solution to 4.2-1-4

Let $u=x-1$. By **Theorem 2.1 (First Substitution Rule)**,

$$
\int\frac{\mathrm dx}{\left(x-1\right)^5}=-\frac1{4\left(x-1\right)^4}+C.
$$

$\blacksquare$

## 4.2-1-6

Find $\int\mathrm{sh}\,x\,\mathrm dx$.

### Solution to 4.2-1-6

Since $\left(\mathrm{ch}\,x\right)'=\mathrm{sh}\,x$, $\int\mathrm{sh}\,x\,\mathrm dx=\mathrm{ch}\,x+C$. $\blacksquare$

## 4.2-1-8

Find $\int\frac{\mathrm dx}{a^2+b^2x^2}$ ($a,b> 0$).

### Solution to 4.2-1-8

Let $u=\frac{bx}{a}$. By **Theorem 2.1 (First Substitution Rule)**,

$$
\int\frac{\mathrm dx}{a^2+b^2x^2}=\frac1{ab}\arctan\frac{bx}{a}+C.
$$

$\blacksquare$

## 4.2-1-10

Find $\int\frac{\mathrm dx}{\sin x+\cos x}$.

### Solution to 4.2-1-10

Using $\sin x+\cos x=\sqrt2\sin\left(x+\frac\pi4\right)$ and letting $u=x+\frac\pi4$,

$$
\int\frac{\mathrm dx}{\sin x+\cos x}=\frac1{\sqrt2}\ln\left|\csc u-\cot u\right|+C.
$$

$\blacksquare$

## 4.2-2-1

Find $\int\sqrt{a^2-x^2}\,\mathrm dx$ ($a> 0$).

### Solution to 4.2-2-1

Let $x=a\sin t$. By **Theorem 2.2 (Second Substitution Rule)**,

$$
\int\sqrt{a^2-x^2}\,\mathrm dx=\frac{a^2}2\arcsin\frac xa+\frac x2\sqrt{a^2-x^2}+C.
$$

$\blacksquare$

## 4.2-2-3

Find $\int\frac{\mathrm dx}{\sqrt{x^2+a^2}}$ ($a> 0$).

### Solution to 4.2-2-3

Let $x=a\tan t$. By **Theorem 2.2 (Second Substitution Rule)**,

$$
\int\frac{\mathrm dx}{\sqrt{x^2+a^2}}=\ln\left(x+\sqrt{x^2+a^2}\right)+C'.
$$

$\blacksquare$

## 4.2-2-5

Find $\int\sqrt{x^2-a^2}\,\mathrm dx$ ($a> 0$).

### Solution to 4.2-2-5

Let $x=a\sec t$. By **Theorem 2.2 (Second Substitution Rule)**,

$$
\int\sqrt{x^2-a^2}\,\mathrm dx=\frac x2\sqrt{x^2-a^2}-\frac{a^2}2\ln\left|x+\sqrt{x^2-a^2}\right|+C.
$$

$\blacksquare$
