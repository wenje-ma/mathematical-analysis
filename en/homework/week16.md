# Assignment 16

> **Theorem 4.1** (Local Taylor Expansion) Let $y=f\left(x\right)$ be defined near $x_0$, and have an $n$-th derivative $f^{\left(n\right)}\left(x_0\right)$. Then
> $$
> f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\frac{f''\left(x_0\right)}{2!}\left(x-x_0\right)^2+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right)\left(x\to x_0\right).
> $$
> **Theorem 4.2** (Taylor Formula with Lagrange Remainder) Let $y=f\left(x\right)$ have $n$ continuous derivatives on $\left[a,b\right]$ and an $n+1$-th derivative on $\left(a,b\right)$. Then for any $x,x_0\in\left[a,b\right]$, there exists a point $\xi$ between $x_0$ and $x$ such that
> $$
> f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+\frac{f^{\left(n+1\right)}\left(\xi\right)}{\left(n+1\right)!}\left(x-x_0\right)^{n+1}.
> $$
### Problem 1

(Problem 3.4-1-2) Write down the local Taylor formula of the function $y=\frac{1}{1-x}$ at $x=0$.

### Solution to Problem 1

Differentiate $f\left(x\right)=\frac{1}{1-x}$ to all orders:
$$
f'\left(x\right)=\frac{1}{\left(1-x\right)^2}, f''\left(x\right)=\frac{2}{\left(1-x\right)^3},\cdots, f^{\left(n\right)}\left(x\right)=\frac{n!}{\left(1-x\right)^{n+1}}.
$$

Hence $f^{\left(n\right)}\left(0\right)=n!$. By **Theorem 4.1** (Local Taylor Expansion),
$$
\frac{1}{1-x}=1+x+x^2+\cdots+x^n+o\left(x^n\right)\left(x\to0\right).
$$

$\blacksquare$
### Problem 2

(Problem 3.4-1-4) Write down the local Taylor formula of the function $y=\arctan x$ at $x=0$ (expand up to $x^5$).

### Solution to Problem 2

Differentiate $f\left(x\right)=\arctan x$ to all orders:
$$
f'\left(x\right)=\frac{1}{1+x^2}, f''\left(x\right)=\frac{-2x}{\left(1+x^2\right)^2}, f'''\left(x\right)=\frac{6x^2-2}{\left(1+x^2\right)^3},
$$
$$
f^{\left(4\right)}\left(x\right)=\frac{24x\left(1-x^2\right)}{\left(1+x^2\right)^4}, f^{\left(5\right)}\left(x\right)=\frac{24\left(1-10x^2+5x^4\right)}{\left(1+x^2\right)^5}.
$$

Substituting $x=0$:
$$
f\left(0\right)=0, f'\left(0\right)=1, f''\left(0\right)=0, f'''\left(0\right)=-2, f^{\left(4\right)}\left(0\right)=0, f^{\left(5\right)}\left(0\right)=24.
$$

By **Theorem 4.1** (Local Taylor Expansion),
$$
\arctan x=x-\frac{x^3}{3}+\frac{x^5}{5}+o\left(x^5\right)\left(x\to0\right).
$$

$\blacksquare$
### Problem 3

(Problem 3.4-1-5) Write down the local Taylor formula of the function $y=\tan x$ at $x=0$ (expand up to $x^3$).

### Solution to Problem 3

Differentiate $f\left(x\right)=\tan x$ to all orders:
$$
f'\left(x\right)=\sec^2 x, f''\left(x\right)=2\sec^2 x\tan x, f'''\left(x\right)=4\sec^2 x\tan^2 x+2\sec^4 x.
$$

Substituting $x=0$:
$$
f\left(0\right)=0, f'\left(0\right)=1, f''\left(0\right)=0, f'''\left(0\right)=2.
$$

By **Theorem 4.1** (Local Taylor Expansion),
$$
\tan x=x+\frac{x^3}{3}+o\left(x^3\right)\left(x\to0\right).
$$

$\blacksquare$
### Problem 4

(Problem 3.4-4) Expand $y=\sin\left(x+\alpha\right)$ at $\alpha=0$ into a Taylor formula with Lagrange remainder, and estimate the size of the remainder in the expansion
$$
\sin\left(x+\alpha\right)=\sin x+\left(\cos x\right)\alpha+r\left(\alpha\right)
$$
.

### Solution to Problem 4

Treat $x$ as a constant and differentiate with respect to $\alpha$:
$$
\frac{\mathrm{d}}{\mathrm{d}\alpha}\sin\left(x+\alpha\right)=\cos\left(x+\alpha\right),\frac{\mathrm{d}^2}{\mathrm{d}\alpha^2}\sin\left(x+\alpha\right)=-\sin\left(x+\alpha\right).
$$

At $\alpha=0$,
$$
\sin\left(x+0\right)=\sin x,\frac{\mathrm{d}}{\mathrm{d}\alpha}\sin\left(x+\alpha\right)\Big|_{\alpha=0}=\cos x.
$$

