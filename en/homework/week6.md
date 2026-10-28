# week6

> **Basic Knowledge: Definition of Function Limit**<br>Let $y=f\left(x\right)$ be defined in a punctured neighborhood of $a$. If there exists $l\in\mathbb R$ such that for every $\varepsilon> 0$ there exists $\delta> 0$ with $0< \left|x-a\right|< \delta$ implying $\left|f\left(x\right)-l\right|< \varepsilon$, then $\lim_{x\to a}f\left(x\right)=l$.

> **Basic Knowledge: The Important Limit $e$ (Function Version)**<br>$\lim_{x\to\infty}\left(1+\frac1x\right)^x=e$.

> **Proposition 1.7 (Triangle Inequality)**<br>For any real $a,b,c$, $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **Theorem 5.1 (Arithmetic of Function Limits)**<br>If $\lim f\left(x\right)=l_1$ and $\lim g\left(x\right)=l_2$, then $\lim\left(f\pm g\right)=l_1\pm l_2$, $\lim\left(f\cdot g\right)=l_1\cdot l_2$, and when $l_2\ne0$, $\lim\frac{f}{g}=\frac{l_1}{l_2}$.

> **Proposition 6.1 (Important Limit $\lim_{x\to0}\frac{\sin x}{x}=1$)**<br>$\lim_{x\to0}\frac{\sin x}{x}=1$.

> **Theorem 6.2 (Squeeze Theorem for Functions)**<br>Let $f\left(x\right),g\left(x\right),h\left(x\right)$ be defined in a punctured neighborhood of $a$ with $h\left(x\right)\le f\left(x\right)\le g\left(x\right)$. If $\lim g\left(x\right)=\lim h\left(x\right)=l$, then $\lim f\left(x\right)=l$.

---

## 1.6-2

Prove by $\varepsilon$-$\delta$ language: if $\lim_{x\to a}f\left(x\right)=l$ and $l> 0$, then there exists $\delta> 0$ such that $f\left(x\right)> \frac l2$ whenever $0< \left|x-a\right|< \delta$.

### Solution 1.6-2

Take $\varepsilon=\frac l2> 0$. By **Basic Knowledge: Definition of Function Limit**, there exists $\delta> 0$ such that $0< \left|x-a\right|< \delta$ implies $\left|f\left(x\right)-l\right|< \frac l2$. By **Proposition 1.7 (Triangle Inequality)**,

$$
f\left(x\right)=l-\left(l-f\left(x\right)\right)\ge l-\left|f\left(x\right)-l\right|> l-\frac l2=\frac l2.
$$

Thus $f\left(x\right)> \frac l2$. $\blacksquare$

---

## 1.6-3

Use $\lim_{x\to0}\frac{\sin x}{x}=1$ to find:

(1) $\lim_{x\to0}\frac{\sin\alpha x}{\sin\beta x}$ ($\beta\ne0$);

(2) $\lim_{x\to0}\frac{\tan3x-\tan5x}{\sin2x}$;

(3) $\lim_{x\to0}\frac{1-\cos x}{x^2}$;

(4) $\lim_{x\to a}\frac{\sin x-\sin a}{x-a}$.

### Solution 1.6-3

(1) $\frac{\sin\alpha x}{\sin\beta x}=\frac{\alpha}{\beta}\cdot\frac{\sin\alpha x}{\alpha x}\cdot\frac{\beta x}{\sin\beta x}$. By **Proposition 6.1 (Important Limit $\lim_{x\to0}\frac{\sin x}{x}=1$)** and **Theorem 5.1 (Arithmetic of Function Limits)**, the limit is $\frac{\alpha}{\beta}$.

(2)

$$
\tan3x-\tan5x=\frac{\sin3x}{\cos3x}-\frac{\sin5x}{\cos5x}=\frac{\sin3x\cos5x-\cos3x\sin5x}{\cos3x\cos5x}=\frac{-\sin2x}{\cos3x\cos5x}.
$$

The expression $=\frac{-1}{\cos3x\cos5x}\to-1$.

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

---

## 1.6-4-1

Use $\lim_{x\to\infty}\left(1+\frac1x\right)^x=e$ to find: $\lim_{x\to\infty}\left(1+\frac3x\right)^x\cdot\left(1+\frac5x\right)^x$.

### Solution 1.6-4-1

$$
\left(1+\frac3x\right)^x=\left[\left(1+\frac3x\right)^{x/3}\right]^3\to e^3,\quad\left(1+\frac5x\right)^x=\left[\left(1+\frac5x\right)^{x/5}\right]^5\to e^5.
$$

By **Theorem 5.1 (Arithmetic of Function Limits)**, the product is $e^3\cdot e^5=e^8$. $\blacksquare$

---

## 1.6-4-3

