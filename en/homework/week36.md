# Assignment 36

> **Theorem 4.1** (Gauss–Ostrogradsky Formula) Let $S$ be a piecewise smooth closed surface in space, let $\Omega$ be the closed spatial region it encloses, and suppose $P,Q,R$ have continuous first-order partial derivatives in $\Omega$. Then

$$
\oiint_{S^+}P\,\mathrm{d}y\mathrm{d}z+Q\,\mathrm{d}z\mathrm{d}x+R\,\mathrm{d}x\mathrm{d}y=\iiint_\Omega\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)\mathrm{d}V,
$$

where $S^+$ denotes the outer side.

> **Theorem 4.2** (Stokes' Formula) Let $S$ be a piecewise smooth two-sided surface, with boundary $L$ a piecewise smooth closed curve, and suppose the orientation of $L$ and the normal vector of $S$ form a right-handed system. Then

$$
\oint_{L^+}P\,\mathrm{d}x+Q\,\mathrm{d}y+R\,\mathrm{d}z=\iint_{S^+}\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right)\mathrm{d}y\mathrm{d}z+\left(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}\right)\mathrm{d}z\mathrm{d}x+\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y.
$$

### Problem 1

(Problem 9.4-1) Evaluate

$$
\displaystyle\oiint_{S^+}xz^2\,\mathrm{d}y\mathrm{d}z+\left(x^2y-z^3\right)\,\mathrm{d}z\mathrm{d}x+\left(2xy+y^2z\right)\,\mathrm{d}x\mathrm{d}y,
$$

where $S^+$ is the outer side of the entire surface of the hemispherical region enclosed by $z=\sqrt{a^2-x^2-y^2}$ and $z=0$.

### Solution to Problem 1

Here $P=xz^2$, $Q=x^2y-z^3$, $R=2xy+y^2z$. By **Theorem 4.1** (Gauss–Ostrogradsky Formula),

$$
\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}=z^2+x^2+y^2.
$$

$\Omega$ is the upper hemisphere $x^2+y^2+z^2\le a^2$, $z\ge0$. Using spherical coordinates:

$$
I=\int_0^{2\pi}\mathrm{d}\theta\int_0^{\pi/2}\mathrm{d}\varphi\int_0^a r^2\cdot r^2\sin\varphi\,\mathrm{d}r=2\pi\cdot\frac{a^5}{5}=\frac{2\pi a^5}{5}.

$$

$\blacksquare$
### Problem 2

(Problem 9.4-3) Evaluate

$$
\displaystyle\oiint_{S^+}x^3\,\mathrm{d}y\mathrm{d}z+y^3\,\mathrm{d}z\mathrm{d}x+z^3\,\mathrm{d}x\mathrm{d}y,
$$

where $S^+$ is the outer side of the sphere $x^2+y^2+z^2=a^2$.

### Solution to Problem 2

By **Theorem 4.1** (Gauss–Ostrogradsky Formula),

$$
I=\iiint_\Omega 3\left(x^2+y^2+z^2\right)\,\mathrm{d}V.
$$

In spherical coordinates:

$$
I=3\int_0^{2\pi}\mathrm{d}\theta\int_0^\pi\mathrm{d}\varphi\int_0^a r^2\cdot r^2\sin\varphi\,\mathrm{d}r=3\cdot4\pi\cdot\frac{a^5}{5}=\frac{12\pi a^5}{5}.

$$

$\blacksquare$
### Problem 3

(Problem 9.4-5) Evaluate $\displaystyle\oiint_{S^+}\boldsymbol{F}\cdot\boldsymbol{n}\,\mathrm{d}S$, where $\boldsymbol{F}=\left(x^4,y^4,z^4\right)$, and $S^+$ is the outer side of the portion of the cone $x^2+y^2=z^2$ with $0\le z\le h$.

### Solution to Problem 3

$S$ is only the lateral surface of the cone and is not closed. Add the top face $S_1$: $z=h$, $x^2+y^2\le h^2$, taken with its upper side. By **Theorem 4.1**,

$$
\oiint_{S\cup S_1}\boldsymbol{F}\cdot\boldsymbol{n}\,\mathrm{d}S=\iiint_\Omega 4\left(x^3+y^3+z^3\right)\,\mathrm{d}V.
$$

