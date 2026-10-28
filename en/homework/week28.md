# week28

> **Basic Knowledge: Properties of Double Integrals**<br>(1) Additivity over regions; (2) monotonicity: $f\le g\Rightarrow\iint_D f\le\iint_D g$; (3) Mean value theorem: $\iint_D f=f\left(x_0,y_0\right)\cdot S$.

> **Proposition 1.3 (Necessary and Sufficient Condition for Measurable Area)**<br>$E$ is measurable iff $\partial E$ has zero area.

> **Theorem 1.4 (Necessary and Sufficient Condition for Integrability)**<br>$f$ is integrable on $D$ iff $\lim_{\lambda\to0}\sum_i\omega_i\Delta\sigma_i=0$.

> **Theorem 1.5 (Continuous Functions Are Integrable)**<br>If $D$ is a bounded closed region with zero-area boundary and $f$ is continuous on $D$, then $f$ is integrable.

---

## 8.1-2

Prove: if $f$ and $g$ are integrable on $D$, then $f\cdot g$ is integrable.

### Solution 8.1-2

Using $\omega_{fg}\le A\omega_g+B\omega_f$ and **Theorem 1.4 (Necessary and Sufficient Condition for Integrability)**, the result follows. $\blacksquare$

---

## 8.1-3

Prove the Dirichlet function $D\left(x,y\right)$ is not integrable on $\left[0,1\right]^2$.

### Solution 8.1-3

Every subregion contains both rational and irrational points, so $\omega_i=1$. The oscillation sum equals $1$, not $0$. By **Theorem 1.4 (Necessary and Sufficient Condition for Integrability)**, not integrable. $\blacksquare$

---

## 8.1-4

Prove: modifying $f$ on a line segment $\gamma$ does not change the integral.

### Solution 8.1-4

By **Proposition 1.3 (Necessary and Sufficient Condition for Measurable Area)**, $\gamma$ has zero area. By additivity, the integral over $\gamma$ is $0$. $\blacksquare$

---

## 8.1-5

Prove: if $f$ is integrable, then $\left|f\right|$ is integrable.

### Solution 8.1-5

Since $\omega_{\left|f\right|}\le\omega_f$, **Theorem 1.4 (Necessary and Sufficient Condition for Integrability)** gives integrability. $\blacksquare$

---

## 8.1-8

Prove: there exists $\left(x_0,y_0\right)$ such that $\iint_D fg=f\left(x_0,y_0\right)\iint_D g$.

### Solution 8.1-8

By **Theorem 1.5 (Continuous Functions Are Integrable)**, $f$ has max $M$ and min $m$. By monotonicity, $m\iint_D g\le\iint_D fg\le M\iint_D g$. The intermediate value theorem gives the result. $\blacksquare$

---

## 8.1-9

Let $f\ge0$ be continuous on $D$ with $\iint_D f=0$. Prove $f\equiv0$.

### Solution 8.1-9

If $f\left(x_0,y_0\right)> 0$, continuity gives a neighborhood where $f> \frac{f\left(x_0,y_0\right)}2$. By monotonicity, the integral is positive. $\blacksquare$
