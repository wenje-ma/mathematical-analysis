# week5

> **Theorem 3.1 (Arithmetic of Limits)**
> 
> If $\left\{a_n\right\}$ and $\left\{b_n\right\}$ have limits $l_1$ and $l_2$ respectively, then $\lim\left(a_n\pm{b}_n\right)=l_1\pm{l}_2$, $\lim\left(a_n\cdot{b}_n\right)=l_1\cdot{l}_2$, and when $l_2\ne0$, $\lim\frac{a_n}{b_n}=\frac{l_1}{l_2}$.

> **Theorem 3.2 (Completeness of the Real Field)**
> 
> If $\left\{a_n\right\}$ is a monotone increasing sequence bounded above, then there exists $l\in\mathbb{R}$ such that $\left\{a_n\right\}$ converges to $l$.

> **Example 3.3 (The $n$-th Root of a Positive Number Tends to 1)**
> 
> If $a$ is any positive number, then $\lim_{n\to\infty}a^{1/n}=1$.

> **Theorem 4.2 (Squeeze Theorem)**
> 
> Let $\left\{a_n\right\},\left\{b_n\right\},\left\{c_n\right\}$ be three sequences, and suppose there exists $N_0$ such that $c_n\le{a}_n\le{b}_n$ for all $n\ge{N}_0$. If both $c_n$ and $b_n$ converge to the same limit $l$, then $a_n$ also converges to $l$.

## 1.4-3-2

Using the fact that a monotone bounded sequence has a limit, prove that the sequence

$$
a_n=\frac1{n+1}+\frac1{n+2}+\cdots+\frac1{2n}
$$

has a limit.

### Solution to 1.4-3-2

First show $\left\{a_n\right\}$ is increasing:

$$
a_{n+1}-a_n=\frac1{2n+1}+\frac1{2n+2}-\frac1{n+1}=\frac1{2n+1}-\frac1{2n+2}>0.
$$

Thus $\left\{a_n\right\}$ is increasing.

Now show it is bounded above:

$$
a_n=\sum_{k=n+1}^{2n}\frac1k\le\frac{n}{n+1}<1.
$$

By **Theorem 3.2 (Completeness of the Real Field)**, the increasing sequence bounded above has a limit, so $\lim_{n\to\infty}a_n$ exists. $\blacksquare$

## 1.4-4

Let $0<{}a<{}b$ and $n$ be a positive integer. Prove:

(1)

$$
\left(n+1\right)a^n<\frac{b^{n+1}-a^{n+1}}{b-a}<\left(n+1\right)b^n;
$$

(2) Setting $a=1+\frac1{n+1}$, $b=1+\frac1n$, deduce that $\left(1+\frac1n\right)^n$ is strictly increasing and $\left(1+\frac1n\right)^{n+1}$ is strictly decreasing.

### Solution to 1.4-4

(1) By factorization,

$$
\frac{b^{n+1}-a^{n+1}}{b-a}=b^n+b^{n-1}a+\cdots+ba^{n-1}+a^n=\sum_{k=0}^nb^{n-k}a^k.
$$

Since $0<{}a<{}b$, for each term $b^{n-k}a^k$ we have $a^n<{}b^{n-k}a^k<{}b^n$. Summing gives

$$
\left(n+1\right)a^n<\sum_{k=0}^nb^{n-k}a^k<\left(n+1\right)b^n,
$$

i.e. (1) holds.

(2) Take $a=1+\frac1{n+1}$, $b=1+\frac1n$, so $b-a=\frac1{n\left(n+1\right)}$.

From the right inequality in (1): $\frac{b^{n+1}-a^{n+1}}{b-a}<\left(n+1\right)b^n$, i.e. $n\left(b^{n+1}-a^{n+1}\right)<{}b^n$. This simplifies to $b^n\left(nb-1\right)<{}na^{n+1}$. Substituting $nb=n+1$ gives $b^n\cdot{n}<{}na^{n+1}$, i.e. $b^n<{}a^{n+1}$, or

$$
\left(1+\frac1n\right)^n<\left(1+\frac1{n+1}\right)^{n+1},
$$

so $\left(1+\frac1n\right)^n$ is strictly increasing.

From the left inequality in (1): $\left(n+1\right)a^n<\frac{b^{n+1}-a^{n+1}}{b-a}$, i.e. $a^n<{}n\left(b^{n+1}-a^{n+1}\right)$. Simplifying and substituting gives $a^{n+2}<{}b^{n+1}$, i.e.

$$
\left(1+\frac1{n+1}\right)^{n+2}<\left(1+\frac1n\right)^{n+1},
$$

so $\left(1+\frac1n\right)^{n+1}$ is strictly decreasing. $\blacksquare$

## 1.4-5

Prove

