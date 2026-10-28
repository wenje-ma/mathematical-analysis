# week15

> **Proposition 3.1 (Unique Extremum is Global)**<br>If $f$ is continuous on $\left(a,b\right)$ (or $\left[a,b\right]$) and $x_0$ is the only extremum point, then it is the global maximum (if a local max) or global minimum (if a local min).

> **Theorem 3.1 (First Sufficient Condition for Extrema)**<br>If $f$ is differentiable on $\left(a,b\right)$ with $f'\left(x_0\right)=0$, and $f'> 0$ on $\left(x_0-r,x_0\right)$ while $f'< 0$ on $\left(x_0,x_0+r\right)$, then $f\left(x_0\right)$ is a local maximum; if the signs are reversed, it is a local minimum.

> **Theorem 3.2 (Second Sufficient Condition for Extrema)**<br>If $f'\left(x_0\right)=0$ and $f''\left(x_0\right)$ exists, then $f''\left(x_0\right)> 0$ implies $x_0$ is a local minimum, and $f''\left(x_0\right)< 0$ implies $x_0$ is a local maximum.

---

## 3.3-1-1

Find the stationary points of $y=x\left(3x^2-5\right)^2$ and classify them.

### Solution 3.3-1-1

Differentiating,

$$
y'=5\left(3x^2-5\right)\left(3x^2-1\right).
$$

Setting $y'=0$ gives $x=\pm\sqrt{\frac53}$, $\pm\frac1{\sqrt3}$. The second derivative is

$$
y''=30x\left(30x^2-26\right).
$$

At $x=\sqrt{\frac53}$ and $x=-\frac1{\sqrt3}$, $y''> 0$ (local minima); at $x=-\sqrt{\frac53}$ and $x=\frac1{\sqrt3}$, $y''< 0$ (local maxima). By **Theorem 3.2 (Second Sufficient Condition for Extrema)**, the classification holds. $\blacksquare$

---

## 3.3-1-3

Find the stationary points of $y=x\ln x$ ($x> 0$) and classify them.

### Solution 3.3-1-3

$y'=\ln x+1=0$ gives $x=\frac1e$. Since $y''=\frac1x> 0$, by **Theorem 3.2 (Second Sufficient Condition for Extrema)**, $x=\frac1e$ is a local minimum with value $-\frac1e$. $\blacksquare$

---

## 3.3-2

Let $f$ be continuous on $\left[a,b\right]$ with a unique extremum point in $\left(a,b\right)$. Prove: (1) it is a strict local max or min; (2) if it is a local max, it is the global maximum; if a local min, the global minimum.

### Solution 3.3-2

(1) Let $x_0$ be the unique extremum. If it is not a strict local maximum, then there are points arbitrarily close with $f\left(x\right)\ge f\left(x_0\right)$, which would force $f$ to be locally constant, yielding infinitely many extrema, contradicting uniqueness. Hence $x_0$ is strict.

(2) Suppose $x_0$ is a local maximum. If $f\left(x_0\right)$ is not the global maximum, there exists $x_1$ with $f\left(x_1\right)> f\left(x_0\right)$. On $\left[x_0,x_1\right]$, since $f\left(x_1\right)> f\left(x_0\right)$ and $x_0$ is a strict local max, the minimum is attained at an interior point, giving a local minimum, contradicting uniqueness. Hence $f\left(x_0\right)$ is the global maximum. This is **Proposition 3.1 (Unique Extremum is Global)**. $\blacksquare$

---

## 3.3-3

