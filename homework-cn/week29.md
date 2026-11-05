# week29

> **定理 2.2 (格林公式)**
> 
> 设 $L$ 为逐段光滑的简单闭曲线, 所围区域为 $D$, $P,Q$ 在 $D$ 上有一阶连续偏导数. 则 $\oint_{L^+}P\,\mathrm{d}x+Q\,\mathrm{d}y=\iint_D\left(\frac{\partial{Q}}{\partial{x}}-\frac{\partial{P}}{\partial{y}}\right)\mathrm{d}x\mathrm{d}y$.

> **定理 2.4 (积分与路径无关的条件)**
> 
> 设 $D$ 为单连通域, $P,Q$ 在 $D$ 内有一阶连续偏导数. 则 $\int{P}\,\mathrm{d}x+Q\,\mathrm{d}y$ 与路径无关的充要条件是 $\frac{\partial{Q}}{\partial{x}}=\frac{\partial{P}}{\partial{y}}$.

> **定理 2.5 (恰当微分形式)**
> 
> $P\,\mathrm{d}x+Q\,\mathrm{d}y$ 为恰当微分形式的充要条件是 $\frac{\partial{Q}}{\partial{x}}=\frac{\partial{P}}{\partial{y}}$.

> **定理 4.1 (奥-高公式)**
> 
> 设 $S$ 为空间闭区域 $\Omega$ 的边界曲面外侧, $P,Q,R$ 在 $\Omega$ 上有一阶连续偏导数. 则 $\oiint_SP\,\mathrm{d}y\mathrm{d}z+Q\,\mathrm{d}z\mathrm{d}x+R\,\mathrm{d}x\mathrm{d}y=\iiint_\Omega\left(\frac{\partial{P}}{\partial{x}}+\frac{\partial{Q}}{\partial{y}}+\frac{\partial{R}}{\partial{z}}\right)\mathrm{d}V$.

> **定理 4.2 (斯托克斯公式)**
> 
> 设 $S$ 为分片光滑的双侧曲面, 边界 $L$ 为分段光滑闭曲线, $L$ 的定向与 $S$ 的法向量构成右手系. 则 $\oint_{L^+}P\,\mathrm{d}x+Q\,\mathrm{d}y+R\,\mathrm{d}z=\iint_{S^+}\left(\frac{\partial{R}}{\partial{y}}-\frac{\partial{Q}}{\partial{z}}\right)\mathrm{d}y\mathrm{d}z+\left(\frac{\partial{P}}{\partial{z}}-\frac{\partial{R}}{\partial{x}}\right)\mathrm{d}z\mathrm{d}x+\left(\frac{\partial{Q}}{\partial{x}}-\frac{\partial{P}}{\partial{y}}\right)\mathrm{d}x\mathrm{d}y$.

## 9.2-5-3

求 $\int_{\left(0,0\right)}^{\left(a,b\right)}e^x\cos{y}\,\mathrm{d}x-e^x\sin{y}\,\mathrm{d}y$.

### 解答 9.2-5-3

由**定理 2.4 (积分与路径无关的条件)**, 积分与路径无关. 又 $d\left(e^x\cos{y}\right)=e^x\cos{y}\,\mathrm{d}x-e^x\sin{y}\,\mathrm{d}y$. 由**定理 2.5 (恰当微分形式)**,

$$
\text{原式}=e^a\cos{b}-1.
$$

$\blacksquare$

## 9.2-6

证明: $\oint_{L_r^+}\frac{x\,\mathrm{d}y-y\,\mathrm{d}x}{A^2x^2+B^2y^2}=\frac{2\pi}{AB}$.

### 解答 9.2-6

在 $L_r$ 上分母为 $r^2$. 由**定理 2.2 (格林公式)** 的推论, $\oint{x}\,\mathrm{d}y-y\,\mathrm{d}x=2m\left(D\right)$. 椭圆面积 $m\left(D\right)=\frac{\pi{r}^2}{AB}$. 故原式 $=\frac{2\pi}{AB}$. $\blacksquare$

