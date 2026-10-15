# Assignment 18

> **Definition** (Antiderivative and Indefinite Integral) Let $y=f\left(x\right)$ be defined on an interval $\left(a,b\right)$. If $F\left(x\right)$ is differentiable on $\left(a,b\right)$ and $F'\left(x\right)=f\left(x\right)$ ($\forall x\in\left(a,b\right)$), then $y=F\left(x\right)$ is called an antiderivative of $y=f\left(x\right)$. All antiderivatives $F\left(x\right)+C$ of $f\left(x\right)$ (where $C$ is an arbitrary constant) are called the indefinite integral of $f\left(x\right)$, denoted by
> $$
> \int f\left(x\right)\,\mathrm{d}x=F\left(x\right)+C.
> $$
> **Theorem 1.3** (Linearity Rule for Indefinite Integrals) Let $y=f\left(x\right)$ and $y=g\left(x\right)$ have antiderivatives on some interval. Then
> $$
> \int\left[af\left(x\right)+bg\left(x\right)\right]\mathrm{d}x=a\int f\left(x\right)\,\mathrm{d}x+b\int g\left(x\right)\,\mathrm{d}x,
> $$
> where $a,b$ are two arbitrary constants.

### Problem 1

(Problem 4.1-1-1) Find the indefinite integral $\displaystyle\int\left(x^3+4\right)\,\mathrm{d}x$.

### Solution to Problem 1

By **Theorem 1.3** (Linearity Rule for Indefinite Integrals),
$$
\int\left(x^3+4\right)\,\mathrm{d}x=\int x^3\,\mathrm{d}x+4\int 1\,\mathrm{d}x=\frac{x^4}{4}+4x+C.
$$

$\blacksquare$
### Problem 2

(Problem 4.1-1-4) Find the indefinite integral $\displaystyle\int\tan^2x\,\mathrm{d}x$.

### Solution to Problem 2

Using the trigonometric identity $\tan^2x=\sec^2x-1$, by **Theorem 1.3** (Linearity Rule for Indefinite Integrals),
$$
\int\tan^2x\,\mathrm{d}x=\int\left(\sec^2x-1\right)\,\mathrm{d}x=\int\sec^2x\,\mathrm{d}x-\int1\,\mathrm{d}x=\tan x-x+C.
$$

$\blacksquare$
### Problem 3

(Problem 4.1-1-6) Find the indefinite integral $\displaystyle\int\left(3^x-4^{-x}\right)^2\,\mathrm{d}x$.

### Solution to Problem 3

Expand the integrand:
$$
\left(3^x-4^{-x}\right)^2=9^x-2\cdot3^x\cdot4^{-x}+16^{-x}=9^x-2\cdot\left(\frac34\right)^x+16^{-x}.
$$

By **Theorem 1.3** (Linearity Rule for Indefinite Integrals) and the integral formula for exponential functions $\displaystyle\int a^x\,\mathrm{d}x=\frac{a^x}{\ln a}+C$,
$$
\int\left(3^x-4^{-x}\right)^2\,\mathrm{d}x=\frac{9^x}{\ln9}-2\cdot\frac{\left(3/4\right)^x}{\ln\left(3/4\right)}+\frac{16^{-x}}{-\ln16}+C.
$$

$\blacksquare$
### Problem 4

(Problem 4.1-1-8) Find the indefinite integral $\displaystyle\int\frac{x^2}{1+x^2}\,\mathrm{d}x$.

### Solution to Problem 4

Rewrite the integrand:
$$
\frac{x^2}{1+x^2}=\frac{x^2+1-1}{1+x^2}=1-\frac{1}{1+x^2}.
$$

By **Theorem 1.3** (Linearity Rule for Indefinite Integrals),
$$
\int\frac{x^2}{1+x^2}\,\mathrm{d}x=\int1\,\mathrm{d}x-\int\frac{1}{1+x^2}\,\mathrm{d}x=x-\arctan x+C.
$$

$\blacksquare$
### Problem 5

