# week33

> **定理 1.1 (柯西收敛原理)**
> 
> $\int_a^{+\infty}f\left(x\right)\mathrm{d}x$ 收敛的充要条件是: 对任意 $\varepsilon>0$, 存在 $X>0$, 使 $\left|\int_{A'}^{A''}f\left(x\right)\mathrm{d}x\right|<\varepsilon$ ($A',A''>{}X$).

> **例 1.2 (p-积分)**
> 
> $\int_1^{+\infty}\frac{\mathrm{d}x}{x^p}$ 当 $p>1$ 时收敛, 当 $p\le1$ 时发散.

> **定理 1.3 (比较判别法)**
> 
> 若 $0\le{f}\left(x\right)\le{g}\left(x\right)$ ($x\ge{X}_0$), 则 $\int{g}$ 收敛蕴含 $\int{f}$ 收敛, $\int{f}$ 发散蕴含 $\int{g}$ 发散.

> **定理 1.6 (狄利克雷判别法)**
> 
> 若 $f\left(x\right)$ 单调趋于零, 且 $\int_a^Ag\left(x\right)\mathrm{d}x$ 对任意 $A$ 有界, 则 $\int_a^{+\infty}f\left(x\right)g\left(x\right)\mathrm{d}x$ 收敛.

> **定理 3.2 (收敛半径的柯西公式)**
> 
> 幂级数 $\sum{a}_nx^n$ 的收敛半径 $R$ 满足 $\frac1R=\limsup_{n\to\infty}\sqrt\left[n\right]{\left|a_n\right|}$.

> **定理 3.3 (收敛半径的达朗贝尔公式)**
> 
> 若 $a_n\ne0$ 且 $\lim_{n\to\infty}\left|\frac{a_n}{a_{n+1}}\right|=R$, 则收敛半径为 $R$.

> **定理 3.4 (内闭一致收敛性)**
> 
> 幂级数在收敛区间内部的任意闭区间上一致收敛, 因而可逐项求导与逐项积分, 且收敛半径不变.

> **定理 4.1 (泰勒级数)**
> 
> 若 $f\left(x\right)$ 可展开为幂级数 $\sum{a}_n\left(x-x_0\right)^n$, 则 $a_n=\frac{f^{\left(n\right)}\left(x_0\right)}{n!}$, 展开唯一.

## 11.3-2-8

求 $\sum\left(1+\frac12+\cdots+\frac1n\right)x^n$ 的收敛点集合.

### 解答 11.3-2-8

由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=1$. 端点处 $h_n\to+\infty\ne0$, 发散. 收敛域为 $\left(-1,1\right)$. $\blacksquare$

## 11.3-2-10

求 $\sum\frac{\left(-1\right)^n\left(2x+3\right)^n}{n\ln{n}}$ 的收敛点集合.

### 解答 11.3-2-10

令 $t=2x+3$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=1$. 端点处发散. 收敛域为 $\left(-2,-1\right)$. $\blacksquare$

## 11.3-3-1

求 $\sum\left(n+1\right)x^n$ 的和函数.

### 解答 11.3-3-1

由**定理 3.4 (内闭一致收敛性)**, 逐项求导: $\sum\left(n+1\right)x^n=\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{x}{1-x}\right)=\frac1{\left(1-x\right)^2}$. $\blacksquare$

## 11.3-3-3

求 $\sum{n}^2x^n$ 的和函数.

### 解答 11.3-3-3

由 $n^2=n\left(n-1\right)+n$ 及**定理 3.4 (内闭一致收敛性)**, 逐项求导两次与一次, 得 $\sum{n}^2x^n=\frac{x\left(1+x\right)}{\left(1-x\right)^3}$. $\blacksquare$

## 11.3-3-5

求 $\sum\frac{x^n}{n\left(n+1\right)}$ 的和函数.

### 解答 11.3-3-5

裂项 $\frac1{n\left(n+1\right)}=\frac1n-\frac1{n+1}$, 利用 $\sum\frac{x^n}n=-\ln\left(1-x\right)$, 得 $1-\frac{1-x}x\ln\left(1-x\right)$. $\blacksquare$

## 11.3-3-7

求 $\sum\frac{x^n}n$ 的和函数.

### 解答 11.3-3-7

由**定理 3.4 (内闭一致收敛性)**, 逐项求导得 $\frac{\mathrm{d}}{\mathrm{d}x}\sum\frac{x^n}n=\frac1{1-x}$. 积分得 $\sum\frac{x^n}n=-\ln\left(1-x\right)$. $\blacksquare$

## 11.3-4

证明: 若 $\sum{a}_nx^n$ 的收敛半径为 $R$, 则 $\sum{a}_nx^{2n}$ 的收敛半径为 $\sqrt{R}$.

### 解答 11.3-4

令 $y=x^2$. 由**定理 3.2 (收敛半径的柯西公式)**, $\sum{a}_ny^n$ 当 $\left|y\right|<{}R$ 时收敛, 即 $\left|x\right|<\sqrt{R}$. $\blacksquare$

## 11.3-5

证明: 若收敛半径为 $R$, 则对任意 $A>\frac1R$, 存在 $C>0$ 使 $\left|a_n\right|\le{C}A^n$.

### 解答 11.3-5

取 $r$ 满足 $\frac1A<{}r<{}R$. 因 $a_nr^n\to0$, 有界, 故 $\left|a_n\right|\le{M}r^{-n}$. 取 $C=M\max\left(1,\frac1{rA}\right)$ 即得. $\blacksquare$

