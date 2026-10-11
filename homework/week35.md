# 作业 35

> **公式**（第一型曲面积分的计算）设光滑曲面 $S$ 由参数方程 $x=x\left(u,v\right)$, $y=y\left(u,v\right)$, $z=z\left(u,v\right)$ ($\left(u,v\right)\in D$) 给出, $E=x_u^2+y_u^2+z_u^2$, $F=x_ux_v+y_uy_v+z_uz_v$, $G=x_v^2+y_v^2+z_v^2$. 则

$$
\iint_S f\left(x,y,z\right)\,\mathrm{d}S=\iint_D f\bigl(x\left(u,v\right),y\left(u,v\right),z\left(u,v\right)\bigr)\sqrt{EG-F^2}\,\mathrm{d}u\mathrm{d}v.
$$

特别地, 当曲面由 $z=g\left(x,y\right)$ ($\left(x,y\right)\in D$) 给出时, $\mathrm{d}S=\sqrt{1+g_x^2+g_y^2}\,\mathrm{d}x\mathrm{d}y$.

> **公式**（第二型曲面积分的计算）设曲面 $S:z=g\left(x,y\right)$ ($\left(x,y\right)\in D$), 取上侧. 则

$$
\iint_S P\,\mathrm{d}y\mathrm{d}z+Q\,\mathrm{d}z\mathrm{d}x+R\,\mathrm{d}x\mathrm{d}y=\iint_D\left[P\left(-g_x\right)+Q\left(-g_y\right)+R\right]\mathrm{d}x\mathrm{d}y.
$$

下侧时取负号.

### 习题一

（习题 9.3-1）求 $\displaystyle\iint_S\left(y+x\right)\,\mathrm{d}S$, 其中 $S$ 为立方体 $V=\left\{\left(x,y,z\right):0\le x\le1,\ 0\le y\le1,\ 0\le z\le1\right\}$ 的表面.

### 解答 习题一

由对称性, $\iint_S x\,\mathrm{d}S=\iint_S y\,\mathrm{d}S$. 分别计算六个面上的 $\iint_S x\,\mathrm{d}S$:

$x=0$ 面: $x=0$, 积分 $=0$; $x=1$ 面: $\iint 1\,\mathrm{d}y\mathrm{d}z=1$; $y=0$ 面: $\iint x\,\mathrm{d}x\mathrm{d}z=\dfrac12$; $y=1$ 面: $\dfrac12$; $z=0$ 面: $\dfrac12$; $z=1$ 面: $\dfrac12$.

故 $\iint_S x\,\mathrm{d}S=0+1+\dfrac12+\dfrac12+\dfrac12+\dfrac12=3$. 因此

$$
\iint_S\left(y+x\right)\,\mathrm{d}S=2\iint_S x\,\mathrm{d}S=6.
$$

$\blacksquare$

### 习题二

（习题 9.3-3）求 $\displaystyle\oiint_S\left(xy+z\right)^2\,\mathrm{d}S$, 其中 $S$ 为球面 $x^2+y^2+z^2=R^2$.

### 解答 习题二

展开 $\left(xy+z\right)^2=x^2y^2+2xyz+z^2$. 由球面关于各坐标面对称, $2xyz$ 关于 $x$ (或 $y$, $z$) 为奇函数, 故 $\oiint_S 2xyz\,\mathrm{d}S=0$.

由对称性, $\oiint_S x^2\,\mathrm{d}S=\oiint_S y^2\,\mathrm{d}S=\oiint_S z^2\,\mathrm{d}S$, 且三者之和为 $\oiint_S\left(x^2+y^2+z^2\right)\,\mathrm{d}S=R^2\cdot4\pi R^2=4\pi R^4$. 故 $\oiint_S z^2\,\mathrm{d}S=\dfrac{4\pi R^4}{3}$.

同理, $\oiint_S x^2y^2=\oiint_S y^2z^2=\oiint_S z^2x^2$. 利用 $\left(x^2+y^2+z^2\right)^2=x^4+y^4+z^4+2\left(x^2y^2+y^2z^2+z^2x^2\right)$, 并由对称性 $\oiint_S x^4=\oiint_S y^4=\oiint_S z^4$, 而 $\oiint_S x^4\,\mathrm{d}S=\dfrac{4\pi R^6}{5}$ (球坐标直接计算). 于是

$$
2\cdot3\oiint_S x^2y^2\,\mathrm{d}S=4\pi R^6-3\cdot\frac{4\pi R^6}{5}=\frac{8\pi R^6}{5},
$$

