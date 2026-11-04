# week7

> **Proposition 1.7 (Triangle Inequality)**
> 
> For any real $a,b,c$, $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **Theorem 5.1 (Arithmetic of Function Limits)**
> 
> If $\lim f\left(x\right)=l_1$ and $\lim g\left(x\right)=l_2$, then $\lim\left(f\pm g\right)=l_1\pm l_2$, $\lim\left(f\cdot g\right)=l_1\cdot l_2$, and when $l_2\ne0$, $\lim\frac{f}{g}=\frac{l_1}{l_2}$.

> **Proposition 6.1 (Important Limit $\lim_{x\to0}\frac{\sin x}{x}=1$)**
> 
> $\lim_{x\to0}\frac{\sin x}{x}=1$.

> **Theorem 6.2 (Squeeze Theorem for Functions)**
> 
> Let $f\left(x\right),g\left(x\right),h\left(x\right)$ be defined in a punctured neighborhood of $a$ with $h\left(x\right)\le f\left(x\right)\le g\left(x\right)$. If $\lim g\left(x\right)=\lim h\left(x\right)=l$, then $\lim f\left(x\right)=l$.

## 1.5-5

Let $\lim_{x\to2}f\left(x\right)=l$. Prove that $f\left(y^2\right)\to l$ as $y\to\sqrt2$.

### Solution to 1.5-5

Given $\varepsilon> 0$, by Definition of Function Limit, there exists $\delta_1> 0$ such that $0< \left|x-2\right|< \delta_1$ implies $\left|f\left(x\right)-l\right|< \varepsilon$. Setting $x=y^2$, we need $0< \left|y^2-2\right|< \delta_1$.

Since $y\to\sqrt2$, restrict to $\left|y-\sqrt2\right|< 1$, so $\left|y+\sqrt2\right|\le2\sqrt2+1$. Take $\delta=\min\left\{1,\frac{\delta_1}{2\sqrt2+1}\right\}$. Then for $0< \left|y-\sqrt2\right|< \delta$,

$$
\left|y^2-2\right|=\left|y-\sqrt2\right|\left|y+\sqrt2\right|< \delta\cdot\left(2\sqrt2+1\right)\le\delta_1,
$$

and $y^2\ne2$ (since $y\to\sqrt2$ with $y\ne\sqrt2$). Hence $\left|f\left(y^2\right)-l\right|< \varepsilon$. By Definition of Function Limit, $f\left(y^2\right)\to l$. $\blacksquare$

## 1.5-6

Discuss the left and right limits at $x=0$ of:

(1) $y=\left[x\right]\cdot\left(1+x\right)$;

(2) $y=\cos x\cdot\operatorname{sgn}x$;

(3) $y=\frac{\left|x\right|}{x}\cdot\frac1{1+x^n}$.

### Solution to 1.5-6

(1) As $x\to0+0$, $\left[x\right]=0$, so $y=0$, right limit $0$. As $x\to0-0$, $\left[x\right]=-1$, so $y=-\left(1+x\right)\to-1$, left limit $-1$.

(2) As $x\to0+0$, $\operatorname{sgn}x=1$, so $y=\cos x\to1$, right limit $1$. As $x\to0-0$, $\operatorname{sgn}x=-1$, so $y=-\cos x\to-1$, left limit $-1$.

(3) As $x\to0+0$, $\frac{\left|x\right|}{x}=1$ and $\frac1{1+x^n}\to1$, right limit $1$. As $x\to0-0$, $\frac{\left|x\right|}{x}=-1$ and $\frac1{1+x^n}\to1$ (since $x^n\to0$), left limit $-1$. $\blacksquare$

## 1.5-7

Find the limits:

(1) $\lim_{x\to-1}\left(\frac1{x+1}-\frac3{x^3+1}\right)$;

(2) $\lim_{x\to0}\frac{\sqrt{a^2+x}-a}{x}$ ($a> 0$).

### Solution to 1.5-7

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

## 1.6-2

Prove by $\varepsilon$-$\delta$ language: if $\lim_{x\to a}f\left(x\right)=l$ and $l> 0$, then there exists $\delta> 0$ such that $f\left(x\right)> \frac l2$ whenever $0< \left|x-a\right|< \delta$.

### Solution to 1.6-2

Take $\varepsilon=\frac l2> 0$. By Definition of Function Limit, there exists $\delta> 0$ such that $0< \left|x-a\right|< \delta$ implies $\left|f\left(x\right)-l\right|< \frac l2$. By **Proposition 1.7 (Triangle Inequality)**,

$$
f\left(x\right)=l-\left(l-f\left(x\right)\right)\ge l-\left|f\left(x\right)-l\right|> l-\frac l2=\frac l2.
$$

Thus $f\left(x\right)> \frac l2$. $\blacksquare$

## 1.6-3

Use $\lim_{x\to0}\frac{\sin x}{x}=1$ to find:

(1) $\lim_{x\to0}\frac{\sin\alpha x}{\sin\beta x}$ ($\beta\ne0$);

(2) $\lim_{x\to0}\frac{\tan3x-\tan5x}{\sin2x}$;

(3) $\lim_{x\to0}\frac{1-\cos x}{x^2}$;

(4) $\lim_{x\to a}\frac{\sin x-\sin a}{x-a}$.

### Solution to 1.6-3

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

## 1.6-4-1

Use $\lim_{x\to\infty}\left(1+\frac1x\right)^x=e$ to find: $\lim_{x\to\infty}\left(1+\frac3x\right)^x\cdot\left(1+\frac5x\right)^x$.

### Solution to 1.6-4-1

$$
\left(1+\frac3x\right)^x=\left[\left(1+\frac3x\right)^{x/3}\right]^3\to e^3,\quad\left(1+\frac5x\right)^x=\left[\left(1+\frac5x\right)^{x/5}\right]^5\to e^5.
$$

By **Theorem 5.1 (Arithmetic of Function Limits)**, the product is $e^3\cdot e^5=e^8$. $\blacksquare$
