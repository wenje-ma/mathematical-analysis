# Assignment 3

> **Definition** (Limit of a Sequence) Let $\left\{a_n\right\}$ be a given sequence. If there exists a real number $l$ such that, for any given positive number $\varepsilon$, no matter how small, there is a natural number $N$ such that $\left|a_n-l\right|< \varepsilon$ whenever $n> N$, then $a_n$ is said to have limit $l$, denoted $\lim\limits_{n\to\infty}a_n=l$.

> **Example 3.3** (The $n$-th Root of a Positive Number Tends to $1$) Let $a$ be any positive number. Then $\lim\limits_{n\to\infty}a^{1/n}=1$.

> **Theorem 3.1** (Arithmetic of Limits) Let $\left\{a_n\right\}$ and $\left\{b_n\right\}$ both have limits, their limits being $l_1$ and $l_2$, respectively. Then $\lim\left(a_n\pm b_n\right)=l_1\pm l_2$, $\lim\left(a_n\cdot b_n\right)=l_1\cdot l_2$, and when $l_2\ne0$, $\lim\frac{a_n}{b_n}=\frac{l_1}{l_2}$.

> **Theorem 3.2** (Completeness of the Real Number Field) Let $\left\{a_n\right\}$ be a monotonically increasing sequence of real numbers bounded above. Then there exists $l\in\mathbb R$ such that $\left\{a_n\right\}$ has limit $l$. In short, every monotonically increasing sequence bounded above has a limit.

### Problem 1

(Problem 1.3-1-2) Prove, using the $\varepsilon$-$N$ language, that $\lim\limits_{n\to\infty}\frac{2n-5}{3n+100}=\frac23$.

### Solution to Problem 1

Rewrite the general term as

$$
\frac{2n-5}{3n+100}=\frac{2-5/n}{3+100/n}.
$$

As $n\to\infty$, $5/n\to0$ and $100/n\to0$ (by **Definition** (Limit of a Sequence), for any $\varepsilon> 0$, take $N> 5/\varepsilon$ and then $\left|5/n\right|< \varepsilon$). By **Theorem 3.1** (Arithmetic of Limits),

$$
\lim_{n\to\infty}\frac{2n-5}{3n+100}=\frac{\lim\left(2-5/n\right)}{\lim\left(3+100/n\right)}=\frac23.

$$

$\blacksquare$
### Problem 2

(Problem 1.3-1-4) Prove, using the $\varepsilon$-$N$ language, that $\lim\limits_{n\to\infty}\frac{n!}{n^n}=0$.

### Solution to Problem 2

For $n\ge1$,

$$
\frac{n!}{n^n}=\frac{1\cdot2\cdots n}{n\cdot n\cdots n}=\frac1n\cdot\frac2n\cdots\frac{n-1}{n}\cdot1\le\frac1n.
$$

Given any $\varepsilon> 0$, take $N=\left[\frac1\varepsilon\right]+1$. Then when $n> N$,

$$
\left|\frac{n!}{n^n}-0\right|\le\frac1n< \varepsilon.
$$

By **Definition** (Limit of a Sequence), $\lim\limits_{n\to\infty}\frac{n!}{n^n}=0$. $\blacksquare$

### Problem 3

(Problem 1.3-1-6) Prove, using the $\varepsilon$-$N$ language, that $\lim\limits_{n\to\infty}\frac{n^2+1}{2n^2-7n}=\frac12$.

### Solution to Problem 3

Rewrite the general term as

$$
\frac{n^2+1}{2n^2-7n}=\frac{1+1/n^2}{2-7/n}.
$$

As $n\to\infty$, $1/n^2\to0$ and $7/n\to0$. By **Theorem 3.1** (Arithmetic of Limits),

$$
\lim_{n\to\infty}\frac{n^2+1}{2n^2-7n}=\frac{\lim\left(1+1/n^2\right)}{\lim\left(2-7/n\right)}=\frac12.

$$

$\blacksquare$
### Problem 4

(Problem 1.3-1-8) Prove, using the $\varepsilon$-$N$ language, that

$$
\lim\limits_{n\to\infty}\left(\frac1{\left(n+1\right)^{3/2}}+\cdots+\frac1{\left(2n\right)^{3/2}}\right)=0.
$$

### Solution to Problem 4

This expression has $n$ terms in total, each satisfying $\frac1{\left(n+k\right)^{3/2}}\le\frac1{n^{3/2}}$ ($1\le k\le n$). Hence

