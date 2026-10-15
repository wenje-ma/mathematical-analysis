# Assignment 54

> **Theorem 3.1** (Dirichlet's Convergence Theorem) Let $f\left(x\right)$ have period $2\pi$ and be piecewise monotone and bounded on $\left[-\pi,\pi\right]$. Then its Fourier series converges at every point $x$ to $\frac{f\left(x+0\right)+f\left(x-0\right)}{2}$; at points where $f$ is continuous it converges to $f\left(x\right)$, and at discontinuities it converges to the average of the left and right limits.

> **Proposition** (Fourier Coefficients) The Fourier coefficients of an integrable function $f\left(x\right)$ with period $2\pi$ are
> $$
\begin{aligned}
> a_n&=\frac1\pi\displaystyle\int_{-\pi}^\pi f\left(x\right)\cos nx\,\mathrm{d}x,\
> b_n&=\frac1\pi\displaystyle\int_{-\pi}^\pi f\left(x\right)\sin nx\,\mathrm{d}x.
\end{aligned}
> $$

> **Theorem** (The Closure Equation) Let the Fourier coefficients of $f\left(x\right)$ be $a_n,b_n$. Then
> $$
> \frac1\pi\displaystyle\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x=\frac{a_0^2}{2}+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right).
> $$

### Problem 1

(Problem 13.3-1) Let $f\left(x\right)$ be a function with period $2\pi$, and on $\left(-\pi,\pi\right]$ let

$$
f\left(x\right)=\begin{cases}0,&x\in\left(-\pi,0\right];\1,&x\in\left(0,\pi\right].\end{cases}
$$
Prove that when $0<x<\pi$,

$$
\displaystyle1=\frac12+\frac2\pi\sum_{n=0}^\infty\frac{\sin\left(2n+1\right)x}{2n+1},
$$

and hence deduce that $\displaystyle\frac\pi4=\sum_{n=0}^\infty\frac{\left(-1\right)^n}{2n+1}$.

### Solution to Problem 1

By **Proposition** (Fourier Coefficients), $a_0=\frac1\pi\displaystyle\int_0^\pi1\,\mathrm{d}x=1$, $a_n=\frac1\pi\displaystyle\int_0^\pi\cos nx\,\mathrm{d}x=0$ ($n\ge1$), and

$$
b_n=\frac1\pi\int_0^\pi\sin nx\,\mathrm{d}x=\frac{1-\left(-1\right)^n}{n\pi}.
$$

Hence $b_n=0$ when $n$ is even, and $b_n=\frac{2}{n\pi}$ when $n$ is odd. Therefore

$$
f\left(x\right)\sim\frac12+\frac2\pi\sum_{n=0}^\infty\frac{\sin\left(2n+1\right)x}{2n+1}.
$$

