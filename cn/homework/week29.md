# 作业 29

> **定理 2.1**（化二重积分为累次积分）设 $z=f\left(x,y\right)$ 在闭区域 $D$ 上连续,
> $$
> D=\left\{\left(x,y\right):a\le x\le b,\varphi_1\left(x\right)\le y\le\varphi_2\left(x\right)\right\},
> $$
> 其中 $\varphi_1,\varphi_2$ 在 $\left[a,b\right]$ 上连续. 则

$$
\iint_D f\left(x,y\right)\,\mathrm{d}x\mathrm{d}y=\int_a^b\mathrm{d}x\int_{\varphi_1\left(x\right)}^{\varphi_2\left(x\right)}f\left(x,y\right)\,\mathrm{d}y.
$$

> **定理 2.2**（极坐标下的二重积分）设 $D$ 为可求面积的有界闭区域, $z=f\left(x,y\right)$ 在 $D$ 上可积. 则

$$
\iint_D f\left(x,y\right)\,\mathrm{d}x\mathrm{d}y=\iint_{D^*}f\left(r\cos\theta,r\sin\theta\right)\,r\,\mathrm{d}r\mathrm{d}\theta,
$$

其中

$$
D^*=\left\{\left(r,\theta\right):\left(r\cos\theta,r\sin\theta\right)\in D\right\}.
$$

### 习题一

（习题 8.2-2）改变下列累次积分的积分次序:
(1) $\displaystyle\int_0^1\mathrm{d}y\int_y^{\sqrt y}f\left(x,y\right)\,\mathrm{d}x$;

(2) $\displaystyle\int_1^2\mathrm{d}x\int_x^{2x}f\left(x,y\right)\,\mathrm{d}y$;

(3) $\displaystyle\int_0^5\mathrm{d}x\int_x^{10-x}f\left(x,y\right)\,\mathrm{d}y$;

(4) $\displaystyle\int_0^1\mathrm{d}x\int_{e^x}^e f\left(x,y\right)\,\mathrm{d}y$.

### 解答 习题一

(1)原积分区域: $0\le y\le1$, $y\le x\le\sqrt y$. 由 $y\le x\le\sqrt y$ 得 $x^2\le y\le x$, 且 $0\le x\le1$. 故

$$
\int_0^1\mathrm{d}y\int_y^{\sqrt y}f\left(x,y\right)\,\mathrm{d}x=\int_0^1\mathrm{d}x\int_{x^2}^x f\left(x,y\right)\,\mathrm{d}y.
$$

(2)原区域: $1\le x\le2$, $x\le y\le2x$. 按 $y$ 分段: $y\in\left[1,2\right]$ 时 $1\le x\le y$; $y\in\left[2,4\right]$ 时 $y/2\le x\le2$. 故

$$
\int_1^2\mathrm{d}x\int_x^{2x}f\left(x,y\right)\,\mathrm{d}y=\int_1^2\mathrm{d}y\int_1^y f\left(x,y\right)\,\mathrm{d}x+\int_2^4\mathrm{d}y\int_{y/2}^2 f\left(x,y\right)\,\mathrm{d}x.
$$

(3)原区域: $0\le x\le5$, $x\le y\le10-x$. 按 $y$ 分段: $y\in\left[0,5\right]$ 时 $0\le x\le y$; $y\in\left[5,10\right]$ 时 $0\le x\le10-y$. 故

$$
\int_0^5\mathrm{d}x\int_x^{10-x}f\left(x,y\right)\,\mathrm{d}y=\int_0^5\mathrm{d}y\int_0^y f\left(x,y\right)\,\mathrm{d}x+\int_5^10\mathrm{d}y\int_0^{10-y}f\left(x,y\right)\,\mathrm{d}x.
$$

(4)原区域: $0\le x\le1$, $e^x\le y\le e$, 即 $0\le x\le\ln y$. 故

$$
\int_0^1\mathrm{d}x\int_{e^x}^e f\left(x,y\right)\,\mathrm{d}y=\int_1^e\mathrm{d}y\int_0^{\ln y}f\left(x,y\right)\,\mathrm{d}x.

