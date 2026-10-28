# week2

> **Basic Knowledge: Definition of a Function**<br>Let $x$ and $y$ be two variables taking values in sets $X$ and $Y$ respectively. If there is a rule $f$ such that to each $x\in X$ there corresponds a unique $y\in Y$, then $f$ is called a function, denoted $f:X\to Y$; $X$ is called the domain of $f$. The set of all function values attainable in $Y$ is called the range of $f$, denoted $f\left(X\right)$.

> **Basic Knowledge: Definition of a Composite Function**<br>Suppose there are two functions $f:X\to Y$ and $g:Y^*\to Z$ with $Y\subset Y^*$. For each $x\in X$, there is a unique $y=f\left(x\right)\in Y$, and then $g$ gives $z=g\left(y\right)$. The correspondence $x\mapsto z$ from $X$ to $Z$, where $z=g\left(f\left(x\right)\right)$, is called the composite function of $f$ and $g$.

> **Basic Knowledge: Definition of a Periodic Function**<br>Let $y=f\left(x\right)$ be defined on $\mathbb R$. If there exists a number $T\ne 0$ such that $f\left(x+T\right)=f\left(x\right)$ for all $x\in\mathbb R$, then $y=f\left(x\right)$ is called a periodic function, and $T$ is called a period of $f$.

> **Proposition 2.1 (Necessary and Sufficient Condition for a Bounded Function)**<br>A function $f:X\to Y$ is bounded if and only if there exists $M> 0$ such that $\left|f\left(x\right)\right|\le M$ for all $x\in X$.

---

## 1.2-1

Find the domains of the following functions:

(1) $y=\sqrt{x^2-16}$;

(2) $y=\frac{1}{\sqrt{x^2-3x+2}}$;

(3) $y=\ln\frac{x^2-2}{2}$;

(4) $y=\arccos\left(2\sin x\right)$.

### Solution 1.2-1

(1) For $\sqrt{x^2-16}$ to be meaningful, we need $x^2-16\ge0$, i.e. $\left|x\right|\ge4$. The domain is $\left(-\infty,-4\right]\cup\left[4,+\infty\right)$.

(2) For $\frac{1}{\sqrt{x^2-3x+2}}$ to be meaningful, we need $x^2-3x+2> 0$, i.e. $\left(x-1\right)\left(x-2\right)> 0$, equivalently $x< 1$ or $x> 2$. The domain is $\left(-\infty,1\right)\cup\left(2,+\infty\right)$.

(3) For $\ln\frac{x^2-2}{2}$ to be meaningful, we need $\frac{x^2-2}{2}> 0$, i.e. $x^2> 2$, equivalently $\left|x\right|> \sqrt2$. The domain is

$$
\left(-\infty,-\sqrt2\right)\cup\left(\sqrt2,+\infty\right).
$$

(4) For $\arccos\left(2\sin x\right)$ to be meaningful, we need $\left|2\sin x\right|\le1$, i.e. $\left|\sin x\right|\le\frac12$. This is equivalent to

$$
x\in\left[k\pi-\frac{\pi}{6},k\pi+\frac{\pi}{6}\right],\quad k\in\mathbb Z.
$$

The domain is $\displaystyle\bigcup_{k\in\mathbb Z}\left[k\pi-\frac{\pi}{6},k\pi+\frac{\pi}{6}\right]$. $\blacksquare$

---

## 1.2-2

Find the range $f\left(X\right)$ of the following functions $f$, where $X$ is the specified domain:

(1)

$$
f\left(x\right)=\sqrt{1+x^2},\quad X=\left(0,5\right);
$$

(2)

$$
f\left(x\right)=\sin\frac1x,\quad X=\mathbb R\backslash\left\{0\right\};
$$

(3) $f\left(x\right)=\left\{x\right\}$ (fractional part of $x$), $X=\mathbb R$;

(4)

$$
f\left(x\right)=x^3+x+1,\quad X=\mathbb R.
$$

### Solution 1.2-2

