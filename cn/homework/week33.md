# 作业 33

> **定理 1.2**（光滑曲线的弧长公式）设空间曲线 $L$ 的参数方程为 $x=x\left(t\right)$, $y=y\left(t\right)$, $z=z\left(t\right)$ ($\alpha\le t\le\beta$), 且 $x'\left(t\right),y'\left(t\right),z'\left(t\right)$ 在 $\left[\alpha,\beta\right]$ 上连续. 则 $L$ 可求长, 且弧长

$$
s=\int_\alpha^\beta\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm{d}t.
$$

弧微分

$$
\mathrm{d}s=\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm{d}t.
$$

> **定理 1.3**（第一型曲线积分的计算）设 $L$ 为光滑曲线, 参数方程同上, $f\left(x,y,z\right)$ 在 $L$ 上连续, 则

$$
\int_L f\left(x,y,z\right)\,\mathrm{d}s=\int_\alpha^\beta f\left(x\left(t\right),y\left(t\right),z\left(t\right)\right)\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm{d}t.
$$

注意上限 $\beta$ 须大于下限 $\alpha$.

### 习题一

（习题 9.1-1）求旋轮线第一拱

$$
\begin{cases}x=a\left(t-\sin t\right),\y=a\left(1-\cos t\right),\end{cases}\left(0\le t\le2\pi\right)
$$

的弧长, 其中 $a> 0$.

### 解答 习题一

$x'\left(t\right)=a\left(1-\cos t\right)$, $y'\left(t\right)=a\sin t$. 由**定理 1.2**,

$$
\mathrm{d}s=\sqrt{a^2\left(1-\cos t\right)^2+a^2\sin^2t}\,\mathrm{d}t=a\sqrt{2-2\cos t}\,\mathrm{d}t=2a\sin\frac t2\,\mathrm{d}t.
$$

故弧长

$$
s=\int_0^{2\pi}2a\sin\frac t2\,\mathrm{d}t=2a\left[-2\cos\frac t2\right]_0^{2\pi}=8a.

$$

$\blacksquare$
### 习题二

（习题 9.1-3）求阿基米德螺线

$$
\begin{cases}x=at\cos t,\y=at\sin t,\end{cases}\left(0\le t\le2\pi\right)
$$

的弧长.

### 解答 习题二

$x'\left(t\right)=a\left(\cos t-t\sin t\right)$, $y'\left(t\right)=a\left(\sin t+t\cos t\right)$. 由**定理 1.2**,

$$
\mathrm{d}s=a\sqrt{\left(\cos t-t\sin t\right)^2+\left(\sin t+t\cos t\right)^2}\,\mathrm{d}t=a\sqrt{1+t^2}\,\mathrm{d}t.
$$

故弧长

$$
s=\int_0^{2\pi}a\sqrt{1+t^2}\,\mathrm{d}t=a\left[\frac t2\sqrt{1+t^2}+\frac12\ln\left(t+\sqrt{1+t^2}\right)\right]_0^{2\pi}=a\pi\sqrt{1+4\pi^2}+\frac a2\ln\left(2\pi+\sqrt{1+4\pi^2}\right).

$$

$\blacksquare$
### 习题三

（习题 9.1-4）求第一型曲线积分 $\displaystyle\oint_L xy\,\mathrm{d}s$, 其中 $L$ 为正方形: $\left| x\right|+\left| y\right|=a$ ($a> 0$).

### 解答 习题三

$L$ 关于 $x$ 轴对称 (即 $\left(x,y\right)\in L\Rightarrow\left(x,-y\right)\in L$), 而被积函数 $f\left(x,y\right)=xy$ 关于 $y$ 为奇函数: $f\left(x,-y\right)=-f\left(x,y\right)$. 在对称点处弧微元 $\mathrm{d}s$ 相同, 故对称两段上的积分值互为相反数, 相互抵消. 因此

$$
\oint_L xy\,\mathrm{d}s=0.