(Snell's Law) Light travels from medium I to medium II with speeds $v_1$ and $v_2$. Snell's law states $\frac{\sin\alpha}{\sin\beta}=\frac{v_1}{v_2}$. Prove that the actual path minimizes travel time.

### Solution 3.3-3

Let the interface be the $x$-axis, $A=\left(0,a\right)$, $B=\left(d,-b\right)$, and the entry point be $P=\left(x,0\right)$. Total time:

$$
T\left(x\right)=\frac{\sqrt{x^2+a^2}}{v_1}+\frac{\sqrt{\left(d-x\right)^2+b^2}}{v_2}.
$$

Differentiating,

$$
T'\left(x\right)=\frac{\sin\alpha}{v_1}-\frac{\sin\beta}{v_2}.
$$

Setting $T'\left(x\right)=0$ gives $\frac{\sin\alpha}{\sin\beta}=\frac{v_1}{v_2}$, i.e. Snell's law. Since $T''\left(x\right)> 0$, this is a minimum. By **Proposition 3.1 (Unique Extremum is Global)**, it is the global minimum time. $\blacksquare$

---

## 3.3-4

A lamp moves along a vertical line $OB$, and $OA$ is a horizontal segment of length $a$. At what height above $O$ is the illumination at $A$ maximized?

### Solution 3.3-4

Let the height be $h$. Illumination is proportional to $\cos\theta/r^2$ where $r=\sqrt{a^2+h^2}$ and $\cos\theta=h/r$. Thus

$$
J\left(h\right)=\frac{Ch}{\left(a^2+h^2\right)^{3/2}}.
$$

Differentiating,

$$
J'\left(h\right)=C\cdot\frac{a^2-2h^2}{\left(a^2+h^2\right)^{5/2}}.
$$

Setting $J'\left(h\right)=0$ gives $h=\frac{a}{\sqrt2}$. By **Theorem 3.1 (First Sufficient Condition for Extrema)**, this is a maximum. By **Proposition 3.1 (Unique Extremum is Global)**, it is the global maximum. $\blacksquare$

---

## 3.3-5

Prove $x^\alpha-\alpha x+\alpha-1\le0$ for all $x> 0$, where $0< \alpha< 1$.

### Solution 3.3-5

Let $f\left(x\right)=x^\alpha-\alpha x+\alpha-1$. Then $f'\left(x\right)=\alpha\left(x^{\alpha-1}-1\right)=0$ gives $x=1$. For $0< x< 1$, $f'> 0$; for $x> 1$, $f'< 0$. By **Theorem 3.1 (First Sufficient Condition for Extrema)**, $x=1$ is a maximum. Since $f\left(1\right)=0$, by **Proposition 3.1 (Unique Extremum is Global)**, $f\left(x\right)\le0$. $\blacksquare$

---

## 3.3-6

Prove: if $a,b> 0$, $p,q> 1$, and $\frac1p+\frac1q=1$, then $a^{1/p}b^{1/q}\le\frac{a}{p}+\frac{b}{q}$.

### Solution 3.3-6

Taking $\alpha=\frac1p$ in 3.3-5 and substituting $x=\frac{a}{b}$, multiplying by $b$, and simplifying using $1-\frac1p=\frac1q$, we obtain

$$
a^{1/p}b^{1/q}\le\frac{a}{p}+\frac{b}{q}.
$$

This is Young's inequality. $\blacksquare$

---

## 3.3-7

Let $\triangle ABC$ have sides $a,b,c$ with $b=c$ and perimeter $a+b+c=2l$. When is the area maximized?

### Solution 3.3-7

Since $b=c$, the triangle is isosceles with $b=l-\frac a2$. The area is

$$
S=\frac12 a\sqrt{l^2-la}.
$$

Maximizing $S^2=\frac14\left(l^2a^2-la^3\right)$, the derivative $\left(S^2\right)'=\frac{la}{4}\left(2l-3a\right)=0$ gives $a=\frac{2l}{3}$. By **Theorem 3.1 (First Sufficient Condition for Extrema)**, this is a maximum. Then $b=c=\frac{2l}{3}$, so the area is maximized when the triangle is equilateral. $\blacksquare$

---

## 3.3-8

Let $f\left(x\right)=\sin^p x+\cos^p x$. Find its maximum and minimum on $\left[0,\frac\pi2\right]$.

### Solution 3.3-8

Differentiating,

$$
f'\left(x\right)=p\sin x\cos x\left(\sin^{p-2}x-\cos^{p-2}x\right).
$$

The critical point in $\left(0,\frac\pi2\right)$ is $x=\frac\pi4$. The values are $f\left(0\right)=1$, $f\left(\frac\pi4\right)=2^{1-p/2}$, $f\left(\frac\pi2\right)=1$. For $p> 2$, the maximum is $1$ (at endpoints) and the minimum is $2^{1-p/2}$ (at $x=\frac\pi4$). $\blacksquare$
