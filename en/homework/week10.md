# Assignment 10

> **Definition** (Differential) Let $y=f\left(x\right)$ be defined near $x_0$. If there exists a constant $A$ such that $\Delta y=A\Delta x+o\left(\Delta x\right)$, then $f$ is said to be differentiable at $x_0$, and $\mathrm dy=A\Delta x$ is called the differential, with $A=f'\left(x_0\right)$.

> **Definition** (Higher-Order Infinitesimal) If $\lim\limits_{x\to0}\frac{\alpha\left(x\right)}{\beta\left(x\right)}=0$, then $\alpha\left(x\right)=o\left(\beta\left(x\right)\right)$.

### Problem 1

(Problem 2.3-1-2) When $x\to0$, of what order is the following infinitesimal: $y=\left(\sqrt{2+x}-\sqrt2\right)x$.

### Solution to Problem 1

$$
\sqrt{2+x}-\sqrt2=\frac{x}{\sqrt{2+x}+\sqrt2}\sim\frac{x}{2\sqrt2}.
$$

Hence $y\sim\frac{x^2}{2\sqrt2}$, and by **Definition** (Higher-Order Infinitesimal), $y$ is a second-order infinitesimal in $x$. $\blacksquare$

### Problem 2

(Problem 2.3-1-4) When $x\to0$, of what order is the following infinitesimal: $y=\ln\left(1+x^2\right)+x^3$.

### Solution to Problem 2

$\ln\left(1+x^2\right)\sim x^2$, while $x^3=o\left(x^2\right)$. By **Definition** (Higher-Order Infinitesimal), $y\sim x^2$, which is a second-order infinitesimal. $\blacksquare$

### Problem 3

(Problem 2.3-3-1) Compute the differential of the following function at the given point $x_0$:

$$
f\left(x\right)=x^2\arcsin x,x_0=0.
$$

### Solution to Problem 3


$$
f'\left(x\right)=2x\arcsin x+\frac{x^2}{\sqrt{1-x^2}}.
$$

$f'\left(0\right)=0$. Hence $\mathrm df\big|_{x_0=0}=0\cdot\mathrm dx=0$. $\blacksquare$

### Problem 4

(Problem 2.3-3-4) Compute the differential of the following function at the given point $x_0$:

$$
f\left(x\right)=x\ln\left(1+x\right),x_0=0.
$$

### Solution to Problem 4

$f'\left(x\right)=\ln\left(1+x\right)+\frac{x}{1+x}$. $f'\left(0\right)=0$. Hence $\mathrm df\big|_{x_0=0}=0$. $\blacksquare$

### Problem 5

(Problem 2.3-4-2) Find the differential of the function: $f\left(x\right)=\ln\left(x+\sqrt{x^2+1}\right)$.

### Solution to Problem 5

$$
f'\left(x\right)=\frac1{x+\sqrt{x^2+1}}\cdot\left(1+\frac{x}{\sqrt{x^2+1}}\right)=\frac1{x+\sqrt{x^2+1}}\cdot\frac{\sqrt{x^2+1}+x}{\sqrt{x^2+1}}=\frac1{\sqrt{x^2+1}}.
$$

Hence $\mathrm df=\frac1{\sqrt{x^2+1}}\mathrm dx$. $\blacksquare$

### Problem 6

(Problem 2.3-4-4) Find the differential of the function:

$$
f\left(x\right)=\sqrt{1+x^2}+\sqrt x\sin x.
$$

### Solution to Problem 6

$$
f'\left(x\right)=\frac{x}{\sqrt{1+x^2}}+\frac1{2\sqrt x}\sin x+\sqrt x\cos x.
$$

Hence

$$
\mathrm df=\left(\frac{x}{\sqrt{1+x^2}}+\frac{\sin x}{2\sqrt x}+\sqrt x\cos x\right)\mathrm dx.
$$

$\blacksquare$

### Problem 7

(Problem 2.3-5-1) Fill in the blank: $\mathrm d\left(\right)=x^n\mathrm dx$.

### Solution to Problem 7


$$
\mathrm d\left(\frac{x^{n+1}}{n+1}\right)=x^n\mathrm dx\left(n\ne-1\right).
$$

$\blacksquare$

### Problem 8

(Problem 2.3-5-3) Fill in the blank: $\mathrm d\left(\right)=\left(e^x+\sin2x\right)\mathrm dx$.

### Solution to Problem 8


$$
\mathrm d\left(e^x-\frac12\cos2x\right)=\left(e^x+\sin2x\right)\mathrm dx.
$$

$\blacksquare$

### Problem 9

(Problem 2.3-5-5) Fill in the blank: $\mathrm d\left(\right)=\frac{\sin x}{\cos x}\mathrm dx$.

### Solution to Problem 9

$\mathrm d\left(-\ln\left|\cos x\right|\right)=\frac{\sin x}{\cos x}\mathrm dx$. $\blacksquare$

### Problem 10

(Problem 2.3-6) Compute the approximate value of $\tan\left(\frac\pi4+0.01\right)$.

### Solution to Problem 10

Set $f\left(x\right)=\tan x$, take $x_0=\frac\pi4$, $\Delta x=0.01$. $f'\left(x\right)=\sec^2x$, $f'\left(\frac\pi4\right)=2$. By the approximation formula

$$
f\left(x_0+\Delta x\right)\approx f\left(x_0\right)+f'\left(x_0\right)\Delta x,
$$

$$
\tan\left(\frac\pi4+0.01\right)\approx\tan\frac\pi4+2\times0.01=1+0.02=1.02.

$$

$\blacksquare$