# Assignment 7

> **Definition** (Continuous Function) Suppose $y=f\left(x\right)$ is defined on $\left(a,b\right)$. If at a point $x_0\in\left(a,b\right)$ one has $\lim\limits_{x\to x_0}f\left(x\right)=f\left(x_0\right)$, then $y=f\left(x\right)$ is said to be continuous at the point $x_0$. If $y=f\left(x\right)$ is continuous at every point of $\left(a,b\right)$, it is said to be continuous on $\left(a,b\right)$.

> **Theorem 7.2** (Continuity of Composite Functions) If $y=g\left(y\right)$ is continuous at the point $y_0$, $y=f\left(x\right)$ is continuous at the point $x_0$ and $f\left(x_0\right)=y_0$, then the composite function $y=g\left(f\left(x\right)\right)$ is continuous at the point $x_0$.

> **Definition** (Elementary Functions) Elementary functions are continuous on their domains.

### Problem 1

(Problem 1.7-1) Point out the discontinuities of the following functions and their types:
(1) $y=\operatorname{sgn}\left(\sin x\right)$;

(2)

$$
y=f\left(x\right)=\begin{cases}x^2e^x,&x>0,\\sin\frac{\pi}{1+x^2},&x<0,\1,&x=0;\end{cases}
$$

(3) $y=\cos\left\{\left(x-\left[x\right]\right)\pi\right\}$;

(4)

$$
y=f\left(x\right)=\begin{cases}e^{\sin\frac1x},&x\ne0,\0,&x=0.\end{cases}
$$

### Solution to Problem 1

(1) When $x=k\pi$ ($k\in\mathbb Z$), $\sin x=0$, and the left and right limits of $\operatorname{sgn}\left(\sin x\right)$ are $1$ and $-1$ (or vice versa), so it is a discontinuity of the first kind (jump discontinuity). It is continuous at all other points.

(2) As $x\to0+0$, $f\left(x\right)=x^2e^x\to0$; as $x\to0-0$,

$$
f\left(x\right)=\sin\frac{\pi}{1+x^2}\to\sin\pi=0.
$$

But $f\left(0\right)=1$, so $x=0$ is a removable discontinuity (first kind).

(3) $x-\left[x\right]=\left\{x\right\}$ is the fractional part; at integer points the left and right limits are $\cos0=1$ and $\cos\pi=-1$, so integer points are jump discontinuities (first kind). It is continuous at all other points.

(4) As $x\to0$, $\frac1x$ oscillates, $\sin\frac1x$ oscillates within $\left[-1,1\right]$, and $e^{\sin\left(1/x\right)}$ oscillates between $e^{-1}$ and $e$; the limit does not exist, so $x=0$ is a discontinuity of the second kind (oscillating discontinuity). $\blacksquare$

### Problem 2

(Problem 1.7-2-2) Using the $\epsilon$-$\delta$ language, prove that if $y=f\left(x\right)$ is continuous at the point $a$, then $y=\left|f\left(x\right)\right|$ is continuous at the point $a$.

### Solution to Problem 2

By **Definition** (Continuous Function), given any $\epsilon>0$, there exists $\delta>0$ such that $\left|f\left(x\right)-f\left(a\right)\right|<\epsilon$ when $\left|x-a\right|<\delta$. By **Proposition 1.7** (Triangle Inequality) in Chapter 1,

$$
\left|\left|f\left(x\right)\right|-\left|f\left(a\right)\right|\right|\le\left|f\left(x\right)-f\left(a\right)\right|<\epsilon.
$$

Hence $\left|f\left(x\right)\right|$ is continuous at the point $a$. $\blacksquare$

### Problem 3

(Problem 1.7-3) Using the continuity of elementary functions, find the following limits:
(1) $\lim\limits_{x\to0}\cos\left(\sqrt{1+x^2}-1\right)$;

(2) $\lim\limits_{x\to0}e^{\frac{\sin x}{\sin2x}}$;

(3) $\lim\limits_{x\to\infty}\arctan\frac{\sqrt{x^4+2}}{1+x^2}$;

(4) $\lim\limits_{x\to5}x^{\sqrt x}$;

(5) $\lim\limits_{x\to\infty}\left(1+\frac1x+\frac1{x^2}\right)^{x+\sqrt x}$.

### Solution to Problem 3