即 $\oiint_S x^2y^2\,\mathrm{d}S=\dfrac{4\pi R^6}{15}$. 故

$$
\oiint_S\left(xy+z\right)^2\,\mathrm{d}S=\frac{4\pi R^6}{15}+\frac{4\pi R^4}{3}.
$$

$\blacksquare$

### 习题三

（习题 9.3-5）求抛物面薄壳 $z=\dfrac12\left(x^2+y^2\right)$ ($0\le z\le1$) 的质量, 假定已知其面密度为 $\rho=x+y+z$.

### 解答 习题三

曲面 $z=\dfrac12\left(x^2+y^2\right)$, 投影区域 $D=\left\{\left(x,y\right):x^2+y^2\le2\right\}$. $z_x=x$, $z_y=y$, 由**公式**（第一型曲面积分的计算）,

$$
\mathrm{d}S=\sqrt{1+x^2+y^2}\,\mathrm{d}x\mathrm{d}y.
$$

质量 $M=\iint_D\left(x+y+\tfrac12\left(x^2+y^2\right)\right)\sqrt{1+x^2+y^2}\,\mathrm{d}x\mathrm{d}y$. 由对称性, $\iint_D x=\iint_D y=0$. 用极坐标,

$$
M=\int_0^{2\pi}\mathrm{d}\theta\int_0^{\sqrt2}\frac{r^2}{2}\sqrt{1+r^2}\,r\,\mathrm{d}r=\pi\int_0^{\sqrt2}r^3\sqrt{1+r^2}\,\mathrm{d}r.
$$

令 $u=1+r^2$, $\mathrm{d}u=2r\,\mathrm{d}r$, $r^2=u-1$, 得

$$
M=\frac\pi2\int_1^3\left(u-1\right)\sqrt u\,\mathrm{d}u=\frac\pi2\left[\frac25u^{5/2}-\frac23u^{3/2}\right]_1^3=\frac{\pi\left(12\sqrt3+2\right)}{15}.
$$

$\blacksquare$

### 习题四

（习题 9.3-6）设 $S$ 是位于第一卦限的球面 $x^2+y^2+z^2=a^2$ ($x\ge0,y\ge0,z\ge0$), 又假定该球面薄壳的面密度为常数, 求其质心坐标.

### 解答 习题四

由对称性, 质心 $\left(\bar x,\bar y,\bar z\right)$ 满足 $\bar x=\bar y=\bar z$. 曲面面积 $=\dfrac18\cdot4\pi a^2=\dfrac{\pi a^2}{2}$.

用球坐标 $x=a\sin\varphi\cos\theta$, $y=a\sin\varphi\sin\theta$, $z=a\cos\varphi$, 第一卦限 $0\le\varphi\le\pi/2$, $0\le\theta\le\pi/2$, $\mathrm{d}S=a^2\sin\varphi\,\mathrm{d}\varphi\mathrm{d}\theta$. 则

$$
\iint_S z\,\mathrm{d}S=\int_0^{\pi/2}\mathrm{d}\theta\int_0^{\pi/2}a\cos\varphi\cdot a^2\sin\varphi\,\mathrm{d}\varphi=\frac\pi2\cdot\frac{a^3}{2}=\frac{\pi a^3}{4}.
$$

故 $\bar z=\dfrac{\pi a^3/4}{\pi a^2/2}=\dfrac a2$. 质心为 $\left(\dfrac a2,\dfrac a2,\dfrac a2\right)$. $\blacksquare$

### 习题五

（习题 9.3-7）$I=\displaystyle\iint_S y\left(x-z\right)\,\mathrm{d}y\mathrm{d}z+x^2\,\mathrm{d}z\mathrm{d}x+\left(y^2+zx\right)\,\mathrm{d}x\mathrm{d}y$, 其中 $S$ 是立方体 $V=\left\{\left(x,y,z\right):0\le x\le a,\ 0\le y\le a,\ 0\le z\le a\right\}$ 之表面的外侧.

### 解答 习题五

这里 $P=y\left(x-z\right)$, $Q=x^2$, $R=y^2+zx$. 由下一节**定理 4.1**（奥-高公式）,

$$
I=\iiint_\Omega\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)\mathrm{d}V=\iiint_\Omega\left(y+0+x\right)\,\mathrm{d}V.
$$

$\Omega=\left[0,a\right]^3$. 故

