# Assignment 46

> **Definition** (Convergence of an Improper Integral) Let the function $f\left(x\right)$ be defined on $\left[a,+\infty\right)$ and integrable on every closed interval $\left[a,A\right]$. If the limit $\lim_{A\to+\infty}\int_a^A f\left(x\right)\,\mathrm{d}x$ exists, then the improper integral $\int_a^{+\infty} f\left(x\right)\,\mathrm{d}x$ is said to converge, and this limit is defined to be the value of the improper integral; otherwise it is said to diverge.

> **Example 1.2** (The $p$-Integral) The improper integral $\int_1^{+\infty}\frac{\mathrm{d}x}{x^p}$ converges when $p> 1$ and diverges when $p\le 1$.

> **Theorem 1.1** (Cauchy Convergence Principle for Improper Integrals) Let $f\left(x\right)$ be defined on $\left[a,+\infty\right)$ and integrable on every closed interval $\left[a,A\right]$. Then $\int_a^{+\infty} f\left(x\right)\,\mathrm{d}x$ converges if and only if: for every given $\varepsilon> 0$, there exists $X> 0$ such that $\left|\int_{A'}^{A''} f\left(x\right)\,\mathrm{d}x\right|< \varepsilon$, whenever $A'> X,A''> X$.

> **Theorem 1.3** (Comparison Test) Let $f\left(x\right)$ and $g\left(x\right)$ be defined on $\left[a,+\infty\right)$ and integrable on every closed interval $\left[a,A\right]$. Suppose further that there exists $X_0> a$ such that
> $$
> 0\le f\left(x\right)\le g\left(x\right)\left(\forall x\ge X_0\right).
> $$
> Then if $\int_a^{+\infty}g\left(x\right)\,\mathrm{d}x$ converges, necessarily $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ converges; and if $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ diverges, necessarily $\int_a^{+\infty}g\left(x\right)\,\mathrm{d}x$ diverges.

> **Theorem 1.6** (Dirichlet's Test) Let $f\left(x\right)$ and $g\left(x\right)$ be defined on $\left[a,+\infty\right)$ and integrable on every interval $\left[a,A\right]$. If $f\left(x\right)$ is monotone on $\left[a,+\infty\right)$ and $\lim_{x\to+\infty}f\left(x\right)=0$; and if for every $A> a$, the integral $\int_a^A g\left(x\right)\,\mathrm{d}x$ is bounded, then the improper integral $\int_a^{+\infty}f\left(x\right)g\left(x\right)\,\mathrm{d}x$ converges.

> **Definition** (Absolute and Conditional Convergence) If $\int_a^{+\infty}\left| f\left(x\right)\right|\,\mathrm{d}x$ converges, then the improper integral $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ is said to converge absolutely; if $\int_a^{+\infty}f\left(x\right)\,\mathrm{d}x$ converges but $\int_a^{+\infty}\left| f\left(x\right)\right|\,\mathrm{d}x$ diverges, then it is said to converge conditionally.

### Problem 1

(Problem 12.1-1-1) Determine whether the improper integral $\displaystyle\int_1^{+\infty}\frac{\ln x}{x^2}\,\mathrm{d}x$ converges; if it converges, find its value.

### Solution to Problem 1

For any $A> 1$, integrating by parts (taking $u=\ln x,\mathrm{d}v=\frac{\mathrm{d}x}{x^2}$) gives

$$
\int_1^A \frac{\ln x}{x^2}\,\mathrm{d}x=\left[-\frac{\ln x}{x}\right]_1^A+\int_1^A\frac{\mathrm{d}x}{x^2}=-\frac{\ln A}{A}+1-\frac1A.
$$

Since $\lim_{A\to+\infty}\frac{\ln A}{A}=0$ and $\frac1A\to0$, the right side tends to $1$. Hence by **Definition** (Convergence of an Improper Integral), this improper integral converges, and its value is $1$. $\blacksquare$

### Problem 2

(Problem 12.1-1-2) Determine whether the improper integral $\displaystyle\int_1^{+\infty} e^{-ax}\,\mathrm{d}x$ ($a> 0$) converges; if it converges, find its value.

### Solution to Problem 2

For any $A> 1$,

$$
\int_1^A e^{-ax}\,\mathrm{d}x=\left[-\frac{e^{-ax}}{a}\right]_1^A=\frac{e^{-a}-e^{-aA}}{a}.
$$

Since $a> 0$, we have $e^{-aA}\to0\left(A\to+\infty\right)$, and the right side tends to $\frac{e^{-a}}{a}$. Hence by **Definition** (Convergence of an Improper Integral), this improper integral converges, and its value is $\frac{e^{-a}}{a}$. $\blacksquare$

### Problem 3

(Problem 12.1-1-3) Determine whether the improper integral $\displaystyle\int_0^{+\infty}\frac{\mathrm{d}x}{1+x^2}$ converges; if it converges, find its value.

### Solution to Problem 3

For any $A> 0$,

$$
\int_0^A\frac{\mathrm{d}x}{1+x^2}=\left[\arctan x\right]_0^A=\arctan A.
$$

As $A\to+\infty$, $\arctan A\to\frac{\pi}{2}$. Hence by **Definition** (Convergence of an Improper Integral), this improper integral converges, and its value is $\frac{\pi}{2}$. $\blacksquare$

### Problem 4

(Problem 12.1-1-4) Determine whether the improper integral $\displaystyle\int_0^{+\infty}x e^{-x}\,\mathrm{d}x$ converges; if it converges, find its value.

### Solution to Problem 4

For any $A> 0$, integrating by parts (taking $u=x,\mathrm{d}v=e^{-x}\,\mathrm{d}x$) gives

$$
\int_0^A x e^{-x}\,\mathrm{d}x=\left[-x e^{-x}\right]_0^A+\int_0^A e^{-x}\,\mathrm{d}x=-A e^{-A}+1-e^{-A}.
$$

As $A\to+\infty$, $A e^{-A}\to0$ and $e^{-A}\to0$, so the right side tends to $1$. Hence by **Definition** (Convergence of an Improper Integral), this improper integral converges, and its value is $1$. $\blacksquare$

### Problem 5

(Problem 12.1-2-1) Discuss the absolute and conditional convergence of the improper integral $\displaystyle\int_1^{+\infty}\frac{\sin x}{x^p}\,\mathrm{d}x$.

### Solution to Problem 5

Consider three cases.

(1) $p> 1$. Since $\left|\frac{\sin x}{x^p}\right|\le\frac1{x^p}$, and by **Example 1.2** (The $p$-Integral), $\int_1^{+\infty}\frac{\mathrm{d}x}{x^p}$ converges. By **Theorem 1.3** (Comparison Test), $\int_1^{+\infty}\left|\frac{\sin x}{x^p}\right|\,\mathrm{d}x$ converges, so the original improper integral converges absolutely.

(2) $0< p\le1$. First, $f\left(x\right)=\frac1{x^p}$ is monotonically decreasing on $\left[1,+\infty\right)$ and tends to $0$; and for any $A> 1$,

$$
\left|\int_1^A\sin x\,\mathrm{d}x\right|=\left|\cos1-\cos A\right|\le2
$$

is bounded. By **Theorem 1.6** (Dirichlet's Test), $\int_1^{+\infty}\frac{\sin x}{x^p}\,\mathrm{d}x$ converges.

Second, it does not converge absolutely. Indeed,

$$
\frac{\left|\sin x\right|}{x^p}\ge\frac{\sin^2 x}{x^p}=\frac{1-\cos2x}{2x^p}=\frac{1}{2x^p}-\frac{\cos2x}{2x^p}.
$$

By **Example 1.2** (The $p$-Integral), $\int_1^{+\infty}\frac{\mathrm{d}x}{x^p}$ diverges when $p\le1$; while $\int_1^{+\infty}\frac{\cos2x}{2x^p}\,\mathrm{d}x$ converges by **Theorem 1.6** (Dirichlet's Test) ($\frac1{x^p}$ decreases monotonically to $0$, and $\int_1^A\cos2x\,\mathrm{d}x$ is bounded). Hence $\int_1^{+\infty}\left|\frac{\sin x}{x^p}\right|\,\mathrm{d}x$ diverges. By **Definition** (Absolute and Conditional Convergence), the original improper integral converges conditionally.

(3) $p\le0$. Then $x^{-p}\ge1\left(x\ge1\right)$. Take $A'_n=2n\pi-\frac{\pi}{4}$, $A''_n=2n\pi+\frac{\pi}{4}$. Then on $\left[A'_n,A''_n\right]$, $\sin x\ge\frac{\sqrt2}{2}$, and hence

$$
\biggl\left|\int_{A'_n}^{A''_n}\frac{\sin x}{x^p}\,\mathrm{d}x\biggr\right|\ge\frac{\sqrt2}{2}\cdot\frac{\pi}{2}=\frac{\sqrt2\pi}{4}> 0,
$$

and this lower bound is a positive constant independent of $n$, which does not tend to $0$ as $A'_n,A''_n\to+\infty$. By **Theorem 1.1** (Cauchy Convergence Principle), the original improper integral diverges. $\blacksquare$

### Problem 6

(Problem 12.1-2-3) Discuss the absolute and conditional convergence of the improper integral $\displaystyle\int_1^{+\infty}\frac{\sqrt x\cos x}{x+3}\,\mathrm{d}x$.

### Solution to Problem 6

Let $f\left(x\right)=\frac{\sqrt x}{x+3}$. When $x> 3$,

$$
f'\left(x\right)=\frac{\left(x+3\right)-2x}{2\sqrt x\,\left(x+3\right)^2}=\frac{3-x}{2\sqrt x\,\left(x+3\right)^2}< 0,
$$

so $f\left(x\right)$ is monotonically decreasing on $\left[3,+\infty\right)$; moreover,

$$
f\left(x\right)\sim\frac1{\sqrt x}\to0\left(x\to+\infty\right).
$$
And for any $A> 1$,

$$
\left|\int_1^A\cos x\,\mathrm{d}x\right|=\left|\sin A-\sin1\right|\le2
$$

is bounded. By **Theorem 1.6** (Dirichlet's Test), the original improper integral converges.

Second, it does not converge absolutely. For $x\ge1$, $x+3\le4x$, so $f\left(x\right)=\frac{\sqrt x}{x+3}\ge\frac1{4\sqrt x}$. Thus

$$
\frac{\sqrt x\,\left|\cos x\right|}{x+3}\ge\frac{\left|\cos x\right|}{4\sqrt x}\ge\frac{\cos^2 x}{4\sqrt x}=\frac{1}{8\sqrt x}+\frac{\cos2x}{8\sqrt x}.
$$

By **Example 1.2** (The $p$-Integral), $\int_1^{+\infty}\frac{\mathrm{d}x}{\sqrt x}$ diverges ($p=\frac12\le1$); while $\int_1^{+\infty}\frac{\cos2x}{8\sqrt x}\,\mathrm{d}x$ converges by **Theorem 1.6** (Dirichlet's Test). Hence $\int_1^{+\infty}\frac{\sqrt x\,\left|\cos x\right|}{x+3}\,\mathrm{d}x$ diverges. By **Definition** (Absolute and Conditional Convergence), the original improper integral converges conditionally. $\blacksquare$

### Problem 7

(Problem 12.1-2-5) Discuss the absolute and conditional convergence of the improper integral $\displaystyle\int_0^{+\infty}\sin x^2\,\mathrm{d}x$.

### Solution to Problem 7

On $\left[0,1\right]$, $\sin x^2\sim x^2$, which is integrable. On $\left[1,+\infty\right)$, make the substitution $t=x^2$, so that $\mathrm{d}x=\frac{\mathrm{d}t}{2\sqrt t}$. Then

$$
\int_1^{+\infty}\sin x^2\,\mathrm{d}x=\frac12\int_1^{+\infty}\frac{\sin t}{\sqrt t}\,\mathrm{d}t.
$$

The function $\frac1{\sqrt t}$ is monotonically decreasing on $\left[1,+\infty\right)$ and tends to $0$, while

$$
\int_1^B\sin t\,\mathrm{d}t=\cos1-\cos B
$$

is bounded. By **Theorem 1.6** (Dirichlet's Test), the integral on the right converges, so the original improper integral converges.

Second, it does not converge absolutely. With the same substitution,

$$
\int_1^{+\infty}\left|\sin x^2\right|\,\mathrm{d}x=\frac12\int_1^{+\infty}\frac{\left|\sin t\right|}{\sqrt t}\,\mathrm{d}t,
$$

while

$$
\left|\sin t\right|/\sqrt t\ge\sin^2 t/\sqrt t=\frac{1}{2\sqrt t}-\frac{\cos2t}{2\sqrt t},
$$

where $\int_1^{+\infty}\frac{\mathrm{d}t}{\sqrt t}$ diverges by **Example 1.2** (The $p$-Integral), and $\int_1^{+\infty}\frac{\cos2t}{2\sqrt t}\,\mathrm{d}t$ converges by **Theorem 1.6**. Hence the integral on the right diverges, and the original improper integral does not converge absolutely. By **Definition** (Absolute and Conditional Convergence), the original improper integral converges conditionally. $\blacksquare$

### Problem 8

(Problem 12.1-3) Let

$$
\displaystyle I_1\left(x\right)=\int_0^{+\infty}e^{-xt}\sin t\,\mathrm{d}t,I_2\left(x\right)=\int_0^{+\infty}e^{-xt}\cos t\,\mathrm{d}t,
$$

where $x\in\left(0,+\infty\right)$. Prove that these two improper integrals converge absolutely, and find their values.

### Solution to Problem 8

First prove absolute convergence. For $t\ge0$, we have $\left| e^{-xt}\sin t\right|\le e^{-xt}$ and $\left| e^{-xt}\cos t\right|\le e^{-xt}$, while

$$
\int_0^{+\infty}e^{-xt}\,\mathrm{d}x=\lim_{A\to+\infty}\frac{1-e^{-xA}}{x}=\frac1x
$$

converges. By **Theorem 1.3** (Comparison Test), both $I_1\left(x\right)$ and $I_2\left(x\right)$ converge absolutely.

Now find their values. Integrating $I_2$ by parts (taking $u=\cos t,\mathrm{d}v=e^{-xt}\,\mathrm{d}t$), noting that

$$
e^{-xt}\cos t\big|_{0}^{+\infty}=0-\left(-\frac1x\right)=\frac1x,
$$

we get

$$
I_2\left(x\right)=\frac1x-\frac1x I_1\left(x\right).
$$

Integrating $I_1$ by parts (taking $u=\sin t,\mathrm{d}v=e^{-xt}\,\mathrm{d}t$), noting that $e^{-xt}\sin t\big|_0^{+\infty}=0$, we get

$$
I_1\left(x\right)=\frac1x I_2\left(x\right).
$$

Substituting the second equation into the first: $I_2=\frac1x-\frac1{x}\cdot\frac{I_2}{x}$, i.e. $\left(1+\frac1{x^2}\right)I_2=\frac1x$, which gives $I_2\left(x\right)=\frac{x}{x^2+1}$; substituting back gives $I_1\left(x\right)=\frac1{x^2+1}$. Hence

$$
I_1\left(x\right)=\frac{1}{x^2+1}, I_2\left(x\right)=\frac{x}{x^2+1}.

$$

$\blacksquare$
### Problem 9

(Problem 12.1-4) Let $f\left(x\right)$ be continuous on $\left(-\infty,+\infty\right)$, and suppose $\displaystyle\int_{-\infty}^{+\infty}f\left(x\right)\,\mathrm{d}x$ converges. Prove that:
(1)

$$
\displaystyle\int_{-\infty}^{+\infty}f\left(-x\right)\,\mathrm{d}x=\int_{-\infty}^{+\infty}f\left(x\right)\,\mathrm{d}x;
$$

(2)

$$
\displaystyle\int_{-\infty}^{+\infty}f\left(x+a\right)\,\mathrm{d}x=\int_{-\infty}^{+\infty}f\left(x\right)\,\mathrm{d}x\left(a\in\mathbb R\right).
$$

### Solution to Problem 9

(1) Make the substitution $u=-x$, so that $\mathrm{d}x=-\mathrm{d}u$. Then

$$
\int_{-B}^{A}f\left(-x\right)\,\mathrm{d}x=\int_{B}^{-A}f\left(u\right)\left(-\mathrm{d}u\right)=\int_{-A}^{B}f\left(u\right)\,\mathrm{d}u.
$$

Letting $A,B\to+\infty$, by **Definition** (Convergence of an Improper Integral) and the convergence of $\int_{-\infty}^{+\infty}f\left(u\right)\,\mathrm{d}u$, the right side tends to $\int_{-\infty}^{+\infty}f\left(u\right)\,\mathrm{d}u$, and the left side tends to $\int_{-\infty}^{+\infty}f\left(-x\right)\,\mathrm{d}x$, so the two are equal.

(2) Make the substitution $u=x+a$, so that $\mathrm{d}x=\mathrm{d}u$. Then

$$
\int_{-B}^{A}f\left(x+a\right)\,\mathrm{d}x=\int_{a-B}^{a+A}f\left(u\right)\,\mathrm{d}u.
$$

Letting $A,B\to+\infty$, the upper and lower limits independently tend to $+\infty$ and $-\infty$. By the assumed convergence of the improper integral, the right side tends to $\int_{-\infty}^{+\infty}f\left(u\right)\,\mathrm{d}u$. Hence

$$
\int_{-\infty}^{+\infty}f\left(x+a\right)\,\mathrm{d}x=\int_{-\infty}^{+\infty}f\left(x\right)\,\mathrm{d}x.
$$

$\blacksquare$

### Problem 10

(Problem 12.1-5) Let $f\left(x\right)$ be defined on $\left[1,+\infty\right)$ and integrable on every interval $\left[1,A\right]$. Suppose $\lim_{x\to+\infty}f\left(x\right)=0$, and set

$$
a_n=\displaystyle\int_n^{n+1}f\left(x\right)\,\mathrm{d}x,n=1,2,\cdots.
$$

Prove that $\displaystyle\int_1^{+\infty}f\left(x\right)\,\mathrm{d}x$ converges if and only if $\displaystyle\sum_{n=1}^{\infty}a_n$ converges.

### Solution to Problem 10

Write $F\left(A\right)=\int_1^A f\left(x\right)\,\mathrm{d}x$. For any positive integer $N$,

$$
\sum_{n=1}^{N}a_n=\sum_{n=1}^{N}\int_n^{n+1}f\left(x\right)\,\mathrm{d}x=\int_1^{N+1}f\left(x\right)\,\mathrm{d}x=F\left(N+1\right).
$$

($\Rightarrow$) If $\int_1^{+\infty}f\left(x\right)\,\mathrm{d}x$ converges, i.e. $F\left(A\right)\to L\left(A\to+\infty\right)$, then $F\left(N+1\right)\to L$, i.e. the series $\sum_{n=1}^{\infty}a_n$ converges, with sum $L$.

($\Leftarrow$) If $\sum_{n=1}^{\infty}a_n$ converges, i.e.

$$
F\left(N+1\right)\to L\left(N\to+\infty\right).
$$

Now prove that $F\left(A\right)\to L$ for arbitrary $A\to+\infty$. For any $A\ge1$, take $N=\left[A\right]$, so that $N\le A< N+1$. Then

$$
F\left(A\right)-L=\left(F\left(N+1\right)-L\right)+\left(F\left(A\right)-F\left(N+1\right)\right)=\left(F\left(N+1\right)-L\right)-\int_A^{N+1}f\left(x\right)\,\mathrm{d}x.
$$

Since $f\left(x\right)\to0\left(x\to+\infty\right)$, for any $\varepsilon> 0$ there exists $X> 0$ such that $\left| f\left(x\right)\right|< \varepsilon$ whenever $x> X$. When $N$ is sufficiently large, $\left[A,N+1\right]\subset\left[X,+\infty\right)$, so

$$
\biggl\left|\int_A^{N+1}f\left(x\right)\,\mathrm{d}x\biggr\right|\le\int_A^{N+1}\left| f\left(x\right)\right|\,\mathrm{d}x< \varepsilon\,\left(N+1-A\right)\le\varepsilon.
$$

At the same time, $F\left(N+1\right)-L\to0$. Therefore $F\left(A\right)-L\to0$, i.e. $F\left(A\right)\to L$. By **Definition** (Convergence of an Improper Integral), $\int_1^{+\infty}f\left(x\right)\,\mathrm{d}x$ converges. $\blacksquare$
