# Assignment 35

> **Formula** (Computation of Surface Integrals of the First Kind) Let a smooth surface $S$ be given by the parametric equations $x=x\left(u,v\right)$, $y=y\left(u,v\right)$, $z=z\left(u,v\right)$ ($\left(u,v\right)\in D$), and set $E=x_u^2+y_u^2+z_u^2$, $F=x_ux_v+y_uy_v+z_uz_v$, $G=x_v^2+y_v^2+z_v^2$. Then

$$
\iint_S f\left(x,y,z\right)\,\mathrm{d}S=\iint_D f\left(x\left(u,v\right),y\left(u,v\right),z\left(u,v\right)\right)\sqrt{EG-F^2}\,\mathrm{d}u\mathrm{d}v.
$$

In particular, when the surface is given by $z=g\left(x,y\right)$ ($\left(x,y\right)\in D$), we have $\mathrm{d}S=\sqrt{1+g_x^2+g_y^2}\,\mathrm{d}x\mathrm{d}y$.

> **Formula** (Computation of Surface Integrals of the Second Kind) Let the surface $S:z=g\left(x,y\right)$ ($\left(x,y\right)\in D$), taken with its upper side. Then

$$
\iint_S P\,\mathrm{d}y\mathrm{d}z+Q\,\mathrm{d}z\mathrm{d}x+R\,\mathrm{d}x\mathrm{d}y=\iint_D\left[P\left(-g_x\right)+Q\left(-g_y\right)+R\right]\mathrm{d}x\mathrm{d}y.
$$

For the lower side, take the negative sign.

### Problem 1

(Problem 9.3-1) Evaluate $\displaystyle\iint_S\left(y+x\right)\,\mathrm{d}S$, where $S$ is the cube

$$
V=\left\{\left(x,y,z\right):0\le x\le1,0\le y\le1,0\le z\le1\right\}
$$

's surface.

### Solution to Problem 1

By symmetry, $\iint_S x\,\mathrm{d}S=\iint_S y\,\mathrm{d}S$. Compute $\iint_S x\,\mathrm{d}S$ separately on each of the six faces:

the face $x=0$: $x=0$, so the integral $=0$; the face $x=1$: $\iint 1\,\mathrm{d}y\mathrm{d}z=1$; the face $y=0$: $\iint x\,\mathrm{d}x\mathrm{d}z=\frac12$; the face $y=1$: $\frac12$; the face $z=0$: $\frac12$; the face $z=1$: $\frac12$.

Hence

$$
\iint_S x\,\mathrm{d}S=0+1+\frac12+\frac12+\frac12+\frac12=3.
$$

Therefore

$$
\iint_S\left(y+x\right)\,\mathrm{d}S=2\iint_S x\,\mathrm{d}S=6.

$$

$\blacksquare$
### Problem 2

(Problem 9.3-3) Evaluate $\displaystyle\oiint_S\left(xy+z\right)^2\,\mathrm{d}S$, where $S$ is the sphere $x^2+y^2+z^2=R^2$.

### Solution to Problem 2

Expanding,

$$
\left(xy+z\right)^2=x^2y^2+2xyz+z^2.
$$

Since the sphere is symmetric about each coordinate plane, $2xyz$ is an odd function in $x$ (or $y$, $z$), so

$$
\oiint_S 2xyz\,\mathrm{d}S=0.
$$

By symmetry,

$$
\oiint_S x^2\,\mathrm{d}S=\oiint_S y^2\,\mathrm{d}S=\oiint_S z^2\,\mathrm{d}S,
$$
and the sum of the three is

$$
\oiint_S\left(x^2+y^2+z^2\right)\,\mathrm{d}S=R^2\cdot4\pi R^2=4\pi R^4.
$$

Hence

$$
\oiint_S z^2\,\mathrm{d}S=\frac{4\pi R^4}{3}.
$$

Similarly,

$$
\oiint_S x^2y^2=\oiint_S y^2z^2=\oiint_S z^2x^2.
$$
Using

$$
\left(x^2+y^2+z^2\right)^2=x^4+y^4+z^4+2\left(x^2y^2+y^2z^2+z^2x^2\right),
$$
and by symmetry

$$
\oiint_S x^4=\oiint_S y^4=\oiint_S z^4,
$$

while $\oiint_S x^4\,\mathrm{d}S=\frac{4\pi R^6}{5}$ (computed directly in spherical coordinates). Thus

$$
2\cdot3\oiint_S x^2y^2\,\mathrm{d}S=4\pi R^6-3\cdot\frac{4\pi R^6}{5}=\frac{8\pi R^6}{5},
$$

