# week18

> **Theorem 1.3 (Lagrange Mean Value Theorem)**
> 
> If $f$ is continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$, then there exists $c\in\left(a,b\right)$ such that $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

> **Theorem 4.1 (Local Taylor Expansion)**
> 
> If $f$ has $n$ derivatives at $x_0$, then $f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right)$ as $x\to x_0$.

> **Theorem 4.2 (Taylor Formula with Lagrange Remainder)**
> 
> If $f$ has $n$ continuous derivatives on $\left[a,b\right]$ and $n+1$ derivatives on $\left(a,b\right)$, then for any $x,x_0\in\left[a,b\right]$, there exists $\xi$ between $x_0$ and $x$ such that $f\left(x\right)=f\left(x_0\right)+\cdots+\frac{f^{\left(n+1\right)}\left(\xi\right)}{\left(n+1\right)!}\left(x-x_0\right)^{n+1}$.

> **Theorem 5.1 (Second Derivative Criterion for Convexity)**
> 
> If $f$ is twice differentiable on $\left(a,b\right)$, then $f$ is convex iff $f''\left(x\right)\ge0$, and concave iff $f''\left(x\right)\le0$.

## 3.4-7

Prove that the derivative of the $\left(n+1\right)$-th Taylor polynomial of $f$ at $a$ equals the $n$-th Taylor polynomial of $f'$ at $a$.

### Solution to 3.4-7

Differentiating $T_{n+1}\left(x\right)=f\left(a\right)+f'\left(a\right)\left(x-a\right)+\cdots+\frac{f^{\left(n+1\right)}\left(a\right)}{\left(n+1\right)!}\left(x-a\right)^{n+1}$ gives

$$
T_{n+1}'\left(x\right)=f'\left(a\right)+f''\left(a\right)\left(x-a\right)+\cdots+\frac{f^{\left(n+1\right)}\left(a\right)}{n!}\left(x-a\right)^n,
$$

which is exactly the $n$-th Taylor polynomial of $f'$. $\blacksquare$

## 3.4-10

Prove that as $x\to0$, $\arctan x=x-\frac{x^3}3+\frac{x^5}5-\cdots+\left(-1\right)^m\frac{x^{2m+1}}{2m+1}+o\left(x^{2m+1}\right)$.

### Solution to 3.4-10

Since $f'\left(x\right)=\frac1{1+x^2}$, substituting $-x^2$ into the geometric expansion (3.4-1-2) gives

$$
\frac1{1+x^2}=1-x^2+x^4-\cdots+\left(-1\right)^m x^{2m}+o\left(x^{2m}\right).
$$

Integrating term by term (by 3.4-7),

$$
\arctan x=x-\frac{x^3}3+\frac{x^5}5-\cdots+\left(-1\right)^m\frac{x^{2m+1}}{2m+1}+o\left(x^{2m+1}\right).
$$

$\blacksquare$

## 3.4-11

Let $f\left(x\right)=x^{1/5}$, $x=32$, $\Delta x=0.16$. Given $f\left(32\right)+f'\left(32\right)\Delta x=2.002$, prove that the absolute error is less than $10^{-6}$.

### Solution to 3.4-11

The error is the Lagrange remainder:

$$
\left|R_1\right|=\frac2{25}\xi^{-9/5}\cdot\left(0.16\right)^2.
$$

Since $\xi> 32$, $\xi^{-9/5}< 2^{-9}=\frac1{512}$. Thus

$$
\left|R_1\right|< \frac2{25}\cdot\frac1{512}\cdot0.0256=4\times10^{-6}.
$$

$\blacksquare$

## 3.4-12

Let $f'\left(x_0\right)=\cdots=f^{\left(n-1\right)}\left(x_0\right)=0$ and $f^{\left(n\right)}\left(x_0\right)\ne0$. Prove: if $n$ is odd, $x_0$ is not an extremum; if $n$ is even and $f^{\left(n\right)}\left(x_0\right)> 0$, $x_0$ is a local minimum; if $f^{\left(n\right)}\left(x_0\right)< 0$, it is a local maximum.

### Solution to 3.4-12

By **Theorem 4.1 (Local Taylor Expansion)**,

$$
f\left(x\right)-f\left(x_0\right)=\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right).
$$

If $n$ is odd, $\left(x-x_0\right)^n$ changes sign on either side of $x_0$, so $f\left(x\right)-f\left(x_0\right)$ changes sign; $x_0$ is not an extremum.

If $n$ is even, $\left(x-x_0\right)^n> 0$ for $x\ne x_0$. If $f^{\left(n\right)}\left(x_0\right)> 0$, then $f\left(x\right)> f\left(x_0\right)$, so $x_0$ is a local minimum. If $f^{\left(n\right)}\left(x_0\right)< 0$, then $f\left(x\right)< f\left(x_0\right)$, so $x_0$ is a local maximum. $\blacksquare$

## 3.5-1-1

Find the convexity intervals and inflection points of $y=xe^x$.

### Solution to 3.5-1-1

$y'=\left(1+x\right)e^x$, $y''=\left(2+x\right)e^x$. Setting $y''=0$ gives $x=-2$. By **Theorem 5.1 (Second Derivative Criterion for Convexity)**, $y$ is concave on $\left(-\infty,-2\right]$ and convex on $\left[-2,+\infty\right)$. The inflection point is $\left(-2,-2e^{-2}\right)$. $\blacksquare$

## 3.5-1-4

Find the convexity intervals and inflection points of $y=x\ln x$.

### Solution to 3.5-1-4

Domain $\left(0,+\infty\right)$. $y''=\frac1x> 0$. By **Theorem 5.1 (Second Derivative Criterion for Convexity)**, $y=x\ln x$ is convex on $\left(0,+\infty\right)$ with no inflection points. $\blacksquare$

## 3.5-2

Use convexity to prove:

(1) $2\arctan\frac{a+b}2\ge\arctan a+\arctan b$ for $a,b> 0$;

(2) $a^\alpha b^\beta c^\gamma\le\alpha a+\beta b+\gamma c$ for $a,b,c> 0$, $\alpha+\beta+\gamma=1$.

### Solution to 3.5-2

(1) $f\left(x\right)=\arctan x$ has $f''\left(x\right)=\frac{-2x}{\left(1+x^2\right)^2}< 0$ for $x> 0$, so it is concave. By Definition of Convex and Concave Functions with $t=\frac12$,

$$
f\left(\frac{a+b}2\right)\ge\frac{f\left(a\right)+f\left(b\right)}2.
$$

(2) $f\left(x\right)=\ln x$ is concave ($f''=-\frac1{x^2}< 0$). By concavity,

$$
\alpha\ln a+\beta\ln b+\gamma\ln c\le\ln\left(\alpha a+\beta b+\gamma c\right),
$$

which gives the weighted AM-GM inequality. $\blacksquare$
