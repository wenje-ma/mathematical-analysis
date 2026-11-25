# week20

> **定理 1.1 (柯西收敛原理)**
> 
> $\int_a^{+\infty}f\left(x\right)\mathrm{d}x$ 收敛的充要条件是: 对任意 $\varepsilon>0$, 存在 $X>0$, 使 $\left|\int_{A'}^{A''}f\left(x\right)\mathrm{d}x\right|<\varepsilon$ ($A',A''>X$).

> **定理 1.3 (比较判别法)**
> 
> 若 $0\le{}f\left(x\right)\le{}g\left(x\right)$ ($x\ge{}X_0$), 则 $\int{}g$ 收敛蕴含 $\int{}f$ 收敛, $\int{}f$ 发散蕴含 $\int{}g$ 发散.

> **定理 1.6 (狄利克雷判别法)**
> 
> 若 $f\left(x\right)$ 单调趋于零, 且 $\int_a^Ag\left(x\right)\mathrm{d}x$ 对任意 $A$ 有界, 则 $\int_a^{+\infty}f\left(x\right)g\left(x\right)\mathrm{d}x$ 收敛.

> **定理 3.2 (收敛半径的柯西公式)**
> 
> 幂级数 $\sum{}a_nx^n$ 的收敛半径 $R$ 满足 $\frac1R=\limsup_{n\to\infty}\sqrt[n]{\left|a_n\right|}$.

> **定理 3.3 (收敛半径的达朗贝尔公式)**
> 
> 若 $a_n\ne0$ 且 $\lim_{n\to\infty}\left|\frac{a_n}{a_{n+1}}\right|=R$, 则收敛半径为 $R$.

> **定理 3.4 (内闭一致收敛性)**
> 
> 幂级数在收敛区间内部的任意闭区间上一致收敛, 因而可逐项求导与逐项积分, 且收敛半径不变.

> **定理 4.1 (泰勒级数)**
> 
> 若 $f\left(x\right)$ 可展开为幂级数 $\sum{}a_n\left(x-x_0\right)^n$, 则 $a_n=\frac{f^{\left(n\right)}\left(x_0\right)}{n!}$, 展开唯一.

## 11.3-1-4

求 $\sum\frac{\left(n!\right)^2}{\left(2n\right)!}x^n$ 的收敛半径.

### 解答 11.3-1-4

$\left|\frac{a_n}{a_{n+1}}\right|=\frac{2\left(2n+1\right)}{n+1}\to4$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=4$.

$\blacksquare$

## 11.3-2-2

求 $\sum{}n^3\left(x-5\right)^n$ 的收敛点集合.

### 解答 11.3-2-2

令 $t=x-5$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=1$. 端点处通项不趋于零, 发散. 收敛域为 $\left(4,6\right)$.

$\blacksquare$

## 11.3-2-4

求 $\sum\frac{\left(-1\right)^n}{\sqrt{n}}x^n$ 的收敛点集合.

### 解答 11.3-2-4

由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=1$. $x=1$ 时为交错级数收敛; $x=-1$ 时为 $p=\frac12<1$ 的 $p$ 级数发散. 收敛域为 $\left(-1,1\right]$.

$\blacksquare$

## 11.3-2-6

求 $\sum\frac{\left(-1\right)^nx^n}{4^n\ln{}n}$ 的收敛点集合.

### 解答 11.3-2-6

由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=4$. 端点处发散. 收敛域为 $\left(-4,4\right)$.

$\blacksquare$

## 11.3-2-8

求 $\sum\left(1+\frac12+\cdots+\frac1n\right)x^n$ 的收敛点集合.

### 解答 11.3-2-8

由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=1$. 端点处 $h_n\to+\infty\ne0$, 发散. 收敛域为 $\left(-1,1\right)$.

$\blacksquare$

## 11.3-2-10

求 $\sum\frac{\left(-1\right)^n\left(2x+3\right)^n}{n\ln{}n}$ 的收敛点集合.

### 解答 11.3-2-10

令 $t=2x+3$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=1$. 端点处发散. 收敛域为 $\left(-2,-1\right)$.

