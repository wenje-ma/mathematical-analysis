# Assignment 26

> **Definition** (Definite Integral) Let $f\left(x\right)$ be defined on the interval $\left[a,b\right]$. Make a partition of $\left[a,b\right]$
> $$
> T:a=x_0<x_1<\cdots<x_n=b,
> $$
where $\Delta x_k=x_k-x_{k-1}$, $\lambda\left(T\right)=\max_{1\le k\le n}\Delta x_k$. If there exists a constant $I$ such that for any $\varepsilon>0$, there exists $\delta>0$ such that whenever $\lambda\left(T\right)<\delta$, no matter how the partition $T$ is chosen and no matter how the intermediate points $\xi_k\in\left[x_{k-1},x_k\right]$ are chosen, we have
> $$
> \left|\sum_{k=1}^n f\left(\xi_k\right)\Delta x_k-I\right|<\varepsilon,
> $$
> then $I$ is called the definite integral of $f\left(x\right)$ on $\left[a,b\right]$, denoted $\int_a^b f\left(x\right)\,\mathrm{d}x$.

> **Property** (Comparison Property of Definite Integrals) Let $f,g$ be integrable on $\left[a,b\right]$, and $f\left(x\right)\le g\left(x\right)$ ($\forall x\in\left[a,b\right]$), then $\int_a^b f\left(x\right)\,\mathrm{d}x\le\int_a^b g\left(x\right)\,\mathrm{d}x$. In particular, when $f\left(x\right)\ge0$, $\int_a^b f\left(x\right)\,\mathrm{d}x\ge0$.

### Problem 1

(Problem 6.1-2) Write down the Riemann sums of the functions $y=x$ and $y=x^2$ on the interval $\left[0,1\right]$, where the partition divides it into $n$ equal parts and the intermediate points $\xi_k$ are taken to be the right endpoints of the subintervals. Find the limit of this Riemann sum as $n\to\infty$. (Hint: use the formula

$$
1^2+2^2+\cdots+n^2=\frac{n\left(n+1\right)\left(2n+1\right)}{6}.
$$

)

### Solution to Problem 1

Divide $\left[0,1\right]$ into $n$ equal parts, with partition points $x_k=k/n$ ($k=0,1,\dots,n$); then $\Delta x_k=1/n$, $\lambda\left(T\right)=1/n$, and take the intermediate points $\xi_k=x_k=k/n$.

For $y=x$, the Riemann sum is

$$
\sum_{k=1}^n \xi_k\Delta x_k=\sum_{k=1}^n \frac{k}{n}\cdot\frac1n=\frac1{n^2}\sum_{k=1}^n k=\frac1{n^2}\cdot\frac{n\left(n+1\right)}2=\frac{n+1}{2n}.
$$

Letting $n\to\infty$, by **Definition** (Definite Integral) we get

$$
\int_0^1 x\,\mathrm{d}x=\lim_{n\to\infty}\frac{n+1}{2n}=\frac12.
$$

For $y=x^2$, the Riemann sum is

$$
\sum_{k=1}^n \xi_k^2\Delta x_k=\sum_{k=1}^n \left(\frac{k}{n}\right)^2\frac1n=\frac1{n^3}\sum_{k=1}^n k^2=\frac1{n^3}\cdot\frac{n\left(n+1\right)\left(2n+1\right)}6=\frac{\left(n+1\right)\left(2n+1\right)}{6n^2}.
$$

Letting $n\to\infty$, by **Definition** (Definite Integral) we get

$$
\int_0^1 x^2\,\mathrm{d}x=\lim_{n\to\infty}\frac{\left(n+1\right)\left(2n+1\right)}{6n^2}=\frac13.
$$

$\blacksquare$

### Problem 2

(Problem 6.1-3) Let the function $x=\varphi\left(y\right)$ be continuous on $\left[c,d\right]$ and satisfy $\varphi\left(y\right)>0$. Express as a definite integral the area of the region bounded by the curve $x=\varphi\left(y\right)$, $y=c$, $y=d$, and the $y$-axis. Moreover, let $c\ge0$ and let $x=\varphi\left(y\right)$ be strictly increasing on $\left[c,d\right]$. Find the integral sum $\int_c^d \varphi\left(y\right)\,\mathrm{d}y+\int_a^b \psi\left(x\right)\,\mathrm{d}x$, where $y=\psi\left(x\right)$ is the inverse function of $x=\varphi\left(y\right)$, $a=\varphi\left(c\right)$, and $b=\varphi\left(d\right)$.

