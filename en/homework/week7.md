# week7

> **Basic Knowledge: Definition of Continuous Function**<br>Let $y=f\left(x\right)$ be defined on $\left(a,b\right)$. If $\lim_{x\to x_0}f\left(x\right)=f\left(x_0\right)$ at some $x_0\in\left(a,b\right)$, then $f$ is continuous at $x_0$. If continuous at every point, it is continuous on $\left(a,b\right)$.

> **Basic Knowledge: Continuity of Elementary Functions**<br>Elementary functions are continuous on their domains.

> **Proposition 1.7 (Triangle Inequality)**<br>For any real $a,b,c$, $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **Theorem 7.2 (Continuity of Composite Functions)**<br>If $y=g\left(u\right)$ is continuous at $u_0$ and $u=f\left(x\right)$ is continuous at $x_0$ with $f\left(x_0\right)=u_0$, then $y=g\left(f\left(x\right)\right)$ is continuous at $x_0$.

---

## 1.7-1

Find the discontinuities and their types:

(1) $y=\operatorname{sgn}\left(\sin x\right)$;

(2)

$$
y=f\left(x\right)=\begin{cases}x^2e^x,&x> 0,\\sin\frac{\pi}{1+x^2},&x< 0,\\1,&x=0;\end{cases}
$$

(3) $y=\cos\left\{\left(x-\left[x\right]\right)\pi\right\}$;

(4)

$$
y=f\left(x\right)=\begin{cases}e^{\sin\frac1x},&x\ne0,\\0,&x=0.\end{cases}
$$

### Solution 1.7-1

(1) At $x=k\pi$ ($k\in\mathbb Z$), $\sin x=0$, and the left/right limits of $\operatorname{sgn}\left(\sin x\right)$ are $1$ and $-1$ (or vice versa), so these are first-kind (jump) discontinuities. All other points are continuous.

(2) As $x\to0+0$, $f\left(x\right)=x^2e^x\to0$; as $x\to0-0$,

$$
f\left(x\right)=\sin\frac{\pi}{1+x^2}\to\sin\pi=0.
$$

But $f\left(0\right)=1$, so $x=0$ is a removable discontinuity (first kind).

(3) $x-\left[x\right]=\left\{x\right\}$ is the fractional part; at integers the left/right limits are $\cos0=1$ and $\cos\pi=-1$, so integers are jump discontinuities (first kind). Other points are continuous.

(4) As $x\to0$, $\frac1x$ oscillates, $\sin\frac1x$ oscillates in $\left[-1,1\right]$, and $e^{\sin\left(1/x\right)}$ oscillates between $e^{-1}$ and $e$; the limit does not exist, so $x=0$ is a second-kind (oscillating) discontinuity. $\blacksquare$

---

## 1.7-2-2

Prove by $\varepsilon$-$\delta$ language: if $y=f\left(x\right)$ is continuous at $a$, then $y=\left|f\left(x\right)\right|$ is continuous at $a$.

### Solution 1.7-2-2

By **Basic Knowledge: Definition of Continuous Function**, given $\varepsilon> 0$, there exists $\delta> 0$ such that $\left|x-a\right|< \delta$ implies $\left|f\left(x\right)-f\left(a\right)\right|< \varepsilon$. By **Proposition 1.7 (Triangle Inequality)**,

$$
\left|\left|f\left(x\right)\right|-\left|f\left(a\right)\right|\right|\le\left|f\left(x\right)-f\left(a\right)\right|< \varepsilon.
$$

Thus $\left|f\left(x\right)\right|$ is continuous at $a$. $\blacksquare$

---

## 1.7-3

Use continuity of elementary functions to find:

(1) $\lim_{x\to0}\cos\left(\sqrt{1+x^2}-1\right)$;

(2) $\lim_{x\to0}e^{\frac{\sin x}{\sin2x}}$;

(3) $\lim_{x\to\infty}\arctan\frac{\sqrt{x^4+2}}{1+x^2}$;

(4) $\lim_{x\to5}x^{\sqrt x}$;

(5) $\lim_{x\to\infty}\left(1+\frac1x+\frac1{x^2}\right)^{x+\sqrt x}$.

### Solution 1.7-3