(Problem 4.1-1-10) Find the indefinite integral $\displaystyle\int\left(a\,\mathrm{sh}\,x+b\,\mathrm{ch}\,x\right)\,\mathrm{d}x$ ($a,b$ are constants).

### Solution to Problem 5

Since $\left(\mathrm{sh}\,x\right)'=\mathrm{ch}\,x$, $\left(\mathrm{ch}\,x\right)'=\mathrm{sh}\,x$, and by **Theorem 1.3** (Linearity Rule for Indefinite Integrals),
$$
\int\left(a\,\mathrm{sh}\,x+b\,\mathrm{ch}\,x\right)\,\mathrm{d}x=a\,\mathrm{ch}\,x+b\,\mathrm{sh}\,x+C.
$$

$\blacksquare$
### Problem 6

(Problem 4.1-1-11) Find the indefinite integral $\displaystyle\int\frac{1}{\sin^2x\cos^2x}\,\mathrm{d}x$.

### Solution to Problem 6

Using the trigonometric identity $1=\sin^2x+\cos^2x$,
$$
\frac{1}{\sin^2x\cos^2x}=\frac{\sin^2x+\cos^2x}{\sin^2x\cos^2x}=\frac{1}{\cos^2x}+\frac{1}{\sin^2x}=\sec^2x+\csc^2x.
$$

By **Theorem 1.3** (Linearity Rule for Indefinite Integrals),
$$
\int\frac{1}{\sin^2x\cos^2x}\,\mathrm{d}x=\int\sec^2x\,\mathrm{d}x+\int\csc^2x\,\mathrm{d}x=\tan x-\cot x+C.
$$

$\blacksquare$
### Problem 7

(Problem 4.1-1-12) Find the indefinite integral $\displaystyle\int\sin^2\frac{x}{2}\,\mathrm{d}x$.

### Solution to Problem 7

Using the half-angle formula $\sin^2\frac{x}{2}=\frac{1-\cos x}{2}$, by **Theorem 1.3** (Linearity Rule for Indefinite Integrals),
$$
\int\sin^2\frac{x}{2}\,\mathrm{d}x=\int\frac{1-\cos x}{2}\,\mathrm{d}x=\frac12\int1\,\mathrm{d}x-\frac12\int\cos x\,\mathrm{d}x=\frac{x}{2}-\frac{\sin x}{2}+C.
$$

$\blacksquare$
### Problem 8

(Problem 4.1-2) Prove:

$$
\displaystyle\int\frac{\mathrm{d}x}{x^2+a^2}=\frac1a\arctan\frac{x}{a}+C\ \left(a>0\right).
$$

### Solution to Problem 8

Differentiate the right-hand side:
$$
\left(\frac1a\arctan\frac{x}{a}\right)'=\frac1a\cdot\frac{1}{1+\left(x/a\right)^2}\cdot\frac1a=\frac{1}{a^2+x^2}.
$$

By **Definition** (Antiderivative and Indefinite Integral), the right-hand side is an antiderivative of the integrand. Hence
$$
\int\frac{\mathrm{d}x}{x^2+a^2}=\frac1a\arctan\frac{x}{a}+C.
$$

$\blacksquare$
### Problem 9

(Problem 4.1-4) Prove:

$$
\displaystyle\int\frac{\mathrm{d}x}{\sqrt{a^2-x^2}}=\arcsin\frac{x}{a}+C\ \left(a>0\right).
$$

### Solution to Problem 9

Differentiate the right-hand side:
$$
\left(\arcsin\frac{x}{a}\right)'=\frac{1}{\sqrt{1-\left(x/a\right)^2}}\cdot\frac1a=\frac{1}{\sqrt{a^2-x^2}}.
$$

By **Definition** (Antiderivative and Indefinite Integral), the right-hand side is an antiderivative of the integrand. Hence
$$
\int\frac{\mathrm{d}x}{\sqrt{a^2-x^2}}=\arcsin\frac{x}{a}+C.
$$

$\blacksquare$