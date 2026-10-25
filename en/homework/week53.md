# Assignment 53

> **Proposition** (Fourier Coefficients) The Fourier series of an integrable function $f\left(x\right)$ with period $2\pi$ is
> $$
> f\left(x\right)\sim\frac{a_0}{2}+\displaystyle\sum_{n=1}^\infty\left(a_n\cos nx+b_n\sin nx\right),
> $$
> where

$$
a_n=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\cos nx\,\mathrm{d}x\left(n=0,1,2,\cdots\right), b_n=\frac1\pi\int_{-\pi}^\pi f\left(x\right)\sin nx\,\mathrm{d}x\left(n=1,2,\cdots\right).
$$

### Problem 1

(Problem 13.2-1-1) Let $y=f\left(x\right)$ be a function with period $2\pi$, and on $\left[-\pi,\pi\right]$ let $f\left(x\right)=x^2$. Find the Fourier series of $f\left(x\right)$.

### Solution to Problem 1

$f\left(x\right)=x^2$ is an even function, so $b_n=0$. By **Proposition** (Fourier Coefficients),

$$
a_0=\frac1\pi\int_{-\pi}^\pi x^2\,\mathrm{d}x=\frac{2}{\pi}\cdot\frac{\pi^3}{3}=\frac{2\pi^2}{3},
$$

$$
a_n=\frac1\pi\int_{-\pi}^\pi x^2\cos nx\,\mathrm{d}x=\frac{2}{\pi}\int_0^\pi x^2\cos nx\,\mathrm{d}x.
$$

Integrating by parts:

$$
\displaystyle\int_0^\pi x^2\cos nx\,\mathrm{d}x=\left[\frac{x^2\sin nx}{n}\right]_0^\pi-\frac{2}{n}\int_0^\pi x\sin nx\,\mathrm{d}x,
$$
and

$$
\displaystyle\int_0^\pi x\sin nx\,\mathrm{d}x=-\frac{\pi\cos n\pi}{n}=\frac{\pi\left(-1\right)^{n+1}}{n}.
$$

Hence

$$
a_n=\frac{2}{\pi}\cdot\left(-\frac{2}{n}\right)\cdot\frac{\pi\left(-1\right)^{n+1}}{n}=\frac{4\left(-1\right)^n}{n^2}.
$$

Therefore

$$
x^2\sim\frac{\pi^2}{3}+4\sum_{n=1}^\infty\frac{\left(-1\right)^n}{n^2}\cos nx.

$$

$\blacksquare$
### Problem 2

(Problem 13.2-1-3) Let $y=f\left(x\right)$ be a function with period $2\pi$, and on $\left[-\pi,\pi\right]$ let $f\left(x\right)=\sin^4 x$. Find the Fourier series of $f\left(x\right)$.

### Solution to Problem 2

Using a trigonometric identity:

$$
\sin^4 x=\left(\sin^2 x\right)^2=\left(\frac{1-\cos2x}{2}\right)^2=\frac{1-2\cos2x+\cos^2 2x}{4}=\frac{3}{8}-\frac12\cos2x+\frac18\cos4x.
$$

This is already a trigonometric polynomial, so by **Proposition** (Fourier Coefficients) we read off its Fourier coefficients directly: $a_0=\frac{3\pi}{2}$ (i.e. the constant term $\frac{a_0}{2}=\frac38$), $a_2=-\frac12$, $a_4=\frac18$, and all other $a_n=b_n=0$. Hence

$$
\sin^4 x=\frac38-\frac12\cos2x+\frac18\cos4x.

$$

$\blacksquare$
### Problem 3

(Problem 13.2-1-5) Let $y=f\left(x\right)$ be a function with period $2\pi$, and on $\left[-\pi,\pi\right]$ let

$$
f\left(x\right)=\begin{cases}0,&-\pi\le x< 0;\x,&0\le x\le\pi.\end{cases}
$$

