# Assignment 5

> **Definition** (Limit of a Function) Let $y=f\left(x\right)$ be defined in a deleted neighborhood $\left(a-r,a+r\right)\backslash\left\{a\right\}$ of the point $a$. If there exists a real number $l$ such that, for any given $\varepsilon> 0$, no matter how small, there is a $\delta> 0$ such that $\left|f\left(x\right)-l\right|< \varepsilon$ whenever $0< \left|x-a\right|< \delta$, then $f\left(x\right)$ is said to have limit $l$ as $x\to a$, denoted $\lim\limits_{x\to a}f\left(x\right)=l$.

> **Definition** (One-Sided Limit) If $f\left(x\right)$ has limit $l$ as $x\to a+0$ (or $x\to a-0$), it is called the right-hand limit (or left-hand limit), denoted $\lim\limits_{x\to a+0}f\left(x\right)=l$ (or $\lim\limits_{x\to a-0}f\left(x\right)=l$).

> **Theorem 5.1** (Arithmetic of Function Limits) If $\lim f\left(x\right)=l_1$ and $\lim g\left(x\right)=l_2$, then $\lim\left(f\pm g\right)=l_1\pm l_2$, $\lim\left(f\cdot g\right)=l_1\cdot l_2$, and when $l_2\ne0$, $\lim\frac{f}{g}=\frac{l_1}{l_2}$.

> **Proposition** (Sign-Preserving Property) If $\lim\limits_{x\to a}f\left(x\right)=l$ and $l\ne0$, then there exists $\delta> 0$ such that $\left|f\left(x\right)\right|> \frac{\left|l\right|}{2}$ whenever $0< \left|x-a\right|< \delta$.

### Problem 1

(Problem 1.5-1-2) Using the $\varepsilon$-$\delta$ language, prove that $\lim\limits_{x\to a}\cos x=\cos a$.

### Solution to Problem 1

By the sum-to-product formula,

$$
\left|\cos x-\cos a\right|=2\left|\sin\frac{x+a}2\right|\left|\sin\frac{x-a}2\right|\le2\cdot1\cdot\frac{\left|x-a\right|}2=\left|x-a\right|,
$$

where we used $\left|\sin t\right|\le\left|t\right|$ for all $t$.

Given any $\varepsilon> 0$, take $\delta=\varepsilon$. Then when $0< \left|x-a\right|< \delta$,

$$
\left|\cos x-\cos a\right|\le\left|x-a\right|< \varepsilon.
$$

By **Definition** (Limit of a Function), $\lim\limits_{x\to a}\cos x=\cos a$. $\blacksquare$

### Problem 2

(Problem 1.5-1-3) Using the $\varepsilon$-$\delta$ language, prove that $\lim\limits_{x\to+\infty}\frac{6x+5}{x+1}=6$.

### Solution to Problem 2

$$
\left|\frac{6x+5}{x+1}-6\right|=\left|\frac{6x+5-6\left(x+1\right)}{x+1}\right|=\frac1{x+1}.
$$

Given any $\varepsilon> 0$, take $X=\frac1\varepsilon-1$. Then when $x> X$,

$$
\left|\frac{6x+5}{x+1}-6\right|=\frac1{x+1}< \varepsilon.
$$

By the $x\to+\infty$ version of **Definition** (Limit of a Function), $\lim\limits_{x\to+\infty}\frac{6x+5}{x+1}=6$. $\blacksquare$

### Problem 3

(Problem 1.5-1-5) Using the $\varepsilon$-$\delta$ language, prove that $\lim\limits_{x\to2-0}\sqrt{4-x^2}=0$.

### Solution to Problem 3

$\left|\sqrt{4-x^2}-0\right|=\sqrt{4-x^2}$. For $\sqrt{4-x^2}< \varepsilon$, we only need $4-x^2< \varepsilon^2$, i.e. $x^2> 4-\varepsilon^2$. Since $x< 2$ when $x\to2-0$, we only need $x> \sqrt{4-\varepsilon^2}$. Take $\delta=2-\sqrt{4-\varepsilon^2}$. Then when $2-\delta< x< 2$,

$$
0< 2-x< \delta\Rightarrow x> \sqrt{4-\varepsilon^2}\Rightarrow\sqrt{4-x^2}< \varepsilon.
$$

By **Definition** (One-Sided Limit), $\lim\limits_{x\to2-0}\sqrt{4-x^2}=0$. $\blacksquare$

### Problem 4

(Problem 1.5-1-7) Let $a> 0$. Prove that $\lim\limits_{x\to0}a^x=1$.

### Solution to Problem 4

Without loss of generality assume $a> 1$ (the case $0< a< 1$ is analogous). For $\left|a^x-1\right|< \varepsilon$, i.e. $1-\varepsilon< a^x< 1+\varepsilon$. Assume $0< \varepsilon< 1$. Then the left side $a^x> 1-\varepsilon> 0$, and taking logarithms gives $x> \log_a\left(1-\varepsilon\right)$; the right side $a^x< 1+\varepsilon$ gives $x< \log_a\left(1+\varepsilon\right)$.

Take

$$
\delta=\min\left\{-\log_a\left(1-\varepsilon\right),\log_a\left(1+\varepsilon\right)\right\}> 0,
$$

then when $0< \left|x\right|< \delta$, $\left|a^x-1\right|< \varepsilon$. By **Definition** (Limit of a Function), $\lim\limits_{x\to0}a^x=1$. $\blacksquare$

### Problem 5

