# Assignment 55

> **Theorem 4.1** (Bessel's Inequality) Let $f\left(x\right)$ be Riemann integrable on $\left[-\pi,\pi\right]$, with Fourier coefficients $a_n,b_n$. Then
> $$
> \frac{a_0^2}{2}+\displaystyle\sum_{n=1}^\infty\left(a_n^2+b_n^2\right)\le\frac1\pi\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x,
> $$
> in particular, both $\displaystyle\sum_{n=1}^\infty a_n^2$ and $\displaystyle\sum_{n=1}^\infty b_n^2$ converge.

> **Theorem 4.2** (The Closure Equation / Parseval Identity) Let $f\left(x\right)$ be Riemann integrable and square-integrable on $\left[-\pi,\pi\right]$. Then
> $$
> \frac1\pi\displaystyle\int_{-\pi}^\pi f^2\left(x\right)\,\mathrm{d}x=\frac{a_0^2}{2}+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right).
> $$

### Problem 1

(Problem 13.4-1) Let $f\left(x\right)$ be Riemann integrable on $\left[-\pi,\pi\right]$, and let

$$
f\left(x\right)\sim\frac{a_0}{2}+\displaystyle\sum_{n=1}^\infty\left(a_n\cos nx+b_n\sin nx\right).
$$

Prove that $\displaystyle\sum_{n=1}^\infty\frac{a_n}{n}$ and $\displaystyle\sum_{n=1}^\infty\frac{b_n}{n}$ converge.

### Solution to Problem 1

