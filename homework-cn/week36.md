# week36

> **定理 3.1 (狄利克雷收敛定理)**
> 
> 设 $f\left(x\right)$ 以 $2\pi$ 为周期且逐段单调有界, 则其傅里叶级数在每点 $x$ 收敛于 $\frac{f\left(x+0\right)+f\left(x-0\right)}2$.

> **定理 4.1 (贝塞尔不等式)**
> 
> $\frac{a_0^2}2+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right)\le\frac1\pi\int_{-\pi}^\pi{f}^2\left(x\right)\mathrm{d}x$, 特别地 $\sum{a}_n^2$ 与 $\sum{b}_n^2$ 均收敛.

> **定理 4.2 (封闭性方程/Parseval 等式)**
> 
> $\frac1\pi\int_{-\pi}^\pi{f}^2\left(x\right)\mathrm{d}x=\frac{a_0^2}2+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right)$.

> **命题 (伽马与贝塔的积分形式)**
> 
> $\int_0^{+\infty}\frac{x^{a-1}}{\left(1+x\right)^{a+b}}\mathrm{d}x=\Beta\left(a,b\right)$; $\int_0^{\pi/2}\sin^mx\cos^nx\,\mathrm{d}x=\frac12\Beta\left(\frac{m+1}2,\frac{n+1}2\right)$.

> **命题 (三角函数系的正交性)**
> 
> 三角函数系 $1,\cos{x},\sin{x},\cos2x,\sin2x,\cdots$ 在 $\left[-\pi,\pi\right]$ 上两两正交, 且 $\int_{-\pi}^\pi1\,\mathrm{d}x=2\pi$, $\int_{-\pi}^\pi\cos^2nx\,\mathrm{d}x=\int_{-\pi}^\pi\sin^2nx\,\mathrm{d}x=\pi$.

> **命题 (傅里叶系数)**
> 
> $a_n=\frac1\pi\int_{-\pi}^\pi{f}\left(x\right)\cos{n}x\,\mathrm{d}x$, $b_n=\frac1\pi\int_{-\pi}^\pi{f}\left(x\right)\sin{n}x\,\mathrm{d}x$.

> **定理 (封闭性方程)**
> 
> $\frac1\pi\int_{-\pi}^\pi{f}^2\left(x\right)\mathrm{d}x=\frac{a_0^2}2+\sum_{n=1}^\infty\left(a_n^2+b_n^2\right)$.

## 12.6-2

证明 $\Gamma\left(\alpha\right)$ 在 $\left(0,+\infty\right)$ 上不一致收敛.

### 解答 12.6-2

取 $\alpha_n=\frac1n\to0+$, 则 $\int_0^{1/n}t^{\alpha_n-1}e^{-t}\mathrm{d}t\to1\ne0$. 故不满足一致收敛的柯西条件. $\blacksquare$

## 13.1-1

证明内积的对称性与线性性.

### 解答 13.1-1

由内积与范数的定义 及积分的线性性, $\left\langle{f},g\right\rangle=\left\langle{g},f\right\rangle$, $\left\langle\lambda{f}+\mu{g},h\right\rangle=\lambda\left\langle{f},h\right\rangle+\mu\left\langle{g},h\right\rangle$. $\blacksquare$

## 13.1-2

证明柯西-施瓦茨不等式: $\left|\left\langle{f},g\right\rangle\right|\le\left|f\right|\cdot\left|g\right|$.

### 解答 13.1-2

对任意 $\lambda$, $\left|f-\lambda{g}\right|^2\ge0$, 展开得关于 $\lambda$ 的二次三项式恒非负, 判别式不大于 $0$, 即得. $\blacksquare$

## 13.1-3

证明等号成立当且仅当 $f,g$ 线性相关.

### 解答 13.1-3

$\left(\Leftarrow\right)$ 若 $g=\lambda{f}$, 直接验证. $\left(\Rightarrow\right)$ 若等号成立, 判别式为 $0$, 存在 $\lambda_0$ 使 $\left|f-\lambda_0g\right|^2=0$. 由连续性, $f\equiv\lambda_0g$. $\blacksquare$

## 13.1-7

证明 $c_1+c_2\cos{x}+c_3\sin{x}\equiv0$ 蕴含 $c_1=c_2=c_3=0$, 并推广到任意有穷个元素线性无关.

### 解答 13.1-7

两端分别乘以 $1,\cos{x},\sin{x}$ 并积分. 由**命题 (三角函数系的正交性)**, 交叉项为零, 得 $2\pi{c}_1=0$, $\pi{c}_2=0$, $\pi{c}_3=0$. 推广同理. $\blacksquare$

## 13.2-1-1

求 $f\left(x\right)=x^2$ ($-\pi\le{x}\le\pi$) 的傅里叶级数.

### 解答 13.2-1-1

由**命题 (傅里叶系数)**, $a_0=\frac{2\pi^2}3$, $a_n=\frac{4\left(-1\right)^n}{n^2}$, $b_n=0$. 故 $x^2\sim\frac{\pi^2}3+4\sum_{n=1}^\infty\frac{\left(-1\right)^n}{n^2}\cos{n}x$. $\blacksquare$

## 13.2-1-3

求 $f\left(x\right)=\sin^4x$ 的傅里叶级数.

### 解答 13.2-1-3

三角恒等变换得 $\sin^4x=\frac38-\frac12\cos2x+\frac18\cos4x$. 由**命题 (傅里叶系数)** 直接读出系数. $\blacksquare$

## 13.2-1-5

求 $f\left(x\right)=\begin{cases}0,&-\pi\le{x}<0\\x,&0\le{x}\le\pi\end{cases}$ 的傅里叶级数.