i.e. $\oiint_S x^2y^2\,\mathrm{d}S=\frac{4\pi R^6}{15}$. Hence

$$
\oiint_S\left(xy+z\right)^2\,\mathrm{d}S=\frac{4\pi R^6}{15}+\frac{4\pi R^4}{3}.

$$

$\blacksquare$
### Problem 3

(Problem 9.3-5) Find the mass of the paraboloidal thin shell $z=\frac12\left(x^2+y^2\right)$ ($0\le z\le1$), assuming its surface density is $\rho=x+y+z$.

### Solution to Problem 3

The surface is $z=\frac12\left(x^2+y^2\right)$, and the projection region is

$$
D=\left\{\left(x,y\right):x^2+y^2\le2\right\}.
$$

$z_x=x$, $z_y=y$. By **Formula** (Computation of Surface Integrals of the First Kind),

$$
\mathrm{d}S=\sqrt{1+x^2+y^2}\,\mathrm{d}x\mathrm{d}y.
$$

The mass is

$$
M=\iint_D\left(x+y+\frac12\left(x^2+y^2\right)\right)\sqrt{1+x^2+y^2}\,\mathrm{d}x\mathrm{d}y.
$$

By symmetry, $\iint_D x=\iint_D y=0$. Using polar coordinates,

$$
M=\int_0^{2\pi}\mathrm{d}\theta\int_0^{\sqrt2}\frac{r^2}{2}\sqrt{1+r^2}\,r\,\mathrm{d}r=\pi\int_0^{\sqrt2}r^3\sqrt{1+r^2}\,\mathrm{d}r.
$$

Let $u=1+r^2$, $\mathrm{d}u=2r\,\mathrm{d}r$, $r^2=u-1$, to get

$$
M=\frac\pi2\int_1^3\left(u-1\right)\sqrt u\,\mathrm{d}u=\frac\pi2\left[\frac25u^{5/2}-\frac23u^{3/2}\right]_1^3=\frac{\pi\left(12\sqrt3+2\right)}{15}.

$$

$\blacksquare$
### Problem 4

(Problem 9.3-6) Let $S$ be the sphere $x^2+y^2+z^2=a^2$ ($x\ge0,y\ge0,z\ge0$) lying in the first octant, and suppose the surface density of this spherical thin shell is constant. Find the coordinates of its center of mass.

### Solution to Problem 4

By symmetry, the center of mass $\left(\overline x,\overline y,\overline z\right)$ satisfies $\overline x=\overline y=\overline z$. The surface area is $=\frac18\cdot4\pi a^2=\frac{\pi a^2}{2}$.

Using spherical coordinates $x=a\sin\varphi\cos\theta$, $y=a\sin\varphi\sin\theta$, $z=a\cos\varphi$, the first octant is $0\le\varphi\le\pi/2$, $0\le\theta\le\pi/2$, and $\mathrm{d}S=a^2\sin\varphi\,\mathrm{d}\varphi\mathrm{d}\theta$. Then

$$
\iint_S z\,\mathrm{d}S=\int_0^{\pi/2}\mathrm{d}\theta\int_0^{\pi/2}a\cos\varphi\cdot a^2\sin\varphi\,\mathrm{d}\varphi=\frac\pi2\cdot\frac{a^3}{2}=\frac{\pi a^3}{4}.
$$

Hence $\overline z=\frac{\pi a^3/4}{\pi a^2/2}=\frac a2$. The center of mass is $\left(\frac a2,\frac a2,\frac a2\right)$. $\blacksquare$

### Problem 5

(Problem 9.3-7)

$$
I=\displaystyle\iint_S y\left(x-z\right)\,\mathrm{d}y\mathrm{d}z+x^2\,\mathrm{d}z\mathrm{d}x+\left(y^2+zx\right)\,\mathrm{d}x\mathrm{d}y,
$$
where $S$ is the cube

$$
V=\left\{\left(x,y,z\right):0\le x\le a,0\le y\le a,0\le z\le a\right\}
$$

's outer surface.

### Solution to Problem 5

Here $P=y\left(x-z\right)$, $Q=x^2$, $R=y^2+zx$. By **Theorem 4.1** (Gauss–Ostrogradsky Formula) of the next section,

$$
I=\iiint_\Omega\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)\mathrm{d}V=\iiint_\Omega\left(y+0+x\right)\,\mathrm{d}V.
$$

$\Omega=\left[0,a\right]^3$. Hence

