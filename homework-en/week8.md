# week8

> **Proposition 1.7 (Triangle Inequality)**
> 
> For any real $a,b,c$, $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **Theorem 5.1 (Arithmetic of Function Limits)**
> 
> If $\lim{f}\left(x\right)=l_1$ and $\lim{g}\left(x\right)=l_2$, then $\lim\left(f\pm{g}\right)=l_1\pm{l}_2$, $\lim\left(f\cdot{g}\right)=l_1\cdot{l}_2$, and when $l_2\ne0$, $\lim\frac{f}{g}=\frac{l_1}{l_2}$.

> **Proposition 6.1 (Important Limit $\lim_{x\to0}\frac{\sin{x}}{x}=1$)**
> 
> $\lim_{x\to0}\frac{\sin{x}}{x}=1$.

> **Theorem 6.2 (Squeeze Theorem for Functions)**
> 
> Let $f\left(x\right),g\left(x\right),h\left(x\right)$ be defined in a punctured neighborhood of $a$ with $h\left(x\right)\le{f}\left(x\right)\le{g}\left(x\right)$. If $\lim{g}\left(x\right)=\lim{h}\left(x\right)=l$, then $\lim{f}\left(x\right)=l$.

> **Theorem 7.2 (Continuity of Composite Functions)**
> 
> If $y=g\left(u\right)$ is continuous at $u_0$ and $u=f\left(x\right)$ is continuous at $x_0$ with $f\left(x_0\right)=u_0$, then $y=g\left(f\left(x\right)\right)$ is continuous at $x_0$.

## 1.6-4-3

Find: $\lim_{x\to0}\left(\frac{1+x}{1-x}\right)^{1/x}$.

### Solution to 1.6-4-3

$$
\left(\frac{1+x}{1-x}\right)^{1/x}=\left[\left(1+\frac{2x}{1-x}\right)^{\frac{1-x}{2x}}\right]^{\frac2{1-x}}.
$$

The base tends to $e$ and the exponent $\frac2{1-x}\to2$. By The Important Limit $e$ (Function Version) and **Theorem 6.2 (Squeeze Theorem for Functions)**, the limit is $e^2$. $\blacksquare$

## 1.6-4-5

Find: $\lim_{y\to0}\left(1-5y\right)^{1/y}$.

### Solution to 1.6-4-5

$$
\left(1-5y\right)^{1/y}=\left[\left(1+\frac1{-1/\left(5y\right)}\right)^{-1/\left(5y\right)}\right]^{-5}.
$$

The base tends to $e$ and the exponent is $-5$. By The Important Limit $e$ (Function Version), the limit is $e^{-5}=\frac1{e^5}$. $\blacksquare$

## 1.6-4-6

Find: $\lim_{x\to\infty}\left(1+\frac1x\right)^{x+100}$.

### Solution to 1.6-4-6

$$
\left(1+\frac1x\right)^{x+100}=\left(1+\frac1x\right)^x\cdot\left(1+\frac1x\right)^{100}\to{e}\cdot1=e.
$$

$\blacksquare$

## 1.6-5

Find constants $a$ and $b$ such that

$$
\lim_{x\to+\infty}\left[\frac{x^2+1}{x+1}-\left(ax+b\right)\right]=0.
$$

Explain the geometric meaning.

### Solution to 1.6-5

$$
\frac{x^2+1}{x+1}-ax-b=\frac{x^2+1-\left(ax+b\right)\left(x+1\right)}{x+1}=\frac{\left(1-a\right)x^2-\left(a+b\right)x+1-b}{x+1}.
$$

For this to tend to $0$, the numerator must have lower degree than the denominator, so $1-a=0$ and $a+b=0$, giving $a=1$, $b=-1$.

Geometrically, the line $y=x-1$ is the oblique asymptote of the curve $y=\frac{x^2+1}{x+1}$ as $x\to+\infty$. $\blacksquare$

## 1.6-7

Prove $\lim_{x\to+\infty}\left(1+\frac1x\right)^{x^2}=+\infty$.

### Solution to 1.6-7

$$
\left(1+\frac1x\right)^{x^2}=\left[\left(1+\frac1x\right)^x\right]^x.
$$

For sufficiently large $x$, $\left(1+\frac1x\right)^x>2$ (since it tends to $e>2$), so $\left(1+\frac1x\right)^{x^2}>2^x\to+\infty$. The limit is $+\infty$. $\blacksquare$

## 1.6-9

Let $\lim_{x\to+\infty}\frac{f\left(x\right)}x=0$ and $f\left(x\right)>0$ ($x>0$). Prove $\lim_{x\to+\infty}\left(1+\frac1x\right)^{f\left(x\right)}=1$.

### Solution to 1.6-9

Taking logarithms,

$$
\left(1+\frac1x\right)^{f\left(x\right)}=e^{f\left(x\right)\ln\left(1+1/x\right)}.
$$

Since

$$
0<{}f\left(x\right)\ln\left(1+\frac1x\right)<{}f\left(x\right)\cdot\frac1x\to0,
$$

by **Theorem 6.2 (Squeeze Theorem for Functions)**, the exponent tends to $0$. By continuity of $e^t$, the limit is $e^0=1$. $\blacksquare$

## 1.6-10

Let $y=D\left(x\right)$ be the Dirichlet function. Prove that for any $a\in\mathbb{R}$, $\lim_{x\to{a}}D\left(x\right)$ does not exist.

