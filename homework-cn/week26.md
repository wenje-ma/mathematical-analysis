# week26

> **命题 1.3 (可求面积的充要条件)**
> 
> $E$ 可求面积的充要条件是 $\partial{E}$ 为零面积集合. 特别地, 边界为逐段光滑曲线的有界区域可求面积.

> **定理 1.4 (可积的充要条件)**
> 
> $f$ 在可求面积区域 $D$ 上可积的充要条件是 $\lim_{\lambda\to0}\sum_i\omega_i\Delta\sigma_i=0$.

> **定理 1.5 (连续函数可积)**
> 
> 若 $D$ 是有界闭区域且边界为零面积集合, $f$ 在 $D$ 上连续, 则 $f$ 在 $D$ 上可积.

> **定理 2.1 (化二重积分为累次积分)**
> 
> 设 $f$ 在 $D=\left\{\left(x,y\right):a\le{x}\le{b},\varphi_1\left(x\right)\le{y}\le\varphi_2\left(x\right)\right\}$ 上连续, 则 $\iint_Df\,\mathrm{d}x\mathrm{d}y=\int_a^b\mathrm{d}x\int_{\varphi_1\left(x\right)}^{\varphi_2\left(x\right)}f\left(x,y\right)\,\mathrm{d}y$.

> **定理 2.2 (极坐标下的二重积分)**
> 
> $\iint_Df\,\mathrm{d}x\mathrm{d}y=\iint_{D^*}f\left(r\cos\theta,r\sin\theta\right)\,r\,\mathrm{d}r\mathrm{d}\theta$.

## 8.1-3

设 $D\left(x,y\right)=1$ (当 $x,y$ 均为有理数), $D\left(x,y\right)=0$ (其他). 证明 $D$ 在 $R=\left[0,1\right]\times\left[0,1\right]$ 上不可积.

### 解答 8.1-3

对 $R$ 作任意分割, 每个小区域 $D_i$ 中既含有理点又含无理点. 故 $\omega_i=1$. 于是 $D\left(T\right)-d\left(T\right)=\sum\Delta\sigma_i=1$, 不趋于 $0$. 由**定理 1.4 (可积的充要条件)**, $D$ 不可积. $\blacksquare$

## 8.1-4

设 $f=g$ 在 $D\setminus\gamma$ 上, 其中 $\gamma$ 是 $D$ 内部的一条直线段. 证明 $\iint_Df=\iint_Dg$.

### 解答 8.1-4

直线段 $\gamma$ 是逐段光滑曲线, 由**命题 1.3 (可求面积的充要条件)**, $\gamma$ 是零面积集合. 由二重积分的基本性质 (可加性),

$$
\iint_Df=\iint_{D\setminus\gamma}f+\iint_\gamma{f}=\iint_{D\setminus\gamma}f.
$$

同理 $\iint_Dg=\iint_{D\setminus\gamma}g$. 因 $f=g$ 在 $D\setminus\gamma$ 上, 故两者相等. $\blacksquare$

## 8.1-5

设 $f$ 在 $D$ 上可积. 证明 $\left|f\right|$ 在 $D$ 上也可积.

### 解答 8.1-5

对每个小区域 $D_i$, 由三角不等式, $\omega_{\left|f\right|}^{\left(i\right)}\le\omega_f^{\left(i\right)}$. 故 $\sum\omega_{\left|f\right|}\Delta\sigma_i\le\sum\omega_f\Delta\sigma_i$. 由**定理 1.4 (可积的充要条件)**, $\left|f\right|$ 可积. $\blacksquare$

## 8.1-8

设 $f$ 在 $D$ 上连续, $g$ 在 $D$ 上连续且 $g>0$. 证明存在 $\left(x_0,y_0\right)\in{D}$ 使 $\iint_Dfg=f\left(x_0,y_0\right)\iint_Dg$.

### 解答 8.1-8

因 $f$ 连续, 由**定理 1.5 (连续函数可积)**, $f$ 在 $D$ 上可积, 且有最大值 $M$ 与最小值 $m$. 由 $mg\le{f}g\le{M}g$ 及二重积分的基本性质 (比较性质),

$$
m\iint_Dg\le\iint_Dfg\le{M}\iint_Dg.
$$

因 $\iint_Dg>0$, 故 $m\le\frac{\iint_Dfg}{\iint_Dg}\le{M}$. 由介值定理, 存在 $\left(x_0,y_0\right)$ 使 $f\left(x_0,y_0\right)=\frac{\iint_Dfg}{\iint_Dg}$. $\blacksquare$

## 8.1-9

设 $f$ 在 $D$ 上连续, 非负, 且 $\iint_Df=0$. 证明 $f\equiv0$.

### 解答 8.1-9

反设存在 $\left(x_0,y_0\right)$ 使 $f\left(x_0,y_0\right)>0$. 由连续性, 在 $R_\delta$ 内 $f>\frac{f\left(x_0,y_0\right)}2$. 由二重积分的基本性质 (比较性质),

$$
\iint_Df\ge\iint_{R_\delta}f\ge\frac{f\left(x_0,y_0\right)}2\cdot\left|R_\delta\right|>0,
$$

矛盾. 故 $f\equiv0$. $\blacksquare$