(1) When $x\in\left(0,5\right)$, $x^2\in\left(0,25\right)$, so $1+x^2\in\left(1,26\right)$, and thus $\sqrt{1+x^2}\in\left(1,\sqrt{26}\right)$. By **Basic Knowledge: Definition of a Function**, $f\left(X\right)=\left(1,\sqrt{26}\right)$.

(2) As $x$ ranges over $\mathbb R\backslash\left\{0\right\}$, $\frac1x$ ranges over $\mathbb R\backslash\left\{0\right\}$. The range of $\sin t$ over $t\in\mathbb R$ is $\left[-1,1\right]$; removing one point $t=0$ (where $\sin0=0$) does not change the range ($0$ is still attainable, e.g. at $t=\pi$). Hence $f\left(X\right)=\left[-1,1\right]$.

(3) For any $x\in\mathbb R$, the fractional part $\left\{x\right\}=x-\left[x\right]$ satisfies $0\le\left\{x\right\}< 1$. Conversely, for any $y\in\left[0,1\right)$, taking $x=y$ gives $\left\{x\right\}=y$. Hence $f\left(X\right)=\left[0,1\right)$.

(4) $f'\left(x\right)=3x^2+1> 0$, so $f$ is strictly increasing on $\mathbb R$. Moreover, as $x\to-\infty$, $f\left(x\right)\to-\infty$, and as $x\to+\infty$, $f\left(x\right)\to+\infty$. By the intermediate value property, $f\left(X\right)=\mathbb R$. $\blacksquare$

---

## 1.2-6

Let $f:\left[a,b\right]\to\left[a,b\right]$ satisfy

$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|\le k\left|x_1-x_2\right|,\quad\forall x_1,x_2\in\left[a,b\right],
$$

where $k< 1$ is a constant. Suppose there exists $c\in\left(a,b\right)$ such that $f\left(c\right)=c$. Prove that $\left|f_n\left(x\right)-c\right|\le k^n\left(b-a\right)$, where $f_n$ is the $n$-fold composite of $f$.

### Solution 1.2-6

Since $f\left(c\right)=c$, by induction $f_n\left(c\right)=c$ (for $n=1$, this is $f\left(c\right)=c$; if $f_n\left(c\right)=c$, then $f_{n+1}\left(c\right)=f\left(f_n\left(c\right)\right)=f\left(c\right)=c$).

For any $x\in\left[a,b\right]$, repeatedly applying the Lipschitz condition:

$$
\left|f_n\left(x\right)-c\right|=\left|f_n\left(x\right)-f_n\left(c\right)\right|\le k\left|f_{n-1}\left(x\right)-f_{n-1}\left(c\right)\right|\le\cdots\le k^n\left|x-c\right|.
$$

Since $x,c\in\left[a,b\right]$, $\left|x-c\right|\le b-a$. Hence

$$
\left|f_n\left(x\right)-c\right|\le k^n\left(b-a\right).
$$

$\blacksquare$

---

## 1.2-10

Consider the function $y=\left[\frac43\sin^2 x\right]$, where $\left[\ \right]$ denotes the integer part. Prove that this function has period $\pi$.

### Solution 1.2-10

By **Basic Knowledge: Definition of a Periodic Function**, it suffices to verify $y\left(x+\pi\right)=y\left(x\right)$. Since

$$
\sin^2\left(x+\pi\right)=\left(\sin\left(x+\pi\right)\right)^2=\left(-\sin x\right)^2=\sin^2 x,
$$

we have

$$
\frac43\sin^2\left(x+\pi\right)=\frac43\sin^2 x,
$$

and after taking the integer part,

$$
\left[\frac43\sin^2\left(x+\pi\right)\right]=\left[\frac43\sin^2 x\right].
$$

That is, $y\left(x+\pi\right)=y\left(x\right)$. By **Basic Knowledge: Definition of a Periodic Function**, $\pi$ is a period of $y$. $\blacksquare$

---

## 1.2-11

Let

$$
f\left(x\right)=\begin{cases}e^x,&x\le0,\\ x,&x> 0;\end{cases}\quad g\left(x\right)=\begin{cases}x,&x\le0,\\ -x^2,&x> 0;\end{cases}
$$

