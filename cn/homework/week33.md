# week33

> **定理 1.2 (光滑曲线的弧长公式)**<br>设空间曲线 $L$ 的参数方程为 $x=x\left(t\right)$, $y=y\left(t\right)$, $z=z\left(t\right)$ ($\alpha\le t\le\beta$), 且导数连续. 则弧长 $s=\int_\alpha^\beta\sqrt{\left[x'\left(t\right)\right]^2+\left[y'\left(t\right)\right]^2+\left[z'\left(t\right)\right]^2}\,\mathrm dt$.

> **定理 1.3 (第一型曲线积分的计算)**<br>$\int_L f\left(x,y,z\right)\,\mathrm ds=\int_\alpha^\beta f\left(x\left(t\right),y\left(t\right),z\left(t\right)\right)\sqrt{\left[x'\right]^2+\left[y'\right]^2+\left[z'\right]^2}\,\mathrm dt$.

---

## 9.1-1

求旋轮线第一拱 $x=a\left(t-\sin t\right)$, $y=a\left(1-\cos t\right)$ ($0\le t\le2\pi$) 的弧长.

### 解答 9.1-1

$x'=a\left(1-\cos t\right)$, $y'=a\sin t$. 由**定理 1.2 (光滑曲线的弧长公式)**,

$$
\mathrm ds=2a\sin\frac t2\,\mathrm dt.
$$

故 $s=\int_0^{2\pi}2a\sin\frac t2\,\mathrm dt=8a$. $\blacksquare$

---

## 9.1-3

求阿基米德螺线 $x=at\cos t$, $y=at\sin t$ ($0\le t\le2\pi$) 的弧长.

### 解答 9.1-3

由**定理 1.2 (光滑曲线的弧长公式)**, $\mathrm ds=a\sqrt{1+t^2}\,\mathrm dt$. 故

$$
s=a\pi\sqrt{1+4\pi^2}+\frac a2\ln\left(2\pi+\sqrt{1+4\pi^2}\right).
$$

$\blacksquare$

---

## 9.1-4

求 $\oint_L xy\,\mathrm ds$, 其中 $L$ 为正方形 $\left|x\right|+\left|y\right|=a$.

### 解答 9.1-4

$L$ 关于 $x$ 轴对称, 而 $xy$ 关于 $y$ 为奇函数. 故对称两段上的积分互为相反数, 相互抵消.

$$
\oint_L xy\,\mathrm ds=0.
$$

$\blacksquare$

---

## 9.1-7

求 $\int_L xy\,\mathrm ds$, 其中 $L$ 为椭圆 $\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$ 在第一象限部分.

### 解答 9.1-7

取参数方程 $x=a\cos t$, $y=b\sin t$. 由**定理 1.3 (第一型曲线积分的计算)**,

$$
\int_L xy\,\mathrm ds=\frac{ab\left(a^2+ab+b^2\right)}{3\left(a+b\right)}.
$$

$\blacksquare$

---

## 9.1-8

求 $\int_L x^2\,\mathrm ds$, 其中 $L$ 为给定的空间曲线.

### 解答 9.1-8

计算弧微元得 $\mathrm ds=a\,\mathrm dt$. 由**定理 1.3 (第一型曲线积分的计算)**, 利用 $\int_0^{2\pi}\cos^2t\,\mathrm dt=\pi$, $\int_0^{2\pi}\sin t\cos t\,\mathrm dt=0$, 得

$$
\int_L x^2\,\mathrm ds=\frac{2\pi a^3}{3}.
$$

$\blacksquare$
