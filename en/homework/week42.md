# Assignment 42

> **Definition** (Uniform Convergence of a Sequence of Functions) Let $\left\{f_n\left(x\right)\right\}$ be defined on a set $X$, and let $f\left(x\right)$ be a function on $X$. If for every $\varepsilon>0$ there exists a natural number $N$ such that whenever $n>N$, for all $x\in X$ we have $\left|f_n\left(x\right)-f\left(x\right)\right|<\varepsilon$, then $\left\{f_n\left(x\right)\right\}$ is said to converge uniformly to $f\left(x\right)$ on $X$.
>
> **Theorem 1.1** (The M-Test) Suppose there exists a sequence $M_n>0$ with $M_n\to 0$ such that $\left|f_n\left(x\right)-f\left(x\right)\right|\le M_n$ holds for all $x\in X$. Then $\left\{f_n\left(x\right)\right\}$ converges uniformly to $f\left(x\right)$ on $X$.
>
> **Theorem 1.2** (Continuity of the Limit Function) Let $\left\{f_n\left(x\right)\right\}$ converge uniformly to $f\left(x\right)$ on an interval $X$, and suppose each $f_n\left(x\right)$ is continuous on $X$. Then $f\left(x\right)$ is continuous on $X$.

### Problem 1

(Problem 11.1-1-1) Discuss the uniform convergence of the sequence of functions $f_n\left(x\right)=\frac{1}{1+nx}$, $x\in\left(0,1\right)$.

### Solution to Problem 1

For any fixed $x\in\left(0,1\right)$, as $n\to\infty$, $1+nx\to+\infty$, so $f_n\left(x\right)\to 0$, i.e. the limit function is $f\left(x\right)\equiv 0$.

Consider

$$
\sup_{0<x<1}\left|f_n\left(x\right)-0\right|=\sup_{0<x<1}\frac{1}{1+nx}.
$$

When $x\to 0^+$, $\frac{1}{1+nx}\to 1$, so this supremum equals $1$ (and does not tend to $0$). Take $\varepsilon_0=\frac12$. For any $n$, take $x_n=\frac{1}{n}\in\left(0,1\right)$. Then

$$
\left|f_n\left(x_n\right)-0\right|=\frac{1}{1+1}=\frac12=\varepsilon_0.
$$

By **Definition** (Uniform Convergence of a Sequence of Functions), it is impossible to find an $N$ such that whenever $n>N$, $\left|f_n\left(x\right)-0\right|<\varepsilon_0$ holds for all $x\in\left(0,1\right)$. Thus $\left\{f_n\left(x\right)\right\}$ does not converge uniformly to $0$ on $\left(0,1\right)$. $\blacksquare$

### Problem 2

(Problem 11.1-1-3) Discuss the uniform convergence of the sequence of functions $f_n\left(x\right)=\frac{\sin\left(nx+n\right)}{n}$, $x\in\left(-\infty,+\infty\right)$.

### Solution to Problem 2

For any $x\in\mathbb R$, $\left|\sin\left(nx+n\right)\right|\le 1$, so $f_n\left(x\right)\to 0$, and the limit function is $f\left(x\right)\equiv 0$. Moreover,

$$
\left|f_n\left(x\right)-f\left(x\right)\right|=\frac{\left|\sin\left(nx+n\right)\right|}{n}\le\frac{1}{n}=M_n,
$$

while $M_n=\frac1n\to 0$. By **Theorem 1.1** (The M-Test), $\left\{f_n\left(x\right)\right\}$ converges uniformly to $0$ on $\mathbb R$. $\blacksquare$

### Problem 3

(Problem 11.1-1-5) Discuss the uniform convergence of the sequence of functions $f_n\left(x\right)=nxe^{-nx^2}$, $x\in\left[0,1\right]$.

### Solution to Problem 3

For any fixed $x\in\left[0,1\right]$: when $x=0$, $f_n\left(0\right)=0$; when $x>0$, $nx^2\to+\infty$, so $nxe^{-nx^2}\to 0$. The limit function is $f\left(x\right)\equiv 0$.

Let $u=\sqrt{n}\,x$. Then

