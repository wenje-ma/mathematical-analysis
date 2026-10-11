# 作业 34

> **定理 2.2**（格林公式）设 $L$ 为平面 $Oxy$ 上逐段光滑的简单闭曲线, 它所围的有界闭区域为 $D$, $P\left(x,y\right),Q\left(x,y\right)$ 在 $D$ 上有一阶连续偏导数. 则

$$
\oint_{L^+}P\left(x,y\right)\,\mathrm{d}x+Q\left(x,y\right)\,\mathrm{d}y=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y,
$$

其中 $L^+$ 表示逆时针方向.

> **定理 2.4**（积分与路径无关的条件）设 $D$ 为平面单连通域, $P,Q$ 在 $D$ 内有一阶连续偏导数. 则 $\int P\,\mathrm{d}x+Q\,\mathrm{d}y$ 在 $D$ 内与路径无关的充要条件是 $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$ 在 $D$ 内处处成立.

> **定理 2.5**（恰当微分形式）在上述条件下, $P\,\mathrm{d}x+Q\,\mathrm{d}y$ 为恰当微分形式的充要条件是 $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$ 在 $D$ 内处处成立.

### 习题一

（习题 9.2-1）求积分 $\displaystyle\oint_{L^+}x^2\,\mathrm{d}y-y^2\,\mathrm{d}x$, 其中 $L$ 为椭圆周: $\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$, 按逆时针方向.

### 解答 习题一

这里 $P=-y^2$, $Q=x^2$. 由**定理 2.2**（格林公式）,

$$
\oint_{L^+}x^2\,\mathrm{d}y-y^2\,\mathrm{d}x=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y=\iint_D\left(2x+2y\right)\,\mathrm{d}x\mathrm{d}y.
$$

椭圆区域 $D$ 关于 $x=0$ 与 $y=0$ 对称, 而被积函数 $2x+2y$ 关于 $x$ 与 $y$ 均为奇函数, 故积分为 $0$. 即原积分 $=0$. $\blacksquare$

### 习题二

（习题 9.2-2）求 $\displaystyle\int_L\left(x^2+y^2\right)\,\mathrm{d}x+\left(x^2-y\right)\,\mathrm{d}y$, 其中 $L$ 是曲线 $y=\lvert x\rvert$ 上从点 $\left(-1,1\right)$ 到 $\left(2,2\right)$ 的有向弧.

### 解答 习题二

$L$ 分为两段: $L_1$ 从 $\left(-1,1\right)$ 到 $\left(0,0\right)$, 此时 $x\in\left[-1,0\right]$, $y=-x$, $\mathrm{d}y=-\mathrm{d}x$; $L_2$ 从 $\left(0,0\right)$ 到 $\left(2,2\right)$, 此时 $x\in\left[0,2\right]$, $y=x$, $\mathrm{d}y=\mathrm{d}x$.

在 $L_1$ 上:

$$
\int_{L_1}=\int_{-1}^0\left[x^2+\left(-x\right)^2\right]\mathrm{d}x+\left[x^2-\left(-x\right)\right]\left(-\mathrm{d}x\right)=\int_{-1}^0\left(x^2-x\right)\,\mathrm{d}x=\frac56.
$$

在 $L_2$ 上:

$$
\int_{L_2}=\int_0^2 2x^2\,\mathrm{d}x+\left(x^2-x\right)\,\mathrm{d}x=\int_0^2\left(3x^2-x\right)\,\mathrm{d}x=6.
$$

故原积分 $=\frac56+6=\frac{41}{6}$. $\blacksquare$

### 习题三

（习题 9.2-3）应用格林公式计算下列积分:
(1) $\displaystyle\oint_{L^+}\left(xy^2+y^3\right)\,\mathrm{d}y-\left(x^3+x^2y\right)\,\mathrm{d}x$, 其中 $L^+$ 为圆周 $x^2+y^2=R^2$, 沿逆时针方向;

(2) $\displaystyle\oint_{L^+}\sqrt{x^2+y^2}\,\mathrm{d}x+y\left[xy+\ln\left(x+\sqrt{x^2+y^2}\right)\right]\mathrm{d}y$, 其中 $L^+$ 为以 $A\left(1,1\right)$、$B\left(2,2\right)$ 和 $C\left(1,3\right)$ 为顶点之三角形, 方向为逆时针;

