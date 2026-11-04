# week28

> **定理 1.2 (光滑曲线的弧长公式)**
> 
> 设空间曲线 $L$ 的参数方程为 $x=x\left(t\right)$, $y=y\left(t\right)$, $z=z\left(t\right)$ ($\alpha\le t\le\beta$), 且导数连续. 则弧长 $s=\int_\alpha^\beta\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm dt$.

> **定理 1.3 (第一型曲线积分的计算)**
> 
> $\int_L f\left(x,y,z\right)\,\mathrm ds=\int_\alpha^\beta f\left(x\left(t\right),y\left(t\right),z\left(t\right)\right)\sqrt{\left[x'\right]^2+\left[y'\right]^2+\left[z'\right]^2}\,\mathrm dt$.

> **定理 2.2 (格林公式)**
> 
> 设 $L$ 为逐段光滑的简单闭曲线, 所围区域为 $D$, $P,Q$ 在 $D$ 上有一阶连续偏导数. 则 $\oint_{L^+}P\,\mathrm dx+Q\,\mathrm dy=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm dx\mathrm dy$.

> **定理 2.4 (积分与路径无关的条件)**
> 
> 设 $D$ 为单连通域, $P,Q$ 在 $D$ 内有一阶连续偏导数. 则 $\int P\,\mathrm dx+Q\,\mathrm dy$ 与路径无关的充要条件是 $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$.

> **定理 2.5 (恰当微分形式)**
> 
> $P\,\mathrm dx+Q\,\mathrm dy$ 为恰当微分形式的充要条件是 $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$.

> **定理 4.2 (三重积分的穿线法)**
> 
> 设 $\Omega=\left\{\left(x,y,z\right):\left(x,y\right)\in D,z_1\left(x,y\right)\le z\le z_2\left(x,y\right)\right\}$. 则 $\iiint_\Omega f\,\mathrm dV=\iint_D\mathrm dx\mathrm dy\int_{z_1\left(x,y\right)}^{z_2\left(x,y\right)}f\,\mathrm dz$.

> **定理 4.4 (三重积分换元公式)**
> 
> $\iiint_\Omega f\,\mathrm dx\mathrm dy\mathrm dz=\iiint_{\Omega'}f\left(x\left(u,v,w\right),y\left(u,v,w\right),z\left(u,v,w\right)\right)\left|J\right|\,\mathrm du\mathrm dv\mathrm dw$. 柱坐标 $\left|J\right|=r$, 球坐标 $\left|J\right|=\rho^2\sin\varphi$.

> **命题 5.1 (曲面面积公式)**
> 
> 设 $z=f\left(x,y\right)$ 在 $D$ 上有连续一阶偏导数, 则曲面面积 $S=\iint_D\sqrt{1+f_x^2+f_y^2}\,\mathrm dx\mathrm dy$.

## 8.4-9

计算 $\iiint_\Omega\sqrt{x^2+y^2+z^2}\,\mathrm dV$, 其中 $\Omega$ 为球面 $x^2+y^2+z^2=x$ 内部.

### 解答 8.4-9

球面方程化为 $\rho=\sin\varphi\cos\theta$. 由**定理 4.4 (三重积分换元公式)**,

$$
\iiint_\Omega\sqrt{x^2+y^2+z^2}\,\mathrm dV=\frac\pi{10}.
$$

$\blacksquare$

## 8.4-10

计算 $\iiint_\Omega\left(x+1\right)\left(y+1\right)\,\mathrm dV$, 其中 $\Omega$ 为椭球体 $\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}\le1$.

### 解答 8.4-10

展开: $\left(x+1\right)\left(y+1\right)=xy+x+y+1$. 由对称性, 前三项积分为 $0$. 故

$$
\iiint_\Omega\left(x+1\right)\left(y+1\right)\,\mathrm dV=\iiint_\Omega 1\,\mathrm dV=\frac{4\pi abc}{3}.
$$

$\blacksquare$

## 8.5-1

求锥面 $z=\sqrt{x^2+y^2}$ 被柱面 $z^2=2x$ 所割下部分的面积.

### 解答 8.5-1

投影区域为圆域 $D=\left\{\left(x-1\right)^2+y^2\le1\right\}$. 由 $f=\sqrt{x^2+y^2}$ 得 $\sqrt{1+f_x^2+f_y^2}=\sqrt2$. 由**命题 5.1 (曲面面积公式)**,

$$
S=\sqrt2\cdot\pi.
$$

$\blacksquare$

## 8.5-2

求曲面 $az=xy$ 包围在圆柱 $x^2+y^2=a^2$ 内部的那部分面积.

### 解答 8.5-2

$z=xy/a$, $\sqrt{1+f_x^2+f_y^2}=\sqrt{1+\frac{x^2+y^2}{a^2}}$. 由**命题 5.1 (曲面面积公式)** 并用极坐标,

$$
S=\frac{2\pi a^2}{3}\left(2\sqrt2-1\right).
$$

$\blacksquare$

## 8.5-3

求第一卦限中均匀椭球体 $\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}\le1$ 的质心坐标.

### 解答 8.5-3

体积 $V=\frac{\pi abc}{6}$. 用广义球坐标, 由质心坐标公式,

$$
z_0=\frac{\iiint z\,\mathrm dV}{V}=\frac{3c}{8}.
$$

由对称性, $x_0=\frac{3a}{8}$, $y_0=\frac{3b}{8}$. 质心为 $\left(\frac{3a}{8},\frac{3b}{8},\frac{3c}{8}\right)$. $\blacksquare$

## 8.5-6

设立方体 $\Omega=\left[0,a\right]^3$, 密度为常数 $\rho$. 求对 $z$ 轴的转动惯量.

### 解答 8.5-6

由转动惯量公式,

$$
J_z=\rho\iiint_\Omega\left(x^2+y^2\right)\,\mathrm dV=\frac{2\rho a^5}{3}.
$$

$\blacksquare$

## 9.1-1

求旋轮线第一拱 $x=a\left(t-\sin t\right)$, $y=a\left(1-\cos t\right)$ ($0\le t\le2\pi$) 的弧长.

### 解答 9.1-1

$x'=a\left(1-\cos t\right)$, $y'=a\sin t$. 由**定理 1.2 (光滑曲线的弧长公式)**,

$$
\mathrm ds=2a\sin\frac t2\,\mathrm dt.
$$

故 $s=\int_0^{2\pi}2a\sin\frac t2\,\mathrm dt=8a$. $\blacksquare$

## 9.1-3

求阿基米德螺线 $x=at\cos t$, $y=at\sin t$ ($0\le t\le2\pi$) 的弧长.

### 解答 9.1-3

由**定理 1.2 (光滑曲线的弧长公式)**, $\mathrm ds=a\sqrt{1+t^2}\,\mathrm dt$. 故

$$
s=a\pi\sqrt{1+4\pi^2}+\frac a2\ln\left(2\pi+\sqrt{1+4\pi^2}\right).
$$

$\blacksquare$

## 9.1-4

求 $\oint_L xy\,\mathrm ds$, 其中 $L$ 为正方形 $\left|x\right|+\left|y\right|=a$.

### 解答 9.1-4

$L$ 关于 $x$ 轴对称, 而 $xy$ 关于 $y$ 为奇函数. 故对称两段上的积分互为相反数, 相互抵消.

$$
\oint_L xy\,\mathrm ds=0.
$$

$\blacksquare$

## 9.1-7

求 $\int_L xy\,\mathrm ds$, 其中 $L$ 为椭圆 $\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$ 在第一象限部分.

### 解答 9.1-7

取参数方程 $x=a\cos t$, $y=b\sin t$. 由**定理 1.3 (第一型曲线积分的计算)**,

$$
\int_L xy\,\mathrm ds=\frac{ab\left(a^2+ab+b^2\right)}{3\left(a+b\right)}.
$$

$\blacksquare$

## 9.1-8

求 $\int_L x^2\,\mathrm ds$, 其中 $L$ 为给定的空间曲线.

### 解答 9.1-8

计算弧微元得 $\mathrm ds=a\,\mathrm dt$. 由**定理 1.3 (第一型曲线积分的计算)**, 利用 $\int_0^{2\pi}\cos^2t\,\mathrm dt=\pi$, $\int_0^{2\pi}\sin t\cos t\,\mathrm dt=0$, 得

$$
\int_L x^2\,\mathrm ds=\frac{2\pi a^3}{3}.
$$

$\blacksquare$

## 9.2-1

求 $\oint_{L^+}x^2\,\mathrm dy-y^2\,\mathrm dx$, 其中 $L$ 为椭圆周.

### 解答 9.2-1

由**定理 2.2 (格林公式)**, 原式 $=\iint_D\left(2x+2y\right)\,\mathrm dx\mathrm dy$. 由对称性, 积分为 $0$. $\blacksquare$

## 9.2-2

求 $\int_L\left(x^2+y^2\right)\,\mathrm dx+\left(x^2-y\right)\,\mathrm dy$, 其中 $L$ 为 $y=\left|x\right|$ 上从 $\left(-1,1\right)$ 到 $\left(2,2\right)$ 的弧.

### 解答 9.2-2

分段计算: $L_1$ 上 $=\frac56$, $L_2$ 上 $=6$. 故原式 $=\frac{41}{6}$. $\blacksquare$

## 9.2-3

应用格林公式计算:

(1) $\oint_{L^+}\left(xy^2+y^3\right)\,\mathrm dy-\left(x^3+x^2y\right)\,\mathrm dx$, $L$ 为圆周;

(2) $\oint_{L^+}\sqrt{x^2+y^2}\,\mathrm dx+y\left[xy+\ln\left(x+\sqrt{x^2+y^2}\right)\right]\mathrm dy$, $L$ 为三角形;

(3) $\oint_{L^+}\left(e^x\sin y+\sin x-8y\right)\,\mathrm dx+\left(e^x\cos y-\sin y\right)\,\mathrm dy$, $L$ 为上半圆边界.

### 解答 9.2-3

(1) 由**定理 2.2 (格林公式)**, $=\iint_D\left(x^2+y^2\right)=\frac{\pi R^4}{2}$.

(2) $\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=y^2$. $=\frac{25}{6}$.

(3) $\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=8$. $=8\cdot\frac{\pi a^2}{8}=\pi a^2$. $\blacksquare$

## 9.2-4

证明: $\oint_{L^+}f\left(xy\right)\left(y\,\mathrm dx+x\,\mathrm dy\right)=0$.

### 解答 9.2-4

$P=yf\left(xy\right)$, $Q=xf\left(xy\right)$. 计算得 $\frac{\partial P}{\partial y}=\frac{\partial Q}{\partial x}=f\left(xy\right)+xyf'\left(xy\right)$. 由**定理 2.2 (格林公式)**, 原式 $=0$. $\blacksquare$
