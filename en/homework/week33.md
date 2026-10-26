# Assignment 33

> **Theorem 1.2** (Arc Length Formula for a Smooth Curve) Let the parametric equations of a space curve $L$ be $x=x\left(t\right)$, $y=y\left(t\right)$, $z=z\left(t\right)$ ($\alpha\le t\le\beta$), and suppose $x'\left(t\right),y'\left(t\right),z'\left(t\right)$ are continuous on $\left[\alpha,\beta\right]$. Then $L$ is rectifiable, and the arc length is

$$
s=\int_\alpha^\beta\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm{d}t.
$$

Arc differential

$$
\mathrm{d}s=\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm{d}t.
$$

> **Theorem 1.3** (Computation of Line Integrals of the First Kind) Let $L$ be a smooth curve with the same parametric equations as above, and let $f\left(x,y,z\right)$ be continuous on $L$. Then

$$
\int_L f\left(x,y,z\right)\,\mathrm{d}s=\int_\alpha^\beta f\left(x\left(t\right),y\left(t\right),z\left(t\right)\right)\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm{d}t.
$$

Note that the upper limit $\beta$ must be greater than the lower limit $\alpha$.

### Problem 1

(Problem 9.1-1) Find the arc length of the first arch of the cycloid

$$
\begin{cases}x=a\left(t-\sin t\right),\y=a\left(1-\cos t\right),\end{cases}\left(0\le t\le2\pi\right)
$$

, where $a> 0$.

### Solution to Problem 1

$x'\left(t\right)=a\left(1-\cos t\right)$, $y'\left(t\right)=a\sin t$. By **Theorem 1.2**,

$$
\mathrm{d}s=\sqrt{a^2\left(1-\cos t\right)^2+a^2\sin^2t}\,\mathrm{d}t=a\sqrt{2-2\cos t}\,\mathrm{d}t=2a\sin\frac t2\,\mathrm{d}t.
$$

Hence the arc length is

$$
s=\int_0^{2\pi}2a\sin\frac t2\,\mathrm{d}t=2a\left[-2\cos\frac t2\right]_0^{2\pi}=8a.

$$

$\blacksquare$
### Problem 2

(Problem 9.1-3) Find the arc length of the Archimedean spiral

$$
\begin{cases}x=at\cos t,\y=at\sin t,\end{cases}\left(0\le t\le2\pi\right)
$$

.

### Solution to Problem 2

$x'\left(t\right)=a\left(\cos t-t\sin t\right)$, $y'\left(t\right)=a\left(\sin t+t\cos t\right)$. By **Theorem 1.2**,

$$
\mathrm{d}s=a\sqrt{\left(\cos t-t\sin t\right)^2+\left(\sin t+t\cos t\right)^2}\,\mathrm{d}t=a\sqrt{1+t^2}\,\mathrm{d}t.
$$

Hence the arc length is

$$
s=\int_0^{2\pi}a\sqrt{1+t^2}\,\mathrm{d}t=a\left[\frac t2\sqrt{1+t^2}+\frac12\ln\left(t+\sqrt{1+t^2}\right)\right]_0^{2\pi}=a\pi\sqrt{1+4\pi^2}+\frac a2\ln\left(2\pi+\sqrt{1+4\pi^2}\right).

$$

$\blacksquare$
### Problem 3

(Problem 9.1-4) Evaluate the first-kind line integral $\displaystyle\oint_L xy\,\mathrm{d}s$, where $L$ is the square $\left| x\right|+\left| y\right|=a$ ($a> 0$).

### Solution to Problem 3

$L$ is symmetric about the $x$-axis (i.e. $\left(x,y\right)\in L\Rightarrow\left(x,-y\right)\in L$), while the integrand $f\left(x,y\right)=xy$ is an odd function in $y$: $f\left(x,-y\right)=-f\left(x,y\right)$. The arc element $\mathrm{d}s$ is the same at symmetric points, so the integrals over the two symmetric segments are negatives of each other and cancel. Therefore

