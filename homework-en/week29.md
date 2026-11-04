# week29

> **Theorem 2.2 (Green's Theorem)**
> 
> $\oint_{L^+}P\,\mathrm dx+Q\,\mathrm dy=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm dx\mathrm dy$.

> **Theorem 2.4 (Path Independence Condition)**
> 
> The integral is path-independent iff $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$.

> **Theorem 2.5 (Exact Differential Form)**
> 
> $P\,\mathrm dx+Q\,\mathrm dy$ is exact iff $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$.

> **Theorem 4.1 (Gauss Divergence Theorem)**
> 
> $\oiint_S P\,\mathrm dy\mathrm dz+Q\,\mathrm dz\mathrm dx+R\,\mathrm dx\mathrm dy=\iiint_\Omega\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)\mathrm dV$.

> **Theorem 4.2 (Stokes' Theorem)**
> 
> $\oint_{L^+}P\,\mathrm dx+Q\,\mathrm dy+R\,\mathrm dz=\iint_{S^+}\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right)\mathrm dy\mathrm dz+\cdots$.

## 9.2-5-3

Compute $\int_{\left(0,0\right)}^{\left(a,b\right)}e^x\cos y\,\mathrm dx-e^x\sin y\,\mathrm dy$.

### Solution to 9.2-5-3

Since $d\left(e^x\cos y\right)=e^x\cos y\,\mathrm dx-e^x\sin y\,\mathrm dy$, the result is $e^a\cos b-1$. $\blacksquare$

## 9.2-6

Prove: $\oint_{L_r^+}\frac{x\,\mathrm dy-y\,\mathrm dx}{A^2x^2+B^2y^2}=\frac{2\pi}{AB}$.

### Solution to 9.2-6

The ellipse area is $\frac{\pi r^2}{AB}$. Hence the integral is $\frac{2\pi}{AB}$. $\blacksquare$

## 9.2-7

Prove the same for any closed curve enclosing the origin.

### Solution to 9.2-7

By Green's theorem on the doubly connected region, the integral equals that over a small ellipse $L_r$. $\blacksquare$

## 9.3-1

Compute $\iint_S\left(y+x\right)\,\mathrm dS$ over the cube surface.

### Solution to 9.3-1

By symmetry, $=6$. $\blacksquare$

## 9.3-3

Compute $\oiint_S\left(xy+z\right)^2$ over the sphere.

### Solution to 9.3-3

$\frac{4\pi R^6}{15}+\frac{4\pi R^4}{3}$. $\blacksquare$

## 9.3-5

Find the mass of the paraboloid shell.

### Solution to 9.3-5

$\frac{\pi\left(12\sqrt3+2\right)}{15}$. $\blacksquare$

## 9.3-6

Find the center of mass of the first-octant spherical shell.

### Solution to 9.3-6

$\left(\frac a2,\frac a2,\frac a2\right)$. $\blacksquare$

## 9.3-7

Compute the surface integral over the cube.

### Solution to 9.3-7

By **Theorem 4.1 (Gauss Divergence Theorem)**, $I=a^4$. $\blacksquare$

## 9.3-8

Compute over the cylinder.

### Solution to 9.3-8

$I=-\frac{9\pi}{2}$. $\blacksquare$

## 9.3-9

Compute the surface integral.

### Solution to 9.3-9

$I=\pi Rr^2$. $\blacksquare$

## 9.3-10

Compute over the ellipsoid.

### Solution to 9.3-10

By **Theorem 4.1 (Gauss Divergence Theorem)**, $I=4\pi abc$. $\blacksquare$

## 9.4-1

Compute the surface integral over the hemisphere boundary.

### Solution to 9.4-1

By **Theorem 4.1 (Gauss Divergence Theorem)**, $I=\frac{2\pi a^5}{5}$. $\blacksquare$

## 9.4-3

Compute over the sphere.

### Solution to 9.4-3

$I=\frac{12\pi a^5}{5}$. $\blacksquare$

## 9.4-5

Compute the flux through the cone surface.

### Solution to 9.4-5

$-\frac{\pi h^6}{3}$. $\blacksquare$

## 9.4-7

Compute the line integral around the intersection.

### Solution to 9.4-7

By **Theorem 4.2 (Stokes' Theorem)**, the integral is $0$. $\blacksquare$

## 9.4-8

Compute the line integral.

### Solution to 9.4-8

By **Theorem 4.2 (Stokes' Theorem)**, $2\pi Rr^2$. $\blacksquare$
