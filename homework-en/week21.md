# week21

> **Theorem 2.1 (First Substitution Rule)**
> 
> If $F'\left(u\right)=f\left(u\right)$ and $u=\varphi\left(x\right)$ is differentiable, then $\int f\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm dx=F\left(\varphi\left(x\right)\right)+C$.

> **Theorem 2.2 (Second Substitution Rule)**
> 
> If $x=\varphi\left(t\right)$ is differentiable with inverse, and $\int f\left(\varphi\left(t\right)\right)\varphi'\left(t\right)\,\mathrm dt=G\left(t\right)+C$, then $\int f\left(x\right)\,\mathrm dx=G\left(\varphi^{-1}\left(x\right)\right)+C$.

> **Theorem 3.1 (Integration by Parts)**
> 
> If $u\left(x\right)$ and $v\left(x\right)$ are differentiable, then $\int u\left(x\right)\,\mathrm dv\left(x\right)=u\left(x\right)v\left(x\right)-\int v\left(x\right)\,\mathrm du\left(x\right)$.

> **Theorem 4.1 (Partial Fraction Decomposition)**
> 
> Any rational function $\frac{P\left(x\right)}{Q\left(x\right)}$ can be decomposed into a polynomial plus partial fractions of the form $\frac{A}{\left(x-a\right)^k}$ or $\frac{Bx+C}{\left(x^2+px+q\right)^m}$.

## 4.2-2-7

Find $\int\frac{\mathrm dx}{x\sqrt{a^2-x^2}}$ ($a> 0$).

### Solution to 4.2-2-7

Let $x=a\sin t$. By **Theorem 2.2 (Second Substitution Rule)**,

$$
\int\frac{\mathrm dx}{x\sqrt{a^2-x^2}}=\frac1a\ln\left|\frac{a-\sqrt{a^2-x^2}}x\right|+C.
$$

$\blacksquare$

## 4.2-2-9

Find $\int\sqrt{7+x-x^2}\,\mathrm dx$.

### Solution to 4.2-2-9

Completing the square: $7+x-x^2=\frac{29}4-\left(x-\frac12\right)^2$. Let $u=x-\frac12$. By **Theorem 2.1 (First Substitution Rule)** and 4.2-2-1,

$$
\int\sqrt{7+x-x^2}\,\mathrm dx=\frac{29}8\arcsin\frac{2x-1}{\sqrt{29}}+\frac{2x-1}4\sqrt{7+x-x^2}+C.
$$

$\blacksquare$

## 4.2-2-11

Find $\int\frac{\mathrm dx}{x^2\sqrt{x^2+a^2}}$ ($a> 0$).

### Solution to 4.2-2-11

Let $x=a\tan t$. By **Theorem 2.2 (Second Substitution Rule)**,

$$
\int\frac{\mathrm dx}{x^2\sqrt{x^2+a^2}}=-\frac{\sqrt{x^2+a^2}}{a^2x}+C.
$$

$\blacksquare$

## 4.3-1-11

Find $\int x\csc^2x\,\mathrm dx$.

### Solution to 4.3-1-11

Let $u=x$, $\mathrm dv=\csc^2x\,\mathrm dx$. By **Theorem 3.1 (Integration by Parts)**,

$$
\int x\csc^2x\,\mathrm dx=-x\cot x+\ln\left|\sin x\right|+C.
$$

$\blacksquare$

## 4.3-1-13

Find $\int\sqrt{1+9x^2}\,\mathrm dx$.

### Solution to 4.3-1-13

Let $u=\sqrt{1+9x^2}$, $\mathrm dv=\mathrm dx$. By **Theorem 3.1 (Integration by Parts)**,

$$
\int\sqrt{1+9x^2}\,\mathrm dx=\frac x2\sqrt{1+9x^2}+\frac16\ln\left(3x+\sqrt{1+9x^2}\right)+C.
$$

$\blacksquare$

## 4.3-1-14

Find $\int\sec^3x\,\mathrm dx$.

### Solution to 4.3-1-14

Let $u=\sec x$, $\mathrm dv=\sec^2x\,\mathrm dx$. By **Theorem 3.1 (Integration by Parts)** and $\tan^2x=\sec^2x-1$,

$$
\int\sec^3x\,\mathrm dx=\frac12\left(\sec x\tan x+\ln\left|\sec x+\tan x\right|\right)+C.
$$

$\blacksquare$

## 4.4-2

Find $\int\frac{x^3}{x^2+x-6}\,\mathrm dx$.

### Solution to 4.4-2

By polynomial division: $x-1+\frac{7x-6}{\left(x+3\right)\left(x-2\right)}$. By **Theorem 4.1 (Partial Fraction Decomposition)**,

$$
\int\frac{x^3}{x^2+x-6}\,\mathrm dx=\frac{x^2}2-x+\frac{27}5\ln\left|x+3\right|+\frac85\ln\left|x-2\right|+C.
$$

$\blacksquare$

## 4.4-4

Find $\int\frac{4x^2}{x\left(x+2\right)}\,\mathrm dx$.

### Solution to 4.4-4

Since $\frac{4x^2}{x\left(x+2\right)}=4-\frac8{x+2}$,

$$
\int\frac{4x^2}{x\left(x+2\right)}\,\mathrm dx=4x-8\ln\left|x+2\right|+C.
$$

$\blacksquare$

## 4.4-6

Find $\int\frac{2x^2-5}{x^4-5x^2+6}\,\mathrm dx$.

### Solution to 4.4-6

By **Theorem 4.1 (Partial Fraction Decomposition)**,

$$
\int\frac{2x^2-5}{x^4-5x^2+6}\,\mathrm dx=\frac1{2\sqrt2}\ln\left|\frac{x-\sqrt2}{x+\sqrt2}\right|+\frac1{2\sqrt3}\ln\left|\frac{x-\sqrt3}{x+\sqrt3}\right|+C.
$$

$\blacksquare$

## 4.4-8

Find $\int\frac x{\left(x^2+2\right)^2}\,\mathrm dx$.

### Solution to 4.4-8

Let $u=x^2+2$. By **Theorem 2.1 (First Substitution Rule)**,

$$
\int\frac x{\left(x^2+2\right)^2}\,\mathrm dx=-\frac1{2\left(x^2+2\right)}+C.
$$

$\blacksquare$

## 4.4-10

Find $\int\frac{x^3}{\left(x-1\right)^2}\,\mathrm dx$.

### Solution to 4.4-10

Let $u=x-1$. Then

$$
\int\frac{x^3}{\left(x-1\right)^2}\,\mathrm dx=\frac{\left(x-1\right)^2}2+3\left(x-1\right)+3\ln\left|x-1\right|-\frac1{x-1}+C.
$$

$\blacksquare$
