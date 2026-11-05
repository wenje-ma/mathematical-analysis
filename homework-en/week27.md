# week27

> **Theorem 2.1 (Reduction to Iterated Integrals)**
> 
> $\iint_Df\,\mathrm{d}x\mathrm{d}y=\int_a^b\mathrm{d}x\int_{\varphi_1\left(x\right)}^{\varphi_2\left(x\right)}f\left(x,y\right)\,\mathrm{d}y$.

> **Theorem 2.2 (Double Integrals in Polar Coordinates)**
> 
> $\iint_Df\,\mathrm{d}x\mathrm{d}y=\iint_{D^*}f\left(r\cos\theta,r\sin\theta\right)\,r\,\mathrm{d}r\mathrm{d}\theta$.

> **Theorem 3.1 (Change of Variables in Double Integrals)**
> 
> $\iint_Df\,\mathrm{d}x\mathrm{d}y=\iint_Gf\left(x\left(u,v\right),y\left(u,v\right)\right)\left|J\left(u,v\right)\right|\,\mathrm{d}u\mathrm{d}v$.

> **Theorem 4.2 (Triple Integral by Cross-Section)**
> 
> $\iiint_\Omega{f}\,\mathrm{d}V=\iint_D\mathrm{d}x\mathrm{d}y\int_{z_1\left(x,y\right)}^{z_2\left(x,y\right)}f\,\mathrm{d}z$.

> **Theorem 4.4 (Change of Variables in Triple Integrals)**
> 
> $\iiint_\Omega{f}=\iiint_{\Omega'}f\left(x\left(u,v,w\right),\dots\right)\left|J\right|\,\mathrm{d}u\mathrm{d}v\mathrm{d}w$. Cylindrical: $\left|J\right|=r$. Spherical: $\left|J\right|=\rho^2\sin\varphi$.

## 8.2-6

Compute $\iint_De^{-x^2-y^2}$ on the quarter annulus.

### Solution to 8.2-6

$\frac\pi4\left(e^{-1}-e^{-4}\right)$. $\blacksquare$

## 8.2-7

Compute.

### Solution to 8.2-7

(1) $-6\pi^2$. (2) $\frac\pi2$. (3) $\frac{\pi{a}^4}{8}$. (4) $4-\pi^2$. $\blacksquare$

## 8.2-8

Prove:

(1) $\left[I\left(a\right)\right]^2=\iint_{R_a}e^{-x^2-y^2}$;

(2) $J\left(a\right)\le\left[I\left(a\right)\right]^2\le{J}\left(\sqrt2a\right)$;

(3) $\lim_{a\to\infty}\int_0^ae^{-x^2}\,\mathrm{d}x=\frac{\sqrt\pi}2$.

### Solution to 8.2-8

(1) By **Theorem 2.1 (Reduction to Iterated Integrals)**.

(2) Since $D_a\subset{R}_a\subset{D}_{\sqrt2a}$, by Comparison Property of Double Integrals.

(3) $J\left(a\right)=\frac\pi4\left(1-e^{-a^2}\right)$. Squeeze theorem gives the result. $\blacksquare$

## 8.3-1

Compute $\iint_D\left(\sqrt{y/x}+\sqrt{xy}\right)$ using a change of variables.

### Solution to 8.3-1

Let $u=xy$, $v=y/x$. By **Theorem 3.1 (Change of Variables in Double Integrals)**,

$$
=8+\frac{52}{3}\ln2.
$$

$\blacksquare$

## 8.3-4

Compute $\iint_D\left(x+y\right)$.

### Solution to 8.3-4

Let $u=y/x^2$, $v=x/y^2$. By **Theorem 3.1 (Change of Variables in Double Integrals)**,

$$
=\frac3{10}\left(9^{-5/3}-4^{-5/3}\right)\left(9^{-4/3}-4^{-4/3}\right).
$$

$\blacksquare$

## 8.3-6

Find the area enclosed by $\left(\frac{x^2}{a^2}+\frac{y^2}{b^2}\right)^2=\frac{xy}{c^2}$.

### Solution to 8.3-6

Use generalized polar coordinates $x=ar\cos\theta$, $y=br\sin\theta$. By **Theorem 3.1 (Change of Variables in Double Integrals)**,

$$
m\left(D\right)=\frac{a^2b^2}{2c^2}.
$$

$\blacksquare$

## 8.4-1

Compute $\iiint_\Omega{z}^2$ over the unit ball.

### Solution to 8.4-1

By symmetry and spherical coordinates (**Theorem 4.4 (Change of Variables in Triple Integrals)**), $\frac{4\pi}{15}$. $\blacksquare$

## 8.4-2

Compute $\iiint_\Omega\left(x+y+z\right)$ over $\left\{x^2+y^2\le4,0\le{z}\le1\right\}$.

### Solution to 8.4-2

By symmetry, $\iiint{x}=\iiint{y}=0$. Cylindrical coordinates give $2\pi$. $\blacksquare$

## 8.4-3

Compute $\iiint_\Omega\left(x+y+z\right)^3$ over a ball.

### Solution to 8.4-3

Every term is odd in some variable. The result is $0$. $\blacksquare$

## 8.4-5

Compute $\iiint_\Omega\left(x^2+y^2+z^2\right)$ over an annulus.

### Solution to 8.4-5

$\frac{4\pi}5\left(b^5-a^5\right)$. $\blacksquare$

## 8.4-6

Compute $\iiint_\Omega\left(x^2+y^2\right)$ over $\left\{x^2+y^2\le{z}\le1\right\}$.

### Solution to 8.4-6

$\frac\pi6$. $\blacksquare$

## 8.4-8

Compute $\iiint_\Omega\left(x^2+y^2\right)^2$.

### Solution to 8.4-8

$\frac{\pi\left(64-43\sqrt2\right)}{420}$. $\blacksquare$
