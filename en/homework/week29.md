# Assignment 29

> **Theorem 2.1** (Reducing a Double Integral to an Iterated Integral) Let $z=f\left(x,y\right)$ be continuous on a closed region $D$,
> $$
> D=\left\{\left(x,y\right):a\le x\le b,\varphi_1\left(x\right)\le y\le\varphi_2\left(x\right)\right\},
> $$
> where $\varphi_1,\varphi_2$ are continuous on $\left[a,b\right]$. Then

$$
\iint_D f\left(x,y\right)\,\mathrm{d}x\mathrm{d}y=\int_a^b\mathrm{d}x\int_{\varphi_1\left(x\right)}^{\varphi_2\left(x\right)}f\left(x,y\right)\,\mathrm{d}y.
$$

> **Theorem 2.2** (Double Integrals in Polar Coordinates) Let $D$ be a bounded closed region that is rectifiable, and let $z=f\left(x,y\right)$ be integrable on $D$. Then

$$
\iint_D f\left(x,y\right)\,\mathrm{d}x\mathrm{d}y=\iint_{D^*}f\left(r\cos\theta,r\sin\theta\right)\,r\,\mathrm{d}r\mathrm{d}\theta,
$$

where

$$
D^*=\left\{\left(r,\theta\right):\left(r\cos\theta,r\sin\theta\right)\in D\right\}.
$$

### Problem 1

(Problem 8.2-2) Reverse the order of integration in the following iterated integrals:
(1) $\displaystyle\int_0^1\mathrm{d}y\int_y^{\sqrt y}f\left(x,y\right)\,\mathrm{d}x$;

(2) $\displaystyle\int_1^2\mathrm{d}x\int_x^{2x}f\left(x,y\right)\,\mathrm{d}y$;

(3) $\displaystyle\int_0^5\mathrm{d}x\int_x^{10-x}f\left(x,y\right)\,\mathrm{d}y$;

(4) $\displaystyle\int_0^1\mathrm{d}x\int_{e^x}^e f\left(x,y\right)\,\mathrm{d}y$.

### Solution to Problem 1

(1) Original region of integration: $0\le y\le1$, $y\le x\le\sqrt y$. From $y\le x\le\sqrt y$ we get $x^2\le y\le x$, and $0\le x\le1$. Hence

$$
\int_0^1\mathrm{d}y\int_y^{\sqrt y}f\left(x,y\right)\,\mathrm{d}x=\int_0^1\mathrm{d}x\int_{x^2}^x f\left(x,y\right)\,\mathrm{d}y.
$$

(2) Original region: $1\le x\le2$, $x\le y\le2x$. Split by $y$: when $y\in\left[1,2\right]$, $1\le x\le y$; when $y\in\left[2,4\right]$, $y/2\le x\le2$. Hence

$$
\int_1^2\mathrm{d}x\int_x^{2x}f\left(x,y\right)\,\mathrm{d}y=\int_1^2\mathrm{d}y\int_1^y f\left(x,y\right)\,\mathrm{d}x+\int_2^4\mathrm{d}y\int_{y/2}^2 f\left(x,y\right)\,\mathrm{d}x.
$$

(3) Original region: $0\le x\le5$, $x\le y\le10-x$. Split by $y$: when $y\in\left[0,5\right]$, $0\le x\le y$; when $y\in\left[5,10\right]$, $0\le x\le10-y$. Hence

$$
\int_0^5\mathrm{d}x\int_x^{10-x}f\left(x,y\right)\,\mathrm{d}y=\int_0^5\mathrm{d}y\int_0^y f\left(x,y\right)\,\mathrm{d}x+\int_5^10\mathrm{d}y\int_0^{10-y}f\left(x,y\right)\,\mathrm{d}x.
$$

(4) Original region: $0\le x\le1$, $e^x\le y\le e$, i.e. $0\le x\le\ln y$. Hence

