# week34

> **定理 1.1 (柯西收敛原理)**
> 
> $\int_a^{+\infty}f\left(x\right)\mathrm dx$ 收敛的充要条件是: 对任意 $\varepsilon> 0$, 存在 $X> 0$, 使 $\left|\int_{A'}^{A''}f\left(x\right)\mathrm dx\right|< \varepsilon$ ($A',A''> X$).

> **例 1.2 (p-积分)**
> 
> $\int_1^{+\infty}\frac{\mathrm dx}{x^p}$ 当 $p> 1$ 时收敛, 当 $p\le1$ 时发散.

> **定理 1.3 (比较判别法)**
> 
> 若 $0\le f\left(x\right)\le g\left(x\right)$ ($x\ge X_0$), 则 $\int g$ 收敛蕴含 $\int f$ 收敛, $\int f$ 发散蕴含 $\int g$ 发散.

> **定理 1.6 (狄利克雷判别法)**
> 
> 若 $f\left(x\right)$ 单调趋于零, 且 $\int_a^A g\left(x\right)\mathrm dx$ 对任意 $A$ 有界, 则 $\int_a^{+\infty}f\left(x\right)g\left(x\right)\mathrm dx$ 收敛.

> **例 2.2 (瑕 p-积分)**
> 
> $\int_a^b\frac{\mathrm dx}{\left(x-a\right)^p}$ 当 $p< 1$ 时收敛, 当 $p\ge1$ 时发散.

> **定理 3.3 (积分号下求导)**
> 
> 设 $f\left(x,y\right)$ 与 $f_y\left(x,y\right)$ 连续, 则 $I\left(y\right)=\int_a^b f\left(x,y\right)\mathrm dx$ 可导, 且 $I'\left(y\right)=\int_a^b f_y\left(x,y\right)\mathrm dx$. 若积分限依赖于 $y$, 则补上边界项: $I'\left(y\right)=f\left(b\left(y\right),y\right)b'\left(y\right)-f\left(a\left(y\right),y\right)a'\left(y\right)+\int_{a\left(y\right)}^{b\left(y\right)}f_y\left(x,y\right)\mathrm dx$.

## 12.1-3

证明 $I_1\left(x\right)=\int_0^{+\infty}e^{-xt}\sin t\mathrm dt$ 与 $I_2\left(x\right)=\int_0^{+\infty}e^{-xt}\cos t\mathrm dt$ 绝对收敛并求值.

### 解答 12.1-3

由 $\left|e^{-xt}\sin t\right|\le e^{-xt}$ 及**定理 1.3 (比较判别法)**, 绝对收敛. 分部积分联立方程解得 $I_1=\frac1{x^2+1}$, $I_2=\frac x{x^2+1}$. $\blacksquare$

## 12.1-4

证明 $\int_{-\infty}^{+\infty}f\left(-x\right)\mathrm dx=\int_{-\infty}^{+\infty}f\left(x\right)\mathrm dx$ 及 $\int_{-\infty}^{+\infty}f\left(x+a\right)\mathrm dx=\int_{-\infty}^{+\infty}f\left(x\right)\mathrm dx$.

### 解答 12.1-4

作代换 $u=-x$ 与 $u=x+a$, 由无穷积分收敛的定义, 等式成立. $\blacksquare$

## 12.1-5

设 $a_n=\int_n^{n+1}f\left(x\right)\mathrm dx$. 证明 $\int_1^{+\infty}f\left(x\right)\mathrm dx$ 收敛当且仅当 $\sum a_n$ 收敛.

### 解答 12.1-5

$\sum_{n=1}^N a_n=\int_1^{N+1}f\left(x\right)\mathrm dx$. 由 $f\left(x\right)\to0$, 相邻整数点之间的积分差趋于零. 由无穷积分收敛的定义, 等价成立. $\blacksquare$

## 12.2-1-1

判断 $\int_0^1\ln x\mathrm dx$ 的收敛性.

### 解答 12.2-1-1

分部积分得 $-1-\eta\ln\eta+\eta\to-1$. 由瑕积分收敛的定义, 收敛且值为 $-1$. $\blacksquare$

## 12.2-1-3

判断 $\int_{-1}^1\frac{\mathrm dx}{\sqrt{1-x^2}}$.

### 解答 12.2-1-3

拆为两段, 各趋于 $\frac\pi2$. 收敛且值为 $\pi$. $\blacksquare$

## 12.2-1-5

判断 $\int_0^1\frac{\mathrm dx}{x\ln^2x}$.

### 解答 12.2-1-5

代换 $u=\ln x$, 得 $-\frac1{\ln\left(1-\eta\right)}+\frac1{\ln\left(1/2\right)}\to+\infty$. 发散. $\blacksquare$

## 12.2-2-1

讨论 $\int_0^{+\infty}\frac{\mathrm dx}{\sqrt x\left(1+x\right)}$.

### 解答 12.2-2-1

在 $x=0$ 附近与 $\frac1{\sqrt x}$ 同阶, 由**例 2.2 (瑕 p-积分)** 收敛; 在 $+\infty$ 与 $\frac1{x^{3/2}}$ 同阶, 收敛. 故收敛, 值为 $\pi$. $\blacksquare$