(3) $\displaystyle\oint_{L^+}\left(e^x\sin y+\sin x-8y\right)\,\mathrm{d}x+\left(e^x\cos y-\sin y\right)\,\mathrm{d}y$, 其中 $L^+$ 为上半圆 $0\le y\le\sqrt{ax-x^2}$ ($0\le x\le a$) 之边界, 方向为逆时针.

### 解答 习题三

（1）$P=-\left(x^3+x^2y\right)$, $Q=xy^2+y^3$. 由**定理 2.2**,

$$
\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=y^2+x^2+2xy.
$$

圆域 $D$ 关于 $x=0,y=0$ 对称, $\iint_D xy\,\mathrm{d}x\mathrm{d}y=0$. 用极坐标,

$$
\oint_{L^+}=\iint_D\left(x^2+y^2\right)\,\mathrm{d}x\mathrm{d}y=\int_0^{2\pi}\mathrm{d}\theta\int_0^R r^2\cdot r\,\mathrm{d}r=2\pi\cdot\frac{R^4}{4}=\frac{\pi R^4}{2}.
$$

（2）$P=\sqrt{x^2+y^2}$, $Q=y\left[xy+\ln\left(x+\sqrt{x^2+y^2}\right)\right]$. 计算:

$$
\frac{\partial P}{\partial y}=\frac{y}{\sqrt{x^2+y^2}},\ \frac{\partial Q}{\partial x}=y^2+\frac{y}{\sqrt{x^2+y^2}}.
$$

故 $\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=y^2$. 三角形区域 $D$: $1\le x\le2$, $x\le y\le4-x$. 由**定理 2.2**,

$$
\oint_{L^+}=\int_1^2\mathrm{d}x\int_x^{4-x}y^2\,\mathrm{d}y=\frac13\int_1^2\left[\left(4-x\right)^3-x^3\right]\mathrm{d}x=\frac{25}{6}.
$$

（3）$P=e^x\sin y+\sin x-8y$, $Q=e^x\cos y-\sin y$. 计算:

$$
\frac{\partial Q}{\partial x}=e^x\cos y,\ \frac{\partial P}{\partial y}=e^x\cos y-8.
$$

故 $\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=8$. 上半圆 $y=\sqrt{ax-x^2}$ 的半径为 $a/2$, 面积为 $\pi a^2/8$. 由**定理 2.2**,

$$
\oint_{L^+}=8\cdot\frac{\pi a^2}{8}=\pi a^2.
$$

$\blacksquare$

### 习题四

（习题 9.2-4）设 $L$ 为平面上一条逐段光滑的简单闭曲线. 又设 $v=f\left(u\right)$ 为 $\left(-\infty,+\infty\right)$ 上的可微函数, 且 $f'\left(u\right)$ 连续. 证明 $\displaystyle\oint_{L^+}f\left(xy\right)\left(y\,\mathrm{d}x+x\,\mathrm{d}y\right)=0$.

### 解答 习题四

这里 $P=yf\left(xy\right)$, $Q=xf\left(xy\right)$. 计算偏导数:

$$
\frac{\partial P}{\partial y}=f\left(xy\right)+xyf'\left(xy\right),\ \frac{\partial Q}{\partial x}=f\left(xy\right)+xyf'\left(xy\right).
$$

故 $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$ 在 $L$ 所围区域 $D$ 内处处成立. 由**定理 2.2**（格林公式）,

$$
\oint_{L^+}f\left(xy\right)\left(y\,\mathrm{d}x+x\,\mathrm{d}y\right)=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y=0.
$$

$\blacksquare$

### 习题五

（习题 9.2-5-3）$\displaystyle\int_{\left(0,0\right)}^{\left(a,b\right)}e^x\cos y\,\mathrm{d}x-e^x\sin y\,\mathrm{d}y$.

### 解答 习题五

这里 $P=e^x\cos y$, $Q=-e^x\sin y$. 在全平面上单连通, 且

$$
\frac{\partial P}{\partial y}=-e^x\sin y=\frac{\partial Q}{\partial x}.
$$

