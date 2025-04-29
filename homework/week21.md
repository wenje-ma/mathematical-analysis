# week21

> **定理 1.1 (柯西收敛原理)**
> 
> $\int_a^{+\infty}f\left(x\right)\mathrm{d}x$ 收敛的充要条件是: 对任意 $\varepsilon>0$, 存在 $X>0$, 使 $\left|\int_{A'}^{A''}f\left(x\right)\mathrm{d}x\right|<\varepsilon$ ($A',A''>X$).

> **定理 1.3 (比较判别法)**
> 
> 若 $0\le{f}\left(x\right)\le{g}\left(x\right)$ ($x\ge{X}_0$), 则 $\int{g}$ 收敛蕴含 $\int{f}$ 收敛, $\int{f}$ 发散蕴含 $\int{g}$ 发散.

> **定理 1.6 (狄利克雷判别法)**
> 
> 若 $f\left(x\right)$ 单调趋于零, 且 $\int_a^Ag\left(x\right)\mathrm{d}x$ 对任意 $A$ 有界, 则 $\int_a^{+\infty}f\left(x\right)g\left(x\right)\mathrm{d}x$ 收敛.

> **定理 3.2 (收敛半径的柯西公式)**
> 
> 幂级数 $\sum{a}_nx^n$ 的收敛半径 $R$ 满足 $\frac1R=\limsup_{n\to\infty}\sqrt[n]{\left|a_n\right|}$.

> **定理 3.3 (收敛半径的达朗贝尔公式)**
> 
> 若 $a_n\ne0$ 且 $\lim_{n\to\infty}\left|\frac{a_n}{a_{n+1}}\right|=R$, 则收敛半径为 $R$.

> **定理 3.4 (内闭一致收敛性)**
> 
> 幂级数在收敛区间内部的任意闭区间上一致收敛, 因而可逐项求导与逐项积分, 且收敛半径不变.

> **定理 4.1 (泰勒级数)**
> 
> 若 $f\left(x\right)$ 可展开为幂级数 $\sum{a}_n\left(x-x_0\right)^n$, 则 $a_n=\frac{f^{\left(n\right)}\left(x_0\right)}{n!}$, 展开唯一.

## 11.4-2

证明 $\sum_{n=0}^\infty\frac{x^n}{\left(n+1\right)!}=\frac1x\left(e^x-1\right)$, 并推出 $\sum_{n=1}^\infty\frac{n}{\left(n+1\right)!}=1$.

### 解答 11.4-2

由基本展开式, $e^x-1=x\sum_{n=0}^\infty\frac{x^n}{\left(n+1\right)!}$. 两边除以 $x$ 即得第一式. 对 $x$ 求导, 令 $x=1$, 得 $\sum_{n=1}^\infty\frac{n}{\left(n+1\right)!}=1$.

$\blacksquare$

## 11.4-3

证明 $\sum_{n=1}^\infty\frac{n}{\left(n+2\right)!}=3-e$.

### 解答 11.4-3

改写 $\frac{n}{\left(n+2\right)!}=\frac1{\left(n+1\right)!}-\frac2{\left(n+2\right)!}$. 利用 $e=\sum_{m=0}^\infty\frac1{m!}$, 计算得 $3-e$.

$\blacksquare$

## 12.1-1-1

判别 $\int_1^{+\infty}\frac{\ln{x}}{x^2}\mathrm{d}x$ 是否收敛, 若收敛求其值.

### 解答 12.1-1-1

分部积分得 $-\frac{\ln{A}}A+1-\frac1A\to1$. 由无穷积分收敛的定义, 收敛且值为 $1$.

$\blacksquare$

## 12.1-1-2

判别 $\int_1^{+\infty}e^{-ax}\mathrm{d}x$ ($a>0$).

### 解答 12.1-1-2

$\frac{e^{-a}-e^{-aA}}a\to\frac{e^{-a}}a$. 收敛.

$\blacksquare$

## 12.1-1-3

判别 $\int_0^{+\infty}\frac{\mathrm{d}x}{1+x^2}$.

### 解答 12.1-1-3

$\arctan{A}\to\frac\pi2$. 收敛.

$\blacksquare$

## 12.1-1-4

判别 $\int_0^{+\infty}xe^{-x}\mathrm{d}x$.

### 解答 12.1-1-4

分部积分得 $1$. 收敛.

$\blacksquare$

## 12.1-2-1

讨论 $\int_1^{+\infty}\frac{\sin{x}}{x^p}\mathrm{d}x$ 的绝对收敛性与条件收敛性.

