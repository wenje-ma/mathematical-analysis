# Assignment 9

> **Theorem 2.1** (Chain Rule for Differentiation) Let $y=f\left(u\right)$ be differentiable at $u$, and $u=g\left(x\right)$ be differentiable at $x$. Then the composite function $y=f\left(g\left(x\right)\right)$ is differentiable at $x$, and
> $$
> \frac{\mathrm dy}{\mathrm dx}=\frac{\mathrm dy}{\mathrm du}\cdot\frac{\mathrm du}{\mathrm dx}=f'\left(g\left(x\right)\right)g'\left(x\right).
> $$

### Problem 1

(Problem 2.2-2) Let $f\left(x\right)=1+x^2$. Find $f'\left(\sin x\right)$ and $\left[f\left(\sin x\right)\right]'$.

### Solution to Problem 1

$f'\left(x\right)=2x$, so $f'\left(\sin x\right)=2\sin x$.

By **Theorem 2.1** (Chain Rule for Differentiation),

$$
\left[f\left(\sin x\right)\right]'=f'\left(\sin x\right)\cdot\left(\sin x\right)'=2\sin x\cos x=\sin2x.

$$

$\blacksquare$
### Problem 2

(Problem 2.2-3-2) Find the derivative: $y=\sqrt{1+x^2}$.

### Solution to Problem 2

$$
y'=\frac1{2\sqrt{1+x^2}}\cdot\left(1+x^2\right)'=\frac{2x}{2\sqrt{1+x^2}}=\frac{x}{\sqrt{1+x^2}}.

$$

$\blacksquare$
### Problem 3

(Problem 2.2-3-4) Find the derivative: $y=\frac12\sqrt{a^2-x^2}$.

### Solution to Problem 3

$$
y'=\frac12\cdot\frac1{2\sqrt{a^2-x^2}}\cdot\left(-2x\right)=-\frac{x}{2\sqrt{a^2-x^2}}.

$$

$\blacksquare$
### Problem 4

(Problem 2.2-3-6) Find the derivative: $y=\frac12\left(e^x-e^{-x}\right)$.

### Solution to Problem 4

$$
y'=\frac12\left(e^x-\left(-e^{-x}\right)\right)=\frac12\left(e^x+e^{-x}\right).

$$

$\blacksquare$
### Problem 5

(Problem 2.2-3-8) Find the derivative: $y=\sqrt{x^3+x+1}$.

### Solution to Problem 5

$$
y'=\frac1{2\sqrt{x^3+x+1}}\cdot\left(3x^2+1\right)=\frac{3x^2+1}{2\sqrt{x^3+x+1}}.

$$

$\blacksquare$
### Problem 6

(Problem 2.2-3-10) Find the derivative: $y=e^x+e^{x^2}+\cos x^2$.

### Solution to Problem 6

$$
y'=e^x+e^{x^2}\cdot2x-\sin x^2\cdot2x=e^x+2xe^{x^2}-2x\sin x^2.

$$

$\blacksquare$
### Problem 7

(Problem 2.2-3-12) Find the derivative: $y=\arctan x^2$.

### Solution to Problem 7

$$
y'=\frac1{1+\left(x^2\right)^2}\cdot2x=\frac{2x}{1+x^4}.

$$

$\blacksquare$
### Problem 8

(Problem 2.2-3-14) Find the derivative: $y=x^{\sqrt x}$.

### Solution to Problem 8

Take logarithms: $\ln y=\sqrt x\ln x$. Differentiating both sides:

$$
\frac{y'}y=\frac1{2\sqrt x}\ln x+\frac{\sqrt x}{x}=\frac{\ln x}{2\sqrt x}+\frac1{\sqrt x}.
$$

Hence

$$
y'=x^{\sqrt x}\left(\frac{\ln x}{2\sqrt x}+\frac1{\sqrt x}\right).

$$

$\blacksquare$
### Problem 9

(Problem 2.2-5) A flywheel of radius $r$ rotates with constant angular velocity $\omega$, and the connecting rod has length $a\left(a>r\right)$. Let $x=x\left(t\right)$ be the distance from the center of the flywheel to the piston endpoint at time $t$, with $x\left(0\right)=a+r$. Give an expression for $x\left(t\right)$, and find $x'\left(t\right)$ and $x'\left(0\right)$.

### Solution to Problem 9

Let the flywheel rotation angle be $\theta\left(t\right)=\omega t$. By the geometry,

$$
x\left(t\right)=r\cos\omega t+\sqrt{a^2-r^2\sin^2\omega t}.
$$

Differentiating:

$$
x'\left(t\right)=-r\omega\sin\omega t+\frac{-2r^2\omega\sin\omega t\cos\omega t}{2\sqrt{a^2-r^2\sin^2\omega t}}=-r\omega\sin\omega t\left(1+\frac{r\cos\omega t}{\sqrt{a^2-r^2\sin^2\omega t}}\right).
$$

Substituting $t=0$: $\sin0=0$, so $x'\left(0\right)=0$. $\blacksquare$

### Problem 10

(Problem 2.2-6) Let $y=y\left(x\right)$ be an implicit function determined by the following equations. Find its derivative:
(1) $x^2+y^2=R^2\left(y\ne0\right)$;

(2)

$$
y^2-2xy-x^2-2x=4\left(y\ne x\right).
$$

### Solution to Problem 10

(1) Differentiating both sides with respect to $x$: $2x+2yy'=0$, so $y'=-\frac{x}{y}$.

(2) Differentiating both sides with respect to $x$:

$$
2yy'-2\left(y+xy'\right)-2x-2=0,
$$
which simplifies to

$$
\left(2y-2x\right)y'=2y+2x+2,
$$

so $y'=\frac{y+x+1}{y-x}$. $\blacksquare$
