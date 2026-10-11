# 作业 30

> **定理 3.1**（二重积分的变量替换公式）设 $z=f\left(x,y\right)$ 在可求面积的有界闭区域 $D$ 上连续. 设变换 $F:\left(u,v\right)\mapsto\left(x\left(u,v\right),y\left(u,v\right)\right)$ 是有界闭区域 $G$ 到 $D$ 的一一映射, $x\left(u,v\right),y\left(u,v\right)$ 在 $G$ 上有连续的一阶偏导数, 且雅可比行列式 $J\left(u,v\right)=\frac{\partial\left(x,y\right)}{\partial\left(u,v\right)}\ne0$. 则

$$
\iint_D f\left(x,y\right)\,\mathrm{d}x\mathrm{d}y=\iint_G f\bigl(x\left(u,v\right),y\left(u,v\right)\bigr)\lvert J\left(u,v\right)\rvert\,\mathrm{d}u\mathrm{d}v.
$$

特别地, 区域 $D$ 的面积 $m\left(D\right)=\iint_G\lvert J\left(u,v\right)\rvert\,\mathrm{d}u\mathrm{d}v$.

### 习题一

（习题 8.3-1）利用适当的坐标变换计算 $\displaystyle\iint_D\left(\sqrt{\frac yx}+\sqrt{xy}\right)\mathrm{d}x\mathrm{d}y$, 其中 $D$ 是由曲线 $xy=1$, $xy=9$, $y=x$ 及 $y=4x$ 所围成的区域.

### 解答 习题一

作变量替换 $u=xy$, $v=\frac yx$, 则 $D$ 变为 $G=\left\{\left(u,v\right):1\le u\le9,\ 1\le v\le4\right\}$. 其逆变换为 $x=\sqrt{u/v}$, $y=\sqrt{uv}$. 雅可比行列式

$$
\frac{\partial\left(u,v\right)}{\partial\left(x,y\right)}=\begin{vmatrix}y&x\\-y/x^2&1/x\end{vmatrix}=\frac{2y}{x}=2v,
$$

故 $\lvert J\rvert=\left\lvert\frac{\partial\left(x,y\right)}{\partial\left(u,v\right)}\right\rvert=\frac1{2v}$. 被积函数 $\sqrt{y/x}+\sqrt{xy}=\sqrt v+\sqrt u$. 由**定理 3.1**,

$$
\begin{aligned}\iint_D\left(\sqrt{\frac yx}+\sqrt{xy}\right)\mathrm{d}x\mathrm{d}y&=\int_1^9\mathrm{d}u\int_1^4\left(\sqrt v+\sqrt u\right)\frac1{2v}\,\mathrm{d}v\\&=\frac12\int_1^9\left[2\sqrt v+\sqrt u\ln v\right]_1^4\mathrm{d}u\\&=\frac12\int_1^9\left(2+\sqrt u\ln4\right)\,\mathrm{d}u\\&=\frac12\left[2u+\frac23u^{3/2}\ln4\right]_1^9\\&=8+\frac{26}{3}\ln4=8+\frac{52}{3}\ln2.\end{aligned}
$$

$\blacksquare$

### 习题二

（习题 8.3-4）计算 $\displaystyle\iint_D\left(x+y\right)\mathrm{d}x\mathrm{d}y$, 其中 $D$ 由曲线 $y=4x^2$, $y=9x^2$, $x=4y^2$, $x=9y^2$ 所围成的区域.

### 解答 习题二

作变量替换 $u=\frac y{x^2}$, $v=\frac x{y^2}$, 则 $D$ 变为 $G=\left\{\left(u,v\right):4\le u\le9,\ 4\le v\le9\right\}$. 由 $y=ux^2=u\left(vy^2\right)^2=uv^2y^4$ 得 $y^3=\frac1{uv^2}$, 即 $y=u^{-1/3}v^{-2/3}$; 同理 $x=u^{-2/3}v^{-1/3}$. 雅可比行列式

$$
J=\frac{\partial\left(x,y\right)}{\partial\left(u,v\right)}=
\begin{vmatrix}
-\frac23u^{-5/3}v^{-1/3}&-\frac13u^{-2/3}v^{-4/3}\\
-\frac13u^{-4/3}v^{-2/3}&-\frac23u^{-1/3}v^{-5/3}
\end{vmatrix}
=\frac1{3u^2v^2}.
$$

由**定理 3.1**,

$$
\begin{aligned}\iint_D\left(x+y\right)\mathrm{d}x\mathrm{d}y&=\int_4^9\!\!\int_4^9\left(u^{-2/3}v^{-1/3}+u^{-1/3}v^{-2/3}\right)\frac1{3u^2v^2}\,\mathrm{d}u\mathrm{d}v\\&=\frac13\left(\int_4^9u^{-8/3}\mathrm{d}u\right)\left(\int_4^9v^{-7/3}\mathrm{d}v\right)+\frac13\left(\int_4^9u^{-7/3}\mathrm{d}u\right)\left(\int_4^9v^{-8/3}\mathrm{d}v\right).\end{aligned}
$$

两项对称, 合并为

$$
\begin{aligned}\iint_D\left(x+y\right)\mathrm{d}x\mathrm{d}y&=\frac23\left[-\frac35u^{-5/3}\right]_4^9\left[-\frac34v^{-4/3}\right]_4^9\\&=\frac3{10}\left(9^{-5/3}-4^{-5/3}\right)\left(9^{-4/3}-4^{-4/3}\right).\end{aligned}
$$

$\blacksquare$

### 习题三

（习题 8.3-6）求曲线 $\left(\frac{x^2}{a^2}+\frac{y^2}{b^2}\right)^2=\frac{xy}{c^2}$ ($a>0,b>0,c>0$) 所围成的区域 $D$ 的面积.

### 解答 习题三

作广义极坐标变换 $x=ar\cos\theta$, $y=br\sin\theta$, 雅可比行列式 $\lvert J\rvert=abr$. 代入曲线方程:

$$
r^4=\frac{\left(ar\cos\theta\right)\left(br\sin\theta\right)}{c^2}=\frac{abr^2\sin\theta\cos\theta}{c^2},
$$

即 $r^2=\frac{ab\sin2\theta}{2c^2}$. 由 $r^2\ge0$ 知 $\sin2\theta\ge0$, 即 $\theta\in\left[0,\pi/2\right]\cup\left[\pi,3\pi/2\right]$. 两部分关于原点对称, 故面积

$$
\begin{aligned}m\left(D\right)&=2\int_0^{\pi/2}\mathrm{d}\theta\int_0^{\sqrt{ab\sin2\theta/\left(2c^2\right)}}abr\,\mathrm{d}r\\&=2\int_0^{\pi/2}ab\cdot\frac12\cdot\frac{ab\sin2\theta}{2c^2}\,\mathrm{d}\theta\\&=\frac{a^2b^2}{2c^2}\int_0^{\pi/2}\sin2\theta\,\mathrm{d}\theta=\frac{a^2b^2}{2c^2}.\end{aligned}
$$

$\blacksquare$
