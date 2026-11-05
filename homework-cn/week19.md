# week19

> **定理 1.3 (拉格朗日中值定理)**
> 
> 设 $y=f\left(x\right)$ 在 $\left[a,b\right]$ 上连续, 在 $\left(a,b\right)$ 内可导. 则存在 $c\in\left(a,b\right)$, 使得 $f'\left(c\right)=\frac{f\left(b\right)-f\left(a\right)}{b-a}$.

> **定理 1.3 (不定积分的线性法则)**
> 
> 设 $y=f\left(x\right)$ 及 $y=g\left(x\right)$ 在某个区间中有原函数. 则 $\int\left[af\left(x\right)+bg\left(x\right)\right]\mathrm{d}x=a\int{f}\left(x\right)\,\mathrm{d}x+b\int{g}\left(x\right)\,\mathrm{d}x$, 其中 $a,b$ 是两个任意常数.

> **定理 5.1 (凸函数的二阶导数判别)**
> 
> 设 $y=f\left(x\right)$ 在 $\left(a,b\right)$ 上二阶可导. 则 $f$ 为凸函数的充要条件是 $f''\left(x\right)\ge0$; $f$ 为凹函数的充要条件是 $f''\left(x\right)\le0$.

## 3.5-3

设 $f\left(x\right)$ 与 $g\left(x\right)$ 均为 $\left(a,b\right)$ 中的凸函数. 令 $F\left(x\right)=\max\left\{f\left(x\right),g\left(x\right)\right\}$, 则 $F\left(x\right)$ 也是凸函数.

### 解答 3.5-3

对任意 $x_1,x_2\in\left(a,b\right)$ 及 $t\in\left(0,1\right)$, 需证

$$
F\left(tx_1+\left(1-t\right)x_2\right)\le{t}F\left(x_1\right)+\left(1-t\right)F\left(x_2\right).
$$

因 $g,f$ 均为凸函数,

$$
f\left(tx_1+\left(1-t\right)x_2\right)\le{t}f\left(x_1\right)+\left(1-t\right)f\left(x_2\right)\le{t}F\left(x_1\right)+\left(1-t\right)F\left(x_2\right),
$$

$$
g\left(tx_1+\left(1-t\right)x_2\right)\le{t}g\left(x_1\right)+\left(1-t\right)g\left(x_2\right)\le{t}F\left(x_1\right)+\left(1-t\right)F\left(x_2\right).
$$

两式右端相同, 故 $\max\left\{f\left(\cdot\right),g\left(\cdot\right)\right\}\le{t}F\left(x_1\right)+\left(1-t\right)F\left(x_2\right)$. 故 $F$ 为凸函数. $\blacksquare$

## 3.5-5

设 $f\left(u\right)$ 在 $\left(-\infty,+\infty\right)$ 中是凸函数且递增. 又设 $g\left(x\right)$ 在 $\left(a,b\right)$ 区间上为凸函数, 证明复合函数 $f\left(g\left(x\right)\right)$ 是凸函数.

### 解答 3.5-5

对任意 $x_1,x_2\in\left(a,b\right)$ 及 $t\in\left(0,1\right)$, 因 $g$ 为凸函数,

$$
g\left(tx_1+\left(1-t\right)x_2\right)\le{t}g\left(x_1\right)+\left(1-t\right)g\left(x_2\right).
$$

又因 $f$ 为递增函数,

$$
f\left(g\left(tx_1+\left(1-t\right)x_2\right)\right)\le{f}\left(tg\left(x_1\right)+\left(1-t\right)g\left(x_2\right)\right).
$$

再由 $f$ 为凸函数,

$$
f\left(tg\left(x_1\right)+\left(1-t\right)g\left(x_2\right)\right)\le{t}f\left(g\left(x_1\right)\right)+\left(1-t\right)f\left(g\left(x_2\right)\right).
$$

合起来即得 $f\left(g\left(x\right)\right)$ 为凸函数. $\blacksquare$

## 3.5-6

设 $f\left(x\right)$ 在 $\left(-\infty,+\infty\right)$ 中是可微的凸函数, 且有界. 证明 $f\left(x\right)$ 为常数.

### 解答 3.5-6

因 $f$ 为凸函数, 由**定理 5.1 (凸函数的二阶导数判别)**, $f''\left(x\right)\ge0$, 故 $f'\left(x\right)$ 为递增函数.

反证: 假定存在 $x_0$ 使得 $f'\left(x_0\right)\ne0$. 若 $f'\left(x_0\right)>0$, 因 $f'$ 递增, 当 $x>{}x_0$ 时 $f'\left(x\right)\ge{f}'\left(x_0\right)>0$. 由**定理 1.3 (拉格朗日中值定理)**,

$$
f\left(x\right)=f\left(x_0\right)+f'\left(\xi\right)\left(x-x_0\right)\ge{f}\left(x_0\right)+f'\left(x_0\right)\left(x-x_0\right)\to+\infty,
$$

