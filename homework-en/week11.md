# week11

> **Theorem 2.1 (Chain Rule)**
> 
> If $y=f\left(u\right)$ is differentiable at $u$ and $u=g\left(x\right)$ is differentiable at $x$, then $y=f\left(g\left(x\right)\right)$ is differentiable at $x$ and $\frac{\mathrm dy}{\mathrm dx}=\frac{\mathrm dy}{\mathrm du}\cdot\frac{\mathrm du}{\mathrm dx}=f'\left(g\left(x\right)\right)g'\left(x\right)$.

## 2.2-3-14

Differentiate: $y=x^{\sqrt x}$.

### Solution to 2.2-3-14

Taking logs: $\ln y=\sqrt x\ln x$. Differentiating both sides:

$$
\frac{y'}y=\frac1{2\sqrt x}\ln x+\frac{\sqrt x}{x}=\frac{\ln x}{2\sqrt x}+\frac1{\sqrt x}.
$$

Thus

$$
y'=x^{\sqrt x}\left(\frac{\ln x}{2\sqrt x}+\frac1{\sqrt x}\right).
$$

$\blacksquare$

## 2.2-5

A flywheel of radius $r$ rotates at constant angular velocity $\omega$, connected to a piston by a rod of length $a$ ($a> r$). Let $x=x\left(t\right)$ be the distance from the flywheel center to the piston endpoint at time $t$, with $x\left(0\right)=a+r$. Find $x\left(t\right)$, $x'\left(t\right)$, and $x'\left(0\right)$.

### Solution to 2.2-5

Let the flywheel angle be $\theta\left(t\right)=\omega t$. Geometrically,

$$
x\left(t\right)=r\cos\omega t+\sqrt{a^2-r^2\sin^2\omega t}.
$$

Differentiating,

$$
x'\left(t\right)=-r\omega\sin\omega t+\frac{-2r^2\omega\sin\omega t\cos\omega t}{2\sqrt{a^2-r^2\sin^2\omega t}}=-r\omega\sin\omega t\left(1+\frac{r\cos\omega t}{\sqrt{a^2-r^2\sin^2\omega t}}\right).
$$

At $t=0$, $\sin0=0$, so $x'\left(0\right)=0$. $\blacksquare$

## 2.2-6

Let $y=y\left(x\right)$ be the implicit function defined by the following equations. Find its derivative:

(1) $x^2+y^2=R^2$ ($y\ne0$);

(2) $y^2-2xy-x^2-2x=4$ ($y\ne x$).

### Solution to 2.2-6

(1) Differentiating both sides w.r.t. $x$: $2x+2yy'=0$, so $y'=-\frac{x}{y}$.

(2) Differentiating both sides w.r.t. $x$:

$$
2yy'-2\left(y+xy'\right)-2x-2=0,
$$

which simplifies to

$$
\left(2y-2x\right)y'=2y+2x+2,
$$

so $y'=\frac{y+x+1}{y-x}$. $\blacksquare$

## 2.3-1-2

As $x\to0$, determine the order of the infinitesimal $y=\left(\sqrt{2+x}-\sqrt2\right)x$.

### Solution to 2.3-1-2

$$
\sqrt{2+x}-\sqrt2=\frac{x}{\sqrt{2+x}+\sqrt2}\sim\frac{x}{2\sqrt2}.
$$

Thus $y\sim\frac{x^2}{2\sqrt2}$; by Definition of Higher-Order Infinitesimal, $y$ is a second-order infinitesimal in $x$. $\blacksquare$

## 2.3-1-4

As $x\to0$, determine the order of the infinitesimal $y=\ln\left(1+x^2\right)+x^3$.

### Solution to 2.3-1-4

$\ln\left(1+x^2\right)\sim x^2$ and $x^3=o\left(x^2\right)$. By Definition of Higher-Order Infinitesimal, $y\sim x^2$, which is second-order. $\blacksquare$

## 2.3-3-1

Compute the differential at $x_0$: $f\left(x\right)=x^2\arcsin x$, $x_0=0$.

### Solution to 2.3-3-1

$$
f'\left(x\right)=2x\arcsin x+\frac{x^2}{\sqrt{1-x^2}}.
$$

$f'\left(0\right)=0$. Hence $\mathrm df\big|_{x_0=0}=0\cdot\mathrm dx=0$. $\blacksquare$

## 2.3-3-4

Compute the differential at $x_0$: $f\left(x\right)=x\ln\left(1+x\right)$, $x_0=0$.

### Solution to 2.3-3-4

