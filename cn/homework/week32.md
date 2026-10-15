# 作业 32

> **命题 5.1**（曲面面积公式）设 $z=f\left(x,y\right)$ 在可求面积的有界闭区域 $D$ 上有连续的一阶偏导数, 则曲面 $z=f\left(x,y\right)$ ($\left(x,y\right)\in D$) 的面积为

$$
S=\iint_D\sqrt{1+f_x^2\left(x,y\right)+f_y^2\left(x,y\right)}\,\mathrm{d}x\mathrm{d}y.
$$

> **公式**（质心坐标）设物体占据区域 $\Omega$, 密度为 $\rho\left(x,y,z\right)$, 质量 $m=\iiint_\Omega\rho\,\mathrm{d}V$, 则质心坐标为

$$
x_0=\frac1m\iiint_\Omega x\rho\,\mathrm{d}V, y_0=\frac1m\iiint_\Omega y\rho\,\mathrm{d}V, z_0=\frac1m\iiint_\Omega z\rho\,\mathrm{d}V.
$$

> **公式**（转动惯量）物体关于 $z$ 轴的转动惯量为

$$
J_z=\iiint_\Omega\left(x^2+y^2\right)\rho\left(x,y,z\right)\,\mathrm{d}V.
$$

### 习题一

（习题 8.5-1）求锥面 $z=\sqrt{x^2+y^2}$ 被柱面 $z^2=2x$ 所割下部分的面积.

### 解答 习题一

锥面方程 $z=\sqrt{x^2+y^2}$ 即 $z=r$. 由 $z^2=2x$ 得 $r^2=2r\cos\theta$, 即 $r=2\cos\theta$ ($r\ge0$, $\theta\in\left[-\pi/2,\pi/2\right]$). 故所割部分在 $Oxy$ 平面上的投影为圆域

$$
D=\left\{\left(x,y\right):\left(x-1\right)^2+y^2\le1\right\},
$$

其面积为 $\pi$.

由 $f\left(x,y\right)=\sqrt{x^2+y^2}$ 得 $f_x=x/\sqrt{x^2+y^2}$, $f_y=y/\sqrt{x^2+y^2}$, 从而

$$
\sqrt{1+f_x^2+f_y^2}=\sqrt{1+\frac{x^2+y^2}{x^2+y^2}}=\sqrt2.
$$

由**命题 5.1**（曲面面积公式）,

$$
S=\iint_D\sqrt2\,\mathrm{d}x\mathrm{d}y=\sqrt2\cdot\pi=\sqrt2\,\pi.

$$

$\blacksquare$
### 习题二

（习题 8.5-2）求曲面 $az=xy$ 包围在圆柱 $x^2+y^2=a^2$ 内部的那部分的面积.

### 解答 习题二

曲面方程 $z=xy/a$, 故 $f_x=y/a$, $f_y=x/a$, 从而

$$
\sqrt{1+f_x^2+f_y^2}=\sqrt{1+\frac{x^2+y^2}{a^2}}.
$$

投影区域为

$$
D=\left\{\left(x,y\right):x^2+y^2\le a^2\right\}.
$$

由**命题 5.1**（曲面面积公式）并用极坐标,

$$
\begin{aligned}S&=\iint_D\sqrt{1+\frac{x^2+y^2}{a^2}}\,\mathrm{d}x\mathrm{d}y\\&=\int_0^{2\pi}\mathrm{d}\theta\int_0^a\sqrt{1+\frac{r^2}{a^2}}\,r\,\mathrm{d}r.\end{aligned}
$$

令 $u=1+r^2/a^2$, $\mathrm{d}u=2r\,\mathrm{d}r/a^2$, 得

$$
S=2\pi\cdot\frac{a^2}{2}\int_1^2\sqrt u\,\mathrm{d}u=\pi a^2\cdot\frac23\left(2\sqrt2-1\right)=\frac{2\pi a^2}{3}\left(2\sqrt2-1\right).

$$

$\blacksquare$
### 习题三

（习题 8.5-3）求位于第一卦限中的部分椭球体 $\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}\le1$ ($a>0,b>0,c>0$) 的质心坐标. 这里我们假定椭球体密度是均匀的.

### 解答 习题三

设密度 $\rho$ 为常数. 第一卦限椭球体体积为 $V=\frac18\cdot\frac{4\pi abc}{3}=\frac{\pi abc}{6}$.

作广义球坐标变换 $x=a\rho\sin\varphi\cos\theta$, $y=b\rho\sin\varphi\sin\theta$, $z=c\rho\cos\varphi$, 雅可比行列式 $\left| J\right|=abc\rho^2\sin\varphi$. 第一卦限对应 $0\le\rho\le1$, $0\le\varphi\le\pi/2$, $0\le\theta\le\pi/2$. 由**公式**（质心坐标）,

$$
\begin{aligned}\iiint_\Omega z\,\mathrm{d}V&=\int_0^{\pi/2}\mathrm{d}\theta\int_0^{\pi/2}\mathrm{d}\varphi\int_0^1 c\rho\cos\varphi\cdot abc\rho^2\sin\varphi\,\mathrm{d}\rho\\&=abc^2\cdot\frac\pi2\cdot\frac12\cdot\frac14=\frac{\pi abc^2}{16}.\end{aligned}
$$

故

$$
z_0=\frac{\pi abc^2/16}{\pi abc/6}=\frac{3c}{8}.
$$

由对称性 (将 $a,x,\theta$ 与 $b,y,\theta+\pi/2$ 互换), 同理得 $x_0=\frac{3a}{8}$, $y_0=\frac{3b}{8}$. 即质心为 $\left(\frac{3a}{8},\frac{3b}{8},\frac{3c}{8}\right)$. $\blacksquare$

### 习题四

（习题 8.5-6）设 $\Omega$ 为一立方体:

$$
\Omega=\left\{\left(x,y,z\right):0\le x\le a,0\le y\le a,0\le z\le a\right\}.
$$

假定它的密度为常数 $\rho$. 求 $\Omega$ 对 $z$ 轴的转动惯量.

### 解答 习题四

由**公式**（转动惯量）,

$$
\begin{aligned}J_z&=\iiint_\Omega\left(x^2+y^2\right)\rho\,\mathrm{d}V\\&=\rho\int_0^a\mathrm{d}x\int_0^a\mathrm{d}y\int_0^a\left(x^2+y^2\right)\,\mathrm{d}z\\&=\rho a\left(\int_0^a x^2\mathrm{d}x\int_0^a\mathrm{d}y+\int_0^a\mathrm{d}x\int_0^a y^2\mathrm{d}y\right)\\&=\rho a\left(\frac{a^4}{3}+\frac{a^4}{3}\right)=\frac{2\rho a^5}{3}.\end{aligned}

$$

$\blacksquare$