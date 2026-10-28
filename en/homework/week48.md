# week48

> **Theorem 3.3 (Differentiation Under the Integral Sign)**<br>$I'\left(y\right)=\int_a^b f_y\left(x,y\right)\mathrm dx$. If limits depend on $y$, add boundary terms.

---

## 12.3-2-5

Find $I'\left(y\right)$ for $I\left(y\right)=\int_{\sin y}^{\cos y}e^{y\sqrt{1-x^2}}\mathrm dx$.

### Solution 12.3-2-5

$I'\left(y\right)=\int_{\sin y}^{\cos y}\sqrt{1-x^2}e^{y\sqrt{1-x^2}}\mathrm dx-e^{y\sin y}\sin y-e^{y\cos y}\cos y$. $\blacksquare$

---

## 12.3-2-6

Find $I'\left(y\right)$ for $I\left(y\right)=\int_0^{x/y}y\sin\left(xy\right)\mathrm dx$.

### Solution 12.3-2-6

$I'\left(y\right)=0$. $\blacksquare$

---

## 12.3-2-7

Find $I'\left(y\right)$ for $I\left(y\right)=\int_0^{y^2}\sin\left(x^2+y^2\right)\mathrm dx$.

### Solution 12.3-2-7

$I'\left(y\right)=\int_0^{y^2}2y\cos\left(x^2+y^2\right)\mathrm dx+2y\sin\left(y^4+y^2\right)$. $\blacksquare$

---

## 12.3-2-8

Find $I'\left(y\right)$ for $I\left(y\right)=\int_0^y\frac{\ln\left(1+xy\right)}x\mathrm dx$.

### Solution 12.3-2-8

$I'\left(y\right)=\frac{\ln\left(1+y^2\right)}y+\int_0^y\frac{\mathrm dx}{1+xy}$. $\blacksquare$

---

## 12.3-4-1

Evaluate $I\left(r\right)=\int_0^\pi\ln\left(1-2r\cos x+r^2\right)\mathrm dx$.

### Solution 12.3-4-1

$I\left(r\right)=0$. $\blacksquare$

---

## 12.3-6

Prove $I\left(\alpha\right)=2\pi\ln\frac{1+\sqrt{1-\alpha^2}}2$.

### Solution 12.3-6

By differentiation under the integral sign. $\blacksquare$
