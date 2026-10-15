# Assignment 44

> **Theorem 3.2** (Cauchy's Formula for the Radius of Convergence) For a power series $\sum_{n=0}^{\infty}a_nx^n$, its radius of convergence $R$ satisfies
> $$
> \frac{1}{R}=\limsup_{n\to\infty}\sqrt\left[n\right]{\left|a_n\right|}.
> $$
>
> **Theorem 3.3** (d'Alembert's Formula for the Radius of Convergence) Let $a_n\ne 0$ and $\lim_{n\to\infty}\left|\frac{a_n}{a_{n+1}}\right|=R$. Then the radius of convergence of this power series is $R$.
>
> **Theorem 3.4** (Closed-Interval Uniform Convergence) A power series converges uniformly on any closed interval inside its interval of convergence; hence it may be differentiated and integrated term by term within the interval of convergence, without changing the radius of convergence.

### Problem 1

(Problem 11.3-1-1) Find the radius of convergence of the power series $\sum_{n=0}^{+\infty}\frac{3^n}{n!}x^n$.

### Solution to Problem 1

Let $a_n=\frac{3^n}{n!}$. Then

$$
\left|\frac{a_n}{a_{n+1}}\right|=\frac{3^n/n!}{3^{n+1}/\left(n+1\right)!}=\frac{n+1}{3}\to+\infty.
$$

By **Theorem 3.3** (d'Alembert's Formula), the radius of convergence is $R=+\infty$. $\blacksquare$

### Problem 2

(Problem 11.3-1-2) Find the radius of convergence of the power series $\sum_{n=0}^{+\infty}\frac{n}{2^n}x^n$.

### Solution to Problem 2

Let $a_n=\frac{n}{2^n}$. Then

$$
\left|\frac{a_n}{a_{n+1}}\right|=\frac{n/2^n}{\left(n+1\right)/2^{n+1}}=\frac{2n}{n+1}\to 2.
$$

By **Theorem 3.3** (d'Alembert's Formula), the radius of convergence is $R=2$. $\blacksquare$

### Problem 3

(Problem 11.3-1-3) Find the radius of convergence of the power series $\sum_{n=0}^{+\infty}\frac{n!}{\left(2n\right)!}x^n$.

### Solution to Problem 3

Let $a_n=\frac{n!}{\left(2n\right)!}$. Then

$$
\left|\frac{a_n}{a_{n+1}}\right|=\frac{n!/\left(2n\right)!}{\left(n+1\right)!/\left(2n+2\right)!}=\frac{\left(2n+2\right)\left(2n+1\right)}{n+1}=2\left(2n+1\right)\to+\infty.
$$

By **Theorem 3.3** (d'Alembert's Formula), the radius of convergence is $R=+\infty$. $\blacksquare$

### Problem 4

(Problem 11.3-1-4) Find the radius of convergence of the power series $\sum_{n=0}^{+\infty}\frac{\left(n!\right)^2}{\left(2n\right)!}x^n$.

### Solution to Problem 4

Let $a_n=\frac{\left(n!\right)^2}{\left(2n\right)!}$. Then

$$
\left|\frac{a_n}{a_{n+1}}\right|=\frac{\left(n!\right)^2/\left(2n\right)!}{\left(\left(n+1\right)!\right)^2/\left(2n+2\right)!}=\frac{\left(2n+2\right)\left(2n+1\right)}{\left(n+1\right)^2}=\frac{2\left(2n+1\right)}{n+1}\to 4.
$$

By **Theorem 3.3** (d'Alembert's Formula), the radius of convergence is $R=4$. $\blacksquare$

### Problem 5

(Problem 11.3-2-2) Find the set of convergence points of the power series $\sum_{n=1}^{+\infty}n^3\left(x-5\right)^n$.

### Solution to Problem 5

Let $t=x-5$. Then the series becomes $\sum n^3 t^n$. By **Theorem 3.3**, $\left|\frac{n^3}{\left(n+1\right)^3}\right|\to 1$, so the radius of convergence is $R=1$, i.e. $\left|t\right|<1$, which means $4<x<6$.

When $t=1$ ($x=6$), the series is $\sum n^3$, whose general term does not tend to zero, so it diverges; when $t=-1$ ($x=4$), the series is $\sum\left(-1\right)^n n^3$, whose general term likewise does not tend to zero, so it diverges. Hence the set of convergence points is $\left(4,6\right)$. $\blacksquare$

### Problem 6

(Problem 11.3-2-4) Find the set of convergence points of the power series $\sum_{n=1}^{+\infty}\frac{\left(-1\right)^n}{\sqrt n}x^n$.

### Solution to Problem 6

By **Theorem 3.3**,

$$
\left|\frac{\left(-1\right)^n/\sqrt n}{\left(-1\right)^{n+1}/\sqrt{n+1}}\right|=\sqrt{\frac{n+1}{n}}\to 1,
$$

so the radius of convergence is $R=1$.

When $x=1$, the series is $\sum\frac{\left(-1\right)^n}{\sqrt n}$, which converges by **Theorem 3.1** (Leibniz's Test) of Chapter 10; when $x=-1$, the series is $\sum\frac{-1}{\sqrt n}$, a $p$-series with $p=\frac12<1$, which diverges. Hence the set of convergence points is $\left(-1,1\right]$. $\blacksquare$

### Problem 7

(Problem 11.3-2-6) Find the set of convergence points of the power series $\sum_{n=2}^{+\infty}\frac{\left(-1\right)^n x^n}{4^n\ln n}$.

### Solution to Problem 7

By **Theorem 3.3**,

$$
\left|\frac{a_n}{a_{n+1}}\right|=\frac{4^{n+1}\ln\left(n+1\right)}{4^n\ln n}=4\frac{\ln\left(n+1\right)}{\ln n}\to 4,
$$

so the radius of convergence is $R=4$.

When $x=\pm 4$, the general terms at both endpoints do not satisfy the convergence condition, so the series diverges. Hence the set of convergence points is $\left(-4,4\right)$. $\blacksquare$

### Problem 8

(Problem 11.3-2-8) Find the set of convergence points of the power series

$$
\sum_{n=1}^{+\infty}\left(1+\frac12+\cdots+\frac1n\right)x^n
$$

.

### Solution to Problem 8

Let

$$
a_n=1+\frac12+\cdots+\frac1n=h_n.
$$

From $h_n-\ln n\to\gamma$ we know $h_n\to+\infty$ but $\frac{h_{n+1}}{h_n}\to 1$. By **Theorem 3.3**,

$$
\left|\frac{a_n}{a_{n+1}}\right|=\frac{h_n}{h_{n+1}}\to 1,
$$

so the radius of convergence is $R=1$.

When $x=1$, the series is $\sum h_n$, whose general term $h_n\to+\infty\ne 0$, so it diverges; when $x=-1$, the series is $\sum\left(-1\right)^n h_n$, whose general term likewise does not tend to zero, so it diverges. Hence the set of convergence points is $\left(-1,1\right)$. $\blacksquare$

### Problem 9

(Problem 11.3-2-10) Find the set of convergence points of the power series $\sum_{n=2}^{+\infty}\frac{\left(-1\right)^n\left(2x+3\right)^n}{n\ln n}$.

### Solution to Problem 9

Let $t=2x+3$. By **Theorem 3.3**, $\left|\frac{a_n}{a_{n+1}}\right|=\frac{\left(n+1\right)\ln\left(n+1\right)}{n\ln n}\to 1$, so the radius of convergence is $R=1$, i.e. $\left|t\right|<1$, which means $-1<2x+3<1$, i.e. $-2<x<-1$.

When $t=\pm 1$, the series diverges at both endpoints. Hence the set of convergence points is $\left(-2,-1\right)$. $\blacksquare$

### Problem 10

(Problem 11.3-3-1) Using the term-by-term differentiation of a power series, find the sum function of $\sum_{n=0}^{+\infty}\left(n+1\right)x^n$.

### Solution to Problem 10

We know $\sum_{n=0}^{\infty}x^{n+1}=\frac{x}{1-x}$ ($\left|x\right|<1$). By **Theorem 3.4** (Closed-Interval Uniform Convergence), we may differentiate term by term within the interval of convergence:

$$
\sum_{n=0}^{\infty}\left(n+1\right)x^n=\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{x}{1-x}\right)=\frac{1}{\left(1-x\right)^2}, \left|x\right|<1.

$$

$\blacksquare$
### Problem 11

(Problem 11.3-3-3) Find the sum function of $\sum_{n=1}^{+\infty}n^2x^n$.

### Solution to Problem 11

Using the decomposition $n^2=n\left(n-1\right)+n$, we have

$$
\sum_{n=1}^{\infty}n^2x^n=x\sum_{n=1}^{\infty}n\left(n-1\right)x^{n-1}+x\sum_{n=1}^{\infty}nx^{n-1}.
$$

By **Theorem 3.4**, differentiating term by term twice and once, we get

$$
\sum_{n=1}^{\infty}n\left(n-1\right)x^{n-1}=\frac{\mathrm{d}^2}{\mathrm{d}x^2}\left(\frac{1}{1-x}\right)=\frac{2}{\left(1-x\right)^3},
$$

$$
\sum_{n=1}^{\infty}nx^{n-1}=\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{1}{1-x}\right)=\frac{1}{\left(1-x\right)^2}.
$$

