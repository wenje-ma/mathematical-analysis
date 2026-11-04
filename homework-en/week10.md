# week10

> **Theorem 2.1 (Chain Rule)**
> 
> If $y=f\left(u\right)$ is differentiable at $u$ and $u=g\left(x\right)$ is differentiable at $x$, then $y=f\left(g\left(x\right)\right)$ is differentiable at $x$ and $\frac{\mathrm dy}{\mathrm dx}=\frac{\mathrm dy}{\mathrm du}\cdot\frac{\mathrm du}{\mathrm dx}=f'\left(g\left(x\right)\right)g'\left(x\right)$.

> **Theorem 8.1 (Intermediate Value Theorem)**
> 
> If $y=f\left(x\right)$ is continuous on $\left[a,b\right]$ and $f\left(a\right)$ and $f\left(b\right)$ have opposite signs, then there exists $c\in\left(a,b\right)$ with $f\left(c\right)=0$. More generally, $f$ takes every value between $f\left(a\right)$ and $f\left(b\right)$.

> **Theorem 8.2 (Boundedness Theorem)**
> 
> A continuous function on a closed interval is bounded and attains its maximum and minimum.

## 1.8-6

Let $f:\left[0,1\right]\to\left[0,1\right]$ be continuous. Prove that it has at least one fixed point in $\left[0,1\right]$, i.e. there exists $x_0\in\left[0,1\right]$ with $f\left(x_0\right)=x_0$.

### Solution to 1.8-6

Let $g\left(x\right)=f\left(x\right)-x$. Then $g\left(0\right)=f\left(0\right)\ge0$ and $g\left(1\right)=f\left(1\right)-1\le0$. By **Theorem 8.1 (Intermediate Value Theorem)**, there exists $x_0\in\left[0,1\right]$ with $g\left(x_0\right)=0$, i.e. $f\left(x_0\right)=x_0$. $\blacksquare$

## 1.8-7

Let $y=f\left(x\right)$ be continuous on $\left[a,b\right]$ with $f\left(a\right)=f\left(b\right)$. Prove that there exist two points $x_1,x_2\in\left[a,b\right]$ such that $\left|x_1-x_2\right|=\frac12\left(b-a\right)$ and $f\left(x_1\right)=f\left(x_2\right)$.

### Solution to 1.8-7

Let $d=\frac{b-a}2$ and consider $g\left(x\right)=f\left(x+d\right)-f\left(x\right)$ for $x\in\left[a,b-d\right]=\left[a,a+d\right]$. Then

$$
g\left(a\right)=f\left(a+d\right)-f\left(a\right),\quad g\left(a+d\right)=f\left(b\right)-f\left(a+d\right)=f\left(a\right)-f\left(a+d\right)=-g\left(a\right).
$$

If $g\left(a\right)=0$, take $x_1=a$, $x_2=a+d$. Otherwise $g\left(a\right)$ and $g\left(a+d\right)$ have opposite signs; by **Theorem 8.1 (Intermediate Value Theorem)**, there exists $\xi\in\left(a,a+d\right)$ with $g\left(\xi\right)=0$, i.e. $f\left(\xi+d\right)=f\left(\xi\right)$. Taking $x_1=\xi$, $x_2=\xi+d$, we have $\left|x_1-x_2\right|=d=\frac{b-a}2$. $\blacksquare$

## 1.8-8

Let $E$ be a bounded infinite set in $\mathbb R$. Prove that there exists $c\in\mathbb R$ such that every punctured neighborhood $\left(c-\delta,c+\delta\right)\backslash\left\{c\right\}$ contains points of $E$.

### Solution to 1.8-8

Since $E$ is bounded, $E\subset\left[a,b\right]$. Split $\left[a,b\right]$ into two closed halves; at least one contains infinitely many points of $E$, call it $\left[a_1,b_1\right]$. Continuing gives a nested sequence $\left\{\left[a_n,b_n\right]\right\}$, each containing infinitely many points of $E$, with

$$
b_n-a_n=\frac{b-a}{2^n}\to0.
$$

By Nested Interval Principle, there exists a unique $c\in\bigcap\left[a_n,b_n\right]$. For any $\delta> 0$, for large $n$, $\left[a_n,b_n\right]\subset\left(c-\delta,c+\delta\right)$ and contains infinitely many points of $E$, so $\left(c-\delta,c+\delta\right)\backslash\left\{c\right\}$ contains points of $E$. $\blacksquare$

## 1.8-9

