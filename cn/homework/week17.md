# 作业 17

> **定义**（凸函数）设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 中有定义. 若对 $\left(a,b\right)$ 中任意两点 $x_1$ 与 $x_2$($x_1< x_2$), 都有
> $$
> f\left(tx_1+\left(1-t\right)x_2\right)\le tf\left(x_1\right)+\left(1-t\right)f\left(x_2\right),
> $$
> 其中 $t$ 是 $\left(0,1\right)$ 中任意数, 则称函数 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 上是凸函数. 反之, 若上述不等式反向成立, 则称 $y=f\left(x\right)$ 为 $\left(a,b\right)$ 上的凹函数.

> **定理 5.1**（凸函数的二阶导数判别）设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 上二阶可导. 则 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 上为凸函数的充要条件是 $f''\left(x\right)\ge0$($\forall x\in\left(a,b\right)$); $y=f\left(x\right)$ 在 $\left(a,b\right)$ 上为凹函数的充要条件是 $f''\left(x\right)\le0$($\forall x\in\left(a,b\right)$).

### 习题一

（习题 3.5-1-1）求出函数 $y=xe^x$ 的凸凹性区间及拐点.

### 解答 习题一

求导得
$$
y'=e^x+xe^x=\left(1+x\right)e^x, y''=e^x+\left(1+x\right)e^x=\left(2+x\right)e^x.
$$

令 $y''=0$, 得 $x=-2$. 因 $e^x> 0$ 恒成立, 故 $y''$ 的符号由 $2+x$ 决定.

当 $x< -2$ 时 $y''< 0$, 函数为凹的; 当 $x> -2$ 时 $y''> 0$, 函数为凸的.

拐点为 $\left(-2,-2e^{-2}\right)$.

由**定理 5.1**（凸函数的二阶导数判别）, $y=xe^x$ 在 $\left(-\infty,-2\right]$ 上为凹函数, 在 $\left[-2,+\infty\right)$ 上为凸函数. $\blacksquare$

### 习题二

（习题 3.5-1-4）求出函数 $y=x\ln x$ 的凸凹性区间及拐点.

### 解答 习题二

定义域为 $\left(0,+\infty\right)$. 求导得
$$
y'=\ln x+1, y''=\frac1x> 0\left(x> 0\right).
$$

由**定理 5.1**（凸函数的二阶导数判别）, $y=x\ln x$ 在 $\left(0,+\infty\right)$ 上为凸函数, 无拐点. $\blacksquare$

### 习题三

（习题 3.5-2）利用凸函数概念证明下列不等式: 
(1) 设 $a> 0,b> 0$, 证明

$$
2\arctan\frac{a+b}{2}\ge\arctan a+\arctan b;
$$

(2) 若 $a,b,c$ 均为正数, 证明 $a^{\alpha}b^{\beta}c^{\gamma}\le\alpha a+\beta b+\gamma c$, 其中 $\alpha+\beta+\gamma=1$, $\alpha,\beta,\gamma> 0$.

### 解答 习题三

(1)令 $f\left(x\right)=\arctan x$. 则
$$
f'\left(x\right)=\frac{1}{1+x^2}, f''\left(x\right)=\frac{-2x}{\left(1+x^2\right)^2}.
$$

当 $x> 0$ 时 $f''\left(x\right)< 0$, 故 $f\left(x\right)=\arctan x$ 在 $\left(0,+\infty\right)$ 上为凹函数. 由凹函数的定义, 对任意 $a,b> 0$ 及 $t\in\left(0,1\right)$, 
$$
f\left(ta+\left(1-t\right)b\right)\ge tf\left(a\right)+\left(1-t\right)f\left(b\right).
$$

取 $t=\frac12$, 得
$$
f\left(\frac{a+b}{2}\right)\ge\frac{f\left(a\right)+f\left(b\right)}{2},
$$

即
$$
2\arctan\frac{a+b}{2}\ge\arctan a+\arctan b.
$$

(2)由习题二, $y=x\ln x$ 在 $\left(0,+\infty\right)$ 上为凸函数. 由凸函数的定义, 对任意 $a,b,c> 0$ 及 $\alpha+\beta+\gamma=1$, 
$$
\alpha a\ln a+\beta b\ln b+\gamma c\ln c\ge\left(\alpha a+\beta b+\gamma c\right)\ln\left(\alpha a+\beta b+\gamma c\right).
$$