$$
\left(1+\frac1n\right)^n<{}e<\left(1+\frac1n\right)^{n+1},\quad{n}=1,2,\cdots.
$$

### Solution to 1.4-5

By 1.4-4, $\left(1+\frac1n\right)^n$ is strictly increasing and its limit is $e$ by The Important Limit $e$, so for all $n$,

$$
\left(1+\frac1n\right)^n<{}e.
$$

Similarly, $\left(1+\frac1n\right)^{n+1}$ is strictly decreasing, and its limit is

$$
\lim_{n\to\infty}\left(1+\frac1n\right)^{n+1}=\lim_{n\to\infty}\left(1+\frac1n\right)^n\cdot\left(1+\frac1n\right)=e\cdot1=e,
$$

so for all $n$,

$$
e<\left(1+\frac1n\right)^{n+1}.
$$

Combining,

$$
\left(1+\frac1n\right)^n<{}e<\left(1+\frac1n\right)^{n+1}.
$$

$\blacksquare$

## 1.4-6

Let $\left\{a_n\right\}$ be increasing and $\left\{b_n\right\}$ be decreasing, with $\lim_{n\to\infty}\left(a_n-b_n\right)=0$. Prove that both $\lim{a}_n$ and $\lim{b}_n$ exist and are equal.

### Solution to 1.4-6

Since $\lim_{n\to\infty}\left(a_n-b_n\right)=0$, there exists $N$ such that for $n>{}N$, $\left|a_n-b_n\right|<1$, i.e. $a_n<{}b_n+1$. Since $\left\{b_n\right\}$ is decreasing, $b_n\le{b}_1$, so $a_n<{}b_1+1$ for $n>{}N$. For $n\le{N}$, $a_n$ takes finitely many values and is bounded. Thus $\left\{a_n\right\}$ is increasing and bounded above; by **Theorem 3.2 (Completeness of the Real Field)**, $\lim_{n\to\infty}a_n=A$ exists.

Similarly, for $n>{}N$, $b_n>{}a_n-1\ge{a}_1-1$ (since $a_n\ge{a}_1$), so $\left\{b_n\right\}$ is decreasing and bounded below. By the decreasing version of **Theorem 3.2 (Completeness of the Real Field)**, $\lim_{n\to\infty}b_n=B$ exists.

Finally,

$$
A-B=\lim_{n\to\infty}\left(a_n-b_n\right)=0,
$$

so $A=B$. $\blacksquare$

## 1.4-9

Prove

$$
e=\lim_{n\to\infty}\left(1+1+\frac1{2!}+\cdots+\frac1{n!}\right).
$$

### Solution to 1.4-9

By the binomial expansion,

$$
\left(1+\frac1n\right)^n=\sum_{k=0}^n\binom{n}k\frac1{n^k}=1+1+\sum_{k=2}^n\frac1{k!}\left(1-\frac1n\right)\left(1-\frac2n\right)\cdots\left(1-\frac{k-1}n\right).
$$

For any fixed $m\ge2$, when $n>{}m$,

$$
\left(1+\frac1n\right)^n>1+1+\sum_{k=2}^m\frac1{k!}\left(1-\frac1n\right)\left(1-\frac2n\right)\cdots\left(1-\frac{k-1}n\right).
$$

Letting $n\to\infty$, by The Important Limit $e$ and **Theorem 3.1 (Arithmetic of Limits)**, the left side tends to $e$ and the right side to $1+1+\frac1{2!}+\cdots+\frac1{m!}$, so

$$
e\ge1+1+\frac1{2!}+\cdots+\frac1{m!}.
$$

On the other hand, for all $n$,

$$
\left(1+\frac1n\right)^n<1+1+\frac1{2!}+\cdots+\frac1{n!}\quad\text{\left(since~each~factor}<1\text{\right)},
$$

so letting $n\to\infty$ gives

$$
e\le\lim_{n\to\infty}\left(1+1+\frac1{2!}+\cdots+\frac1{n!}\right).
$$

Combining both inequalities,

$$
e=\lim_{n\to\infty}\left(1+1+\frac1{2!}+\cdots+\frac1{n!}\right).
$$

$\blacksquare$

## 1.4-10

Using the result above, prove $2<{}e<3$.

### Solution to 1.4-10

By 1.4-9, $e=\sum_{k=0}^{\infty}\frac1{k!}>1+1=2$.

For $k\ge2$, $k!=2\cdot3\cdots{k}\ge2^{k-1}$, so $\frac1{k!}\le\frac1{2^{k-1}}$. Hence

$$
e=1+1+\sum_{k=2}^{\infty}\frac1{k!}\le2+\sum_{k=2}^{\infty}\frac1{2^{k-1}}=2+1=3.
$$

Equality cannot hold (since for $k=3$, $1/6<1/4$), so $e<3$. Therefore $2<{}e<3$. $\blacksquare$
