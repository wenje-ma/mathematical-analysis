# week6

> **Proposition 1.7 (Triangle Inequality)**
> 
> For any real $a,b,c$, $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

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

> **Theorem 5.1 (Arithmetic of Function Limits)**
> 
> If $\lim{f}\left(x\right)=l_1$ and $\lim{g}\left(x\right)=l_2$, then $\lim\left(f\pm{g}\right)=l_1\pm{l}_2$, $\lim\left(f\cdot{g}\right)=l_1\cdot{l}_2$, and when $l_2\ne0$, $\lim\frac{f}{g}=\frac{l_1}{l_2}$.

## 1.4-14

Let $\left\{a_n\right\}$ be an infinitesimal and $\left\{b_n\right\}$ be bounded, i.e. there exists $M>0$ such that $\left|b_n\right|\le{M}$ for all $n$. Prove $\lim_{n\to\infty}a_nb_n=0$.

### Solution to 1.4-14

Since $\left\{a_n\right\}$ is an infinitesimal, $\lim_{n\to\infty}a_n=0$. Since $\left|b_n\right|\le{M}$,

$$
0\le\left|a_nb_n\right|\le{M}\left|a_n\right|.
$$

As $n\to\infty$, $M\left|a_n\right|\to0$ and the left side $0\to0$. By **Theorem 4.2 (Squeeze Theorem)**, $\lim_{n\to\infty}\left|a_nb_n\right|=0$, i.e. $\lim_{n\to\infty}a_nb_n=0$. $\blacksquare$

## 1.4-16

Let $\lim_{n\to\infty}a_n=a$. Prove:

(1) $\lim_{n\to\infty}\frac{\left[na_n\right]}{n}=a$;

(2) If $a>0$ and $a_n>0$, then $\lim_{n\to\infty}\sqrt\left[n\right]{a_n}=1$.

### Solution to 1.4-16

(1) By the floor function, $na_n-1<\left[na_n\right]\le{n}a_n$, so

$$
a_n-\frac1n<\frac{\left[na_n\right]}{n}\le{a}_n.
$$

As $n\to\infty$, $a_n\to{a}$ and $a_n-\frac1n\to{a}$ (since $\frac1n\to0$). By **Theorem 4.2 (Squeeze Theorem)**, $\frac{\left[na_n\right]}{n}\to{a}$.

(2) Since $a_n\to{a}>0$, there exists $N$ such that for $n>{}N$, $\frac{a}2<{}a_n<2a$. Thus

$$
\left(\frac{a}2\right)^{1/n}<{}a_n^{1/n}<\left(2a\right)^{1/n}.
$$

By **Example 3.3 (The $n$-th Root of a Positive Number Tends to 1)**, both ends tend to $1$. By **Theorem 4.2 (Squeeze Theorem)**, $\sqrt\left[n\right]{a_n}\to1$. $\blacksquare$

## 1.4-18

Prove $\lim_{n\to\infty}\left(1+\frac1{n^2}\right)^n=1$.

### Solution to 1.4-18

By the binomial expansion,

$$
\left(1+\frac1{n^2}\right)^n=\sum_{k=0}^n\binom{n}k\frac1{n^{2k}}=1+\frac1n+\sum_{k=2}^n\binom{n}k\frac1{n^{2k}}.
$$

For $k\ge2$, $\binom{n}k\le\frac{n^k}{k!}$, so

$$
0\le\left(1+\frac1{n^2}\right)^n-1\le\frac1n+\frac1{n^2}\sum_{k=2}^n\frac1{k!}\le\frac1n+\frac{e-2}{n^2}.
$$

The right side tends to $0$ as $n\to\infty$. By **Theorem 4.2 (Squeeze Theorem)**, $\left(1+\frac1{n^2}\right)^n\to1$. $\blacksquare$

## 1.5-1-2

Prove by $\varepsilon$-$\delta$ language: $\lim_{x\to{a}}\cos{x}=\cos{a}$.

### Solution to 1.5-1-2

Using sum-to-product identities,

$$
\left|\cos{x}-\cos{a}\right|=2\left|\sin\frac{x+a}2\right|\left|\sin\frac{x-a}2\right|\le2\cdot1\cdot\frac{\left|x-a\right|}2=\left|x-a\right|,
$$

