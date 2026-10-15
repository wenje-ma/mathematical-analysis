# Assignment 32

> **Proposition 5.1** (Surface Area Formula) Let $z=f\left(x,y\right)$ have continuous first-order partial derivatives on a bounded closed region $D$ that is rectifiable. Then the area of the surface $z=f\left(x,y\right)$ ($\left(x,y\right)\in D$) is

$$
S=\iint_D\sqrt{1+f_x^2\left(x,y\right)+f_y^2\left(x,y\right)}\,\mathrm{d}x\mathrm{d}y.
$$

> **Formula** (Coordinates of the Center of Mass) Let a body occupy a region $\Omega$ with density $\rho\left(x,y,z\right)$ and mass $m=\iiint_\Omega\rho\,\mathrm{d}V$. Then the coordinates of the center of mass are

$$
x_0=\frac1m\iiint_\Omega x\rho\,\mathrm{d}V, y_0=\frac1m\iiint_\Omega y\rho\,\mathrm{d}V, z_0=\frac1m\iiint_\Omega z\rho\,\mathrm{d}V.
$$

> **Formula** (Moment of Inertia) The moment of inertia of the body about the $z$-axis is

$$
J_z=\iiint_\Omega\left(x^2+y^2\right)\rho\left(x,y,z\right)\,\mathrm{d}V.
$$

### Problem 1

(Problem 8.5-1) Find the area of the portion of the cone $z=\sqrt{x^2+y^2}$ cut off by the cylinder $z^2=2x$.

### Solution to Problem 1

The cone equation $z=\sqrt{x^2+y^2}$ is $z=r$. From $z^2=2x$ we get $r^2=2r\cos\theta$, i.e. $r=2\cos\theta$ ($r\ge0$, $\theta\in\left[-\pi/2,\pi/2\right]$). Hence the projection of the cut-off portion onto the $Oxy$ plane is the disk

$$
D=\left\{\left(x,y\right):\left(x-1\right)^2+y^2\le1\right\},
$$

whose area is $\pi$.

From $f\left(x,y\right)=\sqrt{x^2+y^2}$ we get $f_x=x/\sqrt{x^2+y^2}$, $f_y=y/\sqrt{x^2+y^2}$, and hence

$$
\sqrt{1+f_x^2+f_y^2}=\sqrt{1+\frac{x^2+y^2}{x^2+y^2}}=\sqrt2.
$$

By **Proposition 5.1** (Surface Area Formula),

$$
S=\iint_D\sqrt2\,\mathrm{d}x\mathrm{d}y=\sqrt2\cdot\pi=\sqrt2\,\pi.

$$

$\blacksquare$
### Problem 2

(Problem 8.5-2) Find the area of the portion of the surface $az=xy$ lying inside the cylinder $x^2+y^2=a^2$.

### Solution to Problem 2

The surface equation is $z=xy/a$, so $f_x=y/a$, $f_y=x/a$, and hence

$$
\sqrt{1+f_x^2+f_y^2}=\sqrt{1+\frac{x^2+y^2}{a^2}}.
$$

The projection region is

$$
D=\left\{\left(x,y\right):x^2+y^2\le a^2\right\}.
$$

By **Proposition 5.1** (Surface Area Formula), using polar coordinates,

$$
\begin{aligned}S&=\iint_D\sqrt{1+\frac{x^2+y^2}{a^2}}\,\mathrm{d}x\mathrm{d}y\\&=\int_0^{2\pi}\mathrm{d}\theta\int_0^a\sqrt{1+\frac{r^2}{a^2}}\,r\,\mathrm{d}r.\end{aligned}
$$

Let $u=1+r^2/a^2$, $\mathrm{d}u=2r\,\mathrm{d}r/a^2$, giving

$$
S=2\pi\cdot\frac{a^2}{2}\int_1^2\sqrt u\,\mathrm{d}u=\pi a^2\cdot\frac23\left(2\sqrt2-1\right)=\frac{2\pi a^2}{3}\left(2\sqrt2-1\right).

$$

$\blacksquare$
### Problem 3

(Problem 8.5-3) Find the coordinates of the center of mass of the portion of the ellipsoid $\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}\le1$ ($a>0,b>0,c>0$) lying in the first octant. Here we assume the ellipsoid has uniform density.

### Solution to Problem 3

Let the density $\rho$ be constant. The volume of the first-octant ellipsoid is $V=\frac18\cdot\frac{4\pi abc}{3}=\frac{\pi abc}{6}$.

Make the generalized spherical coordinate transformation $x=a\rho\sin\varphi\cos\theta$, $y=b\rho\sin\varphi\sin\theta$, $z=c\rho\cos\varphi$; the Jacobian determinant is $\left| J\right|=abc\rho^2\sin\varphi$. The first octant corresponds to $0\le\rho\le1$, $0\le\varphi\le\pi/2$, $0\le\theta\le\pi/2$. By **Formula** (Coordinates of the Center of Mass),

$$
\begin{aligned}\iiint_\Omega z\,\mathrm{d}V&=\int_0^{\pi/2}\mathrm{d}\theta\int_0^{\pi/2}\mathrm{d}\varphi\int_0^1 c\rho\cos\varphi\cdot abc\rho^2\sin\varphi\,\mathrm{d}\rho\\&=abc^2\cdot\frac\pi2\cdot\frac12\cdot\frac14=\frac{\pi abc^2}{16}.\end{aligned}
$$

Hence

$$
z_0=\frac{\pi abc^2/16}{\pi abc/6}=\frac{3c}{8}.
$$

By symmetry (interchanging $a,x,\theta$ with $b,y,\theta+\pi/2$), we similarly get $x_0=\frac{3a}{8}$, $y_0=\frac{3b}{8}$. That is, the center of mass is $\left(\frac{3a}{8},\frac{3b}{8},\frac{3c}{8}\right)$. $\blacksquare$

### Problem 4

(Problem 8.5-6) Let $\Omega$ be a cube:

$$
\Omega=\left\{\left(x,y,z\right):0\le x\le a,0\le y\le a,0\le z\le a\right\}.
$$

Assume its density is the constant $\rho$. Find the moment of inertia of $\Omega$ about the $z$-axis.

### Solution to Problem 4

By **Formula** (Moment of Inertia),

$$
\begin{aligned}J_z&=\iiint_\Omega\left(x^2+y^2\right)\rho\,\mathrm{d}V\\&=\rho\int_0^a\mathrm{d}x\int_0^a\mathrm{d}y\int_0^a\left(x^2+y^2\right)\,\mathrm{d}z\\&=\rho a\left(\int_0^a x^2\mathrm{d}x\int_0^a\mathrm{d}y+\int_0^a\mathrm{d}x\int_0^a y^2\mathrm{d}y\right)\\&=\rho a\left(\frac{a^4}{3}+\frac{a^4}{3}\right)=\frac{2\rho a^5}{3}.\end{aligned}

$$

$\blacksquare$