$f'\left(x\right)=\ln\left(1+x\right)+\frac{x}{1+x}$. $f'\left(0\right)=0$. Hence $\mathrm df\big|_{x_0=0}=0$. $\blacksquare$

## 2.3-4-2

Find the differential: $f\left(x\right)=\ln\left(x+\sqrt{x^2+1}\right)$.

### Solution to 2.3-4-2

$$
f'\left(x\right)=\frac1{x+\sqrt{x^2+1}}\cdot\left(1+\frac{x}{\sqrt{x^2+1}}\right)=\frac1{x+\sqrt{x^2+1}}\cdot\frac{\sqrt{x^2+1}+x}{\sqrt{x^2+1}}=\frac1{\sqrt{x^2+1}}.
$$

Hence $\mathrm df=\frac1{\sqrt{x^2+1}}\mathrm dx$. $\blacksquare$

## 2.3-4-4

Find the differential: $f\left(x\right)=\sqrt{1+x^2}+\sqrt x\sin x$.

### Solution to 2.3-4-4

$$
f'\left(x\right)=\frac{x}{\sqrt{1+x^2}}+\frac1{2\sqrt x}\sin x+\sqrt x\cos x.
$$

Hence

$$
\mathrm df=\left(\frac{x}{\sqrt{1+x^2}}+\frac{\sin x}{2\sqrt x}+\sqrt x\cos x\right)\mathrm dx.
$$

$\blacksquare$

## 2.3-5-1

Fill in: $\mathrm d\left(\right)=x^n\mathrm dx$.

### Solution to 2.3-5-1

$$
\mathrm d\left(\frac{x^{n+1}}{n+1}\right)=x^n\mathrm dx\quad\left(n\ne-1\right).
$$

$\blacksquare$

## 2.3-5-3

Fill in: $\mathrm d\left(\right)=\left(e^x+\sin2x\right)\mathrm dx$.

### Solution to 2.3-5-3

$$
\mathrm d\left(e^x-\frac12\cos2x\right)=\left(e^x+\sin2x\right)\mathrm dx.
$$

$\blacksquare$

## 2.3-5-5

Fill in: $\mathrm d\left(\right)=\frac{\sin x}{\cos x}\mathrm dx$.

### Solution to 2.3-5-5

$\mathrm d\left(-\ln\left|\cos x\right|\right)=\frac{\sin x}{\cos x}\mathrm dx$. $\blacksquare$

## 2.3-6

Compute the approximate value of $\tan\left(\frac\pi4+0.01\right)$.

### Solution to 2.3-6

Let $f\left(x\right)=\tan x$, $x_0=\frac\pi4$, $\Delta x=0.01$. $f'\left(x\right)=\sec^2x$, $f'\left(\frac\pi4\right)=2$. By the approximation formula from Definition of Differential,

$$
f\left(x_0+\Delta x\right)\approx f\left(x_0\right)+f'\left(x_0\right)\Delta x,
$$

$$
\tan\left(\frac\pi4+0.01\right)\approx\tan\frac\pi4+2\times0.01=1+0.02=1.02.
$$

$\blacksquare$

## 2.4-1

Find the $n$-th derivative of:

(1) $y=x^2e^x$;

(4) $y=x\ln\left(1+x\right)$.

### Solution to 2.4-1

By Definition of Higher-Order Derivatives, the $n$-th derivative is obtained by differentiating the $\left(n-1\right)$-th.

(1) By Leibniz Formula, with $u=x^2$, $v=e^x$:

$$
u'=2x,\quad u''=2,\quad u^{\left(k\right)}=0\quad\left(k\ge3\right).
$$

Thus

$$
y^{\left(n\right)}=x^2e^x+2nx e^x+n\left(n-1\right)e^x=e^x\left[x^2+2nx+n\left(n-1\right)\right].
$$

(4) $y'=\ln\left(1+x\right)+\frac{x}{1+x}$.

$$
y''=\frac1{1+x}+\frac1{\left(1+x\right)^2}=\frac{2+x}{\left(1+x\right)^2}.
$$

In general, for $n\ge2$,

$$
y^{\left(n\right)}=\left(-1\right)^n\frac{\left(n-2\right)!}{\left(1+x\right)^{n-1}}+\left(-1\right)^{n-1}\frac{\left(n-1\right)!}{\left(1+x\right)^n}.
$$

Simplifying,

$$
y^{\left(n\right)}=\left(-1\right)^n\frac{\left(n-2\right)!}{\left(1+x\right)^{n-1}}\cdot\frac{x}{1+x}\quad\left(n\ge2\right).
$$

$\blacksquare$
