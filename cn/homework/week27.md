# week27

> **基础知识: 定积分的比较性质**<br>设 $f,g$ 在 $\left[a,b\right]$ 上可积, 且 $f\left(x\right)\le g\left(x\right)$, 则 $\int_a^b f\left(x\right)\,\mathrm dx\le\int_a^b g\left(x\right)\,\mathrm dx$.

> **引理 2.1 (分点加密的效应)**<br>设 $T'$ 是由分割 $T$ 增加有限个分点而形成的分割, 则达布小和不减, 达布大和不增.

> **定理 2.2 (可积的充要条件)**<br>设 $f$ 在 $\left[a,b\right]$ 上有界. 则 $f$ 黎曼可积的充要条件是 $\lim_{\lambda\left(T\right)\to0}\left[D\left(T\right)-d\left(T\right)\right]=0$.

---

## 6.2-1

设 $f$ 在 $\left[a,b\right]$ 上可积, 又设 $\left[c,d\right]\subset\left[a,b\right]$. 证明: $f$ 在 $\left[c,d\right]$ 上也可积.

### 解答 6.2-1

任取 $\left[c,d\right]$ 的分割 $T'$. 将 $T'$ 扩充为 $\left[a,b\right]$ 的分割 $T$. 由**引理 2.1 (分点加密的效应)**,

$$
D\left(T'\right)-d\left(T'\right)\le D\left(T\right)-d\left(T\right).
$$

因 $f$ 在 $\left[a,b\right]$ 上可积, 由**定理 2.2 (可积的充要条件)**, 右端趋于 $0$. 故 $D\left(T'\right)-d\left(T'\right)\to0$. 再由**定理 2.2 (可积的充要条件)**, $f$ 在 $\left[c,d\right]$ 上可积. $\blacksquare$

---

## 6.2-2

设 $f$ 与 $g$ 均在 $\left[a,b\right]$ 中可积. 证明: $f\cdot g$ 在 $\left[a,b\right]$ 中可积.

### 解答 6.2-2

因 $f,g$ 均可积, 故均有界. 记 $M=\sup\left|f\right|$, $N=\sup\left|g\right|$. 对每个小区间 $I_k$,

$$
\omega_{fg}\left(I_k\right)\le M\omega_g\left(I_k\right)+N\omega_f\left(I_k\right).
$$

求和得 $\sum\omega_{fg}\Delta x_k\le M\sum\omega_g\Delta x_k+N\sum\omega_f\Delta x_k$. 由**定理 2.2 (可积的充要条件)**, 右端趋于 $0$, 故左端亦趋于 $0$. 故 $f\cdot g$ 可积. $\blacksquare$

---

## 6.2-4

设 $f$ 在 $\left[a,b\right]$ 上连续且 $f\left(x\right)\ge0$. 证明: 当且仅当 $f\equiv0$ 时, $\int_a^b f\left(x\right)\,\mathrm dx=0$.

### 解答 6.2-4

**充分性**: 若 $f\equiv0$, 显然成立.

**必要性**: 反设存在 $x_0$ 使 $f\left(x_0\right)> 0$. 由连续性, 在 $x_0$ 的某邻域 $J$ 内 $f\left(x\right)> \frac{f\left(x_0\right)}2$. 由**基础知识: 定积分的比较性质**,

$$
\int_a^b f\left(x\right)\,\mathrm dx\ge\int_J f\left(x\right)\,\mathrm dx\ge\frac{f\left(x_0\right)}2\cdot\left|J\right|> 0,
$$

矛盾. 故 $f\equiv0$. $\blacksquare$

---

## 6.2-6

证明: 若 $f$ 在 $\left[a,b\right]$ 上可积, 则 $\left|f\right|$ 可积, 且 $\left|\int_a^b f\left(x\right)\,\mathrm dx\right|\le\int_a^b\left|f\left(x\right)\right|\,\mathrm dx$.

### 解答 6.2-6

**可积性**: 对每个小区间 $I_k$, 由三角不等式, $\omega_{\left|f\right|}\left(I_k\right)\le\omega_f\left(I_k\right)$. 故 $\sum\omega_{\left|f\right|}\Delta x_k\le\sum\omega_f\Delta x_k$. 由**定理 2.2 (可积的充要条件)**, $\left|f\right|$ 可积.

**不等式**: 由 $-\left|f\right|\le f\le\left|f\right|$, 及**基础知识: 定积分的比较性质**,

$$
-\int_a^b\left|f\right|\,\mathrm dx\le\int_a^b f\,\mathrm dx\le\int_a^b\left|f\right|\,\mathrm dx,
$$

即 $\left|\int_a^b f\right|\le\int_a^b\left|f\right|$. $\blacksquare$
