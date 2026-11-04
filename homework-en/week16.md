# week16

> **Theorem 2.1 (Cauchy Mean Value Theorem)**
> 
> If $f$ and $g$ are continuous on $\left[a,b\right]$, differentiable on $\left(a,b\right)$, and $g'\left(x\right)\ne0$ for $a< x< b$, then there exists $c\in\left(a,b\right)$ such that $\frac{f\left(b\right)-f\left(a\right)}{g\left(b\right)-g\left(a\right)}=\frac{f'\left(c\right)}{g'\left(c\right)}$.

> **Theorem 2.2 (L'Hôpital's Rule, $\frac00$ Case)**
> 
> If $f$ and $g$ are defined and differentiable in a punctured neighborhood of $a$, $g'\left(x\right)\ne0$, $\lim_{x\to a}f\left(x\right)=\lim_{x\to a}g\left(x\right)=0$, and $\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ exists, then $\lim_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$.

> **Theorem 2.3 (L'Hôpital's Rule, $\frac{\infty}{\infty}$ Case)**
> 
> If $f$ and $g$ are defined and differentiable in a punctured neighborhood of $a$, $g'\left(x\right)\ne0$, $\lim_{x\to a}f\left(x\right)=\lim_{x\to a}g\left(x\right)=\infty$, and $\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$ exists, then $\lim_{x\to a}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\to a}\frac{f'\left(x\right)}{g'\left(x\right)}$.

> **Proposition 3.1 (Unique Extremum is Global)**
> 
> If $f$ is continuous on $\left(a,b\right)$ (or $\left[a,b\right]$) and $x_0$ is the only extremum point, then it is the global maximum (if a local max) or global minimum (if a local min).

> **Theorem 3.1 (First Sufficient Condition for Extrema)**
> 
> If $f$ is differentiable on $\left(a,b\right)$ with $f'\left(x_0\right)=0$, and $f'> 0$ on $\left(x_0-r,x_0\right)$ while $f'< 0$ on $\left(x_0,x_0+r\right)$, then $f\left(x_0\right)$ is a local maximum; if the signs are reversed, it is a local minimum.

> **Theorem 3.2 (Second Sufficient Condition for Extrema)**
> 
> If $f'\left(x_0\right)=0$ and $f''\left(x_0\right)$ exists, then $f''\left(x_0\right)> 0$ implies $x_0$ is a local minimum, and $f''\left(x_0\right)< 0$ implies $x_0$ is a local maximum.

## 3.2-6

Find $c$ such that $\lim_{x\to\infty}\left(\frac{x+c}{x-c}\right)^x=e^2$.

### Solution to 3.2-6

This is $1^\infty$. Let $y=\left(\frac{x+c}{x-c}\right)^x$. Then

$$
\ln y=x\ln\left(1+\frac{2c}{x-c}\right)\sim x\cdot\frac{2c}{x-c}\to2c.
$$

Thus $\lim y=e^{2c}$. Setting $e^{2c}=e^2$ gives $c=1$. $\blacksquare$

## 3.3-1-1

Find the stationary points of $y=x\left(3x^2-5\right)^2$ and classify them.

### Solution to 3.3-1-1

Differentiating,

$$
y'=5\left(3x^2-5\right)\left(3x^2-1\right).
$$

Setting $y'=0$ gives $x=\pm\sqrt{\frac53}$, $\pm\frac1{\sqrt3}$. The second derivative is

$$
y''=30x\left(30x^2-26\right).
$$

At $x=\sqrt{\frac53}$ and $x=-\frac1{\sqrt3}$, $y''> 0$ (local minima); at $x=-\sqrt{\frac53}$ and $x=\frac1{\sqrt3}$, $y''< 0$ (local maxima). By **Theorem 3.2 (Second Sufficient Condition for Extrema)**, the classification holds. $\blacksquare$

## 3.3-1-3

Find the stationary points of $y=x\ln x$ ($x> 0$) and classify them.

### Solution to 3.3-1-3

$y'=\ln x+1=0$ gives $x=\frac1e$. Since $y''=\frac1x> 0$, by **Theorem 3.2 (Second Sufficient Condition for Extrema)**, $x=\frac1e$ is a local minimum with value $-\frac1e$. $\blacksquare$

## 3.3-2

Let $f$ be continuous on $\left[a,b\right]$ with a unique extremum point in $\left(a,b\right)$. Prove: (1) it is a strict local max or min; (2) if it is a local max, it is the global maximum; if a local min, the global minimum.

### Solution to 3.3-2

(1) Let $x_0$ be the unique extremum. If it is not a strict local maximum, then there are points arbitrarily close with $f\left(x\right)\ge f\left(x_0\right)$, which would force $f$ to be locally constant, yielding infinitely many extrema, contradicting uniqueness. Hence $x_0$ is strict.

(2) Suppose $x_0$ is a local maximum. If $f\left(x_0\right)$ is not the global maximum, there exists $x_1$ with $f\left(x_1\right)> f\left(x_0\right)$. On $\left[x_0,x_1\right]$, since $f\left(x_1\right)> f\left(x_0\right)$ and $x_0$ is a strict local max, the minimum is attained at an interior point, giving a local minimum, contradicting uniqueness. Hence $f\left(x_0\right)$ is the global maximum. This is **Proposition 3.1 (Unique Extremum is Global)**. $\blacksquare$

## 3.3-3

(Snell's Law) Light travels from medium I to medium II with speeds $v_1$ and $v_2$. Snell's law states $\frac{\sin\alpha}{\sin\beta}=\frac{v_1}{v_2}$. Prove that the actual path minimizes travel time.

### Solution to 3.3-3

Let the interface be the $x$-axis, $A=\left(0,a\right)$, $B=\left(d,-b\right)$, and the entry point be $P=\left(x,0\right)$. Total time:

$$
T\left(x\right)=\frac{\sqrt{x^2+a^2}}{v_1}+\frac{\sqrt{\left(d-x\right)^2+b^2}}{v_2}.
$$

Differentiating,

$$
T'\left(x\right)=\frac{\sin\alpha}{v_1}-\frac{\sin\beta}{v_2}.
$$

Setting $T'\left(x\right)=0$ gives $\frac{\sin\alpha}{\sin\beta}=\frac{v_1}{v_2}$, i.e. Snell's law. Since $T''\left(x\right)> 0$, this is a minimum. By **Proposition 3.1 (Unique Extremum is Global)**, it is the global minimum time. $\blacksquare$

## 3.3-4

A lamp moves along a vertical line $OB$, and $OA$ is a horizontal segment of length $a$. At what height above $O$ is the illumination at $A$ maximized?

### Solution to 3.3-4

Let the height be $h$. Illumination is proportional to $\cos\theta/r^2$ where $r=\sqrt{a^2+h^2}$ and $\cos\theta=h/r$. Thus

$$
J\left(h\right)=\frac{Ch}{\left(a^2+h^2\right)^{3/2}}.
$$

Differentiating,

$$
J'\left(h\right)=C\cdot\frac{a^2-2h^2}{\left(a^2+h^2\right)^{5/2}}.
$$

Setting $J'\left(h\right)=0$ gives $h=\frac{a}{\sqrt2}$. By **Theorem 3.1 (First Sufficient Condition for Extrema)**, this is a maximum. By **Proposition 3.1 (Unique Extremum is Global)**, it is the global maximum. $\blacksquare$