不对, 这不是正确的应用. 修正: 凸函数 $f\left(x\right)=x\ln x$ 满足
$$
f\left(\alpha\cdot\frac{a}{\alpha}+\beta\cdot\frac{b}{\beta}+\gamma\cdot\frac{c}{\gamma}\right)\le\alpha f\left(\frac{a}{\alpha}\right)+\beta f\left(\frac{b}{\beta}\right)+\gamma f\left(\frac{c}{\gamma}\right).
$$

即
$$
\left(a+b+c\right)\ln\left(a+b+c\right)\le a\ln\frac{a}{\alpha}+b\ln\frac{b}{\beta}+c\ln\frac{c}{\gamma}.
$$

这也不是题目要求的. 正确的做法是: 由 $f\left(x\right)=\ln x$ 为凹函数, 
$$
\alpha\ln a+\beta\ln b+\gamma\ln c\le\ln\left(\alpha a+\beta b+\gamma c\right).
$$

即
$$
a^\alpha b^\beta c^\gamma\le\alpha a+\beta b+\gamma c.
$$

此即加权 AM-GM 不等式. $\blacksquare$

### 习题四

（习题 3.5-3）设 $f\left(x\right)$ 与 $g\left(x\right)$ 均为 $\left(a,b\right)$ 中的凸函数. 令

$$
F\left(x\right)=\max\left\{f\left(x\right),g\left(x\right)\right\},
$$

则 $F\left(x\right)$ 也是凸函数.

### 解答 习题四

对任意 $x_1,x_2\in\left(a,b\right)$ 及 $t\in\left(0,1\right)$, 需证
$$
F\left(tx_1+\left(1-t\right)x_2\right)\le tF\left(x_1\right)+\left(1-t\right)F\left(x_2\right).
$$

由 $F$ 的定义, 
$$
F\left(tx_1+\left(1-t\right)x_2\right)=\max\left\{f\left(tx_1+\left(1-t\right)x_2\right),g\left(tx_1+\left(1-t\right)x_2\right)\right\}.
$$

因 $f,g$ 均为凸函数, 故
$$
f\left(tx_1+\left(1-t\right)x_2\right)\le tf\left(x_1\right)+\left(1-t\right)f\left(x_2\right)\le tF\left(x_1\right)+\left(1-t\right)F\left(x_2\right),
$$
$$
g\left(tx_1+\left(1-t\right)x_2\right)\le tg\left(x_1\right)+\left(1-t\right)g\left(x_2\right)\le tF\left(x_1\right)+\left(1-t\right)F\left(x_2\right).
$$

两式右端相同, 故

$$
\max\left\{f\left(\cdot\right),g\left(\cdot\right)\right\}\le tF\left(x_1\right)+\left(1-t\right)F\left(x_2\right),
$$

即
$$
F\left(tx_1+\left(1-t\right)x_2\right)\le tF\left(x_1\right)+\left(1-t\right)F\left(x_2\right).
$$

故 $F\left(x\right)$ 为凸函数. $\blacksquare$

### 习题五

（习题 3.5-5）设 $f\left(u\right)$ 在 $\left(-\infty,+\infty\right)$ 中是凸函数, 且是递增函数. 又设 $g\left(x\right)$ 在 $\left(a,b\right)$ 区间上为凸函数, 证明复合函数 $f\left(g\left(x\right)\right)$ 是凸函数.

### 解答 习题五

对任意 $x_1,x_2\in\left(a,b\right)$ 及 $t\in\left(0,1\right)$, 需证
$$
f\left(g\left(tx_1+\left(1-t\right)x_2\right)\right)\le t f\left(g\left(x_1\right)\right)+\left(1-t\right)f\left(g\left(x_2\right)\right).
$$

因 $g\left(x\right)$ 为凸函数, 故
$$
g\left(tx_1+\left(1-t\right)x_2\right)\le t g\left(x_1\right)+\left(1-t\right)g\left(x_2\right).
$$

又因 $f\left(u\right)$ 为递增函数, 故
$$
f\left(g\left(tx_1+\left(1-t\right)x_2\right)\right)\le f\left(t g\left(x_1\right)+\left(1-t\right)g\left(x_2\right)\right).
$$

