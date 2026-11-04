# week22

> **Theorem 1.3 (Necessary and Sufficient Condition for Continuity)**
> 
> $f$ is continuous at $x_0$ iff $\omega_f\left(x_0\right)=0$.

> **Theorem 2.1 (First Substitution Rule)**
> 
> If $F'\left(u\right)=f\left(u\right)$ and $u=\varphi\left(x\right)$ is differentiable, then $\int f\left(\varphi\left(x\right)\right)\varphi'\left(x\right)\,\mathrm dx=F\left(\varphi\left(x\right)\right)+C$.

> **Theorem 4.1 (Partial Fraction Decomposition)**
> 
> Any rational function $\frac{P\left(x\right)}{Q\left(x\right)}$ can be decomposed into a polynomial plus partial fractions of the form $\frac{A}{\left(x-a\right)^k}$ or $\frac{Bx+C}{\left(x^2+px+q\right)^m}$.

> **Theorem 5.1 (Integrals of Rational Trigonometric Expressions)**
> 
> The integral of $R\left(\sin x,\cos x\right)$ can always be rationalized by the substitution $t=\tan\frac x2$, with $\sin x=\frac{2t}{1+t^2}$, $\cos x=\frac{1-t^2}{1+t^2}$, $\mathrm dx=\frac{2\mathrm dt}{1+t^2}$.

## 4.4-12

Find $\int\frac{e^t}{e^{2t}+5e^t+6}\,\mathrm dt$.

### Solution to 4.4-12

Let $u=e^t$. By **Theorem 4.1 (Partial Fraction Decomposition)**,

$$
\int\frac{e^t}{e^{2t}+5e^t+6}\,\mathrm dt=\ln\frac{e^t+2}{e^t+3}+C.
$$

$\blacksquare$

## 4.4-14

Find $\int\frac{\mathrm dx}{\left(x^2+4\right)^2\left(x+1\right)}$.

### Solution to 4.4-14

By **Theorem 4.1 (Partial Fraction Decomposition)**,

$$
\int\frac{\mathrm dx}{\left(x^2+4\right)^2\left(x+1\right)}=\frac1{25}\ln\left|x+1\right|-\frac1{50}\ln\left(x^2+4\right)+\frac{13}{400}\arctan\frac x2+\frac{x+4}{40\left(x^2+4\right)}+C.
$$

$\blacksquare$

## 4.5-1-1

Find $\int\frac{\mathrm dx}{2+\sin x}$.

### Solution to 4.5-1-1

By **Theorem 5.1 (Integrals of Rational Trigonometric Expressions)** with $t=\tan\frac x2$,

$$
\int\frac{\mathrm dx}{2+\sin x}=\frac2{\sqrt3}\arctan\frac{2\tan\left(x/2\right)+1}{\sqrt3}+C.
$$

$\blacksquare$

## 4.5-1-3

Find $\int\cos^2x\,\mathrm dx$.

### Solution to 4.5-1-3

Using $\cos^2x=\frac{1+\cos2x}2$,

$$
\int\cos^2x\,\mathrm dx=\frac x2+\frac{\sin2x}4+C.
$$

$\blacksquare$

## 4.5-1-5

Find $\int\cot^2x\,\mathrm dx$.

### Solution to 4.5-1-5

Using $\cot^2x=\csc^2x-1$,

$$
\int\cot^2x\,\mathrm dx=-\cot x-x+C.
$$

$\blacksquare$

## 4.5-1-7

Find $\int\frac{\mathrm dx}{\sin x+2\cos x}$.

### Solution to 4.5-1-7

Writing the denominator as $\sqrt5\sin\left(x+\varphi\right)$,

$$
\int\frac{\mathrm dx}{\sin x+2\cos x}=\frac1{\sqrt5}\ln\left|\csc\left(x+\varphi\right)-\cot\left(x+\varphi\right)\right|+C.
$$

$\blacksquare$

## 4.5-1-9

Find $\int\sin^2x\cos^2x\,\mathrm dx$.

### Solution to 4.5-1-9

Using $\sin^2x\cos^2x=\frac{1-\cos4x}8$,

$$
\int\sin^2x\cos^2x\,\mathrm dx=\frac x8-\frac{\sin4x}{32}+C.
$$

$\blacksquare$

## 4.5-1-11

Find $\int\frac{\mathrm dx}{x+2}$.

### Solution to 4.5-1-11

$$
\int\frac{\mathrm dx}{x+2}=\ln\left|x+2\right|+C.
$$

$\blacksquare$

## 4.5-1-13

Find $\int\frac{\mathrm dx}{e^x-1}$.

### Solution to 4.5-1-13

Let $t=e^x$. Then

$$
\int\frac{\mathrm dx}{e^x-1}=\ln\left|1-e^{-x}\right|+C.
$$

$\blacksquare$

## 4.5-2

Prove that $\int R\left(\sin^2x,\cos^2x\right)\,\mathrm dx$ can be rationalized by $t=\tan x$.

### Solution to 4.5-2

Let $t=\tan x$. Then $\sin^2x=\frac{t^2}{1+t^2}$, $\cos^2x=\frac1{1+t^2}$, $\mathrm dx=\frac{\mathrm dt}{1+t^2}$. The integrand becomes a rational function of $t$. $\blacksquare$

## 5.1-4

Prove:

(1) $\sup\left\{f+g\right\}\le\sup f+\sup g$;

(2) $\inf\left\{f+g\right\}\ge\inf f+\inf g$.

### Solution to 5.1-4

(1) Since $f\left(x\right)\le\sup f$ and $g\left(x\right)\le\sup g$, their sum is bounded above by $\sup f+\sup g$. By Definition of Supremum and Infimum, $\sup\left\{f+g\right\}\le\sup f+\sup g$.

(2) Similarly, $\inf\left\{f+g\right\}\ge\inf f+\inf g$. $\blacksquare$

## 5.1-5

Prove: $\omega_f\left(I\right)=\sup\left\{\left|f\left(x_1\right)-f\left(x_2\right)\right|:x_1,x_2\in I\right\}$.

### Solution to 5.1-5

Let $M=\sup f$, $m=\inf f$. Then $\omega_f=M-m$. Every $\left|f\left(x_1\right)-f\left(x_2\right)\right|\le M-m$. Conversely, for any $\varepsilon> 0$, there exist $x_1,x_2$ with $f\left(x_1\right)> M-\frac\varepsilon2$, $f\left(x_2\right)< m+\frac\varepsilon2$, giving $\left|f\left(x_1\right)-f\left(x_2\right)\right|> M-m-\varepsilon$. Hence equality. $\blacksquare$

## 5.1-6

Let $D\left(x\right)$ be the Dirichlet function. Prove $\omega_D\left(I\right)=1$ for any interval $I$, and $\omega_D\left(x_0\right)=1$ at every point.

### Solution to 5.1-6

Any interval contains both rational and irrational points, so $\sup D=1$, $\inf D=0$. Thus $\omega_D\left(I\right)=1$. By **Theorem 1.3 (Necessary and Sufficient Condition for Continuity)**, $D$ is discontinuous everywhere. $\blacksquare$