$$
I=\int_0^a\mathrm{d}x\int_0^a\mathrm{d}y\int_0^a\left(x+y\right)\,\mathrm{d}z=a\cdot\left(\frac{a^3}{2}+\frac{a^3}{2}\right)=a^4.
$$

$\blacksquare$

### 习题六

（习题 9.3-8）$I=\displaystyle\iint_S\left(y-z\right)x\,\mathrm{d}y\mathrm{d}z+\left(x-y\right)\,\mathrm{d}x\mathrm{d}y$, 其中 $S$ 为柱面 $x^2+y^2=1$ 与平面 $z=0$ 及 $z=3$ 所围空间区域之表面的外侧.

### 解答 习题六

这里 $P=x\left(y-z\right)$, $Q=0$, $R=x-y$. 由**定理 4.1**（奥-高公式）,

$$
I=\iiint_\Omega\frac{\partial P}{\partial x}\,\mathrm{d}V=\iiint_\Omega\left(y-z\right)\,\mathrm{d}V.
$$

$\Omega$ 为圆柱 $x^2+y^2\le1$, $0\le z\le3$. 用柱坐标:

$$
I=\int_0^3\mathrm{d}z\int_0^{2\pi}\mathrm{d}\theta\int_0^1\left(r\sin\theta-z\right)r\,\mathrm{d}r.
$$

$\int_0^{2\pi}\sin\theta\,\mathrm{d}\theta=0$, 故第一项为 $0$. 第二项: $\int_0^{2\pi}\left(-z\right)\cdot\dfrac12\,\mathrm{d}\theta=-\pi z$. 因此

$$
I=\int_0^3\left(-\pi z\right)\,\mathrm{d}z=-\frac{9\pi}{2}.
$$

$\blacksquare$

### 习题七

（习题 9.3-9）$I=\displaystyle\iint_S\left(y-z\right)\,\mathrm{d}y\mathrm{d}z+\left(z-x\right)\,\mathrm{d}z\mathrm{d}x+\left(x-y\right)\,\mathrm{d}x\mathrm{d}y$, 其中 $S$ 是上半球面 $x^2+y^2+z^2=2Rx$ ($z\ge0$) 被柱面 $x^2+y^2=2rx$ ($0<r<R$) 所截部分的上侧.

### 解答 习题七

$S$ 可表为 $z=\sqrt{2Rx-x^2-y^2}$, 投影区域 $D=\left\{\left(x,y\right):x^2+y^2\le2rx\right\}$. 由**公式**（第二型曲面积分的计算）, 上侧:

$$
z_x=\frac{R-x}{z},\  z_y=-\frac yz.
$$

被积表达式为 $P\left(-z_x\right)+Q\left(-z_y\right)+R$, 其中 $P=y-z$, $Q=z-x$, $R=x-y$. 代入并化简分子:

$$
\left(y-z\right)\left(x-R\right)+y\left(z-x\right)=xy-yR-zx+zR+yz-xy=-yR-zx+zR+yz.
$$

除以 $z$ 得 $-\dfrac{yR}{z}-x+R+y$, 再加 $x-y$ 得 $R-\dfrac{Ry}{z}$.

故

$$
I=\iint_D\left(R-\frac{Ry}{z}\right)\mathrm{d}x\mathrm{d}y=R\cdot m\left(D\right)-R\iint_D\frac{y}{z}\,\mathrm{d}x\mathrm{d}y.
$$

$D$ 关于 $x$ 轴对称, $y/z$ 关于 $y$ 为奇函数, 故第二项为 $0$. $m\left(D\right)=\pi r^2$. 因此 $I=\pi Rr^2$. $\blacksquare$

### 习题八

（习题 9.3-10）$I=\displaystyle\iint_S x\,\mathrm{d}y\mathrm{d}z+y\,\mathrm{d}z\mathrm{d}x+z\,\mathrm{d}x\mathrm{d}y$, 其中 $S$ 为椭球面 $\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}+\dfrac{z^2}{c^2}=1$ ($a>0,b>0,c>0$) 的外侧.

### 解答 习题八

这里 $P=x$, $Q=y$, $R=z$. 由**定理 4.1**（奥-高公式）,

$$
I=\iiint_\Omega\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)\mathrm{d}V=3\iiint_\Omega\mathrm{d}V.
$$

椭球体体积为 $\dfrac{4\pi abc}{3}$, 故 $I=3\cdot\dfrac{4\pi abc}{3}=4\pi abc$. $\blacksquare$
