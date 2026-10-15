# Assignment 39

> **Theorem 2.2** (Comparison Test) Let $\sum a_n$ and $\sum b_n$ be positive-term series, and suppose there is a natural number $N_0$ such that $a_n\le b_n$ ($n\ge N_0$). If $\sum b_n$ converges, then $\sum a_n$ converges; if $\sum a_n$ diverges, then $\sum b_n$ diverges.
>
> **Theorem 2.3** (Limit Form of the Comparison Test) Let $\sum a_n$ and $\sum b_n$ be positive-term series, $b_n\ne 0$, and suppose $\lim_{n\to\infty}\frac{a_n}{b_n}=l$. When $0<l<+\infty$, the two series converge or diverge together; when $l=0$ and $\sum b_n$ converges, $\sum a_n$ converges; when $l=+\infty$ and $\sum b_n$ diverges, $\sum a_n$ diverges.
>
> **Theorem 2.6** (d'Alembert's Ratio Test) Let $\sum a_n$ be a positive-term series, $a_n>0$. If $\lim_{n\to\infty}\frac{a_{n+1}}{a_n}=r$, then the series converges when $r<1$ and diverges when $r>1$.
>
> **Theorem 2.9** (Integral Test) Let $f\left(x\right)$ be positive and monotonically decreasing on $\left[1,+\infty\right)$. Then the series $\sum_{n=1}^{\infty}f\left(n\right)$ and the improper integral $\int_1^{+\infty}f\left(x\right)\,\mathrm{d}x$ converge or diverge together.

### Problem 1

(Problem 10.2-1-15) Discuss the convergence of the series $\sum_{n=1}^{\infty}\frac{\left(n!\right)^2}{\left(2n\right)!}$.

### Solution to Problem 1

Let $a_n=\frac{\left(n!\right)^2}{\left(2n\right)!}$. Then

$$
\frac{a_{n+1}}{a_n}=\frac{\left(\left(n+1\right)!\right)^2}{\left(2n+2\right)!}\cdot\frac{\left(2n\right)!}{\left(n!\right)^2}
=\frac{\left(n+1\right)^2}{\left(2n+2\right)\left(2n+1\right)}=\frac{n+1}{2\left(2n+1\right)}\to\frac14<1.
$$

By **Theorem 2.6** (d'Alembert's Ratio Test), this series converges. $\blacksquare$

### Problem 2

(Problem 10.2-1-18) Discuss the convergence of the series $\sum_{n=3}^{\infty}\frac{1}{n\left(\ln\ln n\right)^q}$ ($q>0$).

### Solution to Problem 2

By the hint, note that $\frac{\ln n}{\left(\ln\ln n\right)^q}\to+\infty$ (the logarithm to any power grows more slowly than $\ln n$), so there exists $N$ such that for $n\ge N$, $\left(\ln\ln n\right)^q<\ln n$, and hence

$$
\frac{1}{n\left(\ln\ln n\right)^q}>\frac{1}{n\ln n}.
$$

On the other hand, the series $\sum_{n=3}^{\infty}\frac{1}{n\ln n}$ diverges by **Theorem 2.9** (Integral Test), because

$$
\int_3^{+\infty}\frac{\mathrm{d}x}{x\ln x}=\ln\ln x\Big|_3^{+\infty}=+\infty.
$$

Then by **Theorem 2.2** (Comparison Test), since the larger one diverges, the smaller one diverges as well. Therefore, for any $q>0$, this series diverges. $\blacksquare$

### Problem 3

(Problem 10.2-2) Use the integral test to discuss the convergence of the series $\sum_{n=3}^{\infty}\frac{1}{n\ln^p n\left(\ln\ln n\right)^q}$ ($p>0,q>0$).

### Solution to Problem 3

Let $f\left(x\right)=\frac{1}{x\ln^p x\left(\ln\ln x\right)^q}$, which is positive and monotonically decreasing when $x$ is sufficiently large. Make the substitution $t=\ln x$, so that $\mathrm{d}t=\mathrm{d}x/x$. By **Theorem 2.9** (Integral Test), the original series and the integral

$$
\int_{\ln 3}^{+\infty}\frac{\mathrm{d}t}{t^p\left(\ln t\right)^q}
$$

converge or diverge together. We discuss four cases.