### 解答 13.2-1-5

由**命题 (傅里叶系数)**, $a_0=\frac\pi2$, $a_n=\frac{\left(-1\right)^n-1}{n^2\pi}$, $b_n=\frac{\left(-1\right)^{n+1}}n$. 故 $f\left(x\right)\sim\frac\pi4-\frac2\pi\sum_{k=0}^\infty\frac{\cos\left(2k+1\right)x}{\left(2k+1\right)^2}+\sum_{n=1}^\infty\frac{\left(-1\right)^{n+1}}n\sin{n}x$. $\blacksquare$

## 13.2-7

证明: 若 $f\left(x+\pi\right)=f\left(x\right)$, 则 $a_{2n-1}=b_{2n-1}=0$; 若 $f\left(x+\pi\right)=-f\left(x\right)$, 则 $a_{2n}=b_{2n}=0$.

### 解答 13.2-7

拆积分并作代换 $x=t-\pi$, 利用 $\cos\left(n\left(t-\pi\right)\right)=\left(-1\right)^n\cos{n}t$. 条件 (i) 时 $\left(-1\right)^n+1=0$ ($n$ 奇); 条件 (ii) 时 $1-\left(-1\right)^n=0$ ($n$ 偶). $\blacksquare$

## 13.3-1

证明: 当 $0<{}x<\pi$ 时 $1=\frac12+\frac2\pi\sum_{n=0}^\infty\frac{\sin\left(2n+1\right)x}{2n+1}$, 并推出 $\frac\pi4=\sum_{n=0}^\infty\frac{\left(-1\right)^n}{2n+1}$.

### 解答 13.3-1

由**命题 (傅里叶系数)**, $a_0=1$, $a_n=0$, $b_n=\frac{1-\left(-1\right)^n}{n\pi}$. 由**定理 3.1 (狄利克雷收敛定理)**, 连续点处等式成立. 取 $x=\frac\pi2$ 得 $\frac\pi4=\sum\frac{\left(-1\right)^n}{2n+1}$. $\blacksquare$

## 13.3-3

求 $f\left(x\right)=\left(\pi-\left|x\right|\right)^2$ 的傅里叶级数, 并求 $\sum\frac1{n^2}$ 与 $\sum\frac1{n^4}$.

### 解答 13.3-3

由**命题 (傅里叶系数)**, $a_0=\frac{2\pi^2}3$, $a_n=\frac4{n^2}$. 在 $x=0$ 处由**定理 3.1 (狄利克雷收敛定理)**, $\pi^2=\frac{\pi^2}3+4\sum\frac1{n^2}$, 得 $\sum\frac1{n^2}=\frac{\pi^2}6$. 由**定理 (封闭性方程)**, 得 $\sum\frac1{n^4}=\frac{\pi^4}{90}$. $\blacksquare$

## 13.3-4

利用 $f\left(x\right)=x^2$ ($\left|x\right|\le\pi$) 的傅里叶级数求 $\sum\frac{\left(-1\right)^{n+1}}{n^2}$ 及 $\sum\frac1{n^2}$.

### 解答 13.3-4

$x^2\sim\frac{\pi^2}3+4\sum\frac{\left(-1\right)^n}{n^2}\cos{n}x$. 取 $x=\pi$ 得 $\sum\frac1{n^2}=\frac{\pi^2}6$; 取 $x=0$ 得 $\sum\frac{\left(-1\right)^{n+1}}{n^2}=\frac{\pi^2}{12}$. $\blacksquare$

## 13.4-1

证明 $\sum\frac{a_n}{n}$ 及 $\sum\frac{b_n}{n}$ 收敛.

### 解答 13.4-1

由**定理 4.1 (贝塞尔不等式)**, $\sum\left(a_n^2+b_n^2\right)<\infty$. 由柯西-施瓦茨不等式, $\sum\left|\frac{a_n}n\right|\le\left(\sum{a}_n^2\right)^{1/2}\left(\sum\frac1{n^2}\right)^{1/2}<\infty$. 故绝对收敛. $\blacksquare$

## 13.4-2

说明 $\frac{a_0}2+\sum\frac1{\ln{n}\cdot\ln\ln{n}}\cos{n}x$ 处处收敛但不是任何可积函数的傅里叶级数.

### 解答 13.4-2

收敛性: 由狄利克雷判别法. 不是傅里叶级数: 由**定理 4.1 (贝塞尔不等式)** 与 13.4-1, 必须 $\sum\frac{a_n}n$ 收敛, 但 $\sum\frac1{n\ln{n}\cdot\ln\ln{n}}$ 由积分判别法发散. $\blacksquare$

## 13.4-5

利用 $f\left(x\right)=x^2$ 的 Parseval 等式求 $\sum\frac1{n^4}$.

### 解答 13.4-5

由**定理 4.2 (封闭性方程/Parseval 等式)**, $\frac{2\pi^4}5=\frac{2\pi^4}9+16\sum\frac1{n^4}$, 得 $\sum\frac1{n^4}=\frac{\pi^4}{90}$. $\blacksquare$

## 13.4-7

利用 $f\left(x\right)=\left|x\right|$ 的 Parseval 等式求 $\sum\frac1{\left(2n-1\right)^4}$.

### 解答 13.4-7

由**定理 4.2 (封闭性方程/Parseval 等式)**, $\frac{2\pi^2}3=\frac{\pi^2}2+\frac{16}{\pi^2}\sum\frac1{\left(2n-1\right)^4}$, 得 $\sum\frac1{\left(2n-1\right)^4}=\frac{\pi^4}{96}$. $\blacksquare$