$$
\int_0^1\mathrm{d}x\int_{e^x}^e f\left(x,y\right)\,\mathrm{d}y=\int_1^e\mathrm{d}y\int_0^{\ln y}f\left(x,y\right)\,\mathrm{d}x.

$$

$\blacksquare$
### Problem 2

(Problem 8.2-3) Evaluate the following double integrals:
(1) $\displaystyle\iint_D y\,\mathrm{d}x\mathrm{d}y$, where $D$ is the region bounded by the line $y=0$ and the curve $y=\sin x$ ($0\le x\le\pi$);

(2) $\displaystyle\iint_D\left(x^2+y\right)\,\mathrm{d}x\mathrm{d}y$, where $D$ is the region bounded by the curves $y=x^2$ and $y^2=x$;

(3) $\displaystyle\iint_D e^{x/y}\,\mathrm{d}x\mathrm{d}y$, where $D$ is the region bounded by $y^2=x$, $x=0$, and $y=1$;

(4) $\displaystyle\iint_D\sqrt{1-x^4}\,\mathrm{d}x\mathrm{d}y$, where $D$ is the region bounded by $y=x^3$, $x=1$, and $y=0$.

### Solution to Problem 2

(1) $D:0\le x\le\pi$, $0\le y\le\sin x$. By **Theorem 2.1**,

$$
\iint_D y\,\mathrm{d}x\mathrm{d}y=\int_0^\pi\mathrm{d}x\int_0^{\sin x}y\,\mathrm{d}y=\frac12\int_0^\pi\sin^2x\,\mathrm{d}x=\frac\pi4.
$$

(2) $D:0\le x\le1$, $x^2\le y\le\sqrt x$. By **Theorem 2.1**,

$$
\iint_D\left(x^2+y\right)\,\mathrm{d}x\mathrm{d}y=\int_0^1\mathrm{d}x\int_{x^2}^{\sqrt x}\left(x^2+y\right)\,\mathrm{d}y=\int_0^1\left(x^{5/2}+\frac x2-\frac32x^4\right)\mathrm{d}x=\frac27+\frac14-\frac3{10}=\frac{33}{140}.
$$

(3) $D:0\le y\le1$, $0\le x\le y^2$. By **Theorem 2.1** (integrate with respect to $x$ first),

$$
\iint_D e^{x/y}\,\mathrm{d}x\mathrm{d}y=\int_0^1\mathrm{d}y\int_0^{y^2}e^{x/y}\,\mathrm{d}x=\int_0^1\left(ye^y-y\right)\mathrm{d}y=\left[ye^y-e^y-\frac12y^2\right]_0^1=\frac12.
$$

(4) $D:0\le x\le1$, $0\le y\le x^3$. By **Theorem 2.1**,

$$
\iint_D\sqrt{1-x^4}\,\mathrm{d}x\mathrm{d}y=\int_0^1\mathrm{d}x\int_0^{x^3}\sqrt{1-x^4}\,\mathrm{d}y=\int_0^1x^3\sqrt{1-x^4}\,\mathrm{d}x.
$$

Let $u=1-x^4$, $\mathrm{d}u=-4x^3\mathrm{d}x$, giving

$$
\iint_D\sqrt{1-x^4}\,\mathrm{d}x\mathrm{d}y=\frac14\int_0^1\sqrt u\,\mathrm{d}u=\frac16.

$$

$\blacksquare$
### Problem 3

(Problem 8.2-4) Evaluate the following iterated integrals:
(1) $\displaystyle\int_0^\pi\mathrm{d}x\int_x^\pi\frac{\sin y}{y}\,\mathrm{d}y$;

(2) $\displaystyle\int_0^2\mathrm{d}x\int_x^2 2y^2\sin\left(xy\right)\,\mathrm{d}y$.

### Solution to Problem 3

(1) Original region of integration: $0\le x\le\pi$, $x\le y\le\pi$. Reversing the order of integration (by **Theorem 2.1**) gives $0\le y\le\pi$, $0\le x\le y$, hence

