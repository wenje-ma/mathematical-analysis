# week30

> **Theorem 3.1 (Change of Variables in Double Integrals)**<br>$\iint_D f\,\mathrm dx\mathrm dy=\iint_G f\left(x\left(u,v\right),y\left(u,v\right)\right)\left|J\left(u,v\right)\right|\,\mathrm du\mathrm dv$.

---

## 8.3-1

Compute $\iint_D\left(\sqrt{y/x}+\sqrt{xy}\right)$ using a change of variables.

### Solution 8.3-1

Let $u=xy$, $v=y/x$. By **Theorem 3.1 (Change of Variables in Double Integrals)**,

$$
=8+\frac{52}{3}\ln2.
$$

$\blacksquare$

---

## 8.3-4

Compute $\iint_D\left(x+y\right)$.

### Solution 8.3-4

Let $u=y/x^2$, $v=x/y^2$. By **Theorem 3.1 (Change of Variables in Double Integrals)**,

$$
=\frac3{10}\left(9^{-5/3}-4^{-5/3}\right)\left(9^{-4/3}-4^{-4/3}\right).
$$

$\blacksquare$

---

## 8.3-6

Find the area enclosed by $\left(\frac{x^2}{a^2}+\frac{y^2}{b^2}\right)^2=\frac{xy}{c^2}$.

### Solution 8.3-6

Use generalized polar coordinates $x=ar\cos\theta$, $y=br\sin\theta$. By **Theorem 3.1 (Change of Variables in Double Integrals)**,

$$
m\left(D\right)=\frac{a^2b^2}{2c^2}.
$$

$\blacksquare$
