# week9

> **Proposition 1.7 (Triangle Inequality)**
> 
> For any real $a,b,c$, $\left|a-c\right|\le\left|a-b\right|+\left|b-c\right|$.

> **Theorem 7.2 (Continuity of Composite Functions)**
> 
> If $y=g\left(u\right)$ is continuous at $u_0$ and $u=f\left(x\right)$ is continuous at $x_0$ with $f\left(x_0\right)=u_0$, then $y=g\left(f\left(x\right)\right)$ is continuous at $x_0$.

> **Theorem 8.1 (Intermediate Value Theorem)**
> 
> If $y=f\left(x\right)$ is continuous on $\left[a,b\right]$ and $f\left(a\right)$ and $f\left(b\right)$ have opposite signs, then there exists $c\in\left(a,b\right)$ with $f\left(c\right)=0$. More generally, $f$ takes every value between $f\left(a\right)$ and $f\left(b\right)$.

> **Theorem 8.2 (Boundedness Theorem)**
> 
> A continuous function on a closed interval is bounded and attains its maximum and minimum.

## 1.7-4

Let $y=f\left(x\right)$ be continuous on $\left(a,b\right)$, and $x=g\left(t\right)$ have a limit as $t\to\infty$ lying in $\left(a,b\right)$. Prove

$$
\lim_{t\to\infty}f\left(g\left(t\right)\right)=f\left(\lim_{t\to\infty}g\left(t\right)\right).
$$

### Solution to 1.7-4

Let $\lim_{t\to\infty}g\left(t\right)=c\in\left(a,b\right)$. By Definition of Continuous Function, given $\varepsilon>0$, there exists $\delta>0$ such that $\left|x-c\right|<\delta$ implies $\left|f\left(x\right)-f\left(c\right)\right|<\varepsilon$. Since $g\left(t\right)\to{c}$, there exists $T>0$ such that $t>{}T$ implies $\left|g\left(t\right)-c\right|<\delta$. Thus for $t>{}T$, $\left|f\left(g\left(t\right)\right)-f\left(c\right)\right|<\varepsilon$, i.e. $\lim{f}\left(g\left(t\right)\right)=f\left(c\right)$. $\blacksquare$

## 1.7-5

Let $f\left(x\right)$ and $g\left(x\right)$ be defined and continuous on $\mathbb{R}$. Suppose $f\left(x\right)=g\left(x\right)$ for all $x\in\mathbb{Q}$. Prove $f\left(x\right)\equiv{g}\left(x\right)$ for all $x\in\mathbb{R}$.

### Solution to 1.7-5

Take any $x_0\in\mathbb{R}$. By density of rationals, there is a rational sequence $\left\{r_n\right\}$ with $r_n\to{x}_0$. Since $f,g$ are continuous,

$$
f\left(x_0\right)=\lim_{n\to\infty}f\left(r_n\right)=\lim_{n\to\infty}g\left(r_n\right)=g\left(x_0\right).
$$

Thus $f\left(x_0\right)=g\left(x_0\right)$. Since $x_0$ is arbitrary, $f\equiv{g}$. $\blacksquare$

## 1.7-6

Let $t_1$ and $t_2$ be arbitrary real numbers. Without using $e^{t_1+t_2}=e^{t_1}\cdot{e}^{t_2}$, prove

$$
\lim_{x\to\infty}\left[\left(1+\frac{t_1}{x}\right)\left(1+\frac{t_2}{x}\right)\right]^x=e^{t_1+t_2}.
$$

### Solution to 1.7-6

$$
\left[\left(1+\frac{t_1}{x}\right)\left(1+\frac{t_2}{x}\right)\right]^x=\left(1+\frac{t_1+t_2+t_1t_2/x}{x}\right)^x=\left[\left(1+\frac{t_1+t_2+o\left(1\right)}{x}\right)^{\frac{x}{t_1+t_2+o\left(1\right)}}\right]^{t_1+t_2+o\left(1\right)}.
$$

The base tends to $e$ and the exponent to $t_1+t_2$. By continuity of the exponential, the limit is $e^{t_1+t_2}$. $\blacksquare$

