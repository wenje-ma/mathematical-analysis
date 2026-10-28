# week16

> **Theorem 4.1 (Local Taylor Expansion)**<br>If $f$ has $n$ derivatives at $x_0$, then $f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right)$ as $x\to x_0$.

> **Theorem 4.2 (Taylor Formula with Lagrange Remainder)**<br>If $f$ has $n$ continuous derivatives on $\left[a,b\right]$ and $n+1$ derivatives on $\left(a,b\right)$, then for any $x,x_0\in\left[a,b\right]$, there exists $\xi$ between $x_0$ and $x$ such that $f\left(x\right)=f\left(x_0\right)+\cdots+\frac{f^{\left(n+1\right)}\left(\xi\right)}{\left(n+1\right)!}\left(x-x_0\right)^{n+1}$.

---

## 3.4-1-2

Write the local Taylor formula of $y=\frac1{1-x}$ at $x=0$.

### Solution 3.4-1-2

Since $f^{\left(n\right)}\left(x\right)=\frac{n!}{\left(1-x\right)^{n+1}}$, we have $f^{\left(n\right)}\left(0\right)=n!$. By **Theorem 4.1 (Local Taylor Expansion)**,

$$
\frac1{1-x}=1+x+x^2+\cdots+x^n+o\left(x^n\right).
$$

$\blacksquare$

---

## 3.4-1-4

Write the local Taylor formula of $y=\arctan x$ at $x=0$ up to $x^5$.

### Solution 3.4-1-4

Computing derivatives at $0$: $f\left(0\right)=0$, $f'\left(0\right)=1$, $f''\left(0\right)=0$, $f'''\left(0\right)=-2$, $f^{\left(4\right)}\left(0\right)=0$, $f^{\left(5\right)}\left(0\right)=24$. By **Theorem 4.1 (Local Taylor Expansion)**,

$$
\arctan x=x-\frac{x^3}3+\frac{x^5}5+o\left(x^5\right).
$$

$\blacksquare$

---

## 3.4-1-5

Write the local Taylor formula of $y=\tan x$ at $x=0$ up to $x^3$.

### Solution 3.4-1-5

Computing: $f\left(0\right)=0$, $f'\left(0\right)=1$, $f''\left(0\right)=0$, $f'''\left(0\right)=2$. By **Theorem 4.1 (Local Taylor Expansion)**,

$$
\tan x=x+\frac{x^3}3+o\left(x^3\right).
$$

$\blacksquare$

---

## 3.4-4

Expand $y=\sin\left(x+\alpha\right)$ at $\alpha=0$ using Taylor formula with Lagrange remainder, and estimate the remainder.

### Solution 3.4-4

Treating $x$ as constant and differentiating w.r.t. $\alpha$, by **Theorem 4.2 (Taylor Formula with Lagrange Remainder)**,

$$
\sin\left(x+\alpha\right)=\sin x+\left(\cos x\right)\alpha-\frac{\sin\left(x+\xi\right)}2\alpha^2,
$$

where $\xi$ is between $0$ and $\alpha$. The remainder satisfies $\left|r\left(\alpha\right)\right|\le\frac{\alpha^2}2$. $\blacksquare$

---

## 3.4-5

Expand $y=x+\frac{x^3}3$ at $x=\pm1$. Explain why the remainder of any polynomial's Taylor expansion is $0$.

### Solution 3.4-5

$f'\left(x\right)=1+x^2$, $f''\left(x\right)=2x$, $f'''\left(x\right)=2$, $f^{\left(4\right)}\left(x\right)=0$. At $x=1$,

$$
x+\frac{x^3}3=\frac43+2\left(x-1\right)+\left(x-1\right)^2+\frac13\left(x-1\right)^3.
$$

At $x=-1$,

$$
x+\frac{x^3}3=-\frac43+2\left(x+1\right)-\left(x+1\right)^2+\frac13\left(x+1\right)^3.
$$

