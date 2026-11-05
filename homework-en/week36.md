# week36

> **Theorem 3.1 (Dirichlet's Convergence Theorem)**
> 
> The Fourier series converges to $\frac{f\left(x+0\right)+f\left(x-0\right)}2$ at every point.

> **Theorem 4.1 (Bessel's Inequality)**
> 
> $\frac{a_0^2}2+\sum\left(a_n^2+b_n^2\right)\le\frac1\pi\int{f}^2$.

> **Theorem 4.2 (Parseval's Identity)**
> 
> $\frac1\pi\int{f}^2=\frac{a_0^2}2+\sum\left(a_n^2+b_n^2\right)$.

> **Proposition (Integral Forms)**
> 
> $\int_0^\infty\frac{x^{a-1}}{\left(1+x\right)^{a+b}}\mathrm{d}x=\Beta\left(a,b\right)$; $\int_0^{\pi/2}\sin^mx\cos^nx\,\mathrm{d}x=\frac12\Beta\left(\frac{m+1}2,\frac{n+1}2\right)$.

> **Proposition (Orthogonality of Trigonometric System)**
> 
> $1,\cos{x},\sin{x},\cdots$ are pairwise orthogonal on $\left[-\pi,\pi\right]$, with $\int1=2\pi$, $\int\cos^2nx=\int\sin^2nx=\pi$.

> **Proposition (Fourier Coefficients)**
> 
> $a_n=\frac1\pi\int_{-\pi}^\pi{f}\cos{n}x$, $b_n=\frac1\pi\int_{-\pi}^\pi{f}\sin{n}x$.

> **Theorem (Parseval's Identity)**
> 
> $\frac1\pi\int_{-\pi}^\pi{f}^2=\frac{a_0^2}2+\sum\left(a_n^2+b_n^2\right)$.

## 12.6-2

Prove $\Gamma\left(\alpha\right)$ does not converge uniformly on $\left(0,+\infty\right)$.

### Solution to 12.6-2

By choosing $\alpha_n=\frac1n$. $\blacksquare$

## 13.1-1

Prove symmetry and linearity of the inner product.

### Solution to 13.1-1

By definition and linearity of integration. $\blacksquare$

## 13.1-2

Prove the Cauchy-Schwarz inequality.

### Solution to 13.1-2

By $\left|f-\lambda{g}\right|^2\ge0$ and discriminant. $\blacksquare$

## 13.1-3

Prove equality holds iff $f,g$ are linearly dependent.

### Solution to 13.1-3

By continuity and $\left|f-\lambda_0g\right|^2=0$. $\blacksquare$

## 13.1-7

Prove linear independence of the trigonometric system.

### Solution to 13.1-7

By orthogonality. $\blacksquare$

## 13.2-1-1

Find the Fourier series of $f\left(x\right)=x^2$.

### Solution to 13.2-1-1

$x^2\sim\frac{\pi^2}3+4\sum\frac{\left(-1\right)^n}{n^2}\cos{n}x$. $\blacksquare$

## 13.2-1-3

Find the Fourier series of $\sin^4x$.

### Solution to 13.2-1-3

$\sin^4x=\frac38-\frac12\cos2x+\frac18\cos4x$. $\blacksquare$

## 13.2-1-5

Find the Fourier series of the given piecewise function.

### Solution to 13.2-1-5

$f\left(x\right)\sim\frac\pi4-\frac2\pi\sum\frac{\cos\left(2k+1\right)x}{\left(2k+1\right)^2}+\sum\frac{\left(-1\right)^{n+1}}n\sin{n}x$. $\blacksquare$

## 13.2-7

Prove: half-period shift implies odd/even coefficient vanishing.

### Solution to 13.2-7

By splitting the integral and substituting $x=t-\pi$. $\blacksquare$

## 13.3-1

Prove $1=\frac12+\frac2\pi\sum\frac{\sin\left(2n+1\right)x}{2n+1}$ and $\frac\pi4=\sum\frac{\left(-1\right)^n}{2n+1}$.

### Solution to 13.3-1

By the Dirichlet theorem and setting $x=\frac\pi2$. $\blacksquare$

## 13.3-3

Find the Fourier series of $\left(\pi-\left|x\right|\right)^2$ and compute $\sum\frac1{n^2}$, $\sum\frac1{n^4}$.

### Solution to 13.3-3

$\sum\frac1{n^2}=\frac{\pi^2}6$, $\sum\frac1{n^4}=\frac{\pi^4}{90}$. $\blacksquare$

## 13.3-4

Use $x^2$ Fourier series to compute $\sum\frac{\left(-1\right)^{n+1}}{n^2}$ and $\sum\frac1{n^2}$.

### Solution to 13.3-4

$\sum\frac1{n^2}=\frac{\pi^2}6$, $\sum\frac{\left(-1\right)^{n+1}}{n^2}=\frac{\pi^2}{12}$. $\blacksquare$

## 13.4-1

Prove $\sum\frac{a_n}{n}$ and $\sum\frac{b_n}{n}$ converge.

### Solution to 13.4-1

By Bessel's inequality and Cauchy-Schwarz. $\blacksquare$

## 13.4-2

Explain why the given series is not a Fourier series.

### Solution to 13.4-2

Because $\sum\frac{a_n}{n}$ diverges. $\blacksquare$

## 13.4-5

Use Parseval's identity for $x^2$ to compute $\sum\frac1{n^4}$.

### Solution to 13.4-5

$\sum\frac1{n^4}=\frac{\pi^4}{90}$. $\blacksquare$

## 13.4-7

Use Parseval's identity for $\left|x\right|$ to compute $\sum\frac1{\left(2n-1\right)^4}$.

### Solution to 13.4-7

$\sum\frac1{\left(2n-1\right)^4}=\frac{\pi^4}{96}$. $\blacksquare$
