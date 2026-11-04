# week14

> **Theorem 1.1 (Fermat's Theorem)**
> 
> If $f\left(x\right)$ is defined near $a$ and differentiable at $a$, and $a$ is an extremum point of $y=f\left(x\right)$, then $f'\left(a\right)=0$.

> **Theorem 1.2 (Rolle's Theorem)**
> 
> If $y=f\left(x\right)$ is continuous on $\left[a,b\right]$, differentiable on $\left(a,b\right)$, and $f\left(a\right)=f\left(b\right)$, then there exists $c\in\left(a,b\right)$ such that $f'\left(c\right)=0$.

> **Theorem 1.3 (Lagrange Mean Value Theorem)**
> 
> If $f$ is continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$, then there exists $c\in\left(a,b\right)$ such that $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

> **Theorem 1.4 (Constant Function Theorem)**
> 
> If $y=f\left(x\right)$ is differentiable on $\left(a,b\right)$ and $f'\left(x\right)=0$ for all $x\in\left(a,b\right)$, then $f$ is constant on $\left(a,b\right)$.

> **Theorem 1.5 (Monotonicity Criterion)**
> 
> If $y=f\left(x\right)$ is continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$, then $f'\left(x\right)> 0$ ($\ge0$) implies strictly increasing (increasing), and $f'\left(x\right)< 0$ ($\le0$) implies strictly decreasing (decreasing).

## 3.1-6

Prove:

(1) $\ln\left(1+x\right)< x$ ($x> 0$);

(2) $\cos x> 1-\frac{x^2}{2}$ ($x\ne0$);

(3) $\sin x< x$ ($x> 0$);

(4) $\tan x> x$ ($0< x< \frac\pi2$).

### Solution to 3.1-6

(1) Let $f\left(x\right)=\ln\left(1+x\right)-x$. $f\left(0\right)=0$, $f'\left(x\right)=-\frac{x}{1+x}< 0$ for $x> 0$. By **Theorem 1.5 (Monotonicity Criterion)**, $f$ is strictly decreasing, so $f\left(x\right)< f\left(0\right)=0$, i.e. $\ln\left(1+x\right)< x$.

(2) Let $f\left(x\right)=\cos x-1+\frac{x^2}{2}$. $f\left(0\right)=0$, $f'\left(x\right)=x-\sin x> 0$ for $x> 0$ (by (3)). By **Theorem 1.5 (Monotonicity Criterion)**, $f$ is strictly increasing, so $f\left(x\right)> 0$, i.e. $\cos x> 1-\frac{x^2}{2}$. By evenness, the result holds for $x< 0$ as well.

(3) Let $f\left(x\right)=x-\sin x$. $f\left(0\right)=0$, $f'\left(x\right)=1-\cos x\ge0$ with equality only at isolated points. By **Theorem 1.5 (Monotonicity Criterion)**, $f$ is strictly increasing, so $f\left(x\right)> 0$, i.e. $\sin x< x$.

(4) Let $f\left(x\right)=\tan x-x$. $f\left(0\right)=0$, $f'\left(x\right)=\tan^2x> 0$ for $0< x< \frac\pi2$. By **Theorem 1.5 (Monotonicity Criterion)**, $f$ is strictly increasing, so $f\left(x\right)> 0$, i.e. $\tan x> x$. $\blacksquare$

## 3.1-8

Let $f$ be continuous near $x_0$ and differentiable on $U\setminus\left\{x_0\right\}$. If $\lim_{x\to x_0}f'\left(x\right)$ exists, prove $f$ is differentiable at $x_0$ and $f'\left(x_0\right)=\lim_{x\to x_0}f'\left(x\right)$.

### Solution to 3.1-8

Let $\lim_{x\to x_0}f'\left(x\right)=A$. For any $x\ne x_0$, apply **Theorem 1.3 (Lagrange Mean Value Theorem)** on the interval between $x_0$ and $x$: there exists $\xi$ between them such that

$$
\frac{f\left(x\right)-f\left(x_0\right)}{x-x_0}=f'\left(\xi\right).
$$

As $x\to x_0$, $\xi\to x_0$, so by assumption,

$$
\lim_{x\to x_0}\frac{f\left(x\right)-f\left(x_0\right)}{x-x_0}=\lim_{\xi\to x_0}f'\left(\xi\right)=A.
$$

Thus $f'\left(x_0\right)=A$. $\blacksquare$

## 3.1-10

Prove Darboux's theorem: if $f$ is differentiable on $\left(a,b\right)$ and $f'\left(x_1\right)> 0$, $f'\left(x_2\right)< 0$ for some $x_1,x_2\in\left(a,b\right)$, then there exists $c$ between them with $f'\left(c\right)=0$.

### Solution to 3.1-10

Assume $x_1< x_2$. From $f'\left(x_1\right)> 0$, there exists $\delta_1> 0$ such that $x\in\left(x_1,x_1+\delta_1\right)$ implies $\frac{f\left(x\right)-f\left(x_1\right)}{x-x_1}> 0$, i.e. $f\left(x\right)> f\left(x_1\right)$. Similarly, $f'\left(x_2\right)< 0$ implies there exists $\delta_2> 0$ such that $x\in\left(x_2-\delta_2,x_2\right)$ implies $f\left(x\right)> f\left(x_2\right)$.

Thus the maximum of $f$ on $\left[x_1,x_2\right]$ is not attained at either endpoint, but at some interior point $c\in\left(x_1,x_2\right)$. Since $f$ is differentiable, by **Theorem 1.1 (Fermat's Theorem)**, $f'\left(c\right)=0$. $\blacksquare$

## 3.1-11

Prove: if $f$ is differentiable on $\left(a,b\right)$ and $f'\left(x\right)\ne0$, then $f$ is either strictly increasing or strictly decreasing.

### Solution to 3.1-11

Suppose not. Then by **Theorem 1.3 (Lagrange Mean Value Theorem)**, $f'$ takes both positive and negative values. By Darboux's theorem (3.1-10), $f'$ must take the value $0$, contradicting $f'\left(x\right)\ne0$. Hence $f$ is strictly increasing or strictly decreasing. $\blacksquare$

## 3.1-13

Prove $e^x> 1+x$ for $x> 0$.

### Solution to 3.1-13

Let $f\left(x\right)=e^x-1-x$. $f\left(0\right)=0$, $f'\left(x\right)=e^x-1> 0$ for $x> 0$. By **Theorem 1.5 (Monotonicity Criterion)**, $f$ is strictly increasing, so $f\left(x\right)> f\left(0\right)=0$, i.e. $e^x> 1+x$. $\blacksquare$
