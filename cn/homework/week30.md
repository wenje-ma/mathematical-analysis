# week30

> **定理 3.1 (二重积分的变量替换公式)**<br>设 $f$ 在 $D$ 上连续, 变换 $F:\left(u,v\right)\mapsto\left(x\left(u,v\right),y\left(u,v\right)\right)$ 是 $G$ 到 $D$ 的一一映射, 雅可比行列式 $J\left(u,v\right)\ne0$. 则 $\iint_D f\,\mathrm dx\mathrm dy=\iint_G f\left(x\left(u,v\right),y\left(u,v\right)\right)\left|J\left(u,v\right)\right|\,\mathrm du\mathrm dv$.

---

## 8.3-1

利用适当的坐标变换计算 $\iint_D\left(\sqrt{y/x}+\sqrt{xy}\right)\mathrm dx\mathrm dy$, 其中 $D$ 由 $xy=1$, $xy=9$, $y=x$, $y=4x$ 围成.

### 解答 8.3-1

令 $u=xy$, $v=y/x$. 则 $G=\left\{\left(u,v\right):1\le u\le9,1\le v\le4\right\}$. 逆变换 $x=\sqrt{u/v}$, $y=\sqrt{uv}$. 雅可比行列式 $\left|J\right|=\frac1{2v}$. 被积函数 $\sqrt{v}+\sqrt{u}$. 由**定理 3.1 (二重积分的变量替换公式)**,

$$
\iint_D\left(\sqrt{y/x}+\sqrt{xy}\right)=8+\frac{52}{3}\ln2.
$$

$\blacksquare$

---

## 8.3-4

计算 $\iint_D\left(x+y\right)\mathrm dx\mathrm dy$, 其中 $D$ 由 $y=4x^2$, $y=9x^2$, $x=4y^2$, $x=9y^2$ 围成.

### 解答 8.3-4

令 $u=y/x^2$, $v=x/y^2$. 则 $G=\left[4,9\right]\times\left[4,9\right]$. 逆变换 $x=u^{-2/3}v^{-1/3}$, $y=u^{-1/3}v^{-2/3}$. 雅可比行列式 $\left|J\right|=\frac1{3u^2v^2}$. 由**定理 3.1 (二重积分的变量替换公式)**,

$$
\iint_D\left(x+y\right)=\frac3{10}\left(9^{-5/3}-4^{-5/3}\right)\left(9^{-4/3}-4^{-4/3}\right).
$$

$\blacksquare$

---

## 8.3-6

求曲线 $\left(\frac{x^2}{a^2}+\frac{y^2}{b^2}\right)^2=\frac{xy}{c^2}$ 所围区域 $D$ 的面积.

### 解答 8.3-6

作广义极坐标变换 $x=ar\cos\theta$, $y=br\sin\theta$. 雅可比行列式 $\left|J\right|=abr$. 代入曲线方程得 $r^2=\frac{ab\sin2\theta}{2c^2}$. 由 $\sin2\theta\ge0$, $\theta\in\left[0,\pi/2\right]\cup\left[\pi,3\pi/2\right]$. 由**定理 3.1 (二重积分的变量替换公式)**,

$$
m\left(D\right)=\frac{a^2b^2}{2c^2}.
$$

$\blacksquare$
