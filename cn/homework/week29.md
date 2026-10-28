# week29

> **基础知识: 二重积分的比较性质**<br>若 $f\le g$ 在 $D$ 上, 则 $\iint_D f\le\iint_D g$.

> **定理 2.1 (化二重积分为累次积分)**<br>设 $f$ 在 $D=\left\{\left(x,y\right):a\le x\le b,\varphi_1\left(x\right)\le y\le\varphi_2\left(x\right)\right\}$ 上连续, 则 $\iint_D f\,\mathrm dx\mathrm dy=\int_a^b\mathrm dx\int_{\varphi_1\left(x\right)}^{\varphi_2\left(x\right)}f\left(x,y\right)\,\mathrm dy$.

> **定理 2.2 (极坐标下的二重积分)**<br>$\iint_D f\,\mathrm dx\mathrm dy=\iint_{D^*}f\left(r\cos\theta,r\sin\theta\right)\,r\,\mathrm dr\mathrm d\theta$.

---

## 8.2-2

改变下列累次积分的积分次序:

(1) $\int_0^1\mathrm dy\int_y^{\sqrt y}f\,\mathrm dx$;

(2) $\int_1^2\mathrm dx\int_x^{2x}f\,\mathrm dy$;

(3) $\int_0^5\mathrm dx\int_x^{10-x}f\,\mathrm dy$;

(4) $\int_0^1\mathrm dx\int_{e^x}^e f\,\mathrm dy$.

### 解答 8.2-2

(1) 由 $y\le x\le\sqrt y$ 得 $x^2\le y\le x$. 故原式 $=\int_0^1\mathrm dx\int_{x^2}^x f\,\mathrm dy$.

(2) 分段: $y\in\left[1,2\right]$ 时 $1\le x\le y$; $y\in\left[2,4\right]$ 时 $y/2\le x\le2$. 故原式 $=\int_1^2\mathrm dy\int_1^y f\,\mathrm dx+\int_2^4\mathrm dy\int_{y/2}^2 f\,\mathrm dx$.

(3) 分段: $y\in\left[0,5\right]$ 时 $0\le x\le y$; $y\in\left[5,10\right]$ 时 $0\le x\le10-y$. 故原式 $=\int_0^5\mathrm dy\int_0^y f\,\mathrm dx+\int_5^{10}\mathrm dy\int_0^{10-y}f\,\mathrm dx$.

(4) 由 $e^x\le y\le e$ 得 $0\le x\le\ln y$. 故原式 $=\int_1^e\mathrm dy\int_0^{\ln y}f\,\mathrm dx$. $\blacksquare$

---

## 8.2-3

计算下列二重积分:

(1) $\iint_D y\,\mathrm dx\mathrm dy$, $D$ 由 $y=0$ 及 $y=\sin x$ ($0\le x\le\pi$) 围成;

(2) $\iint_D\left(x^2+y\right)\,\mathrm dx\mathrm dy$, $D$ 由 $y=x^2$ 及 $y^2=x$ 围成;

(3) $\iint_D e^{x/y}\,\mathrm dx\mathrm dy$, $D$ 由 $y^2=x$, $x=0$, $y=1$ 围成;

(4) $\iint_D\sqrt{1-x^4}\,\mathrm dx\mathrm dy$, $D$ 由 $y=x^3$, $x=1$, $y=0$ 围成.

### 解答 8.2-3

(1) 由**定理 2.1 (化二重积分为累次积分)**, $\iint_D y=\frac12\int_0^\pi\sin^2x\,\mathrm dx=\frac\pi4$.

(2) $\iint_D\left(x^2+y\right)=\int_0^1\left(x^{5/2}+\frac x2-\frac32x^4\right)\mathrm dx=\frac{33}{140}$.

(3) 先对 $x$ 积分: $\iint_D e^{x/y}=\int_0^1\left(ye^y-y\right)\mathrm dy=\frac12$.

(4) $\iint_D\sqrt{1-x^4}=\int_0^1 x^3\sqrt{1-x^4}\,\mathrm dx=\frac16$. $\blacksquare$

---

## 8.2-4

计算下列累次积分:

(1) $\int_0^\pi\mathrm dx\int_x^\pi\frac{\sin y}{y}\,\mathrm dy$;

(2) $\int_0^2\mathrm dx\int_x^2 2y^2\sin\left(xy\right)\,\mathrm dy$.

### 解答 8.2-4