$$
0\le\frac1{\left(n+1\right)^{3/2}}+\cdots+\frac1{\left(2n\right)^{3/2}}\le\frac{n}{n^{3/2}}=\frac1{\sqrt n}.
$$

Given any $\varepsilon> 0$, take $N=\left[1/\varepsilon^2\right]+1$. Then when $n> N$, $\frac1{\sqrt n}< \varepsilon$. By **Definition** (Limit of a Sequence), the original expression tends to $0$. $\blacksquare$

### Problem 5

(Problem 1.3-2-2) Find the limit:

$$
\lim\limits_{n\to\infty}\left(\sqrt\left[n\right]{1}+\sqrt\left[n\right]{2}+\cdots+\sqrt\left[n\right]{100}\right).
$$

### Solution to Problem 5

By **Example 3.3** (The $n$-th Root of a Positive Number Tends to $1$), for each $k=1,2,\dots,100$,

$$
\lim\limits_{n\to\infty}\sqrt\left[n\right]{k}=1.
$$

By the additive extension (finitely many terms) of **Theorem 3.1** (Arithmetic of Limits),

$$
\lim_{n\to\infty}\left(\sqrt\left[n\right]{1}+\sqrt\left[n\right]{2}+\cdots+\sqrt\left[n\right]{100}\right)=\sum_{k=1}^{100}1=100.

$$

$\blacksquare$
### Problem 6

(Problem 1.3-2-4) Find the limit: $\lim\limits_{n\to\infty}\frac{\frac12+\frac1{2^2}+\cdots+\frac1{2^n}}{\frac13+\frac1{3^2}+\cdots+\frac1{3^n}}$.

### Solution to Problem 6

The numerator is a geometric series:

$$
\displaystyle\sum_{k=1}^n\frac1{2^k}=\frac12\cdot\frac{1-\left(1/2\right)^n}{1-1/2}=1-\left(\frac12\right)^n\to1.
$$

The denominator is a geometric series:

$$
\displaystyle\sum_{k=1}^n\frac1{3^k}=\frac13\cdot\frac{1-\left(1/3\right)^n}{1-1/3}=\frac12\left[1-\left(\frac13\right)^n\right]\to\frac12.
$$

By **Theorem 3.1** (Arithmetic of Limits),

$$
\lim_{n\to\infty}\frac{\text{分子}}{\text{分母}}=\frac1{1/2}=2.

$$

$\blacksquare$
### Problem 7

(Problem 1.3-2-6) Find the limit: $\lim\limits_{n\to\infty}\frac{n^3+3n^2-100}{4n^3-n+2}$.

### Solution to Problem 7

Divide numerator and denominator by $n^3$:

$$
\frac{n^3+3n^2-100}{4n^3-n+2}=\frac{1+3/n-100/n^3}{4-1/n^2+2/n^3}.
$$

As $n\to\infty$, $3/n\to0$, $100/n^3\to0$, $1/n^2\to0$, $2/n^3\to0$. By **Theorem 3.1** (Arithmetic of Limits),

$$
\lim_{n\to\infty}\frac{n^3+3n^2-100}{4n^3-n+2}=\frac14.

$$

$\blacksquare$
### Problem 8

(Problem 1.3-2-8) Find the limit: $\lim\limits_{n\to\infty}\left(1+\frac1n\right)^{-2n}$.

### Solution to Problem 8

$$
\left(1+\frac1n\right)^{-2n}=\frac1{\left[\left(1+\frac1n\right)^n\right]^2}.
$$

By **Theorem 3.2** in Chapter 1, the monotonically increasing sequence bounded above $\left\{\left(1+\frac1n\right)^n\right\}$ has a limit, denoted $e$. By **Theorem 3.1** (Arithmetic of Limits),

$$
\lim_{n\to\infty}\left(1+\frac1n\right)^{-2n}=\frac1{e^2}=e^{-2}.

$$

$\blacksquare$
### Problem 9

(Problem 1.3-2-10) Find the limit: $\lim\limits_{n\to\infty}\sin\left(\pi\sqrt{n^2+1}\right)$.

### Solution to Problem 9

$$
\sin\left(\pi\sqrt{n^2+1}\right)=\sin\left(n\pi+\pi\left(\sqrt{n^2+1}-n\right)\right)=\left(-1\right)^n\sin\left(\pi\left(\sqrt{n^2+1}-n\right)\right).
$$

Using sum-to-product and $\left|\sin t\right|\le\left|t\right|$,

