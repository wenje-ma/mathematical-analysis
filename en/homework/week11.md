# Assignment 11

> **Definition** (Higher-Order Derivative) If the derivative $f'\left(x\right)$ of $y=f\left(x\right)$ is differentiable at $x_0$, then its derivative is called the second derivative of $f$, denoted $f''\left(x_0\right)$ or $\frac{\mathrm d^2f}{\mathrm dx^2}$. In general, the $n$-th derivative $f^{\left(n\right)}\left(x\right)$ is obtained by differentiating the $n-1$-st derivative.

### Problem 1

(Problem 2.4-1) Find the $n$-th derivative of the following functions:
(1) $y=x^2e^x$;

(4) $y=x\ln\left(1+x\right)$.

### Solution to Problem 1

By **Definition** (Higher-Order Derivative), the $n$-th derivative is obtained by differentiating the $n-1$-st derivative. (1) By the Leibniz formula

$$
\left(uv\right)^{\left(n\right)}=\sum_{k=0}^n\binom nk u^{\left(k\right)}v^{\left(n-k\right)},
$$
where $u=x^2$, $v=e^x$.

$$
u'=2x,u''=2,u^{\left(k\right)}=0\left(k\ge3\right).
$$

Hence

$$
y^{\left(n\right)}=x^2e^x+2nx e^x+n\left(n-1\right)e^x=e^x\left[x^2+2nx+n\left(n-1\right)\right].
$$

(4) $y'=\ln\left(1+x\right)+\frac{x}{1+x}$.

$$
y''=\frac1{1+x}+\frac1{\left(1+x\right)^2}=\frac{2+x}{\left(1+x\right)^2}.
$$

In general, for $n\ge2$,

$$
y^{\left(n\right)}=\left(-1\right)^n\frac{\left(n-2\right)!}{\left(1+x\right)^{n-1}}+\left(-1\right)^{n-1}\frac{\left(n-1\right)!}{\left(1+x\right)^n}.
$$

Simplifying,

$$
y^{\left(n\right)}=\left(-1\right)^n\frac{\left(n-2\right)!}{\left(1+x\right)^{n-1}}\cdot\frac{x}{1+x}\left(n\ge2\right).
$$

$\blacksquare$

### Problem 2

(Problem 2.4-4) Consider the function

$$
y=\begin{cases}e^{-1/x^2},&x\ne0,\0,&x=0.\end{cases}
$$

Prove that both its first and second derivatives at the point $0$ are $0$.

### Solution to Problem 2

First derivative:

$$
f'\left(0\right)=\lim\limits_{x\to0}\frac{e^{-1/x^2}-0}{x}=\lim\limits_{t\to\infty}\frac{t}{e^{t^2}}=0\ \left(\text{令}t=1/x\text{, 指数增长快于幂函数}\right).
$$

Second derivative: for $x\ne0$, $f'\left(x\right)=\frac2{x^3}e^{-1/x^2}$. Hence

$$
f''\left(0\right)=\lim\limits_{x\to0}\frac{f'\left(x\right)-0}{x}=\lim\limits_{x\to0}\frac{2e^{-1/x^2}}{x^4}=\lim\limits_{t\to\infty}\frac{2t^4}{e^{t^2}}=0.

$$

$\blacksquare$
### Problem 3

(Problem 2.4-6) Let $y=\frac{ax+b}{cx+d}$, where $ad-bc=1$. Prove that:
(1) $y'=\frac1{\left(cx+d\right)^2}$;

(2) $y^{\left(n\right)}=\left(-1\right)^{n+1}\cdot\frac{n!\,c^{n-1}}{\left(cx+d\right)^{n+1}}$.

### Solution to Problem 3

(1)

$$
y'=\frac{a\left(cx+d\right)-c\left(ax+b\right)}{\left(cx+d\right)^2}=\frac{ad-bc}{\left(cx+d\right)^2}=\frac1{\left(cx+d\right)^2}.
$$

(2) Induction on $n$. For $n=1$ this is (1). Assume $y^{\left(n\right)}=\left(-1\right)^{n+1}\frac{n!c^{n-1}}{\left(cx+d\right)^{n+1}}$. Then

$$
y^{\left(n+1\right)}=\left(-1\right)^{n+1}n!c^{n-1}\cdot\left(-\left(n+1\right)\right)c\cdot\left(cx+d\right)^{-\left(n+2\right)}=\left(-1\right)^{n+2}\frac{\left(n+1\right)!c^n}{\left(cx+d\right)^{n+2}}.
$$

This completes the induction. $\blacksquare$

### Problem 4

(Problem 2.4-7) Let $f_{ij}\left(x\right)\left(i,j=1,2\right)$ be infinitely differentiable on $\left(a,b\right)$. Set

$$
W\left(x\right)=\begin{vmatrix}f_{11}\left(x\right)&f_{12}\left(x\right)\f_{21}\left(x\right)&f_{22}\left(x\right)\end{vmatrix}.
$$
Prove that

$$
W'\left(x\right)=\begin{vmatrix}f'_{11}&f'_{12}\f_{21}&f_{22}\end{vmatrix}+\begin{vmatrix}f_{11}&f_{12}\f'_{21}&f'_{22}\end{vmatrix},
$$

and give a formula for $W^{\left(n\right)}\left(x\right)$.

### Solution to Problem 4

$W=f_{11}f_{22}-f_{12}f_{21}$. Differentiating gives

$$
W'=f'_{11}f_{22}+f_{11}f'_{22}-f'_{12}f_{21}-f_{12}f'_{21}=\begin{vmatrix}f'_{11}&f'_{12}\f_{21}&f_{22}\end{vmatrix}+\begin{vmatrix}f_{11}&f_{12}\f'_{21}&f'_{22}\end{vmatrix}.
$$

In general, by the Leibniz formula,

$$
W^{\left(n\right)}\left(x\right)=\sum_{k=0}^n\binom nk\begin{vmatrix}f_{11}^{\left(k\right)}&f_{12}^{\left(n-k\right)}\f_{21}&f_{22}\end{vmatrix}+\sum_{k=0}^n\binom nk\begin{vmatrix}f_{11}&f_{12}\f_{21}^{\left(k\right)}&f_{22}^{\left(n-k\right)}\end{vmatrix}.
$$

Or more concisely:

$$
W^{\left(n\right)}=\displaystyle\sum_{k=0}^n\binom nk\begin{vmatrix}f_{11}^{\left(k\right)}&f_{12}^{\left(k\right)}\f_{21}^{\left(n-k\right)}&f_{22}^{\left(n-k\right)}\end{vmatrix}.
$$

$\blacksquare$
