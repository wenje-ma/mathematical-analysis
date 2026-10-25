# Assignment 24

> **Theorem 2.1** (Upper/Lower Limits and Existence of the Limit) Let $\left\{a_n\right\}$ be a bounded sequence. Then the sequence $\left\{a_n\right\}$ has a limit if and only if its upper limit and lower limit are equal.

> **Theorem 2.2** (Cauchy Convergence Principle) The sequence $\left\{a_n\right\}$ has a limit if and only if: for any given $\varepsilon> 0$, there exists a natural number $N$ such that $\left|a_n-a_m\right|< \varepsilon$ (whenever $m\ge N,n\ge N$).
### Problem 1

(Problem 5.2-1) Use the Cauchy convergence principle for sequences to prove: if $\left\{a_n\right\}$ converges, then $\left\{\left|a_n\right|\right\}$ converges.

### Solution to Problem 1

Let $\lim\limits_{n\to\infty}a_n=l$. By the Cauchy convergence principle, for any $\varepsilon> 0$, there exists $N$ such that $\left|a_n-a_m\right|< \varepsilon$ whenever $m,n\ge N$.

By the triangle inequality,
$$
\left|\right|a_n\left|-\right|a_m\left|\right|\le\left|a_n-a_m\right|< \varepsilon.
$$

Hence $\left\{\left|a_n\right|\right\}$ satisfies the Cauchy condition. By **Theorem 2.2** (Cauchy Convergence Principle), $\left\{\left|a_n\right|\right\}$ converges. $\blacksquare$

### Problem 2

(Problem 5.2-2) Let $\left\{a_n\right\}$ and $\left\{b_n\right\}$ be two bounded sequences. Prove:
(1)

$$
\varlimsup\left(a_n+b_n\right)\le\varlimsup a_n+\varlimsup b_n;
$$

(2)

$$
\varliminf\left(a_n+b_n\right)\ge\varliminf a_n+\varliminf b_n.
$$

### Solution to Problem 2

(1) Set $A_n=\sup\left\{a_k:k\ge n\right\}$, $B_n=\sup\left\{b_k:k\ge n\right\}$. Then for any $k\ge n$,
$$
a_k+b_k\le A_n+B_n.
$$

Hence $A_n+B_n$ is an upper bound of $\left\{a_k+b_k:k\ge n\right\}$. Therefore
$$
\sup\left\{a_k+b_k:k\ge n\right\}\le A_n+B_n.
$$

Letting $n\to\infty$ and taking the limit gives
$$
\varlimsup\left(a_n+b_n\right)\le\varlimsup a_n+\varlimsup b_n.
$$

(2) Similarly, set $C_n=\inf\left\{a_k:k\ge n\right\}$, $D_n=\inf\left\{b_k:k\ge n\right\}$. Then for any $k\ge n$,
$$
a_k+b_k\ge C_n+D_n.
$$

Hence $C_n+D_n$ is a lower bound of $\left\{a_k+b_k:k\ge n\right\}$. Therefore
$$
\inf\left\{a_k+b_k:k\ge n\right\}\ge C_n+D_n.
$$

Letting $n\to\infty$ and taking the limit gives
$$
\varliminf\left(a_n+b_n\right)\ge\varliminf a_n+\varliminf b_n.
$$

$\blacksquare$
### Problem 3

(Problem 5.2-3) Find the upper and lower limits:
(1) $\varlimsup\limits_{x\to0}\sin\frac1x$ and $\varliminf\limits_{x\to0}\sin\frac1x$;

(2) $\varlimsup\limits_{x\to\infty}\sin x$ and $\varliminf\limits_{x\to\infty}\sin x$.

### Solution to Problem 3

(1) As $x\to0$, $\frac1x\to\infty$, and $\sin\frac1x$ oscillates infinitely often between $-1$ and $1$. In every sufficiently small neighborhood of $0$, $\sin\frac1x$ takes both the values $1$ and $-1$ (at $\frac1x=2k\pi+\frac{\pi}{2}$ and $\frac1x=2k\pi+\frac{3\pi}{2}$, respectively). Hence
$$
\varlimsup_{x\to0}\sin\frac1x=1,\varliminf_{x\to0}\sin\frac1x=-1.
$$

(2) As $x\to\infty$, $\sin x$ likewise oscillates infinitely often between $-1$ and $1$. In every neighborhood of infinity, $\sin x$ takes both the values $1$ and $-1$. Hence
$$
\varlimsup_{x\to\infty}\sin x=1,\varliminf_{x\to\infty}\sin x=-1.
$$

$\blacksquare$
### Problem 4

(Problem 5.2-6) Use the Cauchy convergence principle to prove that the following sequences converge:
(1)

$$
a_n=1-\frac12+\frac13-\cdots+\left(-1\right)^{n-1}\frac1n;
$$

(2)

$$
a_n=\frac{\sin1}{1!}+\frac{\sin2}{2!}+\cdots+\frac{\sin n}{n!}.
$$

### Solution to Problem 4

(1) Let $m> n$. Then
$$
\left|a_m-a_n\right|=\left|\frac{\left(-1\right)^n}{n+1}+\frac{\left(-1\right)^{n+1}}{n+2}+\cdots+\frac{\left(-1\right)^{m-1}}{m}\right|.
$$

This is the difference between partial sums of an alternating series. By the Leibniz criterion, this alternating series converges. Expressed via the Cauchy criterion:
$$
\left|a_m-a_n\right|\le\frac{1}{n+1}.
$$

