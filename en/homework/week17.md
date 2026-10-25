# Assignment 17

> **Definition** (Convex Function) Let $y=f\left(x\right)$ be defined on $\left(a,b\right)$. If for any two points $x_1$ and $x_2$ ($x_1< x_2$) in $\left(a,b\right)$, we have
> $$
> f\left(tx_1+\left(1-t\right)x_2\right)\le tf\left(x_1\right)+\left(1-t\right)f\left(x_2\right),
> $$
> where $t$ is any number in $\left(0,1\right)$, then the function $y=f\left(x\right)$ is said to be convex on $\left(a,b\right)$. Conversely, if the above inequality holds in the opposite direction, then $y=f\left(x\right)$ is said to be concave on $\left(a,b\right)$.

> **Theorem 5.1** (Second-Derivative Criterion for Convexity) Let $y=f\left(x\right)$ be twice differentiable on $\left(a,b\right)$. Then $y=f\left(x\right)$ is convex on $\left(a,b\right)$ if and only if $f''\left(x\right)\ge0$ ($\forall x\in\left(a,b\right)$); $y=f\left(x\right)$ is concave on $\left(a,b\right)$ if and only if $f''\left(x\right)\le0$ ($\forall x\in\left(a,b\right)$).

### Problem 1

(Problem 3.5-1-1) Find the intervals of convexity and concavity and the inflection points of the function $y=xe^x$.

### Solution to Problem 1

Differentiating gives
$$
y'=e^x+xe^x=\left(1+x\right)e^x, y''=e^x+\left(1+x\right)e^x=\left(2+x\right)e^x.
$$

Setting $y''=0$, we get $x=-2$. Since $e^x> 0$ always holds, the sign of $y''$ is determined by $2+x$.

When $x< -2$, $y''< 0$ and the function is concave; when $x> -2$, $y''> 0$ and the function is convex.

The inflection point is $\left(-2,-2e^{-2}\right)$.

By **Theorem 5.1** (Second-Derivative Criterion for Convexity), $y=xe^x$ is concave on $\left(-\infty,-2\right]$ and convex on $\left[-2,+\infty\right)$. $\blacksquare$

### Problem 2

(Problem 3.5-1-4) Find the intervals of convexity and concavity and the inflection points of the function $y=x\ln x$.

### Solution to Problem 2

The domain is $\left(0,+\infty\right)$. Differentiating gives
$$
y'=\ln x+1, y''=\frac1x> 0\left(x> 0\right).
$$

By **Theorem 5.1** (Second-Derivative Criterion for Convexity), $y=x\ln x$ is convex on $\left(0,+\infty\right)$, with no inflection points. $\blacksquare$

### Problem 3

(Problem 3.5-2) Use the concept of convex functions to prove the following inequalities:
(1) Let $a> 0,b> 0$, prove

$$
2\arctan\frac{a+b}{2}\ge\arctan a+\arctan b;
$$

(2) If $a,b,c$ are all positive, prove $a^{\alpha}b^{\beta}c^{\gamma}\le\alpha a+\beta b+\gamma c$, where $\alpha+\beta+\gamma=1$, $\alpha,\beta,\gamma> 0$.

### Solution to Problem 3

(1) Let $f\left(x\right)=\arctan x$. Then
$$
f'\left(x\right)=\frac{1}{1+x^2}, f''\left(x\right)=\frac{-2x}{\left(1+x^2\right)^2}.
$$

When $x> 0$, $f''\left(x\right)< 0$, so $f\left(x\right)=\arctan x$ is concave on $\left(0,+\infty\right)$. By the definition of a concave function, for any $a,b> 0$ and $t\in\left(0,1\right)$,
$$
f\left(ta+\left(1-t\right)b\right)\ge tf\left(a\right)+\left(1-t\right)f\left(b\right).
$$

Taking $t=\frac12$, we get
$$
f\left(\frac{a+b}{2}\right)\ge\frac{f\left(a\right)+f\left(b\right)}{2},
$$

i.e.
$$
2\arctan\frac{a+b}{2}\ge\arctan a+\arctan b.
$$

(2) By Problem 2, $y=x\ln x$ is convex on $\left(0,+\infty\right)$. By the definition of a convex function, for any $a,b,c> 0$ and $\alpha+\beta+\gamma=1$,
$$
\alpha a\ln a+\beta b\ln b+\gamma c\ln c\ge\left(\alpha a+\beta b+\gamma c\right)\ln\left(\alpha a+\beta b+\gamma c\right).
$$

