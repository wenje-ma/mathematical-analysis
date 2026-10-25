# Assignment 4

> **Theorem 4.2** (Squeeze Theorem) Let $\left\{a_n\right\},\left\{b_n\right\},\left\{c_n\right\}$ be three sequences, and suppose there exists a natural number $N_0$ such that $c_n\le a_n\le b_n,\forall n\ge N_0$. If both $c_n$ and $b_n$ have limits and both equal $l$, then the limit of $a_n$ exists and also equals $l$.

> **Important Limit** (The Number $e$) $\lim\limits_{n\to\infty}\left(1+\frac1n\right)^n=e$, where $e$ is irrational and $2< e< 3$.

> **Definition** (Infinitesimal) A variable whose limit is $0$ is called an infinitesimal.

### Problem 1

(Problem 1.4-1) Find the following limits:
(1) $\lim\limits_{n\to\infty}\left(1+\frac1{n+1}\right)^{n-1}$;

(2) $\lim\limits_{n\to\infty}\left(1-\frac1{n^2}\right)^{n^2+1}$;

(3) $\lim\limits_{n\to\infty}\left(1+\frac3{3n+1}\right)^n$;

(4) $\lim\limits_{n\to\infty}\left(\frac{n+3}{n+1}\right)^{n+1}$.

### Solution to Problem 1

(1)

$$
\left(1+\frac1{n+1}\right)^{n-1}=\left[\left(1+\frac1{n+1}\right)^{n+1}\right]^{\frac{n-1}{n+1}}.
$$

By the **Important Limit** (The Number $e$) and **Theorem 3.1** in Chapter 1, the base tends to $e$ and the exponent $\frac{n-1}{n+1}\to1$, so the limit is $e$.

(2)

$$
\left(1-\frac1{n^2}\right)^{n^2+1}=\left(1-\frac1{n^2}\right)^{n^2}\cdot\left(1-\frac1{n^2}\right).
$$
Let $m=-n^2$. Then $\left(1+\frac1m\right)^m\to e$, so

$$
\left(1-\frac1{n^2}\right)^{n^2}=\left[\left(1+\frac1{-n^2}\right)^{-n^2}\right]^{-1}\to e^{-1},
$$

and $\left(1-\frac1{n^2}\right)\to1$. Hence the limit is $e^{-1}=\frac1e$.

(3)

$$
\left(1+\frac3{3n+1}\right)^n=\left[\left(1+\frac3{3n+1}\right)^{\frac{3n+1}{3}}\right]^{\frac{3n}{3n+1}}.
$$

By the **Important Limit** (The Number $e$), the base tends to $e$ and the exponent $\frac{3n}{3n+1}\to1$, so the limit is $e$.

(4)

$$
\left(\frac{n+3}{n+1}\right)^{n+1}=\left(1+\frac2{n+1}\right)^{n+1}=\left[\left(1+\frac2{n+1}\right)^{\frac{n+1}{2}}\right]^2.
$$

By the **Important Limit** (The Number $e$), the base tends to $e$, so the limit is $e^2$. $\blacksquare$

### Problem 2

(Problem 1.4-3-2) Using the fact that a monotone bounded sequence has a limit, prove that the sequence

$$
a_n=\frac1{n+1}+\frac1{n+2}+\cdots+\frac1{2n}
$$

has a limit.

### Solution to Problem 2

First prove that $\left\{a_n\right\}$ is monotonically increasing:

$$
a_{n+1}-a_n=\frac1{2n+1}+\frac1{2n+2}-\frac1{n+1}=\frac1{2n+1}-\frac1{2n+2}> 0.
$$

Hence $\left\{a_n\right\}$ is monotonically increasing.

Next prove it is bounded above:

$$
a_n=\displaystyle\sum_{k=n+1}^{2n}\frac1k\le\frac{n}{n+1}< 1.
$$

By **Theorem 3.2** (Completeness of the Real Number Field) in Chapter 1, every monotonically increasing sequence bounded above has a limit, so $\lim a_n$ exists. $\blacksquare$

### Problem 3

(Problem 1.4-4) Let $0< a< b$ and let $n$ be a positive integer. Prove that:
(1)

$$
\left(n+1\right)a^n< \frac{b^{n+1}-a^{n+1}}{b-a}< \left(n+1\right)b^n;
$$

(2) Taking $a=1+\frac1{n+1},b=1+\frac1n$, deduce from the above that $\left(1+\frac1n\right)^n$ is strictly increasing and $\left(1+\frac1n\right)^{n+1}$ is strictly decreasing.

### Solution to Problem 3

(1) By factorization,

$$
\frac{b^{n+1}-a^{n+1}}{b-a}=b^n+b^{n-1}a+\cdots+ba^{n-1}+a^n=\sum_{k=0}^n b^{n-k}a^k.
$$

Since $0< a< b$, for each term $b^{n-k}a^k$ we have $a^n< b^{n-k}a^k< b^n$. Summing gives

$$
\left(n+1\right)a^n< \sum_{k=0}^n b^{n-k}a^k< \left(n+1\right)b^n,
$$