(1) By **Theorem 7.2** (Continuity of Composite Functions), $\lim\limits_{x\to0}\left(\sqrt{1+x^2}-1\right)=0$, so the original expression $=\cos0=1$.

(2) $\frac{\sin x}{\sin2x}\to\frac12$; by the continuity of $e^u$, the original expression $=e^{1/2}=\sqrt e$.

(3) $\frac{\sqrt{x^4+2}}{1+x^2}\to1$; by the continuity of $\arctan u$, the original expression $=\arctan1=\frac\pi4$.

(4) $x^{\sqrt x}=e^{\sqrt x\ln x}$, and $\sqrt x\ln x\to\sqrt5\ln5$; by continuity, the original expression $=e^{\sqrt5\ln5}=5^{\sqrt5}$.

(5)

$$
\left(1+\frac1x+\frac1{x^2}\right)^{x+\sqrt x}=\left[\left(1+\frac{x+1}{x^2}\right)^{\frac{x^2}{x+1}}\right]^{\frac{\left(x+\sqrt x\right)\left(x+1\right)}{x^2}}.
$$

The base tends to $e$ and the exponent tends to $1$, so the original expression $=e$. $\blacksquare$

### Problem 4

(Problem 1.7-4) Let $y=f\left(x\right)$ be continuous on $\left(a,b\right)$. Let $x=g\left(t\right)$ have a limit as $t\to\infty$, and suppose the limit lies in $\left(a,b\right)$. Prove that

$$
\lim\limits_{t\to\infty}f\left(g\left(t\right)\right)=f\left(\lim\limits_{t\to\infty}g\left(t\right)\right).
$$

### Solution to Problem 4

Let $\lim\limits_{t\to\infty}g\left(t\right)=c\in\left(a,b\right)$. By **Definition** (Continuous Function), given any $\epsilon>0$, there exists $\delta>0$ such that $\left|f\left(x\right)-f\left(c\right)\right|<\epsilon$ when $\left|x-c\right|<\delta$. Moreover, since $g\left(t\right)\to c$, there exists $T>0$ such that $\left|g\left(t\right)-c\right|<\delta$ when $t>T$. Hence when $t>T$, $\left|f\left(g\left(t\right)\right)-f\left(c\right)\right|<\epsilon$. That is, $\lim f\left(g\left(t\right)\right)=f\left(c\right)$. $\blacksquare$

### Problem 5

(Problem 1.7-5) Let $y=f\left(x\right)$ and $y=g\left(x\right)$ be defined and continuous on the real field $\mathbb R$. Suppose $f\left(x\right)=g\left(x\right),\forall x\in\mathbb Q$. Prove that $f\left(x\right)\equiv g\left(x\right),\forall x\in\mathbb R$.

### Solution to Problem 5

Take any $x_0\in\mathbb R$. By the density of the rationals, there exists a rational sequence $\left\{r_n\right\}$ such that $r_n\to x_0$. Since $f,g$ are continuous,

$$
f\left(x_0\right)=\lim_{n\to\infty}f\left(r_n\right)=\lim_{n\to\infty}g\left(r_n\right)=g\left(x_0\right).
$$

Hence $f\left(x_0\right)=g\left(x_0\right)$. By the arbitrariness of $x_0$, $f\equiv g$. $\blacksquare$

### Problem 6

(Problem 1.7-6) Let $t_1$ and $t_2$ be any two real numbers. Without using the formula $e^{t_1+t_2}=e^{t_1}\cdot e^{t_2}$, prove the following limit identity:

$$
\lim\limits_{x\to\infty}\left[\left(1+\frac{t_1}{x}\right)\left(1+\frac{t_2}{x}\right)\right]^x=e^{t_1+t_2}.
$$

### Solution to Problem 6

$$
\left[\left(1+\frac{t_1}{x}\right)\left(1+\frac{t_2}{x}\right)\right]^x=\left(1+\frac{t_1+t_2+t_1t_2/x}{x}\right)^x=\left[\left(1+\frac{t_1+t_2+o\left(1\right)}{x}\right)^{\frac{x}{t_1+t_2+o\left(1\right)}}\right]^{t_1+t_2+o\left(1\right)}.
$$

The base tends to $e$ and the exponent tends to $t_1+t_2$. By the continuity of the exponential function, the limit is $e^{t_1+t_2}$. $\blacksquare$