$$

$\blacksquare$
### 习题二

（习题 8.2-3）计算下列二重积分:
(1) $\displaystyle\iint_D y\,\mathrm{d}x\mathrm{d}y$, 其中 $D$ 为由直线 $y=0$ 及曲线 $y=\sin x$ ($0\le x\le\pi$) 所围之区域;

(2) $\displaystyle\iint_D\left(x^2+y\right)\,\mathrm{d}x\mathrm{d}y$, 其中 $D$ 为由曲线 $y=x^2$ 及 $y^2=x$ 所围之区域;

(3) $\displaystyle\iint_D e^{x/y}\,\mathrm{d}x\mathrm{d}y$, 其中 $D$ 为由 $y^2=x$, $x=0$ 及 $y=1$ 所围之区域;

(4) $\displaystyle\iint_D\sqrt{1-x^4}\,\mathrm{d}x\mathrm{d}y$, 其中 $D$ 为由 $y=x^3$, $x=1$ 及 $y=0$ 所围之区域.

### 解答 习题二

(1)$D:0\le x\le\pi$, $0\le y\le\sin x$. 由**定理 2.1**,

$$
\iint_D y\,\mathrm{d}x\mathrm{d}y=\int_0^\pi\mathrm{d}x\int_0^{\sin x}y\,\mathrm{d}y=\frac12\int_0^\pi\sin^2x\,\mathrm{d}x=\frac\pi4.
$$

(2)$D:0\le x\le1$, $x^2\le y\le\sqrt x$. 由**定理 2.1**,

$$
\begin{aligned}\iint_D\left(x^2+y\right)\,\mathrm{d}x\mathrm{d}y&=\int_0^1\mathrm{d}x\int_{x^2}^{\sqrt x}\left(x^2+y\right)\,\mathrm{d}y\\&=\int_0^1\left(x^{5/2}+\frac x2-\frac32x^4\right)\mathrm{d}x\\&=\frac27+\frac14-\frac3{10}=\frac{33}{140}.\end{aligned}
$$

(3)$D:0\le y\le1$, $0\le x\le y^2$. 由**定理 2.1** (先对 $x$ 积分),

$$
\begin{aligned}\iint_D e^{x/y}\,\mathrm{d}x\mathrm{d}y&=\int_0^1\mathrm{d}y\int_0^{y^2}e^{x/y}\,\mathrm{d}x\\&=\int_0^1\left(ye^y-y\right)\mathrm{d}y\\&=\left[ye^y-e^y-\frac12y^2\right]_0^1=\frac12.\end{aligned}
$$

(4)$D:0\le x\le1$, $0\le y\le x^3$. 由**定理 2.1**,

$$
\iint_D\sqrt{1-x^4}\,\mathrm{d}x\mathrm{d}y=\int_0^1\mathrm{d}x\int_0^{x^3}\sqrt{1-x^4}\,\mathrm{d}y=\int_0^1x^3\sqrt{1-x^4}\,\mathrm{d}x.
$$

令 $u=1-x^4$, $\mathrm{d}u=-4x^3\mathrm{d}x$, 得

$$
\iint_D\sqrt{1-x^4}\,\mathrm{d}x\mathrm{d}y=\frac14\int_0^1\sqrt u\,\mathrm{d}u=\frac16.

$$

$\blacksquare$
### 习题三

（习题 8.2-4）计算下列累次积分:
(1) $\displaystyle\int_0^\pi\mathrm{d}x\int_x^\pi\frac{\sin y}{y}\,\mathrm{d}y$;

(2) $\displaystyle\int_0^2\mathrm{d}x\int_x^2 2y^2\sin\left(xy\right)\,\mathrm{d}y$.

### 解答 习题三

(1)原积分区域: $0\le x\le\pi$, $x\le y\le\pi$. 交换积分次序 (由**定理 2.1**), 得 $0\le y\le\pi$, $0\le x\le y$, 故

