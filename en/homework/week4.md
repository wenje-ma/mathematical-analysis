# week4

> **Basic Knowledge: The Important Limit $e$**<br>$\lim_{n\to\infty}\left(1+\frac1n\right)^n=e$, where $e$ is irrational and $2< e< 3$.

> **Basic Knowledge: Definition of Infinitesimal**<br>A variable whose limit is $0$ is called an infinitesimal.

> **Theorem 3.1 (Arithmetic of Limits)**<br>If $\left\{a_n\right\}$ and $\left\{b_n\right\}$ have limits $l_1$ and $l_2$ respectively, then $\lim\left(a_n\pm b_n\right)=l_1\pm l_2$, $\lim\left(a_n\cdot b_n\right)=l_1\cdot l_2$, and when $l_2\ne0$, $\lim\frac{a_n}{b_n}=\frac{l_1}{l_2}$.

> **Theorem 3.2 (Completeness of the Real Field)**<br>If $\left\{a_n\right\}$ is a monotone increasing sequence bounded above, then there exists $l\in\mathbb R$ such that $\left\{a_n\right\}$ converges to $l$.

> **Example 3.3 (The $n$-th Root of a Positive Number Tends to 1)**<br>If $a$ is any positive number, then $\lim_{n\to\infty}a^{1/n}=1$.

> **Theorem 4.2 (Squeeze Theorem)**<br>Let $\left\{a_n\right\},\left\{b_n\right\},\left\{c_n\right\}$ be three sequences, and suppose there exists $N_0$ such that $c_n\le a_n\le b_n$ for all $n\ge N_0$. If both $c_n$ and $b_n$ converge to the same limit $l$, then $a_n$ also converges to $l$.

---

## 1.4-1

Find the following limits:

(1) $\lim_{n\to\infty}\left(1+\frac1{n+1}\right)^{n-1}$;

(2) $\lim_{n\to\infty}\left(1-\frac1{n^2}\right)^{n^2+1}$;

(3) $\lim_{n\to\infty}\left(1+\frac3{3n+1}\right)^n$;

(4) $\lim_{n\to\infty}\left(\frac{n+3}{n+1}\right)^{n+1}$.

### Solution 1.4-1

(1)

$$
\left(1+\frac1{n+1}\right)^{n-1}=\left[\left(1+\frac1{n+1}\right)^{n+1}\right]^{\frac{n-1}{n+1}}.
$$

By **Basic Knowledge: The Important Limit $e$** and **Theorem 3.1 (Arithmetic of Limits)**, the base tends to $e$ and the exponent $\frac{n-1}{n+1}\to1$, so the limit is $e$.

(2)

$$
\left(1-\frac1{n^2}\right)^{n^2+1}=\left(1-\frac1{n^2}\right)^{n^2}\cdot\left(1-\frac1{n^2}\right).
$$

Setting $m=-n^2$, we have $\left(1+\frac1m\right)^m\to e$, so

$$
\left(1-\frac1{n^2}\right)^{n^2}=\left[\left(1+\frac1{-n^2}\right)^{-n^2}\right]^{-1}\to e^{-1},
$$

and $\left(1-\frac1{n^2}\right)\to1$. The limit is $e^{-1}=\frac1e$.

(3)

$$
\left(1+\frac3{3n+1}\right)^n=\left[\left(1+\frac3{3n+1}\right)^{\frac{3n+1}{3}}\right]^{\frac{3n}{3n+1}}.
$$

By **Basic Knowledge: The Important Limit $e$**, the base tends to $e$ and the exponent $\frac{3n}{3n+1}\to1$, so the limit is $e$.

(4)

$$
\left(\frac{n+3}{n+1}\right)^{n+1}=\left(1+\frac2{n+1}\right)^{n+1}=\left[\left(1+\frac2{n+1}\right)^{\frac{n+1}{2}}\right]^2.
$$

By **Basic Knowledge: The Important Limit $e$**, the base tends to $e$, so the limit is $e^2$. $\blacksquare$

---

## 1.4-3-2

Using the fact that a monotone bounded sequence has a limit, prove that the sequence

$$
a_n=\frac1{n+1}+\frac1{n+2}+\cdots+\frac1{2n}
$$

has a limit.

### Solution 1.4-3-2

First show $\left\{a_n\right\}$ is increasing:

$$
a_{n+1}-a_n=\frac1{2n+1}+\frac1{2n+2}-\frac1{n+1}=\frac1{2n+1}-\frac1{2n+2}> 0.
$$

Thus $\left\{a_n\right\}$ is increasing.

Now show it is bounded above:

$$
a_n=\sum_{k=n+1}^{2n}\frac1k\le\frac{n}{n+1}< 1.
$$

By **Theorem 3.2 (Completeness of the Real Field)**, the increasing sequence bounded above has a limit, so $\lim_{n\to\infty}a_n$ exists. $\blacksquare$

---

## 1.4-4

