# week9

> **Theorem 2.1 (Chain Rule)**<br>If $y=f\left(u\right)$ is differentiable at $u$ and $u=g\left(x\right)$ is differentiable at $x$, then $y=f\left(g\left(x\right)\right)$ is differentiable at $x$ and $\frac{\mathrm dy}{\mathrm dx}=\frac{\mathrm dy}{\mathrm du}\cdot\frac{\mathrm du}{\mathrm dx}=f'\left(g\left(x\right)\right)g'\left(x\right)$.

---

## 2.2-2

Let $f\left(x\right)=1+x^2$. Find $f'\left(\sin x\right)$ and $\left[f\left(\sin x\right)\right]'$.

### Solution 2.2-2

$f'\left(x\right)=2x$, so $f'\left(\sin x\right)=2\sin x$.

By **Theorem 2.1 (Chain Rule)**,

$$
\left[f\left(\sin x\right)\right]'=f'\left(\sin x\right)\cdot\left(\sin x\right)'=2\sin x\cos x=\sin2x.
$$

$\blacksquare$

---

## 2.2-3-2

Differentiate: $y=\sqrt{1+x^2}$.

### Solution 2.2-3-2

$$
y'=\frac1{2\sqrt{1+x^2}}\cdot\left(1+x^2\right)'=\frac{2x}{2\sqrt{1+x^2}}=\frac{x}{\sqrt{1+x^2}}.
$$

$\blacksquare$

---

## 2.2-3-4

Differentiate: $y=\frac12\sqrt{a^2-x^2}$.

### Solution 2.2-3-4

$$
y'=\frac12\cdot\frac1{2\sqrt{a^2-x^2}}\cdot\left(-2x\right)=-\frac{x}{2\sqrt{a^2-x^2}}.
$$

$\blacksquare$

---

## 2.2-3-6

Differentiate: $y=\frac12\left(e^x-e^{-x}\right)$.

### Solution 2.2-3-6

$$
y'=\frac12\left(e^x-\left(-e^{-x}\right)\right)=\frac12\left(e^x+e^{-x}\right).
$$

$\blacksquare$

---

## 2.2-3-8

Differentiate: $y=\sqrt{x^3+x+1}$.

### Solution 2.2-3-8

$$
y'=\frac1{2\sqrt{x^3+x+1}}\cdot\left(3x^2+1\right)=\frac{3x^2+1}{2\sqrt{x^3+x+1}}.
$$

$\blacksquare$

---

## 2.2-3-10

Differentiate: $y=e^x+e^{x^2}+\cos x^2$.

### Solution 2.2-3-10

$$
y'=e^x+e^{x^2}\cdot2x-\sin x^2\cdot2x=e^x+2xe^{x^2}-2x\sin x^2.
$$

$\blacksquare$

---

## 2.2-3-12

Differentiate: $y=\arctan x^2$.

### Solution 2.2-3-12

$$
y'=\frac1{1+\left(x^2\right)^2}\cdot2x=\frac{2x}{1+x^4}.
$$

$\blacksquare$

---

## 2.2-3-14

Differentiate: $y=x^{\sqrt x}$.

### Solution 2.2-3-14

Taking logs: $\ln y=\sqrt x\ln x$. Differentiating both sides:

$$
\frac{y'}y=\frac1{2\sqrt x}\ln x+\frac{\sqrt x}{x}=\frac{\ln x}{2\sqrt x}+\frac1{\sqrt x}.
$$

Thus

$$
y'=x^{\sqrt x}\left(\frac{\ln x}{2\sqrt x}+\frac1{\sqrt x}\right).
$$

$\blacksquare$

---

## 2.2-5

A flywheel of radius $r$ rotates at constant angular velocity $\omega$, connected to a piston by a rod of length $a$ ($a> r$). Let $x=x\left(t\right)$ be the distance from the flywheel center to the piston endpoint at time $t$, with $x\left(0\right)=a+r$. Find $x\left(t\right)$, $x'\left(t\right)$, and $x'\left(0\right)$.

### Solution 2.2-5

Let the flywheel angle be $\theta\left(t\right)=\omega t$. Geometrically,

$$
x\left(t\right)=r\cos\omega t+\sqrt{a^2-r^2\sin^2\omega t}.
$$

Differentiating,

$$
x'\left(t\right)=-r\omega\sin\omega t+\frac{-2r^2\omega\sin\omega t\cos\omega t}{2\sqrt{a^2-r^2\sin^2\omega t}}=-r\omega\sin\omega t\left(1+\frac{r\cos\omega t}{\sqrt{a^2-r^2\sin^2\omega t}}\right).
$$

At $t=0$, $\sin0=0$, so $x'\left(0\right)=0$. $\blacksquare$

---

## 2.2-6

Let $y=y\left(x\right)$ be the implicit function defined by the following equations. Find its derivative:

(1) $x^2+y^2=R^2$ ($y\ne0$);

(2) $y^2-2xy-x^2-2x=4$ ($y\ne x$).

### Solution 2.2-6

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
