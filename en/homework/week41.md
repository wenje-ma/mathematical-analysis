# Assignment 41

> **Theorem 4.1** (Relation Between Infinite Products and Series) Let $p_n> 0$ ($n=1,2,\dots$). Then the infinite product $\prod_{n=1}^{\infty}p_n$ converges if and only if the series $\sum_{n=1}^{\infty}\ln p_n$ converges, and in that case
> $$
> \prod_{n=1}^{\infty}p_n=\exp\left(\sum_{n=1}^{\infty}\ln p_n\right).
> $$
> 
> **Theorem 4.2** (Infinite Products with Terms of the Same Sign) Let $\alpha_n\ge 0$ (or $\alpha_n\le 0$). Then the infinite product $\prod_{n=1}^{\infty}\left(1+\alpha_n\right)$ converges if and only if the series $\sum_{n=1}^{\infty}\alpha_n$ converges.
> 
> **Theorem 4.4** (Absolute Convergence) Let $\alpha_n\ne -1$. Then the infinite product $\prod_{n=1}^{\infty}\left(1+\alpha_n\right)$ converges absolutely if and only if the series $\sum_{n=1}^{\infty}\left|\alpha_n\right|$ converges.

### Problem 1

(Problem 10.4-1-2) Discuss the convergence of the infinite product $\prod_{n=2}^{\infty}\sqrt{\frac{n^2+1}{n^2-1}}$.

### Solution to Problem 1

Rewrite the general term:

$$
\sqrt{\frac{n^2+1}{n^2-1}}=\left(1+\frac{2}{n^2-1}\right)^{1/2}.
$$

Let $\alpha_n=\frac{2}{n^2-1}> 0$. Since $\alpha_n\sim\frac{2}{n^2}$, and $\sum\frac{1}{n^2}$ is a $p$-series with $p=2> 1$, which converges, by **Theorem 2.3** (Limit Form of the Comparison Test) of the previous chapter, $\sum\alpha_n$ converges. By **Theorem 4.2** (Infinite Products with Terms of the Same Sign), $\prod\left(1+\alpha_n\right)$ converges. Then by **Theorem 4.1**,

$$
\ln\sqrt{\left(n^2+1\right)/\left(n^2-1\right)}=\frac12\ln\left(1+\alpha_n\right)
$$

the resulting series converges, so the original infinite product converges. $\blacksquare$

### Problem 2

(Problem 10.4-1-4) Discuss the convergence of the infinite product $\prod_{n=1}^{\infty}\left(1+\frac{x^n}{2^n}\right)$.

### Solution to Problem 2

Let $\alpha_n=\frac{x^n}{2^n}=\left(\frac{x}{2}\right)^n$. When $\left|x\right|< 2$, $\left|x/2\right|< 1$, and $\sum\alpha_n$ is a convergent geometric series, so by **Theorem 4.2** (Infinite Products with Terms of the Same Sign), the original infinite product converges.

When $\left|x\right|> 2$, $\left|\alpha_n\right|=\left|x/2\right|^n$ does not tend to zero, and hence the general term $1+\alpha_n$ of $\prod\left(1+\alpha_n\right)$ does not tend to $1$, so the infinite product diverges.

When $x=2$, $\alpha_n=1$ and $1+\alpha_n=2$, so the partial products tend to $+\infty$ and it diverges. When $x=-2$, $\alpha_n=\left(-1\right)^n$ and $1+\alpha_n$ alternates between $0$ and $2$, so the partial products are $0$ and do not tend to a nonzero finite limit, and it diverges.

In summary, the original infinite product converges if and only if $x\in\left(-2,2\right)$. $\blacksquare$

### Problem 3

(Problem 10.4-1-6) Discuss the convergence of the infinite product $\prod_{n=1}^{\infty}\cos\frac{1}{n}$.

### Solution to Problem 3

Let $p_n=\cos\frac1n> 0$. By **Theorem 4.1**, examine $\sum\ln\cos\frac1n$. When $x\to 0$,

$$
\ln\cos x=\ln\left(1-2\sin^2\left(x/2\right)\right)\sim -2\sin^2\left(x/2\right)\sim-\frac{x^2}{2}.
$$