Let $0< a< b$ and $n$ be a positive integer. Prove:

(1)

$$
\left(n+1\right)a^n< \frac{b^{n+1}-a^{n+1}}{b-a}< \left(n+1\right)b^n;
$$

(2) Setting $a=1+\frac1{n+1}$, $b=1+\frac1n$, deduce that $\left(1+\frac1n\right)^n$ is strictly increasing and $\left(1+\frac1n\right)^{n+1}$ is strictly decreasing.

### Solution 1.4-4

(1) By factorization,

$$
\frac{b^{n+1}-a^{n+1}}{b-a}=b^n+b^{n-1}a+\cdots+ba^{n-1}+a^n=\sum_{k=0}^n b^{n-k}a^k.
$$

Since $0< a< b$, for each term $b^{n-k}a^k$ we have $a^n< b^{n-k}a^k< b^n$. Summing gives

$$
\left(n+1\right)a^n< \sum_{k=0}^n b^{n-k}a^k< \left(n+1\right)b^n,
$$

i.e. (1) holds.

(2) Take $a=1+\frac1{n+1}$, $b=1+\frac1n$, so $b-a=\frac1{n\left(n+1\right)}$.

From the right inequality in (1): $\frac{b^{n+1}-a^{n+1}}{b-a}< \left(n+1\right)b^n$, i.e. $n\left(b^{n+1}-a^{n+1}\right)< b^n$. This simplifies to $b^n\left(nb-1\right)< na^{n+1}$. Substituting $nb=n+1$ gives $b^n\cdot n< na^{n+1}$, i.e. $b^n< a^{n+1}$, or

$$
\left(1+\frac1n\right)^n< \left(1+\frac1{n+1}\right)^{n+1},
$$

so $\left(1+\frac1n\right)^n$ is strictly increasing.

From the left inequality in (1): $\left(n+1\right)a^n< \frac{b^{n+1}-a^{n+1}}{b-a}$, i.e. $a^n< n\left(b^{n+1}-a^{n+1}\right)$. Simplifying and substituting gives $a^{n+2}< b^{n+1}$, i.e.

$$
\left(1+\frac1{n+1}\right)^{n+2}< \left(1+\frac1n\right)^{n+1},
$$

so $\left(1+\frac1n\right)^{n+1}$ is strictly decreasing. $\blacksquare$

---

## 1.4-5

Prove

$$
\left(1+\frac1n\right)^n< e< \left(1+\frac1n\right)^{n+1},\quad n=1,2,\cdots.
$$

### Solution 1.4-5

By 1.4-4, $\left(1+\frac1n\right)^n$ is strictly increasing and its limit is $e$ by **Basic Knowledge: The Important Limit $e$**, so for all $n$,

$$
\left(1+\frac1n\right)^n< e.
$$

Similarly, $\left(1+\frac1n\right)^{n+1}$ is strictly decreasing, and its limit is

$$
\lim_{n\to\infty}\left(1+\frac1n\right)^{n+1}=\lim_{n\to\infty}\left(1+\frac1n\right)^n\cdot\left(1+\frac1n\right)=e\cdot1=e,
$$

so for all $n$,

$$
e< \left(1+\frac1n\right)^{n+1}.
$$

Combining,

$$
\left(1+\frac1n\right)^n< e< \left(1+\frac1n\right)^{n+1}.
$$

$\blacksquare$

---

## 1.4-6

Let $\left\{a_n\right\}$ be increasing and $\left\{b_n\right\}$ be decreasing, with $\lim_{n\to\infty}\left(a_n-b_n\right)=0$. Prove that both $\lim a_n$ and $\lim b_n$ exist and are equal.

### Solution 1.4-6

Since $\lim_{n\to\infty}\left(a_n-b_n\right)=0$, there exists $N$ such that for $n> N$, $\left|a_n-b_n\right|< 1$, i.e. $a_n< b_n+1$. Since $\left\{b_n\right\}$ is decreasing, $b_n\le b_1$, so $a_n< b_1+1$ for $n> N$. For $n\le N$, $a_n$ takes finitely many values and is bounded. Thus $\left\{a_n\right\}$ is increasing and bounded above; by **Theorem 3.2 (Completeness of the Real Field)**, $\lim_{n\to\infty}a_n=A$ exists.

Similarly, for $n> N$, $b_n> a_n-1\ge a_1-1$ (since $a_n\ge a_1$), so $\left\{b_n\right\}$ is decreasing and bounded below. By the decreasing version of **Theorem 3.2 (Completeness of the Real Field)**, $\lim_{n\to\infty}b_n=B$ exists.

Finally,

$$
A-B=\lim_{n\to\infty}\left(a_n-b_n\right)=0,
$$

so $A=B$. $\blacksquare$

---

## 1.4-9

Prove

$$
e=\lim_{n\to\infty}\left(1+1+\frac1{2!}+\cdots+\frac1{n!}\right).
$$

### Solution 1.4-9

By the binomial expansion,