By **Theorem 4.2** (Taylor Formula with Lagrange Remainder),
$$
\sin\left(x+\alpha\right)=\sin x+\left(\cos x\right)\alpha+\frac{-\sin\left(x+\xi\right)}{2!}\alpha^2,
$$

where $\xi$ lies between $0$ and $\alpha$.

The remainder is $r\left(\alpha\right)=-\frac{\sin\left(x+\xi\right)}{2}\alpha^2$, hence
$$
\left|r\left(\alpha\right)\right|\le\frac{\alpha^2}{2}.
$$

$\blacksquare$
### Problem 5

(Problem 3.4-5) Expand $y=x+\frac{x^3}{3}$ at $x=\pm1$ into a Taylor formula. Show that the remainder of the $n$-th Taylor expansion of any polynomial $P_n\left(x\right)$ at any point $a$ is $0$.

### Solution to Problem 5

Differentiate $f\left(x\right)=x+\frac{x^3}{3}$ to all orders:
$$
f'\left(x\right)=1+x^2, f''\left(x\right)=2x, f'''\left(x\right)=2, f^{\left(4\right)}\left(x\right)=0.
$$

At $x=1$:
$$
f\left(1\right)=1+\frac13=\frac43, f'\left(1\right)=2, f''\left(1\right)=2, f'''\left(1\right)=2.
$$

By **Theorem 4.1** (Local Taylor Expansion),
$$
x+\frac{x^3}{3}=\frac43+2\left(x-1\right)+\frac{2}{2!}\left(x-1\right)^2+\frac{2}{3!}\left(x-1\right)^3=\frac43+2\left(x-1\right)+\left(x-1\right)^2+\frac13\left(x-1\right)^3.
$$

At $x=-1$:
$$
f\left(-1\right)=-1-\frac13=-\frac43, f'\left(-1\right)=2, f''\left(-1\right)=-2, f'''\left(-1\right)=2.
$$

Hence
$$
x+\frac{x^3}{3}=-\frac43+2\left(x+1\right)-\left(x+1\right)^2+\frac13\left(x+1\right)^3.
$$

For a general polynomial $P_n\left(x\right)$ of degree $n$, we have $P_n^{\left(n+1\right)}\left(x\right)\equiv0$. By **Theorem 4.2** (Taylor Formula with Lagrange Remainder), the remainder is
$$
R_n\left(x\right)=\frac{P_n^{\left(n+1\right)}\left(\xi\right)}{\left(n+1\right)!}\left(x-a\right)^{n+1}=0.
$$

That is, the Taylor expansion of a polynomial is exact, with remainder $0$. $\blacksquare$

### Problem 6

(Problem 3.4-7) Let $y=f\left(x\right)$ have an $n+1$-th derivative at $a$. Prove that the derivative of the $n+1$-th Taylor polynomial of $f$ at $a$ equals the $n$-th Taylor polynomial of $f'$ at $a$.

### Solution to Problem 6

The $n+1$-th Taylor polynomial of $f$ at $a$ is
$$
T_{n+1}\left(x\right)=f\left(a\right)+f'\left(a\right)\left(x-a\right)+\frac{f''\left(a\right)}{2!}\left(x-a\right)^2+\cdots+\frac{f^{\left(n+1\right)}\left(a\right)}{\left(n+1\right)!}\left(x-a\right)^{n+1}.
$$

Differentiating with respect to $x$:
$$
T_{n+1}'\left(x\right)=f'\left(a\right)+f''\left(a\right)\left(x-a\right)+\frac{f'''\left(a\right)}{2!}\left(x-a\right)^2+\cdots+\frac{f^{\left(n+1\right)}\left(a\right)}{n!}\left(x-a\right)^n.
$$

On the other hand, the $n$-th Taylor polynomial of $f'$ at $a$ is
$$
U_n\left(x\right)=f'\left(a\right)+\left(f'\right)'\left(a\right)\left(x-a\right)+\frac{\left(f'\right)''\left(a\right)}{2!}\left(x-a\right)^2+\cdots+\frac{\left(f'\right)^{\left(n\right)}\left(a\right)}{n!}\left(x-a\right)^n.
$$

Note that $\left(f'\right)^{\left(k\right)}\left(a\right)=f^{\left(k+1\right)}\left(a\right)$, hence
$$
U_n\left(x\right)=f'\left(a\right)+f''\left(a\right)\left(x-a\right)+\frac{f'''\left(a\right)}{2!}\left(x-a\right)^2+\cdots+\frac{f^{\left(n+1\right)}\left(a\right)}{n!}\left(x-a\right)^n.
$$

Comparing the two expressions, we obtain $T_{n+1}'\left(x\right)=U_n\left(x\right)$. $\blacksquare$

### Problem 7

(Problem 3.4-10) Prove that as $x\to0$,
$$
\arctan x=x-\frac{x^3}{3}+\frac{x^5}{5}-\cdots+\left(-1\right)^m\frac{x^{2m+1}}{2m+1}+o\left(x^{2m+1}\right).
$$
### Solution to Problem 7

By the result of Problem 6 (the 7th problem), the derivative of the Taylor polynomial of $f$ equals the Taylor polynomial of $f'$.

