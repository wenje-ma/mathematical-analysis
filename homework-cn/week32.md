# week32

> **定理 1.1 (M 判别法)**
> 
> 若存在 $M_n>0$, $M_n\to0$, 使 $\left|f_n\left(x\right)-f\left(x\right)\right|\le{M}_n$ 对一切 $x\in{X}$ 成立, 则 $\left\{f_n\right\}$ 在 $X$ 上一致收敛于 $f$.

> **定理 1.2 (极限函数的连续性)**
> 
> 若 $\left\{f_n\right\}$ 在区间 $X$ 上一致收敛于 $f$, 且每个 $f_n$ 连续, 则 $f$ 在 $X$ 上连续.

> **定理 2.2 (魏尔斯特拉斯 M 判别法)**
> 
> 若 $\left|u_n\left(x\right)\right|\le{a}_n$ 对一切 $x\in{X}$ 成立, 且 $\sum{a}_n$ 收敛, 则 $\sum{u}_n\left(x\right)$ 在 $X$ 上一致收敛.

> **定理 2.4 (狄利克雷判别法)**
> 
> 若 $\sum{a}_n\left(x\right)$ 的部分和一致有界, $b_n\left(x\right)$ 单调且一致趋于零, 则 $\sum{a}_n\left(x\right)b_n\left(x\right)$ 一致收敛.

> **定理 2.5 (和函数的连续性)**
> 
> 若 $u_n\left(x\right)$ 连续且 $\sum{u}_n\left(x\right)$ 一致收敛, 则和函数 $S\left(x\right)$ 连续.

> **定理 2.7 (逐项求导定理)**
> 
> 若 $\sum{u}_n\left(x\right)$ 收敛, $u_n'\left(x\right)$ 连续, 且 $\sum{u}_n'\left(x\right)$ 一致收敛, 则 $S'\left(x\right)=\sum{u}_n'\left(x\right)$.

> **定理 3.2 (收敛半径的柯西公式)**
> 
> 幂级数 $\sum{a}_nx^n$ 的收敛半径 $R$ 满足 $\frac1R=\limsup_{n\to\infty}\sqrt\left[n\right]{\left|a_n\right|}$.

> **定理 3.3 (收敛半径的达朗贝尔公式)**
> 
> 若 $a_n\ne0$ 且 $\lim_{n\to\infty}\left|\frac{a_n}{a_{n+1}}\right|=R$, 则收敛半径为 $R$.

> **定理 3.4 (内闭一致收敛性)**
> 
> 幂级数在收敛区间内部的任意闭区间上一致收敛, 因而可逐项求导与逐项积分, 且收敛半径不变.

## 11.1-3

证明 $f_n\left(x\right)=\left(1+\frac{x}n\right)^n$ 在 $\left[0,+\infty\right)$ 上不一致收敛于 $e^x$.

### 解答 11.1-3

取 $x_n=n$, 则 $\left|f_n\left(x_n\right)-e^{x_n}\right|=e^n-2^n\to+\infty$. 由函数序列一致收敛的定义, 不一致收敛. $\blacksquare$

## 11.1-4

证明 $f_n\left(x\right)=\left(1+\frac{x}n\right)^n$ 在任一闭区间 $\left[0,A\right]$ 上一致收敛于 $e^x$.

### 解答 11.1-4

由不等式 $0\le{e}^x-\left(1+\frac{x}n\right)^n\le{e}^A\cdot\frac{A^2}{2n}=M_n$, $M_n\to0$. 由**定理 1.1 (M 判别法)**, 一致收敛. $\blacksquare$

## 11.1-5

设 $f$ 及 $f_n$ 均连续, $M_n=\max_{x\in\left[a,b\right]}\left|f_n\left(x\right)-f\left(x\right)\right|$. 证明: $f_n$ 在 $\left[a,b\right]$ 上一致收敛于 $f$ 当且仅当 $M_n\to0$.

### 解答 11.1-5

必要性: 由一致收敛性直接得 $M_n<\varepsilon$. 充分性: 由 $M_n\to0$, 对一切 $x$ 有 $\left|f_n\left(x\right)-f\left(x\right)\right|\le{M}_n<\varepsilon$. 由函数序列一致收敛的定义, 一致收敛. $\blacksquare$

## 11.2-1-2

讨论 $\sum\frac{\left(-1\right)^{n+1}}{x^2+n}$ 在 $\mathbb{R}$ 上的一致收敛性.

### 解答 11.2-1-2

令 $a_n=\left(-1\right)^{n+1}$, $b_n=\frac1{x^2+n}$. 部分和一致有界, $b_n$ 单调且 $\left|b_n\right|\le\frac1n\to0$ 一致. 由**定理 2.4 (狄利克雷判别法)**, 一致收敛. $\blacksquare$

## 11.2-1-4

讨论 $\sum\frac{x}{\left(1+\left(n-1\right)x\right)\left(1+nx\right)}$ 在 $\left(0,+\infty\right)$ 上的一致收敛性.

### 解答 11.2-1-4

裂项得 $S_N\left(x\right)=1-\frac1{1+Nx}$. 和函数在 $x=0$ 处不连续(右极限为 $1$, 值为 $0$). 由**定理 2.5 (和函数的连续性)**, 若一致收敛则和函数必连续, 矛盾. 故不一致收敛. $\blacksquare$

## 11.2-1-6

讨论 $\sum\frac1{n^2+x^2}$ 在 $\left[0,+\infty\right)$ 上的一致收敛性.

### 解答 11.2-1-6

