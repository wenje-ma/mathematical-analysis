# Assignment 6

> **Proposition 6.1** (Important Limit $\lim\limits_{x\to0}\frac{\sin x}{x}=1$) $\lim\limits_{x\to0}\frac{\sin x}{x}=1$.

> **Important Limit** (Functional Version of the Number $e$) $\lim\limits_{x\to\infty}\left(1+\frac1x\right)^x=e$.

> **Theorem 6.2** (Squeeze Theorem for Functions) Let
> $$
> y=f\left(x\right),y=g\left(x\right),y=h\left(x\right)
> $$
> be defined in a deleted neighborhood of the point $a$, and suppose $h\left(x\right)\le f\left(x\right)\le g\left(x\right)$. If $\lim g\left(x\right)=\lim h\left(x\right)=l$, then $\lim f\left(x\right)=l$.

### Problem 1

(Problem 1.6-2) Using the $\varepsilon$-$\delta$ language, prove that if $\lim\limits_{x\to a}f\left(x\right)=l$ and $l> 0$, then there exists a $\delta> 0$ such that $f\left(x\right)> \frac l2$ whenever $0< \left|x-a\right|< \delta$.

### Solution to Problem 1

Take $\varepsilon=\frac l2> 0$. By **Definition** (Limit of a Function), there exists $\delta> 0$ such that $\left|f\left(x\right)-l\right|< \frac l2$ when $0< \left|x-a\right|< \delta$. By **Proposition 1.7** (Triangle Inequality) in Chapter 1,

$$
f\left(x\right)=l-\left(l-f\left(x\right)\right)\ge l-\left|f\left(x\right)-l\right|> l-\frac l2=\frac l2.
$$

Hence $f\left(x\right)> \frac l2$. $\blacksquare$

### Problem 2

(Problem 1.6-3) Using the limit $\lim\limits_{x\to0}\frac{\sin x}{x}=1$, find the following limits:
(1) $\lim\limits_{x\to0}\frac{\sin\alpha x}{\sin\beta x}\left(\beta\ne0\right)$;

(2) $\lim\limits_{x\to0}\frac{\tan3x-\tan5x}{\sin2x}$;

(3) $\lim\limits_{x\to0}\frac{1-\cos x}{x^2}$;

(4) $\lim\limits_{x\to a}\frac{\sin x-\sin a}{x-a}$.

### Solution to Problem 2

(1) $\frac{\sin\alpha x}{\sin\beta x}=\frac{\alpha}{\beta}\cdot\frac{\sin\alpha x}{\alpha x}\cdot\frac{\beta x}{\sin\beta x}$. By **Proposition 6.1** (Important Limit) and **Theorem 5.1** in Chapter 1, the limit is $\frac{\alpha}{\beta}$.

(2)

$$
\tan3x-\tan5x=\frac{\sin3x}{\cos3x}-\frac{\sin5x}{\cos5x}=\frac{\sin3x\cos5x-\cos3x\sin5x}{\cos3x\cos5x}=\frac{-\sin2x}{\cos3x\cos5x}.
$$

Hence the original expression $=\frac{-1}{\cos3x\cos5x}\to-1$.

(3) $1-\cos x=2\sin^2\frac x2$, so

$$
\frac{1-\cos x}{x^2}=\frac{2\sin^2\left(x/2\right)}{x^2}=\frac12\left(\frac{\sin\left(x/2\right)}{x/2}\right)^2\to\frac12.
$$

(4)

$$
\sin x-\sin a=2\cos\frac{x+a}2\sin\frac{x-a}2,
$$
so

$$
\frac{\sin x-\sin a}{x-a}=\cos\frac{x+a}2\cdot\frac{\sin\left(x-a\right)/2}{\left(x-a\right)/2}\to\cos a.
$$

$\blacksquare$

### Problem 3

(Problem 1.6-4-1) Using $\lim\limits_{x\to\infty}\left(1+\frac1x\right)^x=e$, find the limit: $\lim\limits_{x\to\infty}\left(1+\frac3x\right)^x\cdot\left(1+\frac5x\right)^x$.

### Solution to Problem 3

$$
\left(1+\frac3x\right)^x=\left[\left(1+\frac3x\right)^{x/3}\right]^3\to e^3,\left(1+\frac5x\right)^x=\left[\left(1+\frac5x\right)^{x/5}\right]^5\to e^5.
$$

By **Theorem 5.1** in Chapter 1, the limit of the product is $e^3\cdot e^5=e^8$. $\blacksquare$

### Problem 4

(Problem 1.6-4-3) Find the limit: $\lim\limits_{x\to0}\left(\frac{1+x}{1-x}\right)^{1/x}$.

### Solution to Problem 4