再由 $f\left(u\right)$ 为凸函数, 
$$
f\left(t g\left(x_1\right)+\left(1-t\right)g\left(x_2\right)\right)\le t f\left(g\left(x_1\right)\right)+\left(1-t\right)f\left(g\left(x_2\right)\right).
$$

合起来即得
$$
f\left(g\left(tx_1+\left(1-t\right)x_2\right)\right)\le t f\left(g\left(x_1\right)\right)+\left(1-t\right)f\left(g\left(x_2\right)\right).
$$

故 $f\left(g\left(x\right)\right)$ 为凸函数. $\blacksquare$

### 习题六

（习题 3.5-6）设 $f\left(x\right)$ 在 $\left(-\infty,+\infty\right)$ 中是可微的凸函数, 且有界. 证明 $f\left(x\right)$ 为常数.

### 解答 习题六

因 $f\left(x\right)$ 为凸函数, 由**定理 5.1**（凸函数的二阶导数判别）, $f''\left(x\right)\ge0$, 故 $f'\left(x\right)$ 为递增函数.

反证: 假定 $f'\left(x\right)$ 不恒为 $0$. 则存在 $x_0$ 使得 $f'\left(x_0\right)> 0$ 或 $f'\left(x_0\right)< 0$.

若 $f'\left(x_0\right)> 0$, 因 $f'$ 递增, 故当 $x> x_0$ 时 $f'\left(x\right)\ge f'\left(x_0\right)> 0$. 由拉格朗日中值定理, 
$$
f\left(x\right)=f\left(x_0\right)+f'\left(\xi\right)\left(x-x_0\right)\ge f\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)\to+\infty\left(x\to+\infty\right).
$$

这与 $f\left(x\right)$ 有界矛盾.

若 $f'\left(x_0\right)< 0$, 因 $f'$ 递增, 故当 $x< x_0$ 时 $f'\left(x\right)\le f'\left(x_0\right)< 0$. 由拉格朗日中值定理, 
$$
f\left(x_0\right)-f\left(x\right)=f'\left(\xi\right)\left(x_0-x\right)\le f'\left(x_0\right)\left(x_0-x\right)< 0,
$$

即

$$
f\left(x\right)\ge f\left(x_0\right)-f'\left(x_0\right)\left(x-x_0\right)\to+\infty\ \left(x\to-\infty\text{, 因}-f'\left(x_0\right)> 0\right).
$$

这与 $f\left(x\right)$ 有界矛盾.

故 $f'\left(x\right)\equiv0$, 即 $f\left(x\right)$ 为常数. $\blacksquare$

### 习题七

（习题 3.5-7-1）作函数 $y=\frac{\left(x+1\right)^3}{\left(x-1\right)^2}$ 的图形.

### 解答 习题七

**定义域** $\left(-\infty,1\right)\cup\left(1,+\infty\right)$.

**渐近线**: $\lim\limits_{x\to1}y=\infty$, 故 $x=1$ 为垂直渐近线. 又
$$
\lim_{x\to\infty}\frac{y}{x}=\lim_{x\to\infty}\frac{\left(x+1\right)^3}{x\left(x-1\right)^2}=1,
$$
$$
\lim_{x\to\infty}\left(y-x\right)=\lim_{x\to\infty}\frac{\left(x+1\right)^3-x\left(x-1\right)^2}{\left(x-1\right)^2}=\lim_{x\to\infty}\frac{5x^2+x+1}{x^2-2x+1}=5.
$$

故斜渐近线为 $y=x+5$.

**单调区间与极值**: 求导
$$
y'=\frac{3\left(x+1\right)^2\left(x-1\right)^2-\left(x+1\right)^3\cdot2\left(x-1\right)}{\left(x-1\right)^4}=\frac{\left(x+1\right)^2\left[3\left(x-1\right)-2\left(x+1\right)\right]}{\left(x-1\right)^3}=\frac{\left(x+1\right)^2\left(x-5\right)}{\left(x-1\right)^3}.
$$

令 $y'=0$, 得 $x=-1$ 或 $x=5$.

当 $x< -1$ 时 $y'< 0$(分母负, 分子正); 当 $-1< x< 1$ 时 $y'< 0$; 当 $1< x< 5$ 时 $y'< 0$; 当 $x> 5$ 时 $y'> 0$.

