# week22

> **定理 1.1 (柯西收敛原理)**
> 
> $\int_a^{+\infty}f\left(x\right)\mathrm{d}x$ 收敛的充要条件是: 对任意 $\varepsilon>0$, 存在 $X>0$, 使 $\left|\int_{A'}^{A''}f\left(x\right)\mathrm{d}x\right|<\varepsilon$ ($A',A''>X$).

> **定理 1.3 (比较判别法)**
> 
> 若 $0\le{f}\left(x\right)\le{g}\left(x\right)$ ($x\ge{X}_0$), 则 $\int{g}$ 收敛蕴含 $\int{f}$ 收敛, $\int{f}$ 发散蕴含 $\int{g}$ 发散.

> **定理 1.6 (狄利克雷判别法)**
> 
> 若 $f\left(x\right)$ 单调趋于零, 且 $\int_a^Ag\left(x\right)\mathrm{d}x$ 对任意 $A$ 有界, 则 $\int_a^{+\infty}f\left(x\right)g\left(x\right)\mathrm{d}x$ 收敛.

> **定理 3.3 (积分号下求导)**
> 
> 设 $f\left(x,y\right)$ 与 $f_y\left(x,y\right)$ 连续, 则 $I\left(y\right)=\int_a^bf\left(x,y\right)\mathrm{d}x$ 可导, 且 $I'\left(y\right)=\int_a^bf_y\left(x,y\right)\mathrm{d}x$. 若积分限依赖于 $y$, 则补上边界项: $I'\left(y\right)=f\left(b\left(y\right),y\right)b'\left(y\right)-f\left(a\left(y\right),y\right)a'\left(y\right)+\int_{a\left(y\right)}^{b\left(y\right)}f_y\left(x,y\right)\mathrm{d}x$.

## 12.2-2-1

讨论 $\int_0^{+\infty}\frac{\mathrm{d}x}{\sqrt{x}\left(1+x\right)}$.

### 解答 12.2-2-1

在 $x=0$ 附近与 $\frac1{\sqrt{x}}$ 同阶, 由**例 2.2 (瑕 p-积分)** 收敛; 在 $+\infty$ 与 $\frac1{x^{3/2}}$ 同阶, 收敛. 故收敛, 值为 $\pi$.

$\blacksquare$

## 12.2-2-3

讨论 $\int_0^{+\infty}\frac{\mathrm{d}x}{x^p+x^q}$.

### 解答 12.2-2-3

$x=0$ 端收敛当且仅当 $\min\left(p,q\right)<1$; $+\infty$ 端收敛当且仅当 $\max\left(p,q\right)>1$. 故收敛当且仅当 $\min\left(p,q\right)<1<\max\left(p,q\right)$.

$\blacksquare$

## 12.2-2-5

讨论 $\int_0^{\pi/2}\frac{\mathrm{d}x}{\sin^2x\cos^2x}$.

### 解答 12.2-2-5

在 $x=0$ 附近与 $\frac1{x^2}$ 同阶, 由**例 2.2 (瑕 p-积分)**, $p=2\ge1$, 发散.

$\blacksquare$

## 12.2-2-7

讨论 $\int_0^1x^p\left(1-x\right)^q\mathrm{d}x$ ($p>0,q>0$).

### 解答 12.2-2-7

在 $x=0$ 附近与 $x^p$ 同阶 ($p>0$ 故收敛); 在 $x=1$ 附近与 $\left(1-x\right)^q$ 同阶 ($q>0$ 故收敛). 故对一切 $p>0,q>0$ 收敛.

$\blacksquare$

## 12.2-3

证明: 若 $\int_a^bf^2$ 收敛, 则 $\int_a^bf$ 绝对收敛. 反之是否成立?

### 解答 12.2-3

由 $2\left|f\right|\le1+f^2$, 得 $\left|f\right|\le\frac12+\frac{f^2}2$. 由绝对收敛与条件收敛的定义, 绝对收敛. 反之不然, 反例 $f\left(x\right)=\frac1{\sqrt{x}}$.

$\blacksquare$

## 12.2-4-1

判断 $\int_0^2\frac{\mathrm{d}x}{x-1}$ 是否在柯西主值意义下收敛.

### 解答 12.2-4-1

由柯西主值的定义, $\mathrm{CPV}=\lim_{\eta\to0+}\left(\ln\eta-\ln1+\ln1-\ln\eta\right)=0$. 收敛且主值为 $0$.

$\blacksquare$

## 12.2-4-2

判断 $\int_{1/2}^2\frac{\mathrm{d}x}{x\ln{x}}$ 是否在柯西主值意义下收敛.

### 解答 12.2-4-2

由柯西主值的定义, 主值 $=\lim_{\eta\to0+}\ln\frac{-\ln\left(1-\eta\right)}{\ln\left(1+\eta\right)}=\ln1=0$. 收敛且主值为 $0$.

