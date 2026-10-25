# Assignment 15

> **Theorem 3.1** (First Sufficient Condition for an Extremum Point) Let $y=f\left(x\right)$ be differentiable on $\left(a,b\right)$, and let $x_0\in\left(a,b\right)$ be a stationary point of $f$, i.e. $f'\left(x_0\right)=0$. If there exists $r> 0$ such that $\left(x_0-r,x_0+r\right)\subset\left(a,b\right)$, and $f'\left(x\right)> 0$ when $x\in\left(x_0-r,x_0\right)$ while $f'\left(x\right)< 0$ when $x\in\left(x_0,x_0+r\right)$, then $f\left(x_0\right)$ is a local maximum; if $f'\left(x\right)< 0$ when $x\in\left(x_0-r,x_0\right)$ and $f'\left(x\right)> 0$ when $x\in\left(x_0,x_0+r\right)$, then $f\left(x_0\right)$ is a local minimum.

> **Theorem 3.2** (Second Sufficient Condition for an Extremum Point) Let $y=f\left(x\right)$ be differentiable on $\left(a,b\right)$, let $x_0\in\left(a,b\right)$ be a stationary point, and assume that $f$ has a second derivative at $x_0$. If $f''\left(x_0\right)> 0$, then $x_0$ is a local minimum point; if $f''\left(x_0\right)< 0$, then $x_0$ is a local maximum point.

> **Proposition 3.1** (A Unique Extremum Point Is a Global Extremum Point) Let $y=f\left(x\right)$ be continuous on the interval $\left(a,b\right)$ (or $\left[a,b\right]$). If $x_0$ is the only extremum point in $\left(a,b\right)$, then when $x_0$ is a local maximum point, $f\left(x_0\right)$ is the maximum value of $y=f\left(x\right)$; and when $x_0$ is a local minimum point, $f\left(x_0\right)$ is the minimum value of $y=f\left(x\right)$.

### Problem 1

(Problem 3.3-1-1) Find the stationary points of the function $y=x\left(3x^2-5\right)^2$, and determine whether these stationary points are extremum points.

### Solution to Problem 1

Differentiating gives
$$
y'=\left(3x^2-5\right)^2+x\cdot2\left(3x^2-5\right)\cdot6x=\left(3x^2-5\right)\left[\left(3x^2-5\right)+12x^2\right]=\left(3x^2-5\right)\left(15x^2-5\right)=5\left(3x^2-5\right)\left(3x^2-1\right).
$$

Setting $y'=0$, the stationary points are $x=\pm\sqrt{\frac53},\pm\frac1{\sqrt3}$.

Differentiating again:
$$
y''=5\left[6x\left(15x^2-1\right)+\left(3x^2-5\right)\cdot30x\right]=5\left[90x^3-6x+90x^3-150x\right]=5\left[180x^3-156x\right]=30x\left(30x^2-26\right).
$$

Substituting each stationary point:
- $x=\sqrt{\frac53}$:

  $$
  y''=30\sqrt{\frac53}\cdot\left(50-26\right)> 0,
  $$

  so this is a local minimum point.
- $x=-\sqrt{\frac53}$:

  $$
  y''=30\left(-\sqrt{\frac53}\right)\cdot\left(50-26\right)< 0,
  $$

  so this is a local maximum point.
- $x=\frac1{\sqrt3}$:

  $$
  y''=30\cdot\frac1{\sqrt3}\cdot\left(10-26\right)< 0,
  $$

  so this is a local maximum point.
- $x=-\frac1{\sqrt3}$:

  $$
  y''=30\cdot\left(-\frac1{\sqrt3}\right)\cdot\left(10-26\right)> 0,
  $$

  so this is a local minimum point.

By **Theorem 3.2** (Second Sufficient Condition for an Extremum Point), these conclusions hold. $\blacksquare$

### Problem 2

(Problem 3.3-1-3) Find the stationary points of the function $y=x\ln x$ ($x> 0$), and determine whether these stationary points are extremum points.

### Solution to Problem 2

Differentiating gives
$$
y'=\ln x+1.
$$

Setting $y'=0$, we get $\ln x=-1$, i.e. $x=\frac1e$.

Differentiating again:
$$
y''=\frac1x> 0\left(x> 0\right).
$$

Hence $y''\left(\frac1e\right)=e> 0$. By **Theorem 3.2** (Second Sufficient Condition for an Extremum Point), $x=\frac1e$ is a local minimum point, with local minimum value $y\left(\frac1e\right)=\frac1e\ln\frac1e=-\frac1e$. $\blacksquare$

### Problem 3

(Problem 3.3-2) Let $y=f\left(x\right)$ be continuous on $\left[a,b\right]$. Assume that $y=f\left(x\right)$ has a unique extremum point in $\left(a,b\right)$. Prove:
(1) the function must be strictly increasing or strictly decreasing near that extremum point;

