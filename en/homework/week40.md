# Assignment 40

> **Theorem 3.2** (Dirichlet's Test) Let the sequence $\left\{b_n\right\}$ be monotonically tending to zero, and suppose the sequence of partial sums of the series $\sum a_n$ is bounded. Then the series $\sum a_nb_n$ converges.
> 
> **Theorem 3.3** (Abel's Test) Let the sequence $\left\{b_n\right\}$ be monotone and bounded, and suppose the series $\sum a_n$ converges. Then the series $\sum a_nb_n$ converges.

### Problem 1

(Problem 10.3-2) Prove that $\sum_{n=1}^{+\infty}\frac{\cos nx}{n^p}$ ($0< x< 2\pi$) converges absolutely when $p> 1$, and converges conditionally when $0< p\le 1$.

### Solution to Problem 1

(1) When $p> 1$, $\left|\frac{\cos nx}{n^p}\right|\le\frac{1}{n^p}$, and $\sum\frac{1}{n^p}$ is a $p$-series with $p> 1$, which converges. By **Theorem 2.2** (Comparison Test) of the previous chapter, $\sum\left|\frac{\cos nx}{n^p}\right|$ converges, so the original series converges absolutely.

(2) When $0< p\le 1$, first prove that it does not converge absolutely. Note that

$$
\left|\cos nx\right|\ge\cos^2 nx=\frac{1+\cos 2nx}{2},
$$

so

$$
\frac{\left|\cos nx\right|}{n^p}\ge\frac{1}{2n^p}+\frac{\cos 2nx}{2n^p}.
$$

The first term on the right, $\sum\frac{1}{2n^p}$, diverges when $p\le 1$, while the second term $\sum\frac{\cos 2nx}{2n^p}$ itself converges (see below); hence if $\sum\frac{\left|\cos nx\right|}{n^p}$ were to converge, it would force $\sum\frac{1}{2n^p}$ to converge, a contradiction. Thus the original series does not converge absolutely.

Now prove that the original series converges. For $0< x< 2\pi$, we have

$$
\sum_{n=1}^{N}\cos nx=\frac{\sin\left(Nx+\frac{x}{2}\right)}{2\sin\frac{x}{2}}-\frac12,
$$

and since $\sin\frac{x}{2}\ne 0$ and is bounded, the sequence of partial sums of $\sum\cos nx$ is bounded. Moreover, $\frac{1}{n^p}$ is monotonically tending to zero when $p> 0$. By **Theorem 3.2** (Dirichlet's Test), $\sum\frac{\cos nx}{n^p}$ converges. In summary, when $0< p\le 1$ the original series converges conditionally. $\blacksquare$

### Problem 2

(Problem 10.3-4) The series $\sum_{n=1}^{+\infty}\frac{a_n}{n^x}$ is called a Dirichlet series. Prove that if $\sum_{n=1}^{\infty}\frac{a_n}{n^{x_0}}$ converges (diverges), then for $x> x_0$ ($x< x_0$), the series $\sum_{n=1}^{\infty}\frac{a_n}{n^x}$ also converges (diverges).

### Solution to Problem 2

First prove the convergent case. Let $x> x_0$, and write

$$
\frac{a_n}{n^x}=\frac{a_n}{n^{x_0}}\cdot\frac{1}{n^{x-x_0}}.
$$

By assumption, $\sum\frac{a_n}{n^{x_0}}$ converges. Moreover, $x-x_0> 0$, so the sequence $\left\{\frac{1}{n^{x-x_0}}\right\}$ is monotonically decreasing to zero, and hence monotone and bounded. By **Theorem 3.3** (Abel's Test), $\sum\frac{a_n}{n^x}$ converges.

Now prove the divergent case. Let $x< x_0$ and suppose $\sum\frac{a_n}{n^{x_0}}$ diverges. Assume for contradiction that $\sum\frac{a_n}{n^x}$ converges. Set $y=x_0-x> 0$. Then

$$
\frac{a_n}{n^{x_0}}=\frac{a_n}{n^x}\cdot\frac{1}{n^y}.
$$

By the contradictory assumption, $\sum\frac{a_n}{n^x}$ converges, while $\left\{\frac{1}{n^y}\right\}$ is monotone and bounded (decreasing to zero). By **Theorem 3.3** (Abel's Test), $\sum\frac{a_n}{n^{x_0}}$ should converge, contradicting the assumption. Therefore $\sum\frac{a_n}{n^x}$ diverges. $\blacksquare$

### Problem 3

(Problem 10.3-5) Let

$$
h_n=\sum_{k=1}^{n}\frac{1}{k},S_n=\sum_{k=1}^{n}\frac{\left(-1\right)^{k-1}}{k}.
$$
(1) Prove that $S_{2n}=h_{2n}-h_n$;

(2) Using $h_n-\ln n\to\gamma$ ($n\to\infty$), prove that $S_{2n}\to\ln 2$ ($n\to\infty$);

(3) Prove that $\sum_{n=1}^{+\infty}\frac{\left(-1\right)^{n-1}}{n}=\ln 2$.

### Solution to Problem 3

(1) Directly compute the even-term partial sum:

$$
\begin{aligned}
S_{2n}&=1-\frac12+\frac13-\frac14+\cdots+\frac{1}{2n-1}-\frac{1}{2n}\\
&=\left(1+\frac12+\frac13+\cdots+\frac{1}{2n}\right)-2\left(\frac12+\frac14+\cdots+\frac{1}{2n}\right)\\
&=h_{2n}-\left(1+\frac12+\cdots+\frac1n\right)=h_{2n}-h_n.
\end{aligned}
$$

(2) By assumption, $h_n=\ln n+\gamma+o\left(1\right)$, so

$$
S_{2n}=h_{2n}-h_n=\left(\ln\left(2n\right)+\gamma+o\left(1\right)\right)-\left(\ln n+\gamma+o\left(1\right)\right)=\ln 2+o\left(1\right),
$$

i.e. $S_{2n}\to\ln 2$ ($n\to\infty$).

(3) Now look at the odd-term partial sum:

$$
S_{2n-1}=S_{2n}+\frac{1}{2n}\to\ln 2+0=\ln 2.
$$

Both the even-term and odd-term partial sums tend to the same limit $\ln 2$, so $\lim_{n\to\infty}S_n=\ln 2$, i.e.

$$
\sum_{n=1}^{\infty}\frac{\left(-1\right)^{n-1}}{n}=\ln 2.

$$

$\blacksquare$