# week3

> **Basic Knowledge: Definition of Sequence Limit**<br>Let $\left\{a_n\right\}$ be a given sequence. If there exists a real number $l$ such that for every $\varepsilon> 0$, no matter how small, there exists a natural number $N$ such that $\left|a_n-l\right|< \varepsilon$ whenever $n> N$, then $a_n$ is said to have limit $l$, denoted $\lim_{n\to\infty}a_n=l$.

> **Proposition 1.6 (Properties of Absolute Value)**<br>For any $x,y\in\mathbb R$: (1) $\left|x\right|\ge0$, equality iff $x=0$; (2) $\left|-x\right|=\left|x\right|$; (3) $\left|x+y\right|\le\left|x\right|+\left|y\right|$.

> **Proposition 1.7 (Triangle Inequality)**<br>For any real $a,b,c$: (1) $\left|a-b\right|\ge0$, equality iff $a=b$; (2) $\left|a-b\right|=\left|b-a\right|$; (3) $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **Theorem 3.1 (Arithmetic of Limits)**<br>If $\left\{a_n\right\}$ and $\left\{b_n\right\}$ have limits $l_1$ and $l_2$ respectively, then $\lim\left(a_n\pm b_n\right)=l_1\pm l_2$, $\lim\left(a_n\cdot b_n\right)=l_1\cdot l_2$, and when $l_2\ne0$, $\lim\frac{a_n}{b_n}=\frac{l_1}{l_2}$.

> **Theorem 3.2 (Completeness of the Real Field)**<br>If $\left\{a_n\right\}$ is a monotone increasing sequence bounded above, then there exists $l\in\mathbb R$ such that $\left\{a_n\right\}$ converges to $l$. In short, a monotone increasing sequence bounded above has a limit.

> **Example 3.3 (The $n$-th Root of a Positive Number Tends to 1)**<br>If $a$ is any positive number, then $\lim_{n\to\infty}a^{1/n}=1$.

---

## 1.3-1-2

Prove by $\varepsilon$-$N$ language: $\lim_{n\to\infty}\frac{2n-5}{3n+100}=\frac23$.

### Solution 1.3-1-2

Rewrite the general term as

$$
\frac{2n-5}{3n+100}=\frac{2-5/n}{3+100/n}.
$$

As $n\to\infty$, $5/n\to0$ and $100/n\to0$ (by **Basic Knowledge: Definition of Sequence Limit**, for any $\varepsilon> 0$, take $N> 5/\varepsilon$ so that $\left|5/n\right|< \varepsilon$). By **Theorem 3.1 (Arithmetic of Limits)**,

$$
\lim_{n\to\infty}\frac{2n-5}{3n+100}=\frac{\lim\left(2-5/n\right)}{\lim\left(3+100/n\right)}=\frac23.
$$

$\blacksquare$

---

## 1.3-1-4

Prove by $\varepsilon$-$N$ language: $\lim_{n\to\infty}\frac{n!}{n^n}=0$.

### Solution 1.3-1-4

For $n\ge1$,

$$
\frac{n!}{n^n}=\frac{1\cdot2\cdots n}{n\cdot n\cdots n}=\frac1n\cdot\frac2n\cdots\frac{n-1}{n}\cdot1\le\frac1n.
$$

Given $\varepsilon> 0$, take $N=\left[\frac1\varepsilon\right]+1$. Then for $n> N$,

$$
\left|\frac{n!}{n^n}-0\right|\le\frac1n< \varepsilon.
$$

By **Basic Knowledge: Definition of Sequence Limit**, $\lim_{n\to\infty}\frac{n!}{n^n}=0$. $\blacksquare$

---

## 1.3-1-6

Prove by $\varepsilon$-$N$ language: $\lim_{n\to\infty}\frac{n^2+1}{2n^2-7n}=\frac12$.

### Solution 1.3-1-6

Rewrite the general term as

$$
\frac{n^2+1}{2n^2-7n}=\frac{1+1/n^2}{2-7/n}.
$$

As $n\to\infty$, $1/n^2\to0$ and $7/n\to0$. By **Theorem 3.1 (Arithmetic of Limits)**,

$$
\lim_{n\to\infty}\frac{n^2+1}{2n^2-7n}=\frac{\lim\left(1+1/n^2\right)}{\lim\left(2-7/n\right)}=\frac12.
$$

$\blacksquare$

---

## 1.3-1-8

Prove by $\varepsilon$-$N$ language:

$$
\lim_{n\to\infty}\left(\frac1{\left(n+1\right)^{3/2}}+\cdots+\frac1{\left(2n\right)^{3/2}}\right)=0.
$$

### Solution 1.3-1-8

The sum has $n$ terms, each satisfying $\frac1{\left(n+k\right)^{3/2}}\le\frac1{n^{3/2}}$ ($1\le k\le n$), so

$$
0\le\frac1{\left(n+1\right)^{3/2}}+\cdots+\frac1{\left(2n\right)^{3/2}}\le\frac{n}{n^{3/2}}=\frac1{\sqrt n}.
$$

Given $\varepsilon> 0$, take $N=\left[1/\varepsilon^2\right]+1$. Then for $n> N$, $\frac1{\sqrt n}< \varepsilon$. By **Basic Knowledge: Definition of Sequence Limit**, the expression tends to $0$. $\blacksquare$

---

## 1.3-2-2

Find the limit:

$$
\lim_{n\to\infty}\left(\sqrt[n]{1}+\sqrt[n]{2}+\cdots+\sqrt[n]{100}\right).
$$

### Solution 1.3-2-2

By **Example 3.3 (The $n$-th Root of a Positive Number Tends to 1)**, for each $k=1,2,\dots,100$,

$$
\lim_{n\to\infty}\sqrt[n]{k}=1.
$$

By the addition extension of **Theorem 3.1 (Arithmetic of Limits)** (finite terms),

$$
\lim_{n\to\infty}\left(\sqrt[n]{1}+\sqrt[n]{2}+\cdots+\sqrt[n]{100}\right)=\sum_{k=1}^{100}1=100.
$$

$\blacksquare$

---

## 1.3-2-4

Find the limit: $\lim_{n\to\infty}\frac{\frac12+\frac1{2^2}+\cdots+\frac1{2^n}}{\frac13+\frac1{3^2}+\cdots+\frac1{3^n}}$.

### Solution 1.3-2-4

The numerator is a geometric series:

$$
\sum_{k=1}^n\frac1{2^k}=\frac12\cdot\frac{1-\left(1/2\right)^n}{1-1/2}=1-\left(\frac12\right)^n\to1.
$$

The denominator is a geometric series:

$$
\sum_{k=1}^n\frac1{3^k}=\frac13\cdot\frac{1-\left(1/3\right)^n}{1-1/3}=\frac12\left[1-\left(\frac13\right)^n\right]\to\frac12.
$$

By **Theorem 3.1 (Arithmetic of Limits)**,

$$
\lim_{n\to\infty}\frac{\text{numerator}}{\text{denominator}}=\frac1{1/2}=2.
$$

$\blacksquare$

---

## 1.3-2-6

Find the limit: $\lim_{n\to\infty}\frac{n^3+3n^2-100}{4n^3-n+2}$.

### Solution 1.3-2-6

Divide numerator and denominator by $n^3$:

$$
\frac{n^3+3n^2-100}{4n^3-n+2}=\frac{1+3/n-100/n^3}{4-1/n^2+2/n^3}.
$$

As $n\to\infty$, $3/n\to0$, $100/n^3\to0$, $1/n^2\to0$, $2/n^3\to0$. By **Theorem 3.1 (Arithmetic of Limits)**,

$$
\lim_{n\to\infty}\frac{n^3+3n^2-100}{4n^3-n+2}=\frac14.
$$

$\blacksquare$

---

## 1.3-2-8

Find the limit: $\lim_{n\to\infty}\left(1+\frac1n\right)^{-2n}$.

### Solution 1.3-2-8

$$
\left(1+\frac1n\right)^{-2n}=\frac1{\left[\left(1+\frac1n\right)^n\right]^2}.
$$

By **Theorem 3.2 (Completeness of the Real Field)**, the monotone increasing sequence $\left\{\left(1+\frac1n\right)^n\right\}$ bounded above has a limit, denoted $e$. By **Theorem 3.1 (Arithmetic of Limits)**,

$$
\lim_{n\to\infty}\left(1+\frac1n\right)^{-2n}=\frac1{e^2}=e^{-2}.
$$

$\blacksquare$

---

## 1.3-2-10

Find the limit: $\lim_{n\to\infty}\sin\left(\pi\sqrt{n^2+1}\right)$.

### Solution 1.3-2-10

$$
\sin\left(\pi\sqrt{n^2+1}\right)=\sin\left(n\pi+\pi\left(\sqrt{n^2+1}-n\right)\right)=\left(-1\right)^n\sin\left(\pi\left(\sqrt{n^2+1}-n\right)\right).
$$

