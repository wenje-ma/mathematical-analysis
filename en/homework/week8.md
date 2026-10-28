# week8

> **Basic Knowledge: Nested Interval Principle**<br>If $\left\{\left[a_n,b_n\right]\right\}$ is a sequence of closed intervals with $\left[a_{n+1},b_{n+1}\right]\subset\left[a_n,b_n\right]$ and $b_n-a_n\to0$, then there exists a unique real number $l$ belonging to all intervals.

> **Theorem 8.1 (Intermediate Value Theorem)**<br>If $y=f\left(x\right)$ is continuous on $\left[a,b\right]$ and $f\left(a\right)$ and $f\left(b\right)$ have opposite signs, then there exists $c\in\left(a,b\right)$ with $f\left(c\right)=0$. More generally, $f$ takes every value between $f\left(a\right)$ and $f\left(b\right)$.

> **Theorem 8.2 (Boundedness Theorem)**<br>A continuous function on a closed interval is bounded and attains its maximum and minimum.

---

## 1.8-2

Let $y=f\left(x\right)$ be continuous on $\left(a,b\right)$, and let $x_1,x_2,x_3\in\left(a,b\right)$ with $x_1< x_2< x_3$. Set

$$
\eta=\frac13\left[f\left(x_1\right)+f\left(x_2\right)+f\left(x_3\right)\right].
$$

Prove that there exists $\xi\in\left[x_1,x_3\right]$ such that $f\left(\xi\right)=\eta$.

### Solution 1.8-2

$f$ is continuous on $\left[x_1,x_3\right]$. By **Theorem 8.2 (Boundedness Theorem)**, let the max be $M$ and min be $m$. Then $m\le f\left(x_i\right)\le M$, so $m\le\eta\le M$. By **Theorem 8.1 (Intermediate Value Theorem)**, there exists $\xi\in\left[x_1,x_3\right]$ with $f\left(\xi\right)=\eta$. $\blacksquare$

---

## 1.8-3

Let $y=f\left(x\right)$ be continuous on $\left[a,+\infty\right)$ with $\lim_{x\to+\infty}f\left(x\right)=l$ and $l> f\left(a\right)$. Prove that for any $\eta$ with $f\left(a\right)< \eta< l$, there exists $\xi\in\left(a,+\infty\right)$ such that $f\left(\xi\right)=\eta$.

### Solution 1.8-3

Since $\lim_{x\to+\infty}f\left(x\right)=l> \eta$, there exists $A> a$ such that $x> A$ implies $f\left(x\right)> \eta$. Take $b> A$, so $f\left(a\right)< \eta< f\left(b\right)$. Since $f$ is continuous on $\left[a,b\right]$, by **Theorem 8.1 (Intermediate Value Theorem)**, there exists $\xi\in\left(a,b\right)\subset\left(a,+\infty\right)$ with $f\left(\xi\right)=\eta$. $\blacksquare$

---

## 1.8-4

Let $y=f\left(x\right)$ be continuous on $\left[a,+\infty\right)$ and $\lim_{x\to+\infty}f\left(x\right)$ exists. Prove $f$ is bounded on $\left[a,+\infty\right)$.

### Solution 1.8-4

Let $\lim_{x\to+\infty}f\left(x\right)=l$. There exists $A> a$ such that $x> A$ implies $\left|f\left(x\right)-l\right|< 1$, i.e. $\left|f\left(x\right)\right|< \left|l\right|+1$. On $\left[a,A\right]$, by **Theorem 8.2 (Boundedness Theorem)**, $f$ is bounded, say $\left|f\left(x\right)\right|\le M$. Take $\widetilde M=\max\left\{M,\left|l\right|+1\right\}$; then $\left|f\left(x\right)\right|\le\widetilde M$ for all $x\in\left[a,+\infty\right)$. $\blacksquare$

---

## 1.8-5

Let $y=f\left(x\right)$ be continuous on $\left(a,b\right)$, and let $x_1,x_2\in\left(a,b\right)$ with $x_1< x_2$, $m_1> 0$, $m_2> 0$. Prove that there exists $\xi\in\left(a,b\right)$ such that

$$
f\left(\xi\right)=\frac{m_1f\left(x_1\right)+m_2f\left(x_2\right)}{m_1+m_2}.
$$

### Solution 1.8-5

Let the max and min of $f$ on $\left[x_1,x_2\right]$ be $M$ and $m$. Then

$$
m=\frac{m_1m+m_2m}{m_1+m_2}\le\frac{m_1f\left(x_1\right)+m_2f\left(x_2\right)}{m_1+m_2}\le\frac{m_1M+m_2M}{m_1+m_2}=M.
$$

By **Theorem 8.1 (Intermediate Value Theorem)**, there exists $\xi\in\left[x_1,x_2\right]\subset\left(a,b\right)$ with $f\left(\xi\right)=\frac{m_1f\left(x_1\right)+m_2f\left(x_2\right)}{m_1+m_2}$. $\blacksquare$

---

## 1.8-6

Let $f:\left[0,1\right]\to\left[0,1\right]$ be continuous. Prove that it has at least one fixed point in $\left[0,1\right]$, i.e. there exists $x_0\in\left[0,1\right]$ with $f\left(x_0\right)=x_0$.

