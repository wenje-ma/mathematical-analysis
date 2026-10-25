# Assignment 43

> **Theorem 2.2** (The Weierstrass M-Test) Suppose $\left|u_n\left(x\right)\right|\le a_n$ holds for all $x\in X$ and all sufficiently large $n$, and suppose $\sum a_n$ converges. Then the series of functions $\sum u_n\left(x\right)$ converges uniformly on $X$.
> 
> **Theorem 2.4** (Dirichlet's Test) In the series of functions $\sum a_n\left(x\right)b_n\left(x\right)$, suppose the sequence of partial sums of $\sum a_n\left(x\right)$ is uniformly bounded on $X$, $b_n\left(x\right)$ is monotone in $n$ for each $x\in X$, and $b_n\left(x\right)$ tends uniformly to zero on $X$. Then $\sum a_n\left(x\right)b_n\left(x\right)$ converges uniformly on $X$.
> 
> **Theorem 2.5** (Continuity of the Sum Function) Let $u_n\left(x\right)$ be continuous on an interval $X$, and suppose $\sum u_n\left(x\right)$ converges uniformly on $X$. Then its sum function $S\left(x\right)$ is continuous on $X$.
> 
> **Theorem 2.7** (Term-by-Term Differentiation Theorem) Let $\sum u_n\left(x\right)$ converge to $S\left(x\right)$ on $\left[a,b\right]$, let the $u_n\left(x\right)$ have continuous derivatives on $\left[a,b\right]$, and suppose $\sum u_n'\left(x\right)$ converges uniformly on $\left[a,b\right]$. Then $S\left(x\right)$ is differentiable on $\left[a,b\right]$ and $S'\left(x\right)=\sum u_n'\left(x\right)$.

### Problem 1

(Problem 11.2-1-2) Discuss the uniform convergence of the series $\sum_{n=1}^{+\infty}\frac{\left(-1\right)^{n+1}}{x^2+n}$ for $x\in\left(-\infty,+\infty\right)$.

### Solution to Problem 1

Let $a_n\left(x\right)=\left(-1\right)^{n+1}$ and $b_n\left(x\right)=\frac{1}{x^2+n}$. The partial sums $\sum_{k=1}^{N}a_k\left(x\right)$ oscillate between $-1$ and $0$ and are uniformly bounded. For each fixed $x$, $b_n\left(x\right)$ is monotonically decreasing in $n$; and

$$
\left|b_n\left(x\right)\right|\le\frac{1}{n}\to 0
$$

uniformly in $x\in\mathbb R$. By **Theorem 2.4** (Dirichlet's Test), this series converges uniformly on $\mathbb R$. $\blacksquare$

### Problem 2

(Problem 11.2-1-4) Discuss the uniform convergence of the series $\sum_{n=1}^{+\infty}\frac{x}{\left(1+\left(n-1\right)x\right)\left(1+nx\right)}$ for $x\in\left(-\infty,+\infty\right)$.

### Solution to Problem 2

Note that

$$
\frac{x}{\left(1+\left(n-1\right)x\right)\left(1+nx\right)}=\frac{1}{1+\left(n-1\right)x}-\frac{1}{1+nx},
$$

so the partial sums are

$$
S_N\left(x\right)=1-\frac{1}{1+Nx}.
$$

When $x> 0$, $S_N\left(x\right)\to 1$; when $x=0$, $S_N\left(0\right)=0$; when $x< 0$, $1+Nx$ eventually becomes $0$ or negative, so the series is undefined or diverges for $x< 0$. Hence the sum function is not continuous at $x=0$ (the right limit is $1$, while the function value is $0$). Since each term $\frac{x}{\left(1+\left(n-1\right)x\right)\left(1+nx\right)}$ is continuous on $\left(0,+\infty\right)$, by **Theorem 2.5** (Continuity of the Sum Function), if the series converged uniformly on $\left(0,+\infty\right)$ the sum function would have to be continuous, a contradiction. Thus this series does not converge uniformly on $\left(0,+\infty\right)$. $\blacksquare$

### Problem 3

(Problem 11.2-1-6) Discuss the uniform convergence of the series $\sum_{n=1}^{+\infty}\frac{1}{n^2+x^2}$ for $x\in\left[0,+\infty\right)$.

### Solution to Problem 3

For all $x\in\left[0,+\infty\right)$,

$$
\left|\frac{1}{n^2+x^2}\right|\le\frac{1}{n^2}=a_n,
$$

and $\sum\frac{1}{n^2}$ is a $p$-series with $p=2> 1$, which converges. By **Theorem 2.2** (The Weierstrass M-Test), this series converges uniformly on $\left[0,+\infty\right)$. $\blacksquare$

### Problem 4

(Problem 11.2-9) Discuss the uniform convergence of the series $\sum_{n=1}^{+\infty}\left(-1\right)^n\frac{n+x^2}{n^2}$:
(i) $x\in\left[a,b\right]$;

(ii) $x\in\left(-\infty,+\infty\right)$.

### Solution to Problem 4

(i) Let $a_n\left(x\right)=\left(-1\right)^n$ and $b_n\left(x\right)=\frac{n+x^2}{n^2}=\frac1n+\frac{x^2}{n^2}$. The partial sums $\sum_{k=1}^{N}\left(-1\right)^k$ are uniformly bounded. For each fixed $x$, $b_n\left(x\right)$ is monotonically decreasing in $n$ (since both $\frac1n$ and $\frac{x^2}{n^2}$ decrease). Moreover, for $x\in\left[a,b\right]$, $x^2\le C=\max\left(a^2,b^2\right)$, so

$$
0\le b_n\left(x\right)\le\frac1n+\frac{C}{n^2}\to 0
$$

uniformly in $x\in\left[a,b\right]$. By **Theorem 2.4** (Dirichlet's Test), the series converges uniformly on $\left[a,b\right]$.

(ii) On $\mathbb R$, the absolute value of the general term

$$
u_n\left(x\right)=\left(-1\right)^n\left(\frac1n+\frac{x^2}{n^2}\right)
$$

attains $\frac1n+\frac1n=\frac2n$ at $x=\sqrt n$, but $\sup_{x\in\mathbb R}\frac{x^2}{n^2}=+\infty$, so the general term does not tend uniformly to zero. By a corollary of **Theorem 2.1** (Cauchy Convergence Principle) (the uniform tending of the general term to zero is a necessary condition for uniform convergence), the series does not converge uniformly on $\mathbb R$. $\blacksquare$

### Problem 5

(Problem 11.2-10) Discuss the uniform convergence of the series $\sum_{n=1}^{+\infty}\left(-1\right)^{n-1}x^2e^{-nx^2}$ ($-\infty< x< +\infty$).

### Solution to Problem 5

Let $a_n\left(x\right)=\left(-1\right)^{n-1}$ and $b_n\left(x\right)=x^2e^{-nx^2}$. For each fixed $x$, $b_n\left(x\right)$ is monotonically decreasing in $n$ (since $e^{-nx^2}$ decreases). Moreover,

$$
\left|b_n\left(x\right)\right|=x^2e^{-nx^2}.
$$

Let $t=x^2\ge 0$. The maximum of $te^{-nt}$ in $t$ is attained at $t=\frac1n$, with maximum value $\frac1n e^{-1}=\frac{1}{en}\to 0$, and this estimate is uniform in $x$. Hence $b_n\left(x\right)$ tends uniformly to zero on $\mathbb R$. The partial sums $\sum_{k=1}^{N}\left(-1\right)^{k-1}$ are uniformly bounded. By **Theorem 2.4** (Dirichlet's Test), the series converges uniformly on $\mathbb R$. $\blacksquare$

### Problem 6

(Problem 11.2-11) Discuss the uniform convergence of the series $\sum_{n=1}^{+\infty}\frac{\sin x\cdot\sin nx}{\sqrt{n^2+x^2}}$ ($0\le x\le 2\pi$).

### Solution to Problem 6

Let $a_n\left(x\right)=\sin nx$ and $b_n\left(x\right)=\frac{\sin x}{\sqrt{n^2+x^2}}$. First prove that the product of $\sum_{k=1}^{N}a_k\left(x\right)$ and $\sin x$ is uniformly bounded on $\left[0,2\pi\right]$. From the formula

$$
\sum_{k=1}^{N}\sin kx=\frac{\cos\frac{x}{2}-\cos\left(Nx+\frac{x}{2}\right)}{2\sin\frac{x}{2}},
$$

multiplying both sides by $\sin x=2\sin\frac{x}{2}\cos\frac{x}{2}$, we get

$$
\sin x\sum_{k=1}^{N}\sin kx=\cos\frac{x}{2}\left(\cos\frac{x}{2}-\cos\left(Nx+\frac{x}{2}\right)\right).
$$

The absolute value of the right side does not exceed $2$, so $\sum_{k=1}^{N}\sin x\cdot\sin kx$ is uniformly bounded in $N$ and $x\in\left[0,2\pi\right]$.

Moreover, $b_n\left(x\right)=\frac{\sin x}{\sqrt{n^2+x^2}}\le\frac{1}{n}$, which tends uniformly to zero in $x$ and is monotonically decreasing in $n$ for fixed $x$. By **Theorem 2.4** (Dirichlet's Test), the original series converges uniformly on $\left[0,2\pi\right]$. $\blacksquare$

### Problem 7

(Problem 11.2-5) Prove that the function
$$
f\left(x\right)=\sum_{n=1}^{\infty}2^n\sin\frac{x}{3^n}
$$
has a continuous derivative everywhere on $\left(-\infty,+\infty\right)$.

### Solution to Problem 7

Each term $u_n\left(x\right)=2^n\sin\frac{x}{3^n}$ is continuously differentiable on $\mathbb R$. Formally differentiating term by term gives

$$
u_n'\left(x\right)=2^n\cdot\frac{1}{3^n}\cos\frac{x}{3^n}=\left(\frac23\right)^n\cos\frac{x}{3^n}.
$$

For all $x\in\mathbb R$,

$$
\left|u_n'\left(x\right)\right|\le\left(\frac23\right)^n,
$$

and $\sum\left(\frac23\right)^n$ is a convergent geometric series. By **Theorem 2.2** (The Weierstrass M-Test), $\sum u_n'\left(x\right)$ converges uniformly on $\mathbb R$.

Moreover, the original series $\sum u_n\left(x\right)$ converges for every $x$ (since

$$
\left|u_n\left(x\right)\right|\le 2^n\left|x/3^n\right|=\left|\frac{2x}{3}\right|
$$

is controlled afterwards by the ratio test). By **Theorem 2.7** (Term-by-Term Differentiation Theorem), $f\left(x\right)$ is differentiable on any closed interval $\left[a,b\right]$, and

$$
f'\left(x\right)=\sum_{n=1}^{\infty}\left(\frac23\right)^n\cos\frac{x}{3^n}.
$$

Each term on the right is continuous, and by the M-test it converges uniformly on any $\left[a,b\right]$, so by **Theorem 2.5** (Continuity of the Sum Function), $f'\left(x\right)$ is continuous. By the arbitrariness of $\left[a,b\right]$, $f\left(x\right)$ has a continuous derivative everywhere on $\mathbb R$. $\blacksquare$

### Problem 8

(Problem 11.2-6) Let $\zeta\left(x\right)=\sum_{n=1}^{\infty}\frac{1}{n^x}$ ($x> 1$). Prove that the derivative of $\zeta\left(x\right)$ exists, and give its expression.

### Solution to Problem 8

For any $x_0> 1$, choose $a$ such that $1< a< x_0$. On the interval $\left[a,+\infty\right)$, consider the formally term-by-term differentiated series:

$$
\sum_{n=1}^{\infty}\left(\frac{1}{n^x}\right)'=-\sum_{n=1}^{\infty}\frac{\ln n}{n^x}.
$$

For $x\ge a$,

$$
\left|\frac{\ln n}{n^x}\right|\le\frac{\ln n}{n^a}.
$$

Since $a> 1$, choose $\varepsilon> 0$ such that $a-\varepsilon> 1$. Then

$$
\frac{\ln n}{n^a}=\frac{\ln n}{n^\varepsilon}\cdot\frac{1}{n^{a-\varepsilon}}\le C\cdot\frac{1}{n^{a-\varepsilon}},
$$

and $\sum\frac{1}{n^{a-\varepsilon}}$ converges, so $\sum\frac{\ln n}{n^a}$ converges. By **Theorem 2.2** (The Weierstrass M-Test), the differentiated series converges uniformly on $\left[a,+\infty\right)$.

Moreover, the original series $\sum\frac{1}{n^x}$ converges when $x> 1$. By **Theorem 2.7** (Term-by-Term Differentiation Theorem), $\zeta\left(x\right)$ is differentiable on $\left[a,+\infty\right)$, and

$$
\zeta'\left(x\right)=-\sum_{n=1}^{\infty}\frac{\ln n}{n^x}.
$$

By the arbitrariness of $x_0> 1$, the derivative of $\zeta\left(x\right)$ exists on $\left(1,+\infty\right)$, with the expression above. $\blacksquare$
