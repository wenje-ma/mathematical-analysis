# week11

> **Basic Knowledge: Definition of Higher-Order Derivatives**<br>If $f'\left(x\right)$ is differentiable at $x_0$, its derivative is the second derivative, denoted $f''\left(x_0\right)$ or $\frac{\mathrm d^2f}{\mathrm dx^2}$. In general, $f^{\left(n\right)}\left(x\right)$ is obtained by differentiating $f^{\left(n-1\right)}\left(x\right)$.

> **Basic Knowledge: Leibniz Formula**<br>$\left(uv\right)^{\left(n\right)}=\sum_{k=0}^n\binom nk u^{\left(k\right)}v^{\left(n-k\right)}$.

---

## 2.4-1

Find the $n$-th derivative of:

(1) $y=x^2e^x$;

(4) $y=x\ln\left(1+x\right)$.

### Solution 2.4-1

By **Basic Knowledge: Definition of Higher-Order Derivatives**, the $n$-th derivative is obtained by differentiating the $(n-1)$-th.

(1) By **Basic Knowledge: Leibniz Formula**, with $u=x^2$, $v=e^x$:

$$
u'=2x,\quad u''=2,\quad u^{\left(k\right)}=0\quad\left(k\ge3\right).
$$

Thus

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
y^{\left(n\right)}=\left(-1\right)^n\frac{\left(n-2\right)!}{\left(1+x\right)^{n-1}}\cdot\frac{x}{1+x}\quad\left(n\ge2\right).
$$

$\blacksquare$

---

## 2.4-4

Let

$$
y=\begin{cases}e^{-1/x^2},&x\ne0,\\0,&x=0.\end{cases}
$$

Prove that both the first and second derivatives at $0$ are $0$.

### Solution 2.4-4

First derivative:

$$
f'\left(0\right)=\lim_{x\to0}\frac{e^{-1/x^2}-0}{x}=\lim_{t\to\infty}\frac{t}{e^{t^2}}=0\quad\left(\text{with }t=1/x,\text{ exponential grows faster than powers}\right).
$$

Second derivative: for $x\ne0$, $f'\left(x\right)=\frac2{x^3}e^{-1/x^2}$. Thus

$$
f''\left(0\right)=\lim_{x\to0}\frac{f'\left(x\right)-0}{x}=\lim_{x\to0}\frac{2e^{-1/x^2}}{x^4}=\lim_{t\to\infty}\frac{2t^4}{e^{t^2}}=0.
$$

$\blacksquare$

---

## 2.4-6

Let $y=\frac{ax+b}{cx+d}$ with $ad-bc=1$. Prove:

(1) $y'=\frac1{\left(cx+d\right)^2}$;

(2) $y^{\left(n\right)}=\left(-1\right)^{n+1}\cdot\frac{n!\,c^{n-1}}{\left(cx+d\right)^{n+1}}$.

### Solution 2.4-6

(1)

$$
y'=\frac{a\left(cx+d\right)-c\left(ax+b\right)}{\left(cx+d\right)^2}=\frac{ad-bc}{\left(cx+d\right)^2}=\frac1{\left(cx+d\right)^2}.
$$

(2) Induction on $n$. The base $n=1$ is (1). Assume $y^{\left(n\right)}=\left(-1\right)^{n+1}\frac{n!c^{n-1}}{\left(cx+d\right)^{n+1}}$. Then

$$
y^{\left(n+1\right)}=\left(-1\right)^{n+1}n!c^{n-1}\cdot\left(-\left(n+1\right)\right)c\cdot\left(cx+d\right)^{-\left(n+2\right)}=\left(-1\right)^{n+2}\frac{\left(n+1\right)!c^n}{\left(cx+d\right)^{n+2}}.
$$

The induction is complete. $\blacksquare$

---

## 2.4-7

Let $f_{ij}\left(x\right)$ ($i,j=1,2$) be infinitely differentiable on $\left(a,b\right)$. Set

$$
W\left(x\right)=\begin{vmatrix}f_{11}\left(x\right)&f_{12}\left(x\right)\\f_{21}\left(x\right)&f_{22}\left(x\right)\end{vmatrix}.
$$

Prove

$$
W'\left(x\right)=\begin{vmatrix}f'_{11}&f'_{12}\\f_{21}&f_{22}\end{vmatrix}+\begin{vmatrix}f_{11}&f_{12}\\f'_{21}&f'_{22}\end{vmatrix},
$$

and give a formula for $W^{\left(n\right)}\left(x\right)$.

### Solution 2.4-7

$W=f_{11}f_{22}-f_{12}f_{21}$. Differentiating,

$$
W'=f'_{11}f_{22}+f_{11}f'_{22}-f'_{12}f_{21}-f_{12}f'_{21}=\begin{vmatrix}f'_{11}&f'_{12}\\f_{21}&f_{22}\end{vmatrix}+\begin{vmatrix}f_{11}&f_{12}\\f'_{21}&f'_{22}\end{vmatrix}.
$$

In general, by **Basic Knowledge: Leibniz Formula**,

$$
W^{\left(n\right)}\left(x\right)=\sum_{k=0}^n\binom nk\begin{vmatrix}f_{11}^{\left(k\right)}&f_{12}^{\left(n-k\right)}\\f_{21}&f_{22}\end{vmatrix}+\sum_{k=0}^n\binom nk\begin{vmatrix}f_{11}&f_{12}\\f_{21}^{\left(k\right)}&f_{22}^{\left(n-k\right)}\end{vmatrix}.
$$

Or more compactly,

$$
W^{\left(n\right)}=\sum_{k=0}^n\binom nk\begin{vmatrix}f_{11}^{\left(k\right)}&f_{12}^{\left(k\right)}\\f_{21}^{\left(n-k\right)}&f_{22}^{\left(n-k\right)}\end{vmatrix}.
$$

$\blacksquare$