$$
\oint_L xy\,\mathrm{d}s=0.

$$

$\blacksquare$
### Problem 4

(Problem 9.1-7) Evaluate $\displaystyle\int_L xy\,\mathrm{d}s$, where $L$ is the portion of the ellipse $\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$ in the first quadrant.

### Solution to Problem 4

Take the parametric equations $x=a\cos t$, $y=b\sin t$ ($0\le t\le\pi/2$). By **Theorem 1.3**,

$$
\mathrm{d}s=\sqrt{a^2\sin^2t+b^2\cos^2t}\,\mathrm{d}t.
$$

Hence

$$
\int_L xy\,\mathrm{d}s=\int_0^{\pi/2}ab\cos t\sin t\sqrt{a^2\sin^2t+b^2\cos^2t}\,\mathrm{d}t.
$$

Let $u=a^2\sin^2t+b^2\cos^2t$,

$$
\mathrm{d}u=2\left(a^2-b^2\right)\sin t\cos t\,\mathrm{d}t.
$$

When $t=0$, $u=b^2$, and when $t=\pi/2$, $u=a^2$. Thus

$$
\int_L xy\,\mathrm{d}s=\frac{ab}{2\left(a^2-b^2\right)}\int_{b^2}^{a^2}\sqrt u\,\mathrm{d}u=\frac{ab}{2\left(a^2-b^2\right)}\cdot\frac23\left(a^3-b^3\right)=\frac{ab\left(a^2+ab+b^2\right)}{3\left(a+b\right)}.

$$

$\blacksquare$
### Problem 5

(Problem 9.1-8) Evaluate $\displaystyle\int_L x^2\,\mathrm{d}s$, where the parametric equations of $L$ are

$$
\begin{cases}
x=\frac a{\sqrt2}\left(\frac1{\sqrt3}\cos t-\sin t\right),\\[4pt\right]
y=\frac a{\sqrt2}\left(\frac1{\sqrt3}\cos t+\sin t\right),\\[4pt\right]
z=-\frac{\sqrt2}{\sqrt3}a\cos t,
\end{cases}\left(0\le t\le2\pi,a> 0\right).
$$

### Solution to Problem 5

Differentiating:

$$
x'=\frac a{\sqrt2}\left(-\frac1{\sqrt3}\sin t-\cos t\right), y'=\frac a{\sqrt2}\left(-\frac1{\sqrt3}\sin t+\cos t\right), z'=\frac{\sqrt2}{\sqrt3}a\sin t.
$$

Computing the arc element:

$$
\left[x'\right]^2+\left[y'\right]^2+\left[z'\right]^2=\frac{a^2}{2}\left(\frac13\sin^2t+\frac2{\sqrt3}\sin t\cos t+\cos^2t\right)+\frac{a^2}{2}\left(\frac13\sin^2t-\frac2{\sqrt3}\sin t\cos t+\cos^2t\right)+\frac{2a^2}{3}\sin^2t=a^2\sin^2t+a^2\cos^2t=a^2.
$$

Hence $\mathrm{d}s=a\,\mathrm{d}t$. Moreover,

$$
x^2=\frac{a^2}{2}\left(\frac1{\sqrt3}\cos t-\sin t\right)^2=\frac{a^2}{2}\left(\frac13\cos^2t-\frac2{\sqrt3}\sin t\cos t+\sin^2t\right).
$$

By **Theorem 1.3**, noting that $\int_0^{2\pi}\sin t\cos t\,\mathrm{d}t=0$,

$$
\int_0^{2\pi}\cos^2t\,\mathrm{d}t=\int_0^{2\pi}\sin^2t\,\mathrm{d}t=\pi,
$$

we get

$$
\int_L x^2\,\mathrm{d}s=\int_0^{2\pi}x^2\cdot a\,\mathrm{d}t=\frac{a^3}{2}\left(\frac13\pi+\pi\right)=\frac{2\pi a^3}{3}.

$$

$\blacksquare$