故 $x=5$ 为极小值点, 极小值 $y\left(5\right)=\frac{6^3}{4^2}=\frac{216}{16}=\frac{27}{2}$. $x=-1$ 不是极值点(两侧导数同号).

**凸凹性与拐点**: 
$$
y''=\frac{\left[\left(x+1\right)^2\left(x-5\right)\right]'\left(x-1\right)^3-\left(x+1\right)^2\left(x-5\right)\cdot3\left(x-1\right)^2}{\left(x-1\right)^6}=\frac{2\left(x+1\right)\left(x-1\right)^2-3\left(x+1\right)^2\left(x-5\right)}{\left(x-1\right)^4}=\frac{16\left(x+1\right)}{\left(x-1\right)^4}.
$$

当 $x< -1$ 时 $y''< 0$(凹); 当 $x> -1$ 且 $x\ne1$ 时 $y''> 0$(凸). 拐点为 $\left(-1,0\right)$.

综合以上信息可描绘函数图形. $\blacksquare$

### 习题八

（习题 3.5-7-2）作函数 $y=xe^{-x}$ 的图形.

### 解答 习题八

**定义域** $\left(-\infty,+\infty\right)$.

**渐近线**: $\lim\limits_{x\to+\infty}xe^{-x}=0$, 故 $y=0$ 为水平渐近线($x\to+\infty$).

**单调区间与极值**: 求导
$$
y'=e^{-x}-xe^{-x}=\left(1-x\right)e^{-x}.
$$

令 $y'=0$, 得 $x=1$. 当 $x< 1$ 时 $y'> 0$, 当 $x> 1$ 时 $y'< 0$. 故 $x=1$ 为极大值点, 极大值 $y\left(1\right)=e^{-1}=\frac1e$.

**凸凹性与拐点**: 
$$
y''=-e^{-x}-\left(1-x\right)e^{-x}=\left(x-2\right)e^{-x}.
$$

令 $y''=0$, 得 $x=2$. 当 $x< 2$ 时 $y''< 0$(凹); 当 $x> 2$ 时 $y''> 0$(凸). 拐点为 $\left(2,2e^{-2}\right)$.

综合以上信息可描绘函数图形. $\blacksquare$

### 习题九

（习题 3.5-7-3）作函数 $y=xe^{-x^2}$ 的图形.

### 解答 习题九

**定义域** $\left(-\infty,+\infty\right)$. 函数为奇函数, 图形关于原点对称.

**渐近线**: $\lim\limits_{x\to\pm\infty}xe^{-x^2}=0$, 故 $y=0$ 为水平渐近线.

**单调区间与极值**: 求导
$$
y'=e^{-x^2}+x\cdot\left(-2x\right)e^{-x^2}=\left(1-2x^2\right)e^{-x^2}.
$$

令 $y'=0$, 得

$$
x=\pm\frac{1}{\sqrt2}}.
$$

当 $x< -\frac{1}{\sqrt2}$ 时 $y'< 0$; 当 $-\frac{1}{\sqrt2}< x< \frac{1}{\sqrt2}$ 时 $y'> 0$; 当 $x> \frac{1}{\sqrt2}$ 时 $y'< 0$.

故 $x=-\frac{1}{\sqrt2}$ 为极小值点, 极小值 $-\frac{1}{\sqrt{2e}}$; $x=\frac{1}{\sqrt2}$ 为极大值点, 极大值 $\frac{1}{\sqrt{2e}}$.

**凸凹性与拐点**: 
$$
y''=-4xe^{-x^2}+\left(1-2x^2\right)\left(-2x\right)e^{-x^2}=\left(4x^3-6x\right)e^{-x^2}=2x\left(2x^2-3\right)e^{-x^2}.
$$

令 $y''=0$, 得 $x=0$ 或 $x=\pm\sqrt{\frac32}$.

当 $x< -\sqrt{\frac32}$ 时 $y''< 0$(凹); 当 $-\sqrt{\frac32}< x< 0$ 时 $y''> 0$(凸); 当 $0< x< \sqrt{\frac32}$ 时 $y''< 0$(凹); 当 $x> \sqrt{\frac32}$ 时 $y''> 0$(凸).

拐点为 $\left(0,0\right)$ 及 $\left(\pm\sqrt{\frac32},\pm\sqrt{\frac32}e^{-3/2}\right)$.

综合以上信息可描绘函数图形. $\blacksquare$
