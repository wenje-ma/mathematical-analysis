# week35

> **定理 4.1 (奥-高公式)**
> 
> 设 $S$ 为空间闭区域 $\Omega$ 的边界曲面外侧, $P,Q,R$ 在 $\Omega$ 上有一阶连续偏导数. 则 $\oiint_S P\,\mathrm dy\mathrm dz+Q\,\mathrm dz\mathrm dx+R\,\mathrm dx\mathrm dy=\iiint_\Omega\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)\mathrm dV$.

---

## 9.3-1

求 $\iint_S\left(y+x\right)\,\mathrm dS$, 其中 $S$ 为立方体表面.

### 解答 9.3-1

由对称性, $\iint_S x=\iint_S y$. 分别计算六个面得 $\iint_S x=3$. 故原式 $=6$. $\blacksquare$

---

## 9.3-3

求 $\oiint_S\left(xy+z\right)^2\,\mathrm dS$, 其中 $S$ 为球面 $x^2+y^2+z^2=R^2$.

### 解答 9.3-3

展开: $\left(xy+z\right)^2=x^2y^2+2xyz+z^2$. 由对称性, $2xyz$ 积分为 $0$. 故

$$
\oiint_S\left(xy+z\right)^2=\frac{4\pi R^6}{15}+\frac{4\pi R^4}{3}.
$$

$\blacksquare$

---

## 9.3-5

求抛物面薄壳 $z=\frac12\left(x^2+y^2\right)$ ($0\le z\le1$) 的质量, 面密度 $\rho=x+y+z$.

### 解答 9.3-5

由第一型曲面积分的计算, $\mathrm dS=\sqrt{1+x^2+y^2}\,\mathrm dx\mathrm dy$. 由对称性, $x,y$ 项积分为 $0$. 用极坐标,

$$
M=\frac{\pi\left(12\sqrt3+2\right)}{15}.
$$

$\blacksquare$

---

## 9.3-6

求第一卦限球面 $x^2+y^2+z^2=a^2$ 的质心坐标.

### 解答 9.3-6

由对称性, $\overline x=\overline y=\overline z$. 曲面面积 $=\frac{\pi a^2}{2}$. 计算得 $\overline z=\frac a2$. 质心为 $\left(\frac a2,\frac a2,\frac a2\right)$. $\blacksquare$

---

## 9.3-7

求 $I=\iint_S y\left(x-z\right)\,\mathrm dy\mathrm dz+x^2\,\mathrm dz\mathrm dx+\left(y^2+zx\right)\,\mathrm dx\mathrm dy$, 其中 $S$ 为立方体外侧.

### 解答 9.3-7

由**定理 4.1 (奥-高公式)**,

$$
I=\iiint_\Omega\left(y+0+x\right)\mathrm dV=a^4.
$$

$\blacksquare$

---

## 9.3-8

求 $I=\iint_S\left(y-z\right)x\,\mathrm dy\mathrm dz+\left(x-y\right)\,\mathrm dx\mathrm dy$, 其中 $S$ 为圆柱面外侧.

### 解答 9.3-8

由**定理 4.1 (奥-高公式)**, $I=\iiint_\Omega\left(y-z\right)\mathrm dV$. 用柱坐标, 由对称性 $y$ 项为 $0$, 得

$$
I=-\frac{9\pi}{2}.
$$

$\blacksquare$

---

## 9.3-9

求 $I=\iint_S\left(y-z\right)\,\mathrm dy\mathrm dz+\left(z-x\right)\,\mathrm dz\mathrm dx+\left(x-y\right)\,\mathrm dx\mathrm dy$.

### 解答 9.3-9

由第二型曲面积分的计算, 代入上侧公式. 由对称性, 奇函数项积分为 $0$. 故 $I=\pi Rr^2$. $\blacksquare$

---

## 9.3-10

求 $I=\iint_S x\,\mathrm dy\mathrm dz+y\,\mathrm dz\mathrm dx+z\,\mathrm dx\mathrm dy$, 其中 $S$ 为椭球面外侧.

### 解答 9.3-10

由**定理 4.1 (奥-高公式)**,

$$
I=3\iiint_\Omega\mathrm dV=4\pi abc.
$$

$\blacksquare$