By **Theorem 4.1** (Bessel's Inequality), $\displaystyle\sum_{n=1}^\infty\left(a_n^2+b_n^2\right)< \infty$. Also $\displaystyle\sum_{n=1}^\infty\frac1{n^2}< \infty$. By the Cauchy–Schwarz inequality,

$$
\sum_{n=1}^\infty\left|\frac{a_n}{n}\right|\le\left(\sum_{n=1}^\infty a_n^2\right)^{1/2}\left(\sum_{n=1}^\infty\frac1{n^2}\right)^{1/2}< \infty,
$$

so $\sum\frac{a_n}{n}$ converges absolutely. Similarly, $\sum\frac{b_n}{n}$ converges absolutely. $\blacksquare$

### Problem 2

(Problem 13.4-2) Show that the series

$$
\frac{a_0}{2}+\displaystyle\sum_{n=1}^\infty\frac{1}{\ln n\cdot\ln\ln n}\cos nx
$$

converges everywhere, but is not the Fourier series of any function integrable on $\left[-\pi,\pi\right]$.

### Solution to Problem 2

**Convergence**: write $a_n=\frac{1}{\ln n\cdot\ln\ln n}$. The sequence $\left\{a_n\right\}$ decreases monotonically to $0$. For any fixed $x\not\equiv0\pmod{2\pi}$, the partial sums

$$
\sum_{n=1}^N\cos nx=\frac{\sin\left(Nx/2\right)\cos\left(\left(N+1\right)x/2\right)}{\sin\left(x/2\right)}
$$

are bounded in $N$. By Dirichlet's Test, the series converges everywhere.

**Not a Fourier series**: By Problem 13.4-1, the Fourier series of any function integrable on $\left[-\pi,\pi\right]$ must have $\displaystyle\sum_{n=1}^\infty\frac{a_n}{n}$ convergent. But here

$$
\sum_{n=1}^\infty\frac{a_n}{n}=\sum_{n=1}^\infty\frac{1}{n\ln n\cdot\ln\ln n}.
$$

By the integral test,

$$
\int_3^{+\infty}\frac{\mathrm{d}x}{x\ln x\cdot\ln\ln x}
=\ln\ln\ln x\Big|_3^{+\infty}=+\infty,
$$

so $\displaystyle\sum_{n=1}^\infty\frac{a_n}{n}$ diverges, failing the necessary condition for Fourier coefficients of an integrable function. Hence the series is not the Fourier series of any function integrable on $\left[-\pi,\pi\right]$. $\blacksquare$

### Problem 3

(Problem 13.4-5) Using the Parseval identity for the Fourier series of $f\left(x\right)=x^2$ ($\left| x\right|\le\pi$), sum $\displaystyle\sum_{n=1}^\infty\frac1{n^4}$.

### Solution to Problem 3

By Problem 13.2-1-1,

$$
x^2\sim\frac{\pi^2}{3}+4\displaystyle\sum_{n=1}^\infty\frac{\left(-1\right)^n}{n^2}\cos nx,
$$

i.e. $a_0=\frac{2\pi^2}{3}$, $a_n=\frac{4\left(-1\right)^n}{n^2}$, $b_n=0$.

By **Theorem 4.2** (The Closure Equation / Parseval Identity),

$$
\frac1\pi\int_{-\pi}^\pi x^4\,\mathrm{d}x=\frac{a_0^2}{2}+\sum_{n=1}^\infty a_n^2.
$$

The left side is $=\frac{1}{\pi}\cdot\frac{2\pi^5}{5}=\frac{2\pi^4}{5}$; the right side

$$
=\frac12\left(\frac{2\pi^2}{3}\right)^2+\displaystyle\sum_{n=1}^\infty\frac{16}{n^4}=\frac{2\pi^4}{9}+16\sum\frac1{n^4}.
$$

Hence

$$
16\sum_{n=1}^\infty\frac1{n^4}=2\pi^4\left(\frac15-\frac19\right)=\frac{8\pi^4}{45},\sum_{n=1}^\infty\frac1{n^4}=\frac{\pi^4}{90}.

$$

$\blacksquare$
### Problem 4

(Problem 13.4-7) Using the Parseval identity for the Fourier series of the function

$$
f\left(x\right)=\begin{cases}x,&x\in\left[0,\pi\right];\-x,&x\in\left[-\pi,0\right)\end{cases}\ \left(\text{即}f\left(x\right)=\left| x\right|\right)
$$

sum $\displaystyle\sum_{n=1}^\infty\frac{1}{\left(2n-1\right)^4}$.

### Solution to Problem 4

$f\left(x\right)=\left| x\right|$ is an even function, so $b_n=0$. Computing the Fourier coefficients:

$$
a_0=\frac1\pi\int_{-\pi}^\pi\left| x\right|\,\mathrm{d}x=\frac{2}{\pi}\int_0^\pi x\,\mathrm{d}x=\pi,
$$

$$
a_n=\frac{2}{\pi}\int_0^\pi x\cos nx\,\mathrm{d}x=\frac{2}{\pi}\cdot\frac{\cos n\pi-1}{n^2}=\frac{2\left(\left(-1\right)^n-1\right)}{\pi n^2}.
$$

i.e. $a_n=0$ when $n$ is even, and $a_n=-\frac{4}{\pi n^2}$ when $n$ is odd.

By **Theorem 4.2** (The Closure Equation / Parseval Identity),

$$
\frac1\pi\int_{-\pi}^\pi x^2\,\mathrm{d}x=\frac{a_0^2}{2}+\sum_{n=1}^\infty a_n^2.
$$

The left side is $=\frac{2\pi^2}{3}$; the right side

$$
=\frac{\pi^2}{2}+\displaystyle\sum_{n\text{ 奇}}\frac{16}{\pi^2 n^4}=\frac{\pi^2}{2}+\frac{16}{\pi^2}\sum_{n=1}^\infty\frac{1}{\left(2n-1\right)^4}.
$$

Hence

$$
\frac{16}{\pi^2}\sum_{n=1}^\infty\frac{1}{\left(2n-1\right)^4}=\frac{2\pi^2}{3}-\frac{\pi^2}{2}=\frac{\pi^2}{6},
$$

and solving gives

$$
\sum_{n=1}^\infty\frac{1}{\left(2n-1\right)^4}=\frac{\pi^4}{96}.

$$

$\blacksquare$