For $f\left(x\right)=\arctan x$, we have
$$
f'\left(x\right)=\frac{1}{1+x^2}.
$$

By the result of Problem 1 (the 1(2)-th problem), substitute $-x^2$ into the expansion of $\frac{1}{1-t}$:
$$
\frac{1}{1+x^2}=1-x^2+x^4-\cdots+\left(-1\right)^m x^{2m}+o\left(x^{2m}\right)\left(x\to0\right).
$$

That is, the $2m$-th Taylor polynomial of $f'\left(x\right)$ is
$$
1-x^2+x^4-\cdots+\left(-1\right)^m x^{2m}.
$$

By the result of Problem 6 (the 7th problem), the $2m+1$-th Taylor polynomial of $f\left(x\right)$ is obtained by integrating the above polynomial term by term starting from the constant term (i.e. finding its antiderivative):
$$
\arctan x=x-\frac{x^3}{3}+\frac{x^5}{5}-\cdots+\left(-1\right)^m\frac{x^{2m+1}}{2m+1}+o\left(x^{2m+1}\right)\left(x\to0\right).
$$

$\blacksquare$
### Problem 8

(Problem 3.4-11) Let $f\left(x\right)=x^{1/5}$, $x=32$, $\Delta x=0.16$. Then
$$
f\left(32.16\right)=f\left(32\right)+f'\left(32\right)\Delta x+\frac{f''\left(\xi\right)}{2!}\left(\Delta x\right)^2,
$$
where $\xi$ lies between $32$ and $32.16$. From the example in Chapter 2 we have

$$
f\left(32\right)+f'\left(32\right)\Delta x=2.002.
$$

Prove that as an approximation to $32.16^{1/5}$, the absolute error of $2.002$ is less than $10^{-6}$.

### Solution to Problem 8

The error is the Lagrange remainder:
$$
R_1=\frac{f''\left(\xi\right)}{2!}\left(\Delta x\right)^2,\xi\in\left(32,32.16\right).
$$

Differentiate $f\left(x\right)=x^{1/5}$ twice:
$$
f'\left(x\right)=\frac15 x^{-4/5}, f''\left(x\right)=\frac15\cdot\left(-\frac45\right)x^{-9/5}=-\frac{4}{25}x^{-9/5}.
$$

Hence
$$
\left|R_1\right|=\left|\frac{f''\left(\xi\right)}{2}\right|\left(0.16\right)^2=\frac{2}{25}\xi^{-9/5}\cdot\left(0.16\right)^2.
$$

Since $\xi>32$,

$$
\xi^{-9/5}<32^{-9/5}=\left(2^5\right)^{-9/5}=2^{-9}=\frac{1}{512}.
$$

Thus
$$
\left|R_1\right|<\frac{2}{25}\cdot\frac{1}{512}\cdot\left(0.16\right)^2=\frac{2\cdot0.0256}{25\cdot512}=4\times10^{-6}.
$$

That is, as an approximation to $32.16^{1/5}$, the absolute error of $2.002$ is about $4\times10^{-6}$. $\blacksquare$

### Problem 9

(Problem 3.4-12) Use the local Taylor expansion to prove the following conclusion: let $y=f\left(x\right)$ have an $n$-th derivative at $x_0$, $n>1$, and
$$
f'\left(x_0\right)=f''\left(x_0\right)=\cdots=f^{\left(n-1\right)}\left(x_0\right)=0, f^{\left(n\right)}\left(x_0\right)\ne0.
$$
When $n$ is odd, $x_0$ is definitely not an extremum point; when $n$ is even, if $f^{\left(n\right)}\left(x_0\right)>0$, then $x_0$ is a local minimum point; if $f^{\left(n\right)}\left(x_0\right)<0$, then $x_0$ is a local maximum point.

### Solution to Problem 9

By **Theorem 4.1** (Local Taylor Expansion), near $x_0$,
$$
f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right).
$$

By the assumption

$$
f'\left(x_0\right)=\cdots=f^{\left(n-1\right)}\left(x_0\right)=0,
$$

hence
$$
f\left(x\right)-f\left(x_0\right)=\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right).
$$

When $n$ is odd, $\left(x-x_0\right)^n$ changes sign on the two sides of $x_0$ (negative on the left, positive on the right), while $\frac{f^{\left(n\right)}\left(x_0\right)}{n!}$ is a fixed nonzero constant; hence $f\left(x\right)-f\left(x_0\right)$ changes sign on the two sides of $x_0$. Therefore $x_0$ is not an extremum point.

When $n$ is even, $\left(x-x_0\right)^n>0$ ($x\ne x_0$). If $f^{\left(n\right)}\left(x_0\right)>$, then $f\left(x\right)-f\left(x_0\right)>0$ ($x$ sufficiently close to $x_0$ and $x\ne x_0$), i.e. $f\left(x\right)>f\left(x_0\right)$, so $x_0$ is a local minimum point. If $f^{\left(n\right)}\left(x_0\right)<0$, then $f\left(x\right)-f\left(x_0\right)<0$, i.e. $f\left(x\right)<f\left(x_0\right)$, so $x_0$ is a local maximum point. $\blacksquare$