$$
\int_0^\pi\mathrm{d}x\int_x^\pi\frac{\sin y}{y}\,\mathrm{d}y=\int_0^\pi\mathrm{d}y\int_0^y\frac{\sin y}{y}\,\mathrm{d}x=\int_0^\pi\sin y\,\mathrm{d}y=2.
$$

(2) Original region: $0\le x\le2$, $x\le y\le2$. Reversing the order gives $0\le y\le2$, $0\le x\le y$. Hence

$$
\int_0^2\mathrm{d}x\int_x^2 2y^2\sin\left(xy\right)\,\mathrm{d}y=\int_0^2\mathrm{d}y\int_0^y 2y^2\sin\left(xy\right)\,\mathrm{d}x=\int_0^2 2y\left[1-\cos\left(y^2\right)\right]\,\mathrm{d}y=\left[y^2-\sin\left(y^2\right)\right]_0^2=4-\sin4.

$$

$\blacksquare$
### Problem 4

(Problem 8.2-5) Convert the following iterated integrals into double integrals, then evaluate the double integrals using polar coordinates:
(1)

$$
\displaystyle\int_{-1}^0\mathrm{d}x\int_{-\sqrt{1-x^2}}^0\frac{2}{1+\sqrt{x^2+y^2}}\,\mathrm{d}y;
$$

(2) $\displaystyle\int_0^2\mathrm{d}x\int_0^{\sqrt{1-\left(x-1\right)^2}}3xy\,\mathrm{d}y$;

(3)

$$
\displaystyle\int_0^R\mathrm{d}x\int_0^{\sqrt{R^2-x^2}}\ln\left(1+x^2+y^2\right)\,\mathrm{d}y\left(R> 0\right).
$$

### Solution to Problem 4

(1) The original region is the part of the unit circle in the third quadrant ($x\le0$, $y\le0$). By **Theorem 2.2**, $\theta\in\left[\pi,3\pi/2\right]$, $r\in\left[0,1\right]$,

$$
\iint_D\frac{2}{1+\sqrt{x^2+y^2}}\,\mathrm{d}x\mathrm{d}y=\int_\pi^{3\pi/2}\mathrm{d}\theta\int_0^1\frac{2}{1+r}\,r\,\mathrm{d}r=\pi\left[r-\ln\left(1+r\right)\right]_0^1=\pi\left(1-\ln2\right).
$$

(2) The original region is the upper half of the circle $\left(x-1\right)^2+y^2\le1$, whose polar equation is $r=2\cos\theta$, $\theta\in\left[0,\pi/2\right]$. By **Theorem 2.2**,

$$
\iint_D 3xy\,\mathrm{d}x\mathrm{d}y=\int_0^{\pi/2}\mathrm{d}\theta\int_0^{2\cos\theta}3\left(r\cos\theta\right)\left(r\sin\theta\right)\,r\,\mathrm{d}r=12\int_0^{\pi/2}\sin\theta\cos^5\theta\,\mathrm{d}\theta=2.
$$

(3) The original region is the quarter disk in the first quadrant $x^2+y^2\le R^2$, $x,y\ge0$. By **Theorem 2.2**,

$$
\iint_D\ln\left(1+x^2+y^2\right)\,\mathrm{d}x\mathrm{d}y=\int_0^{\pi/2}\mathrm{d}\theta\int_0^R\ln\left(1+r^2\right)\,r\,\mathrm{d}r=\frac\pi2\cdot\frac12\left[\left(1+r^2\right)\ln\left(1+r^2\right)-r^2\right]_0^R=\frac\pi4\left[\left(1+R^2\right)\ln\left(1+R^2\right)-R^2\right].

$$

$\blacksquare$
### Problem 5

(Problem 8.2-6) Evaluate the double integral $\displaystyle\iint_D e^{-x^2-y^2}\,\mathrm{d}x\mathrm{d}y$, where $D$ is the annulus

