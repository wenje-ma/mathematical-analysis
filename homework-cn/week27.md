# week27

> **定理 2.1 (化二重积分为累次积分)**
> 
> 设 $f$ 在 $D=\left\{\left(x,y\right):a\le{x}\le{b},\varphi_1\left(x\right)\le{y}\le\varphi_2\left(x\right)\right\}$ 上连续, 则 $\iint_Df\,\mathrm{d}x\mathrm{d}y=\int_a^b\mathrm{d}x\int_{\varphi_1\left(x\right)}^{\varphi_2\left(x\right)}f\left(x,y\right)\,\mathrm{d}y$.

> **定理 2.2 (极坐标下的二重积分)**
> 
> $\iint_Df\,\mathrm{d}x\mathrm{d}y=\iint_{D^*}f\left(r\cos\theta,r\sin\theta\right)\,r\,\mathrm{d}r\mathrm{d}\theta$.

> **定理 3.1 (二重积分的变量替换公式)**
> 
> 设 $f$ 在 $D$ 上连续, 变换 $F:\left(u,v\right)\mapsto\left(x\left(u,v\right),y\left(u,v\right)\right)$ 是 $G$ 到 $D$ 的一一映射, 雅可比行列式 $J\left(u,v\right)\ne0$. 则 $\iint_Df\,\mathrm{d}x\mathrm{d}y=\iint_Gf\left(x\left(u,v\right),y\left(u,v\right)\right)\left|J\left(u,v\right)\right|\,\mathrm{d}u\mathrm{d}v$.

> **定理 4.2 (三重积分的穿线法)**
> 
> 设 $\Omega=\left\{\left(x,y,z\right):\left(x,y\right)\in{D},z_1\left(x,y\right)\le{z}\le{z}_2\left(x,y\right)\right\}$. 则 $\iiint_\Omega{f}\,\mathrm{d}V=\iint_D\mathrm{d}x\mathrm{d}y\int_{z_1\left(x,y\right)}^{z_2\left(x,y\right)}f\,\mathrm{d}z$.

