# week48

> **定理 3.3 (积分号下求导)**<br>设 $f\left(x,y\right)$ 与 $f_y\left(x,y\right)$ 连续, 则 $I\left(y\right)=\int_a^b f\left(x,y\right)\mathrm dx$ 可导, 且 $I'\left(y\right)=\int_a^b f_y\left(x,y\right)\mathrm dx$. 若积分限依赖于 $y$, 则补上边界项: $I'\left(y\right)=f\left(b\left(y\right),y\right)b'\left(y\right)-f\left(a\left(y\right),y\right)a'\left(y\right)+\int_{a\left(y\right)}^{b\left(y\right)}f_y\left(x,y\right)\mathrm dx$.

---

## 12.3-2-5

求 $I\left(y\right)=\int_{\sin y}^{\cos y}e^{y\sqrt{1-x^2}}\mathrm dx$ 的导数.

### 解答 12.3-2-5

由**定理 3.3 (积分号下求导)**,

$$
I'\left(y\right)=\int_{\sin y}^{\cos y}\sqrt{1-x^2}e^{y\sqrt{1-x^2}}\mathrm dx-e^{y\sin y}\sin y-e^{y\cos y}\cos y.
$$

$\blacksquare$

---

## 12.3-2-6

求 $I\left(y\right)=\int_0^{x/y}y\sin\left(xy\right)\mathrm dx$ 的导数.

### 解答 12.3-2-6

由**定理 3.3 (积分号下求导)**, 边界项与积分项相消, 得 $I'\left(y\right)=0$. $\blacksquare$

---

## 12.3-2-7

求 $I\left(y\right)=\int_0^{y^2}\sin\left(x^2+y^2\right)\mathrm dx$ 的导数.

### 解答 12.3-2-7

由**定理 3.3 (积分号下求导)**, $I'\left(y\right)=\int_0^{y^2}2y\cos\left(x^2+y^2\right)\mathrm dx+2y\sin\left(y^4+y^2\right)$. $\blacksquare$

---

## 12.3-2-8

求 $I\left(y\right)=\int_0^y\frac{\ln\left(1+xy\right)}x\mathrm dx$ 的导数.

### 解答 12.3-2-8

由**定理 3.3 (积分号下求导)**, $I'\left(y\right)=\frac{\ln\left(1+y^2\right)}y+\int_0^y\frac{\mathrm dx}{1+xy}$. $\blacksquare$

---

## 12.3-4-1

计算 $I\left(r\right)=\int_0^\pi\ln\left(1-2r\cos x+r^2\right)\mathrm dx$ ($\left|r\right|< 1$).

### 解答 12.3-4-1

由**定理 3.3 (积分号下求导)**, $I'\left(r\right)=\int_0^\pi\frac{2r-2\cos x}{1-2r\cos x+r^2}\mathrm dx$. 利用标准积分 $\int_0^\pi\frac{\mathrm dx}{1-2r\cos x+r^2}=\frac\pi{1-r^2}$, 得 $I'\left(r\right)=0$. 又 $I\left(0\right)=0$, 故 $I\left(r\right)=0$. $\blacksquare$

---

## 12.3-6

设 $I\left(\alpha\right)=\int_0^{2\pi}\ln\left(1-\alpha\cos\theta\right)\mathrm d\theta$ ($\left|\alpha\right|< 1$). 证明 $I'\left(\alpha\right)=\frac{2\pi\left(\sqrt{1-\alpha^2}-1\right)}{\alpha\sqrt{1-\alpha^2}}$ 并推出 $I\left(\alpha\right)=2\pi\ln\frac{1+\sqrt{1-\alpha^2}}2$.

### 解答 12.3-6

由**定理 3.3 (积分号下求导)**, $I'\left(\alpha\right)=\int_0^{2\pi}\frac{-\cos\theta}{1-\alpha\cos\theta}\mathrm d\theta$. 分解被积函数并利用标准积分 $\int_0^{2\pi}\frac{\mathrm d\theta}{1-\alpha\cos\theta}=\frac{2\pi}{\sqrt{1-\alpha^2}}$, 得 $I'\left(\alpha\right)=\frac{2\pi\left(\sqrt{1-\alpha^2}-1\right)}{\alpha\sqrt{1-\alpha^2}}$. 积分并利用 $I\left(0\right)=0$, 得 $I\left(\alpha\right)=2\pi\ln\frac{1+\sqrt{1-\alpha^2}}2$. $\blacksquare$