$$
\left\{\left(x,y\right):1\le x^2+y^2\le4\right\}
$$

in the first quadrant.

### Solution to Problem 5

By **Theorem 2.2**, the polar-coordinate representation of $D$ is $\theta\in\left[0,\pi/2\right]$, $r\in\left[1,2\right]$, hence

$$
\iint_D e^{-x^2-y^2}\,\mathrm{d}x\mathrm{d}y=\int_0^{\pi/2}\mathrm{d}\theta\int_1^2 e^{-r^2}r\,\mathrm{d}r=\frac\pi2\cdot\left[-\frac12e^{-r^2}\right]_1^2=\frac\pi4\left(e^{-1}-e^{-4}\right).

$$

$\blacksquare$
### Problem 6

(Problem 8.2-7) Evaluate the following double integrals:
(1) $\displaystyle\iint_D\sin\sqrt{x^2+y^2}\,\mathrm{d}x\mathrm{d}y$, where

$$
D=\left\{\left(x,y\right):\pi^2\le x^2+y^2\le4\pi^2\right\};
$$

(2) $\displaystyle\iint_D\left(x+y\right)\,\mathrm{d}x\mathrm{d}y$, where

$$
D=\left\{\left(x,y\right):x^2+y^2\le x+y\right\};
$$

(3) $\displaystyle\iint_D\left(x^2+y^2\right)\,\mathrm{d}x\mathrm{d}y$, where

$$
D=\left\{\left(x,y\right):\left(x^2+y^2\right)^2\le a^2\left(x^2-y^2\right)\right\};
$$

(4) $\displaystyle\iint_D x\,\mathrm{d}x\mathrm{d}y$, where $D$ is the region bounded by the Archimedean spiral $r=\theta$ and the ray $\theta=\pi$.

### Solution to Problem 6

(1) By **Theorem 2.2**, $\theta\in\left[0,2\pi\right]$, $r\in\left[\pi,2\pi\right]$,

$$
\iint_D\sin\sqrt{x^2+y^2}\,\mathrm{d}x\mathrm{d}y=\int_0^{2\pi}\mathrm{d}\theta\int_\pi^{2\pi}\sin r\cdot r\,\mathrm{d}r=2\pi\left[\sin r-r\cos r\right]_\pi^{2\pi}=2\pi\left(-2\pi-\pi\right)=-6\pi^2.
$$

(2) Rewrite $D$ as

$$
\left(x-\frac12\right)^2+\left(y-\frac12\right)^2\le\frac12.
$$

Let $u=x-\frac12$, $v=y-\frac12$; then $D$ becomes $u^2+v^2\le\frac12$. By symmetry, $\iint u=\iint v=0$, hence

$$
\iint_D\left(x+y\right)\,\mathrm{d}x\mathrm{d}y=\iint_{u^2+v^2\le1/2}\left(u+v+1\right)\,\mathrm{d}u\mathrm{d}v=\iint_{u^2+v^2\le1/2}1\,\mathrm{d}u\mathrm{d}v=\frac\pi2.
$$

(3) In polar coordinates,

$$
\left(x^2+y^2\right)^2\le a^2\left(x^2-y^2\right)
$$

becomes $r^2\le a^2\cos2\theta$, i.e. $r\le a\sqrt{\cos2\theta}$, $\cos2\theta\ge0$. Using symmetry (four symmetric petals),

$$
\iint_D\left(x^2+y^2\right)\,\mathrm{d}x\mathrm{d}y=4\int_0^{\pi/4}\mathrm{d}\theta\int_0^{a\sqrt{\cos2\theta}}r^2\cdot r\,\mathrm{d}r=a^4\int_0^{\pi/4}\cos^22\theta\,\mathrm{d}\theta=\frac{\pi a^4}{8}.
$$