$$
f_n\left(x\right)=\sqrt n\,u\,e^{-u^2}, u\in\left[0,\sqrt n\right].
$$

The function $u e^{-u^2}$ attains its maximum $\frac{1}{\sqrt{2e}}$ at $u=\frac{1}{\sqrt2}$. Take $x_n=\frac{1}{\sqrt{2n}}\in\left[0,1\right]$. Then

$$
\left|f_n\left(x_n\right)-0\right|=\sqrt n\cdot\frac{1}{\sqrt2}e^{-1/2}=\sqrt{\frac{n}{2e}}\to+\infty.
$$

Hence $\sup_{x\in\left[0,1\right]}\left|f_n\left(x\right)-0\right|\not\to 0$. By **Definition** (Uniform Convergence of a Sequence of Functions), $\left\{f_n\left(x\right)\right\}$ does not converge uniformly to $0$ on $\left[0,1\right]$. $\blacksquare$

### Problem 4

(Problem 11.1-2) Let $f_n\left(x\right)$ converge uniformly to $f\left(x\right)$ on $\left(a,b\right)$. Suppose further that for each $n$, the limit $\lim_{x\to x_0}f_n\left(x\right)$ exists, where $x_0\in\left(a,b\right)$. Assuming that $\lim_{x\to x_0}f\left(x\right)$ exists, prove that
$$
\lim_{x\to x_0}f\left(x\right)=\lim_{n\to\infty}\left(\lim_{x\to x_0}f_n\left(x\right)\right).
$$

### Solution to Problem 4

This problem is a generalization of **Theorem 1.2** (Continuity of the Limit Function) to the case where the $f_n$ need not be continuous and only have a limit at $x_0$; the proof idea is the same as for **Theorem 1.2**. Write $A_n=\lim_{x\to x_0}f_n\left(x\right)$. For any $\varepsilon>0$, since $\left\{f_n\left(x\right)\right\}$ converges uniformly to $f\left(x\right)$ on $\left(a,b\right)$, there exists $N$ such that whenever $n>N$, for all $x\in\left(a,b\right)$ we have

$$
\left|f_n\left(x\right)-f\left(x\right)\right|<\frac{\varepsilon}{3}.
$$

Fix $m,n>N$. Letting $x\to x_0$, by the order-preserving property of limits,

$$
\left|A_m-A_n\right|=\lim_{x\to x_0}\left|f_m\left(x\right)-f_n\left(x\right)\right|\le\frac{2\varepsilon}{3}<\varepsilon.
$$

Hence $\left\{A_n\right\}$ is a Cauchy sequence, so there exists a finite limit $A=\lim_{n\to\infty}A_n$.

Now prove that $\lim_{x\to x_0}f\left(x\right)=A$. Fix $n>N$. Since $A_n=\lim_{x\to x_0}f_n\left(x\right)$, there exists $\delta>0$ such that whenever $0<\left|x-x_0\right|<\delta$,

$$
\left|f_n\left(x\right)-A_n\right|<\frac{\varepsilon}{3}.
$$

Then whenever $0<\left|x-x_0\right|<\delta$,

$$
\left|f\left(x\right)-A\right|\le \left|f\left(x\right)-f_n\left(x\right)\right|+\left|f_n\left(x\right)-A_n\right|+\left|A_n-A\right|<\frac{\varepsilon}{3}+\frac{\varepsilon}{3}+\frac{\varepsilon}{3}=\varepsilon.
$$

Hence

$$
\lim_{x\to x_0}f\left(x\right)=A=\lim_{n\to\infty}\left(\lim_{x\to x_0}f_n\left(x\right)\right).
$$

$\blacksquare$

### Problem 5

(Problem 11.1-3) Prove that $f_n\left(x\right)=\left(1+\frac{x}{n}\right)^n$ does not converge uniformly on $\left[0,+\infty\right)$ to the limit function $e^x$.

### Solution to Problem 5

For any fixed $x\in\left[0,+\infty\right)$, $\lim_{n\to\infty}\left(1+\frac{x}{n}\right)^n=e^x$, so the limit function is $f\left(x\right)=e^x$.

