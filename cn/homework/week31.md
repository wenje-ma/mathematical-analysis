# week31

> **定理 4.2 (三重积分的穿线法)**<br>设 $\Omega=\left\{\left(x,y,z\right):\left(x,y\right)\in D,z_1\left(x,y\right)\le z\le z_2\left(x,y\right)\right\}$. 则 $\iiint_\Omega f\,\mathrm dV=\iint_D\mathrm dx\mathrm dy\int_{z_1\left(x,y\right)}^{z_2\left(x,y\right)}f\,\mathrm dz$.

> **定理 4.4 (三重积分换元公式)**<br>$\iiint_\Omega f\,\mathrm dx\mathrm dy\mathrm dz=\iiint_{\Omega'}f\left(x\left(u,v,w\right),y\left(u,v,w\right),z\left(u,v,w\right)\right)\left|J\right|\,\mathrm du\mathrm dv\mathrm dw$. 柱坐标 $\left|J\right|=r$, 球坐标 $\left|J\right|=\rho^2\sin\varphi$.

---

## 8.4-1

计算 $\iiint_\Omega z^2\,\mathrm dV$, 其中 $\Omega$ 为单位球.

### 解答 8.4-1

由对称性, $\iiint z^2=\frac13\iiint\left(x^2+y^2+z^2\right)$. 用球坐标, 由**定理 4.4 (三重积分换元公式)**,

$$
\iiint_\Omega z^2\,\mathrm dV=\frac{4\pi}{15}.
$$

$\blacksquare$

---

## 8.4-2

计算 $\iiint_\Omega\left(x+y+z\right)\,\mathrm dV$, 其中 $\Omega=\left\{x^2+y^2\le4,0\le z\le1\right\}$.

### 解答 8.4-2

由对称性, $\iiint x=\iiint y=0$. 用柱坐标, 由**定理 4.4 (三重积分换元公式)**,

$$
\iiint_\Omega z\,\mathrm dV=2\pi.
$$

$\blacksquare$

---

## 8.4-3

计算 $\iiint_\Omega\left(x+y+z\right)^3\,\mathrm dV$, 其中 $\Omega$ 为球体 $x^2+y^2+z^2\le R^2$.

### 解答 8.4-3

展开后每一项均为某个变量的奇函数, 而球体关于各坐标平面对称. 故

$$
\iiint_\Omega\left(x+y+z\right)^3\,\mathrm dV=0.
$$

$\blacksquare$

---

## 8.4-5

计算 $\iiint_\Omega\left(x^2+y^2+z^2\right)\,\mathrm dV$, 其中 $\Omega=\left\{a^2\le x^2+y^2+z^2\le b^2\right\}$.

### 解答 8.4-5

用球坐标, 由**定理 4.4 (三重积分换元公式)**,

$$
\iiint_\Omega\left(x^2+y^2+z^2\right)\,\mathrm dV=\frac{4\pi}5\left(b^5-a^5\right).
$$

$\blacksquare$

---

## 8.4-6

计算 $\iiint_\Omega\left(x^2+y^2\right)\,\mathrm dV$, 其中 $\Omega=\left\{x^2+y^2\le z\le1\right\}$.

### 解答 8.4-6

用柱坐标, 由**定理 4.2 (三重积分的穿线法)** 与**定理 4.4 (三重积分换元公式)**,

$$
\iiint_\Omega\left(x^2+y^2\right)\,\mathrm dV=\frac\pi6.
$$

$\blacksquare$

---

## 8.4-8

计算 $\iiint_\Omega\left(x^2+y^2\right)^2\,\mathrm dV$, 其中 $\Omega$ 由 $z=\sqrt{1-x^2-y^2}$ 与 $z=\sqrt{x^2+y^2}$ 围成.

### 解答 8.4-8

在球坐标下, $0\le\rho\le1$, $0\le\varphi\le\pi/4$. 由**定理 4.4 (三重积分换元公式)**,

$$
\iiint_\Omega\left(x^2+y^2\right)^2\,\mathrm dV=\frac{\pi\left(64-43\sqrt2\right)}{420}.
$$

$\blacksquare$

---

## 8.4-9

计算 $\iiint_\Omega\sqrt{x^2+y^2+z^2}\,\mathrm dV$, 其中 $\Omega$ 为球面 $x^2+y^2+z^2=x$ 内部.

### 解答 8.4-9

球面方程化为 $\rho=\sin\varphi\cos\theta$. 由**定理 4.4 (三重积分换元公式)**,

$$
\iiint_\Omega\sqrt{x^2+y^2+z^2}\,\mathrm dV=\frac\pi{10}.
$$

$\blacksquare$

---

## 8.4-10

计算 $\iiint_\Omega\left(x+1\right)\left(y+1\right)\,\mathrm dV$, 其中 $\Omega$ 为椭球体 $\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}\le1$.

### 解答 8.4-10

展开: $\left(x+1\right)\left(y+1\right)=xy+x+y+1$. 由对称性, 前三项积分为 $0$. 故

$$
\iiint_\Omega\left(x+1\right)\left(y+1\right)\,\mathrm dV=\iiint_\Omega 1\,\mathrm dV=\frac{4\pi abc}{3}.
$$

$\blacksquare$
