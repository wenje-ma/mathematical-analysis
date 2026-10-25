# Assignment 34

> **Theorem 2.2** (Green's Formula) Let $L$ be a piecewise smooth simple closed curve in the plane $Oxy$, let $D$ be the bounded closed region enclosed by it, and suppose $P\left(x,y\right),Q\left(x,y\right)$ have continuous first-order partial derivatives on $D$. Then

$$
\oint_{L^+}P\left(x,y\right)\,\mathrm{d}x+Q\left(x,y\right)\,\mathrm{d}y=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y,
$$

where $L^+$ denotes the counterclockwise direction.

> **Theorem 2.4** (Condition for a Path-Independent Integral) Let $D$ be a simply connected domain in the plane, and suppose $P,Q$ have continuous first-order partial derivatives in $D$. Then $\int P\,\mathrm{d}x+Q\,\mathrm{d}y$ is path-independent in $D$ if and only if $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$ holds everywhere in $D$.

> **Theorem 2.5** (Exact Differential Forms) Under the above conditions, $P\,\mathrm{d}x+Q\,\mathrm{d}y$ is an exact differential form if and only if $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$ holds everywhere in $D$.

### Problem 1

(Problem 9.2-1) Evaluate the integral $\displaystyle\oint_{L^+}x^2\,\mathrm{d}y-y^2\,\mathrm{d}x$, where $L$ is the ellipse $\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$, traversed counterclockwise.

### Solution to Problem 1

Here $P=-y^2$, $Q=x^2$. By **Theorem 2.2** (Green's Formula),

$$
\oint_{L^+}x^2\,\mathrm{d}y-y^2\,\mathrm{d}x=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y=\iint_D\left(2x+2y\right)\,\mathrm{d}x\mathrm{d}y.
$$

The elliptical region $D$ is symmetric about $x=0$ and $y=0$, while the integrand $2x+2y$ is an odd function in both $x$ and $y$, so the integral is $0$. That is, the original integral $=0$. $\blacksquare$

### Problem 2

(Problem 9.2-2) Evaluate

$$
\displaystyle\int_L\left(x^2+y^2\right)\,\mathrm{d}x+\left(x^2-y\right)\,\mathrm{d}y,
$$

where $L$ is the directed arc of the curve $y=\left| x\right|$ from the point $\left(-1,1\right)$ to $\left(2,2\right)$.

### Solution to Problem 2

$L$ splits into two segments: $L_1$ goes from $\left(-1,1\right)$ to $\left(0,0\right)$, for which $x\in\left[-1,0\right]$, $y=-x$, $\mathrm{d}y=-\mathrm{d}x$; $L_2$ goes from $\left(0,0\right)$ to $\left(2,2\right)$, for which $x\in\left[0,2\right]$, $y=x$, $\mathrm{d}y=\mathrm{d}x$.

On $L_1$:

$$
\int_{L_1}=\int_{-1}^0\left[x^2+\left(-x\right)^2\right]\mathrm{d}x+\left[x^2-\left(-x\right)\right]\left(-\mathrm{d}x\right)=\int_{-1}^0\left(x^2-x\right)\,\mathrm{d}x=\frac56.
$$

On $L_2$:

$$
\int_{L_2}=\int_0^2 2x^2\,\mathrm{d}x+\left(x^2-x\right)\,\mathrm{d}x=\int_0^2\left(3x^2-x\right)\,\mathrm{d}x=6.
$$

Hence the original integral $=\frac56+6=\frac{41}{6}$. $\blacksquare$

### Problem 3

(Problem 9.2-3) Apply Green's formula to evaluate the following integrals:
(1)

$$
\displaystyle\oint_{L^+}\left(xy^2+y^3\right)\,\mathrm{d}y-\left(x^3+x^2y\right)\,\mathrm{d}x,
$$

where $L^+$ is the circle $x^2+y^2=R^2$, traversed counterclockwise;

(2)

$$
\displaystyle\oint_{L^+}\sqrt{x^2+y^2}\,\mathrm{d}x+y\left[xy+\ln\left(x+\sqrt{x^2+y^2}\right)\right]\mathrm{d}y,
$$

where $L^+$ is the triangle with vertices $A\left(1,1\right)$, $B\left(2,2\right)$ and $C\left(1,3\right)$, directed counterclockwise;

(3)

$$
\displaystyle\oint_{L^+}\left(e^x\sin y+\sin x-8y\right)\,\mathrm{d}x+\left(e^x\cos y-\sin y\right)\,\mathrm{d}y,
$$

where $L^+$ is the boundary of the upper semicircle $0\le y\le\sqrt{ax-x^2}$ ($0\le x\le a$), directed counterclockwise.

### Solution to Problem 3

(1) $P=-\left(x^3+x^2y\right)$, $Q=xy^2+y^3$. By **Theorem 2.2**,

$$
\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=y^2+x^2+2xy.
$$

The circular region $D$ is symmetric about $x=0,y=0$, so $\iint_D xy\,\mathrm{d}x\mathrm{d}y=0$. Using polar coordinates,

$$
\oint_{L^+}=\iint_D\left(x^2+y^2\right)\,\mathrm{d}x\mathrm{d}y=\int_0^{2\pi}\mathrm{d}\theta\int_0^R r^2\cdot r\,\mathrm{d}r=2\pi\cdot\frac{R^4}{4}=\frac{\pi R^4}{2}.
$$

(2) $P=\sqrt{x^2+y^2}$,

$$
Q=y\left[xy+\ln\left(x+\sqrt{x^2+y^2}\right)\right].
$$

Computing:

$$
\frac{\partial P}{\partial y}=\frac{y}{\sqrt{x^2+y^2}},\frac{\partial Q}{\partial x}=y^2+\frac{y}{\sqrt{x^2+y^2}}.
$$

Hence $\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=y^2$. The triangular region $D$: $1\le x\le2$, $x\le y\le4-x$. By **Theorem 2.2**,

$$
\oint_{L^+}=\int_1^2\mathrm{d}x\int_x^{4-x}y^2\,\mathrm{d}y=\frac13\int_1^2\left[\left(4-x\right)^3-x^3\right]\mathrm{d}x=\frac{25}{6}.
$$

(3) $P=e^x\sin y+\sin x-8y$, $Q=e^x\cos y-\sin y$. Computing:

$$
\frac{\partial Q}{\partial x}=e^x\cos y,\frac{\partial P}{\partial y}=e^x\cos y-8.
$$

Hence $\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=8$. The upper semicircle $y=\sqrt{ax-x^2}$ has radius $a/2$ and area $\pi a^2/8$. By **Theorem 2.2**,

$$
\oint_{L^+}=8\cdot\frac{\pi a^2}{8}=\pi a^2.

$$

$\blacksquare$
### Problem 4

(Problem 9.2-4) Let $L$ be a piecewise smooth simple closed curve in the plane. Suppose also that $v=f\left(u\right)$ is a differentiable function on $\left(-\infty,+\infty\right)$ with $f'\left(u\right)$ continuous. Prove that

$$
\displaystyle\oint_{L^+}f\left(xy\right)\left(y\,\mathrm{d}x+x\,\mathrm{d}y\right)=0.
$$

### Solution to Problem 4

Here $P=yf\left(xy\right)$, $Q=xf\left(xy\right)$. Computing the partial derivatives:

$$
\frac{\partial P}{\partial y}=f\left(xy\right)+xyf'\left(xy\right),\frac{\partial Q}{\partial x}=f\left(xy\right)+xyf'\left(xy\right).
$$

Hence $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$ holds everywhere in the region $D$ enclosed by $L$. By **Theorem 2.2** (Green's Formula),

$$
\oint_{L^+}f\left(xy\right)\left(y\,\mathrm{d}x+x\,\mathrm{d}y\right)=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y=0.

$$

$\blacksquare$
### Problem 5

(Problem 9.2-5-3)

$$
\displaystyle\int_{\left(0,0\right)}^{\left(a,b\right)}e^x\cos y\,\mathrm{d}x-e^x\sin y\,\mathrm{d}y.
$$

### Solution to Problem 5

Here $P=e^x\cos y$, $Q=-e^x\sin y$. The whole plane is simply connected, and

$$
\frac{\partial P}{\partial y}=-e^x\sin y=\frac{\partial Q}{\partial x}.
$$

By **Theorem 2.4** (Condition for a Path-Independent Integral), this integral is path-independent. Moreover, note that

$$
\mathrm{d}\left(e^x\cos y\right)=e^x\cos y\,\mathrm{d}x-e^x\sin y\,\mathrm{d}y,
$$

i.e. the integrand is an exact differential form, and $u=e^x\cos y$ is a primitive. By **Theorem 2.5**,

$$
\int_{\left(0,0\right)}^{\left(a,b\right)}e^x\cos y\,\mathrm{d}x-e^x\sin y\,\mathrm{d}y=\left.e^x\cos y\right|_{\left(0,0\right)}^{\left(a,b\right)}=e^a\cos b-1.

$$

$\blacksquare$
### Problem 6

(Problem 9.2-6) Let $A> 0,B> 0$ be constants. Let $L_r$ be the ellipse $A^2x^2+B^2y^2=r^2$ ($r> 0$). Prove that $\displaystyle\oint_{L_r^+}\frac{x\,\mathrm{d}y-y\,\mathrm{d}x}{A^2x^2+B^2y^2}=\frac{2\pi}{AB}$, where $L_r^+$ means the integral is taken along $L_r$ in the counterclockwise direction.

### Solution to Problem 6

On $L_r$, $A^2x^2+B^2y^2=r^2$, so the denominator is the constant $r^2$. Thus

$$
\oint_{L_r^+}\frac{x\,\mathrm{d}y-y\,\mathrm{d}x}{A^2x^2+B^2y^2}=\frac1{r^2}\oint_{L_r^+}x\,\mathrm{d}y-y\,\mathrm{d}x.
$$

By a corollary of **Theorem 2.2** (Green's Formula), $\oint_{L_r^+}x\,\mathrm{d}y-y\,\mathrm{d}x=2m\left(D\right)$, where $m\left(D\right)$ is the area of the ellipse $A^2x^2+B^2y^2=r^2$. The semi-axes of this ellipse are $r/A$ and $r/B$, so $m\left(D\right)=\pi\cdot\frac rA\cdot\frac rB=\frac{\pi r^2}{AB}$. Therefore

$$
\oint_{L_r^+}\frac{x\,\mathrm{d}y-y\,\mathrm{d}x}{A^2x^2+B^2y^2}=\frac1{r^2}\cdot\frac{2\pi r^2}{AB}=\frac{2\pi}{AB}.

$$

$\blacksquare$
### Problem 7

(Problem 9.2-7) Under the assumptions of the previous problem, prove that for any piecewise smooth simple closed curve $\Gamma$, as long as the origin $\left(0,0\right)$ lies in the interior of $\Gamma$, we have $\displaystyle\oint_{\Gamma^+}\frac{x\,\mathrm{d}y-y\,\mathrm{d}x}{A^2x^2+B^2y^2}=\frac{2\pi}{AB}$, where $\Gamma^+$ denotes the counterclockwise direction.

### Solution to Problem 7

Write $P=\frac{-y}{A^2x^2+B^2y^2}$, $Q=\frac{x}{A^2x^2+B^2y^2}$. At points with $\left(x,y\right)\ne\left(0,0\right)$,

$$
\frac{\partial Q}{\partial x}=\frac{A^2y^2-B^2x^2}{\left(A^2x^2+B^2y^2\right)^2}=\frac{\partial P}{\partial y}.
$$

Take a sufficiently small $r> 0$ so that the ellipse $L_r$ lies entirely in the interior of $\Gamma$. Applying **Theorem 2.3** (Green's Formula on Multiply Connected Regions) to the multiply connected region between $\Gamma$ and $L_r$, take the outer boundary $\Gamma$ in the positive direction and the inner boundary $L_r$ in the clockwise direction. Since in this region $\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=0$, we get

$$
\oint_{\Gamma^+}P\,\mathrm{d}x+Q\,\mathrm{d}y-\oint_{L_r^+}P\,\mathrm{d}x+Q\,\mathrm{d}y=0,
$$

i.e. $\oint_{\Gamma^+}=\oint_{L_r^+}$. By the result of Problem 6, $\oint_{L_r^+}=\frac{2\pi}{AB}$, so the original integral $=\frac{2\pi}{AB}$. $\blacksquare$
