# week34

> **定理 2.2 (格林公式)**<br>设 $L$ 为逐段光滑的简单闭曲线, 所围区域为 $D$, $P,Q$ 在 $D$ 上有一阶连续偏导数. 则 $\oint_{L^+}P\,\mathrm dx+Q\,\mathrm dy=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm dx\mathrm dy$.

> **定理 2.4 (积分与路径无关的条件)**<br>设 $D$ 为单连通域, $P,Q$ 在 $D$ 内有一阶连续偏导数. 则 $\int P\,\mathrm dx+Q\,\mathrm dy$ 与路径无关的充要条件是 $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$.

> **定理 2.5 (恰当微分形式)**<br>$P\,\mathrm dx+Q\,\mathrm dy$ 为恰当微分形式的充要条件是 $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$.

---

## 9.2-1

求 $\oint_{L^+}x^2\,\mathrm dy-y^2\,\mathrm dx$, 其中 $L$ 为椭圆周.

### 解答 9.2-1

由**定理 2.2 (格林公式)**, 原式 $=\iint_D\left(2x+2y\right)\,\mathrm dx\mathrm dy$. 由对称性, 积分为 $0$. $\blacksquare$

---

## 9.2-2

求 $\int_L\left(x^2+y^2\right)\,\mathrm dx+\left(x^2-y\right)\,\mathrm dy$, 其中 $L$ 为 $y=\left|x\right|$ 上从 $\left(-1,1\right)$ 到 $\left(2,2\right)$ 的弧.

### 解答 9.2-2

分段计算: $L_1$ 上 $=\frac56$, $L_2$ 上 $=6$. 故原式 $=\frac{41}{6}$. $\blacksquare$

---

## 9.2-3

应用格林公式计算:

(1) $\oint_{L^+}\left(xy^2+y^3\right)\,\mathrm dy-\left(x^3+x^2y\right)\,\mathrm dx$, $L$ 为圆周;

(2) $\oint_{L^+}\sqrt{x^2+y^2}\,\mathrm dx+y\left[xy+\ln\left(x+\sqrt{x^2+y^2}\right)\right]\mathrm dy$, $L$ 为三角形;

(3) $\oint_{L^+}\left(e^x\sin y+\sin x-8y\right)\,\mathrm dx+\left(e^x\cos y-\sin y\right)\,\mathrm dy$, $L$ 为上半圆边界.

### 解答 9.2-3

(1) 由**定理 2.2 (格林公式)**, $=\iint_D\left(x^2+y^2\right)=\frac{\pi R^4}{2}$.

(2) $\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=y^2$. $=\frac{25}{6}$.

(3) $\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=8$. $=8\cdot\frac{\pi a^2}{8}=\pi a^2$. $\blacksquare$

---

## 9.2-4

证明: $\oint_{L^+}f\left(xy\right)\left(y\,\mathrm dx+x\,\mathrm dy\right)=0$.

### 解答 9.2-4

$P=yf\left(xy\right)$, $Q=xf\left(xy\right)$. 计算得 $\frac{\partial P}{\partial y}=\frac{\partial Q}{\partial x}=f\left(xy\right)+xyf'\left(xy\right)$. 由**定理 2.2 (格林公式)**, 原式 $=0$. $\blacksquare$

---

## 9.2-5-3

求 $\int_{\left(0,0\right)}^{\left(a,b\right)}e^x\cos y\,\mathrm dx-e^x\sin y\,\mathrm dy$.

### 解答 9.2-5-3

由**定理 2.4 (积分与路径无关的条件)**, 积分与路径无关. 又 $d\left(e^x\cos y\right)=e^x\cos y\,\mathrm dx-e^x\sin y\,\mathrm dy$. 由**定理 2.5 (恰当微分形式)**,

$$
\text{原式}=e^a\cos b-1.
$$

$\blacksquare$

---

## 9.2-6

证明: $\oint_{L_r^+}\frac{x\,\mathrm dy-y\,\mathrm dx}{A^2x^2+B^2y^2}=\frac{2\pi}{AB}$.

### 解答 9.2-6

在 $L_r$ 上分母为 $r^2$. 由**定理 2.2 (格林公式)** 的推论, $\oint x\,\mathrm dy-y\,\mathrm dx=2m\left(D\right)$. 椭圆面积 $m\left(D\right)=\frac{\pi r^2}{AB}$. 故原式 $=\frac{2\pi}{AB}$. $\blacksquare$

---

## 9.2-7

证明: 对任意包含原点的闭曲线 $\Gamma$, $\oint_{\Gamma^+}\frac{x\,\mathrm dy-y\,\mathrm dx}{A^2x^2+B^2y^2}=\frac{2\pi}{AB}$.

### 解答 9.2-7

在 $\left(x,y\right)\ne\left(0,0\right)$ 处, $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$. 取充分小的椭圆 $L_r$ 含于 $\Gamma$ 内部, 在复连通区域上应用**定理 2.2 (格林公式)**, 得 $\oint_{\Gamma^+}=\oint_{L_r^+}$. 由 9.2-6, $=\frac{2\pi}{AB}$. $\blacksquare$