Take $x_n=n\in\left[0,+\infty\right)$. Then

$$
\left|f_n\left(x_n\right)-e^{x_n}\right|=\left|\left(1+1\right)^n-e^n\right|=\left|2^n-e^n\right|=e^n-2^n\to+\infty.
$$

Hence

$$
\sup_{x\in\left[0,+\infty\right)}\left|f_n\left(x\right)-e^x\right|\not\to 0,
$$

and by **Definition** (Uniform Convergence of a Sequence of Functions), $\left\{f_n\left(x\right)\right\}$ does not converge uniformly to $e^x$ on $\left[0,+\infty\right)$. $\blacksquare$

### Problem 6

(Problem 11.1-4) Prove that $f_n\left(x\right)=\left(1+\frac{x}{n}\right)^n$ converges uniformly to $e^x$ on every closed interval $\left[0,A\right]$, where $A>0$.

### Solution to Problem 6

For fixed $x\in\left[0,A\right]$, the limit function is $f\left(x\right)=e^x$. From the inequality $e^t\ge 1+t$ ($t\ge 0$), we have

$$
0\le e^x-\left(1+\frac{x}{n}\right)^n.
$$

Using the expansion $\ln\left(1+t\right)\le t$, we get

$$
n\ln\left(1+\frac{x}{n}\right)\le x,
$$

and hence $\left(1+\frac{x}{n}\right)^n\le e^x$. Moreover, from

$$
\ln\left(1+t\right)=t-\frac{t^2}{2\left(1+\xi\right)^2}\ge t-\frac{t^2}{2}\ \left(\xi\in\left[0,t\right]\right),
$$

for $x\in\left[0,A\right]$,

$$
n\ln\left(1+\frac{x}{n}\right)\ge n\left(\frac{x}{n}-\frac{x^2}{2n^2}\right)=x-\frac{x^2}{2n}\ge x-\frac{A^2}{2n}.
$$

Thus

$$
0\le e^x-\left(1+\frac{x}{n}\right)^n\le e^x\left(1-e^{-A^2/\left(2n\right)}\right)\le e^A\cdot\frac{A^2}{2n}=M_n,
$$

where $M_n=\frac{A^2e^A}{2n}\to 0$. By **Theorem 1.1** (The M-Test), $\left\{f_n\left(x\right)\right\}$ converges uniformly to $e^x$ on $\left[0,A\right]$. $\blacksquare$

### Problem 7

(Problem 11.1-5) Let both $f\left(x\right)$ and $f_n\left(x\right)$ be continuous functions on $\left[a,b\right]$. Set
$$
M_n=\max_{x\in\left[a,b\right]}\left|f_n\left(x\right)-f\left(x\right)\right|,
$$
Prove that $f_n\left(x\right)$ converges uniformly to $f\left(x\right)$ on $\left[a,b\right]$ if and only if $M_n\to 0$ ($n\to\infty$).

### Solution to Problem 7

(1) Necessity. Suppose $\left\{f_n\left(x\right)\right\}$ converges uniformly to $f\left(x\right)$ on $\left[a,b\right]$. For any $\varepsilon>0$, there exists $N$ such that whenever $n>N$, for all $x\in\left[a,b\right]$ we have $\left|f_n\left(x\right)-f\left(x\right)\right|<\varepsilon$. By continuity, the maximum is attained at some point $x_n\in\left[a,b\right]$, so

$$
M_n=\left|f_n\left(x_n\right)-f\left(x_n\right)\right|<\varepsilon.
$$

By the arbitrariness of $\varepsilon$, $M_n\to 0$.

(2) Sufficiency. Suppose $M_n\to 0$. For any $\varepsilon>0$, there exists $N$ such that whenever $n>N$, $M_n<\varepsilon$. Then for all $x\in\left[a,b\right]$,

$$
\left|f_n\left(x\right)-f\left(x\right)\right|\le M_n<\varepsilon.
$$

By **Definition** (Uniform Convergence of a Sequence of Functions), $\left\{f_n\left(x\right)\right\}$ converges uniformly to $f\left(x\right)$ on $\left[a,b\right]$. $\blacksquare$