$$
\int_0^\pi\mathrm{d}x\int_x^\pi\frac{\sin y}{y}\,\mathrm{d}y=\int_0^\pi\mathrm{d}y\int_0^y\frac{\sin y}{y}\,\mathrm{d}x=\int_0^\pi\sin y\,\mathrm{d}y=2.
$$

(2)原区域: $0\le x\le2$, $x\le y\le2$. 交换次序得 $0\le y\le2$, $0\le x\le y$. 故

$$
\begin{aligned}\int_0^2\mathrm{d}x\int_x^2 2y^2\sin\left(xy\right)\,\mathrm{d}y&=\int_0^2\mathrm{d}y\int_0^y 2y^2\sin\left(xy\right)\,\mathrm{d}x\\&=\int_0^2 2y\left[1-\cos\left(y^2\right)\right]\,\mathrm{d}y\\&=\left[y^2-\sin\left(y^2\right)\right]_0^2=4-\sin4.\end{aligned}

$$

$\blacksquare$
### 习题四

（习题 8.2-5）将下列累次积分化成二重积分, 然后用极坐标计算该二重积分:
(1)

$$
\displaystyle\int_{-1}^0\mathrm{d}x\int_{-\sqrt{1-x^2}}^0\frac{2}{1+\sqrt{x^2+y^2}}\,\mathrm{d}y;
$$

(2) $\displaystyle\int_0^2\mathrm{d}x\int_0^{\sqrt{1-\left(x-1\right)^2}}3xy\,\mathrm{d}y$;

(3)

$$
\displaystyle\int_0^R\mathrm{d}x\int_0^{\sqrt{R^2-x^2}}\ln\left(1+x^2+y^2\right)\,\mathrm{d}y\left(R> 0\right).
$$

### 解答 习题四

(1)原区域为单位圆在第三象限部分 ($x\le0$, $y\le0$). 由**定理 2.2**, $\theta\in\left[\pi,3\pi/2\right]$, $r\in\left[0,1\right]$,

$$
\begin{aligned}\iint_D\frac{2}{1+\sqrt{x^2+y^2}}\,\mathrm{d}x\mathrm{d}y&=\int_\pi^{3\pi/2}\mathrm{d}\theta\int_0^1\frac{2}{1+r}\,r\,\mathrm{d}r\\&=\pi\left[r-\ln\left(1+r\right)\right]_0^1=\pi\left(1-\ln2\right).\end{aligned}
$$

(2)原区域为圆 $\left(x-1\right)^2+y^2\le1$ 的上半部分, 其极坐标方程为 $r=2\cos\theta$, $\theta\in\left[0,\pi/2\right]$. 由**定理 2.2**,

$$
\begin{aligned}\iint_D 3xy\,\mathrm{d}x\mathrm{d}y&=\int_0^{\pi/2}\mathrm{d}\theta\int_0^{2\cos\theta}3\left(r\cos\theta\right)\left(r\sin\theta\right)\,r\,\mathrm{d}r\\&=12\int_0^{\pi/2}\sin\theta\cos^5\theta\,\mathrm{d}\theta=2.\end{aligned}
$$

(3)原区域为第一象限的四分之一圆盘 $x^2+y^2\le R^2$, $x,y\ge0$. 由**定理 2.2**,

$$
\begin{aligned}\iint_D\ln\left(1+x^2+y^2\right)\,\mathrm{d}x\mathrm{d}y&=\int_0^{\pi/2}\mathrm{d}\theta\int_0^R\ln\left(1+r^2\right)\,r\,\mathrm{d}r\\&=\frac\pi2\cdot\frac12\left[\left(1+r^2\right)\ln\left(1+r^2\right)-r^2\right]_0^R\\&=\frac\pi4\left[\left(1+R^2\right)\ln\left(1+R^2\right)-R^2\right].\end{aligned}

$$

$\blacksquare$
### 习题五