(Problem 1.5-4) Let $\lim\limits_{x\to a}f\left(x\right)=l$ and $l\ne0$. Prove that the function $y=\frac1{f\left(x\right)}$ is a bounded variable as $x\to a$.

### Solution to Problem 5

Take $\varepsilon=\frac{\left|l\right|}{2}$. By **Definition** (Limit of a Function), there exists $\delta> 0$ such that $\left|f\left(x\right)-l\right|< \frac{\left|l\right|}{2}$ when $0< \left|x-a\right|< \delta$. By **Proposition 1.7** (Triangle Inequality) in Chapter 1,

$$
\left|f\left(x\right)\right|=\left|l-\left(l-f\left(x\right)\right)\right|\ge\left|l\right|-\left|l-f\left(x\right)\right|> \left|l\right|-\frac{\left|l\right|}{2}=\frac{\left|l\right|}{2}.
$$

Hence $\left|\frac1{f\left(x\right)}\right|< \frac2{\left|l\right|}$, i.e. $\frac1{f\left(x\right)}$ is bounded as $x\to a$. This is a corollary of **Proposition** (Sign-Preserving Property). $\blacksquare$

### Problem 6

(Problem 1.5-5) Let $\lim\limits_{x\to2}f\left(x\right)=l$. Prove that as $y\to\sqrt2$, $f\left(y^2\right)\to l$.

### Solution to Problem 6

Given any $\varepsilon> 0$, by **Definition** (Limit of a Function), there exists $\delta_1> 0$ such that $\left|f\left(x\right)-l\right|< \varepsilon$ when $0< \left|x-2\right|< \delta_1$. Set $x=y^2$. Then we need $0< \left|y^2-2\right|< \delta_1$.

Since $y\to\sqrt2$, we may restrict $\left|y-\sqrt2\right|< 1$, in which case $\left|y+\sqrt2\right|\le2\sqrt2+1$. Take $\delta=\min\left\{1,\frac{\delta_1}{2\sqrt2+1}\right\}$. Then when $0< \left|y-\sqrt2\right|< \delta$,

$$
\left|y^2-2\right|=\left|y-\sqrt2\right|\left|y+\sqrt2\right|< \delta\cdot\left(2\sqrt2+1\right)\le\delta_1,
$$

and $y^2\ne2$ (otherwise $y=\pm\sqrt2$, while as $y\to\sqrt2$ with $y\ne\sqrt2$, we have $y^2\ne2$). Hence $\left|f\left(y^2\right)-l\right|< \varepsilon$. By **Definition** (Limit of a Function), $f\left(y^2\right)\to l$. $\blacksquare$

### Problem 7

(Problem 1.5-6) Discuss the left and right limits of the following functions at the point $x=0$:
(1) $y=\left[x\right]\cdot\left(1+x\right)$;

(2) $y=\cos x\cdot\operatorname{sgn}x$;

(3) $y=\frac{\left|x\right|}{x}\cdot\frac1{1+x^n}$.

### Solution to Problem 7

(1) When $x\to0+0$, $\left[x\right]=0$, so $y=0$, and the right-hand limit is $0$. When $x\to0-0$, $\left[x\right]=-1$, so $y=-\left(1+x\right)\to-1$, and the left-hand limit is $-1$.

(2) When $x\to0+0$, $\operatorname{sgn}x=1$, so $y=\cos x\to1$, and the right-hand limit is $1$. When $x\to0-0$, $\operatorname{sgn}x=-1$, so $y=-\cos x\to-1$, and the left-hand limit is $-1$.

(3) When $x\to0+0$, $\frac{\left|x\right|}{x}=1$ and $\frac1{1+x^n}\to1$, so the right-hand limit is $1$. When $x\to0-0$, $\frac{\left|x\right|}{x}=-1$ and $\frac1{1+x^n}\to1$ (since $x^n\to0$), so the left-hand limit is $-1$. $\blacksquare$

### Problem 8

(Problem 1.5-7) Find the limits:
(1) $\lim\limits_{x\to-1}\left(\frac1{x+1}-\frac3{x^3+1}\right)$;

(2) $\lim\limits_{x\to0}\frac{\sqrt{a^2+x}-a}{x}\left(a> 0\right)$.

### Solution to Problem 8

(1) By factorization

$$
x^3+1=\left(x+1\right)\left(x^2-x+1\right),
$$

$$
\frac1{x+1}-\frac3{x^3+1}=\frac{x^2-x+1-3}{\left(x+1\right)\left(x^2-x+1\right)}=\frac{x^2-x-2}{\left(x+1\right)\left(x^2-x+1\right)}=\frac{\left(x-2\right)\left(x+1\right)}{\left(x+1\right)\left(x^2-x+1\right)}=\frac{x-2}{x^2-x+1}.
$$

By **Theorem 5.1** (Arithmetic of Function Limits),

$$
\lim_{x\to-1}\frac{x-2}{x^2-x+1}=\frac{-1-2}{1+1+1}=-1.
$$

(2) Rationalize the numerator:

$$
\frac{\sqrt{a^2+x}-a}{x}=\frac{\left(\sqrt{a^2+x}-a\right)\left(\sqrt{a^2+x}+a\right)}{x\left(\sqrt{a^2+x}+a\right)}=\frac{x}{x\left(\sqrt{a^2+x}+a\right)}=\frac1{\sqrt{a^2+x}+a}.
$$

By **Theorem 5.1** (Arithmetic of Function Limits) and $\lim\limits_{x\to0}\sqrt{a^2+x}=a$,

$$
\lim_{x\to0}\frac{\sqrt{a^2+x}-a}{x}=\frac1{2a}.

$$

$\blacksquare$