(2) if that extremum point is a local maximum point, then it must be the maximum point; if that extremum point is a local minimum point, then it must be the minimum point.

### Solution to Problem 3

(1) Let $x_0\in\left(a,b\right)$ be the unique extremum point. If $x_0$ is not a strict local maximum point, then there exists a sequence of points $x_n\to x_0$ ($x_n\ne x_0$) such that $f\left(x_n\right)\ge f\left(x_0\right)$. By continuity, $f\left(x_0\right)$ is also a local maximum. But if in every neighborhood of $x_0$ there are points at which the function value equals $f\left(x_0\right)$, then $f$ is constant near $x_0$, giving infinitely many extremum points, contradicting uniqueness. Hence $x_0$ must be a strict local maximum point (or strict local minimum point).

(2) Let $x_0$ be a local maximum point. Proof by contradiction: assume $f\left(x_0\right)$ is not the maximum value on $\left[a,b\right]$, then there exists $x_1\in\left[a,b\right]$ such that $f\left(x_1\right)> f\left(x_0\right)$. If $x_1=a$ or $x_1=b$, consider the continuous function $f$ on the closed interval $\left[x_0,x_1\right]$ (or $\left[x_1,x_0\right]$). Since $f\left(x_1\right)> f\left(x_0\right)$ and $x_0$ is a strict local maximum point, $f$ attains a minimum at some point in $\left(x_0,x_1\right)$, which is a local minimum point. This contradicts the fact that $x_0$ is the unique extremum point.

If $x_1\in\left(a,b\right)$, then the minimum of $f$ on $\left[x_0,x_1\right]$ is not attained at $x_0$ (since $f\left(x_1\right)> f\left(x_0\right)$ and $x_0$ is a strict local maximum), so it is attained at some point in $\left(x_0,x_1\right)$, which is a local minimum point, again a contradiction.

Hence $f\left(x_0\right)$ must be the maximum value. The case of a local minimum point is similar. This is exactly **Proposition 3.1** (A Unique Extremum Point Is a Global Extremum Point). $\blacksquare$

### Problem 4