### 解答 12.1-2-1

(1) $p>1$: 由 $\left|\frac{\sin{x}}{x^p}\right|\le\frac1{x^p}$ 及**例 1.2 (p-积分)** 与**定理 1.3 (比较判别法)**, 绝对收敛.

(2) $0<{}p\le1$: 由**定理 1.6 (狄利克雷判别法)**, 收敛. 又 $\frac{\left|\sin{x}\right|}{x^p}\ge\frac1{2x^p}-\frac{\cos2x}{2x^p}$, 其中 $\int\frac1{x^p}$ 发散, $\int\frac{\cos2x}{x^p}$ 收敛, 故不绝对收敛. 条件收敛.

(3) $p\le0$: 由**定理 1.1 (柯西收敛原理)**, 发散.

$\blacksquare$

## 12.1-2-3

讨论 $\int_1^{+\infty}\frac{\sqrt{x}\cos{x}}{x+3}\mathrm{d}x$.

### 解答 12.1-2-3

由**定理 1.6 (狄利克雷判别法)**, 收敛. 又 $\frac{\sqrt{x}\left|\cos{x}\right|}{x+3}\ge\frac1{8\sqrt{x}}+\frac{\cos2x}{8\sqrt{x}}$, 其中 $\int\frac1{\sqrt{x}}$ 发散, 故不绝对收敛. 条件收敛.

$\blacksquare$

## 12.1-2-5

讨论 $\int_0^{+\infty}\sin{x}^2\mathrm{d}x$.

### 解答 12.1-2-5

代换 $t=x^2$ 得 $\frac12\int_1^{+\infty}\frac{\sin{t}}{\sqrt{t}}\mathrm{d}t$. 由**定理 1.6 (狄利克雷判别法)**, 收敛. 同理不绝对收敛. 条件收敛.

$\blacksquare$

## 12.1-3

证明 $I_1\left(x\right)=\int_0^{+\infty}e^{-xt}\sin{t}\mathrm{d}t$ 与 $I_2\left(x\right)=\int_0^{+\infty}e^{-xt}\cos{t}\mathrm{d}t$ 绝对收敛并求值.

### 解答 12.1-3

由 $\left|e^{-xt}\sin{t}\right|\le{e}^{-xt}$ 及**定理 1.3 (比较判别法)**, 绝对收敛. 分部积分联立方程解得 $I_1=\frac1{x^2+1}$, $I_2=\frac{x}{x^2+1}$.

$\blacksquare$

## 12.1-4

证明 $\int_{-\infty}^{+\infty}f\left(-x\right)\mathrm{d}x=\int_{-\infty}^{+\infty}f\left(x\right)\mathrm{d}x$ 及 $\int_{-\infty}^{+\infty}f\left(x+a\right)\mathrm{d}x=\int_{-\infty}^{+\infty}f\left(x\right)\mathrm{d}x$.

### 解答 12.1-4

作代换 $u=-x$ 与 $u=x+a$, 由无穷积分收敛的定义, 等式成立.

$\blacksquare$

## 12.1-5

设 $a_n=\int_n^{n+1}f\left(x\right)\mathrm{d}x$. 证明 $\int_1^{+\infty}f\left(x\right)\mathrm{d}x$ 收敛当且仅当 $\sum{a}_n$ 收敛.

### 解答 12.1-5

$\sum_{n=1}^Na_n=\int_1^{N+1}f\left(x\right)\mathrm{d}x$. 由 $f\left(x\right)\to0$, 相邻整数点之间的积分差趋于零. 由无穷积分收敛的定义, 等价成立.

$\blacksquare$

## 12.2-1-1

判断 $\int_0^1\ln{x}\mathrm{d}x$ 的收敛性.

### 解答 12.2-1-1

分部积分得 $-1-\eta\ln\eta+\eta\to-1$. 由瑕积分收敛的定义, 收敛且值为 $-1$.

$\blacksquare$

## 12.2-1-3

判断 $\int_{-1}^1\frac{\mathrm{d}x}{\sqrt{1-x^2}}$.

### 解答 12.2-1-3

拆为两段, 各趋于 $\frac\pi2$. 收敛且值为 $\pi$.

$\blacksquare$

## 12.2-1-5

判断 $\int_0^1\frac{\mathrm{d}x}{x\ln^2x}$.

### 解答 12.2-1-5

代换 $u=\ln{x}$, 得 $-\frac1{\ln\left(1-\eta\right)}+\frac1{\ln\left(1/2\right)}\to+\infty$. 发散.

$\blacksquare$
