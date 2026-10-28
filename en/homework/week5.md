# week5

> **Basic Knowledge: Definition of Function Limit**<br>Let $y=f\left(x\right)$ be defined in a punctured neighborhood $\left(a-r,a+r\right)\backslash\left\{a\right\}$ of $a$. If there exists $l\in\mathbb R$ such that for every $\varepsilon> 0$ there exists $\delta> 0$ such that $0< \left|x-a\right|< \delta$ implies $\left|f\left(x\right)-l\right|< \varepsilon$, then $f\left(x\right)$ is said to have limit $l$ as $x\to a$, denoted $\lim_{x\to a}f\left(x\right)=l$.

> **Basic Knowledge: Definition of One-Sided Limits**<br>If $f\left(x\right)$ has limit $l$ as $x\to a+0$ (resp. $x\to a-0$), it is called the right (resp. left) limit, denoted $\lim_{x\to a+0}f\left(x\right)=l$ (resp. $\lim_{x\to a-0}f\left(x\right)=l$).

> **Basic Knowledge: Sign Preservation of Limits**<br>If $\lim_{x\to a}f\left(x\right)=l$ and $l\ne0$, then there exists $\delta> 0$ such that $0< \left|x-a\right|< \delta$ implies $\left|f\left(x\right)\right|> \frac{\left|l\right|}{2}$.

> **Proposition 1.7 (Triangle Inequality)**<br>For any real $a,b,c$: (1) $\left|a-b\right|\ge0$, equality iff $a=b$; (2) $\left|a-b\right|=\left|b-a\right|$; (3) $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **Theorem 5.1 (Arithmetic of Function Limits)**<br>If $\lim f\left(x\right)=l_1$ and $\lim g\left(x\right)=l_2$, then $\lim\left(f\pm g\right)=l_1\pm l_2$, $\lim\left(f\cdot g\right)=l_1\cdot l_2$, and when $l_2\ne0$, $\lim\frac{f}{g}=\frac{l_1}{l_2}$.

---

## 1.5-1-2

Prove by $\varepsilon$-$\delta$ language: $\lim_{x\to a}\cos x=\cos a$.

### Solution 1.5-1-2

Using sum-to-product identities,

$$
\left|\cos x-\cos a\right|=2\left|\sin\frac{x+a}2\right|\left|\sin\frac{x-a}2\right|\le2\cdot1\cdot\frac{\left|x-a\right|}2=\left|x-a\right|,
$$

using $\left|\sin t\right|\le\left|t\right|$ for all $t$.

Given $\varepsilon> 0$, take $\delta=\varepsilon$. Then for $0< \left|x-a\right|< \delta$,

$$
\left|\cos x-\cos a\right|\le\left|x-a\right|< \varepsilon.
$$

By **Basic Knowledge: Definition of Function Limit**, $\lim_{x\to a}\cos x=\cos a$. $\blacksquare$

---

## 1.5-1-3

Prove by $\varepsilon$-$\delta$ language: $\lim_{x\to+\infty}\frac{6x+5}{x+1}=6$.

### Solution 1.5-1-3

$$
\left|\frac{6x+5}{x+1}-6\right|=\left|\frac{6x+5-6\left(x+1\right)}{x+1}\right|=\frac1{x+1}.
$$

Given $\varepsilon> 0$, take $X=\frac1\varepsilon-1$. Then for $x> X$,

$$
\left|\frac{6x+5}{x+1}-6\right|=\frac1{x+1}< \varepsilon.
$$

By the $x\to+\infty$ version of **Basic Knowledge: Definition of Function Limit**, $\lim_{x\to+\infty}\frac{6x+5}{x+1}=6$. $\blacksquare$

---

## 1.5-1-5

Prove by $\varepsilon$-$\delta$ language: $\lim_{x\to2-0}\sqrt{4-x^2}=0$.

### Solution 1.5-1-5

$\left|\sqrt{4-x^2}-0\right|=\sqrt{4-x^2}$. To make $\sqrt{4-x^2}< \varepsilon$, it suffices that $4-x^2< \varepsilon^2$, i.e. $x^2> 4-\varepsilon^2$. Since $x\to2-0$ means $x< 2$, it suffices that $x> \sqrt{4-\varepsilon^2}$. Take $\delta=2-\sqrt{4-\varepsilon^2}$. Then for $2-\delta< x< 2$,

$$
0< 2-x< \delta\Rightarrow x> \sqrt{4-\varepsilon^2}\Rightarrow\sqrt{4-x^2}< \varepsilon.
$$

By **Basic Knowledge: Definition of One-Sided Limits**, $\lim_{x\to2-0}\sqrt{4-x^2}=0$. $\blacksquare$

---

## 1.5-1-7

Let $a> 0$. Prove $\lim_{x\to0}a^x=1$.

### Solution 1.5-1-7

Assume $a> 1$ (the case $0< a< 1$ is analogous). To make $\left|a^x-1\right|< \varepsilon$, i.e. $1-\varepsilon< a^x< 1+\varepsilon$. For $0< \varepsilon< 1$, the left inequality $a^x> 1-\varepsilon> 0$ gives $x> \log_a\left(1-\varepsilon\right)$; the right inequality $a^x< 1+\varepsilon$ gives $x< \log_a\left(1+\varepsilon\right)$.

Take

$$
\delta=\min\left\{-\log_a\left(1-\varepsilon\right),\log_a\left(1+\varepsilon\right)\right\}> 0,
$$