$$
\left(1+\frac1n\right)^n=\sum_{k=0}^n\binom nk\frac1{n^k}=1+1+\sum_{k=2}^n\frac1{k!}\left(1-\frac1n\right)\left(1-\frac2n\right)\cdots\left(1-\frac{k-1}n\right).
$$

For any fixed $m\ge2$, when $n> m$,

$$
\left(1+\frac1n\right)^n> 1+1+\sum_{k=2}^m\frac1{k!}\left(1-\frac1n\right)\left(1-\frac2n\right)\cdots\left(1-\frac{k-1}n\right).
$$

Letting $n\to\infty$, by **Basic Knowledge: The Important Limit $e$** and **Theorem 3.1 (Arithmetic of Limits)**, the left side tends to $e$ and the right side to $1+1+\frac1{2!}+\cdots+\frac1{m!}$, so

$$
e\ge1+1+\frac1{2!}+\cdots+\frac1{m!}.
$$

On the other hand, for all $n$,

$$
\left(1+\frac1n\right)^n< 1+1+\frac1{2!}+\cdots+\frac1{n!}\quad\text{(since each factor}< 1\text{)},
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

---

## 1.4-10

Using the result above, prove $2< e< 3$.

### Solution 1.4-10

By 1.4-9, $e=\sum_{k=0}^{\infty}\frac1{k!}> 1+1=2$.

For $k\ge2$, $k!=2\cdot3\cdots k\ge2^{k-1}$, so $\frac1{k!}\le\frac1{2^{k-1}}$. Hence

$$
e=1+1+\sum_{k=2}^{\infty}\frac1{k!}\le2+\sum_{k=2}^{\infty}\frac1{2^{k-1}}=2+1=3.
$$

Equality cannot hold (since for $k=3$, $1/6< 1/4$), so $e< 3$. Therefore $2< e< 3$. $\blacksquare$

---

## 1.4-14

Let $\left\{a_n\right\}$ be an infinitesimal and $\left\{b_n\right\}$ be bounded, i.e. there exists $M> 0$ such that $\left|b_n\right|\le M$ for all $n$. Prove $\lim_{n\to\infty}a_nb_n=0$.

### Solution 1.4-14

Since $\left\{a_n\right\}$ is an infinitesimal, $\lim_{n\to\infty}a_n=0$. Since $\left|b_n\right|\le M$,

$$
0\le\left|a_nb_n\right|\le M\left|a_n\right|.
$$

As $n\to\infty$, $M\left|a_n\right|\to0$ and the left side $0\to0$. By **Theorem 4.2 (Squeeze Theorem)**, $\lim_{n\to\infty}\left|a_nb_n\right|=0$, i.e. $\lim_{n\to\infty}a_nb_n=0$. $\blacksquare$

---

## 1.4-16

Let $\lim_{n\to\infty}a_n=a$. Prove:

(1) $\lim_{n\to\infty}\frac{\left[na_n\right]}{n}=a$;

(2) If $a> 0$ and $a_n> 0$, then $\lim_{n\to\infty}\sqrt[n]{a_n}=1$.

### Solution 1.4-16

(1) By the floor function, $na_n-1< \left[na_n\right]\le na_n$, so

$$
a_n-\frac1n< \frac{\left[na_n\right]}{n}\le a_n.
$$

As $n\to\infty$, $a_n\to a$ and $a_n-\frac1n\to a$ (since $\frac1n\to0$). By **Theorem 4.2 (Squeeze Theorem)**, $\frac{\left[na_n\right]}{n}\to a$.

(2) Since $a_n\to a> 0$, there exists $N$ such that for $n> N$, $\frac a2< a_n< 2a$. Thus

$$
\left(\frac a2\right)^{1/n}< a_n^{1/n}< \left(2a\right)^{1/n}.
$$

By **Example 3.3 (The $n$-th Root of a Positive Number Tends to 1)**, both ends tend to $1$. By **Theorem 4.2 (Squeeze Theorem)**, $\sqrt[n]{a_n}\to1$. $\blacksquare$

---

## 1.4-18

Prove $\lim_{n\to\infty}\left(1+\frac1{n^2}\right)^n=1$.

### Solution 1.4-18

By the binomial expansion,

$$
\left(1+\frac1{n^2}\right)^n=\sum_{k=0}^n\binom nk\frac1{n^{2k}}=1+\frac1n+\sum_{k=2}^n\binom nk\frac1{n^{2k}}.
$$

For $k\ge2$, $\binom nk\le\frac{n^k}{k!}$, so

$$
0\le\left(1+\frac1{n^2}\right)^n-1\le\frac1n+\frac1{n^2}\sum_{k=2}^n\frac1{k!}\le\frac1n+\frac{e-2}{n^2}.
$$

The right side tends to $0$ as $n\to\infty$. By **Theorem 4.2 (Squeeze Theorem)**, $\left(1+\frac1{n^2}\right)^n\to1$. $\blacksquare$
