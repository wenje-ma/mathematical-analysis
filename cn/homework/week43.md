# week43

> **定理 2.2 (魏尔斯特拉斯 M 判别法)**<br>若 $\left|u_n\left(x\right)\right|\le a_n$ 对一切 $x\in X$ 成立, 且 $\sum a_n$ 收敛, 则 $\sum u_n\left(x\right)$ 在 $X$ 上一致收敛.

> **定理 2.4 (狄利克雷判别法)**<br>若 $\sum a_n\left(x\right)$ 的部分和一致有界, $b_n\left(x\right)$ 单调且一致趋于零, 则 $\sum a_n\left(x\right)b_n\left(x\right)$ 一致收敛.

> **定理 2.5 (和函数的连续性)**<br>若 $u_n\left(x\right)$ 连续且 $\sum u_n\left(x\right)$ 一致收敛, 则和函数 $S\left(x\right)$ 连续.

> **定理 2.7 (逐项求导定理)**<br>若 $\sum u_n\left(x\right)$ 收敛, $u_n'\left(x\right)$ 连续, 且 $\sum u_n'\left(x\right)$ 一致收敛, 则 $S'\left(x\right)=\sum u_n'\left(x\right)$.

---

## 11.2-1-2

讨论 $\sum\frac{\left(-1\right)^{n+1}}{x^2+n}$ 在 $\mathbb R$ 上的一致收敛性.

### 解答 11.2-1-2

令 $a_n=\left(-1\right)^{n+1}$, $b_n=\frac1{x^2+n}$. 部分和一致有界, $b_n$ 单调且 $\left|b_n\right|\le\frac1n\to0$ 一致. 由**定理 2.4 (狄利克雷判别法)**, 一致收敛. $\blacksquare$

---

## 11.2-1-4

讨论 $\sum\frac{x}{\left(1+\left(n-1\right)x\right)\left(1+nx\right)}$ 在 $\left(0,+\infty\right)$ 上的一致收敛性.

### 解答 11.2-1-4

裂项得 $S_N\left(x\right)=1-\frac1{1+Nx}$. 和函数在 $x=0$ 处不连续(右极限为 $1$, 值为 $0$). 由**定理 2.5 (和函数的连续性)**, 若一致收敛则和函数必连续, 矛盾. 故不一致收敛. $\blacksquare$

---

## 11.2-1-6

讨论 $\sum\frac1{n^2+x^2}$ 在 $\left[0,+\infty\right)$ 上的一致收敛性.

### 解答 11.2-1-6

因 $\left|\frac1{n^2+x^2}\right|\le\frac1{n^2}$, 及**定理 2.2 (魏尔斯特拉斯 M 判别法)**, 一致收敛. $\blacksquare$

---

## 11.2-9

讨论 $\sum\left(-1\right)^n\frac{n+x^2}{n^2}$ 在 $\left[a,b\right]$ 及 $\mathbb R$ 上的一致收敛性.

### 解答 11.2-9

(i) 在 $\left[a,b\right]$ 上, $b_n=\frac1n+\frac{x^2}{n^2}$ 单调且 $\le\frac1n+\frac C{n^2}\to0$ 一致. 由**定理 2.4 (狄利克雷判别法)**, 一致收敛.

(ii) 在 $\mathbb R$ 上, $\sup_{x\in\mathbb R}\frac{x^2}{n^2}=+\infty$, 通项不一致趋于零. 故不一致收敛. $\blacksquare$

---

## 11.2-10

讨论 $\sum\left(-1\right)^{n-1}x^2e^{-nx^2}$ 在 $\mathbb R$ 上的一致收敛性.

### 解答 11.2-1-10

令 $t=x^2\ge0$, $\max_{t\ge0}te^{-nt}=\frac1{en}\to0$ 一致. 由**定理 2.4 (狄利克雷判别法)**, 一致收敛. $\blacksquare$

---

## 11.2-11

讨论 $\sum\frac{\sin x\sin nx}{\sqrt{n^2+x^2}}$ 在 $\left[0,2\pi\right]$ 上的一致收敛性.

### 解答 11.2-11

$\sin x\sum_{k=1}^N\sin kx$ 一致有界. $b_n=\frac{\sin x}{\sqrt{n^2+x^2}}\le\frac1n\to0$ 一致. 由**定理 2.4 (狄利克雷判别法)**, 一致收敛. $\blacksquare$

---

## 11.2-5

证明 $f\left(x\right)=\sum2^n\sin\frac x{3^n}$ 在 $\mathbb R$ 上处处有连续的导函数.

### 解答 11.2-5

逐项求导得 $u_n'\left(x\right)=\left(\frac23\right)^n\cos\frac x{3^n}$. 因 $\left|u_n'\left(x\right)\right|\le\left(\frac23\right)^n$, 及**定理 2.2 (魏尔斯特拉斯 M 判别法)**, 求导级数一致收敛. 由**定理 2.7 (逐项求导定理)**, $f'\left(x\right)=\sum\left(\frac23\right)^n\cos\frac x{3^n}$. 由**定理 2.5 (和函数的连续性)**, $f'\left(x\right)$ 连续. $\blacksquare$

---

## 11.2-6

设 $\zeta\left(x\right)=\sum\frac1{n^x}$ ($x> 1$), 证明 $\zeta'\left(x\right)$ 存在并给出表达式.

### 解答 11.2-6

对任意 $a> 1$, 在 $\left[a,+\infty\right)$ 上, $\left|\frac{\ln n}{n^x}\right|\le\frac{\ln n}{n^a}$, 而 $\sum\frac{\ln n}{n^a}$ 收敛. 由**定理 2.2 (魏尔斯特拉斯 M 判别法)** 与**定理 2.7 (逐项求导定理)**, $\zeta'\left(x\right)=-\sum\frac{\ln n}{n^x}$. $\blacksquare$