By symmetry, $\iiint_\Omega x^3=\iiint_\Omega y^3=0$. The conical region $\Omega$: $x^2+y^2\le z^2$, $0\le z\le h$, so

$$
\iiint_\Omega z^3\,\mathrm{d}V=\int_0^h z^3\cdot\pi z^2\,\mathrm{d}z=\frac{\pi h^6}{6}.
$$

Hence the triple integral $=4\cdot\frac{\pi h^6}{6}=\frac{2\pi h^6}{3}$. On $S_1$, $\boldsymbol{F}\cdot\boldsymbol{n}=z^4=h^4$,

$$
\iint_{S_1}h^4\,\mathrm{d}x\mathrm{d}y=h^4\cdot\pi h^2=\pi h^6.
$$

Hence

$$
\oiint_{S^+}\boldsymbol{F}\cdot\boldsymbol{n}\,\mathrm{d}S=\frac{2\pi h^6}{3}-\pi h^6=-\frac{\pi h^6}{3}.

$$

$\blacksquare$
### Problem 4

(Problem 9.4-7) Evaluate $\displaystyle\oint_{L^+}y^2\,\mathrm{d}x+xy\,\mathrm{d}y+xz\,\mathrm{d}z$, where $L$ is the curve of intersection of the cylinder $x^2+y^2=2y$ and the plane $y=z$, traversed counterclockwise.

### Solution to Problem 4

$P=y^2$, $Q=xy$, $R=xz$. The curl is

$$
\nabla\times\boldsymbol{F}=\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z},\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x},\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)=\left(0,-z,-y\right).
$$

Take the surface $S$ to be the region in the plane $y=z$ bounded by $L$, with projection $D$: $x^2+y^2\le2y$. Here $z=y$, $z_x=0$, $z_y=1$. By **Theorem 4.2** (Stokes' Formula),

$$
\oint_{L^+}=\iint_D\left[0\cdot\left(-z_x\right)+\left(-z\right)\left(-z_y\right)+\left(-y\right)\right]\mathrm{d}x\mathrm{d}y=\iint_D\left(z-y\right)\,\mathrm{d}x\mathrm{d}y=0.

$$

$\blacksquare$
### Problem 5

(Problem 9.4-8)

$$
\displaystyle\oint_{L^+}\left(y^2+z^2-x^2\right)\,\mathrm{d}x+\left(x^2+z^2-y^2\right)\,\mathrm{d}y+\left(x^2+y^2-z^2\right)\,\mathrm{d}z,
$$

where $L$ is the curve of intersection of the sphere $z=\sqrt{2Rx-x^2-y^2}$ and the cylinder $x^2+y^2=2rx$ ($0< r< R$, $z\ge0$), and $L^+$ forms a right-handed system with the upper side of the sphere.

### Solution to Problem 5

$P=y^2+z^2-x^2$, $Q=x^2+z^2-y^2$, $R=x^2+y^2-z^2$. The curl is

$$
\nabla\times\boldsymbol{F}=2\left(y-z,z-x,x-y\right).
$$

The surface $S$ is the upper hemisphere $z=\sqrt{2Rx-x^2-y^2}$, with projection $D$: $x^2+y^2\le2rx$. Here $z_x=\frac{R-x}{z}$, $z_y=-\frac yz$. By **Theorem 4.2** (Stokes' Formula), for the upper side:

$$
\oint_{L^+}=\iint_D 2\left[\left(y-z\right)\frac{-\left(R-x\right)}{z}+\left(z-x\right)\frac yz+\left(x-y\right)\right]\mathrm{d}x\mathrm{d}y.
$$

Simplifying the expression inside the brackets:

$$
\frac{\left(y-z\right)\left(x-R\right)+y\left(z-x\right)}{z}+x-y=\frac{-yR-zx+zR+yz}{z}+x-y=R-\frac{Ry}{z}.
$$

Hence

$$
\oint_{L^+}=2\iint_D\left(R-\frac{Ry}{z}\right)\mathrm{d}x\mathrm{d}y.
$$

$D$ is symmetric about the $x$-axis, and $y/z$ is an odd function in $y$, so the second term is $0$. $m\left(D\right)=\pi r^2$. Therefore

$$
\oint_{L^+}=2R\cdot\pi r^2=2\pi Rr^2.

$$

$\blacksquare$