Find the Fourier series of $f\left(x\right)$.

### Solution to Problem 3

By **Proposition** (Fourier Coefficients),

$$
a_0=\frac1\pi\int_0^\pi x\,\mathrm{d}x=\frac{\pi}{2},
$$

$$
a_n=\frac1\pi\int_0^\pi x\cos nx\,\mathrm{d}x=\frac1\pi\left(\left[\frac{x\sin nx}{n}\right]_0^\pi-\frac1n\int_0^\pi\sin nx\,\mathrm{d}x\right)=\frac{\left(-1\right)^n-1}{n^2\pi},
$$

i.e. $a_n=0$ when $n$ is even, and $a_n=-\frac{2}{n^2\pi}$ when $n$ is odd. Moreover,

$$
b_n=\frac1\pi\int_0^\pi x\sin nx\,\mathrm{d}x=\frac1\pi\left(\left[-\frac{x\cos nx}{n}\right]_0^\pi+\frac1n\int_0^\pi\cos nx\,\mathrm{d}x\right)=\frac{\left(-1\right)^{n+1}}{n}.
$$

Hence

$$
f\left(x\right)\sim\frac{\pi}{4}-\frac{2}{\pi}\sum_{k=0}^\infty\frac{\cos\left(2k+1\right)x}{\left(2k+1\right)^2}+\sum_{n=1}^\infty\frac{\left(-1\right)^{n+1}}{n}\sin nx.

$$

$\blacksquare$
### Problem 4

(Problem 13.2-7) Let $y=f\left(x\right)$ satisfy the following condition on $\left[-\pi,\pi\right]$:
(i) $f\left(x+\pi\right)=f\left(x\right)$,

or (ii) $f\left(x+\pi\right)=-f\left(x\right)$.
Prove that under condition (i),

$$
a_{2n-1}=b_{2n-1}=0\left(n=1,2,\cdots\right),
$$
while under condition (ii),

$$
a_{2n}=b_{2n}=0\left(n=1,2,\cdots\right).
$$

### Solution to Problem 4

Split the coefficient integrals into the two segments $\left[-\pi,0\right]$ and $\left[0,\pi\right]$. In the first segment make the substitution $x=t-\pi$. Then

$$
\int_{-\pi}^0 f\left(x\right)\cos nx\,\mathrm{d}x=\int_0^\pi f\left(t-\pi\right)\cos\left(n\left(t-\pi\right)\right)\,\mathrm{d}t=\cos n\pi\int_0^\pi f\left(t-\pi\right)\cos nt\,\mathrm{d}t,
$$

using

$$
\cos\left(n\left(t-\pi\right)\right)=\left(-1\right)^n\cos nt\ \left(\sin n\pi=0\right).
$$

The same substitution applies to $\sin nx$.

**Condition (i)** $f\left(t-\pi\right)=f\left(t\right)$:

$$
a_n=\frac1\pi\left[\left(-1\right)^n+1\right]\int_0^\pi f\left(t\right)\cos nt\,\mathrm{d}t, b_n=\frac1\pi\left[\left(-1\right)^n+1\right]\int_0^\pi f\left(t\right)\sin nt\,\mathrm{d}t.
$$

When $n$ is odd, $\left(-1\right)^n+1=0$, so $a_n=b_n=0$, i.e. $a_{2n-1}=b_{2n-1}=0$.

**Condition (ii)** $f\left(t-\pi\right)=-f\left(t\right)$:

$$
a_n=\frac1\pi\left[1-\left(-1\right)^n\right]\int_0^\pi f\left(t\right)\cos nt\,\mathrm{d}t, b_n=\frac1\pi\left[1-\left(-1\right)^n\right]\int_0^\pi f\left(t\right)\sin nt\,\mathrm{d}t.
$$

When $n$ is even, $1-\left(-1\right)^n=0$, so $a_n=b_n=0$, i.e. $a_{2n}=b_{2n}=0$. $\blacksquare$