$\blacksquare$

## 11.3-3-1

求 $\sum\left(n+1\right)x^n$ 的和函数.

### 解答 11.3-3-1

由**定理 3.4 (内闭一致收敛性)**, 逐项求导: $\sum\left(n+1\right)x^n=\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{x}{1-x}\right)=\frac1{\left(1-x\right)^2}$.

$\blacksquare$

## 11.3-3-3

求 $\sum{}n^2x^n$ 的和函数.

### 解答 11.3-3-3

由 $n^2=n\left(n-1\right)+n$ 及**定理 3.4 (内闭一致收敛性)**, 逐项求导两次与一次, 得 $\sum{}n^2x^n=\frac{x\left(1+x\right)}{\left(1-x\right)^3}$.

$\blacksquare$

## 11.3-3-5

求 $\sum\frac{x^n}{n\left(n+1\right)}$ 的和函数.

### 解答 11.3-3-5

裂项 $\frac1{n\left(n+1\right)}=\frac1n-\frac1{n+1}$, 利用 $\sum\frac{x^n}n=-\ln\left(1-x\right)$, 得 $1-\frac{1-x}x\ln\left(1-x\right)$.

$\blacksquare$

## 11.3-3-7

求 $\sum\frac{x^n}n$ 的和函数.

### 解答 11.3-3-7

由**定理 3.4 (内闭一致收敛性)**, 逐项求导得 $\frac{\mathrm{d}}{\mathrm{d}x}\sum\frac{x^n}n=\frac1{1-x}$. 积分得 $\sum\frac{x^n}n=-\ln\left(1-x\right)$.

$\blacksquare$

## 11.3-4

证明: 若 $\sum{}a_nx^n$ 的收敛半径为 $R$, 则 $\sum{}a_nx^{2n}$ 的收敛半径为 $\sqrt{R}$.

### 解答 11.3-4

令 $y=x^2$. 由**定理 3.2 (收敛半径的柯西公式)**, $\sum{}a_ny^n$ 当 $\left|y\right|<{}R$ 时收敛, 即 $\left|x\right|<\sqrt{R}$.

$\blacksquare$

## 11.3-5

证明: 若收敛半径为 $R$, 则对任意 $A>\frac1R$, 存在 $C>0$ 使 $\left|a_n\right|\le{}CA^n$.

### 解答 11.3-5

取 $r$ 满足 $\frac1A<{}r<{}R$. 因 $a_nr^n\to0$, 有界, 故 $\left|a_n\right|\le{}Mr^{-n}$. 取 $C=M\max\left(1,\frac1{rA}\right)$ 即得.

$\blacksquare$

## 11.4-1-3

求 $f\left(x\right)=e^x$ 在 $x_0=3$ 处的幂级数展开式.

### 解答 11.4-1-3

令 $t=x-3$, 由基本展开式, $e^x=e^3\sum_{n=0}^\infty\frac{\left(x-3\right)^n}{n!}$. 由**定理 4.1 (泰勒级数)**, 此即泰勒展开式.

$\blacksquare$

## 11.4-1-4

求 $f\left(x\right)=\ln{}x$ 在 $x_0=2$ 处的幂级数展开式.

### 解答 11.4-1-4

$\ln{}x=\ln2+\ln\left(1+\frac{x-2}2\right)$. 由基本展开式, $\ln{}x=\ln2+\sum_{n=1}^\infty\frac{\left(-1\right)^{n-1}}{n\cdot2^n}\left(x-2\right)^n$, $0<{}x<4$.

$\blacksquare$

## 11.4-1-5

求 $f\left(x\right)=\cos^2x$ 在 $x_0=0$ 处的幂级数展开式.

### 解答 11.4-1-5

由半角公式 $\cos^2x=\frac{1+\cos2x}2$. 由基本展开式, $\cos^2x=\frac12+\sum_{n=0}^\infty\frac{\left(-1\right)^n2^{2n-1}}{\left(2n\right)!}x^{2n}$.

$\blacksquare$