(1) 交换次序: $\int_0^\pi\mathrm dy\int_0^y\frac{\sin y}{y}\,\mathrm dx=\int_0^\pi\sin y\,\mathrm dy=2$.

(2) 交换次序: $\int_0^2\mathrm dy\int_0^y 2y^2\sin\left(xy\right)\,\mathrm dx=\int_0^2 2y\left[1-\cos\left(y^2\right)\right]\mathrm dy=4-\sin4$. $\blacksquare$

---

## 8.2-5

用极坐标计算:

(1) $\int_{-1}^0\mathrm dx\int_{-\sqrt{1-x^2}}^0\frac{2}{1+\sqrt{x^2+y^2}}\,\mathrm dy$;

(2) $\int_0^2\mathrm dx\int_0^{\sqrt{1-\left(x-1\right)^2}}3xy\,\mathrm dy$;

(3) $\int_0^R\mathrm dx\int_0^{\sqrt{R^2-x^2}}\ln\left(1+x^2+y^2\right)\,\mathrm dy$.

### 解答 8.2-5

(1) 第三象限单位圆. 由**定理 2.2 (极坐标下的二重积分)**, $\pi\left(1-\ln2\right)$.

(2) 上半圆 $\left(x-1\right)^2+y^2\le1$. $=2$.

(3) 第一象限四分之一圆盘. $=\frac\pi4\left[\left(1+R^2\right)\ln\left(1+R^2\right)-R^2\right]$. $\blacksquare$

---

## 8.2-6

求 $\iint_D e^{-x^2-y^2}\,\mathrm dx\mathrm dy$, 其中 $D$ 为圆环 $1\le x^2+y^2\le4$ 在第一象限部分.

### 解答 8.2-6

由**定理 2.2 (极坐标下的二重积分)**,

$$
\iint_D e^{-x^2-y^2}=\frac\pi4\left(e^{-1}-e^{-4}\right).
$$

$\blacksquare$

---

## 8.2-7

计算:

(1) $\iint_D\sin\sqrt{x^2+y^2}\,\mathrm dx\mathrm dy$, $D=\left\{\pi^2\le x^2+y^2\le4\pi^2\right\}$;

(2) $\iint_D\left(x+y\right)\,\mathrm dx\mathrm dy$, $D=\left\{x^2+y^2\le x+y\right\}$;

(3) $\iint_D\left(x^2+y^2\right)\,\mathrm dx\mathrm dy$, $D=\left\{\left(x^2+y^2\right)^2\le a^2\left(x^2-y^2\right)\right\}$;

(4) $\iint_D x\,\mathrm dx\mathrm dy$, $D$ 为阿基米德螺线 $r=\theta$ 与 $\theta=\pi$ 所围区域.

### 解答 8.2-7

(1) $=-6\pi^2$.

(2) 平移后由对称性, $=\frac\pi2$.

(3) 双纽线, $=\frac{\pi a^4}{8}$.

(4) $=4-\pi^2$. $\blacksquare$

---

## 8.2-8

设 $I\left(a\right)=\int_0^a e^{-x^2}\,\mathrm dx$, $J\left(a\right)=\iint_{D_a}e^{-x^2-y^2}\,\mathrm dx\mathrm dy$, 其中 $D_a$ 为第一象限四分之一圆盘. 证明:

(1) $\left[I\left(a\right)\right]^2=\iint_{R_a}e^{-x^2-y^2}\,\mathrm dx\mathrm dy$;

(2) $J\left(a\right)\le\left[I\left(a\right)\right]^2\le J\left(\sqrt2 a\right)$;

(3) $\lim_{a\to\infty}\int_0^a e^{-x^2}\,\mathrm dx=\frac{\sqrt\pi}2$.

### 解答 8.2-8

(1) 由**定理 2.1 (化二重积分为累次积分)**, $\left[I\left(a\right)\right]^2=\iint_{R_a}e^{-x^2-y^2}$.

(2) 因 $D_a\subset R_a\subset D_{\sqrt2 a}$, 由**基础知识: 二重积分的比较性质**, 得 $J\left(a\right)\le\left[I\left(a\right)\right]^2\le J\left(\sqrt2 a\right)$.

(3) 由**定理 2.2 (极坐标下的二重积分)**, $J\left(a\right)=\frac\pi4\left(1-e^{-a^2}\right)$. 代入 (2) 并令 $a\to\infty$, 由夹逼定理, $\left[I\left(a\right)\right]^2\to\frac\pi4$, 故 $I\left(a\right)\to\frac{\sqrt\pi}2$. $\blacksquare$