When $0<x<\pi$, $f$ is continuous and $f\left(x\right)=1$. By **Theorem 3.1** (Dirichlet's Convergence Theorem),

$$
1=\frac12+\frac2\pi\sum_{n=0}^\infty\frac{\sin\left(2n+1\right)x}{2n+1}.
$$

Taking $x=\frac\pi2$, we have $\sin\frac{\left(2n+1\right)\pi}{2}=\left(-1\right)^n$, giving

$$
1=\frac12+\frac2\pi\sum_{n=0}^\infty\frac{\left(-1\right)^n}{2n+1},\text{即}\;\frac\pi4=\sum_{n=0}^\infty\frac{\left(-1\right)^n}{2n+1}.

$$

$\blacksquare$
### Problem 2

(Problem 13.3-3) Let $f\left(x\right)$ be a function with period $2\pi$, and on $\left[-\pi,\pi\right]$ let $f\left(x\right)=\left(\pi-\left| x\right|\right)^2$. Find the Fourier series of this function, and use it to find the values of $\displaystyle\sum_{n=1}^\infty\frac1{n^2}$ and $\displaystyle\sum_{n=1}^\infty\frac1{n^4}$.

### Solution to Problem 2

$f\left(x\right)=\left(\pi-\left| x\right|\right)^2$ is an even function, so $b_n=0$. By **Proposition** (Fourier Coefficients),

$$
a_0=\frac{2}{\pi}\int_0^\pi\left(\pi-x\right)^2\,\mathrm{d}x=\frac{2\pi^2}{3},
$$

$$
a_n=\frac{2}{\pi}\int_0^\pi\left(\pi-x\right)^2\cos nx\,\mathrm{d}x.
$$

Let $u=\pi-x$. Then

$$
\cos nx=\cos\left(n\pi-nu\right)=\left(-1\right)^n\cos nu,
$$

and therefore

$$
a_n=\frac{2\left(-1\right)^n}{\pi}\int_0^\pi u^2\cos nu\,\mathrm{d}u=\frac{2\left(-1\right)^n}{\pi}\cdot\frac{2\pi\left(-1\right)^n}{n^2}=\frac{4}{n^2}.
$$

Hence
$$
f\left(x\right)\sim\frac{\pi^2}{3}+4\displaystyle\sum_{n=1}^\infty\frac{\cos nx}{n^2}.
$$

At $x=0$, $f$ is continuous. By **Theorem 3.1** (Dirichlet's Convergence Theorem),

$$
f\left(0\right)=\pi^2=\frac{\pi^2}{3}+4\displaystyle\sum_{n=1}^\infty\frac1{n^2},
$$

and solving gives

$$
\displaystyle\sum_{n=1}^\infty\frac1{n^2}=\frac{\pi^2}{6}.
$$

Then by **Theorem** (The Closure Equation),

$$
\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x=\frac{a_0^2}{2}+\sum_{n=1}^\infty a_n^2.
$$

The left side

$$
=\frac{2}{\pi}\displaystyle\int_0^\pi\left(\pi-x\right)^4\,\mathrm{d}x=\frac{2\pi^4}{5};
$$
the right side

$$
=\frac12\left(\frac{2\pi^2}{3}\right)^2+\displaystyle\sum_{n=1}^\infty\frac{16}{n^4}=\frac{2\pi^4}{9}+16\sum\frac1{n^4}.
$$

Hence

$$
16\sum_{n=1}^\infty\frac1{n^4}=2\pi^4\left(\frac15-\frac19\right)=\frac{8\pi^4}{45},\sum_{n=1}^\infty\frac1{n^4}=\frac{\pi^4}{90}.

$$

$\blacksquare$
### Problem 3

(Problem 13.3-4) Using the Fourier series of $f\left(x\right)=x^2$ ($\left| x\right|\le\pi$), find $\displaystyle\sum_{n=1}^\infty\frac{\left(-1\right)^{n+1}}{n^2}$ and $\displaystyle\sum_{n=1}^\infty\frac1{n^2}$.

### Solution to Problem 3

By the **Proposition** (Fourier Coefficients) of Chapter 13, $f\left(x\right)=x^2$ is an even function, and its Fourier series is (see Problem 13.2-1-1)

$$
x^2\sim\frac{\pi^2}{3}+4\sum_{n=1}^\infty\frac{\left(-1\right)^n}{n^2}\cos nx.
$$

By **Theorem 3.1** (Dirichlet's Convergence Theorem), equality holds at points of continuity.

Taking $x=\pi$:

$$
\pi^2=\frac{\pi^2}{3}+4\displaystyle\sum_{n=1}^\infty\frac{\left(-1\right)^n}{n^2}\cdot\left(-1\right)^n=\frac{\pi^2}{3}+4\sum\frac1{n^2},
$$

and solving gives

$$
\sum_{n=1}^\infty\frac1{n^2}=\frac{\pi^2}{6}.
$$

Taking $x=0$: $0=\frac{\pi^2}{3}+4\displaystyle\sum_{n=1}^\infty\frac{\left(-1\right)^n}{n^2}$, solving gives $\displaystyle\sum_{n=1}^\infty\frac{\left(-1\right)^n}{n^2}=-\frac{\pi^2}{12}$, i.e.

$$
\sum_{n=1}^\infty\frac{\left(-1\right)^{n+1}}{n^2}=\frac{\pi^2}{12}.

$$

$\blacksquare$