Hence

$$
\sum_{n=1}^{\infty}n^2x^n=x\cdot\frac{2}{\left(1-x\right)^3}+x\cdot\frac{1}{\left(1-x\right)^2}=\frac{x\left(1+x\right)}{\left(1-x\right)^3}, \left|x\right|<1.

$$

$\blacksquare$
### Problem 12

(Problem 11.3-3-5) Find the sum function of $\sum_{n=1}^{+\infty}\frac{x^n}{n\left(n+1\right)}$.

### Solution to Problem 12

Note that $\frac{1}{n\left(n+1\right)}=\frac1n-\frac{1}{n+1}$, so

$$
\sum_{n=1}^{\infty}\frac{x^n}{n\left(n+1\right)}=\sum_{n=1}^{\infty}\frac{x^n}{n}-\sum_{n=1}^{\infty}\frac{x^n}{n+1}.
$$

We know $\sum_{n=1}^{\infty}\frac{x^n}{n}=-\ln\left(1-x\right)$ ($\left|x\right|<1$), while

$$
\sum_{n=1}^{\infty}\frac{x^n}{n+1}=\frac1x\sum_{n=1}^{\infty}\frac{x^{n+1}}{n+1}=\frac1x\left(-\ln\left(1-x\right)-x\right).
$$

