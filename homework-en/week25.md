# week25

> **Theorem 1.3 (Lagrange Mean Value Theorem)**
> 
> If $f$ is continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$, then there exists $c\in\left(a,b\right)$ such that $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

> **Proposition 1.3 (Necessary and Sufficient Condition for Measurable Area)**
> 
> $E$ is measurable iff $\partial E$ has zero area.

> **Theorem 1.4 (Necessary and Sufficient Condition for Integrability)**
> 
> $f$ is integrable on $D$ iff $\lim_{\lambda\to0}\sum_i\omega_i\Delta\sigma_i=0$.

> **Theorem 1.5 (Continuous Functions Are Integrable)**
> 
> If $D$ is a bounded closed region with zero-area boundary and $f$ is continuous on $D$, then $f$ is integrable.

> **Lemma 2.1 (Effect of Refining a Partition)**
> 
> Adding points to a partition decreases the upper sum and increases the lower sum.

> **Theorem 2.2 (Necessary and Sufficient Condition for Integrability)**
> 
> $f$ is Riemann integrable iff $\lim_{\lambda\to0}\left[D\left(T\right)-d\left(T\right)\right]=0$.

## 6.1-3

Express the area as an integral; find $\int_c^d\varphi+\int_a^b\psi$.

### Solution to 6.1-3

The area is $\int_c^d\varphi\left(y\right)\,\mathrm dy$. The sum equals $bd-ac$. $\blacksquare$

## 6.1-5

Prove: $f$ is integrable iff the lower and upper Darboux sums converge to the same limit.

### Solution to 6.1-5

Necessity: if $f$ is integrable with integral $I$, then both lower and upper sums approach $I$.

Sufficiency: if both limits equal $I$, then by squeeze theorem any Riemann sum approaches $I$. $\blacksquare$

## 6.1-6

Prove:

(1) $\frac\pi2\le\int_0^{\pi/2}\left(1+\sin x\right)\,\mathrm dx\le\pi$;

(2) $\sqrt2\le\int_0^1\sqrt{2+x-x^2}\,\mathrm dx\le\frac32$.

### Solution to 6.1-6

By the comparison property of integrals. $\blacksquare$

## 6.1-8

Prove: $\int_a^b f\left(x\right)\,\mathrm dx=F\left(b\right)-F\left(a\right)$.

### Solution to 6.1-8

For any partition, by **Theorem 1.3 (Lagrange Mean Value Theorem)**,

$$
F\left(b\right)-F\left(a\right)=\sum f\left(\xi_k\right)\Delta x_k.
$$

Taking the limit gives the result. $\blacksquare$

## 6.2-1

Prove: if $f$ is integrable on $\left[a,b\right]$, then it is integrable on any subinterval $\left[c,d\right]$.

### Solution to 6.2-1

By **Lemma 2.1 (Effect of Refining a Partition)**, the oscillation sum on $\left[c,d\right]$ is bounded by that on $\left[a,b\right]$. By **Theorem 2.2 (Necessary and Sufficient Condition for Integrability)**, it tends to $0$. $\blacksquare$

## 6.2-2

Prove: if $f$ and $g$ are integrable, then $f\cdot g$ is integrable.

### Solution to 6.2-2

Using $\omega_{fg}\le M\omega_g+N\omega_f$ and **Theorem 2.2 (Necessary and Sufficient Condition for Integrability)**, the result follows. $\blacksquare$

## 6.2-4

Let $f$ be continuous, $f\ge0$. Prove $\int_a^b f=0$ iff $f\equiv0$.

### Solution to 6.2-4

If $f\left(x_0\right)> 0$, continuity gives a neighborhood where $f> \frac{f\left(x_0\right)}2$. By comparison property, the integral is positive. $\blacksquare$

## 6.2-6

Prove: if $f$ is integrable, then $\left|f\right|$ is integrable and $\left|\int_a^b f\right|\le\int_a^b\left|f\right|$.

### Solution to 6.2-6

Since $\omega_{\left|f\right|}\le\omega_f$, **Theorem 2.2 (Necessary and Sufficient Condition for Integrability)** gives integrability of $\left|f\right|$. The inequality follows from $-\left|f\right|\le f\le\left|f\right|$ and the comparison property. $\blacksquare$

## 8.1-2

Prove: if $f$ and $g$ are integrable on $D$, then $f\cdot g$ is integrable.

### Solution to 8.1-2

Using $\omega_{fg}\le A\omega_g+B\omega_f$ and **Theorem 1.4 (Necessary and Sufficient Condition for Integrability)**, the result follows. $\blacksquare$
