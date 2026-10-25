# 作业 36

> **定理 4.1**（奥-高公式）设空间曲面 $S$ 是分片光滑的封闭曲面, 所围空间闭区域为 $\Omega$, $P,Q,R$ 在 $\Omega$ 中有一阶连续偏导数. 则

$$
\oiint_{S^+}P\,\mathrm{d}y\mathrm{d}z+Q\,\mathrm{d}z\mathrm{d}x+R\,\mathrm{d}x\mathrm{d}y=\iiint_\Omega\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)\mathrm{d}V,
$$

其中 $S^+$ 表示外侧.

> **定理 4.2**（斯托克斯公式）设 $S$ 为分片光滑的双侧曲面, 边界 $L$ 为分段光滑闭曲线, $L$ 的定向与 $S$ 的法向量构成右手系. 则

$$
\oint_{L^+}P\,\mathrm{d}x+Q\,\mathrm{d}y+R\,\mathrm{d}z=\iint_{S^+}\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z}\right)\mathrm{d}y\mathrm{d}z+\left(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}\right)\mathrm{d}z\mathrm{d}x+\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y.
$$

### 习题一

（习题 9.4-1）求

$$
\displaystyle\oiint_{S^+}xz^2\,\mathrm{d}y\mathrm{d}z+\left(x^2y-z^3\right)\,\mathrm{d}z\mathrm{d}x+\left(2xy+y^2z\right)\,\mathrm{d}x\mathrm{d}y,
$$

其中 $S^+$ 是 $z=\sqrt{a^2-x^2-y^2}$ 和 $z=0$ 所围的半球区域的全表面的外侧.

### 解答 习题一

这里 $P=xz^2$, $Q=x^2y-z^3$, $R=2xy+y^2z$. 由**定理 4.1**（奥-高公式）,

$$
\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}=z^2+x^2+y^2.
$$

$\Omega$ 为上半球 $x^2+y^2+z^2\le a^2$, $z\ge0$. 用球坐标:

$$
I=\int_0^{2\pi}\mathrm{d}\theta\int_0^{\pi/2}\mathrm{d}\varphi\int_0^a r^2\cdot r^2\sin\varphi\,\mathrm{d}r=2\pi\cdot\frac{a^5}{5}=\frac{2\pi a^5}{5}.

$$

$\blacksquare$
### 习题二

（习题 9.4-3）求

$$
\displaystyle\oiint_{S^+}x^3\,\mathrm{d}y\mathrm{d}z+y^3\,\mathrm{d}z\mathrm{d}x+z^3\,\mathrm{d}x\mathrm{d}y,
$$

$S^+$ 为球面 $x^2+y^2+z^2=a^2$ 的外侧.

### 解答 习题二

由**定理 4.1**（奥-高公式）,

$$
I=\iiint_\Omega 3\left(x^2+y^2+z^2\right)\,\mathrm{d}V.
$$

球坐标下:

$$
I=3\int_0^{2\pi}\mathrm{d}\theta\int_0^\pi\mathrm{d}\varphi\int_0^a r^2\cdot r^2\sin\varphi\,\mathrm{d}r=3\cdot4\pi\cdot\frac{a^5}{5}=\frac{12\pi a^5}{5}.

$$

$\blacksquare$
### 习题三

（习题 9.4-5）求 $\displaystyle\oiint_{S^+}\boldsymbol{F}\cdot\boldsymbol{n}\,\mathrm{d}S$, 其中 $\boldsymbol{F}=\left(x^4,y^4,z^4\right)$, $S^+$ 是锥面 $x^2+y^2=z^2$ 在 $0\le z\le h$ 部分的外侧.

### 解答 习题三

$S$ 仅为锥面侧面, 不封闭. 补上顶面 $S_1$: $z=h$, $x^2+y^2\le h^2$, 取上侧. 由**定理 4.1**,

$$
\oiint_{S\cup S_1}\boldsymbol{F}\cdot\boldsymbol{n}\,\mathrm{d}S=\iiint_\Omega 4\left(x^3+y^3+z^3\right)\,\mathrm{d}V.
$$