（习题 8.2-6）求二重积分 $\displaystyle\iint_D e^{-x^2-y^2}\,\mathrm{d}x\mathrm{d}y$, 其中 $D$ 为圆环

$$
\left\{\left(x,y\right):1\le x^2+y^2\le4\right\}
$$

在第一象限中的部分.

### 解答 习题五

由**定理 2.2**, $D$ 的极坐标表示为 $\theta\in\left[0,\pi/2\right]$, $r\in\left[1,2\right]$, 故

$$
\iint_D e^{-x^2-y^2}\,\mathrm{d}x\mathrm{d}y=\int_0^{\pi/2}\mathrm{d}\theta\int_1^2 e^{-r^2}r\,\mathrm{d}r=\frac\pi2\cdot\left[-\frac12e^{-r^2}\right]_1^2=\frac\pi4\left(e^{-1}-e^{-4}\right).

$$

$\blacksquare$
### 习题六

（习题 8.2-7）计算下列二重积分:
(1) $\displaystyle\iint_D\sin\sqrt{x^2+y^2}\,\mathrm{d}x\mathrm{d}y$, 其中

$$
D=\left\{\left(x,y\right):\pi^2\le x^2+y^2\le4\pi^2\right\};
$$

(2) $\displaystyle\iint_D\left(x+y\right)\,\mathrm{d}x\mathrm{d}y$, 其中

$$
D=\left\{\left(x,y\right):x^2+y^2\le x+y\right\};
$$

(3) $\displaystyle\iint_D\left(x^2+y^2\right)\,\mathrm{d}x\mathrm{d}y$, 其中

$$
D=\left\{\left(x,y\right):\left(x^2+y^2\right)^2\le a^2\left(x^2-y^2\right)\right\};
$$

(4) $\displaystyle\iint_D x\,\mathrm{d}x\mathrm{d}y$, 其中 $D$ 为阿基米德螺线 $r=\theta$ 与半射线 $\theta=\pi$ 所围成的区域.

### 解答 习题六

(1)由**定理 2.2**, $\theta\in\left[0,2\pi\right]$, $r\in\left[\pi,2\pi\right]$,

$$
\begin{aligned}\iint_D\sin\sqrt{x^2+y^2}\,\mathrm{d}x\mathrm{d}y&=\int_0^{2\pi}\mathrm{d}\theta\int_\pi^{2\pi}\sin r\cdot r\,\mathrm{d}r\\&=2\pi\left[\sin r-r\cos r\right]_\pi^{2\pi}\\&=2\pi\left(-2\pi-\pi\right)=-6\pi^2.\end{aligned}
$$

(2)将 $D$ 改写为

$$
\left(x-\frac12\right)^2+\left(y-\frac12\right)^2\le\frac12.
$$

令 $u=x-\frac12$, $v=y-\frac12$, 则 $D$ 变为 $u^2+v^2\le\frac12$. 由对称性, $\iint u=\iint v=0$, 故

$$
\iint_D\left(x+y\right)\,\mathrm{d}x\mathrm{d}y=\iint_{u^2+v^2\le1/2}\left(u+v+1\right)\,\mathrm{d}u\mathrm{d}v=\iint_{u^2+v^2\le1/2}1\,\mathrm{d}u\mathrm{d}v=\frac\pi2.
$$

(3)在极坐标下

$$
\left(x^2+y^2\right)^2\le a^2\left(x^2-y^2\right)
$$

化为 $r^2\le a^2\cos2\theta$, 即 $r\le a\sqrt{\cos2\theta}$, $\cos2\theta\ge0$. 利用对称性 (四个对称瓣),

$$
\begin{aligned}\iint_D\left(x^2+y^2\right)\,\mathrm{d}x\mathrm{d}y&=4\int_0^{\pi/4}\mathrm{d}\theta\int_0^{a\sqrt{\cos2\theta}}r^2\cdot r\,\mathrm{d}r\\&=a^4\int_0^{\pi/4}\cos^22\theta\,\mathrm{d}\theta=\frac{\pi a^4}{8}.\end{aligned}
$$