因 $\left|\frac1{n^2+x^2}\right|\le\frac1{n^2}$, 及**定理 2.2 (魏尔斯特拉斯 M 判别法)**, 一致收敛. $\blacksquare$

## 11.2-9

讨论 $\sum\left(-1\right)^n\frac{n+x^2}{n^2}$ 在 $\left[a,b\right]$ 及 $\mathbb{R}$ 上的一致收敛性.

### 解答 11.2-9

(i) 在 $\left[a,b\right]$ 上, $b_n=\frac1n+\frac{x^2}{n^2}$ 单调且 $\le\frac1n+\frac{C}{n^2}\to0$ 一致. 由**定理 2.4 (狄利克雷判别法)**, 一致收敛.

(ii) 在 $\mathbb{R}$ 上, $\sup_{x\in\mathbb{R}}\frac{x^2}{n^2}=+\infty$, 通项不一致趋于零. 故不一致收敛. $\blacksquare$

## 11.2-10

讨论 $\sum\left(-1\right)^{n-1}x^2e^{-nx^2}$ 在 $\mathbb{R}$ 上的一致收敛性.

### 解答 11.2-1-10

令 $t=x^2\ge0$, $\max_{t\ge0}te^{-nt}=\frac1{en}\to0$ 一致. 由**定理 2.4 (狄利克雷判别法)**, 一致收敛. $\blacksquare$

## 11.2-11

讨论 $\sum\frac{\sin{x}\sin{n}x}{\sqrt{n^2+x^2}}$ 在 $\left[0,2\pi\right]$ 上的一致收敛性.

### 解答 11.2-11

$\sin{x}\sum_{k=1}^N\sin{k}x$ 一致有界. $b_n=\frac{\sin{x}}{\sqrt{n^2+x^2}}\le\frac1n\to0$ 一致. 由**定理 2.4 (狄利克雷判别法)**, 一致收敛. $\blacksquare$

## 11.2-5

证明 $f\left(x\right)=\sum2^n\sin\frac{x}{3^n}$ 在 $\mathbb{R}$ 上处处有连续的导函数.

### 解答 11.2-5

逐项求导得 $u_n'\left(x\right)=\left(\frac23\right)^n\cos\frac{x}{3^n}$. 因 $\left|u_n'\left(x\right)\right|\le\left(\frac23\right)^n$, 及**定理 2.2 (魏尔斯特拉斯 M 判别法)**, 求导级数一致收敛. 由**定理 2.7 (逐项求导定理)**, $f'\left(x\right)=\sum\left(\frac23\right)^n\cos\frac{x}{3^n}$. 由**定理 2.5 (和函数的连续性)**, $f'\left(x\right)$ 连续. $\blacksquare$

## 11.2-6

设 $\zeta\left(x\right)=\sum\frac1{n^x}$ ($x>1$), 证明 $\zeta'\left(x\right)$ 存在并给出表达式.

### 解答 11.2-6

对任意 $a>1$, 在 $\left[a,+\infty\right)$ 上, $\left|\frac{\ln{n}}{n^x}\right|\le\frac{\ln{n}}{n^a}$, 而 $\sum\frac{\ln{n}}{n^a}$ 收敛. 由**定理 2.2 (魏尔斯特拉斯 M 判别法)** 与**定理 2.7 (逐项求导定理)**, $\zeta'\left(x\right)=-\sum\frac{\ln{n}}{n^x}$. $\blacksquare$

## 11.3-1-1

求 $\sum\frac{3^n}{n!}x^n$ 的收敛半径.

### 解答 11.3-1-1

$\left|\frac{a_n}{a_{n+1}}\right|=\frac{n+1}3\to+\infty$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=+\infty$. $\blacksquare$

## 11.3-1-2

求 $\sum\frac{n}{2^n}x^n$ 的收敛半径.

### 解答 11.3-1-2

$\left|\frac{a_n}{a_{n+1}}\right|=\frac{2n}{n+1}\to2$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=2$. $\blacksquare$

## 11.3-1-3

求 $\sum\frac{n!}{\left(2n\right)!}x^n$ 的收敛半径.

### 解答 11.3-1-3

$\left|\frac{a_n}{a_{n+1}}\right|=2\left(2n+1\right)\to+\infty$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=+\infty$. $\blacksquare$

## 11.3-1-4

求 $\sum\frac{\left(n!\right)^2}{\left(2n\right)!}x^n$ 的收敛半径.

### 解答 11.3-1-4

$\left|\frac{a_n}{a_{n+1}}\right|=\frac{2\left(2n+1\right)}{n+1}\to4$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=4$. $\blacksquare$

## 11.3-2-2

求 $\sum{n}^3\left(x-5\right)^n$ 的收敛点集合.

### 解答 11.3-2-2

令 $t=x-5$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=1$. 端点处通项不趋于零, 发散. 收敛域为 $\left(4,6\right)$. $\blacksquare$

## 11.3-2-4

求 $\sum\frac{\left(-1\right)^n}{\sqrt{n}}x^n$ 的收敛点集合.

### 解答 11.3-2-4

由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=1$. $x=1$ 时为交错级数收敛; $x=-1$ 时为 $p=\frac12<1$ 的 $p$ 级数发散. 收敛域为 $\left(-1,1\right]$. $\blacksquare$

## 11.3-2-6

求 $\sum\frac{\left(-1\right)^nx^n}{4^n\ln{n}}$ 的收敛点集合.

### 解答 11.3-2-6

由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=4$. 端点处发散. 收敛域为 $\left(-4,4\right)$. $\blacksquare$