Let $E$ be a nonempty set in $\mathbb R$ bounded above. Prove that $E$ has a least upper bound, i.e. there exists $M_0$ which is an upper bound of $E$ and satisfies $M_0\le M$ for every upper bound $M$ of $E$.

### Solution to 1.8-9

Let $E\subset\left[a,b\right]$ where $b$ is an upper bound. Split $\left[a,b\right]$ into two halves. If the right half contains an upper bound, take it; otherwise take the left half (its right endpoint is then a new upper bound). Continuing gives a nested sequence $\left\{\left[a_n,b_n\right]\right\}$ where each $b_n$ is an upper bound and each $a_n$ is not.

By Nested Interval Principle, there exists a unique $M_0\in\bigcap\left[a_n,b_n\right]$. Since $b_n\to M_0$ and each $b_n$ is an upper bound, for any $x\in E$, $x\le b_n$; letting $n\to\infty$ gives $x\le M_0$, so $M_0$ is an upper bound. If $M$ is any upper bound, then $M\ge a_n$ for all $n$ (since $a_n$ is not an upper bound, there is $x\in E$ with $x> a_n$, and $M\ge x$), so $M\ge M_0$. $\blacksquare$

## 1.8-11

Let $y=f\left(x\right)$ be defined near $a$ with $\lim_{x\to a}f\left(x\right)=0$, and let $y=g\left(x\right)$ be defined near $a$ and bounded. Prove $\lim_{x\to a}f\left(x\right)g\left(x\right)=0$.

### Solution to 1.8-11

Let $\left|g\left(x\right)\right|\le M$. Given $\varepsilon> 0$, since $f\left(x\right)\to0$, there exists $\delta> 0$ such that $0< \left|x-a\right|< \delta$ implies $\left|f\left(x\right)\right|< \varepsilon/M$. Then

$$
\left|f\left(x\right)g\left(x\right)\right|\le M\left|f\left(x\right)\right|< \varepsilon.
$$

Hence $\lim f\left(x\right)g\left(x\right)=0$. $\blacksquare$

## 2.2-2

Let $f\left(x\right)=1+x^2$. Find $f'\left(\sin x\right)$ and $\left[f\left(\sin x\right)\right]'$.

### Solution to 2.2-2

$f'\left(x\right)=2x$, so $f'\left(\sin x\right)=2\sin x$.

By **Theorem 2.1 (Chain Rule)**,

$$
\left[f\left(\sin x\right)\right]'=f'\left(\sin x\right)\cdot\left(\sin x\right)'=2\sin x\cos x=\sin2x.
$$

$\blacksquare$

## 2.2-3-2

Differentiate: $y=\sqrt{1+x^2}$.

### Solution to 2.2-3-2

$$
y'=\frac1{2\sqrt{1+x^2}}\cdot\left(1+x^2\right)'=\frac{2x}{2\sqrt{1+x^2}}=\frac{x}{\sqrt{1+x^2}}.
$$

$\blacksquare$

## 2.2-3-4

Differentiate: $y=\frac12\sqrt{a^2-x^2}$.

### Solution to 2.2-3-4

$$
y'=\frac12\cdot\frac1{2\sqrt{a^2-x^2}}\cdot\left(-2x\right)=-\frac{x}{2\sqrt{a^2-x^2}}.
$$

$\blacksquare$

## 2.2-3-6

Differentiate: $y=\frac12\left(e^x-e^{-x}\right)$.

### Solution to 2.2-3-6

$$
y'=\frac12\left(e^x-\left(-e^{-x}\right)\right)=\frac12\left(e^x+e^{-x}\right).
$$

$\blacksquare$

## 2.2-3-8

Differentiate: $y=\sqrt{x^3+x+1}$.

### Solution to 2.2-3-8

$$
y'=\frac1{2\sqrt{x^3+x+1}}\cdot\left(3x^2+1\right)=\frac{3x^2+1}{2\sqrt{x^3+x+1}}.
$$

$\blacksquare$

## 2.2-3-10

Differentiate: $y=e^x+e^{x^2}+\cos x^2$.

### Solution to 2.2-3-10

$$
y'=e^x+e^{x^2}\cdot2x-\sin x^2\cdot2x=e^x+2xe^{x^2}-2x\sin x^2.
$$

$\blacksquare$

## 2.2-3-12

Differentiate: $y=\arctan x^2$.

### Solution to 2.2-3-12

$$
y'=\frac1{1+\left(x^2\right)^2}\cdot2x=\frac{2x}{1+x^4}.
$$

$\blacksquare$
