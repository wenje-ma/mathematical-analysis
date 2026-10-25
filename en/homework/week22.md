# Assignment 22

> **Theorem 5.1** (Integration of Rational Expressions in Trigonometric Functions) The indefinite integral of a rational expression $R\left(\sin x,\cos x\right)$ in trigonometric functions can always be reduced to the indefinite integral of a rational function in $t$ by the universal substitution $t=\tan\frac{x}{2}$. In this case,
> 
> $$
> \begin{aligned}
> \sin x&=\frac{2t}{1+t^2},\\
> \cos x&=\frac{1-t^2}{1+t^2},\\
> \mathrm{d}x&=\frac{2\,\mathrm{d}t}{1+t^2}.
> \end{aligned}
> $$
### Problem 1

(Problem 4.5-1-1) Find the indefinite integral $\displaystyle\int\frac{\mathrm{d}x}{2+\sin x}$.

### Solution to Problem 1

By **Theorem 5.1** (Integration of Rational Expressions in Trigonometric Functions), make the universal substitution $t=\tan\frac{x}{2}$, then $\sin x=\frac{2t}{1+t^2}$, $\mathrm{d}x=\frac{2\mathrm{d}t}{1+t^2}$. Substituting gives
$$
\int\frac{\mathrm{d}x}{2+\sin x}=\int\frac{1}{2+\frac{2t}{1+t^2}}\cdot\frac{2\mathrm{d}t}{1+t^2}=\int\frac{\mathrm{d}t}{t^2+t+1}.
$$

Complete the square:

$$
t^2+t+1=\left(t+\frac12\right)^2+\frac34.
$$

Hence
$$
\int\frac{\mathrm{d}t}{t^2+t+1}=\frac{2}{\sqrt3}\arctan\frac{2t+1}{\sqrt3}+C=\frac{2}{\sqrt3}\arctan\frac{2\tan\left(x/2\right)+1}{\sqrt3}+C.
$$

$\blacksquare$
### Problem 2

(Problem 4.5-1-3) Find the indefinite integral $\displaystyle\int\cos^2x\,\mathrm{d}x$.

### Solution to Problem 2

Using the half-angle formula $\cos^2x=\frac{1+\cos2x}{2}$,
$$
\int\cos^2x\,\mathrm{d}x=\int\frac{1+\cos2x}{2}\,\mathrm{d}x=\frac{x}{2}+\frac{\sin2x}{4}+C.
$$

$\blacksquare$
### Problem 3

(Problem 4.5-1-5) Find the indefinite integral $\displaystyle\int\cot^2x\,\mathrm{d}x$.

### Solution to Problem 3

Using the identity $\cot^2x=\csc^2x-1$,
$$
\int\cot^2x\,\mathrm{d}x=\int\left(\csc^2x-1\right)\,\mathrm{d}x=-\cot x-x+C.
$$

$\blacksquare$
### Problem 4

(Problem 4.5-1-7) Find the indefinite integral $\displaystyle\int\frac{\mathrm{d}x}{\sin x+2\cos x}$.

### Solution to Problem 4

Write the denominator in the form $R\sin\left(x+\varphi\right)$:
$$
\sin x+2\cos x=\sqrt5\sin\left(x+\varphi\right),
$$

where $\varphi=\arctan2$. Hence
$$
\int\frac{\mathrm{d}x}{\sin x+2\cos x}=\frac{1}{\sqrt5}\int\frac{\mathrm{d}x}{\sin\left(x+\varphi\right)}=\frac{1}{\sqrt5}\ln\left|\csc\left(x+\varphi\right)-\cot\left(x+\varphi\right)\right|+C.
$$

$\blacksquare$
### Problem 5

(Problem 4.5-1-9) Find the indefinite integral $\displaystyle\int\sin^2x\cos^2x\,\mathrm{d}x$.

### Solution to Problem 5

Using the identity

$$
\sin^2x\cos^2x=\frac{\sin^22x}{4}=\frac{1-\cos4x}{8},
$$
$$
\int\sin^2x\cos^2x\,\mathrm{d}x=\int\frac{1-\cos4x}{8}\,\mathrm{d}x=\frac{x}{8}-\frac{\sin4x}{32}+C.
$$

$\blacksquare$
### Problem 6

(Problem 4.5-1-11) Find the indefinite integral $\displaystyle\int\frac{\mathrm{d}x}{x+2}$.

### Solution to Problem 6

This is a basic integral:
$$
\int\frac{\mathrm{d}x}{x+2}=\ln\left|x+2\right|+C.
$$

$\blacksquare$
### Problem 7

(Problem 4.5-1-13) Find the indefinite integral $\displaystyle\int\frac{\mathrm{d}x}{e^x-1}$.

### Solution to Problem 7

Let $t=e^x$, then $\mathrm{d}x=\frac{\mathrm{d}t}{t}$. Substituting gives
$$
\int\frac{\mathrm{d}x}{e^x-1}=\int\frac{\mathrm{d}t}{t\left(t-1\right)}=\int\left(\frac{1}{t-1}-\frac1t\right)\mathrm{d}t=\ln\left|t-1\right|-\ln\left|t\right|+C=\ln\left|\frac{e^x-1}{e^x}\right|+C=\ln\left|1-e^{-x}\right|+C.
$$

$\blacksquare$
### Problem 8

(Problem 4.5-2) Let $R\left(X,Y\right)$ be a rational expression in the variables $X$ and $Y$. Prove that the indefinite integral
$$
\int R\left(\sin^2x,\cos^2x\right)\,\mathrm{d}x
$$
can be rationalized by the substitution $t=\tan x$.

### Solution to Problem 8

Let $t=\tan x$, then $x=\arctan t$, $\mathrm{d}x=\frac{\mathrm{d}t}{1+t^2}$. Moreover,
$$
\sin^2x=\frac{t^2}{1+t^2},\cos^2x=\frac{1}{1+t^2}.
$$

Substituting into the integrand:
$$
R\left(\sin^2x,\cos^2x\right)\,\mathrm{d}x=R\left(\frac{t^2}{1+t^2},\frac{1}{1+t^2}\right)\cdot\frac{\mathrm{d}t}{1+t^2}.
$$

The right-hand side is a rational function in $t$ (since $R$ is a rational expression, and both $\frac{t^2}{1+t^2}$ and $\frac{1}{1+t^2}$ are rational functions of $t$). Hence the original integral can be rationalized by $t=\tan x$. $\blacksquare$