## 8.2-2

改变下列累次积分的积分次序:

(1) $\int_0^1\mathrm{d}y\int_y^{\sqrt{y}}f\,\mathrm{d}x$;

(2) $\int_1^2\mathrm{d}x\int_x^{2x}f\,\mathrm{d}y$;

(3) $\int_0^5\mathrm{d}x\int_x^{10-x}f\,\mathrm{d}y$;

(4) $\int_0^1\mathrm{d}x\int_{e^x}^ef\,\mathrm{d}y$.

### 解答 8.2-2

(1) 由 $y\le{x}\le\sqrt{y}$ 得 $x^2\le{y}\le{x}$. 故原式 $=\int_0^1\mathrm{d}x\int_{x^2}^xf\,\mathrm{d}y$.

(2) 分段: $y\in\left[1,2\right]$ 时 $1\le{x}\le{y}$; $y\in\left[2,4\right]$ 时 $y/2\le{x}\le2$. 故原式 $=\int_1^2\mathrm{d}y\int_1^yf\,\mathrm{d}x+\int_2^4\mathrm{d}y\int_{y/2}^2f\,\mathrm{d}x$.

(3) 分段: $y\in\left[0,5\right]$ 时 $0\le{x}\le{y}$; $y\in\left[5,10\right]$ 时 $0\le{x}\le10-y$. 故原式 $=\int_0^5\mathrm{d}y\int_0^yf\,\mathrm{d}x+\int_5^{10}\mathrm{d}y\int_0^{10-y}f\,\mathrm{d}x$.

(4) 由 $e^x\le{y}\le{e}$ 得 $0\le{x}\le\ln{y}$. 故原式 $=\int_1^e\mathrm{d}y\int_0^{\ln{y}}f\,\mathrm{d}x$. $\blacksquare$

## 8.2-3

计算下列二重积分:

(1) $\iint_Dy\,\mathrm{d}x\mathrm{d}y$, $D$ 由 $y=0$ 及 $y=\sin{x}$ ($0\le{x}\le\pi$) 围成;

(2) $\iint_D\left(x^2+y\right)\,\mathrm{d}x\mathrm{d}y$, $D$ 由 $y=x^2$ 及 $y^2=x$ 围成;

(3) $\iint_De^{x/y}\,\mathrm{d}x\mathrm{d}y$, $D$ 由 $y^2=x$, $x=0$, $y=1$ 围成;

(4) $\iint_D\sqrt{1-x^4}\,\mathrm{d}x\mathrm{d}y$, $D$ 由 $y=x^3$, $x=1$, $y=0$ 围成.

### 解答 8.2-3

(1) 由**定理 2.1 (化二重积分为累次积分)**, $\iint_Dy=\frac12\int_0^\pi\sin^2x\,\mathrm{d}x=\frac\pi4$.

(2) $\iint_D\left(x^2+y\right)=\int_0^1\left(x^{5/2}+\frac{x}2-\frac32x^4\right)\mathrm{d}x=\frac{33}{140}$.

(3) 先对 $x$ 积分: $\iint_De^{x/y}=\int_0^1\left(ye^y-y\right)\mathrm{d}y=\frac12$.

(4) $\iint_D\sqrt{1-x^4}=\int_0^1x^3\sqrt{1-x^4}\,\mathrm{d}x=\frac16$. $\blacksquare$

## 8.2-4

计算下列累次积分:

(1) $\int_0^\pi\mathrm{d}x\int_x^\pi\frac{\sin{y}}{y}\,\mathrm{d}y$;

(2) $\int_0^2\mathrm{d}x\int_x^22y^2\sin\left(xy\right)\,\mathrm{d}y$.

### 解答 8.2-4

(1) 交换次序: $\int_0^\pi\mathrm{d}y\int_0^y\frac{\sin{y}}{y}\,\mathrm{d}x=\int_0^\pi\sin{y}\,\mathrm{d}y=2$.

(2) 交换次序: $\int_0^2\mathrm{d}y\int_0^y2y^2\sin\left(xy\right)\,\mathrm{d}x=\int_0^22y\left[1-\cos\left(y^2\right)\right]\mathrm{d}y=4-\sin4$. $\blacksquare$

## 8.2-5

用极坐标计算:

(1) $\int_{-1}^0\mathrm{d}x\int_{-\sqrt{1-x^2}}^0\frac{2}{1+\sqrt{x^2+y^2}}\,\mathrm{d}y$;

(2) $\int_0^2\mathrm{d}x\int_0^{\sqrt{1-\left(x-1\right)^2}}3xy\,\mathrm{d}y$;

(3) $\int_0^R\mathrm{d}x\int_0^{\sqrt{R^2-x^2}}\ln\left(1+x^2+y^2\right)\,\mathrm{d}y$.

### 解答 8.2-5

(1) 第三象限单位圆. 由**定理 2.2 (极坐标下的二重积分)**, $\pi\left(1-\ln2\right)$.

(2) 上半圆 $\left(x-1\right)^2+y^2\le1$. $=2$.

(3) 第一象限四分之一圆盘. $=\frac\pi4\left[\left(1+R^2\right)\ln\left(1+R^2\right)-R^2\right]$. $\blacksquare$
