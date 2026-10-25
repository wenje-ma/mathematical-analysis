# Assignment 13

> **Theorem 1.1** (Fermat's Theorem) Let $f\left(x\right)$ be defined near a point $a$ and be differentiable at $a$. If $a$ is an extremum point of $y=f\left(x\right)$, then $f'\left(a\right)=0$.

> **Theorem 1.2** (Rolle's Theorem) Let the function $y=f\left(x\right)$ be continuous on the closed interval $\left[a,b\right]$, differentiable at every point of $\left(a,b\right)$, and satisfy $f\left(a\right)=f\left(b\right)$. Then there exists at least one point $c$ in $\left(a,b\right)$ such that $f'\left(c\right)=0$.

> **Theorem 1.3** (Lagrange Mean Value Theorem) Let $y=f\left(x\right)$ be continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$. Then there exists a point $c\in\left(a,b\right)$ such that
> $$
> f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}.
> $$
> **Theorem 1.4** (Constant Function Theorem) Let $y=f\left(x\right)$ be differentiable at every point of $\left(a,b\right)$, with $f'\left(x\right)=0$ ($x\in\left(a,b\right)$). Then $y=f\left(x\right)$ must be constant on $\left(a,b\right)$.

> **Theorem 1.5** (Monotonicity Criterion) Let $y=f\left(x\right)$ be continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$. If $f'\left(x\right)> 0$ ($\ge 0$) $\forall x\in\left(a,b\right)$, then $y=f\left(x\right)$ is strictly increasing (increasing) on $\left[a,b\right]$; if $f'\left(x\right)< 0$ ($\le 0$) $\forall x\in\left(a,b\right)$, then $y=f\left(x\right)$ is strictly decreasing (decreasing) on $\left[a,b\right]$.

### Problem 1

(Problem 3.1-1) Let $y=f\left(x\right)$ be differentiable on $\left(-\infty,+\infty\right)$, and suppose $\lim\limits_{x\to-\infty}f\left(x\right)=\lim\limits_{x\to+\infty}f\left(x\right)$. Prove that there exists a point $c\in\left(-\infty,+\infty\right)$ such that $f'\left(c\right)=0$.

### Solution to Problem 1

Set

$$
l=\lim_{x\to-\infty}f\left(x\right)=\lim_{x\to+\infty}f\left(x\right).
$$

Consider two cases.

If $f\left(x\right)\equiv l$, then $f'\left(x\right)\equiv0$, and the conclusion is obvious.

If $f$ is not identically $l$, then there exists $x_0$ such that $f\left(x_0\right)\ne l$. Without loss of generality suppose $f\left(x_0\right)> l$ (the case $f\left(x_0\right)< l$ is analogous). Since $\lim_{x\to\pm\infty}f\left(x\right)=l$, take $\varepsilon=\frac{f\left(x_0\right)-l}{2}> 0$. Then there exists $A> \left|x_0\right|$ such that $\left|f\left(x\right)-l\right|< \varepsilon$ when $\left|x\right|> A$, i.e.
$$
f\left(x\right)< l+\varepsilon=\frac{f\left(x_0\right)+l}{2}< f\left(x_0\right).
$$
Consider the continuous function $f$ on the closed interval $\left[-A,A\right]$. Since $f\left(-A\right)< f\left(x_0\right)$ and $f\left(A\right)< f\left(x_0\right)$, while $x_0\in\left(-A,A\right)$, the maximum of $f$ on $\left[-A,A\right]$ is attained not at the endpoints $-A$ or $A$ but at some point $c\in\left(-A,A\right)$. Hence $c$ is a local maximum point. Moreover $f$ is differentiable on $\left(-A,A\right)$, so by **Theorem 1.1** (Fermat's Theorem), $f'\left(c\right)=0$. $\blacksquare$

### Problem 2

(Problem 3.1-2) Let $p\left(x\right)=x^n+qx+r$ ($n$ a positive integer, $q,r$ real numbers). Prove that when $n$ is even, there are at most two real roots; when $n$ is odd, at most three real roots.

### Solution to Problem 2

Proof by contradiction. Let $n$ be even, and suppose $p\left(x\right)$ has at least three distinct real roots $x_1< x_2< x_3$. By **Theorem 1.2** (Rolle's Theorem), there exist points $\xi_1,\xi_2$ in $\left(x_1,x_2\right)$ and $\left(x_2,x_3\right)$ respectively, such that
$$
p'\left(\xi_1\right)=0, p'\left(\xi_2\right)=0.
$$
But $p'\left(x\right)=nx^{n-1}+q$. Since $n$ is even, $n-1$ is odd, and the equation $nx^{n-1}+q=0$ has at most one real root (the odd power $x^{n-1}$ is strictly increasing). This contradicts $p'\left(\xi_1\right)=p'\left(\xi_2\right)=0$ with $\xi_1\ne\xi_2$. Hence when $n$ is even, $p\left(x\right)$ has at most two real roots.

Let $n$ be odd, and suppose $p\left(x\right)$ has at least four distinct real roots $x_1< x_2< x_3< x_4$. By **Theorem 1.2** (Rolle's Theorem), there exist $\xi_1,\xi_2,\xi_3$ in $\left(x_1,x_2\right),\left(x_2,x_3\right),\left(x_3,x_4\right)$ respectively, such that

$$
p'\left(\xi_1\right)=p'\left(\xi_2\right)=p'\left(\xi_3\right)=0.
$$

Applying **Theorem 1.2** (Rolle's Theorem) again to $p'\left(x\right)$, there exist $\eta_1,\eta_2$ in $\left(\xi_1,\xi_2\right)$ and $\left(\xi_2,\xi_3\right)$ respectively, such that
$$
p''\left(\eta_1\right)=0, p''\left(\eta_2\right)=0.
$$
But $p''\left(x\right)=n\left(n-1\right)x^{n-2}$. Since $n$ is odd, $n-2$ is also odd, and the equation $n\left(n-1\right)x^{n-2}=0$ has only one real root $x=0$. This contradicts $p''\left(\eta_1\right)=p''\left(\eta_2\right)=0$ with $\eta_1\ne\eta_2$. Hence when $n$ is odd, $p\left(x\right)$ has at most three real roots. $\blacksquare$

### Problem 3

(Problem 3.1-4) Determine the monotonicity intervals of the following functions:
(1) $f\left(x\right)=xe^x$;

(2) $f\left(x\right)=\frac{x^2-1}{x}$;

(3) $f\left(x\right)=\sqrt{x-2}$;

(4) $f\left(x\right)=x^4-x+1$.

### Solution to Problem 3

(1)

$$
f'\left(x\right)=e^x+xe^x=\left(1+x\right)e^x.
$$

Since $e^x> 0$ always, the sign of $f'\left(x\right)$ is determined by $1+x$. When $x< -1$, $f'\left(x\right)< 0$; when $x> -1$, $f'\left(x\right)> 0$. By **Theorem 1.5** (Monotonicity Criterion), $f\left(x\right)$ is strictly decreasing on $\left(-\infty,-1\right]$ and strictly increasing on $\left[-1,+\infty\right)$.

(2) $f\left(x\right)=x-\frac1x$, domain $\left(-\infty,0\right)\cup\left(0,+\infty\right)$. $f'\left(x\right)=1+\frac1{x^2}> 0$ always. By **Theorem 1.5** (Monotonicity Criterion), $f\left(x\right)$ is strictly increasing on $\left(-\infty,0\right)$ and strictly increasing on $\left(0,+\infty\right)$.

(3) Domain $\left[2,+\infty\right)$. $f'\left(x\right)=\frac{1}{2\sqrt{x-2}}> 0$ ($x> 2$). By **Theorem 1.5** (Monotonicity Criterion), $f\left(x\right)$ is strictly increasing on $\left[2,+\infty\right)$.

(4) $f'\left(x\right)=4x^3-1$. Setting $f'\left(x\right)=0$ gives

$$
x=\sqrt\left[3\right]{\frac14}.
$$
When

$$
x< \sqrt\left[3\right]{\frac14}
$$
$f'\left(x\right)< 0$, and when

$$
x> \sqrt\left[3\right]{\frac14}
$$
$f'\left(x\right)> 0$. By **Theorem 1.5** (Monotonicity Criterion), $f\left(x\right)$ is on

$$
\left(-\infty,\sqrt\left[3\right]{\frac14}\right]
$$
strictly decreasing, and on

$$
\left[\sqrt\left[3\right]{\frac14},+\infty\right)
$$

strictly increasing. $\blacksquare$

### Problem 4

(Problem 3.1-5) Let $f\left(x\right)$ and $g\left(x\right)$ be continuous on $\left[a,b\right]$, differentiable on $\left(a,b\right)$, with $f'\left(x\right)> g'\left(x\right)$. Suppose $f\left(a\right)=g\left(a\right)$. Prove that $f\left(x\right)> g\left(x\right)$ for $x\in\left(a,b\right]$.

### Solution to Problem 4

Set $h\left(x\right)=f\left(x\right)-g\left(x\right)$. By assumption, $h\left(x\right)$ is continuous on $\left[a,b\right]$, differentiable on $\left(a,b\right)$, and
$$
h'\left(x\right)=f'\left(x\right)-g'\left(x\right)> 0\left(\forall x\in\left(a,b\right)\right).
$$
By **Theorem 1.5** (Monotonicity Criterion), $h\left(x\right)$ is strictly increasing on $\left[a,b\right]$. Moreover $h\left(a\right)=f\left(a\right)-g\left(a\right)=0$, so for any $x\in\left(a,b\right]$,
$$
h\left(x\right)> h\left(a\right)=0,
$$
i.e. $f\left(x\right)-g\left(x\right)> 0$, i.e. $f\left(x\right)> g\left(x\right)$. $\blacksquare$

### Problem 5

(Problem 3.1-6) Prove the following inequalities:
(1) $\ln\left(1+x\right)< x$ ($x> 0$);

(2) $\cos x> 1-\frac{x^2}{2}$ ($x\ne0$);

(3) $\sin x< x$ ($x> 0$);

(4) $\tan x> x$ ($0< x< \frac{\pi}{2}$).

### Solution to Problem 5

(1) Set $f\left(x\right)=\ln\left(1+x\right)-x$. Then $f\left(0\right)=0$, and
$$
f'\left(x\right)=\frac{1}{1+x}-1=-\frac{x}{1+x}< 0\left(x> 0\right).
$$
By **Theorem 1.5** (Monotonicity Criterion), $f\left(x\right)$ is strictly decreasing on $\left[0,+\infty\right)$. Hence when $x> 0$, $f\left(x\right)< f\left(0\right)=0$, i.e. $\ln\left(1+x\right)-x< 0$, i.e. $\ln\left(1+x\right)< x$.

(2) Set $f\left(x\right)=\cos x-1+\frac{x^2}{2}$. Then $f\left(0\right)=0$, and
$$
f'\left(x\right)=-\sin x+x.
$$
By (3) (see below), when $x> 0$, $\sin x< x$, so $f'\left(x\right)=x-\sin x> 0$. By **Theorem 1.5** (Monotonicity Criterion), $f\left(x\right)$ is strictly increasing on $\left[0,+\infty\right)$. Hence when $x> 0$, $f\left(x\right)> f\left(0\right)=0$, i.e. $\cos x> 1-\frac{x^2}{2}$. When $x< 0$, set $t=-x> 0$; by evenness the same conclusion follows.

(3) Set $f\left(x\right)=x-\sin x$. Then $f\left(0\right)=0$, and
$$
f'\left(x\right)=1-\cos x\ge0.
$$
Moreover $f'\left(x\right)=0$ holds only at the isolated points $x=2k\pi$. By **Theorem 1.5** (Monotonicity Criterion), $f\left(x\right)$ is strictly increasing on $\left[0,+\infty\right)$. Hence when $x> 0$, $f\left(x\right)> f\left(0\right)=0$, i.e. $x-\sin x> 0$, i.e. $\sin x< x$.

(4) Set $f\left(x\right)=\tan x-x$. Then $f\left(0\right)=0$, and
$$
f'\left(x\right)=\sec^2 x-1=\tan^2 x> 0\left(0< x< \frac{\pi}{2}\right).
$$
By **Theorem 1.5** (Monotonicity Criterion), $f\left(x\right)$ is strictly increasing on $\left[0,\frac{\pi}{2}\right)$. Hence when $0< x< \frac{\pi}{2}$, $f\left(x\right)> f\left(0\right)=0$, i.e. $\tan x-x> 0$, i.e. $\tan x> x$. $\blacksquare$

### Problem 6

(Problem 3.1-8) Let $f\left(x\right)$ be continuous in a neighborhood $U$ of the point $x_0$, and differentiable in the deleted neighborhood $U\setminus\left\{x_0\right\}$ of $x_0$. Prove that if the limit $\lim\limits_{x\to x_0}f'\left(x\right)$ exists, then $f\left(x\right)$ is differentiable at $x_0$, and
$$
f'\left(x_0\right)=\lim_{x\to x_0}f'\left(x\right).
$$
### Solution to Problem 6

Let $\lim_{x\to x_0}f'\left(x\right)=A$. For any $x\in U\setminus\left\{x_0\right\}$, applying **Theorem 1.3** (Lagrange Mean Value Theorem) on the closed interval with endpoints $x_0$ and $x$, there exists a point $\xi$ between $x_0$ and $x$ such that
$$
f\left(x\right)-f\left(x_0\right)=f'\left(\xi\right)\left(x-x_0\right).
$$
Hence
$$
\frac{f\left(x\right)-f\left(x_0\right)}{x-x_0}=f'\left(\xi\right).
$$
As $x\to x_0$, $\xi\to x_0$. By assumption $\lim_{x\to x_0}f'\left(x\right)=A$, so
$$
\lim_{x\to x_0}\frac{f\left(x\right)-f\left(x_0\right)}{x-x_0}=\lim_{\xi\to x_0}f'\left(\xi\right)=A.
$$
By the definition of the derivative, $f$ is differentiable at $x_0$, and

$$
f'\left(x_0\right)=A=\lim_{x\to x_0}f'\left(x\right).
$$

$\blacksquare$

### Problem 7

(Problem 3.1-10) Prove Darboux's theorem: Let $y=f\left(x\right)$ be differentiable on $\left(a,b\right)$. If there exist $x_1,x_2\in\left(a,b\right)$ such that $f'\left(x_1\right)> 0$ and $f'\left(x_2\right)< 0$, then there is a point $c$ between $x_1$ and $x_2$ such that $f'\left(c\right)=0$.

### Solution to Problem 7

Without loss of generality suppose $x_1< x_2$. Since $f'\left(x_1\right)> 0$, by the definition of the derivative, there exists $\delta_1> 0$ such that when $x\in\left(x_1,x_1+\delta_1\right)$,
$$
\frac{f\left(x\right)-f\left(x_1\right)}{x-x_1}> 0,
$$
i.e. $f\left(x\right)> f\left(x_1\right)$. Similarly, since $f'\left(x_2\right)< 0$, there exists $\delta_2> 0$ such that when $x\in\left(x_2-\delta_2,x_2\right)$,
$$
\frac{f\left(x\right)-f\left(x_2\right)}{x-x_2}< 0.
$$
Since $x-x_2< 0$, it follows that $f\left(x\right)-f\left(x_2\right)> 0$, i.e. $f\left(x\right)> f\left(x_2\right)$.

Consider the maximum of $f$ on the closed interval $\left[x_1,x_2\right]$. From the above, at points just to the right of $x_1$, the value of $f$ is greater than $f\left(x_1\right)$, so the maximum is not attained at $x_1$; similarly, at points just to the left of $x_2$, the value of $f$ is greater than $f\left(x_2\right)$, so the maximum is not attained at $x_2$. Hence the maximum is attained at some point $c\in\left(x_1,x_2\right)$, i.e. $c$ is a local maximum point. Moreover $f$ is differentiable on $\left(a,b\right)$, so by **Theorem 1.1** (Fermat's Theorem), $f'\left(c\right)=0$. $\blacksquare$

### Problem 8

(Problem 3.1-11) Prove that if $y=f\left(x\right)$ is differentiable on $\left(a,b\right)$ and $f'\left(x\right)\ne0$, then $f$ is either strictly increasing or strictly decreasing on $\left(a,b\right)$.

### Solution to Problem 8

By contradiction. Suppose $f$ is neither strictly increasing nor strictly decreasing on $\left(a,b\right)$. Then there exist $x_1< x_2< x_3$ such that $f\left(x_2\right)\le f\left(x_1\right)$ and $f\left(x_2\right)\le f\left(x_3\right)$ (or the analogous reverse situation).

Consider the minimum of $f$ on $\left[x_1,x_3\right]$. If the minimum is attained at $x_2$, then $x_2$ is a local minimum point, and by **Theorem 1.1** (Fermat's Theorem), $f'\left(x_2\right)=0$, contradicting the assumption.

If the minimum is not attained at $x_2$, then it is attained at an endpoint of one of the intervals $\left(x_1,x_2\right)$ or $\left(x_2,x_3\right)$. Suppose, without loss of generality, the minimum is attained at some point in $\left(x_2,x_3\right]$. Moreover, by the assumption $f\left(x_2\right)\le f\left(x_1\right)$, the relation between the maximum and minimum of $f$ on $\left[x_1,x_2\right]$ forces $f'$ to change sign somewhere. By Problem 7 (Darboux's theorem), $f'$ must take the value zero, a contradiction.

More rigorously: by **Theorem 1.3** (Lagrange Mean Value Theorem), if there exist two points for which the increment of $f$ is positive and two points for which the increment of $f$ is negative, then $f'$ takes a positive value somewhere and a negative value somewhere. By Darboux's theorem (Problem 7), $f'$ must take the value zero, contradicting $f'\left(x\right)\ne0$.

Hence $f$ can only be strictly increasing or strictly decreasing. $\blacksquare$

### Problem 9

(Problem 3.1-13) Prove the inequality $e^x> 1+x$ ($x> 0$).

### Solution to Problem 9

Set $f\left(x\right)=e^x-1-x$. Then $f\left(0\right)=0$, and
$$
f'\left(x\right)=e^x-1> 0\left(x> 0\right).
$$
By **Theorem 1.5** (Monotonicity Criterion), $f\left(x\right)$ is strictly increasing on $\left[0,+\infty\right)$. Hence when $x> 0$, $f\left(x\right)> f\left(0\right)=0$, i.e. $e^x-1-x> 0$, i.e. $e^x> 1+x$. $\blacksquare$

### Problem 10

(Problem 3.1-14) Let

$$
f\left(x\right)=\arctan\frac{1+x}{1-x}-\arctan x,
$$

and let $\left(a,b\right)$ be any interval not containing $x=1$. Prove that $f\left(x\right)=C$ for all $\forall x\in\left(a,b\right)$, where $C$ is a constant. Taking $\left(a,b\right)=\left(-\infty,1\right)$, prove that in this case $C=\frac{\pi}{4}$. Also ask: when $x\in\left(1,+\infty\right)$, what is the value of $C$?

### Solution to Problem 10

Differentiating gives
$$
\begin{aligned}
f'\left(x\right)&=\frac{1}{1+\left(\frac{1+x}{1-x}\right)^2}\cdot\frac{\left(1-x\right)+\left(1+x\right)}{\left(1-x\right)^2}-\frac{1}{1+x^2}\\
&=\frac{\left(1-x\right)^2}{\left(1-x\right)^2+\left(1+x\right)^2}\cdot\frac{2}{\left(1-x\right)^2}-\frac{1}{1+x^2}\\
&=\frac{2}{\left(1-x\right)^2+\left(1+x\right)^2}-\frac{1}{1+x^2}\\
&=\frac{1}{1+x^2}-\frac{1}{1+x^2}=0.
\end{aligned}
$$

By **Theorem 1.4** (Constant Function Theorem), $f\left(x\right)$ is constant on $\left(a,b\right)$, denoted $C$.

When $\left(a,b\right)=\left(-\infty,1\right)$, take $x=0$. Then
$$
f\left(0\right)=\arctan 1-\arctan 0=\frac{\pi}{4}.
$$
Hence $C=\frac{\pi}{4}$, i.e.
$$
\arctan\frac{1+x}{1-x}=\arctan x+\frac{\pi}{4}\left(x< 1\right).
$$
When $x\in\left(1,+\infty\right)$, take $x\to+\infty$. Then $\frac{1+x}{1-x}\to-1$, $\arctan\frac{1+x}{1-x}\to-\frac{\pi}{4}$, while $\arctan x\to\frac{\pi}{2}$. Hence

$$
C=\lim_{x\to+\infty}f\left(x\right)=-\frac{\pi}{4}-\frac{\pi}{2}=-\frac{3\pi}{4}.
$$

$\blacksquare$