### Solution to Problem 2

(1) The region bounded by the curve $x=\varphi\left(y\right)$, $y=c$, $y=d$, and the $y$-axis can be divided along the $y$-axis into horizontal strips: at height $y$, the strip has width $\varphi\left(y\right)$ and height $\mathrm{d}y$, so the area element is $\varphi\left(y\right)\,\mathrm{d}y$. By **Definition** (Definite Integral), the enclosed area is $\displaystyle S=\int_c^d \varphi\left(y\right)\,\mathrm{d}y$.

(2) Since $x=\varphi\left(y\right)$ is strictly increasing on $\left[c,d\right]$ and $c\ge0$, its inverse function $y=\psi\left(x\right)$ is also strictly increasing on $\left[a,b\right]$, where $a=\varphi\left(c\right)\ge0$ and $b=\varphi\left(d\right)$.

Consider the rectangles $\left[0,b\right]\times\left[0,d\right]$ and $\left[0,a\right]\times\left[0,c\right]$. The region

$$
\left[0,b\right]\times\left[0,d\right]\setminus\left[0,a\right]\times\left[0,c\right]
$$

is divided by the curve $x=\varphi\left(y\right)$ (i.e. $y=\psi\left(x\right)$) into two parts: the part to the left of the curve between $y=c$ and $y=d$, with area $\int_c^d \varphi\left(y\right)\,\mathrm{d}y$; and the part below the curve between $x=a$ and $x=b$, with area $\int_a^b \psi\left(x\right)\,\mathrm{d}x$. The sum of the two areas equals the area of the large rectangle minus the area of the small rectangle, i.e.

$$
\int_c^d \varphi\left(y\right)\,\mathrm{d}y+\int_a^b \psi\left(x\right)\,\mathrm{d}x=bd-ac.

$$

$\blacksquare$
### Problem 3

(Problem 6.1-5) Let the function $y=f\left(x\right)$ be defined on $\left[a,b\right]$, and assume that $y=f\left(x\right)$ has a maximum and minimum value on every closed subinterval. For any partition

$$
T:a=x_0<x_1<\cdots<x_n=b,
$$

let $m_i$ be the minimum of $y=f\left(x\right)$ on $\left[x_{i-1},x_i\right]$ and $M_i$ the maximum. Prove that $y=f\left(x\right)$ is integrable on $\left[a,b\right]$ if and only if the limits $\lim_{\lambda\left(T\right)\to0}\sum_{i=1}^n m_i\Delta x_i$ and $\lim_{\lambda\left(T\right)\to0}\sum_{i=1}^n M_i\Delta x_i$ exist and are equal.

### Solution to Problem 3

**Necessity** Let $f$ be integrable on $\left[a,b\right]$ with integral $I$. For any $\varepsilon>0$, by **Definition** (Definite Integral), there exists $\delta>0$ such that when $\lambda\left(T\right)<\delta$, for any intermediate points $\xi_i\in\left[x_{i-1},x_i\right]$ we have

$$
\left|\sum_{i=1}^n f\left(\xi_i\right)\Delta x_i-I\right|<\varepsilon.
$$

For each subinterval $\left[x_{i-1},x_i\right]$, since $m_i$ is the minimum of $f$ on it, there exists $\xi_i^*\in\left[x_{i-1},x_i\right]$ such that $f\left(\xi_i^*\right)<m_i+\frac{\varepsilon}{b-a}$. Thus

$$
\sum_{i=1}^n m_i\Delta x_i\le\sum_{i=1}^n f\left(\xi_i^*\right)\Delta x_i<\sum_{i=1}^n m_i\Delta x_i+\varepsilon.
$$

Combining with $\left|\sum f\left(\xi_i^*\right)\Delta x_i-I\right|<\varepsilon$ gives $\left|\sum m_i\Delta x_i-I\right|<2\varepsilon$. Similarly, taking $\xi_i^{**}\in\left[x_{i-1},x_i\right]$ such that $f\left(\xi_i^{**}\right)>M_i-\frac{\varepsilon}{b-a}$, we get $\left|\sum M_i\Delta x_i-I\right|<2\varepsilon$. Hence both limits exist and equal $I$.

**Sufficiency** Let

