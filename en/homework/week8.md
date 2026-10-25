# Assignment 8

> **Theorem 8.1** (Intermediate Value Theorem) Let $y=f\left(x\right)$ be continuous on the closed interval $\left[a,b\right]$, and suppose $f\left(a\right)$ and $f\left(b\right)$ have opposite signs. Then there exists a point $c\in\left(a,b\right)$ such that $f\left(c\right)=0$. More generally, $f$ takes every value between $f\left(a\right)$ and $f\left(b\right)$.

> **Theorem 8.2** (Boundedness Theorem) A continuous function on a closed interval is bounded and attains its maximum and minimum.

> **Nested Interval Principle** Let $\left\{\left[a_n,b_n\right]\right\}$ be a sequence of closed intervals satisfying $\left[a_{n+1},b_{n+1}\right]\subset\left[a_n,b_n\right]$ and $b_n-a_n\to0$. Then there exists a unique real number $l$ belonging to all the intervals.

### Problem 1

(Problem 1.8-2) Let $y=f\left(x\right)$ be continuous on $\left(a,b\right)$. Let $x_1,x_2,x_3$ be three points in $\left(a,b\right)$ with $x_1< x_2< x_3$. Set

$$
\eta=\frac13\left[f\left(x_1\right)+f\left(x_2\right)+f\left(x_3\right)\right].
$$

Prove that there exists a point $\xi$ in $\left[x_1,x_3\right]$ such that $f\left(\xi\right)=\eta$.

### Solution to Problem 1

$f$ is continuous on $\left[x_1,x_3\right]$. By **Theorem 8.2**, let the maximum be $M$ and the minimum be $m$. Then $m\le f\left(x_i\right)\le M$, so $m\le\eta\le M$. By **Theorem 8.1** (Intermediate Value Theorem), there exists $\xi\in\left[x_1,x_3\right]$ such that $f\left(\xi\right)=\eta$. $\blacksquare$

### Problem 2

(Problem 1.8-3) Let $y=f\left(x\right)$ be continuous on $\left[a,+\infty\right)$, and suppose $\lim\limits_{x\to+\infty}f\left(x\right)=l$ with $l> f\left(a\right)$. Prove that for any number $\eta:f\left(a\right)< \eta< l$, there must exist a point $\xi\in\left(a,+\infty\right)$ such that $f\left(\xi\right)=\eta$.

### Solution to Problem 2

Since $\lim\limits_{x\to+\infty}f\left(x\right)=l> \eta$, there exists $A> a$ such that $f\left(x\right)> \eta$ when $x> A$. Take $b> A$. Then $f\left(a\right)< \eta< f\left(b\right)$. Moreover $f$ is continuous on $\left[a,b\right]$, so by **Theorem 8.1** (Intermediate Value Theorem), there exists $\xi\in\left(a,b\right)\subset\left(a,+\infty\right)$ such that $f\left(\xi\right)=\eta$. $\blacksquare$

### Problem 3

(Problem 1.8-4) Let $y=f\left(x\right)$ be continuous on $\left[a,+\infty\right)$, and suppose $\lim\limits_{x\to+\infty}f\left(x\right)$ exists. Prove that $f$ is a bounded function on $\left[a,+\infty\right)$.

### Solution to Problem 3

Let $\lim\limits_{x\to+\infty}f\left(x\right)=l$. There exists $A> a$ such that $\left|f\left(x\right)-l\right|< 1$ when $x> A$, i.e. $\left|f\left(x\right)\right|< \left|l\right|+1$. On $\left[a,A\right]$, by **Theorem 8.2** (Boundedness Theorem), $f$ is bounded; let $\left|f\left(x\right)\right|\le M$. Take $\widetilde M=\max\left\{M,\left|l\right|+1\right\}$. Then for all $x\in\left[a,+\infty\right)$, $\left|f\left(x\right)\right|\le\widetilde M$. $\blacksquare$

### Problem 4

(Problem 1.8-5) Let $y=f\left(x\right)$ be continuous on $\left(a,b\right)$. Suppose

$$
x_1,x_2\in\left(a,b\right),x_1< x_2,m_1> 0,m_2> 0.
$$

Prove that there exists a point $\xi\in\left(a,b\right)$ such that

$$
f\left(\xi\right)=\frac{m_1f\left(x_1\right)+m_2f\left(x_2\right)}{m_1+m_2}.
$$

### Solution to Problem 4

Let the maximum of $f$ on $\left[x_1,x_2\right]$ be $M$ and the minimum be $m$. Then

$$
m=\frac{m_1m+m_2m}{m_1+m_2}\le\frac{m_1f\left(x_1\right)+m_2f\left(x_2\right)}{m_1+m_2}\le\frac{m_1M+m_2M}{m_1+m_2}=M.
$$

By **Theorem 8.1** (Intermediate Value Theorem), there exists $\xi\in\left[x_1,x_2\right]\subset\left(a,b\right)$ such that $f\left(\xi\right)=\frac{m_1f\left(x_1\right)+m_2f\left(x_2\right)}{m_1+m_2}$. $\blacksquare$

### Problem 5

(Problem 1.8-6) Let $f:\left[0,1\right]\to\left[0,1\right]$ be a continuous map. Prove that it has at least one fixed point in $\left[0,1\right]$, i.e. there exists a point $x_0\in\left[0,1\right]$ such that $f\left(x_0\right)=x_0$.

### Solution to Problem 5

