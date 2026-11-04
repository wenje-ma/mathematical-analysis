# week28

> **Theorem 1.2 (Arc Length Formula)**
> 
> $s=\int_\alpha^\beta\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm dt$.

> **Theorem 1.3 (Computation of First Type Line Integral)**
> 
> $\int_L f\,\mathrm ds=\int_\alpha^\beta f\left(x\left(t\right),y\left(t\right),z\left(t\right)\right)\sqrt{\left[x'\right]^2+\left[y'\right]^2+\left[z'\right]^2}\,\mathrm dt$.

> **Theorem 2.2 (Green's Theorem)**
> 
> $\oint_{L^+}P\,\mathrm dx+Q\,\mathrm dy=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm dx\mathrm dy$.

> **Theorem 2.4 (Path Independence Condition)**
> 
> The integral is path-independent iff $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$.

> **Theorem 2.5 (Exact Differential Form)**
> 
> $P\,\mathrm dx+Q\,\mathrm dy$ is exact iff $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$.

> **Theorem 4.2 (Triple Integral by Cross-Section)**
> 
> $\iiint_\Omega f\,\mathrm dV=\iint_D\mathrm dx\mathrm dy\int_{z_1\left(x,y\right)}^{z_2\left(x,y\right)}f\,\mathrm dz$.

> **Theorem 4.4 (Change of Variables in Triple Integrals)**
> 
> $\iiint_\Omega f=\iiint_{\Omega'}f\left(x\left(u,v,w\right),\dots\right)\left|J\right|\,\mathrm du\mathrm dv\mathrm dw$. Cylindrical: $\left|J\right|=r$. Spherical: $\left|J\right|=\rho^2\sin\varphi$.

> **Proposition 5.1 (Surface Area Formula)**
> 
> $S=\iint_D\sqrt{1+f_x^2+f_y^2}\,\mathrm dx\mathrm dy$.

## 8.4-9

Compute $\iiint_\Omega\sqrt{x^2+y^2+z^2}$.

### Solution to 8.4-9

$\frac\pi{10}$. $\blacksquare$

## 8.4-10

Compute $\iiint_\Omega\left(x+1\right)\left(y+1\right)$ over an ellipsoid.

### Solution to 8.4-10

By symmetry, the result is the volume: $\frac{4\pi abc}{3}$. $\blacksquare$

## 8.5-1

Find the area of the cone $z=\sqrt{x^2+y^2}$ cut by $z^2=2x$.

### Solution to 8.5-1

The projection is a disk. Since $\sqrt{1+f_x^2+f_y^2}=\sqrt2$, by **Proposition 5.1 (Surface Area Formula)**, $S=\sqrt2\pi$. $\blacksquare$

## 8.5-2

Find the area of $az=xy$ inside $x^2+y^2=a^2$.

### Solution to 8.5-2

$S=\frac{2\pi a^2}{3}\left(2\sqrt2-1\right)$. $\blacksquare$

## 8.5-3

Find the center of mass of the first-octant ellipsoid.

### Solution to 8.5-3

By symmetry and Center of Mass Formula, $\left(\frac{3a}{8},\frac{3b}{8},\frac{3c}{8}\right)$. $\blacksquare$

## 8.5-6

Find the moment of inertia of a cube about the $z$-axis.

### Solution to 8.5-6

$J_z=\frac{2\rho a^5}{3}$. $\blacksquare$

## 9.1-1

Find the arc length of the cycloid arch.

### Solution to 9.1-1

By **Theorem 1.2 (Arc Length Formula)**, $s=8a$. $\blacksquare$

## 9.1-3

Find the arc length of the Archimedean spiral.

### Solution to 9.1-3

By **Theorem 1.2 (Arc Length Formula)**, $s=a\pi\sqrt{1+4\pi^2}+\frac a2\ln\left(2\pi+\sqrt{1+4\pi^2}\right)$. $\blacksquare$

## 9.1-4

Compute $\oint_L xy\,\mathrm ds$ over the diamond $\left|x\right|+\left|y\right|=a$.

### Solution to 9.1-4

By symmetry, the integral is $0$. $\blacksquare$

## 9.1-7

Compute $\int_L xy\,\mathrm ds$ over the first-quadrant ellipse.

### Solution to 9.1-7

$\frac{ab\left(a^2+ab+b^2\right)}{3\left(a+b\right)}$. $\blacksquare$

## 9.1-8

Compute $\int_L x^2\,\mathrm ds$.

### Solution to 9.1-8

$\frac{2\pi a^3}{3}$. $\blacksquare$

## 9.2-1

Compute $\oint_{L^+}x^2\,\mathrm dy-y^2\,\mathrm dx$.

### Solution to 9.2-1

By symmetry, the integral is $0$. $\blacksquare$

## 9.2-2

Compute the line integral along $y=\left|x\right|$.

### Solution to 9.2-2

$\frac{41}{6}$. $\blacksquare$

## 9.2-3

Apply Green's theorem.

### Solution to 9.2-3

(1) $\frac{\pi R^4}{2}$. (2) $\frac{25}{6}$. (3) $\pi a^2$. $\blacksquare$

## 9.2-4

Prove: $\oint_{L^+}f\left(xy\right)\left(y\,\mathrm dx+x\,\mathrm dy\right)=0$.

### Solution to 9.2-4

Since $\frac{\partial P}{\partial y}=\frac{\partial Q}{\partial x}$, Green's theorem gives $0$. $\blacksquare$
