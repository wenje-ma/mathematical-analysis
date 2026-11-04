# week2

> **Proposition 2.1 (Necessary and Sufficient Condition for a Bounded Function)**
> 
> A function $f:X\to Y$ is bounded if and only if there exists $M> 0$ such that $\left|f\left(x\right)\right|\le M$ for all $x\in X$.

## 1.2-1

Find the domains of the following functions:

(1) $y=\sqrt{x^2-16}$;

(2) $y=\frac{1}{\sqrt{x^2-3x+2}}$;

(3) $y=\ln\frac{x^2-2}{2}$;

(4) $y=\arccos\left(2\sin x\right)$.

### Solution to 1.2-1

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

### Solution to 1.2-2

(1) When $x\in\left(0,5\right)$, $x^2\in\left(0,25\right)$, so $1+x^2\in\left(1,26\right)$, and thus $\sqrt{1+x^2}\in\left(1,\sqrt{26}\right)$. By Definition of a Function, $f\left(X\right)=\left(1,\sqrt{26}\right)$.

(2) As $x$ ranges over $\mathbb R\backslash\left\{0\right\}$, $\frac1x$ ranges over $\mathbb R\backslash\left\{0\right\}$. The range of $\sin t$ over $t\in\mathbb R$ is $\left[-1,1\right]$; removing one point $t=0$ (where $\sin0=0$) does not change the range ($0$ is still attainable, e.g. at $t=\pi$). Hence $f\left(X\right)=\left[-1,1\right]$.

(3) For any $x\in\mathbb R$, the fractional part $\left\{x\right\}=x-\left[x\right]$ satisfies $0\le\left\{x\right\}< 1$. Conversely, for any $y\in\left[0,1\right)$, taking $x=y$ gives $\left\{x\right\}=y$. Hence $f\left(X\right)=\left[0,1\right)$.

(4) $f'\left(x\right)=3x^2+1> 0$, so $f$ is strictly increasing on $\mathbb R$. Moreover, as $x\to-\infty$, $f\left(x\right)\to-\infty$, and as $x\to+\infty$, $f\left(x\right)\to+\infty$. By the intermediate value property, $f\left(X\right)=\mathbb R$. $\blacksquare$

## 1.2-6

Let $f:\left[a,b\right]\to\left[a,b\right]$ satisfy

$$
\left|f\left(x_1\right)-f\left(x_2\right)\right|\le k\left|x_1-x_2\right|,\quad\forall x_1,x_2\in\left[a,b\right],
$$

where $k< 1$ is a constant. Suppose there exists $c\in\left(a,b\right)$ such that $f\left(c\right)=c$. Prove that $\left|f_n\left(x\right)-c\right|\le k^n\left(b-a\right)$, where $f_n$ is the $n$-fold composite of $f$.

### Solution to 1.2-6

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

## 1.2-10

Consider the function $y=\left[\frac43\sin^2 x\right]$, where $\left[\ \right]$ denotes the integer part. Prove that this function has period $\pi$.

### Solution to 1.2-10

By Definition of a Periodic Function, it suffices to verify $y\left(x+\pi\right)=y\left(x\right)$. Since

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

That is, $y\left(x+\pi\right)=y\left(x\right)$. By Definition of a Periodic Function, $\pi$ is a period of $y$. $\blacksquare$