由对称性 $\iiint_\Omega x^3=\iiint_\Omega y^3=0$. 锥域 $\Omega$: $x^2+y^2\le z^2$, $0\le z\le h$, 故

$$
\iiint_\Omega z^3\,\mathrm{d}V=\int_0^h z^3\cdot\pi z^2\,\mathrm{d}z=\frac{\pi h^6}{6}.
$$

因此三重积分 $=4\cdot\frac{\pi h^6}{6}=\frac{2\pi h^6}{3}$. 在 $S_1$ 上, $\boldsymbol{F}\cdot\boldsymbol{n}=z^4=h^4$,

$$
\iint_{S_1}h^4\,\mathrm{d}x\mathrm{d}y=h^4\cdot\pi h^2=\pi h^6.
$$

故

$$
\oiint_{S^+}\boldsymbol{F}\cdot\boldsymbol{n}\,\mathrm{d}S=\frac{2\pi h^6}{3}-\pi h^6=-\frac{\pi h^6}{3}.

$$

$\blacksquare$
### 习题四

（习题 9.4-7）$\displaystyle\oint_{L^+}y^2\,\mathrm{d}x+xy\,\mathrm{d}y+xz\,\mathrm{d}z$, 其中 $L$ 是圆柱面 $x^2+y^2=2y$ 与平面 $y=z$ 的交线, 逆时针方向.

### 解答 习题四

$P=y^2$, $Q=xy$, $R=xz$. 旋度

$$
\nabla\times\boldsymbol{F}=\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z},\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x},\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)=\left(0,-z,-y\right).
$$

取曲面 $S$ 为平面 $y=z$ 上被 $L$ 围成的区域, 投影 $D$: $x^2+y^2\le2y$. $z=y$, $z_x=0$, $z_y=1$. 由**定理 4.2**（斯托克斯公式）,

$$
\oint_{L^+}=\iint_D\left[0\cdot\left(-z_x\right)+\left(-z\right)\left(-z_y\right)+\left(-y\right)\right]\mathrm{d}x\mathrm{d}y=\iint_D\left(z-y\right)\,\mathrm{d}x\mathrm{d}y=0.

$$

$\blacksquare$
### 习题五

（习题 9.4-8）

$$
\displaystyle\oint_{L^+}\left(y^2+z^2-x^2\right)\,\mathrm{d}x+\left(x^2+z^2-y^2\right)\,\mathrm{d}y+\left(x^2+y^2-z^2\right)\,\mathrm{d}z,
$$

其中 $L$ 为球面 $z=\sqrt{2Rx-x^2-y^2}$ 与柱面 $x^2+y^2=2rx$ ($0< r< R$, $z\ge0$) 的交线, $L^+$ 与球面上侧成右手系.

### 解答 习题五

$P=y^2+z^2-x^2$, $Q=x^2+z^2-y^2$, $R=x^2+y^2-z^2$. 旋度

$$
\nabla\times\boldsymbol{F}=2\left(y-z,z-x,x-y\right).
$$

曲面 $S$ 为上半球面 $z=\sqrt{2Rx-x^2-y^2}$, 投影 $D$: $x^2+y^2\le2rx$. $z_x=\frac{R-x}{z}$, $z_y=-\frac yz$. 由**定理 4.2**（斯托克斯公式）, 上侧:

$$
\oint_{L^+}=\iint_D 2\left[\left(y-z\right)\frac{-\left(R-x\right)}{z}+\left(z-x\right)\frac yz+\left(x-y\right)\right]\mathrm{d}x\mathrm{d}y.
$$

化简括号内:

$$
\frac{\left(y-z\right)\left(x-R\right)+y\left(z-x\right)}{z}+x-y=\frac{-yR-zx+zR+yz}{z}+x-y=R-\frac{Ry}{z}.
$$

故

$$
\oint_{L^+}=2\iint_D\left(R-\frac{Ry}{z}\right)\mathrm{d}x\mathrm{d}y.
$$

$D$ 关于 $x$ 轴对称, $y/z$ 关于 $y$ 为奇函数, 第二项为 $0$. $m\left(D\right)=\pi r^2$. 因此

$$
\oint_{L^+}=2R\cdot\pi r^2=2\pi Rr^2.

$$

$\blacksquare$