No, this is not the correct application. Corrected: the convex function $f\left(x\right)=x\ln x$ satisfies
$$
f\left(\alpha\cdot\frac{a}{\alpha}+\beta\cdot\frac{b}{\beta}+\gamma\cdot\frac{c}{\gamma}\right)\le\alpha f\left(\frac{a}{\alpha}\right)+\beta f\left(\frac{b}{\beta}\right)+\gamma f\left(\frac{c}{\gamma}\right).
$$

That is,
$$
\left(a+b+c\right)\ln\left(a+b+c\right)\le a\ln\frac{a}{\alpha}+b\ln\frac{b}{\beta}+c\ln\frac{c}{\gamma}.
$$

This is also not what the problem asks for. The correct approach is: since $f\left(x\right)=\ln x$ is concave,
$$
\alpha\ln a+\beta\ln b+\gamma\ln c\le\ln\left(\alpha a+\beta b+\gamma c\right).
$$

That is,
$$
a^\alpha b^\beta c^\gamma\le\alpha a+\beta b+\gamma c.
$$

This is the weighted AM-GM inequality. $\blacksquare$

### Problem 4

(Problem 3.5-3) Let $f\left(x\right)$ and $g\left(x\right)$ both be convex functions on $\left(a,b\right)$. Set

$$
F\left(x\right)=\max\left\{f\left(x\right),g\left(x\right)\right\},
$$

then $F\left(x\right)$ is also convex.

### Solution to Problem 4

For any $x_1,x_2\in\left(a,b\right)$ and $t\in\left(0,1\right)$, we need to prove
$$
F\left(tx_1+\left(1-t\right)x_2\right)\le tF\left(x_1\right)+\left(1-t\right)F\left(x_2\right).
$$

By the definition of $F$,
$$
F\left(tx_1+\left(1-t\right)x_2\right)=\max\left\{f\left(tx_1+\left(1-t\right)x_2\right),g\left(tx_1+\left(1-t\right)x_2\right)\right\}.
$$

Since $f,g$ are both convex,
$$
f\left(tx_1+\left(1-t\right)x_2\right)\le tf\left(x_1\right)+\left(1-t\right)f\left(x_2\right)\le tF\left(x_1\right)+\left(1-t\right)F\left(x_2\right),
$$
$$
g\left(tx_1+\left(1-t\right)x_2\right)\le tg\left(x_1\right)+\left(1-t\right)g\left(x_2\right)\le tF\left(x_1\right)+\left(1-t\right)F\left(x_2\right).
$$

The right-hand sides of the two inequalities are the same, hence

$$
\max\left\{f\left(\cdot\right),g\left(\cdot\right)\right\}\le tF\left(x_1\right)+\left(1-t\right)F\left(x_2\right),
$$

i.e.
$$
F\left(tx_1+\left(1-t\right)x_2\right)\le tF\left(x_1\right)+\left(1-t\right)F\left(x_2\right).
$$

Hence $F\left(x\right)$ is convex. $\blacksquare$

### Problem 5

(Problem 3.5-5) Let $f\left(u\right)$ be a convex function on $\left(-\infty,+\infty\right)$ and also an increasing function. Let $g\left(x\right)$ be a convex function on the interval $\left(a,b\right)$. Prove that the composite function $f\left(g\left(x\right)\right)$ is convex.

### Solution to Problem 5

For any $x_1,x_2\in\left(a,b\right)$ and $t\in\left(0,1\right)$, we need to prove
$$
f\left(g\left(tx_1+\left(1-t\right)x_2\right)\right)\le t f\left(g\left(x_1\right)\right)+\left(1-t\right)f\left(g\left(x_2\right)\right).
$$

Since $g\left(x\right)$ is convex,
$$
g\left(tx_1+\left(1-t\right)x_2\right)\le t g\left(x_1\right)+\left(1-t\right)g\left(x_2\right).
$$

Since $f\left(u\right)$ is increasing,
$$
f\left(g\left(tx_1+\left(1-t\right)x_2\right)\right)\le f\left(t g\left(x_1\right)+\left(1-t\right)g\left(x_2\right)\right).
$$