> **定理 4.4 (三重积分换元公式)**
> 
> $\iiint_\Omega{f}\,\mathrm{d}x\mathrm{d}y\mathrm{d}z=\iiint_{\Omega'}f\left(x\left(u,v,w\right),y\left(u,v,w\right),z\left(u,v,w\right)\right)\left|J\right|\,\mathrm{d}u\mathrm{d}v\mathrm{d}w$. 柱坐标 $\left|J\right|=r$, 球坐标 $\left|J\right|=\rho^2\sin\varphi$.

## 8.2-6

求 $\iint_De^{-x^2-y^2}\,\mathrm{d}x\mathrm{d}y$, 其中 $D$ 为圆环 $1\le{x}^2+y^2\le4$ 在第一象限部分.

### 解答 8.2-6

由**定理 2.2 (极坐标下的二重积分)**,

$$
\iint_De^{-x^2-y^2}=\frac\pi4\left(e^{-1}-e^{-4}\right).
$$

$\blacksquare$

## 8.2-7

计算:

(1) $\iint_D\sin\sqrt{x^2+y^2}\,\mathrm{d}x\mathrm{d}y$, $D=\left\{\pi^2\le{x}^2+y^2\le4\pi^2\right\}$;

(2) $\iint_D\left(x+y\right)\,\mathrm{d}x\mathrm{d}y$, $D=\left\{x^2+y^2\le{x}+y\right\}$;

(3) $\iint_D\left(x^2+y^2\right)\,\mathrm{d}x\mathrm{d}y$, $D=\left\{\left(x^2+y^2\right)^2\le{a}^2\left(x^2-y^2\right)\right\}$;

(4) $\iint_Dx\,\mathrm{d}x\mathrm{d}y$, $D$ 为阿基米德螺线 $r=\theta$ 与 $\theta=\pi$ 所围区域.

### 解答 8.2-7

(1) $=-6\pi^2$.

(2) 平移后由对称性, $=\frac\pi2$.

(3) 双纽线, $=\frac{\pi{a}^4}{8}$.

(4) $=4-\pi^2$. $\blacksquare$

## 8.2-8

设 $I\left(a\right)=\int_0^ae^{-x^2}\,\mathrm{d}x$, $J\left(a\right)=\iint_{D_a}e^{-x^2-y^2}\,\mathrm{d}x\mathrm{d}y$, 其中 $D_a$ 为第一象限四分之一圆盘. 证明:

(1) $\left[I\left(a\right)\right]^2=\iint_{R_a}e^{-x^2-y^2}\,\mathrm{d}x\mathrm{d}y$;

(2) $J\left(a\right)\le\left[I\left(a\right)\right]^2\le{J}\left(\sqrt2a\right)$;

(3) $\lim_{a\to\infty}\int_0^ae^{-x^2}\,\mathrm{d}x=\frac{\sqrt\pi}2$.

### 解答 8.2-8

(1) 由**定理 2.1 (化二重积分为累次积分)**, $\left[I\left(a\right)\right]^2=\iint_{R_a}e^{-x^2-y^2}$.

(2) 因 $D_a\subset{R}_a\subset{D}_{\sqrt2a}$, 由二重积分的比较性质, 得 $J\left(a\right)\le\left[I\left(a\right)\right]^2\le{J}\left(\sqrt2a\right)$.

(3) 由**定理 2.2 (极坐标下的二重积分)**, $J\left(a\right)=\frac\pi4\left(1-e^{-a^2}\right)$. 代入 (2) 并令 $a\to\infty$, 由夹逼定理, $\left[I\left(a\right)\right]^2\to\frac\pi4$, 故 $I\left(a\right)\to\frac{\sqrt\pi}2$. $\blacksquare$

## 8.3-1

利用适当的坐标变换计算 $\iint_D\left(\sqrt{y/x}+\sqrt{xy}\right)\mathrm{d}x\mathrm{d}y$, 其中 $D$ 由 $xy=1$, $xy=9$, $y=x$, $y=4x$ 围成.

### 解答 8.3-1

令 $u=xy$, $v=y/x$. 则 $G=\left\{\left(u,v\right):1\le{u}\le9,1\le{v}\le4\right\}$. 逆变换 $x=\sqrt{u/v}$, $y=\sqrt{uv}$. 雅可比行列式 $\left|J\right|=\frac1{2v}$. 被积函数 $\sqrt{v}+\sqrt{u}$. 由**定理 3.1 (二重积分的变量替换公式)**,

$$
\iint_D\left(\sqrt{y/x}+\sqrt{xy}\right)=8+\frac{52}{3}\ln2.
$$

$\blacksquare$

## 8.3-4

计算 $\iint_D\left(x+y\right)\mathrm{d}x\mathrm{d}y$, 其中 $D$ 由 $y=4x^2$, $y=9x^2$, $x=4y^2$, $x=9y^2$ 围成.

### 解答 8.3-4

令 $u=y/x^2$, $v=x/y^2$. 则 $G=\left[4,9\right]\times\left[4,9\right]$. 逆变换 $x=u^{-2/3}v^{-1/3}$, $y=u^{-1/3}v^{-2/3}$. 雅可比行列式 $\left|J\right|=\frac1{3u^2v^2}$. 由**定理 3.1 (二重积分的变量替换公式)**,

$$
\iint_D\left(x+y\right)=\frac3{10}\left(9^{-5/3}-4^{-5/3}\right)\left(9^{-4/3}-4^{-4/3}\right).
$$

$\blacksquare$

## 8.3-6

求曲线 $\left(\frac{x^2}{a^2}+\frac{y^2}{b^2}\right)^2=\frac{xy}{c^2}$ 所围区域 $D$ 的面积.

### 解答 8.3-6

作广义极坐标变换 $x=ar\cos\theta$, $y=br\sin\theta$. 雅可比行列式 $\left|J\right|=abr$. 代入曲线方程得 $r^2=\frac{ab\sin2\theta}{2c^2}$. 由 $\sin2\theta\ge0$, $\theta\in\left[0,\pi/2\right]\cup\left[\pi,3\pi/2\right]$. 由**定理 3.1 (二重积分的变量替换公式)**,

$$
m\left(D\right)=\frac{a^2b^2}{2c^2}.
$$

$\blacksquare$

## 8.4-1

计算 $\iiint_\Omega{z}^2\,\mathrm{d}V$, 其中 $\Omega$ 为单位球.

### 解答 8.4-1

由对称性, $\iiint{z}^2=\frac13\iiint\left(x^2+y^2+z^2\right)$. 用球坐标, 由**定理 4.4 (三重积分换元公式)**,

$$
\iiint_\Omega{z}^2\,\mathrm{d}V=\frac{4\pi}{15}.
$$

$\blacksquare$

## 8.4-2

计算 $\iiint_\Omega\left(x+y+z\right)\,\mathrm{d}V$, 其中 $\Omega=\left\{x^2+y^2\le4,0\le{z}\le1\right\}$.

### 解答 8.4-2

由对称性, $\iiint{x}=\iiint{y}=0$. 用柱坐标, 由**定理 4.4 (三重积分换元公式)**,

$$
\iiint_\Omega{z}\,\mathrm{d}V=2\pi.
$$

$\blacksquare$

## 8.4-3

计算 $\iiint_\Omega\left(x+y+z\right)^3\,\mathrm{d}V$, 其中 $\Omega$ 为球体 $x^2+y^2+z^2\le{R}^2$.

### 解答 8.4-3

展开后每一项均为某个变量的奇函数, 而球体关于各坐标平面对称. 故

$$
\iiint_\Omega\left(x+y+z\right)^3\,\mathrm{d}V=0.
$$

$\blacksquare$

## 8.4-5

计算 $\iiint_\Omega\left(x^2+y^2+z^2\right)\,\mathrm{d}V$, 其中 $\Omega=\left\{a^2\le{x}^2+y^2+z^2\le{b}^2\right\}$.

### 解答 8.4-5

用球坐标, 由**定理 4.4 (三重积分换元公式)**,

$$
\iiint_\Omega\left(x^2+y^2+z^2\right)\,\mathrm{d}V=\frac{4\pi}5\left(b^5-a^5\right).
$$

$\blacksquare$

## 8.4-6

计算 $\iiint_\Omega\left(x^2+y^2\right)\,\mathrm{d}V$, 其中 $\Omega=\left\{x^2+y^2\le{z}\le1\right\}$.

### 解答 8.4-6

用柱坐标, 由**定理 4.2 (三重积分的穿线法)** 与**定理 4.4 (三重积分换元公式)**,

$$
\iiint_\Omega\left(x^2+y^2\right)\,\mathrm{d}V=\frac\pi6.
$$

$\blacksquare$

## 8.4-8

计算 $\iiint_\Omega\left(x^2+y^2\right)^2\,\mathrm{d}V$, 其中 $\Omega$ 由 $z=\sqrt{1-x^2-y^2}$ 与 $z=\sqrt{x^2+y^2}$ 围成.

### 解答 8.4-8

在球坐标下, $0\le\rho\le1$, $0\le\varphi\le\pi/4$. 由**定理 4.4 (三重积分换元公式)**,

$$
\iiint_\Omega\left(x^2+y^2\right)^2\,\mathrm{d}V=\frac{\pi\left(64-43\sqrt2\right)}{420}.
$$

$\blacksquare$