$\blacksquare$

## 12.3-2-5

求 $I\left(y\right)=\int_{\sin{y}}^{\cos{y}}e^{y\sqrt{1-x^2}}\mathrm{d}x$ 的导数.

### 解答 12.3-2-5

由**定理 3.3 (积分号下求导)**,

$$
I'\left(y\right)=\int_{\sin{y}}^{\cos{y}}\sqrt{1-x^2}e^{y\sqrt{1-x^2}}\mathrm{d}x-e^{y\sin{y}}\sin{y}-e^{y\cos{y}}\cos{y}.
$$

$\blacksquare$

## 12.3-2-6

求 $I\left(y\right)=\int_0^{x/y}y\sin\left(xy\right)\mathrm{d}x$ 的导数.

### 解答 12.3-2-6

由**定理 3.3 (积分号下求导)**, 边界项与积分项相消, 得 $I'\left(y\right)=0$.

$\blacksquare$

## 12.3-2-7

求 $I\left(y\right)=\int_0^{y^2}\sin\left(x^2+y^2\right)\mathrm{d}x$ 的导数.

### 解答 12.3-2-7

由**定理 3.3 (积分号下求导)**, $I'\left(y\right)=\int_0^{y^2}2y\cos\left(x^2+y^2\right)\mathrm{d}x+2y\sin\left(y^4+y^2\right)$.

$\blacksquare$

## 12.3-2-8

求 $I\left(y\right)=\int_0^y\frac{\ln\left(1+xy\right)}x\mathrm{d}x$ 的导数.

### 解答 12.3-2-8

由**定理 3.3 (积分号下求导)**, $I'\left(y\right)=\frac{\ln\left(1+y^2\right)}y+\int_0^y\frac{\mathrm{d}x}{1+xy}$.

$\blacksquare$

## 12.3-4-1

计算 $I\left(r\right)=\int_0^\pi\ln\left(1-2r\cos{x}+r^2\right)\mathrm{d}x$ ($\left|r\right|<1$).

### 解答 12.3-4-1

由**定理 3.3 (积分号下求导)**, $I'\left(r\right)=\int_0^\pi\frac{2r-2\cos{x}}{1-2r\cos{x}+r^2}\mathrm{d}x$. 利用标准积分 $\int_0^\pi\frac{\mathrm{d}x}{1-2r\cos{x}+r^2}=\frac\pi{1-r^2}$, 得 $I'\left(r\right)=0$. 又 $I\left(0\right)=0$, 故 $I\left(r\right)=0$.

$\blacksquare$

## 12.3-6

设 $I\left(\alpha\right)=\int_0^{2\pi}\ln\left(1-\alpha\cos\theta\right)\mathrm{d}\theta$ ($\left|\alpha\right|<1$). 证明 $I'\left(\alpha\right)=\frac{2\pi\left(\sqrt{1-\alpha^2}-1\right)}{\alpha\sqrt{1-\alpha^2}}$ 并推出 $I\left(\alpha\right)=2\pi\ln\frac{1+\sqrt{1-\alpha^2}}2$.

### 解答 12.3-6

由**定理 3.3 (积分号下求导)**, $I'\left(\alpha\right)=\int_0^{2\pi}\frac{-\cos\theta}{1-\alpha\cos\theta}\mathrm{d}\theta$. 分解被积函数并利用标准积分 $\int_0^{2\pi}\frac{\mathrm{d}\theta}{1-\alpha\cos\theta}=\frac{2\pi}{\sqrt{1-\alpha^2}}$, 得 $I'\left(\alpha\right)=\frac{2\pi\left(\sqrt{1-\alpha^2}-1\right)}{\alpha\sqrt{1-\alpha^2}}$. 积分并利用 $I\left(0\right)=0$, 得 $I\left(\alpha\right)=2\pi\ln\frac{1+\sqrt{1-\alpha^2}}2$.

$\blacksquare$

## 12.4-1-1

讨论 $\int_0^{+\infty}e^{-\alpha{x}^2}\mathrm{d}x$ 在 $\alpha\in\left[\alpha_0,+\infty\right)$ 上的一致收敛性.

### 解答 12.4-1-1

因 $e^{-\alpha{x}^2}\le{e}^{-\alpha_0x^2}$, 及**定理 4.3 (魏尔斯特拉斯判别法)**, 一致收敛.

$\blacksquare$

## 12.4-1-3

讨论 $\int_1^{+\infty}e^{-xy}\frac{\cos{x}}{x}\mathrm{d}x$ 在 $y\in\left[0,+\infty\right)$ 上的一致收敛性.

### 解答 12.4-1-3

$\int_1^{+\infty}\frac{\cos{x}}{x}\mathrm{d}x$ 收敛且不含 $y$, $e^{-xy}$ 单调且一致有界. 由**定理 4.4 (阿贝尔判别法)**, 一致收敛.

$\blacksquare$
