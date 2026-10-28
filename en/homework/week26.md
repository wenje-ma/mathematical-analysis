# week26

> **Basic Knowledge: Definition of Definite Integral**<br>$I=\int_a^b f\left(x\right)\,\mathrm dx$ if the Riemann sums converge to $I$ as the mesh $\lambda\left(T\right)\to0$, uniformly in the choice of sample points.

> **Basic Knowledge: Comparison Property of Integrals**<br>If $f\le g$ on $\left[a,b\right]$, then $\int_a^b f\le\int_a^b g$.

> **Theorem 1.3 (Lagrange Mean Value Theorem)**<br>If $f$ is continuous on $\left[a,b\right]$ and differentiable on $\left(a,b\right)$, then there exists $c\in\left(a,b\right)$ such that $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

---

## 6.1-2

Compute the Riemann sums for $y=x$ and $y=x^2$ on $\left[0,1\right]$ ($n$ equal subintervals, right endpoints) and take $n\to\infty$.

### Solution 6.1-2

For $y=x$: $\frac{n+1}{2n}\to\frac12$, so $\int_0^1 x\,\mathrm dx=\frac12$.

For $y=x^2$: $\frac{\left(n+1\right)\left(2n+1\right)}{6n^2}\to\frac13$, so $\int_0^1 x^2\,\mathrm dx=\frac13$. $\blacksquare$

---

## 6.1-3

Express the area as an integral; find $\int_c^d\varphi+\int_a^b\psi$.

### Solution 6.1-3

The area is $\int_c^d\varphi\left(y\right)\,\mathrm dy$. The sum equals $bd-ac$. $\blacksquare$

---

## 6.1-5

Prove: $f$ is integrable iff the lower and upper Darboux sums converge to the same limit.

### Solution 6.1-5

**Necessity**: if $f$ is integrable with integral $I$, then both lower and upper sums approach $I$.

**Sufficiency**: if both limits equal $I$, then by squeeze theorem any Riemann sum approaches $I$. $\blacksquare$

---

## 6.1-6

Prove:

(1) $\frac\pi2\le\int_0^{\pi/2}\left(1+\sin x\right)\,\mathrm dx\le\pi$;

(2) $\sqrt2\le\int_0^1\sqrt{2+x-x^2}\,\mathrm dx\le\frac32$.

### Solution 6.1-6

By the comparison property of integrals. $\blacksquare$

---

## 6.1-8

Prove: $\int_a^b f\left(x\right)\,\mathrm dx=F\left(b\right)-F\left(a\right)$.

### Solution 6.1-8

For any partition, by **Theorem 1.3 (Lagrange Mean Value Theorem)**,

$$
F\left(b\right)-F\left(a\right)=\sum f\left(\xi_k\right)\Delta x_k.
$$

Taking the limit gives the result. $\blacksquare$