Since $f\left(u\right)$ is convex,
$$
f\left(t g\left(x_1\right)+\left(1-t\right)g\left(x_2\right)\right)\le t f\left(g\left(x_1\right)\right)+\left(1-t\right)f\left(g\left(x_2\right)\right).
$$

Combining, we obtain
$$
f\left(g\left(tx_1+\left(1-t\right)x_2\right)\right)\le t f\left(g\left(x_1\right)\right)+\left(1-t\right)f\left(g\left(x_2\right)\right).
$$

Hence $f\left(g\left(x\right)\right)$ is convex. $\blacksquare$

### Problem 6

(Problem 3.5-6) Let $f\left(x\right)$ be a differentiable convex function on $\left(-\infty,+\infty\right)$ and bounded. Prove that $f\left(x\right)$ is constant.

### Solution to Problem 6

Since $f\left(x\right)$ is convex, by **Theorem 5.1** (Second-Derivative Criterion for Convexity), $f''\left(x\right)\ge0$, so $f'\left(x\right)$ is increasing.

Proof by contradiction: assume $f'\left(x\right)$ is not identically $0$. Then there exists $x_0$ such that $f'\left(x_0\right)> 0$ or $f'\left(x_0\right)< 0$.

If $f'\left(x_0\right)> 0$, since $f'$ is increasing, when $x> x_0$ we have $f'\left(x\right)\ge f'\left(x_0\right)> 0$. By the Lagrange mean value theorem,
$$
f\left(x\right)=f\left(x_0\right)+f'\left(\xi\right)\left(x-x_0\right)\ge f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)\to+\infty\left(x\to+\infty\right).
$$

This contradicts the boundedness of $f\left(x\right)$.

If $f'\left(x_0\right)< 0$, since $f'$ is increasing, when $x< x_0$ we have $f'\left(x\right)\le f'\left(x_0\right)< 0$. By the Lagrange mean value theorem,
$$
f\left(x_0\right)-f\left(x\right)=f'\left(\xi\right)\left(x_0-x\right)\le f'\left(x_0\right)\left(x_0-x\right)< 0,
$$

i.e.

$$
f\left(x\right)\ge f\left(x_0\right)-f'\left(x_0\right)\left(x-x_0\right)\to+\infty\ \left(x\to-\infty\text{, 因}-f'\left(x_0\right)> 0\right).
$$

This contradicts the boundedness of $f\left(x\right)$.

Hence $f'\left(x\right)\equiv0$, i.e. $f\left(x\right)$ is constant. $\blacksquare$

### Problem 7

(Problem 3.5-7-1) Sketch the graph of the function $y=\frac{\left(x+1\right)^3}{\left(x-1\right)^2}$.

### Solution to Problem 7

**Domain** $\left(-\infty,1\right)\cup\left(1,+\infty\right)$.

**Asymptotes**: $\lim\limits_{x\to1}y=\infty$, so $x=1$ is a vertical asymptote. Moreover,
$$
\lim_{x\to\infty}\frac{y}{x}=\lim_{x\to\infty}\frac{\left(x+1\right)^3}{x\left(x-1\right)^2}=1,
$$
$$
\lim_{x\to\infty}\left(y-x\right)=\lim_{x\to\infty}\frac{\left(x+1\right)^3-x\left(x-1\right)^2}{\left(x-1\right)^2}=\lim_{x\to\infty}\frac{5x^2+x+1}{x^2-2x+1}=5.
$$

Hence the oblique asymptote is $y=x+5$.

**Monotonicity intervals and extrema**: differentiate
$$
y'=\frac{3\left(x+1\right)^2\left(x-1\right)^2-\left(x+1\right)^3\cdot2\left(x-1\right)}{\left(x-1\right)^4}=\frac{\left(x+1\right)^2\left[3\left(x-1\right)-2\left(x+1\right)\right]}{\left(x-1\right)^3}=\frac{\left(x+1\right)^2\left(x-5\right)}{\left(x-1\right)^3}.
$$

Setting $y'=0$, we get $x=-1$ or $x=5$.

When $x< -1$, $y'< 0$ (denominator negative, numerator positive); when $-1< x< 1$, $y'< 0$; when $1< x< 5$, $y'< 0$; when $x> 5$, $y'> 0$.