Find the piecewise expressions for $f\left(g\left(x\right)\right)$ and $g\left(f\left(x\right)\right)$, and compute $f\left(g\left(1\right)\right)$.

### Solution 1.2-11

First find $f\left(g\left(x\right)\right)$. By **Basic Knowledge: Definition of a Composite Function**:

- When $x\le0$, $g\left(x\right)=x\le0$, so $f\left(g\left(x\right)\right)=f\left(x\right)=e^x$;
- When $x> 0$, $g\left(x\right)=-x^2< 0$, so

$$
f\left(g\left(x\right)\right)=f\left(-x^2\right)=e^{-x^2}.
$$

Therefore

$$
f\left(g\left(x\right)\right)=\begin{cases}e^x,&x\le0,\\ e^{-x^2},&x> 0.\end{cases}
$$

Now find $g\left(f\left(x\right)\right)$:

- When $x\le0$, $f\left(x\right)=e^x> 0$ (since $0< e^x\le1$ for $x\le0$), so

$$
g\left(f\left(x\right)\right)=g\left(e^x\right)=-\left(e^x\right)^2=-e^{2x};
$$

- When $x> 0$, $f\left(x\right)=x> 0$, so $g\left(f\left(x\right)\right)=g\left(x\right)=-x^2$.

Therefore

$$
g\left(f\left(x\right)\right)=\begin{cases}-e^{2x},&x\le0,\\ -x^2,&x> 0.\end{cases}
$$

Finally, $g\left(1\right)=-1^2=-1$, so

$$
f\left(g\left(1\right)\right)=f\left(-1\right)=e^{-1}=\frac1e.
$$

$\blacksquare$

---

## 1.2-14

Determine whether the following functions are bounded:

(1) $y=5\sin e^x+10^{10}$;

(2)

$$
y=\sqrt{x+10}-\sqrt{x}\quad\left(x> 0\right);
$$

(3) $y=\operatorname{ch}x$;

(4)

$$
y=\ln\left(x+\sqrt{x^2+1}\right)\quad\left(x> 0\right).
$$

### Solution 1.2-14

(1) For any $x\in\mathbb R$, $\left|\sin e^x\right|\le1$, so $\left|5\sin e^x\right|\le5$, and thus

$$
\left|y\right|=\left|5\sin e^x+10^{10}\right|\le5+10^{10}.
$$

Taking $M=5+10^{10}$, by **Proposition 2.1 (Necessary and Sufficient Condition for a Bounded Function)**, $y=5\sin e^x+10^{10}$ is bounded.

(2) For $x> 0$, rationalizing gives

$$
\sqrt{x+10}-\sqrt{x}=\frac{10}{\sqrt{x+10}+\sqrt{x}}.
$$

Since the denominator $\sqrt{x+10}+\sqrt{x}> \sqrt{10}$ ($x> 0$), we have $0< y< \frac{10}{\sqrt{10}}=\sqrt{10}$. Taking $M=\sqrt{10}$, by **Proposition 2.1 (Necessary and Sufficient Condition for a Bounded Function)**, $y=\sqrt{x+10}-\sqrt{x}$ is bounded.

(3) $y=\operatorname{ch}x=\frac{e^x+e^{-x}}2$. As $x\to+\infty$, $e^x\to+\infty$, so $y\to+\infty$; there is no constant $M> 0$ such that $\left|y\right|\le M$ for all $x\in\mathbb R$. By **Proposition 2.1 (Necessary and Sufficient Condition for a Bounded Function)**, $y=\operatorname{ch}x$ is not bounded.

(4) As $x\to+\infty$, $x+\sqrt{x^2+1}\sim2x$, so

$$
y=\ln\left(x+\sqrt{x^2+1}\right)\sim\ln\left(2x\right)\to+\infty,
$$

and there is no constant $M> 0$ such that $\left|y\right|\le M$ for all $x> 0$. By **Proposition 2.1 (Necessary and Sufficient Condition for a Bounded Function)**, $y=\ln\left(x+\sqrt{x^2+1}\right)$ is not bounded. $\blacksquare$
