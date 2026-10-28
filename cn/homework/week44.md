# week44

> **定理 3.2 (收敛半径的柯西公式)**<br>幂级数 $\sum a_nx^n$ 的收敛半径 $R$ 满足 $\frac1R=\limsup_{n\to\infty}\sqrt[n]{\left|a_n\right|}$.

> **定理 3.3 (收敛半径的达朗贝尔公式)**<br>若 $a_n\ne0$ 且 $\lim_{n\to\infty}\left|\frac{a_n}{a_{n+1}}\right|=R$, 则收敛半径为 $R$.

> **定理 3.4 (内闭一致收敛性)**<br>幂级数在收敛区间内部的任意闭区间上一致收敛, 因而可逐项求导与逐项积分, 且收敛半径不变.

---

## 11.3-1-1

求 $\sum\frac{3^n}{n!}x^n$ 的收敛半径.

### 解答 11.3-1-1

$\left|\frac{a_n}{a_{n+1}}\right|=\frac{n+1}3\to+\infty$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=+\infty$. $\blacksquare$

---

## 11.3-1-2

求 $\sum\frac n{2^n}x^n$ 的收敛半径.

### 解答 11.3-1-2

$\left|\frac{a_n}{a_{n+1}}\right|=\frac{2n}{n+1}\to2$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=2$. $\blacksquare$

---

## 11.3-1-3

求 $\sum\frac{n!}{\left(2n\right)!}x^n$ 的收敛半径.

### 解答 11.3-1-3

$\left|\frac{a_n}{a_{n+1}}\right|=2\left(2n+1\right)\to+\infty$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=+\infty$. $\blacksquare$

---

## 11.3-1-4

求 $\sum\frac{\left(n!\right)^2}{\left(2n\right)!}x^n$ 的收敛半径.

### 解答 11.3-1-4

$\left|\frac{a_n}{a_{n+1}}\right|=\frac{2\left(2n+1\right)}{n+1}\to4$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=4$. $\blacksquare$

---

## 11.3-2-2

求 $\sum n^3\left(x-5\right)^n$ 的收敛点集合.

### 解答 11.3-2-2

令 $t=x-5$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=1$. 端点处通项不趋于零, 发散. 收敛域为 $\left(4,6\right)$. $\blacksquare$

---

## 11.3-2-4

求 $\sum\frac{\left(-1\right)^n}{\sqrt n}x^n$ 的收敛点集合.

### 解答 11.3-2-4

由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=1$. $x=1$ 时为交错级数收敛; $x=-1$ 时为 $p=\frac12< 1$ 的 $p$ 级数发散. 收敛域为 $\left(-1,1\right]$. $\blacksquare$

---

## 11.3-2-6

求 $\sum\frac{\left(-1\right)^nx^n}{4^n\ln n}$ 的收敛点集合.

### 解答 11.3-2-6

由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=4$. 端点处发散. 收敛域为 $\left(-4,4\right)$. $\blacksquare$

---

## 11.3-2-8

求 $\sum\left(1+\frac12+\cdots+\frac1n\right)x^n$ 的收敛点集合.

### 解答 11.3-2-8

由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=1$. 端点处 $h_n\to+\infty\ne0$, 发散. 收敛域为 $\left(-1,1\right)$. $\blacksquare$

---

## 11.3-2-10

求 $\sum\frac{\left(-1\right)^n\left(2x+3\right)^n}{n\ln n}$ 的收敛点集合.

### 解答 11.3-2-10

令 $t=2x+3$. 由**定理 3.3 (收敛半径的达朗贝尔公式)**, $R=1$. 端点处发散. 收敛域为 $\left(-2,-1\right)$. $\blacksquare$

---

## 11.3-3-1

求 $\sum\left(n+1\right)x^n$ 的和函数.

### 解答 11.3-3-1

由**定理 3.4 (内闭一致收敛性)**, 逐项求导: $\sum\left(n+1\right)x^n=\frac{\mathrm d}{\mathrm dx}\left(\frac x{1-x}\right)=\frac1{\left(1-x\right)^2}$. $\blacksquare$

---

## 11.3-3-3

求 $\sum n^2x^n$ 的和函数.

### 解答 11.3-3-3

由 $n^2=n\left(n-1\right)+n$ 及**定理 3.4 (内闭一致收敛性)**, 逐项求导两次与一次, 得 $\sum n^2x^n=\frac{x\left(1+x\right)}{\left(1-x\right)^3}$. $\blacksquare$

---

## 11.3-3-5

求 $\sum\frac{x^n}{n\left(n+1\right)}$ 的和函数.

### 解答 11.3-3-5

裂项 $\frac1{n\left(n+1\right)}=\frac1n-\frac1{n+1}$, 利用 $\sum\frac{x^n}n=-\ln\left(1-x\right)$, 得 $1-\frac{1-x}x\ln\left(1-x\right)$. $\blacksquare$

---

## 11.3-3-7

求 $\sum\frac{x^n}n$ 的和函数.

### 解答 11.3-3-7

由**定理 3.4 (内闭一致收敛性)**, 逐项求导得 $\frac{\mathrm d}{\mathrm dx}\sum\frac{x^n}n=\frac1{1-x}$. 积分得 $\sum\frac{x^n}n=-\ln\left(1-x\right)$. $\blacksquare$

---

## 11.3-4

证明: 若 $\sum a_nx^n$ 的收敛半径为 $R$, 则 $\sum a_nx^{2n}$ 的收敛半径为 $\sqrt R$.

### 解答 11.3-4

令 $y=x^2$. 由**定理 3.2 (收敛半径的柯西公式)**, $\sum a_ny^n$ 当 $\left|y\right|< R$ 时收敛, 即 $\left|x\right|< \sqrt R$. $\blacksquare$

---

## 11.3-5

证明: 若收敛半径为 $R$, 则对任意 $A> \frac1R$, 存在 $C> 0$ 使 $\left|a_n\right|\le CA^n$.

### 解答 11.3-5

取 $r$ 满足 $\frac1A< r< R$. 因 $a_nr^n\to0$, 有界, 故 $\left|a_n\right|\le Mr^{-n}$. 取 $C=M\max\left(1,\frac1{rA}\right)$ 即得. $\blacksquare$