### Solution 1.8-6

Let $g\left(x\right)=f\left(x\right)-x$. Then $g\left(0\right)=f\left(0\right)\ge0$ and $g\left(1\right)=f\left(1\right)-1\le0$. By **Theorem 8.1 (Intermediate Value Theorem)**, there exists $x_0\in\left[0,1\right]$ with $g\left(x_0\right)=0$, i.e. $f\left(x_0\right)=x_0$. $\blacksquare$

---

## 1.8-7

Let $y=f\left(x\right)$ be continuous on $\left[a,b\right]$ with $f\left(a\right)=f\left(b\right)$. Prove that there exist two points $x_1,x_2\in\left[a,b\right]$ such that $\left|x_1-x_2\right|=\frac12\left(b-a\right)$ and $f\left(x_1\right)=f\left(x_2\right)$.

### Solution 1.8-7

Let $d=\frac{b-a}2$ and consider $g\left(x\right)=f\left(x+d\right)-f\left(x\right)$ for $x\in\left[a,b-d\right]=\left[a,a+d\right]$. Then

$$
g\left(a\right)=f\left(a+d\right)-f\left(a\right),\quad g\left(a+d\right)=f\left(b\right)-f\left(a+d\right)=f\left(a\right)-f\left(a+d\right)=-g\left(a\right).
$$

If $g\left(a\right)=0$, take $x_1=a$, $x_2=a+d$. Otherwise $g\left(a\right)$ and $g\left(a+d\right)$ have opposite signs; by **Theorem 8.1 (Intermediate Value Theorem)**, there exists $\xi\in\left(a,a+d\right)$ with $g\left(\xi\right)=0$, i.e. $f\left(\xi+d\right)=f\left(\xi\right)$. Taking $x_1=\xi$, $x_2=\xi+d$, we have $\left|x_1-x_2\right|=d=\frac{b-a}2$. $\blacksquare$

---

## 1.8-8

Let $E$ be a bounded infinite set in $\mathbb R$. Prove that there exists $c\in\mathbb R$ such that every punctured neighborhood $\left(c-\delta,c+\delta\right)\backslash\left\{c\right\}$ contains points of $E$.

### Solution 1.8-8

Since $E$ is bounded, $E\subset\left[a,b\right]$. Split $\left[a,b\right]$ into two closed halves; at least one contains infinitely many points of $E$, call it $\left[a_1,b_1\right]$. Continuing gives a nested sequence $\left\{\left[a_n,b_n\right]\right\}$, each containing infinitely many points of $E$, with

$$
b_n-a_n=\frac{b-a}{2^n}\to0.
$$

By **Basic Knowledge: Nested Interval Principle**, there exists a unique $c\in\bigcap\left[a_n,b_n\right]$. For any $\delta> 0$, for large $n$, $\left[a_n,b_n\right]\subset\left(c-\delta,c+\delta\right)$ and contains infinitely many points of $E$, so $\left(c-\delta,c+\delta\right)\backslash\left\{c\right\}$ contains points of $E$. $\blacksquare$

---

## 1.8-9

Let $E$ be a nonempty set in $\mathbb R$ bounded above. Prove that $E$ has a least upper bound, i.e. there exists $M_0$ which is an upper bound of $E$ and satisfies $M_0\le M$ for every upper bound $M$ of $E$.

### Solution 1.8-9

Let $E\subset\left[a,b\right]$ where $b$ is an upper bound. Split $\left[a,b\right]$ into two halves. If the right half contains an upper bound, take it; otherwise take the left half (its right endpoint is then a new upper bound). Continuing gives a nested sequence $\left\{\left[a_n,b_n\right]\right\}$ where each $b_n$ is an upper bound and each $a_n$ is not.

By **Basic Knowledge: Nested Interval Principle**, there exists a unique $M_0\in\bigcap\left[a_n,b_n\right]$. Since $b_n\to M_0$ and each $b_n$ is an upper bound, for any $x\in E$, $x\le b_n$; letting $n\to\infty$ gives $x\le M_0$, so $M_0$ is an upper bound. If $M$ is any upper bound, then $M\ge a_n$ for all $n$ (since $a_n$ is not an upper bound, there is $x\in E$ with $x> a_n$, and $M\ge x$), so $M\ge M_0$. $\blacksquare$

---

## 1.8-11

Let $y=f\left(x\right)$ be defined near $a$ with $\lim_{x\to a}f\left(x\right)=0$, and let $y=g\left(x\right)$ be defined near $a$ and bounded. Prove $\lim_{x\to a}f\left(x\right)g\left(x\right)=0$.

### Solution 1.8-11

Let $\left|g\left(x\right)\right|\le M$. Given $\varepsilon> 0$, since $f\left(x\right)\to0$, there exists $\delta> 0$ such that $0< \left|x-a\right|< \delta$ implies $\left|f\left(x\right)\right|< \varepsilon/M$. Then

$$
\left|f\left(x\right)g\left(x\right)\right|\le M\left|f\left(x\right)\right|< \varepsilon.
$$

Hence $\lim f\left(x\right)g\left(x\right)=0$. $\blacksquare$