$$

$\blacksquare$
### 习题四

（习题 9.1-7）求 $\displaystyle\int_L xy\,\mathrm{d}s$, 其中 $L$ 为椭圆 $\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$ 在第一象限的部分.

### 解答 习题四

取参数方程 $x=a\cos t$, $y=b\sin t$ ($0\le t\le\pi/2$). 由**定理 1.3**,

$$
\mathrm{d}s=\sqrt{a^2\sin^2t+b^2\cos^2t}\,\mathrm{d}t.
$$

故

$$
\int_L xy\,\mathrm{d}s=\int_0^{\pi/2}ab\cos t\sin t\sqrt{a^2\sin^2t+b^2\cos^2t}\,\mathrm{d}t.
$$

令 $u=a^2\sin^2t+b^2\cos^2t$,

$$
\mathrm{d}u=2\left(a^2-b^2\right)\sin t\cos t\,\mathrm{d}t.
$$

当 $t=0$ 时 $u=b^2$, 当 $t=\pi/2$ 时 $u=a^2$. 于是

$$
\int_L xy\,\mathrm{d}s=\frac{ab}{2\left(a^2-b^2\right)}\int_{b^2}^{a^2}\sqrt u\,\mathrm{d}u=\frac{ab}{2\left(a^2-b^2\right)}\cdot\frac23\left(a^3-b^3\right)=\frac{ab\left(a^2+ab+b^2\right)}{3\left(a+b\right)}.

$$

$\blacksquare$
### 习题五

（习题 9.1-8）求 $\displaystyle\int_L x^2\,\mathrm{d}s$, 其中 $L$ 的参数方程为

$$
\begin{cases}
x=\frac a{\sqrt2}\left(\frac1{\sqrt3}\cos t-\sin t\right),\\[4pt\right]
y=\frac a{\sqrt2}\left(\frac1{\sqrt3}\cos t+\sin t\right),\\[4pt\right]
z=-\frac{\sqrt2}{\sqrt3}a\cos t,
\end{cases}\left(0\le t\le2\pi,a> 0\right).
$$

### 解答 习题五

求导:

$$
x'=\frac a{\sqrt2}\left(-\frac1{\sqrt3}\sin t-\cos t\right), y'=\frac a{\sqrt2}\left(-\frac1{\sqrt3}\sin t+\cos t\right), z'=\frac{\sqrt2}{\sqrt3}a\sin t.
$$

计算弧微元:

$$
\begin{aligned}\left[x'\right]^2+\left[y'\right]^2+\left[z'\right]^2&=\frac{a^2}{2}\left(\frac13\sin^2t+\frac2{\sqrt3}\sin t\cos t+\cos^2t\right)\\&\;+\frac{a^2}{2}\left(\frac13\sin^2t-\frac2{\sqrt3}\sin t\cos t+\cos^2t\right)+\frac{2a^2}{3}\sin^2t\\&=a^2\sin^2t+a^2\cos^2t=a^2.\end{aligned}
$$

故 $\mathrm{d}s=a\,\mathrm{d}t$. 又

$$
x^2=\frac{a^2}{2}\left(\frac1{\sqrt3}\cos t-\sin t\right)^2=\frac{a^2}{2}\left(\frac13\cos^2t-\frac2{\sqrt3}\sin t\cos t+\sin^2t\right).
$$

由**定理 1.3**, 注意到 $\int_0^{2\pi}\sin t\cos t\,\mathrm{d}t=0$,

$$
\int_0^{2\pi}\cos^2t\,\mathrm{d}t=\int_0^{2\pi}\sin^2t\,\mathrm{d}t=\pi,
$$

得

$$
\int_L x^2\,\mathrm{d}s=\int_0^{2\pi}x^2\cdot a\,\mathrm{d}t=\frac{a^3}{2}\left(\frac13\pi+\pi\right)=\frac{2\pi a^3}{3}.

$$

$\blacksquare$