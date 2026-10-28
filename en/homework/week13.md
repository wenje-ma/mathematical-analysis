# week13

> **Theorem 1.1 (Fermat's Theorem)**<br>If $f\left(x\right)$ is defined near $a$ and differentiable at $a$, and $a$ is an extremum point of $y=f\left(x\right)$, then $f'\left(a\right)=0$.

> **Theorem 1.2 (Rolle's Theorem)**<br>If $y=f\left(x\right)$ is continuous on $\left[a,b\right]$, differentiable on $\left(a,b\right)$, and $f\left(a\right)=f\left(b\right)$, then there exists $c\in\left(a,b\right)$ such that $f'\left(c\right)=0$.

> **Theorem 1.3 (Lagrange Mean Value Theorem)**<br>If $y=f\left(x\right)$ is continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$, then there exists $c\in\left(a,b\right)$ such that $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

> **Theorem 1.4 (Constant Function Theorem)**<br>If $y=f\left(x\right)$ is differentiable on $\left(a,b\right)$ and $f'\left(x\right)=0$ for all $x\in\left(a,b\right)$, then $f$ is constant on $\left(a,b\right)$.

> **Theorem 1.5 (Monotonicity Criterion)**<br>If $y=f\left(x\right)$ is continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$, then $f'\left(x\right)> 0$ ($\ge0$) implies strictly increasing (increasing), and $f'\left(x\right)< 0$ ($\le0$) implies strictly decreasing (decreasing).

---

## 3.1-1

Let $y=f\left(x\right)$ be differentiable on $\left(-\infty,+\infty\right)$ with $\lim_{x\to-\infty}f\left(x\right)=\lim_{x\to+\infty}f\left(x\right)$. Prove that there exists $c\in\left(-\infty,+\infty\right)$ such that $f'\left(c\right)=0$.

### Solution 3.1-1

Let

$$
l=\lim_{x\to-\infty}f\left(x\right)=\lim_{x\to+\infty}f\left(x\right).
$$

If $f\left(x\right)\equiv l$, then $f'\left(x\right)\equiv0$ and the result is immediate.

Otherwise, there exists $x_0$ with $f\left(x_0\right)\ne l$; assume $f\left(x_0\right)> l$. By $\lim_{x\to\pm\infty}f\left(x\right)=l$, taking $\varepsilon=\frac{f\left(x_0\right)-l}{2}> 0$, there exists $A> \left|x_0\right|$ such that $\left|x\right|> A$ implies

$$
f\left(x\right)< l+\varepsilon=\frac{f\left(x_0\right)+l}{2}< f\left(x_0\right).
$$

On $\left[-A,A\right]$, since $f\left(-A\right)< f\left(x_0\right)$ and $f\left(A\right)< f\left(x_0\right)$ while $x_0\in\left(-A,A\right)$, the maximum of $f$ on $\left[-A,A\right]$ is attained at some interior point $c\in\left(-A,A\right)$. Thus $c$ is a local maximum. Since $f$ is differentiable on $\left(-A,A\right)$, by **Theorem 1.1 (Fermat's Theorem)**, $f'\left(c\right)=0$. $\blacksquare$

---

## 3.1-2

Let $p\left(x\right)=x^n+qx+r$ ($n\in\mathbb N$, $q,r\in\mathbb R$). Prove: if $n$ is even, $p$ has at most two real roots; if $n$ is odd, at most three.

### Solution 3.1-2

Suppose $n$ is even and $p$ has at least three distinct roots $x_1< x_2< x_3$. By **Theorem 1.2 (Rolle's Theorem)**, there exist $\xi_1\in\left(x_1,x_2\right)$ and $\xi_2\in\left(x_2,x_3\right)$ with

$$
p'\left(\xi_1\right)=0,\quad p'\left(\xi_2\right)=0.
$$

But $p'\left(x\right)=nx^{n-1}+q$; since $n-1$ is odd, $nx^{n-1}+q=0$ has at most one real root. Contradiction. Thus $n$ even implies at most two roots.

Now suppose $n$ is odd and $p$ has at least four roots $x_1< x_2< x_3< x_4$. By **Theorem 1.2 (Rolle's Theorem)**, there exist $\xi_1\in\left(x_1,x_2\right)$, $\xi_2\in\left(x_2,x_3\right)$, $\xi_3\in\left(x_3,x_4\right)$ with $p'\left(\xi_i\right)=0$. Applying Rolle again to $p'$, there exist $\eta_1\in\left(\xi_1,\xi_2\right)$ and $\eta_2\in\left(\xi_2,\xi_3\right)$ with $p''\left(\eta_1\right)=p''\left(\eta_2\right)=0$. But $p''\left(x\right)=n\left(n-1\right)x^{n-2}$; since $n-2$ is odd, this has only one root $x=0$. Contradiction. Thus $n$ odd implies at most three roots. $\blacksquare$

---

## 3.1-4

Find the intervals of monotonicity:

(1) $f\left(x\right)=xe^x$;

(2) $f\left(x\right)=\frac{x^2-1}{x}$;

(3) $f\left(x\right)=\sqrt{x-2}$;

(4) $f\left(x\right)=x^4-x+1$.

### Solution 3.1-4

(1) $f'\left(x\right)=\left(1+x\right)e^x$. Since $e^x> 0$, the sign is determined by $1+x$. By **Theorem 1.5 (Monotonicity Criterion)**, $f$ is strictly decreasing on $\left(-\infty,-1\right]$ and strictly increasing on $\left[-1,+\infty\right)$.

(2) $f\left(x\right)=x-\frac1x$ on $\left(-\infty,0\right)\cup\left(0,+\infty\right)$. $f'\left(x\right)=1+\frac1{x^2}> 0$. By **Theorem 1.5 (Monotonicity Criterion)**, $f$ is strictly increasing on both intervals.

(3) Domain $\left[2,+\infty\right)$. $f'\left(x\right)=\frac1{2\sqrt{x-2}}> 0$ for $x> 2$. By **Theorem 1.5 (Monotonicity Criterion)**, $f$ is strictly increasing on $\left[2,+\infty\right)$.

(4) $f'\left(x\right)=4x^3-1=0$ gives $x=\sqrt[3]{\frac14}$. By **Theorem 1.5 (Monotonicity Criterion)**, $f$ is strictly decreasing on $\left(-\infty,\sqrt[3]{\frac14}\right]$ and strictly increasing on $\left[\sqrt[3]{\frac14},+\infty\right)$. $\blacksquare$

---

## 3.1-5

Let $f$ and $g$ be continuous on $\left[a,b\right]$, differentiable on $\left(a,b\right)$, with $f'\left(x\right)> g'\left(x\right)$ and $f\left(a\right)=g\left(a\right)$. Prove $f\left(x\right)> g\left(x\right)$ for all $x\in\left(a,b\right]$.

### Solution 3.1-5

Let $h\left(x\right)=f\left(x\right)-g\left(x\right)$. Then $h'\left(x\right)=f'\left(x\right)-g'\left(x\right)> 0$ on $\left(a,b\right)$. By **Theorem 1.5 (Monotonicity Criterion)**, $h$ is strictly increasing on $\left[a,b\right]$. Since $h\left(a\right)=0$, for $x\in\left(a,b\right]$, $h\left(x\right)> h\left(a\right)=0$, i.e. $f\left(x\right)> g\left(x\right)$. $\blacksquare$

---

## 3.1-6

Prove:

(1) $\ln\left(1+x\right)< x$ ($x> 0$);

(2) $\cos x> 1-\frac{x^2}{2}$ ($x\ne0$);

(3) $\sin x< x$ ($x> 0$);

(4) $\tan x> x$ ($0< x< \frac\pi2$).

### Solution 3.1-6

(1) Let $f\left(x\right)=\ln\left(1+x\right)-x$. $f\left(0\right)=0$, $f'\left(x\right)=-\frac{x}{1+x}< 0$ for $x> 0$. By **Theorem 1.5 (Monotonicity Criterion)**, $f$ is strictly decreasing, so $f\left(x\right)< f\left(0\right)=0$, i.e. $\ln\left(1+x\right)< x$.

(2) Let $f\left(x\right)=\cos x-1+\frac{x^2}{2}$. $f\left(0\right)=0$, $f'\left(x\right)=x-\sin x> 0$ for $x> 0$ (by (3)). By **Theorem 1.5 (Monotonicity Criterion)**, $f$ is strictly increasing, so $f\left(x\right)> 0$, i.e. $\cos x> 1-\frac{x^2}{2}$. By evenness, the result holds for $x< 0$ as well.

(3) Let $f\left(x\right)=x-\sin x$. $f\left(0\right)=0$, $f'\left(x\right)=1-\cos x\ge0$ with equality only at isolated points. By **Theorem 1.5 (Monotonicity Criterion)**, $f$ is strictly increasing, so $f\left(x\right)> 0$, i.e. $\sin x< x$.

(4) Let $f\left(x\right)=\tan x-x$. $f\left(0\right)=0$, $f'\left(x\right)=\tan^2x> 0$ for $0< x< \frac\pi2$. By **Theorem 1.5 (Monotonicity Criterion)**, $f$ is strictly increasing, so $f\left(x\right)> 0$, i.e. $\tan x> x$. $\blacksquare$

---

## 3.1-8

Let $f$ be continuous near $x_0$ and differentiable on $U\setminus\left\{x_0\right\}$. If $\lim_{x\to x_0}f'\left(x\right)$ exists, prove $f$ is differentiable at $x_0$ and $f'\left(x_0\right)=\lim_{x\to x_0}f'\left(x\right)$.

### Solution 3.1-8

Let $\lim_{x\to x_0}f'\left(x\right)=A$. For any $x\ne x_0$, apply **Theorem 1.3 (Lagrange Mean Value Theorem)** on the interval between $x_0$ and $x$: there exists $\xi$ between them such that

$$
\frac{f\left(x\right)-f\left(x_0\right)}{x-x_0}=f'\left(\xi\right).
$$

As $x\to x_0$, $\xi\to x_0$, so by assumption,

$$
\lim_{x\to x_0}\frac{f\left(x\right)-f\left(x_0\right)}{x-x_0}=\lim_{\xi\to x_0}f'\left(\xi\right)=A.
$$

Thus $f'\left(x_0\right)=A$. $\blacksquare$

---

## 3.1-10

Prove Darboux's theorem: if $f$ is differentiable on $\left(a,b\right)$ and $f'\left(x_1\right)> 0$, $f'\left(x_2\right)< 0$ for some $x_1,x_2\in\left(a,b\right)$, then there exists $c$ between them with $f'\left(c\right)=0$.

### Solution 3.1-10

Assume $x_1< x_2$. From $f'\left(x_1\right)> 0$, there exists $\delta_1> 0$ such that $x\in\left(x_1,x_1+\delta_1\right)$ implies $\frac{f\left(x\right)-f\left(x_1\right)}{x-x_1}> 0$, i.e. $f\left(x\right)> f\left(x_1\right)$. Similarly, $f'\left(x_2\right)< 0$ implies there exists $\delta_2> 0$ such that $x\in\left(x_2-\delta_2,x_2\right)$ implies $f\left(x\right)> f\left(x_2\right)$.

Thus the maximum of $f$ on $\left[x_1,x_2\right]$ is not attained at either endpoint, but at some interior point $c\in\left(x_1,x_2\right)$. Since $f$ is differentiable, by **Theorem 1.1 (Fermat's Theorem)**, $f'\left(c\right)=0$. $\blacksquare$

---

## 3.1-11

Prove: if $f$ is differentiable on $\left(a,b\right)$ and $f'\left(x\right)\ne0$, then $f$ is either strictly increasing or strictly decreasing.

### Solution 3.1-11

Suppose not. Then by **Theorem 1.3 (Lagrange Mean Value Theorem)**, $f'$ takes both positive and negative values. By Darboux's theorem (3.1-10), $f'$ must take the value $0$, contradicting $f'\left(x\right)\ne0$. Hence $f$ is strictly increasing or strictly decreasing. $\blacksquare$

---

## 3.1-13

Prove $e^x> 1+x$ for $x> 0$.

### Solution 3.1-13

Let $f\left(x\right)=e^x-1-x$. $f\left(0\right)=0$, $f'\left(x\right)=e^x-1> 0$ for $x> 0$. By **Theorem 1.5 (Monotonicity Criterion)**, $f$ is strictly increasing, so $f\left(x\right)> f\left(0\right)=0$, i.e. $e^x> 1+x$. $\blacksquare$

---

## 3.1-14

Let

$$
f\left(x\right)=\arctan\frac{1+x}{1-x}-\arctan x.
$$

On any interval $\left(a,b\right)$ not containing $x=1$, prove $f\left(x\right)=C$ constant. For $\left(a,b\right)=\left(-\infty,1\right)$, show $C=\frac\pi4$. What is $C$ on $\left(1,+\infty\right)$?

### Solution 3.1-14

Differentiating,

$$
f'\left(x\right)=\frac{2}{\left(1-x\right)^2+\left(1+x\right)^2}-\frac1{1+x^2}=\frac1{1+x^2}-\frac1{1+x^2}=0.
$$

By **Theorem 1.4 (Constant Function Theorem)**, $f$ is constant on $\left(a,b\right)$.

On $\left(-\infty,1\right)$, take $x=0$: $f\left(0\right)=\arctan1=\frac\pi4$, so $C=\frac\pi4$.

On $\left(1,+\infty\right)$, as $x\to+\infty$, $\frac{1+x}{1-x}\to-1$ so $\arctan\frac{1+x}{1-x}\to-\frac\pi4$, while $\arctan x\to\frac\pi2$. Thus

$$
C=-\frac\pi4-\frac\pi2=-\frac{3\pi}4.
$$

$\blacksquare$