## 11.4-1-3

求 $f\left(x\right)=e^x$ 在 $x_0=3$ 处的幂级数展开式.

### 解答 11.4-1-3

令 $t=x-3$, 由基本展开式, $e^x=e^3\sum_{n=0}^\infty\frac{\left(x-3\right)^n}{n!}$. 由**定理 4.1 (泰勒级数)**, 此即泰勒展开式. $\blacksquare$

## 11.4-1-4

求 $f\left(x\right)=\ln{x}$ 在 $x_0=2$ 处的幂级数展开式.

### 解答 11.4-1-4

$\ln{x}=\ln2+\ln\left(1+\frac{x-2}2\right)$. 由基本展开式, $\ln{x}=\ln2+\sum_{n=1}^\infty\frac{\left(-1\right)^{n-1}}{n\cdot2^n}\left(x-2\right)^n$, $0<{}x<4$. $\blacksquare$

## 11.4-1-5

求 $f\left(x\right)=\cos^2x$ 在 $x_0=0$ 处的幂级数展开式.

### 解答 11.4-1-5

由半角公式 $\cos^2x=\frac{1+\cos2x}2$. 由基本展开式, $\cos^2x=\frac12+\sum_{n=0}^\infty\frac{\left(-1\right)^n2^{2n-1}}{\left(2n\right)!}x^{2n}$. $\blacksquare$

## 11.4-2

证明 $\sum_{n=0}^\infty\frac{x^n}{\left(n+1\right)!}=\frac1x\left(e^x-1\right)$, 并推出 $\sum_{n=1}^\infty\frac{n}{\left(n+1\right)!}=1$.

### 解答 11.4-2

由基本展开式, $e^x-1=x\sum_{n=0}^\infty\frac{x^n}{\left(n+1\right)!}$. 两边除以 $x$ 即得第一式. 对 $x$ 求导, 令 $x=1$, 得 $\sum_{n=1}^\infty\frac{n}{\left(n+1\right)!}=1$. $\blacksquare$

## 11.4-3

证明 $\sum_{n=1}^\infty\frac{n}{\left(n+2\right)!}=3-e$.

### 解答 11.4-3

改写 $\frac{n}{\left(n+2\right)!}=\frac1{\left(n+1\right)!}-\frac2{\left(n+2\right)!}$. 利用 $e=\sum_{m=0}^\infty\frac1{m!}$, 计算得 $3-e$. $\blacksquare$

## 12.1-1-1

判别 $\int_1^{+\infty}\frac{\ln{x}}{x^2}\mathrm{d}x$ 是否收敛, 若收敛求其值.

### 解答 12.1-1-1

分部积分得 $-\frac{\ln{A}}A+1-\frac1A\to1$. 由无穷积分收敛的定义, 收敛且值为 $1$. $\blacksquare$

## 12.1-1-2

判别 $\int_1^{+\infty}e^{-ax}\mathrm{d}x$ ($a>0$).

### 解答 12.1-1-2

$\frac{e^{-a}-e^{-aA}}a\to\frac{e^{-a}}a$. 收敛. $\blacksquare$

## 12.1-1-3

判别 $\int_0^{+\infty}\frac{\mathrm{d}x}{1+x^2}$.

### 解答 12.1-1-3

$\arctan{A}\to\frac\pi2$. 收敛. $\blacksquare$

## 12.1-1-4

判别 $\int_0^{+\infty}xe^{-x}\mathrm{d}x$.

### 解答 12.1-1-4

分部积分得 $1$. 收敛. $\blacksquare$

## 12.1-2-1

讨论 $\int_1^{+\infty}\frac{\sin{x}}{x^p}\mathrm{d}x$ 的绝对收敛性与条件收敛性.

### 解答 12.1-2-1

(1) $p>1$: 由 $\left|\frac{\sin{x}}{x^p}\right|\le\frac1{x^p}$ 及**例 1.2 (p-积分)** 与**定理 1.3 (比较判别法)**, 绝对收敛.

(2) $0<{}p\le1$: 由**定理 1.6 (狄利克雷判别法)**, 收敛. 又 $\frac{\left|\sin{x}\right|}{x^p}\ge\frac1{2x^p}-\frac{\cos2x}{2x^p}$, 其中 $\int\frac1{x^p}$ 发散, $\int\frac{\cos2x}{x^p}$ 收敛, 故不绝对收敛. 条件收敛.

(3) $p\le0$: 由**定理 1.1 (柯西收敛原理)**, 发散. $\blacksquare$

## 12.1-2-3

讨论 $\int_1^{+\infty}\frac{\sqrt{x}\cos{x}}{x+3}\mathrm{d}x$.

### 解答 12.1-2-3

由**定理 1.6 (狄利克雷判别法)**, 收敛. 又 $\frac{\sqrt{x}\left|\cos{x}\right|}{x+3}\ge\frac1{8\sqrt{x}}+\frac{\cos2x}{8\sqrt{x}}$, 其中 $\int\frac1{\sqrt{x}}$ 发散, 故不绝对收敛. 条件收敛. $\blacksquare$

## 12.1-2-5

讨论 $\int_0^{+\infty}\sin{x}^2\mathrm{d}x$.

### 解答 12.1-2-5

代换 $t=x^2$ 得 $\frac12\int_1^{+\infty}\frac{\sin{t}}{\sqrt{t}}\mathrm{d}t$. 由**定理 1.6 (狄利克雷判别法)**, 收敛. 同理不绝对收敛. 条件收敛. $\blacksquare$