$$
\left(\frac{1+x}{1-x}\right)^{1/x}=\left[\left(1+\frac{2x}{1-x}\right)^{\frac{1-x}{2x}}\right]^{\frac{2}{1-x}}.
$$

The base tends to $e$ and the exponent $\frac2{1-x}\to2$. By the **Important Limit** (The Number $e$) and the related operations of **Theorem 6.2**, the limit is $e^2$. $\blacksquare$

### Problem 5

(Problem 1.6-4-5) Find the limit: $\lim\limits_{y\to0}\left(1-5y\right)^{1/y}$.

### Solution to Problem 5

$$
\left(1-5y\right)^{1/y}=\left[\left(1+\frac1{-1/\left(5y\right)}\right)^{-1/\left(5y\right)}\right]^{-5}.
$$

The base tends to $e$ and the exponent is $-5$. By the **Important Limit** (The Number $e$), the limit is $e^{-5}=\frac1{e^5}$. $\blacksquare$

### Problem 6

(Problem 1.6-4-6) Find the limit: $\lim\limits_{x\to\infty}\left(1+\frac1x\right)^{x+100}$.

### Solution to Problem 6

$$
\left(1+\frac1x\right)^{x+100}=\left(1+\frac1x\right)^x\cdot\left(1+\frac1x\right)^{100}\to e\cdot1=e.

$$

$\blacksquare$
### Problem 7

(Problem 1.6-5) Find the constants $a$ and $b$ such that

$$
\lim\limits_{x\to+\infty}\left[\frac{x^2+1}{x+1}-\left(ax+b\right)\right]=0.
$$

Explain the geometric meaning.

### Solution to Problem 7

$$
\frac{x^2+1}{x+1}-ax-b=\frac{x^2+1-\left(ax+b\right)\left(x+1\right)}{x+1}=\frac{\left(1-a\right)x^2-\left(a+b\right)x+1-b}{x+1}.
$$

For this to tend to $0$, the degree of the numerator must be lower than that of the denominator, so $1-a=0$ and $a+b=0$. Solving gives $a=1,b=-1$.

Geometric meaning: the line $y=x-1$ is the slant asymptote of the curve $y=\frac{x^2+1}{x+1}$ as $x\to+\infty$. $\blacksquare$

### Problem 8

(Problem 1.6-7) Prove that $\lim\limits_{x\to+\infty}\left(1+\frac1x\right)^{x^2}=+\infty$.

### Solution to Problem 8

$$
\left(1+\frac1x\right)^{x^2}=\left[\left(1+\frac1x\right)^x\right]^x.
$$

When $x$ is sufficiently large, $\left(1+\frac1x\right)^x> 2$ (since it tends to $e> 2$), so $\left(1+\frac1x\right)^{x^2}> 2^x\to+\infty$. Hence the limit is $+\infty$. $\blacksquare$

### Problem 9

(Problem 1.6-9) Let $\lim\limits_{x\to+\infty}\frac{f\left(x\right)}x=0$ and $f\left(x\right)> 0\left(x> 0\right)$. Prove that $\lim\limits_{x\to+\infty}\left(1+\frac1x\right)^{f\left(x\right)}=1$.

### Solution to Problem 9

Taking logarithms:

$$
\left(1+\frac1x\right)^{f\left(x\right)}=e^{f\left(x\right)\ln\left(1+1/x\right)}.
$$

Since

$$
0< f\left(x\right)\ln\left(1+\frac1x\right)< f\left(x\right)\cdot\frac1x\to0,
$$

by **Theorem 6.2** (Squeeze Theorem for Functions), the exponent tends to $0$. By the continuity of $e^\top$, the original limit is $e^0=1$. $\blacksquare$

### Problem 10

(Problem 1.6-10) Let $y=D\left(x\right)$ be the Dirichlet function. Prove that for any point $a\in\mathbb R$, the limit $\lim\limits_{x\to a}D\left(x\right)$ does not exist.

### Solution to Problem 10

Take a rational sequence $\left\{r_n\right\}$ and an irrational sequence $\left\{s_n\right\}$, both with limit $a$ (by the density of the rationals and irrationals). Then $D\left(r_n\right)=1\to1$ and $D\left(s_n\right)=0\to0$. The two subsequences have different limits; by the sequential criterion relating functional limits to sequential limits, $\lim\limits_{x\to a}D\left(x\right)$ does not exist. $\blacksquare$

### Problem 11

(Problem 1.6-11) Find the limit: $\lim\limits_{x\to+\infty}\frac{\left(\ln x\right)^5}{x}$.

### Solution to Problem 11

Make the substitution $y=\ln x$, so $x=e^y$. As $x\to+\infty$, $y\to+\infty$. The original expression becomes $\lim\limits_{y\to+\infty}\frac{y^5}{e^y}=0$ (the exponential function grows faster than any power function). $\blacksquare$
