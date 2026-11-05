# week12

> **Theorem 5.1 (Parametric Differentiation Formula)**
> 
> If $x=\varphi\left(t\right)$, $y=\psi\left(t\right)$ are differentiable at $t_0$ with $\varphi'\left(t_0\right)\ne0$, then $\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{\psi'\left(t\right)}{\varphi'\left(t\right)}$.

## 2.4-4

Let

$$
y=\begin{cases}e^{-1/x^2},&x\ne0,\\0,&x=0.\end{cases}
$$

Prove that both the first and second derivatives at $0$ are $0$.

### Solution to 2.4-4

First derivative:

$$
f'\left(0\right)=\lim_{x\to0}\frac{e^{-1/x^2}-0}{x}=\lim_{t\to\infty}\frac{t}{e^{t^2}}=0\quad\left(\text{with~}t=1/x,\text{~exponential~grows~faster~than~powers}\right).
$$

Second derivative: for $x\ne0$, $f'\left(x\right)=\frac2{x^3}e^{-1/x^2}$. Thus

$$
f''\left(0\right)=\lim_{x\to0}\frac{f'\left(x\right)-0}{x}=\lim_{x\to0}\frac{2e^{-1/x^2}}{x^4}=\lim_{t\to\infty}\frac{2t^4}{e^{t^2}}=0.
$$

$\blacksquare$

## 2.4-6

Let $y=\frac{ax+b}{cx+d}$ with $ad-bc=1$. Prove:

(1) $y'=\frac1{\left(cx+d\right)^2}$;

(2) $y^{\left(n\right)}=\left(-1\right)^{n+1}\cdot\frac{n!\,c^{n-1}}{\left(cx+d\right)^{n+1}}$.

### Solution to 2.4-6

(1)

$$
y'=\frac{a\left(cx+d\right)-c\left(ax+b\right)}{\left(cx+d\right)^2}=\frac{ad-bc}{\left(cx+d\right)^2}=\frac1{\left(cx+d\right)^2}.
$$

(2) Induction on $n$. The base $n=1$ is (1). Assume $y^{\left(n\right)}=\left(-1\right)^{n+1}\frac{n!c^{n-1}}{\left(cx+d\right)^{n+1}}$. Then

$$
y^{\left(n+1\right)}=\left(-1\right)^{n+1}n!c^{n-1}\cdot\left(-\left(n+1\right)\right)c\cdot\left(cx+d\right)^{-\left(n+2\right)}=\left(-1\right)^{n+2}\frac{\left(n+1\right)!c^n}{\left(cx+d\right)^{n+2}}.
$$

The induction is complete. $\blacksquare$

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

### Solution to 2.4-7

$W=f_{11}f_{22}-f_{12}f_{21}$. Differentiating,

$$
W'=f'_{11}f_{22}+f_{11}f'_{22}-f'_{12}f_{21}-f_{12}f'_{21}=\begin{vmatrix}f'_{11}&f'_{12}\\f_{21}&f_{22}\end{vmatrix}+\begin{vmatrix}f_{11}&f_{12}\\f'_{21}&f'_{22}\end{vmatrix}.
$$

In general, by Leibniz Formula,

$$
W^{\left(n\right)}\left(x\right)=\sum_{k=0}^n\binom{n}k\begin{vmatrix}f_{11}^{\left(k\right)}&f_{12}^{\left(n-k\right)}\\f_{21}&f_{22}\end{vmatrix}+\sum_{k=0}^n\binom{n}k\begin{vmatrix}f_{11}&f_{12}\\f_{21}^{\left(k\right)}&f_{22}^{\left(n-k\right)}\end{vmatrix}.
$$

Or more compactly,

$$
W^{\left(n\right)}=\sum_{k=0}^n\binom{n}k\begin{vmatrix}f_{11}^{\left(k\right)}&f_{12}^{\left(k\right)}\\f_{21}^{\left(n-k\right)}&f_{22}^{\left(n-k\right)}\end{vmatrix}.
$$

$\blacksquare$

## 2.5-1-2

Find $\frac{\mathrm{d}y}{\mathrm{d}x}$ for: $\begin{cases}x=t\ln{t},\\y=e^t.\end{cases}$

### Solution to 2.5-1-2

$\frac{\mathrm{d}x}{\mathrm{d}t}=\ln{t}+1$, $\frac{\mathrm{d}y}{\mathrm{d}t}=e^t$. By **Theorem 5.1 (Parametric Differentiation Formula)**,

$$
\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{e^t}{\ln{t}+1}.
$$

$\blacksquare$

## 2.5-1-4

Find $\frac{\mathrm{d}y}{\mathrm{d}x}$ for: $\begin{cases}x=\cos^4t,\\y=\sin^4t.\end{cases}$

### Solution to 2.5-1-4

$\frac{\mathrm{d}x}{\mathrm{d}t}=-4\cos^3t\sin{t}$, $\frac{\mathrm{d}y}{\mathrm{d}t}=4\sin^3t\cos{t}$. By **Theorem 5.1 (Parametric Differentiation Formula)**,

$$
\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{4\sin^3t\cos{t}}{-4\cos^3t\sin{t}}=-\tan^2t.
$$

$\blacksquare$

## 2.5-3

The curve is given by $\begin{cases}x=1-t^2,\\y=t-t^2.\end{cases}$ Find the tangent lines at $t=1$ and $t=\frac{\sqrt2}2$.

### Solution to 2.5-3

$\frac{\mathrm{d}x}{\mathrm{d}t}=-2t$, $\frac{\mathrm{d}y}{\mathrm{d}t}=1-2t$, $\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{1-2t}{-2t}=\frac{2t-1}{2t}$.

At $t=1$: $x=0$, $y=0$, slope $k=\frac{2-1}{2}=\frac12$. Tangent: $y=\frac12x$.

At $t=\frac{\sqrt2}2$: $x=1-\frac12=\frac12$, $y=\frac{\sqrt2}2-\frac12=\frac{\sqrt2-1}2$, slope $k=\frac{\sqrt2-1}{\sqrt2}=1-\frac{\sqrt2}2$. Tangent:

$$
y-\frac{\sqrt2-1}2=\left(1-\frac{\sqrt2}2\right)\left(x-\frac12\right).
$$

$\blacksquare$

## 2.5-4

Let $x=\varphi\left(t\right)$, $y=\psi\left(t\right)$ be differentiable at $t_0$ with $\varphi'\left(t_0\right)\ne0$. For $\Delta{t}\ne0$, set

$$
\Delta{x}=\varphi\left(t_0+\Delta{t}\right)-\varphi\left(t_0\right),\quad\Delta{y}=\psi\left(t_0+\Delta{t}\right)-\psi\left(t_0\right).
$$

Prove $\lim_{\Delta{t}\to0}\frac{\Delta{y}}{\Delta{x}}=\frac{\psi'\left(t_0\right)}{\varphi'\left(t_0\right)}$.

### Solution to 2.5-4

$$
\frac{\Delta{y}}{\Delta{x}}=\frac{\psi\left(t_0+\Delta{t}\right)-\psi\left(t_0\right)}{\varphi\left(t_0+\Delta{t}\right)-\varphi\left(t_0\right)}=\frac{\frac{\psi\left(t_0+\Delta{t}\right)-\psi\left(t_0\right)}{\Delta{t}}}{\frac{\varphi\left(t_0+\Delta{t}\right)-\varphi\left(t_0\right)}{\Delta{t}}}.
$$

As $\Delta{t}\to0$, the numerator tends to $\psi'\left(t_0\right)$ and the denominator to $\varphi'\left(t_0\right)\ne0$. By arithmetic of limits,

$$
\lim_{\Delta{t}\to0}\frac{\Delta{y}}{\Delta{x}}=\frac{\psi'\left(t_0\right)}{\varphi'\left(t_0\right)}.
$$

$\blacksquare$
