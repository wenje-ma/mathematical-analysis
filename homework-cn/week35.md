# week35

> **定理 3.3 (积分号下求导)**
> 
> 设 $f\left(x,y\right)$ 与 $f_y\left(x,y\right)$ 连续, 则 $I\left(y\right)=\int_a^bf\left(x,y\right)\mathrm{d}x$ 可导, 且 $I'\left(y\right)=\int_a^bf_y\left(x,y\right)\mathrm{d}x$. 若积分限依赖于 $y$, 则补上边界项: $I'\left(y\right)=f\left(b\left(y\right),y\right)b'\left(y\right)-f\left(a\left(y\right),y\right)a'\left(y\right)+\int_{a\left(y\right)}^{b\left(y\right)}f_y\left(x,y\right)\mathrm{d}x$.

> **定理 4.3 (魏尔斯特拉斯判别法)**
> 
> 若 $\left|f\left(x,y\right)\right|\le{F}\left(x\right)$ 且瑕积分 $\int_a^bF\left(x\right)\mathrm{d}x$ 收敛, 则 $\int_a^bf\left(x,y\right)\mathrm{d}x$ 关于 $y$ 一致收敛.

> **定理 4.4 (阿贝尔判别法)**
> 
> 若 $\int_a^{+\infty}f\left(x,y\right)\mathrm{d}x$ 一致收敛, $g\left(x,y\right)$ 关于 $x$ 单调且一致有界, 则 $\int_a^{+\infty}fg\,\mathrm{d}x$ 一致收敛.

> **例 4.5 (狄利克雷积分)**
> 
> $\int_0^{+\infty}\frac{\sin{x}}{x}\mathrm{d}x=\frac\pi2$. 一般地, $\int_0^{+\infty}\frac{\sin\left(kx\right)}x\mathrm{d}x=\frac\pi2\operatorname{sgn}\left(k\right)$.

> **定理 4.7 (积分次序交换定理)**
> 
> 若 $f$ 连续且 $\int_a^{+\infty}f\left(x,y\right)\mathrm{d}x$ 关于 $y\in\left[c,d\right]$ 一致收敛, 则 $\int_c^d\mathrm{d}y\int_a^{+\infty}f\,\mathrm{d}x=\int_a^{+\infty}\mathrm{d}x\int_c^df\,\mathrm{d}y$.

> **定理 4.8 (积分号下求导)**
> 
> 若 $f$ 与 $f_y$ 连续, $\int_a^{+\infty}f$ 收敛, $\int_a^{+\infty}f_y$ 一致收敛, 则 $I'\left(y\right)=\int_a^{+\infty}f_y\,\mathrm{d}x$.

> **命题 (伽马与贝塔的积分形式)**
> 
> $\int_0^{+\infty}\frac{x^{a-1}}{\left(1+x\right)^{a+b}}\mathrm{d}x=\Beta\left(a,b\right)$; $\int_0^{\pi/2}\sin^mx\cos^nx\,\mathrm{d}x=\frac12\Beta\left(\frac{m+1}2,\frac{n+1}2\right)$.

## 12.3-6

设 $I\left(\alpha\right)=\int_0^{2\pi}\ln\left(1-\alpha\cos\theta\right)\mathrm{d}\theta$ ($\left|\alpha\right|<1$). 证明 $I'\left(\alpha\right)=\frac{2\pi\left(\sqrt{1-\alpha^2}-1\right)}{\alpha\sqrt{1-\alpha^2}}$ 并推出 $I\left(\alpha\right)=2\pi\ln\frac{1+\sqrt{1-\alpha^2}}2$.

### 解答 12.3-6

由**定理 3.3 (积分号下求导)**, $I'\left(\alpha\right)=\int_0^{2\pi}\frac{-\cos\theta}{1-\alpha\cos\theta}\mathrm{d}\theta$. 分解被积函数并利用标准积分 $\int_0^{2\pi}\frac{\mathrm{d}\theta}{1-\alpha\cos\theta}=\frac{2\pi}{\sqrt{1-\alpha^2}}$, 得 $I'\left(\alpha\right)=\frac{2\pi\left(\sqrt{1-\alpha^2}-1\right)}{\alpha\sqrt{1-\alpha^2}}$. 积分并利用 $I\left(0\right)=0$, 得 $I\left(\alpha\right)=2\pi\ln\frac{1+\sqrt{1-\alpha^2}}2$. $\blacksquare$