Find: $\lim_{x\to0}\left(\frac{1+x}{1-x}\right)^{1/x}$.

### Solution 1.6-4-3

$$
\left(\frac{1+x}{1-x}\right)^{1/x}=\left[\left(1+\frac{2x}{1-x}\right)^{\frac{1-x}{2x}}\right]^{\frac2{1-x}}.
$$

The base tends to $e$ and the exponent $\frac2{1-x}\to2$. By **Basic Knowledge: The Important Limit $e$ (Function Version)** and **Theorem 6.2 (Squeeze Theorem for Functions)**, the limit is $e^2$. $\blacksquare$

---

## 1.6-4-5

Find: $\lim_{y\to0}\left(1-5y\right)^{1/y}$.

### Solution 1.6-4-5

$$
\left(1-5y\right)^{1/y}=\left[\left(1+\frac1{-1/\left(5y\right)}\right)^{-1/\left(5y\right)}\right]^{-5}.
$$

The base tends to $e$ and the exponent is $-5$. By **Basic Knowledge: The Important Limit $e$ (Function Version)**, the limit is $e^{-5}=\frac1{e^5}$. $\blacksquare$

---

## 1.6-4-6

Find: $\lim_{x\to\infty}\left(1+\frac1x\right)^{x+100}$.

### Solution 1.6-4-6

$$
\left(1+\frac1x\right)^{x+100}=\left(1+\frac1x\right)^x\cdot\left(1+\frac1x\right)^{100}\to e\cdot1=e.
$$

$\blacksquare$

---

## 1.6-5

Find constants $a$ and $b$ such that

$$
\lim_{x\to+\infty}\left[\frac{x^2+1}{x+1}-\left(ax+b\right)\right]=0.
$$

Explain the geometric meaning.

### Solution 1.6-5

$$
\frac{x^2+1}{x+1}-ax-b=\frac{x^2+1-\left(ax+b\right)\left(x+1\right)}{x+1}=\frac{\left(1-a\right)x^2-\left(a+b\right)x+1-b}{x+1}.
$$

For this to tend to $0$, the numerator must have lower degree than the denominator, so $1-a=0$ and $a+b=0$, giving $a=1$, $b=-1$.

Geometrically, the line $y=x-1$ is the oblique asymptote of the curve $y=\frac{x^2+1}{x+1}$ as $x\to+\infty$. $\blacksquare$

---

## 1.6-7

Prove $\lim_{x\to+\infty}\left(1+\frac1x\right)^{x^2}=+\infty$.

### Solution 1.6-7

$$
\left(1+\frac1x\right)^{x^2}=\left[\left(1+\frac1x\right)^x\right]^x.
$$

For sufficiently large $x$, $\left(1+\frac1x\right)^x> 2$ (since it tends to $e> 2$), so $\left(1+\frac1x\right)^{x^2}> 2^x\to+\infty$. The limit is $+\infty$. $\blacksquare$

---

## 1.6-9

Let $\lim_{x\to+\infty}\frac{f\left(x\right)}x=0$ and $f\left(x\right)> 0$ ($x> 0$). Prove $\lim_{x\to+\infty}\left(1+\frac1x\right)^{f\left(x\right)}=1$.

### Solution 1.6-9

Taking logarithms,

$$
\left(1+\frac1x\right)^{f\left(x\right)}=e^{f\left(x\right)\ln\left(1+1/x\right)}.
$$

Since

$$
0< f\left(x\right)\ln\left(1+\frac1x\right)< f\left(x\right)\cdot\frac1x\to0,
$$

by **Theorem 6.2 (Squeeze Theorem for Functions)**, the exponent tends to $0$. By continuity of $e^t$, the limit is $e^0=1$. $\blacksquare$

---

## 1.6-10

Let $y=D\left(x\right)$ be the Dirichlet function. Prove that for any $a\in\mathbb R$, $\lim_{x\to a}D\left(x\right)$ does not exist.

### Solution 1.6-10

Take a rational sequence $\left\{r_n\right\}$ and an irrational sequence $\left\{s_n\right\}$, both converging to $a$ (by density of rationals and irrationals). Then $D\left(r_n\right)=1\to1$ and $D\left(s_n\right)=0\to0$. The two subsequential limits differ; by the Heine principle, $\lim_{x\to a}D\left(x\right)$ does not exist. $\blacksquare$

---

## 1.6-11

Find: $\lim_{x\to+\infty}\frac{\left(\ln x\right)^5}{x}$.

### Solution 1.6-11

Substitute $y=\ln x$, so $x=e^y$, and as $x\to+\infty$, $y\to+\infty$. The expression becomes $\lim_{y\to+\infty}\frac{y^5}{e^y}=0$ (the exponential grows faster than any power). $\blacksquare$