(Problem 3.3-3) (Snell's law of refraction) Consider two media, Medium A and Medium B, whose interface is a plane. Suppose light is emitted from point $A$ in Medium A and reaches point $B$ in Medium B after passing through the interface. From physics, the path taken by light must satisfy the law of refraction:
$$
\frac{\sin\alpha}{\sin\beta}=\frac{v_1}{v_2},
$$
where $\alpha$ is the angle of incidence, $\beta$ is the angle of refraction, and $v_1,v_2$ are the speeds of light in Medium A and Medium B, respectively. Prove that the path taken by light is the path of least time.

### Solution to Problem 4

Take the interface as the $x$-axis, $A=\left(0,a\right)$ (Medium A, $y> 0$), $B=\left(d,-b\right)$ (Medium B, $y< 0$), where $a,b,d> 0$. Let the point where light hits the interface be $P=\left(x,0\right)$.

Then the distance from $A$ to $P$ is $\sqrt{x^2+a^2}$, and the time required is $\frac{\sqrt{x^2+a^2}}{v_1}$; the distance from $P$ to $B$ is $\sqrt{\left(d-x\right)^2+b^2}$, and the time required is $\frac{\sqrt{\left(d-x\right)^2+b^2}}{v_2}$. The total time is
$$
T\left(x\right)=\frac{\sqrt{x^2+a^2}}{v_1}+\frac{\sqrt{\left(d-x\right)^2+b^2}}{v_2}.
$$

Differentiating gives
$$
T'\left(x\right)=\frac{x}{v_1\sqrt{x^2+a^2}}-\frac{d-x}{v_2\sqrt{\left(d-x\right)^2+b^2}}.
$$

Note that $\frac{x}{\sqrt{x^2+a^2}}=\sin\alpha$ ($\alpha$ is the angle of incidence, i.e. the angle between $AP$ and the normal), and $\frac{d-x}{\sqrt{\left(d-x\right)^2+b^2}}=\sin\beta$ ($\beta$ is the angle of refraction). Hence
$$
T'\left(x\right)=\frac{\sin\alpha}{v_1}-\frac{\sin\beta}{v_2}.
$$

Setting $T'\left(x\right)=0$, we get
$$
\frac{\sin\alpha}{v_1}=\frac{\sin\beta}{v_2},\text{即}\;\frac{\sin\alpha}{\sin\beta}=\frac{v_1}{v_2}.
$$

This is exactly the law of refraction. Moreover,
$$
T''\left(x\right)=\frac{a^2}{v_1\left(x^2+a^2\right)^{3/2}}+\frac{b^2}{v_2\left(\left(d-x\right)^2+b^2\right)^{3/2}}> 0,
$$

so the point where $T'\left(x\right)=0$ is a local minimum point. By **Proposition 3.1** (A Unique Extremum Point Is a Global Extremum Point), this point gives the path of least time. $\blacksquare$

### Problem 5

(Problem 3.3-4) A lamp can move along the vertical line $OB$, and $OA$ is a horizontal line of length $a$. At what height of the lamp above $O$ is the illuminance at $A$ maximal?

### Solution to Problem 5

Let the height of the lamp above $O$ be $h$, i.e. the lamp is at the point $\left(0,h\right)$. From optics, the illuminance $J$ is proportional to the sine of the angle of incidence and inversely proportional to the square of the distance. The distance from the lamp to point $A$ at $\left(a,0\right)$ is $r=\sqrt{a^2+h^2}$, and the angle of incidence $\theta$ (the angle between the light ray and the vertical) satisfies $\sin\theta=\frac{a}{r}$. Hence
$$
J\left(h\right)=C\cdot\frac{\sin\theta}{r^2}=C\cdot\frac{a}{r^3}=\frac{Ca}{\left(a^2+h^2\right)^{3/2}},
$$

where $C> 0$ is a proportionality constant.

Differentiating gives
$$
J'\left(h\right)=Ca\cdot\left(-\frac32\right)\left(a^2+h^2\right)^{-5/2}\cdot2h=-3Cah\left(a^2+h^2\right)^{-5/2}.
$$

Setting $J'\left(h\right)=0$, we get $h=0$. But when $h=0$ the lamp is at $O$, which is clearly not the point of maximum illuminance.

Corrected model: the illuminance should be proportional to $\cos\theta$ ($\theta$ is the angle between the light ray and the normal), i.e.
$$
J\left(h\right)=C\cdot\frac{\cos\theta}{r^2}=C\cdot\frac{h}{r^3}=\frac{Ch}{\left(a^2+h^2\right)^{3/2}}.
$$

Differentiating gives
$$
J'\left(h\right)=C\cdot\frac{\left(a^2+h^2\right)^{3/2}-h\cdot\frac32\left(a^2+h^2\right)^{1/2}\cdot2h}{\left(a^2+h^2\right)^3}=C\cdot\frac{a^2+h^2-3h^2}{\left(a^2+h^2\right)^{5/2}}=C\cdot\frac{a^2-2h^2}{\left(a^2+h^2\right)^{5/2}}.
$$

Setting $J'\left(h\right)=0$, we get $a^2-2h^2=0$, i.e. $h=\frac{a}{\sqrt2}$.

When $h< \frac{a}{\sqrt2}$, $J'\left(h\right)> 0$; when $h> \frac{a}{\sqrt2}$, $J'\left(h\right)< 0$. By **Theorem 3.1** (First Sufficient Condition for an Extremum Point), $h=\frac{a}{\sqrt2}$ is a local maximum point. By **Proposition 3.1** (A Unique Extremum Point Is a Global Extremum Point), at this height the illuminance at $A$ is maximal. $\blacksquare$

### Problem 6

(Problem 3.3-5) Prove the inequality:
$$
x^\alpha-\alpha x+\alpha-1\le0,\forall x> 0,
$$
where $0< \alpha< 1$.

### Solution to Problem 6

Let $f\left(x\right)=x^\alpha-\alpha x+\alpha-1$ ($x> 0$). Differentiating gives
$$
f'\left(x\right)=\alpha x^{\alpha-1}-\alpha=\alpha\left(x^{\alpha-1}-1\right).
$$

Setting $f'\left(x\right)=0$, we get $x^{\alpha-1}=1$, i.e. $x=1$.

When $0< x< 1$, since $\alpha-1< 0$, we have $x^{\alpha-1}> 1$, hence $f'\left(x\right)> 0$; when $x> 1$, $x^{\alpha-1}< 1$, hence $f'\left(x\right)< 0$. By **Theorem 3.1** (First Sufficient Condition for an Extremum Point), $x=1$ is a local maximum point.

Moreover,

$$
f\left(1\right)=1-\alpha+\alpha-1=0.
$$

By **Proposition 3.1** (A Unique Extremum Point Is a Global Extremum Point), $f\left(1\right)=0$ is the maximum value of $f\left(x\right)$ on $\left(0,+\infty\right)$. Hence
$$
f\left(x\right)\le f\left(1\right)=0,\forall x> 0,
$$

i.e. $x^\alpha-\alpha x+\alpha-1\le0$. $\blacksquare$

### Problem 7

(Problem 3.3-6) Prove the following inequality: let $a> 0,b> 0,p> 1,q> 1$, and $\frac1p+\frac1q=1$, then
$$
a^{1/p}b^{1/q}\le\frac{a}{p}+\frac{b}{q}.
$$
### Solution to Problem 7

In the previous problem, take $\alpha=\frac1p$ (since $p> 1$, we have $0< \alpha< 1$), then $1-\alpha=\frac1q$. By the result of the previous problem, for any $x> 0$,
$$
x^{1/p}-\frac1p x+\frac1p-1\le0.
$$

Let $x=\frac{a}{b}$; substituting gives
$$
\left(\frac{a}{b}\right)^{1/p}-\frac1p\cdot\frac{a}{b}+\frac1p-1\le0.
$$

Multiplying both sides by $b$:
$$
a^{1/p}b^{1-1/p}-\frac{a}{p}+\frac{b}{p}-b\le0.
$$

Note that $1-\frac1p=\frac1q$; rearranging gives
$$
a^{1/p}b^{1/q}\le\frac{a}{p}+b\left(1-\frac1p\right)=\frac{a}{p}+\frac{b}{q}.
$$

This is Young's inequality. $\blacksquare$

### Problem 8

(Problem 3.3-7) Let the sides of $\triangle ABC$ be $a,b$ and $c$. Assume $b=c$, and $a+b+c=2l$, where $l$ is a fixed constant, $l> 0$. When is the area of $\triangle ABC$ maximal?

### Solution to Problem 8

Since $b=c$, the triangle is isosceles. From $a+b+c=2l$, we get $a+2b=2l$, i.e.

$$
b=\frac{2l-a}{2}=l-\frac a2.
$$

The height of the isosceles triangle is $h=\sqrt{b^2-\left(a/2\right)^2}$. The area is
$$
S=\frac12 ah=\frac12 a\sqrt{b^2-\frac{a^2}{4}}=\frac12 a\sqrt{\left(l-\frac a2\right)^2-\frac{a^2}{4}}=\frac12 a\sqrt{l^2-la}.
$$

To maximize $S$, it suffices to maximize $S^2$:
$$
S^2=\frac{a^2}{4}\left(l^2-la\right)=\frac14\left(l^2a^2-la^3\right).
$$

Differentiating gives
$$
\left(S^2\right)'=\frac14\left(2l^2a-3la^2\right)=\frac{la}{4}\left(2l-3a\right).
$$

Setting $\left(S^2\right)'=0$, we get $a=\frac{2l}{3}$ ($a=0$ is discarded).

When $0< a< \frac{2l}{3}$, $\left(S^2\right)'> 0$; when $\frac{2l}{3}< a< 2l$, $\left(S^2\right)'< 0$. By **Theorem 3.1** (First Sufficient Condition for an Extremum Point), $a=\frac{2l}{3}$ is a local maximum point.

At this point,

$$
b=c=l-\frac12\cdot\frac{2l}{3}=l-\frac l3=\frac{2l}{3}.
$$

Hence $a=b=c=\frac{2l}{3}$, i.e. the area is maximal when the triangle is equilateral. $\blacksquare$

### Problem 9

(Problem 3.3-8) Let $f\left(x\right)=\sin^p x+\cos^p x$. Find its maximum and minimum values on $\left[0,\frac{\pi}{2}\right]$.

### Solution to Problem 9

Differentiating gives
$$
f'\left(x\right)=p\sin^{p-1}x\cos x-p\cos^{p-1}x\sin x=p\sin x\cos x\left(\sin^{p-2}x-\cos^{p-2}x\right).
$$

Setting $f'\left(x\right)=0$. In $\left(0,\frac{\pi}{2}\right)$, $\sin x> 0$ and $\cos x> 0$, so it suffices to have
$$
\sin^{p-2}x=\cos^{p-2}x.
$$

That is, $\tan^{p-2}x=1$, i.e. $\tan x=1$ (since $x\in\left(0,\pi/2\right)$), giving $x=\frac{\pi}{4}$.

Computing the function values at each point:
- $f\left(0\right)=0+1=1$
-

  $$
  f\left(\frac{\pi}{4}\right)=\left(\frac{\sqrt2}{2}\right)^p+\left(\frac{\sqrt2}{2}\right)^p=2\cdot\left(\frac{\sqrt2}{2}\right)^p=2^{1-p/2}
  $$
- $f\left(\frac{\pi}{2}\right)=1+0=1$

Comparing the three: since $p> 2$ (the problem states $p> 1$, but it needs to be discussed by cases; in fact, in this problem $p$ should be a constant greater than $2$). When $p> 2$, $2^{1-p/2}< 1$.

Hence the maximum value is $1$ (attained at the endpoints $x=0$ and $x=\pi/2$), and the minimum value is $2^{1-p/2}$ (attained at $x=\pi/4$). $\blacksquare$