## 12.4-1-1

讨论 $\int_0^{+\infty}e^{-\alpha{x}^2}\mathrm{d}x$ 在 $\alpha\in\left[\alpha_0,+\infty\right)$ 上的一致收敛性.

### 解答 12.4-1-1

因 $e^{-\alpha{x}^2}\le{e}^{-\alpha_0x^2}$, 及**定理 4.3 (魏尔斯特拉斯判别法)**, 一致收敛. $\blacksquare$

## 12.4-1-3

讨论 $\int_1^{+\infty}e^{-xy}\frac{\cos{x}}{x}\mathrm{d}x$ 在 $y\in\left[0,+\infty\right)$ 上的一致收敛性.

### 解答 12.4-1-3

$\int_1^{+\infty}\frac{\cos{x}}{x}\mathrm{d}x$ 收敛且不含 $y$, $e^{-xy}$ 单调且一致有界. 由**定理 4.4 (阿贝尔判别法)**, 一致收敛. $\blacksquare$

## 12.4-1-5

讨论 $\int_0^{+\infty}e^{-x^2y^2}\cos{x}\,\mathrm{d}x$ 在 $y\in\left[y_0,+\infty\right)$ 上的一致收敛性.

### 解答 12.4-1-5

因 $\left|e^{-x^2y^2}\cos{x}\right|\le{e}^{-x^2y_0^2}$, 及**定理 4.3 (魏尔斯特拉斯判别法)**, 一致收敛. $\blacksquare$

## 12.4-2-1

求 $\int_0^{+\infty}\frac{e^{-ax}-e^{-bx}}x\mathrm{d}x$ ($0<{}a<{}b$).

### 解答 12.4-2-1

由 $\frac{e^{-ax}-e^{-bx}}x=\int_a^be^{-xy}\mathrm{d}y$, 及**定理 4.7 (积分次序交换定理)**, $I=\int_a^b\frac{\mathrm{d}y}y=\ln\frac{b}a$. $\blacksquare$

## 12.4-2-2

求 $\int_0^{+\infty}\frac{\sin\left(\alpha{x}\right)\cos\left(\beta{x}\right)}x\mathrm{d}x$.

### 解答 12.4-2-2

利用三角恒等式及**例 4.5 (狄利克雷积分)**, 得 $I=\begin{cases}0,&\alpha<\beta\\\frac\pi4,&\alpha=\beta\\\frac\pi2,&\alpha>\beta\end{cases}$. $\blacksquare$

## 12.4-2-4

求 $\int_0^{+\infty}\frac{1-\cos\left(\alpha{x}\right)}xe^{-x}\mathrm{d}x$.

### 解答 12.4-2-4

由**定理 4.8 (积分号下求导)**, $I'\left(\alpha\right)=\int_0^{+\infty}e^{-x}\sin\left(\alpha{x}\right)\mathrm{d}x=\frac{\alpha}{1+\alpha^2}$. 积分并利用 $I\left(0\right)=0$, 得 $I\left(\alpha\right)=\frac12\ln\left(1+\alpha^2\right)$. $\blacksquare$

## 12.4-5

证明迪尼定理: 若 $u_n\left(x\right)\ge0$ 连续, $\sum{u}_n\left(x\right)$ 点态收敛于连续函数 $S\left(x\right)$, 则一致收敛.

### 解答 12.4-5

令余项 $R_N\left(x\right)=S\left(x\right)-S_N\left(x\right)$. 反证: 若不一致收敛, 则存在 $x_k\to{x}_0$ 使 $R_{N_k}\left(x_k\right)\ge\varepsilon_0$. 由单调性与连续性, 对任意 $m$, $R_m\left(x_0\right)\ge\varepsilon_0$, 与 $R_m\left(x_0\right)\to0$ 矛盾. $\blacksquare$

