# week31

> **Theorem 1.1 (Weierstrass M-Test)**
> 
> If $\left|f_n\left(x\right)-f\left(x\right)\right|\le M_n$ and $M_n\to0$, then the convergence is uniform.

> **Theorem 1.2 (Continuity of the Limit Function)**
> 
> If $\left\{f_n\right\}$ converges uniformly to $f$ and each $f_n$ is continuous, then $f$ is continuous.

> **Theorem 2.2 (Comparison Test)**
> 
> If $0\le a_n\le b_n$ and $\sum b_n$ converges, then $\sum a_n$ converges.

> **Theorem 2.3 (Limit Form of Comparison Test)**
> 
> If $\lim\frac{a_n}{b_n}=l\in\left(0,+\infty\right)$, then both series converge or both diverge.

> **Theorem 3.2 (Dirichlet's Test)**
> 
> If $\left\{b_n\right\}$ is monotone tending to $0$ and the partial sums of $\sum a_n$ are bounded, then $\sum a_nb_n$ converges.

> **Theorem 3.3 (Abel's Test)**
> 
> If $\left\{b_n\right\}$ is monotone and bounded, and $\sum a_n$ converges, then $\sum a_nb_n$ converges.

> **Theorem 4.1 (Relation between Infinite Products and Series)**
> 
> $\prod p_n$ converges iff $\sum\ln p_n$ converges, and $\prod p_n=\exp\left(\sum\ln p_n\right)$.

> **Theorem 4.2 (Same-Sign Infinite Products)**
> 
> If $\alpha_n\ge0$, then $\prod\left(1+\alpha_n\right)$ converges iff $\sum\alpha_n$ converges.

> **Theorem 4.4 (Absolute Convergence)**
> 
> $\prod\left(1+\alpha_n\right)$ converges absolutely iff $\sum\left|\alpha_n\right|$ converges.

## 10.3-2

Prove: $\sum\frac{\cos nx}{n^p}$ converges absolutely for $p> 1$ and conditionally for $0< p\le1$.

### Solution to 10.3-2

For $p> 1$, by comparison with $\sum\frac1{n^p}$. For $0< p\le1$, not absolutely convergent (since $\left|\cos nx\right|\ge\cos^2nx$), but convergent by Dirichlet's test. $\blacksquare$

## 10.3-4

Prove the Dirichlet series has a half-line domain of convergence.

### Solution to 10.3-4

By Abel's test applied to $\frac{a_n}{n^x}=\frac{a_n}{n^{x_0}}\cdot\frac1{n^{x-x_0}}$. $\blacksquare$

## 10.3-5

Prove: $S_{2n}=h_{2n}-h_n$, $S_{2n}\to\ln2$, and $\sum\frac{\left(-1\right)^{n-1}}n=\ln2$.

### Solution to 10.3-5

Direct computation and using $h_n=\ln n+\gamma+o\left(1\right)$. $\blacksquare$

## 10.4-1-2

Discuss $\prod\sqrt{\frac{n^2+1}{n^2-1}}$.

### Solution to 10.4-1-2

Converges by comparison with $\sum\frac1{n^2}$. $\blacksquare$

## 10.4-1-4

Discuss $\prod\left(1+\frac{x^n}{2^n}\right)$.

### Solution to 10.4-1-4

Converges for $\left|x\right|< 2$, diverges otherwise. $\blacksquare$

## 10.4-1-6

Discuss $\prod\cos\frac1n$.

### Solution to 10.4-1-6

Since $\ln\cos\frac1n\sim-\frac1{2n^2}$, converges. $\blacksquare$

## 10.4-1-8

Discuss $\prod\left(1+\frac1{\sqrt n}\right)$.

### Solution to 10.4-1-8

Diverges since $\sum\frac1{\sqrt n}$ diverges. $\blacksquare$

## 10.4-2

Prove: if $\sum\alpha_n^2$ converges, then $\prod\cos\alpha_n$ converges.

### Solution to 10.4-2

Since $\ln\cos\alpha_n\sim-\frac{\alpha_n^2}{2}$. $\blacksquare$

## 10.4-3

Prove: if $\sum\left|\alpha_n\right|$ converges, then $\prod\tan\left(\frac\pi4+\alpha_n\right)$ converges absolutely.

### Solution to 10.4-3

Since $\left|\tan\left(\frac\pi4+\alpha_n\right)-1\right|\sim2\left|\alpha_n\right|$. $\blacksquare$

## 10.4-5

Prove: if $\prod\left(1+\left|\alpha_n\right|\right)$ converges, then $\prod\left(1+\alpha_n\right)$ converges.

### Solution to 10.4-5

By absolute convergence. $\blacksquare$

## 11.1-1-1

Discuss $f_n\left(x\right)=\frac1{1+nx}$ on $\left(0,1\right)$.

### Solution to 11.1-1-1

Not uniformly convergent since $\sup\left|f_n\right|=1\not\to0$. $\blacksquare$

## 11.1-1-3

Discuss $f_n\left(x\right)=\frac{\sin\left(nx+n\right)}n$ on $\mathbb R$.

### Solution to 11.1-1-3

Uniformly convergent by the M-test. $\blacksquare$

## 11.1-1-5

Discuss $f_n\left(x\right)=nxe^{-nx^2}$ on $\left[0,1\right]$.

### Solution to 11.1-1-5

Not uniformly convergent since $\sup\left|f_n\right|\to\infty$. $\blacksquare$

## 11.1-2

Prove the interchange of limits.

### Solution to 11.1-2

Using the Cauchy criterion and triangle inequality. $\blacksquare$