## 9.2-7

证明: 对任意包含原点的闭曲线 $\Gamma$, $\oint_{\Gamma^+}\frac{x\,\mathrm{d}y-y\,\mathrm{d}x}{A^2x^2+B^2y^2}=\frac{2\pi}{AB}$.

### 解答 9.2-7

在 $\left(x,y\right)\ne\left(0,0\right)$ 处, $\frac{\partial{Q}}{\partial{x}}=\frac{\partial{P}}{\partial{y}}$. 取充分小的椭圆 $L_r$ 含于 $\Gamma$ 内部, 在复连通区域上应用**定理 2.2 (格林公式)**, 得 $\oint_{\Gamma^+}=\oint_{L_r^+}$. 由 9.2-6, $=\frac{2\pi}{AB}$. $\blacksquare$

## 9.3-1

求 $\iint_S\left(y+x\right)\,\mathrm{d}S$, 其中 $S$ 为立方体表面.

### 解答 9.3-1

由对称性, $\iint_Sx=\iint_Sy$. 分别计算六个面得 $\iint_Sx=3$. 故原式 $=6$. $\blacksquare$

## 9.3-3

求 $\oiint_S\left(xy+z\right)^2\,\mathrm{d}S$, 其中 $S$ 为球面 $x^2+y^2+z^2=R^2$.

### 解答 9.3-3

展开: $\left(xy+z\right)^2=x^2y^2+2xyz+z^2$. 由对称性, $2xyz$ 积分为 $0$. 故

$$
\oiint_S\left(xy+z\right)^2=\frac{4\pi{R}^6}{15}+\frac{4\pi{R}^4}{3}.
$$

$\blacksquare$

## 9.3-5

求抛物面薄壳 $z=\frac12\left(x^2+y^2\right)$ ($0\le{z}\le1$) 的质量, 面密度 $\rho=x+y+z$.

### 解答 9.3-5

由第一型曲面积分的计算, $\mathrm{d}S=\sqrt{1+x^2+y^2}\,\mathrm{d}x\mathrm{d}y$. 由对称性, $x,y$ 项积分为 $0$. 用极坐标,

$$
M=\frac{\pi\left(12\sqrt3+2\right)}{15}.
$$

$\blacksquare$

## 9.3-6

求第一卦限球面 $x^2+y^2+z^2=a^2$ 的质心坐标.

### 解答 9.3-6

由对称性, $\overline{x}=\overline{y}=\overline{z}$. 曲面面积 $=\frac{\pi{a}^2}{2}$. 计算得 $\overline{z}=\frac{a}2$. 质心为 $\left(\frac{a}2,\frac{a}2,\frac{a}2\right)$. $\blacksquare$

## 9.3-7

求 $I=\iint_Sy\left(x-z\right)\,\mathrm{d}y\mathrm{d}z+x^2\,\mathrm{d}z\mathrm{d}x+\left(y^2+zx\right)\,\mathrm{d}x\mathrm{d}y$, 其中 $S$ 为立方体外侧.

### 解答 9.3-7

由**定理 4.1 (奥-高公式)**,

$$
I=\iiint_\Omega\left(y+0+x\right)\mathrm{d}V=a^4.
$$

$\blacksquare$

## 9.3-8

求 $I=\iint_S\left(y-z\right)x\,\mathrm{d}y\mathrm{d}z+\left(x-y\right)\,\mathrm{d}x\mathrm{d}y$, 其中 $S$ 为圆柱面外侧.

### 解答 9.3-8

由**定理 4.1 (奥-高公式)**, $I=\iiint_\Omega\left(y-z\right)\mathrm{d}V$. 用柱坐标, 由对称性 $y$ 项为 $0$, 得

$$
I=-\frac{9\pi}{2}.
$$

$\blacksquare$

## 9.3-9

