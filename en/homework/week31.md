# Assignment 31

> **Theorem 4.2** (The Projection Method for Triple Integrals) Let
> $$
> \Omega=\left\{\left(x,y,z\right):\left(x,y\right)\in D,z_1\left(x,y\right)\le z\le z_2\left(x,y\right)\right\},
> $$
> where $D$ is a bounded closed region that is rectifiable in the $Oxy$ plane, $z_1,z_2$ are continuous on $D$, and $f$ is continuous on $\Omega$. Then

$$
\iiint_\Omega f\left(x,y,z\right)\,\mathrm{d}V=\iint_D\mathrm{d}x\mathrm{d}y\int_{z_1\left(x,y\right)}^{z_2\left(x,y\right)}f\left(x,y,z\right)\,\mathrm{d}z.
$$

> **Theorem 4.4** (Change of Variables Formula for Triple Integrals) Under the change of variables $x=x\left(u,v,w\right)$, $y=y\left(u,v,w\right)$, $z=z\left(u,v,w\right)$,

$$
\iiint_\Omega f\,\mathrm{d}x\mathrm{d}y\mathrm{d}z=\iiint_{\Omega'}f\left(x\left(u,v,w\right),y\left(u,v,w\right),z\left(u,v,w\right)\right)\left| J\left(u,v,w\right)\right|\,\mathrm{d}u\mathrm{d}v\mathrm{d}w,
$$

where $J=\frac{\partial\left(x,y,z\right)}{\partial\left(u,v,w\right)}$. In particular, in cylindrical coordinates $\left(r,\theta,z\right)$, $\left| J\right|=r$; in spherical coordinates $\left(\rho,\varphi,\theta\right)$, $\left| J\right|=\rho^2\sin\varphi$.

### Problem 1

(Problem 8.4-1) Evaluate $\displaystyle\iiint_\Omega z^2\,\mathrm{d}V$, where $\Omega$ is the unit ball

$$
\Omega=\left\{\left(x,y,z\right):x^2+y^2+z^2\le1\right\}.
$$

### Solution to Problem 1

By symmetry, $\iiint x^2=\iiint y^2=\iiint z^2$, hence

$$
\iiint_\Omega z^2\,\mathrm{d}V=\frac13\iiint_\Omega\left(x^2+y^2+z^2\right)\,\mathrm{d}V.
$$

Using spherical coordinates $x=\rho\sin\varphi\cos\theta$, $y=\rho\sin\varphi\sin\theta$, $z=\rho\cos\varphi$, $\Omega$ becomes $0\le\rho\le1$, $0\le\varphi\le\pi$, $0\le\theta\le2\pi$. By **Theorem 4.4**,

$$
\iiint_\Omega z^2\,\mathrm{d}V=\frac13\int_0^{2\pi}\mathrm{d}\theta\int_0^\pi\sin\varphi\,\mathrm{d}\varphi\int_0^1\rho^2\cdot\rho^2\,\mathrm{d}\rho=\frac13\cdot2\pi\cdot2\cdot\frac15=\frac{4\pi}{15}.

$$

$\blacksquare$
### Problem 2

(Problem 8.4-2) Evaluate $\displaystyle\iiint_\Omega\left(x+y+z\right)\,\mathrm{d}V$, where

$$
\Omega=\left\{\left(x,y,z\right):x^2+y^2\le4,0\le z\le1\right\}.
$$

### Solution to Problem 2

$\Omega$ is symmetric about the planes $x=0$ and $y=0$, and in the integrand, $x$ is an odd function of $x$ and $y$ is an odd function of $y$, hence $\iiint x\,\mathrm{d}V=\iiint y\,\mathrm{d}V=0$. Thus

$$
\iiint_\Omega\left(x+y+z\right)\,\mathrm{d}V=\iiint_\Omega z\,\mathrm{d}V.
$$

Using cylindrical coordinates $x=r\cos\theta$, $y=r\sin\theta$, by **Theorem 4.4**,

$$
\iiint_\Omega z\,\mathrm{d}V=\int_0^1 z\,\mathrm{d}z\int_0^{2\pi}\mathrm{d}\theta\int_0^2 r\,\mathrm{d}r=\frac12\cdot2\pi\cdot2=2\pi.

$$

$\blacksquare$
### Problem 3

(Problem 8.4-3) Evaluate $\displaystyle\iiint_\Omega\left(x+y+z\right)^3\,\mathrm{d}V$, where

$$
\Omega=\left\{\left(x,y,z\right):x^2+y^2+z^2\le R^2\right\}\ \left(R> 0\right).
$$

(Hint: make use of the symmetry of the region of integration.)

### Solution to Problem 3

Expand the integrand:

$$
\left(x+y+z\right)^3=x^3+y^3+z^3+3x^2y+3x^2z+3y^2x+3y^2z+3z^2x+3z^2y+6xyz.
$$

The ball $\Omega$ is symmetric about the planes $x=0$, $y=0$, and $z=0$. Each term in the above expression contains at least an odd power of one variable: $x^3,y^3,z^3$ are odd functions of the respective variables; $3x^2y,3x^2z,\dots,3z^2y$ are odd functions of $y,z,x,\dots,y$, respectively; $6xyz$ is an odd function of each variable. Hence the integral of each term over $\Omega$ is $0$.

$$
\iiint_\Omega\left(x+y+z\right)^3\,\mathrm{d}V=0.

$$

$\blacksquare$
### Problem 4

(Problem 8.4-5) Evaluate $\displaystyle\iiint_\Omega\left(x^2+y^2+z^2\right)\,\mathrm{d}V$, where

$$
\Omega=\left\{\left(x,y,z\right):a^2\le x^2+y^2+z^2\le b^2\right\}\ \left(0< a< b\right).
$$

### Solution to Problem 4

Using **Theorem 4.4** with spherical coordinates, $\Omega$ becomes $a\le\rho\le b$, $0\le\varphi\le\pi$, $0\le\theta\le2\pi$, hence

$$
\iiint_\Omega\left(x^2+y^2+z^2\right)\,\mathrm{d}V=\int_0^{2\pi}\mathrm{d}\theta\int_0^\pi\sin\varphi\,\mathrm{d}\varphi\int_a^b\rho^2\cdot\rho^2\,\mathrm{d}\rho=2\pi\cdot2\cdot\frac{b^5-a^5}{5}=\frac{4\pi}{5}\left(b^5-a^5\right).

$$

$\blacksquare$
### Problem 5

(Problem 8.4-6) Evaluate $\displaystyle\iiint_\Omega\left(x^2+y^2\right)\,\mathrm{d}V$, where

$$
\Omega=\left\{\left(x,y,z\right):x^2+y^2\le z\le1\right\}.
$$

### Solution to Problem 5

The projection of $\Omega$ onto the $Oxy$ plane is

$$
D=\left\{\left(x,y\right):x^2+y^2\le1\right\}.
$$

Using cylindrical coordinates, by **Theorem 4.2** and **Theorem 4.4**,

$$
\iiint_\Omega\left(x^2+y^2\right)\,\mathrm{d}V=\int_0^{2\pi}\mathrm{d}\theta\int_0^1 r\,\mathrm{d}r\int_{r^2}^1 r^2\,\mathrm{d}z=2\pi\int_0^1 r^3\left(1-r^2\right)\,\mathrm{d}r=2\pi\left(\frac14-\frac16\right)=\frac\pi6.

$$

$\blacksquare$
### Problem 6

(Problem 8.4-8) Evaluate $\displaystyle\iiint_\Omega\left(x^2+y^2\right)^2\,\mathrm{d}V$, where $\Omega$ is the region bounded by $z=\sqrt{1-x^2-y^2}$ and $z=\sqrt{x^2+y^2}$.

### Solution to Problem 6

The two surfaces $z=\sqrt{1-r^2}$ and $z=r$ intersect at $r=1/\sqrt2$. In spherical coordinates, the cone $z=r$ corresponds to $\varphi=\pi/4$, and the upper hemisphere corresponds to $\rho=1$. Hence $\Omega$ becomes $0\le\rho\le1$, $0\le\varphi\le\pi/4$, $0\le\theta\le2\pi$. By **Theorem 4.4**,

$$
\iiint_\Omega\left(x^2+y^2\right)^2\,\mathrm{d}V=\int_0^{2\pi}\mathrm{d}\theta\int_0^{\pi/4}\sin\varphi\,\mathrm{d}\varphi\int_0^1\left(\rho^2\sin^2\varphi\right)^2\cdot\rho^2\,\mathrm{d}\rho=2\pi\int_0^{\pi/4}\sin^5\varphi\,\mathrm{d}\varphi\cdot\frac17.
$$

Let $u=\cos\varphi$,

$$
\int\sin^5\varphi\,\mathrm{d}\varphi=-\int\left(1-2u^2+u^4\right)\mathrm{d}u=-u+\frac23u^3-\frac15u^5.
$$

Substituting the limits:

$$
\int_0^{\pi/4}\sin^5\varphi\,\mathrm{d}\varphi=\frac8{15}-\frac{43\sqrt2}{120}.
$$

Hence

$$
\iiint_\Omega\left(x^2+y^2\right)^2\,\mathrm{d}V=\frac{2\pi}{7}\left(\frac8{15}-\frac{43\sqrt2}{120}\right)=\frac{\pi\left(64-43\sqrt2\right)}{420}.

$$

$\blacksquare$
### Problem 7

(Problem 8.4-9) Evaluate $\displaystyle\iiint_\Omega\sqrt{x^2+y^2+z^2}\,\mathrm{d}V$, where $\Omega$ is the interior of the sphere $x^2+y^2+z^2=x$.

### Solution to Problem 7

The sphere equation $x^2+y^2+z^2=x$ becomes $\rho^2=\rho\sin\varphi\cos\theta$ in spherical coordinates, i.e. $\rho=\sin\varphi\cos\theta$. Since $\rho\ge0$, we have $\sin\varphi\cos\theta\ge0$, i.e. $\theta\in\left[-\pi/2,\pi/2\right]$. By **Theorem 4.4**,

$$
\iiint_\Omega\sqrt{x^2+y^2+z^2}\,\mathrm{d}V=\int_{-\pi/2}^{\pi/2}\mathrm{d}\theta\int_0^\pi\sin\varphi\,\mathrm{d}\varphi\int_0^{\sin\varphi\cos\theta}\rho\cdot\rho^2\,\mathrm{d}\rho=\frac14\int_{-\pi/2}^{\pi/2}\cos^4\theta\,\mathrm{d}\theta\int_0^\pi\sin^5\varphi\,\mathrm{d}\varphi.
$$

where $\int_{-\pi/2}^{\pi/2}\cos^4\theta\,\mathrm{d}\theta=\frac{3\pi}{8}$, $\int_0^\pi\sin^5\varphi\,\mathrm{d}\varphi=\frac{16}{15}$. Hence

$$
\iiint_\Omega\sqrt{x^2+y^2+z^2}\,\mathrm{d}V=\frac14\cdot\frac{3\pi}{8}\cdot\frac{16}{15}=\frac\pi{10}.

$$

$\blacksquare$
### Problem 8

(Problem 8.4-10) Evaluate $\displaystyle\iiint_\Omega\left(x+1\right)\left(y+1\right)\,\mathrm{d}V$, where $\Omega$ is the ellipsoid $\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}\le1$ ($a> 0,b> 0,c> 0$).

### Solution to Problem 8

Expand the integrand:

$$
\left(x+1\right)\left(y+1\right)=xy+x+y+1.
$$
The ellipsoid $\Omega$ is symmetric about the planes $x=0$, $y=0$, and $z=0$. $xy$ is an odd function of $x$ (or $y$), $x$ is an odd function of $x$, and $y$ is an odd function of $y$, hence

$$
\iiint xy=\iiint x=\iiint y=0.
$$

Thus

$$
\iiint_\Omega\left(x+1\right)\left(y+1\right)\,\mathrm{d}V=\iiint_\Omega 1\,\mathrm{d}V=m\left(\Omega\right).
$$

The volume of the ellipsoid is $\frac{4\pi abc}{3}$, hence

$$
\iiint_\Omega\left(x+1\right)\left(y+1\right)\,\mathrm{d}V=\frac{4\pi abc}{3}.

$$

$\blacksquare$