### Solution to 1.6-10

Take a rational sequence $\left\{r_n\right\}$ and an irrational sequence $\left\{s_n\right\}$, both converging to $a$ (by density of rationals and irrationals). Then $D\left(r_n\right)=1\to1$ and $D\left(s_n\right)=0\to0$. The two subsequential limits differ; by the Heine principle, $\lim_{x\to{a}}D\left(x\right)$ does not exist. $\blacksquare$

## 1.6-11

Find: $\lim_{x\to+\infty}\frac{\left(\ln{x}\right)^5}{x}$.

### Solution to 1.6-11

Substitute $y=\ln{x}$, so $x=e^y$, and as $x\to+\infty$, $y\to+\infty$. The expression becomes $\lim_{y\to+\infty}\frac{y^5}{e^y}=0$ (the exponential grows faster than any power). $\blacksquare$

## 1.7-1

Find the discontinuities and their types:

(1) $y=\operatorname{sgn}\left(\sin{x}\right)$;

(2)

$$
y=f\left(x\right)=\begin{cases}x^2e^x,&x>0,\\sin\frac{\pi}{1+x^2},&x<0,\\1,&x=0;\end{cases}
$$

(3) $y=\cos\left\{\left(x-\left[x\right]\right)\pi\right\}$;

(4)

$$
y=f\left(x\right)=\begin{cases}e^{\sin\frac1x},&x\ne0,\\0,&x=0.\end{cases}
$$

### Solution to 1.7-1

(1) At $x=k\pi$ ($k\in\mathbb{Z}$), $\sin{x}=0$, and the left/right limits of $\operatorname{sgn}\left(\sin{x}\right)$ are $1$ and $-1$ (or vice versa), so these are first-kind (jump) discontinuities. All other points are continuous.

(2) As $x\to0+0$, $f\left(x\right)=x^2e^x\to0$; as $x\to0-0$,

$$
f\left(x\right)=\sin\frac{\pi}{1+x^2}\to\sin\pi=0.
$$

But $f\left(0\right)=1$, so $x=0$ is a removable discontinuity (first kind).

(3) $x-\left[x\right]=\left\{x\right\}$ is the fractional part; at integers the left/right limits are $\cos0=1$ and $\cos\pi=-1$, so integers are jump discontinuities (first kind). Other points are continuous.

(4) As $x\to0$, $\frac1x$ oscillates, $\sin\frac1x$ oscillates in $\left[-1,1\right]$, and $e^{\sin\left(1/x\right)}$ oscillates between $e^{-1}$ and $e$; the limit does not exist, so $x=0$ is a second-kind (oscillating) discontinuity. $\blacksquare$

## 1.7-2-2

Prove by $\varepsilon$-$\delta$ language: if $y=f\left(x\right)$ is continuous at $a$, then $y=\left|f\left(x\right)\right|$ is continuous at $a$.

### Solution to 1.7-2-2

By Definition of Continuous Function, given $\varepsilon>0$, there exists $\delta>0$ such that $\left|x-a\right|<\delta$ implies $\left|f\left(x\right)-f\left(a\right)\right|<\varepsilon$. By **Proposition 1.7 (Triangle Inequality)**,

$$
\left|\left|f\left(x\right)\right|-\left|f\left(a\right)\right|\right|\le\left|f\left(x\right)-f\left(a\right)\right|<\varepsilon.
$$

Thus $\left|f\left(x\right)\right|$ is continuous at $a$. $\blacksquare$

## 1.7-3

Use continuity of elementary functions to find:

(1) $\lim_{x\to0}\cos\left(\sqrt{1+x^2}-1\right)$;

(2) $\lim_{x\to0}e^{\frac{\sin{x}}{\sin2x}}$;

(3) $\lim_{x\to\infty}\arctan\frac{\sqrt{x^4+2}}{1+x^2}$;

(4) $\lim_{x\to5}x^{\sqrt{x}}$;

(5) $\lim_{x\to\infty}\left(1+\frac1x+\frac1{x^2}\right)^{x+\sqrt{x}}$.

### Solution to 1.7-3

(1) By **Theorem 7.2 (Continuity of Composite Functions)**, $\lim_{x\to0}\left(\sqrt{1+x^2}-1\right)=0$, so the expression $=\cos0=1$.

(2) $\frac{\sin{x}}{\sin2x}\to\frac12$; by continuity of $e^u$, the expression $=e^{1/2}=\sqrt{e}$.

(3) $\frac{\sqrt{x^4+2}}{1+x^2}\to1$; by continuity of $\arctan{u}$, the expression $=\arctan1=\frac\pi4$.

(4) $x^{\sqrt{x}}=e^{\sqrt{x}\ln{x}}$; $\sqrt{x}\ln{x}\to\sqrt5\ln5$; by continuity, the expression $=e^{\sqrt5\ln5}=5^{\sqrt5}$.

(5)

$$
\left(1+\frac1x+\frac1{x^2}\right)^{x+\sqrt{x}}=\left[\left(1+\frac{x+1}{x^2}\right)^{\frac{x^2}{x+1}}\right]^{\frac{\left(x+\sqrt{x}\right)\left(x+1\right)}{x^2}}.
$$

The base tends to $e$ and the exponent to $1$, so the expression $=e$. $\blacksquare$
