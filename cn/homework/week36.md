# week36

> **定理 4.1 (奥-高公式)**<br>设 $S$ 是分片光滑的封闭曲面, 所围区域为 $\Omega$, $P,Q,R$ 在 $\Omega$ 中有一阶连续偏导数. 则 $\oiint_{S^+}P\,\mathrm dy\mathrm dz+Q\,\mathrm dz\mathrm dx+R\,\mathrm dx\mathrm dy=\iiint_\Omega\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)\mathrm dV$.

> **定理 4.2 (斯托克斯公式)**<br>设 $S$ 为分片光滑的双侧曲面, 边界 $L$ 为分段光滑闭曲线, $L$ 的定向与 $S$ 的法向量构成右手系. 则 $\oint_{L^+}P\,\mathrm dx+Q\,\mathrm dy+R\,\mathrm dz=\iint_{S^+}\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right)\mathrm dy\mathrm dz+\left(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}\right)\mathrm dz\mathrm dx+\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm dx\mathrm dy$.

---

## 9.4-1

求 $\oiint_{S^+}xz^2\,\mathrm dy\mathrm dz+\left(x^2y-z^3\right)\,\mathrm dz\mathrm dx+\left(2xy+y^2z\right)\,\mathrm dx\mathrm dy$, 其中 $S^+$ 为半球区域全表面外侧.

### 解答 9.4-1

由**定理 4.1 (奥-高公式)**, 被积散度为 $z^2+x^2+y^2$. 用球坐标,

$$
I=\frac{2\pi a^5}{5}.
$$

$\blacksquare$

---

## 9.4-3

求 $\oiint_{S^+}x^3\,\mathrm dy\mathrm dz+y^3\,\mathrm dz\mathrm dx+z^3\,\mathrm dx\mathrm dy$, $S^+$ 为球面外侧.

### 解答 9.4-3

由**定理 4.1 (奥-高公式)**, $I=3\iiint_\Omega\left(x^2+y^2+z^2\right)\mathrm dV=\frac{12\pi a^5}{5}$. $\blacksquare$

---

## 9.4-5

求 $\oiint_{S^+}\boldsymbol F\cdot\boldsymbol n\,\mathrm dS$, 其中 $\boldsymbol F=\left(x^4,y^4,z^4\right)$, $S^+$ 为锥面侧面.

### 解答 9.4-5

补上顶面 $S_1$. 由**定理 4.1 (奥-高公式)**, 散度为 $4\left(x^3+y^3+z^3\right)$. 由对称性 $x^3,y^3$ 项为 $0$. 三重积分 $=\frac{2\pi h^6}{3}$. 顶面贡献 $=\pi h^6$. 故原式 $=-\frac{\pi h^6}{3}$. $\blacksquare$

---

## 9.4-7

求 $\oint_{L^+}y^2\,\mathrm dx+xy\,\mathrm dy+xz\,\mathrm dz$, 其中 $L$ 为圆柱面与平面 $y=z$ 的交线.

### 解答 9.4-7

旋度 $\nabla\times\boldsymbol F=\left(0,-z,-y\right)$. 取曲面 $S$ 为平面 $y=z$ 上的区域. 由**定理 4.2 (斯托克斯公式)**, 因 $z=y$, 被积表达式为 $0$. 故 $\oint_{L^+}=0$. $\blacksquare$

---

## 9.4-8

求 $\oint_{L^+}\left(y^2+z^2-x^2\right)\,\mathrm dx+\left(x^2+z^2-y^2\right)\,\mathrm dy+\left(x^2+y^2-z^2\right)\,\mathrm dz$.

### 解答 9.4-8

旋度 $\nabla\times\boldsymbol F=2\left(y-z,z-x,x-y\right)$. 取曲面 $S$ 为上半球面. 由**定理 4.2 (斯托克斯公式)**, 化简后被积函数为 $2\left(R-\frac{Ry}{z}\right)$. 由对称性, $y/z$ 项积分为 $0$. 故 $\oint_{L^+}=2\pi Rr^2$. $\blacksquare$
