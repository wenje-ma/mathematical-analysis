# week17

> **Proposition 3.1 (Unique Extremum is Global)**
> 
> If $f$ is continuous on $\left(a,b\right)$ (or $\left[a,b\right]$) and $x_0$ is the only extremum point, then it is the global maximum (if a local max) or global minimum (if a local min).

> **Theorem 3.1 (First Sufficient Condition for Extrema)**
> 
> If $f$ is differentiable on $\left(a,b\right)$ with $f'\left(x_0\right)=0$, and $f'>0$ on $\left(x_0-r,x_0\right)$ while $f'<0$ on $\left(x_0,x_0+r\right)$, then $f\left(x_0\right)$ is a local maximum; if the signs are reversed, it is a local minimum.

> **Theorem 3.2 (Second Sufficient Condition for Extrema)**
> 
> If $f'\left(x_0\right)=0$ and $f''\left(x_0\right)$ exists, then $f''\left(x_0\right)>0$ implies $x_0$ is a local minimum, and $f''\left(x_0\right)<0$ implies $x_0$ is a local maximum.

> **Theorem 4.1 (Local Taylor Expansion)**
> 
> If $f$ has $n$ derivatives at $x_0$, then $f\left(x\right)=f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{f^{\left(n\right)}\left(x_0\right)}{n!}\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right)$ as $x\to{x}_0$.

> **Theorem 4.2 (Taylor Formula with Lagrange Remainder)**
> 
> If $f$ has $n$ continuous derivatives on $\left[a,b\right]$ and $n+1$ derivatives on $\left(a,b\right)$, then for any $x,x_0\in\left[a,b\right]$, there exists $\xi$ between $x_0$ and $x$ such that $f\left(x\right)=f\left(x_0\right)+\cdots+\frac{f^{\left(n+1\right)}\left(\xi\right)}{\left(n+1\right)!}\left(x-x_0\right)^{n+1}$.

## 3.3-5

Prove $x^\alpha-\alpha{x}+\alpha-1\le0$ for all $x>0$, where $0<\alpha<1$.

### Solution to 3.3-5

Let $f\left(x\right)=x^\alpha-\alpha{x}+\alpha-1$. Then $f'\left(x\right)=\alpha\left(x^{\alpha-1}-1\right)=0$ gives $x=1$. For $0<{}x<1$, $f'>0$; for $x>1$, $f'<0$. By **Theorem 3.1 (First Sufficient Condition for Extrema)**, $x=1$ is a maximum. Since $f\left(1\right)=0$, by **Proposition 3.1 (Unique Extremum is Global)**, $f\left(x\right)\le0$. $\blacksquare$

## 3.3-6

Prove: if $a,b>0$, $p,q>1$, and $\frac1p+\frac1q=1$, then $a^{1/p}b^{1/q}\le\frac{a}{p}+\frac{b}{q}$.

### Solution to 3.3-6

Taking $\alpha=\frac1p$ in 3.3-5 and substituting $x=\frac{a}{b}$, multiplying by $b$, and simplifying using $1-\frac1p=\frac1q$, we obtain

$$
a^{1/p}b^{1/q}\le\frac{a}{p}+\frac{b}{q}.
$$

This is Young's inequality. $\blacksquare$

## 3.3-7

Let $\triangle{A}BC$ have sides $a,b,c$ with $b=c$ and perimeter $a+b+c=2l$. When is the area maximized?

### Solution to 3.3-7

Since $b=c$, the triangle is isosceles with $b=l-\frac{a}2$. The area is

$$
S=\frac12a\sqrt{l^2-la}.
$$

Maximizing $S^2=\frac14\left(l^2a^2-la^3\right)$, the derivative $\left(S^2\right)'=\frac{la}{4}\left(2l-3a\right)=0$ gives $a=\frac{2l}{3}$. By **Theorem 3.1 (First Sufficient Condition for Extrema)**, this is a maximum. Then $b=c=\frac{2l}{3}$, so the area is maximized when the triangle is equilateral. $\blacksquare$

## 3.3-8

