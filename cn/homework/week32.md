# week32

> **基础知识: 质心坐标公式**<br>设物体占据区域 $\Omega$, 密度为 $\rho$, 质量 $m=\iiint_\Omega\rho\,\mathrm dV$, 则质心坐标为 $x_0=\frac1m\iiint_\Omega x\rho\,\mathrm dV$, $y_0=\frac1m\iiint_\Omega y\rho\,\mathrm dV$, $z_0=\frac1m\iiint_\Omega z\rho\,\mathrm dV$.

> **基础知识: 转动惯量公式**<br>物体关于 $z$ 轴的转动惯量为 $J_z=\iiint_\Omega\left(x^2+y^2\right)\rho\,\mathrm dV$.

> **命题 5.1 (曲面面积公式)**<br>设 $z=f\left(x,y\right)$ 在 $D$ 上有连续一阶偏导数, 则曲面面积 $S=\iint_D\sqrt{1+f_x^2+f_y^2}\,\mathrm dx\mathrm dy$.

---

## 8.5-1

求锥面 $z=\sqrt{x^2+y^2}$ 被柱面 $z^2=2x$ 所割下部分的面积.

### 解答 8.5-1

投影区域为圆域 $D=\left\{\left(x-1\right)^2+y^2\le1\right\}$. 由 $f=\sqrt{x^2+y^2}$ 得 $\sqrt{1+f_x^2+f_y^2}=\sqrt2$. 由**命题 5.1 (曲面面积公式)**,

$$
S=\sqrt2\cdot\pi.
$$

$\blacksquare$

---

## 8.5-2

求曲面 $az=xy$ 包围在圆柱 $x^2+y^2=a^2$ 内部的那部分面积.

### 解答 8.5-2

$z=xy/a$, $\sqrt{1+f_x^2+f_y^2}=\sqrt{1+\frac{x^2+y^2}{a^2}}$. 由**命题 5.1 (曲面面积公式)** 并用极坐标,

$$
S=\frac{2\pi a^2}{3}\left(2\sqrt2-1\right).
$$

$\blacksquare$

---

## 8.5-3

求第一卦限中均匀椭球体 $\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}\le1$ 的质心坐标.

### 解答 8.5-3

体积 $V=\frac{\pi abc}{6}$. 用广义球坐标, 由**基础知识: 质心坐标公式**,

$$
z_0=\frac{\iiint z\,\mathrm dV}{V}=\frac{3c}{8}.
$$

由对称性, $x_0=\frac{3a}{8}$, $y_0=\frac{3b}{8}$. 质心为 $\left(\frac{3a}{8},\frac{3b}{8},\frac{3c}{8}\right)$. $\blacksquare$

---

## 8.5-6

设立方体 $\Omega=\left[0,a\right]^3$, 密度为常数 $\rho$. 求对 $z$ 轴的转动惯量.

### 解答 8.5-6

由**基础知识: 转动惯量公式**,

$$
J_z=\rho\iiint_\Omega\left(x^2+y^2\right)\,\mathrm dV=\frac{2\rho a^5}{3}.
$$

$\blacksquare$
