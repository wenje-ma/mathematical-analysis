# week30

> **Theorem 1.1 (Necessary Condition for Convergence)**
> 
> If $\sum a_n$ converges, then $\lim_{n\to\infty}a_n=0$.

> **Theorem 2.2 (Comparison Test)**
> 
> If $0\le a_n\le b_n$ and $\sum b_n$ converges, then $\sum a_n$ converges.

> **Theorem 2.3 (Limit Form of Comparison Test)**
> 
> If $\lim\frac{a_n}{b_n}=l\in\left(0,+\infty\right)$, then both series converge or both diverge.

> **Theorem 2.6 (d'Alembert's Ratio Test)**
> 
> If $\lim\frac{a_{n+1}}{a_n}=r< 1$, the series converges; if $r> 1$, it diverges.

> **Theorem 2.9 (Integral Test)**
> 
> If $f$ is positive and decreasing on $\left[1,+\infty\right)$, then $\sum f\left(n\right)$ and $\int_1^\infty f\left(x\right)\,\mathrm dx$ have the same convergence behavior.

## 9.5-1

Find div and rot.

### Solution to 9.5-1

(1) $\operatorname{div}\boldsymbol F=5-2x$, $\operatorname{rot}\boldsymbol F=\left(0,0,-2y\right)$.

(2) $\operatorname{div}\boldsymbol F=10x+2y+2z$, $\operatorname{rot}\boldsymbol F=\left(0,0,0\right)$. $\blacksquare$

## 9.5-2

Prove: $\operatorname{div}\left(\Phi\boldsymbol F\right)=\Phi\operatorname{div}\boldsymbol F+\boldsymbol F\cdot\operatorname{grad}\Phi$.

### Solution to 9.5-2

By the product rule for divergence. $\blacksquare$

## 9.5-3

Prove: $\operatorname{rot}\left(\Phi\boldsymbol F\right)=\Phi\operatorname{rot}\boldsymbol F+\operatorname{grad}\Phi\times\boldsymbol F$.

### Solution to 9.5-3

By component-wise computation. $\blacksquare$

## 9.5-4

Prove: $\operatorname{rot}\left(\operatorname{grad}\Phi\right)=0$.

### Solution to 9.5-4

Mixed partial derivatives commute. $\blacksquare$

## 9.5-5

Prove: $\operatorname{div}\left(\operatorname{rot}\boldsymbol F\right)=0$.

### Solution to 9.5-5

Mixed partial derivatives commute. $\blacksquare$

## 10.1-1

Prove the geometric series converges for $\left|q\right|< 1$ and diverges otherwise.

### Solution to 10.1-1

Partial sums $S_n=a_0\frac{1-q^{n+1}}{1-q}$. For $\left|q\right|< 1$, $S_n\to\frac{a_0}{1-q}$. For $\left|q\right|\ge1$, by **Theorem 1.1 (Necessary Condition for Convergence)**, the series diverges. $\blacksquare$

## 10.1-2-1

Discuss $\sum\left(\sqrt{n+1}-\sqrt n\right)$.

### Solution to 10.1-2-1

$S_N=\sqrt{N+1}-1\to+\infty$. Diverges. $\blacksquare$

## 10.1-2-2

Discuss $\sum\frac1{\left(2n-1\right)\left(2n+1\right)}$.

### Solution to 10.1-2-2

Telescoping gives $S_N\to\frac12$. Converges. $\blacksquare$

## 10.1-2-3

Discuss $\sum\ln\frac n{n+5}$.

### Solution to 10.1-2-3

$S_N\to-\infty$. Diverges. $\blacksquare$

## 10.1-2-7

Discuss $\sum\cos^2\frac\pi n$.

### Solution to 10.1-2-7

The general term tends to $1\ne0$. By **Theorem 1.1 (Necessary Condition for Convergence)**, diverges. $\blacksquare$

## 10.1-2-8

Discuss $\sum\arctan\frac1{2n^2}$.

### Solution to 10.1-2-8

Since $0\le\arctan\frac1{2n^2}\le\frac1{2n^2}$ and $\sum\frac1{n^2}$ converges, the series converges. $\blacksquare$

## 10.2-1-15

Discuss $\sum\frac{\left(n!\right)^2}{\left(2n\right)!}$.

### Solution to 10.2-1-15

$\frac{a_{n+1}}{a_n}\to\frac14< 1$. Converges by ratio test. $\blacksquare$

## 10.2-1-18

Discuss $\sum\frac1{n\left(\ln\ln n\right)^q}$.

### Solution to 10.2-1-18

Since $\frac1{n\left(\ln\ln n\right)^q}> \frac1{n\ln n}$ and $\sum\frac1{n\ln n}$ diverges by the integral test, the series diverges. $\blacksquare$

## 10.2-2

Discuss $\sum\frac1{n\ln^p n\left(\ln\ln n\right)^q}$.

### Solution to 10.2-2

Converges if $p> 1$, or $p=1$ and $q> 1$. Diverges otherwise. $\blacksquare$

## 10.2-6

Prove: if $\lim na_n=l\in\left(0,+\infty\right)$, then $\sum a_n^2$ converges but $\sum a_n$ diverges.

### Solution to 10.2-6

By the limit comparison test with $\frac1n$ and $\frac1{n^2}$. $\blacksquare$

## 10.2-7

Prove: if $\sum a_n^2$ and $\sum b_n^2$ converge, then $\sum\left|a_nb_n\right|$, $\sum\left(a_n+b_n\right)^2$, and $\sum\frac{\left|a_n\right|}{n}$ all converge.

### Solution to 10.2-7

Using $2\left|a_nb_n\right|\le a_n^2+b_n^2$ and the comparison test. $\blacksquare$