(4)由**定理 2.2**, $\theta\in\left[0,\pi\right]$, $r\in\left[0,\theta\right]$,

$$
\begin{aligned}\iint_D x\,\mathrm{d}x\mathrm{d}y&=\int_0^\pi\mathrm{d}\theta\int_0^\theta\left(r\cos\theta\right)\,r\,\mathrm{d}r\\&=\frac13\int_0^\pi\theta^3\cos\theta\,\mathrm{d}\theta\\&=\frac13\left[\theta^3\sin\theta+3\theta^2\cos\theta-6\theta\sin\theta-6\cos\theta\right]_0^\pi\\&=\frac13\left(-3\pi^2+12\right)=4-\pi^2.\end{aligned}

$$

$\blacksquare$
### 习题七

（习题 8.2-8）设 $a> 0$, 令

$$
I\left(a\right)=\int_0^a e^{-x^2}\,\mathrm{d}x, J\left(a\right)=\iint_{D_a}e^{-x^2-y^2}\,\mathrm{d}x\mathrm{d}y,
$$

其中

$$
D_a=\left\{\left(x,y\right)\mid x^2+y^2\le a^2,x\ge0,y\ge0\right\}.
$$

证明:
(1)

$$
\displaystyle\left[I\left(a\right)\right]^2=\iint_{R_a}e^{-x^2-y^2}\,\mathrm{d}x\mathrm{d}y,
$$
其中

$$
R_a=\left\{\left(x,y\right)\mid0\le x\le a,0\le y\le a\right\};
$$

(2)

$$
J\left(a\right)\le\left[I\left(a\right)\right]^2\le J\left(\sqrt2\,a\right);
$$

(3) 利用本节例 2.8 的结果推出 $\displaystyle\lim_{a\to+\infty}\int_0^a e^{-x^2}\,\mathrm{d}x=\frac{\sqrt\pi}{2}$.

### 解答 习题七

(1)由**定理 2.1**,

$$
\left[I\left(a\right)\right]^2=\left(\int_0^a e^{-x^2}\mathrm{d}x\right)\left(\int_0^a e^{-y^2}\mathrm{d}y\right)=\int_0^a\mathrm{d}x\int_0^a e^{-x^2-y^2}\mathrm{d}y=\iint_{R_a}e^{-x^2-y^2}\,\mathrm{d}x\mathrm{d}y.
$$

(2)注意到 $D_a$ 是半径为 $a$ 的四分之一圆盘, $R_a=\left[0,a\right]\times\left[0,a\right]$ 是边长为 $a$ 的正方形, $D_{\sqrt2 a}$ 是半径为 $\sqrt2 a$ 的四分之一圆盘. 显然 $D_a\subset R_a\subset D_{\sqrt2 a}$. 因被积函数 $e^{-x^2-y^2}> 0$, 由第一章**性质**（二重积分的比较性质）,

$$
J\left(a\right)=\iint_{D_a}\le\iint_{R_a}=\left[I\left(a\right)\right]^2\le\iint_{D_{\sqrt2 a}}=J\left(\sqrt2\,a\right).
$$

(3)由**定理 2.2**, $D_a$ 的极坐标表示为 $\theta\in\left[0,\pi/2\right]$, $r\in\left[0,a\right]$, 故

$$
J\left(a\right)=\int_0^{\pi/2}\mathrm{d}\theta\int_0^a e^{-r^2}r\,\mathrm{d}r=\frac\pi2\cdot\frac{1-e^{-a^2}}2=\frac\pi4\left(1-e^{-a^2}\right).
$$

代入 (2) 得

$$
\frac\pi4\left(1-e^{-a^2}\right)\le\left[I\left(a\right)\right]^2\le\frac\pi4\left(1-e^{-2a^2}\right).
$$

令 $a\to+\infty$, 两端均趋于 $\pi/4$. 由夹逼定理, $\left[I\left(a\right)\right]^2\to\pi/4$, 故 $I\left(a\right)\to\sqrt\pi/2$. $\blacksquare$
