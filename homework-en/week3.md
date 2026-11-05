# week3

> **Proposition 1.6 (Properties of Absolute Value)**
> 
> For any $x,y\in\mathbb{R}$: (1) $\left|x\right|\ge0$, equality iff $x=0$; (2) $\left|-x\right|=\left|x\right|$; (3) $\left|x+y\right|\le\left|x\right|+\left|y\right|$.

> **Proposition 1.7 (Triangle Inequality)**
> 
> For any real $a,b,c$, $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **Proposition 2.1 (Necessary and Sufficient Condition for a Bounded Function)**
> 
> A function $f:X\to{Y}$ is bounded if and only if there exists $M>0$ such that $\left|f\left(x\right)\right|\le{M}$ for all $x\in{X}$.

> **Theorem 3.1 (Arithmetic of Limits)**
> 
> If $\left\{a_n\right\}$ and $\left\{b_n\right\}$ have limits $l_1$ and $l_2$ respectively, then $\lim\left(a_n\pm{b}_n\right)=l_1\pm{l}_2$, $\lim\left(a_n\cdot{b}_n\right)=l_1\cdot{l}_2$, and when $l_2\ne0$, $\lim\frac{a_n}{b_n}=\frac{l_1}{l_2}$.

> **Theorem 3.2 (Completeness of the Real Field)**
> 
> If $\left\{a_n\right\}$ is a monotone increasing sequence bounded above, then there exists $l\in\mathbb{R}$ such that $\left\{a_n\right\}$ converges to $l$.

> **Example 3.3 (The $n$-th Root of a Positive Number Tends to 1)**
> 
> If $a$ is any positive number, then $\lim_{n\to\infty}a^{1/n}=1$.

## 1.2-11

Let

$$
f\left(x\right)=\begin{cases}e^x,&x\le0,\\x,&x>0;\end{cases}\quad{g}\left(x\right)=\begin{cases}x,&x\le0,\\-x^2,&x>0;\end{cases}
$$

Find the piecewise expressions for $f\left(g\left(x\right)\right)$ and $g\left(f\left(x\right)\right)$, and compute $f\left(g\left(1\right)\right)$.

### Solution to 1.2-11

First find $f\left(g\left(x\right)\right)$. By Definition of a Composite Function:

- When $x\le0$, $g\left(x\right)=x\le0$, so $f\left(g\left(x\right)\right)=f\left(x\right)=e^x$;
- When $x>0$, $g\left(x\right)=-x^2<0$, so

$$
f\left(g\left(x\right)\right)=f\left(-x^2\right)=e^{-x^2}.
$$

Therefore

$$
f\left(g\left(x\right)\right)=\begin{cases}e^x,&x\le0,\\e^{-x^2},&x>0.\end{cases}
$$

Now find $g\left(f\left(x\right)\right)$:

- When $x\le0$, $f\left(x\right)=e^x>0$ (since $0<{}e^x\le1$ for $x\le0$), so

$$
g\left(f\left(x\right)\right)=g\left(e^x\right)=-\left(e^x\right)^2=-e^{2x};
$$

- When $x>0$, $f\left(x\right)=x>0$, so $g\left(f\left(x\right)\right)=g\left(x\right)=-x^2$.

Therefore

$$
g\left(f\left(x\right)\right)=\begin{cases}-e^{2x},&x\le0,\\-x^2,&x>0.\end{cases}
$$

Finally, $g\left(1\right)=-1^2=-1$, so

$$
f\left(g\left(1\right)\right)=f\left(-1\right)=e^{-1}=\frac1e.
$$

$\blacksquare$

## 1.2-14

Determine whether the following functions are bounded:

(1) $y=5\sin{e}^x+10^{10}$;

(2)

$$
y=\sqrt{x+10}-\sqrt{x}\quad\left(x>0\right);
$$

(3) $y=\operatorname{ch}x$;

(4)

$$
y=\ln\left(x+\sqrt{x^2+1}\right)\quad\left(x>0\right).
$$

### Solution to 1.2-14

(1) For any $x\in\mathbb{R}$, $\left|\sin{e}^x\right|\le1$, so $\left|5\sin{e}^x\right|\le5$, and thus

$$
\left|y\right|=\left|5\sin{e}^x+10^{10}\right|\le5+10^{10}.
$$

Taking $M=5+10^{10}$, by **Proposition 2.1 (Necessary and Sufficient Condition for a Bounded Function)**, $y=5\sin{e}^x+10^{10}$ is bounded.

(2) For $x>0$, rationalizing gives

$$
\sqrt{x+10}-\sqrt{x}=\frac{10}{\sqrt{x+10}+\sqrt{x}}.
$$

Since the denominator $\sqrt{x+10}+\sqrt{x}>\sqrt{10}$ ($x>0$), we have $0<{}y<\frac{10}{\sqrt{10}}=\sqrt{10}$. Taking $M=\sqrt{10}$, by **Proposition 2.1 (Necessary and Sufficient Condition for a Bounded Function)**, $y=\sqrt{x+10}-\sqrt{x}$ is bounded.