(4) By **Theorem 2.2**, $\theta\in\left[0,\pi\right]$, $r\in\left[0,\theta\right]$,

$$
\iint_D x\,\mathrm{d}x\mathrm{d}y=\int_0^\pi\mathrm{d}\theta\int_0^\theta\left(r\cos\theta\right)\,r\,\mathrm{d}r=\frac13\int_0^\pi\theta^3\cos\theta\,\mathrm{d}\theta=\frac13\left[\theta^3\sin\theta+3\theta^2\cos\theta-6\theta\sin\theta-6\cos\theta\right]_0^\pi=\frac13\left(-3\pi^2+12\right)=4-\pi^2.

$$

$\blacksquare$
### Problem 7

(Problem 8.2-8) Let $a> 0$, and set

$$
I\left(a\right)=\int_0^a e^{-x^2}\,\mathrm{d}x, J\left(a\right)=\iint_{D_a}e^{-x^2-y^2}\,\mathrm{d}x\mathrm{d}y,
$$

where

$$
D_a=\left\{\left(x,y\right)\mid x^2+y^2\le a^2,x\ge0,y\ge0\right\}.
$$

Prove:
(1)

$$
\displaystyle\left[I\left(a\right)\right]^2=\iint_{R_a}e^{-x^2-y^2}\,\mathrm{d}x\mathrm{d}y,
$$
where

$$
R_a=\left\{\left(x,y\right)\mid0\le x\le a,0\le y\le a\right\};
$$

(2)

$$
J\left(a\right)\le\left[I\left(a\right)\right]^2\le J\left(\sqrt2\,a\right);
$$

(3) using the result of Example 2.8 in this section, deduce that $\displaystyle\lim_{a\to+\infty}\int_0^a e^{-x^2}\,\mathrm{d}x=\frac{\sqrt\pi}{2}$.

### Solution to Problem 7

(1) By **Theorem 2.1**,

$$
\left[I\left(a\right)\right]^2=\left(\int_0^a e^{-x^2}\mathrm{d}x\right)\left(\int_0^a e^{-y^2}\mathrm{d}y\right)=\int_0^a\mathrm{d}x\int_0^a e^{-x^2-y^2}\mathrm{d}y=\iint_{R_a}e^{-x^2-y^2}\,\mathrm{d}x\mathrm{d}y.
$$

(2) Note that $D_a$ is a quarter disk of radius $a$, $R_a=\left[0,a\right]\times\left[0,a\right]$ is a square of side $a$, and $D_{\sqrt2 a}$ is a quarter disk of radius $\sqrt2 a$. Clearly $D_a\subset R_a\subset D_{\sqrt2 a}$. Since the integrand $e^{-x^2-y^2}> 0$, by **Property** (Comparison Property of Double Integrals) in Chapter 1,

$$
J\left(a\right)=\iint_{D_a}\le\iint_{R_a}=\left[I\left(a\right)\right]^2\le\iint_{D_{\sqrt2 a}}=J\left(\sqrt2\,a\right).
$$

(3) By **Theorem 2.2**, the polar-coordinate representation of $D_a$ is $\theta\in\left[0,\pi/2\right]$, $r\in\left[0,a\right]$, hence

$$
J\left(a\right)=\int_0^{\pi/2}\mathrm{d}\theta\int_0^a e^{-r^2}r\,\mathrm{d}r=\frac\pi2\cdot\frac{1-e^{-a^2}}2=\frac\pi4\left(1-e^{-a^2}\right).
$$

Substituting into (2) gives

$$
\frac\pi4\left(1-e^{-a^2}\right)\le\left[I\left(a\right)\right]^2\le\frac\pi4\left(1-e^{-2a^2}\right).
$$

Letting $a\to+\infty$, both ends tend to $\pi/4$. By the squeeze theorem, $\left[I\left(a\right)\right]^2\to\pi/4$, hence $I\left(a\right)\to\sqrt\pi/2$. $\blacksquare$