(i) When $p>1$, choose $p'$ such that $1<p'<p$. Since $\frac{t^{p'}}{t^p\left(\ln t\right)^q}=\frac{1}{t^{p-p'}\left(\ln t\right)^q}\to 0$, for sufficiently large $t$ we have $\frac{1}{t^p\left(\ln t\right)^q}\le\frac{1}{t^{p'}}$, and $\int^{+\infty}\frac{\mathrm{d}t}{t^{p'}}$ converges, so the original integral converges and the original series converges.

(ii) When $p<1$, since

$$
\frac{t}{t^p\left(\ln t\right)^q}=t^{1-p}/\left(\ln t\right)^q\to+\infty,
$$

for sufficiently large $t$ we have $\frac{1}{t^p\left(\ln t\right)^q}\ge\frac{1}{t}$, and $\int^{+\infty}\frac{\mathrm{d}t}{t}$ diverges, so the original series diverges.

(iii) When $p=1$ and $q>1$, make the substitution $u=\ln t$, so that $\mathrm{d}u=\mathrm{d}t/t$. The original integral becomes $\int^{+\infty}\frac{\mathrm{d}u}{u^q}$, which converges when $q>1$, so the original series converges.

(iv) When $p=1$ and $q\le 1$, similarly the original integral becomes $\int^{+\infty}\frac{\mathrm{d}u}{u^q}$, which diverges when $q\le 1$, so the original series diverges. $\blacksquare$

### Problem 4

(Problem 10.2-6) Suppose that

$$
\lim_{n\to\infty}na_n=l,0<l<+\infty.
$$

Prove that $\sum_{n=1}^{\infty}a_n^2$ converges, while $\sum_{n=1}^{\infty}a_n$ diverges.

### Solution to Problem 4

From $\lim_{n\to\infty}na_n=l$ we get $\lim_{n\to\infty}a_n=\frac{l}{n}$, i.e.

$$
\lim_{n\to\infty}\frac{a_n}{1/n}=l\in\left(0,+\infty\right).
$$

By **Theorem 2.3** (Limit Form of the Comparison Test), $\sum a_n$ and $\sum\frac1n$ diverge together, so $\sum a_n$ diverges.

Moreover,

$$
\lim_{n\to\infty}\frac{a_n^2}{1/n^2}=\lim_{n\to\infty}\left(na_n\right)^2=l^2\in\left(0,+\infty\right),
$$

and $\sum\frac{1}{n^2}$ is a $p$-series with $p=2>1$, which converges. Then by **Theorem 2.3**, $\sum a_n^2$ converges. $\blacksquare$

### Problem 5

(Problem 10.2-7) If both the series $\sum_{n=1}^{\infty}a_n^2$ and $\sum_{n=1}^{\infty}b_n^2$ converge, prove that each of the following series converges:
$$
\sum_{n=1}^{\infty}\left|a_nb_n\right|;\;\sum_{n=1}^{\infty}\left(a_n+b_n\right)^2;\;\sum_{n=1}^{\infty}\frac{\left|a_n\right|}{n}.
$$

### Solution to Problem 5

(1) From the inequality $2\left|a_nb_n\right|\le a_n^2+b_n^2$, we get

$$
\left|a_nb_n\right|\le\frac{a_n^2+b_n^2}{2}.
$$

By assumption, both $\sum a_n^2$ and $\sum b_n^2$ converge, so $\sum\frac{a_n^2+b_n^2}{2}$ converges. By **Theorem 2.2** (Comparison Test), $\sum\left|a_nb_n\right|$ converges.

(2) Expanding,

$$
\left(a_n+b_n\right)^2=a_n^2+2a_nb_n+b_n^2,
$$

and hence

$$
\left(a_n+b_n\right)^2\le a_n^2+2\left|a_nb_n\right|+b_n^2.
$$

The three series on the right are convergent by the assumption and by (1), respectively, so $\sum\left(a_n+b_n\right)^2$ converges by **Theorem 2.2**.

(3) From the inequality $2\frac{\left|a_n\right|}{n}\le a_n^2+\frac{1}{n^2}$, we get

$$
\frac{\left|a_n\right|}{n}\le\frac{a_n^2}{2}+\frac{1}{2n^2}.
$$

The two series on the right are convergent by the assumption and by the $p$-series ($p=2$), respectively, so again by **Theorem 2.2**, $\sum\frac{\left|a_n\right|}{n}$ converges. $\blacksquare$