Hence $x=5$ is a local minimum point, with local minimum $y\left(5\right)=\frac{6^3}{4^2}=\frac{216}{16}=\frac{27}{2}$. $x=-1$ is not an extremum point (the derivative has the same sign on both sides).

**Convexity and inflection points**:
$$
y''=\frac{\left[\left(x+1\right)^2\left(x-5\right)\right]'\left(x-1\right)^3-\left(x+1\right)^2\left(x-5\right)\cdot3\left(x-1\right)^2}{\left(x-1\right)^6}=\frac{2\left(x+1\right)\left(x-1\right)^2-3\left(x+1\right)^2\left(x-5\right)}{\left(x-1\right)^4}=\frac{16\left(x+1\right)}{\left(x-1\right)^4}.
$$

When $x< -1$, $y''< 0$ (concave); when $x> -1$ and $x\ne1$, $y''> 0$ (convex). The inflection point is $\left(-1,0\right)$.

Combining the above information, one can sketch the graph. $\blacksquare$

### Problem 8

(Problem 3.5-7-2) Sketch the graph of the function $y=xe^{-x}$.

### Solution to Problem 8

**Domain** $\left(-\infty,+\infty\right)$.

**Asymptotes**: $\lim\limits_{x\to+\infty}xe^{-x}=0$, so $y=0$ is a horizontal asymptote ($x\to+\infty$).

**Monotonicity intervals and extrema**: differentiate
$$
y'=e^{-x}-xe^{-x}=\left(1-x\right)e^{-x}.
$$

Setting $y'=0$, we get $x=1$. When $x< 1$, $y'> 0$; when $x> 1$, $y'< 0$. Hence $x=1$ is a local maximum point, with local maximum $y\left(1\right)=e^{-1}=\frac1e$.

**Convexity and inflection points**:
$$
y''=-e^{-x}-\left(1-x\right)e^{-x}=\left(x-2\right)e^{-x}.
$$

Setting $y''=0$, we get $x=2$. When $x< 2$, $y''< 0$ (concave); when $x> 2$, $y''> 0$ (convex). The inflection point is $\left(2,2e^{-2}\right)$.

Combining the above information, one can sketch the graph. $\blacksquare$

### Problem 9

(Problem 3.5-7-3) Sketch the graph of the function $y=xe^{-x^2}$.

### Solution to Problem 9

**Domain** $\left(-\infty,+\infty\right)$. The function is odd, and its graph is symmetric about the origin.

**Asymptotes**: $\lim\limits_{x\to\pm\infty}xe^{-x^2}=0$, so $y=0$ is a horizontal asymptote.

**Monotonicity intervals and extrema**: differentiate
$$
y'=e^{-x^2}+x\cdot\left(-2x\right)e^{-x^2}=\left(1-2x^2\right)e^{-x^2}.
$$

Setting $y'=0$, we get

$$
x=\pm\frac{1}{\sqrt2}}.
$$

When $x< -\frac{1}{\sqrt2}$, $y'< 0$; when $-\frac{1}{\sqrt2}< x< \frac{1}{\sqrt2}$, $y'> 0$; when $x> \frac{1}{\sqrt2}$, $y'< 0$.

Hence $x=-\frac{1}{\sqrt2}$ is a local minimum point, with local minimum $-\frac{1}{\sqrt{2e}}$; $x=\frac{1}{\sqrt2}$ is a local maximum point, with local maximum $\frac{1}{\sqrt{2e}}$.

**Convexity and inflection points**:
$$
y''=-4xe^{-x^2}+\left(1-2x^2\right)\left(-2x\right)e^{-x^2}=\left(4x^3-6x\right)e^{-x^2}=2x\left(2x^2-3\right)e^{-x^2}.
$$

Setting $y''=0$, we get $x=0$ or $x=\pm\sqrt{\frac32}$.

When $x< -\sqrt{\frac32}$, $y''< 0$ (concave); when $-\sqrt{\frac32}< x< 0$, $y''> 0$ (convex); when $0< x< \sqrt{\frac32}$, $y''< 0$ (concave); when $x> \sqrt{\frac32}$, $y''> 0$ (convex).

The inflection points are $\left(0,0\right)$ and $\left(\pm\sqrt{\frac32},\pm\sqrt{\frac32}e^{-3/2}\right)$.

Combining the above information, one can sketch the graph. $\blacksquare$