由**定理 2.4**（积分与路径无关的条件）, 该积分与路径无关. 又注意到

$$
\mathrm{d}\left(e^x\cos y\right)=e^x\cos y\,\mathrm{d}x-e^x\sin y\,\mathrm{d}y,
$$

即被积表达式是恰当微分形式, $u=e^x\cos y$ 为原函数. 由**定理 2.5**,

$$
\int_{\left(0,0\right)}^{\left(a,b\right)}e^x\cos y\,\mathrm{d}x-e^x\sin y\,\mathrm{d}y=\left.e^x\cos y\right|_{\left(0,0\right)}^{\left(a,b\right)}=e^a\cos b-1.
$$

$\blacksquare$

### 习题六

（习题 9.2-6）设 $A>0,B>0$ 为常数. 又设 $L_r$ 为椭圆 $A^2x^2+B^2y^2=r^2$ ($r>0$). 试证明 $\displaystyle\oint_{L_r^+}\frac{x\,\mathrm{d}y-y\,\mathrm{d}x}{A^2x^2+B^2y^2}=\frac{2\pi}{AB}$, 其中 $L_r^+$ 表示积分沿 $L_r$ 的逆时针方向进行.

### 解答 习题六

在 $L_r$ 上, $A^2x^2+B^2y^2=r^2$, 故分母为常数 $r^2$. 于是

$$
\oint_{L_r^+}\frac{x\,\mathrm{d}y-y\,\mathrm{d}x}{A^2x^2+B^2y^2}=\frac1{r^2}\oint_{L_r^+}x\,\mathrm{d}y-y\,\mathrm{d}x.
$$

由**定理 2.2**（格林公式）的推论, $\oint_{L_r^+}x\,\mathrm{d}y-y\,\mathrm{d}x=2m\left(D\right)$, 其中 $m\left(D\right)$ 为椭圆 $A^2x^2+B^2y^2=r^2$ 的面积. 该椭圆半轴长为 $r/A$ 与 $r/B$, 故 $m\left(D\right)=\pi\cdot\frac rA\cdot\frac rB=\frac{\pi r^2}{AB}$. 因此

$$
\oint_{L_r^+}\frac{x\,\mathrm{d}y-y\,\mathrm{d}x}{A^2x^2+B^2y^2}=\frac1{r^2}\cdot\frac{2\pi r^2}{AB}=\frac{2\pi}{AB}.
$$

$\blacksquare$

### 习题七

（习题 9.2-7）在上题假定下, 证明对于任意一条逐段光滑的简单闭曲线 $\Gamma$, 只要原点 $\left(0,0\right)$ 在 $\Gamma$ 的内部, 则 $\displaystyle\oint_{\Gamma^+}\frac{x\,\mathrm{d}y-y\,\mathrm{d}x}{A^2x^2+B^2y^2}=\frac{2\pi}{AB}$, 其中 $\Gamma^+$ 表示逆时针方向.

### 解答 习题七

记 $P=\frac{-y}{A^2x^2+B^2y^2}$, $Q=\frac{x}{A^2x^2+B^2y^2}$. 在 $\left(x,y\right)\ne\left(0,0\right)$ 处,

$$
\frac{\partial Q}{\partial x}=\frac{A^2y^2-B^2x^2}{\left(A^2x^2+B^2y^2\right)^2}=\frac{\partial P}{\partial y}.
$$

取充分小的 $r>0$, 使椭圆 $L_r$ 完全含于 $\Gamma$ 内部. 在 $\Gamma$ 与 $L_r$ 所夹的复连通区域上应用**定理 2.3**（复连通区域上的格林公式）, 外边界 $\Gamma$ 取正向, 内边界 $L_r$ 取顺时针方向. 由于区域内 $\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=0$, 得

$$
\oint_{\Gamma^+}P\,\mathrm{d}x+Q\,\mathrm{d}y-\oint_{L_r^+}P\,\mathrm{d}x+Q\,\mathrm{d}y=0,
$$

即 $\oint_{\Gamma^+}=\oint_{L_r^+}$. 由习题六的结果, $\oint_{L_r^+}=\frac{2\pi}{AB}$, 故原积分 $=\frac{2\pi}{AB}$. $\blacksquare$
