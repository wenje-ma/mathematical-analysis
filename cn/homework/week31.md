# 作业 31

> **定理 4.2**（三重积分的穿线法）设
> $$
> \Omega=\left\{\left(x,y,z\right):\left(x,y\right)\in D,z_1\left(x,y\right)\le z\le z_2\left(x,y\right)\right\},
> $$
> 其中 $D$ 为 $Oxy$ 平面上可求面积的有界闭区域, $z_1,z_2$ 在 $D$ 上连续, $f$ 在 $\Omega$ 上连续. 则

$$
\iiint_\Omega f\left(x,y,z\right)\,\mathrm{d}V=\iint_D\mathrm{d}x\mathrm{d}y\int_{z_1\left(x,y\right)}^{z_2\left(x,y\right)}f\left(x,y,z\right)\,\mathrm{d}z.
$$

> **定理 4.4**（三重积分换元公式）在变量替换 $x=x\left(u,v,w\right)$, $y=y\left(u,v,w\right)$, $z=z\left(u,v,w\right)$ 下,

$$
\iiint_\Omega f\,\mathrm{d}x\mathrm{d}y\mathrm{d}z=\iiint_{\Omega'}f\left(x\left(u,v,w\right),y\left(u,v,w\right),z\left(u,v,w\right)\right)\left| J\left(u,v,w\right)\right|\,\mathrm{d}u\mathrm{d}v\mathrm{d}w,
$$

其中 $J=\frac{\partial\left(x,y,z\right)}{\partial\left(u,v,w\right)}$. 特别地, 柱坐标 $\left(r,\theta,z\right)$ 下 $\left| J\right|=r$, 球坐标 $\left(\rho,\varphi,\theta\right)$ 下 $\left| J\right|=\rho^2\sin\varphi$.

### 习题一

（习题 8.4-1）计算 $\displaystyle\iiint_\Omega z^2\,\mathrm{d}V$, 其中 $\Omega$ 为单位球

$$
\Omega=\left\{\left(x,y,z\right):x^2+y^2+z^2\le1\right\}.
$$

### 解答 习题一

由对称性, $\iiint x^2=\iiint y^2=\iiint z^2$, 故

$$
\iiint_\Omega z^2\,\mathrm{d}V=\frac13\iiint_\Omega\left(x^2+y^2+z^2\right)\,\mathrm{d}V.
$$

用球坐标 $x=\rho\sin\varphi\cos\theta$, $y=\rho\sin\varphi\sin\theta$, $z=\rho\cos\varphi$, $\Omega$ 变为 $0\le\rho\le1$, $0\le\varphi\le\pi$, $0\le\theta\le2\pi$. 由**定理 4.4**,

$$
\iiint_\Omega z^2\,\mathrm{d}V=\frac13\int_0^{2\pi}\mathrm{d}\theta\int_0^\pi\sin\varphi\,\mathrm{d}\varphi\int_0^1\rho^2\cdot\rho^2\,\mathrm{d}\rho=\frac13\cdot2\pi\cdot2\cdot\frac15=\frac{4\pi}{15}.

$$

$\blacksquare$
### 习题二

（习题 8.4-2）计算 $\displaystyle\iiint_\Omega\left(x+y+z\right)\,\mathrm{d}V$, 其中

$$
\Omega=\left\{\left(x,y,z\right):x^2+y^2\le4,0\le z\le1\right\}.
$$

### 解答 习题二

$\Omega$ 关于平面 $x=0$ 与 $y=0$ 对称, 而被积函数中 $x$ 关于 $x$ 为奇函数, $y$ 关于 $y$ 为奇函数, 故 $\iiint x\,\mathrm{d}V=\iiint y\,\mathrm{d}V=0$. 于是

$$
\iiint_\Omega\left(x+y+z\right)\,\mathrm{d}V=\iiint_\Omega z\,\mathrm{d}V.
$$

用柱坐标 $x=r\cos\theta$, $y=r\sin\theta$, 由**定理 4.4**,

$$
\iiint_\Omega z\,\mathrm{d}V=\int_0^1 z\,\mathrm{d}z\int_0^{2\pi}\mathrm{d}\theta\int_0^2 r\,\mathrm{d}r=\frac12\cdot2\pi\cdot2=2\pi.

$$

$\blacksquare$
### 习题三

（习题 8.4-3）计算 $\displaystyle\iiint_\Omega\left(x+y+z\right)^3\,\mathrm{d}V$, 其中

$$
\Omega=\left\{\left(x,y,z\right):x^2+y^2+z^2\le R^2\right\}\ \left(R> 0\right).
$$

(提示: 注意利用积分区域的对称性.)

### 解答 习题三

展开被积函数:

$$
\left(x+y+z\right)^3=x^3+y^3+z^3+3x^2y+3x^2z+3y^2x+3y^2z+3z^2x+3z^2y+6xyz.
$$

球体 $\Omega$ 关于平面 $x=0$, $y=0$, $z=0$ 均对称. 上式每一项至少含有一个变量的奇次幂: $x^3,y^3,z^3$ 分别关于相应变量为奇函数; $3x^2y,3x^2z,\dots,3z^2y$ 分别关于 $y,z,x,\dots,y$ 为奇函数; $6xyz$ 关于每个变量均为奇函数. 故各项在 $\Omega$ 上的积分均为 $0$.

$$
\iiint_\Omega\left(x+y+z\right)^3\,\mathrm{d}V=0.

$$

$\blacksquare$
### 习题四

（习题 8.4-5）计算 $\displaystyle\iiint_\Omega\left(x^2+y^2+z^2\right)\,\mathrm{d}V$, 其中

$$
\Omega=\left\{\left(x,y,z\right):a^2\le x^2+y^2+z^2\le b^2\right\}\ \left(0< a< b\right).
$$

### 解答 习题四

由**定理 4.4** 用球坐标, $\Omega$ 变为 $a\le\rho\le b$, $0\le\varphi\le\pi$, $0\le\theta\le2\pi$, 故

$$
\iiint_\Omega\left(x^2+y^2+z^2\right)\,\mathrm{d}V=\int_0^{2\pi}\mathrm{d}\theta\int_0^\pi\sin\varphi\,\mathrm{d}\varphi\int_a^b\rho^2\cdot\rho^2\,\mathrm{d}\rho=2\pi\cdot2\cdot\frac{b^5-a^5}{5}=\frac{4\pi}{5}\left(b^5-a^5\right).

$$

$\blacksquare$
### 习题五

（习题 8.4-6）计算 $\displaystyle\iiint_\Omega\left(x^2+y^2\right)\,\mathrm{d}V$, 其中

$$
\Omega=\left\{\left(x,y,z\right):x^2+y^2\le z\le1\right\}.
$$

### 解答 习题五

$\Omega$ 在 $Oxy$ 平面上的投影为

$$
D=\left\{\left(x,y\right):x^2+y^2\le1\right\}.
$$

用柱坐标, 由**定理 4.2** 与**定理 4.4**,

$$
\begin{aligned}\iiint_\Omega\left(x^2+y^2\right)\,\mathrm{d}V&=\int_0^{2\pi}\mathrm{d}\theta\int_0^1 r\,\mathrm{d}r\int_{r^2}^1 r^2\,\mathrm{d}z\\&=2\pi\int_0^1 r^3\left(1-r^2\right)\,\mathrm{d}r=2\pi\left(\frac14-\frac16\right)=\frac\pi6.\end{aligned}

$$

$\blacksquare$
### 习题六

（习题 8.4-8）计算 $\displaystyle\iiint_\Omega\left(x^2+y^2\right)^2\,\mathrm{d}V$, 其中 $\Omega$ 为 $z=\sqrt{1-x^2-y^2}$ 与 $z=\sqrt{x^2+y^2}$ 所围区域.

### 解答 习题六

两曲面 $z=\sqrt{1-r^2}$ 与 $z=r$ 相交于 $r=1/\sqrt2$. 在球坐标下, 锥面 $z=r$ 对应 $\varphi=\pi/4$, 上半球面对应 $\rho=1$. 故 $\Omega$ 变为 $0\le\rho\le1$, $0\le\varphi\le\pi/4$, $0\le\theta\le2\pi$. 由**定理 4.4**,

$$
\begin{aligned}\iiint_\Omega\left(x^2+y^2\right)^2\,\mathrm{d}V&=\int_0^{2\pi}\mathrm{d}\theta\int_0^{\pi/4}\sin\varphi\,\mathrm{d}\varphi\int_0^1\left(\rho^2\sin^2\varphi\right)^2\cdot\rho^2\,\mathrm{d}\rho\\&=2\pi\int_0^{\pi/4}\sin^5\varphi\,\mathrm{d}\varphi\cdot\frac17.\end{aligned}
$$

令 $u=\cos\varphi$,

$$
\int\sin^5\varphi\,\mathrm{d}\varphi=-\int\left(1-2u^2+u^4\right)\mathrm{d}u=-u+\frac23u^3-\frac15u^5.
$$

代入上下限:

$$
\int_0^{\pi/4}\sin^5\varphi\,\mathrm{d}\varphi=\frac8{15}-\frac{43\sqrt2}{120}.
$$

故

$$
\iiint_\Omega\left(x^2+y^2\right)^2\,\mathrm{d}V=\frac{2\pi}{7}\left(\frac8{15}-\frac{43\sqrt2}{120}\right)=\frac{\pi\left(64-43\sqrt2\right)}{420}.

$$

$\blacksquare$
### 习题七

（习题 8.4-9）计算 $\displaystyle\iiint_\Omega\sqrt{x^2+y^2+z^2}\,\mathrm{d}V$, 其中 $\Omega$ 为球面 $x^2+y^2+z^2=x$ 之内部.

### 解答 习题七

球面方程 $x^2+y^2+z^2=x$ 在球坐标下化为 $\rho^2=\rho\sin\varphi\cos\theta$, 即 $\rho=\sin\varphi\cos\theta$. 由 $\rho\ge0$ 得 $\sin\varphi\cos\theta\ge0$, 即 $\theta\in\left[-\pi/2,\pi/2\right]$. 由**定理 4.4**,

$$
\begin{aligned}\iiint_\Omega\sqrt{x^2+y^2+z^2}\,\mathrm{d}V&=\int_{-\pi/2}^{\pi/2}\mathrm{d}\theta\int_0^\pi\sin\varphi\,\mathrm{d}\varphi\int_0^{\sin\varphi\cos\theta}\rho\cdot\rho^2\,\mathrm{d}\rho\\&=\frac14\int_{-\pi/2}^{\pi/2}\cos^4\theta\,\mathrm{d}\theta\int_0^\pi\sin^5\varphi\,\mathrm{d}\varphi.\end{aligned}
$$

其中 $\int_{-\pi/2}^{\pi/2}\cos^4\theta\,\mathrm{d}\theta=\frac{3\pi}{8}$, $\int_0^\pi\sin^5\varphi\,\mathrm{d}\varphi=\frac{16}{15}$. 故

$$
\iiint_\Omega\sqrt{x^2+y^2+z^2}\,\mathrm{d}V=\frac14\cdot\frac{3\pi}{8}\cdot\frac{16}{15}=\frac\pi{10}.

$$

$\blacksquare$
### 习题八

（习题 8.4-10）计算 $\displaystyle\iiint_\Omega\left(x+1\right)\left(y+1\right)\,\mathrm{d}V$, 其中 $\Omega$ 为椭球体 $\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}\le1$ ($a> 0,b> 0,c> 0$).

### 解答 习题八

展开被积函数:

$$
\left(x+1\right)\left(y+1\right)=xy+x+y+1.
$$
椭球体 $\Omega$ 关于平面 $x=0$, $y=0$, $z=0$ 均对称. $xy$ 关于 $x$ (或 $y$) 为奇函数, $x$ 关于 $x$ 为奇函数, $y$ 关于 $y$ 为奇函数, 故

$$
\iiint xy=\iiint x=\iiint y=0.
$$

于是

$$
\iiint_\Omega\left(x+1\right)\left(y+1\right)\,\mathrm{d}V=\iiint_\Omega 1\,\mathrm{d}V=m\left(\Omega\right).
$$

椭球体体积为 $\frac{4\pi abc}{3}$, 故

$$
\iiint_\Omega\left(x+1\right)\left(y+1\right)\,\mathrm{d}V=\frac{4\pi abc}{3}.

$$

$\blacksquare$