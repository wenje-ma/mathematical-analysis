# week28

> **基础知识: 二重积分的基本性质**<br>(1) 积分对区域的可加性: 若 $D=D_1\cup D_2$ 互不重叠, 则 $\iint_D f=\iint_{D_1}f+\iint_{D_2}f$; (2) 积分保持不等号: 若 $f\le g$, 则 $\iint_D f\le\iint_D g$; (3) 积分中值定理: 若 $f$ 在 $D$ 上连续, 则存在 $\left(x_0,y_0\right)\in D$ 使 $\iint_D f=f\left(x_0,y_0\right)\cdot S$.

> **命题 1.3 (可求面积的充要条件)**<br>$E$ 可求面积的充要条件是 $\partial E$ 为零面积集合. 特别地, 边界为逐段光滑曲线的有界区域可求面积.

> **定理 1.4 (可积的充要条件)**<br>$f$ 在可求面积区域 $D$ 上可积的充要条件是 $\lim_{\lambda\to0}\sum_i\omega_i\Delta\sigma_i=0$.

> **定理 1.5 (连续函数可积)**<br>若 $D$ 是有界闭区域且边界为零面积集合, $f$ 在 $D$ 上连续, 则 $f$ 在 $D$ 上可积.

---

## 8.1-2

设 $f$ 与 $g$ 在有界闭区域 $D$ 上可积. 证明 $f\cdot g$ 在 $D$ 上也可积.

### 解答 8.1-2

因 $f,g$ 均可积, 故均有界. 记 $A=\sup_D\left|f\right|$, $B=\sup_D\left|g\right|$. 对每个小区域 $D_i$,

$$
\omega_{fg}^{\left(i\right)}\le A\omega_g^{\left(i\right)}+B\omega_f^{\left(i\right)}.
$$

求和得 $\sum\omega_{fg}\Delta\sigma_i\le A\sum\omega_g\Delta\sigma_i+B\sum\omega_f\Delta\sigma_i$. 由**定理 1.4 (可积的充要条件)**, 右端趋于 $0$, 故左端亦趋于 $0$. 故 $f\cdot g$ 可积. $\blacksquare$

---

## 8.1-3

设 $D\left(x,y\right)=1$ (当 $x,y$ 均为有理数), $D\left(x,y\right)=0$ (其他). 证明 $D$ 在 $R=\left[0,1\right]\times\left[0,1\right]$ 上不可积.

### 解答 8.1-3

对 $R$ 作任意分割, 每个小区域 $D_i$ 中既含有理点又含无理点. 故 $\omega_i=1$. 于是 $D\left(T\right)-d\left(T\right)=\sum\Delta\sigma_i=1$, 不趋于 $0$. 由**定理 1.4 (可积的充要条件)**, $D$ 不可积. $\blacksquare$

---

## 8.1-4

设 $f=g$ 在 $D\setminus\gamma$ 上, 其中 $\gamma$ 是 $D$ 内部的一条直线段. 证明 $\iint_D f=\iint_D g$.

### 解答 8.1-4

直线段 $\gamma$ 是逐段光滑曲线, 由**命题 1.3 (可求面积的充要条件)**, $\gamma$ 是零面积集合. 由**基础知识: 二重积分的基本性质** (可加性),

$$
\iint_D f=\iint_{D\setminus\gamma}f+\iint_\gamma f=\iint_{D\setminus\gamma}f.
$$

同理 $\iint_D g=\iint_{D\setminus\gamma}g$. 因 $f=g$ 在 $D\setminus\gamma$ 上, 故两者相等. $\blacksquare$

---

## 8.1-5

设 $f$ 在 $D$ 上可积. 证明 $\left|f\right|$ 在 $D$ 上也可积.

### 解答 8.1-5

对每个小区域 $D_i$, 由三角不等式, $\omega_{\left|f\right|}^{\left(i\right)}\le\omega_f^{\left(i\right)}$. 故 $\sum\omega_{\left|f\right|}\Delta\sigma_i\le\sum\omega_f\Delta\sigma_i$. 由**定理 1.4 (可积的充要条件)**, $\left|f\right|$ 可积. $\blacksquare$

---

## 8.1-8

设 $f$ 在 $D$ 上连续, $g$ 在 $D$ 上连续且 $g> 0$. 证明存在 $\left(x_0,y_0\right)\in D$ 使 $\iint_D fg=f\left(x_0,y_0\right)\iint_D g$.

### 解答 8.1-8

因 $f$ 连续, 由**定理 1.5 (连续函数可积)**, $f$ 在 $D$ 上可积, 且有最大值 $M$ 与最小值 $m$. 由 $mg\le fg\le Mg$ 及**基础知识: 二重积分的基本性质** (比较性质),

$$
m\iint_D g\le\iint_D fg\le M\iint_D g.
$$

因 $\iint_D g> 0$, 故 $m\le\frac{\iint_D fg}{\iint_D g}\le M$. 由介值定理, 存在 $\left(x_0,y_0\right)$ 使 $f\left(x_0,y_0\right)=\frac{\iint_D fg}{\iint_D g}$. $\blacksquare$

---

## 8.1-9

设 $f$ 在 $D$ 上连续, 非负, 且 $\iint_D f=0$. 证明 $f\equiv0$.

### 解答 8.1-9

反设存在 $\left(x_0,y_0\right)$ 使 $f\left(x_0,y_0\right)> 0$. 由连续性, 在 $R_\delta$ 内 $f> \frac{f\left(x_0,y_0\right)}2$. 由**基础知识: 二重积分的基本性质** (比较性质),

$$
\iint_D f\ge\iint_{R_\delta}f\ge\frac{f\left(x_0,y_0\right)}2\cdot\left|R_\delta\right|> 0,
$$

矛盾. 故 $f\equiv0$. $\blacksquare$