(1) By **Theorem 7.2 (Continuity of Composite Functions)**, $\lim_{x\to0}\left(\sqrt{1+x^2}-1\right)=0$, so the expression $=\cos0=1$.

(2) $\frac{\sin x}{\sin2x}\to\frac12$; by continuity of $e^u$, the expression $=e^{1/2}=\sqrt e$.

(3) $\frac{\sqrt{x^4+2}}{1+x^2}\to1$; by continuity of $\arctan u$, the expression $=\arctan1=\frac\pi4$.

(4) $x^{\sqrt x}=e^{\sqrt x\ln x}$; $\sqrt x\ln x\to\sqrt5\ln5$; by continuity, the expression $=e^{\sqrt5\ln5}=5^{\sqrt5}$.

(5)

$$
\left(1+\frac1x+\frac1{x^2}\right)^{x+\sqrt x}=\left[\left(1+\frac{x+1}{x^2}\right)^{\frac{x^2}{x+1}}\right]^{\frac{\left(x+\sqrt x\right)\left(x+1\right)}{x^2}}.
$$

The base tends to $e$ and the exponent to $1$, so the expression $=e$. $\blacksquare$

---

## 1.7-4

Let $y=f\left(x\right)$ be continuous on $\left(a,b\right)$, and $x=g\left(t\right)$ have a limit as $t\to\infty$ lying in $\left(a,b\right)$. Prove

$$
\lim_{t\to\infty}f\left(g\left(t\right)\right)=f\left(\lim_{t\to\infty}g\left(t\right)\right).
$$

### Solution 1.7-4

Let $\lim_{t\to\infty}g\left(t\right)=c\in\left(a,b\right)$. By **Basic Knowledge: Definition of Continuous Function**, given $\varepsilon> 0$, there exists $\delta> 0$ such that $\left|x-c\right|< \delta$ implies $\left|f\left(x\right)-f\left(c\right)\right|< \varepsilon$. Since $g\left(t\right)\to c$, there exists $T> 0$ such that $t> T$ implies $\left|g\left(t\right)-c\right|< \delta$. Thus for $t> T$, $\left|f\left(g\left(t\right)\right)-f\left(c\right)\right|< \varepsilon$, i.e. $\lim f\left(g\left(t\right)\right)=f\left(c\right)$. $\blacksquare$

---

## 1.7-5

Let $f\left(x\right)$ and $g\left(x\right)$ be defined and continuous on $\mathbb R$. Suppose $f\left(x\right)=g\left(x\right)$ for all $x\in\mathbb Q$. Prove $f\left(x\right)\equiv g\left(x\right)$ for all $x\in\mathbb R$.

### Solution 1.7-5

Take any $x_0\in\mathbb R$. By density of rationals, there is a rational sequence $\left\{r_n\right\}$ with $r_n\to x_0$. Since $f,g$ are continuous,

$$
f\left(x_0\right)=\lim_{n\to\infty}f\left(r_n\right)=\lim_{n\to\infty}g\left(r_n\right)=g\left(x_0\right).
$$

Thus $f\left(x_0\right)=g\left(x_0\right)$. Since $x_0$ is arbitrary, $f\equiv g$. $\blacksquare$

---

## 1.7-6

Let $t_1$ and $t_2$ be arbitrary real numbers. Without using $e^{t_1+t_2}=e^{t_1}\cdot e^{t_2}$, prove

$$
\lim_{x\to\infty}\left[\left(1+\frac{t_1}{x}\right)\left(1+\frac{t_2}{x}\right)\right]^x=e^{t_1+t_2}.
$$

### Solution 1.7-6

$$
\left[\left(1+\frac{t_1}{x}\right)\left(1+\frac{t_2}{x}\right)\right]^x=\left(1+\frac{t_1+t_2+t_1t_2/x}{x}\right)^x=\left[\left(1+\frac{t_1+t_2+o\left(1\right)}{x}\right)^{\frac{x}{t_1+t_2+o\left(1\right)}}\right]^{t_1+t_2+o\left(1\right)}.
$$

The base tends to $e$ and the exponent to $t_1+t_2$. By continuity of the exponential, the limit is $e^{t_1+t_2}$. $\blacksquare$