求 $I=\iint_S\left(y-z\right)\,\mathrm{d}y\mathrm{d}z+\left(z-x\right)\,\mathrm{d}z\mathrm{d}x+\left(x-y\right)\,\mathrm{d}x\mathrm{d}y$.

### 解答 9.3-9

由第二型曲面积分的计算, 代入上侧公式. 由对称性, 奇函数项积分为 $0$. 故 $I=\pi{R}r^2$. $\blacksquare$

## 9.3-10

求 $I=\iint_Sx\,\mathrm{d}y\mathrm{d}z+y\,\mathrm{d}z\mathrm{d}x+z\,\mathrm{d}x\mathrm{d}y$, 其中 $S$ 为椭球面外侧.

### 解答 9.3-10

由**定理 4.1 (奥-高公式)**,

$$
I=3\iiint_\Omega\mathrm{d}V=4\pi{a}bc.
$$

$\blacksquare$

## 9.4-1

求 $\oiint_{S^+}xz^2\,\mathrm{d}y\mathrm{d}z+\left(x^2y-z^3\right)\,\mathrm{d}z\mathrm{d}x+\left(2xy+y^2z\right)\,\mathrm{d}x\mathrm{d}y$, 其中 $S^+$ 为半球区域全表面外侧.

### 解答 9.4-1

由**定理 4.1 (奥-高公式)**, 被积散度为 $z^2+x^2+y^2$. 用球坐标,

$$
I=\frac{2\pi{a}^5}{5}.
$$

$\blacksquare$

## 9.4-3

求 $\oiint_{S^+}x^3\,\mathrm{d}y\mathrm{d}z+y^3\,\mathrm{d}z\mathrm{d}x+z^3\,\mathrm{d}x\mathrm{d}y$, $S^+$ 为球面外侧.

### 解答 9.4-3

由**定理 4.1 (奥-高公式)**, $I=3\iiint_\Omega\left(x^2+y^2+z^2\right)\mathrm{d}V=\frac{12\pi{a}^5}{5}$. $\blacksquare$

## 9.4-5

求 $\oiint_{S^+}\boldsymbol{F}\cdot\boldsymbol{n}\,\mathrm{d}S$, 其中 $\boldsymbol{F}=\left(x^4,y^4,z^4\right)$, $S^+$ 为锥面侧面.

### 解答 9.4-5

补上顶面 $S_1$. 由**定理 4.1 (奥-高公式)**, 散度为 $4\left(x^3+y^3+z^3\right)$. 由对称性 $x^3,y^3$ 项为 $0$. 三重积分 $=\frac{2\pi{h}^6}{3}$. 顶面贡献 $=\pi{h}^6$. 故原式 $=-\frac{\pi{h}^6}{3}$. $\blacksquare$

## 9.4-7

求 $\oint_{L^+}y^2\,\mathrm{d}x+xy\,\mathrm{d}y+xz\,\mathrm{d}z$, 其中 $L$ 为圆柱面与平面 $y=z$ 的交线.

### 解答 9.4-7

旋度 $\nabla\times\boldsymbol{F}=\left(0,-z,-y\right)$. 取曲面 $S$ 为平面 $y=z$ 上的区域. 由**定理 4.2 (斯托克斯公式)**, 因 $z=y$, 被积表达式为 $0$. 故 $\oint_{L^+}=0$. $\blacksquare$

## 9.4-8

求 $\oint_{L^+}\left(y^2+z^2-x^2\right)\,\mathrm{d}x+\left(x^2+z^2-y^2\right)\,\mathrm{d}y+\left(x^2+y^2-z^2\right)\,\mathrm{d}z$.

### 解答 9.4-8

旋度 $\nabla\times\boldsymbol{F}=2\left(y-z,z-x,x-y\right)$. 取曲面 $S$ 为上半球面. 由**定理 4.2 (斯托克斯公式)**, 化简后被积函数为 $2\left(R-\frac{Ry}{z}\right)$. 由对称性, $y/z$ 项积分为 $0$. 故 $\oint_{L^+}=2\pi{R}r^2$. $\blacksquare$