Since $\left|\sin t\right|\le\left|t\right|$,

$$
\left|\sin\left(\pi\sqrt{n^2+1}\right)\right|=\left|\sin\left(\pi\left(\sqrt{n^2+1}-n\right)\right)\right|\le\pi\left(\sqrt{n^2+1}-n\right)=\frac{\pi}{\sqrt{n^2+1}+n}\to0.
$$

By **Proposition 1.6 (Properties of Absolute Value)** and the squeeze principle, $\lim_{n\to\infty}\sin\left(\pi\sqrt{n^2+1}\right)=0$. $\blacksquare$

---

## 1.3-3

Prove the following facts from the definition of limit:

(1) If $\lim_{n\to\infty}a_n=l$, then for any positive integer $k$,

$$
\lim_{n\to\infty}a_{n+k}=l;
$$

(2) If $\lim_{n\to\infty}a_n=l$, then

$$
\lim_{n\to\infty}a_{2n-1}=l,\quad\lim_{n\to\infty}a_{2n}=l.
$$

### Solution 1.3-3

(1) Given $\varepsilon> 0$, by **Basic Knowledge: Definition of Sequence Limit**, there exists $N$ such that $\left|a_n-l\right|< \varepsilon$ whenever $n> N$. Take $N'=\max\left(1,N-k+1\right)$. Then for $n> N'$, $n+k> N$, so $\left|a_{n+k}-l\right|< \varepsilon$. Hence $\lim_{n\to\infty}a_{n+k}=l$.

(2) Given $\varepsilon> 0$, by **Basic Knowledge: Definition of Sequence Limit**, there exists $N$ such that $\left|a_n-l\right|< \varepsilon$ whenever $n> N$. Take $N'=\left[N/2\right]+1$. Then for $n> N'$, $2n> N$ and $2n-1> N$, so $\left|a_{2n}-l\right|< \varepsilon$ and $\left|a_{2n-1}-l\right|< \varepsilon$. Both subsequences converge to $l$. $\blacksquare$

---

## 1.3-4

Let $\lim_{n\to\infty}a_n=l$. Prove: $\lim_{n\to\infty}\left|a_n\right|=\left|l\right|$.

### Solution 1.3-4

By **Proposition 1.7 (Triangle Inequality)**, $\left|\left|a_n\right|-\left|l\right|\right|\le\left|a_n-l\right|$. Given $\varepsilon> 0$, by **Basic Knowledge: Definition of Sequence Limit**, there exists $N$ such that $\left|a_n-l\right|< \varepsilon$ for $n> N$. Then for $n> N$,

$$
\left|\left|a_n\right|-\left|l\right|\right|\le\left|a_n-l\right|< \varepsilon.
$$

By **Basic Knowledge: Definition of Sequence Limit**, $\lim_{n\to\infty}\left|a_n\right|=\left|l\right|$. $\blacksquare$

---

## 1.3-5

Let $x_1> \sqrt2$, $x_{n+1}=\frac12\left(x_n+\frac2{x_n}\right)$, $n=1,2,\cdots$. Prove:

(1) $x_n\ge\sqrt2$;

(2) $\left\{x_n\right\}$ is monotonically decreasing;

(3) $\lim_{n\to\infty}x_n$ exists and equals $\sqrt2$.

### Solution 1.3-5

(1) By the arithmetic-geometric mean inequality,

$$
x_{n+1}=\frac12\left(x_n+\frac2{x_n}\right)\ge\sqrt{x_n\cdot\frac2{x_n}}=\sqrt2.
$$

By induction, $x_n\ge\sqrt2$ for all $n$ (base case $x_1> \sqrt2$).

(2)

$$
x_{n+1}-x_n=\frac12\left(\frac2{x_n}-x_n\right)=\frac{2-x_n^2}{2x_n}.
$$

From (1), $x_n^2\ge2$, so $x_{n+1}-x_n\le0$, i.e. $\left\{x_n\right\}$ is decreasing.

(3) $\left\{x_n\right\}$ is decreasing and bounded below by $\sqrt2$. By the decreasing version of **Theorem 3.2 (Completeness of the Real Field)**, $\lim_{n\to\infty}x_n$ exists, say $l$. Taking limits on both sides of $x_{n+1}=\frac12\left(x_n+\frac2{x_n}\right)$, by **Theorem 3.1 (Arithmetic of Limits)**,

$$
l=\frac12\left(l+\frac2l\right),
$$

i.e. $l^2=2$. Since $l\ge\sqrt2> 0$, $l=\sqrt2$. $\blacksquare$
