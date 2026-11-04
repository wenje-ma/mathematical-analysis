# week32

> **Theorem 1.1 (Weierstrass M-Test)**
> 
> If $\left|f_n\left(x\right)-f\left(x\right)\right|\le M_n$ and $M_n\to0$, then the convergence is uniform.

> **Theorem 1.2 (Continuity of the Limit Function)**
> 
> If $\left\{f_n\right\}$ converges uniformly to $f$ and each $f_n$ is continuous, then $f$ is continuous.

> **Theorem 2.2 (Weierstrass M-Test)**
> 
> If $\left|u_n\left(x\right)\right|\le a_n$ and $\sum a_n$ converges, then $\sum u_n\left(x\right)$ converges uniformly.

> **Theorem 2.4 (Dirichlet's Test)**
> 
> If partial sums of $\sum a_n\left(x\right)$ are uniformly bounded and $b_n\left(x\right)$ is monotone and uniformly tends to $0$, then $\sum a_nb_n$ converges uniformly.

> **Theorem 2.5 (Continuity of the Sum Function)**
> 
> If $u_n$ are continuous and $\sum u_n$ converges uniformly, then the sum is continuous.

> **Theorem 2.7 (Term-by-Term Differentiation)**
> 
> If $\sum u_n$ converges, $u_n'$ are continuous, and $\sum u_n'$ converges uniformly, then $S'=\sum u_n'$.

> **Theorem 3.2 (Cauchy's Formula for Radius of Convergence)**
> 
> $\frac1R=\limsup_{n\to\infty}\sqrt\left[n\right]{\left|a_n\right|}$.

> **Theorem 3.3 (d'Alembert's Formula for Radius of Convergence)**
> 
> If $\lim\left|\frac{a_n}{a_{n+1}}\right|=R$, then the radius is $R$.

> **Theorem 3.4 (Uniform Convergence on Closed Intervals)**
> 
> Power series converge uniformly on closed intervals inside the radius, and can be differentiated and integrated term by term.

## 11.1-3

Prove $\left(1+\frac xn\right)^n$ does not converge uniformly to $e^x$ on $\left[0,+\infty\right)$.

### Solution to 11.1-3

Since $\left|\left(1+1\right)^n-e^n\right|\to+\infty$. $\blacksquare$

## 11.1-4

Prove uniform convergence on $\left[0,A\right]$.

### Solution to 11.1-4

By the M-test with $M_n=\frac{A^2e^A}{2n}$. $\blacksquare$

## 11.1-5

Prove: uniform convergence iff $M_n=\max\left|f_n-f\right|\to0$.

### Solution to 11.1-5

Direct from the definition. $\blacksquare$

## 11.2-1-2

Discuss $\sum\frac{\left(-1\right)^{n+1}}{x^2+n}$.

### Solution to 11.2-1-2

Uniformly convergent by Dirichlet's test. $\blacksquare$

## 11.2-1-4

Discuss the telescoping series.

### Solution to 11.2-1-4

Not uniformly convergent since the sum is discontinuous. $\blacksquare$

## 11.2-1-6

Discuss $\sum\frac1{n^2+x^2}$.

### Solution to 11.2-1-6

Uniformly convergent by the M-test. $\blacksquare$

## 11.2-9

Discuss $\sum\left(-1\right)^n\frac{n+x^2}{n^2}$.

### Solution to 11.2-9

Uniformly convergent on $\left[a,b\right]$, not on $\mathbb R$. $\blacksquare$

## 11.2-10

Discuss $\sum\left(-1\right)^{n-1}x^2e^{-nx^2}$.

### Solution 11.2-1-10

Uniformly convergent by Dirichlet's test. $\blacksquare$

## 11.2-11

Discuss $\sum\frac{\sin x\sin nx}{\sqrt{n^2+x^2}}$.

### Solution to 11.2-11

Uniformly convergent on $\left[0,2\pi\right]$. $\blacksquare$

## 11.2-5

Prove $f\left(x\right)=\sum2^n\sin\frac x{3^n}$ has a continuous derivative everywhere.

### Solution to 11.2-5

By the M-test and term-by-term differentiation. $\blacksquare$

## 11.2-6

Prove $\zeta'\left(x\right)=-\sum\frac{\ln n}{n^x}$.

### Solution to 11.2-6

By the M-test and term-by-term differentiation. $\blacksquare$

## 11.3-1-1

Find the radius of convergence of $\sum\frac{3^n}{n!}x^n$.

### Solution to 11.3-1-1

$R=+\infty$. $\blacksquare$

## 11.3-1-2

Find the radius of $\sum\frac n{2^n}x^n$.

### Solution to 11.3-1-2

$R=2$. $\blacksquare$

## 11.3-1-3

Find the radius of $\sum\frac{n!}{\left(2n\right)!}x^n$.

### Solution to 11.3-1-3

$R=+\infty$. $\blacksquare$

## 11.3-1-4

Find the radius of $\sum\frac{\left(n!\right)^2}{\left(2n\right)!}x^n$.

### Solution to 11.3-1-4

$R=4$. $\blacksquare$

## 11.3-2-2

Find the convergence set of $\sum n^3\left(x-5\right)^n$.

### Solution to 11.3-2-2

$\left(4,6\right)$. $\blacksquare$

## 11.3-2-4

Find the convergence set of $\sum\frac{\left(-1\right)^n}{\sqrt n}x^n$.

### Solution to 11.3-2-4

$\left(-1,1\right]$. $\blacksquare$

## 11.3-2-6

Find the convergence set.

### Solution to 11.3-2-6

$\left(-4,4\right)$. $\blacksquare$