Let $f\left(x\right)=\sin^px+\cos^px$. Find its maximum and minimum on $\left[0,\frac\pi2\right]$.

### Solution to 3.3-8

Differentiating,

$$
f'\left(x\right)=p\sin{x}\cos{x}\left(\sin^{p-2}x-\cos^{p-2}x\right).
$$

The critical point in $\left(0,\frac\pi2\right)$ is $x=\frac\pi4$. The values are $f\left(0\right)=1$, $f\left(\frac\pi4\right)=2^{1-p/2}$, $f\left(\frac\pi2\right)=1$. For $p>2$, the maximum is $1$ (at endpoints) and the minimum is $2^{1-p/2}$ (at $x=\frac\pi4$). $\blacksquare$

## 3.4-1-2

Write the local Taylor formula of $y=\frac1{1-x}$ at $x=0$.

### Solution to 3.4-1-2

Since $f^{\left(n\right)}\left(x\right)=\frac{n!}{\left(1-x\right)^{n+1}}$, we have $f^{\left(n\right)}\left(0\right)=n!$. By **Theorem 4.1 (Local Taylor Expansion)**,

$$
\frac1{1-x}=1+x+x^2+\cdots+x^n+o\left(x^n\right).
$$

$\blacksquare$

## 3.4-1-4

Write the local Taylor formula of $y=\arctan{x}$ at $x=0$ up to $x^5$.

### Solution to 3.4-1-4

Computing derivatives at $0$: $f\left(0\right)=0$, $f'\left(0\right)=1$, $f''\left(0\right)=0$, $f'''\left(0\right)=-2$, $f^{\left(4\right)}\left(0\right)=0$, $f^{\left(5\right)}\left(0\right)=24$. By **Theorem 4.1 (Local Taylor Expansion)**,

$$
\arctan{x}=x-\frac{x^3}3+\frac{x^5}5+o\left(x^5\right).
$$

$\blacksquare$

## 3.4-1-5

Write the local Taylor formula of $y=\tan{x}$ at $x=0$ up to $x^3$.

### Solution to 3.4-1-5

Computing: $f\left(0\right)=0$, $f'\left(0\right)=1$, $f''\left(0\right)=0$, $f'''\left(0\right)=2$. By **Theorem 4.1 (Local Taylor Expansion)**,

$$
\tan{x}=x+\frac{x^3}3+o\left(x^3\right).
$$

$\blacksquare$

## 3.4-4

Expand $y=\sin\left(x+\alpha\right)$ at $\alpha=0$ using Taylor formula with Lagrange remainder, and estimate the remainder.

### Solution to 3.4-4

Treating $x$ as constant and differentiating w.r.t. $\alpha$, by **Theorem 4.2 (Taylor Formula with Lagrange Remainder)**,

$$
\sin\left(x+\alpha\right)=\sin{x}+\left(\cos{x}\right)\alpha-\frac{\sin\left(x+\xi\right)}2\alpha^2,
$$

where $\xi$ is between $0$ and $\alpha$. The remainder satisfies $\left|r\left(\alpha\right)\right|\le\frac{\alpha^2}2$. $\blacksquare$

## 3.4-5

Expand $y=x+\frac{x^3}3$ at $x=\pm1$. Explain why the remainder of any polynomial's Taylor expansion is $0$.

### Solution to 3.4-5

$f'\left(x\right)=1+x^2$, $f''\left(x\right)=2x$, $f'''\left(x\right)=2$, $f^{\left(4\right)}\left(x\right)=0$. At $x=1$,

$$
x+\frac{x^3}3=\frac43+2\left(x-1\right)+\left(x-1\right)^2+\frac13\left(x-1\right)^3.
$$

At $x=-1$,

$$
x+\frac{x^3}3=-\frac43+2\left(x+1\right)-\left(x+1\right)^2+\frac13\left(x+1\right)^3.
$$

For any polynomial $P_n$ of degree $n$, $P_n^{\left(n+1\right)}\equiv0$. By **Theorem 4.2 (Taylor Formula with Lagrange Remainder)**, the remainder is $0$. $\blacksquare$