using $\left|\sin{t}\right|\le\left|t\right|$ for all $t$.

Given $\varepsilon>0$, take $\delta=\varepsilon$. Then for $0<\left|x-a\right|<\delta$,

$$
\left|\cos{x}-\cos{a}\right|\le\left|x-a\right|<\varepsilon.
$$

By Definition of Function Limit, $\lim_{x\to{a}}\cos{x}=\cos{a}$. $\blacksquare$

## 1.5-1-3

Prove by $\varepsilon$-$\delta$ language: $\lim_{x\to+\infty}\frac{6x+5}{x+1}=6$.

### Solution to 1.5-1-3

$$
\left|\frac{6x+5}{x+1}-6\right|=\left|\frac{6x+5-6\left(x+1\right)}{x+1}\right|=\frac1{x+1}.
$$

Given $\varepsilon>0$, take $X=\frac1\varepsilon-1$. Then for $x>{}X$,

$$
\left|\frac{6x+5}{x+1}-6\right|=\frac1{x+1}<\varepsilon.
$$

By the $x\to+\infty$ version of Definition of Function Limit, $\lim_{x\to+\infty}\frac{6x+5}{x+1}=6$. $\blacksquare$

## 1.5-1-5

Prove by $\varepsilon$-$\delta$ language: $\lim_{x\to2-0}\sqrt{4-x^2}=0$.

### Solution to 1.5-1-5

$\left|\sqrt{4-x^2}-0\right|=\sqrt{4-x^2}$. To make $\sqrt{4-x^2}<\varepsilon$, it suffices that $4-x^2<\varepsilon^2$, i.e. $x^2>4-\varepsilon^2$. Since $x\to2-0$ means $x<2$, it suffices that $x>\sqrt{4-\varepsilon^2}$. Take $\delta=2-\sqrt{4-\varepsilon^2}$. Then for $2-\delta<{}x<2$,

$$
0<2-x<\delta\Rightarrow{x}>\sqrt{4-\varepsilon^2}\Rightarrow\sqrt{4-x^2}<\varepsilon.
$$

By Definition of One-Sided Limits, $\lim_{x\to2-0}\sqrt{4-x^2}=0$. $\blacksquare$

## 1.5-1-7

Let $a>0$. Prove $\lim_{x\to0}a^x=1$.

### Solution to 1.5-1-7

Assume $a>1$ (the case $0<{}a<1$ is analogous). To make $\left|a^x-1\right|<\varepsilon$, i.e. $1-\varepsilon<{}a^x<1+\varepsilon$. For $0<\varepsilon<1$, the left inequality $a^x>1-\varepsilon>0$ gives $x>\log_a\left(1-\varepsilon\right)$; the right inequality $a^x<1+\varepsilon$ gives $x<\log_a\left(1+\varepsilon\right)$.

Take

$$
\delta=\min\left\{-\log_a\left(1-\varepsilon\right),\log_a\left(1+\varepsilon\right)\right\}>0,
$$

then for $0<\left|x\right|<\delta$, $\left|a^x-1\right|<\varepsilon$. By Definition of Function Limit, $\lim_{x\to0}a^x=1$. $\blacksquare$

## 1.5-4

Let $\lim_{x\to{a}}f\left(x\right)=l$ and $l\ne0$. Prove that $y=\frac1{f\left(x\right)}$ is bounded as $x\to{a}$.

### Solution to 1.5-4

Take $\varepsilon=\frac{\left|l\right|}{2}$. By Definition of Function Limit, there exists $\delta>0$ such that $0<\left|x-a\right|<\delta$ implies $\left|f\left(x\right)-l\right|<\frac{\left|l\right|}{2}$. By **Proposition 1.7 (Triangle Inequality)**,

$$
\left|f\left(x\right)\right|=\left|l-\left(l-f\left(x\right)\right)\right|\ge\left|l\right|-\left|l-f\left(x\right)\right|>\left|l\right|-\frac{\left|l\right|}{2}=\frac{\left|l\right|}{2}.
$$

Hence $\left|\frac1{f\left(x\right)}\right|<\frac2{\left|l\right|}$, i.e. $\frac1{f\left(x\right)}$ is bounded as $x\to{a}$. This is a corollary of Sign Preservation of Limits. $\blacksquare$