For any polynomial $P_n$ of degree $n$, $P_n^{\left(n+1\right)}\equiv0$. By **Theorem 4.2 (Taylor Formula with Lagrange Remainder)**, the remainder is $0$. $\blacksquare$

---

## 3.4-7

Prove that the derivative of the $(n+1)$-th Taylor polynomial of $f$ at $a$ equals the $n$-th Taylor polynomial of $f'$ at $a$.

### Solution 3.4-7

Differentiating $T_{n+1}\left(x\right)=f\left(a\right)+f'\left(a\right)\left(x-a\right)+\cdots+\frac{f^{\left(n+1\right)}\left(a\right)}{\left(n+1\right)!}\left(x-a\right)^{n+1}$ gives

$$
T_{n+1}'\left(x\right)=f'\left(a\right)+f''\left(a\right)\left(x-a\right)+\cdots+\frac{f^{\left(n+1\right)}\left(a\right)}{n!}\left(x-a\right)^n,
$$

which is exactly the $n$-th Taylor polynomial of $f'$. $\blacksquare$

---

## 3.4-10

Prove that as $x\to0$, $\arctan x=x-\frac{x^3}3+\frac{x^5}5-\cdots+\left(-1\right)^m\frac{x^{2m+1}}{2m+1}+o\left(x^{2m+1}\right)$.

### Solution 3.4-10

Since $f'\left(x\right)=\frac1{1+x^2}$, substituting $-x^2$ into the geometric expansion (3.4-1-2) gives

$$
\frac1{1+x^2}=1-x^2+x^4-\cdots+\left(-1\right)^m x^{2m}+o\left(x^{2m}\right).
$$

Integrating term by term (by 3.4-7),

$$
\arctan x=x-\frac{x^3}3+\frac{x^5}5-\cdots+\left(-1\right)^m\frac{x^{2m+1}}{2m+1}+o\left(x^{2m+1}\right).
$$

$\blacksquare$

---

## 3.4-11

Let $f\left(x\right)=x^{1/5}$, $x=32$, $\Delta x=0.16$. Given $f\left(32\right)+f'\left(32\right)\Delta x=2.002$, prove that the absolute error is less than $10^{-6}$.

### Solution 3.4-11

The error is the Lagrange remainder:

$$
\left|R_1\right|=\frac2{25}\xi^{-9/5}\cdot\left(0.16\right)^2.
$$

Since $\xi> 32$, $\xi^{-9/5}< 2^{-9}=\frac1{512}$. Thus

$$
\left|R_1\right|< \frac2{25}\cdot\frac1{512}\cdot0.0256=4\times10^{-6}.
$$

$\blacksquare$

---

## 3.4-12

Let $f'\left(x_0\right)=\cdots=f^{\left(n-1\right)}\left(x_0\right)=0$ and $f^{\left(n\right)}\left(x_0\right)\ne0$. Prove: if $n$ is odd, $x_0$ is not an extremum; if $n$ is even and $f^{\left(n\right)}\left(x_0\right)> 0$, $x_0$ is a local minimum; if $f^{\left(n\right)}\left(x_0\right)< 0$, it is a local maximum.

### Solution 3.4-12

By **Theorem 4.1 (Local Taylor Expansion)**,

$$
f\left(x\right)-f\left(x_0\right)=\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right).
$$

If $n$ is odd, $\left(x-x_0\right)^n$ changes sign on either side of $x_0$, so $f\left(x\right)-f\left(x_0\right)$ changes sign; $x_0$ is not an extremum.

If $n$ is even, $\left(x-x_0\right)^n> 0$ for $x\ne x_0$. If $f^{\left(n\right)}\left(x_0\right)> 0$, then $f\left(x\right)> f\left(x_0\right)$, so $x_0$ is a local minimum. If $f^{\left(n\right)}\left(x_0\right)< 0$, then $f\left(x\right)< f\left(x_0\right)$, so $x_0$ is a local maximum. $\blacksquare$