$$
\left|\sin\left(\pi\sqrt{n^2+1}\right)\right|=\left|\sin\left(\pi\left(\sqrt{n^2+1}-n\right)\right)\right|\le\pi\left(\sqrt{n^2+1}-n\right)=\frac{\pi}{\sqrt{n^2+1}+n}\to0.
$$

By **Proposition 1.6** (Properties of the Absolute Value) in Chapter 1 and the squeeze idea, $\lim\sin\left(\pi\sqrt{n^2+1}\right)=0$. $\blacksquare$

### Problem 10

(Problem 1.3-3) Prove the following facts using the definition of the limit:
(1) If $\lim\limits_{n\to\infty}a_n=l$, then for any positive integer $k$, we have

$$
\lim\limits_{n\to\infty}a_{n+k}=l;
$$

(2) If $\lim\limits_{n\to\infty}a_n=l$, then

$$
\lim\limits_{n\to\infty}a_{2n-1}=l,\lim\limits_{n\to\infty}a_{2n}=l.
$$

### Solution to Problem 10

(1) Given any $\varepsilon> 0$, by **Definition** (Limit of a Sequence), there exists a natural number $N$ such that $\left|a_n-l\right|< \varepsilon$ whenever $n> N$. Take $N'=\max\left(1,N-k+1\right)$. Then when $n> N'$, we have $n+k> N$, and hence $\left|a_{n+k}-l\right|< \varepsilon$. Therefore $\lim a_{n+k}=l$.

(2) Given any $\varepsilon> 0$, by **Definition** (Limit of a Sequence), there exists a natural number $N$ such that $\left|a_n-l\right|< \varepsilon$ whenever $n> N$. Take $N'=\left[N/2\right]+1$. Then when $n> N'$, we have $2n> N$ and $2n-1> N$, and hence $\left|a_{2n}-l\right|< \varepsilon$ and $\left|a_{2n-1}-l\right|< \varepsilon$. Therefore both subsequences have limit $l$. $\blacksquare$

### Problem 11

(Problem 1.3-4) Let $\lim\limits_{n\to\infty}a_n=l$. Prove that $\lim\limits_{n\to\infty}\left|a_n\right|=\left|l\right|$.

### Solution to Problem 11

By **Proposition 1.7** (Triangle Inequality) in Chapter 1, $\left|\left|a_n\right|-\left|l\right|\right|\le\left|a_n-l\right|$. Given any $\varepsilon> 0$, by **Definition** (Limit of a Sequence), there exists $N$ such that $\left|a_n-l\right|< \varepsilon$ whenever $n> N$. Then when $n> N$,

$$
\left|\left|a_n\right|-\left|l\right|\right|\le\left|a_n-l\right|< \varepsilon.
$$

By **Definition** (Limit of a Sequence), $\lim\left|a_n\right|=\left|l\right|$. $\blacksquare$

### Problem 12

(Problem 1.3-5) Let $x_1> \sqrt2$, $x_{n+1}=\frac12\left(x_n+\frac2{x_n}\right)$, $n=1,2,\cdots$. Prove that:
(1) $x_n\ge\sqrt2$;

(2) $\left\{x_n\right\}$ is monotonically decreasing;

(3) $\lim\limits_{n\to\infty}x_n$ exists, and

$$
\lim\limits_{n\to\infty}x_n=\sqrt2.
$$

### Solution to Problem 12

(1) By the arithmetic-geometric mean inequality,

$$
x_{n+1}=\frac12\left(x_n+\frac2{x_n}\right)\ge\sqrt{x_n\cdot\frac2{x_n}}=\sqrt2.
$$

By induction, $x_n\ge\sqrt2$ holds for all $n$ (with $x_1> \sqrt2$ as the base case).

(2)

$$
x_{n+1}-x_n=\frac12\left(\frac2{x_n}-x_n\right)=\frac{2-x_n^2}{2x_n}.
$$

By (1), $x_n^2\ge2$, hence $x_{n+1}-x_n\le0$, i.e. $\left\{x_n\right\}$ is monotonically decreasing.

(3) $\left\{x_n\right\}$ is monotonically decreasing and bounded below by $\sqrt2$. By the decreasing version of **Theorem 3.2** (Completeness of the Real Number Field), $\lim x_n$ exists; denote it by $l$. Taking limits on both sides of $x_{n+1}=\frac12\left(x_n+\frac2{x_n}\right)$, and using **Theorem 3.1** (Arithmetic of Limits), we get

$$
l=\frac12\left(l+\frac2l\right),
$$

i.e. $l^2=2$. Moreover $l\ge\sqrt2> 0$, hence $l=\sqrt2$. $\blacksquare$
