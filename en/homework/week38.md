# Assignment 38

> **Definition** (Convergence of a Series) Given a sequence $\left\{a_n\right\}$, form the partial sums $S_n=\sum_{k=1}^{n}a_k$. If $\lim_{n\to\infty}S_n=S$ exists and is finite, then the series $\sum_{n=1}^{\infty}a_n$ is said to converge, and $S$ is called its sum; otherwise the series is said to diverge.
> 
> **Theorem 1.1** (Necessary Condition for a Convergent Series) If the series $\sum_{n=1}^{\infty}a_n$ converges, then $\lim_{n\to\infty}a_n=0$.

### Problem 1

(Problem 10.1-1) Prove that the geometric series
$$
a_0+a_0q+a_0q^2+\cdots+a_0q^n+\cdots\left(a_0\ne 0\right)
$$
converges when $\left|q\right|< 1$, with $a_0+a_0q+\cdots=\frac{a_0}{1-q}$. When $\left|q\right|\ge 1$, the above series diverges.

### Solution to Problem 1

The partial sum of the first $n+1$ terms of this series is

$$
S_n=a_0+a_0q+\cdots+a_0q^n=a_0\cdot\frac{1-q^{n+1}}{1-q}, q\ne 1.
$$

When $\left|q\right|< 1$, $\lim_{n\to\infty}q^{n+1}=0$, so by **Definition** (Convergence of a Series),

$$
\lim_{n\to\infty}S_n=\frac{a_0}{1-q},
$$

and the series converges with sum $\frac{a_0}{1-q}$.

When $q=1$, $S_n=a_0\left(n+1\right)\to\infty$ ($a_0\ne 0$), so the series diverges. When $q=-1$, $S_n$ oscillates between $a_0$ and $0$ and does not converge. When $\left|q\right|> 1$, the general term $a_0q^n$ does not tend to $0$, so by **Theorem 1.1** (Necessary Condition for a Convergent Series), the series diverges. $\blacksquare$

### Problem 2

(Problem 10.1-2-1) Discuss the convergence or divergence of the series $\sum_{n=1}^{+\infty}\left(\sqrt{n+1}-\sqrt{n}\right)$.

### Solution to Problem 2

Its partial sums are

$$
S_N=\sum_{n=1}^{N}\left(\sqrt{n+1}-\sqrt{n}\right)=\sqrt{N+1}-1.
$$

When $N\to\infty$, $S_N\to+\infty$, and the limit has no finite value, so by **Definition** (Convergence of a Series), this series diverges. $\blacksquare$

### Problem 3

(Problem 10.1-2-2) Discuss the convergence or divergence of the series $\sum_{n=1}^{+\infty}\frac{1}{\left(2n-1\right)\left(2n+1\right)}$.

### Solution to Problem 3

Note that

$$
\frac{1}{\left(2n-1\right)\left(2n+1\right)}=\frac{1}{2}\left(\frac{1}{2n-1}-\frac{1}{2n+1}\right),
$$

so the partial sums are

$$
S_N=\frac{1}{2}\sum_{n=1}^{N}\left(\frac{1}{2n-1}-\frac{1}{2n+1}\right)=\frac{1}{2}\left(1-\frac{1}{2N+1}\right).
$$

When $N\to\infty$, $S_N\to\frac{1}{2}$, so by **Definition** (Convergence of a Series), this series converges with sum $\frac{1}{2}$. $\blacksquare$

### Problem 4

(Problem 10.1-2-3) Discuss the convergence or divergence of the series $\sum_{n=1}^{+\infty}\ln\frac{n}{n+5}$.

### Solution to Problem 4

The general term is $\ln n-\ln\left(n+5\right)$, so the partial sums are

$$
\begin{aligned}
S_N&=\sum_{n=1}^{N}\left(\ln n-\ln\left(n+5\right)\right)\\
&=\ln\left(1\cdot 2\cdot 3\cdot 4\cdot 5\right)-\ln\left(\left(N+1\right)\left(N+2\right)\left(N+3\right)\left(N+4\right)\left(N+5\right)\right).
\end{aligned}
$$

When $N\to\infty$, the argument of the latter logarithm tends to $+\infty$, and hence $S_N\to-\infty$, so the limit has no finite value. Thus by **Definition** (Convergence of a Series), this series diverges. $\blacksquare$

### Problem 5

(Problem 10.1-2-7) Discuss the convergence or divergence of the series $\sum_{n=1}^{+\infty}\cos^2\frac{\pi}{n}$.

### Solution to Problem 5

When $n\to\infty$, $\frac{\pi}{n}\to 0$, so

$$
\cos^2\frac{\pi}{n}\to\cos^2 0=1\ne 0.
$$

By **Theorem 1.1** (Necessary Condition for a Convergent Series), the general term does not tend to zero, so this series diverges. $\blacksquare$

### Problem 6

(Problem 10.1-2-8) Discuss the convergence or divergence of the series $\sum_{n=1}^{+\infty}\arctan\frac{1}{2n^2}$.

### Solution to Problem 6

For $x\ge 0$, $\arctan x\le x$, so

$$
0\le\arctan\frac{1}{2n^2}\le\frac{1}{2n^2}.
$$

Moreover, when $n\ge 2$,

$$
\frac{1}{n^2}\le\frac{1}{n\left(n-1\right)}=\frac{1}{n-1}-\frac{1}{n},
$$

and hence

$$
\sum_{n=2}^{N}\frac{1}{n^2}\le\sum_{n=2}^{N}\left(\frac{1}{n-1}-\frac{1}{n}\right)=1-\frac{1}{N}< 1.
$$

The partial sums of the positive-term series $\sum\frac{1}{2n^2}$ are bounded, so it converges. Furthermore,

$$
0\le\sum_{n=1}^{N}\arctan\frac{1}{2n^2}\le\sum_{n=1}^{N}\frac{1}{2n^2}< \frac12,
$$

so the partial sums of $\sum\arctan\frac{1}{2n^2}$ are monotonically increasing and bounded above; by the completeness of the real numbers (**Proposition 1.5** of Chapter 1) its limit exists and is finite, and hence by **Definition** (Convergence of a Series), this series converges. $\blacksquare$
