# week31

> **Theorem 4.2 (Triple Integral by Cross-Section)**<br>$\iiint_\Omega f\,\mathrm dV=\iint_D\mathrm dx\mathrm dy\int_{z_1\left(x,y\right)}^{z_2\left(x,y\right)}f\,\mathrm dz$.

> **Theorem 4.4 (Change of Variables in Triple Integrals)**<br>$\iiint_\Omega f=\iiint_{\Omega'}f\left(x\left(u,v,w\right),\dots\right)\left|J\right|\,\mathrm du\mathrm dv\mathrm dw$. Cylindrical: $\left|J\right|=r$. Spherical: $\left|J\right|=\rho^2\sin\varphi$.

---

## 8.4-1

Compute $\iiint_\Omega z^2$ over the unit ball.

### Solution 8.4-1

By symmetry and spherical coordinates (**Theorem 4.4 (Change of Variables in Triple Integrals)**), $\frac{4\pi}{15}$. $\blacksquare$

---

## 8.4-2

Compute $\iiint_\Omega\left(x+y+z\right)$ over $\left\{x^2+y^2\le4,0\le z\le1\right\}$.

### Solution 8.4-2

By symmetry, $\iiint x=\iiint y=0$. Cylindrical coordinates give $2\pi$. $\blacksquare$

---

## 8.4-3

Compute $\iiint_\Omega\left(x+y+z\right)^3$ over a ball.

### Solution 8.4-3

Every term is odd in some variable. The result is $0$. $\blacksquare$

---

## 8.4-5

Compute $\iiint_\Omega\left(x^2+y^2+z^2\right)$ over an annulus.

### Solution 8.4-5

$\frac{4\pi}5\left(b^5-a^5\right)$. $\blacksquare$

---

## 8.4-6

Compute $\iiint_\Omega\left(x^2+y^2\right)$ over $\left\{x^2+y^2\le z\le1\right\}$.

### Solution 8.4-6

$\frac\pi6$. $\blacksquare$

---

## 8.4-8

Compute $\iiint_\Omega\left(x^2+y^2\right)^2$.

### Solution 8.4-8

$\frac{\pi\left(64-43\sqrt2\right)}{420}$. $\blacksquare$

---

## 8.4-9

Compute $\iiint_\Omega\sqrt{x^2+y^2+z^2}$.

### Solution 8.4-9

$\frac\pi{10}$. $\blacksquare$

---

## 8.4-10

Compute $\iiint_\Omega\left(x+1\right)\left(y+1\right)$ over an ellipsoid.

### Solution 8.4-10

By symmetry, the result is the volume: $\frac{4\pi abc}{3}$. $\blacksquare$