i.e. (1) holds.

(2) Take $a=1+\frac1{n+1},b=1+\frac1n$. Then

$$
b-a=\frac1{n\left(n+1\right)}.
$$

From the right half of (1): $\frac{b^{n+1}-a^{n+1}}{b-a}< \left(n+1\right)b^n$, i.e.

$$
n\left(n+1\right)\left(b^{n+1}-a^{n+1}\right)< \left(n+1\right)b^n,
$$

i.e. $n\left(b^{n+1}-a^{n+1}\right)< b^n$. Rearranging gives $nb^{n+1}-b^n< na^{n+1}$, i.e. $b^n\left(nb-1\right)< na^{n+1}$. Substituting $nb=n+1$ gives $b^n\cdot n< na^{n+1}$, i.e. $b^n< a^{n+1}$, i.e.

$$
\left(1+\frac1n\right)^n< \left(1+\frac1{n+1}\right)^{n+1},
$$

so $\left(1+\frac1n\right)^n$ is strictly increasing.

From the left half of (1): $\left(n+1\right)a^n< \frac{b^{n+1}-a^{n+1}}{b-a}$, i.e.

$$
\left(n+1\right)a^n< n\left(n+1\right)\left(b^{n+1}-a^{n+1}\right),
$$

i.e. $a^n< n\left(b^{n+1}-a^{n+1}\right)$. Rearranging gives $a^n+na^{n+1}< nb^{n+1}$, i.e. $a^n\left(na+1\right)< nb^{n+1}$. Substituting $na=\frac{n\left(n+2\right)}{n+1}$ and simplifying gives $a^{n+2}< b^{n+1}$, i.e.

$$
\left(1+\frac1{n+1}\right)^{n+2}< \left(1+\frac1n\right)^{n+1},
$$

so $\left(1+\frac1n\right)^{n+1}$ is strictly decreasing. $\blacksquare$

### Problem 4

(Problem 1.4-5) Prove that

$$
\left(1+\frac1n\right)^n< e< \left(1+\frac1n\right)^{n+1},n=1,2,\cdots.
$$

### Solution to Problem 4

By **Problem 3**, $\left(1+\frac1n\right)^n$ is strictly increasing, and by the **Important Limit** (The Number $e$) its limit is $e$, so for all $n$

$$
\left(1+\frac1n\right)^n< e.
$$

Similarly, $\left(1+\frac1n\right)^{n+1}$ is strictly decreasing, and its limit is

$$
\lim\left(1+\frac1n\right)^{n+1}=\lim\left(1+\frac1n\right)^n\cdot\left(1+\frac1n\right)=e\cdot1=e,
$$

so for all $n$

$$
e< \left(1+\frac1n\right)^{n+1}.
$$

Combining,

$$
\left(1+\frac1n\right)^n< e< \left(1+\frac1n\right)^{n+1}.
$$

$\blacksquare$

### Problem 5

(Problem 1.4-6) Let $\left\{a_n\right\}$ be an increasing sequence and $\left\{b_n\right\}$ a decreasing sequence, and suppose $\lim\limits_{n\to\infty}\left(a_n-b_n\right)=0$. Prove that both $\lim a_n$ and $\lim b_n$ exist and are equal.

### Solution to Problem 5

Since $\lim\left(a_n-b_n\right)=0$, there exists $N$ such that $\left|a_n-b_n\right|< 1$ when $n> N$, i.e. $a_n< b_n+1$. Moreover $\left\{b_n\right\}$ is decreasing, so $b_n\le b_1$, and hence $a_n< b_1+1$ ($n> N$). For $n\le N$, $a_n$ takes finitely many values and is bounded. Thus $\left\{a_n\right\}$ is increasing and bounded above, and by **Theorem 3.2** (Completeness of the Real Number Field) in Chapter 1, $\lim a_n=A$ exists.

Similarly, when $n> N$, $b_n> a_n-1\ge a_1-1$ (since $a_n\ge a_1$), so $\left\{b_n\right\}$ is decreasing and bounded below. By the decreasing version of **Theorem 3.2**, $\lim b_n=B$ exists.

Finally,

$$
A-B=\lim\left(a_n-b_n\right)=0,
$$

so $A=B$. $\blacksquare$

### Problem 6

(Problem 1.4-9) Prove that

$$
e=\lim\limits_{n\to\infty}\left(1+1+\frac1{2!}+\cdots+\frac1{n!}\right).
$$

### Solution to Problem 6

By the Newton binomial expansion,

$$
\left(1+\frac1n\right)^n=\sum_{k=0}^n\binom nk\frac1{n^k}=1+1+\sum_{k=2}^n\frac1{k!}\left(1-\frac1n\right)\left(1-\frac2n\right)\cdots\left(1-\frac{k-1}n\right).
$$

For any fixed $m\ge2$, when $n> m$,

$$
\left(1+\frac1n\right)^n> 1+1+\sum_{k=2}^m\frac1{k!}\left(1-\frac1n\right)\left(1-\frac2n\right)\cdots\left(1-\frac{k-1}n\right).
$$