$$
\lim_{\lambda\left(T\right)\to0}\sum m_i\Delta x_i=\lim_{\lambda\left(T\right)\to0}\sum M_i\Delta x_i=I.
$$

For any intermediate points $\xi_i\in\left[x_{i-1},x_i\right]$, from $m_i\le f\left(\xi_i\right)\le M_i$ we get

$$
\sum_{i=1}^n m_i\Delta x_i\le\sum_{i=1}^n f\left(\xi_i\right)\Delta x_i\le\sum_{i=1}^n M_i\Delta x_i.
$$

Letting $\lambda\left(T\right)\to0$, by the squeeze theorem, $\sum f\left(\xi_i\right)\Delta x_i\to I$. By **Definition** (Definite Integral), $f$ is integrable on $\left[a,b\right]$. $\blacksquare$

### Problem 4

(Problem 6.1-6) Prove the following inequalities (assume all functions involved are integrable):
(1)

$$
\frac{\pi}{2}\le\int_0^{\pi/2}\left(1+\sin x\right)\,\mathrm{d}x\le\pi;
$$

(2)

$$
\sqrt2\le\int_0^1\sqrt{2+x-x^2}\,\mathrm{d}x\le\frac32.
$$

### Solution to Problem 4

(1) On $\left[0,\pi/2\right]$, $0\le\sin x\le1$, so $1\le1+\sin x\le2$. By **Property** (Comparison Property of Definite Integrals),

$$
1\cdot\frac{\pi}{2}\le\int_0^{\pi/2}\left(1+\sin x\right)\,\mathrm{d}x\le2\cdot\frac{\pi}{2}=\pi.
$$

(2) On $\left[0,1\right]$,

$$
2+x-x^2=2+x\left(1-x\right).
$$

Since $0\le x\left(1-x\right)\le\frac14$ (the maximum is attained at $x=\frac12$), we have

$$
2\le2+x-x^2\le\frac94.
$$

Taking square roots gives $\sqrt2\le\sqrt{2+x-x^2}\le\frac32$. By **Property** (Comparison Property of Definite Integrals),

$$
\sqrt2\cdot1\le\int_0^1\sqrt{2+x-x^2}\,\mathrm{d}x\le\frac32\cdot1.

$$

$\blacksquare$
### Problem 5

(Problem 6.1-8) Let $F\left(x\right)$ be continuous on $\left[a,b\right]$, differentiable on $\left(a,b\right)$, and $F'\left(x\right)=f\left(x\right)$. Assume $y=f\left(x\right)$ is integrable on $\left[a,b\right]$, then

$$
\int_a^b f\left(x\right)\,\mathrm{d}x=F\left(b\right)-F\left(a\right).
$$
(Hint: for any partition $T$ of $\left[a,b\right]$, we have

$$
F\left(b\right)-F\left(a\right)=\sum_{k=1}^n\left[F\left(x_k\right)-F\left(x_{k-1}\right)\right],
$$

apply the mean value theorem to $F\left(x_k\right)-F\left(x_{k-1}\right)$.)

### Solution to Problem 5

Make any partition of $\left[a,b\right]$

$$
T:a=x_0<x_1<\cdots<x_n=b.
$$

Then

$$
F\left(b\right)-F\left(a\right)=\sum_{k=1}^n\left[F\left(x_k\right)-F\left(x_{k-1}\right)\right].
$$

On each subinterval $\left[x_{k-1},x_k\right]$, $F$ satisfies the conditions of the Lagrange mean value theorem (continuous, differentiable), so there exists $\xi_k\in\left(x_{k-1},x_k\right)$ such that

$$
F\left(x_k\right)-F\left(x_{k-1}\right)=F'\left(\xi_k\right)\left(x_k-x_{k-1}\right)=f\left(\xi_k\right)\Delta x_k.
$$

Thus

$$
F\left(b\right)-F\left(a\right)=\sum_{k=1}^n f\left(\xi_k\right)\Delta x_k,
$$

which is a Riemann sum of $f$. Since $f$ is integrable on $\left[a,b\right]$, letting $\lambda\left(T\right)\to0$, by **Definition** (Definite Integral), this Riemann sum tends to $\int_a^b f\left(x\right)\,\mathrm{d}x$. Hence

$$
\int_a^b f\left(x\right)\,\mathrm{d}x=F\left(b\right)-F\left(a\right).

$$

$\blacksquare$