# Assignment 45

> **Theorem 4.1** (Taylor Series) If a function $f\left(x\right)$ can be expanded as a power series on $\left(x_0-R,x_0+R\right)$
> $$
> f\left(x\right)=\sum_{n=0}^{\infty}a_n\left(x-x_0\right)^n,
> $$
> then its coefficients must be
> $$
> a_n=\frac{f^{\left(n\right)}\left(x_0\right)}{n!},
> $$
> i.e. the power series expansion is unique, and is called the Taylor series of $f$ at $x_0$.
> 
> **Definition** (Basic Expansions) At $x=0$ we have: $e^x=\sum_{n=0}^{\infty}\frac{x^n}{n!}$ ($\left|x\right|< +\infty$);
> $$
> \ln\left(1+x\right)=\sum_{n=1}^{\infty}\frac{\left(-1\right)^{n-1}x^n}{n}\ \left(\left|x\right|< 1\right);
> $$
> $\cos x=\sum_{n=0}^{\infty}\frac{\left(-1\right)^n x^{2n}}{\left(2n\right)!}$ ($\left|x\right|< +\infty$).

### Problem 1

(Problem 11.4-1-3) Find the power series expansion of $f\left(x\right)=e^x$ at $x_0=3$.

### Solution to Problem 1

By **Definition** (Basic Expansions), $e^t=\sum_{n=0}^{\infty}\frac{t^n}{n!}$. Let $t=x-3$. Then

$$
e^x=e^3\cdot e^{x-3}=e^3\sum_{n=0}^{\infty}\frac{\left(x-3\right)^n}{n!}=\sum_{n=0}^{\infty}\frac{e^3}{n!}\left(x-3\right)^n, \left|x-3\right|< +\infty.
$$

By **Theorem 4.1** (Taylor Series), this is the Taylor expansion of $e^x$ at $x_0=3$. $\blacksquare$

### Problem 2

(Problem 11.4-1-4) Find the power series expansion of $f\left(x\right)=\ln x$ at $x_0=2$.

### Solution to Problem 2

Rewrite

$$
\ln x=\ln\left(2+\left(x-2\right)\right)=\ln 2+\ln\left(1+\frac{x-2}{2}\right).
$$

By **Definition** (Basic Expansions),

$$
\ln\left(1+t\right)=\sum_{n=1}^{\infty}\frac{\left(-1\right)^{n-1}t^n}{n}, \left|t\right|< 1.
$$

Let $t=\frac{x-2}{2}$. We get

$$
\ln x=\ln 2+\sum_{n=1}^{\infty}\frac{\left(-1\right)^{n-1}}{n}\left(\frac{x-2}{2}\right)^n=\ln 2+\sum_{n=1}^{\infty}\frac{\left(-1\right)^{n-1}}{n\cdot 2^n}\left(x-2\right)^n,
$$

with the convergence range $\left|\frac{x-2}{2}\right|< 1$, i.e. $0< x< 4$. $\blacksquare$

### Problem 3

(Problem 11.4-1-5) Find the power series expansion of $f\left(x\right)=\cos^2 x$ at $x_0=0$.

### Solution to Problem 3

Using the half-angle formula $\cos^2x=\frac{1+\cos 2x}{2}$. By **Definition** (Basic Expansions),

$$
\cos t=\sum_{n=0}^{\infty}\frac{\left(-1\right)^n t^{2n}}{\left(2n\right)!}, \left|t\right|< +\infty.
$$

Let $t=2x$. We get

$$
\cos^2x=\frac12+\frac12\cos 2x=\frac12+\frac12\sum_{n=0}^{\infty}\frac{\left(-1\right)^n\left(2x\right)^{2n}}{\left(2n\right)!}
=\frac12+\sum_{n=0}^{\infty}\frac{\left(-1\right)^n 2^{2n-1}}{\left(2n\right)!}x^{2n},
$$

with the convergence range $\left|x\right|< +\infty$. $\blacksquare$

### Problem 4

(Problem 11.4-2) Prove that
$$
\sum_{n=0}^{\infty}\frac{x^n}{\left(n+1\right)!}=\frac{1}{x}\left(e^x-1\right), x\ne 0,
$$
and deduce that $\sum_{n=1}^{\infty}\frac{n}{\left(n+1\right)!}=1$.

### Solution to Problem 4

By **Definition** (Basic Expansions), $e^x=\sum_{n=0}^{\infty}\frac{x^n}{n!}$, so

$$
e^x-1=\sum_{n=1}^{\infty}\frac{x^n}{n!}=x\sum_{n=1}^{\infty}\frac{x^{n-1}}{n!}=x\sum_{n=0}^{\infty}\frac{x^n}{\left(n+1\right)!}.
$$

When $x\ne 0$, dividing both sides by $x$ gives

$$
\sum_{n=0}^{\infty}\frac{x^n}{\left(n+1\right)!}=\frac{1}{x}\left(e^x-1\right).
$$

Differentiating both sides of the above with respect to $x$ (by **Theorem 4.1** and the validity of term-by-term differentiation of power series), we get

$$
\sum_{n=1}^{\infty}\frac{nx^{n-1}}{\left(n+1\right)!}=\frac{xe^x-\left(e^x-1\right)}{x^2}=\frac{e^x\left(x-1\right)+1}{x^2}.
$$

Letting $x=1$, the left side is $\sum_{n=1}^{\infty}\frac{n}{\left(n+1\right)!}$, and the right side is $e\left(0\right)+1=1$. Hence

$$
\sum_{n=1}^{\infty}\frac{n}{\left(n+1\right)!}=1.

$$

$\blacksquare$
### Problem 5

(Problem 11.4-3) Using the result of the previous problem, prove that
$$
\sum_{n=1}^{\infty}\frac{n}{\left(n+2\right)!}=3-e.
$$

### Solution to Problem 5

Rewrite the general term:

$$
\frac{n}{\left(n+2\right)!}=\frac{\left(n+2\right)-2}{\left(n+2\right)!}=\frac{1}{\left(n+1\right)!}-\frac{2}{\left(n+2\right)!}.
$$

Thus

$$
\sum_{n=1}^{\infty}\frac{n}{\left(n+2\right)!}=\sum_{n=1}^{\infty}\frac{1}{\left(n+1\right)!}-2\sum_{n=1}^{\infty}\frac{1}{\left(n+2\right)!}.
$$

First compute the first sum:

$$
\sum_{n=1}^{\infty}\frac{1}{\left(n+1\right)!}=\sum_{m=2}^{\infty}\frac{1}{m!}=e-1-1=e-2.
$$

Then compute the second sum:

$$
\sum_{n=1}^{\infty}\frac{1}{\left(n+2\right)!}=\sum_{m=3}^{\infty}\frac{1}{m!}=e-1-1-\frac12=e-\frac52.
$$

Hence

$$
\sum_{n=1}^{\infty}\frac{n}{\left(n+2\right)!}=\left(e-2\right)-2\left(e-\frac52\right)=e-2-2e+5=3-e.

$$

$\blacksquare$