Letting $n\to\infty$, by the **Important Limit** (The Number $e$) and **Theorem 3.1** in Chapter 1, the left side tends to $e$ and the right side tends to $1+1+\frac1{2!}+\cdots+\frac1{m!}$, so

$$
e\ge1+1+\frac1{2!}+\cdots+\frac1{m!}.
$$

On the other hand, for all $n$,

$$
\left(1+\frac1n\right)^n< 1+1+\frac1{2!}+\cdots+\frac1{n!}\ \left(\text{因各项因子}< 1\right),
$$

and letting $n\to\infty$ gives

$$
e\le\lim_{n\to\infty}\left(1+1+\frac1{2!}+\cdots+\frac1{n!}\right).
$$

Combining the two sides,

$$
e=\lim\limits_{n\to\infty}\left(1+1+\frac1{2!}+\cdots+\frac1{n!}\right).
$$

$\blacksquare$

### Problem 7

(Problem 1.4-10) Using the result of the previous problem, prove that $2< e< 3$.

### Solution to Problem 7

By **Problem 6**, $e=\displaystyle\sum_{k=0}^{\infty}\frac1{k!}> 1+1=2$.

Moreover, for $k\ge2$, $k!=2\cdot3\cdots k\ge2^{k-1}$, so $\frac1{k!}\le\frac1{2^{k-1}}$. Hence

$$
e=1+1+\sum_{k=2}^{\infty}\frac1{k!}\le2+\sum_{k=2}^{\infty}\frac1{2^{k-1}}=2+1=3.
$$

Moreover equality cannot hold (since for $k=3$, $1/6< 1/4$), so $e< 3$. In summary, $2< e< 3$. $\blacksquare$

### Problem 8

(Problem 1.4-14) Let there be two sequences $\left\{a_n\right\}$ and $\left\{b_n\right\}$, where $\left\{a_n\right\}$ is an **infinitesimal** and $\left\{b_n\right\}$ is a bounded sequence, i.e. there exists a positive number $M$ such that $\left|b_n\right|\le M,\forall n=1,2,\cdots$. Prove that $\lim\limits_{n\to\infty}a_nb_n=0$.

### Solution to Problem 8

Since $\left\{a_n\right\}$ is an **infinitesimal**, i.e. $\lim a_n=0$. And $\left|b_n\right|\le M$, so

$$
0\le\left|a_nb_n\right|\le M\left|a_n\right|.
$$

As $n\to\infty$, $M\left|a_n\right|\to0$ and the left side $0\to0$. By **Theorem 4.2** (Squeeze Theorem), $\lim\left|a_nb_n\right|=0$, i.e. $\lim a_nb_n=0$. $\blacksquare$

### Problem 9

(Problem 1.4-16) Let $\lim\limits_{n\to\infty}a_n=a$. Prove that:
(1) $\lim\limits_{n\to\infty}\frac{\left[na_n\right]}{n}=a$;

(2) If $a> 0$ and $a_n> 0$, then

$$
\lim\limits_{n\to\infty}\sqrt\left[n\right]{a_n}=1.
$$

### Solution to Problem 9

(1) By the definition of the floor function, $na_n-1< \left[na_n\right]\le na_n$, so

$$
a_n-\frac1n< \frac{\left[na_n\right]}{n}\le a_n.
$$

As $n\to\infty$, $a_n\to a$ and $a_n-\frac1n\to a$ (since $\frac1n\to0$). By **Theorem 4.2** (Squeeze Theorem), $\frac{\left[na_n\right]}{n}\to a$.

(2) Since $a_n\to a> 0$, there exists $N$ such that $\frac a2< a_n< 2a$ when $n> N$. Hence

$$
\left(\frac a2\right)^{1/n}< a_n^{1/n}< \left(2a\right)^{1/n}.
$$

By **Example 3.3** in Chapter 1 (The $n$-th Root of a Positive Number Tends to $1$), both ends tend to $1$. By **Theorem 4.2** (Squeeze Theorem),

$$
\sqrt\left[n\right]{a_n}\to1.
$$

$\blacksquare$

### Problem 10

(Problem 1.4-18) Prove that $\lim\limits_{n\to\infty}\left(1+\frac1{n^2}\right)^n=1$.

### Solution to Problem 10

By the Newton binomial expansion,

$$
\left(1+\frac1{n^2}\right)^n=\sum_{k=0}^n\binom nk\frac1{n^{2k}}=1+\frac1n+\sum_{k=2}^n\binom nk\frac1{n^{2k}}.
$$

For $k\ge2$, $\binom nk\le\frac{n^k}{k!}$, so

$$
0\le\left(1+\frac1{n^2}\right)^n-1\le\frac1n+\frac1{n^2}\sum_{k=2}^n\frac1{k!}\le\frac1n+\frac{e-2}{n^2}.
$$

The right side tends to $0$ as $n\to\infty$. By **Theorem 4.2** (Squeeze Theorem), $\left(1+\frac1{n^2}\right)^n\to1$. $\blacksquare$