(3) $y=\operatorname{ch}x=\frac{e^x+e^{-x}}2$. As $x\to+\infty$, $e^x\to+\infty$, so $y\to+\infty$; there is no constant $M>0$ such that $\left|y\right|\le{M}$ for all $x\in\mathbb{R}$. By **Proposition 2.1 (Necessary and Sufficient Condition for a Bounded Function)**, $y=\operatorname{ch}x$ is not bounded.

(4) As $x\to+\infty$, $x+\sqrt{x^2+1}\sim2x$, so

$$
y=\ln\left(x+\sqrt{x^2+1}\right)\sim\ln\left(2x\right)\to+\infty,
$$

and there is no constant $M>0$ such that $\left|y\right|\le{M}$ for all $x>0$. By **Proposition 2.1 (Necessary and Sufficient Condition for a Bounded Function)**, $y=\ln\left(x+\sqrt{x^2+1}\right)$ is not bounded. $\blacksquare$

## 1.3-1-2

Prove by $\varepsilon$-$N$ language: $\lim_{n\to\infty}\frac{2n-5}{3n+100}=\frac23$.

### Solution to 1.3-1-2

Rewrite the general term as

$$
\frac{2n-5}{3n+100}=\frac{2-5/n}{3+100/n}.
$$

As $n\to\infty$, $5/n\to0$ and $100/n\to0$ (by Definition of Sequence Limit, for any $\varepsilon>0$, take $N>5/\varepsilon$ so that $\left|5/n\right|<\varepsilon$). By **Theorem 3.1 (Arithmetic of Limits)**,

$$
\lim_{n\to\infty}\frac{2n-5}{3n+100}=\frac{\lim\left(2-5/n\right)}{\lim\left(3+100/n\right)}=\frac23.
$$

$\blacksquare$

## 1.3-1-4

Prove by $\varepsilon$-$N$ language: $\lim_{n\to\infty}\frac{n!}{n^n}=0$.

### Solution to 1.3-1-4

For $n\ge1$,

$$
\frac{n!}{n^n}=\frac{1\cdot2\cdots{n}}{n\cdot{n}\cdots{n}}=\frac1n\cdot\frac2n\cdots\frac{n-1}{n}\cdot1\le\frac1n.
$$

Given $\varepsilon>0$, take $N=\left[\frac1\varepsilon\right]+1$. Then for $n>{}N$,

$$
\left|\frac{n!}{n^n}-0\right|\le\frac1n<\varepsilon.
$$

By Definition of Sequence Limit, $\lim_{n\to\infty}\frac{n!}{n^n}=0$. $\blacksquare$

## 1.3-1-6

Prove by $\varepsilon$-$N$ language: $\lim_{n\to\infty}\frac{n^2+1}{2n^2-7n}=\frac12$.

### Solution to 1.3-1-6

Rewrite the general term as

$$
\frac{n^2+1}{2n^2-7n}=\frac{1+1/n^2}{2-7/n}.
$$

As $n\to\infty$, $1/n^2\to0$ and $7/n\to0$. By **Theorem 3.1 (Arithmetic of Limits)**,

$$
\lim_{n\to\infty}\frac{n^2+1}{2n^2-7n}=\frac{\lim\left(1+1/n^2\right)}{\lim\left(2-7/n\right)}=\frac12.
$$

$\blacksquare$

## 1.3-1-8

Prove by $\varepsilon$-$N$ language:

$$
\lim_{n\to\infty}\left(\frac1{\left(n+1\right)^{3/2}}+\cdots+\frac1{\left(2n\right)^{3/2}}\right)=0.
$$

### Solution to 1.3-1-8

The sum has $n$ terms, each satisfying $\frac1{\left(n+k\right)^{3/2}}\le\frac1{n^{3/2}}$ ($1\le{k}\le{n}$), so

$$
0\le\frac1{\left(n+1\right)^{3/2}}+\cdots+\frac1{\left(2n\right)^{3/2}}\le\frac{n}{n^{3/2}}=\frac1{\sqrt{n}}.
$$

Given $\varepsilon>0$, take $N=\left[1/\varepsilon^2\right]+1$. Then for $n>{}N$, $\frac1{\sqrt{n}}<\varepsilon$. By Definition of Sequence Limit, the expression tends to $0$. $\blacksquare$

## 1.3-2-2

Find the limit:

$$
\lim_{n\to\infty}\left(\sqrt\left[n\right]{1}+\sqrt\left[n\right]{2}+\cdots+\sqrt\left[n\right]{100}\right).
$$

### Solution to 1.3-2-2

By **Example 3.3 (The $n$-th Root of a Positive Number Tends to 1)**, for each $k=1,2,\dots,100$,

$$
\lim_{n\to\infty}\sqrt\left[n\right]{k}=1.
$$

By the addition extension of **Theorem 3.1 (Arithmetic of Limits)** (finite terms),

$$
\lim_{n\to\infty}\left(\sqrt\left[n\right]{1}+\sqrt\left[n\right]{2}+\cdots+\sqrt\left[n\right]{100}\right)=\sum_{k=1}^{100}1=100.
$$

$\blacksquare$