For any $\varepsilon> 0$, take $N> \frac1\varepsilon$; then when $m,n> N$, $\left|a_m-a_n\right|< \varepsilon$. By **Theorem 2.2** (Cauchy Convergence Principle), $\left\{a_n\right\}$ converges.

(2) Let $m> n$. Then
$$
\left|a_m-a_n\right|=\left|\frac{\sin\left(n+1\right)}{\left(n+1\right)!}+\cdots+\frac{\sin m}{m!}\right|\le\frac{1}{\left(n+1\right)!}+\cdots+\frac{1}{m!}.
$$

When $n$ is sufficiently large, $\left(n+1\right)!> 2^{n+1}$, hence
$$
\left|a_m-a_n\right|\le\frac{1}{2^{n+1}}+\frac{1}{2^{n+2}}+\cdots=\frac{1}{2^n}.
$$

For any $\varepsilon> 0$, take $N$ such that $2^N> \frac1\varepsilon$; then when $m,n> N$, $\left|a_m-a_n\right|< \varepsilon$. By **Theorem 2.2** (Cauchy Convergence Principle), $\left\{a_n\right\}$ converges. $\blacksquare$

### Problem 5

(Problem 5.2-7) Let $f\left(x\right)$ be defined and bounded in a punctured neighborhood of $a$. Let $\left\{x_n\right\}$ be a sequence with limit $a$. Prove: if $\lim\limits_{n\to\infty}f\left(x_n\right)$ exists, then
$$
\varliminf_{x\to a}f\left(x\right)\le\lim_{n\to\infty}f\left(x_n\right)\le\varlimsup_{x\to a}f\left(x\right).
$$
### Solution to Problem 5

Set $l=\lim\limits_{n\to\infty}f\left(x_n\right)$. For any $\delta> 0$, when $n$ is sufficiently large

$$
x_n\in\left\{x:0< \left|x-a\right|< \delta\right\}.
$$

Hence
$$
\inf\left\{f\left(x\right):0< \left|x-a\right|< \delta\right\}\le f\left(x_n\right)\le\sup\left\{f\left(x\right):0< \left|x-a\right|< \delta\right\}.
$$

Letting $n\to\infty$, we get
$$
\inf\left\{f\left(x\right):0< \left|x-a\right|< \delta\right\}\le l\le\sup\left\{f\left(x\right):0< \left|x-a\right|< \delta\right\}.
$$

Then letting $\delta\to0$, by the definition of upper and lower limits,
$$
\varliminf_{x\to a}f\left(x\right)\le l\le\varlimsup_{x\to a}f\left(x\right).
$$

$\blacksquare$
### Problem 6

(Problem 5.2-8) Assume $f\left(x\right)$ is bounded in a punctured neighborhood of $a$. Prove that there exist sequences $\left\{x_n'\right\}$ and $\left\{x_n''\right\}$ such that $x_n'\to a$ ($n\to\infty$), $x_n''\to a$ ($n\to\infty$), and
$$
\lim_{n\to\infty}f\left(x_n'\right)=\varlimsup_{x\to a}f\left(x\right),\lim_{n\to\infty}f\left(x_n''\right)=\varliminf_{x\to a}f\left(x\right).
$$
### Solution to Problem 6

Set $L=\varlimsup_{x\to a}f\left(x\right)$. By the definition of the upper limit, for any $n$, there exists $x_n'$ in $\left\{x:0< \left|x-a\right|< 1/n\right\}$ such that
$$
f\left(x_n'\right)> \sup\left\{f\left(x\right):0< \left|x-a\right|< 1/n\right\}-\frac1n.
$$

Clearly $x_n'\to a$ ($n\to\infty$). Moreover,
$$
\sup\left\{f\left(x\right):0< \left|x-a\right|< 1/n\right\}-\frac1n< f\left(x_n'\right)\le\sup\left\{f\left(x\right):0< \left|x-a\right|< 1/n\right\}.
$$

Letting $n\to\infty$, by the squeeze theorem, $\lim\limits_{n\to\infty}f\left(x_n'\right)=L$.

The case of the lower limit is similar; take $x_n''$ such that

$$
f\left(x_n''\right)< \inf\left\{f\left(x\right):0< \left|x-a\right|< 1/n\right\}+\frac1n
$$

. $\blacksquare$

### Problem 7

(Problem 5.2-9) Use the above two problems to prove: as $x\to a$, $f\left(x\right)$ has a limit if and only if, for every sequence of points $x_n\to a$ ($n\to\infty$), the limit $\lim\limits_{n\to\infty}f\left(x_n\right)$ exists and is the same.

### Solution to Problem 7

**Necessity** Let $\lim\limits_{x\to a}f\left(x\right)=l$. For any $x_n\to a$, by the relationship between function limits and sequence limits, $\lim\limits_{n\to\infty}f\left(x_n\right)=l$.

**Sufficiency** Assume that for any $x_n\to a$, $\lim f\left(x_n\right)$ exists and is the same. By Problem 6 (the 8th problem), there exists $x_n'\to a$ such that $\lim f\left(x_n'\right)=\varlimsup f\left(x\right)$, and there exists $x_n''\to a$ such that $\lim f\left(x_n''\right)=\varliminf f\left(x\right)$. By assumption, these two limits are equal, i.e.
$$
\varlimsup_{x\to a}f\left(x\right)=\varliminf_{x\to a}f\left(x\right).
$$

By **Theorem 2.1** (Upper/Lower Limits and Existence of the Limit), $\lim\limits_{x\to a}f\left(x\right)$ exists. $\blacksquare$