## 12.2-2-3

讨论 $\int_0^{+\infty}\frac{\mathrm dx}{x^p+x^q}$.

### 解答 12.2-2-3

$x=0$ 端收敛当且仅当 $\min\left(p,q\right)< 1$; $+\infty$ 端收敛当且仅当 $\max\left(p,q\right)> 1$. 故收敛当且仅当 $\min\left(p,q\right)< 1< \max\left(p,q\right)$. $\blacksquare$

## 12.2-2-5

讨论 $\int_0^{\pi/2}\frac{\mathrm dx}{\sin^2x\cos^2x}$.

### 解答 12.2-2-5

在 $x=0$ 附近与 $\frac1{x^2}$ 同阶, 由**例 2.2 (瑕 p-积分)**, $p=2\ge1$, 发散. $\blacksquare$

## 12.2-2-7

讨论 $\int_0^1 x^p\left(1-x\right)^q\mathrm dx$ ($p> 0,q> 0$).

### 解答 12.2-2-7

在 $x=0$ 附近与 $x^p$ 同阶 ($p> 0$ 故收敛); 在 $x=1$ 附近与 $\left(1-x\right)^q$ 同阶 ($q> 0$ 故收敛). 故对一切 $p> 0,q> 0$ 收敛. $\blacksquare$

## 12.2-3

证明: 若 $\int_a^b f^2$ 收敛, 则 $\int_a^b f$ 绝对收敛. 反之是否成立?

### 解答 12.2-3

由 $2\left|f\right|\le1+f^2$, 得 $\left|f\right|\le\frac12+\frac{f^2}2$. 由绝对收敛与条件收敛的定义, 绝对收敛. 反之不然, 反例 $f\left(x\right)=\frac1{\sqrt x}$. $\blacksquare$

## 12.2-4-1

判断 $\int_0^2\frac{\mathrm dx}{x-1}$ 是否在柯西主值意义下收敛.

### 解答 12.2-4-1

由柯西主值的定义, $\mathrm{CPV}=\lim_{\eta\to0+}\left(\ln\eta-\ln1+\ln1-\ln\eta\right)=0$. 收敛且主值为 $0$. $\blacksquare$

## 12.2-4-2

判断 $\int_{1/2}^2\frac{\mathrm dx}{x\ln x}$ 是否在柯西主值意义下收敛.

### 解答 12.2-4-2

由柯西主值的定义, 主值 $=\lim_{\eta\to0+}\ln\frac{-\ln\left(1-\eta\right)}{\ln\left(1+\eta\right)}=\ln1=0$. 收敛且主值为 $0$. $\blacksquare$

## 12.3-2-5

求 $I\left(y\right)=\int_{\sin y}^{\cos y}e^{y\sqrt{1-x^2}}\mathrm dx$ 的导数.

### 解答 12.3-2-5

由**定理 3.3 (积分号下求导)**,

$$
I'\left(y\right)=\int_{\sin y}^{\cos y}\sqrt{1-x^2}e^{y\sqrt{1-x^2}}\mathrm dx-e^{y\sin y}\sin y-e^{y\cos y}\cos y.
$$

$\blacksquare$

## 12.3-2-6

求 $I\left(y\right)=\int_0^{x/y}y\sin\left(xy\right)\mathrm dx$ 的导数.

### 解答 12.3-2-6

由**定理 3.3 (积分号下求导)**, 边界项与积分项相消, 得 $I'\left(y\right)=0$. $\blacksquare$

## 12.3-2-7

求 $I\left(y\right)=\int_0^{y^2}\sin\left(x^2+y^2\right)\mathrm dx$ 的导数.

### 解答 12.3-2-7

由**定理 3.3 (积分号下求导)**, $I'\left(y\right)=\int_0^{y^2}2y\cos\left(x^2+y^2\right)\mathrm dx+2y\sin\left(y^4+y^2\right)$. $\blacksquare$

## 12.3-2-8

求 $I\left(y\right)=\int_0^y\frac{\ln\left(1+xy\right)}x\mathrm dx$ 的导数.

### 解答 12.3-2-8

由**定理 3.3 (积分号下求导)**, $I'\left(y\right)=\frac{\ln\left(1+y^2\right)}y+\int_0^y\frac{\mathrm dx}{1+xy}$. $\blacksquare$

## 12.3-4-1

计算 $I\left(r\right)=\int_0^\pi\ln\left(1-2r\cos x+r^2\right)\mathrm dx$ ($\left|r\right|< 1$).

### 解答 12.3-4-1

由**定理 3.3 (积分号下求导)**, $I'\left(r\right)=\int_0^\pi\frac{2r-2\cos x}{1-2r\cos x+r^2}\mathrm dx$. 利用标准积分 $\int_0^\pi\frac{\mathrm dx}{1-2r\cos x+r^2}=\frac\pi{1-r^2}$, 得 $I'\left(r\right)=0$. 又 $I\left(0\right)=0$, 故 $I\left(r\right)=0$. $\blacksquare$