Set $g\left(x\right)=f\left(x\right)-x$. Then $g\left(0\right)=f\left(0\right)\ge0$ and $g\left(1\right)=f\left(1\right)-1\le0$. By **Theorem 8.1** (Intermediate Value Theorem), there exists $x_0\in\left[0,1\right]$ such that $g\left(x_0\right)=0$, i.e. $f\left(x_0\right)=x_0$. $\blacksquare$

### Problem 6

(Problem 1.8-7) Let $y=f\left(x\right)$ be continuous on $\left[a,b\right]$ and suppose $f\left(a\right)=f\left(b\right)$. Prove that there must exist two points $x_1$ and $x_2$ in $\left[a,b\right]$ such that $\left|x_1-x_2\right|=\frac12\left(b-a\right)$ and $f\left(x_1\right)=f\left(x_2\right)$.

### Solution to Problem 6

Set $d=\frac{b-a}2$, and consider the auxiliary function $g\left(x\right)=f\left(x+d\right)-f\left(x\right)$ for $x\in\left[a,b-d\right]=\left[a,a+d\right]$. Then

$$
g\left(a\right)=f\left(a+d\right)-f\left(a\right), g\left(a+d\right)=f\left(b\right)-f\left(a+d\right)=f\left(a\right)-f\left(a+d\right)=-g\left(a\right).
$$

If $g\left(a\right)=0$, take $x_1=a,x_2=a+d$. If $g\left(a\right)\ne0$, then $g\left(a\right)$ and $g\left(a+d\right)$ have opposite signs, so by **Theorem 8.1**, there exists $\xi\in\left(a,a+d\right)$ such that $g\left(\xi\right)=0$, i.e. $f\left(\xi+d\right)=f\left(\xi\right)$. Take $x_1=\xi,x_2=\xi+d$; then $\left|x_1-x_2\right|=d=\frac{b-a}2$. $\blacksquare$

### Problem 7

(Problem 1.8-8) Let $E$ be a bounded infinite set in $\mathbb R$. Prove that there exists a point $c\in\mathbb R$ such that every deleted neighborhood $\left(c-\delta,c+\delta\right)\backslash\left\{c\right\}$ of $c$ contains points of $E$.

### Solution to Problem 7

Since $E$ is bounded, suppose $E\subset\left[a,b\right]$. Divide $\left[a,b\right]$ into two closed intervals; at least one contains infinitely many points of $E$, and denote it by $\left[a_1,b_1\right]$. Continuing in this way gives a nested sequence $\left\{\left[a_n,b_n\right]\right\}$, each $\left[a_n,b_n\right]$ containing infinitely many points of $E$, and

$$
b_n-a_n=\frac{b-a}{2^n}\to0.
$$

By the **Nested Interval Principle**, there exists a unique $c\in\bigcap\left[a_n,b_n\right]$. For any $\delta> 0$, when $n$ is sufficiently large, $\left[a_n,b_n\right]\subset\left(c-\delta,c+\delta\right)$, and since $\left[a_n,b_n\right]$ contains infinitely many points of $E$, there must be points of $E$ in $\left(c-\delta,c+\delta\right)\backslash\left\{c\right\}$. $\blacksquare$

### Problem 8

(Problem 1.8-9) Let $E$ be a nonempty set in $\mathbb R$ that is bounded above. Prove that among the upper bounds of $E$ there is a least upper bound, i.e. there exists $M_0$, with $M_0$ itself being an upper bound of $E$, and for any upper bound $M$ of $E$, $M_0\le M$.

### Solution to Problem 8

Suppose $E\subset\left[a,b\right]$, where $b$ is an upper bound of $E$. Divide $\left[a,b\right]$ into two closed intervals. If the right half contains an upper bound of $E$, take the right half; otherwise take the left half (in which case the right endpoint of the left half becomes the new upper bound). Continuing in this way gives a nested sequence $\left\{\left[a_n,b_n\right]\right\}$, where each $b_n$ is an upper bound of $E$ and each $a_n$ is not an upper bound of $E$.

By the **Nested Interval Principle**, there exists a unique $M_0\in\bigcap\left[a_n,b_n\right]$. Since $b_n\to M_0$ and each $b_n$ is an upper bound, for any $x\in E$ one has $x\le b_n$; letting $n\to\infty$ gives $x\le M_0$, i.e. $M_0$ is an upper bound. Moreover, if $M$ is any upper bound, then $M\ge b_n$ (otherwise, if $M< b_n$, it is not inconsistent with $b_n$ being an upper bound...); in fact $M\ge a_n$ for all $n$, so $M\ge M_0$. $\blacksquare$

### Problem 9

(Problem 1.8-11) Let $y=f\left(x\right)$ be defined near the point $a$ and have limit $\lim\limits_{x\to a}f\left(x\right)=0$. Let $y=g\left(x\right)$ be defined near the point $a$ and be a bounded function. Prove that $\lim\limits_{x\to a}f\left(x\right)g\left(x\right)=0$.

### Solution to Problem 9

Let $\left|g\left(x\right)\right|\le M$. Given any $\varepsilon> 0$, since $f\left(x\right)\to0$, there exists $\delta> 0$ such that $\left|f\left(x\right)\right|< \varepsilon/M$ when $0< \left|x-a\right|< \delta$. Hence

$$
\left|f\left(x\right)g\left(x\right)\right|\le M\left|f\left(x\right)\right|< \varepsilon.
$$

Hence $\lim f\left(x\right)g\left(x\right)=0$. $\blacksquare$
