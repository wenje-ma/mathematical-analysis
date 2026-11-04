# week26

> **Proposition 1.3 (Necessary and Sufficient Condition for Measurable Area)**
> 
> $E$ is measurable iff $\partial E$ has zero area.

> **Theorem 1.4 (Necessary and Sufficient Condition for Integrability)**
> 
> $f$ is integrable on $D$ iff $\lim_{\lambda\to0}\sum_i\omega_i\Delta\sigma_i=0$.

> **Theorem 1.5 (Continuous Functions Are Integrable)**
> 
> If $D$ is a bounded closed region with zero-area boundary and $f$ is continuous on $D$, then $f$ is integrable.

> **Theorem 2.1 (Reduction to Iterated Integrals)**
> 
> $\iint_D f\,\mathrm dx\mathrm dy=\int_a^b\mathrm dx\int_{\varphi_1\left(x\right)}^{\varphi_2\left(x\right)}f\left(x,y\right)\,\mathrm dy$.

> **Theorem 2.2 (Double Integrals in Polar Coordinates)**
> 
> $\iint_D f\,\mathrm dx\mathrm dy=\iint_{D^*}f\left(r\cos\theta,r\sin\theta\right)\,r\,\mathrm dr\mathrm d\theta$.

## 8.1-3

Prove the Dirichlet function $D\left(x,y\right)$ is not integrable on $\left[0,1\right]^2$.

### Solution to 8.1-3

Every subregion contains both rational and irrational points, so $\omega_i=1$. The oscillation sum equals $1$, not $0$. By **Theorem 1.4 (Necessary and Sufficient Condition for Integrability)**, not integrable. $\blacksquare$

## 8.1-4

Prove: modifying $f$ on a line segment $\gamma$ does not change the integral.

### Solution to 8.1-4

By **Proposition 1.3 (Necessary and Sufficient Condition for Measurable Area)**, $\gamma$ has zero area. By additivity, the integral over $\gamma$ is $0$. $\blacksquare$

## 8.1-5

Prove: if $f$ is integrable, then $\left|f\right|$ is integrable.

### Solution to 8.1-5

Since $\omega_{\left|f\right|}\le\omega_f$, **Theorem 1.4 (Necessary and Sufficient Condition for Integrability)** gives integrability. $\blacksquare$

## 8.1-8

Prove: there exists $\left(x_0,y_0\right)$ such that $\iint_D fg=f\left(x_0,y_0\right)\iint_D g$.

### Solution to 8.1-8

By **Theorem 1.5 (Continuous Functions Are Integrable)**, $f$ has max $M$ and min $m$. By monotonicity, $m\iint_D g\le\iint_D fg\le M\iint_D g$. The intermediate value theorem gives the result. $\blacksquare$

## 8.1-9

Let $f\ge0$ be continuous on $D$ with $\iint_D f=0$. Prove $f\equiv0$.

### Solution to 8.1-9

If $f\left(x_0,y_0\right)> 0$, continuity gives a neighborhood where $f> \frac{f\left(x_0,y_0\right)}2$. By monotonicity, the integral is positive. $\blacksquare$

## 8.2-2

Change the order of integration.

### Solution to 8.2-2

(1) $\int_0^1\mathrm dx\int_{x^2}^x f\,\mathrm dy$.

(2) $\int_1^2\mathrm dy\int_1^y f\,\mathrm dx+\int_2^4\mathrm dy\int_{y/2}^2 f\,\mathrm dx$.

(3) $\int_0^5\mathrm dy\int_0^y f\,\mathrm dx+\int_5^{10}\mathrm dy\int_0^{10-y}f\,\mathrm dx$.

(4) $\int_1^e\mathrm dy\int_0^{\ln y}f\,\mathrm dx$. $\blacksquare$

## 8.2-3

Compute.

### Solution to 8.2-3

(1) $\frac\pi4$. (2) $\frac{33}{140}$. (3) $\frac12$. (4) $\frac16$. $\blacksquare$

## 8.2-4

Compute.

### Solution to 8.2-4

(1) $2$. (2) $4-\sin4$. $\blacksquare$

## 8.2-5

Use polar coordinates.

### Solution to 8.2-5

(1) $\pi\left(1-\ln2\right)$. (2) $2$. (3) $\frac\pi4\left[\left(1+R^2\right)\ln\left(1+R^2\right)-R^2\right]$. $\blacksquare$
