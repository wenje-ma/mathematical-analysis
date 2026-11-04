# week33

> **Theorem 1.1 (Cauchy Criterion)**
> 
> The integral converges iff for every $\varepsilon> 0$, there exists $X$ such that $\left|\int_{A'}^{A''}f\right|< \varepsilon$ for $A',A''> X$.

> **Example 1.2 (p-Integral)**
> 
> $\int_1^\infty\frac{\mathrm dx}{x^p}$ converges iff $p> 1$.

> **Theorem 1.3 (Comparison Test)**
> 
> If $0\le f\le g$, then $\int g$ convergent implies $\int f$ convergent.

> **Theorem 1.6 (Dirichlet's Test)**
> 
> If $f$ is monotone tending to $0$ and $\int_a^A g$ is bounded for all $A$, then $\int fg$ converges.

> **Theorem 3.2 (Cauchy's Formula for Radius of Convergence)**
> 
> $\frac1R=\limsup_{n\to\infty}\sqrt\left[n\right]{\left|a_n\right|}$.

> **Theorem 3.3 (d'Alembert's Formula for Radius of Convergence)**
> 
> If $\lim\left|\frac{a_n}{a_{n+1}}\right|=R$, then the radius is $R$.

> **Theorem 3.4 (Uniform Convergence on Closed Intervals)**
> 
> Power series converge uniformly on closed intervals inside the radius, and can be differentiated and integrated term by term.

> **Theorem 4.1 (Taylor Series)**
> 
> If $f$ has a power series expansion, then the coefficients are uniquely determined: $a_n=\frac{f^{\left(n\right)}\left(x_0\right)}{n!}$.

## 11.3-2-8

Find the convergence set.

### Solution to 11.3-2-8

$\left(-1,1\right)$. $\blacksquare$

## 11.3-2-10

Find the convergence set.

### Solution to 11.3-2-10

$\left(-2,-1\right)$. $\blacksquare$

## 11.3-3-1

Find the sum of $\sum\left(n+1\right)x^n$.

### Solution to 11.3-3-1

$\frac1{\left(1-x\right)^2}$. $\blacksquare$

## 11.3-3-3

Find the sum of $\sum n^2x^n$.

### Solution to 11.3-3-3

$\frac{x\left(1+x\right)}{\left(1-x\right)^3}$. $\blacksquare$

## 11.3-3-5

Find the sum of $\sum\frac{x^n}{n\left(n+1\right)}$.

### Solution to 11.3-3-5

$1-\frac{1-x}x\ln\left(1-x\right)$. $\blacksquare$

## 11.3-3-7

Find the sum of $\sum\frac{x^n}n$.

### Solution to 11.3-3-7

$-\ln\left(1-x\right)$. $\blacksquare$

## 11.3-4

Prove: if $\sum a_nx^n$ has radius $R$, then $\sum a_nx^{2n}$ has radius $\sqrt R$.

### Solution to 11.3-4

Set $y=x^2$. $\blacksquare$

## 11.3-5

Prove: for any $A> \frac1R$, there exists $C> 0$ such that $\left|a_n\right|\le CA^n$.

### Solution to 11.3-5

Choose $r$ with $\frac1A< r< R$. $\blacksquare$

## 11.4-1-3

Expand $e^x$ around $x_0=3$.

### Solution to 11.4-1-3

$e^x=e^3\sum\frac{\left(x-3\right)^n}{n!}$. $\blacksquare$

## 11.4-1-4

Expand $\ln x$ around $x_0=2$.

### Solution to 11.4-1-4

$\ln x=\ln2+\sum\frac{\left(-1\right)^{n-1}}{n\cdot2^n}\left(x-2\right)^n$. $\blacksquare$

## 11.4-1-5

Expand $\cos^2x$ around $x_0=0$.

### Solution to 11.4-1-5

$\cos^2x=\frac12+\sum\frac{\left(-1\right)^n2^{2n-1}}{\left(2n\right)!}x^{2n}$. $\blacksquare$

## 11.4-2

Prove $\sum\frac{x^n}{\left(n+1\right)!}=\frac1x\left(e^x-1\right)$ and $\sum\frac n{\left(n+1\right)!}=1$.

### Solution to 11.4-2

From the expansion of $e^x$. $\blacksquare$

## 11.4-3

Prove $\sum\frac n{\left(n+2\right)!}=3-e$.

### Solution to 11.4-3

By splitting the general term. $\blacksquare$

## 12.1-1-1

Evaluate $\int_1^\infty\frac{\ln x}{x^2}\mathrm dx$.

### Solution to 12.1-1-1

Integration by parts gives $1$. $\blacksquare$

## 12.1-1-2

Evaluate $\int_1^\infty e^{-ax}\mathrm dx$.

### Solution to 12.1-1-2

$\frac{e^{-a}}a$. $\blacksquare$

## 12.1-1-3

Evaluate $\int_0^\infty\frac{\mathrm dx}{1+x^2}$.

### Solution to 12.1-1-3

$\frac\pi2$. $\blacksquare$

## 12.1-1-4

Evaluate $\int_0^\infty xe^{-x}\mathrm dx$.

### Solution to 12.1-1-4

$1$. $\blacksquare$

## 12.1-2-1

Discuss $\int_1^\infty\frac{\sin x}{x^p}\mathrm dx$.

### Solution to 12.1-2-1

Absolutely convergent for $p> 1$, conditionally for $0< p\le1$, divergent for $p\le0$. $\blacksquare$

## 12.1-2-3

Discuss $\int_1^\infty\frac{\sqrt x\cos x}{x+3}\mathrm dx$.

### Solution to 12.1-2-3

Conditionally convergent. $\blacksquare$

## 12.1-2-5

Discuss $\int_0^\infty\sin x^2\mathrm dx$.

### Solution to 12.1-2-5

Conditionally convergent. $\blacksquare$
