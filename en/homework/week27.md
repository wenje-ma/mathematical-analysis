# week27

> **Basic Knowledge: Comparison Property of Integrals**<br>If $f\le g$ on $\left[a,b\right]$, then $\int_a^b f\le\int_a^b g$.

> **Lemma 2.1 (Effect of Refining a Partition)**<br>Adding points to a partition decreases the upper sum and increases the lower sum.

> **Theorem 2.2 (Necessary and Sufficient Condition for Integrability)**<br>$f$ is Riemann integrable iff $\lim_{\lambda\to0}\left[D\left(T\right)-d\left(T\right)\right]=0$.

---

## 6.2-1

Prove: if $f$ is integrable on $\left[a,b\right]$, then it is integrable on any subinterval $\left[c,d\right]$.

### Solution 6.2-1

By **Lemma 2.1 (Effect of Refining a Partition)**, the oscillation sum on $\left[c,d\right]$ is bounded by that on $\left[a,b\right]$. By **Theorem 2.2 (Necessary and Sufficient Condition for Integrability)**, it tends to $0$. $\blacksquare$

---

## 6.2-2

Prove: if $f$ and $g$ are integrable, then $f\cdot g$ is integrable.

### Solution 6.2-2

Using $\omega_{fg}\le M\omega_g+N\omega_f$ and **Theorem 2.2 (Necessary and Sufficient Condition for Integrability)**, the result follows. $\blacksquare$

---

## 6.2-4

Let $f$ be continuous, $f\ge0$. Prove $\int_a^b f=0$ iff $f\equiv0$.

### Solution 6.2-4

If $f\left(x_0\right)> 0$, continuity gives a neighborhood where $f> \frac{f\left(x_0\right)}2$. By comparison property, the integral is positive. $\blacksquare$

---

## 6.2-6

Prove: if $f$ is integrable, then $\left|f\right|$ is integrable and $\left|\int_a^b f\right|\le\int_a^b\left|f\right|$.

### Solution 6.2-6

Since $\omega_{\left|f\right|}\le\omega_f$, **Theorem 2.2 (Necessary and Sufficient Condition for Integrability)** gives integrability of $\left|f\right|$. The inequality follows from $-\left|f\right|\le f\le\left|f\right|$ and the comparison property. $\blacksquare$