then for $0< \left|x\right|< \delta$, $\left|a^x-1\right|< \varepsilon$. By **Basic Knowledge: Definition of Function Limit**, $\lim_{x\to0}a^x=1$. $\blacksquare$

---

## 1.5-4

Let $\lim_{x\to a}f\left(x\right)=l$ and $l\ne0$. Prove that $y=\frac1{f\left(x\right)}$ is bounded as $x\to a$.

### Solution 1.5-4

Take $\varepsilon=\frac{\left|l\right|}{2}$. By **Basic Knowledge: Definition of Function Limit**, there exists $\delta> 0$ such that $0< \left|x-a\right|< \delta$ implies $\left|f\left(x\right)-l\right|< \frac{\left|l\right|}{2}$. By **Proposition 1.7 (Triangle Inequality)**,

$$
\left|f\left(x\right)\right|=\left|l-\left(l-f\left(x\right)\right)\right|\ge\left|l\right|-\left|l-f\left(x\right)\right|> \left|l\right|-\frac{\left|l\right|}{2}=\frac{\left|l\right|}{2}.
$$

Hence $\left|\frac1{f\left(x\right)}\right|< \frac2{\left|l\right|}$, i.e. $\frac1{f\left(x\right)}$ is bounded as $x\to a$. This is a corollary of **Basic Knowledge: Sign Preservation of Limits**. $\blacksquare$

---

## 1.5-5

Let $\lim_{x\to2}f\left(x\right)=l$. Prove that $f\left(y^2\right)\to l$ as $y\to\sqrt2$.

### Solution 1.5-5

Given $\varepsilon> 0$, by **Basic Knowledge: Definition of Function Limit**, there exists $\delta_1> 0$ such that $0< \left|x-2\right|< \delta_1$ implies $\left|f\left(x\right)-l\right|< \varepsilon$. Setting $x=y^2$, we need $0< \left|y^2-2\right|< \delta_1$.

Since $y\to\sqrt2$, restrict to $\left|y-\sqrt2\right|< 1$, so $\left|y+\sqrt2\right|\le2\sqrt2+1$. Take $\delta=\min\left\{1,\frac{\delta_1}{2\sqrt2+1}\right\}$. Then for $0< \left|y-\sqrt2\right|< \delta$,

$$
\left|y^2-2\right|=\left|y-\sqrt2\right|\left|y+\sqrt2\right|< \delta\cdot\left(2\sqrt2+1\right)\le\delta_1,
$$

and $y^2\ne2$ (since $y\to\sqrt2$ with $y\ne\sqrt2$). Hence $\left|f\left(y^2\right)-l\right|< \varepsilon$. By **Basic Knowledge: Definition of Function Limit**, $f\left(y^2\right)\to l$. $\blacksquare$

---

## 1.5-6

Discuss the left and right limits at $x=0$ of:

(1) $y=\left[x\right]\cdot\left(1+x\right)$;

(2) $y=\cos x\cdot\operatorname{sgn}x$;

(3) $y=\frac{\left|x\right|}{x}\cdot\frac1{1+x^n}$.

### Solution 1.5-6

(1) As $x\to0+0$, $\left[x\right]=0$, so $y=0$, right limit $0$. As $x\to0-0$, $\left[x\right]=-1$, so $y=-\left(1+x\right)\to-1$, left limit $-1$.

(2) As $x\to0+0$, $\operatorname{sgn}x=1$, so $y=\cos x\to1$, right limit $1$. As $x\to0-0$, $\operatorname{sgn}x=-1$, so $y=-\cos x\to-1$, left limit $-1$.

(3) As $x\to0+0$, $\frac{\left|x\right|}{x}=1$ and $\frac1{1+x^n}\to1$, right limit $1$. As $x\to0-0$, $\frac{\left|x\right|}{x}=-1$ and $\frac1{1+x^n}\to1$ (since $x^n\to0$), left limit $-1$. $\blacksquare$

---

## 1.5-7

Find the limits:

(1) $\lim_{x\to-1}\left(\frac1{x+1}-\frac3{x^3+1}\right)$;

(2) $\lim_{x\to0}\frac{\sqrt{a^2+x}-a}{x}$ ($a> 0$).

### Solution 1.5-7

(1) By factorization $x^3+1=\left(x+1\right)\left(x^2-x+1\right)$,

$$
\frac1{x+1}-\frac3{x^3+1}=\frac{x^2-x+1-3}{\left(x+1\right)\left(x^2-x+1\right)}=\frac{x^2-x-2}{\left(x+1\right)\left(x^2-x+1\right)}=\frac{\left(x-2\right)\left(x+1\right)}{\left(x+1\right)\left(x^2-x+1\right)}=\frac{x-2}{x^2-x+1}.
$$

By **Theorem 5.1 (Arithmetic of Function Limits)**,

$$
\lim_{x\to-1}\frac{x-2}{x^2-x+1}=\frac{-1-2}{1+1+1}=-1.
$$

(2) Rationalizing the numerator,

$$
\frac{\sqrt{a^2+x}-a}{x}=\frac{\left(\sqrt{a^2+x}-a\right)\left(\sqrt{a^2+x}+a\right)}{x\left(\sqrt{a^2+x}+a\right)}=\frac{x}{x\left(\sqrt{a^2+x}+a\right)}=\frac1{\sqrt{a^2+x}+a}.
$$

By **Theorem 5.1 (Arithmetic of Function Limits)** and $\lim_{x\to0}\sqrt{a^2+x}=a$,

$$
\lim_{x\to0}\frac{\sqrt{a^2+x}-a}{x}=\frac1{2a}.
$$

$\blacksquare$
