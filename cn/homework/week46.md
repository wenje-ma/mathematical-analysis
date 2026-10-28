# week46

> **基础知识: 无穷积分收敛的定义**<br>若 $\lim_{A\to+\infty}\int_a^A f\left(x\right)\mathrm dx$ 存在, 则称 $\int_a^{+\infty}f\left(x\right)\mathrm dx$ 收敛, 否则发散.

> **基础知识: 绝对收敛与条件收敛的定义**<br>若 $\int_a^{+\infty}\left|f\left(x\right)\right|\mathrm dx$ 收敛, 则称绝对收敛; 若 $\int_a^{+\infty}f\left(x\right)\mathrm dx$ 收敛但 $\int_a^{+\infty}\left|f\left(x\right)\right|\mathrm dx$ 发散, 则称条件收敛.

> **定理 1.1 (柯西收敛原理)**<br>$\int_a^{+\infty}f\left(x\right)\mathrm dx$ 收敛的充要条件是: 对任意 $\varepsilon> 0$, 存在 $X> 0$, 使 $\left|\int_{A'}^{A''}f\left(x\right)\mathrm dx\right|< \varepsilon$ ($A',A''> X$).

> **例 1.2 (p-积分)**<br>$\int_1^{+\infty}\frac{\mathrm dx}{x^p}$ 当 $p> 1$ 时收敛, 当 $p\le1$ 时发散.

> **定理 1.3 (比较判别法)**<br>若 $0\le f\left(x\right)\le g\left(x\right)$ ($x\ge X_0$), 则 $\int g$ 收敛蕴含 $\int f$ 收敛, $\int f$ 发散蕴含 $\int g$ 发散.

> **定理 1.6 (狄利克雷判别法)**<br>若 $f\left(x\right)$ 单调趋于零, 且 $\int_a^A g\left(x\right)\mathrm dx$ 对任意 $A$ 有界, 则 $\int_a^{+\infty}f\left(x\right)g\left(x\right)\mathrm dx$ 收敛.

---

## 12.1-1-1

判别 $\int_1^{+\infty}\frac{\ln x}{x^2}\mathrm dx$ 是否收敛, 若收敛求其值.

### 解答 12.1-1-1

分部积分得 $-\frac{\ln A}A+1-\frac1A\to1$. 由**基础知识: 无穷积分收敛的定义**, 收敛且值为 $1$. $\blacksquare$

---

## 12.1-1-2

判别 $\int_1^{+\infty}e^{-ax}\mathrm dx$ ($a> 0$).

### 解答 12.1-1-2

$\frac{e^{-a}-e^{-aA}}a\to\frac{e^{-a}}a$. 收敛. $\blacksquare$

---

## 12.1-1-3

判别 $\int_0^{+\infty}\frac{\mathrm dx}{1+x^2}$.

### 解答 12.1-1-3

$\arctan A\to\frac\pi2$. 收敛. $\blacksquare$

---

## 12.1-1-4

判别 $\int_0^{+\infty}xe^{-x}\mathrm dx$.

### 解答 12.1-1-4

分部积分得 $1$. 收敛. $\blacksquare$

---

## 12.1-2-1

讨论 $\int_1^{+\infty}\frac{\sin x}{x^p}\mathrm dx$ 的绝对收敛性与条件收敛性.

### 解答 12.1-2-1

(1) $p> 1$: 由 $\left|\frac{\sin x}{x^p}\right|\le\frac1{x^p}$ 及**例 1.2 (p-积分)** 与**定理 1.3 (比较判别法)**, 绝对收敛.

(2) $0< p\le1$: 由**定理 1.6 (狄利克雷判别法)**, 收敛. 又 $\frac{\left|\sin x\right|}{x^p}\ge\frac1{2x^p}-\frac{\cos2x}{2x^p}$, 其中 $\int\frac1{x^p}$ 发散, $\int\frac{\cos2x}{x^p}$ 收敛, 故不绝对收敛. 条件收敛.

(3) $p\le0$: 由**定理 1.1 (柯西收敛原理)**, 发散. $\blacksquare$

---

## 12.1-2-3

讨论 $\int_1^{+\infty}\frac{\sqrt x\cos x}{x+3}\mathrm dx$.

### 解答 12.1-2-3

由**定理 1.6 (狄利克雷判别法)**, 收敛. 又 $\frac{\sqrt x\left|\cos x\right|}{x+3}\ge\frac1{8\sqrt x}+\frac{\cos2x}{8\sqrt x}$, 其中 $\int\frac1{\sqrt x}$ 发散, 故不绝对收敛. 条件收敛. $\blacksquare$

---

## 12.1-2-5

讨论 $\int_0^{+\infty}\sin x^2\mathrm dx$.

### 解答 12.1-2-5

代换 $t=x^2$ 得 $\frac12\int_1^{+\infty}\frac{\sin t}{\sqrt t}\mathrm dt$. 由**定理 1.6 (狄利克雷判别法)**, 收敛. 同理不绝对收敛. 条件收敛. $\blacksquare$

---

## 12.1-3

证明 $I_1\left(x\right)=\int_0^{+\infty}e^{-xt}\sin t\mathrm dt$ 与 $I_2\left(x\right)=\int_0^{+\infty}e^{-xt}\cos t\mathrm dt$ 绝对收敛并求值.

### 解答 12.1-3

由 $\left|e^{-xt}\sin t\right|\le e^{-xt}$ 及**定理 1.3 (比较判别法)**, 绝对收敛. 分部积分联立方程解得 $I_1=\frac1{x^2+1}$, $I_2=\frac x{x^2+1}$. $\blacksquare$

---

## 12.1-4

证明 $\int_{-\infty}^{+\infty}f\left(-x\right)\mathrm dx=\int_{-\infty}^{+\infty}f\left(x\right)\mathrm dx$ 及 $\int_{-\infty}^{+\infty}f\left(x+a\right)\mathrm dx=\int_{-\infty}^{+\infty}f\left(x\right)\mathrm dx$.

### 解答 12.1-4

作代换 $u=-x$ 与 $u=x+a$, 由**基础知识: 无穷积分收敛的定义**, 等式成立. $\blacksquare$

---

## 12.1-5

设 $a_n=\int_n^{n+1}f\left(x\right)\mathrm dx$. 证明 $\int_1^{+\infty}f\left(x\right)\mathrm dx$ 收敛当且仅当 $\sum a_n$ 收敛.

### 解答 12.1-5

$\sum_{n=1}^N a_n=\int_1^{N+1}f\left(x\right)\mathrm dx$. 由 $f\left(x\right)\to0$, 相邻整数点之间的积分差趋于零. 由**基础知识: 无穷积分收敛的定义**, 等价成立. $\blacksquare$