Hence $\ln\cos\frac1n\sim-\frac{1}{2n^2}$. Since $\sum\frac{1}{n^2}$ converges, by **Theorem 2.3** (Limit Form of the Comparison Test) of the previous chapter, $\sum\ln\cos\frac1n$ converges. By **Theorem 4.1**, the original infinite product converges. $\blacksquare$

### Problem 4

(Problem 10.4-1-8) Discuss the convergence of the infinite product $\prod_{n=1}^{\infty}\left(1+\frac{1}{\sqrt n}\right)$.

### Solution to Problem 4

Let $\alpha_n=\frac{1}{\sqrt n}> 0$. Since $\sum\frac{1}{\sqrt n}$ is a $p$-series with $p=\frac12< 1$, it diverges. By **Theorem 4.2** (Infinite Products with Terms of the Same Sign), the original infinite product diverges. $\blacksquare$

### Problem 5

(Problem 10.4-2) Let $0< \alpha_n< \frac{\pi}{2}$ and let $\sum_{n=1}^{\infty}\alpha_n^2$ converge. Prove that $\prod_{n=1}^{\infty}\cos\alpha_n$ converges.

### Solution to Problem 5

By **Theorem 4.1**, it suffices to prove that $\sum\ln\cos\alpha_n$ converges. When $\alpha\to 0$,

$$
\ln\cos\alpha=\ln\left(1-2\sin^2\left(\alpha/2\right)\right)\sim-2\sin^2\left(\alpha/2\right)\sim-\frac{\alpha^2}{2}.
$$

Hence

$$
\lim_{n\to\infty}\frac{\ln\cos\alpha_n}{\alpha_n^2}=-\frac12.
$$

By **Theorem 2.3** (Limit Form of the Comparison Test) of the previous chapter, $\sum\ln\cos\alpha_n$ and $\sum\alpha_n^2$ converge together. By assumption, $\sum\alpha_n^2$ converges, so $\sum\ln\cos\alpha_n$ converges. Then by **Theorem 4.1**, $\prod\cos\alpha_n$ converges. $\blacksquare$

### Problem 6

(Problem 10.4-3) Let $\left|\alpha_n\right|< \frac{\pi}{4}$ and suppose $\sum_{n=1}^{\infty}\left|\alpha_n\right|$ converges. Prove that $\prod_{n=1}^{\infty}\tan\left(\frac{\pi}{4}+\alpha_n\right)$ converges absolutely.

### Solution to Problem 6

By **Theorem 4.4**, it suffices to prove that $\sum\left|\tan\left(\frac{\pi}{4}+\alpha_n\right)-1\right|$ converges. Computing:

$$
\tan\left(\frac{\pi}{4}+\alpha_n\right)=\frac{1+\tan\alpha_n}{1-\tan\alpha_n},
$$

so

$$
\tan\left(\frac{\pi}{4}+\alpha_n\right)-1=\frac{2\tan\alpha_n}{1-\tan\alpha_n}.
$$

Since $\alpha_n\to 0$ (from the convergence of $\sum\left|\alpha_n\right|$), $\tan\alpha_n\sim\alpha_n$, and $1-\tan\alpha_n\to 1$, and hence

$$
\left|\tan\left(\frac{\pi}{4}+\alpha_n\right)-1\right|\sim 2\left|\alpha_n\right|.
$$

By **Theorem 2.3** (Limit Form of the Comparison Test) of the previous chapter, $\sum\left|\tan\left(\frac{\pi}{4}+\alpha_n\right)-1\right|$ and $\sum\left|\alpha_n\right|$ converge together. By assumption the latter converges, so by **Theorem 4.4**, the original infinite product converges absolutely. $\blacksquare$

### Problem 7

(Problem 10.4-5) Let $\alpha_n\ne -1$ ($n=1,2,\dots$). Prove that if $\prod_{n=1}^{\infty}\left(1+\left|\alpha_n\right|\right)$ converges, then $\prod_{n=1}^{\infty}\left(1+\alpha_n\right)$ converges.

### Solution to Problem 7

Since $\left|\alpha_n\right|\ge 0$, by **Theorem 4.2** (Infinite Products with Terms of the Same Sign), the convergence of $\prod\left(1+\left|\alpha_n\right|\right)$ implies the convergence of $\sum\left|\alpha_n\right|$. Then by **Theorem 4.4** (Absolute Convergence), $\prod\left(1+\alpha_n\right)$ converges absolutely, and hence must converge. $\blacksquare$