$$
I=\int_0^a\mathrm{d}x\int_0^a\mathrm{d}y\int_0^a\left(x+y\right)\,\mathrm{d}z=a\cdot\left(\frac{a^3}{2}+\frac{a^3}{2}\right)=a^4.

$$

$\blacksquare$
### Problem 6

(Problem 9.3-8)

$$
I=\displaystyle\iint_S\left(y-z\right)x\,\mathrm{d}y\mathrm{d}z+\left(x-y\right)\,\mathrm{d}x\mathrm{d}y,
$$

where $S$ is the outer surface of the spatial region enclosed by the cylinder $x^2+y^2=1$ and the planes $z=0$ and $z=3$.

### Solution to Problem 6

Here $P=x\left(y-z\right)$, $Q=0$, $R=x-y$. By **Theorem 4.1** (Gauss–Ostrogradsky Formula),

$$
I=\iiint_\Omega\frac{\partial P}{\partial x}\,\mathrm{d}V=\iiint_\Omega\left(y-z\right)\,\mathrm{d}V.
$$

$\Omega$ is the cylinder $x^2+y^2\le1$, $0\le z\le3$. Using cylindrical coordinates:

$$
I=\int_0^3\mathrm{d}z\int_0^{2\pi}\mathrm{d}\theta\int_0^1\left(r\sin\theta-z\right)r\,\mathrm{d}r.
$$

Since $\int_0^{2\pi}\sin\theta\,\mathrm{d}\theta=0$, the first term is $0$. The second term: $\int_0^{2\pi}\left(-z\right)\cdot\frac12\,\mathrm{d}\theta=-\pi z$. Therefore

$$
I=\int_0^3\left(-\pi z\right)\,\mathrm{d}z=-\frac{9\pi}{2}.

$$

$\blacksquare$
### Problem 7

(Problem 9.3-9)

$$
I=\displaystyle\iint_S\left(y-z\right)\,\mathrm{d}y\mathrm{d}z+\left(z-x\right)\,\mathrm{d}z\mathrm{d}x+\left(x-y\right)\,\mathrm{d}x\mathrm{d}y,
$$

where $S$ is the upper side of the portion of the upper hemisphere $x^2+y^2+z^2=2Rx$ ($z\ge0$) cut out by the cylinder $x^2+y^2=2rx$ ($0< r< R$).

### Solution to Problem 7

$S$ can be written as $z=\sqrt{2Rx-x^2-y^2}$, with projection region

$$
D=\left\{\left(x,y\right):x^2+y^2\le2rx\right\}.
$$

By **Formula** (Computation of Surface Integrals of the Second Kind), for the upper side:

$$
z_x=\frac{R-x}{z}, z_y=-\frac yz.
$$

The integrand is $P\left(-z_x\right)+Q\left(-z_y\right)+R$, where $P=y-z$, $Q=z-x$, $R=x-y$. Substituting and simplifying the numerator:

$$
\left(y-z\right)\left(x-R\right)+y\left(z-x\right)=xy-yR-zx+zR+yz-xy=-yR-zx+zR+yz.
$$

Dividing by $z$ gives $-\frac{yR}{z}-x+R+y$, and adding $x-y$ gives $R-\frac{Ry}{z}$.

Hence

$$
I=\iint_D\left(R-\frac{Ry}{z}\right)\mathrm{d}x\mathrm{d}y=R\cdot m\left(D\right)-R\iint_D\frac{y}{z}\,\mathrm{d}x\mathrm{d}y.
$$

$D$ is symmetric about the $x$-axis, and $y/z$ is an odd function in $y$, so the second term is $0$. $m\left(D\right)=\pi r^2$. Therefore $I=\pi Rr^2$. $\blacksquare$

### Problem 8

(Problem 9.3-10)

$$
I=\displaystyle\iint_S x\,\mathrm{d}y\mathrm{d}z+y\,\mathrm{d}z\mathrm{d}x+z\,\mathrm{d}x\mathrm{d}y,
$$

where $S$ is the outer side of the ellipsoid $\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}=1$ ($a> 0,b> 0,c> 0$).

### Solution to Problem 8

Here $P=x$, $Q=y$, $R=z$. By **Theorem 4.1** (Gauss–Ostrogradsky Formula),

$$
I=\iiint_\Omega\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)\mathrm{d}V=3\iiint_\Omega\mathrm{d}V.
$$

The volume of the ellipsoid is $\frac{4\pi abc}{3}$, so $I=3\cdot\frac{4\pi abc}{3}=4\pi abc$. $\blacksquare$