与 $f$ 有界矛盾. 若 $f'\left(x_0\right)<0$, 同理当 $x<{}x_0$ 时 $f'\left(x\right)\le{f}'\left(x_0\right)<0$, 推出 $f\left(x\right)\to+\infty$ ($x\to-\infty$), 同样矛盾.

故 $f'\left(x\right)\equiv0$, 即 $f$ 为常数. $\blacksquare$

## 3.5-7-1

作函数 $y=\frac{\left(x+1\right)^3}{\left(x-1\right)^2}$ 的图形.

### 解答 3.5-7-1

定义域: $\left(-\infty,1\right)\cup\left(1,+\infty\right)$.

渐近线: $\lim_{x\to1}y=\infty$, 故 $x=1$ 为垂直渐近线. 又 $\lim_{x\to\infty}\frac{y}x=1$, $\lim_{x\to\infty}\left(y-x\right)=5$, 故斜渐近线为 $y=x+5$.

单调区间与极值: $y'=\frac{\left(x+1\right)^2\left(x-5\right)}{\left(x-1\right)^3}$. 令 $y'=0$, 得 $x=-1$ 或 $x=5$. 当 $x<5$ 时 $y'\le0$ (除 $x=-1$ 外), 当 $x>5$ 时 $y'>0$. 故 $x=5$ 为极小值点, 极小值 $y\left(5\right)=\frac{27}2$. $x=-1$ 不是极值点.

凸凹性与拐点: $y''=\frac{16\left(x+1\right)}{\left(x-1\right)^4}$. 当 $x<-1$ 时 $y''<0$ (凹); 当 $x>-1$ 且 $x\ne1$ 时 $y''>0$ (凸). 拐点为 $\left(-1,0\right)$. $\blacksquare$

## 3.5-7-2

作函数 $y=xe^{-x}$ 的图形.

### 解答 3.5-7-2

定义域: $\left(-\infty,+\infty\right)$.

渐近线: $\lim_{x\to+\infty}xe^{-x}=0$, 故 $y=0$ 为水平渐近线.

单调区间与极值: $y'=\left(1-x\right)e^{-x}$. 令 $y'=0$, 得 $x=1$. 当 $x<1$ 时 $y'>0$, 当 $x>1$ 时 $y'<0$. 故 $x=1$ 为极大值点, 极大值 $y\left(1\right)=\frac1e$.

凸凹性与拐点: $y''=\left(x-2\right)e^{-x}$. 令 $y''=0$, 得 $x=2$. 当 $x<2$ 时 $y''<0$ (凹); 当 $x>2$ 时 $y''>0$ (凸). 拐点为 $\left(2,2e^{-2}\right)$. $\blacksquare$

## 3.5-7-3

作函数 $y=xe^{-x^2}$ 的图形.

### 解答 3.5-7-3

定义域: $\left(-\infty,+\infty\right)$. 函数为奇函数, 图形关于原点对称.

渐近线: $\lim_{x\to\pm\infty}xe^{-x^2}=0$, 故 $y=0$ 为水平渐近线.

单调区间与极值: $y'=\left(1-2x^2\right)e^{-x^2}$. 令 $y'=0$, 得 $x=\pm\frac1{\sqrt2}$. 当 $x<-\frac1{\sqrt2}$ 时 $y'<0$; 当 $-\frac1{\sqrt2}<{}x<\frac1{\sqrt2}$ 时 $y'>0$; 当 $x>\frac1{\sqrt2}$ 时 $y'<0$. 故 $x=-\frac1{\sqrt2}$ 为极小值点, 极小值 $-\frac1{\sqrt{2e}}$; $x=\frac1{\sqrt2}$ 为极大值点, 极大值 $\frac1{\sqrt{2e}}$.

凸凹性与拐点: $y''=2x\left(2x^2-3\right)e^{-x^2}$. 令 $y''=0$, 得 $x=0$ 或 $x=\pm\sqrt{\frac32}$. 拐点为 $\left(0,0\right)$ 及 $\left(\pm\sqrt{\frac32},\pm\sqrt{\frac32}e^{-3/2}\right)$. $\blacksquare$

## 4.1-1-1

求不定积分 $\int\left(x^3+4\right)\,\mathrm{d}x$.

### 解答 4.1-1-1

由**定理 1.3 (不定积分的线性法则)**,

$$
\int\left(x^3+4\right)\,\mathrm{d}x=\int{x}^3\,\mathrm{d}x+4\int1\,\mathrm{d}x=\frac{x^4}4+4x+C.
$$

$\blacksquare$

## 4.1-1-4

求不定积分 $\int\tan^2x\,\mathrm{d}x$.

### 解答 4.1-1-4

利用三角恒等式 $\tan^2x=\sec^2x-1$, 由**定理 1.3 (不定积分的线性法则)**,

$$
\int\tan^2x\,\mathrm{d}x=\int\left(\sec^2x-1\right)\,\mathrm{d}x=\tan{x}-x+C.
$$

$\blacksquare$