## 1.8-2

Let $y=f\left(x\right)$ be continuous on $\left(a,b\right)$, and let $x_1,x_2,x_3\in\left(a,b\right)$ with $x_1<{}x_2<{}x_3$. Set

$$
\eta=\frac13\left[f\left(x_1\right)+f\left(x_2\right)+f\left(x_3\right)\right].
$$

Prove that there exists $\xi\in\left[x_1,x_3\right]$ such that $f\left(\xi\right)=\eta$.

### Solution to 1.8-2

$f$ is continuous on $\left[x_1,x_3\right]$. By **Theorem 8.2 (Boundedness Theorem)**, let the max be $M$ and min be $m$. Then $m\le{f}\left(x_i\right)\le{M}$, so $m\le\eta\le{M}$. By **Theorem 8.1 (Intermediate Value Theorem)**, there exists $\xi\in\left[x_1,x_3\right]$ with $f\left(\xi\right)=\eta$. $\blacksquare$

## 1.8-3

Let $y=f\left(x\right)$ be continuous on $\left[a,+\infty\right)$ with $\lim_{x\to+\infty}f\left(x\right)=l$ and $l>{}f\left(a\right)$. Prove that for any $\eta$ with $f\left(a\right)<\eta<{}l$, there exists $\xi\in\left(a,+\infty\right)$ such that $f\left(\xi\right)=\eta$.

### Solution to 1.8-3

Since $\lim_{x\to+\infty}f\left(x\right)=l>\eta$, there exists $A>{}a$ such that $x>{}A$ implies $f\left(x\right)>\eta$. Take $b>{}A$, so $f\left(a\right)<\eta<{}f\left(b\right)$. Since $f$ is continuous on $\left[a,b\right]$, by **Theorem 8.1 (Intermediate Value Theorem)**, there exists $\xi\in\left(a,b\right)\subset\left(a,+\infty\right)$ with $f\left(\xi\right)=\eta$. $\blacksquare$

## 1.8-4

Let $y=f\left(x\right)$ be continuous on $\left[a,+\infty\right)$ and $\lim_{x\to+\infty}f\left(x\right)$ exists. Prove $f$ is bounded on $\left[a,+\infty\right)$.

### Solution to 1.8-4

Let $\lim_{x\to+\infty}f\left(x\right)=l$. There exists $A>{}a$ such that $x>{}A$ implies $\left|f\left(x\right)-l\right|<1$, i.e. $\left|f\left(x\right)\right|<\left|l\right|+1$. On $\left[a,A\right]$, by **Theorem 8.2 (Boundedness Theorem)**, $f$ is bounded, say $\left|f\left(x\right)\right|\le{M}$. Take $\widetilde{M}=\max\left\{M,\left|l\right|+1\right\}$; then $\left|f\left(x\right)\right|\le\widetilde{M}$ for all $x\in\left[a,+\infty\right)$. $\blacksquare$

## 1.8-5

Let $y=f\left(x\right)$ be continuous on $\left(a,b\right)$, and let $x_1,x_2\in\left(a,b\right)$ with $x_1<{}x_2$, $m_1>0$, $m_2>0$. Prove that there exists $\xi\in\left(a,b\right)$ such that

$$
f\left(\xi\right)=\frac{m_1f\left(x_1\right)+m_2f\left(x_2\right)}{m_1+m_2}.
$$

### Solution to 1.8-5

Let the max and min of $f$ on $\left[x_1,x_2\right]$ be $M$ and $m$. Then

$$
m=\frac{m_1m+m_2m}{m_1+m_2}\le\frac{m_1f\left(x_1\right)+m_2f\left(x_2\right)}{m_1+m_2}\le\frac{m_1M+m_2M}{m_1+m_2}=M.
$$

By **Theorem 8.1 (Intermediate Value Theorem)**, there exists $\xi\in\left[x_1,x_2\right]\subset\left(a,b\right)$ with $f\left(\xi\right)=\frac{m_1f\left(x_1\right)+m_2f\left(x_2\right)}{m_1+m_2}$. $\blacksquare$