## 12.5-1-1

讨论 $\int_0^1\frac{\sin{x}}{x^\alpha}\mathrm{d}x$ 在 (i) $\alpha\le\alpha_0<2$; (ii) $\alpha<2$ 上的一致收敛性.

### 解答 12.5-1-1

(i) 因 $\left|\frac{\sin{x}}{x^\alpha}\right|\le{x}^{1-\alpha_0}$, 及**定理 4.3 (魏尔斯特拉斯判别法)**, 一致收敛.

(ii) 取 $\alpha_n=2-\frac1n$, 则 $\int_0^{1/n}\frac{\sin{x}}{x^{\alpha_n}}\mathrm{d}x\to1\ne0$. 故在 $\alpha<2$ 上不一致收敛. $\blacksquare$

## 12.5-1-2

讨论 $\int_0^1x^{p-1}\mathrm{d}x$ 在 (i) $p\ge{p}_0>0$; (ii) $p>0$ 上的一致收敛性.

### 解答 12.5-1-2

(i) 因 $x^{p-1}\le{x}^{p_0-1}$, 及**定理 4.3 (魏尔斯特拉斯判别法)**, 一致收敛.

(ii) 取 $p_n=\frac1n$, 则 $\int_0^{1/n}x^{p_n-1}\mathrm{d}x\to1\ne0$. 故在 $p>0$ 上不一致收敛. $\blacksquare$

## 12.5-2-1

求 $\int_0^1\frac{x^b-x^a}{\ln{x}}\mathrm{d}x$ ($a>-1,b>-1$).

### 解答 12.5-2-1

由 $\frac{x^b-x^a}{\ln{x}}=\int_a^bx^y\mathrm{d}y$, 及**定理 4.7 (积分次序交换定理)**, $I=\int_a^b\frac{\mathrm{d}y}{y+1}=\ln\frac{1+b}{1+a}$. $\blacksquare$

## 12.6-1-1

计算 $\int_0^{+\infty}\frac{4\sqrt{x}}{\left(1+x\right)^2}\mathrm{d}x$.

### 解答 12.6-1-1

由**命题 (伽马与贝塔的积分形式)**, $a=\frac32$, $b=\frac12$. 由伽马函数的定义, $\Gamma\left(\frac32\right)=\frac{\sqrt\pi}2$, $\Gamma\left(\frac12\right)=\sqrt\pi$. 故原式 $=4\cdot\frac{\pi}2=2\pi$. $\blacksquare$

## 12.6-1-2

计算 $\int_0^{+\infty}x^{-1/2}e^{-\alpha{x}}\mathrm{d}x$ ($\alpha>0$).

### 解答 12.6-1-2

代换 $t=\alpha{x}$, 由伽马函数的定义, 得 $\sqrt{\frac\pi\alpha}$. $\blacksquare$

## 12.6-1-3

计算 $\int_0^1x^8\sqrt{1-x^3}\mathrm{d}x$.

### 解答 12.6-1-3

代换 $t=x^3$, 得 $\frac13\Beta\left(3,\frac32\right)=\frac{16}{315}$. $\blacksquare$

## 12.6-1-4

计算 $\int_0^{\pi/2}\sin^6x\cos^4x\,\mathrm{d}x$.

### 解答 12.6-1-4

由**命题 (伽马与贝塔的积分形式)**, $=\frac12\Beta\left(\frac72,\frac52\right)=\frac{3\pi}{512}$. $\blacksquare$

## 12.6-1-9

计算 $\int_0^1\frac{\mathrm{d}x}{\sqrt{1-x^4}}$.

### 解答 12.6-1-9

代换 $t=x^4$, 得 $\frac14\Beta\left(\frac14,\frac12\right)$. $\blacksquare$

## 12.6-1-10

计算 $\int_0^{+\infty}\frac{\mathrm{d}x}{1+x^3}$.

### 解答 12.6-1-10

代换 $u=x^3$, 得 $\frac13\Beta\left(\frac13,\frac23\right)=\frac13\Gamma\left(\frac13\right)\Gamma\left(\frac23\right)$. $\blacksquare$
