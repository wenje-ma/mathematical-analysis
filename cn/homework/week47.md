# week47

> **基础知识: 瑕积分收敛的定义**<br>若 $\lim_{\eta\to0+}\int_{a+\eta}^b f\left(x\right)\mathrm dx$ 存在, 则称瑕积分 $\int_a^b f\left(x\right)\mathrm dx$ 收敛, 否则发散.

> **基础知识: 绝对收敛与条件收敛的定义**<br>若 $\int_a^b\left|f\left(x\right)\right|\mathrm dx$ 收敛则称绝对收敛; 若 $\int_a^b f\left(x\right)\mathrm dx$ 收敛而 $\int_a^b\left|f\left(x\right)\right|\mathrm dx$ 发散则称条件收敛.

> **基础知识: 柯西主值的定义**<br>若 $\lim_{\eta\to0+}\left[\int_a^{c-\eta}f\left(x\right)\mathrm dx+\int_{c+\eta}^b f\left(x\right)\mathrm dx\right]$ 存在, 则称该瑕积分在柯西主值意义下收敛.

> **例 2.2 (瑕 p-积分)**<br>$\int_a^b\frac{\mathrm dx}{\left(x-a\right)^p}$ 当 $p< 1$ 时收敛, 当 $p\ge1$ 时发散.

---

## 12.2-1-1

判断 $\int_0^1\ln x\mathrm dx$ 的收敛性.

### 解答 12.2-1-1

分部积分得 $-1-\eta\ln\eta+\eta\to-1$. 由**基础知识: 瑕积分收敛的定义**, 收敛且值为 $-1$. $\blacksquare$

---

## 12.2-1-3

判断 $\int_{-1}^1\frac{\mathrm dx}{\sqrt{1-x^2}}$.

### 解答 12.2-1-3

拆为两段, 各趋于 $\frac\pi2$. 收敛且值为 $\pi$. $\blacksquare$

---

## 12.2-1-5

判断 $\int_0^1\frac{\mathrm dx}{x\ln^2x}$.

### 解答 12.2-1-5

代换 $u=\ln x$, 得 $-\frac1{\ln\left(1-\eta\right)}+\frac1{\ln\left(1/2\right)}\to+\infty$. 发散. $\blacksquare$

---

## 12.2-2-1

讨论 $\int_0^{+\infty}\frac{\mathrm dx}{\sqrt x\left(1+x\right)}$.

### 解答 12.2-2-1

在 $x=0$ 附近与 $\frac1{\sqrt x}$ 同阶, 由**例 2.2 (瑕 p-积分)** 收敛; 在 $+\infty$ 与 $\frac1{x^{3/2}}$ 同阶, 收敛. 故收敛, 值为 $\pi$. $\blacksquare$

---

## 12.2-2-3

讨论 $\int_0^{+\infty}\frac{\mathrm dx}{x^p+x^q}$.

### 解答 12.2-2-3

$x=0$ 端收敛当且仅当 $\min\left(p,q\right)< 1$; $+\infty$ 端收敛当且仅当 $\max\left(p,q\right)> 1$. 故收敛当且仅当 $\min\left(p,q\right)< 1< \max\left(p,q\right)$. $\blacksquare$

---

## 12.2-2-5

讨论 $\int_0^{\pi/2}\frac{\mathrm dx}{\sin^2x\cos^2x}$.

### 解答 12.2-2-5

在 $x=0$ 附近与 $\frac1{x^2}$ 同阶, 由**例 2.2 (瑕 p-积分)**, $p=2\ge1$, 发散. $\blacksquare$

---

## 12.2-2-7

讨论 $\int_0^1 x^p\left(1-x\right)^q\mathrm dx$ ($p> 0,q> 0$).

### 解答 12.2-2-7

在 $x=0$ 附近与 $x^p$ 同阶 ($p> 0$ 故收敛); 在 $x=1$ 附近与 $\left(1-x\right)^q$ 同阶 ($q> 0$ 故收敛). 故对一切 $p> 0,q> 0$ 收敛. $\blacksquare$

---

## 12.2-3

证明: 若 $\int_a^b f^2$ 收敛, 则 $\int_a^b f$ 绝对收敛. 反之是否成立?

### 解答 12.2-3

由 $2\left|f\right|\le1+f^2$, 得 $\left|f\right|\le\frac12+\frac{f^2}2$. 由**基础知识: 绝对收敛与条件收敛的定义**, 绝对收敛. 反之不然, 反例 $f\left(x\right)=\frac1{\sqrt x}$. $\blacksquare$

---

## 12.2-4-1

判断 $\int_0^2\frac{\mathrm dx}{x-1}$ 是否在柯西主值意义下收敛.

### 解答 12.2-4-1

由**基础知识: 柯西主值的定义**, $\mathrm{CPV}=\lim_{\eta\to0+}\left(\ln\eta-\ln1+\ln1-\ln\eta\right)=0$. 收敛且主值为 $0$. $\blacksquare$

---

## 12.2-4-2

判断 $\int_{1/2}^2\frac{\mathrm dx}{x\ln x}$ 是否在柯西主值意义下收敛.

### 解答 12.2-4-2

由**基础知识: 柯西主值的定义**, 主值 $=\lim_{\eta\to0+}\ln\frac{-\ln\left(1-\eta\right)}{\ln\left(1+\eta\right)}=\ln1=0$. 收敛且主值为 $0$. $\blacksquare$