Subtracting the two gives

$$
\sum_{n=1}^{\infty}\frac{x^n}{n\left(n+1\right)}=-\ln\left(1-x\right)+\frac{\ln\left(1-x\right)}{x}+1=1-\frac{1-x}{x}\ln\left(1-x\right), 0<\left|x\right|<1.
$$

When $x=0$, the sum function is $0$ (extended by continuity). $\blacksquare$

### Problem 13

(Problem 11.3-3-7) Find the sum function of $\sum_{n=1}^{+\infty}\frac{x^n}{n}$.

### Solution to Problem 13

By **Theorem 3.4**, differentiating term by term within the interval of convergence:

$$
\frac{\mathrm{d}}{\mathrm{d}x}\left(\sum_{n=1}^{\infty}\frac{x^n}{n}\right)=\sum_{n=1}^{\infty}x^{n-1}=\frac{1}{1-x}.
$$

Integrating and noting that the sum is $0$ at $x=0$, we get

$$
\sum_{n=1}^{\infty}\frac{x^n}{n}=\int_0^x\frac{\mathrm{d}t}{1-t}=-\ln\left(1-x\right), \left|x\right|<1.

$$

$\blacksquare$
### Problem 14

(Problem 11.3-4) Prove that if the radius of convergence of $\sum_{n=0}^{+\infty}a_nx^n$ is $R$ ($0<R<+\infty$), then the radius of convergence of $\sum_{n=0}^{+\infty}a_nx^{2n}$ is $\sqrt R$.

### Solution to Problem 14

Let $y=x^2$. Then $\sum a_nx^{2n}=\sum a_ny^n$. The latter converges if and only if $\left|y\right|<R$ (by the definition of the radius of convergence), i.e. $\left|x^2\right|<R$, which means $\left|x\right|<\sqrt R$. When $\left|x\right|>\sqrt R$, $\left|y\right|>R$, and the series diverges. By **Theorem 3.2** (Cauchy's Formula), the radius of convergence of $\sum a_nx^{2n}$ is $\sqrt R$. $\blacksquare$

### Problem 15

(Problem 11.3-5) Let the radius of convergence of $\sum_{n=0}^{+\infty}a_nx^n$ be $R$ ($0<R<+\infty$). Prove that, for a given $A>\frac{1}{R}$, there exists $C>0$ such that $\left|a_n\right|\le CA^n$, $\forall n=1,2,\cdots$.

### Solution to Problem 15

From $A>\frac1R$ we get $\frac1A<R$. Choose $r$ such that $\frac1A<r<R$. Then the power series converges at $x=r$, so the general term $a_nr^n\to 0$ and is therefore bounded, i.e. there exists $M>0$ such that $\left|a_nr^n\right|\le M$, $\forall n$. Hence

$$
\left|a_n\right|\le M\cdot r^{-n}=M\left(\frac1r\right)^n.
$$

Since $\frac1r<A$, let $q=\frac{1/\left(rA\right)}{1}<1$. Then $\left(\frac1r\right)^n=A^n\left(\frac{1}{rA}\right)^n\le A^n$ (when $\frac{1}{rA}\le 1$), or more generally take $C=M\max\left(1,\frac{1}{rA}\right)$, to obtain $\left|a_n\right|\le CA^n$. $\blacksquare$
